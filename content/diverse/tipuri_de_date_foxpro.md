---
title: "Tipuri de Date in FoxPRO"
date: 2018-08-20T03:16:20+03:00
weight: 15
draft: false
---


<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
T<em><span style="font-size: 12pt;">ipuri de date şi funcţii standard</span></em><em><span style="font-size: 12pt;"> în FoxPro</span></em><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Datele cu care lucrează FoxPro sunt de tip numeric, caracter, data calendaristică, logic. Asupra acestor tipuri de date s-au definit operaţii specifice şi au fost realizate funcţii standard dintre care cele mai des folosite vor fi explicate în continuare.</span></span><br />
<span style="text-align: justify;"><strong><em><span style="font-size: 11pt;">Funcţii uzuale asupra tuturor tipurilor de date:</span></em></strong></span><br />


<table class="wiki_table">
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">MAX (&lt;e1&gt;,&lt;e2&gt;)</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">calculează maximul dintre două valori &lt;e1&gt; şi &lt;e2&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">MIN (&lt;e1&gt;,&lt;e2&gt;)</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">calculează minimul dintre două valori &lt;e1&gt; şi &lt;e2&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">TYPE(&lt;eC&gt;)</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce litera corespunzătoare tipului de dată.</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">IIF(&lt;eL&gt;,&lt;e1&gt;,&lt;e2&gt;)</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce &lt;e1&gt; dacă &lt;eL&gt; este adevărat şi &lt;e2&gt;în caz contrar</span></span><br />
</td>
    </tr>
</table>

<span style="text-align: justify;"> </span><br />
<h3 id="toc0"><a name="x--Tipul numeric"></a>Tipul numeric</h3>
 <span style="text-align: justify;"><span style="font-size: 11pt;">O mare parte a datelor prelucrate de calculator este reprezentată de numere, pentru a căror descriere se foloseşte tipul numeric. Cu toate că limbajul FoxPro este un limbaj orientat pe lucrul cu baze de date şi nu unul orientat pe calcule matematice, ştiinţifice, tipul numeric este imlementat astfel ăcât să permită realizarea majorităţii operaţiilor matematice întâlnite în practică.</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">De asemenea, sunt prevăzute o serie de funcţii matematice prin care se pot calcula funcţiile matematice elementare.</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Operanzii numerici care intervin în expresii pot fi:</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">- câmpuri numerice ale unei baze de date;</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">- funcţii care returnează valori numerice;</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">- variabile de tip numeric;</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">- constante numerice.</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Operatori care se aplică unor operanzi numerici, având ca rezultate tot valori numerice sunt : <strong>, ^ (ridicarea la putere), * ( înmulţire), / (împărţire), % (modulo, restul împărţirii), + (adunare), - scădere. Între două expresii numerice se pot aplica, de asemenea, operatori relaţionali, obţinându-se expresii logice.</span></span><br />
<span style="text-align: justify;"></strong><span style="font-size: 11pt;">Funcţiile standard uzuale:</span>**</span><br />
<span style="text-align: justify;"> </span><br />


<table class="wiki_table">
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">ABS (&lt;eN&gt;)</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">calculează valoarea absolută din &lt;eN&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">SQRT (&lt;eN&gt;)</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">calculează radical din &lt;eN&gt; (strict pozitiv)</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">ROUND (&lt;eN1&gt;,&lt;eN2&gt;)</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">&lt;eN1&gt; este rotunjită la zecimala dată de &lt;eN2&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">MOD (&lt;eN1&gt;,&lt;eN2&gt;)</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">calculează restul împărţirii întregi a lui &lt;eN1&gt; la &lt;eN2&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">INT (&lt;eN&gt;)</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce un întreg rezultat prin trunchierea zecimalelor</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">CEILING (&lt;eN&gt;)</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce cel mai mic întreg mai mare sau egal cu argumentul &lt;eN&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">FLOOR (&lt;eN&gt;)</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce cel mai mare întreg mai mic sau egal cu argumentul &lt;eN&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">SIGN (&lt;eN&gt;)</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce valoarea –1 pentru argument negativ, 1 pentru argument pozitiv şi 0 pentru argument nul.</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">RAND ()</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">returnează un număr aleator în intervalul (0, 1)</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">STR (&lt;eN1&gt;[,&lt;eN2&gt; [,&lt;eN3&gt;]])</span></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">conversia între tipul numeric şi tipul şir: &lt;eN1&gt; este numărul, &lt;eN2&gt; este lungimea, &lt;eN3&gt; numărul de poziţii pe care se va face reprezentarea părţii zecimale.</span></span><br />
</td>
    </tr>
