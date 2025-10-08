1. **Kaj je standard?**  
    Standard je formalno določen protokol oz. dogovor, ki določa pravila za komunikacijo med napravami v omrežju. Namen standarda je zagotoviti kompatibilnost med različnimi napravami in sistemi.
    
2. **Naštej in na kratko predstavi aktivno omrežno opremo.**
    
    - **Stikalo (Switch):** povezuje naprave v lokalnem omrežju in usmerja podatke na podlagi MAC naslovov.
        
    - **Usmerjevalnik (Router):** povezuje različna omrežja, usmerja promet glede na IP naslove.
        
    - **Dostopna točka (Access Point):** omogoča brezžično povezavo naprav v omrežje.
        
    - **Modem:** pretvarja signale med digitalno in analogno obliko za dostop do interneta.
        
3. **Kaj je DHCP?**  
    Protokol za samodejno dodeljevanje IP-naslovov napravam v omrežju.
    
4. **Katere informacije DHCP strežnik dodeli?**  
    IP naslov, masko omrežja, gateway, DNS strežnik.
    
5. **Kje se uporablja DHCP?**  
    V lokalnih omrežjih – doma, v pisarnah, na šolah – kjer se napravam dodeljujejo IP-naslovi dinamično.
    
6. **Kako deluje DHCP?**  
    DHCP strežnik napravi dodeli IP-naslov, ko ta zahteva dostop do omrežja (postopek: Discover → Offer → Request → Acknowledge).
    
7. **Katere so prednosti uporabe DHCP?**  
    Hitro in enostavno dodeljevanje IP-naslovov, zmanjšuje napake, omogoča centralizirano upravljanje.
    
8. **Naslov omrežja je npr.: 192.168.0.0/28 Zapiši masko omrežja v desetiški obliki. Naslov namenjen celotnemu omrežju (broadcast)**
    - Maska: 255.255.255.240
    
    - Broadcast: 192.168.0.15
        
9. **Naslov omrežja je npr.: 192.168.0.128/28 Zapiši in razloži koliko naprav (računalnikov) lahko priključimo v to omrežje?**
    - Število naslovov: 16 ( od 32 bitov je maska nastavljena na 28, kar nam da 4 bite za naslove naprav, 4 biti nam omogočijo 16 različnih ip-jev za naprave)
        
    - Možnih naprav: 14 (ena za omrežje, ena za broadcast)
        
10. **S katerim ukazom preverimo omrežne nastavitve na osebnem računalniku z Windows OS?**  
    `ipconfig`
    
11. **Kakšna je razlika med fizičnim naslovom in logičnim naslovom na omrežni kartici?**
    
    - Fizični (MAC): edinstven naslov, dodeljen strojno
        
    - Logični (IP): naslov, ki se dodeli programsko, lahko se spreminja
        
12. **Koliko MAC naslovov ima usmerjevalnik, ki ima 4 ethernet priključke?**  
    4 MAC naslove – enega za vsak priključek.
    
13. **DHCP strežnik bo imel območje za dodeljevanje IP-jev 192.168.0.2 - 192.168.0.200. Katere IP naslove sme imeti DHCP strežnik? Izberi in zapiši omrežne nastavitve eth0 za DHCP strežnik.**  
    DHCP strežnik mora imeti naslov zunaj tega območja, npr. **192.168.0.1**  
    Nastavitve:
    ```
    IP: 192.168.0.1
    Maska: 255.255.255.0
    Gateway: 192.168.0.1
    DNS: Ni potreben za samo lokalno omrežje, drugeče pa javen (8.8.8.8 ali 1.1.1.1 sta pogosta)
    ```
    
14. **Naštej nekaj usmerjevalnih algoritmov.**

| Algoritem | Tip | Opis |
| --- | --- | --- |
| RIP | Vektor razdalj | Uporablja štetje skokov, enostaven, počasnejši, max 15 skokov. |
| IGRP	    | Vektor razdalj	  | Bolj napreden kot RIP, podpira več metrik (npr. pasovna širina).          |
| EIGRP	    | Hibridni protokol | Cisco protokol, kombinira hitrost in zanesljivost, učinkovito usmerjanje. |
| OSPF	    | Glede na stanje	  | Hitro prilagajanje, uporablja Dijkstrov algoritem, skalabilen             |
| IS-IS	    | Glede na stanje	  | Podoben OSPF, pogosto uporabljen v velikih omrežjih in pri ponudnikih.    |
        
16. **Naprave za povezovanje v omrežje so:**  
    Switch, router, modem, hub, dostopna točka, omrežna kartica (NIC).
    
