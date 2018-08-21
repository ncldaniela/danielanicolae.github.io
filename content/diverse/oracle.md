---
title: "Oracle"
date: 2018-08-20T03:16:20+03:00
weight: 18
draft: false
---

<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
<h5 id="toc0"><a name="x----Comanda UPDATE"></a><u>Comanda UPDATE</u></h5>
 <br />
<span style="font-size: 16px;">Comanda </span><span style="font-family: 'Courier New'; font-size: 16px;">UPDATE</span><span style="font-size: 16px;"> este folosită pentru a modifica valorile datelor existente în tabele. </span><br />
<span style="font-size: 16px;">Sintaxa uzuală a comenzii UPDATE prezintă următoarele variante:</span><br />
<span style="font-size: 16px;"> 1)</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">UPDATE tabel </span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">SET coloana1 = expresie1,</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> coloana2 = expresie2, ...</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> [WHERE condiţie];</span><br />
<span style="font-size: 16px;">2)</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">UPDATE tabel </span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">SET coloana1 = expresie1,</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> coloana2 = expresie2, ...</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">FROM tabele_cuplate</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> [WHERE condiţie];</span><br />
Clauza FROM este o extensie specifica SQL Server, inexistenta în standardul SQL92 . Prin această extensie se poate specifica o cuplare de mai multe tabele care se poate folosi în locul unei fraze Select imbricată în clauza WHERE. Sunt acceptate toate tipurile de asocieri (Inner, Left, Right, Full) sunt acceptate şi reyultate obţinute din fraze Select.<br />
<br />
<br />
Comanda <span style="font-family: 'Courier New';">UPDATE</span> modifică valorile înregistrărilor în funcţie de condiţia clauzei <span style="font-family: 'Courier New';">WHERE</span>. În lipsa clauzei <span style="font-family: 'Courier New';">WHERE</span>, vor fi actualizate toate înregistrările din tabelul dat. <br />
<br />
Expresia furnizată ca valoare nouă a unei coloane poate cuprinde valorile curente ale câmpurilor din înregistrarea care este actualizată.<br />
Exemple:<br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">update</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tProduse </span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">set</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> pret</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">=</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">pret</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">*</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">1.1 </span><br />
<br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">update</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tProduse </span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">set</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> pret</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">=</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">pret</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">*</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">0.95 where categoria = ‘Alimentare’</span><br />
<br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">update</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tProduse </span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">set</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> pret</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">=</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">pret</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">*</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">0.95 where codProd in (select codProd from tProduse where categoria = ‘Alimentare’)</span><br />
<br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">update</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tProduse </span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">set</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> pret=CASE</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> When pret<100 then pret*1.1</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> When pret<200 then pret*1.08</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> When pret<300 then pret*1.05</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> Else pret*1.03</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> END</span><br />
<br />
<br />
<span style="font-size: 16px;">Presupunând că avem un tabel tModiPret cu structura:</span><br />
<br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">create</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">table</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tModiPret</span><br />
<span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> (</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> codProd </span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">char</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">(</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">10</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">)</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">primarykey</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">,</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> procent </span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">float</span><br />
<span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> )</span><br />
<br />
<span style="font-size: 16px;">ce conţine procentele diferentiate de modificare a preturilor anumitor produse,</span><br />
<span style="font-size: 16px;">Pentru a modifica datele din tabela <strong>tProduse</strong> pe baza datelor din tabela </span><strong><span style="font-family: 'Courier New';">tModiPret</span></strong><span style="color: #0000ff; font-family: 'Courier New';"> s<span style="color: #000000;">e poate folosi următoarea comandă care conţine tabele corelate</span><br />
</span><br />
<br />
<br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">update</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tProduse </span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">set</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> pret</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">=</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">pret</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">*</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">1.1 </span><br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">from</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">tProduse A</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> inner join </span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">tModiPret B</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> on </span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">A.codProd=B.codProd</span><br />
<span style="text-align: justify;"><span style="font-size: 16px;">sau</span></span><br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">UPDATE</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tProduse </span><br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">SET</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> pret</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">=</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">pret</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">*(</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">1</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">+(</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">SELECT</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> procent </span><br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> FROM</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tModiPret A</span><br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> WHERE</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> A</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">.</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">codP</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">=</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">tProduse</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">.</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">codProd</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">)/</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">100</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">)</span><br />
<span style="text-align: justify;"><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">WHERE</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> codProd IN </span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">(</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">SELECT</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> codProd </span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">FROM</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tModiPret</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">);</span></span><br />
Obs. Daca nu includem conditia<br />
<span style="text-align: justify;"><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">WHERE</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> codProd IN </span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">(</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">SELECT</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> codProd </span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">FROM</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tModiPret</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">)</span></span><br />
atunci <br />
<span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">(</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">SELECT</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> procent </span><br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">FROM</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tModiPret A</span><br />
<span style="text-align: justify;"><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">WHERE</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> A</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">.</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">codP</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">=</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">tProduse</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">.</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">codProd</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">)/</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">100</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">)</span></span><br />
Va returna null pentru valorile din coloana codProd ce nu se gasesc în tModiPret şi prin urmare pentru aceste coduri, pret va fi setat cu null<br />
<span style="text-align: justify;"><span style="font-size: 16px;">Dacă tabelul de actualizat este implicat în diverse legături cu alte tabele ca partea unu a unei legături unu la multi şi opţiunea update cascading este activată atunci orice modificare în cămpul de legatură va fi propagată şi în tabelele secundare corelate</span></span><br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">ALTER</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">TABLE</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tDetaliiBon </span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">ADDFOREIGNKEY</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">(</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">CodProd</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">)</span><br />
<span style="text-align: justify;"><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> REFERENCES</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tProduse </span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">(</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">CodProd</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">)</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">onupdatecascade</span></span><br />
<span style="text-align: justify;"><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">update</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tProduse </span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">set</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> codProd </span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">=</span><span style="color: #ff0000; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">'p101'</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">where</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> codProd</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">=</span><span style="color: #ff0000; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">'p1'</span></span><br />
<span style="text-align: justify;"><span style="font-size: 16px;">va produce automat modificarea în tabelul <strong>tDetaliiBon</strong> din <strong>codProd</strong>='p1' în <strong>codProd</strong> ='p101'</span></span><br />
<h5 id="toc1"><a name="x----Comanda DELETE"></a><u>Comanda DELETE</u></h5>
 <span style="text-align: justify;"><span style="font-size: 16px;">Comanda </span><span style="font-family: 'Courier New'; font-size: 16px;">DELETE</span><span style="font-size: 16px;"> realizează ştergerea înregistrărilor dintr-un tabel în funcţie de anumite condiţii.</span></span><br />
