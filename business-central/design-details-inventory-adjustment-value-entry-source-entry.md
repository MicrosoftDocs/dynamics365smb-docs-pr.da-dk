---
title: Bogføringsdatoen for regulerings værdiposten sammenlignet med kildeposten
description: 'Få mere at vide om scenariet "Bogføringsdato for reguleringsværdipost mellem bogføringsdato for post, der medfører, at reguleringen f. eks. værdiregulering eller varegebyr" identificeres.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Bogføringsdatoen for regulerings værdiposten sammenlignet med kildeposten

Denne artikel sammenligner bogføringsdatoen for regulerings værdiposten med bogføringsdatoen på posten, der medfører, at kørslen Reguler kostværdi - vareposter er blevet kørt, især et reguleringsscenarie og et varegebyrscenario.

Kørslen **Reguler kostværdi - vareposter** behandler dine data, afhængigt af dit scenario og din konfiguration af [!INCLUDE[prod_short](includes/prod_short.md)]. I dette afsnit beskrives to separate processer, og hver af dem viser, hvilken type indflydelse kørslen Juster kostpris - vareposter har på dataene.

## Værdireguleringsscenarie

### Forudsætninger  

Indtast følgende værdier:

**Opsætning af lager**:  

- Aut. lagerværdibogføring = Ja  

- Automatisk kostregulering = Altid  

- Beregn.type for gnsn. kostpris = Vare  

- Gennemsnitlig omkostningsperiode = Dag  

**Opsætning af Finans**:  

- Bogf. tilladt fra = 1. januar 2021  

- Bogf. tilladt til = Tom  

**Brugeropsætning**:  

- Bogf. tilladt fra = 1. december 2020  

- Bogf. tilladt til = Tom  

### Sådan testes scenariet

Test dette scenario ved at udføre følgende trin.

1. Opret et **element** med navnet test med følgende værdier:  

     - Basisenhed = STK  

     - Kostmetode = Gennemsnit  

     - Vælg valgfrie bogføringsgrupper.  

2. Åbn **varekladden**, opret en ny post, og bogfør en linje på følgende måde:  

     - Bogføringsdato = 15. december 2020  

     - Vare = TEST  

     - Posttype = Køb  

     - Antal = 100  

     - Pris = 10  

3. Åbn **varekladden**, opret en ny post, og bogfør en linje på følgende måde:  

     - Dato = 20. december 2020  

     - Vare = TEST  

     - Posttype = Nedregulering  

     - Antal = 2  

4. Åbn **varekladden**, opret en ny post, og bogfør en linje på følgende måde:  

     - Dato = 15. januar, 2021.  

     - Vare = TEST  

     - Posttype = Nedregulering  

     - Antal = 3  

5. Åbn **vareværdireguleringskladde**, opret en ny post, og bogfør en linje på følgende måde:  

     - Vare = TEST  

     - Udligningspost = Vælg købspost, der er bogført i trin 2. Bogføringsdatoen for værdireguleringen er den samme som for den post, den regulerer.  

     - Kostpris (reguleret) = 40  

Følgende **Varepost** og **Værdiposter** er bogført:  

**Vareposttype - Køb**  

|Løbenummer  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TEST         |2020-12-15         |Køb         |T00001         |100         |4000         |95        |

**Værdiposter**  

|Løbenummer  |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  |Varenummerpostens mængde  |Kostbeløb (faktisk)  |Bogført kostværdi  |Regulering  |Udligningspost  |Kildespor  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TEST|   2020-12-15    |317         |Køb         |Købspris         |T00001         |100         |1.000,00          |1.000,00    |Nej         |0         |ITEMNL         |
|379     |TEST   |**2020-12-15**    |317         |Køb         |Regulering         |T04002         |0         |3.000,00         |3.000,00         |Nej         |0         |REVALINL         |

**Varepost - nedregulering, trin 3**  

