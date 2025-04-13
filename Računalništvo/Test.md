Kaj je operacijski sistem
Kaj je naloga operacijskega sistema
Opiši in predstavi kaj je PCB
Kako se izvede prekinitev
Napiši vse plasti/nivoje ISO/OSI referenčnega modela v pravem vrstnem redu
Predstavi niti v operacijskih sistemih
Naštej razvrščevalne algoritme
Kaj je zbirni in kaj je strojni jezik
Kaj je sklad in kako ga uporabimo
Katere načine naslavljanja pozamo
Kakšna je razlika med procesorjem in mikrokrmilnikom
Opiši in predstavi naloge fizičnega sloja
Kakšna je razlika med WAN in LAN omrežji
Kaj predstavlja zapis 192.168.100.0

## Prekinitve
- prekinitev je dejanje na katerega se procesor takoj odzove in ne čaka v vrsti na izvršitev. Ob vsaki prekinitvi se izvršijo različni ukazi.
- Past(en.: trap) je vrsta prekinitve ki izvira iz procesorja zaradi poskusa izvršitve neobstoječe ukaza ali prekoračitve aritmetičnih sposobnosti(deljenje z 0)
- Prekinitve so lahko zunanje(strojne) ali pa notranje(programske)
- PSP - prekinitveni servisni program <- izvede se ob vsaki prekinitvi
- Ko se pojavi prekinitev se izvede PSP, ta shrani stanje procesorja(vrednosti vseh registrov) v sklad, preveri v prekinitveni vektor(seznam možnih prekinitev) kaj mora izvesti ob tej prekinitvi in to rutino izvrši. Na koncu obnovi stanje procesorja(vrednosti registrov) iz sklada
## Operacijski sistemi
- Operacijski sistem zapolni vrzel med strojno opremo in uporabniškimi ter sistemskimi programi(OS poda enostaven vmesnik ki ga lahko programi uporabijo da komunicirajo z strojno opremo)
- Ko se računalnik zažene OS naloži vse gonilnike potrebne za delovanje priklopljene strojne opreme(miška, tipkovnica, zaslon)
- Med uporabo računalnika OS dinamično dodeljuje in odvzema sredstva(RAM, CPE cikli,...) programom, ki se izvajajo(tudi tistim v ozadju)
- SISTEMSKA PROGRAMSKA OPREMA: programi ki omogočajo lažje izvrševanje ukazov. Delimo jih na:
	- Sistemski programi - za omrežje, upravljanje baz podatkov, za varnost
	- Sistemska orodja - sistemski programi za razvijanje računalniških sistemov


## Procesi
- Ko računalnik zaposlimo rečemo da mu damo "posel" - sinonim za proces. Takrat se mora ta proces naložit v glavni pomnilnik in pripraviti na izvršitev
- Izvrševanje poslov ima 4 faze:
	- vnos posla v računalniški sistem(naloži se v glavni pomnilnik)
	- čakanje v vhodni vrsti na obdelavo/izvršitev(naenkrat se lahko izvaja samo en proces/posel zato obstaja čakalna vrsta)
	- izvršitev posla
	- končanje posla

- Proces je program ki je naložen v glavni pomnilnik in je pripravljen na izvršitev
	- STANJA: aktiven, se izvaja, blokiran, čaka
	- ZGRADBA:
```
		+----------+  +----------+  +-------+
		|Programska|  |Programski|  | Sklad |
		| sekcija  |  |  števec  |  +-------+
		+----------+  +----------+  |       |
		.             +----------+  +-------+
		+----------+  | Registri |  |       |
		|Podatkovna|  +----------+  +-------+
		| sekcija  |  +----------+  |       |
		+----------+  +----------+  +-------+
```
- Razvrščevalnik procesov je program ki nadzoruje kateri proces se kdaj izvaja
- Informacije o procesu so zapisane v interni podatkovni strukturi(način zapisa podatkov). Ta struktura se imenuje PCB(en.: Process control block) - procesni nadzorni blok
- ZGRADBA:
```
	+---------------------+---------+
	| Kazalec za povezavo | Stanje  | <- lokacija datoteke na disku
	|     v programu      | procesa | <- aktiven/se izvaja/blokiran/čaka
	+---------------------+---------+
	|     Številka procesa(ID)      |
	+-------------------------------+
	|       programski števec       |
	+-------------------------------+
	|           prioriteta          | <- kako pomemben je proces
	+-------------------------------+
	|        meje pomnilnika        | <- območje v pomnilniku namenjeno 
	+- - - - - - - - - - - - - - - -+    procesu
	|         tabela strani         | <- shranjuje kateri logični naslov
	+-------------------------------+    ima kateri fizični naslov v RAM
	|     Seznam odprtih zbirk      | <- katere knjižnice uporablje
	+-------------------------------+    (zbirke sistemskih orodij)
	|        podatki računa         |
	+-------------------------------+
```

