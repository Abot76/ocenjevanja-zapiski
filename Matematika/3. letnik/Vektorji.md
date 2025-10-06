Vektor je usmerjena daljica, ki je določena z dolžino in smerjo.
# VRSTE VEKTORJEV
## KRAJEVNI VEKTOR
- Krajevni vektor točke A zapišemo kot $\vec{r}_a$ ali $\vec{0A}$ (vektor iz izhodišča do točke A) 
- Krajevni vektorji imajo začetek v izhodišču in konec v poljubni točki

## NASPROTNI VEKTOR
- Je vektor ki je vzporeden danemu vektorju, ima enako dolžino ampak nasprotno smer.
- zapišemo ga kot $\vec{-a}$ za vektor $\vec{a}$ ali kot $\vec{BA}$ za vektor $\vec{AB}$
- $\vec{a} \parallel \vec{-a}$
- $|\vec{a}| = |\vec{-a}|$
## NIČELNI VEKTOR
- Ima dolžino 0, zato sta začetek in konec v isti točki
- $\vec{AA} = \vec{0}$ ($\vec{AA}$ je zapis vektorja ki se začne in konča v isti točki - torej ničelni vektor, $\vec{0}$ pa je oznaka za ničelni vektor)
- $|\vec{0}| = 0$
## ENOTSKI VEKTOR
- Ima dolžni 1
- Izrazimo ga kot nek vektor deljen s svojo dolžino( $\frac{\vec{a}}{|\vec{a}|}$)
- Enotske vektorje pogosto uporabimo da izrazimo osi koordinatnega sistema, v katerem lahko zapišemo vektorje z ortonomirano bazo, npr: enotska vektorja $\vec{i}$ in $\vec{j}$ predstavljata x in y os, zato lahko zapišemo vektor $\vec{a} = (2, 3)$ z tema enotskima vektorjema(linearna kombinacija) $\vec{a} = (2\vec{i}, 3\vec{j}$)

## ENAKOST VEKTORJEV
- Vektorja sta enaka če imata enako dolžni in smer, posledično ležita tudi na isti premici ali pa sta si vzporedna.

# RAČUNANJE Z VEKTORJI
## SEŠTEVANJE VEKTORJEV
### Trikotniško pravilo
- Vektorja postavimo v sosednjo lego(konec 1. vektorja leži v isti točki kot začetek 2. vektorja - rečemo da začetek in konec sovpadata). Seštevek vektorjev je vektor ki se začne v začetku 1. vektorja in konča v koncu drugega vektorja.
### Paralelogramsko pravilo
- Vektorja postavimo tako da sta njuna začetka v isti točki(rečemo da začetka sovpadata) in ju dokončamo v paralelogram.
## ODŠTEVANJE VEKTORJEV
- Odštevanje vektorjev je prištevanje nasprotnega vektorja od 2. vektorja k 1. vektorju ($\vec{a} + (-\vec{b})$)
## MNOŽENJE VEKTORJA S SKALARJEM(ŠTEVILOM)
- Če vektor pomnožimo s številom $n$ dobimo nov vektor, z enako ali pa nasprotno smerjo(če je $n$ negativen), in dolžino ki je $n$-krat daljša oz krajša.
- Če je $n$ negativen se smer obrne za 180°(kaže v nasprotno smer)
- Če je absolutna vrednost $n$ večja od 1 potem bo nov vektor $n$ krat daljši, npr.: $\vec{a} * 3$ dobimo vektor z enako smerjo in je 3 krat daljši
- Če je absolutna vrednost $n$ manjša od 1 ampak večja od nič bo nov vektor krajši, npr.: $\vec{a} * \frac{1}{2}$ dobimo vektor z enako smerjo in polovično dolžino
## MNOŽENJE VEKTORJA Z VEKTORJEM
- Rezultat množenja vektorja z vektorjem je skalar(število) - zato to računsko operacijo imenujemo *skalarni produkt*
- vektorje lahko množimo na 2 načina odvisno od podatkov ki jih imamo na voljo
- Lastnosti(potrebne samo pri teoriji):
	- *komutativnost* -> $\vec{a} \cdot \vec{b} = \vec{b} \cdot \vec{a}$
	- *asociativnost* -> $\vec{a} (\vec{b} \cdot \vec{c}) = ni asociativnosti$
	- *homogenost* -> $(m * \vec{a}) \cdot \vec{b} = m * (\vec{a} \cdot \vec{b})$
	- 
### Skalarni produkt
- skalarni produkt dobimo ko množimo 2 vektorja med seboj
- $\vec{a} \cdot \vec{b} = |\vec{a}| * |\vec{b}| * \cos\alpha$
- skalarni produkt (produkt množenja 2 vektorjev) je enak produktu dolžini teh 2 vektorjev in njunemu vmesnemu kotu

### Množenje po komponentah
- Je mogoče če imamo vektorje v ortonomirani bazi in poznamo njihove komponente
- Če imamo $\vec{a} = (a_1, a_2)$ in $\vec{b} = (b_1, b_2)$ potem lahko izračunamo: $\vec{a} \cdot \vec{b} = (a_1 * b_1) + (a_2 * b_2)$
- rezultat je seštevek produktov posamičnih komponent

# ODVISNI IN NEODVISNI VEKTORJI
- Linearna kombinacija pomeni da izrazimo 1 vektor kot kombinacijo večih drugih vektorjev, v kombinacijo lahko dodamo tudi skalarje(števila), npr.:
	- $\vec{a} = \vec{b} - \vec{c}$
	- $\vec{c} = n * \vec{a} + m * \vec{b}$
