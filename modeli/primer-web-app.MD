# Model pretnji veb aplikacije za podršku zubarske ordinacije

Dokument definiše rezultat bezbednosne analize dizajna veb aplikacije za podršku zubarske ordinacije. Aplikacija reklamira usluge zubarske ordinacije i podržava zubare i pacijente za zakazivanju pregleda i razmenu poruka koje mogu uključiti zakačene fotografije i dokumente. Softver se sastoji od klijentske aplikacije, izgrađene u React tehnologiji, serverske aplikacije izgrađene u ASP.NET radnom okviru i PostgreSQL baze podataka.

## Terminologija korišćena u dokumentu

U ovoj sekciji su definisani bitni termini koji se koriste u ostatku teksta.

### Bezbednosni koncepti

**Ciljani modul**: Sistem fizičkih i digitalnih *resursa* koji zajedno čine veću celinu i koji su meta bezbednosne analize. Informacioni sistem se sastoji od više aplikacija, hardverskih uređaja i korisnika. Aplikacija se sastoji od više komponenti i obrađuje različite podatke. Komponenta se sastoji od više klasa i interaguje sa određenim bibliotekama.

**Resurs**: Fizički ili digitalan objekat čija *bezbednosna svojstva* *napadač* želi da naruši.

**Bezbednosno svojstvo objekta**: Apstraktan termin koji uključuje **poverljivost**, **integritet** i **dostupnost**, odnosno svojstva koja želimo da zaštitimo u kontekstu informacione bezbednosti.

**Napadač**: Pojedinac ili organizacija koja želi da naruši bezbednosna svojstva pojedinih objekata iz našeg sistema.


### Softverski koncepti
