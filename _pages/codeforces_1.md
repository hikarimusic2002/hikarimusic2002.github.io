---
layout: splash
title: "Codeforces"
permalink: /solutions/codeforces_1
author_profile: false
redirect_from:
  - /resume
---

# Codeforces Problems 1 ~ 100

### 1B. Spreadsheets

```cpp
#include <bits/stdc++.h>
using namespace std;

int n ;
string str ;

int main()
{
    cin>>n ;
    for (int t=0;t<n;++t) {
        cin>>str ;
        int k=1 ;
        int len=str.length() ;
        while (k<len && isdigit(str[k]) ) {
            ++k ;
        }
        if (k==1 || k==len) {
            int m=0, col=0 ;
            while (isalpha(str[m]) ) {
                col=col*26+str[m]-'A'+1 ;
                ++m ;
            }
            string ans='R'+str.substr(m,len-m) ;
            ans+='C'+to_string(col) ;
            cout<<ans<<'\n' ;
        }
        else {
            int row=0 ;
            for (int i=k+1;i<len;++i) {
                row=row*10+str[i]-'0' ;
            }
            string temp ;
            while (row>0) {
                temp+=(row-1)%26+'A' ;
                row=(row-1)/26 ;
            }
            reverse(temp.begin(),temp.end()) ;
            string ans=temp+str.substr(1,k-1) ;
            cout<<ans<<'\n' ;
        }
    }
    return 0;
}

```

### 1C. Ancient Berland Circus

```cpp
#include <bits/stdc++.h>
using namespace std;
#define PI acos(-1)
#define EPS 0.001

double x[3],y[3],dis[3],ang[3] ;

bool feq(double a, double b) {
    return fabs(a-b)<EPS ;
}

double fgcd(double a, double b) {
    if (feq(a,0)) return b ;
    if (feq(b,0)) return a ;
    return fgcd(b,fmod(a,b)) ;
}

int main()
{
    for (int i=0;i<3;++i) scanf("%lf %lf",&x[i],&y[i]) ;
    for (int i=0;i<3;++i) {
        double dx=x[i]-x[(i+1)%3] ;
        double dy=y[i]-y[(i+1)%3] ;
        dis[i]=sqrt(dx*dx+dy*dy) ;
    }
    for (int i=0;i<3;++i) {
        double a=dis[i] ;
        double b=dis[(i+1)%3] ;
        double c=dis[(i+2)%3] ;
        ang[i]=2*acos((b*b+c*c-a*a)/(2*b*c)) ;
    }
    double min_ang=fgcd(ang[0],fgcd(ang[1],ang[2])) ;
    double R=dis[0]/(2*sin(ang[0]/2)) ;
    double ans=(2*PI/min_ang)*R*R*sin(min_ang)/2 ;
    printf("%.8lf",ans) ;
    return 0;
}
```

### 7C. Line

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long

ll exgcd(ll a, ll b, ll& x, ll& y) {
    if (b==0) {
        x=1 ;
        y=0 ;
        return a ;
    }
    ll x1, y1, g ;
    g=exgcd(b,a%b,x1,y1) ;
    x=y1 ;
    y=x1-y1*(a/b) ;
    return g ;
}

int main()
{
    ll A,B,C ;
    scanf("%lld %lld %lld",&A,&B,&C) ;
    ll g,x,y ;
    g=exgcd(A,B,x,y) ;
    if (C%g==0) printf("%lld %lld",-x*C/g,-y*C/g) ;
    else printf("%d",-1) ;
    return 0;
}

```

### 10C. Digital Root

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long

ll N, a[9], ans ;

int main()
{
    scanf("%lld",&N) ;
    for (int i=1;i<=N;++i) {
        a[i%9]+=1 ;
    }
    for (int i=0;i<9;++i) {
        for (int j=0;j<9;++j) {
            ans+=a[i]*a[j]*a[i*j%9] ;
        }
    }
    for (int i=1;i<=N;++i) {
        ans-=N/i ;
    }
    printf("%lld",ans) ;
    return 0;
}

```

### 14D. Two Paths

```cpp
#include <bits/stdc++.h>
using namespace std ;
#define MAXN 205

int n ;
vector<vector<int>> g(MAXN) ;
int sum ;

int dfs(int u, int f, int a, int b) {
    int l1=0, l2=0 ;
    for (int v : g[u]) {
        if (v==f) continue ;
        if (u==a && v==b) continue ;
        if (u==b && v==a) continue ;
        int l=1+dfs(v,u,a,b) ;
        if (l>l1) l2=l1, l1=l ;
        else if (l>l2) l2=l ;
    }
    sum=max(sum,l1+l2) ;
    return l1 ;
}

int main() {
    scanf("%d",&n) ;
    for (int i=0;i<n-1;++i) {
        int a,b ;
        scanf("%d %d",&a,&b) ;
        g[a].push_back(b) ;
        g[b].push_back(a) ;
    }
    int ans=0 ;
    for (int i=1;i<=n;++i) {
        for (int j : g[i]) {
            int a,b ;
            if (j<i) continue ;
            sum=0, dfs(i,0,i,j), a=sum ;
            sum=0, dfs(j,0,i,j), b=sum ;
            ans=max(ans,a*b) ;
        }
    }
    printf("%d",ans) ;
}

```

### 16C. Monitor

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long

ll a,b,x,y ;

ll gcd(ll a, ll b) {
    return ( b ? gcd(b,a%b) : a ) ;
}

int main()
{
    scanf("%lld %lld %lld %lld",&a,&b,&x,&y) ;
    ll g=gcd(x,y) ;
    x/=g ;
    y/=g ;
    ll k=min(a/x,b/y) ;
    printf("%lld %lld",x*k,y*k) ;
    return 0;
}

```


