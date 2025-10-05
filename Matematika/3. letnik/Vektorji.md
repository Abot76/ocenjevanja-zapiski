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
- Rezultat množenja vektorja z vektorjem je skalar(število)
- vektorje lahko množimo na 2 načina odvisno od podatkov ki jih imamo na voljo
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
# KOLINEARNI In KOMPLANARNI VEKTORJI
- Da sta vektorja *kolinearna* pomeni da lahko 1 vektor izrazimo kot $n$-krat drugi vektor, torej imata enako ali pa nasprotno smer
- Da sta vektorja *linearno nedovisna* pomeni ravno nasprotno - nimata enaka ali nasprotno smeri, posledično velja da nemoremo 1 izrazizi kot $n$-krat 2 vektor. To zapišemo kot $m * \vec{a} + n * \vec{b} = 0$ kjer sta $m$ in $n$ enaka **0**
- *Linearna odvisnost* je enaka kot *kolinearnost*, stem da *linearno odvisnost* ponavadi zapišemo tako da izrazimo da je 1 vektor enak linearni kombinaciji 2 drugih vektorjev. Enačba je enaka: $m * \vec{a} + n * \vec{b} = 0$, stem da pri *linearni odvisnosti* $m$ in $n$ nista enaka **0**!
- 2 *nekolinearna* oz. *linearno neodvisna* vektorja lahko določata bazo ravnine podobno kot enotski vektorji, saj nimata enake ali nasprotne smeri, in lahko izrazita osi ravnine
