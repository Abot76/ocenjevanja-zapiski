## Kompleksna števila
1. **Definirajte množico kompleksnih števil. Kako grafično upodobimo (predstavimo) kompleksna števila?**
	Kompleksna števila so razširitev realnih števil, ki vključujejo imaginarno enoto i, za katero velja $i^2 = -1$. Vsako kompleksno število lahko zapišemo v obliki $z = a + bi$, kjer sta $a$ in $b$ realni števili.
	Grafično kompleksna števila predstavimo v kompleksni ravnini, kjer:
	- Vodoravna os (x-os) predstavlja realni del števila (Re(z))
	- Navpična os (y-os) predstavlja imaginarni del števila (Im(z))
2. **Definirajte operacijo seštevanja v množici kompleksnih števil. Opišite geometrijski pomen seštevanja kompleksnih števil.**
	Seštevanje kompleksnih števil je definirano po komponentah:
	$(a + bi) + (c + di) = (a + c) + (b + d)i$
	Geometrijski pomen seštevanja kompleksnih števil je vektorsko seštevanje v kompleksni ravnini - če kompleksni števili predstavimo kot vektorja iz izhodišča do točk, ki predstavljata ti števili, je vsota teh števil vektor, ki ga dobimo po pravilu paralelogram.
3. **V kompleksni ravnini predstavite podmnožici kompleksnih števil $A = {z \in C; Im(z) = 2}$ in $B = {z \in C; Im(z) = Re(z)}$**
	Množica A predstavlja vse kompleksne številke, ki imajo imaginarni del enak 2 - to je vodoravna premica z y-koordinato 2.

	Množica B predstavlja vse kompleksne številke, kjer je imaginarni del enak realnemu delu - to je premica, ki poteka pod kotom 45° in gre skozi koordinatno izhodišče.
___
## Množenje kompleksnih števil
1. **Definirajte operacijo množenja v množici kompleksnih števil. Zapišite primer.**
	Množenje kompleksnih števil je definirano kot:
	$(a+bi)(c+di) = (ac-bd) + (ad+bc)i$
	Primer: $(2+3i)(1+i) = (2-3) + (2+3)i = -1+5i$
2. **Opišite geometrijski pomen množenja kompleksnega števila s številom -1 in geometrijski pomen množenja kompleksnega števila s pozitivnim realnim številom.**
	Geometrijski pomen množenja:
	- Množenje z -1 pomeni rotacijo za 180° okoli izhodišča
	- Množenje s pozitivnim realnim številom pomeni razteg za ta faktor
3. **Naj bo n naravno število. Izračunajte in , kjer je n letošnja letnica.**
	$i^{2025}=i$
4. **Izberite kompleksno število z = a + bi, kjer sta a in b od nič različni realni števili, in izračunajte z 2.**
	$a^2 - b^2 + 2abi$
	$a, b \neq 0$
___
## Absolutna vrednost kompleksnega števila
1. **Definirajte absolutno vrednost kompleksnega števila. Na primeru pokažite izračun absolutne vrednosti kompleksnega števila.**
	$$|z| = \sqrt{a^2 + b^2}$$
	Primer: Za $z=3+4i$ je $|z| = \sqrt{3^2 + 4^2} = \sqrt{25} = 5$

2. **Na primeru izbranega kompleksnega števila $z =a +bi$, kjer je $a \neq 0$ in $b \neq 0$, pokažite, da je $|2z|=2|z|$.**
	$z=2+3i$
	$|2z|=2|z|$
	$|2z| = |2(2+3i)| = |4+6i| = \sqrt{16+36} = \sqrt{52}$
	$2|z| = 2|2+3i| = 2\sqrt{4+9} = 2\sqrt{13} = \sqrt{52}$
	$|2z| = 2|z|$

3. **V kompleksni ravnini predstavite množico točk ${z \in C; |z| \leq 3}$ Zapišite primer kompleksnega števila $z = a + bi$ iz te množice, kjer je a pozitivno, b pa negativno realno število.**
	Množica $\{z \in \mathbb{C} ; |z| \leq 3\}$ predstavlja krog s središčem v izhodišču in polmerom 3.
___
## Konjugirana vrednost kompleksnega števila
1. **Definirajte konjugirano vrednost kompleksnega števila in razložite njen geometrijski pomen.**
	Konjugirana vrednost kompleksnega števila $z=a+bi$ je $\overline{z}=a-bi$. Geometrijski pomen: točka je zrcaljena čez realno os.
