---
layout: splash
title: "Codeforces"
permalink: /solutions/codeforces_7
author_profile: false
redirect_from:
  - /resume
---

# Codeforces Problems 601 ~700

### 616C. The Labyrinth

```cpp
#include <bits/stdc++.h>
using namespace std;
#define n_max 1000 

int n,m ;
vector<string> mp ;
bool vis[n_max+5][n_max+5] ;
int com[n_max+5][n_max+5] ;
int num[n_max*n_max+5] ;
int dx[4]={1,-1,0,0} ;
int dy[4]={0,0,1,-1} ;

bool check(int x,int y) {
    if (x<0||x>=n) return 0 ;
    if (y<0||y>=m) return 0 ;
    if (mp[x][y]=='*') return 0 ;
    return 1 ;
}

void dfs(int x, int y, int cnt) {
    vis[x][y]=1 ;
    com[x][y]=cnt ;
    ++num[cnt] ;
    for (int i=0;i<4;++i) {
        int x1=x+dx[i] ;
        int y1=y+dy[i] ;
        if (!check(x1,y1)) continue ;
        if (!vis[x1][y1]) dfs(x1,y1,cnt) ;
    }
}

int main()
{
    scanf("%d %d",&n,&m) ;
    string in ;
    for (int i=0;i<n;++i) {
        cin>>in ;
        mp.push_back(in) ;
    }
    int cnt=1 ;
    for (int i=0;i<n;++i) {
        for (int j=0;j<m;++j) {
            if (!vis[i][j] && mp[i][j]=='.') {
                dfs(i,j,cnt) ;
                ++cnt ;
            }
        }
        
    }
    for (int i=0;i<n;++i) {
        string out(m,'.') ;
        for (int j=0;j<m;++j) {
            set<int> sur ;
            if (check(i,j)) continue ;
            int ans=1 ;
            for (int k=0;k<4;++k) {
                int x=i+dx[k] ;
                int y=j+dy[k] ;
                if (!check(x,y)) continue ;
                sur.insert(com[x][y]) ;
            }
            for (int t : sur) {
                ans+=num[t] ;
            }
            out[j]=(char) (ans%10)+'0'  ;
        }
        cout<<out<<'\n' ;
    }
    return 0;
}

```

### 630I. Parking lot

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long

ll binpow(ll a, ll b)
{
    long long r=1 ;
    while(b) {
        if (b&1) r*=a ;
        a*=a ;
        b>>=1 ;
    }
    return r ;
}

int main()
{
    ll n ;
    scanf("%lld",&n) ;
    printf("%lld",(9*n-3)*binpow(4,n-3)) ;
    return 0;
}

```

### 687B. Remainders Game

```cpp
#include <bits/stdc++.h>
using namespace std;
#define c_max 1000000

vector<int> lp(c_max+5,0) ;
vector<int> pr ;

void lin_sieve(int N) {
    for (int i=2;i<=N;++i) {
        if (lp[i]==0) {
            lp[i]=i ;
            pr.push_back(i) ;
        }
        for (int j=0;j<pr.size() && pr[j]<=lp[i] && i*pr[j]<=N;++j) {
            lp[i*pr[j]]=pr[j] ;
        }
    }
}

int main()
{
    lin_sieve(c_max) ;
    int n,k,c ;
    scanf("%d %d",&n,&k) ;
    vector<int> fac(c_max+5,0) ;
    for (int t=0;t<n;++t) {
        scanf("%d",&c) ;
        while (c>1) {
            int p=lp[c] ;
            int q=0 ;
            while (c%p==0) {
                ++q ;
                c/=p ;
            }
            if (q>fac[p]) fac[p]=q ;
        }
    }
    bool ans=1 ;
    while (k>1) {
        --fac[lp[k]] ;
        if (fac[lp[k]]<0) {
            ans=0 ;
            break ;
        }
        k/=lp[k] ;
    }
    printf("%s",ans?"Yes":"No") ;
    return 0;
}

```

### 689D. Friends and Subsequences

```cpp
#include <bits/stdc++.h>
using namespace std;
#define nmax 200005
#define pmax 20
#define ll long long

int n ;
ll a[nmax], b[nmax] ;
ll sta[nmax][pmax] ;
ll stb[nmax][pmax] ;

void sta_build() {
    for (int i=0;i<n;++i) sta[i][0]=a[i] ;
    int k=(int)log2(n)+1 ;
    for (int j=1;j<=k;++j) {
        for (int i=0;i+(1<<j)<=n;++i) {
            sta[i][j]=max(sta[i][j-1], sta[i+(1<<(j-1))][j-1]) ;
        }
    }
}

void stb_build() {
    for (int i=0;i<n;++i) stb[i][0]=b[i] ;
    int k=(int)log2(n)+1 ;
    for (int j=1;j<=k;++j) {
        for (int i=0;i+(1<<j)<=n;++i) {
            stb[i][j]=min(stb[i][j-1], stb[i+(1<<(j-1))][j-1]) ;
        }
    }
}

ll sta_quiry(int L, int R) {
    int k=(int)log2(R-L+1) ;
    return max(sta[L][k],sta[R-(1<<k)+1][k]) ;
}

ll stb_quiry(int L, int R) {
    int k=(int)log2(R-L+1) ;
    return min(stb[L][k],stb[R-(1<<k)+1][k]) ;
}

ll ans_count() {
    ll ans=0 ;
    for (int i=0;i<n;++i) {
        int P1=i-1, P2=n ;
        int L=i, R=n-1, M ;
        while (L<=R) {
            M=(L+R)/2 ;
            if (stb_quiry(i,M)-sta_quiry(i,M)>0) {
                P1=M ;
                L=M+1 ;
            }
            else R=M-1 ;
        }
        L=P1+1, R=n-1 ;
        while (L<=R) {
            M=(L+R)/2 ;
            if (stb_quiry(i,M)-sta_quiry(i,M)<0) {
                P2=M ;
                R=M-1 ;
            }
            else L=M+1 ;
        }
        ans+=P2-P1-1 ;
    }
    return ans ;
}

int main()
{
    scanf("%d",&n) ;
    for (int i=0;i<n;++i) scanf("%lld",&a[i]) ;
    for (int i=0;i<n;++i) scanf("%lld",&b[i]) ;
    sta_build() ;
    stb_build() ;
    printf("%lld",ans_count()) ;
    return 0;
}

```

