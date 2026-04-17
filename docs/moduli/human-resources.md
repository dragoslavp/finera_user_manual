# Korisničko uputstvo za modul Human Resources

## 1. Svrha modula

Modul `Human Resources` služi za vođenje zaposlenih, ugovora, obračuna plata, evidencije radnog vremena i pratećih izveštaja. Pored operativnog rada, modul sadrži i važan deo za podešavanja obračuna.

U ovom modulu korisnik najčešće radi sledeće:

- vodi zaposlene i njihove lične podatke
- vodi ugovore zaposlenih
- evidentira radno vreme
- održava elemente obračuna i šablone plata
- vodi konstante obračuna
- radi obračun plata
- podešava knjiženje plata i pravila isplata
- koristi personalne i obračunske izveštaje

## 2. Kako je organizovan modul

Modul je praktično podeljen na dve velike celine:

- operativni rad
- podešavanja modula

Operativni rad obuhvata:

- `Employees`
- `Employees' Contracts`
- `Time Logs`
- `Payroll Pages`
- `Reports`

Podešavanja modula obuhvataju:

- `Education Degrees`
- `Employee Contract Types`
- `Tax Exempt Types`
- `Payroll Elements`
- `Payroll Templates`
- `Employees' Payroll Elements`
- `Payroll Constants`
- `Payroll Accountings`

Preporučeni redosled rada je:

1. prvo podesiti šifarnike i pravila obračuna
2. zatim uneti zaposlene i ugovore
3. po potrebi uneti radne evidencije
4. na kraju raditi obračun plata i izveštaje

## 3. Zaposleni

### 3.1. Employees

Ekran `Employees` služi za vođenje evidencije zaposlenih. Podaci se vode kroz istoriju, što znači da se mogu pratiti promene kroz vreme.

Kada se koristi:

- kada se uvodi novi zaposleni
- kada se menjaju lični ili kontakt podaci zaposlenog
- kada se ažuriraju podaci bitni za obračun plate

Na ovom ekranu korisnik vodi:

- osnovne lične podatke
- identifikacione podatke
- kontakt i adresu
- podatke za obračun plate
- bankovne račune zaposlenog

Osnovni koraci:

1. Otvorite `Employees`.
2. Dodajte novog zaposlenog.
3. Po potrebi povežite postojeće lice iz partnera ako je već ranije uneseno.
4. Unesite osnovne lične podatke.
5. Unesite adresu i kontakt podatke.
6. U delu za obračun plate unesite obrazovanje, zanimanje i druge obračunske podatke.
7. Po potrebi unesite prethodni radni staž i penzijski staž.
8. Sačuvajte zapis.

Očekivani ishod:

- zaposleni postaje dostupan za ugovore, evidenciju vremena i obračun plata

Šta proveriti ako unos ne prolazi:

- da su obavezna lična polja popunjena
- da su lookup podaci poput države, opštine i valute već uneseni u sistem
- da su podaci za domaće lice usklađeni sa internim pravilima firme

## 4. Ugovori zaposlenih

### 4.1. Employees' Contracts

Ekran `Employees' Contracts` služi za vođenje ugovora zaposlenih, takođe kroz istoriju promena.

Kada se koristi:

- kada zaposleni dobija novi ugovor
- kada se menja tip ugovora, plata ili radno vreme
- kada se ažuriraju parametri potrebni za obračun

Na ugovoru se vode podaci kao što su:

- tip ugovora
- poslovnica
- stručna sprema i radno mesto
- datum i mesto potpisivanja
- osnovna plata
- tip isplate platne liste
- koeficijent poreskog oslobođenja
- smena i vrsta rada
- radni sati i radni dani
- beneficije i druga prava

Osnovni koraci:

1. Otvorite `Employees' Contracts`.
2. Dodajte novi ugovor za zaposlenog.
3. Unesite osnovne podatke o ugovoru.
4. U delu `Payroll data` unesite obračunske parametre.
5. Proverite radno vreme, koeficijente i dodatke.
6. Sačuvajte ugovor.

