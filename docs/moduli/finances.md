icon:fontawesome/solid/cash-register

# Korisničko uputstvo za modul Finances

## 1. Svrha modula

Modul `Finances` služi za vođenje finansijskog dnevnika, finansijskih stavki i izveštaja Glavne knjige. U njemu korisnik može da:

- vodi finansijske dnevnike i stranice dnevnika
- unosi i uređuje stavke knjiženja
- prati saldo i veze otvorenih stavki
- radi specijalne obrade iz alatne trake dnevnika
- pregleda finansijske izveštaje

Ovo uputstvo je namenjeno operativnim i računovodstvenim korisnicima koji rade u finansijskom dijelu aplikacije.

## 2. Kako je organizovan modul

Modul je organizovan u dve glavne cjeline:

- `Journal Pages`
- `Reports`

U okviru `Journal Pages` korisnik radi na dva nivoa:

1. pregled i otvaranje stranica finansijskog dnevnika
2. pregled i obrada pojedinačnih stavki knjiženja

Praktično, najčešći tok rada izgleda ovako:

1. otvorite ili napravite stranicu dnevnika
2. unesite ili proverite zaglavlje dokumenta
3. dodajte stavke knjiženja
4. po potrebi koristite alatnu traku za specijalne akcije
5. proverite rezultat kroz listu stavki i izveštaje

## 3. Journal Pages

### 3.1. Pregled stranica dnevnika

Ekran `Journal Pages` služi za pregled svih finansijskih stranica dnevnika.

Kada se koristi:

- kada tražite ranije unet dokument
- kada želite da otvorite postojeću finansijsku stranicu
- kada pravite novu stranicu dnevnika

Na listi se tipično vide:

- broj stranice dnevnika
- datum
- tip dokumenta
- status
- opis
- podaci o reviziji
- podatak da li je dokument auto-kreiran

Osnovni koraci:

1. Otvorite `Journal Pages`.
2. Pregledajte listu stranica dnevnika.
3. Po potrebi koristite filtere i sortiranje.
4. Otvorite postojeću stranicu ili kreirajte novu.

Očekivani ishod:

- korisnik dolazi do konkretne stranice dnevnika na kojoj radi dalje knjiženje

### 3.2. Zaglavlje stranice dnevnika

Na samoj stranici dnevnika korisnik unosi ili proverava osnovne podatke dokumenta.

Najvažnija polja zaglavlja su:

- datum
- tip dokumenta
- opis
- opis revizije, kada je dokument revidiran

Pored toga, sistem prikazuje i informativna polja kao što su:

- status
- broj dnevnika
- datum aktivacije
- datum revizije
- ko je menjao dokument
- da li je dokument auto-kreiran

Osnovni koraci:

1. Otvorite novu ili postojeću stranicu dnevnika.
2. Unesite datum.
3. Izaberite tip dokumenta.
4. Po potrebi unesite opis.
5. Sačuvajte zaglavlje.

Očekivani ishod:

- stranica dnevnika je spremna za unos stavki ili za pokretanje specijalnih akcija

## 4. Stavke finansijskog dnevnika

### 4.1. Pregled stavki

Na stranici dnevnika korisnik radi sa stavkama knjiženja.

Za svaku stavku mogu se voditi podaci kao što su:

- datum dokumenta
- datum dospijeća
- poslovnica
- konto
- kontra konto pri unosu nove stavke
- partner
- agent partnera
- opis veze knjiženja
- oznake ili labeli
- opis
- dugovna i potražna vrednost
- valuta i kurs
- iznos u stranoj valuti
- obračunski period od-do

### 4.2. Unos nove stavke

Osnovni koraci:

1. Na otvorenoj stranici dnevnika dodajte novu stavku.
2. Unesite datum dokumenta i datum dospijeća.
3. Izaberite poslovnicu.
4. Izaberite konto.
5. Po potrebi unesite partnera, agenta i opis veze.
6. Po potrebi dodajte labele.
7. Unesite opis stavke.
8. Ako konto radi u stranoj valuti, izaberite valutu i unesite strani iznos.
9. Proverite preračun u valutu dnevnika.
10. Ako postoji vremensko razgraničenje, unesite period od-do.
11. Sačuvajte stavku.

Očekivani ishod:

- stavka ulazi u dnevnik i učestvuje u ukupnom saldu stranice

### 4.3. Rad sa stranom valutom