- Poseben redko-uporabljen primer linearne kombinacije je *trivialna linearna kombinacija* v kateri so vsi skalarji($m$, $n$,...) enaki **0**
# KOLINEARNI IN KOMPLANARNI VEKTORJI
- Da sta vektorja *kolinearna* pomeni da lahko 1 vektor izrazimo kot $n$-krat drugi vektor, torej imata enako ali pa nasprotno smer
- Da sta vektorja *linearno nedovisna* pomeni ravno nasprotno - nimata enaka ali nasprotno smeri, posledično velja da nemoremo 1 izrazizi kot $n$-krat 2 vektor. To zapišemo kot $m * \vec{a} + n * \vec{b} = 0$ kjer sta $m$ in $n$ enaka **0**
- *Linearna odvisnost* je enaka kot *kolinearnost*, stem da *linearno odvisnost* ponavadi zapišemo tako da izrazimo da je 1 vektor enak linearni kombinaciji 2 drugih vektorjev. Enačba je enaka: $m * \vec{a} + n * \vec{b} = 0$, stem da pri *linearni odvisnosti* $m$ in $n$ nista enaka **0**!
- 2 *nekolinearna* oz. *linearno neodvisna* vektorja lahko določata bazo ravnine podobno kot enotski vektorji, saj nimata enake ali nasprotne smeri, in lahko izrazita osi ravnine
# PRAVOKOTNA PROJEKCIJA
- Geometrijski pomen pravokotne projekcije je $\vec{a} * \vec{b} = |\vec{a}| * pr_\vec{a} \vec{b}$, kjer je $\vec{b}$ tisti vektor ki ga projiciramo in $\vec{a}$ tisti vektor **na** katerega projiciramo

# KOSINUSNI IZREK(NISEM ZIHER DA JE V TESTU)
- Z njim lahko izračunamo katero koli stranico ali kot v trikotniku pod pogojem da imamo vsaj 2 drugi stranici in 1 kot ali pa 1 stranico in 2 kota.
- $a² = b² + c² - 2*b*c*\cos\alpha$
- $b² = a² + c² - 2*a*c*\cos\beta$
- $c² = a² + b² - 2*a*b*\cos\gamma$
# VEKTORJI V ORTONOMIRANI BAZI
- ortonomirana baza je koordinatni sistem v katerem vsako os predstavlja en enotski vektor(navadno sta to $\vec{i}$ za x in $\vec{j}$ za y os, $\vec{i} \perp \vec{j}$ - sta pravokotna in linearno neodvisna, ker ne ležita na skupni premici)
- Vektorje v ortonomirani bazi zapišemo kot $\vec{a} = n*\vec{i} + m*\vec{j}$ - n-krat vektor i + m-krat vektor j, kar je vbistvu linearna kombinacija enotskih vektorjev. Ta vektorj bi v koordinatem sistemu zapisali tako: $\vec{a} = (n, m)$
- Vektorje v ortonomirani bazi seštevamo in odštevamo po komponentah
- Vektorje v ortonomirani bazi množimo s skalarjem tako da vsako komponento pomnožimo s skalarjem
## ZAPIS VEKTORJA V ORTONOMIRANI BAZI ČE POZNAMO ZAČETNO IN KONČNO TOČKO

^6d8e14

- Recimo da želimo zapisati vektor v ortonomirani bazi ki se začne v točki A in konča v točki B, to naredimo tako za odštejemo krajevna vektorja teh dveh točk in kot rezultat bomo dobili naš vektor. Npr.: točka A - začetek, točka B konec, zapis: $\vec{AB} = \vec{r_B} - \vec{r_A} = (B_1 - A_1, B_2 - A_2)$
# VEKTORJI V ORTONOMIRANI BAZI V PROSTORU
- dodamo še eno os v primerjavi z navadno ortonomirano bazo, in sicer Z os(imenuje se tudi aplikativna os), ki jo predstavimo z enotskim vektorjem $\vec{k}$
- Ostalo je vse enako kot pri navadni ortonomirani bazi

# RAZPOLOVIŠČE DALJICE
- Recimo da imamo vektor $\vec{AB}$ in želimo najti razpolovišče ki je v točki $R$, potem moramo najti komponente vektorja ki se začne v koncu ali začetku vektorja $\vec{AB}$(npr.: točka $A$) in se konča v razpolovišču(točka $R$). Ker je točka $R$ razpolovišče tega vektorja, bo imel novi vektor polovično dolžino in to zapišemo kot: $\vec{AR} = \frac{1}{2}\vec{AB}$
- To potem pretvorimo v krajevne vektorje kot piše zgoraj pri *zapisu vektorja v ortonomirani bazi če poznamo začetno in končno točko: $\vec{r_R} - \vec{r_A} = \frac{1}{2} * (\vec{r_B} - \vec{A})$
- Če izrazimo $\vec{r_R}$ potem dobimo da ima koordinate $(\frac{A_1 + B_1}{2}, \frac{A_2 + B_2}{2})$
# TEŽIŠČE
- Težišče je presečišče vseh težiščnic
- Težišče lahko tudi zapišemo kot *točka ki deli daljico med ogliščem in razpoloviščem nasprotne stranice v razmerju 2:1*
- Torej če imamo oglišče v trikotniku $A$ in točko $R$ ki razpolavlja stranico $a$ bo vektor ki se začne v oglišču $A$ in konča v težišču izražen z: $\vec{AT} = \frac{2}{3}\vec{AR}$ in če poznamo koordinate točk $A$ in $R$(dobimo tako da izračunamo razpolovišče kot v prejšni točki) ter komponente vektorja $\vec{AT}$, lahko to enačbo izrazimo z krajevnimi vektorji: $\vec{r_T} - \vec{r_A} = \frac{2}{3} (\vec{r_R} - \vec{r_A})$, potem pa samo izpostavimo krajevni vektor $\vec{r_T}$ in izračunamo njegove komponente da dobimo koordinate težišča