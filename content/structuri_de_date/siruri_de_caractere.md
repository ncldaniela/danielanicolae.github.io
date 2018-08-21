---
title: "Siruri de Caractere"
date: 2018-08-20T03:16:20+03:00
weight: 3
draft: false
---

<html>
  <body>
    <div class="wiki" id="content_view" style="display: block;">
<h1 id="toc0"><a name="Notiuni teoretice"></a><span style="color: #008000;">Notiuni teoretice</span></h1>
 <a href="/files/SIRURI%20DE%20CARACTERE.doc">SIRURI DE CARACTERE.doc</a><br />
<h1 id="toc1"><a name="TESTE GRILA"></a><span style="color: #008000;">TESTE GRILA</span></h1>
 <a href="/files/TESTE%20GRILA.docx">TESTE GRILA.docx</a><br />
<h2 id="toc2"><a name="TESTE GRILA-PROBLEME PROPUSE"></a><span style="color: #008000;">PROBLEME PROPUSE</span></h2>
 <a class="wiki_link_ext" href="http://info.mcip.ro/?cap=Siruri%20de%20caractere" rel="nofollow">http://info.mcip.ro/?cap=Siruri%20de%20caractere</a><br />
<span style="display: block; text-align: right;"><br />
</span><br />
<a href="/files/Probleme%20backtracking.doc">Probleme backtracking.doc</a><br />
<h1 id="toc3"><a name="PROBLEME REZOLVATE"></a><span style="color: #0011ff;"> PROBLEME REZOLVATE</span></h1>
 <span style="color: #c00000; font-size: 13.3333px;">1. Se citeşte de la tastatură un cuvânt. Să se afişeze numărul iniţial de caractere ale cuvântului şi apoi să se şteargă toate vocalele din cuvânt.</span><br />