2. **Dokažite, da je konjugirana vrednost vsote dveh kompleksnih števil enaka vsoti njunih konjugiranih vrednosti**
	 $(z_1 + z_2)^- = \overline{z_1} + \overline{z_2}$:
	 $$(z_1 + z_2)^- = (a + c) - (b + d)i$$
$$\overline{z_1} + \overline{z_2} = (a + c) - (b + d)i$$

3. **Izberite kompleksno število $z =a +bi$, kjer sta a in b od nič različni realni števili, in izračunajte $z^{-1}$.**
	$z^{-1}=\frac{1 \cdot (2 - 3i)}{(2 + 3i)(2 - 3i)} = \frac{2 - 3i}{2^2 - (3i)^2}$
	$z^{-1} = \frac{2}{13} - \frac{3}{13}i$
___
## Potence s celimi eksponenti
1. **Definirajte potenco z naravnim in potenco s celim eksponentom.**
	Potenca z naravnim eksponentom je produkt n enakih faktorjev: $a^n = a \cdot a \cdot ... \cdot a$ (n-krat)
	Potenca s celim eksponentom: za negativne eksponente velja $a^{-n} = \frac{1}{a^n}$
2. **Naštejte tri pravila za računanje s potencami s celimi eksponenti.**
	Tri pravila za računanje s potencami:
	$a^m \cdot a^n = a^{m+n}$
	$\frac{a^m}{a^n} = a^{m-n}$
	$(a^m)^n = a^{m \cdot n}$
3. **Na primerih potenc s celimi eksponenti pokažite uporabo dveh izmed zgornjih pravil.**
	Primer uporabe dveh pravil:
	$2^3 \cdot 2^4 = 2^{3+4} = 2^7$ (prvo pravilo)
	$(2^3)^2 = 2^{3 \cdot 2} = 2^6$ (tretje pravilo)
___
## Koreni
1. **Definirajte $\sqrt[n]{x}$ za poljubno naravno število n. Zakaj je pomembno, ali je n sodo ali liho število?** 
	$y = \sqrt[n]{x}$ natanko takrat, ko je $y^n = x$.
	Sodost/lihost n je pomembna, ker:
	Pri sodem n ima enačba $y^n = x$ za x > 0 dve rešitvi (±$\sqrt[n]{x}$), za x < 0 pa nima realnih rešitev
	Pri lihem n ima enačba $y^n = x$ natanko eno realno rešitev za vsak x
2. **Kako množimo korene z enakima in kako z različnima korenskima eksponentoma?**
	Z enakima eksponentoma: $\sqrt[n]{a} \cdot \sqrt[n]{b} = \sqrt[n]{ab}$
	Z različnima eksponentoma: pretvorimo na skupni eksponent
3. **Kako korenimo produkt? Kako korenimo korene?**
	Korenjenje produkta in korenov:
	Korenjenje produkta: $\sqrt[n]{ab} = \sqrt[n]{a} \cdot \sqrt[n]{b}$
	Korenjenje korena: $\sqrt[m]{\sqrt[n]{a}} = \sqrt[mn]{a}$
4. **Racionalizirajte imenovalec ulomka $\frac{a}{a+\sqrt{b}}$**
	$\frac{a}{a+\sqrt{b}} \cdot \frac{a-\sqrt{b}}{a-\sqrt{b}}$
	
	$\frac{a^2 - a\sqrt{b}}{a^2 - b}$
	$a^2 \neq b$
___
## Potence z racionalnimi eksponenti
1. **Definirajte potenco s pozitivno osnovo in racionalnim eksponentom.** 
	Potenca s pozitivno osnovo in racionalnim eksponentom $\frac{p}{q}$ je definirana kot:
	$a^{\frac{p}{q}} = \sqrt[q]{a^p}$, kjer je $a > 0$
2. **Povejte tri pravila za računanje s takimi potencami**
	$a^r \cdot a^s = a^{r+s}$
	$\frac{a^r}{a^s} = a^{r-s}$
	$(a^r)^s = a^{r \cdot s}$
