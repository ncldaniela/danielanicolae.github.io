---
title: "Recursivitate"
date: 2018-08-20T03:16:20+03:00
weight: 1
draft: false
---

<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;"><strong>Recursivitatea</strong> este un mecanism general de elaborare a algoritmilor. O <u><span style="color: #0000ff;">functie</span></u> se numeste <u><span style="color: #0000ff;">recursiva</span></u> daca ea se autoapeleaza, fie <em><span style="color: #0000ff;">direct</span></em> (in definitia ei, se face apel la ea insasi), fie <em><span style="color: #0000ff;">indirect</span></em> (functia X apeleaza functia Y, care apeleaza functia X).</span><br />
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;">Recursivitatea a aparut din necesitati practice date de transcrierea directa a formulelor matematice recursive. Apoi, acest mecanism a fost extins, fiind utilizat in elaborarea multor algoritmi.</span><br />
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;">Pornim de la un exemplu : Sa se calculeze n !</span><br />
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;">Se observa ca n !=(n-1) !*n si se stie ca 0 !=1. Asadar :</span><br />
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;">5 !=4 !*5</span><br />
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;">4 !=3 !*4</span><br />
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;">3 !=2 !*1</span><br />
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;">1 !=0 !*1</span><br />
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;">0 !=1 (prin conventie matematica)</span><br />
<span style="font-family: 'Times New Roman','serif'; font-size: 16px;">Functia recursiva se va scrie astfel:</span><br />
<span style="color: #0000ff; display: block; font-family: "Courier New"; font-size: 13.3333px; text-align: justify;">long factorial(int n)</span><br />
<span style="color: #0000ff; display: block; font-family: "Courier New"; font-size: 13.3333px; text-align: justify;">{if(n==0) return 1;</span><br />
<span style="color: #0000ff; display: block; font-family: "Courier New"; font-size: 13.3333px; text-align: justify;">else return factorial(n-1)*n;}</span><br />
<span style="color: #0000ff; display: block; font-family: "Courier New"; font-size: 13.3333px; text-align: justify;">void main()</span><br />
<span style="color: #0000ff; display: block; font-family: "Courier New"; font-size: 13.3333px; text-align: justify;">{cout&lt;&lt;factorial(5) ;}</span><br />
<span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman','serif'; font-size: 16px;">Se observa ca functia factorial se autoapeleaza. Autoapelul se realizeaza prininstructiunea</span><span style="color: #0000ff; font-family: 'Courier New'; font-size: 13.3333px;">return factorial(n-1)*n</span><span style="font-family: 'Courier New'; font-size: 13.3333px;">.</span></span><br />
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;">Sa vedem care este mecanismul prin care subprogramele se pot autoapela. Se stie ca la apelul fiecarui subprogram, se genereaza un nou nivel in segmentul de stiva, corespunzator acelui apel. Pe acel nivel se memoreaza :</span><br />
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;">- valorile parametrilor transmisi prin valoare</span><br />
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;">- adresele parametrilor transmisi prin referinta</span><br />
<span style="display: block; font-family: "Times New Roman",serif; font-size: 16px; text-align: justify;">- variabilele locale</span><br />
Fiecare apel de functie lucreaza cu datele aflate pe nivelul corespunzator acelui apel. La iesirea din apelul unei functii, nivelul respectiv se elibereaza si datele aflate acolo se pierd. Exista posibilitatea ca subprogramul sa lucreze direct cu variabilele globale, dar in acest caz, subprogramul isi pierde independenta.<br />
<br />
Cum gandim un algoritm recursiv ?<br />
Iata cateva exemple de rationament recursiv :<br />
- O camera de luat vederi are in obiectiv un televizor care transmite imaginile primite de la camera. In televizor se vede un televizor in care se vede un televizor…<br />
- Anunt : Azi nu se fumeaza !<br />
O gandire recursiva exprima concentrat o anumita stare, care se repeta la infinit. Aceasta gandire se aplica in elaborarea algoritmilor recursivi cu o modificare esentiala: adaugarea conditiei de terminare. In absenta acestei conditii nu se poate vorbi despre un algoritm deoarece acestia sunt finiti. Din acest punct de vedere, exemplele de mai sus nu sunt corecte.Atunci cand gandim un algoritm recursiv, privim problema la un anumit nivel. Ce se intampla la acel nivel se va intampla la toate celelalte.<br />
<strong><u>Observatii</u> :</strong><br />
<strong>- In cazul unui numar mare de autoapelari, exista posibilitatea ca segmentul de stiva sa se ocupe total, caz in care programul se va termina cu eroarea STACK OVERFLOW. Aceasta se intampla mai ales atunci cand conditia de terminare este pusa gresit si subprogramul se apeleaza la nesfarsit.</strong><br />
<strong>- Pentru orice algoritm recursiv exista unul iterativ care rezolva aceeasi problema.</strong><br />
<strong>- Mecanismul recursivitatii inlocuieste instructiunile repetitive.</strong><br />
<strong>- Datorita faptului ca la fiecare autoapel se ocupa o zona de memorie, recursivitatea este eficienta numai daca numarul de autoapelari nu este prea mare pentru a nu se ajunge la umplerea zonei de memorie alocata.</strong><br />
<strong>- Recursivitatea ofera avantajul unor solutii mai clare pentru probleme si a unei lungimi mai mici a programului. Ea prezinta insa dezavantajul unui timp mai mare de executie si a unui spatiu de memorie alocata mai mare. Este de preferat ca atunci cand programul recursiv poate fi transformat cu usurinta intr-unul iterativ sa se faca apel la cel din urma (vezi sirul lui Fibonacci)</strong><br />
<strong><u>Exemplu</u></strong> de functii ce calculeaza produsul primelor n numere naturale :<br />
<h1 id="toc0"><a name="Functia iterativa"></a>Functia iterativa</h1>
 <span style="font-family: 'Courier New'; font-size: 13.3333px;">int f(int n)</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;">{int i=1, P=1;</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;"> while <strong><span style="color: #ff0000;">(i&lt;=n)</span></strong></span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;"> {P=P*i ;</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;"> i++ ;}</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;">return P ;}</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;"> void main()</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;">{int n=5;</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;"> cout&lt;&lt;f(n);}</span><br />
