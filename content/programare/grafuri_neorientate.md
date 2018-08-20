---
title: "Grafuri Neorientate"
date: 2018-08-20T03:16:20+03:00
draft: false
---

<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
<h1 id="toc0"><a name="NOŢIUNI INTRODUCTIVE. DEFINIŢII"></a><span style="color: #008000;">NOŢIUNI INTRODUCTIVE. DEFINIŢII</span></h1>
 <h1 id="toc1"><a name="file:Grafuri_neorientate.doc"></a><a href="files/Grafuri_neorientate.doc">Grafuri_neorientate.doc</a></h1>
 <br />
<h1 id="toc2"><a name="METODE DE REPREZENTARE"></a><span style="color: #008000;">METODE DE REPREZENTARE</span></h1>
 <span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">Există mai multe moduri de reprezentare a grafurilor, alegerea făcându-se în funcţie de tipurile de operaţii care urmează să se efectueze:</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">1. <u>Matricea de adiacenţă</u>: face o asociere între noduri şi indicii matricei. Este o matrice simentrică faţă de diagonala principală, cu nXn elemente, unde n este numărul de noduri.</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">aij= 1, dacă muchia [i,j] există</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">0, dacă muchia [i,j] nu există</span><br />
<span style="display: block; text-align: justify;"><u><span style="font-family: 'Tahoma','sans-serif'; font-size: 10.6667px;">Obs.</span></u><span style="font-family: 'Tahoma','sans-serif'; font-size: 10.6667px;"> Numarul de valori “1” de pe linia “i” (sau de pe coloana “i”) reprezintă gradul nodului “i”.</span></span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">2. <u>Matricea lanţurilor</u>: este o matrice pătratică simetrică faţă de diagonala principală cu nXn elemente, unde n este numărul de noduri.</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">aij= 1, dacă lanţul de la i la j există</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">0, dacă lanţul de la i la j nu există</span><br />
<span style="display: block; text-align: justify;"><u><span style="font-family: 'Tahoma','sans-serif'; font-size: 10.6667px;">Obs.</span></u><span style="font-family: 'Tahoma','sans-serif'; font-size: 10.6667px;"> matricea lanţurilor se obţine din matricea de adiacenţă prin aplicarea algoritmului lui Roy-Warshall. Se utilizează pentru a arăta dacă un graf este conex sau nu. Dacă are în matrice numai valori de 1, insemnă că graful este conex.</span></span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">3. <u>Matricea costurilor</u>: pentru reprezentarea grafurilor valorice. Este o matrice simentrică faţă de diagonala principală, cu nXn elemente, unde n este numărul de noduri.</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">aij= costul muchiei, dacă muchia [i,j] există</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">0, dacă muchia [i,j] nu există</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">∞, dacă este o problemă de minim (-∞, dacă este o problemă de maxim)</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">4. <u>Lista de adiacenţă</u> reprezentată folosind <u>alocarea dinamică</u> se reţine pentru fiecare nod lista vecinilor</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">a) se foloseşte un vector care reţine adresa de început a listei vecinilor fiecărui nod</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">b) se foloseşte o listă care reţine adresa de început a listei vecinilor fiecărui nod</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">5. <u>Lista de adiacenţă</u> reprezentată folosind <u>tablouri bidimensionale</u> cu n+2m coloane şi două linii (n=numărul de noduri, m=numărul de muchii), pe prima linie se scriu numerele de la 1 la n+2m, iar pe a doua se reţine în coloanele de la 1 la n coloana în care apare primul vecin al său, iar pe coloanele de la n+1 la n+2m coloana pe care se află următorul vecin al nodului.</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">6. <u>Doi vectori</u>: se reţine un capăt al muchiei într-un vector, iar celălalt capăt în al doilea vector. Lungimea vecorilor este egală cu numărul de muchii.</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">7. <u>Un vector de muchii</u>: se defineşte tipul muchie (reţine capetele muchiei si eventual costul-pentru grafuri valorizate), apoi definim un vector de muchii care are atâtea componente câte muchii sunt</span><br />
<span style="display: block; font-family: Tahoma,sans-serif; font-size: 10.6667px; text-align: justify;">8. <u>lista de muchii</u>: se defineşte tipul nod care reţine capetele muchiei şi eventual costul - pentru grafuri valorice.</span><br />
<h1 id="toc3"><a name="Probleme propuse:"></a><span style="font-size: 13px;">Probleme propuse:</span></h1>
 <h1 id="toc4"><a name="Fie G un graf neorientat, cu n vârfuri si m muchii, reprezentat prin matricea de adiacentă."></a><span style="font-size: 13px;">Fie G un graf neorientat, cu n vârfuri si m muchii, reprezentat prin matricea de adiacentă.</span></h1>
 <h1 id="toc5"><a name="Să se realizeze programe, în C/C++, care:"></a><span style="font-size: 13px;">Să se realizeze programe, în C/C++, care:</span></h1>
 <h1 id="toc6"><a name="a) afisează gradele tuturor vârfurilor;"></a><span style="font-size: 13px;">a) afisează gradele tuturor vârfurilor;</span></h1>
 <h1 id="toc7"><a name="b) afisează vârfurile de grad par;"></a><span style="font-size: 13px;">b) afisează vârfurile de grad par;</span></h1>
 <h1 id="toc8"><a name="c) afisează vârfurile izolate;"></a><span style="font-size: 13px;">c) afisează vârfurile izolate;</span></h1>
 <h1 id="toc9"><a name="d) afisează vârfurile terminale;"></a><span style="font-size: 13px;">d) afisează vârfurile terminale;</span></h1>
 <h1 id="toc10"><a name="e) verifică dacă graful are vârfuri izolate;"></a><span style="font-size: 13px;">e) verifică dacă graful are vârfuri izolate;</span></h1>
 <h1 id="toc11"><a name="t) verifică dacă graful are vârfuri terminale;"></a><span style="font-size: 13px;">t) verifică dacă graful are vârfuri terminale;</span></h1>
 <h1 id="toc12"><a name="g) verifică dacă graful are vârfuri interioare (nu sunt nici izolate nici terminale);"></a><span style="font-size: 13px;">g) verifică dacă graful are vârfuri interioare (nu sunt nici izolate nici terminale);</span></h1>
 <h1 id="toc13"><a name="h) verifică dacă graful are toate vârfurile izolate;"></a><span style="font-size: 13px;">h) verifică dacă graful are toate vârfurile izolate;</span></h1>
 <h1 id="toc14"><a name="i) verifică dacă graful are toate vârfurile interioare (nu sunt nici izolate nici terminale);"></a><span style="font-size: 13px;">i) verifică dacă graful are toate vârfurile interioare (nu sunt nici izolate nici terminale);</span></h1>
 <h1 id="toc15"><a name="j) afisează gradul unui vârf dat;"></a><span style="font-size: 13px;">j) afisează gradul unui vârf dat;</span></h1>
 <h1 id="toc16"><a name="k) afisează vecinii unui nod dat, vf;"></a><span style="font-size: 13px;">k) afisează vecinii unui nod dat, vf;</span></h1>
 <h1 id="toc17"><a name="l) verifică dacă un vârf dat este terminal, izolat sau interior;"></a><span style="font-size: 13px;">l) verifică dacă un vârf dat este terminal, izolat sau interior;</span></h1>
 <h1 id="toc18"><a name="m) afisează gradul cel mai mare si toate vârfurile care au acest grad"></a><span style="font-size: 13px;">m) afisează gradul cel mai mare si toate vârfurile care au acest grad</span></h1>
 <h1 id="toc19"><a name="n) afisează frecventa vârfurilor:"></a><span style="font-size: 13px;">n) afisează frecventa vârfurilor:</span></h1>
 <h1 id="toc20"><a name="izolate : n1"></a><span style="font-size: 13px;">izolate : n1</span></h1>
 <h1 id="toc21"><a name="terminale : n2"></a><span style="font-size: 13px;">terminale : n2</span></h1>
 <h1 id="toc22"><a name="interioare : n3"></a><span style="font-size: 13px;">interioare : n3</span></h1>
 <br />
