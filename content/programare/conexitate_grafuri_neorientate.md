---
title: "Conexitate in Grafuri Neorientate"
date: 2018-08-20T03:16:20+03:00
draft: false
---

<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
<h2 id="toc0"><a name="x-Algoritmul Roy-Warshall:Exista drum intre nodul x si nodul y?"></a><span style="background-color: #ffffff; color: #222222; font-family: Arial,Tahoma,Helvetica,FreeSans,sans-serif; font-size: 22px;">Algoritmul Roy-Warshall:Exista drum intre nodul x si nodul y?</span></h2>
 <span style="background-color: #ffffff; color: #222222; display: block; font-family: Arial,Tahoma,Helvetica,FreeSans,sans-serif; font-size: 10.8px;"><span style="color: #6aa84f;">#include &lt;iostream&gt;</span></span><span style="background-color: #ffffff; color: #222222; display: block; font-family: Arial,Tahoma,Helvetica,FreeSans,sans-serif; font-size: 13.2px;"><span style="color: #6aa84f;">#include &lt;conio.h&gt;</span><br />
using namespace std;<br />
int main()<br />
{<br />
int n,i,a[100][100],j,k,x,y;<br />
cout&lt;&lt;&quot;n=&quot;;cin&gt;&gt;n;<br />
for(i=1;i&lt;=n;i++)<br />
for(j=1;j&lt;=n;j++)<br />
{cout&lt;&lt;&quot;a[&quot;&lt;&lt;i&lt;&lt;&quot;][&quot;&lt;&lt;j&lt;&lt;&quot;]=&quot;;<br />
cin&gt;&gt;a[i][j];<br />
}<br />
for(k=1;k&lt;=n;k++)<br />
for(i=1;i&lt;=n;i++)<br />
for(j=1;j&lt;=n;j++)<br />
if(a[i][j]==0&amp;&amp; i!=k&amp;&amp;j!=k)<br />
a[i][j]=a[i][k]*a[k][j];<br />
cout&lt;&lt;&quot;Nodul initial:&quot;;cin&gt;&gt;x;<br />
cout&lt;&lt;&quot;Nodul final:&quot;;cin&gt;&gt;y;<br />
if(a[x][y]==1)<br />
cout&lt;&lt;&quot;Exista drum intre nodul &quot;&lt;&lt;x&lt;&lt;&quot; si nodul &quot;&lt;&lt;y&lt;&lt;&quot;.&quot;;<br />
else<br />
cout&lt;&lt;&quot;NU exista drum intre nodul &quot;&lt;&lt;x&lt;&lt;&quot; si nodul &quot;&lt;&lt;y&lt;&lt;&quot;.&quot;;<br />
getch();<br />
return 0;<br />
}</span><br />
<h1 id="toc1"><a name="file:Conexitate în grafuri neorientate.pptx"></a><a href="files/Conexitate%20%C3%AEn%20grafuri%20neorientate.pptx">Conexitate în grafuri neorientate.pptx</a></h1>
 <h2 id="toc2"> </h2>
 <h2 id="toc3"><a name="file:Conexitate în grafuri neorientate.pptx-CONEXITATE IN GRAFURI NEORIENTATE"></a><span style="color: #24913c;">CONEXITATE IN GRAFURI NEORIENTATE</span></h2>
 
<style type="text/css"><!--
/**
 * GeSHi (C) 2004 - 2007 Nigel McNie, 2007 - 2008 Benny Baumann
 * (http://qbnz.com/highlighter/ and http://geshi.org/)
 */
.text  {font-family:monospace;}
.text .imp {font-weight: bold; color: red;}
.text span.xtra { display:block; }

-->
</style><pre class="text">#include&lt;fstream&gt;
using namespace std;
int k,m,n,x[100],a[100][100],p[100];
&nbsp;
fstream f(&quot;date.in&quot;,ios::in);
fstream g(&quot;date.out&quot;,ios::out);
&nbsp;
void citire()
 {int x,y;
  f&gt;&gt;n&gt;&gt;m;
  for(int i=1;i&lt;=m;i++)
   {f&gt;&gt;x&gt;&gt;y;
    a[x][y]=1;
    a[y][x]=1;
   }
 }
void rw()
 {int i, j, k;
  for(k=1;k&lt;=n;k++)
   for(i=1;i&lt;=n;i++)
    for(j=1;j&lt;=n;j++)
   if(i!=j)
   if(a[i][j]==0)
   a[i][j]=a[i][k]*a[k][j];
 }
 void afis()
  {for(int i=1;i&lt;=n;i++)
    if(!p[i])
    { g&lt;&lt;i&lt;&lt;&quot; &quot;;
      p[i]=1;
      for(int j=1;j&lt;=n;j++)
         if(a[i][j]) { g&lt;&lt;j&lt;&lt;&quot; &quot;; p[j]=1;}
      g&lt;&lt;endl;
   }
  }
&nbsp;
int main()
  {citire();
   rw();
   afis();
   f.close();
   g.close();
   return 0;
  }
&nbsp;
&lt;/span&gt;</pre>

<h1 id="toc4"> </h1>

    </div>
  </body>
</html>