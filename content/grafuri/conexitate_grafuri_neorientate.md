---
title: "Conexitate in Grafuri Neorientate"
date: 2018-08-20T03:16:20+03:00
weight: 2
draft: false
---

<html>
  <body>
<h2 id="toc0"><a name="x-Algoritmul Roy-Warshall:Exista drum intre nodul x si nodul y?"></a><span style="background-color: #ffffff; color: #222222; font-family: Arial,Tahoma,Helvetica,FreeSans,sans-serif; font-size: 22px;">Algoritmul Roy-Warshall: Exista drum intre nodul x si nodul y?</span></h2>

```c++
#include <iostream>
#include <conio.h>

using namespace std;

int main() {
  int n,i,a[100][100],j,k,x,y;
  cout<<"n=";cin>>n;
  for(i=1;i<=n;i++)
  for(j=1;j<=n;j++)
  {cout<<"a["<<i<<"]["<<j<<"]=";
  cin>>a[i][j];
  }
  for(k=1;k<=n;k++)
    for(i=1;i<=n;i++)
      for(j=1;j<=n;j++)
        if(a[i][j]==0 && i!=k && j!=k)
          a[i][j]=a[i][k]*a[k][j];
          cout<<"Nodul initial:";cin>>x;
        cout<<"Nodul final:";cin>>y;
  if(a[x][y]==1)
    cout<<"Exista drum intre nodul "<<x<<" si nodul "<<y<<".";
  else
    cout<<"NU exista drum intre nodul "<<x<<" si nodul "<<y<<".";
  getch();
  return 0;
}
```

<h1 id="toc1"><a name="file:Conexitate în grafuri neorientate.pptx"></a><a href="/files/Conexitate%20%C3%AEn%20grafuri%20neorientate.pptx">Conexitate în grafuri neorientate.pptx</a></h1>
 <h2 id="toc2"> </h2>
 <h2 id="toc3"><a name="file:Conexitate în grafuri neorientate.pptx-CONEXITATE IN GRAFURI NEORIENTATE"></a><span style="color: #24913c;">CONEXITATE IN GRAFURI NEORIENTATE</span></h2>
 
```c++
#include<fstream>

using namespace std;

int k,m,n,x[100],a[100][100],p[100];

fstream f("date.in",ios::in);
fstream g("date.out",ios::out);

void citire()
 {int x,y;
  f>>n>>m;
  for(int i=1;i<=m;i++)
   {f>>x>>y;
    a[x][y]=1;
    a[y][x]=1;
   }
 }

void rw()
 {int i, j, k;
  for(k=1;k<=n;k++)
   for(i=1;i<=n;i++)
    for(j=1;j<=n;j++)
   if(i!=j)
   if(a[i][j]==0)
   a[i][j]=a[i][k]*a[k][j];
 }
 
 void afis()
  {for(int i=1;i<=n;i++)
    if(!p[i])
    { g<<i<<" ";
      p[i]=1;
      for(int j=1; j<=n; j++)
         if(a[i][j]) { g<<j<<" "; p[j]=1;}
      g<<endl;
   }
  }

int main()
  {citire();
   rw();
   afis();
   f.close();
   g.close();
   return 0;
  }
```

  </body>
</html>