3. **Podajte primera dveh potenc z enakima osnovama in različnima pozitivnima racionalnima eksponentoma (ki nista celi števili) in izračunajte njun produkt. Izrazite ti dve potenci še kot korena in izračunajte njun produkt.**
	$2^{\frac{1}{2}}$ in $2^{\frac{1}{3}}$
	$2^{\frac{5}{6}}$
	$\sqrt[6]{2^5}$
___
## Premice
1. **Definirajte vzporednost premic v ravnini.**
	Premici sta vzporedni, če ležita v isti ravnini in nimata skupne točke.
2. **Naštejte vse možne medsebojne lege dveh premic v ravnini.**
	Možne medsebojne lege dveh premic:
    1. Sekajoči se premici (imata eno skupno točko)
    2. Vzporedni premici (nimata skupne točke)
    3. Sovpadajoči premici (imata vse točke skupne)
3. **Naštejte dve lastnosti relacije vzporednosti premic v ravnini.**
	 Lastnosti relacije vzporednosti:
    1. Refleksivnost (vsaka premica je vzporedna sama sebi)
    2. Simetričnost (če je p || q, je tudi q || p)
4. **Povejte aksiom o vzporednici.**
	Skozi točko, ki ne leži na dani premici, lahko potegnemo natanko eno vzporednico k dani premici.
___
## Koti 1
1. **Pojasnite pojme ničelni, pravi, iztegnjeni in polni kot.**
	- Vrste kotov:
    - Ničelni kot: 0°
    - Pravi kot: 90°
    - Iztegnjeni kot: 180°
    - Polni kot: 360°
2. **Pojasnite pojma sokota in sovršna kota.**
	- Sokota sta dva kota s skupnim vrhom in enim skupnim krakom
	- Sovršna kota sta dva kota s skupnim vrhom, katerih kraka sta nasprotna poltraka
3. **Kdaj je dani kot oster in kdaj top?**
	- Oster kot: meri manj kot 90°
	- Top kot: meri več kot 90° in manj kot 180°
4. **Kdaj sta kota komplementarna in kdaj suplementarna?**
	- Komplementarna kota: vsota je 90°
	- Suplementarna kota: vsota je 180°
