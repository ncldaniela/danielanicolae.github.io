---
title: "Fisiere Text"
date: 2018-08-20T03:16:20+03:00
weight: 2
draft: false
---

<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">Declararea, închiderea şi deschiderea fişierelor în C++ utilizează anumite clase şi funcţii care sunt declarate în biblioteca <em>fstream.h.</em></span></span><br />
<span style="display: block; text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New'; font-size: 10pt;">#include<fstream.h></span></strong></span><br />
<span style="display: block; text-align: justify;"><strong><em><span style="font-family: Arial,sans-serif; font-size: 10pt;">Declararea fişierelor</span></em></strong></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">Pentru a putea citi/scrie informaţii dintr-un/într-un fişier, acesta se asociază unui <em>stream</em> (flux) de intrare/ieşire.</span></span><br />
<span style="display: block; text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New'; font-size: 10pt;">ifstream nume_fişier_logic (nume_fişier);</span></strong><strong><span style="font-family: 'Courier New'; font-size: 10pt;"> <em>deschiderea unui fisier pentr a citi date</em></span></strong></span><br />
<span style="display: block; text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New'; font-size: 10pt;">ofstream nume_fişier_logic (nume_fişier);</span></strong></span><br />
<strong>deschiderea unui fisier pentru a scrie date</strong><br />
<span style="display: block; text-align: justify;"><strong><em><span style="font-family: Arial,sans-serif; font-size: 10pt;">Exemplu:</span></em></strong></span><br />
<span style="font-family: Arial,sans-serif; font-size: 10pt;">fisier de intrare fişier de iesire</span><br />
<span style="display: block; text-align: justify;"><strong><span style="font-family: 'Courier New';">ifstream f(”numere.in”); ofstream g(”numere.out”);</span></strong></span><br />
<span style="display: block; text-align: justify;"><em><span style="font-family: Arial,sans-serif; font-size: 10pt;">Crearea unui fisier cu date ce urmeaza a fi citite prin program</span></em></span><br />
<span style="display: block; text-align: justify;"><strong><em><span style="font-family: Arial,sans-serif; font-size: 10pt;">FILE</span></em></strong><strong><em><span style="font-family: Wingdings; font-size: 10pt;">à</span></em></strong><strong><em><span style="font-family: Arial,sans-serif; font-size: 10pt;"> New</span></em></strong><strong><em><span style="font-family: Wingdings; font-size: 10pt;">à</span></em></strong></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">- scriem date in fisier</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">- salvam fisierul cu numele specificat intre parantezele rotunde ale functiei ifstream </span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;"> (de exemplu numere.in)</span></span><span style="display: block; text-align: center;"><span style="display: block; text-align: center;"><strong><span style="color: #cc0066; font-family: 'Courier New';">CITIREA datelor</span></strong></span><br />


<table class="wiki_table">
    <tr>
        <td><span style="display: block; text-align: center;"><strong><span style="color: #cc0066; font-family: 'Courier New'; font-size: 10pt;">de la tastatura</span></strong></span><br />
</td>
        <td><span style="display: block; text-align: center;"><strong><span style="color: #cc0066; font-family: 'Courier New'; font-size: 10pt;">din fisier</span></strong></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">#include<iostream.h></span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">void main()</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">{ int x;</span></strong></span><br />
<span style="text-align: justify;"> <strong><span style="color: #cc0066; font-family: 'Courier New';">cin>>x;</span><span style="font-family: 'Courier New';"><em>citim un numar</em></span></strong></span><br />
<em><span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">}</span></strong></span></em><br />
</td>
        <td><span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">#include<fstream.h></span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">void main()</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">{ </span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">ifstream f(”numere.in”); </span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">int x;</span></strong></span><br />
<br />
<span style="text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New';">f>>x;</span></strong><strong><span style="font-family: 'Courier New';"> citim un numar din fisier</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">}</span></strong></span><br />
</td>
    </tr>
</table>

</span><br />
<span style="display: block; font-family: Arial,sans-serif; font-size: 10pt; text-align: justify;">Fisierele de iesire, cele in care se vor afisa rezultatele NU trebuie create de noi, le va crea programul.</span><br />
<span style="display: block; text-align: center;"><br />
<span style="display: block; text-align: center;"><strong><span style="color: #cc0066; font-family: 'Courier New';">SCRIEREA datelor</span></strong></span><br />


