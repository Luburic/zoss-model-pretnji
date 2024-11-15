# Model pretnji veb aplikacije za podršku zubarske ordinacije

Dokument definiše rezultat bezbednosne analize dizajna veb aplikacije za podršku zubarske ordinacije. Aplikacija reklamira usluge zubarske ordinacije i podržava zubare i pacijente za zakazivanju pregleda i razmenu poruka koje mogu uključiti zakačene fotografije i dokumente. Softver se sastoji od klijentske aplikacije, izgrađene u React tehnologiji, serverske aplikacije izgrađene u ASP.NET radnom okviru i PostgreSQL baze podataka.

## Terminologija korišćena u dokumentu

U ovoj sekciji su definisani bitni termini koji se koriste u ostatku teksta.

### Terminologija pretnji

**Analiziran modul**: Sistem fizičkih i digitalnih **resursa** koji zajedno čine veću celinu i koji su meta bezbednosne analize. Informacioni sistem se sastoji od više aplikacija, hardverskih uređaja i korisnika. Aplikacija se sastoji od više komponenti i obrađuje različite podatke. Komponenta se sastoji od više klasa i interaguje sa određenim bibliotekama.

**Resurs**: Fizički ili digitalan objekat čija **bezbednosna svojstva** **napadač** želi da naruši.

**Bezbednosno svojstvo**: Apstraktan termin koji uključuje **poverljivost**, **integritet** i **dostupnost**, odnosno svojstva resursa koja želimo da zaštitimo u kontekstu informacione bezbednosti.

**Napadač**: Pojedinac ili organizacija koja želi da naruši bezbednosna svojstva resursa analiziranog modula.

**Pretnja visokog nivoa**: Cilj ili korak ka cilju napadača, definisan kao narušavanje bezbednosnog svojstva konkretnog resursa. Na primer, *spoofing servisa za vremensku prognozu* ili *tampering kriptografskog ključa*.

**Pretnja niskog nivoa**: Pretnja visokog nivoa konkretizovana na podsistem analiziranog modula. Na primer, *tampering kriptografskih ključeva u keystoru A*.

**Napad**: Interakcija napadača sa analiziranim modulom radi ostvarenja pretnje. Uspešan napad ostvaruje pretnju tako što iskorištava prisustvo **ranjivosti** u analiziranom modulu.

**Ranjivost**: Funkcionalnost analiziranog modula koja ima dve bitne karakteristike: 1) predstavlja neželjenu *dodatnu* funkcionalnost i 2) napadaču omogućuje da ostvari pretnju. Na primer, izvršavanje proizvoljnog koda kroz HTTP zaglavlje nije funkcionalnost koju je korisnik tražio, a svašta omogućuje napadaču. Spram toga, prikaz konfeta pri registraciji korisnika može biti neželjena funkcionalnost, ali ako ne može da se eksploatiše ne predstavlja ranjivost.

### Terminologija tokova podataka

**Dijagram toka podataka**: Grafički prikaz toka podataka kroz analizirani modul, koji opisuje kako podaci ulaze, prolaze kroz procese, skladište se i izlaze iz sistema. Služi za identifikaciju resursa, interakcija i potencijalnih ranjivosti u sistemu.

**Eksterni entitet**: Spoljni sistem, korisnik ili aplikacija koja razmenjuje podatke sa analiziranim modulom. Entiteti su izvan granica analiziranog modula i predstavljaju izvore ili odredišta podataka. Na primer, korisnik koji unosi podatke u aplikaciju.

**Proces**: Funkcionalna jedinica analiziranog modula koja obrađuje podatke. Procesi transformišu ulazne podatke u izlazne rezultate. Na primer, komponenta za računanje statistika ili aplikacija za opsluživanje grupe korisnika.

**Tok podataka**: Veza između entiteta, procesa i skladišta koja prikazuje kako se podaci prenose kroz analizirani modul. Tok podataka specificira tip i sadržaj prenetih podataka.

**Skladište podataka**: Mesto gde se podaci čuvaju u okviru analiziranog modula, bilo privremeno ili trajno. Skladišta podataka se koriste za čitanje i/ili zapisivanje podataka tokom procesa.

**Granica poverenja**: Granica koja razdvaja analizirani modul od spoljnog sveta ili podsistem analiziranog modula od drugog podsistema, ali samo u slučaju kada jednom podsistemu verujemo više od drugog. Na primer, sve klase koje su deo jednog DLLa imaju isti stepen poverenja, bez obzira da li su kontroleri, servisi ili domenske klase.