___
## Koti 2
1. **Definirajte kotno stopinjo, kotno minuto in kotno sekundo.**
	- Kotna stopinja (1°): 1/360 polnega kota
	- Kotna minuta (1'): 1/60 stopinje
	- Kotna sekunda (1''): 1/60 minute
2. **Definirajte radian.**
	- Radian (rad): razmerje med dolžino loka ki ga na krožnici označuje kot in med polmerom kroga
3. **Zapišite zvezo med stopinjami in radiani.**
	- Zveza: 180° = π radianov
4. **Koliko stopinj meri en radian?**
	- 1 radian ≈ 57.2958°
5. **Koliko radianov merijo koti 30°, 45°, 60° in 90°?**
	- 30° = $\frac{π} {6}$
	- 45° = $\frac{π} {4}$
	- 60° = $\frac {π} {3}$
	- 90° = $\frac {π} {2}$
6. **Kdaj sta kota skladna?**
	- Skladna kota imata enako vrednost.
___
## Trikotnik
1. **Definirajte trikotnik.**
	Trikotnik je geometrijski lik, določen s tremi točkami, ki ne ležijo na isti premici, in daljicami, ki jih povezujejo.
2. **Definirajte notranji in zunanji kot trikotnika.**
	- Notranji kot: kot med dvema stranicama trikotnika
	- Zunanji kot: kot med stranico in podaljškom sosednje stranice
3. **Kolikšna je vsota notranjih kotov trikotnika? Trditev dokažite.**
	Vsota notranjih kotov trikotnika je 180°. Dokaz: Če skozi eno oglišče narišemo vzporednico nasproti ležeči stranici, dobimo z ostalima stranicama enake kote kot v trikotniku. Na premici je vsota kotov 180°.
4. **Kolikšna je vsota zunanjih kotov trikotnika?**
	Vsota zunanjih kotov trikotnika je 360°.
___
## Znamenite točke trikotnika
1. **Opišite konstrukcijo simetrale daljice in simetrale kota.**
	- Simetrala daljice: premica, ki daljico razpolavlja pravokotno
	- Simetrala kota: premica, ki notranji kot razpolavlja
2. **Kako poiščemo težišče trikotnika, središče trikotniku očrtane krožnice, središče trikotniku včrtane krožnice in višinsko točko?**
	1. Težišče: presečišče težiščnic (daljic iz oglišč do razpolovišč nasprotnih stranic)
	2. Središče očrtane krožnice: presečišče simetral stranic
	3. Središče včrtane krožnice: presečišče simetral notranjih kotov
	4. Višinska točka: presečišče višin (daljic iz oglišč pravokotno na nasprotne stranice)
___
## Skladnost likov
1. **Definirajte podobnost likov.**
	 Dva lika sta skladna, če sta enake oblike in velikosti. To pomeni, da imata enake stranice in enake kote ter ju lahko s premikom, vrtenjem ali zrcaljenjem popolnoma prekrijemo.
2. **Povejte štiri izreke o skladnosti trikotnikov.**
	 Štirje izreki o skladnosti trikotnikov so
	- S-K-S (stranica-kot-stranica): Trikotnika sta skladna, če se ujemata v dveh stranicah in kotu med njima
	- K-S-K (kot-stranica-kot): Trikotnika sta skladna, če se ujemata v eni stranici in obeh priležnih kotih
	- S-S-S (stranica-stranica-stranica): Trikotnika sta skladna, če se ujemata v vseh treh stranicah
	- P-S-K (pravokotna trikotnika sta skladna, če se ujemata v preponi in še eni stranici ali v preponi in enem ostrem kotu)
3. **V paralelogramu narišemo obe diagonali. Koliko parov skladnih trikotnikov dobimo?**
	Ko v paralelogramu narišemo obe diagonali, dobimo 2 para skladnih trikotnikov. To se zgodi, ker:
	1. Diagonali se sekata v točki, ki razpolovi obe diagonali
	2. Nasprotne stranice paralelograma so vzporedne in enako dolge
	3. Prvi par skladnih trikotnikov dobimo na nasprotnih koncih ene diagonale
	4. Drugi par skladnih trikotnikov dobimo na nasprotnih koncih druge diagonale
___
## Podobnost likov
1. **Definirajte podobnost likov.**
	Dva lika sta podobna, če imata enako obliko, a sta lahko različnih velikosti. To pomeni, da imata enake kote, stranice pa so v enakem razmerju (sorazmerne).
2. **Povejte tri izreke o podobnosti trikotnikov.**
	 Trije izreki o podobnosti trikotnikov so:
	- K-K (kot-kot): Trikotnika sta podobna, če imata dva kota enaka (tretji kot je potem avtomatsko enak)
	- S-K-S (stranica-kot-stranica): Trikotnika sta podobna, če imata enak kot in sta razmerji stranic ob tem kotu enaki
	- S-S-S (stranica-stranica-stranica): Trikotnika sta podobna, če so razmerja vseh istoležnih stranic enaka
3. **Trikotnika ABC in A'B'C ' sta podobna. Stranica AB prvega trikotnika meri c, stranica A'B' drugega trikotnika pa meri k c. Kolikšna sta obseg in ploščina trikotnika A'B'C ', če je o obseg trikotnika ABC in S ploščina trikotnika ABC ?**
	Ker sta trikotnika ABCABC in A′B′C′A'B'C' podobna, velja, da so vsi njihovi sorazmerni elementi v enakem razmerju k. To pomeni:
	$o′=k⋅o$  
	kjer je o′ obseg trikotnika A′B′C', o pa obseg trikotnika ABC
	Ploščini podobnih trikotnikov sta v razmerju kvadrata faktorja podobnosti $k^2$. Torej velja:
	$S′=k^2⋅S$
	kjer je S′ ploščina trikotnika A′B′C′, S pa ploščina trikotnika ABC
	Tako dobimo:
		$o′=k⋅o$
		$S′=k2⋅S$

___
## Premice in krožnice
1. **V kakšni medsebojni legi sta lahko premica in krožnica, ki ležita v isti ravnini?**
	 Medsebojna lega premice in krožnice:
	- Sekanta: premica seka krožnico v dveh točkah
	- Tangenta: premica se dotika krožnice v natanko eni točki
	- Mimobežnica: premica ne seka krožnice (nima skupnih točk)
2. **Kako imenujemo daljico, ki povezuje dve točki krožnice?**
	Daljica, ki povezuje dve točki krožnice, se imenuje tetiva.
3. **Opišite konstrukcijo tangente na krožnico v dani točki krožnice.**
	Konstrukcija tangente na krožnico v dani točki:
	- Narišemo polmer do dane točke na krožnici
	- V tej točki narišemo pravokotnico na polmer
	- Ta pravokotnica je tangenta na krožnico
___
## Središčni in obodni kot
1. **Definirajte središčni in obodni kot v krogu.**
	Definicije:
	- Središčni kot je kot z vrhom v središču krožnice
	- Obodni kot je kot z vrhom na krožnici in krakoma skozi dve drugi točki krožnice
2. **V kakšni zvezi sta, če ležita nad istim lokom kroga?**
	Zveza med središčnim in obodnim kotom nad istim lokom: Središčni kot je dvakrat večji od obodnega kota nad istim lokom.
3. **Povejte in dokažite Talesov izrek o kotu v polkrogu.**
	Talesov izrek o kotu v polkrogu: Obodni kot nad premerom krožnice je pravi kot (90°). Dokaz:
	- Središčni kot nad premerom je 180°
	- Obodni kot je polovica središčnega kota
	- Torej je obodni kot 90°
4. **V enakostraničnem trikotniku ABC je S središče trikotniku očrtane krožnice. Koliko meri kot  ∠ASB?**
	V enakostraničnem trikotniku ABC, kjer je S središče očrtane krožnice, kot ∠ASB meri 120°. To je zato, ker:
	- V enakostraničnem trikotniku so vsi koti 60°
	- Središče očrtane krožnice razdeli trikotnik na tri enake dele
	- Zato je kot ∠ASB enak 120° (dvakrat večji od kota v trikotniku)
___
## Paralelogram
1. **Definirajte paralelogram.**
	Paralelogram je štirikotnik, ki ima dva para vzporednih stranic.
2. **Navedite lastnosti kotov in stranic paralelograma.**
	Lastnosti kotov in stranic paralelograma:
	- Nasprotni stranici sta vzporedni in enako dolgi
	- Nasprotna kota sta skladna
	- Vsota sosednjih kotov je 180°
	- Vsota vseh notranjih kotov je 360°
3. **Navedite posebne vrste paralelogramov in opišite njihove lastnosti.**
	Posebne vrste paralelogramov:
	- Pravokotnik: paralelogram s štirimi pravimi koti
	- Romb: paralelogram z vsemi stranicami enake dolžine
	- Kvadrat: paralelogram s štirimi pravimi koti in vsemi stranicami enake dolžine
4. **Kaj velja za diagonali paralelograma?**
	Za diagonali paralelograma velja:
	- Sekata se v razmerju 1:1 (razpolovita se)
	- Razdelita paralelogram na dva para skladnih trikotnikov
___
## Trapez
1. **Definirajte trapez.**
	Trapez je štirikotnik, ki ima natanko en par vzporednih stranic (imenujemo ju osnovnici).
2. **Navedite lastnosti kotov trapeza.**
	Lastnosti kotov trapeza:
	- Vsota notranjih kotov je 360°
	- Kota ob istem kraku sta suplementarna (njihova vsota je 180°)
3. **Kaj je srednjica trapeza in katere lastnosti ima?**
	Srednjica trapeza:
	Je daljica, ki povezuje razpolovišči krakov
	Vzporedna je osnovnicama
	Njena dolžina je aritmetična sredina dolžin osnovnic ($\frac {a+c}{2})$, kjer sta $a$ in $c$ dolžini osnovnic).
