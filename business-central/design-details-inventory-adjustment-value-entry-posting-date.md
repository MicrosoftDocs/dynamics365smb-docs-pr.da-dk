---
title: Bogføringsdato på værdiposter
description: Få mere at vide, hvordan kørslen Juster kostpris - vareposter identificerer og tildeler en posteringsdato til de værdiposter, der er ved at blive oprettet.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/19/2021
ms.author: edupont
ms.openlocfilehash: 3dcda7f44797f52e50babe4dbec90e3b2be6f19d
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440724"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Designoplysninger: Bogføringsdato på post med reguleringsværdi  

Denne artikel indeholder en vejledning til brugere af funktionen Lagerkostmetode i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne specifikke artikel giver en vejledning i, hvordan kørslen **Juster kostpris - vareposter** identificerer og tildeler en bogføringsdato til de værdiposter, der er ved at blive oprettet.  

Først gennemgås konceptet i processen, hvordan kørslen identificerer og tildeler en bogføringsdato til den værdipost, der er ved at blive oprettet. Derefter beskrives nogle scenarier, som vi i supportteamet støder på fra tid til anden, og endelig vises der en oversigt over de begreber, der er brugt.  

## <a name="the-concept"></a>Konceptet  

Kørslen **Reguler kostværdi – vareposter** tildeler en bogføringsdato til den værdipost, der er ved at blive oprettet i følgende trin:  

1.  Først har bogføringsdatoen for posten, der skal oprettes, den samme dato som den post, den regulerer.  

2.  Bogføringsdatoen valideres op mod lagerperioder og/eller Opsætning af Finans.  

3.  Tildeling af bogføringsdato. Hvis den oprindelige bogføringsdato ikke er inden for det tilladte datointerval for posteringen, tildeler kørslen en tilladt bogføringsdato fra Opsætning af Finans eller lagerperiode. Hvis både lagerperioder og tilladte bogføringsdatoer i Opsætning af Finans er defineret, så er det den seneste dato af de to, der tildeles til posten med reguleringsværdien.  

 Lad os gennemgå processen mere i praksis. Antag, at vi har en varepost for varesalg. Varen blev leveret på den 5. september 2020, og den blev faktureret dagen efter.  


**Varepost**  
Datoformat ÅÅÅÅ-MM-DD

|Løbenr.  |Varenr.  |Bogføringsdato  |Postens type  | Bilagsnr. |Lokationskode  |Antal  |Kostbeløb (faktisk)  |Faktureret antal  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Salg       |102033     |  Blå       | -1    |    -11     |-1     |    0     |

Nedenfor repræsenterer den første værdipost (379) forsendelsen og har den samme bogføringsdato som den overordnede varepost.  
  
Den anden værdipost (381) repræsenterer fakturaen.  

Den tredje værdipost (391) er en regulering af faktureringsværdiposten (381).  
  

|Løbenr.  |Varenr.  |Bogføringsdato  |Vareposttype  |Postens type  |Bilagsnr.  |Varepostløbenr.  |Lokationskode  |Varepostmængde  |Faktureret antal  |Kostbeløb (faktisk)  |Kostbeløb (forventet)  |Regulering  |Udlign.postløbenr.  |Kildespor  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Salg     | Købspris   | 102033        |319     | Blå        | -1       |0         |  0       |     -10   |Nr.   |0    |Salg          |
|381     |  A       |    2020-09-06     |    Salg     | Købspris   | 103022        |319     | Blå        |  0       |-1        |-10       |    10     | Nr.  |0      |       Salg   |
|391     |  A       |    2020-09-10     |    Salg     | Købspris   | 103022        |319     | Blå        |  0       |0         |-1        |    0     |Ja   |    181   | INVTADJMT   |

