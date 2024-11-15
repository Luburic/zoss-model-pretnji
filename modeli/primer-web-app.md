# Model pretnji veb aplikacije za podršku zubarske ordinacije

Dokument definiše podskup rezultata bezbednosne analize dizajna veb aplikacije za podršku zubarske ordinacije. Služi za ilustraciju kako se definiše model pretnji, gde navodi 2 resursa, 1 pretnju za svaki resurs, 1 napad za svaku pretnju i bezbednosne kontrole koje sprečavaju dati napad.

Dokument se služi terminima vezanim za pretnje i tokove podataka koje definiše [sledeći dokument](https://github.com/Luburic/zoss-model-pretnji/blob/main/modeli/terminologija.md).

## Tokovi podataka analiziranog modula

Analiziran modul predstavlja **aplikaciju za podršku zubarske ordinacije**. Reklamira usluge zubarske ordinacije i podržava zubare i pacijente za zakazivanju pregleda i razmenu poruka koje mogu uključiti zakačene fotografije. Softver se sastoji od klijentske aplikacije, izgrađene u React tehnologiji, serverske aplikacije izgrađene u ASP.NET radnom okviru i PostgreSQL baze podataka.

Dijagram ispod prikazuje procesne komponente (P), skladišta (S), tokove podataka (T) i eksterne entitete (E) sa kojim analiziran modul interaguje.

![DFD](https://github.com/user-attachments/assets/65aa38d4-b277-4dc8-b6fe-0ed86063774e)

## Resursi i pretnje visokog nivoa

Za ovaj primer analiziramo dva resursa i po jednu pretnju visokog nivoa za svaki resurs.

| Resursi         | Pretnje                                         |
|-----------------|-------------------------------------------------|
| R1. Fotografije | PR1. Krađa fotografija (information disclosure) radi rušenja reputacije. |
| R2. ASP.NET App | Rušenje aplikacije (denial of service) radi rušenja reputacije. |