<h1 id="toc1"><a name="Functia recursiva 1"></a>Functia recursiva 1</h1>
 <span style="font-family: 'Courier New'; font-size: 13.3333px;">int n;</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;">int f(int i)</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;">{if <strong><span style="color: #ff0000;">(i&lt;=n)</span></strong></span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;"> return i*f(i+1);</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;">else return 1 ;}</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;">void main()</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;">{n=5;</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;"> cout&lt;&lt;f(1);}</span><br />
<h1 id="toc2"><a name="Functia recursiva 2"></a>Functia recursiva 2</h1>
 <span style="font-family: 'Courier New'; font-size: 13.3333px;">int f(int i)</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;">{if (i&gt;1)</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;"> return i*f(i-1);</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;">else return 1 ;}</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;">void main()</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;">{int n=5;</span><br />
<span style="font-family: 'Courier New'; font-size: 13.3333px;"> cout&lt;&lt;f(n);}</span><br />
Observati ca la primele doua subprograme conditia de continuare (a iteratiei respectiv a autoapelului este aceeasi)<br />
<strong><span style="color: #ff0000;">Recomandare</span></strong> : inainte de elaborarea algoritmilor recusivi generati mai intai subprogramul iterativ apoi treceti-l in subprogram recursiv.<br />
<h2 id="toc3"><a name="Functia recursiva 2-TESTE GRILA"></a>TESTE GRILA</h2>
 <a href="/files/Grile%20recursivitate3.pdf">Grile recursivitate3.pdf</a><br />
<a href="/files/grile%20recursivitate1.doc">grile recursivitate1.doc</a><br />
<a href="/files/Grile%20recursivitate%202.doc">Grile recursivitate 2.doc</a><br />
<h2 id="toc4"><a name="Functia recursiva 2-Aplicatii rezolvate online"></a><strong>Aplicatii rezolvate online</strong></h2>
 <a class="wiki_link_ext" href="http://info.mcip.ro/?cap=Recursivitate" rel="nofollow">http://info.mcip.ro/?cap=Recursivitate</a>
    </div>
  </body>
</html>