## Niti
- proces lahko razdelimo na več niti - npr.: ena bere podatke iz diska, druga jih procesira... Izvajajo se asinhrono(sočasno)
- Uporabne so zato ker lahko en proces dela samo eno stvar naenkrat(npr.: bere disk, procesira, shranjuje podatke...) in vsako napravo lahko uporablja samo en proces naenkrat(npr.: bere disk). Če proces razdelimo na niti lahko ena bere disk, medtem ko druga sproti procesira podatke, tako znatno zmanjšamo čas da nek proces izvede svojo opravilo in posledično drugi procesi pridejo prej na vrsto
- Nit lahko imenujemo tudi LWP(en.: light weight process), vsak težek proces ima samo 1 nit
- TEŽEK PROCES:
```
	+-------------------------+
	| [REGISTRI] [PC] [SKLAD] |
	+-------------------------+
	|  [PODATKI]  [DATOTEKE]  |
	+-------------------------+
	|        [PROGRAM]        |
	|            |            |
	|            V            |
	|     samostojna nit      |
	+-------------------------+

```
- PROCES RAZDELJEN NA NITI:
```
	+--------------+--------------+--------------+
	|  [REGISTRI]  |  [REGISTRI]  |  [REGISTRI]  |
	| [PC] [SKLDA] | [PC] [SKLAD] | [PC] [SKLAD] |
	+--------------+--------------+--------------+
	|        [PODATKI]          [DATOTEKE]       |
	+--------------------------------------------+
	|      |          [PROGRAM]          |       |
	|      |              |              |       |
	|      V              V              V       |
	|    NIT 1          NIT 2          NIT 3     |
	+--------------------------------------------+
```
- Problem pri nitih je da je imajo skupni pomnilniški prostor(delijo si območje v pomnilniku), ker so vse del istega procesa, zato lahko pride do izgube podatkov če pri snovanju procesa ne uskladimo katera nit bo kdaj pisala na kateri naslov v pomnilniku, in na katerem naslovu bo pričakovala podatke od druge niti. To je problem samo pri nitih ki izvirajo iz istega procesa

## Medprocesna komunikacija
- Če proces nima dobenega stika z drugimi procesi in iz njimi ne komunicira/ne izmenjuje podatkov potem rečemo da je neodvisen.
- Pogosto potrebujemo procese ki komunicirajo med seboj <- takim procesom rečemo da so sočasni(concurrent), med njimi mora biti vzpostavljena vez. Ta vez se uporablja ali za izmenjavo informacij ali pa sinhronizacijo
- Poznamo 2 načina medprocesne komunikacije (IPC - en.: Inter-process communication)
	- Skupni pomniški prostor(območje v pomnilniku) - enako kot niti istega procesa. Tam lahko sočasni procesi shranjujejo podatke ki si potem dostopni ostalim procesom
	- Pošiljanje sporočil(kot nabiralniki - en.: socket) - deluje kot navadna pošta stem da se mora najprej med procesoma vzpostaviti komunikacijska zveza da si lahko pošiljata sporočila. Ta vrsta medprocesne komunikacije je mogoča samo na OS ki podpirajo IPC

## Razvrščevanje procesov
- procesi se razvrščujejo glede na:
	- izkoriščenost procesorja - kako zaposlen je procesor trenutno
	- prepustnost(throughput) - kako produktiven je CPE/kako hitro dela
	- obračalni čas(turnaround time) - koliko časa bo nek proces trajal
	- čakalni čas - čas da ta proces pride na vrsto
	- odzivni čas - čas od izida ukaza do vrnitve rezultatov
- Algoritmi:
	- prvi v čakalni vrsti, najprej izvršen(en.: FIFO - first in, first out)
	- najkrajši posli naprej - najprej se izvedejo posli katerih obračalni čas je najkrajši
	- prioriteta - posli se izvajajo po vrsti glede na njihovo prioriteto/nujnost
	- krožna prioriteta

