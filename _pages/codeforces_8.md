---
layout: splash
title: "Codeforces"
permalink: /solutions/codeforces_8
author_profile: false
redirect_from:
  - /resume
---

# Codeforces Problems 701 ~ 800

### 722C. Destroying Array

```cpp
#include <bits/stdc++.h>
using namespace std;
#define MAXN 100005
#define ll long long

int n, a[MAXN], s[MAXN] ;
int p[MAXN] ;
ll sum[MAXN] ;
bool exist[MAXN] ;
vector<ll> ans ;

int find_set(int v) {
    if (p[v]==v) return v ;
    return p[v]=find_set(p[v]) ;
}

void union_set(int v, int u) {
    int pv=find_set(v) ;
    int pu=find_set(u) ;
    if (pv!=pu) {
        p[u]=v ;
        sum[v]+=sum[u] ;
    }
}

int main()
{
    scanf("%d",&n) ;
    for (int i=1;i<=n;++i) {
        scanf("%d",&a[i]) ;
        p[i]=i ;
        sum[i]=a[i] ;
    }
    for (int i=1;i<=n;++i) scanf("%d",&s[i]) ;
    ll M=0 ;
    ans.push_back(0) ;
    for (int i=n;i>=1;--i) {
        int x=s[i] ;
        exist[x]=1 ;
        if (exist[x-1]) union_set(x,find_set(x-1)) ;
        if (exist[x+1]) union_set(x,find_set(x+1)) ;
        M=max(M,sum[x]) ;
        ans.push_back(M) ;
    }
    for (int i=n-1;i>=0;--i) printf("%lld\n",ans[i]) ;
    return 0;
}

```

### 780C. Andryusha and Colored Balloons

```cpp
#include <bits/stdc++.h>
using namespace std;
#define n_max 200000

int n ;
vector<vector<int>> g(n_max+5) ;
vector<bool> vis(n_max+5,0) ;
vector<int> p(n_max+5,0) ;
vector<int> clr(n_max+5) ;
int k=0 ;

void dfs(int v){
    vis[v]=1 ;
    int cnt=0 ;
    for (int u : g[v]) {
        if (!vis[u]) {
            p[u]=v ;
            ++cnt ;
            while (cnt==clr[v]||cnt==clr[p[v]]) {
                ++cnt ;
            }
            clr[u]=cnt ;
            k=max(k,cnt) ;
            dfs(u) ;
        }
    }
}

int main()
{
    scanf("%d",&n) ;
    for (int i=0;i<n-1;++i) {
        int x,y ;
        scanf("%d %d",&x,&y) ;
        g[x].push_back(y) ;
        g[y].push_back(x) ;
    }
    clr[1]=1, p[1]=0, clr[0]=0 ;
    dfs(1) ;
    printf("%d\n",k) ;
    for (int i=1;i<=n;++i) {
        printf("%d ",clr[i]) ;
    }
    return 0;
}

```

### 793B. Igor and his way to work

```cpp
#include <bits/stdc++.h>
using namespace std;
#define n_max 1000

int n,m ;
bool mp[n_max+5][n_max+5] ;
int vis[n_max+5][n_max+5][5] ;
int dx[4]={1,-1,0,0} ;
int dy[4]={0,0,1,-1} ;

struct point {
    int x,y,dir,cnt ;
}s,t,u,v ;

bool bfs() {
    for (int i=0;i<n+5;++i) 
    for (int j=0;j<m+5;++j) 
    for (int k=0;k<5;++k) 
    vis[i][j][k]=5 ;
    queue<point> q ;
    s.dir=-1 ;
    s.cnt=0 ;
    q.push(s) ;
    while (!q.empty()) {
        v=q.front() ;
        q.pop() ;
        if (v.x==t.x && v.y==t.y) return 1 ;
        for (int i=0;i<4;++i) {
            u.x=v.x+dx[i] ;
            u.y=v.y+dy[i] ;
            u.dir=i ;
            if (v.dir==-1) u.cnt=0 ;
            else if (v.dir==i) u.cnt=v.cnt ;
            else if (v.dir!=i) u.cnt=v.cnt+1 ;
            if (u.x<0||u.y<0) continue ;
            if (!mp[u.x][u.y]||u.cnt>2) continue ;
            if (vis[u.x][u.y][u.dir]<=u.cnt) continue ;
            vis[u.x][u.y][i]=u.cnt ;
            q.push(u) ;
        }
    }
    return 0 ;
}

int main()
{
    scanf("%d %d",&n,&m) ;
    for (int i=0;i<n;++i) {
        string seq ;
        cin>>seq ;
        for (int j=0;j<m;++j) {
            if (seq[j]!='*') mp[i][j]=1 ;
            if (seq[j]=='S') s.x=i,s.y=j ;
            if (seq[j]=='T') t.x=i,t.y=j ;
        }
    }
    printf("%s",bfs()?"YES":"NO") ;
    return 0;
}

```

