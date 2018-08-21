---
title: "Tipul Struct"
date: 2018-08-20T03:16:20+03:00
weight: 4
draft: false
---

<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
O structura este o colectie de valori eterogene, stocate intr-o zona compacta de memorie.<br />
Componentele unei structuri, denumite campuri, sunt identificate prin nume simbolice, denumite selectori.<br />
Campurile unei structuri pot fi de orice tip, simplu sau derivat, dar nu void sau functie.<br />
<br />
<span style="color: #548dd4;">Declararea structurilor</span> se face folosind cuvantul cheie <span style="color: #548dd4;">struct:</span><br />
<br />
struct [nume_structura]{<br />
tip1 membrii;<br />
tip2 membrii;<br />
................<br />
tipn membrii;<br />
}[lista_declaratori]; <em>variabile de tip structura</em><br />
<br />
<em>nume_structura saulista_declaratori pot lipsi, dar nu simultan.</em><br />
<em>Daca se precizeaza nume_structura, atunci inseamna ca se face definirea tipului struct nume_structura, care poate fi apoi folosit pentru declararea de variabile, ca tip de parametri formali sau ca tip de rezultat returnat de functii:</em><br />
<br />
<em><strong>Exemplu1:</strong></em><br />
<em>struct persoana{</em> se declara tipul struct persoana<br />
char nume[20];<br />
int varsta;<br />
}; <em>lipseste lista_declaratori</em><br />
<br />
<em><strong>Exemplu2:</strong></em><br />
<em>struct{</em> lipseste nume_struct<br />
char titlu[20],autor[15],editura[12];<br />
int an_aparitie;<br />
}carte,biblioteca[1000]; <em>nu se declara un tip, deci</em><br />
doar aici pot fi facute declaratiile de variabile<br />
<br />
Un camp al unei structuri poate fi de tip structura, dar nu aceeasi cu cea definita.<br />
<br />
<strong>Exemplu3:</strong><br />
struct persoana{ <em>se declara tipul struct persoana</em><br />
<em>char nume[20];</em><br />
<em>struct</em><br />
<em>{</em><em>int zi,an,luna;</em><br />
<em>} datan;</em> camp de tip structura<br />
}p;<br />
<br />
<strong>Exemplu4:</strong><br />
struct data{<br />
int zi,luna,an;};<br />
<br />
struct persoana{<br />
char nume[30];<br />
data datan;} p;<br />
<br />
<br />
Folosind cuvantul cheie <span style="color: #548dd4;">typedef </span>se pot defini tipuri utilizator echivalente pentru cele structura.<br />
<br />
Selectarea unui camp al unei variabile structura se realizeaza folosind operatorul de selectie .<span style="color: #fff2cc; font-size: 32px;">. </span><br />
Campul selectat se comporta ca o variabila de acelasi tip, deci i se pot aplica aceleasi prelucrari ca oricarei variabile de tipul respectiv.<br />
<br />
variabila_structura.nume_camp<br />
<br />
Exemplu:<br />
persoana p; //se declara variabila p de tip persoana<br />
<br />
p.nume - campul nume din structura persoana<br />
p.datan.an - campul an din data nasterii<br />
p.datan.luna - campul luna din data nasterii<br />
p.datan.zi - campul zi din data nasterii<br />
<br />
<br />
APLICATII<br />
<strong><span style="font-family: 'Arial','sans-serif';">Probleme rezolvate</span></strong><br />
<br />
<h3 id="toc0"><a name="x--1.Se citesc de la tastatură două numere complexe. Să se efectueze operaţiile de adunare, scadere, înmulţire şi împărţire cu aceste numere complexe."></a><span style="font-family: 'Arial','sans-serif';">1.Se citesc de la tastatură două numere complexe. Să se efectueze operaţiile de adunare, scadere, înmulţire şi împărţire cu aceste numere complexe.</span></h3>
 <br />