|Løbenr.  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TEST      |2020-12-20   |Nedregulering  |T00002         |-2         |-80         | 0        |

**Værdiposter**  

|Løbenummer  |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  |Varenummerpostens mængde  |Kostbeløb (faktisk)  |Bogført kostværdi til Finans  |Regulering  |Udligningspost  |Kildespor  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TEST|   2020-12-20    |318         |Nedregulering         |Købspris         |T00002         |-2         |-20          |-20    |Nej         |0         |ITEMNL         |
|380     |TEST   |**2021-01-01**    |318         |Nedregulering         |Købspris         |T04002         |0         |-60         |-60         |Ja         |377         |INVTADAMT         |

**Varepost - nedregulering, trin 4**  

|Løbenr.  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TEST      |2021-01-15   |Nedregulering  |T00003         |-3         |-120         | 0        |

**Værdiposter**  

|Løbenummer  |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  |Varenummerpostens mængde  |Kostbeløb (faktisk)  |Bogført kostværdi til Finans  |Regulering  |Udligningspost  |Kildespor  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TEST|   2021-01-15    |319         |Nedregulering         |Købspris         |T00003         |-3         |-30          |-30    |Nej         |0         |ITEMNL         |
|381     |TEST   |**2021-01-15**    |319         |Nedregulering         |Købspris         |T04003         |0         |-90         |-90         |Ja         |378         |INVTADAMT         |

Kørslen **Juster kostpris - vareposter** har registreret en ændring i kostprisen og har justeret de negative reguleringer.  

**Gennemgang af bogføringsdatoer på oprettede reguleringsværdiposter:** Den tidligst tilladte bogføringsdato, som kørslen Reguler kostpris - vareposter skal forholde sig til, er 1. januar 2021 som anført i Opsætning af Finans.  

**Negativ regulering i trin 3:** den tildelte bogføringsdato er 1. januar fra Opsætning af Finans. Bogføringsdatoen for værdiposten i området til regulering er 20. december 2020. I henhold til Opsætning af Finans er datoen ikke inden for det tilladte bogføringsdatointerval. Derfor tildeles den bogføringsdato, der er angivet i feltet Bogf. tilladt fra i Opsætning af Finans, til værdireguleringsposten.  

**Negativ regulering i trin 4:** den tildelte bogføringsdato er 15. januar. Værdiposten i reguleringen har bogføringsdatoen 15. januar, som er inden for det tilladte bogføringsdatointerval i henhold til Opsætning af Finans.  

Reguleringen, der er foretaget for nedreguleringen i trin 3 giver problemer. Den favorable bogføringsdato for værdireguleringsposten ville have været 20. december eller i det mindste i december, da værdireguleringen som medfører ændringen i vareforbruget blev bogført i december.  

For at opnå regulering i december af nedreguleringen i trin 3, skal Opsætning af Finans i feltet Bogf. tilladt fra angive en dato i december.  

### Konklusion

Når du overvejer den mest velegnede opsætning for et firmas tilladte datointerval, kan det være en god idé at overveje følgende. Så længe ændringer i lagerværdien skal bogføres i en periode, f. eks. december, skal den opsætning, som firmaet bruger til at tillade bogføringsdato intervaller, justeres i henhold til denne beslutning. Bogf. tilladt fra i Opsætning af Finans angiver 1. december, og det tillader at, værdireguleringen foretaget i december kan sendes til berørte udgående poster i samme periode.  

Brugergrupper, der ikke må bogføre i december, men i januar, hvilket sandsynligvis var beregnet til at være begrænset af Opsætning af Finans i dette scenarie, skal i stedet behandles via Brugeropsætning.  

## Scenarie med varegebyr  

### Forudsætninger  

Indtast følgende værdier:

**Opsætning af lager**:  

- Aut. lagerværdibogføring = Ja  

- Automatisk kostregulering = Altid  

- Beregn.type for gnsn. kostpris = Vare  

- Gennemsnitlig omkostningsperiode = Dag  