Comanda <span style="font-family: 'Courier New';">DELETE</span> şterge numai înregistrări din tabel nu şi tabelul. Pentru a şterge un tabel se foloseşte comanda <span style="font-family: 'Courier New';">DROPTABLE</span>.<br />
<span style="font-size: 16px;">Sintaxa uzuală a comenzii DELETE prezintă următoarele variante:</span><br />
<span style="text-align: justify;"><span style="font-size: 16px;">1)</span></span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">DELETE [FROM] tabel</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> [WHERE condiţie];</span><br />
<br />
2)<br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">DELETE [FROM] tabel </span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">FROM tabele_cuplate</span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> [WHERE condiţie];</span><br />
<br />
<br />
Similar comenzii <span style="font-family: 'Courier New';">UPDATE</span>, comanda <span style="font-family: 'Courier New';">DELETE</span> şterge anumite înregistrări în funcţie de condiţia din clauza <span style="font-family: 'Courier New';">WHERE</span>. În lipsa clauzei <span style="font-family: 'Courier New';">WHERE</span> vor fi şterse toate înregistrările din tabelul dat. În această clauză pot fi incluse şi subinterogări.<br />
<br />
De exemplu următoarea comandă şterge toate înregistrările pentru care gradul didactic este asistent<br />
<br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">DELETE tDetaliiBon</span><br />
Şterge toate rândurile tabelului tDetaliiBon<br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">DELETE tDetaliiBon where NrBon=’101’</span><br />
Şterge toate rândurile tabelului tDetaliiBon pentru care <span style="font-family: 'Courier New';">NrBon=’101’</span><br />
<br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">DELETE tDetaliiBon </span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">from tBonuriConsum A inner join tDetaliiBon B on A.NrBon=B.NrBon </span><br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">where dataBon <'01/01/2008'</span><br />
<br />
<span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">DELETE tBonuriConsum where dataBon <'01/01/2008'</span><br />
<br />
<span style="text-align: justify;"><span style="font-size: 16px;">Dacă tabelul din care ştergem este implicat în diverse legături cu alte tabele ca partea unu a unei legături unu la multi şi opţiunea delete cascading este activată atunci ştergerea unui rând va genera ştergerea tuturor rândurilor ce corespund la cheie din tabelele secundare corelate.</span></span><br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">alter</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">table</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tDetaliiBon</span><br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">addconstraint</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> Fk_NrBon_tDet </span><br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">foreignkey</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">(</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">NrBon</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">)</span><br />
<span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">references</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tBonuriConsum </span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">(</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">NrBon</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">)</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">ondeletecascade</span><br />
<span style="text-align: justify;"><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">delete</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">from</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tBonuriConsum </span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">where</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> NrBon</span><span style="color: #808080; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">=</span><span style="color: #ff0000; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">'104'</span></span><br />
<span style="text-align: justify;"><span style="font-size: 16px;">va produce stergerea automată din tabelul <strong>tDetaliiBon</strong> a tuturor rândurilor pentru care NrBon=’104’</span></span><br />
<br />
<h3 id="toc2"><a name="x--Comanda TRUNCATE"></a><u><span style="font-family: 'Times New Roman','serif';">Comanda TRUNCATE </span></u></h3>
 <span style="text-align: justify;"> </span><br />
<span style="text-align: justify;"><span style="font-size: 16px;">Pentru a şterge în mod rapid toate înregistrările dintr-o tabelă se foloseşte comanda </span><span style="font-family: 'Courier New'; font-size: 16px;">TRUNCATE</span><span style="font-size: 16px;"> cu următoarea sintaxă:</span></span><br />
<span style="text-align: justify;"><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;">TRUNCATE TABLE tabel </span></span><br />
<span style="text-align: justify;"><span style="font-size: 16px;">Exemplu</span></span><br />
<span style="text-align: justify;"><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">truncate</span><span style="color: #0000ff; font-family: 'Arial','sans-serif'; font-size: 14.6667px;">table</span><span style="font-family: 'Arial','sans-serif'; font-size: 14.6667px;"> tModiPret</span></span><br />
<span style="text-align: justify;"><span style="font-size: 16px;">Ştergerea înregistrărilor cu ajutorul comenzii </span><span style="font-family: 'Courier New'; font-size: 16px;">TRUNCATE</span><span style="font-size: 16px;"> este mult mai avantajoasă decât eliminarea tabelului şi recrearea lui ulterioară deoarece eliminarea tabelului necesită recrearea indecşilor, constrângerilor de integritate, declanşatoarelor etc.</span></span>
    </div>
  </body>
</html>