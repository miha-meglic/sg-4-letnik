# Ponovitev OOP

Objektno orientirano programiranje (_ang. object-oriented programming_) oz. OOP je način programiranja, ki temelji na konceptu **objektov**, ki lahko vsebujejo **podatke** in **kodo**.  
Podatke shranjujejo v t.i. atributih (_ang. attribute_), kodo pa v obliki metod (_ang. method_).

## Objekti in razredi

Obstaja veliko različnih OOP programskih jezikov, a najbolj razširjeni temeljijo na razredih (_ang. class-based_).

### Objekt

**Objekt** (_ang. object_) je element, ki ima dane lastnosti (atribute) in funkcije (metode). Tako rekoč ima vsak objekt svoji **identiteto**, **stanje** in **obnašanje**.

Pogosto objekti predstavljajo fizičen svet (npr. avto, učenec, ...) ali nek pojem (npr. projekt, proces, ...).

### Razred

**Razred** (_ang. class_) je vzorec/kalup iz katerega ustvarimo objekte. Razredi nam omogočajo nastavljanje začetnih vrednosti objekta ter definiranje metod.

Objekt je torej instanca nekega razreda.

## Enkapsulacija

**Enkapsulacija** je proces povezovanja atributov in metod znotraj razreda. Tako so lahko notranje podrobnosti razreda skrite zunanjemu svetu.

### Skrivanje podatkov

Razredi so običajno načrtovani tako, da nimamo direktnega dostopa do njihovih atributov, ampak jih dostopamo preko metod. Tako izolacijo uporabljamo, da preprečimo drugim razredom, in posledično končnemu uporabniku, vnašanje napačnih podatkov in spreminjanje podatkov (_npr. spremenljivko, ki beleži interno stanje_), ko tega ne pričakujemo.

## Dedovanje

Dedovanje je mehanizem ustvarjanja novih razredov, ki ohranjajo podobno implementacijo svojih staršev. Tako lahko zmanjšamo količino ponovljene kode med več razredi.

**Starševski razred** (_ang. parent/super/base class_) je tisti, ki ohranjuje osnovno implementacijo, ki jo **podrazredi** (_ang. subclass_) "_podedujejo_" in (običajno) nadgradijo.

Podrazredi lahko starševski razred nadgradijo na več različnih načinov. Lahko preprosto dodajo nove atribute in metode, lahko pa nadomestijo (_ang. override_) obstoječe metode in jih tako nadgradijo ali pa kar v celoti zamenjajo.

Večina jezikov pozna tudi razrede, od katerih ne moremo dedovati, in metode, ki jih ne moremo nadomestiti (_npr. v Javi, lahko ustvarimo `final` razred ali metodo_).

## Polimorfizem

**Polimorfizem** (_iz gr. "več oblik"_) omogoča ustvarjanje razredov z različnimi internimi strukturami ter skupnim zujanjim vmesnikom (_tj. poseben razred, ki določa obvezne metode razreda_).

> Vmesnik _Žival_ definira metodo _glas()_. Vsi razredi, ki implementirajo vmesnik _Žival_ morajo torej implementirati metodo _glas()_.  
> To nam sedaj omogoča, da ustvarimo razreda _Pes_ in _Maček_, ki implementirata metodo vsak na svoj način (Pes: `return "Meow"` in Maček: `return "Woof"`).  
> Ustvarili smo **dve obliki** vmesnika _Žival_.

## Sporočila

Objektni v dani aplikaciji potrebujejo način komunikacije, da lahko sodelujejo. Pri objektno usmerjenem pristopu objekt ne more direktno klicati funkcije drugega objekta, zato mu mora poslati **sporočilo** (_ang. message_). V sporočilu je zapisano ime metode in vsi potrebni parametri za to funkcijo.

Primer sporočil bomo videli pri diagramih zaporedja.
