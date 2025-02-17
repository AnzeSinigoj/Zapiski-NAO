# Netwok ukazi
    
#### Sintaksa:
    ukaz [argumenti]

#### Ukazi:
- **ping:** previrjanje dosegljivosti
- **netstat:** prikaže aktivne povezave 
- **ipconfig (ip a):** nastavitve in konfiguracija NIC
- **hostname:** prikaže mrežno ime PC-ja
- **arp:** prikaže ARP tabelo/informacije
- **nslookup:** prikaže podatke v zvezi s DNS
- **traceroute (tracert):** prikaže sled prometa
- **getmac:** prikaže MAC naslove NIC-ov
- **route:** omogoča manipulacijo in prikaz usmerjevalne tabele

<br>

# ISO/OSI in TCP/IP

#### ISO/OSI
- **Aplication** : data
- **Presentation** : data
- **Session** : data
- **Transportation** : segment
- **Network** : packet
- **Data link** : frame
- **Pysical** : bit

#### TCP/IP
- **Aplication** : data
- **Transportation** : segment
- **Network** : packet
- **Network acess layer** : bit

## Fizična plast

### Naloga fizične plasti
- moduliranje bitov v signale
- prenos signala po prenosnem mediju
- določitev standardnih vmesnikov

### Osnovni pojmi
- Prenosni mediji
- Signal

### Smeri prenosa:
- **simplex** : enosmerno
- **half duplex** : izmenično dvosmerno
- **full duplex** : dvosmerno

### Tipi signalov
- **Analogni** : n stanji (odvisno na natančnost HW)
- **Digitalni** : 2 stanja

### Elektromagnetni signali
- Pasovna širina
- Spekter frekvenc

### A-D pretvorba
Pretvorba analognih signalov v digitalne signale

**Postopek:**
- vzorčenje signala
- dodelovanja binarne kode vzorčenemu signalu

### Neželjeni pojavi pri prenosu
- **Slabenje** : moč signala upada [dB]
- **Popačenje** : drugačna oblika signala
- **Šum** : motje na vodilu se mešajo s signalom

### Tipi network kablov
- **Bakreni:**
    - **UTP** : unshielded twisted pair
    - **STP** : shielded twisted pair
    - **FTP** : foiled twister pair
- **Koaksialni kabelj** : star/ne več v uporabi
- **Optični kabelj** : najnovejša tehnologija

### Tipi brezžičnih povezav
- Radijske 
- Mikrovalovne 
- Infrardeče
- Sateljitske

### Kodiranje
Spreminjanje signalov v pravo obliko.

**D -> A** = Modulacija

**A -> D** = Demodulacija

#### Modulacija:
- **AM** - **A**mplitude **M**odulation
- **FM** - **F**requency **M**odulation
- **PM** - **P**hase **M**odulation
- **QAM** - **Q**uadrature **A**mplitude **M**odulation



**AM in FM:**

<img src="slike/am-fm.gif" alt="AM-FM" width="256" height="200">

**PM:**

<img src="slike/pm.png" alt="PM" width="256" height="200">

**QAM:**

<img src="slike/qam.gif" alt="QAM" width="256" height="200">

(Ne niti provat razumet kako to dela)

#### Digitalna kodiranja:
- **NRZ-L** - Non Return to Zero-Level
- **NRZI** - Non Return to Zero Inverted
- **Manchester**
- **Diferencialni Manchester**
- **in druga..**

#### Non Return Zero-Level (NRZ-L)
- Enka se kodira s pozitivnim nivojem
- Ničla se kodira s negativnim nivojem
- Slabost je sinhroniacija


#### Non Return Zero Inverted (NRZI)
- Ničla ne spremeni signala
- Enka obrne signal (invertira)

<img src="slike/NRZ.png" alt="NRZ" height="256">

<hr>

#### Manchester
- Ničla obrne signal na negativno stanje (predhodno)
- Enka obrne signal na pozitivno stanje
- Uporablja se na LAN omrežjih
- IEEE 802.5

#### Diferenčni Manchester 
- Ničla prehoodi tudi na začetku intervala
- Enka ne prehodi na začetku intervala

Za oba Manchester velja da, se stanje spremeni na polovici trajanja signala.

<img src="slike/manchester.png" alt="Manchester" height="256">

**V Manchester si lahko predstavljamo stanja 1 in 0 tako:**

<img src="slike/man-ez.png" alt="Manchester" height="256">

<hr>

## Povezovalna plast

### Naloge povezovalne plasti
- okvirjanje datagramov
- zaznavanje in odpravljanje napak
- dostop do medija
- zagotavljanje zanesljive dostave
- kontrola pretoka

### Okvirjanje datagramov
Dodajanje repa in glave paketu iz višje plasti

Izgled okvirja:
**[glava]****[podatki]****[rep]**

### Zaznavanje in odpravljanje napak
#### Tehnike:
- **Parity bit**
    - doda se 1 ali 0 tako da je skupno št. enic paketa sodo oz. liho 
    - nevemo kje je prišlo do napake
    - če pride do 2 bit-flipa napake ne zaznamo
    <img src="slike/parity-bit-normal.png" alt="parity bit">
- **2D parity bit**
    - enako samo na več paketih skupaj
    - lahko zaznamo na katerem paketu je prišlo do napake
    <img src="slike/parity-bit-2d.png" alt="2D parity bit">

- **Hamming code**
    - Zazna in popravi napake na posameznih bitih tako, da podatkom doda dodatne paritetne bite. Uporablja specifičen vzorec paritetnih pregledov, ki so postavljeni na mesta, ki so potence števila 2 (1, 2, 4, 8 itd.), da omogoči zaznavanje in popravljanje napak. Če med prenosom pride do napake, koda izračuna sindrom, ki pomaga določiti točno napako in jo popraviti.
    <img src="slike/hamming.jpg" alt="haming">

- **tmp**
<hr>

>#### Random pojmi:
>- TTL = time to live
>- Metric = v routing table pove koliko je vir zanesljiv (majnše kot je bolje je)
>- Modem = Modulator/Demodulator
>- Carrier signal = osnovni signal kateri nosi podatke
>- EDC (Error Detection Code) dodatni poslani biti namenjeni preverjanju pravilnosti