Bogføringsdatoen på reguleringsposten bliver i udgangspunktet angivet til samme bogføringsdato som den post, den regulerer.

 Trin 1: Reguleringsværdiposten, der skal oprettes, er knyttet til samme bogføringsdato, som den post, den justerer, illustreret ovenfor af værdipost 391.  
  
 Trin 2: Validering af oprindelig tildelt bogføringsdato.  

Kørslen **Juster kostpris - vareposter** bestemmer, om den første bogføringsdato for reguleringsværdiposten er inden for det tilladte bogføringsdatointerval, der er baseret på lagerperioder og/eller Opsætning af Finans.  

Lad os gennemgå ovennævnte salg ved at tilføje opsætningen af tilladte bogføringsdatointervaller.  
  
**Lagerperioder**

|Afslutningsdato  |Name  |Lukket  |
|---------|---------|---------|
|2020-01-31     |2020. januar      |  Ja    |
|2020-02-28     |Februar 2020     |  Ja    |
|2020-03-31     |Marts 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Maj 2020        |  Ja    |
|2020-06-30     |Juni 2020       |  Ja    |
|2020-07-31     |Juli 2020        |   Ja   |
|2020-08-31     |August 2020     |   Ja   |
|2020-09-30     |September 2020  |         |
|2020-10-31     |Oktober 2020    |         |
|2020-11-30     |November 2020   |         |
|2020-12-31     |December 2020   |         |

Den først tilladte bogføringsdato er den første dag i den første åbne periode. 1. september 2020.  

**Opsætning af Finans**

|Felt|Værdi  |
|---------|---------|
|Bogf. tilladt fra:  |  2020-09-10      |
|Bogf. tilladt til:    |  2020-09-30      |
|Registrer tid:       |         |
|Lokalt adresseformat:|   Postnr.      |  

 Første tilladte bogføringsdato er den dato, der er angivet i feltet Tillad bogføring fra: 10. september 2020.  
 Hvis både lagerperioder og tilladte bogføringsdatoer i Opsætning af Finans er defineret, så er det den seneste dato af de to, der definerer det tilladte bogføringsdatointerval.  

 Trin 3: Tildeling af en tilladt bogføringsdato.  

 Den oprindeligt tildelt bogføringsdato er 6. september, som vist i trin 1. Men i 2. trin identificerer kørslen Juster kostpris - vareposter, at den tidligst tilladte bogføringsdato er 10. september, og dermed tildeles 10. september til 10 reguleringsværdiposten nedenfor.  

   
|Løbenr.  |Varenr.  |Bogføringsdato  |Vareposttype  |Postens type  |Bilagsnr.  |Varepostløbenr.  |Lokationskode  |Varepostmængde  |Faktureret antal  |Kostbeløb (faktisk)  |Kostbeløb (forventet)  |Regulering  |Udlign.postløbenr.  |Kildespor  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Salg     | Købspris   | 102033        |319     | Blå        | -1       |0         |  0       |     -10   |Nr.   |0    |Salg          |
|381     |  A       |    2020-09-06     |    Salg     | Købspris   | 103022        |319     | Blå        |  0       |-1        |-10       |    10     | Nr.  |0      |       Salg   |
|391     |  A       |    **2020-09-10**     |    Salg     | Købspris   | 103022        |319     | Blå        |  0       |0         |-1        |    0     |Ja   |    181   | INVTADJMT   |

 Vi har nu gennemgået konceptet for tildeling af bogføringsdatoer til værdiposter, der er oprettet af kørslen Juster kostpris - vareposter.  

 Lad os fortsætte med at gennemse nogle scenarier, som vi i supportteamet støder på fra tid til anden i forbindelse med tilknyttede bogføringsdatoer i kørslen Juster kostpris – vareposter og de relaterede opsætninger.  

## <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Scenarie I: "Bogføringsdatoen er ikke inden for intervallet af tilladte bogføringsdatoer..."  

 Dette er en scenarie, hvor en bruger får vist den nævnte fejlmeddelelse, under kørsel af Juster kostpris - vareposter.  

 I det foregående afsnit, der beskriver konceptet med tildeling af bogføringsdatoer, var formålet med kørslen Juster kostpris - vareposter at oprette en værdipost med bogføringsdatoen 10. september.  

