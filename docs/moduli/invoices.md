# Korisničko uputstvo za modul Invoices

## 1. Svrha modula

Modul `Invoices` služi za svakodnevni rad sa izlaznim fakturama, ulaznim računima, proizvodima i pratećim podešavanjima. U okviru ovog modula korisnik može da:

- vodi šifarnik proizvoda i pomoćne šifarnike
- evidentira izlazne fakture
- evidentira ulazne račune
- povezuje fakture i račune kada je to potrebno
- podešava način numeracije faktura
- vodi prodajna mesta
- koristi izveštaje za promet, proizvode i PDV

Ovo uputstvo je namenjeno operativnim korisnicima i opisuje rad kroz ekrane i tipične korake, bez tehničkih detalja implementacije.

## 2. Kako je organizovan modul

U praksi se rad u modulu najčešće odvija ovim redosledom:

1. Podesite osnovne šifarnike i pomoćne podatke.
2. Unesite ili ažurirajte proizvode.
3. Kreirajte izlazne fakture ili ulazne račune.
4. Po potrebi povežite dokumente ili pokrenite dodatne akcije.
5. Na kraju proverite rezultate kroz izveštaje.

Ako korisnik nema popunjene osnovne šifarnike, rad na dokumentima će biti otežan jer se više polja bira iz unapred definisanih listi.

## 3. Šifarnici i podešavanja

### 3.1. Proizvodi

Ekran `Products` koristi se za unos robe i usluga koje će se kasnije koristiti na izlaznim fakturama i ulaznim računima.

Kada se koristi:

- kada uvodite novi proizvod ili uslugu
- kada menjate cenu, poresku grupu ili namenu proizvoda
- kada proizvod treba da bude dostupan za fakture, račune ili za oba toka

Osnovni koraci:

1. Otvorite `Products`.
2. Unesite osnovne podatke o proizvodu, kao što su šifra, naziv, tip, kategorija, PDV grupa i jedinica mere.
3. Ako se proizvod koristi u izlaznim fakturama, uključite deo za korišćenje u fakturama i proverite valutu, grupu prihoda, cenu i ostala ponuđena polja.
4. Ako se proizvod koristi u ulaznim računima, uključite deo za korišćenje u računima i proverite valutu, grupu rashoda, cenu i ostala ponuđena polja.
5. Sačuvajte unos.

Očekivani ishod:

- proizvod postaje dostupan za izbor na stavkama fakture i/ili računa, u zavisnosti od toga kako je podešen

Šta proveriti ako unos ne prolazi ili proizvod nije dostupan:

- da su popunjeni osnovni podaci proizvoda
- da je dodeljena odgovarajuća PDV grupa
- da je proizvod uključen za fakture, račune ili oba toka
- da su za uključeni tok popunjena obavezna poslovna polja kao što su valuta i cena

### 3.2. Kategorije proizvoda

Ekran `Product Categories` služi za grupisanje proizvoda.

Kada se koristi:

- kada želite uredniji šifarnik proizvoda
- kada korisnici treba lakše da filtriraju ili pretražuju proizvode

Osnovni koraci:

1. Otvorite `Product Categories`.
2. Dodajte novu kategoriju ili izmenite postojeću.
3. Sačuvajte promenu.
4. Po potrebi tu kategoriju dodelite proizvodima u ekranu `Products`.

Očekivani ishod:

- proizvodi se mogu svrstati u logične grupe radi lakšeg rada i pregleda

### 3.3. PDV grupe proizvoda

Ekran `Product VAT Groups` služi za definisanje poreskih grupa koje se koriste na proizvodima i dokumentima.

Kada se koristi:

- pri početnom podešavanju sistema
- kada dođe do promene poreskih pravila ili interne klasifikacije proizvoda

Osnovni koraci:

1. Otvorite `Product VAT Groups`.
2. Unesite novu PDV grupu ili izmenite postojeću.
3. Sačuvajte promenu.
4. Proverite da li su proizvodi vezani za odgovarajuću grupu.

Očekivani ishod:

- pri izboru proizvoda na stavci dokumenta PDV se preuzima iz odgovarajuće grupe

### 3.4. Prodajna mesta

Ekran `Points of Sale` služi za vođenje prodajnih mesta po poslovnicama.