Vom defini tipul structurat <strong>complex,</strong> care conţine partea reală şi partea imaginară a numărului.<br />
<br />
<span style="font-size: 14.6667px;">#include <iostream.h> <strong><em>OPERATII CU NUMERE COMPLEXE</em></strong></span><br />
<em><span style="font-size: 14.6667px;">#include <conio.h></span></em><br />
<br />
<span style="display: block; text-align: justify;"><strong><span style="font-size: 14.6667px;">struct complex </span></strong></span><br />
x-partea reala , y-partea imaginara<br />
<strong><span style="font-size: 14.6667px;"> {float x,y;</span></strong><br />
<strong><span style="font-size: 14.6667px;"> };</span></strong><br />
<strong><span style="font-size: 14.6667px;">complex a,b,c;</span></strong><br />
<strong><span style="font-size: 14.6667px;">void afisare(complex e) <em>afisarea unui numar complex</em></span></strong><br />
<em><span style="font-size: 14.6667px;">{if(e.y>=0)</span></em><br />
<em><span style="font-size: 14.6667px;"> cout<<e.x<<"+"<<e.y<<"i"<<endl;</span></em><br />
<em><span style="font-size: 14.6667px;"> else</span></em><br />
<em>cout<<e.x<<e.y<<"i"<<endl;</em><br />
<em>}</em><br />
<em><strong>void adunare()</strong></em> <strong>adunarea a doua numere complexe</strong><br />
{c.x=a.x+b.x;<br />
c.y=a.y+b.y;<br />
}<br />
<strong>void scadere() <em>scaderea a doua numere complexe</em></strong><br />
<em>{c.x=a.x-b.x;</em><br />
<em>c.y=a.y-b.y;</em><br />
<em>}</em><br />
<em><strong>void inmultire()</strong></em> <strong>inmultirea a doua nume</strong><br />
<h3 id="toc1"> </h3>
 <strong>re complexe</strong><br />
{c.x=a.x*b.y-a.y*b.x;<br />
c.y=a.x*b.y+a.y*b.x;<br />
}<br />
<strong>void impartire() //impartirea a doua numere complexe</strong><br />
{c.x=(a.x*b.x+a.y*b.y)/(b.x*b.x+b.y*b.y);<br />
c.y=(a.y*b.x-a.x*b.y)/(b.x*b.x+b.y*b.y);<br />
}<br />
<strong><span style="font-size: 14.6667px;"> void main()</span></strong><br />
<span style="font-size: 14.6667px;"> {cout<<"primul numar:"; cin>>a.x>>a.y;</span><br />
<span style="font-size: 14.6667px;"> cout<<"al doilea numar:"; cin>>b.x>>b.y;</span><br />
<span style="font-size: 14.6667px;"> cout<<"a="; afisare(a);</span><br />
<span style="font-size: 14.6667px;"> cout<<"b="; afisare(b);</span><br />
<span style="font-size: 14.6667px;"> adunare();</span><br />
<span style="font-size: 14.6667px;"> cout<<"suma=";</span><br />
<span style="font-size: 14.6667px;"> afisare(c);</span><br />
<h3 id="toc2"> </h3>
 <span style="font-size: 14.6667px;"> scadere();</span><br />
<span style="font-size: 14.6667px;"> cout<<"diferenta=";</span><br />
<span style="font-size: 14.6667px;"> afisare(c);</span><br />
<span style="font-size: 14.6667px;"> inmultire();</span><br />
<span style="font-size: 14.6667px;"> cout<<"produsul=";</span><br />
<span style="font-size: 14.6667px;"> afisare(c);</span><br />
<span style="font-size: 14.6667px;"> impartire();</span><br />
<span style="font-size: 14.6667px;"> cout<<"impartire=";</span><br />
<span style="font-size: 14.6667px;"> afisare(c); </span><br />
<span style="font-size: 14.6667px;"> getch();</span><br />
<span style="font-size: 14.6667px;"> }</span><br />
<h3 id="toc3"><a name="x--2. Pentru n elevi se citesc: numele şi două note la informatică. Să se calculeze media fiecărui elev. Să se afişeze elevii în ordinea descrescătoare a mediilor, iar pentru medii egale, în ordine alfabetică."></a>2. Pentru n elevi se citesc: numele şi două note la informatică. Să se calculeze media fiecărui elev. Să se afişeze elevii în ordinea descrescătoare a mediilor, iar pentru medii egale, în ordine alfabetică.</h3>
 <span style="font-size: 14.6667px;">#include<iostream.h></span><br />
<span style="font-size: 14.6667px;">#include<conio.h></span><br />
<span style="font-size: 14.6667px;">#define MAX 30</span><br />
<strong><span style="font-size: 14.6667px;">struct elev </span></strong><span style="font-size: 14.6667px;"><em>definirea structurii de date elev</em></span><br />
<em><strong><span style="font-size: 14.6667px;">{char nume[MAX];</span></strong></em><br />
<em><strong><span style="font-size: 14.6667px;"> int n1,n2;</span></strong></em><br />
<em><strong><span style="font-size: 14.6667px;"> float media;</span></strong></em><br />
<em><strong><span style="font-size: 14.6667px;">};</span></strong></em><br />
<em><strong><span style="font-size: 14.6667px;">elev a[MAX]; </span></strong></em>a-tabl<br />
<h3 id="toc4"> </h3>
 oul pentru memorarea elevilor<br />
