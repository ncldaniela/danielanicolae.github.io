---
title: "Programare FoxPRO"
date: 2018-08-20T03:16:20+03:00
weight: 12
draft: false
---

<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
<span style="display: block; text-align: center;"><span style="font-family: 'Times New Roman',serif;">Mecanismele programarii în Visual FoxPro</span></span><br />
<span style="font-family: 'Times New Roman',serif;">Programarea în Visual FoxPro implica scrierea unor secvente de cod<strong><em>: instructiuni sub forma de comenzi, functii sau operatii pe care Visual FoxPro le poate interpreta</em></strong>. Acestea pot fi introduse în:</span><br />
<span style="font-family: 'Times New Roman',serif;">- fisiere de programe;</span><br />
<span style="font-family: 'Times New Roman',serif;">- ferestre de cod pentru evenimente sau metode în cadrul proiectantului de formulare (Form Designer) sau al proiectantului de clase (Class Designer);</span><br />
<span style="font-family: 'Times New Roman',serif;">- ferestre procedurale în cadrul proiectantului de meniuri (Menu Designer);</span><br />
<span style="font-family: 'Times New Roman',serif;">- ferestre procedurale în cadrul proiectantului de rapoarte (Report Designer).</span><br />
<h1 id="toc0"><a name="Crearea de programe"></a><u><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Crearea de programe</span></u></h1>
 <span style="font-family: 'Times New Roman',serif;">- 1. în <strong>Project Manager</strong> se selecteaza optiunea <strong>Programs</strong> din fila <strong>Code;</strong></span><br />
<span style="font-family: 'Times New Roman',serif;"> 2. se alege comanda <strong>New</strong></span><br />
<span style="font-family: 'Times New Roman',serif;">- 1. se alege comanda <strong>New</strong> din meniul <strong>File</strong></span><br />
<span style="font-family: 'Times New Roman',serif;">2. din caseta de dialog <strong>New</strong> se alege <strong>Program</strong></span><br />
<ol><li><span style="font-family: 'Times New Roman',serif;">3. se alege <strong>New File</strong>.</span></li></ol><span style="font-family: 'Times New Roman',serif;">- în fereastra <strong>Command</strong> se foloseste comanda <strong>MODIFY COMMAND</strong> </span><br />
<span style="display: block; text-align: left;"><strong><span style="font-family: 'Times New Roman',serif;">MODIFY COMMAND [<em>FileName</em> | ?] </span></strong></span><br />
<span style="font-family: 'Times New Roman',serif;">Visual Fox Pro va deschide o noua fereastra, în care se pot edita instructiunile programului.</span><br />
<h1 id="toc1"><a name="Salvarea programelor"></a><u><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Salvarea programelor</span></u></h1>
 <span style="font-family: 'Times New Roman',serif;">- din meniul <strong>File</strong> se alege <strong>Save</strong></span><br />
<span style="font-family: 'Times New Roman',serif;">- daca se salveaza un program creat în <strong>Progect Manager</strong> , acesta este automat adaugat proiectului.</span><br />
<br />
<h1 id="toc2"><a name="Modificarea programelor"></a><u><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Modificarea programelor</span></u></h1>
 <span style="font-family: 'Times New Roman',serif;">Înainte de a modifica un program, acesta trebuie redeschis prin una din urmatoarele metode:</span><br />
<span style="font-family: 'Times New Roman',serif;">- pentru programele cuprinse într-un proiect, se selecteaza în <strong>Project Manager</strong> si se alege comanda <strong>Modify</strong></span><br />
<span style="font-family: 'Times New Roman',serif;">- în meniul <strong>File</strong> se alege comanda <strong>Open</strong>. Din lista <strong>Files of Type</strong> se alege <strong>Program</strong>, se selecteaza fisierul de modificat si se alege comanda <strong>Open</strong>.</span><br />
<span style="font-family: 'Times New Roman',serif;">- Se foloseste comanda <strong>MODIFY COMMAND</strong> în care se specifica numele programului sau parametrul &quot;?&quot;.</span><br />
<h1 id="toc3"><a name="Rularea programelor"></a><u><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Rularea programelor</span></u></h1>
 <span style="font-family: 'Times New Roman',serif;">- daca programul este cuprins într-un proiect, se selecteaza din <strong>Project Manager</strong> si se alege comanda <strong>Run</strong>.</span><br />
