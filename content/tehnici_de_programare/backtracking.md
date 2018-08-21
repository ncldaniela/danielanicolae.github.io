---
title: "Backtracking"
date: 2018-08-20T03:16:20+03:00
weight: 2
draft: false
---

<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
<span style="font-size: 10pt;">Metoda backtracking se aplica problemelor in care solutia se poate prezenta sub forma unui vector x={x1,x2,…,xn} unde x1 apartine unei multimi S1, x2 apartine multimii S2 s.a.m.d.Si i=1…n sunt multimi finite. Cerinta problemei este, de obicei, gasirea tuturor solutiilor posibile sau gasirea numarului de solutii care satisfac anumite conditii specifice problemei. De multe ori metoda se foloseste si pentru gasirea unei singure solutii (dupa gasirea acesteia se intrerupe executia programului), a unei solutii maxime/minime insa, pentru astfel de cazuri recomandam gasirea unei alte solutii de rezolvare datorita faptului ca metoda Backtracking consuma resurse mari de memorie si timp.</span><br />
<span style="font-size: 10pt;">Conditiile interne, numite si conditii de continuitate, sunt acele conditii care trebuie indeplinite de un element pentru a fi adaugat la solutie. Validitatea elementului se verifica in functie de elementele aflate in fata lui in vectorul solutie (vectorul x).</span><br />
<span style="font-size: 10pt;"> Metoda evita generarea tuturor solutiilor posibile. Se va cauta obtinerea unei solutii prin alegerea succesiva de elemente din multimile S1, S2, S3,…,Sn. Astfel, la pasul k, se va alege un element xk din multimea Sk. Inainte de a trece la pasul k+1, se verifica daca sunt satisfacute conditiile de continuitate. In cazul in care pentru o valoare xk aleasa, conditiile de continuare nu sunt satisfacute, se va alege o alta valoare din multimea Sk, pana cand fie se va gasi o valoare care sa satisfaca conditiile de continuitate, fie se epuizeaza toate elementele multimii Sk. In cazul in care se gaseşte un element xk convenabil avem doua cazuri: fie s-a ajuns la obtinerea unei solutii caz in care se afiseaza solutia, fie nu s-a ajuns la o solutie caz in care se trece la gasirea urmatorului element din vectorul solutie (cel de pe pozitia k+1). Exista şi cazul in care pozitia k din vectorul solutie nu s-a putut completa cu un element xk din Sk, adica nu s-a gasit un element care sa indeplineasca conditiile de continuitate. In acest caz se va reveni la pasul anterior (k-1). Se va renunta la valoarea x(k-1) aleasa şi se va cauta alegerea unei alte valori (urmatoarea valoare din multimea k-1).</span><br />
<span style="font-size: 10pt;"> Ca orice algoritm in care sunt prezente instructiuni repetitive, algoritmul backtracking poate fi reprezentat intr-o maniera recursiva sau nerecursiva.</span><br />
<br />
<span style="color: #ed4040; display: block; font-family: 'Courier New',Courier,monospace; font-size: 10pt; text-align: center;"><strong>APLICATII</strong></span><br />
<span style="font-size: 10pt;">1. </span><strong><em><span style="font-family: Arial,sans-serif;">Dintr-un numar de 6 cursuri opţionale un elev trebuie să aleagă 3. Să se afişeze toate posibilităţile de alegere precum şi numarul lor.</span></em></strong><br />
<br />
<strong><em><span style="font-family: Arial,sans-serif;">2.Lui IRINEL îi plac nr. formate numai din cifre pare cifre aflate în ordine descrescătoare. Să se determine şi să se afişeze pe ecran toate nr. de n cifre (0<n<10) care îi plac lui Irinel. Valoarea lui n este un nr. natural care se citeşte de la tastatură.{ex.: n=3 200; 220; 222; 400; 402; 422; 440; 442; 444; 600; 620; 622; 640; 644; 660; 662; 664; 666; 800; 820; 822; 840; 842; 844; 860; 862; 864; 866; 880; 882; 884; 886; 888.} </span></em></strong><br />
<br />
<span style="font-size: 10pt;">3.</span><strong><span style="font-family: Arial,sans-serif; font-size: 10pt;">Problema celor n dame. </span></strong><span style="font-family: Arial,sans-serif; font-size: 10pt;">Fiind dată o tablă de şah n</span><span style="font-family: Symbol; font-size: 10pt;">´</span><span style="font-family: Arial,sans-serif; font-size: 10pt;">n se cer toate soluţiile de aranjare a n dame, astfel încât să nu se afle două dame pe aceeaşi linie, coloană sau diagonală (damele să nu se atace reciproc).</span><br />
<br />
<em><span style="font-family: Arial,sans-serif; font-size: 10pt;">4.</span></em><strong><span style="color: black; font-family: Arial,sans-serif; font-size: 10pt;">.PROBLEMA COLORARII HARTILOR: Fiind dată o hartă cu n ţări, se cer toate soluţiile de colorare a hărţii, utilizând cel mult patru culori, astfel încât două ţări de frontieră comună să fie colorate diferit. Este demonstrat faptul că sunt suficiente numai patru culori pentru ca orice hartă să poată fi colorată.</span></strong><br />
<strong><span style="color: black; font-family: Arial,sans-serif; font-size: 10pt;">5. PROBLEMA DRAPELELOR : </span></strong>Avem la dipoziţie 6 culori: alb, galben, roşu, verde, albastru, negru. Să se precizeze toate drapelele tricolore care se pot proiecta, ştiind că trebuie respectate regulile:<br />
<span style="font-family: Arial,sans-serif; font-size: 10pt;">- orice drapel are culoarea din mijloc galben sau verde </span><br />
<span style="font-family: Arial,sans-serif; font-size: 10pt;">- cele trei culori de pe drapel sunt distincte. </span><br />
<span style="font-family: Arial,sans-serif; font-size: 10pt;">Observaţie: utilizaţi facilităţile unit-ului crt, în afişarea culorilor drapelelor generate</span><br />
<br />
6. <strong>Produsul cartezian a n mulţimi.</strong> Se dau mulţimile de mai jos şi se cere produsul cartezian al lor.<br />
<br />
<span style="color: black; font-family: Arial,sans-serif; font-size: 10pt;"> A1 = {1, 2, 3, …, k1}</span><br />
<br />
<span style="color: black; font-family: Arial,sans-serif; font-size: 10pt;"> A2 = {1, 2, 3, …, k2}</span><br />
………………………<br />
An = {1, 2, 3, …, kn}<br />
<br />
<strong>7.</strong> <strong>TURNURI DE CUBUR</strong>I Se dau n cuburi numerotate 1,2,...,n, de laturi Li si culori Ci, i=1,2,...,n (fiecare culoare este codificata printr-un caracter). Sa se afişeze toate turnurile care se pot forma luând k cuburi din cele n disponibile, astfel încât:<br />
<span style="font-family: Arial,sans-serif; font-size: 10pt;"> -laturile cuburilor din turn sa fie in ordine crescătoare;</span><br />
<span style="font-family: Arial,sans-serif; font-size: 10pt;"> -culorile a oricare doua cuburi alăturate din turn sa fie diferite.</span><br />
<br />
8. <strong>Problema comis-voiajorului.</strong> Un comis voiajor trebuie să viziteze un număr n de oraşe. Iniţial, el se află într-unul dintre ele, notat 1. Comis – voiajorul doreşte să nu treacă de două ori prin acelaşi oraş, iar la întoarcere să revină în oraşul 1. Cunoscând legăturile existente între oraşe, se cere să se tipărească toate drumurile posibile pe care le poate efectua comis – voiajorul.<br />
<br />
9 <strong>Sa se genereze partitiile nr.natural n.<a href="/files/partitii.cpp">partitii.cpp</a></strong><br />
ex.n=5<br />
5=1+1+1+1+1<br />
5=1+1+1+2<br />
5=1+1+3<br />
5=1+4<br />
5=5.<br />
10.<br />