4. **Kdaj je trapez enakokrak? Kaj velja za kote in diagonali v** enakokrakem trapezu?
	 Enakokrak trapez:
	- Kraka sta enako dolga
	- Kota ob isti osnovnici sta skladna
	- Diagonali sta enako dolgi
5. **Opišite, kako v enakokrakem trapezu z znanimi dolžinami stranic izračunamo višino trapeza.**
	$d = \frac{a-c}{2}$
	To je kateta pravokotnega trikotnika.
	Druga kateta je višina $v$.
	Hipotenuza je krak $b$.
	$v = \sqrt{b^2 - d^2}$
	Rešitev: $v = \sqrt{b^2 - (\frac{a-c}{2})^2}$
___
## Funkcije
1. **Definirajte pojem funkcije (preslikave) iz množice A v množico B.**
	Funkcija (preslikava) iz množice A v množico B je predpis, ki vsakemu elementu iz množice A priredi natanko en element iz množice B.
2. **Definirajte pojme definicijsko območje, zaloga vrednosti in graf funkcije.**
	- Definicijsko območje ($D_f$): množica vseh x, za katere je funkcija definirana
	- Zaloga vrednosti ($Z_f$): množica vseh y, ki so slike elementov iz definicijskega območja
	- Graf funkcije ($G_f$): množica vseh točk (x,y), kjer je y = f(x)