Očekivani ishod:

- zaposleni dobija aktivan ugovor koji može učestvovati u obračunu i radnim evidencijama

## 5. Evidencija radnog vremena

### 5.1. Time Logs

Ekran `Time Logs` služi za vođenje perioda evidencije rada.

Kada se koristi:

- kada pripremate obračun plate na osnovu evidencije rada
- kada vodite radne dane, sate i vrste prihoda po ugovorima

Na listi evidencija korisnik vodi:

- broj evidencije
- period od-do
- napomenu

Osnovni koraci:

1. Otvorite `Time Logs`.
2. Dodajte novu evidenciju rada.
3. Unesite period od-do.
4. Po potrebi unesite napomenu.
5. Sačuvajte zapis.

### 5.2. Rad sa jednom evidencijom vremena

Na pojedinačnoj evidenciji rada korisnik radi u tri celine:

- zaglavlje evidencije
- izbor ugovora
- unos stavki po danima i vrstama prihoda

Korisnik može:

- uzeti sve aktivne ugovore
- odabrati samo određene ugovore
- filtrirati po kategoriji ili tipu ugovora
- birati da li ulaze vikendi i praznici

Za svaku stavku rada mogu se unositi:

- datum
- vrsta prihoda
- trajanje
- početak i kraj rada
- napomena

Očekivani ishod:

- evidencija rada je spremna za korišćenje u obračunu redovne plate

## 6. Obračun plata

### 6.1. Payroll Pages

Ekran `Payroll Pages` služi za vođenje obračuna plata.

Kada se koristi:

- za redovan obračun plate
- za pregled ugovora uključenih u obračun
- za generisanje naloga za plaćanje i izvoz platnih listi

Na zaglavlju obračuna korisnik vodi:

- datum obračuna
- tip dokumenta
- period od-do
- vezu sa radnom evidencijom kod redovne plate
- očekivani datum isplate
- opis

Kod redovnog obračuna, radna evidencija može biti obavezna, u zavisnosti od vrste dokumenta.

Osnovni koraci:

1. Otvorite `Payroll Pages`.
2. Dodajte novi obračun.
3. Izaberite tip dokumenta.
4. Unesite period obračuna.
5. Ako je potreban redovan obračun, izaberite `Time Log`.
6. Unesite očekivani datum isplate i opis.
7. Sačuvajte obračun.

### 6.2. Obračun po ugovorima

Na pojedinačnom obračunu korisnik vidi listu ugovora i zbirne vrednosti obračuna po zaposlenom ili ugovoru.

Prikazuju se podaci kao što su:

- bruto prihod
- doprinosi
- porez
- odbici
- neto prihod
- neoporezivi iznosi
- iznos za isplatu
- kontrola obračuna

Na stranici su dostupne važne akcije:

- `Calculate`
- povezivanje sa finansijskom stranicom
- kreiranje naloga za plaćanje
- pregled naloga za plaćanje
- izvoz platnih listi

### 6.3. Calculate

Akcija `Calculate` služi za obračun svih ugovora uključenih u platnu listu.

Kada se koristi:

- nakon unosa ili izmene zaglavlja obračuna
- nakon izmene šablona, elemenata ili radne evidencije

Očekivani ishod:

- sistem izračuna bruto, doprinose, porez, odbitke i neto iznose za sve ugovore na obračunu

### 6.4. Nalog za plaćanje i platne liste

Iz obračuna je moguće:

- kreirati nalog za plaćanje
- otvoriti postojeći nalog za plaćanje
- izvesti platne liste

Kod kreiranja naloga za plaćanje korisnik unosi:

- datum isplate
- blagajnički ili bankovni račun

## 7. Izveštaji

### 7.1. Reports

Modul sadrži dve osnovne grupe izveštaja:

- obračunske izveštaje
- personalne izveštaje

Na osnovu koda modula podržani su izveštaji kao što su:

- analitike obračuna
- proširene analitike obračuna
- analitike po zaposlenom
- poreske analitike
- rekapitulacije doprinosa
- rekapitulacije prihoda
- broj zaposlenih po obrazovanju i vrsti ugovora
- starosna struktura zaposlenih

Kada se koriste:

- za proveru obračuna
- za izveštavanje prema internoj evidenciji
- za statistiku zaposlenih i personalne preglede

## 8. Podešavanja modula Human Resources

Ovo je važan deo modula. Bez pravilno podešenih šifarnika i pravila obračuna, obračun plata neće dati očekivane rezultate.

### 8.1. Education Degrees

Ekran `Education Degrees` služi za vođenje stepena obrazovanja.

Kada se koristi:

- pri unosu zaposlenih
- u personalnim izveštajima

Očekivani ishod:

- stepen obrazovanja postaje dostupan na kartici zaposlenog

### 8.2. Employee Contract Types

Ekran `Employee Contract Types` služi za vođenje vrsta ugovora zaposlenih.

Kada se koristi:

- pri unosu ugovora
- u filtriranju i izveštajima
- u šablonima obračuna

Očekivani ishod:

- tipovi ugovora postaju dostupni na ugovorima i šablonima

### 8.3. Tax Exempt Types

Ekran `Tax Exempt Types` služi za vođenje vrsta poreskih oslobođenja.

Kada se koristi:

- pri definisanju elemenata obračuna koji su neoporezivi
- kod posebnih vrsta primanja

Očekivani ishod:

- poreska oslobođenja postaju dostupna na elementima obračuna

### 8.4. Payroll Elements

Ekran `Payroll Elements` služi za definisanje svih elemenata obračuna plate.

To uključuje:

- prihode
- poreze
- doprinose
- odbitke
- neoporezive stavke

Kada se koristi:

- pri početnom podešavanju obračuna
- kada se menjaju pravila obračuna plata
- kada se uvode nova primanja, odbici ili poreske stavke

Za svaki element može se definisati:

- vrsta elementa
- osnovica i pravila obračuna
- poreska i doprinosna svojstva
- prioritet odbitka
- stopa ili fiksna vrednost
- dodatni parametri kao što su poreski dani, umanjenja ili posebna raspodela

Praktična preporuka:

- ovaj ekran treba da održava napredniji korisnik koji razume pravila obračuna plate

Na ovom ekranu je najvažnije razumeti da se ponašanje i dostupna polja menjaju zavisno od `Payroll Element Type`. Svaki tip elementa utiče na obračun na drugačiji način.

#### 8.4.1. Zajednička polja za sve tipove

Bez obzira na tip elementa, za svaki `Payroll Element` vode se osnovni podaci:

- `Type`
- `Name`
- `Valid from`
- `Valid to`
- `Inactive`

Uticaj na obračun:

- `Type` određuje logiku elementa i koja dodatna polja će biti dostupna
- `Name` služi za izbor elementa u šablonima, individualnim dodelama i pravilima knjiženja
- period važenja određuje od kada se element koristi u obračunu
- `Inactive` sprečava upotrebu elementa u novim obračunima, ali ne briše istoriju

#### 8.4.2. Tip `Income`

Ovaj tip se koristi za elemente koji predstavljaju prihod ili osnovu prihoda u obračunu plate.

Polja koja se mogu podesiti:

- `Income type`
- `Tax return type`
- `Adjusting coefficient`
- `Previous employment base`
- `Deduction permission`
- `Tax/Contribution adjusting coefficient`
- `Tax code`
- `Defined absolutely`
- `Sick leave days`
- `Base for food allowance`
- `Tax free distribution`
- `Include in total duration`
- `Non-monetary benefit`

Objašnjenje i uticaj na obračun:

- `Income type`
  Određuje poslovnu vrstu prihoda. Taj podatak se koristi u evidenciji rada, šablonima obračuna i logici računanja prihoda.

- `Tax return type`
  Određuje kako se prihod klasifikuje u poreskom izveštavanju.

