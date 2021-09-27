# Podatkovne baze

> **Podatki** so dejstva, ki se jim lahko pripiše pomen. Pri opravljanju kakšnega koli dela skoraj vedno potrebujemo in/ali ustvarjamo podatke.
> 
> Trajni podatek je podatek, katerega življenjski čas je daljši od življenskega časa enega procesa.

V računalništvu poznamo dva načina trajnega elektornskega hranjenja podatkov:

- zapisovanje v binarne ali besedilne **datoteke** (_ang. flat file_)
- zapisovanje v **podatkovne baze**, preko sistema za upravljanje s podatkovno bazo

**Sistem za upravljanje s podatkovno bazo** - **SPUB** (_ang. Database Management System - **DBMS**_) je računalniški program, ki povezuje uporabnike, aplikacije in samo bazo podatkov z namenom zajemanja in analiziranja podatkov. _Več o SPUB v sledečih poglavjih._

## Opredelitev PB

**Podatkovna baza** - **PB** (_Database - **DB**_) je izvedljiv in poenostavljen model realnosti v računalniku, ki služi kot osnova za sprejemanje odločitev in izvajanje akcij v realnosti. Je temelj za delovanje katerekoli sodobne organizacije.

Da pa lahko zbirko podatkov imenujemo podatkovna baza, mora po definiciji **ANSI** (_ang. American National Standards Institute_) izpolnjevati naslednje zahteve:

- podatki v bazi so **povezani** in **urejeni** (strukturirani)
- podatke v bazi lahko istočasno uporablja **več uporabnikov**
- shranjena je na računalniku
- podatki se v bazi **ne ponavljajo** (redundanca ni dovoljena oz. je nadzorovana)

Podatke v bazi uredimo v skladu s podatkovnim modelom, ki opisuje strukturo baze. Poznamo več vrst podatkovnih modelov a najpogosteje se uporablja **entitetno-relacijski**.

## Vloga PB v organizaciji

Podatkovna baza je srce informacijskega sistema, v katerem se nahajajo podatki za izvajanje poslovnih procesov ter za pridobivanje in pretvorbo podatkov v informacije.  
Dan danes so podatki najpomembnejše sredstvo vsake organizacije, saj so v primeru izgube praktično nenadomestljivi.

Nekoč je vsak člen organizacije hranil svoje podatke v knjigah, mapah in fasciklih, sedaj pa so te metode nadomestile podatkovne baze, ki hranijo podatke v centralni lokaciji in preko SPUB omogočajo omejitev dostopa do relevantnih podatkov. Najvčja pridobitev te spremembe je hitejši in vedno točen dostop do podatkov.

Pojavil pa se je tudi trend rudarjenja podatkov in podatkovnega skladiščenja, kjer organizacija zbira in hrani, na prvi pogled, irelevantne podatke za namen analize ipd.

## Arhitektura PB

Osnovna arhitekrura je **trinivojska** oz. **ANSI-SPARC** arhitektura, ki zagotavlja podatkovno neodvisnost.

Posamezni nivoji trinivojske arhitekture so:

1. **zunanji** nivo (_ang. external level_), ki opisuje uporabo podatkov
2. **konceptualni** nivo (_ang. conceptual level_), ki opisuje pomen podatkov
3. **notranji** nivo (_ang. internal level_), ki opisuje način shranjevanja podatkov

Opis posameznega nivoja imenujemo **shema**. Preslikave med shemami pa izvaja SPUB.

![ANSI-SPARC Arhitektura](https://www.researchgate.net/profile/Arjen-De-Vries/publication/220692027/figure/download/fig3/AS:654765310611459@1533119623297/The-three-schema-or-ANSI-SPARC-architecture.png)

**ANSI-SPARC arhitektura** sicer nikoli ni postala formalni standard, vendar večina sistemov za upravljanje PB približno sledi vodilom, ki jih je postavila.

### Zunanji nivo

Na zunanjem nivoju se konceptualna baza prikaže kot uporabnikov model okolja, ki obsega le tisti del celotnega modela, ki je zanj zanimiv oz. mu je dostopen. Zunanja shema omogoča posamezni vrsti uporabnika prilagojen pogled na konceptualno bazo podatkov.

Npr. uporabniški vmesnik za eAsistent daje ravnatelju, razredniku in učitelju različne obsege dostopa, spet drugačen vmesnik je na voljo dijaku, ki večinoma lahko samo pregleduje vnesene podatke vezane nanj.

Značilnosti zunanjega nivoja so:

- različni pogledi za posameznega uporabnika
- pregledi so prilagojeni potrebam uporabnika
- prispeva k zagotavljanju varnosti zaupnih podatkov
- pogosto prikazuje izračunane podatke

### Konceptualni nivo

je **globalen pogled** na podatkovno bazo, predstavljen z vsemi entitetami, ralacijami in pripadajočimi atributi ter omejitvami. Preko tega nivoja vidimo vsebino in strukturo celotne baze, saj so opisani vsi podatki v PB ter njihove medsebojne povezave.

Vsaka baza ima **le eno konceptualno shemo**. Ta pa ne opredeljuje, kako so podatki fizično hranjeni - tj. je neodvisna od strojne in programske opreme.

Iz tega nivoja izhajajo podatki na zunanjem nivoju.

### Notranji nivo

Notranji nivo opisuje **fizično predstavitev PB** s pomočjo SPUB. Pove nam torej kakšne strukture podatkov se uporabljajo in kje ter kako lahko do njih dostopamo.

Ta nivo zajema:

- podatkovne strukture
- datotečne organizacije
- opis zapisov in podatke
- indekse
- dodelitev pomnilnika
- tehnike šifriranja in stiskanja podatkov

Notranja shema je v celoti odvisna od SPUB.

## Podatkovna neodvisnost

Cilj trinivojske arhitekture je zagotavljanje podatkovne neodvisnosti oz. odpornosti višjega nivoja na spremembe nižjega.

**Obstajata 2 vrsti podatkovne neodvisnosti:**

- fizična podatkovna neodvisnost - med notranjim in konceptualnim nivojem
- logična podatkovna neodvisnost - med konceptualnim in zunanjim nivojem

## Prednosti in slabosti PB

_Za primerjavo prednosti in slabosti si oglejte učbenik na straneh 44 in 45._
