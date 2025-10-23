# ALGORITMI

Definicija:
`Algoritem je navodilo, s katerim rešujemo določen problem. Običajno je zapisan kot seznam korakov, ki nas pripeljejo do rešitve problema.`
Algoritem lahko zapišemo na več načinov:
- naravni jezik
- grafično - diagram poteka
- psevdokod
- programski jezik
Način na kateri zapišemo algoritem je odvisen od potreb. Recimo če bo računalnik izvajal algoritem ga bomo zapisali v programskem jeziku.

Lastnosti algoritma:
- pravilni algoritem mora pravilno rešiti problem - za določene vhodne podatke mora izračunati pravilne izhodne podatke
- popolnost - vedno vrne rešitev problema če obstaja
- razumljivost - izvajalec(človek, računalnik) ga mora enoumno razumeti
- končnost - izvajanje se mora po določenem številu korakov končati(ne sme biti neskončen)
- enoumnost - obstaja le en način interpretacije ukazov
- determinizem - če sledimo ukazom, bomo vedno dosegli želeni rezultat
- splošnosti - algoritem mora biti sposoben rešiti čim več problemov
# PROGRAMSKI JEZIKI
Programski jezik je umetni jezik, namenjen reševanju problemov z računalnikom. V programskem jeziku lahko napišemo navodila/algoritem, ki ga potem računalnik lahko izvede. 
Program moramo pred izvajanjem prevesti v jezik ki ga računalnik razume - strojni jezik.

Programskih jezikov je veliko, lahko jih delimo glede na 2 merili
1. Po namembnosti:
	- proceduralni
	- objektni
	- skriptni
	- funkcijski
	- spletni
2. Kronološko
	1. generacija: nižji jeziki - strojni jeziki
	2. generacija: nižji jeziki - zbirni jeziki
	3. generacija: višji jeziki - C++, Java, PHP
	4. generacija: višji jeziki - SQL, Matlab

# DIAGRAM POTEKA
## Spremenljivke, tekst, operatorji in računanje
### Spremenljivke
- Spremenljivke **shranjujejo** v sebi vrednost, ki se lahko čez čas **spreminja**, označimo jih lahko z poljubnimi črkami in besedami, ampak **brez simbolov in brez presledkov**.
- Poznamo tudi konstante. So podobne spremenljivka, vendar njim vrednosti nemoremo spreminjati(je stalna). V diagramu poteka jih **ne uporabljamo**
### Tekst
- Ko moramo v diagramu poteka uporabiti nek tekst, besedo ali črko, to damo med narekovaje(`"Test 123"`, `"test"`, `"a"`). Ker je v narekovajih to ni spremenljivka, če pa nebi uporabili narekovajev bi algoritem to smatral kot spremenljivko. **ŠTEVILK NE PIŠEMO MED NAREKOVAJE RAZEN ČE SO DEL TEKSTA TAKO KOT V ZGORNJEM PRIMERU!**
### Operatorji
- Uporabljamo različne operatorje da stvari primerjamo med sabo, to imenujemo trditev. Trditev je lahko resnična ali pa neresnična:
	- je enako: `==` <- 2 enačaja
	- ni enako: `!=` <- klicaj in enačaj
	- je večje: `>`
	- je manjše: `<`
	- je večje ali enako: `>=`
	- je manjše ali enako: `<=`
- ko želimo preveriti ali sta 2 trditvi resnični, ali pa je vsaj ena izmed trditev resnična lahko to napišemo z besedami ali pa operatorji
	- in: `&&`
	- ali: `||` 
	```Primer
	x > 1 in x < 5 <- preveri da je x večji od 1 in hkrati manjši od 5
	x > 1 && x < 5 <- drug način zapisa z operatorjem
	
	x == 1 ali x == 2 <- preveri če je x enak 1 ali pa če je enak 2
	x == 1 || x == 2 <- druga možnost zapisa z operatorjem
	```
- Med seboj lahko primerjamo spremenljivke, tekst in številke

### Računanje
- pri računanju v diagramu poteka uporabimo malo drugačne simbole:
	- seštevanje in odštevanje ostane enako
	- množenje: `*`
	- deljenje: `/`
	- ostanek deljenja: `%`
