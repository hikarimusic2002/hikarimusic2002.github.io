---
layout: splash
title: "Codeforces 1 ~ 100"
permalink: /solutions/codeforces_01
author_profile: false
redirect_from:
  - /resume
---

# Codeforces Problems 1 ~ 100

### 1A. Theatre Square

```cpp
#include <bits/stdc++.h>
using namespace std ;

long long  n, m, a ;

int main() {
    cin>>n>>m>>a ;
    cout<<(n/a+((n%a==0)?0:1))*(m/a+((m%a==0)?0:1)) ;
    return 0 ;
}
```

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

### 20C. Dijkstra

```cpp
#include <bits/stdc++.h>
using namespace std;
#define n_max 100000
#define INF 1e18
#define ll long long
#define pll pair<ll,ll>

vector<vector<pair<ll,ll>>> g(n_max+5) ;

void dijkstra (vector<ll>& d, vector<ll>& p) {
    ll n=g.size() ;
    d[1]=0 ;
    priority_queue<pll, vector<pll>, greater<pll>> q ;
    q.push({0,1}) ;
    while (!q.empty()) {
        ll v=q.top().second ;
        ll d_v=q.top().first ;
        q.pop() ;
        if (d_v!=d[v]) continue ;
        for (auto edge : g[v]) {
            ll to=edge.first ;
            ll len=edge.second ;
            if (d[v]+len<d[to]) {
                d[to]=d[v]+len ;
                p[to]=v ;
                q.push({d[to],to}) ;
            }
        }
    }
}

void showpath(ll n, vector<ll>& p) {
    if (p[n]==-1) printf("%d",-1) ;
    else {
        vector<ll> path ;
        for (int v=n;v!=-1;v=p[v]) {
            path.push_back(v) ;
        }
        reverse(path.begin(),path.end()) ;
        for (auto i : path) printf("%lld ",i) ;
    }
}

int main()
{
    ll n,m ;
    scanf("%lld %lld",&n,&m) ;
    for (int i=0;i<m;++i) {
        ll a,b,w ;
        scanf("%lld %lld %lld",&a,&b,&w) ;
        g[a].push_back({b,w}) ;
        g[b].push_back({a,w}) ;
    }
    vector<ll> d(n+1,INF) ;
    vector<ll> p(n+1,-1) ;
    dijkstra(d,p) ;
    showpath(n,p) ;
    return 0;
}
```

### 25C. Roads in Berlands

```cpp
#include <bits/stdc++.h>
using namespace std ;
#define MAXN 305
#define ll long long

ll n,k ;
ll d[MAXN][MAXN] ;

int main() {
    scanf("%lld",&n) ;
    for (int i=1;i<=n;++i) {
        for (int j=1;j<=n;++j) {
            scanf("%lld",&d[i][j]) ;
        }
    }
    scanf("%lld",&k) ;
    while (k--) {
        ll a,b,c ;
        scanf("%lld %lld %lld",&a,&b,&c) ;
        ll s=0 ;
        for (int i=1;i<=n;++i) {
            for (int j=1;j<=n;++j) {
                d[i][j]=min(d[i][j],d[i][a]+c+d[b][j]) ;
                d[i][j]=min(d[i][j],d[i][b]+c+d[a][j]) ;
                if (j>i) s+=d[i][j] ;
            }
        }
        printf("%lld ",s) ;
    }
}
```

### 25D. Roads not only in Berland

```cpp
#include <bits/stdc++.h>
using namespace std;
#define n_max 1000

int n ;
vector<int> par(n_max+5) ;
vector<int> siz(n_max+5,1) ;
vector<int> cls ;
vector<int> bld ;

void mak(int v) {
    par[v]=v ;
}

int fnd(int v) {
    if (v==par[v]) return v ;
    par[v]=fnd(par[v]) ;
    return par[v] ;
}

void uni(int v, int u) {
    v=fnd(v) ;
    u=fnd(u) ;
    if (v!=u) {
        if (siz[v]<siz[u]) swap(v,u) ;
        par[u]=v ;
        siz[v]+=siz[u] ;
    }
}

int main()
{
    scanf("%d",&n) ;
    for (int i=1;i<=n;++i) mak(i) ;
    for (int i=1;i<n;++i) {
        int a,b ;
        scanf("%d %d",&a,&b) ;
        if (fnd(a)==fnd(b)) {
            cls.push_back(a) ;
            cls.push_back(b) ;
        }
        uni(a,b) ;
    }
    for (int i=2;i<=n;++i) {
        if (fnd(1)!=fnd(i)) {
            bld.push_back(1) ;
            bld.push_back(i) ;
            uni(1,i) ;
        }
    }
    int t=cls.size()/2 ;
    printf("%d\n",t) ;
    for (int i=0;i<t;++i) {
        printf("%d %d ",cls[2*i],cls[2*i+1]) ;
        printf("%d %d\n",bld[2*i],bld[2*i+1]) ;
    }
    return 0;
}
```

