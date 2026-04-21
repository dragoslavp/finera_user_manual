icon: fontawesome/solid/coins

# Korisničko uputstvo za modul Cash Accounts

## 1. Pregled modula

Modul `Cash Accounts` služi za vođenje prometa po blagajnama i bankovnim računima, unos i obradu bankovnih izvoda, povezivanje izvoda sa otvorenim stavkama iz Glavne knjige, kao i za kreiranje i obradu platnih naloga.

U praksi se modul koristi za sledeće poslovne tokove:

1. vođenje dnevnika prometa po novčanim računima
2. preuzimanje i pregled bankovnih izvoda
3. usklađivanje stavki izvoda sa finansijskim stavkama
4. unos standardnih knjiženja po blagajni i banci
5. kreiranje i obradu platnih naloga
6. pregled izveštaja o prometu i stanju

## 2. Glavne celine modula

Modul je podeljen na sledeće glavne celine:

1. `Cash Account Pages`
2. `Bank Statements`
3. `Payment Orders`
4. `Bank Statement Groupings`
5. `Reports`

U ovom uputstvu su `Dnevnik`, `Bankovni izvodi` i `Platni nalozi` obrađeni kao posebna poglavlja, jer su to glavni operativni tokovi rada.

## 3. Preduslovi za rad

Pre redovnog korišćenja modula poželjno je da budu podešeni:

1. novčani računi i njihove valute
2. poslovnice
3. banke i bankovni računi
4. dnevnik za rad u modulu
5. tipovi dokumenata za početno stanje, izvod i standardna knjiženja
6. konta i partneri, ako će se raditi usklađivanje sa Glavnom knjigom

Bez ovih podataka neke forme će se otvoriti, ali unos neće moći da se završi.

## 4. Dnevnik finansijskih računa

Odeljak `Cash Account Pages` je centralno mesto za rad sa dnevnikom blagajne i banke. Ovde se otvaraju i obrađuju dokumenti nad novčanim računima.

Na listi se vide podaci kao što su:

1. status dokumenta
2. broj dokumenta
3. broj finansijskog dokumenta
4. datum
5. tip dokumenta
6. poslovnica
7. banka
8. novčani račun
9. broj bankovnog izvoda, kada postoji
10. opis i revizija

### 4.1. Vrste dokumenata u dnevniku

Na osnovu koda modul podržava tri osnovne vrste dnevničkih dokumenata:

1. `Initial State`
2. `Bank Statement Reconciliation`
3. `Standard Entry`

### 4.2. Početno stanje

Početno stanje se koristi kada se uvodi početno stanje blagajne ili bankovnog računa.

Pri otvaranju dokumenta korisnik bira:

1. način prenosa početnog stanja
2. prethodni dnevnik, ako se stanje prenosi iz ranijeg dnevnika

### Kada se koristi

1. kod početka rada u sistemu
2. pri otvaranju novog obračunskog perioda
3. kada treba preneti stanje iz prethodnog dnevnika

### Preporučeni postupak

1. Otvorite `Cash Account Pages`.
2. Dodajte novi dokument.
3. Izaberite tip dokumenta za početno stanje.
4. Unesite datum.
5. Izaberite način kreiranja početnog stanja.
6. Ako se stanje prenosi iz prethodnog dnevnika, izaberite odgovarajući dnevnik.
7. Sačuvajte dokument.
8. Unesite ili proverite stavke.
9. Aktivirajte dokument.

### Šta proveriti ako unos ne prolazi

1. da li je izabran tip dokumenta za početno stanje
2. da li je unet datum
3. da li je izabran prethodni dnevnik kada je to potrebno

### 4.3. Usklađivanje sa bankovnim izvodom

Ova vrsta dokumenta služi za povezivanje bankovnog izvoda sa stavkama iz Glavne knjige i za knjiženje kretanja na bankovnom računu.

Kod otvaranja dokumenta korisnik bira:

1. poslovnicu
2. banku
3. račun
4. bankovni izvod

Važno je da se za ovu vrstu dokumenta bira samo izvod koji još nije usklađen, jer model koristi izbor `LookupUnreconciled`.

### Preporučeni postupak

