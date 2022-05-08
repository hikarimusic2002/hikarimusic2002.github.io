---
layout: splash
title: "Codeforces 1001 ~ 1100"
permalink: /solutions/codeforces_11
author_profile: false
redirect_from:
  - /resume
---

# Codeforces Problems 1001 ~ 1100

### 1025B. Weakened Common Divisor

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long
void factorize(ll n, vector<ll>& fac) {
    if (n%2==0) {
        fac.push_back(2) ;
        while (n%2==0) n/=2 ;
    }
    for (ll i=3;i*i<=n;i+=2) {
        if (n%i!=0) continue ;
        fac.push_back(i) ;
        while (n%i==0) {
            n/=i ;
        }
    }
    if (n>1) fac.push_back(n) ;
}
int main()
{
    ll n, a, b ;
    scanf("%lld %lld %lld",&n,&a,&b) ;
    vector<ll> fac ;
    factorize(a, fac) ;
    factorize(b, fac) ;
    for (int i=0;i<n-1;++i) {
        scanf("%lld %lld",&a,&b) ;
        for (int j=0;j<fac.size();) {
            if (a%fac[j] == 0 || b%fac[j] == 0) {
                j+=1 ;
                continue ;
            }
            fac.erase(fac.begin()+j) ;
        }
    }
    if (fac.size()) printf("%lld",fac[0]) ;
    else printf("-1") ;
    return 0;
}
```

### 1037D. Valid BFS

```cpp
#include <bits/stdc++.h>
using namespace std;
#define n_max 200000
int n ;
vector<vector<int>> g(n_max+5) ;
vector<int> seq ;
vector<int> ord(n_max+5) ;
vector<int> p ;
bool com(int a, int b) {
    return ord[a]<ord[b] ;
}
void bfs(int s) {
    queue<int> q ;
    vector<bool> u(n+1,0) ;
    u[s]=1 ;
    q.push(s) ;
    p.push_back(s) ;
    while (!q.empty()) {
        int v=q.front() ;
        q.pop() ;
        for (int w : g[v]) {
            if (!u[w]) {
                u[w]=1 ;
                q.push(w) ;
                p.push_back(w) ;
            }
        }
    }
}
int main()
{
    scanf("%d",&n) ;
    for (int t=0;t<n-1;++t) {
        int x,y ;
        scanf("%d %d",&x,&y) ;
        g[x].push_back(y) ;
        g[y].push_back(x) ;
    }
    for (int i=0;i<n;++i) {
        int x ;
        scanf("%d",&x) ;
        seq.push_back(x) ;
        ord[x]=i ;
    }
    for (int i=1;i<=n;++i) {
        sort(g[i].begin(),g[i].end(),com) ;
    }
    bfs(1) ;
    bool ans=1 ;
    for (int i=0;i<n;++i) {
        if (p[i]!=seq[i]) {
            ans=0 ;
            break ;
        }
    }
    printf("%s",ans?"Yes":"No") ;
    return 0;
}
```

### 1047C. Enlarge GCD

```cpp
#include <bits/stdc++.h>
using namespace std;
#define n_max 300000 
#define a_max 15000000 
vector<int> lp(a_max+5,0) ;
void lin_sieve(int N) {
    vector<int> pr ;
    for (int i=2;i<=N;++i) {
        if (lp[i]==0) {
            lp[i]=i ;
            pr.push_back(i) ;
        }
        for (int j=0; j<pr.size() && pr[j]<=lp[i] && i*pr[j]<=N; ++j ) {
            lp[i*pr[j]]=pr[j] ;
        }
    }
}
int gcd(int a, int b) {
    if (b==0) return a ;
    return gcd(b,a%b) ;
}
int main()
{
    lin_sieve(a_max) ;
    int n ;
    scanf("%d",&n) ;
    vector<int> a(n) ;
    int g=0 ;
    for (int i=0;i<n;++i) {
        scanf("%d",&a[i]) ;
        g=gcd(a[i],g) ;
    }
    vector<int> fac(a_max+5, 0) ;
    for (int i=0;i<n;++i) {
        a[i]/=g ;
        while (a[i]>1) {
            int x=lp[a[i]] ;
            fac[x]+=1 ;
            while (a[i]%x==0) a[i]/=x ;
        }
    }
    int m=0 ;
    for (int i=0;i<fac.size();++i) {
        m=(fac[i]>m)?fac[i]:m ;
    }
    if (m>0) printf("%d",n-m) ;
    else printf("-1") ;
    return 0;
}
```