<table class="wiki_table">
    <tr>
        <td><span style="display: block; text-align: center;"><strong><span style="color: #cc0066; font-family: 'Courier New'; font-size: 10pt;">Pe ecran</span></strong></span><br />
</td>
        <td><span style="display: block; text-align: center;"><strong><span style="color: #cc0066; font-family: 'Courier New'; font-size: 10pt;">in fisier</span></strong></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">#include<iostream.h></span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">void main()</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">{ int x;</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';"> cin>>x;</span></strong></span><br />
<strong><span style="color: #cc0066; font-family: 'Courier New';">cout<<x;</span></strong><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">}</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">#include<fstream.h></span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">void main()</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">{ </span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">ifstream f(”numere.in”); </span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">ofstream g(”numere.out”); </span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">int x;</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">f>>x; <em>citim un numar din fisier</em></span></strong></span><br />
<em><span style="text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New';">g<<x;</span></strong></span></em><strong>scriem in fisier</strong><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">}</span></strong></span><br />
</td>
    </tr>
</table>

</span><br />
<span style="display: block; text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New';">ATENTIE:</span></strong></span><br />
<span style="display: block; text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New';"> NU mai utilizati clrscr() si getch() cand lucrati cu fisiere!</span></strong></span><br />
<span style="display: block; text-align: justify;"><strong><em><span style="font-family: Arial,sans-serif; font-size: 10pt;">Funcţii utile în prelucrarea fişierelor text</span></em></strong></span><br />
<span style="display: block; text-align: justify;"><br />
</span><span style="display: block; text-align: justify;"><strong><span style="font-family: 'Courier New';">eof()</span></strong><span style="font-family: Arial,sans-serif; font-size: 10pt;"> – se utilizează pentru detectarea sfârşitului de fişier. Funcţia returnează 0 dacă valoarea curentă nu este sfârşitul de fişier şi 1 în caz contrar.</span></span><br />
<span style="display: block; text-align: justify;"><strong><span style="font-family: 'Courier New';">f.close()</span></strong><span style="font-family: Arial,sans-serif; font-size: 10pt;"> – se utilizează pentru închiderea fişierului</span></span><br />
<span style="display: block; text-align: center;"><span style="display: block; text-align: center;"><strong><span style="color: #cc0066; font-family: 'Courier New';">CITIREA datelor din fisier</span></strong></span><br />


<table class="wiki_table">
    <tr>
        <td><span style="display: block; text-align: center;"><strong><span style="color: #cc0066; font-family: 'Courier New'; font-size: 10pt;">este cunoscut numarul n al valorilor</span></strong></span><br />
</td>
        <td><span style="display: block; text-align: center;"><strong><span style="color: #cc0066; font-family: 'Courier New'; font-size: 10pt;">cand nu este cunoscut numarul valorilor din fisier</span></strong></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">Enunt: </span></strong><span style="font-family: Arial,sans-serif; font-size: 10pt;">Se citesc n numere intregi , calculati suma lor si afisati aceasta suma in fisierul date.out.</span></span><br />
<br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">#include<fstream.h></span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">void main()</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">{ </span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">ifstream f(”date.in”); </span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">ofstream g(”date.out”); </span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">int x,s=0,n;</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">f>>n;</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New';">for(i=1;i<=n;i++)</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New';"> { f>>x;</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New';"> s=s+x;</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New';"> }</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">g<<s;</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">f.close();g.close();</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';"> }</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">Enunt: </span></strong><span style="font-family: Arial,sans-serif; font-size: 10pt;">Se citesc toate numerele intregi din fisierul date.in, calculati suma lor si afisati aceasta suma in fisierul date.out.</span></span><br />
VARIANTA 1<br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">#include<fstream.h></span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">void main()</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">{ </span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">ifstream f(”date.in”); </span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">ofstream g(”date.out”); </span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">int x,s=0;</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New';">while(f>>x)</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="color: #cc0066; font-family: 'Courier New';"> s=s+x;</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">g<<s;</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';">f.close();g.close();</span></strong></span><br />
<span style="text-align: justify;"><strong><span style="font-family: 'Courier New';"> }</span></strong></span><br />
VARIANTA 2<br />
<span style="display: block; text-align: justify;"><strong><span style="font-family: 'Courier New';">#include<fstream.h></span></strong></span><strong>void main()</strong><br />
<strong>{</strong><br />
<strong>ifstream f(”date.in”);</strong><br />
<strong>ofstream g(”date.out”);</strong><br />
<strong>int x,s=0;</strong><br />
<strong>f>>x;</strong><br />
<strong><span style="color: #cc0066;">while(!f.eof())</span></strong><br />
<strong><span style="color: #cc0066;">{s=s+x;</span></strong><br />
<strong><span style="color: #cc0066;">f>>x;}</span></strong><br />
g<<s;<br />
<strong>f.close();g.close();</strong><br />
<strong>}</strong><br />
</td>
    </tr>
