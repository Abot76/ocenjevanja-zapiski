1. Značilnosti, lastnosti in namen uporabe opreme:
Usmerjevalnik (Router):
Deluje na omrežni plasti (Layer 3), uporablja usmerjevalne tabele in algoritme za prenos podatkov med različnimi omrežji (npr. povezava z internetom).

Stikalo (Switch):
Deluje na povezavni plasti (Layer 2), uporablja MAC tabele, omogoča učinkovito komunikacijo med napravami v istem omrežju.

Povezovališče (Hub):
Deluje na fizični plasti (Layer 1), pošilja podatke vsem napravam, ne razlikuje naslovov – danes se redko uporablja zaradi slabše učinkovitosti.

2. Načini usmerjanja:
Statično usmerjanje: Administrator ročno nastavi poti.

Dinamično usmerjanje: Poti se samodejno prilagajajo glede na razmere v omrežju.

Centralizirano usmerjanje: Odločitve sprejema en osrednji usmerjevalnik.

Porazdeljeno usmerjanje: Vsak usmerjevalnik sprejema lastne odločitve.

Usmerjanje po eni poti: Vedno uporabi eno določeno pot.

Usmerjanje po več poteh: Lahko izbere med več potmi (npr. za razbremenitev).

3. Usmerjevalni algoritmi in primerjava:
| Algoritem	| Tip               | Opis                                                                      |
| --------- | ----------------- | ------------------------------------------------------------------------- |
| RIP       | Vektor razdalj  	| Uporablja štetje skokov, enostaven, počasnejši, max 15 skokov.            |
| IGRP	    | Vektor razdalj	  | Bolj napreden kot RIP, podpira več metrik (npr. pasovna širina).          |
| EIGRP	    | Hibridni protokol | Cisco protokol, kombinira hitrost in zanesljivost, učinkovito usmerjanje. |
| OSPF	    | Glede na stanje	  | Hitro prilagajanje, uporablja Dijkstrov algoritem, skalabilen             |
| IS-IS	    | Glede na stanje	  | Podoben OSPF, pogosto uporabljen v velikih omrežjih in pri ponudnikih.    |

4. Kaj pokažejo ukazi show v privilegiranem načinu:
Ukazi pokažejo trenutne nastavitve usmerjevalnika, vmesnike, shranjeno konfiguracijo, različico, pomnilnik, stanje ARP tabele ipd.

5. Kaj se spremeni po nastavitvi IP naslovov:
Po nastavitvi IP naslovov in ukazu no shutdown se vmesniki aktivirajo, IP naslovi se pojavijo v izpisu show running-config, usmerjevalnik lahko začne komunicirati z drugimi napravami.


