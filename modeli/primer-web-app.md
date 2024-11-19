# Model pretnji veb aplikacije za podršku zubarske ordinacije

Dokument definiše mali podskup rezultata bezbednosne analize dizajna veb aplikacije za podršku zubarske ordinacije i služi kao primer za model pretnji koji će tvoj tim sprovesti.

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

U nastavku definišemo (podskup) resursa sistema i pretnji visokog nivoa za svaki resurs.

| Resursi         | Pretnje                                         |
|-----------------|-------------------------------------------------|
| R1. Fotografije | P11. Krađa fotografija (information disclosure) radi rušenja reputacije. |
| R2. ASP.NET App | P21. Rušenje aplikacije (denial of service) radi rušenja reputacije. |
|  | P22. Otkazivanje tuđih pregleda (elevation of privilege) radi rušenja reputacije ili pronalaska termina za sebe. |

Prethodni dijagram anotiramo identifikovanim resursima, radi identifikacije pretnji niskog nivoa.

![image](https://github.com/user-attachments/assets/afc090c8-3af1-47e0-8136-c3bb3dcaae98)

## Analiza prentje R21. Rušenje ASP.NET aplikacije (DoS)

Slika ispod sumira (podskup) pretnji niskog nivoa, napada i bezbednosnih kontrola koje se izvlače iz analizirane pretnje.