![Fejlmeddelelse om bogføringsdato.](media/helene/TechArticleAdjustcost6.png "Fejlmeddelelse om bogføringsdato")

 Vi følger op på brugeropsætningen:  

**Brugeropsætning**  

Sortering: Bruger-id  

|Bruger-id  |Bogf. tilladt fra  | Bogf. tilladt til  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

 Brugeren har i dette tilfælde et tilladt bogføringsdatointerval fra 11. september til 30. september og må derfor ikke bogføre reguleringsværdiposten med bogføringsdatoen 10. september.  

### <a name="overview-of-involved-posting-date-setup"></a>Oversigt over opsætning af den involverede bogføringsdato:

**Lagerperioder**  

|Afslutningsdato  |Name  |Lukket  |
|---------|---------|---------|
|2020-01-31     |2020. januar      |  Ja    |
|2020-02-28     |Februar 2020     |  Ja    |
|2020-03-31     |Marts 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Maj 2020        |  Ja    |
|2020-06-30     |Juni 2020       |  Ja    |
|2020-07-31     |Juli 2020        |   Ja   |
|2020-08-31     |August 2020     |   Ja   |
|2020-09-30     |September 2020  |         |
|2020-10-31     |Oktober 2020    |         |
|2020-11-30     |November 2020   |         |
|2020-12-31     |December 2020   |         |  

**Opsætning af Finans**  

|Felt|Værdi|
|---------|---------|
|Bogf. tilladt fra:  |  2020-09-10      |
|Bogf. tilladt til:    |  2020-09-30      |
|Registrer tid:       |         |
|Lokalt adresseformat:|   Postnr.      |  

**Brugeropsætning**    

|Bruger-id  |Bogf. tilladt fra  | Bogf. tilladt til  |
|---------|---------|--------|
|BRUGERNAVN |  2020-09-10      |2020-09-30      |

 Hvis brugeren knyttes til et større (eller samme) tilladte bogføringsdatointerval i lagerperioden eller finansopsætningen, undgås den nævnte konflikt. Reguleringen af værdiposten med bogføringsdatoen 10. september bogføres automatisk med denne opsætning.