17. **Kaj je fizična topologija omrežja in katere poznamo?**  
    Fizična topologija opisuje fizično razporeditev naprav in kablov. Poznamo: zvezdo, vodilo, obroč, mrežo, drevo.
    
18. **Navedi prednosti in slabosti posameznih topologij.**
    - **Zvezda:** +enostavna za vzdrževanje, -centralna točka
    - **Vodilo:** +malo kablov, -moteče za več naprav
    - **Obroč:** +enakomerna razdalja, -pokvarjena naprava prekine celoten obroč
    - **Mreža:** +zelo zanesljiva, -kompleksna in draga
    - **Drevo:** +hierarhija, -težje razširjanje
        
19. **Kakšne osnovne logične topologije omrežij poznamo?**  
    Vodilo, zvezda, obroč.
    
20. **Katere fizične komponente potrebujemo za gradnjo omrežij s topologijo vodila?**  
    kable, omrežne kartice in naprave ki jih bomo povezali.
    
21. **Katere fizične komponente potrebujemo za gradnjo omrežij s topologijo zvezde?**  
    Switch ali hub, kabli, omrežne kartice.
    
22. **Katere pristopne metode urejajo prenos podatkov v lokalnem omrežju?**
    - **CSMA/CD** (Ethernet)
    - **CSMA/CA** (Wi-Fi)
        
23. **Na kratko opiši princip delovanja pristopne metode CSMA/CD.**  
    Naprava posluša kanal, če je prost, pošlje podatke. Če pride do trka, počaka naključno količino časa in ponovno pošlje.
    
24. **Zapišite plasti TCP/IP in ISO/OSI modela ju primerjajte.**
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
25. **Kaj je enkapsulacija?**  
    Proces, ki paketu podatkov doda svojo glavno in rep(header) preden jih pošlje naprej.
    
26. **Kaj je definirano na fizični plasti?**  
    Vrsta kablov, konektorjev, signalizacija, električne napetosti – fizični prenos bitov.
    
27. **Zapišite glavne lastnosti prenosnih medijev, ki jih uporabljamo v računalniških omrežjih.**
    
    - **Twisted pair (UTP):** cenovno ugoden, do 10 Gbps, občutljiv na motnje
        
    - **Koaksialni kabel:** odporen na motnje, do 2 Gbps
        
    - **Optični kabel:** zelo hiter in odporen, do več 10 Tbps
        

---

### **Izberi pravilen odgovor**

**S katero storitvijo lahko povežemo protokole SMTP, POP3 in IMAP?**  
B. Z elektronsko pošto

**Zapišite ime sloja oz. plasti modela TCP/IP, na katerem se uporablja fizični naslov mrežne kartice za razlikovanje med napravami istega omrežja.**  
Plast omrežnega vmesnika (angl. Network Interface Layer)

**Iz koliko bitov je sestavljen fizični naslov mrežne kartice?**  
48 bitov (6 bajtov)

**Pri omrežnih nastavitvah uporabimo prehod, ko želimo:**  
A. določiti vhod naprave, prek katere bomo dostopali v druga omrežja.

## Osnovni ukazi v CMD

**1. V CMD oknu naredite dve novi mapi in v eno mapo shranite txt dokument s svojim imenom. Nato pa naredite kopijo tega dokumenta in ga skopirajte v drugo mapo.**

```
mkdir mapa1 
mkdir mapa2 
echo MojeIme > mapa1\ime.txt 
copy mapa1\ime.txt mapa2\
```

---

## Linux - osnovni ukazi (VM)

**1. Zapiši, kaj naredijo naslednji ukazi:**

- `ls` – izpiše seznam datotek in map v trenutni mapi
- `rm` – izbriše datoteko (ali mapo z dodatkom `-r`)
- `ps` – izpiše seznam aktivnih procesov
- `cp` – kopira datoteke ali mape
- `wget` – prenese datoteko z interneta prek URL-ja

---

