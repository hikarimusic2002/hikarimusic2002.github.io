---
layout: splash
title: "Codeforces 901 ~ 1000"
permalink: /solutions/codeforces_10
author_profile: false
redirect_from:
  - /resume
---

# Codeforces Problems 901 ~ 1000

### 919E. Congruence Equation

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
    ll x1, y1 ;
    ll g=exgcd(b,a%b,x1,y1) ;
    x=y1 ;
    y=x1-(a/b)*y1 ;
    return g ;
}
int main()
{
    ll a,b,p,x ;
    scanf("%lld %lld %lld %lld",&a,&b,&p,&x) ;
    ll ans=0, a0=1 ;
    for (ll i=1;i<=p-1;++i) {
        a0=a0*a%p ;
        ll t=i*a0%p ;
        ll r=x/(p-1) ;
        r += (i <= x%(p-1) ) ? 1 : 0 ;
        ll k, m ;
        exgcd(a0,p,k,m) ;
        k*=b ;
        k=(((i+1-k)%p)+p)%p ;
        if (k==0) k=p ;
        if (r>=k) ans += 1+(r-k)/p ;
    }
    printf("%lld",ans) ;
    return 0;
}
```

### 954D. Fight Against Traffic

```cpp
#include <bits/stdc++.h>
using namespace std;
#define n_max 1000
int n,m,s,t ;
vector<vector<int>> g(n_max+5) ;
vector<int> ds(n_max+5) ;
vector<bool> vis(n_max+5) ;
vector<int> dt(n_max+5) ;
void bfs(int src, vector<int>& d) {
    queue<int> q ;
    vis[src]=1 ;
    d[src]=0 ;
    q.push(src) ;
    while (!q.empty()) {
        int v=q.front() ;
        q.pop() ;
        for (int u : g[v]) {
            if (!vis[u]) {
                d[u]=d[v]+1 ;
                vis[u]=1 ;
                q.push(u) ;
            }
        }
    }
}
bool valid(int i, int j) {
    for (int v : g[i]) {
        if (v==j) return 0 ;
    }
    if (ds[i]+dt[j]+1<ds[t]) return 0 ;
    if (ds[j]+dt[i]+1<ds[t]) return 0 ;
    return 1 ;
}
int main()
{
    scanf("%d %d %d %d",&n,&m,&s,&t) ;
    for (int i=0;i<m;++i) {
        int u,v ;
        scanf("%d %d",&u,&v) ;
        g[u].push_back(v) ;
        g[v].push_back(u) ;
    }
    vis.assign(n_max+5,0) ;
    bfs(s,ds) ;
    vis.assign(n_max+5,0) ;
    bfs(t,dt) ;
    int ans=0 ;
    for (int i=1;i<=n;++i) {
        for (int j=i+1;j<=n;++j) {
            if (valid(i,j)) ++ans ;
        }
    }
    printf("%d",ans) ;
    return 0;
}
```
