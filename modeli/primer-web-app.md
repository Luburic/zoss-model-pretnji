# Model pretnji veb aplikacije za podršku zubarske ordinacije

Dokument definiše podskup rezultata bezbednosne analize dizajna veb aplikacije za podršku zubarske ordinacije. Služi za ilustraciju kako se definiše model pretnji, gde navodi 2 resursa, 1 pretnju za svaki resurs, 1 napad za svaku pretnju i bezbednosne kontrole koje sprečavaju dati napad.

Dokument se služi terminima vezanim za pretnje i tokove podataka koje definiše [sledeći dokument](https://github.com/Luburic/zoss-model-pretnji/blob/main/modeli/terminologija.md).

# Tokovi podataka analiziranog modula

Analiziran modul predstavlja **aplikaciju za podršku zubarske ordinacije**. Aplikacija pruža sledeće funkcionalnosti:
- Reklama usluga i vrlina zubarske ordinacije radi privlačenja novih pacijenata,
- Funkciju zakazivanja pregleda za registrovane pacijente,
- Funkciju pregleda i analize pregleda za zubare,
- Funkciju razmene poruka između pacijenta i zubara, gde poruke uz tekst mogu da sadrže fotografije.

Softver se sastoji od klijentske aplikacije, izgrađene u React tehnologiji, serverske aplikacije izgrađene u ASP.NET radnom okviru i PostgreSQL baze podataka.

Dijagram ispod prikazuje za analiziran modul (m) procesne komponente (mP), skladišta (mS), tokove podataka (mT) i eksterne entitete (mE) sa kojim modul interaguje.

![DFD](https://github.com/user-attachments/assets/3b37e3f9-7626-45f8-8fd1-fad1f0ad9e1a)

# Resursi i pretnje visokog nivoa

Za ovaj primer analiziramo dva resursa i po jednu pretnju visokog nivoa za svaki resurs.

| Resursi         | Pretnje                                         |
|-----------------|-------------------------------------------------|
| R1. Fotografije | P11. Krađa fotografija (information disclosure) radi rušenja reputacije. |
| R2. ASP.NET App | P21. Rušenje aplikacije (denial of service) radi rušenja reputacije. |

## Bezbednosna analiza `R1. Fotografija`
TODO
