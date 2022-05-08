---
layout: splash
title: "Codeforces 401 ~500"
permalink: /solutions/codeforces_05
author_profile: false
redirect_from:
  - /resume
---

# Codeforces Problems 401 ~500

### 466C. Number of Ways

```cpp
#include <bits/stdc++.h>
using namespace std ;
#define ll long long
#define MAXN 500005

ll n, s[MAXN] ;

int main() {
    scanf("%lld",&n) ;
    ll a ;
    for (int i=1;i<=n;++i) {
        scanf("%lld",&a) ;
        s[i]=s[i-1]+a ;
    }
    if (s[n]%3!=0) printf("%d",0) ;
    else {
        ll q1=s[n]/3 ,q2=s[n]*2/3 ;
        ll cnt=0, ans=0 ;
        for (int i=1;i<n;++i) {
            if (s[i]==q2) ans+=cnt ;
            if (s[i]==q1) cnt+=1 ;
        }
        printf("%lld",ans) ;
    }
    return 0 ;
}

```

### 474F. Ant colony

```cpp
#include <bits/stdc++.h>
using namespace std;
#define MAXN 100005
#define pii pair<int,int>

int n, t, s[MAXN] ;

struct T {
    int L, R ;
    pii gcd ;
} tree[MAXN*4] ;

pii combine(pii a, pii b) {
    int G=__gcd(a.first,b.first) ;
    int N=0 ;
    if (G==a.first) N+=a.second ;
    if (G==b.first) N+=b.second ;
    return {G,N} ;
}

void build(int v, int l, int r) {
    tree[v].L=l ;
    tree[v].R=r ;
    if (l==r) {
        tree[v].gcd={s[l],1} ;
        return ;
    }
    build(2*v, l, (l+r)/2) ;
    build(2*v+1, (l+r)/2+1, r) ;
    tree[v].gcd=combine(tree[2*v].gcd,tree[2*v+1].gcd) ;
}

pii query(int v, int l, int r) {
    if (tree[v].L>r || tree[v].R<l) return {0,0} ;
    if (tree[v].L>=l && tree[v].R<=r) return tree[v].gcd ;
    return combine(query(2*v,l,r),query(2*v+1,l,r)) ;
}

int main()
{
    scanf("%d",&n) ;
    for (int i=1;i<=n;++i) scanf("%d",&s[i]) ;
    build(1,1,n) ;
    scanf("%d",&t) ;
    while (t--) {
        int l,r ;
        scanf("%d %d",&l,&r) ;
        printf("%d\n",r-l+1-query(1,l,r).second) ;
    }
    return 0;
}

```

### 475D. CGCDSSQ

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long
#define nmax 100005
#define pmax 20

int n,q ;
ll a[nmax] ;
ll st[nmax][pmax] ;
unordered_map<ll,ll> ans ;

ll gcd(ll a,ll b) {
    return (b==0) ? a : gcd(b,a%b) ;
}

void st_build() {
    int k= (int)log2(n) ;
    for (int i=0;i<n;++i) st[i][0]=a[i] ;
    for (int j=1;j<=k;++j) {
        for (int i=0;i+(1<<j)<=n;++i) {
            st[i][j]=gcd(st[i][j-1], st[i+(1<<(j-1))][j-1] ) ;
        } 
    }
}

ll st_quiry(ll L, ll R) {
    int j= (int)log2(R-L+1) ;
    return gcd(st[L][j], st[R-(1<<j)+1][j] ) ;
}

void ans_count() {
    ll L, R1, R2 ;
    for (L=0;L<n;++L) {
        R1=L ;
        while (R1<n) {
            ll now=st_quiry(L,R1) ;
            ll low=R1, high=n-1, mid ;
            while (low<=high) {
                mid=(low+high)/2 ;
                if (st_quiry(L,mid)==now) {
                    R2=mid ;
                    low=mid+1 ;
                }
                else high=mid-1 ;
            }
            ans[now]+=R2-R1+1 ;
            R1=R2+1 ;
        }
    }
}

int main()
{
    scanf("%d",&n) ;
    for (int i=0;i<n;++i) scanf("%lld",&a[i]) ;
    st_build() ;
    ans_count() ;
    scanf("%d",&q) ;
    for (int i=0;i<q;++i) {
        ll x ;
        scanf("%lld",&x) ;
        printf("%lld\n",ans[x]) ;
    }
    return 0;
}

```

### 500A. New Year Transportation

```cpp
#include <bits/stdc++.h>
using namespace std ;
#define MAXN 30005

int n,t ;
int a[MAXN] ;

int main() {
    scanf("%d %d",&n,&t) ;
    for (int i=1;i<=n-1;++i) scanf("%d",&a[i]) ;
    int c=1 ;
    while (c<t) c+=a[c] ;
    printf("%s",(c==t)?"YES":"NO") ;
    return 0 ;
}

```