<span style="font-size: 13.3333px;">#include<iostream.h></span><br />
<span style="font-size: 13.3333px;">#include<string.h></span><br />
<span style="font-size: 13.3333px;">#include<conio.h></span><br />
<span style="font-size: 13.3333px;">void main()</span><br />
<span style="font-size: 13.3333px;">{int i;</span><br />
<span style="font-size: 13.3333px;">char s[100];</span><br />
<span style="font-size: 13.3333px;">cout<<"s=";cin.get(s,100);</span><br />
<span style="font-size: 13.3333px;">cout<<"Sirul are: "<<strlen(s)<<" caractere"<<endl;</span><br />
<span style="font-size: 13.3333px;">strlwr(s);</span><br />
<span style="font-size: 13.3333px;">for(i=0;i<strlen(s);i++)</span><br />
<span style="font-size: 13.3333px;"> if(s[i]=='a'||s[i]=='e'||s[i]=='i'||s[i]=='o'||s[i]=='u')</span><br />
<span style="font-size: 13.3333px;"> strcpy(s+i,s+i+1);</span><br />
<span style="font-size: 13.3333px;">cout<<"sirul fara vocale="<<s;</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<br />
<span style="color: #c00000; display: block; font-size: 13.3333px; text-align: justify;">2. Se citesc de la tastatură 2 şiruri de caractere. Să se verifice dacă sunt egale (la fel) fără a se face deosebire între literele mari şi literele mici.</span><br />
<span style="font-size: 13.3333px;">#include<iostream.h></span><br />
<span style="font-size: 13.3333px;">#include<string.h></span><br />
<span style="font-size: 13.3333px;">#include<conio.h></span><br />
<span style="font-size: 13.3333px;">char s1[100],s2[100];</span><br />
<span style="font-size: 13.3333px;">void citire()</span><br />
<span style="font-size: 13.3333px;">{</span><br />
<span style="font-size: 13.3333px;">cout<<"primul sir: ";cin.get(s1,100);cin.get();</span><br />
<span style="font-size: 13.3333px;">cout<<"al doilea sir ";cin.get(s2,100);</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<span style="font-size: 13.3333px;">void compara()</span><br />
<span style="font-size: 13.3333px;">{int x;</span><br />
<span style="font-size: 13.3333px;">x=stricmp(s1,s2);</span><br />
<span style="font-size: 13.3333px;">strlwr(s1);strlwr(s2);</span><br />
<span style="font-size: 13.3333px;">//transformam cele doua siruri in siruri numai cu litere mici</span><br />
<span style="font-size: 13.3333px;">if(x>0) cout<<"Primul sir este mai mare\n ";</span><br />
<span style="font-size: 13.3333px;"> else if(x==0) cout<<"Siruri sunt egale\n ";</span><br />
<span style="font-size: 13.3333px;"> else cout<<"Al doilea sir este mai mare decat primul\n ";</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<span style="font-size: 13.3333px;">void main()</span><br />
<span style="font-size: 13.3333px;">{citire();</span><br />
<span style="font-size: 13.3333px;">compara();</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<br />
<span style="color: #c00000; display: block; font-size: 13.3333px; text-align: justify;">3. Fişierul litere.txt conţine un text scris cu litere mari pe una sau mai multe linii. Se cere:</span><br />
<span style="color: #c00000; display: block; font-size: 13.3333px; text-align: justify;">a) Să se afişeze litera ( literele) care apare de cele mai multe ori;</span><br />
<span style="color: #c00000; display: block; font-size: 13.3333px; text-align: justify;">b) Să se afişeze vocalele din text.</span><br />
<br />
<br />
<span style="font-size: 13.3333px;">#include<iostream.h></span><br />
<span style="font-size: 13.3333px;">#include<string.h></span><br />
<span style="font-size: 13.3333px;">#include<fstream.h></span><br />
<span style="font-size: 13.3333px;">#include<io.h></span><br />
<span style="font-size: 13.3333px;">ifstream f("litere.txt");</span><br />
<span style="font-size: 13.3333px;">int n;</span><br />
<span style="font-size: 13.3333px;">char a[100];</span><br />
<span style="font-size: 13.3333px;">void citire()</span><br />
<span style="font-size: 13.3333px;">{int i;</span><br />
<span style="font-size: 13.3333px;">i=0;</span><br />
<span style="font-size: 13.3333px;">f>>a[i];</span><br />
<span style="font-size: 13.3333px;">while(!f.eof())</span><br />
<span style="font-size: 13.3333px;">{cout<<a[i];</span><br />
<span style="font-size: 13.3333px;">i++;</span><br />
<span style="font-size: 13.3333px;">/*pt nu a avea surprize ca fisierul sa nu aiba decat majuscule</span><br />
<span style="font-size: 13.3333px;">transformam sirul in majusculele*/</span><br />
<span style="font-size: 13.3333px;">strupr(a);</span><br />
<span style="font-size: 13.3333px;">f>>a[i];</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<span style="font-size: 13.3333px;">n=i;</span><br />
<span style="font-size: 13.3333px;">f.close();</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<span style="font-size: 13.3333px;">void maxim()</span><br />
<span style="font-size: 13.3333px;">{</span><br />
<span style="font-size: 13.3333px;">int b[50];</span><br />
<span style="font-size: 13.3333px;">cout<<"\n numarul de caractere="<<n<<"\n";</span><br />
<span style="font-size: 13.3333px;">int k=0;</span><br />
<span style="font-size: 13.3333px;">for(char c='A';c<='Z';c++){</span><br />
<span style="font-size: 13.3333px;"> b[k]=0;</span><br />
<span style="font-size: 13.3333px;"> for(int j=0;j<n;j++)</span><br />
<span style="font-size: 13.3333px;"> if(c==a[j]) b[k]++;</span><br />
<span style="font-size: 13.3333px;"> k++;</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<span style="font-size: 13.3333px;">int max=b[0];</span><br />
<span style="font-size: 13.3333px;">for(int i=1;i<k;i++)</span><br />
<span style="font-size: 13.3333px;"> if(max<b[i])max=b[i];</span><br />
<span style="font-size: 13.3333px;">cout<<"caracterele cu numar maxim de aparitii="<<max<<endl;</span><br />
<span style="font-size: 13.3333px;">for(i=0;i<k;i++)</span><br />
<span style="font-size: 13.3333px;"> if(b[i]==max)cout<<char(65+i)<<" ";</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<span style="font-size: 13.3333px;">void vocale()</span><br />
<span style="font-size: 13.3333px;">{char voc[]="AEIOU";</span><br />
<span style="font-size: 13.3333px;">cout<<"\nvocalele din text\n";</span><br />
<span style="font-size: 13.3333px;">for(int i=0;i<n;i++)</span><br />
<span style="font-size: 13.3333px;"> for(int j=0;j<strlen(voc);j++)</span><br />
<span style="font-size: 13.3333px;"> if(a[i]==voc[j])cout<<a[i]<<" ";</span><br />
<span style="font-size: 13.3333px;">cout<<"\n";</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<span style="font-size: 13.3333px;">void main()</span><br />
<span style="font-size: 13.3333px;">{citire();</span><br />
<span style="font-size: 13.3333px;">maxim();</span><br />
<span style="font-size: 13.3333px;">vocale();</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<br />
<span style="color: #c00000; display: block; font-size: 13.3333px; text-align: justify;">4. Se citeşte un text într-o variabilă de tip string, in care cuvintele se despart prin spaţii. Se cere:</span><br />
<span style="color: #c00000; display: block; font-size: 13.3333px; text-align: justify;">a) să se afişeze cuvintele în ordine alfabetică;</span><br />
<span style="color: #c00000; display: block; font-size: 13.3333px; text-align: justify;">b) să se numere cuvintele cu minim 4 vocale distincte.</span><br />
<br />
<span style="font-size: 13.3333px;">#include <iostream.h></span><br />
<span style="font-size: 13.3333px;">#include <conio.h></span><br />
<span style="font-size: 13.3333px;">#include <string.h></span><br />
<span style="font-size: 13.3333px;">char cuv[10][10];</span><br />
<span style="font-size: 13.3333px;">int n;</span><br />
<span style="font-size: 13.3333px;">void sortare()</span><br />
<span style="font-size: 13.3333px;">{ char aux[10];int x;</span><br />
<span style="font-size: 13.3333px;">for(int i=1;i<n;i++)</span><br />
<span style="font-size: 13.3333px;"> for(int j=1+i;j<=n;j++)</span><br />
<span style="font-size: 13.3333px;"> {x=strcmp(cuv[i],cuv[j]);</span><br />
<span style="font-size: 13.3333px;"> if(x>0){</span><br />
<span style="font-size: 13.3333px;"> strcpy(aux,cuv[i]);</span><br />
<span style="font-size: 13.3333px;"> strcpy(cuv[i],cuv[j]);</span><br />
<span style="font-size: 13.3333px;"> strcpy(cuv[j],aux);</span><br />
<span style="font-size: 13.3333px;"> }</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<span style="font-size: 13.3333px;">for(i=1;i<=n;i++)cout<<cuv[i]<<" ";</span><br />
<span style="font-size: 13.3333px;">cout<<endl;</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<span style="font-size: 13.3333px;">int nrvocale(char s[10])</span><br />
<span style="font-size: 13.3333px;">{char vocale[]="aeiou";int c;int nr=0;</span><br />
<span style="font-size: 13.3333px;">strlwr(s);</span><br />
<span style="font-size: 13.3333px;">for(int i=0;i<strlen(vocale);i++)</span><br />
<span style="font-size: 13.3333px;"> { c=0;</span><br />
<span style="font-size: 13.3333px;"> for(int j=0;j<strlen(s);j++)</span><br />
<span style="font-size: 13.3333px;"> if(vocale[i]==s[j])c++;</span><br />
<span style="font-size: 13.3333px;"> if(c!=0)nr++;</span><br />
<span style="font-size: 13.3333px;"> }</span><br />
<span style="font-size: 13.3333px;">if (nr>=4)return 1;</span><br />
<span style="font-size: 13.3333px;"> else return 0;</span><br />
<br />
<span style="font-size: 13.3333px;">}</span><br />
<span style="font-size: 13.3333px;">void vocale4()</span><br />
<span style="font-size: 13.3333px;">{</span><br />
<span style="font-size: 13.3333px;">for(int i=1;i<=n;i++)</span><br />
<span style="font-size: 13.3333px;"> if(nrvocale(cuv[i])==1)cout<<cuv[i]<<" ";</span><br />
<span style="font-size: 13.3333px;">cout<<"\n";</span><br />
<span style="font-size: 13.3333px;">}</span><br />
<span style="font-size: 13.3333px;">int main()</span><br />
<span style="font-size: 13.3333px;">{char a[100],*p,separator[]=" ";</span><br />
<span style="font-size: 13.3333px;">int i=0,nr=0;</span><br />
<span style="font-size: 13.3333px;">cout<<"Dati sirul:";cin.get(a,100);</span><br />
<span style="font-size: 13.3333px;">strcpy(p,a);</span><br />
<span style="font-size: 13.3333px;">p=strtok(p,separator);</span><br />
<span style="font-size: 13.3333px;">while (p)</span><br />
<span style="font-size: 13.3333px;"> {strcpy(cuv[++nr],p);</span><br />
<span style="font-size: 13.3333px;"> p=strtok(NULL,separator);}</span><br />
<span style="font-size: 13.3333px;">cout<<"Sunt "<<nr<<" cuvinte:"<<endl;</span><br />
<span style="font-size: 13.3333px;">for (i=1;i<=nr;i++) cout<<cuv[i]<<endl;</span><br />
<span style="font-size: 13.3333px;">n=nr;</span><br />
<span style="font-size: 13.3333px;">sortare();</span><br />
<span style="font-size: 13.3333px;">vocale4();</span><br />
<span style="font-size: 13.3333px;">return 0;</span><br />
}
    </div>
  </body>
</html>