icon:fontawesome/solid/building

# Korisničko uputstvo za modul Fixed Assets

## 1. Pregled modula

Modul `Fixed Assets` služi za vođenje evidencije osnovnih sredstava, njihovih klasa, lokacija, zaduženja po zaposlenima, promena vrednosti i obračuna amortizacije.

U okviru modula korisnik najčešće radi sledeće:

1. podešava klase osnovnih sredstava i lokacije
2. unosi kartice osnovnih sredstava
3. formira dokumente promena nad sredstvima
4. obračunava amortizaciju
5. podešava pravila knjiženja za prenos u finansijsko knjigovodstvo
6. koristi izveštaje za pregled stanja, promena i zaduženja

## 2. Šta je poželjno podesiti pre rada

Pre redovnog rada u modulu preporučuje se da budu pripremljeni:

1. dnevnik za osnovna sredstva
2. tipovi dokumenata za osnovna sredstva
3. klase osnovnih sredstava
4. lokacije osnovnih sredstava
5. pravila knjiženja, ako se promene iz ovog modula prenose u Glavnu knjigu

Ako neki od ovih podataka nije podešen, korisnik može moći da otvori ekran, ali neće moći da završi unos ili obradu dokumenta.

## 3. Klase osnovnih sredstava

Odeljak `Fixed Asset Classes` služi za definisanje osnovnih pravila amortizacije koja važe za grupu sredstava iste vrste.

### Kada se koristi

Koristi se pre unosa pojedinačnih sredstava, da bi svako sredstvo moglo da se veže za odgovarajuću klasu.

### Podaci koji se podešavaju

Za klasu se podešavaju:

1. `Name`
2. `Depreciation method`
3. `Depreciation rate`
4. `Life in months`

### Kako unos funkcioniše

Kod unosa klase moguće je raditi na dva načina:

1. uneti stopu amortizacije, pa će sistem iz toga izračunati vek trajanja u mesecima
2. uključiti unos preko `Life in months`, pa će sistem iz broja meseci preračunati stopu

### Preporučeni postupak

1. Otvorite `Fixed Asset Classes`.
2. Dodajte novu klasu.
3. Unesite naziv klase.
4. Izaberite metod amortizacije.
5. Unesite stopu ili broj meseci, zavisno od načina rada.
6. Sačuvajte zapis.

### Očekivani rezultat

Klasa postaje dostupna pri unosu osnovnog sredstva i pri pravilima knjiženja.

### Šta proveriti ako unos ne prolazi

1. da li je unet naziv klase
2. da li je izabran metod amortizacije
3. da li je uneta stopa ili vek trajanja kada je to potrebno

## 4. Lokacije osnovnih sredstava

Odeljak `Fixed Asset Locations` služi za definisanje fizičkih ili organizacionih lokacija na kojima se sredstva nalaze.

### Kada se koristi

Koristi se kada želite da pratite gde se sredstvo nalazi i kojoj poslovnici pripada.

### Podaci koji se podešavaju

Za lokaciju se unose:

1. `Branch`
2. `Name`

### Preporučeni postupak

1. Otvorite `Fixed Asset Locations`.
2. Dodajte novu lokaciju.
3. Izaberite poslovnicu.
4. Unesite naziv lokacije.
5. Sačuvajte zapis.

### Očekivani rezultat

Lokacija postaje dostupna u dokumentima osnovnih sredstava, posebno kod zaduženja, stavljanja u upotrebu i početnog stanja.

### Šta proveriti ako unos ne prolazi

1. da li je izabrana poslovnica
2. da li je unet naziv lokacije

## 5. Evidencija osnovnih sredstava

Odeljak `Fixed Assets` služi za vođenje kartice svakog pojedinačnog sredstva.

### Kada se koristi

Koristi se kada se uvodi novo sredstvo u evidenciju ili kada treba ažurirati njegove osnovne podatke.

### Podaci koji se vode na kartici sredstva

Na kartici sredstva vode se sledeći podaci:

1. klasa sredstva
2. naziv
3. šifra
4. serijski broj
5. broj modela
6. dobavljač
7. proizvođač
8. opis
9. datum nabavke
10. datum stavljanja u upotrebu
11. datum prestanka upotrebe
12. metod amortizacije
13. stopa amortizacije
14. vek trajanja u mesecima
15. rezidualna vrednost
16. pregled podrazumevane amortizacije preuzete iz klase

### Važna napomena o amortizaciji

Na kartici sredstva prikazuju se i podaci amortizacije definisani na klasi sredstva. To omogućava da korisnik uporedi:

1. amortizaciju definisanu na samom sredstvu
2. amortizaciju koja važi po klasi

U praksi to znači da se može proveriti da li sredstvo koristi opšta pravila klase ili ima posebno podešene parametre.

### Preporučeni postupak za unos novog sredstva

1. Otvorite `Fixed Assets`.
2. Dodajte novo sredstvo.
3. Izaberite `Asset class`.
4. Unesite naziv sredstva.
5. Po potrebi unesite šifru, serijski broj, model i dobavljača.
6. Unesite proizvođača i opis ako su ti podaci bitni za praćenje.
7. Unesite datum nabavke.
8. Po potrebi unesite datum stavljanja u upotrebu.
9. Podesite amortizaciju na sredstvu ako treba da odstupa od klase.
10. Unesite rezidualnu vrednost ako se vodi.
11. Sačuvajte sredstvo.

### Očekivani rezultat

Sredstvo postaje dostupno za izbor u dokumentima osnovnih sredstava, pravilima knjiženja i izveštajima.

### Šta proveriti ako unos ne prolazi

1. da li je izabrana klasa sredstva
2. da li je unet naziv sredstva
3. da li su datumi logični u odnosu na poslovni tok
4. da li su podaci amortizacije uneseni u odgovarajućem obliku

## 6. Dokumenti osnovnih sredstava

Odeljak `Fixed Asset Pages` služi za unos i obradu svih promena nad osnovnim sredstvima kroz dokumente.

Dokument sadrži:

1. zaglavlje dokumenta
2. stavke dokumenta
3. pregled trenutnog stanja po sredstvu na stavci

### 6.1. Zaglavlje dokumenta

U zaglavlju dokumenta se vode:

1. broj dokumenta
2. datum
3. kategorija dokumenta
4. tip dokumenta
5. revizija
6. opis
7. opis revizije
8. status
9. datum aktivacije i izmene
10. veza prema finansijskom dokumentu, kada je dostupna

### 6.2. Tipične vrste promena koje se vode kroz dokumente

Na osnovu koda modula vidi se da sistem podržava više vrsta dokumenata, uključujući:

1. početno stanje osnovnih sredstava
2. stavljanje sredstva u upotrebu
3. razduženje ili prestanak upotrebe
4. obračun amortizacije
5. promenu metode amortizacije
6. promene vezane za lokaciju i odgovorno lice

Tačan naziv vrste dokumenta korisnik bira kroz `Document type`, u skladu sa podešenjima firme.

### 6.3. Kako se unosi novi dokument

1. Otvorite `Fixed Asset Pages`.
2. Dodajte novi dokument.
3. Unesite datum.
4. Izaberite tip dokumenta.
5. Po potrebi unesite opis.
6. Sačuvajte zaglavlje dokumenta.
7. Otvorite stavke dokumenta i unesite promene po sredstvima.

### 6.4. Kako se unosi stavka dokumenta

Na stavci dokumenta korisnik može unositi:

1. sredstvo
2. lokaciju sredstva
3. zaposlenog koji je zadužen za sredstvo
4. količinu ulaza i izlaza
5. vrednost
6. ispravku vrednosti
7. revalorizaciju
8. ispravku revalorizacije
9. stopu i metod amortizacije
10. osnovicu amortizacije
11. period obračuna amortizacije

Koja polja će biti dostupna zavisi od vrste dokumenta. Na primer:

1. kod amortizacije su u fokusu stopa, metod, osnovica i period
2. kod promene metode amortizacije ne koriste se sva vrednosna polja
3. kod drugih promena u fokusu su količine, vrednosti, lokacija i odgovorno lice

### 6.5. Pregled stanja na stavci

Na ekranu stavke prikazuje se i pregled stanja sredstva, uključujući:

1. neto količinu
2. nabavnu vrednost
3. ispravku vrednosti
4. neto vrednost
5. revalorizaciju
6. ispravku revalorizacije
7. neto revalorizaciju

Ovaj pregled pomaže korisniku da pre unosa ili potvrde promene vidi trenutno stanje sredstva.

### 6.6. Akcije nad dokumentima

Zavisno od vrste dokumenta, nad dokumentom su dostupne sledeće akcije:

1. `Activate`
2. `Publish`
3. `Revise`
4. `Delete`
5. veza ka finansijskom dokumentu, kada je podržana

Uobičajeno značenje akcija je sledeće:

1. `Publish` koristi se za potvrdu i knjiženje dokumenta u dalji tok rada
2. `Activate` se koristi kod određenih vrsta dokumenata, kao što su početno stanje ili promena metode amortizacije
3. `Revise` služi za izmenu kroz novu reviziju
4. `Delete` uklanja dokument koji ne treba da ostane u evidenciji

