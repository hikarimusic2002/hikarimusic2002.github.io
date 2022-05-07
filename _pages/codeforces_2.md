---
layout: splash
title: "Codeforces"
permalink: /solutions/codeforces_2
author_profile: false
redirect_from:
  - /resume
---

# Codeforces Problems 101 ~ 200

### 111B. Petya and Divisors

```cpp
#include <bits/stdc++.h>
using namespace std;
#define n_max 100000

int d[n_max+5] ;

int main()
{
    int n,x,y ;
    scanf("%d",&n) ;
    for (int i=1;i<=n;++i) {
        int ans=0 ;
        scanf("%d %d",&x,&y) ;
        for (int k=1;k*k<=x;++k) {
            if (x%k==0) {
                if ( (i-y)>d[k] ) ++ans ;
                if ( k*k!=x && (i-y)>d[x/k] ) ++ans ; 
                d[k]=d[x/k]=i ;
            }
        }
        printf("%d\n",ans) ;
    }
    return 0;
}

```

112A. Petya and Strings

```cpp
//Codeforces 112A - Petya and Strings

#include <bits/stdc++.h>
using namespace std ;

string a,b ;

int main() {
    cin>>a>>b ;
    int t=0 ;
    for (int i=0;i<a.length();++i) {
        if (a[i]<97) a[i]+=32 ;
        if (b[i]<97) b[i]+=32 ;
        if (a[i]<b[i]) {
            t=-1 ;
            break ;
        }
        if (a[i]>b[i]) {
            t=1 ;
            break ;
        }
    }
    cout<<t ;
    return 0 ;
}

```

### 115A. Party

```cpp
#include <bits/stdc++.h>
using namespace std ;
#define MAXN 2005

int n,ans ;
vector<vector<int>> g(MAXN) ;
bool vis[MAXN] ;

void dfs(int u, int l) {
    vis[u]=1 ;
    ans=max(ans,l+1) ;
    for (int v : g[u]) dfs(v,l+1) ;
}

int main() {
    cin>>n ;
    for (int i=1;i<=n;++i) {
        int j ;
        cin>>j ;
        if (j!=-1) g[j].push_back(i) ;
    }
    for (int i=1;i<=n;++i) {
        if (!vis[i]) dfs(i,0) ;
    }
    cout<<ans ;
    return 0 ;
}

```

### 117B. Very Interesting Game

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long

ll a, b, mod ;

void prst(ll n) {
    ll k=100000000 ;
    for (int i=0;i<9;++i) {
        printf("%lld",(n/k)%10) ;
        k/=10 ;
    }
}

int main()
{
    scanf("%lld %lld %lld",&a,&b,&mod) ;
    bool win=0 ;
    ll i ;
    for (i=0;i<=a && i<mod;++i) {
        if ( b< ((mod-i*1000000000%mod)%mod+mod)%mod ) {
            win=1 ;
            break ;
        }
    }
    if (win) {
        printf("%d ",1) ;
        prst(i) ;
    }
    else printf("%d",2) ;
    return 0;
}

```

### 118A. A String Task

```cpp
#include <bits/stdc++.h>
using namespace std ;

string s ;

int main() {
    cin>>s ;
    for (int i=0;i<s.length();++i) {
        char c=s[i] ;
        if (c<97) c+=32 ;
        if (c=='a'||c=='o'||c=='y'||c=='e'||c=='u'||c=='i') continue ;
        cout<<'.'<<c ;
    }
    return 0 ;
}

```

### 131A. cAPS lOCK

```cpp
#include <bits/stdc++.h>
using namespace std ;

string s ;

int main() {
    cin>>s ;
    bool b=1 ;
    for (int i=1;i<s.length();++i) {
        if (s[i]>=97) {
            b=0 ;
            break ;
        }
    }
    if (b) {
        s[0]+=(s[0]<97)?(32):(-32) ;
        for (int i=1;i<s.length();++i) {
            s[i]+=32 ;
        }
    }
    cout<<s ;
    return 0 ;
}

```

### 140A. New Year Table

```cpp
#include <bits/stdc++.h>
using namespace std;
#define PI acos(-1)

double n,R,r ;

double round_6 (double a) {
    return round(a*1000000)/1000000 ;
}

int main()
{
    scanf("%lf %lf %lf",&n,&R,&r) ;
    if (r<=R/2) {
        double m=round_6(PI/asin(r/(R-r))) ;
        printf("%s",(n<=m)?"YES":"NO") ;
    }
    if (r>R/2 && r<=R) {
        printf("%s",(n<=1)?"YES":"NO") ;
    }
    if (r>R) printf("%s","NO") ;
    return 0;
}

```

### 154B. Colliders

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long
#define n_max 100000

vector<bool> pr(n_max+5,1) ;
vector<int> prime ;

void sieve() {
    pr[0]=pr[1]=0 ;
    for (int i=2;i<=n_max;++i) {
        if (pr[i]) {
            prime.push_back(i) ;
            for (ll j=(ll)i*i;j<=n_max;j+=i) pr[j]=0 ;
        }
    }
}

void factorize(int n, vector<int>& fac) {
    for (int i : prime) {
        if (i*i>n) break ;
        if (n%i==0) {
            fac.push_back(i) ;
            while (n%i==0) n/=i ;
        }
    }
    if (n>1) fac.push_back(n) ;
}

int main()
{
    sieve() ;
    int n,m ;
    cin>>n>>m ;
    vector<bool> on(n+1,0) ;
    vector<int> act(n+1,0) ;
    for (int t=0;t<m;++t) {
        char pm ;
        int num ;
        cin>>pm>>num ;
        vector<int> fac ;
        factorize(num,fac) ;
        if (pm=='+') {
            if (on[num]) printf("Already on\n") ;
            else {
                int con=0 ;
                for (int i : fac) {
                    if (act[i]) {
                        con=act[i] ;
                        break ;
                    }
                }
                if (con) printf("Conflict with %d\n",con) ;
                else {
                    printf("Success\n") ;
                    on[num]=1 ;
                    for (int i : fac) act[i]=num ;
                }
            }
        }
        if (pm=='-') {
            if (!on[num]) printf("Already off\n") ;
            else {
                printf("Success\n") ;
                on[num]=0 ;
                for (int i : fac) act[i]=0 ;
            }
        }
    }
    return 0;
}

```


