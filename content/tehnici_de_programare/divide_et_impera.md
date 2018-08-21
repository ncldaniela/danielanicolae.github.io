---
title: "Divide et Impera"
date: 2018-08-20T03:16:20+03:00
weight: 3
draft: false
---

<html>
  <body>
Divide et impera se bazează pe principiul descompunerii problemei în două sau mai multe subprobleme (mai ușoare), care se rezolvă, iar soluția pentru problema inițială se obține combinând soluțiile subproblemelor. De multe ori, subproblemele sunt de același tip și pentru fiecare din ele se poate aplica aceeași tactică a descompunerii în (alte) subprobleme, până când (în urma descompunerilor repetate) se ajunge la probleme care admit rezolvare imediată.<br />
Nu toate problemele pot fi rezolvate prin utilizarea acestei tehnici. Se poate afirma că numărul celor rezolvabile prin "divide et impera" este relativ mic, tocmai datorită cerinței ca problema să admită o descompunere repetată.<br />
Divide et impera este o tehnică ce admite o implementare <a class="wiki_link_ext" href="http://ro.wikipedia.org/wiki/Recursivitate" rel="nofollow">recursivă</a>. Principiul general prin care se elaborează algoritmi recursivi este: "ce se întâmplă la un nivel, se întâmplă la orice nivel" (având grijă să asigurăm condițiile de terminare). Așadar, un algoritm prin divide et impera se elaborează astfel: la un anumit nivel avem două posibilități:<br />
<ol><li>s-a ajuns la o problemă care admite o rezolvare imediată (condiția de terminare), caz în care se rezolvă și se revine din apel;</li><li>nu s-a ajuns în situația de la punctul 1, caz în care problema curentă este descompusă în (două sau mai multe) subprobleme, pentru fiecare din ele urmează un apel recursiv al funcției, după care combinarea rezultatelor are loc fie pentru fiecare subproblemă, fie la final, înaintea revenirii din apel.</li></ol><h2 id="toc0"><a name="x-Aplicații"></a><span class="mw-headline">Aplicații</span></h2>
 <h3 id="toc1"><a name="x-Aplicații-Maximul dintr-un vector"></a><span class="editsection"><a class="wiki_link_ext" href="http://ro.wikipedia.org/wiki/Maximul_dintr-un_vector" rel="nofollow">Maximul dintr-un vector</a></span></h3>
 Se citește un vector cu n componente, numere naturale. Se cere să se tipărească valoarea maximă.<br />
Funcția căutată va genera valoarea maximă dintre numerele reținute în vector pe o poziție dintre i și j (inițial, i=1, j=n). Pentru aceasta, se procedează astfel:<br />
<ul><li>dacă i=j, valoarea maxima va fi v[i];</li><li>în caz contrar, se imparte vectorul în doi subvectori - presupunem varianta pentru paralelizare pe 2 procesoare. Se calculează mijlocul m al intervalului [i, j]: m = (i+j) div 2. Primul subvector va conține componentele de la i la m, al doilea va conține componentele de la (m+1) la j; se rezolvă subproblemele (aflându-se astfel maximul pentru fiecare din subvectori), iar soluția curentă va fi dată de valoarea maximă dintre rezultatele celor două subprobleme.</li></ul><br />

```c++
#include <iostream>
using namespace std;
int v[10], n;
int max(int i, int j) {
  int a, b, m;
  if (i == j)
    return v[i];
  else {
    m = (i + j) / 2;
    a = max(i, m);
    b = max(m + 1, j);
    if (a > b)
      return a;
    else
      return b;
  }
}
int main() {
  cout <<”n =”;
  cin >> n;
  for (int i = 1; i <= n; i++) { 
    cout<<"v["<cin>>v[i];
  }
  cout<<"max="<1,n);
  return 0;
}
```