En ældre vidensbaseartikel [952996](https://support.microsoft.com/topic/information-about-inventory-adjustment-posting-dates-in-microsoft-dynamics-nav-99e22b2b-5b79-a9b2-3b43-7f3484fa31d9) beskriver yderligere scenarier, der er relateret til den nævnte fejlmeddelelse.  

## <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Scenarie II: Bogføringsdato på reguleringsværdipost og bogføringsdatoen på post, der forårsager reguleringen, f.eks. værdiregulering eller varegebyr.  

### <a name="revaluation-scenario"></a>Værdireguleringsscenarie:  

 Forudsætninger:  

 Opsætning af lager:  
ff
-   Aut. lagerværdibogføring = Ja  

-   Automatisk kostregulering = Altid  

-   Beregn.type for gnsn. kostpris = Vare  

-   Gennemsnitlig omkostningsperiode = Dag  

 Opsætning af Finans:  

-   Bogf. tilladt fra = 1. januar 2021  

-   Bogf. tilladt til = tom  

 Brugeropsætning:  

-   Bogf. tilladt fra = 1. december 2020  

-   Bogf. tilladt til = tom  

### <a name="to-test-the-scenario"></a>Sådan testes scenariet  

1.  Opret varen TEST:  

     Basisenhed = STK  

     Kostmetode = Gennemsnit  

     Vælg valgfrie bogføringsgrupper.  

2.  Åbn varekladden, opret og bogfør en linje på følgende måde:  

     Bogføringsdato = 15. december 2020  

     Vare = TEST  

     Posttype = Køb  

     Antal = 100  

     Pris = 10  

3.  Åbn varekladden, opret og bogfør en linje på følgende måde:  

     Dato = 20. december 2020  

     Vare = TEST  

     Posttype = Nedregulering  

     Antal = 2  

4.  Åbn varekladden, opret og bogfør en linje på følgende måde:  

     Dato = 15. januar, 2021.  

     Vare = TEST  

     Posttype = Nedregulering  

     Antal = 3  

5.  Åbn værdireguleringskladden, opret og bogfør en linje på følgende måde:  

     Vare = TEST  

     Udligningspost = Vælg købspost, der er bogført i trin 2. Bogføringsdatoen for værdireguleringen er den samme som for den post, den regulerer.  

     Kostpris (reguleret) = 40  

Følgende **Varepost** og **Værdiposter** er bogført:  

**Vareposttype - Køb**  
Datoformat ÅÅÅÅ-MM-DD  

|Løbenummer  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TEST         |2020-12-15         |Køb         |T00001         |100         |4000         |95        |

**Værdiposter**  

|Løbenummer  |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  |Varenummerpostens mængde  |Kostbeløb (faktisk)  |Bogført kostværdi  |Regulering  |Udligningspost  |Kildespor  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TEST|   2020-12-15    |317         |Køb         |Købspris         |T00001         |100         |1.000,00          |1.000,00    |Nr.         |0         |ITEMNL         |
|379     |TEST   |**2020-12-15**    |317         |Køb         |Regulering         |T04002         |0         |3.000,00         |3.000,00         |Nr.         |0         |REVALINL         |

**Varepost - nedregulering, trin 3**  

|Løbenr.  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TEST      |2020-12-20   |Nedregulering  |T00002         |-2         |-80         | 0        |

**Værdiposter**  

|Løbenummer  |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  |Varenummerpostens mængde  |Kostbeløb (faktisk)  |Bogført kostværdi til Finans  |Regulering  |Udligningspost  |Kildespor  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TEST|   2020-12-20    |318         |Nedregulering         |Købspris         |T00002         |-2         |-20          |-20    |Nr.         |0         |ITEMNL         |
|380     |TEST   |**2021-01-01**    |318         |Nedregulering         |Købspris         |T04002         |0         |-60         |-60         |Ja         |377         |INVTADAMT         |

**Varepost - nedregulering, trin 4**  

|Løbenr.  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TEST      |2021-01-15   |Nedregulering  |T00003         |-3         |-120         | 0        |

**Værdiposter**  

|Løbenummer  |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  |Varenummerpostens mængde  |Kostbeløb (faktisk)  |Bogført kostværdi til Finans  |Regulering  |Udligningspost  |Kildespor  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TEST|   2021-01-15    |319         |Nedregulering         |Købspris         |T00003         |-3         |-30          |-30    |Nr.         |0         |ITEMNL         |
|381     |TEST   |**2021-01-15**    |319         |Nedregulering         |Købspris         |T04003         |0         |-90         |-90         |Ja         |378         |INVTADAMT         |

Kørslen Juster kostpris - vareposter har registreret en ændring i kostprisen og har justeret de negative reguleringer.  

**Gennemgang af bogføringsdatoer på oprettede reguleringsværdiposter:** Den tidligst tilladte bogføringsdato, som kørslen Reguler kostpris - vareposter skal forholde sig til, er 1. januar 2021 som anført i Opsætning af Finans.  

**Negativ regulering i trin 3:** den tildelte bogføringsdato er 1. januar fra Opsætning af Finans. Bogføringsdatoen for værdiposten i området til regulering er 20. december 2020. I henhold til Opsætning af Finans er datoen ikke inden for det tilladte bogføringsdatointerval. Derfor tildeles den bogføringsdato, der er angivet i feltet Bogf. tilladt fra i Opsætning af Finans, til værdireguleringsposten.  

**Negativ regulering i trin 4:** den tildelte bogføringsdato er 15. januar. Værdiposten i reguleringen har bogføringsdatoen 15. januar, som er inden for det tilladte bogføringsdatointerval i henhold til Opsætning af Finans.  

Reguleringen, der er foretaget for nedreguleringen i trin 3 giver problemer. Den favorable bogføringsdato for værdireguleringsposten ville have været 20. december eller i det mindste i december, da værdireguleringen som medfører ændringen i vareforbruget blev bogført i december.  

For at opnå regulering i december af nedreguleringen i trin 3, skal Opsætning af Finans i feltet Bogf. tilladt fra angive en dato i december.  

**Konklusion:**  

Med oplevelserne fra dette scenarie, hvor vi overvejer den mest velegnede opsætning af tilladt bogføringsdatointerval for en virksomhed, kan følgende være nyttigt: Så længe ændringer i lagerværdien må bogføres i en periode, december i det tilfælde, skal den opsætning, virksomheden bruger til tilladte bogføringsdatointervaller, justeres i forhold til beslutningen. Bogf. tilladt fra i Opsætning af Finans angiver 1. december, og det tillader at, værdireguleringen foretaget i december kan sendes til berørte udgående poster i samme periode.  

Brugergrupper, der ikke må bogføre i december, men i januar, hvilket sandsynligvis var beregnet til at være begrænset af Opsætning af Finans i dette scenarie, skal i stedet behandles via Brugeropsætning.  

### <a name="item-charge-scenario"></a>Scenarie med varegebyr:  

 Forudsætninger:  

 Opsætning af lager:  

-   Aut. lagerværdibogføring = Ja  

-   Automatisk kostregulering = Altid  

-   Beregn.type for gnsn. kostpris = Vare  

-   Gennemsnitlig omkostningsperiode = Dag  

 Opsætning af Finans:  

-   Bogf. tilladt fra = 1. december 2020  

-   Bogf. tilladt til = tom  

 Brugeropsætning:  

-   Bogf. tilladt fra = 1. december 2020  

-   Bogf. tilladt til = tom  


### <a name="to-test-the-scenario"></a>Sådan testes scenariet  

1.  Opret varegebyr:  

     Basisenhed = STK  

     Kostmetode = Gennemsnit  

     Vælg valgfrie bogføringsgrupper.  

2.  Opret en ny købsordre  

     Leverandørnr.: 10000  

     Bogføringsdato = 15. december 2020

     Kreditors fakturanr.: 1234  

     På købsordrelinje:  

     Vare = GEBYR  

     Antal = 1  

     Købspris = 100  

     Bogfør modtagelse og faktura.  

3.  Opret en ny salgsordre:  

     Kundenr.: 10000  

     Bogføringsdato = 16. december 2020  

     På salgsordrelinjen:  

     Vare = GEBYR  

     Antal = 1  

     Salgspris = 135  

     Bogfør levering og faktura.  

4.  Opsætning af Finans:  

     Bogf. tilladt fra = 1. januar 2021  

     Bogf. tilladt til = tom  

5.  Opret en ny købsordre:  

     Leverandørnr.: 10000  

     Bogføringsdato = 2. januar 2021  

     Kreditors fakturanr.: 2345  

     På købsordrelinje:  

     Varegebyr = JB-FRAGT  

     Antal = 1  

     Købspris = 3  

     Tildele varegebyrer til købsleverance fra trin 2.  

     Bogfør modtagelse og faktura.  


**Statusvarepost på købstrin 2**:  
  
|Løbenummer  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |GEBYR         |2020-12-15         |Køb         |107030         |1         |105         |0        |

**Værdiposter**  

|Løbenummer |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  | Varegebyrnr.    |  Varepostmængde   |Kostbeløb (faktisk)     |Bogført kostværdi til Finans |Regulering |Udlign.postløbenr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |GEBYR|   2020-12-15    |324         |Køb         |Købspris         |108029         |         |1          |100    |100         |NUMMER         |0         |
|399      |GEBYR   |2021-01-02    |324         |Køb         |Købspris         |108009         |JBFREIGHT         |0         |3         |3         |NUMMER         |0         |


**Statusvarepost for salg**:  
  
|Løbenr.  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |GEBYR         |2020-12-16         |Salg         |102035         |-1         |-105         |0        |

**Værdiposter**  

|Løbenummer |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  | Varegebyrnr.    |  Varepostmængde   |Kostbeløb (faktisk)     |Bogført kostværdi til Finans |Regulering |Udlign.postløbenr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |GEBYR|   2020-12-16    |325         |Salg         |Købspris         |109024         |         |-1          |-100    |-100         |NUMMER         |0         |
|400      |GEBYR   |2021-01-01    |325         |Salg         |Købspris         |109024         |         |0         |-3         |-3         |Ja         |398         |


6.  På arbejdsdatoen 3. januar ankommer en købsfaktura, der indeholder et ekstra varegebyr for købet, der er oprettet i trin 2. Fakturaen er dateret 30. december og bogføres derfor med bogføringsdato 30. december 2020.  

     Opret en ny købsordre:  

     Leverandørnr.: 10000  

     Bogføringsdato = 30. december 2020  

     Kreditors fakturanr.: 3456  

     På købsordrelinje:  

     Varegebyr = JB-FRAGT  

     Antal = 1  

     Købspris = 2  

     Tildele varegebyrer til købsleverance fra trin 2  

     Bogfør kvittering og faktura.  


**Statusvarepost for køb**:  

|Løbenummer  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |GEBYR         |2020-12-15         |Køb         |107030         |1         |105         |0        |

**Værdiposter**  

|Løbenr. |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  | Varegebyrnr.    |  Varepostmængde   |Kostbeløb (faktisk)     |Bogført kostværdi til Finans |Regulering |Udlign.postløbenr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |GEBYR   |2020-12-15    |324         |Køb         |Købspris         |108029         |            |1         |100    |100         |Nr.         |0         |
|399      |GEBYR   |2021-01-02    |324         |Køb         |Købspris         |108030         |JBFREIGHT   |0         |3         |3         |Nr.         |0         |
|401      |GEBYR   |**2020-12-30**    |324         |Køb         |Købspris         |108031         |JBFREIGHT   |0         |2         |2         |Nr.         |0         |

**Statusvarepost for salg**:  
  
|Løbenummer  |Varenr.  |Bogføringsdato  |Postens type  |Bilagsnr.  |Antal  |Kostbeløb (faktisk)  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |GEBYR         |2020-12-16         |Salg         |102035         |-1         |-105         |0        |

**Værdiposter**  

|Løbenr. |Varenr.  |Bogføringsdato  |Varepostløbenr.  |Vareposttype  |Postens type  |Bilagsnr.  | Varegebyrnr.    |  Varepostmængde   |Kostbeløb (faktisk)     |Bogført kostværdi til Finans |Regulering |Udlign.postløbenr. |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |GEBYR   |2020-12-16        |325         |Salg         |Købspris         |103024         |            |-1         |-100       |-100         |Nr.         |0         |
|400      |GEBYR   |2021-01-01        |325         |Salg         |Købspris         |103024         |            |0          |-3         |-3         |Ja         |398         |
|402      |GEBYR   |**2021-01-01**    |325         |Salg         |Købspris         |103024         |            |0          |-2         |-2         |Ja         |398         |

Lageropgørelsesrapporten udskrives pr. dato 31. december 2020

![Indholdet i lagerværdirapport.](media/helene/TechArticleAdjustcost13.png "Indholdet i lagerværdirapport")

 **Oversigt over scenarie:**  

 Det beskrevne scenarie afsluttes med rapporten Lagerværdi, der viser Antal = 0, mens værdien = 2. Varegebyret, der er bogført i trin 11, er en del af lagerforøgelsesværdien i december, mens lagerfaldet i samme periode ikke påvirkes.  

 Det var godt for det første varegebyr, at Opsætning af Finans angav Bogf. tilladt fra 1. januar. Omkostningerne til lagerforøgelse og -fald blev registreret i samme periode. For anden varegebyret medfører Opsætning af Finans dog, at ændringen i vareforbrug registreres i perioden efter.  

 **Konklusion:**  

 Det er en udfordring, at rapporten Lagerværdi viser antal = 0, mens værdien er <> 0. I dette tilfælde er det også sværere at angive de optimale indstillinger, da købsfakturaer ankommer den samme dag, men drejer sig om forskellige perioder eller endda regnskabsår. Overgangen til et nyt regnskabsår kræver som regel nogen planlægning, og som en del af denne indsigt, skal processen Juster kostpris - vareposter, der genkender vareforbrug, tages i betragtning.  

 I dette scenarie kunne det være en mulighed at lade feltet Bogf. tilladt fra i Opsætning af Finans angive en dato i december i et par dage til, og lade bogføringen af det første varegebyr vente for at tillade, at alle omkostninger fra den forrige periode/det forrige regnskabsår blev genkendt i den periode, hvor de hører til, og køre kørslen Juster kostpris - vareposter og derefter flytte den tilladte bogføringsdato til den nye periode\/det nye regnskabsår. Den første varegebyr med bogføringsdatoen 2. januar kan derefter bogføres.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Oversigt over kørslen Juster kostpris - vareposter  

 Nedenfor vises en oversigt over konceptet for tildeling af bogføringsdatoer til reguleringsværdier i kørslen Juster kostpris - vareposterkørsel.  

### <a name="about-the-request-form-posting-date"></a>Om bogføringsdatoen for anmodningsformularen:  

 Der skal ikke længere angives en bogføringsdato i anmodningsformularen til kørslen Juster kostpris - vareposter. Kørslen kører gennem alle nødvendige rettelser og oprettet værdiposter med den bogføringsdato, der er angivet i den værdipost, som justeres. Hvis bogføringsdatoen ikke er inden for det tilladte bogføringsdatointerval, bruges bogføringsdatoen i feltet Bogf. tilladt fra i Opsætning af Finans, ELLER hvis der anvendes lagerperioder, bruges den seneste dato af disse to. Se det beskrevne koncept ovenfor.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Oversigt over kørslen Bogfør lagerregulering  

 Kørslen Bogfør lagerregulering er tæt forbundet med kørslen Juster kostpris - vareposter, hvorfor oversigten over denne kørsel opsummeres og deles også her.  
 
![Faktisk kostpris ift. forventet kostpris.](media/helene/TechArticleAdjustcost14.png "Faktisk omkostning ift. forventet omkostning")

### <a name="about-the-posting-date"></a>Om bogføringsdato  

 Der skal ikke længere angives en bogføringsdato i anmodningsformularen til kørslen Bogfør lagerregulering. Finansposten oprettes med samme bogføringsdato som den tilknyttede værdipost. Med henblik på at udføre kørslen skal det tilladte bogføringsdatointerval tillade bogføringsdatoen for den tilknyttede finanspost. Hvis ikke, skal det tilladte bogføringsdatointerval midlertidigt åbnes igen ved at ændre eller fjerne datoerne i felterne Bogf. tilladt fra og Bogf. tilladt til i Opsætning af Finans. Det er nødvendigt for at undgå problemer med afstemningen, at bogføringsdato på finansposten svarer til bogføringsdatoen for værdiposten.  

 Kørslen søger i tabel 5811 - Bogfør værdi for at identificere værdiposterne i området til bogføring i Finans. Tabellen tømmes efter korrekt gennemført kørsel.

## <a name="see-also"></a>Se også  

[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  
[Designoplysninger: Vareudligning](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
