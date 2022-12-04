Kursmoment05 Analys
=======================

I detta kursmoment består en del av uppgiften i att analysera webbplatsers laddningstid.
Vi ska använda oss av webbverktyg, på ett urval webbplatser, för att mäta prestanda och obververa hur utfallen för respektive webbplats ser ut. 

# Urval
-----------------------
Vi ska välja ut tre webbplatser att analysera.

Vi valde att återanvända oss av de webbplatser som vi använde i det tidigare kursmomentet gällande analys av bland annat färgschema och typografi.

Första valet: https://www.kevinpowell.co/, hädanefter “Hemsida 1”.

Andra valet: https://feber.se/, hädanefter “Hemsida 2”.

Tredje valet: https://aforestlife.com/, hädanefter “Hemsida 3”.


# Metod
-----------------------

Under genomförandet av denna uppgift så använde vi oss utav webbverktyget 'pagespeed.web.dev' från google.com. Detta webbverktyg assisterade oss i att sammanställa prestandan hos de olika webbplatserna samt diagnostisera prestandaproblem.


# Resultat
-----------------------

### Hemsida 1

Överlag följer webbplatsen de generella rekommendationerna för sökmotoroptimering och tillgänglighet. Något som är värt att anmärka är att vid mätning för mobila-användare så är värdet för Cumulative Layout Shift (CLS) något avvikande från resterande parametrar. Den vanligaste orsaken till sämre CLS är bland annat bilder som saknar angiven dimension men det gäller även ads, embeds och iframes. Prestandan är dock bättre för desktop-användare där CLS inte urskiljer sig anmärkningsvärt. Se bilaga 1.1 för statistik på dator och 1.2 för mobil.

### Hemsida 2

På mobila enheter så ger Pagespeed anmärkning på CLS. Som vi nämnde tidigare beror sämre CLS bland annat på bilder, ads, embeds och iframes som saknar angiven dimension.
Vår uppfattning är även att webbplatsens laddningstid skulle påverkas positivt av implementeringen av modernare bildformat och att skapa en ordning över vilka element som ska prioriteras över andra i webbplatsens inläsning, där mindre essentiella element. Se bilaga 2.2.

För desktop-enheter så var åter CLS något som uttryckte sig ur mängden i mätningen av webbplatsens hastighet. Vi drog slutsatsen att laddningstiden skulle påverkas positivt av att skjuta upp inläsningen av bilder som inte visas på skärmen, men i detta fall även dra nytta av att reducera JavaScript som inte används. Se bilaga 2.1.


### Hemsida 3

Pagespeed visar möjligheter till förbättring. Hemsida 3 har ett stort förbättringsområde när det kommer till att skicka bilder i ett modernare format samt att använda rätt bildstorlek. Detta är relevant då sidan bygger på användning av många bilder. 

Gällande möjliga förbättringar så har vi, med hjälp av Pagespeed, noterat att det med stor sannolikhet skulle vara gynnsamt för webbplatsens laddningstid om man minskar serverns första svarstid, om webbplatsen skickade bilder i modernare format samt om skaparen tog bort resurser som blockerar renderingen.

Övriga anmärkningar som vi noterade med hjälp av Pagespeed var bland annat att
First Contentful Paint(FCP), som mäter tiden från att sidan laddar till att första saken i content syns, samt Time to First Byte(TTFB), dvs tiden mellan förfrågan av resurs till att första “byten” av förfrågan har anlänt, uppmättes lägre i vår mätning. Vidare så fann vi att Interaction to Next Paint(INP), ett värde som mäter hur responsiv sidan är under dess livslängd(när användaren är inne på den), även hade ett avvikande värde, vilket är ett värde som kan förbättras till stor del genom att optimera javascript koden för hemsidan.

Se bilaga 3.1 för statistik på dator och 3.2 för mobil.


# Analys
-----------------------
Viktigt för användarupplevelsen där undersökningar visar att webbplatser med längre laddningstider har lägre genomsnittlig besökstid.

En viktig beståndsdel i effektiviseringen av en webbsidas laddningshastighet är att optimera bildelement och fastställa att de inte är av ett större format än vad som verkligen behövs, men även att de är lagrade i rätt filformat då detta påverkar laddningstiden för hemsidan. 

