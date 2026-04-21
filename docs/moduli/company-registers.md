icon:fontawesome/solid/clipboard-list

# Korisničko uputstvo za modul Company Registers

## 1. Svrha modula

Modul `Company Registers` služi za vođenje šifarnika i podešavanja na nivou konkretne kompanije. Podaci iz ovog modula koriste se svakodnevno u drugim poslovnim modulima, posebno u fakturama, finansijama, kasama i evidenciji partnera.

U ovom modulu korisnik najčešće vodi:

- poslovnice
- partnere
- bankovne račune partnera
- dnevnike
- oznake i pomoćne šifarnike
- knjige kursnih lista
- tipove dokumenata
- jedinice mere
- kontne planove i konta
- račune blagajne ili banke
- praznike

## 2. Preporučeni redosled rada

Ako se modul podešava od početka, preporučen redosled je:

1. proverite da su `Global Registers` već popunjeni
2. unesite poslovnice
3. unesite jedinice mere
4. unesite tipove dokumenata
5. podesite kontne planove, klase i konta
6. unesite dnevnike
7. unesite partnere i njihove bankovne račune
8. podesite račune blagajne ili banke
9. po potrebi unesite knjige kursnih lista i praznike

Ovim redosledom se smanjuje broj praznih lookup listi i prekida pri unosu.

## 3. Branches

Ekran `Branches` služi za vođenje poslovnica kompanije.

Kada se koristi:

- kada kompanija radi kroz jednu ili više poslovnica
- kada dokumenti, partneri ili računi zavise od poslovnice

Na ovom ekranu vodi se istorijski zapis, što znači da se promene podataka poslovnice mogu pratiti kroz vreme.

Osnovni koraci:

1. Otvorite `Branches`.
2. Dodajte novu poslovnicu.
3. Unesite osnovne podatke kao što su šifra, identifikacija i adresa.
4. Izaberite državu, entitet, regiju i opštinu gde je to potrebno.
5. Obeležite da li je poslovnica sedište.
6. Ako nije sedište, po potrebi povežite glavnu poslovnicu.
7. Sačuvajte unos.

Očekivani ishod:

- poslovnica postaje dostupna u dokumentima, kasama, prodajnim mestima i izveštajima

Šta proveriti ako unos ne prolazi:

- da su osnovni teritorijalni šifarnici već uneti u `Global Registers`
- da glavna poslovnica nije ista kao tekuća poslovnica
- da su istorijski podaci uneseni u ispravnom kontekstu

## 4. Parties

Ekran `Parties` služi za vođenje partnera. Modul podržava rad sa pravnim licima, fizičkim licima, bankama i opštim tipovima partnera.

Kada se koristi:

- kada unosite kupce, dobavljače, banke ili druge subjekte
- kada menjate identifikacione, kontakt ili poreske podatke partnera

Na ovom ekranu takođe postoji istorija podataka, pa je moguće voditi promene kroz vreme.

Osnovni koraci:

1. Otvorite `Parties`.
2. Dodajte novog partnera.
3. Izaberite tip partnera.
4. Unesite osnovne identifikacione podatke.
5. Ako je partner pravno lice, proverite PDV status, PIB i povezane podatke.
6. Ako je partner fizičko lice, unesite lične podatke i identifikacioni dokument.
7. U delu adrese i prebivališta unesite državu, entitet, regiju, opštinu, mesto i adresu.
8. Po potrebi unesite pravnu formu, telefone, email i web adresu.
9. Sačuvajte partnera.

Očekivani ishod:

- partner je dostupan za izbor u fakturama, računima, bankovnim računima i drugim modulima

Posebnosti koje treba znati:

- za domaće partnere identifikacioni broj i lokacijski podaci mogu biti obavezni
- kod pravnih lica PDV status utiče na dodatna polja
- banke se mogu voditi kao poseban tip partnera

## 5. Party Bank Accounts

Ekran `Party bank accounts` služi za vođenje bankovnih računa partnera.

Kada se koristi:

- kada partner ima jedan ili više računa
- kada je račun potreban za plaćanja, naplatu ili eksport prema banci

