---
title: "Liste Liniare"
date: 2018-08-20T03:16:20+03:00
draft: false
---

<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
<h2 id="toc0"> </h2>
 <span style="font-family: 'Times New Roman'; font-size: 11pt;">Structurile dinamice de date sunt date structurate ale caror componente se aloca in mod dinamic.</span><br />
<h2 id="toc1"><a name="x-Avantajul alocarii dinamice fata de alocarea acelorasi structuri de date in mod static (in segmentul de date) sau volatil (in segmentul de stiva) sunt:"></a><span style="font-family: 'Times New Roman'; font-size: 11pt; line-height: 1.5;">Avantajul alocarii dinamice fata de alocarea acelorasi structuri de date in mod static (in segmentul de date) sau volatil (in segmentul de stiva) sunt:</span></h2>
 <h2 id="toc2"><a name="x-- memorie suplimentara pentru programe"></a><span style="font-family: 'Times New Roman'; font-size: 11pt; line-height: 1.5;">- memorie suplimentara pentru programe</span></h2>
 <h2 id="toc3"><a name="x-- posibilitatea de a utiliza aceasta memorie"></a><span style="font-family: 'Times New Roman'; font-size: 11pt; line-height: 1.5;">- posibilitatea de a utiliza aceasta memorie</span></h2>
 <h2 id="toc4"><a name="x-Alocarea dinamica a componentelor structurii impune un mecanism prin care o noua componenta aparuta este legata in succesiune logica de corpul structurii deja format pana atunci. Rezulta ca fiecare componenta, pe langa informatia propriu-zisa pe care o detine, trebuie sa contina si o informatie de legatura cu componenta cu care se leaga logic in succesiune. Aceasta informatie de legatura va fi adresa componentei spre care se realizeaza succesiunea logica, iar mecanismul se mai numeste si alocare inlantuita dupa adrese."></a><span style="color: #3366ff; font-family: 'Times New Roman'; font-size: 11pt;">Alocarea dinamica a componentelor structurii impune un mecanism prin care o noua componenta aparuta este legata in succesiune logica de corpul structurii deja format pana atunci. Rezulta ca fiecare componenta, pe langa informatia propriu-zisa pe care o detine, trebuie sa contina si o informatie de legatura cu componenta cu care se leaga logic in succesiune. Aceasta informatie de legatura va fi adresa componentei spre care se realizeaza succesiunea logica, iar mecanismul se mai numeste si </span><em><span style="font-family: Arial; font-size: medium; line-height: 1.5;"><u><span style="color: #3366ff; font-family: 'Times New Roman'; font-size: 11pt;">alocare inlantuita dupa adrese</span></u></span></em><span style="color: #3366ff; font-family: 'Times New Roman'; font-size: 11pt;">.</span></h2>
 <h2 id="toc5"><a name="x-In HEAP, structura respectiva va avea zone alocate componentelor sale in locurile gasite disponibile, care nu se succed intotdeauna in ordinea in care este realizata inlantuirea logica."></a><span style="font-family: 'Times New Roman'; font-size: 11pt; line-height: 1.5;">In HEAP, structura respectiva va avea zone alocate componentelor sale in locurile gasite disponibile, care nu se succed intotdeauna in ordinea in care este realizata inlantuirea logica.</span></h2>
 <h2 id="toc6"><a name="x-In functie de tipul inlantuirii realizate intre componente, exista urmatoarele tipuri de organizari:"></a><span style="font-family: 'Times New Roman'; font-size: 11pt; line-height: 1.5;">In functie de tipul inlantuirii realizate intre componente, exista urmatoarele tipuri de organizari:</span></h2>
 <h2 id="toc7"><a name="x-- structuri liniare (de exeplu o lista care prelucreaza elevii care se inscriu la un examen)"></a><span style="font-family: 'Times New Roman'; font-size: 11pt; line-height: 1.5;">- structuri liniare (de exeplu o lista care prelucreaza elevii care se inscriu la un examen)</span></h2>
 <h2 id="toc8"><a name="x-o liste simplu inlantuite (liniare si circulare)"></a><span style="font-family: 'Courier New'; font-size: 11pt;">o</span> <span style="font-family: 'Times New Roman'; font-size: 11pt;">liste simplu inlantuite (liniare si circulare)</span></h2>
 <h2 id="toc9"><a name="x-o liste dublu inlantuite (liniare si circulare)"></a><span style="font-family: 'Courier New'; font-size: 11pt;">o</span> <span style="font-family: 'Times New Roman'; font-size: 11pt;">liste dublu inlantuite (liniare si circulare)</span></h2>
 <h2 id="toc10"><a name="x-- structuri arborescente (de exemplu reteaua ierarhica a angajatilor dintr-o firma)"></a><span style="font-family: 'Times New Roman'; font-size: 11pt; line-height: 1.5;">- structuri arborescente (de exemplu reteaua ierarhica a angajatilor dintr-o firma)</span></h2>
 <h2 id="toc11"><a name="x-- structuri retea (de exemplu o retea de orase care schimba materiale, combustibili etc)"></a><span style="font-family: 'Times New Roman'; font-size: 11pt; line-height: 1.5;">- structuri retea (de exemplu o retea de orase care schimba materiale, combustibili etc)</span></h2>
 <br />