Kada se koristi:

- kada fakture nastaju preko konkretne poslovnice ili prodajnog mesta
- kada isti korisnik radi sa više lokacija

Osnovni koraci:

1. Otvorite `Points of Sale`.
2. Dodajte novo prodajno mesto.
3. Povežite ga sa odgovarajućom poslovnicom.
4. Sačuvajte unos.

Očekivani ishod:

- prodajno mesto je dostupno za izbor na izlaznim fakturama

### 3.5. Numeracija faktura

Ekran `Invoice Number Format Settings` služi za podešavanje načina formiranja brojeva faktura.

Kada se koristi:

- pre početka rada sa fakturama
- kada firma menja pravila numeracije po tipu dokumenta

Osnovni koraci:

1. Otvorite `Invoice Number Format Settings`.
2. Dodajte ili izmenite podešavanje numeracije.
3. Proverite da li je podešavanje vezano za odgovarajući tip dokumenta.
4. Sačuvajte promenu.

Očekivani ishod:

- nove izlazne fakture dobijaju broj u skladu sa podešenim pravilima

Šta proveriti ako broj nije očekivan:

- da je izabran ispravan tip dokumenta
- da je numeracija podešena pre kreiranja dokumenta
- da korisnik ručno nije menjao broj na dokumentu gde je to dozvoljeno

### 3.6. Pravila knjiženja

Ekran `Accounting Rules` služi za održavanje pravila knjiženja za izlazne fakture i ulazne račune.

Kada se koristi:

- pri početnom podešavanju sistema
- kada računovodstvo menja način knjiženja po dokumentu, proizvodu ili grupi

Napomena za operativne korisnike:

- ovaj ekran najčešće održava napredniji korisnik ili administrator procesa
- preporučljivo je da se pravila menjaju planski, jer utiču na ponašanje dokumenata i izveštaja

### 3.7. Knjiženje faktura i računa u Glavnu knjigu

U modulu faktura odjeljak `Knjiženje` služi za podešavanje pravila po kojima se izlazne fakture i ulazni računi knjiže u Glavnu knjigu.

Ovaj odjeljak je praktično rad sa pravilima knjiženja, ali organizovan tako da korisnik posebno podešava:

- knjiženje izlaznih faktura
- knjiženje ulaznih računa

Pravila se vode po kontnom planu, što znači da korisnik najpre bira kontni plan, a zatim pregleda i uređuje pravila koja važe za taj plan.

Kada se koristi:

- pri početnom podešavanju knjiženja modula faktura
- kada se menja način knjiženja ulaznih računa ili izlaznih faktura
- kada treba preciznije odrediti koje konto se koristi za određenu vrstu prometa
- kada treba razlikovati knjiženje po vrsti dokumenta, partneru, proizvodu ili drugom kriterijumu

#### 3.7.1. Kako je organizovan ekran

Na ekranu knjiženja pravila su odvojena po vrsti dokumenta:

- `Invoices` za izlazne fakture
- `Bills` za ulazne račune

U okviru svake od te dve cjeline pravila su grupisana po tipu knjiženja. U praksi to znači da korisnik podešava zasebna pravila za različite obračunske vrednosti dokumenta, kao što su:

- neto iznos
- PDV
- bruto iznos

Kod pregleda liste pravila korisnik vidi samo popunjena svojstva pravila, što olakšava proveru da li je pravilo opšte ili je vezano za konkretniji slučaj.

#### 3.7.2. Koji podaci ulaze u jedno pravilo knjiženja

Svako pravilo knjiženja može sadržati sledeće grupe podataka:

- instrukciju knjiženja
- uslove vezane za partnera
- uslove vezane za proizvod ili karakteristike proizvoda
- uslove vezane za dokument

U delu instrukcije knjiženja podešavaju se najvažniji elementi:

- tip knjiženja
- strana konta
- konto
- konto vremenskog razgraničenja, kada je primenljivo

Uslovi vezani za partnera mogu razlikovati knjiženje prema podacima kao što su:

- lokacija partnera
- država ili entitet
- tip partnera
- da li je partner PDV obveznik
- da li je povezano lice
- način plaćanja

Uslovi vezani za proizvod mogu se podešavati na dva načina:

- izborom konkretnog proizvoda po nazivu
- izborom po karakteristikama proizvoda

Ako se koristi izbor po karakteristikama, pravilo može zavisiti od:

- tipa proizvoda
- tipa sredstva, kod ulaznih računa
- grupe prihoda ili rashoda

Uslovi vezani za dokument mogu uključivati:

- kategoriju dokumenta
- tip dokumenta

#### 3.7.3. Kako uneti novo pravilo knjiženja

Osnovni koraci:

1. Otvorite odjeljak `Knjiženje`.
2. Izaberite da li radite pravila za izlazne fakture ili ulazne račune.
3. Proverite koji je kontni plan izabran.
4. Dodajte novo pravilo.
5. U delu instrukcije knjiženja izaberite tip knjiženja, stranu konta i konto.
6. Ako pravilo zahteva vremensko razgraničenje, unesite i konto vremenskog razgraničenja.
7. Po potrebi zadajte dodatne uslove za partnera.
8. U delu za proizvod odlučite da li pravilo važi za konkretan proizvod ili za grupu karakteristika.
9. Po potrebi zadajte kategoriju i tip dokumenta.
10. Sačuvajte pravilo.

Očekivani ishod:

- novo pravilo postaje dostupno u izabranom kontnom planu i primenjuje se na odgovarajuće ulazne račune ili izlazne fakture

#### 3.7.4. Kada koristiti opšte, a kada specifično pravilo

U ovom delu posebno je važno razumeti da pravilo može biti:

- opšte, bez mnogo dodatnih uslova
- specifično, vezano za tačno određenu vrstu dokumenta, partnera ili proizvoda

Preporuka za rad:

1. Najpre definišite osnovna opšta pravila za knjiženje.
2. Zatim dodajte specifična pravila samo tamo gde postoji realna poslovna potreba.
3. Ako želite različito knjiženje za određenu kategoriju dokumenta, partnera ili proizvod, unesite to kao dodatni uslov umesto da menjate opšte pravilo.

Na osnovu koda modula vidi se da sistem kod pojedinih vrsta knjiženja ume da daje prednost specifičnijem pravilu za kategoriju dokumenta, a ako takvo pravilo ne postoji, koristi opštije pravilo bez te dodatne odrednice. Zato je važno da se posebna pravila dodaju promišljeno i samo kada zaista treba da imaju prednost nad opštim.

#### 3.7.5. Posebnosti koje treba znati pri unosu pravila

- Konto vremenskog razgraničenja koristi se samo u određenim slučajevima, a nije potreban za sve tipove knjiženja.
- Ako je pravilo vezano za konkretan proizvod, ostale karakteristike proizvoda se ne koriste kao dodatni kriterijum.
- Kod ulaznih računa deo kriterijuma može biti tip sredstva.
- Kod izlaznih faktura deo kriterijuma može biti tip proizvoda.
- Ako je izabrana lokacija partnera koja nije domaća, polje za državu ili entitet ne mora biti relevantno kao u domaćem prometu.

#### 3.7.6. Import, export i održavanje pravila

Na ekranu knjiženja dostupne su i pomoćne radnje za masovniji rad sa pravilima:

- uvoz pravila
- izvoz pravila
- osvežavanje liste
- napredno sortiranje
- brisanje pravila

Ove opcije su korisne kada:

- imate veći broj pravila
- pripremate pravila van aplikacije i potom ih uvozite
- želite proveru ili arhivu postojećih pravila kroz izvoz

Kod uvoza treba posebno proveriti da li nazivi i šifre iz uvoza odgovaraju postojećim podacima u sistemu, kao što su:

- kontni plan
- konto
- kategorija i tip dokumenta
- proizvod
- grupa prihoda ili rashoda
- država ili entitet

Ako bilo koji od tih podataka ne postoji u sistemu, unos pravila može biti odbijen.

#### 3.7.7. Šta proveriti ako knjiženje ne daje očekivan rezultat

Ako knjiženje ulazne ili izlazne fakture nije očekivano, proveriti sledeće:

1. da li je pravilo podešeno za odgovarajući kontni plan
2. da li je pravilo uneseno u odgovarajućoj cjelini, `Invoices` ili `Bills`
3. da li je izabran ispravan tip knjiženja, na primer neto, PDV ili bruto
4. da li je postavljena odgovarajuća strana konta
5. da li je pravilo suviše opšte ili suviše specifično
6. da li su partner, način plaćanja, tip proizvoda ili tip sredstva pravilno zadati kao uslovi
7. da li kategorija dokumenta i tip dokumenta odgovaraju stvarnom dokumentu
8. da li postoji drugo specifičnije pravilo koje ima prednost

Praktična preporuka je da se kod svake izmene pravila proveri jedan konkretan ulazni račun ili izlazna faktura, kako bi se odmah videlo da li je logika knjiženja podešena na željeni način.

## 4. Izlazne fakture

### 4.1. Pregled liste faktura

Ekran `Invoice Pages` služi za pregled, pretragu i otvaranje izlaznih faktura.

Kada se koristi:

- kada tražite ranije unetu fakturu
- kada unosite novu fakturu
- kada proveravate status i sadržaj postojećeg dokumenta

Tipične radnje:

1. Otvorite `Invoice Pages`.
2. Pregledajte listu faktura.
3. Po potrebi koristite dostupne filtere i pretragu.
4. Otvorite postojeći dokument ili pokrenite unos novog.

### 4.2. Unos zaglavlja izlazne fakture

Na pojedinačnom ekranu fakture korisnik unosi osnovne podatke o dokumentu.

Tipični podaci koje treba proveriti:

- datum dokumenta
- datum dospeća
- broj dokumenta
- tip dokumenta
- fiskalni broj, ako je primenljivo
- poslovnica
- prodajno mesto
- partner
- način plaćanja
- valuta i kurs
- datum isporuke ili period od-do
- opis, napomena i drugi dodatni podaci

Osnovni koraci:

1. Otvorite novu ili postojeću izlaznu fakturu.
2. U delu osnovnih podataka unesite datum i rok dospeća.
3. Izaberite tip dokumenta i proverite broj dokumenta.
4. U delu za partnera izaberite poslovnicu, prodajno mesto, partnera i način plaćanja.
5. U delu za valutu proverite valutu, datum kursa i kurs.
6. U delu za robu ili usluge unesite datum isporuke ili period ako je potreban.
7. Po potrebi dopunite opis, napomenu i ostale dodatne podatke.
8. Sačuvajte dokument.

Očekivani ishod:

- zaglavlje fakture je sačuvano i spremno za unos stavki

Šta proveriti ako unos ne prolazi:

- da su popunjena ključna polja kao što su datum, tip dokumenta i partner
- da je izabrana poslovnica i, gde je potrebno, prodajno mesto
- da su podaci o valuti i kursu validni
- da su oba polja perioda usklađena ako koristite raspon od-do

### 4.3. Unos stavki izlazne fakture

Stavke fakture određuju šta se fakturiše i po kojoj ceni.

Osnovni koraci:

1. Na otvorenoj fakturi dodajte novu stavku.
2. Izaberite proizvod iz šifarnika proizvoda za izlazne fakture.
3. Proverite da li su automatski preuzeti naziv, šifra, jedinica mere, PDV i cena.
4. Po potrebi unesite opis stavke.
5. Izaberite način unosa cene:
   - neto cena
   - bruto cena
6. Unesite ili proverite količinu, popust i stopu PDV-a.
7. Proverite obračunate iznose.
8. Sačuvajte stavku.

Očekivani ishod:

- stavka ulazi u zbir dokumenta i učestvuje u obračunu

Šta proveriti ako rezultat nije očekivan:

- da je izabran pravi proizvod za fakture
- da je proizvod povezan sa odgovarajućom PDV grupom
- da je odabran ispravan režim unosa cene, neto ili bruto
- da količina nije ostala na podrazumevanoj vrednosti ako to nije namera

### 4.4. Završna provera fakture

Pre završetka rada proverite:

1. da li su zaglavlje i stavke usklađeni
2. da li partner, poslovnica i prodajno mesto odgovaraju dokumentu
3. da li su ukupni iznosi logični
4. da li je broj dokumenta u skladu sa pravilima numeracije
5. da li su opis i napomena dovoljni za internu evidenciju

## 5. Ulazni računi

### 5.1. Pregled liste računa

Ekran `Bill Pages` služi za pregled i obradu ulaznih računa dobavljača.