<span style="font-size: 14.6667px;">int n;</span><br />
<strong><span style="font-size: 14.6667px;">void citire() </span></strong><span style="font-size: 14.6667px;"><em>citire date</em></span><br />
<em><span style="font-size: 14.6667px;">{int i;</span></em><br />
<em><span style="font-size: 14.6667px;"> clrscr();</span></em><br />
<em><span style="font-size: 14.6667px;"> for(i=1; i<=n; i++)</span></em><br />
<em><span style="font-size: 14.6667px;"> {cout<<"numele persoanei:"; cin.get();cin.get(a[i].nume,20,'\n'); </span></em>citeste numele<br />
<span style="font-size: 14.6667px;"> cout<<"nota1: "; cin>>a[i].n1; <em>citeste notele</em></span><br />
<em><span style="font-size: 14.6667px;"> cout<<"nota2: "; cin>>a[i].n2;</span></em><br />
<em><span style="font-size: 14.6667px;"> a[i].media=(((float)a[i].n1+a[i].n2)/2); </span></em>calculeaza media<br />
<span style="font-size: 14.6667px;"> }</span><br />
<span style="font-size: 14.6667px;">}</span><br />
<strong><span style="font-size: 14.6667px;">void afisare() </span></strong><span style="font-size: 14.6667px;"><em>afiseaza datele elevilor</em></span><br />
<em><span style="font-size: 14.6667px;">{int i;</span></em><br />
<em><span style="font-size: 14.6667px;"> for(i=1; i<=n; i++)</span></em><br />
<em><span style="font-size: 14.6667px;"> cout<<a[i].nume <<" "<<a[i].n1<<" "<<a[i].n2<<" "<<a[i].media<<endl;</span></em><br />
<em><span style="font-size: 14.6667px;"> getch();</span></em><br />
<em><span style="font-size: 14.6667px;">}</span></em><br />
<em><strong><span style="font-size: 14.6667px;">void ordonare() </span></strong></em><span style="font-size: 14.6667px;">ordoneaza elevii descrescator după medii, iar la medii egale alfabetic</span><br />
<span style="font-size: 14.6667px;">{int i,sw;</span><br />
<span style="font-size: 14.6667px;"> elev aux;</span><br />
<span style="font-size: 14.6667px;"> do{</span><br />
<span style="font-size: 14.6667px;"> sw=1;</span><br />
<span style="font-size: 14.6667px;"> for(i=1; i<n; i++)</span><br />
<span style="font-size: 14.6667px;"> if((a[i+1].media>a[i].media)||(a[i+1].media==a[i].media &amp;&amp; strcmp(a[i+1].nume,a[i].nume)<0))</span><br />
<span style="font-size: 14.6667px;"> {aux=a[i+1]; a[i+1]=a[i]; a[i]=aux; sw=0; }</span><br />
<span style="font-size: 14.6667px;"> } while(!sw);</span><br />
<span style="font-size: 14.6667px;">}</span><br />
<strong><span style="font-size: 14.6667px;">void main()</span></strong><br />
<span style="font-size: 14.6667px;">{ clrscr(); </span><br />
<span style="font-size: 14.6667px;"> cout<<"n=";cin>>n; <em>n-nr.elevi</em></span><br />
<em><span style="font-size: 14.6667px;"> citire(); clrscr(); afisare(); </span></em>citeste datele elevilor<br />
<span style="font-size: 14.6667px;"> ordonare(); <em>ordoneaza elevii</em></span><br />
<em><span style="font-size: 14.6667px;"> cout<<"Elevii in ordinea descrescatoare a mediilor"<<endl;</span></em><br />
<em><span style="font-size: 14.6667px;"> afisare(); </span></em>afiseaza datele elevilor<br />
<span style="font-size: 14.6667px;"> getch();</span><br />
<span style="font-family: 'Arial','sans-serif';">}</span><br />
<br />
<h3 id="toc5"><a name="x--file:Fisa de lucru_tipul_struct.pdf"></a><span style="font-family: 'Arial','sans-serif';"><a href="/files/Fisa%20de%20lucru_tipul_struct.pdf">Fisa de lucru_tipul_struct.pdf</a></span></h3>

    </div>
  </body>
</html>