<br />
<span class="mw-headline"><a class="wiki_link_ext" href="http://ro.wikipedia.org/wiki/C%C4%83utare_binar%C4%83" rel="nofollow">Căutare binară</a></span><br />
Se citește un vector cu n componente numere întregi (numerele se presupun ordonate crescător) și o valoare întreagă ("nr"). Să se decidă dacă nr se găsește sau nu printre numerele citite, iar în caz afirmativ să se tipărească indicele componentei care conține această valoare.<br />
O rezolvare în care nr se compară pe rând cu toate cele n componente reperzintă o pierdere de performanță (nu exploatează faptul că cele n valori sunt în secvență crescătoare). Algoritmul care va fi propus este optim și se poate spune că face parte dintre algoritmii "clasici".<br />
Funcția care va fi implementată va decide dacă valoarea căutată se găsește printre numerele aflate pe poziții de indice cuprins între i și j (inițial, i=1, j=n). Pentru aceasta, se va proceda astfel:<br />
<ul><li>dacă nr coincide cu valoarea de la mijloc, aflată pe poziția de indice (i+j)/2, se tipărește indicele și se revine din apel (problema a fost rezolvată).</li><li>în caz contrar, dacă mai sunt și alte elemente de analizat (adică i<j, deci nu au fost verificate toate pozițiile necesare), problema se descompune astfel:</li><li>dacă nr este mai mic decât valoarea testată (din mijloc), înseamnă că nu se poate afla pe pozițiile din partea dreaptă, întrucât acestea sunt cel puțin mai mari decât valoarea testată. Nr se poate găsi doar printre componentele cu indice între i și (i+j)/2 - 1, caz în care se reapelează funcția cu acești parametri;</li><li>dacă nr este mai mare decât valoarea testată (din mijloc), înseamnă că nu se poate afla în stânga; se poate găsi doar printre componentele cu indicele între (i+j)/2 + 1 și j, caz în care se reapelează funcția cu acești parametri.</li><li>dacă nu mai sunt alte elemente de analizat (pentru că i=j și valoarea din mijloc, v[i], nu coincide cu nr), se concluzionează că nr nu apare în cadrul vectorului.</li></ul>Această problemă nu mai necesită analiza tuturor subproblemelor în care se descompune, ea se reduce la o singură subproblemă, iar partea de combinare a soluțiilor dispare. În linii mari, această rezolvare este tot de tip "divide et impera".<br />

```c++
#include <iostream>
using namespace std;
int v[100], n, nr;
void caut(int i, int j) {
  int m = (i + j) / 2;
  if (nr == v[m])
    cout <<”gasit, indice =”<< m;
  else if (i < j)
    if (nr < v[m])
      caut(i, m - 1);
    else
      caut(m + 1, j);
  else
    cout <<”nu a fost gasit.”;
}
int main() {
  cout <<”n =”;
  cin >> n;
  for (int i = 1; i <= n; i++) {
    cout <<”v[“<< i <<”] =”;
    cin >> v[i];
  }
  cout <<”nr =”;
  cin >> nr;
  caut(1, n);
  return 0;
}
```

<h1 id="toc2"><a name="QUICKSORT"></a><span style="color: #008000; font-family: 'Courier New'; font-size: 13.3333px;">QUICKSORT</span></h1>
 Functia poz rezolva o portiune din vector cuprinsa intre indicii p si u piv=v[p] este un reper.La sfarsitul executiei acestei functii piv se va gasi pe o pozitie k cuprinsa intre p si u astfel incat toate componentele vectorului cuprinse intre p si k-1 vor fi mai mici decat piv iar componentele cuprinse intre k+1 si u vor fi mai mari decat piv. Deci piv se va gasi pe pozitia k corespunzatoare ordinii in vector<br />

```c++
#include <iostream.h>
#include <conio.h>
#include <stdlib.h>
int x[2000], n;
int poz(int p, int u) {
  int piv, aux, k;
  piv = x[p];
  while (p < u) {
    if (x[p] > x[u]) {
      aux = x[p];
      x[p] = x[u];
      x[u] = aux;
    }
    if (x[p] == piv)
      u--;
    else
      p++;
  }
  k = p;
  return k;
}
void quick(int p, int u) {
  int k;
  if (p < u) {
    k = poz(p, u);
    quick(p, k - 1);
    quick(k + 1, u);
  }
}
void main() {
  clrscr();
  cout << "n=";
  cin >> n;
  for (int i = 1; i <= n; i++) {
    cout << "x[" << i << "]=";
    cin >> x[i];
  }
  quick(1, n);
  for (i = 1; i <= n; i++) cout << x[i] << ' ';
  getch();
}
```