### 6.7. Posebne akcije sa alatne trake liste dokumenata

Sa alatne trake liste `Fixed Asset Pages` dostupne su i posebne akcije:

1. `Create depreciation`
2. `Transfer initial state`

#### Create depreciation

Ova akcija služi za masovno kreiranje dokumenta amortizacije.

Tok rada:

1. Otvorite listu `Fixed Asset Pages`.
2. U meniju akcija izaberite `Create depreciation`.
3. Unesite tražene podatke dokumenta.
4. Izaberite jednu ili više klasa sredstava.
5. Potvrdite kreiranje.

Očekivani rezultat:

Sistem kreira dokument amortizacije za izabrane klase sredstava.

Šta proveriti ako akcija nije dostupna ili ne daje rezultat:

1. da li je izabrana bar jedna klasa sredstva
2. da li su podešeni tipovi dokumenata za amortizaciju
3. da li postoji aktivan dnevnik za rad sa osnovnim sredstvima

#### Transfer initial state

Ova akcija služi za formiranje dokumenta početnog stanja.

Tok rada:

1. Otvorite listu `Fixed Asset Pages`.
2. U meniju akcija izaberite `Transfer initial state`.
3. Unesite potrebne podatke dokumenta.
4. Potvrdite akciju.

Očekivani rezultat:

Sistem formira dokument početnog stanja koji se dalje može pregledati i obraditi.

Šta proveriti ako unos ne prolazi:

1. da li su dostupni tipovi dokumenata za početno stanje
2. da li je unet obavezan podatak u zaglavlju akcije

### 6.8. Obračun amortizacije na dokumentu i stavci

Kod dokumenata amortizacije dostupna je akcija `Calculate depreciation`.

Ona se može koristiti:

1. na samom dokumentu
2. na pojedinačnoj stavci dokumenta

### Kada se koristi

Koristi se kada želite da sistem izračuna iznos amortizacije na osnovu parametara sredstva i perioda obračuna.

### Šta utiče na rezultat obračuna

Na obračun utiču:

1. metoda amortizacije
2. stopa amortizacije
3. osnovica amortizacije
4. period od datuma `Date from` do `Date to`
5. stanje sredstva pre obračuna

### Šta proveriti ako obračun ne daje očekivan rezultat

1. da li je izabrano sredstvo
2. da li dokument pripada vrsti amortizacije
3. da li su pravilno definisani metod i stopa
4. da li je period obračuna odgovarajući
5. da li sredstvo ima stanje na osnovu koga je moguće obračunati amortizaciju

## 7. Pravila knjiženja osnovnih sredstava

Odeljak `Fixed Asset Accounting Rules` služi za podešavanje načina na koji se promene iz modula osnovnih sredstava prenose na konta u Glavnoj knjizi.

Ovaj odeljak je važan kada firma želi da se dokumenti osnovnih sredstava automatski ili standardizovano knjiže u finansijsko knjigovodstvo.

### 7.1. Šta čini jedno pravilo

Pravilo knjiženja sadrži:

1. `Name`
2. `Document category`
3. `Document type`
4. `Asset class`
5. konkretno sredstvo, ako pravilo važi samo za jedno sredstvo

To znači da se pravilo može definisati:

1. na nivou kategorije dokumenta i klase sredstva
2. detaljnije, za tačan tip dokumenta
3. još uže, za pojedinačno sredstvo

### 7.2. Stavke pravila

Svako pravilo ima i svoje stavke. U njima se definiše redosled i konta na koja se knjiženje vrši.

Pošto modul koristi poseban pregled pravila i stavki, preporučeni rad je:

1. prvo otvoriti ili uneti glavno pravilo
2. zatim u desnom delu ekrana dodati stavke pravila
3. proveriti redosled stavki i izabrana konta

### 7.3. Kada se koristi

Pravila knjiženja treba podesiti pre redovnog korišćenja dokumenata ako se očekuje veza sa finansijskim knjigovodstvom.

### 7.4. Preporučeni postupak

1. Otvorite `Fixed Asset Accounting Rules`.
2. Dodajte novo pravilo.
3. Unesite naziv pravila.
4. Izaberite kategoriju dokumenta.
5. Po potrebi izaberite tip dokumenta.
6. Izaberite klasu sredstva.
7. Po potrebi izaberite i konkretno sredstvo.
8. Sačuvajte pravilo.
9. Dodajte jednu ili više stavki pravila.
10. U svakoj stavci definišite potrebna konta i redosled knjiženja.

### Očekivani rezultat