Osnovni koraci:

1. Otvorite `Party bank accounts`.
2. Dodajte novi račun.
3. Izaberite partnera.
4. Izaberite banku partnera.
5. Izaberite valutu računa.
6. Unesite broj računa i ostale potrebne podatke.
7. Sačuvajte unos.

Očekivani ishod:

- bankovni račun postaje dostupan u procesima plaćanja i povezanim dokumentima

Šta proveriti ako račun nije dostupan:

- da partner postoji i da je sačuvan
- da banka partnera postoji u sistemu
- da je izabrana ispravna valuta

## 6. Journals

Ekran `Journals` služi za vođenje dnevnika.

Kada se koristi:

- kada kompanija vodi poslovne događaje kroz različite dnevnike
- kada drugi moduli traže izbor dnevnika pri unosu dokumenata

Osnovni koraci:

1. Otvorite `Journals`.
2. Dodajte novi dnevnik.
3. Proverite podrazumevane vrednosti koje sistem nudi za novi unos.
4. Unesite ili dopunite godinu, valutu i vezu sa kontnim planom.
5. Sačuvajte dnevnik.

Očekivani ishod:

- dnevnik je dostupan pri radu sa dokumentima i knjiženjem

## 7. Labels

Ekran `Labels` služi za vođenje pomoćnih oznaka.

Kada se koristi:

- kada firma koristi interne klasifikacije ili oznake
- kada je potrebno dodatno označavanje podataka radi filtriranja ili organizacije

Osnovni koraci:

1. Otvorite `Labels`.
2. Dodajte novu oznaku ili izmenite postojeću.
3. Sačuvajte promenu.

Očekivani ishod:

- oznaka postaje dostupna tamo gde je sistem koristi

## 8. Currency Exchange Books

Ekran `Currency Exchange Books` služi za vođenje knjiga kursnih lista i njihovih dnevnih kurseva.

Kada se koristi:

- kada firma vodi sopstvene kursne liste
- kada se kursevi unose ručno ili uvoze iz izvora

Osnovni koraci:

1. Otvorite `Currency Exchange Books`.
2. Dodajte novu knjigu kursne liste.
3. Izaberite valutu ili izvor kursa, u zavisnosti od načina rada.
4. Sačuvajte knjigu.
5. Otvorite deo sa kursevima za izabranu knjigu.
6. Dodajte nove kurseve ručno ili koristite import iz feed-a ako je izvor podešen.

Očekivani ishod:

- knjiga kursne liste i njeni kursevi postaju dostupni za procese koji koriste kurs

Šta proveriti ako import ne radi:

- da knjiga ima definisan izvor
- da je izabran period od-do
- da podaci za taj period već nisu ažurni

## 9. Document Types

Ekran `Ledger document category types` služi za vođenje tipova dokumenata po vrsti glavne knjige ili ledgera.

Kada se koristi:

- kada dokumenti moraju biti razvrstani po tipu
- kada drugi moduli, poput faktura i knjiženja, zavise od tipa dokumenta

Osnovni koraci:

1. Otvorite `Document Types`.
2. Izaberite ledger sa leve strane.
3. Dodajte novi tip dokumenta ili izmenite postojeći.
4. Po potrebi izaberite kategoriju dokumenta.
5. Sačuvajte promenu.

Dodatna mogućnost:

- sistem podržava kreiranje tipova iz postojećih kategorija dokumenata

Očekivani ishod:

- tipovi dokumenata postaju dostupni na ekranima gde se bira vrsta dokumenta

## 10. Measure Units

Ekran `Measure Units` služi za vođenje jedinica mere.

Kada se koristi:

- kada unosite robu ili usluge
- kada količine na dokumentima moraju imati standardizovanu jedinicu mere

Osnovni koraci:

1. Otvorite `Measure Units`.
2. Dodajte novu jedinicu mere ili izmenite postojeću.
3. Sačuvajte promenu.

Očekivani ishod:

- jedinica mere je dostupna na proizvodima i stavkama dokumenata