Ako je konto definisan kao konto sa stranom valutom, sistem podržava unos:

- valute
- kursa
- datuma kursa
- dugovne ili potražne vrednosti u stranoj valuti

Na osnovu tih podataka sistem može izračunati vrednost u valuti dnevnika.

Šta proveriti ako iznos nije očekivan:

- da je izabrana odgovarajuća valuta
- da je datum kursa ispravan
- da je kurs validan
- da je konto zaista definisan kao konto sa stranom valutom

### 4.4. Veze i zatvaranje stavki

Na stavkama je podržan i rad sa vezama otvorenih stavki.

Kada se koristi:

- kada želite da povežete otvorene dugovne i potražne stavke
- kada zatvarate salda po partneru ili kontu

Na stranici dnevnika postoji posebna akcija `Zatvori veze` koja omogućava izbor postojećih linkova i kreiranje stavki za njihovo zatvaranje.

## 5. Akcije sa alatne trake Dnevnika finansija

Na listi `Journal Pages` dostupna je posebna alatna traka sa poslovnim akcijama koje automatski kreiraju novu finansijsku stranicu dnevnika i odgovarajuće stavke. Ove akcije se nalaze u dodatnom meniju sa tri tačke.

Svaka od ovih akcija:

- otvara poseban dijalog za unos parametara
- kreira novu stranicu dnevnika
- korisnika po završetku vodi direktno na novonastalu stranicu

### 5.1. Zatvori konto / klasu

Akcija `Zatvori konto / klasu` služi za zatvaranje konta ili cele klase konta i prenos salda na novo konto.

Kada se koristi:

- na kraju obračunskog perioda
- kada se saldo jedne klase ili grupe konta prenosi na završno konto
- kada se radi zaključavanje rezultata za određeni segment kontnog plana

Polja koja korisnik unosi:

- datum
- tip dokumenta
- opis
- konto ili klasa koja se zatvara
- novo konto
- opcija `Kreiraj jednu novu stavku`

Kako radi:

1. Sistem pronalazi salda svih konta koja počinju zadatim kodom.
2. Za ta konta formira zatvarajuće stavke.
3. Zatim formira novu stavku ili više novih stavki na ciljnom kontu.

Ako je uključena opcija `Kreiraj jednu novu stavku`:

- sistem sabira rezultat i pravi jednu zbirnu novu stavku na ciljnom kontu

Ako opcija nije uključena:

- sistem pravi nove stavke po detaljnijoj strukturi postojećih salda

Osnovni koraci:

1. Otvorite meni akcija na listi `Journal Pages`.
2. Izaberite `Zatvori konto / klasu`.
3. Unesite datum i tip dokumenta.
4. U polje za zatvaranje unesite konto ili početak šifre klase koju zatvarate.
5. Izaberite novo konto na koje se rezultat prenosi.
6. Po potrebi uključite opciju za jednu zbirnu stavku.
7. Unesite opis.
8. Potvrdite kreiranje.

Očekivani ishod:

- kreira se nova auto-kreirana stranica dnevnika sa stavkama zatvaranja i protivstavkama na novom kontu

Šta proveriti ako rezultat nije očekivan:

- da li je unet pravi kod konta ili klase
- da li je novo konto ispravno izabrano
- da li u dnevniku postoje salda za zatvaranje
- da li ciljna šifra konta pripada odgovarajućem kontnom planu

### 5.2. Prenesi početno stanje

Akcija `Prenesi početno stanje` služi za prenos početnog stanja iz prethodnog dnevnika u aktivni dnevnik.

Kada se koristi:

- na početku nove poslovne godine
- kada treba preneti početna stanja aktive, pasive, kapitala i vanbilansnih konta

Polja koja korisnik unosi:

- datum
- tip dokumenta
- izvorni dnevnik
- opis

Kako radi:

1. Sistem uzima aktivne stavke iz izvornog dnevnika.
2. Računa saldo po kontima koja ulaze u početno stanje.
3. Pokušava da mapira konta po šifri iz izvornog kontnog plana u aktivni kontni plan.
4. Kreira novu početnu finansijsku stranicu dnevnika sa odgovarajućim stavkama.

Ako aktivni dnevnik i izvorni dnevnik koriste različitu valutu:

- sistem preračunava stavke prema kursu aktivnog dnevnika

Osnovni koraci:

1. Otvorite meni akcija.
2. Izaberite `Prenesi početno stanje`.
3. Proverite datum, koji je po pravilu početak godine aktivnog dnevnika.
4. Izaberite tip dokumenta.
5. Izaberite izvorni dnevnik, najčešće iz prethodne godine.
6. Unesite opis.
7. Potvrdite kreiranje.

Očekivani ishod:

- kreira se auto-kreirana stranica dnevnika sa početnim stanjima u aktivnom dnevniku

Šta proveriti ako akcija ne daje rezultat:

- da li je prethodni dnevnik pravilno izabran
- da li u izvornoj godini postoje aktivne stavke za prenos
- da li se konta iz prethodnog i tekućeg kontnog plana mogu mapirati po šifri
- da li je za firmu definisana glavna poslovnica

### 5.3. Revalorizuj stavke u stranoj valuti

Akcija `Revalorizuj stavke u stranoj valuti` služi za obračun kursnih razlika na kontima koja su označena za revalorizaciju strane valute.

Kada se koristi:

- na kraju perioda
- kada treba uskladiti vrednosti stavki u stranoj valuti sa aktuelnim kursom
- pri pripremi mesečnog ili godišnjeg zatvaranja

Polja koja korisnik unosi:

- datum
- tip dokumenta
- opis

Kako radi:

1. Sistem pronalazi konta aktivnog dnevnika koja imaju uključenu revalorizaciju strane valute.
2. Uzima salda tih konta po valuti.
3. Za svako saldo obračunava novu vrednost po kursu na zadati datum.
4. Izračunava razliku između postojeće i nove vrednosti.
5. Kreira stavke revalorizacije i protivstavke na kontima pozitivnih ili negativnih kursnih razlika.

Važno:

- konto mora imati definisana konta za pozitivne i negativne kursne razlike

Osnovni koraci:

1. Otvorite meni akcija.
2. Izaberite `Revalorizuj stavke u stranoj valuti`.
3. Unesite datum obračuna.
4. Izaberite tip dokumenta.
5. Po potrebi unesite opis.
6. Potvrdite kreiranje.

Očekivani ishod:

- kreira se nova auto-kreirana finansijska stranica dnevnika sa stavkama revalorizacije

Šta proveriti ako akcija ne prolazi:

- da li postoje konta označena za revalorizaciju
- da li ta konta imaju definisana konta pozitivnih i negativnih kursnih razlika
- da li postoje salda u stranim valutama na datum obračuna

### 5.4. Vremensko razgraničenje prihoda i rashoda

Akcija `Vremensko razgraničenje prihoda i rashoda` služi za automatsko priznavanje dela prihoda ili rashoda po obračunskom periodu.

Kada se koristi:

- kada se trošak ili prihod odnosi na period duži od jednog datuma knjiženja
- kada je potrebno rasporediti iznos na odgovarajući obračunski period
- pri mesečnim obračunima i zatvaranjima

Polja koja korisnik unosi:

- datum
- tip dokumenta
- opis
- šifra konta ili klase za koje se radi razgraničenje

Kako radi:

1. Sistem pronalazi konta koja imaju definisan konto razgraničenja.
2. Uzima ranije stavke sa obračunskim periodom `od-do`.
3. Izračunava koliko do zadatog datuma treba priznati kao prihod ili rashod.
4. Umanjuje izvorni konto za obračunati deo.
5. Kreira protivstavku na kontu razgraničenja.

Akcija koristi samo stavke koje:

- imaju definisan obračunski period
- pripadaju kontima sa podešenim kontom razgraničenja
- imaju saldo koji još nije u potpunosti razgraničen

Osnovni koraci:

1. Otvorite meni akcija.
2. Izaberite `Vremensko razgraničenje prihoda i rashoda`.
3. Unesite datum do kog se vrši priznavanje.
4. Izaberite tip dokumenta.
5. Unesite šifru konta ili klase za koje radite razgraničenje.
6. Po potrebi unesite opis.
7. Potvrdite kreiranje.

Očekivani ishod:

- kreira se nova auto-kreirana stranica dnevnika sa stavkama vremenskog razgraničenja

Šta proveriti ako nema rezultata:

- da li konta imaju podešen konto razgraničenja u kontnom planu
- da li postoje stavke sa popunjenim poljima perioda `od-do`
- da li je zadati konto ili prefiks konta ispravan