1. Otvorite `Cash Account Pages`.
2. Dodajte novi dokument.
3. Izaberite tip dokumenta za usklađivanje izvoda.
4. Izaberite poslovnicu, banku i račun.
5. Izaberite odgovarajući bankovni izvod.
6. Sačuvajte dokument.
7. Otvorite dokument i radite usklađivanje po stavkama izvoda.
8. Kada je usklađivanje završeno, objavite dokument.

### 4.4. Standardno knjiženje

`Standard Entry` se koristi za ručni unos knjiženja po blagajni ili banci kada unos nije direktno vezan za bankovni izvod.

Kod otvaranja dokumenta korisnik bira:

1. poslovnicu
2. tip novčanog računa
3. banku, ako je tip računa banka
4. račun

### Kada se koristi

1. za blagajničke uplate i isplate
2. za ručna knjiženja po bankovnom računu
3. za unos prometa koji ne dolazi kroz uvoz bankovnog izvoda

### Preporučeni postupak

1. Otvorite `Cash Account Pages`.
2. Dodajte novi dokument.
3. Izaberite tip dokumenta za standardno knjiženje.
4. Unesite poslovnicu i tip računa.
5. Po potrebi izaberite banku.
6. Izaberite račun.
7. Sačuvajte dokument.
8. Unesite stavke knjiženja.
9. Objavite dokument.

### 4.5. Rad na pojedinačnom dokumentu

Na dokumentu se vide:

1. zaglavlje dokumenta
2. stavke dokumenta
3. kod usklađivanja izvoda, lista stavki izvoda
4. pregled zbirnog stanja po računu

Zavisno od vrste dokumenta, na alatnoj traci su dostupne akcije:

1. `Activate`
2. `Publish`
3. `Revise`
4. `Delete`
5. veza prema finansijskom dokumentu
6. `Synchronize Page, Items and Entries with Bank Statement`

### 4.6. Sinhronizacija sa bankovnim izvodom

Kod dokumenta usklađivanja postoji posebna akcija za sinhronizaciju dokumenta sa izvodom.

Ona služi da se:

1. preuzmu nove stavke sa izvoda na dokument
2. ažuriraju iznosi na postojećim stavkama
3. uklone stavke koje više ne postoje na izvodu

Praktično, ako je izvod izmenjen nakon otvaranja dokumenta, ova akcija osvežava vezu između dokumenta i izvoda.

### Šta proveriti ako rezultat nije očekivan

1. da li je dokument povezan sa odgovarajućim izvodom
2. da li je izvod menjan nakon prvog povezivanja
3. da li su neke ručno unesene stavke vezane za izbrisane stavke izvoda

### 4.7. Stavke dnevnika

Na stavkama dokumenta unose se ili povezuju podaci kao što su:

1. poslovnica
2. tip novčanog računa
3. banka
4. račun
5. konto
6. partner
7. oznake
8. opis
9. dugovna i potražna vrednost
10. valuta i kurs
11. veza zatvaranja

Ako je uključena strana valuta, sistem može da postavlja kurs i preračunava vrednosti.

## 5. Bankovni izvodi

Odeljak `Bank Statements` služi za unos, pregled i uvoz izvoda banke, zajedno sa pojedinačnim stavkama izvoda.

Na listi izvoda se vide:

1. poslovnica
2. banka
3. račun
4. valuta
5. broj izvoda
6. datum
7. početno stanje
8. ukupan dugovni promet
9. ukupan potražni promet
10. stanje
11. veza ka dnevničkom dokumentu, ako je izvod povezan

### 5.1. Ručni unos izvoda

Izvod se može uneti ručno kroz editor.

### Podaci zaglavlja izvoda

1. poslovnica
2. banka
3. račun
4. valuta
5. broj izvoda
6. datum
7. početno stanje
8. dugovni promet
9. potražni promet
10. stanje

### Stavke izvoda

Za svaku stavku izvoda unose se:

1. broj računa druge strane
2. svrha plaćanja
3. dugovni ili potražni iznos
4. poziv na broj ili referenca

Kod stavke mora postojati ili dugovni ili potražni iznos. Ako jedan nije unet, drugi postaje obavezan.

### 5.2. Uvoz izvoda iz fajla

