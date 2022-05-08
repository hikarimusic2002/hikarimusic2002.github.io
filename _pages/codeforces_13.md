---
layout: splash
title: "Codeforces 1201 ~ 1300"
permalink: /solutions/codeforces_13
author_profile: false
redirect_from:
  - /resume
---

# Codeforces Problems 1201 ~ 1300

### 1244C. The Football Season

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long

ll gcd(ll a, ll b, ll& x, ll& y) {
    if (b==0) {
        x=1 ;
        y=0 ;
        return a ;
    }
    ll g,x1,y1 ;
    g=gcd(b,a%b,x1,y1) ;
    x=y1 ;
    y=x1-(a/b)*y1 ;
    return g ; 
}

int main() 
{
    ll n,p,w,d ;
    scanf("%lld %lld %lld %lld",&n,&p,&w,&d) ;
    ll g,x0,y0 ;
    g=gcd(w,d,x0,y0) ;
    if (p%g==0) {
        ll x,y,m ;
        m=w/g ;
        y=( (y0%m)*((p/g)%m)%m+m)%m ;
        x=(p-y*d)/w ;
        if (x>=0 && y>=0 && x+y<=n) {
            printf("%lld %lld %lld",x,y,n-x-y) ;
            return 0 ;
        }
    }
    printf("-1") ;
    return 0 ;
}
```

### 1295D Same GCDs

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long

ll gcd (ll a, ll b) {
    return b ? gcd(b,a%b) : a ;
}

ll phi (ll n) {
    ll ans=n ;
    for (ll i=2;i*i<=n;++i) {
        if (n%i==0) {
            ans-=ans/i ;
            while (n%i==0) n/=i ;
        }
    }
    if (n>1) {
        ans-=ans/n ;
    }
    return ans ;
}

int main()
{
    int T ;
    scanf("%d",&T) ;
    for (int i=0;i<T;++i) {
        ll a, m, g ;
        scanf("%lld %lld",&a,&m) ;
        g=gcd(a,m) ;
        cout<<phi(m/g)<<'\n' ;
    }
    return 0;
}
```


