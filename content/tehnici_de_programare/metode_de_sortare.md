---
title: "Metode de Sortare"
date: 2018-08-20T03:16:20+03:00
weight: 5
draft: false
---

<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
<span style="display: block; text-align: center;"><span style="display: block; text-align: center;"><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">METODE SI TEHNICI DE SORTARE A UNUI VECTOR</span></strong></span></span><br />
<span style="display: block; text-align: center;"><span style="display: block; text-align: center;"><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">(SORTARE IN ORDINE CRESCATOARE)</span></strong></span></span><br />
<span style="display: block; text-align: center;"><br />
</span><br />
<ol><li><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">1.</span></strong> <strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">METODA DE SORTARE PRIN INTERSCHIMBARE</span></strong></li></ol><ul><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Aceasta metoda consta in parcurgerea sirului utilizand doi contori (<strong>i</strong> si <strong>j</strong>) . </span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Fiecare element <strong>a</strong></span><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">[i]</span></strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;"> se va compara cu toate elementele din dreapta sa, elemente de forma <strong>a[j]</strong>,cu <strong>j=i+1,n</strong></span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Daca <strong>a[i]&gt;a[j]</strong> atunci cele doua component e se vor interschimba</span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Obs: aceasta metoda nu este eficienta deoarece daca sirul ar fi de la inceput sortat sirul tot se parcurge realizand <strong>n(n-1)/2</strong> comparatii </span></li></ul><span style="display: block; text-align: justify;"><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">ALGORITMUL:</span></strong></span><span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Citeste <strong>n</strong></span></span><br />
Citeste sirul <strong>a</strong> cu <strong>n</strong> elemente<br />
Pentru <strong>i=1,n-1</strong> executa<br />
Pentru <strong>j=i+1,n</strong> executa<br />
Daca <strong>a[i]&gt;a[j]</strong> atunci<br />
{<br />
<span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">aux=a[i]</span></span><span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">a[i]=a[j]</span></span><span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">a[j]=aux</span></span><br />
}<br />
Afisare sir <strong>a</strong><br />
<strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">2.</span></strong> <strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">SORTAREA PRIN METODA BULELOR</span></strong><br />
<ul><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Metoda consta in parcurgerea sirului ori de cate ori este nevoie pana cand sirul devine sortat sau cat timp sirul nu este sortat</span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Inainte de parcurgerea sirului se presupune de fiecare daca ca sirul ar fi sortat utilizand o variabila logica</span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">La fiecare iteratie sirul se va parcurge pana la ultima componenta care nu este sortata .</span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Parcurgerea sirului consta in compararea de fiecare data a doua componente de pe pozitii consecutive, de forma <strong>a[i]</strong> si <strong>a[i+1]</strong></span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Daca <strong>a[i]&gt;a[i+1]</strong> cele doua componente se vor interschimba</span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Daca la o parcurgere a sirului exista cel putin o interschimbare inseamna ca sirul inca nu este sigur sortat si se reia parcurgerea sirului</span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Daca la o parcurgere a sirului nu exista nicio interschimbare atunci cu siguranta sirul este sortat </span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Obs : metoda are rolul de a transporta , la fiecare parcurgere a sirului, valoare maxima dintre componente nesortate si de a o plasa pe pozitia finala in sirul sortat . </span></li></ul><span style="display: block; text-align: justify;"><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">ALGORITMUL</span></strong></span><br />
<span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Citeste <strong>n</strong></span></span><br />
Citeste sirul <strong>a</strong> cu <strong>n</strong> elemente<br />
<strong>executa</strong><br />
{<span style="font-family: 'Times New Roman',serif; font-size: 12pt;">ok=1</span><br />
// se presupune ca sirul este sortat<br />
Pentru <strong>i=1,n-1</strong> executa<br />
Daca <strong>a[i]&gt;a[i+1]</strong> atunci<br />
{<strong>aux=a[i]</strong><br />
<span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">a[i]=a[i+1]</span></span><span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">a[i+1]=aux</span></span><span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">ok=0</span></span><br />
}}<br />
<strong>cat timp (ok==0)</strong><br />
Se afiseaza sirul <strong>a</strong><br />
<strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">3.</span></strong> <strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">METODA DE SORTARE PRIN NUMARARE</span></strong><br />
<ul><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Este o metoda ineficienta ca spatiu de memorie deoarece utilizeaza <strong>3</strong> siruri astfel : sirul <strong>a</strong> cel care trebuie sortat, sirul <strong>b</strong> cel in care se vor plasa elementele sortate si respectiv sirul <strong>nr</strong> avand semnificatia ca <strong>nr[i]=</strong> numarul elementelor sirului <strong>a</strong> care sunt mai mici decat <strong>a[i]</strong></span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Pentru formarea sirului nr se parcurge sirul cu doua foruri avand variabilele contor <strong>i</strong> si respectiv <strong>j</strong> </span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Fiecare element <strong>a[i]</strong> se compara cu toate elementele din dreapta sa, elemente de forma <strong>a[j]</strong> cu <strong>j=i+1,n</strong></span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Daca <strong>a[i]&gt;a[j]</strong> creste <strong>nr[i]</strong> cu o unitate , in caz contrar creste <strong>nr[j]</strong> cu o unitate</span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Dupa formarea sirului <strong>nr</strong> , orice componenta <strong>nr[i]</strong>, la care se aduna o unitate reprezinta pozitia elementului <strong>a[i]</strong> in sirul sortat</span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Sirul sortat b se formeaza dupa urmatoarea regula : <strong>b[nr</strong></span><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">[</span></strong><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">i]+1]=a[i]</span></strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">, unde <strong>i=1,n</strong></span></li></ul><span style="display: block; text-align: justify;"><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">ALGORITMUL</span></strong></span><span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Citeste <strong>n</strong></span></span><br />
Citeste sirul <strong>a</strong> cu <strong>n</strong> elemente<br />
Pentru <strong>i=1,n</strong> executa<br />
Pentru <strong>j=i+1, n</strong> executa<br />
Daca <strong>a[i]&gt;a[j]</strong> atunci <strong>nr[i]=nr[i]+1</strong><br />
Altfel <strong>nr[j]=nr[j]+1</strong><br />
Pentru <strong>i=1,n</strong> executa<br />
<strong>b[nr</strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">[i]+1]=a[i]</span><br />
<br />
Afiseaza sirul <strong>b</strong><br />
<strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">4.</span></strong> <strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">METODA DE SORTARE PRIN SELECTIE DIRECTA</span></strong><br />
<ul><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Metoda consta in parcurgerea sirului de la prima componenta pana la componenta <strong>n-1</strong> inclusiv</span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">La pasul <strong>i</strong> componentele <strong>a[1],a[2],...,a[i-1]</strong> sunt deja sortate . </span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">La pasul <strong>i</strong> se determina valoarea minima respectiv pozitia elementului minim dintrea componentele <strong>a[i],a[i+1],...,a[n]</strong> . </span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Fie <strong>p</strong> pozitia elementului minim . Daca <strong>p</strong> este diferit de <strong>i</strong> atunci componentele <strong>a[i]</strong> si <strong>a[p]</strong> se vor interschimba </span></li></ul><span style="display: block; text-align: justify;"><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">ALGORITMUL</span></strong></span><br />
Citeste <strong>n</strong><br />
Citeste sirul <strong>a</strong> cu <strong>n</strong> componente<br />
Pentru <strong>i=1,n-1</strong> executa<br />
{<br />
<strong>min=a[i]</strong><br />
<strong>p=i</strong><br />
Pentru <strong>j=i+1,n</strong> executa<br />
Daca <strong>a[j]&lt;min</strong> atunci<br />
{m<strong>in=a[j]</strong><br />
<strong>p=j</strong><br />
}<br />
Daca <strong>p!=i</strong> atunci<br />
{<br />
<strong>a[p]=a[i]</strong><br />
<span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">a[i]=min</span></span><br />
}<br />
}<br />
Afiseaza sirul <strong>a</strong><br />
<strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">5.</span></strong> <strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">METODA DE SORTARE PRIN INSERTIE DIRECTA</span></strong><br />
<ul><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Aceasta metoda consta in parcurgerea sirului incepand cu a doua componenta pana la final</span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">La pasul <strong>i</strong> elementele <strong>a[1],a[2],..,a[i-1]</strong> sunt deja sortate si trebuie sa plasam elementul <strong>a[i]</strong> printre elementele deja sortate </span></li><li><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Pentru a plasa elementul <strong>a[i]</strong> vom parcurge urmatorii pasi :</span></li></ul><span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">i) Se retine <strong>a[i]</strong> intr-o variabila temporara <strong>t</strong></span></span><span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">ii) Indicele <strong>j</strong> parcurge in ordine inversa elementele deja sortate</span></span><span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">iii) Cat timp <strong>a[j]&gt;t</strong> si <strong>j&gt;0</strong> elementul <strong>a[j]</strong> se deplaseaza la dreapta cu o unitate, iar <strong>j</strong> descreste cu o unitate</span></span><span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">iv) In final <strong>t</strong> se va pozitiona pe urmatoare componenta pentru care nu a mai fost adevarata conditia : <strong>a[j+1]=t</strong></span></span><span style="display: block; text-align: justify;"><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">ALGORITMUL</span></strong></span><br />
Citeste <strong>n</strong><br />
Citeste sirul <strong>a</strong> cu <strong>n</strong> elemente<br />
Pentru <strong>i=2,n</strong> executa<br />
{<br />
<span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">t=a[i]</span></span><span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">j=i-1</span></span><br />
Cat timp <strong>a[j]&gt;t</strong> si <strong>j&gt;0</strong> executa<br />
{<br />
<span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">a[j+1]=a[j]</span></span><span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">j=j-1</span></span><br />
}<br />
<strong>a[j+1]=t</strong><br />
}<br />
Afiseaza sirul <strong>a</strong>
    </div>
  </body>
</html>