- `Adjusting coefficient`
  Menja vrednost ili osnovicu prihoda kroz koeficijent. Promena ovog polja utiče na visinu obračunatog prihoda.

- `Previous employment base`
  Određuje da li prethodni radni staž zaposlenog utiče na obračun tog prihoda.

- `Deduction permission`
  Određuje da li se na ovaj prihod mogu primenjivati odbici. Ako nije uključeno, odbici se neće raspoređivati na taj prihod kao na ostale prihode.

- `Tax/Contribution adjusting coefficient`
  Menja osnovicu za poreze i doprinose vezane za taj prihod.

- `Tax code`
  Koristi se za poresku klasifikaciju i dalje izveštavanje.

- `Defined absolutely`
  Određuje da li je vrednost prihoda unapred definisana kao apsolutna vrednost, umesto da se računa preko sati, dana ili drugih količina.

- `Sick leave days`
  Koristi se kod prihoda koji se odnose na bolovanje. Menja logiku obračuna tog prihoda u zavisnosti od broja dana.

- `Base for food allowance`
  Određuje da li taj prihod učestvuje u osnovici za topli obrok ili sličnu naknadu.

- `Tax free distribution`
  Određuje da li prihod učestvuje u raspodeli neoporezivog dela.

- `Include in total duration`
  Određuje da li se prihod uzima u obzir u ukupnom fondu rada ili trajanja angažmana.

- `Non-monetary benefit`
  Označava da se prihod tretira kao nenovčana korist, što može promeniti način obračuna i prikaza.

Praktičan rezultat u obračunu:

- prihod ulazi u bruto stranu obračuna
- može se vezati za sate, dane ili druge količine iz evidencije rada
- na njega se dalje mogu primenjivati porezi, doprinosi i odbici, zavisno od podešenja

#### 8.4.3. Tip `Tax`

Ovaj tip se koristi za poreske elemente obračuna.

Polja koja se mogu podesiti:

- `Calculation base`
- `Paid by employer`
- `Cost recognised rate`
- `Rate` ili `Value`
- `Tax free base`
- `Tax free value`
- `Tax day factor`

Objašnjenje i uticaj na obračun:

- `Calculation base`
  Određuje od koje osnovice se računa porez. Ovo je jedno od ključnih polja za tačnost obračuna.

- `Paid by employer`
  Određuje da li porez ide na teret poslodavca. To menja kako porez utiče na neto zaposlenog i ukupni trošak poslodavca.

- `Cost recognised rate`
  Određuje koliki deo osnovice se priznaje kao trošak pre obračuna poreza.

- `Rate`
  Koristi se kada se porez računa procentualno.

- `Value`
  Koristi se kada se porez obračunava kao fiksna vrednost.

- `Tax free base`
  Određuje osnovicu neoporezivog dela.

- `Tax free value`
  Određuje iznos neoporezivog dela koji smanjuje poreski teret.

- `Tax day factor`
  Koristi se kada obračun poreza zavisi od dana ili dnevnog faktora.

Praktičan rezultat u obračunu:

- porez umanjuje neto primanje ili se vodi kao teret poslodavca, zavisno od podešenja
- utiče na poreske analitike, rekapitulacije i platne liste

#### 8.4.4. Tip `Contribution`

Ovaj tip se koristi za doprinose.

Polja koja se mogu podesiti:

- `Contribution type`
- `Calculation base`
- `Paid by employer`
- `Cost recognised rate`
- `Rate` ili `Value`
- `Tax free base`
- `Tax free value`

Objašnjenje i uticaj na obračun:

- `Contribution type`
  Određuje kojoj vrsti doprinosa element pripada.

- `Calculation base`
  Određuje osnovicu za obračun doprinosa.

- `Paid by employer`
  Razdvaja doprinose koje snosi poslodavac od onih koji terete zaposlenog.

- `Cost recognised rate`
  Menja način priznavanja osnovice kod posebnih obračunskih slučajeva.

- `Rate`
  Koristi se za procentualni obračun doprinosa.