- Ostanek deljenja nam vrne ostanek pri deljenju nekega števila z enim drugim, npr.: ostanek pri deljenu 7 z 3 je 1, `7 % 3 == 1` <- ta trditev je resnična  
## Simboli
### Start in konec
- označujeta kje se algoritem začne in konča
```mermaid
flowchart TD
	A([Start])
	B([Konec])
```
### Smer poteka
- Smer poteka v algoritmu označimo tako da posamezne bloke povežemo s puščicami
```mermaid
flowchart TD
	A([Start]) --> B[naredi nekaj]
	B --> C([Konec])
```


### Vnos in izhod
- Uporabimo ju ko želimo uporabniku za zaslon **izpisati neke informacije**, ali pa od njega **potrebujemo da nekaj vnese**
#### Izhod
- v okvir napišemo veliko **tiskano črko i in dvopičje**(`I: `), zatem pa to kar želimo izpisati. Če je to spremenljivka napišemo **ime spremenljivke**, če pa želimo izpisati tekst pa ta **tekst damo med narekovaje**(`"test"`). Če želimo izpisati več vrstic **dodamo znak $\sqcup$**
```mermaid
flowchart TD
	A[/I: "test"/]
```
#### Vhod
- v okvir napišemo **veliko tiskano črko v in dvopičje**, za tem pa **ime spremenljivke** v katero hočemo shranit to kar bo uporabnik vnesel(`V: x` - *primer za spremenljivko x*). Po tem ko uporabnik vnese nekaj se avtomatsko naredi na zaslonu **nova vrstica**, torej če bi za vnosom nekaj izpisali na ekran, bi ta tekst bil v novi vrstici, brez da mi dodamo simbol za novo vrstico.```
```Primer vnosa

  15 <- vnesel uporabnik
  Vnesel si število 15. <- izhod avtomatsko izpisan v novi vrstici
```
  ```mermaid
  flowchart TD
	  A[/V: x/]
  ```
### Shranjevanje v spremenljivke
- V spremenljivke shranimo vrednost tako da napišemo ime spremenljivke, enačaj in nato vrednost ki jo želimo shraniti. Namesto vrednosti lahko zapišemo tudi račun, ki lahko tudi vsebuje isto spremenljivko v katero bomo shranili to vrednost.
```mermaid
flowchart TD
	A[x = 5]
```
```mermaid
flowchart TD
	A[x = 4 * 5]
```
```mermaid
flowchart TD
	A[x = x + 1]
```
- Zadnji primer bi uporabili ko moramo nekaj šteti, vsakič ko pridemo do teka bloka se bo vrednost spremenljivke x povečala za ena, saj v spremenljivko x shranimo vrednost, trenutne spremenljivke x(preden shranimo novo vrednost) + 1. Recimo da je `x = 2`, potem ko izvedemo `x = x + 1`, bo diagram najprej preveril kaj je vrednost računa na desni strani enačaja. Ker je trenutno `x = 2` je vrednost računa 3 in bo v spremenljivko x shranil vrednost 3. Ko se ta blok ponovno izvede, vrednost x nebo več 2 ampak 3 in bo zato po izvedbi tega bloka `x = 4`
### Odločitev
- V simbol za izbiro napišemo neko trditev ali pa kombinacijo trditev. Iz simbola pa povlečemo 2 puščici za 2 možni vejitvi - je trditev pravilna, ali pa če je nepravilna. Ti 2 puščici označimo z `DA` ali pa `NE`.
```mermaid
flowchart TD
	A{trditev}
	A --> |DA| B[vejitev 1]
	A --> |NE| C[vejitev 2]
```
#### Zanka
- če želimo narediti zanko, ki se ponovi n krat potem uporabimo simbol za izbiro, in eno spremenljivko ki bo štela kolikokrat smo zanko že ponovili. *Primer kjer želimo da se zanka ponovi 5 krat. Spremenljivka x šteje ponovitve*
 ```mermaid
  flowchart TD
	  A[Start] --> K[x = 1]
	  K --> B{x > 5} 
	  B -->|DA| C[konec] 
	  B -->|NE| D[x = x + 1]
	  D --> E[naredi nekaj]
	  E --> B
  ```
  