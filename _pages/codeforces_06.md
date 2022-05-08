---
layout: splash
title: "Codeforces 501 ~600"
permalink: /solutions/codeforces_06
author_profile: false
redirect_from:
  - /resume
---

# Codeforces Problems 501 ~600

### 514C. Watto and Mechanism

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long
#define lmax 600005
#define p 5
#define mod 10000000000000061

int n,m ;
string s ;
vector<ll> ppow (lmax,0) ;
set<ll> myset ;

void get_pow() {
    ppow[0]=1 ;
    for (int i=1;i<lmax;++i) {
        ppow[i]=ppow[i-1]*p%mod ;
    }
}

ll get_hash(string& s) {
    ll ans=0 ;
    ll len=s.length() ;
    for (int i=0;i<len;++i) {
        ans+=(s[i]-'a'+1)*ppow[i] ;
        ans%=mod ;
    }
    return ans ;
}

int main()
{
    get_pow() ;
    scanf("%d %d",&n,&m) ;
    for (int t=0;t<n;t++) {
        cin>>s ;
        myset.insert(get_hash(s)) ;
    }
    for (int t=0;t<m;++t) {
        cin>>s ;
        bool flag=false ;
        ll val=get_hash(s) ;
        ll len=s.length() ;
        for (ll i=0;i<len;++i) {
            for (ll j=0;j<3;++j) {
                ll c='a'+j-s[i] ;
                if (c==0) continue ;
                ll x=((val+c*ppow[i])%mod+mod)%mod ;
                if (myset.count(x)) {
                    flag=true ;
                    break ;
                }
            }
            if (flag==true) break ;
        }
        printf("%s\n",flag?"YES":"NO") ;
    }
    return 0;
}
```

### 520B. Two Buttons

```cpp
#include <bits/stdc++.h>
using namespace std ;

int n,m ;

int main() {
    scanf("%d %d",&n,&m) ;
    int c=0 ;
    while (m>n) {
        if (m&1) {
            m+=1 ;
            c++ ;
        }
        m/=2 ;
        c++ ;
    }
    c+=(n-m) ;
    printf("%d",c) ;
    return 0 ;
}
```

### 580C. Kefa and Park

```cpp
#include <bits/stdc++.h>
using namespace std ;
#define MAXN 100005

int n,m,ans ;
vector<vector<int>> g(MAXN) ;
vector<int> c(MAXN) ;

void dfs (int u, int v, int s) {
    int ss=(c[u]==1)?(s+1):0 ;
    if (ss>m) return ;
    for (int w : g[u]) {
        if (w!=v) dfs(w,u,ss) ;
    }
    if (u!=1 && g[u].size()==1) ans++ ;
}

int main() {
    scanf("%d %d",&n,&m) ;
    for (int i=1;i<=n;++i) {
        scanf("%d",&c[i]) ;
    }
    for (int i=0;i<n-1;++i) {
        int a, b;
        scanf("%d %d",&a,&b) ;
        g[a].push_back(b) ;
        g[b].push_back(a) ;
    }
    dfs(1,0,0) ;
    printf("%d",ans) ;
    return 0 ;
}
```

### 584D. Dima and Lisa

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long

bool is_prime(ll n) {
    for (int i=2;i*i<=n;++i) {
        if (n%i==0) return false ;
    }
    return true ;
}

int main()
{
    ll n ;
    scanf("%lld",&n) ;
    if (is_prime(n)) printf("1\n%lld",n) ;
    else if (is_prime(n-2)) printf("2\n%lld 2",n-2) ;
    else if (is_prime(n-4)) printf("3\n%lld 2 2",n-4) ;
    else {
        ll a=n-6, b=3 ;
        while (a){
            if (is_prime(a)) break ;
            a-=2 ;
        }
        while (b) {
            if (is_prime(b) && is_prime(n-a-b)) {
                printf("3\n%lld %lld %lld",a,b,n-a-b) ;
                break ;
            }
            b+=2 ;
        }
    }
    return 0;
}
```

