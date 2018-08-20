---
title: "Greedy"
date: 2018-08-20T03:16:20+03:00
draft: false
---

<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
<span style="display: block; text-align: center;"><strong><span style="color: #0000ff; font-family: 'Times New Roman','serif'; font-size: 24px;"><span class="wiki_link_ext">Metoda Greedy</span></span></strong></span><br />
<span style="display: block; font-family: 'Times New Roman',serif; font-size: 16px; text-align: justify;">“<em>De alegerea strategiei depinde atât timpul de rezolvare cât și calitatea soluției gasite</em>“</span><br />
<h1 id="toc0"><a name="x1. Descrierea metodei"></a>1. Descrierea metodei</h1>
 <span style="display: block; text-align: justify;">Se dă o mulţime A cu <em>n</em> elemente şi se cere să se determine o submulţime a sa(B) care satisface anumite restricţii. Această submulţime se numeşte <em>soluţie posibilă</em>. Se cere să se determine o soluţie posibilă care fie să maximizeze fie să minimizeze o anumită <em>funcţie obiectiv</em> dată. Această soluţie posibilă se numeşte <em>soluţie optimă</em>.</span><br />
<span style="display: block; text-align: justify;">Metoda Greedy lucrează în paşi astfel:</span><br />
<ol><li>se iniţializează mulţimea soluţiilor (B) cu mulţimea vidă</li><li>se alege un anumit element <em>x</em> <span style="font-family: Arial,Helvetica,sans-serif;">din </span> A</li><li>se verifică dacă elementul ales poate fi adăugat la mulţimea soluţiilor, dacă da atunci va fi adăugat</li><li>procedeul continuă astfel, repetitiv, cu pasul 2 până când au fost determinate toate elementele din mulţimea soluţiilor</li></ol><span style="display: block; text-align: justify;">Observaţie. Metoda Greedy nu caută să determine toate soluţiile posibile ( care ar putea fi prea numeroase) şi apoi să aleagă din ele pe cea optimă, ci caută să introducă direct un element <em>x</em> în soluţia optimă.</span><br />
<span style="display: block; text-align: justify;"><strong><span style="font-family: 'Times New Roman','serif'; font-size: 16px;">2. Ideea metodei: </span></strong><span style="font-family: 'Times New Roman','serif'; font-size: 16px;">La fiecare pas se alege un element care face solutia partiala cat mai buna. Se presupune ca facand mereu alegerea cea mai buna la moment, avem sansa (dar nu certitudinea) obtinerii solutiei optime, in final.</span></span><span style="display: block; text-align: justify;"><br />
<strong><em>Algoritmii Greedy sunt foarte eficienți, dar nu conduc în mod necesar la o soluție optimă. Şi nici nu este posibilă formularea unui criteriu general conform căruia să putem stabili exact dacă metoda Greedy rezolvă sau nu o anumită problemă de optimizare. Din acest motiv, orice algoritm Greedy trebuie însoțit de o demonstrație a corectitudinii sale . Demonstrația faptului că o anumită problemă are proprietatea alegerii Greedy se face de obicei prin inducție matematică</em></strong><br />
</span><br />
O întrebare firească este aceea dacă algoritmul Greedy duce totdeauna la soluţie optimă? Evident că nu Sunt situaţii când soluţia găsită nu este optimă. Mai mult, pentru cele mai multe din probleme nu se cunosc algoritmi Greedy de rezolvare. Spre deosebire de Backtracking, algoritmul Greedy nu permite atunci când s-a oservat că nu se poate ajunge la soluţie pentru o anumită secvenţă de elemente, revenirea înapoi, pe nivelele anterioare. Pentru problemele care nu duc la soluţia optimă este necesar să se caute soluţii, chiar dacă nu optime, dar cât mai apropiate de acestea.<br />
<strong>Între metoda Greedy şi metoda Backtracking putem enumera următoarele diferenţe:</strong><br />
• ambele tehnici oferă soluţii sub formă de vector<br />
• tehnica Backtracking oferă toate soluţiile problemei, în timp ce Greedy oferă o singură soluţie<br />
• tehnica Greedy nu dispune de mecanismul întoarcerii, specific tehnicii Backtracking<br />
<span style="display: block; line-height: 1.5; text-align: justify;"><span style="font-family: 'Times New Roman','serif'; font-size: 24px;">Algoritmi clasici:</span></span><span style="display: block; line-height: 1.5; text-align: justify;"><em><span style="font-family: 'Times New Roman','serif'; font-size: 16px;">Problema rucsacului. </span></em></span><span style="display: block; font-family: 'Times New Roman',serif; font-size: 16px; text-align: justify;">Un hot are la dispozitie un rucsac cu care poate transporta o greutate maxima Gmax. Hotul are de ales din n obiecte si intentioneaza sa obtina un castig maxim in urma singurului transport pe care il poate face. Cunoscand, pentru fiecare obiect i greutatea Gi si castigul Ci pe care hotul l-ar obtine transportand obiectul respectiv in intregime, scrieti un program care sa determine o incarcare optima a rucsacului.</span><br />
<a href="files/rucsac.cpp">rucsac.cpp</a><br />
<br />
<br />
<span style="display: block; text-align: justify;"><strong><em><span style="font-family: 'Times New Roman','serif'; font-size: 16px;">Problema platii unui salariu. </span></em></strong><span style="font-family: 'Times New Roman','serif'; font-size: 16px;">Sa se plateasca un salariu dat cu numar minim de monezi, daca se cunosc tipurile de monezi existente. Monedele sunt in numar nelimitat (variante cu/fara atingerea solutiei optime).</span></span><br />
<span style="display: block; font-family: 'Times New Roman',serif; font-size: 16px; line-height: 1.5; text-align: justify;"><u>Cazul 1.</u></span><span style="display: block; font-family: 'Times New Roman',serif; font-size: 16px; line-height: 1.5; text-align: justify;">Se atinge solutia optima.</span><br />
<span style="font-family: 'Times New Roman',serif; font-size: 16px; line-height: 1.5; text-align: justify;">Suma= 360; Monedele sunt 100, 50, 20,10,3</span><br />
<span style="font-family: 'Times New Roman',serif; font-size: 16px; line-height: 1.5; text-align: justify;">360=3*100+1*50+1*10+0*3</span><br />
<span style="font-family: 'Times New Roman',serif; font-size: 16px; line-height: 1.5; text-align: justify;">Cazul 2.</span><br />
<span style="display: block; font-family: 'Times New Roman',serif; font-size: 16px; line-height: 1.5; text-align: justify;">Nu se atinge solutia optima</span><br />
<span style="font-family: 'Times New Roman',serif; font-size: 16px; line-height: 1.5; text-align: justify;">Suma= 365; Monedele sunt 100, 50, 20,10,3</span><br />
<span style="font-family: 'Times New Roman',serif; font-size: 16px; line-height: 1.5; text-align: justify;">365=3*100+1*50+1*10+1*3 NEPLATIT 2</span><br />
<span style="font-family: 'Times New Roman',serif; font-size: 16px; line-height: 1.5; text-align: justify;">Optim ar fi fost:</span><br />
<span style="font-family: 'Times New Roman',serif; font-size: 16px; line-height: 1.5; text-align: justify;">365=3*100+1*50+0*10+5*3</span><br />
<br />
#include&lt;iostream&gt;<br />
using namespace std;<br />
int n,i,aux,ok,s,a[100], nr[100];<br />
main()<br />
{<br />
cout&lt;&lt;&quot;Suma=&quot;;cin&gt;&gt;s;<br />
cout&lt;&lt;&quot;Numarul de bancnote:&quot;;cin&gt;&gt;n;<br />
for(i=1;i&lt;=n;i++)<br />
{<br />
cout&lt;&lt;&quot;a[&quot;&lt;&lt;i&lt;&lt;&quot;]=&quot;;cin&gt;&gt;a[i];<br />
nr[i]=i;<br />
}<br />
do<br />
{<br />
ok=1;<br />
for(i=1;i&lt;=n-1;i++)<br />
if(a[nr[i]]&lt;a[nr[i+1]])<br />
{<br />
aux=nr[i];<br />
nr[i]=nr[i+1];<br />
nr[i+1]=aux;<br />
ok=0;<br />
}<br />
}<br />
while(ok==0);<br />
for(i=1;i&lt;=n;i++)<br />
cout&lt;&lt;nr[i]&lt;&lt;&quot; &quot;;<br />
i=1;<br />
cout&lt;&lt;s&lt;&lt;endl;<br />
do<br />
{<br />
if(s/a[nr[i]]&gt;0)<br />
{cout&lt;&lt;s/a[nr[i]]&lt;&lt;&quot; bancnote cu valoarea &quot;&lt;&lt;a[nr[i]]&lt;&lt;endl;<br />
s=s%a[nr[i]];}<br />
i++;<br />
}<br />
while(i&lt;=n);<br />
}<br />
<strong><span style="line-height: 1.5; text-align: justify;">Problema spectacolelor</span></strong><br />
<span style="display: block; text-align: justify;">Managerul artistic al unui festival trebuie să selecteze o mulțime cât mai amplă de spectacole ce pot fi jucate în singura sală pe care o are la dispoziție. Ştiind că i s-au propus n≤100 spectacole şi pentru fiecare spectacol i i-a fost anunțat intervalul în care se poate desfăşura [si, fi) (si reprezintă ora şi minutul de început, iar fi ora şi minutul de final al spectacolului i) scrieți un program care să permită spectatorilor vizionarea unui număr cât mai mare de spectacole. De exemplu, dacă vom citi n=5 şi următorii timpi:<br />
12 30 16 30<br />
15 0 18 0<br />
10 0 18 30<br />
18 0 20 45<br />
12 15 13 0<br />
Spectacolele selectate sunt: 5 2 4.<br />
<strong><u>Soluție</u></strong><br />
Ordonăm spectacolele crescător după ora de final. Selectăm inițial primul spectacol (deci cel care se termină cel mai devreme). La fiecare pas selectăm primul spectacol neselectat, care nu se suprapune cu cele deja selectate (deci care începe după ce se termină ultimul spectacol selectat).<br />
#include &lt;iostream.h&gt;<br />
int inceput[100], sfarsit[100], nr[100];<br />
int main()<br />
{int n, i, h, m, ok, ultim, aux;<br />
cout &lt;&lt; &quot;n= &quot;; cin &gt;&gt; n; <em>citire</em><br />
<em>cout&lt;&lt;&quot;Introduceti inceputul si sfarsitul spectacolelor&quot;;</em><br />
<em>for (i=1; i&lt;=n; i++)</em><br />
<em><span style="line-height: 1.5;"> {nr[i]=i; </span></em></span><br />
transform timpul in minute<br />
<span style="line-height: 1.5;">cin&gt;&gt;h&gt;&gt;m; inceput[i]=h*60+m;</span><br />
cin&gt;&gt;h&gt;&gt;m; sfarsit[i]=h*60+m;} <em>ordonez spectacolele crescator dupa ora de final</em><br />
<em>do</em><br />
<em>{ok=1;</em><br />
<em><span style="line-height: 1.5;">for (i=1; i&lt;n; i++)</span></em><br />
<em>if (sfarsit[nr[i]]&gt;sfarsit[nr[i+1]])</em><br />
<em>{aux=nr[i];nr[i]=nr[i+1];nr[i+1]=aux; ok=0;}</em><br />
<em>}</em><br />
<em>while (ok==0);</em><br />
<em>cout &lt;&lt; &quot;Spectacolele selectate sunt:&quot;&lt;&lt;nr[1]&lt;&lt;' ';</em><br />
<em>ultim=1;</em><br />
<em>for ( i=2; i&lt;=n; i++)</em><br />
<em>if (inceput[nr[i]]&gt;=sfarsit[nr[ultim]])</em><br />
<em>{cout &lt;&lt;nr[i]&lt;&lt;' '; ultim=i;}</em><br />
<em>cout&lt;&lt;endl;</em><br />
<em>return 0;}</em><br />
<br />
<strong><span style="font-family: 'Times New Roman','serif'; font-size: 16px;">Problema comis-voiajorului. </span></strong><br />
<span style="display: block; font-family: 'Times New Roman',serif; font-size: 16px; text-align: justify;">Se cunosc distantele dintre mai multe orase. Un comis-voiajor pleaca dintr-un oras si doreste sa se intoarca in acelasi oras, dupa ce a vizitat fiecare din celelalte orase exact o data. Problema este de a minimiza lungimea drumului parcurs. (Indicatie. La fiecare pas se alege orasul nou, cel mai apropiat).</span><br />
<a href="files/comis.cpp">comis.cpp</a><br />
<strong><span style="font-family: 'Calibri','sans-serif'; font-size: 14.6667px;">Problema</span> partitiilor de numere prime</strong>// Se da un sir de numere naturale citite pe rand pana la intalnirea numarului 0.Sa se determine un grup maxim de elemente ale sirului cu proprietatea ca elementele sunt numerele prime iar suma lor e egala cu cel mult un numar m dat .<br />
<br />
<span style="display: block; text-align: justify;"><a href="files/part.cpp">part.cpp</a></span>
    </div>
  </body>
</html>