<table class="wiki_table">
    <tr>
        <td>10. Se citeste de la tastatura un numar natural n par, n<30. Sa se genereze si sa se afiseze pe ecran toate combinatiile de n paranteze rotunde care se închid corect. De exemplu, pentru n=4 se obtin urmatoarele combinatii: ( ( ) ) si ( ) ( ) .<a href="/files/PARANTEZE.CPP">PARANTEZE.CPP</a><br />
</td>
    </tr>
</table>

<br />
11.Se citeste un numar natural n<30. Sa se afiseze toate modalitatile de a-l calcula prin adunari sau scaderi ale numerelor 1,2, ...n. Fiecare numar de la 1 la n va aparea o singura data în descompunerea lui n. Daca acest lucru nu este posibil, se va afisa mesajul „Imposibil”.<br />
Exemplu:<br />
5=1+2+3+4-5<br />
5=1-2-3+4+5<br />
5=-1+2+3-4+5<br />
<a href="/files/SUMA.CPP">SUMA.CPP</a><br />
<h2 id="toc0"><a name="x-LISTA PROBLEME"></a><strong>LISTA PROBLEME</strong></h2>
 <h2 id="toc1"><a name="x-file:backtracking_proiect.docx file:subiecte_informatica_limbajul_c_(sub_3).zip"></a><a href="/files/backtracking_proiect.docx">backtracking_proiect.docx</a> <a href="/files/subiecte_informatica_limbajul_c_%28sub_3%29.zip">subiecte_informatica_limbajul_c_(sub_3).zip</a></h2>
 <h2 id="toc2"><a name="x-GRILE BACKTRACKING"></a><strong>GRILE BACKTRACKING</strong></h2>
 <a href="/files/grile%20backtracking.pdf">grile backtracking.pdf</a>
    </div>
  </body>
</html>