Kada se koristi:

- kada evidentirate novi račun dobavljača
- kada naknadno proveravate postojeći račun
- kada treba pripremiti plaćanje ili dodatnu akciju nad računom

Osnovni koraci:

1. Otvorite `Bill Pages`.
2. Pregledajte listu postojećih računa.
3. Po potrebi filtrirajte ili otvorite pojedinačan dokument.
4. Kreirajte novi dokument ako unosite novi račun.

### 5.2. Unos zaglavlja ulaznog računa

Na pojedinačnom ekranu računa korisnik unosi osnovne podatke o ulaznom dokumentu.

Tipični podaci koje treba proveriti:

- datum dokumenta
- datum dospeća
- datum prijema
- tip dokumenta
- broj dokumenta
- fiskalni broj
- poziv na broj plaćanja
- poslovnica
- partner
- način plaćanja
- valuta i kurs
- period od-do
- podaci o uvozu, ako postoje
- opis, napomena i link ka dokumentu

Osnovni koraci:

1. Otvorite novi ili postojeći ulazni račun.
2. Unesite datum, datum dospeća i datum prijema.
3. Izaberite tip dokumenta i broj dokumenta.
4. Po potrebi dopunite fiskalni broj i poziv na broj plaćanja.
5. Izaberite poslovnicu, partnera i način plaćanja.
6. Proverite valutu, datum kursa i kurs.
7. Ako dokument pokriva period, unesite period od-do.
8. Ako je dokument vezan za uvoz, uključite oznaku za uvoznu deklaraciju i unesite broj deklaracije.
9. Po potrebi dopunite opis, napomenu i link ka pratećem dokumentu.
10. Sačuvajte zaglavlje računa.

Očekivani ishod:

- račun je sačuvan i spreman za unos stavki i dodatne akcije

Šta proveriti ako unos ne prolazi:

- da su datum, partner i tip dokumenta uneseni
- da je broj uvozne deklaracije unet ako je uključena oznaka da deklaracija postoji
- da su period od-do ili oba popunjena ili oba prazna
- da je link ka dokumentu ispravno unet ako se koristi

### 5.3. Unos stavki ulaznog računa

Osnovni koraci:

1. Na otvorenom računu dodajte novu stavku.
2. Izaberite proizvod iz šifarnika proizvoda za ulazne račune.
3. Po potrebi povežite stavku sa osnovnim sredstvom ako se koristi ta mogućnost.
4. Proverite jedinicu mere.
5. Unesite ili proverite količinu, cenu, popust i stopu PDV-a.
6. Po potrebi unesite poseban iznos PDV-a.
7. Proverite neto, PDV i bruto iznos.
8. Sačuvajte stavku.

Očekivani ishod:

- stavka ulaznog računa je uključena u zbir dokumenta

Šta proveriti ako obračun nije očekivan:

- da je odabran ispravan proizvod za ulazne račune
- da je cena preuzeta ili korigovana po potrebi
- da stopa PDV-a odgovara stvarnom računu dobavljača
- da eventualni posebni iznos PDV-a nije ostao pogrešno unet

### 5.4. Dodatne akcije nad računom

Na ulaznim računima mogu biti dostupne dodatne radnje iz alatne trake ili menija.

Najvažnije radnje koje treba očekivati:

- pregled ili povezivanje sa nalogom za plaćanje
- kreiranje naloga za plaćanje
- pokretanje prenosa PDV-a na izlaznu fakturu, kada je to podržano i kada su uslovi ispunjeni

Pre pokretanja dodatnih akcija proverite:

- da je račun sačuvan
- da su zaglavlje i stavke kompletirani
- da dokument nije u režimu koji onemogućava traženu akciju

## 6. Povezivanje faktura i računa

Ekran `Invoice page bill links` služi za povezivanje izlaznih faktura i ulaznih računa kada poslovni proces to zahteva.

Kada se koristi:

- kada želite da održite vezu između dva dokumenta
- kada je potrebno pratiti prenos, pokriće ili zavisnost između fakture i računa

Osnovni koraci:

1. Otvorite `Invoice page bill links`.
2. Izaberite izlaznu fakturu.
3. Izaberite ulazni račun.
4. Sačuvajte vezu.