För att optimera storleken på CSS, HTML och JS-filer bör man komprimera dessa när de överstiger 150 bytes. Enligt https://developers.google.com/speed/docs/insights/ så kan man minska filstorleken med upp till 90% om man använder sig av Gzip.

En webbplats laddningshastighet är även en av variablerna som används i algoritmen för googles sökmotor i att rangordna sidor. Ju snabbare sida desto högre upp i indexeringen hamnar sidan i resultatet.

Några återkommande förbättringsområden gällande både mobila enheter och datorer, för vårt urval av webbplatser, är att skicka bilder i modernare bildformat. En sak som urskiljer sig för mobila enheter är att det är anmärkningsvärt mycket bättre att skjuta upp inläsningen av bilder som inte visas på skärmen.

Det anses rimligt att en webbplats laddningstid har en enorm påverkan när det kommer till att behålla och attrahera nya användare. Exempel på detta är Pintrest som reducerade sin uppfattade laddningstid med 40% och noterade att trafiken till webbplatsen ökade med 15% via sökmotoroptimering(https://web.dev/why-speed-matters/). Även för Mobify så föranledde en snabbare laddningshastighet, på bolagets webbplats, till ökade intäkter, där skillnaden på laddningstid var som mest framträdande i bolagets checkout-sida(https://web.dev/why-speed-matters/). 

Det finns således tydliga samband mellan laddningshastighet och bolagens tillväxt men även lönsamhet.

Baserat på de värden som vi kunde avläsa via Pagespeed samt Lighthouse är vår samlade bedömning att webbplatserna bör rangordnas likt nedan utefter respektive webbplats laddningstid, vilket beräknats genom att vi mätt laddningstid tre gånger för varje enskild hemsida: 

kevinpowell.co
Feber.se
aforestlife.com

Hemsida 1 utmärker sig tydligt som hemsidan med kortast laddningstid, vilket egentligen inte är ett oväntat resultat då den har en minimal layout till skillnad från Hemsida 2 och Hemsida 3. I det bifogade kalkylbladet så går det även att tyda att Hemsida 1 vidare urskiljde sig i att endast kalla på nio resurser mot Hemsida 2 och Hemsida 3 som kallar på en betydligt större mängd vilket överstiger hundra stycken. För både Hemsida 2 och Hemsida 3 finns det även stor förbättringspotential, så därav anser vi att Hemsida 1 blir vinnaren i detta fallet.

<iframe class="spreadsheet" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTmFU97IHE0GotcE4FXNo_8dOboQlRHjePuEUy5DdoVHPxIPqwVMykQy9xbZ5GgJeKK-pDKzNd8n-LC/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

Vår bedömning är att den optimala absoluta laddningstiden understiger 2000MS. Mot bakgrund av detta kan vi avläsa att hemsida 1 står sig förhållandevis bra mot detta gränsvärde medan hemsida 2 och hemsida 3 har fortsatt förbättringspotential.


# Referenser
-----------------------
I vår analys använde vi oss av nedan källor:
https://moz.com/learn/seo/page-speed<br>
https://web.dev/<br>
https://developers.google.com/search/blog/2018/01/using-page-speed-in-mobile-search<br>
https://developers.google.com/speed/docs/insights/<br>


# Övrigt
-----------------------

Följande personer har deltagit i att författa rapporten:
Rickard Malmgren, Eva-Lotta Andersson, Jesper Yli-Hukka Högback

# Bilagor
-----------------------
Bilaga 1.1

<img class="picture" src="assets/img/kevinMobile.jpg" width=500 alt="feber" />


Bilaga 1.2. 
<img class="picture" src="assets/img/kevinDesk.jpg" width=500 alt="feber" />


Bilaga 2.1

<img class="picture" src="assets/img/feberMobil.jpg" width=500 alt="feber" />

Bilaga 2.2
<img class="picture" src="assets/img/feberDator.jpg" width=500 alt="feber" />
 

Bilaga 3.1
<img class="picture" src="assets/img/aflMobile.jpg" width=500 alt="feber" />

Bilaga 3.2
<img class="picture" src="assets/img/aflDesk.jpg" width=500 alt="feber" />