</table>

</span><br />
<span style="display: block; text-align: justify;"><strong><span style="font-family: 'Courier New';">Enunt: </span></strong><span style="font-family: Arial,sans-serif; font-size: 10pt;">Se citesc n numere intregi , calculati suma lor si afisati aceasta suma in fisierul date.out.</span></span><br />
<span style="display: block; text-align: justify;"><strong><span style="font-family: 'Courier New';">Enunt: </span></strong><span style="font-family: Arial,sans-serif; font-size: 10pt;">Se citesc toate numerele intregi din fisierul date.in, calculati suma lor si afisati aceasta suma in fisierul date.out.</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">Aplicatii:</span></span><br />
<span style="display: block; text-align: justify;"><strong>Problema: Buchete</strong></span><br />
<span style="display: block; text-align: justify;">(olimpiada locala de informatica 2003 – autor: Crstina Iordaiche)</span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">La o florarie s-au primit n (n<=30000) fire de flori. Din fisierul buchete.in se citeste numarul n.</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">Florareasa doreste sa le aranjeze in vaze astfel incat:</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">- toate vazele sa contina acelasi numar de flori</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">- numarul florilor din vaza sa fie impar</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">Cerinta: Afisati in fisierul buchete.out, in cate moduri poate imparti florareasa cele n fire de flori.</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">Pentru fiecare caz afisati numarul de vaze necesare si cate flori va contine fiecare vaza.</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">Exemplu:</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">n=9</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">1 vaza a cate 9 flori</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">3 vaze a cate 3 flori</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">9 vaze cate 1 floare</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">----------------------</span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">Florile se pot imparti in 3 moduri:</span></span><br />
<span style="display: block; text-align: justify;"><strong>Problema:Parola</strong></span><br />
<span style="display: block; text-align: justify;">(Concursul National de informatica SATU MARE 2009 – autor: Crstina Iordaiche)</span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">La un joc computerizat trecerea de la un nivel la altul se face prin intermediul unei parole in functie de punctajul obtinut de jucator, la nivelul anterior. Parola este un numar de maxim 9 cifre, cel mai mare posibil care se obtine luand in considerare o singura data toate cifrele ce fac parte din punctajul realizat de jucator. Citindu-se din fisierul parola.in punctajul P obtinut de jucator, afisati in fisierul parola.out, parola ce trebuie tastata pentru trecerea la nivelul urmator.</span></span><br />
<span style="display: block; font-family: Arial,sans-serif; font-size: 10pt; text-align: justify;">Exemplu:</span><br />
<span style="display: block; font-family: Arial,sans-serif; font-size: 10pt; text-align: justify;">P= 41100 parola=410</span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;">Probleme pentru pregatire in vederea participarii la olimpiada:</span></span><span style="display: block; font-family: Arial,sans-serif; font-size: 10pt; text-align: justify;"><a class="wiki_link_ext" href="http://olimpiada.info/oji2007/index.php?cid=arhiva" rel="nofollow">http://olimpiada.info/oji2007/index.php?cid=arhiva</a></span><br />
<br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;"><a class="wiki_link_ext" href="http://campion.edu.ro/arhiva/index.php?page=problem&amp;action=view&amp;id=912" rel="nofollow">http://campion.edu.ro/arhiva/index.php?page=problem&amp;action=view&amp;id=912</a></span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;"><a class="wiki_link_ext" href="http://campion.edu.ro/arhiva/index.php?page=problem&amp;action=view&amp;id=413" rel="nofollow">http://campion.edu.ro/arhiva/index.php?page=problem&amp;action=view&amp;id=413</a></span></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: Arial,sans-serif; font-size: 10pt;"><a class="wiki_link_ext" href="http://campion.edu.ro/arhiva/index.php?page=problem&amp;action=view&amp;id=407" rel="nofollow">http://campion.edu.ro/arhiva/index.php?page=problem&amp;action=view&amp;id=407</a></span></span>
    </div>
  </body>
</html>