Očekivani ishod:

- dokumenti su međusobno povezani i mogu se pratiti kroz proces

Šta proveriti ako povezivanje nije moguće:

- da oba dokumenta postoje i da su sačuvana
- da korisnik bira ispravne dokumente iz odgovarajućih listi
- da prethodna obrada dokumenta nije ostavila stanje koje sprečava novo povezivanje

## 7. Izveštaji

Ekran `Reports` objedinjuje izveštaje za izlazne fakture, ulazne račune i kombinovane PDV preglede.

Pre pokretanja izveštaja preporučuje se da proverite filtere kao što su:

- period
- poslovnica
- partner
- broj dokumenta
- valuta
- način plaćanja
- proizvod
- kategorija dokumenta

### 7.1. Izveštaji za izlazne fakture

Dostupne su sledeće celine izveštavanja:

- kartica izlaznih faktura
- promet po proizvodima na izlaznim fakturama
- analitički pregled proizvoda na izlaznim fakturama

Kada se koriste:

- za kontrolu prometa prema partnerima
- za pregled prometa po proizvodima
- za detaljniji analitički uvid po dokumentima i grupisanjima

### 7.2. Izveštaji za ulazne račune

Dostupne su sledeće celine:

- kartica ulaznih računa
- promet po proizvodima na ulaznim računima
- analitički pregled proizvoda na ulaznim računima

Kada se koriste:

- za praćenje ulaznih troškova i nabavke
- za proveru količina i iznosa po proizvodima
- za pregled dobavljača i poslovnica kroz grupisanje

### 7.3. Kombinovani i PDV izveštaji

U kombinovanim izveštajima dostupni su pregledi kao što su:

- mesečni PDV pregled
- mesečna potrošnja bez PDV-a
- mesečna PDV analitika

Kada se koriste:

- za zbirnu poresku kontrolu
- za mesečne preglede ulaza i izlaza
- za analitičku proveru po periodu i lokaciji

Osnovni koraci za rad sa izveštajima:

1. Otvorite `Reports`.
2. Izaberite grupu izveštaja.
3. Podesite filtere.
4. Pokrenite pregled.
5. Po potrebi menjajte grupisanje i ponovite pregled.

Očekivani ishod:

- dobijate pregled podataka iz dokumentacije modula `Invoices` za izabrane kriterijume

## 8. Najčešće situacije koje treba proveriti

Ako korisnik ne može da završi unos ili dobija neočekivan rezultat, najpre proveriti sledeće:

### 8.1. Dokument se ne može sačuvati

Proveriti:

- da su popunjena ključna polja zaglavlja
- da partner i poslovnica postoje i da su ispravno izabrani
- da je tip dokumenta odgovarajući
- da su polja perioda usklađena

### 8.2. Proizvod nije dostupan na stavci

Proveriti:

- da proizvod postoji u šifarniku
- da je uključen za izlazne fakture ili ulazne račune, zavisno od toka
- da ima dodeljenu jedinicu mere i PDV grupu

### 8.3. Iznosi ili PDV nisu očekivani

Proveriti:

- da je izabrana odgovarajuća PDV grupa proizvoda
- da je stopa PDV-a na stavci ispravna
- da je način unosa cene ispravan
- da popust, količina ili poseban iznos PDV-a nisu pogrešno uneti

### 8.4. Broj fakture nije očekivan

Proveriti:

- podešavanja u `Invoice Number Format Settings`
- tip dokumenta na samoj fakturi
- da li je broj ručno promenjen tamo gde je to dozvoljeno

### 8.5. Dodatna akcija nije dostupna

Proveriti:

- da li je dokument prethodno sačuvan
- da li su stavke unete
- da li je dokument u odgovarajućem režimu rada za tu akciju

## 9. Preporučeni redosled rada za nove korisnike

Ako prvi put radite u modulu, preporučen redosled je:

1. proverite PDV grupe, kategorije proizvoda i prodajna mesta
2. unesite ili ažurirajte proizvode
3. proverite numeraciju faktura
4. unesite jednu probnu izlaznu fakturu
5. unesite jedan probni ulazni račun
6. proverite podatke kroz izveštaje

Na taj način korisnik najbrže povezuje šifarnike, dokumenta i izveštaje u jednu celinu.