Na alatnoj traci izvoda postoji akcija za uvoz `E-bank` fajla.

Tok rada:

1. Otvorite `Bank Statements`.
2. Kliknite na uvoz izvoda.
3. Izaberite fajl koji banka generiše.
4. Sačekajte da sistem obradi fajl.

### Očekivani rezultat

Sistem kreira ili dopuni izvod i njegove stavke, a novi ili ažurirani izvod postaje selektovan na listi.

### Šta proveriti ako uvoz ne uspe

1. da li fajl odgovara formatu koji sistem podržava
2. da li podaci iz fajla sadrže račun, datum i stavke
3. da li za račun iz fajla postoji odgovarajući novčani račun u sistemu

## 6. Uvezivanje bankovnog izvoda sa Glavnom knjigom

Ovo je najvažniji radni tok kod bankovnih izvoda. U sistemu se usklađivanje radi kroz dokument `Bank Statement Reconciliation` unutar dnevnika.

Kada otvorite takav dokument, sistem prikazuje:

1. listu stavki bankovnog izvoda
2. listu stavki knjiženja na dokumentu
3. prozor za izbor otvorenih finansijskih stavki iz Glavne knjige

Za svaku stavku izvoda sistem vodi:

1. `Item balance`
2. `Entries balance`
3. `Closing balance`
4. status da li je stavka zatvorena

To znači:

1. `Item balance` je vrednost same stavke izvoda
2. `Entries balance` je zbir već povezanih knjiženja
3. `Closing balance` pokazuje koliko još ostaje da se zatvori

### 6.1. Ručno povezivanje stavke izvoda

Ručno povezivanje se koristi kada korisnik sam bira koje otvorene stavke iz finansija zatvaraju određenu stavku izvoda.

### Preporučeni postupak

1. Otvorite dokument usklađivanja izvoda.
2. U levoj listi izaberite stavku bankovnog izvoda.
3. Kliknite na akciju za izbor finansijskih stavki.
4. U prozoru `Select Finance Page Entries to reconcile` pregledajte otvorene stavke iz Glavne knjige.
5. Izaberite jednu ili više stavki koje treba povezati.
6. Po potrebi raspodelite iznos ručno ili akcijom `Distribute values proportionally`.
7. Potvrdite kreiranje povezivanja.

### Šta sistem prikazuje u prozoru za povezivanje

Sistem prikazuje otvorene finansijske stavke po podacima kao što su:

1. datum dospeća
2. poslovnica
3. konto i klasa konta
4. partner
5. link zatvaranja
6. oznake
7. finansijski dugovni i potražni promet
8. otvoreni saldo

### Važna pomoć pri ručnom povezivanju

Sistem za svaku stavku izvoda računa:

1. `Selected balance`
2. `New balance`

To korisniku odmah pokazuje da li je izabrani skup finansijskih stavki dovoljan, prevelik ili tačno odgovara izvodu.

### Podrazumevani filteri koje sistem predlaže

Kod ručnog povezivanja sistem pokušava da olakša izbor tako što unapred sužava listu:

1. po smeru novčanog toka
2. po tipu konta
3. po partneru, kada može da ga prepozna

Za uliv sistem traži otvorene stavke jednog tipa salda, a za odliv suprotnog tipa. Takođe pokušava da prepozna partnera na osnovu:

1. broja računa sa izvoda
2. identifikatora u opisu plaćanja
3. naziva partnera u tekstu svrhe plaćanja

### 6.2. Ručni izbor linka zatvaranja

Na formi pojedinačne stavke dnevnika postoji i poseban izbor `Select journal link`.

On se koristi kada korisnik ručno unosi stavku, ali želi da je veže za konkretan otvoreni link zatvaranja u finansijama.

Ova opcija je dostupna kada su poznati:

1. konto
2. poslovnica
3. po potrebi partner
4. po potrebi oznake

Kada korisnik otvori izbor linka, sistem prikazuje raspoložive otvorene linkove sa njihovim saldom. Izabrani link se zatim prenosi na stavku dnevnika.

### 6.3. Automatsko povezivanje

Sistem podržava i automatsko pokušavanje zatvaranja kroz akciju `Try close journal links`.