<span style="display: block; text-align: justify;"><br />
<h4 id="toc12"><a name="x-- structuri retea (de exemplu o retea de orase care schimba materiale, combustibili etc)--O listã înlãntuitã este o structurã dinamicã, flexibilã, care se poate adapta cerintelor aplicatiei, fãrã ca utilizatorul sã fie preocupat de posibilitatea depãsirii unei dimensiuni estimate initial ."></a><span style="font-size: 130%;">O listã înlãntuitã este o structurã dinamicã, flexibilã, care se poate adapta cerintelor aplicatiei, fãrã ca utilizatorul sã fie preocupat de posibilitatea depãsirii unei dimensiuni estimate initial .</span></h4>
 <h4 id="toc13"><a name="x-- structuri retea (de exemplu o retea de orase care schimba materiale, combustibili etc)--Avantajul folosirii listelor consta in gestionarea dinamica a memoriei. Alocarea sau eliberarea nodurilor se face dinamic, la fiecare inserare respectiv stergere,ceea ce face ca nodurile listei sa fie plasate dispersat in memorie (in cazul vectorilor – structuri de date omogene alocate static, zona de memorie folosita este contigua). Legatura dintre nodurile invecinate trebuie facuta logic explicit de catre programator, prin pastrarea informatiilor de legatura in fiecare nod (pe langa valoarea utila)."></a><span style="font-size: 130%;">Avantajul folosirii listelor consta in gestionarea dinamica a memoriei. Alocarea sau eliberarea nodurilor se face dinamic, la fiecare inserare respectiv stergere,ceea ce face ca nodurile listei sa fie plasate dispersat in memorie (in cazul vectorilor – structuri de date omogene alocate static, zona de memorie folosita este contigua). Legatura dintre nodurile invecinate trebuie facuta logic explicit de catre programator, prin pastrarea informatiilor de legatura in fiecare nod (pe langa valoarea utila).</span></h4>
 </span><br />
<span style="color: #008000; font-size: 1.3em; line-height: 1.5;"><strong>liste simplu inlantuite</strong></span><br />
<img src="http://ocw.cs.pub.ro/courses/_media/sd-ca/playground/lista_simplu.png" alt="external image lista_simplu.png" title="external image lista_simplu.png" /><br />
<img src="http://ocw.cs.pub.ro/courses/_media/sd-ca/playground/lista_circ_simplu.png" alt="external image lista_circ_simplu.png" title="external image lista_circ_simplu.png" /><br />
<img src="http://andreidiaconeasa.site90.com/imagini/lista.jpg" alt="external image lista.jpg" title="external image lista.jpg" /><br />
<h1 id="toc14"><a name="liste dublu inlantuite"></a><span style="color: #008000;">liste dublu inlantuite</span></h1>
 <span style="color: #008000;"><img src="http://ocw.cs.pub.ro/courses/_media/sd-ca/playground/lista_dublu.png" alt="external image lista_dublu.png" title="external image lista_dublu.png" style="height: 102px; width: 800px;" /></span><br />
<br />
<img src="http://ocw.cs.pub.ro/courses/_media/sd-ca/playground/lista_circ_dublu.png" alt="external image lista_circ_dublu.png" title="external image lista_circ_dublu.png" /><br />


<table class="wiki_table">
    <tr>
        <td><h2 id="toc15"><a name="liste dublu inlantuite-PROGRAME SURSA"></a><span style="color: #008000;">PROGRAME SURSA</span></h2>
 <h2 id="toc16"> </h2>
</td>
        <td><h2 id="toc17"><a name="liste dublu inlantuite-PROBLEME PROPUSE"></a><span style="color: #008000;">PROBLEME PROPUSE</span></h2>
</td>
    </tr>
</table>

<br />


<table class="wiki_table">
    <tr>
        <td><a href="/files/creare.cpp">creare.cpp</a><br />
</td>
        <td><a href="/files/liste_simplu_inlantuite1.doc">liste_simplu_inlantuite1.doc</a><br />
</td>
    </tr>
    <tr>
        <td><a href="/files/liste_simplu_inlantuite.cxx">liste_simplu_inlantuite.cxx</a><br />
</td>
        <td><a href="/files/liste_simplu_inlantuite2.doc">liste_simplu_inlantuite2.doc</a><br />
</td>
    </tr>
    <tr>
        <td style="text-align: center;"><a href="/files/liste_dublu.cpp">liste_dublu.cpp</a><br />
</td>
        <td><br />
</td>
    </tr>
</table>

<h2 id="toc18"><a name="liste dublu inlantuite-GRILE"></a><span style="color: #008000;">GRILE</span></h2>
 <h2 id="toc19"><a name="liste dublu inlantuite-file:Grile_alocare_dinamica_C++.doc"></a><a href="/files/Grile_alocare_dinamica_C%2B%2B.doc">Grile_alocare_dinamica_C++.doc</a></h2>

    </div>
  </body>
</html>