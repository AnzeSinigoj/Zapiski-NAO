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

#### Digitalna kodiranja:
- **NRZ-L** - Non Return to Zero-Level
- **NRZI** - Non Return to Zero Inverted
- **Manchester**
- **Diferencialni Manchester**
- **in druga..**

<hr>

>#### Random pojmi:
>- TTL = time to live
>- Metric = v routing table pove koliko je vir zanesljiv (majnše kot je bolje je)
>- Modem = Modulator/Demodulator
>- Carrier signal = osnovni signal kateri nosi podatke