Ova akcija se koristi kada želite da sistem sam pronađe najverovatnija podudaranja između stavki izvoda i otvorenih finansijskih stavki.

### Šta sistem uzima u obzir pri automatskom povezivanju

Na osnovu backend logike, sistem koristi sledeće kriterijume:

1. broj računa druge strane sa izvoda
2. svrhu plaćanja
3. referencu ili poziv na broj
4. smer novčanog toka, uliv ili odliv
5. otvoreni saldo u Glavnoj knjizi
6. partnera koji se može vezati za broj računa ili tekst opisa
7. link zatvaranja iz finansijskih stavki
8. iznos stavke izvoda

### Redosled logike pri automatskom pokušaju

Sistem radi približno sledećim redosledom:

1. uzima samo otvorene stavke izvoda koje još nisu zatvorene
2. pokušava da prepozna partnera po broju računa druge strane
3. ako partner nije pronađen, pokušava da ga zaključi iz reference ili svrhe plaćanja
4. traži otvorene finansijske stavke tog partnera i odgovarajućeg smera
5. prvo traži jača podudaranja:
   tačan ili vrlo blizak tekst linka zatvaranja u referenci ili svrsi plaćanja i isti iznos
6. zatim traži slabija podudaranja:
   podudaranje teksta bez istog iznosa, jedinstvenu stavku sa istim iznosom ili skup stavki čiji zbir odgovara izvodu
7. kada nađe podudaranje, kreira stavke dnevnika koje zatvaraju izvod

### Šta korisnik može da zada pre automatskog pokušaja

Akcija podržava sledeće scenarije:

1. da radi samo nad selektovanim stavkama izvoda
2. da radi samo nad prilivima
3. da radi samo nad odlivima
4. da radi nad svim otvorenim stavkama

### Kako tumačiti rezultat

Automatsko povezivanje nije potpuno "crna kutija". Ono pomaže kod jasnih situacija, ali i dalje treba proveriti rezultat u sledećim slučajevima:

1. kada jedan partner ima više otvorenih stavki sličnog iznosa
2. kada u opisu plaćanja nema dovoljno podataka
3. kada broj računa nije evidentiran na partneru
4. kada isti iznos može odgovarati na više finansijskih stavki

### 6.4. Raspodela iznosa proporcionalno

Kod ručnog povezivanja postoji i akcija `Distribute values proportionally`.

Ona služi kada korisnik izabere više otvorenih finansijskih stavki, a želi da sistem automatski raspodeli iznos stavke izvoda proporcionalno veličini otvorenih salda.

Ovo je korisno kada:

1. jedna uplata zatvara više otvorenih stavki
2. jedna isplata pokriva više obaveza
3. korisnik želi brzu početnu raspodelu koju će po potrebi doraditi

### 6.5. Kreiranje iste stavke za više selektovanih stavki izvoda

Kod usklađivanja postoji i opcija `Create the same entry for selected Bank statement items`.

Ona služi kada više stavki izvoda treba knjižiti na isti način. Sistem tada kopira istu logiku unosa na sve izabrane stavke, uz prilagođavanje iznosa prema njihovom preostalom saldu.

## 7. Platni nalozi

Odeljak `Payment Orders` služi za kreiranje, pregled, reviziju, izvoz i označavanje platnih naloga.

Na listi naloga vide se:

1. status naloga
2. broj naloga
3. banka
4. račun
5. datum
6. opis
7. ukupan iznos
8. broj stavki
9. veza sa izvornim dokumentom iz nekog drugog modula, kada postoji

### 7.1. Statusi platnog naloga

Na osnovu koda sistem koristi više statusa, uključujući:

1. `Draft`
2. `Active`
3. `E-Bank File Created`
4. `Paid`

### 7.2. Kreiranje novog platnog naloga

Kod kreiranja zaglavlja naloga korisnik unosi:

1. banku
2. račun
3. datum
4. opis

### Preporučeni postupak

1. Otvorite `Payment Orders`.
2. Dodajte novi nalog.
3. Izaberite banku.
4. Izaberite račun.
5. Unesite datum i opis.
6. Sačuvajte nalog.
7. Otvorite stavke naloga i unesite primaoce i iznose.

### 7.3. Stavke platnog naloga

