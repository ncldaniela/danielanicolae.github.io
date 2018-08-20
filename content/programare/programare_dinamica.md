---
title: "Metode si Tehnici Clasice de Programare"
date: 2018-08-20T03:16:20+03:00
draft: false
---


<html>
  <head>
    <title>DomnulTudor - PROGRAMAREA DINAMICA</title>
    <link rel="stylesheet" href="static/style.css" type="text/css" />
    <meta http-equiv="Content-Type" content="text/html;charset=utf-8" />
  </head>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
<span style="display: block; text-align: center;"><strong><span style="font-family: 'Arial','sans-serif'; font-size: 18.6667px;">Programare Dinamica</span></strong></span><br />
<span style="color: #000000; display: block; font-family: 'Arial','sans-serif'; text-align: justify;">Programare dinamica presupune rezolvarea unei probleme prin descompunerea ei in subprobleme si rezolvarea acestora. Spre deosebire de divide-et-impera, subproblemele nu sunt disjuncte, ci se suprapun.</span><br />
<span style="color: #000000; display: block; font-family: 'Arial','sans-serif'; text-align: justify;">Pentru a evita recalcularea portiunilor care se suprapun, rezolvarea se face pornind de la cele mai mici subprobleme si folosindu-ne de rezultatul acestora calculam subproblema imediat mai mare. Cele mai mici subprobleme sunt numite subprobleme unitare. Acestea pot fi rezolvate intr-o complexitate constanta, ex: cea mai mare subsecventa dintr-o multime de un singur element.</span><br />
<span style="display: block; text-align: justify;"><span style="color: #000000; font-family: 'Arial','sans-serif';">Pentru a nu recalcula solutiile subproblemelor ce ar trebui rezolvate de mai multe ori, pe ramuri diferite, se retine solutia subproblemelor folosind o tabela (matrice uni, bi sau multidimensionala in functie de problema) cu rezultatul fiecarei subprobleme. Aceasta tehnica se numeste </span><strong><span style="color: #000000; font-family: 'Arial','sans-serif';">memorizare</span></strong><span style="color: #000000; font-family: 'Arial','sans-serif';">.</span></span><br />
<span style="color: #000000; display: block; font-family: 'Arial','sans-serif'; text-align: justify;">Aceasta tehnica afla „valoarea” solutiei optime pentru fiecare din subprobleme. Mergand de la subprobleme mici la subprobleme din ce in ce mai mari ajungem sa gasim „valoarea” problemei intregi. Motivul pentru care aceasta tehnica se numeste Programare Dinamica este datorat flexibilitatii ei, „valoarea” schimbandu-si intelesul logic de la o Problema la alta. In probleme de minimizarea costului, „valoarea” este acest cost minim. In probleme de aflarea unei componente maxime, „valoarea” este dimensiunea componentei.</span><br />
<span style="color: #000000; display: block; font-family: 'Arial','sans-serif'; text-align: justify;">Dupa calcularea valorii pentru toate subproblemele se pot afla efectiv elementele ce alcatuiesc solutia.</span><br />
<span style="color: #000000; display: block; font-family: 'Arial','sans-serif'; text-align: justify;">„Reconstructia” solutiei se face mergand din subproblema in subproblema incepand de la problema cu valoarea optima si ajungand in subprobleme unitare. Metoda admite nuante in cazuri particulare, o sa se inteleaga mai bine din exemple.</span><br />
<span style="display: block; text-align: justify;"><span style="color: #000000; font-family: 'Arial','sans-serif';">Aplicand aceasta tehnica determinam </span><strong><span style="color: #000000; font-family: 'Arial','sans-serif';">una </span></strong><span style="color: #000000; font-family: 'Arial','sans-serif';">din solutiile optime, problema putand avea mai multe solutii optime. In cazul in care se doreste determinarea tuturor solutiilor optime, algoritmul trebuie combinat cu unul de backtracking in reconstructia solutiilor.</span></span><br />
<span style="color: #000000; display: block; font-family: 'Arial','sans-serif'; text-align: justify;">Dupa cum probabil ati intuit deja, diferenta majora dintre cele doua metode prezentate este ca algoritmul greedy mentine doar solutiile partiale de la pasul curent pentru a le folosi la pasul urmator, in timp ce programarea dinamica poate utiliza la un pas subsolutii generate la oricare alt pas anterior.</span><br />
<span style="color: #000000; display: block; font-family: 'Arial','sans-serif'; text-align: justify;">Programarea Dinamica poate fi descompusa in urmatoarea secventa de pasi:</span><br />
<span style="color: #000000; display: block; font-family: 'Arial','sans-serif'; text-align: justify;">1. Descoperirea structurii si &quot;masurii&quot; pe care o are o solutie optima.</span><br />
<span style="color: #000000; display: block; font-family: 'Arial','sans-serif'; text-align: justify;">2. Determinarea unei metode de calcul recursive pentru a afla valoarea fiecarei subprobleme.</span><br />
<span style="color: #000000; display: block; font-family: 'Arial','sans-serif'; text-align: justify;">3. Calcularea &quot;de jos in sus&quot; a acestei valori (de la subproblemele cele mai mici la cele mai mari)</span><br />
<span style="color: #000000; display: block; font-family: 'Arial','sans-serif'; text-align: justify;">4. Reconstructia solutiei optime pornind de la rezultatele obtinute anterior.</span><br />
<br />
<span style="display: block; text-align: justify;"><strong><span style="color: #000000; font-family: 'Arial','sans-serif';">Exemple de probleme:</span></strong></span><br />
<span style="display: block; text-align: justify;"><strong><span style="color: #000000; font-family: 'Arial','sans-serif';">1.Determinarea celui mai lung subsir strict crescator dintr-un sir de numere. </span></strong><span style="color: #000000; font-family: 'Arial','sans-serif';">Un subsir al unui sir este format din caractere (nu neaparat consecutive) ale sirului respectiv, in ordinea in care acestea apar in sir.</span></span><br />
Exemplu: şirul {2, 4, 3, 5, 3, 6} are cel mai lung subsir crescator de lungime 4: {2, 4, 5, 6} sau {2, 3, 5, 6}.<br />
<strong>Rezolvare:</strong><br />
<strong>Soluţia problemei nu este unică, dar lungimea maximă a subşirului crescător, da.</strong><br />
<strong>Vom nota cu L[k] lungimea celui mai lung subşir crescător care începe de la poziţia k şi până la sfârşitul şirului iniţial. Calculăm, pe rând, L[n], L[n-1], L[n-2] … L[2], L[1]. Lungimea celui mai lung subşir crescător va fi dată de cea mai mare valoare a lui L.</strong><br />
<strong>L[n] = 1</strong><br />
<strong>L[k] = 1+ max {L[i ], unde k&lt;i≤n şi v[k]≤v[i ]}, k=n-1,1</strong><br />
<br />
<em>#include&lt;fstream.h&gt;</em><br />
<em>int v[10000],n,i,L[1000],max,mx,k,t;</em><br />
<em>void main(){</em><br />
<em>fstream f(&quot;subsir.txt&quot;,ios::in);</em><br />
<em>for(i=1;i&lt;=n;i++) f&gt;&gt;v[i];</em><br />
<em>L[n]=1;</em> subsir maxim de lung 1<br />
for(k=n-1;k&gt;0;k--)<br />
{mx=0;<br />
for(i=k+1;i&lt;=n;i++)<br />
if(v[i]&gt;=v[k] &amp;&amp; L[i]&gt;mx)<br />
mx=L[i];<br />
L[k]=mx+1;<br />
if(L[k]&gt;max)<br />
{max=L[k];<br />
t=k;}<br />
}<br />
cout&lt;&lt;&quot;lungimea maxima:&quot;&lt;&lt;max;<br />
<em>afisarea subsirului</em><br />
<em>cout&lt;&lt;endl&lt;&lt;v[t]&lt;&lt;' ';</em><br />
<em>for(i=t+1;i&lt;=n;i++)</em><br />
<em>if ((v[i]&gt;=v[t]) &amp;&amp; (L[i]==max-1))</em><br />
<em>{cout&lt;&lt;v[i]&lt;&lt;' ';</em><br />
<em>max--;}</em><br />
<em>}</em><br />
<strong>2. Subşir comun maximal</strong><br />
Fie X=(x1, x2, ..., xn) şi Y=(y1, y2, ..., ym) două şiruri de n, respectiv m numere întregi. Determinaţi un subşir comun de lungime maximă.<br />
Exemplu<br />
Pentru X=(2,5,5,6,2,8,4,0,1,3,5,8) şi Y=(6,2,5,6,5,5,4,3,5,8) o soluţie posibilă este: Z=(2,5,5,4,3,5,8)<br />
<strong>Rezolvare:</strong><br />
Notăm cu Xk=(x1, x2, ..., xk) (prefixul lui X de lungime k) şi cu Yh=(y1, y2, ..., yh) prefixul lui Y de lungime h. O subproblemă a problemei date constă în determinarea celui mai lung subşir comun al lui Xk, Yh. Notăm cu LCS(k,h) lungimea celui mai lung subşir comun al lui Xk, Yh. Utilizând aceste notaţii, problema cere determinarea LCS(n,m), precum şi un astfel de subşir.<br />
Pentru a reţine soluţiile subproblemelor vom utiliza o matrice cu n+1 linii şi m+1 coloane, denumită LCS. Linia şi coloana 0 sunt iniţializate cu 0, iar elementul LCS[k][h] va fi lungimea celui mai lung subşir comun al şirurilor Xk şi Yh.<br />
Vom caracteriza substructura optimală a problemei prin următoarea relaţie de recurenţă:<br />
<br />
lcs[k][0]=lcs[0][h]=0, k din {1,2,..,n}, h din {1,2,..,m}<br />
lcs[k][h]=1+lcs[k-1][h-1], dacă x[k]=y[h]<br />
max{lcs[k][h-1], lcs[k-1][h]}, dacă x[k]&lt;&gt;y[h]<br />
<br />
<em>#include&lt;fstream.h&gt;</em><br />
<em>int x[100],y[100],n,m;</em><br />
<em>int lcs[100][100],max;</em><br />
<br />
<em>void rezolva(){</em><br />
<em>for(int k=1;k&lt;=n;k++)</em><br />
<em>for(int h=1;h&lt;=m;h++)</em><br />
<em>if(x[k]==y[h]) lcs[k][h]=1+lcs[k-1][h-1];</em><br />
<em>else</em><br />
<em>if (lcs[k-1][h]&gt;lcs[k][h-1]) lcs[k][h]=lcs[k-1][h];</em><br />
<em>else lcs[k][h]=lcs[k][h-1];</em><br />
<em>}</em><br />
<em>void afiseaza_solutie_max(int k,int h){</em><br />
<em>if(lcs[k][h])</em><br />
<em>if(x[k]==y[h])</em><br />
<em>{afiseaza_solutie_max(k-1,h-1);</em><br />
<em>cout&lt;&lt;x[k]&lt;&lt;' ';}</em><br />
<em>else</em><br />
<em>{if (lcs[k][h]==lcs[k-1][h])</em><br />
<em>afiseaza_solutie_max(k-1,h);</em><br />
<em>else if (lcs[k][h]==lcs[k][h-1])</em><br />
<em>afiseaza_solutie_max(k,h-1);</em><br />
<em>}</em><br />
<em>}</em><br />
<em>void main(){</em><br />
<em>ifstream f(&quot;lcs.txt&quot;,ios::in);</em><br />
<em>f&gt;&gt;n&gt;&gt;m;</em><br />
<em>for(int i=1;i&lt;=n;i++) f&gt;&gt;x[i];</em><br />
<em>for(i=1;i&lt;=m;i++) f&gt;&gt;y[i];</em><br />
<em>rezolva();</em><br />
<em>afiseaza_solutie_max(n,m);</em><br />
<em>}</em><br />
<strong>3. Sumă maximă în triunghi</strong><br />
Fie triunghiul format din n linii (1&lt;n&lt;=100), fiecare linie conţinând numere întregi din domeniul [1,99], ca în exemplul următor:<br />
<br />
<table class="captionBox"><tr><td class="captionedImage"><img src="http://i44.tinypic.com/b989aa.png" alt="Image" title="Image" /></td></tr><tr><td class="imageCaption">Image</td></tr></table><br />
<br />
Determinaţi cea mai mare sumă de numere aflate pe un drum între numărul de pe prima linie şi un număr de pe ultima linie. Fiecare număr din acest drum este situat sub precedentul, la stânga sau la dreapta acestuia.<br />
<strong>Rezolvare</strong><br />
1. Vom reţine triunghiul într-o matrice pătratică T, de ordin n, sub diagonala principală. Subproblemele problemei date constau în determinarea sumei maxime care se poate obţine din numere aflate pe un drum între numărul T[i ][j], până la un număr de pe ultima linie, fiecare număr din acest drum fiind situat sub precedentul, la stânga sau la dreapta sa. Evident, subproblemele nu sunt independente: pentru a calcula suma maximă a numerelor de pe un drum de la T[i ][j] la ultima linie, trebuie să calculăm suma maximă a numerelor de pe un drum de la T[i+1][j] la ultima linie şi suma maximă a numerelor de pe un drum de la T[i+1][j+1] la ultima linie.<br />
2. Pentru a reţine soluţiile subproblemelor, vom utiliza o matrice suplimentară S, pătratică de ordin n, cu semnificaţia<br />
S[i ][j]= suma maximă ce se poate obţine pe un drum de la T[i ][j] la un element de pe ultima linie, respectând condiţiile problemei.<br />
Soluţia problemei va fi S[1][1].<br />
3. Relaţia de recurenţă care caracterizează substructura optimală a problemei este:<br />
S[n][ i]=T[n][i ], i din {1,2,...,n}<br />
S[i ][j]=T[i ][j]+max{S[i+1][j], S[i+1][j+1]}<br />
<em>Secvenţa de program este:</em><br />
for (i=1; i&lt;=n; i++) S[n][i]=T[n][i];<br />
for (i=n-1; i&gt;=1; i--)<br />
for (j=1; j&lt;=i; j++)<br />
{if (S[i+1][j]&lt;S[i+1][j+1])<br />
S[i][j]=T[i][j]+S[i+1][j+1]);<br />
else<br />
S[i][j]=T[i][j]+S[i+1][j];}<br />
<a href="files/SUMATRI.cpp">SUMATRI.cpp</a><br />
<em><strong>PROBLEME PROPUSE</strong></em><br />
<strong><span style="color: #008080;">1. Împărţirea unei mulţimi în 2 submulţimi de sume cât mai apropiate</span></strong><br />
La sfarsitul noptii de Craciun, Mosul a poposit la bradul a doi frati, unde si-a golit sacul. Cand s-au trezit, fratii au intrat intr-o mare dilema: cum isi vor imparti ei cadourile mosului? Stiind ca fiecare cadou are o valoare (cuprinsa intre 1 si 100 inclusiv) si ca sunt maxim 100 de cadouri scrieti un program care sa determine sumele cadourilor fratilor, precum si modul de impartire, astfel incat sumele obtinute sa fie cele mai apropiate posibil.<br />
Date de intrare:<br />
In fisierul CADOURI.IN se gasesc informaţiile referitoare la cadouri: pe prima linie numarul total de cadouri, pe urmatoarea linie valorile lor.<br />
Date de iesire: In fişierul CADOURI.OUT trebuie scrise doua sume care sunt cele mai apropiate corespunzătoare unei impartiri a cadourilor, pe a doua linie valorile corespunzătoare cadourilor care însumează prima suma găsită, pe a treia linie, valorile corespunzătoare cadourilor care însumează a doua suma găsită.<br />
Exemplu:<br />
CADOURI.IN CADOURI.OUT<br />
7 48 49<br />
28 7 11 8 9 7 27 28 11 9<br />
7 8 7 27<br />
<strong><span style="color: #008080;">2. Sumă maximă</span></strong><br />
Se consideră un şir de N (N£1000) numere naturale cuprinse între 1 şi 10.000. Să se determine o sumă maximă de componente ale şirului astfel încât în sumă să nu intre două numere care se află pe poziţii consecutive în şir.<br />
Exemplu: pentru şirul 1 10 2 40 100, suma maximă este 110 (10+100)
    </div>
  </body>
</html>