<h3 id="toc3"><a name="QUICKSORT--TURNURILE DIN HANOI"></a><span style="color: #008000; font-family: 'Courier New'; font-size: 13.3333px;">TURNURILE DIN HANOI</span></h3>
 <a title="View Turnurile Din Hanoi on Scribd" href="http://www.scribd.com/doc/86186533/Turnurile-Din-Hanoi?secret_password=y8btftpoekbwitpx8d5" style="margin: 12px auto 6px auto; font-family: Helvetica,Arial,Sans-serif; font-style: normal; font-variant: normal; font-weight: normal; font-size: 14px; line-height: normal; font-size-adjust: none; font-stretch: normal; -x-system-font: none; display: block; text-decoration: underline;" rel="nofollow">Turnurile Din Hanoi</a><iframe class="scribd_iframe_embed" src="http://www.scribd.com/embeds/86186533/content?start_page=1&amp;view_mode=list&amp;access_key=key-gkfc92pybl4lb8r23gz&amp;secret_password=y8btftpoekbwitpx8d5" data-auto-height="true" data-aspect-ratio="1.33333333333333" scrolling="no" id="doc_62658" width="100%" height="600" frameborder="0" name="doc_62658"></iframe><script type="text/javascript">
//<![CDATA[
(function() { var scribd = document.createElement("script"); scribd.type = "text/javascript"; scribd.async = true; scribd.src = "http://www.scribd.com/javascripts/embed_code/inject.js"; var s = document.getElementsByTagName("script")[0]; s.parentNode.insertBefore(scribd, s); })();
//]]>
</script><br />
<br />
<h3 id="toc4"><a name="QUICKSORT--PROBLEME PROPUSE"></a><span style="font-family: 'Courier New'; font-size: 13.3333px;">PROBLEME PROPUSE</span></h3>
 <br />
<span style="font-family: 'Times New Roman'; font-size: 13.3333px;">1. Se citeste un numar natural n si n numere naturale. Sa se calculeze cel mai mare divizor comun al celor n numere, folosind un algoritm Divide et Impera.</span><br />
<br />
<span style="font-family: 'Times New Roman'; font-size: 13.3333px;">2. Scrieti un program pentru determinarea minimului dintr-un sir de numere intregi, folosind Divide et Impera.</span><br />
<br />
<span style="font-family: 'Times New Roman'; font-size: 13.3333px;">3. Scrieti un program pentru calculul sumei valorilor dintr-un sir de numere intregi, folosind Divide et Impera.</span><br />
<br />
<span style="font-family: 'Times New Roman'; font-size: 13.3333px;">4. Sa se determine cate elemente pare are un vector</span><br />
<br />
<span style="font-family: 'Times New Roman'; font-size: 13.3333px;">5. Fie un tablou neordonat de numere intregi. Sa se determine prin metoda D&amp;I de cate ori apare in tablou o anumita valoare v.</span><br />
<br />
<br />
6. Să se calculeze n!<br />
<br />
7. Să se calculeze simultan produsul şi suma a n numere memorate într-un vector.<br />
<br />
8. Să se calculeze suma 1x2+2x3+3x4+...+nx(n+1).<br />
<br />
9. Să se calculeze suma 1x2+1x2x3+...+1x2x3x...xn.<br />
<br />
10. Să se numere elementele divizibile cu 5 dintr-un vector.<br />
<br />
11. Să se verifice dacă un vector conţine numai numere pozitive sau numai numere negative.<br />
12. Sa se gaseasca intr-un vector cu n elemente un element cu proprietatea ca valoarea lui este egala cu pozitia pe care apare. (a[k]=k)<br />
<br />
13. Scrieti o functie ce inverseaza un sir de caractere<br />
<br />
14. Să se afişeze dacă un cuvânt este palindrom.<br />
<br />
15. Să se verifice dacă un şir de numere este simetric.<br />
<br />
16. Sa se determine valoarea unui polinom intr-un punct<br />
17. Se citesc numele si inaltimile a n persoane.<br />
<br />
a) Sa se afiseze persoanele avand inaltimea mai mare sau egala cu un h citit.<br />
<br />
b) Sa se ordoneze crescator persoanele dupa inaltime.<br />
<br />
c) Sa se afiseze o persoana avand o inaltime data. Daca nu exista o astfel de persoana se va afisa un mesaj.<br />
<br />
18. Se citesc numele a n persoane si inaltimile<br />
<br />
a) Sa se determine daca persoanele sunt ordonate dupa inaltime<br />
<br />
b) Sa se afiseze persoana cea mai inalta<br />
<br />
c) Care este inaltimea medie?<br />
<br />
d) Sa se ordoneze alfabetic persoanele prin metoada QuickSort<br />
<br />
e) Sa se afiseze inaltimea unei persoane al carei nume se va citi de la tastatura (cautare binara dupa nume)<br />
<br />
f) Sa se ordoneze persoanele descrescator dupa inaltime utilizand MergeSort<br />
<br />
g) Sa se afiseze toate persoanele cu inaltimea mai mare de 1.70<br />
<br />
h) Sa se determine cate persoane au inaltimea 1.80
  </body>
</html>