- `Value`
  Koristi se za fiksni obračun doprinosa.

- `Tax free base` i `Tax free value`
  Koriste se kada deo osnovice ne ulazi u obračun doprinosa.

Praktičan rezultat u obračunu:

- doprinosi utiču na bruto-neto računicu
- mogu povećati trošak poslodavca ili smanjiti iznos zaposlenog
- ulaze u izveštaje o doprinosima i zakonske rekapitulacije

#### 8.4.5. Tip `Deduction`

Ovaj tip se koristi za odbitke od plate.

Polja koja se mogu podesiti:

- `Priority`
- `Rate`
- `Tax reduction rate`
- `Contribution reduction rate`

Objašnjenje i uticaj na obračun:

- `Priority`
  Određuje redosled primene odbitaka. Važno je kada postoji više odbitaka, jer redosled može promeniti konačan rezultat.

- `Rate`
  Određuje procenat odbitka.

- `Tax reduction rate`
  Određuje koliko odbitak utiče na umanjenje poreza ili poreske osnovice.

- `Contribution reduction rate`
  Određuje koliko odbitak utiče na doprinosnu osnovicu ili doprinos.

Praktičan rezultat u obračunu:

- odbici smanjuju iznos za isplatu ili menjaju osnovice za dalji obračun
- posebno su važni kod kredita, administrativnih zabrana i drugih obustava

#### 8.4.6. Tip `Tax Exempt`

Ovaj tip se koristi za neoporezive elemente.

Polja koja se mogu podesiti:

- `Type`
- `Tax / Contribution`

Objašnjenje i uticaj na obračun:

- `Type`
  Određuje vrstu poreskog oslobođenja iz šifarnika `Tax Exempt Types`.

- `Tax / Contribution`
  Određuje na koji poreski ili doprinosni element se oslobođenje odnosi.

Praktičan rezultat u obračunu:

- neoporezivi elementi smanjuju deo osnovice ili iznosa koji bi inače bio predmet poreza ili doprinosa
- koriste se kod posebnih vrsta primanja i zakonskih oslobođenja

#### 8.4.7. Kako birati između `Rate` i `Value`

Kod poreza i doprinosa sistem podržava dva pristupa:

- obračun preko polja `Rate`
- obračun preko polja `Value`

Praktično pravilo:

- koristite `Rate` kada se element računa kao procenat osnovice
- koristite `Value` kada element ima unapred zadat iznos

Ta dva pristupa ne treba mešati bez jasnog razloga, jer menjaju logiku obračuna.

#### 8.4.8. Kako `Payroll Elements` utiču dalje na obračun

`Payroll Elements` sami ne rade obračun dok nisu uključeni u ostatak modula. Njihov puni efekat nastaje tek kada se povežu sa:

- `Payroll Templates`
- `Employees' Payroll Elements`
- `Payroll Constants`
- `Payroll Accountings`
- `Time Logs`
- `Payroll Pages`

To praktično znači:

- element definiše pravilo obračuna
- šablon određuje kada se element koristi
- individualni elementi zaposlenog dodaju izuzetke i posebne slučajeve
- konstante daju važeće vrednosti i stope za određeni period
- evidencija rada daje sate, dane ili trajanje
- obračun plate sve sabira u konačan rezultat

Zbog toga se promena i na jednom polju `Payroll Element` često vidi tek kada se ponovo izračuna konkretan obračun plate.

### 8.5. Payroll Templates

Ekran `Payroll Templates` služi za definisanje šablona obračuna.

Šablon povezuje:

- tip ugovora
- tip dokumenta obračuna
- teritorijalni kontekst, ako postoji
- listu prihoda
- listu poreza i doprinosa

Kada se koristi:

- kada želite standardizovan obračun po vrsti ugovora ili vrsti zaposlenja
- kada se isti raspored elemenata koristi više puta

U šablonu se može:

- izabrati više prihoda
- odrediti redosled prioriteta
- definisati na koje prihode se primenjuju određeni porezi i doprinosi