</table>

<br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Exemplu: </span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> ? 2 / 3</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> <strong>0, 67</strong></span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> SET DECIMAL TO 4</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? 2 / 3</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">0 , 6667</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Exemple cu funcţii:</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> ? ABS ( a )</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> <strong>400</strong></span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> ? SIGN ( - 32 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">- 1</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">a = - 2 / 3</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? a = SIGN ( a ) * ABS ( a )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">. T .</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? INT ( 14 . 46 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">14</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? INT ( - 2 . 25 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">- 2</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">a = 14 . 46</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? a – INT ( a )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">0 . 46</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">a = - 2 . 25</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? a – INT ( a )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">- 0 . 25</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? CEILING ( 8 . 32 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">9</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? CEILING ( -4 . 23 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">- 4</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? FLOOR ( 8 . 32 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">8</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? FLOOR ( - 4 . 23 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">- 5</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? EXP ( 2 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">7 . 39</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? LOG ( 2 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">0 . 69</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? LOG 10 ( 2 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">1 . 00</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? EXP ( LOG ( 3 ) )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">3 . 00</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? SQRT ( 2 )</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">1 . 41</span></span><br />
<br />
<h3 id="toc1"><a name="x--Tipul şir de caractere"></a><span style="font-size: 11pt;">Tipul şir de caractere </span></h3>
 <span style="text-align: justify;"><span style="font-size: 11pt;"> Un şir de caractere reprezintă o mulţime ordonată de caractere care se tratează ca un tot unitar. Într-un şir de caractere ordinea acestora fiind esenţială, fiecărui caracter I se poate asocia un număr reprezentând poziţia aceastuia în cadrul şirului. </span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> Numărul caracterelor dintr-un şir reprezintă lungimea şirului. Un subşir al şirului dat repreuintă o porţiune din şir, începând de la o poziţie specificată şi de lungimea dată</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> Constantele de tip şir de caractere se specifică prin mulţimea caracterelor care le compun, încadrate între apostrofuri simple sau duble ( la ambele capete trebuie să fie acelaşi tip de apostrof ). </span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> Pentru a include unul dintre cele două delimitatoare într-un şir de caractere, mulţimea caracterelor ce alcătuiesc şirul va fi încadrată între delimitatorul de celălalt tip decât cel din şir. Dacă lungimea şirului este 0 obţinem şirul vid sau nul, care se specifică prin două apostrofuri consecutive fără spaţii sau alte caractere între ele.</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Datele de tip şir de caractere pot avea lungimea maxim 255 caractere ASCII şi se reprezintă intern câte un caracter pe octet în binar. </span></span><br />
<span style="text-align: justify;"><strong><em><span style="font-size: 11pt;">Operaţii asupra datelor de tip şir</span></em></strong><em><span style="font-size: 11pt;">:</span></em></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">- concatenarea a două şiruri se realizează prin operatorii de concatenare (+, -); (+) realizează concatenarea a două şiruri; </span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Exemplu: “ strada _ “ + “ George _ Coşbuc “</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">După evaluare, va avea valoarea:</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> “ strada _ George _ Coşbuc “</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Operatorul (-) realizează concatenarea termenilor cu mutarea spaţiilor de la sfârşitul primului şir la sfârşitul şirului rezultat.</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Exemplu: “ Salut “ - “ prieteni !“</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">După evaluare, vom obţine şirul de caractere</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> “ Salut prieteni ! “</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">se observă că blancurile de la începutul şirului al doilea îşi păstrează poziţia în şir.</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">- testarea apartenenţei unui şir la un alt şir este realizată prin operatorul ($); poate fi folosit în expresii logice.</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">De exemplu, expresia:</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> “ calcul “ $ “ calculator “</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">este adevărată, pe când expresia:</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> “ calcule “ $ “ calculator “</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">va fi evaluată la valoarea logică fals.</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Compararea şirurilor de caractere de lungimi diferite este controlată de comanda :</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;"> SET EXACT ON / OFF</span></strong></span><br />
<span style="text-align: justify;"> </span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">În starea ON şirurile se compară de pe toată lungimea lor (cu excepţia spaţiilor de la sfârşitul şirului). În starea OFF se ia lungimea cea mai scurtă şi, dacă pe aceeaşi lungime şirurile sunt egale, rezultatul este .T..</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">Funcţii uzuale asupra şirurilor</span></strong></span><br />


<table class="wiki_table">
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">SUBSTR </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;, &lt;eN1&gt;,&lt;eN2&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">extrage un subşir din şirul &lt;eC&gt; începând cu </span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">caracterul de pe poziţia &lt;eN1&gt; pe lungime</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> &lt;eN2&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">LEFT </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;, &lt;eN&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">extrage primele &lt;eN&gt; caractere din şirul &lt;eC&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">RIGHT </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;, &lt;eN&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">extrage ultimele &lt;eN&gt; caractere din şirul &lt;eC&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">LEN </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce lungimea şirului &lt;eC&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">REPLICATE </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;, &lt;eN&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce un şir având &lt;eC&gt; multiplicat de </span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">&lt;eN&gt; ori</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">SPACE </span></strong><strong><span style="font-size: 11pt;">(&lt;eN&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">Întoarce un şir de &lt;eN&gt; spaţii</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">LTRIM </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">elimină spaţiile de la stânga şirului &lt;eC&gt;</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">ex.: LTRIM(’MIA’)=”MIA”</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">RTRIM </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;)/ TRIM (&lt;eC&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">elimină spaţiile de la dreapta şirului &lt;eC&gt;</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">ex.: RTRIM(“MAI”’)=”MAI”</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">AT </span></strong><strong><span style="font-size: 11pt;">(&lt;eC1&gt;, &lt;eC2&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce poziţiile şirului &lt;eC1&gt; în &lt;eC2&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">ISALPHA </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">testează dacă şirul începe cu o literă</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">ISLOWER </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">testează dacă şirul începe cu minusculă</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">ISUPPER </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">testează dacă şirul începe cu majusculă </span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">LOWER </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">transformă şirul în minuscule </span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">UPPER </span></strong><strong><span style="font-size: 11pt;">(expC)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">transformă şirul în majuscule</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">STUFF </span></strong><strong><span style="font-size: 11pt;">(&lt;eC1&gt;,&lt;eN1&gt;, &lt;eN2&gt;, &lt;eC2&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">înlocuieşte în &lt;eC1&gt; începând cu poziţia &lt;eN1&gt; un subşir de lungime &lt;eN2&gt; prin şirul &lt;eC2&gt;</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">CTOD </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">realizează conversia unui şir la data calendaristică </span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">VAL </span></strong><strong><span style="font-size: 11pt;">(&lt;eC&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">realizează conversia unui şir la număr</span></span><br />
</td>
    </tr>
</table>

<span style="text-align: justify;"><span style="font-size: 11pt;">Exemple:</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> ? CHR ( 49 ) </span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> <strong>1</strong></span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> ? CHR ( 65 ) == “ A “</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">. T .</span></strong></span><br />
<span style="text-align: justify;"> <span style="font-size: 11pt;">? ASC ( “ A “ )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;"> 65</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? ASC ( “ a “ ) = ASC ( alfa )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">. T .</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? “ A “ == CHR ( ASC ( “ A “ ) )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">. T .</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? 65 == ASC ( CHR ) 65 ) )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">. T .</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? SUBSTR ( “ ABCDEF “ , 2, 3 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">BCD</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? SUBSTR ( “ Ziua Bună “ , 6 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">Bună</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? LEFT ( “ La mulţi ani ! “ , 2 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">La</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? RIGHT ( “ Noapte bună ! “ , 6 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">bună !</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? REPLICATE ( “ a “ , 5 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">a a a a a </span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? REPLICATE ( “ “ , 6 ) == SPACE ( 6 )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">. T .</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? ALLTRIM ( “ GAMA “ ) == “ GAMA “</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">. T .</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? “ Mă numesc “ + RTRIM ( “ Ionescu “ ) + “ Daniel “</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">Mă numesc Ionescu Daniel</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? “ şi am “ + LTRIM ( “ 24 “ ) + “ ani. “</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">şi am 24 ani</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? AT ( “ nr. “ , “ Strada George Coşbuc, nr. 63 – 64 “ )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">22</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? LEN ( “ Salutări ! “ )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">10</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? LEN ( “ Strada George Coşbuc “ + “ nr. 150 “ )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">27</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">a = “ ALFA “</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">b = “ alfa “</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? UPPER ( a ) == UPPER ( b )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">. T .</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? LOWER ( a ) == LOWER ( b )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">. T .</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">STORE “ pala “ TO şir</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">şir = STUFF ( şir , 3 , 0 , “ rale “ )</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? şir</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">paralela</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">şir = STUFF ( şir , 3 , 3 , “ sar “ )</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? şir</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">pasarela</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">şir = STUFF ( şir , 7 , 2 , “ “ )</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">? şir</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">pasare</span></strong></span><br />
<h3 id="toc2"><a name="x--Tipul dată calendaristică"></a><span style="font-size: 11pt;">Tipul dată calendaristică</span></h3>
 <span style="text-align: justify;"><span style="font-size: 11pt;">Datele calendaristice pot fi reprezentate în mai multe formate având ca delimitator acolada. Forma de prezentare a unei date calendaristice depinde de comanda SET DATE:</span></span><br />


<table class="wiki_table">
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">SET DATE [TO] &lt;format&gt; </span></strong></span><br />
</td>
    </tr>
</table>

<span style="text-align: justify;"><span style="font-size: 11pt;">unde &lt;format&gt; poate fi: AMERICAN / GERMAN / ANSI / ITALIAN / DMY /BRITISH /JAPAN /FRENCH /USA /MDY /YMD</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Formatul AMERICAN prezintă data calendaristică sub forma: ll/zz/aa.; formatul GERMAN sub forma zz.ll.aa., etc.</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Includerea secolului în formatul de dată este determinată de starea comutatorului SET CENTURY ON/<u>OFF</u>. Implicit este OFF.</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Indicarea semnului folosit ca separator al informaţiilor de tip dată calendaristică este dat de comanda SET MARK. Implicit separatorul este dat de formatul de reprezentare. De exemplu formatul AMERICAN foloseşte ca separator ”/”.</span></span><br />


<table class="wiki_table">
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">SET DATE TO &lt;car&gt; </span></strong></span><br />
</td>
    </tr>
</table>

<span style="text-align: justify;"><span style="font-size: 11pt;">unde &lt;car&gt; reprezintă un singur caracter ce va fi folosit ca separator al informaţiilor din data calendaristică.</span></span><br />
<span style="text-align: justify;"> </span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Operaţii care se pot face cu datele calendaristice sunt:</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">- compararea a două date se realizează prin operatorii relaţionali:</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">- diferenţa dintre două date calendaristice returnează un număr de zile:</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">- </span></strong><span style="font-size: 11pt;">prin adunarea unui număr de zile la o dată calendaristică se obţine o altă dată:</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;">- </span></strong><span style="font-size: 11pt;">prin scăderea unui număr dintr-o dată calendaristică se obţine tot o dată;</span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;">Funcţiile referitoare la date calendaristice sunt :</span></span><br />


<table class="wiki_table">
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">DATE()</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce data curentă de la sistem</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">DAY </span></strong><strong><span style="font-size: 11pt;">(&lt;eD&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">extrage nr. zilei din dată</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">MONTH</span></strong><strong><span style="font-size: 11pt;">(&lt;eD&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">extrage nr. lunii din dată</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">CMONTH</span></strong><strong><span style="font-size: 11pt;">(&lt;eD&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce numele lunii </span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">YEAR</span></strong><strong><span style="font-size: 11pt;">(&lt;eD&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">extrage anul din data calendaristică</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">TIME()</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">extrage ora sistem sub forma şirului ‘HH:MM:SS’</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">DTOS</span></strong><strong><span style="font-size: 11pt;">(&lt;eD&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce data sub forma ‘secol – an lună zi’</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">DMY</span></strong><strong><span style="font-size: 11pt;">(&lt;eD&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce data sub forma ‘zi nume-lună an’</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">MDY</span></strong><strong><span style="font-size: 11pt;">(&lt;eD&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">întoarce data sub forma ‘nume – lună zi an’</span></span><br />
</td>
    </tr>
    <tr>
        <td><span style="text-align: justify;"><strong><span style="font-size: 11pt;">DTOC</span></strong><strong><span style="font-size: 11pt;">(&lt;eD&gt;)</span></strong></span><br />
</td>
        <td><span style="text-align: justify;"><span style="font-size: 11pt;">conversie data la şir</span></span><br />
</td>
    </tr>
</table>

<span style="text-align: justify;"><span style="font-size: 11pt;">Exemple: </span></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> ? DATE ( )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;"> 11 / 12 / 2000</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> ? CDOW ( DATE ( ) )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;"> Saturday</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> ? DOW ( {10 / 02 / 1864} )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;"> 1</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> ? DAY ( {03 / 14 / 1990} )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;"> 14</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> ? MONTH ( DATE ( ) )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;"> 3</span></strong></span><br />
<span style="text-align: justify;"><span style="font-size: 11pt;"> ? CMONTH ( {03 / 25 / 1990} )</span></span><br />
<span style="text-align: justify;"><strong><span style="font-size: 11pt;"> March</span></strong></span>
    </div>
  </body>
</html>