Za svaku stavku naloga vode se:

1. tip plaćanja
2. partner
3. naziv primaoca
4. grad primaoca
5. adresa primaoca
6. broj računa primaoca
7. svrha plaćanja
8. referenca
9. iznos
10. budžetska polja, kada je tip plaćanja budžetski

Za budžetska plaćanja dodatno se unose:

1. šifra opštine
2. šifra prihoda
3. budžetska organizacija
4. period od
5. period do

### 7.4. Izbor partnera i bankovnog računa

Kod unosa stavke postoji pomoćni prozor za izbor partnera.

Korisnik može:

1. izabrati partnera
2. preuzeti njegov grad i adresu
3. izabrati odgovarajući bankovni račun partnera

Ovo ubrzava unos i smanjuje mogućnost greške pri prepisivanju podataka.

### 7.5. Akcije nad platnim nalogom

Na dokumentu platnog naloga dostupne su akcije:

1. `Activate`
2. `Revise`
3. `Create E-bank file`
4. `Pay`
5. `Delete`
6. veza prema izvornom dokumentu, kada nalog dolazi iz drugog modula

### Šta znače ove akcije

1. `Activate` potvrđuje nalog za dalju upotrebu
2. `Revise` otvara mogućnost nove verzije naloga
3. `Create E-bank file` priprema fajl za elektronsko bankarstvo
4. `Pay` označava da je nalog izvršen
5. `Delete` briše nalog kada to poslovni status dozvoljava

### 7.6. E-bank fajl

Kod kreiranja E-bank fajla korisnik bira tip elektronskog bankarstva, a zatim sistem generiše odgovarajući fajl.

### Šta proveriti ako izvoz ne uspe

1. da li nalog ima stavke
2. da li su popunjeni obavezni podaci primaoca
3. da li je broj računa ispravan
4. da li je izabran odgovarajući tip E-bank fajla

## 8. Grupisanja izvoda

Odeljak `Bank Statement Groupings` postoji kao posebna funkcionalna celina modula. Služi za podešavanja grupisanja izvoda po banci i računu, kada firma koristi takvu organizaciju rada.

Ako se ova celina koristi u vašoj organizaciji, preporuka je da se podešava pre redovnog uvoza izvoda.

## 9. Izveštaji

U modulu su dostupni i izveštaji za pregled prometa i stanja po novčanim računima. Na osnovu koda dostupni su izveštaji kao što su:

1. promet po dokumentima
2. promene po računima
3. stanje po računima
4. valutna struktura
5. knjiga prometa

Tipični filteri uključuju:

1. dnevnik
2. period
3. banku
4. račun
5. poslovnicu
6. kategoriju i tip dokumenta

## 10. Najčešće situacije za proveru

Ako rad u modulu ne daje očekivan rezultat, proverite sledeće:

1. da li je izabran odgovarajući dnevnik
2. da li su podešeni tipovi dokumenata za početno stanje, izvod i standardna knjiženja
3. da li je bankovni izvod već povezan sa nekim dokumentom
4. da li broj računa druge strane postoji na partneru kada očekujete automatsko prepoznavanje
5. da li opis plaćanja ili referenca sadrže dovoljno podataka za automatsko uvezivanje
6. da li postoje otvorene finansijske stavke odgovarajućeg smera i iznosa
7. da li je kod ručnog povezivanja izabrana stavka izvoda pre dodavanja knjiženja
8. da li su kod platnih naloga popunjeni svi obavezni podaci primaoca
9. da li je kod strane valute postavljen kurs i valuta računa

## 11. Preporučeni redosled rada

Za tipičan rad sa bankom preporučeni redosled je:

1. uvezite ili unesite bankovni izvod
2. otvorite dokument za usklađivanje izvoda u dnevniku
3. sinhronizujte stavke izvoda sa dokumentom
4. pokušajte automatsko zatvaranje ako su podaci kvalitetni
5. ručno proverite i dopunite preostale otvorene stavke
6. objavite dokument
7. po potrebi kreirajte i obradite platne naloge

Na taj način modul `Cash Accounts` ostaje usklađen i sa bankarskim prometom i sa otvorenim stavkama u Glavnoj knjizi.