## 11. Accounting Plans

Ekran `Accounting Plans` služi za podešavanje kontnih planova, klasa konta i pojedinačnih konta.

Kada se koristi:

- pri početnom računovodstvenom podešavanju sistema
- kada se menja struktura konta ili dodaju nova konta

Ekran je organizovan u tri povezane celine:

- kontni planovi
- klase konta
- pojedinačna konta

### 11.1. Kontni planovi

Osnovni koraci:

1. Otvorite `Accounting Plans`.
2. Dodajte novi kontni plan ili izmenite postojeći.
3. Sačuvajte promenu.

### 11.2. Klase konta

Osnovni koraci:

1. Izaberite kontni plan.
2. Otvorite tab za klase.
3. Dodajte klasu konta.
4. Sačuvajte promenu.

### 11.3. Konta

Osnovni koraci:

1. Izaberite kontni plan.
2. Otvorite tab za konta.
3. Dodajte novo konto.
4. Unesite šifru i naziv konta.
5. Po potrebi podesite da li je konto vezano za partnera ili dnevnik.
6. Po potrebi unesite podrazumevani opis i konto razgraničenja.
7. Ako konto radi sa stranom valutom, uključite tu opciju i podesite revalorizaciju i konta kursnih razlika.
8. Sačuvajte konto.

Očekivani ishod:

- kontni plan i njegova konta postaju dostupni dnevnicima, knjiženju i finansijskim procesima

## 12. Cash Accounts

Ekran `Cash Accounts` služi za vođenje blagajničkih i bankovnih računa firme.

Kada se koristi:

- kada firma radi sa gotovinom
- kada firma koristi bankovne račune za plaćanja i naplatu

Osnovni koraci:

1. Otvorite `Cash Accounts`.
2. Dodajte novi račun.
3. Izaberite poslovnicu.
4. Izaberite tip računa.
5. Ako je tip bankovni, izaberite banku i e-banking tip gde je potreban.
6. Izaberite valutu.
7. Povežite konto ako je to deo podešavanja.
8. Sačuvajte unos.

Očekivani ishod:

- račun je dostupan za bankovne izvode, naloge za plaćanje i druge procese

Šta proveriti ako unos ne prolazi:

- da su poslovnica, valuta i banka već uneti
- da je za bankovni račun uneta banka i potrebni dodatni podaci

## 13. Holidays

Ekran `Holidays` služi za vođenje praznika.

Kada se koristi:

- kada radni kalendar ili obračuni zavise od praznika
- kada sistemski procesi treba da uzmu u obzir neradne dane

Osnovni koraci:

1. Otvorite `Holidays`.
2. Dodajte novi praznik.
3. Unesite datum i opis.
4. Sačuvajte promenu.

Očekivani ishod:

- praznik je zabeležen i dostupan procesima koji koriste kalendar rada

## 14. Najčešće situacije koje treba proveriti

### 14.1. Lookup polje je prazno

Proveriti:

- da li su odgovarajući šifarnici već uneti u `Global Registers`
- da li je prethodni povezani podatak sačuvan

### 14.2. Partner se ne može sačuvati

Proveriti:

- tip partnera
- da li su za domaće partnere uneti obavezni identifikacioni i adresni podaci
- da li su PDV podaci dosledni

### 14.3. Konto ili dnevnik nije dostupno u drugim modulima

Proveriti:

- da li je konto uneto u odgovarajućem kontnom planu
- da li je dnevnik vezan za ispravan kontni plan i godinu

### 14.4. Kursna lista ne daje očekivane podatke

Proveriti:

- da li knjiga ima kurseve za traženi datum
- da li je izvor podešen ako se koristi import

## 15. Preporuka za rad

- prvo održavajte osnovne šifarnike, pa tek onda operativne module
- veće izmene na partnerima, kontima i dnevnicima radite planski
- posle svake važne izmene proverite jedan konkretan poslovni tok, na primer unos fakture ili naloga za plaćanje

Na taj način `Company Registers` ostaje stabilna baza za svakodnevni rad u ostatku sistema.