### 27E. Number With The Given Amount Of Divisors

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll unsigned long long
#define n_max 1000
#define p_max 10
#define lim 1e18

ll dp[n_max+5][p_max+5], n ;
ll pr[p_max+5]={0,2,3,5,7,11,13,17,19,23,29,31,37,41,43} ;

ll mul (ll a,ll b) {
    ll ans=a*b ;
    if (b>lim/a) ans=lim ;
    return ans ;
}

ll binpow(ll a,int n) {
    ll ans=1 ;
    while (n) {
        if (n&1) {
            ans=mul(ans,a) ;
        }
        a=mul(a,a) ;
        n>>=1 ;
    }
    return ans ;
}

void cal() {
    for (int i=1;i<=n_max;++i) {
        dp[i][1]= binpow(2,i-1) ;
    }
    for (int j=2;j<=p_max;++j) {
        for (int i=1;i<=n_max;++i) {
            dp[i][j]=dp[i][j-1] ;
            for (int k=1;k*k<=i;++k) {
                if (i%k==0) {
                    dp[i][j]=min( dp[i][j], mul(dp[i/k][j-1],binpow(pr[j],k-1)) ) ;
                }
            }
        }
    }
}

int main()
{
    cal() ;
    scanf("%lld",&n) ;
    printf("%lld",dp[n][p_max]) ;
    return 0;
}
```

### 28B. pSort

```cpp
#include <bits/stdc++.h>
using namespace std;
#define n_max 100

int n ;
vector<int> pmt(n_max+5) ;
vector<int> fav(n_max+5) ;

vector<int> par(n_max+5) ;
vector<int> siz(n_max+5) ;

void mak(int v) {
    par[v]=v ;
    siz[v]=1 ;
}

int fnd(int v) {
    if (v==par[v]) return v ;
    par[v]=fnd(par[v]) ;
    return par[v] ;
}

void uni(int a, int b) {
    a=fnd(a) ;
    b=fnd(b) ;
    if (a!=b) {
        if (siz[a]<siz[b]) swap(a,b) ;
        par[b]=a ;
    }
}

int main()
{
    scanf("%d",&n) ;
    for (int i=1;i<=n;++i) scanf("%d",&pmt[i]) ;
    for (int i=1;i<=n;++i) scanf("%d",&fav[i]) ;
    for (int i=1;i<=n;++i) mak(i) ;
    for (int i=1;i<=n;++i) {
        if (i-fav[i]>=1) uni(i,i-fav[i]) ;
        if (i+fav[i]<=n) uni(i,i+fav[i]) ;
    }
    bool ans=1 ;
    for (int i=1;i<=n;++i) {
        if (fnd(pmt[i])!=fnd(i)) {
            ans=0 ;
            break ;
        }
    }
    printf("%s",ans?"YES":"NO") ;
    return 0;
}
```

### 34D. Road Map

```cpp
#include <bits/stdc++.h>
using namespace std;
#define n_max 50000

vector<vector<int>> adj(n_max+5) ;
vector<int> p(n_max+5) ;
vector<bool> vis(n_max+5,0) ;

void dfs (int v) {
    vis[v]=1 ;
    for (int u : adj[v]) {
        if (!vis[u]) {
            p[u]=v ;
            dfs(u) ;
        }
    }
}

int main()
{
    int n,r1,r2,x ;
    scanf("%d %d %d",&n,&r1,&r2) ;
    for (int i=1;i<=n;++i) {
        if (i==r1) continue ;
        scanf("%d",&x) ;
        adj[i].push_back(x) ;
        adj[x].push_back(i) ;
    }
    dfs(r2) ;
    for (int i=1;i<=n;++i) {
        if (i==r2) continue ;
        printf("%d ",p[i]) ;
    }
    return 0;
}
```

### 58A. Chat room

```cpp
#include <bits/stdc++.h>
using namespace std ;

string a,b ;