<h3 id="toc23"><a name="interioare : n3--Aplicaţii cu grafuri neorientate"></a><span style="color: #e60e4e;">Aplicaţii cu grafuri neorientate </span></h3>
 <strong>1. Din fişierul graf.in se citeşte de pe prima linie valorile n (numărul de noduri) şi m (numărul de muchii) ale unui graf neorientat G=(X,U). De pe următoarele m linii se citeşte lista muchiilor. Scrieţi funcţiile pentru:</strong><br />
a) Citirea grafului;<br />
b) Afişaţi matricea de adiacenţă a grafului;<br />
c) Afişaţi gradele tuturor nodurilor<br />
d) Afişaţi toate nodurile de grad maxim<br />
e) Afişaţi toate nodurile terminale<br />
f) Afişaţi toate nodurile izolate<br />
<strong>2. Din fişierul graf.in se citeşte de pe prima linie valorile n (numărul de noduri) şi m (numărul de muchii) ale unui graf neorientat G=(X,U). De pe următoarele m linii se citeşte lista muchiilor. Scrieţi funcţiile pentru:</strong><br />
a) Citirea grafului;<br />
b) Afişaţi listele de adiacenta;<br />
c) Afisati varfurile cu numar maxim de vecini;<br />
d) Afisati varfurile cu un singur vecin;<br />
e) Afisati varfurile fara vecini<br />
<strong>3. Din fişierul graf.in se citeşte de pe prima linie valorile n (numărul de noduri) şi m (numărul de muchii) ale unui graf neorientat G=(X,U). De pe următoarele m linii se citeşte lista muchiilor. Scrieţi funcţiile pentru:</strong><br />
a) Citirea grafului;<br />
b) Afişaţi matricea de adiacenţă a grafului;<br />
c) Afişaţi parcurgerile in latime din fiecare varf<br />
<strong>4. Din fişierul graf.in se citeşte de pe prima linie valorile n (numărul de noduri) şi m (numărul de muchii) ale unui graf neorientat G=(X,U). De pe următoarele m linii se citeşte lista muchiilor. Scrieţi funcţiile pentru:</strong><br />
a) Citirea grafului;<br />
b) Afişaţi matricea de adiacenţă a grafului;<br />
c)Afişaţi parcurgerile in adancime din fiecare varf<br />
<strong>5. Din fişierul graf.in se citeşte de pe prima linie valorile n (numărul de noduri) şi m (numărul de muchii) ale unui graf neorientat G=(X,U). De pe următoarele m linii se citeşte lista muchiilor. Scrieţi funcţiile pentru:</strong><br />
a) Citirea grafului;<br />
b) Afişaţi matricea de adiacenţă a grafului;<br />
c) Afişaţi matricea lanţurilor<br />
<h2 id="toc24"> </h2>

    </div>
  </body>
</html>