## Popolni zastoj in pomanjkanje
- Do popolnega zastoja pride ko se delovanje procesorja nepričakovano ustavi
- Popolni zastoj nastane zaradi:
	- če vsaj 1 vir sistema ni deljiv(npr.:disk)
	- če en proces zasede en vir in čaka na še na drugi vir, ki pa ga trenutno zaseda drug proces
	- če OS deluje na neprekinjevalnem načinu - zaseden vir lahko sprosti samo proces ki ga trenutno ukopira, to pa naredi samo takrat ko je končal z svojo rutino
	- če pride do krožnega čakanja - proces 1 čaka na vir ki ga zaseda proces 2, proces 2 pa čaka na vir ki ga zaseda proces 1
- Metode za obravnavanje zastojev
	- Protokol da nikoli ne vstopimo v zastoj - OS je zgrajen na način da ne more nikoli priti do dobene od teh situacij
	- Dovolimo vstop v zastoj vendar se iz njega znamo rešit - imamo navodila kaj narediti v primeru zastoja da ga razrešimo
	- Možnost popolnega zastoja ignoriramo - Pretvarjamo se da popoln zastoj ni mogoč, če pa pride do njega pa zamrzne cel računalnik. Tak pristop ima UNIX operacijski sistem(na njem sta zgrajene MacOS in Linux)

## Pomnilnik
- Računalnik za svoje delovanje potrebuje delavni pomnilnik v katerega shrani začasne informacije potrebne za delovanje programov, OS...
- Del pomnilnika vedno zaseda OS z vsemi podatkovnimi strukturami, rutinami, algoritmi...
- V večprogramskem okolju je zelo pomembno da ima vsak proces na voljo dovolj pomnilnika za svoje delovanje in je v njegovem območju v pomnilniku zavarovan pred nezaželenimi posegi v njegove podatke
- Dodeljevanje pomnilnika procesom upravlja OS, tako da doseže največjo zmogljivost
- Naslovna logika - Severni most(tako se imenuje ker je na sistemskih programih prikazan nad vsemi ostalimi napravami) prevede virualne naslove pomnilnika ki jih želi dostopati procesor v dejanske fizične naslove v pravem čipu na pomnilniku
- Npr.: Imamo 4 64bitne pomnilniške čipe
```                         +------+
                        +-->|ČIP 00|  virtualni naslov ki ga pozna CPE: 10 011101
                        |   +------+                                    ^  ^
          +--------+    |   +------+                                    |  naslov
+-----+   |Naslovna|    +-->|ČIP 01|                                    ID čipa
| CPE |-->| logika |----+   +------+   Naslovna logika prevede naslov
+-----+   +--------+    |   +------+   iz procesorja v naslov na enem 
					    +-->|ČIP 10|   izmed pomnilnišik čipov. V tem 
					    |   +------+   primeru sta prva 2 bita namenjena
					    |   +------+   ID-ju čipa, in ostalih 6 naslovu
					    +-->|ČIP 11|   na tem čipu.
					        +------+
```

## Zbirčni/datotečni sistem
- Podatki so lahko shranjeni na različnih medijih: magnetni diski(HDD), SSD, diskete, trakovi, optični diski... Podatki so na njih vedno zapisani v zbirkah/datotekah kot skupki informacij, ki so med seboj logično vezani glede na izvor, uporabo...
- Podatkovne zbirke lahko gledamo kot skupek fizičnih zapisov na podatkovnih nosilcih(npr.: zareze na gramofonski plošči), ali pa kot skupek logičnih zapisov, ki vsak zase vsebuje neke informacije.
- Organizacija - praviloma so zbirke opremljene z naslednjimi atributi:
	- Ime - namenjeno za uporabnika, da ve kaj je v datoteki
	- tip - katere vrste podatkov vsebuje datoteka(npr.: video, tekst, zvok...)
	- lokacija - kje v podatkovni strukturi se nahaja datoteka - to ni fizična lokacija datoteke na fizičnem mediju
	- velikost - kako dolg je ta zapis podatkov(datoteka) - merjen v zlogih(dolžina zloga je odvisna od datotečnega sistema, ponavadi 4096 bytov)
	- zaščita - kdo ima dovoljenje delati kaj z datoteko(npr.: en uporabnik jo lahko samo bere, drug pa ima popoln nadzor)