**Opsætning af Finans**:  

- Bogf. tilladt fra = 1. december 2020  

- Bogf. tilladt til = Tom  

**Brugeropsætning**:  

- Bogf. tilladt fra = 1. december 2020.  

- Bogf. tilladt til = Tom  

### Sådan testes scenariet  

Test dette scenario ved at udføre følgende trin:

1.  Opret et **element** Gebyr med følgende værdier:  

     - Basisenhed = STK  

     - Kostmetode = Gennemsnit  

     - Vælg valgfrie bogføringsgrupper.  

2.  Opret en ny **købsordre** med følgende værdier:  

     - Leverandørnr.: 10000  

     - Bogføringsdato = 15. december 2020

     - Kreditors fakturanr.: 1234  

     Vælg følgende værdier på købsordrelinjen:  

     - Vare = GEBYR  

     - Antal = 1  

     - Købspris = 100  

     Bogfør dokumentet som modtaget og faktureret for at fuldføre trinnet.  

3.  Opret en ny **Salgsordre** med følgende værdier:  

     - Kundenr.: 10000  

     - Bogføringsdato = 16. december 2020  

     På salgsordrelinjen:  

     - Vare = GEBYR  

     - Antal = 1  

     - Salgspris = 135  

     Bogfør dokumentet som modtaget og faktureret for at fuldføre trinnet.  

4.  Angiv værdier for **Finansopsætning**-siden:  

     - Bogf. tilladt fra = 1. januar 2021  

    -  Bogf. tilladt til = tom  

5.  Opret en ny **købsordre** med følgende værdier:  

     - Leverandørnr.: 10000  

     - Bogføringsdato = 2. januar 2021  

     - Kreditors fakturanr.: 2345  

     På købsordrelinje:  

     - Varegebyr = JB-FRAGT  

     - Antal = 1  

     - Købspris = 3  

     - Tildele varegebyrer til købsleverance fra trin 2.  

     Bogfør dokumentet som modtaget og faktureret for at fuldføre trinnet.  


**Statusvarepost på købstrin 2**:  
  
|Løbenummer  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |GEBYR         |2020-12-15         |Køb         |107030         |1         |105         |0        |

**Værdiposter**  

|Løbenummer |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  | Varegebyrnr.    |  Varepostmængde   |Kostbeløb (faktisk)     |Bogført kostværdi til Finans |Regulering |Udlign.postløbenr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |GEBYR|   2020-12-15    |324         |Køb         |Købspris         |108029         |         |1          |100    |100         |NEJ         |0         |
|399      |GEBYR   |2021-01-02    |324         |Køb         |Købspris         |108009         |JBFREIGHT         |0         |3         |3         |NEJ         |0         |

**Statusvarepost for salg**:  
  
|Løbenr.  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |GEBYR         |2020-12-16         |Salg         |102035         |-1         |-105         |0        |

**Værdiposter**  

|Løbenummer |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  | Varegebyrnr.    |  Varepostmængde   |Kostbeløb (faktisk)     |Bogført kostværdi til Finans |Regulering |Udlign.postløbenr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |GEBYR|   2020-12-16    |325         |Salg         |Købspris         |109024         |         |-1          |-100    |-100         |NEJ         |0         |
|400      |GEBYR   |2021-01-01    |325         |Salg         |Købspris         |109024         |         |0         |-3         |-3         |Ja         |398         |

6.  På arbejdsdatoen 3. januar ankommer en købsfaktura, der indeholder et ekstra varegebyr for købet, der er oprettet i trin 2. Fakturaen er dateret 30. december og bogføres derfor med bogføringsdato 30. december 2020.  

     Opret en ny **købsordre** med følgende værdier:  

     - Leverandørnr.: 10000  

     - Bogføringsdato = 30. december 2020  

     - Kreditors fakturanr.: 3456  

     Vælg følgende værdier på købsordrelinjen:  

     - Varegebyr = JB-FRAGT  

     - Antal = 1  

     - Købspris = 2  

     Tildele varegebyrer til købsleverance fra trin 2  

     Bogfør dokumentet som modtaget og faktureret for at fuldføre trinnet.  


