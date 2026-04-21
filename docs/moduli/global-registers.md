icon: fontawesome/solid/globe

# Korisničko uputstvo za modul Global Registers

## 1. Svrha modula

Modul `Global Registers` služi za održavanje zajedničkih šifarnika na nivou sistema. Podaci iz ovog modula koriste se i u drugim modulima, naročito u `Company Registers`, `Invoices` i ostalim poslovnim procesima.

U ovom modulu korisnik najčešće vodi:

- biroe
- kompanije
- države
- entitete ili regije
- opštine
- valute
- pravne forme

Ovo su osnovni matični podaci. Zbog toga se preporučuje da se izmene rade pažljivo i planski.

## 2. Preporučeni redosled rada

Ako prvi put podešavate sistem, preporučen redosled je:

1. unesite države
2. unesite entitete ili regije po državama
3. unesite opštine
4. unesite valute
5. unesite pravne forme
6. unesite biroe
7. unesite kompanije

Na taj način će kasniji ekrani imati spremne lookup liste i manje je verovatno da će doći do prekida pri unosu.

## 3. Bureaux

Ekran `Bureaux` služi za vođenje biroa u sistemu.

Kada se koristi:

- kada jedna instalacija obuhvata više biroa
- kada kompanije treba povezati sa određenim biroom

Osnovni koraci:

1. Otvorite `Bureaux`.
2. Dodajte novi biro ili izmenite postojeći.
3. Unesite osnovne identifikacione podatke.
4. Sačuvajte promenu.

Očekivani ishod:

- biro postaje dostupan za izbor na drugim ekranima, naročito pri unosu kompanije

Šta proveriti ako biro nije dostupan:

- da je zapis sačuvan
- da nije filtriran u trenutnom prikazu

## 4. Companies

Ekran `Companies` služi za vođenje kompanija koje postoje u sistemu.

Kada se koristi:

- kada se uvodi nova kompanija
- kada se menjaju osnovni podaci kompanije
- kada kompaniju treba povezati sa državom i biroom

Osnovni koraci:

1. Otvorite `Companies`.
2. Dodajte novu kompaniju ili otvorite postojeću.
3. Unesite osnovne podatke kompanije.
4. Izaberite državu.
5. Izaberite biro ako je to deo vaše organizacije rada.
6. Sačuvajte promenu.

Očekivani ishod:

- kompanija je dostupna za dalja podešavanja i rad u drugim modulima

Dodatna mogućnost:

- na ekranu je podržan i upload logotipa za izabranu kompaniju

Šta proveriti ako unos ne prolazi:

- da su obavezna polja popunjena
- da država i biro postoje u sistemu
- da je najpre izabrana ili sačuvana kompanija pre pokušaja slanja logotipa

## 5. Countries

Ekran `Countries` služi za vođenje država.

Kada se koristi:

- pri početnom podešavanju sistema
- kada sistem treba da podrži rad sa novom državom

Osnovni koraci:

1. Otvorite `Countries`.
2. Dodajte novu državu ili izmenite postojeću.
3. Sačuvajte promenu.

Očekivani ishod:

- država postaje dostupna u svim povezanim šifarnicima i dokumentima

Napomena:

- države se koriste kao osnova za dalji unos entiteta, regija i opština

## 6. Country States

Ekran `Country States` služi za vođenje entiteta ili administrativnih jedinica u okviru države.

Kada se koristi:

- kada za određenu državu želite detaljniju teritorijalnu podelu
- kada je unos adresa ili klasifikacije vezan za entitet

Osnovni koraci:

1. Otvorite `Country States`.
2. Dodajte novu stavku.
3. Izaberite državu kojoj pripada.
4. Unesite naziv i ostale potrebne podatke.
5. Sačuvajte promenu.

Očekivani ishod:

- entitet postaje dostupan pri daljem unosu regija, opština i adresa

## 7. Country Regions

Ekran `Country Regions` služi za vođenje regija u okviru države i po potrebi u okviru izabranog entiteta.

Kada se koristi:

- kada se adrese i teritorijalna podela vode detaljnije od nivoa države
- kada je regija potrebna za filtriranje, klasifikaciju ili tačnu adresu

Osnovni koraci:

1. Otvorite `Country Regions`.
2. Dodajte novu regiju.
3. Izaberite državu.
4. Po potrebi izaberite i entitet ili državni nivo kojem regija pripada.
5. Sačuvajte promenu.

Očekivani ishod:

- regija je dostupna pri unosu opština i adresa

## 8. Country Municipalities

Ekran `Country Municipalities` služi za vođenje opština.

Kada se koristi:

- pri definisanju kompletne teritorijalne strukture
- kada korisnici kasnije unose adrese poslovnica, partnera ili drugih subjekata

Osnovni koraci:

1. Otvorite `Country Municipalities`.
2. Dodajte novu opštinu.
3. Izaberite državu.
4. Po potrebi izaberite entitet i regiju.
5. Sačuvajte promenu.

Očekivani ishod:

- opština je dostupna za izbor na ekranima gde se unose adrese

Šta proveriti ako lookup lista nije očekivana:

- da su država, entitet i regija prethodno ispravno uneti
- da korisnik bira odgovarajući viši nivo teritorijalne podele

## 9. Currencies

Ekran `Currencies` služi za vođenje valuta.

Kada se koristi:

- pri početnom podešavanju sistema
- kada se uvodi rad sa novom valutom

Osnovni koraci:

1. Otvorite `Currencies`.
2. Dodajte novu valutu ili izmenite postojeću.
3. Po potrebi povežite je sa državom ili drugim opisnim podacima.
4. Sačuvajte promenu.

Očekivani ishod:

- valuta postaje dostupna u dnevnicima, kasama, partnerima, cenovnicima i dokumentima

## 10. Entity Legal Forms

Ekran `Entity legal forms` služi za vođenje pravnih formi.

Kada se koristi:

- kada vodite partnere ili kompanije po pravnoj formi
- kada izveštavanje ili evidencija zahteva taj podatak

Osnovni koraci:

1. Otvorite `Entity legal forms`.
2. Dodajte novu pravnu formu.
3. Po potrebi povežite je sa državom ili odgovarajućom klasifikacijom.
4. Sačuvajte promenu.

Očekivani ishod:

- pravna forma je dostupna pri unosu partnera i drugih subjekata

## 11. Najčešće situacije koje treba proveriti

### 11.1. Podatak nije dostupan u drugom modulu

Proveriti:

- da je zapis sačuvan
- da nije obrisan ili filtriran
- da je prethodno unet odgovarajući nadređeni podatak, na primer država pre entiteta ili opštine

### 11.2. Lookup lista je prazna

Proveriti:

- da li postoje osnovni šifarnici od kojih zavisi taj ekran
- da li korisnik bira ispravan kontekst, na primer odgovarajuću državu

### 11.3. Kompanija ne može da se unese do kraja

Proveriti:

- da li su država i biro već uneti
- da li su obavezni identifikacioni podaci popunjeni

## 12. Preporuka za održavanje

- izmene u ovom modulu radite pre masovnog rada u drugim modulima
- ne menjajte nazive i klasifikacije bez prethodne provere gde se sve koriste
- posle svake veće izmene proverite lookup polja u `Company Registers`

Na taj način `Global Registers` ostaje stabilna osnova za ceo sistem.
