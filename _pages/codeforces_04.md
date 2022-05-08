---
layout: splash
title: "Codeforces 301 ~400"
permalink: /solutions/codeforces_04
author_profile: false
redirect_from:
  - /resume
---

# Codeforces Problems 301 ~400

### 339A. Helpful Maths

```cpp
#include <bits/stdc++.h>
using namespace std ;

string s ;
int a[4] ;
int main() {
    cin>>s ;
    for (int i=0;i<s.length();++i) {
        if (s[i]=='+') continue ;
        a[s[i]-'0']++ ;
    }
    string ss ;
    for (int i=1;i<=3;++i) {
        for (int j=0;j<a[i];++j) {
            ss.append(to_string(i)+"+") ;
        }
    }
    cout<<ss.substr(0,ss.length()-1) ;
    return 0 ;
}

```

### 339D. Xenia and Bit Operations

```cpp
#include <bits/stdc++.h>
using namespace std;
#define MAXN 1000000

int n,m ;
int a[MAXN], t[4*MAXN] ;

void build(int v, int tl, int tr, bool f) {
    if (tl==tr) t[v]=a[tl] ;
    else {
        int tm=(tl+tr)/2 ;
        build(v*2, tl, tm, f^1) ;
        build(v*2+1, tm+1, tr, f^1) ;
        t[v]= f ? (t[v*2]|t[v*2+1]) : (t[v*2]^t[v*2+1]) ;
    }
}

void update(int v, int tl, int tr, bool f, int pos, int val) {
    if (tl==tr) t[v]=val ;
    else {
        int tm=(tl+tr)/2 ;
        if (pos<=tm) update(v*2,tl,tm,f^1,pos,val) ;
        else update(v*2+1,tm+1,tr,f^1,pos,val) ;
        t[v]= f ? (t[v*2]|t[v*2+1]) : (t[v*2]^t[v*2+1]) ;
    }
}

int main()
{
    scanf("%d %d",&n,&m) ;
    int N=(1<<n) ;
    for (int i=0;i<N;++i) scanf("%d",&a[i]) ;
    build(1,0,N-1,n&1) ;
    for (int i=0;i<m;++i) {
        int p,b ;
        scanf("%d %d",&p,&b) ;
        update(1,0,N-1,n&1,p-1,b) ;
        printf("%d\n",t[1]) ;
    }
    return 0;
}

```

### 380C. Sereja and Brackets

```cpp
#include <bits/stdc++.h>
using namespace std;
#define MAXN 1000005

char s[MAXN] ;
int n, m ;

struct T {
    int L, R ;
    int cor, opn, cls ;
} tree[MAXN*4] ;

T combine(T a, T b) {
    T c ;
    c.L=a.L ;
    c.R=b.R ;
    int t=min(a.opn, b.cls) ;
    c.cor=a.cor+b.cor+2*t ;
    c.opn=a.opn+b.opn-t ;
    c.cls=a.cls+b.cls-t ;
    return c ;
}

void build(int v, int l, int r) {
    tree[v].L=l ;
    tree[v].R=r ;
    if (l==r) {
        tree[v].cor=0 ;
        tree[v].opn= (s[l]=='(') ? 1 : 0 ;
        tree[v].cls= (s[l]==')') ? 1 : 0 ;
        return ;
    }
    build(v*2,l,(l+r)/2) ;
    build(v*2+1,(l+r)/2+1,r) ;
    tree[v]=combine(tree[2*v],tree[2*v+1]) ;
}

T quiry(int v, int l, int r) {
    if (tree[v].L>r || tree[v].R<l) {
        T res ;
        res.cor=res.opn=res.cls=0 ;
        return res ;
    }
    if (tree[v].L>=l && tree[v].R<=r) {
        T res ;
        res.cor=tree[v].cor ;
        res.opn=tree[v].opn ;
        res.cls=tree[v].cls ;
        return res ;
    }
    return combine(quiry(2*v,l,r), quiry(2*v+1,l,r) ) ;
}

int main()
{
    scanf("%s",s+1) ;
    n=strlen(s+1) ;
    build(1,1,n) ;
    scanf("%d",&m) ;
    while (m--) {
        int l,r ;
        scanf("%d %d",&l,&r) ;
        printf("%d\n",quiry(1,l,r).cor) ;
    }
    return 0;
}

```