**2. Zapiši zaporedje ukazov za naslednjo aktivnost:  
iz mape ~/temp/prenos/slika1.jpg, slika2.jpg, slika3.jpg premakni v mapo /www/slike/**

```
mv ~/temp/prenos/slika1.jpg /www/slike/ 
mv ~/temp/prenos/slika2.jpg /www/slike/ 
mv ~/temp/prenos/slika3.jpg /www/slike/
```

---

**3. Zapiši osnovne Linux shell ukaze in en primer:**

- **Ukaz za spreminjanje imenika:**  
    `cd /pot/do/mape`  
    primer: `cd /home/uporabnik`
    
- **Ukaz za listanje datotek:**  
    `ls` - izpiše vse datoteke in mape ki se nahajajo v trenutni mapi
    primer: `ls -l`
    
- **Dovoljenja za pristop datoteki:**  
    `chmod` - spremeni kateri uporabnik ima kaka dovoljenja do datoteke - npr. en uporabnik jo lahko samo bere medtem ko drugi tudi ureja
    primer: `chmod +x script.sh`
    
- **Ukaz za tip datoteke:**  
    `file` - izpiše kakšnega tipa so podatki shranjeni v datoteki
    primer: `file dokument.txt` vrne `UTF-8 text`
    
- **Ukaz za listanje vsebine datoteke:**  
    `cat` - izpiše vsebino datoteke
    primer: `cat dokument.txt`
    
- **Absolutna in relativna pot (primer):**
    `pwd` - izpiše pot do trenutne mape
    - Absolutna: `/home/uporabnik/datoteka.txt`
    - Relativna: `~/dokument.txt` 
        

---

**4. Zapiši kaj naredijo naslednji ukazi in en primer:**

- `$ man ime_ukaza` – prikaže priročnik za ukaz  
    npr. `man ls`
    
- `$ date` – izpiše trenutni čas in datum  
    
- `$ cal` – prikaže koledar  
    
- `$ pwd` – izpiše trenutno pot (mapo)  
    npr. `/home/uporabnik`
    
- `$ cd ..` – premakne za eno mapo nazaj v imeniku(direktoriju)
    
- `$ ls -l` – podrobno izpiše datoteke v trenutni mapi in zraven še detajle npr. dovoljenja
    

---

**5. V operacijskem sistemu Linux bi želeli izpisati vsebino imenika vaje, ki se nahaja v korenskem imeniku.  
Kateri ukaz moramo uporabiti?**

`ls C:\vaje`

---

**6. Izvedba ukaza `ls -l` izpiše:**  
`-rw-r--r-- 1 user user 394 2020-08-30 09:53 matura.rtf`  
**Zapišite ukaz, s katerim trenutni uporabnik, ki je skrbnik, spremeni lastništvo datoteke `matura.rtf` na uporabnika `nekdo`.**

`sudo chown nekdo matura.rtf`

---

## **Procesi**

**1. Kaj je PCB?**  
PCB (Process Control Block) je podatkovna struktura, ki vsebuje informacije o procesu: PID, stanje, prioriteta, registri, pomnilnik, odprte datoteke ipd.

**2. Podatki, ki jih lahko vidiš o delujočih procesih v Windowsih so:**

- PID
- Uporaba CPU in pomnilnika
- Ime procesa
- Uporabnik
- Stanje (aktivno, ustavljeno)
- Pot do datoteke procesa
    

**3. Katere procese lahko izbrišeš brez posledic?**  
Nekritične, uporabniške procese (npr. Chrome, Notepad). Kritičnih sistemskih procesov ne smeš preklicati.

**4. Kaj se lahko zgodi, če izbrišeš kritičen proces OS-a?**

Windows ti tega ne dovoli, če pa bi ti uspelo:
- Sesutje sistema
- Zmrzovanje
- Takojšen ponovni zagon ali BSOD (modri zaslon)
    

**5. Poleg osnovnih informacij, kot so PID, uporaba CPU in pomnilnika, lahko ugotovim tudi:**

- Pot do izvršljive datoteke
- Število niti
- Čas zagona procesa
- Pripadajoči uporabnik
- Starševski proces (PPID)
    

**6. Poiščite podatke o datotečnih sistemih, ki jih uporablja ali podpira OS Linux.**

- ext4  
- Btrfs  
- XFS  
- ZFS
    

**7. Narišite ali poiščite sliko strukture datotečnega sistema, ki ga uporabljate (Ubuntu?).**  
Mape v korenskem direktoriju(imeniku): `/home`, `/etc`, `/bin`, `/var`, `/tmp`, `/usr`, `/dev`, `/mnt`, `/boot`...

**8. Na kratko predstavite pomen posameznih direktorijev:**

- `/` – korenska mapa
- `/home` – domači direktoriji uporabnikov
- `/etc` – konfiguracijske datoteke
- `/bin` – osnovni sistemski programi
- `/usr` – dodatni programi in knjižnice
- `/tmp` – začasne datoteke
- `/var` – logi, e-pošta, baza podatkov
- `/dev` – naprave (disk, USB, itd.)
- `/boot` - bootloader
    

**9. Pravice dostopov; na tem primeru zapišite kakšne pravice dostopov so dodeljene:  
`-rwxr-x--- 1 sers sers 12 Jun 25 09:25 datoteka.txt`**

- **Uporabnik (sers) lahko:** bere, piše, izvaja
    
- **Skupina (sers) lahko:** bere, izvaja
    
- **Drugi:** nimajo dostopa