<span style="font-family: 'Times New Roman',serif;">- Din meniul <strong>Program</strong> se alege comanda <strong>Do</strong></span><br />
<span style="font-family: 'Times New Roman',serif;">- Se foloseşte butonul de execuţie din bara de instrumente <img src="/files/external-1bef85c6d9df8188c556bb52f08c92a8https://domnultudor.wikispaces.com/site/embedthumbnail/placeholder?w=200&amp;h=50" alt="external image placeholder?w=200&amp;h=50" title="external image placeholder?w=200&amp;h=50" style="height: 50px; width: 200px;" /></span><br />
<span style="font-family: 'Times New Roman',serif;">- în fereastra de comenzi se foloseste comanda <strong>DO</strong></span><br />
<span style="display: block; text-align: left;"><strong><span style="font-family: 'Times New Roman',serif;">DO <em>ProgramName1</em> | <em>ProcedureName</em> [IN <em>ProgramName2</em>] [WITH <em>ParameterList</em>]</span></strong></span><br />
<br />
<span style="display: block; text-align: center;"><span style="font-family: 'Times New Roman',serif;">Conceptele de baza ale programării</span></span><br />
<span style="display: block; text-align: center;"><span style="display: block; text-align: center;"><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Variabile. Macrosubstituţia.</span></strong></span></span><br />
<strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Crearea unei variabile sau modificarea </span></strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">valorii acesteia se face prin una din metodele următoare:</span><br />
<strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">(1) memvar = expr</span></strong><br />
<span style="color: #0000ff; font-family: 'Times New Roman',serif; font-size: 12pt;">Exemplu: msal=1000</span><br />
<span style="color: #0000ff; font-family: 'Times New Roman',serif; font-size: 12pt;"> mdata=date()</span><br />
<strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">(2)</span></strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;"> <strong>STORE <em>expr</em> TO <em>lista var</em></strong></span><br />
<strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">O tehnica speciala de lucru cu variabile o reprezinta</span></strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;"> <strong>macrosubstitutia</strong>, prin care continutul unei variabile de tip sir de caractere este tratat ca numele altei variabile sau alt element FoxPro (câmp al unei baze de date, denumire fişier). Macrosubstituţia functionează ca şi cum în locul variabilei respective ar fi pus şirul de caractere conţinut de aceasta, fără apostrofurile delimitatoare.</span><br />
<span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Operatorul de macrosubstitutie este <strong>&amp;</strong>. ( &amp;&amp; indică un comentariu)</span><br />
<strong><span style="color: #0000ff; font-family: 'Times New Roman',serif; font-size: 12pt;">Exemplu</span></strong><span style="color: #0000ff; font-family: 'Times New Roman',serif; font-size: 12pt;">:1. a=”var” </span><br />
<span style="color: #0000ff; font-family: 'Times New Roman',serif; font-size: 12pt;"> var= ”Continutul variabilei var” </span><br />
<span style="color: #0000ff; font-family: 'Times New Roman',serif; font-size: 12pt;"> ? a &amp;&amp; se afisaza <strong>var</strong> </span><br />
<span style="color: #0000ff; font-family: 'Times New Roman',serif; font-size: 12pt;"> ? &amp;a &amp;&amp; rezultatul afisarii este <strong>Continutul variabilei var</strong> ? var &amp;&amp; rezultatul afisarii este <strong>Continutul variabilei var</strong> </span><br />
<strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Obs.:</span></strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;"> Dezavantajul este ca apare o problema de performanta pentru compilator, in sensul ca linia pe care apare, trebuie compilata &quot;din mers&quot; in momentul rularii.</span><br />
<br />
<strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Comenzi pentru afişarea variabilelor de memorie existente la un moment dat:</span></strong><br />
<br />
<span style="display: block; text-align: left;"><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">LIST / DISPLAY MEMORY [NOCONSOLE][TO PRINTER [PROMPT]| TO FILE &lt;file&gt;]</span></strong></span><br />
<br />
<span style="display: block; text-align: center;"><span style="font-family: 'Times New Roman',serif;">Manipularea datelor</span></span><br />
<strong><u><span style="font-family: 'Times New Roman',serif;">a) Operatori</span></u></strong><br />
<span style="display: block; text-align: justify;"><span style="font-family: 'Times New Roman',serif;">Operatoriiutilizati pentru a crea expresii în Visual FoxPro sunt <strong>operatori aritmetici, operatori relationali</strong>, <strong>operatori logici, operatori specifici şirurilor de caractere</strong>: concatenare (+,-) apartenenta $, etc, <strong>operatori specifici datelor calendaristice</strong>: adunare sau scadere numar de zile dintr-o data calendaristica, compararea a doua date.</span></span><br />
<strong><span style="color: #0000ff; font-family: 'Times New Roman',serif;">Exemplu:</span></strong><br />
<strong><span style="color: #0000ff; font-family: 'Times New Roman',serif;">1.</span></strong><span style="color: #0000ff; font-family: 'Times New Roman',serif;"> Fie urmatoarele valori de tip caracter stocate în variabilele v1 si v2:</span><br />
<span style="color: #0000ff; font-family: 'Times New Roman',serif;"> v1= &quot;Univ. &quot; şi v2=&quot;Stefan Cel Mare&quot;</span><br />
<strong><em><span style="color: #0000ff; font-family: 'Times New Roman',serif;">Expresia:</span></em></strong><span style="color: #0000ff; font-family: 'Times New Roman',serif;"> ? v1+v2 va avea ca efect afişarea pe ecran a valorii &quot; Univ. Stefan Cel Mare&quot;</span><br />
<strong><span style="color: #0000ff; font-family: 'Times New Roman',serif;">2. </span></strong><span style="color: #0000ff; font-family: 'Times New Roman',serif;"> Daca variabilele v1 si v2 au valorile următoare: </span><br />
<span style="color: #0000ff; font-family: 'Times New Roman',serif;"> v1= &quot; Str. Univ. &quot; şi v2=21</span><br />
<strong><em><span style="color: #0000ff; font-family: 'Times New Roman',serif;">Expresia:</span></em></strong><span style="color: #0000ff; font-family: 'Times New Roman',serif;"> ? v1+v2 va avea ca efect afisarea pe ecran a unui mesaj de eroare.</span><br />
<span style="display: block; text-align: center;"><br />
</span><br />
<strong><u><span style="font-family: 'Times New Roman',serif;">b) Comenzi</span></u></strong><br />
<span style="font-family: 'Times New Roman',serif;">Fiecare comandă determină executarea unei acţiuni. Sintaxa generala a unei comenzi este:</span><br />
<strong><span style="font-family: 'Times New Roman',serif;">Verb</span></strong><span style="font-family: 'Times New Roman',serif;"> &lt;clauza,&gt;&lt; clauza &gt;..</span><br />
<span style="font-family: 'Times New Roman',serif;">Unde: verb indica acţiunea ce trebuie executată iar clauzele sunt opţionale si furnizează informaţii suplimentare legate de modul cum se va executa actiunea</span><br />
<span style="display: block; text-align: left;"><strong><span style="font-family: 'Times New Roman',serif;">Daca o comanda este scrisa pe mai mult de o linie, atunci la sfarsitul fiecarei linii intermedare se va plasa simbolul “;”.</span></strong></span><br />
<br />
<ol><li><strong><em><span style="font-family: 'Times New Roman',serif;">1.</span></em></strong> <strong><em><u><span style="font-family: 'Times New Roman',serif;">Instructiuni (comenzi) de intrare-iesire </span></u></em></strong></li></ol><br />
<span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Sunt <em>instructiuni de afisare</em> si <em>instructiuni pentru citirea</em> de la tastatura.</span><br />
<br />
<span style="font-family: 'Times New Roman',serif; font-size: 12pt;">a) <strong><u>Instructiuni de afisare.</u></strong></span><br />
<span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Aceasta categorie de comenzi cuprinde urmatoarele instructiuni:</span><br />
<span style="display: block; text-align: left;"><strong><span style="font-family: 'Times New Roman',serif;">(1)</span></strong><span style="font-family: 'Times New Roman',serif;"> <strong>? <em>Expr1</em> [PICTURE <em>Cod_format</em>] | [FUNCTION <em>Cod_format</em>] |[AT <em>nColumn</em>] [FONT <em>Nume_font</em> [,<em>Dimens_Font</em>]</strong> </span></span><br />
<strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Efect:</span></strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;"> Afiseaza, pe ecran, valorile uneia sau mai multor expresii Visual FoxPro valide sau le tipareste la imprimanta, daca SET PRINTER este pe ON , conform valorilor clauzelor PICTURE, FUNCTION,etc.</span><br />
<span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Obs.: - clauza AT &lt;expN1&gt; defineste coloana unde se afiseaza &lt;expr1&gt;;</span><br />
<br />
<strong><u><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">b) Instructiuni de citire de la tastatura.</span></u></strong><br />
<span style="display: block; text-align: left;"><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">(1) ACCEPT <em>[&lt;cExpr&gt;</em> ] TO <em>&lt;memvar&gt;</em></span></strong></span><br />
<span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Se afiseaza pe ecran valoarea &lt;cExpr&gt; dupa care se asteapta introducerea unui <strong><em>sir de caractere</em></strong>, de la tastatura, ce se atribuie variabilei de memorie &lt;memvar&gt;.</span><br />
<span style="display: block; text-align: left;"><br />
</span><br />
<span style="display: block; text-align: left;"><strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">(2) INPUT [&lt;<em>cExpr&gt;</em> ] TO <em>&lt;memvar&gt;</em></span></strong></span><br />
<span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Se afiseaza pe ecran valoarea &lt;cExpr&gt; dupa care se asteapta introducerea unei <strong><em>expresii</em></strong> de la tastatura, a carei valoare se atribuie variabilei de memorie &lt;memvar&gt;.</span><br />
<strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;">Obs.:</span></strong><span style="font-family: 'Times New Roman',serif; font-size: 12pt;"> - comanda cere obligatoriu introducerea unei expresii; - pentru introducerea constantelor de tip sir sau data calendaristica se vor folosi delimitatorii specifici (&quot;,',[ ], resp. {}).</span><br />
<span style="display: block; text-align: left;"><br />
</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif;">-transformarea şirurilor de caractere in valori numerice</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif;">VAL(<em>cExpr</em>)</span><br />
<span style="display: block; text-align: center;"><span style="color: #339966;">ANEXA 2</span></span><span style="display: block; text-align: center;"><span style="display: block; text-align: center;"><strong><span style="color: #339966; font-family: 'Times New Roman',serif; font-size: 14pt;">Instrucţiuni (comenzi) de configurare</span></strong></span></span><br />
<br />
<strong><span style="color: #339966; font-family: 'Times New Roman',serif; font-size: 12pt;">Instructiuni pentru controlul formatului datei calendaristice</span></strong><br />
<span style="color: #339966; font-family: 'Times New Roman',serif; font-size: 12pt;">SET CENTURY ON/OFF / validează, respectiv invalidează afişarea anului pe patru digiţi</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif; font-size: 12pt;">SET DATE TO DMY|MDY| BRITISH|FRENCH| GERMAN – stabileşte formatul de afişare a datei calendaristice</span><br />
<strong><span style="color: #339966; font-family: 'Times New Roman',serif; font-size: 12pt;">Instructiuni pentru controlul formatului de afişare al ceasului sistem:</span></strong><br />
<span style="color: #339966; font-family: 'Times New Roman',serif; font-size: 12pt;"> SET CLOCK ON | OFF – validează/invalidează afişarea ceasului </span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif; font-size: 12pt;"> SET CLOCK TO [&lt;ROW&gt;,&lt;COL&gt;]- stabileşte poziţia pe ecran în care se va afişa ceasul</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif; font-size: 12pt;"> SET HOURS TO [12 | 24] – stabileşte formatul de afişare al orei</span><br />
<strong><span style="color: #339966; font-family: 'Times New Roman',serif;">Diverse instrucţiuni de configurare</span></strong><br />
<span style="color: #339966; font-family: 'Times New Roman',serif;"> SET BELL ON/OFF – validează/invalidează alarma sonoră a mediului</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif;"> SET CARRY ON/OFF – validează/invalidează păstrarea valorilor din înregistrarea curentă pentru o nouă înregistrare introdusă prin una din comenzile INSERT, APPEND sau BROWSE</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif;"> SET DATABASE TO [<em>NumeBD</em>] – stabileşte baza de date curentă</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif;"> SET DEFAULT TO [<em>Specificator_director</em>] – stabileşte directorul curent</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif;"> SET DELETED ON/OFF – invalidează/validează utilizarea înregistrărilor marcate pentru ştergere în comenzi ulterioare</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif;"> SET ESCAPE ON/OFF – validează/invalidează întreruperea execuţiei unui program sau a unei comenzi la apăsarea tastei ESCAPE</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif;"> SET EXCLUSIVE ON/OFF – stabileşte dacă fişierele tabel vor fi deschise pentru uzul exclusiv sau partajat într-o reţea</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif;"> SET LOCK ON/OFF – validează/invalidează blocarea automată a tabelelor pentru anumite comenzi.</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif;"> SET PATH TO [<em>lista_cai_de_cautare</em>] – stabileşte o listă a căilor de căutare pentru fişiere</span><br />
<span style="color: #339966; font-family: 'Times New Roman',serif;"> SET TALK ON/OFF – validează/invalidează afişarea rezultatelor comenzilor Visual FoxPro</span>
    </div>
  </body>
</html>