Kod obrade odgovarajućih dokumenata sistem ima unapred definisanu logiku knjiženja prema Glavnoj knjizi.

### Šta proveriti ako rezultat nije očekivan

1. da li pravilo odgovara tačnoj kategoriji dokumenta
2. da li je izabran odgovarajući tip dokumenta, ako se koristi
3. da li pravilo važi za pravu klasu sredstva ili konkretno sredstvo
4. da li su stavke pravila potpuno definisane
5. da li postoji aktivna veza sa finansijskim dokumentom za dati tip promene

## 8. Izveštaji

Odeljak `Reports` služi za pregled stanja i promena nad osnovnim sredstvima.

Na raspolaganju su sledeći izveštaji:

1. `Fixed Asset Balances`
2. `Fixed Asset Changes`
3. `Fixed Asset Put In Uses`
4. `Fixed Asset Put Out Of Uses`
5. `Fixed Asset Depreciations`
6. `Fixed Asset Write Offs`
7. `Fixed Asset Inventory Drafts`
8. `Fixed Asset Responsibility And Locations`

### 8.1. Filteri koji su podržani

Zavisno od izveštaja, dostupni su filteri kao što su:

1. dnevnik
2. period
3. klasa sredstva
4. sredstvo
5. poslovnica
6. lokacija
7. zaposleni
8. kategorija dokumenta
9. tip dokumenta
10. broj dokumenta
11. grupisanje po izabranim kolonama

### 8.2. Kratko objašnjenje izveštaja

#### Fixed Asset Balances

Koristi se za pregled trenutnog ili filtriranog stanja sredstava, uključujući količinu, nabavnu vrednost, ispravku vrednosti i neto vrednost.

#### Fixed Asset Changes

Koristi se kada želite pregled svih promena po sredstvu, klasi ili poslovnici, sa datumom, dokumentom i efektom na količinu i vrednost.

#### Fixed Asset Put In Uses

Koristi se za pregled sredstava stavljenih u upotrebu, sa osnovnim identifikacionim i vrednosnim podacima.

#### Fixed Asset Put Out Of Uses

Koristi se za pregled sredstava koja su razdužena, otpisana ili prestala da se koriste.

#### Fixed Asset Depreciations

Koristi se za pregled obračunate amortizacije po sredstvu i periodu.

#### Fixed Asset Write Offs

Koristi se za pregled otpisa i preostalih vrednosti sredstava.

#### Fixed Asset Inventory Drafts

Koristi se kao radni pregled za popis osnovnih sredstava po poslovnici i lokaciji.

#### Fixed Asset Responsibility And Locations

Koristi se za pregled gde se sredstvo nalazi i ko je odgovoran za njega. Podržano je grupisanje po poslovnici, lokaciji, zaposlenom, klasi i samom sredstvu.

### 8.3. Preporučeni postupak rada sa izveštajima

1. Otvorite `Reports`.
2. Izaberite željeni izveštaj.
3. Podesite period i druge filtere.
4. Po potrebi suzite pregled na klasu, sredstvo, lokaciju ili zaposlenog.
5. Ako je izveštaj pregledniji po grupama, podesite `Group by`.
6. Pokrenite pregled i analizirajte rezultat.

## 9. Najčešće situacije za proveru

Ako rad u modulu ne daje očekivan rezultat, proverite sledeće:

1. da li su unesene klase osnovnih sredstava
2. da li postoje lokacije i poslovnice potrebne za zaduženje sredstva
3. da li sredstvo ima pravilno popunjenu karticu
4. da li je izabran odgovarajući tip dokumenta
5. da li su unesene stavke dokumenta za konkretno sredstvo
6. da li je dokument u odgovarajućem statusu za dalju obradu
7. da li su podešena pravila knjiženja ako očekujete prenos u finansije
8. da li je za obračun amortizacije definisana stopa, metod i osnovica
9. da li su filteri na izveštaju previše suženi pa ne vraćaju podatke

## 10. Preporučeni redosled uvođenja modula u rad

Za korisnike koji prvi put uvode modul u upotrebu, preporučeni redosled je:

1. uneti klase osnovnih sredstava
2. uneti lokacije osnovnih sredstava
3. uneti kartice svih osnovnih sredstava
4. podesiti pravila knjiženja
5. preneti početno stanje, ako je potrebno
6. dalje voditi sve promene kroz dokumente osnovnih sredstava
7. redovno koristiti izveštaje za kontrolu stanja, amortizacije i odgovornosti

Na taj način evidencija osnovnih sredstava ostaje usklađena sa operativnim promenama i, po potrebi, sa finansijskim knjigovodstvom.