3. **Narišite graf ali povejte predpis funkcije f , ki ima zalogo vrednosti $Z_f = (2,∞)$**
	$f(x)={2}+{e}^{{x}}$
4. **Narišite graf ali povejte predpis funkcije g, ki ima definicijsko območje $D_g = (2,c)$**
	$g(x)={\log{{\left({x}-{2}\right)}}}$
___
## Lastnosti funkcij
1. **Kdaj je funkcija na intervalu naraščajoča in kdaj padajoča?**
	Funkcija je:
	- Naraščajoča na intervalu: če za vsaka x₁,x₂ iz intervala velja: x₁<x₂ ⟹ f(x₁)<f(x₂)
	- Padajoča na intervalu: če za vsaka x₁,x₂ iz intervala velja: x₁<x₂ ⟹ f(x₁)>f(x₂)
2. **Narišite graf ali povejte predpis funkcije, ki ni niti naraščajoča niti padajoča.**
	$f(x)={\sin{{\left({x}\right)}}}$
3. **Kdaj je funkcija $f$ omejena?**
	Funkcija je omejena, če obstajata števili m in M, da za vsak x iz definicijskega območja velja: $m ≤ f(x) ≤ M$.
	ALI
	Ko ima zaloga vrednosti dane funkcije minimalno in maksimalno vrednost. *Npr.: Zf = (0,∞) <- spodnja meja je 0*
4. **Narišite graf ali povejte predpis padajoče funkcije, ki je navzgor omejena, navzdol pa neomejena.**
	$f(e)=-{e}^{{x}}$
___
## Lastnosti funkcij
1. **Kdaj je funkcija $f$ liha in kdaj soda?**
	Funkcija f je:
	- Liha: če za vsak x iz definicijskega območja velja f(-x) = -f(x)
	- Soda: če za vsak x iz definicijskega območja velja f(-x) = f(x)
2. **Kako iz grafa funkcije $f$ vidimo, ali je funkcija $f$ soda oziroma liha?**
	Iz grafa funkcije vidimo:
	- Soda funkcija: graf je simetričen glede na y-os
	- Liha funkcija: graf je simetričen glede na koordinatno izhodišče
3. **Naj bo funkcija $f$ bijektivna. Kako poiščemo predpis inverzne funkcije $f^{-1}$?**
	Za bijektivno funkcijo f poiščemo inverzno funkcijo f⁻¹ tako, da:
	1. Zamenjamo x in y v enačbi y = f(x)
	2. Izrazimo y iz dobljene enačbe
	3. Dobljeni y je predpis za f⁻¹(x)
4. **Kaj velja za grafa funkcij $f$ in $f^{-1}$?**
	Za grafa funkcij f in f⁻¹ velja:
	- Sta si simetrična glede na premico y = x
	- Če točka (a,b) leži na grafu f, potem točka (b,a) leži na grafu f⁻¹
___
## Potenčna funkcija
1. **Definirajte potenčno funkcijo z naravnim eksponentom.**
	Potenčna funkcija z naravnim eksponentom n je funkcija oblike f(x) = xⁿ.
2. **Narišite grafa potenčnih funkcij, ki imata eksponenta 2 in 3.**
	![[Pasted image 20250323131829.png]]
3. **Navedite vsaj dve lastnosti potenčnih funkcij.**
	- So zvezne funkcije
	- Gredo skozi točko (0,0) in (1,1)
4. **Navedite osnovne razlike v lastnostih med potenčnimi funkcijami s sodim in potenčnimi funkcijami z lihim naravnim eksponentom.**
	Razlike med sodimi in lihimi eksponenti:
	- Sode: graf je simetričen glede na y-os (soda funkcija)
	- Lihe: graf je simetričen glede na izhodišče (liha funkcija)
___
## Kvadratna funkcija
1. **Definirajte kvadratno funkcijo.**
	Kvadratna funkcija je funkcija oblike f(x) = ax² + bx + c, kjer je a ≠ 0.