**Statusvarepost for køb**:  

|Løbenummer  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |GEBYR         |2020-12-15         |Køb         |107030         |1         |105         |0        |

**Værdiposter**  

|Løbenr. |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  | Varegebyrnr.    |  Varepostmængde   |Kostbeløb (faktisk)     |Bogført kostværdi til Finans |Regulering |Udlign.postløbenr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |GEBYR   |2020-12-15    |324         |Køb         |Købspris         |108029         |            |1         |100    |100         |Nej         |0         |
|399      |GEBYR   |2021-01-02    |324         |Køb         |Købspris         |108030         |JBFREIGHT   |0         |3         |3         |Nej         |0         |
|401      |GEBYR   |**2020-12-30**    |324         |Køb         |Købspris         |108031         |JBFREIGHT   |0         |2         |2         |Nej         |0         |

**Statusvarepost for salg**:  
  
|Løbenummer  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |GEBYR         |2020-12-16         |Salg         |102035         |-1         |-105         |0        |

**Værdiposter**  

|Løbenr. |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  | Varegebyrnr.    |  Varepostmængde   |Kostbeløb (faktisk)     |Bogført kostværdi til Finans |Regulering |Udlign.postløbenr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |GEBYR   |2020-12-16        |325         |Salg         |Købspris         |103024         |            |-1         |-100       |-100         |Nej         |0         |
|400      |GEBYR   |2021-01-01        |325         |Salg         |Købspris         |103024         |            |0          |-3         |-3         |Ja         |398         |
|402      |GEBYR   |**2021-01-01**    |325         |Salg         |Købspris         |103024         |            |0          |-2         |-2         |Ja         |398         |

Lageropgørelsesrapporten udskrives pr. dato 31. december 2020

![Indholdet i lagerværdirapport.](media/helene/TechArticleAdjustcost13.png "Indholdet i lagerværdirapport")

**Oversigt over scenarie:**  

Det beskrevne scenarie afsluttes med rapporten Lagerværdi, der viser Antal = 0, mens værdien = 2. Varegebyret, der er bogført i trin 6, er en del af lagerforøgelsesværdien i december, mens lagerfaldet i samme periode ikke påvirkes.  

Det var godt for det første varegebyr, at Opsætning af Finans angav Bogf. tilladt fra 1. januar. Omkostningerne til lagerforøgelse og -fald blev registreret i samme periode. For anden varegebyret medfører Opsætning af Finans dog, at ændringen i vareforbrug registreres i perioden efter.  

**Konklusion:**  

Det er en udfordring, at rapporten Lagerværdi viser antal = 0, mens værdien er <> 0. I dette tilfælde er det også sværere at angive de optimale indstillinger, da købsfakturaer ankommer den samme dag, men drejer sig om forskellige perioder eller endda regnskabsår. Overgangen til et nyt regnskabsår kræver som regel nogen planlægning, og som en del af denne indsigt, skal processen Juster kostpris - vareposter, der genkender vareforbrug, tages i betragtning.  

I dette scenarie kunne det være en mulighed at lade feltet Bogf. tilladt fra i Opsætning af Finans angive en dato i december i et par dage til, og lade bogføringen af det første varegebyr vente for at tillade, at alle omkostninger fra den forrige periode/det forrige regnskabsår blev genkendt i den periode, hvor de hører til, og køre kørslen Juster kostpris - vareposter og derefter flytte den tilladte bogføringsdato til den nye periode\/det nye regnskabsår. Den første varegebyr med bogføringsdatoen 2. januar kan derefter bogføres.  

## Se også  

[Designoplysninger: Bogføringsdato på post med reguleringsværdi](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  
[Designoplysninger: Vareudligning](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