## Računalniška omrežja
- sestavljena iz fizičnega in storitvenega dela
	- fizični del - fizične komponente ki povezujejo računalnike(npr.:NIC - omrežna vmesniška kartica(en.:Network interface card), omrežno stikalo(ruter), dostopna točka...)
	- storitveni del - infrastruktura ki omogoča storitve aplikacijam(npr.: IPTV, VoIP, www...)
- Komponente omrežja:
	- končni sistemi(odjemalniki in stržniki)
	- jedro omrežja(usmerjevalniki paketov)
	- komunikacijske povezave(optika, bakrene žice, brezžične povezave - WiFi...)
- Da lahko komuniciramo z vsemi napravami morajo vse naprave razumeti enak protokol. 2 najbolj uporabljena sta omrežni standardni protokol - OSI in prenosni nadzorni protokol - TCP(en.: Transmission control protocol), ki pogosto uporablja skupaj z internetnim protokolom IP. Skupaj ju imenujemo TCP/IP
- OSI:
```
    OSI referenčni model           TCP/IP model <- novejši
+-------------------------+      +-------------------------+
|    Aplikacijski sloj    |      |    Aplikacijska plast   |
+-------------------------+      |                         |
|   Predstavitveni sloj   |      |                         |
+-------------------------+      |                         |
|       Sejni sloj        |      |                         |
+-------------------------+      +-------------------------+
|    Transportni sloj     |      |    Transportna plast    |
+-------------------------+      +-------------------------+
|      Omrežni sloj       |      |       Omrežna plast     |
+-------------------------+      +-------------------------+
|Sloj podatkovne povetzave|      |     Plast omrežnega     |
+-------------------------+      |        vmesnika         |
|       Fizični sloj      |      |                         |
+-------------------------+      +-------------------------+
```

## Omrežni standardi
- standard pomeni en ali več formalno sprejetih protokolov, ki ga razumejo vsi uporabniki, procesi in naprave
- dogovorjena pravila in postopki tvorijo protokole
- INDUSTRIJSKI(proizvajajo jih večji proizvajalci):
	- Za njih je značilno da se zaradi enostavne in široke uporabe hitro razširijo
	- SNA <- proizvedel IBM
	- DSN <- proizvedel Hawlett Packard(HP)
	- TCP/IP
- PRAVNI(nastanejo v okviru mednarodnih organizacij za standardizacijo)
	- ISO
	- ANSI
	- IEEE

## Fizična plast omrežja
- Opredeljuje način kodiranja bitov z neko fizično opremo za prenos po mediju(baker, optika, WiFi)
- prenos bitov poteka v analogni ali pa fizični obliki
- prenosni medij - naprava ki prenaša te bite od točke A do točke B
- prenosni mediji prenašajo informacije z neko frekvenco(hitrostjo). Frekvenčna karakteristika medija nam pove katere frekvence lahko prenaša. Lahko so digitalni - prenašajo diskretne vrednosti(0 ali 1) ali pa analogni(vrednosti ki jih ne moremo natančno izmeriti).
- Modem - naprava ki prevaja analogne signale v digitalne in obratno

## Prenosni mediji
- Zvit par(en.: twisted pair) - bakrene žice ki so po parih zvite skupaj(do 4 pare na kabel). navadno ime RJ45 priključek. Zmore hitrosti do 10Gbps <- to hitrost lahko doseže zaradi prepletenih parov, ki izničijo motnje in šum
- Koaksialni kabel - žica, ki je ovita z izolacijo, preko izolacije še z enim prevodnikom in nato še z eno izolacijo. Zelo odporna proti motnjam. Hitrost do 2Gbps
- Optika - zelo prosojno steklo, ki je v obliki žice in obdan z izolacijo. Prenaša lahko več valovnih dolžin svetlobe, katera vsaka prenaša svoj signal. Teoretična hitrost 32Tbps

## Logični naslovi/IP naslovi
- Poznamo 2 standarda: IPv4 in IPv6
	- IPv4 ima 32 bitov(4 byte)
	- IPv6 ima 128 bitov(16 bytov)
- Pri logičnih naslovim imamo tudi masko ki nam pove koliko bitov od logičnega naslova je namenjenih za Net ID in koliko za Host ID. posledično določa tudi maksimalno število naprav povezanih na to omrežje
```             |
IPv4: 192 . 168 | 100 . 045 <- primer
      | NET ID| | |HOST ID|
			    V
              maska
```