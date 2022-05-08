---
layout: splash
title: "Codeforces 201 ~300"
permalink: /solutions/codeforces_03
author_profile: false
redirect_from:
  - /resume
---

# Codeforces Problems 201 ~300

### 222E. Decoding Genome

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long
#define mod 1000000007
#define m_max 52

ll n,m,k ;
vector<vector<ll>> MA(m_max+5,vector<ll>(m_max+5,1)) ;
vector<vector<ll>> MS(m_max+5,vector<ll>(m_max+5,0)) ;

int asc (char c) {
    int x=(int) c-'a'+1 ;
    if (x<0) return x+32+26 ;
    return x ;
}

void mat_mul(vector<vector<ll>>& A, vector<vector<ll>>& B) {
    vector<vector<ll>> C(m_max+5,vector<ll>(m_max+5,0)) ;
    for (int i=1;i<=m;++i) {
        for (int j=1;j<=m;++j) {
            for (int k=1;k<=m;++k) {
                C[i][j]=(C[i][j]+(A[i][k]*B[k][j]%mod) )%mod ;
            }
        }
    }
    for (int i=1;i<=m;++i) {
        for (int j=1;j<=m;++j) {
            A[i][j]=C[i][j] ;
        }
    }
}

void mat_pow(vector<vector<ll>>& A, ll n) {
    vector<vector<ll>> B(m_max+5,vector<ll>(m_max+5,0)) ;
    for (int i=1;i<=m_max;++i) {
        B[i][i]=1 ;
    }
    while (n>0) {
        if (n&1) mat_mul(B,A) ;
        mat_mul(A,A) ;
        n=n>>1 ;
    }
    for (int i=1;i<=m;++i) {
        for (int j=1;j<=m;++j) {
            A[i][j]=B[i][j] ;
        }
    }
}

int main()
{
    cin>>n>>m>>k ;
    for (ll i=1;i<=k;++i) {
        string in ;
        cin>>in ;
        MA[asc(in[0])][asc(in[1])]=0 ;
    }
    MS[1].assign(m_max+5,1) ;
    mat_pow(MA,n-1) ;
    mat_mul(MS,MA) ;
    ll ans=0 ;
    for (int i=1;i<=m;++i) {
        ans=(ans+MS[1][i])%mod ;
    }
    cout<<ans ;
    return 0;
}
```

### 242C. King's Path

{% raw %}
```cpp
#include <bits/stdc++.h>
using namespace std;

map<pair<int,int>, bool> mp ;

int bfs (pair<int,int> a, pair<int,int> b) {
    map<pair<int,int>,int> d ;
    map<pair<int,int>,bool> u ;
    queue<pair<int,int>> q ;
    d[a]=0 ;
    u[a]=1 ;
    q.push(a) ;
    int dir[8][2]={{1,0},{-1,0},{0,1},{0,-1},{1,1},{1,-1},{-1,1},{-1,-1}} ;
    while (!q.empty()) {
        pair<int,int> x=q.front() ;
        q.pop() ;
        for (int i=0;i<8;++i) {
            pair<int,int> y=make_pair(x.first+dir[i][0], x.second+dir[i][1]) ;
            if (mp[y] && !u[y]) {
                d[y]=d[x]+1 ;
                u[y]=1 ;
                q.push(y) ;
            }
        }
    }
    return (u[b] ? d[b] : -1 ) ;
}

int main()
{
    int x0,y0,x1,y1,n ;
    scanf("%d %d %d %d %d",&x0,&y0,&x1,&y1,&n) ;
    mp[make_pair(x0,y0)]=1 ;
    mp[make_pair(x1,y1)]=1 ;
    for (int i=0;i<n;++i) {
        int r,a,b ;
        scanf("%d %d %d",&r,&a,&b) ;
        for (int j=a;j<=b;++j) {
            mp[make_pair(r,j)]=1 ;
        }
    }
    printf("%d",bfs(make_pair(x0,y0),make_pair(x1,y1)) ) ;
    return 0;
}
```
{% endraw %}

### 257C. View Angle

```cpp
#include <bits/stdc++.h>
using namespace std;
#define PI acos(-1)

int n ;
vector<double> a ;

int main()
{
    scanf("%d",&n) ;
    for (int i=0;i<n;++i) {
        double x,y ;
        scanf("%lf %lf",&x,&y) ;
        a.push_back(atan2(y,x)) ;
    }
    sort(a.begin(),a.end()) ;
    a.push_back(a[0]+2*PI) ;
    double ans=2*PI ;
    for (int i=0;i<n;++i) {
        ans=min(ans,2*PI-(a[i+1]-a[i])) ;
    }
    printf("%.10lf",ans*180/PI) ;
    return 0;
}
```

### 281A. Word Capitalization

```cpp
#include <bits/stdc++.h>
using namespace std ;

string s ;

int main() {
    cin>>s ;
    if (s[0]>=97) s[0]-=32 ;
    cout<<s ;
    return 0 ;
}
```

### 300C. Beautiful Numbers

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long
#define mod 1000000007
#define n_max 1000000

void cal_fac(vector<ll>& fac) {
    for (int i=2;i<=n_max;++i) {
        fac[i]=i*fac[i-1] % mod ;
    }
}

bool is_good(ll n, ll a, ll b) {
    while (n) {
        if (n%10!=a && n%10!=b) return false ;
        n/=10 ;
    }
    return true ;
}

ll inv(ll a) {
    ll n=mod-2 ;
    ll ans=1 ;
    while (n) {
        if (n&1) {
            ans*=a ;
            ans%=mod ;
        }
        a*=a ;
        a%=mod ;
        n>>=1 ;
    }
    return ans ;
}

int main()
{
    vector<ll> fac(n_max+5,1) ;
    cal_fac(fac) ;
    ll a,b,n, ans=0 ;
    scanf("%lld %lld %lld",&a,&b,&n) ;
    for (ll i=0;i<=n;++i) {
        if (is_good(i*a+(n-i)*b, a, b)) {
            ans+=fac[n]*inv(fac[n-i]*fac[i]%mod) % mod ;
            ans%=mod ;
        }
    }
    printf("%lld",ans) ;
    return 0;
}
```