2. **Naštejte vsaj štiri lastnosti kvadratne funkcije in jih razložite.**
	1. Graf je parabola
	2. Os simetrije je vzporedna y-osi
	3. Ima največ dve ničli
	4. Je zvezna funkcija
3. **Povejte primer navzgor omejene kvadratne funkcije, katere graf seka ordinatno os v točki $N(0, 3)$.**
	Primer navzgor omejene kvadratne funkcije, ki seka ordinatno os v (0,3): f(x) = -x² + 3
___
## Teme grafa kvadratne funkcije
1. **Kaj je teme grafa kvadratne funkcije? Kako ga izračunamo?**
	Teme je najvišja (a < 0) ali najnižja (a > 0) točka grafa. Izračunamo ga z obrazcem: $p=\frac{-b} {2a}$, 
	$q=\frac {-(b^2-4ac)} {4a}$
2. **Povejte temensko obliko predpisa kvadratne funkcije. Kako je njen graf odvisen od vodilnega koeficienta ter koordinat temena?**
	Temenska oblika: f(x) = a(x - p)² + q, kjer je T(p,q) teme
	- a > 0: parabola navzgor
	- a < 0: parabola navzdol
	- (p,q) so koordinate temena
3. **Povejte primer navzgor omejene kvadratne funkcije, katere graf ima teme v prvem kvadrantu.**
	Primer navzgor omejene funkcije s temenom v prvem kvadrantu: $f(x) = -(x - 2)^2 + 4$
___
## Ničle kvadratne funkcije
1. **Definirajte ničlo funkcije.**
	 Ničla funkcije je vrednost x, pri kateri je f(x) = 0
2. **Povejte ničelno obliko predpisa kvadratne funkcije.**
	 Ničelna oblika: $f(x) = a(x - x₁)(x - x₂)$, kjer sta $x₁$ in $x₂$ ničli
3. **Kaj je diskriminanta kvadratne funkcije?**
	- Diskriminanta je $D = b² - 4ac$
4. **Razložite pomen diskriminante kvadratne funkcije pri iskanju njenih ničel.**
	Pomen diskriminante pri iskanju ničel:
	- D > 0: dve različni realni ničli
	- D = 0: ena dvojna realna ničla
	- D < 0: dve konjugirano kompleksni ničli
___
## Kvadratna enačba
1. **Kaj je kvadratna enačba?**
	 Kvadratna enačba je enačba oblike ax² + bx + c = 0, kjer je a ≠ 0.
2. **Kako izračunamo rešitve kvadratne enačbe?**
	Rešitve izračunamo po formuli: $x_{1,2} = \frac{-b ± \sqrt{b² - 4ac}} {2a}$
3. **Kako je z rešljivostjo kvadratne enačbe v množici realnih števil in kako v množici kompleksnih števil?**
	- V ℝ: rešljiva, če je D ≥ 0
	- V ℂ: vedno rešljiva (ima natanko dve rešitvi)
4. **Povejte in rešite primer kvadratne enačbe, ki ima dve konjugirano kompleksni rešitvi.**
	$x^2 + 1 = 0$
	$x_1 = i$
	$x_2 = -i$
___
## Kvadratna neenačba
1. **Kaj je kvadratna neenačba?**
	 Kvadratna neenačba je neenačba oblike ax² + bx + c > 0 (ali <, ≤, ≥).
2. **Kako rešujemo kvadratno neenačbo?**
	1. Narišemo graf kvadratne funkcije
	2. Poiščemo ničle
	3. Določimo predznak na intervalih
	4. Zapišemo rešitev glede na znak neenačbe
3. **Kaj je množica rešitev poljubne kvadratne neenačbe? Povejte vse možnosti.**
	Možne množice rešitev:
	- Prazen interval: $∅$
	- En interval: $(a,∞)$ ali $(-∞,a)$
	- Unija dveh intervalov: $(-∞,a)∪(b,∞)$
	- Zaprt interval: $[a,b]$
	- Polodprt interval: $[a,b)$ ali $(a,b]$
4. **Povejte primer kvadratne neenačbe, katere množica rešitev je interval $[1, 2]$.**
	$[1,2]: (x - 1)(x - 2) ≤ 0$
	Če je ${\left({1}\le{x}\le{2},{\left({x}-{1}\right)}\cdot{\left({x}-{2}\right)}\right)}$
___