int main() {
    cin>>a ;
    b="hello" ;
    int cnt=0 ;
    for (int i=0;i<a.length();++i) {
        if (cnt==5) break ;
        if (a[i]==b[cnt]) ++cnt ;
    }
    if (cnt==5) cout<<"YES" ;
    else cout<<"NO" ;
    return 0 ;
}
```

### 61D. Eternal Victory

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long
#define n_max 100000

vector<vector<pair<int,int>>> g(n_max+5) ;
vector<bool> vis(n_max+5);
vector<ll> dis(n_max+5) ;
ll d_max, d_sum ;

void dfs(int a) {
    vis[a]=1 ;
    for (pair<int,int> p : g[a]) {
        if (!vis[p.first]) {
            dis[p.first]=dis[a]+p.second ;
            d_sum+=p.second ;
            d_max=max(d_max,dis[p.first]) ;
            dfs(p.first) ;
        }
    }
}

int main()
{
    int n ;
    cin>>n ;
    for (int i=0;i<n-1;++i) {
        int x,y,w ;
        cin>>x>>y>>w ;
        g[x].push_back(make_pair(y,w)) ;
        g[y].push_back(make_pair(x,w)) ;
    }
    dfs(1) ;
    cout<<2*d_sum-d_max ;
    return 0;
}
```

### 66D. Petya and His Friends

```cpp
#include <bits/stdc++.h>
using namespace std;

int n ;

int main()
{
    scanf("%d",&n) ;
    if (n==2) printf("%d",-1) ;
    else {
        for (int i=1;i<=n-2;++i) {
            printf("%d\n",2*3*i) ;
        }
        printf("%d\n",2*5) ;
        printf("%d\n",3*5) ;
    }

    return 0;
}
```

### 71A. Way Too Long Words

```cpp
#include <bits/stdc++.h>
using namespace std ;

int n ;
string s ;

int main() {
    cin>>n ;
    while (n--) {
        cin>>s ;
        int l=s.length() ;
        if (l<=10) cout<<s<<'\n' ;
        else cout<<s[0]<<l-2<<s[l-1]<<'\n' ;
    }
    return 0 ;
}
```

### 71C. Round Table Knights

```cpp
#include <bits/stdc++.h>
using namespace std;
#define n_max 100000

int n ;
int a[n_max+5] ;

bool good(int i) {
    if (i==n) return 0 ;
    if (n%2==0 && i==n/2) return 0 ;
    for (int j=0;j<i;++j) {
        bool ans=1 ;
        for (int k=0;k<n/i;++k) {
            if (a[(j+k*i)%n]==0) {
                ans=0 ;
                
                
                
                break ;
            }
        }
        if (ans==1) return 1 ;
    }
    return 0 ;
} 

int main()
{
    scanf("%d",&n) ;
    for (int i=0;i<n;++i) {
        scanf("%d",&a[i]) ;
    }
    bool ans=0 ;
    for (int i=1;i*i<=n;++i) {
        if (n%i==0) {
            if (good(i) || good(n/i)) {
                ans=1 ;
                break ;
            }
        }
    }
    printf("%s",(ans?"YES":"NO")) ;
    return 0;
}
```

### 75C. Modified GCD

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long

ll gcd(ll a,ll b) {
    return b ? gcd(b,a%b) : a ;
}

void factorize(vector<ll>& fac, ll g) {
    for (int i=1;i*i<=g;++i) {
        if (g%i==0) {
            fac.push_back(i) ;
            fac.push_back(g/i) ;
        }
    }
    sort(fac.begin(),fac.end()) ;
}

ll search(vector<ll> fac, ll low, ll high) {
    ll l=0, h=fac.size()-1, ans=-1 ;
    while (l<=h) {
        ll m=l+(h-l)/2 ;
        if (fac[m]>high) h=m-1 ;
        else {
            ans=fac[m] ;
            l=m+1 ;
        }
    }
    if (ans>=low) return ans ;
    return -1 ;
}

int main()
{
    ll a,b,n,low,high,g ;
    vector<ll> fac ;
    scanf("%lld %lld",&a,&b) ;
    g=gcd(a,b) ;
    factorize(fac,g) ;
    scanf("%lld",&n) ;
    for (int i=0;i<n;++i) {
        scanf("%lld %lld",&low,&high) ;
        printf("%lld\n",search(fac,low,high)) ;
    }
    return 0;
}
```

### 78C. Beaver Game

```cpp
#include <bits/stdc++.h>
using namespace std;
#define ll long long

bool win(ll n, ll m, ll k) {
    if (n%2==1) {
        if (m!=1 && k==1) return 1 ;
        for (int i=2;i*i<=m;++i) {
            if (m%i==0) {
                if (i>=k || (m/i)>=k) return 1 ;
            }
        }
    }
    return 0 ;
}

int main()
{
    ll n,m,k ;
    scanf("%lld %lld %lld",&n,&m,&k) ;
    printf("%s",win(n,m,k)?"Timur":"Marsel") ;
    return 0;
}
```