## 6. Dodatne korisne akcije na stranici dnevnika

Pored akcija sa liste dnevnika, na samoj stranici postoje i korisne pomoćne radnje:

- `Zatvori veze`
- `Napravi kontra stavove`
- `Podesi datume sa stranice`
- ažuriranje kurseva i revalorizacija odabranih stavki
- pregled bilansa stavki

### 6.1. Napravi kontra stavove

Ova akcija se koristi kada želite da od odabranih stavki automatski napravite kontra knjiženja na zadatom kontu.

Korisnik bira:

- kontra konto
- da li će se stavke grupisati

### 6.2. Podesi datume sa stranice

Ova akcija postavlja datum dokumenta i datum dospijeća na stavkama prema datumu same stranice dnevnika.

Kada se koristi:

- kada su stavke unete sa različitim datumima koje treba uskladiti

### 6.3. Ažuriranje kurseva i revalorizacija odabranih stavki

Na odabranim stavkama moguće je pokrenuti ažuriranje kursa i novi preračun.

Kada se koristi:

- kada su promene kursa nastale nakon unosa stavki
- kada je potrebno korigovati vrednost u valuti dnevnika za izabrane stavke

## 7. Entries pregled i sažeci

U okviru `Journal Pages` postoji i pregled svih finansijskih stavki kroz poseban panel `Entries`.

Tu korisnik može da:

- filtrira stavke po datumu, dokumentu, kontu, partneru i ledgeru
- uvozi i izvozi podatke
- podešava kolone
- koristi napredno sortiranje
- pregleda zbirne iznose

Pored detaljne liste postoji i sažeti prikaz sa grupisanjem i agregacijama, gde se može:

- grupisati po kontu, partneru, poslovnici, valuti i drugim poljima
- birati agregatna polja
- uključiti periodnu promenu

Ovaj deo je posebno koristan za analizu prometa i salda bez otvaranja svake pojedinačne stranice.

## 8. Reports

Ekran `Reports` služi za finansijske izveštaje.

Na osnovu koda modula izveštaji su organizovani u više grupa, uključujući:

- bruto bilanse
- kartice
- izveštaje po partnerima
- specifikacije konta

Tipični filteri u izveštajima su:

- dnevnik
- period
- poslovnica
- dokument i tip dokumenta
- konto ili raspon konta
- partner
- valuta
- rok dospijeća
- uključivanje ili isključivanje početnih i završnih stavki

Kada se koriste:

- za proveru prometa i salda
- za analizu otvorenih stavki
- za kontrolu po partneru, kontu ili poslovnici
- za pripremu računovodstvenih izveštaja

## 9. Najčešće situacije koje treba proveriti

### 9.1. Stranica dnevnika se ne može sačuvati

Proveriti:

- da li su datum i tip dokumenta uneseni
- da li su stavke uravnotežene kada je to potrebno

### 9.2. Stavka ne daje očekivani iznos

Proveriti:

- konto
- duguje ili potražuje stranu
- valutu, kurs i datum kursa
- da li je konto vezan za stranu valutu

### 9.3. Zatvaranje konta ili klase ne daje rezultat

Proveriti:

- da li uneti prefiks zaista odgovara kontima koja imaju saldo
- da li je novo konto ispravno podešeno

### 9.4. Prenos početnog stanja ne uspeva

Proveriti:

- izvorni dnevnik
- mapiranje konta po šifri
- postojanje glavne poslovnice

### 9.5. Revalorizacija ne kreira stavke

Proveriti:

- da li postoje salda u stranoj valuti
- da li su konta označena za revalorizaciju
- da li su definisana konta kursnih razlika

### 9.6. Vremensko razgraničenje ne daje rezultat

Proveriti:

- da li stavke imaju period `od-do`
- da li konto ima konto razgraničenja
- da li je izabrani datum u okviru obračunskog toka

## 10. Preporučeni redosled rada za korisnike

Za svakodnevni rad preporučen redosled je:

1. proverite aktivni dnevnik i tip dokumenta
2. unesite ili otvorite finansijsku stranicu
3. unesite stavke
4. proverite bilans i veze stavki
5. po potrebi pokrenite specijalne akcije iz alatne trake
6. proverite rezultat kroz `Entries` i `Reports`

Na taj način modul `Finances` ostaje pregledan, a svaka automatska akcija može odmah da se proveri kroz novonastalu stranicu dnevnika.