Očekivani ishod:

- obračun plate koristi unapred definisanu logiku, bez ručnog sastavljanja svakog elementa

### 8.6. Employees' Payroll Elements

Ekran `Employees' Payroll Elements` služi za dodelu individualnih elemenata obračuna zaposlenima.

Kada se koristi:

- kada konkretan zaposleni ima poseban prihod
- kada ima individualni odbitak, kredit ili neoporezivu stavku
- kada element važi samo za jednog zaposlenog ili određeni period

Ovde se mogu voditi:

- dodatni prihodi
- odbici
- neoporezive stavke
- period važenja
- iznos, stopa, broj rata i početno stanje, gde je primenljivo

Očekivani ishod:

- pojedinačni elementi ulaze u obračun konkretnog zaposlenog

### 8.7. Payroll Constants

Ekran `Payroll Constants` služi za vođenje konstanti obračuna.

Kada se koristi:

- kada se menjaju stope, koeficijenti ili druge vrednosti koje zavise od perioda
- kada postoje različite vrednosti po državi, entitetu ili regionu

Za svaku konstantu vodi se:

- vrsta konstante
- teritorijalni kontekst
- datum važenja od
- datum važenja do
- vrednost

Očekivani ishod:

- obračun koristi odgovarajuću vrednost konstante za dati period

### 8.8. Payroll Accountings

Ekran `Payroll Accountings` služi za podešavanje pravila knjiženja i raspodele isplata za elemente obračuna plate.

To je ključni deo podešavanja modula, jer određuje:

- na koja konta se knjiže elementi obračuna
- kako se formiraju nalozi za plaćanje
- kome se isplata raspoređuje

Za svako pravilo korisnik može definisati:

- element obračuna
- šablon, region zaposlenog ili element prihoda kao kriterijum
- tip naloga za plaćanje
- poziv na broj
- budžetske podatke kada su potrebni
- konto duguje
- konto potražuje
- jednu ili više partija isplate sa procentualnom raspodelom

Kada se koristi:

- pri početnom podešavanju knjiženja plata
- kada se menjaju konta ili pravila isplate
- kada se menjaju primaoci određenih uplata

Važna preporuka:

- zbir raspodele po partijama treba da bude 100%

## 9. Šta prvo podesiti pre početka rada

Ako modul postavljate od početka, preporučen redosled je:

1. `Education Degrees`
2. `Employee Contract Types`
3. `Tax Exempt Types`
4. `Payroll Elements`
5. `Payroll Templates`
6. `Payroll Constants`
7. `Payroll Accountings`
8. `Employees`
9. `Employees' Contracts`
10. `Employees' Payroll Elements`
11. `Time Logs`
12. `Payroll Pages`

## 10. Najčešće situacije koje treba proveriti

### 10.1. Zaposleni nije dostupan u obračunu

Proveriti:

- da li postoji aktivan ugovor
- da li je ugovor unet u odgovarajućem periodu

### 10.2. Obračun ne daje očekivane vrednosti

Proveriti:

- elemente obračuna
- šablon obračuna
- individualne elemente zaposlenog
- konstante obračuna

### 10.3. Radna evidencija ne ulazi u obračun

Proveriti:

- da li je `Time Log` povezan sa obračunom
- da li su ugovori i stavke rada sačuvani
- da li period obračuna odgovara periodu evidencije

### 10.4. Nalog za plaćanje ili knjiženje nije očekivano

Proveriti:

- `Payroll Accountings`
- raspodelu po partijama
- izabrane kontne račune
- tip naloga za plaćanje i budžetske podatke

## 11. Preporuka za rad

- najpre zaključajte podešavanja obračuna, pa tek onda krenite sa operativnim unosom
- izmene na elementima obračuna, šablonima i konstantama radite planski
- posle svake veće izmene proverite jedan probni obračun plate

Na taj način modul `Human Resources` ostaje pouzdan za svakodnevni rad, a obračun plata konzistentan i proverljiv.
