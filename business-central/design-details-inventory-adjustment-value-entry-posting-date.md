---
title: Bogføringsdato på værdiposter
description: 'Få mere at vide, hvordan kørslen Juster kostpris - vareposter identificerer og tildeler en posteringsdato til de værdiposter, der er ved at blive oprettet.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><a name="design-details-posting-date-on-adjustment-value-entry"></a>Designoplysninger: Bogføringsdato på post med reguleringsværdi

Denne artikel indeholder en vejledning til brugere af funktionen til lagerprisberegning i [!INCLUDE[prod_short](includes/prod_short.md)], og det er især, at kørslen **Reguler kostværdi-vareposter** identificerer og tildeler en bogføringsdato til de værdiposter, som kørslen skal til at oprette.

## <a name="how-posting-dates-are-assigned"></a><a name="how-posting-dates-are-assigned"></a>Sådan tildeles bogføringsdatoer

Kørslen **Reguler kostværdi – vareposter** tildeler en bogføringsdato til den værdipost, der er ved at blive oprettet i følgende trin:  

1. Først har bogføringsdatoen for posten, der skal oprettes, den samme dato som den post, den regulerer.  

2. Bogføringsdatoen valideres op mod lagerperioder og/eller Opsætning af Finans.  

3. Tildeling af bogføringsdato. Hvis den oprindelige bogføringsdato ikke er inden for det tilladte datointerval for posteringen, tildeler kørslen en tilladt bogføringsdato fra Opsætning af Finans eller lagerperiode. Hvis både lagerperioder og tilladte bogføringsdatoer i Opsætning af Finans er defineret, så er det den seneste dato af de to, der tildeles til posten med reguleringsværdien.  

Lad os gennemgå processen mere i praksis. Antag, at vi har en varepost for varesalg. Varen blev leveret på den 5. september 2020, og den blev faktureret dagen efter.  

#### <a name="item-ledger-entry"></a><a name="item-ledger-entry"></a>Varepost

|Løbenr.  |Varenr.  |Bogføringsdato  |Postens type  | Bilagsnr. |Lokationskode  |Antal  |Kostbeløb (faktisk)  |Faktureret antal  |Restantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Salg       |102033     |  Blå       | -1    |    -11     |-1     |    0     |

Nedenfor vises de relaterede værdiposter:

- **Postnr. 379** repræsenterer forsendelsen og har den samme bogføringsdato som den overordnede varepost.  
- **Postnr. 381** repræsenterer fakturaen.  
- **Postnr. 391** er en regulering af faktureringsværdiposten (Postnr. 381 ovenfor).  

|Løbenr.  |Varenr.  |Bogføringsdato  |Vareposttype  |Postens type  |Bilagsnr.  |Varepostløbenr.  |Lokationskode  |Varepostmængde  |Faktureret antal  |Kostbeløb (faktisk)  |Kostbeløb (forventet)  |Regulering  |Udlign.postløbenr.  |Kildespor  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Salg     | Købspris   | 102033        |319     | Blå        | -1       |0         |  0       |     -10   |Nr.   |0    |Salg          |
|381     |  A       |    2020-09-06     |    Salg     | Købspris   | 103022        |319     | Blå        |  0       |-1        |-10       |    10     | Nr.  |0      |       Salg   |
|391     |  A       |    2020-09-10     |    Salg     | Købspris   | 103022        |319     | Blå        |  0       |0         |-1        |    0     |Ja   |    181   | INVTADJMT   |

Du kan tildele bogføringsdatoen for **Postnr. 391** ved at benytte følgende fremgangsmåde:

1. **Reguleringsværdiposten**, der skal oprettes (**Postnr. 391**), er knyttet til samme **bogføringsdato**, som den post, den justerer.

2. Kørslen **Juster kostpris - vareposter** bestemmer, om den første bogføringsdato for reguleringsværdiposten er inden for det tilladte bogføringsdatointerval, der er baseret på lagerperioder og/eller Opsætning af Finans.  

Lad os gennemgå ovennævnte salg ved at tilføje opsætningen af tilladte bogføringsdatointervaller.  
  
#### <a name="inventory-periods"></a><a name="inventory-periods"></a>Lagerperioder

|Afslutningsdato  |Name  |Lukket  |
|---------|---------|---------|
|2020-01-31     |2020. januar      |  Ja    |
|2020-02-28     |Februar 2020     |  Ja    |
|2020-03-31     |Marts 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Maj 2020        |  Ja    |
|2020-06-30     |Juni 2020       |  Ja    |
|2020-07-31     |Juli 2020        |  Ja    |
|2020-08-31     |August 2020     |  Ja    |
|2020-09-30     |September 2020  |         |
|2020-10-31     |Oktober 2020    |         |
|2020-11-30     |November 2020   |         |
|2020-12-31     |December 2020   |         |

Den første tilladte bogføringsdato er den første dag i den første åbne periode, som er 1. september 2020.  

#### <a name="general-ledger-setup"></a><a name="general-ledger-setup"></a>Opsætning af Finans

|Felt|Værdi  |
|---------|---------|
|Bogf. tilladt fra:  |  2020-09-10      |
|Bogf. tilladt til:    |  2020-09-30      |
|Registrer tid:       |         |
|Lokalt adresseformat:|   Postnr.      |  

Den første tilladte bogføringsdato er den dato, der er angivet i feltet **Tillad bogføring fra**: 10. september 2020. Hvis både lagerperioder og tilladte bogføringsdatoer i **Opsætning af Finans** er defineret, så er det den seneste dato af de to, der definerer det tilladte bogføringsdatointerval.  

**Tildeling af en tilladt bogføringsdato**  

Den oprindeligt tildelt bogføringsdato er 6. september, som vist i trin 1. Men i 2. trin identificerer kørslen Juster kostpris - vareposter, at den tidligst tilladte bogføringsdato er 10. september, og dermed tildeles 10. september til 10 reguleringsværdiposten (**Postnr. 391**) nedenfor.  


|Løbenr.  |Varenr.  |Bogføringsdato  |Vareposttype  |Postens type  |Bilagsnr.  |Varepostløbenr.  |Lokationskode  |Varepostmængde  |Faktureret antal  |Kostbeløb (faktisk)  |Kostbeløb (forventet)  |Regulering  |Udlign.postløbenr.  |Kildespor  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Salg     | Købspris   | 102033        |319     | Blå        | -1       |0         |  0       |     -10   |Nr.   |0    |Salg          |
|381     |  A       |    2020-09-06     |    Salg     | Købspris   | 103022        |319     | Blå        |  0       |-1        |-10       |    10     | Nr.  |0      |       Salg   |
|391     |  A       |    **2020-09-10**     |    Salg     | Købspris   | 103022        |319     | Blå        |  0       |0         |-1        |    0     |Ja   |    181   | INVTADJMT   |

## <a name="common-problems-with-the-adjust-cost---item-entries-batch-job"></a><a name="common-problems-with-the-adjust-cost---item-entries-batch-job"></a>Almindelige problemer med "Juster kostpris - vareposter"-kørsel

Der er to scenarier, som supportteamet ofte støder på for at garantere deres egne problemløsningsartikler.

### <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Fejlmeddelelse: "Bogføringsdatoen er ikke inden for intervallet af tilladte bogføringsdatoer..."

Hvis denne fejl opstår, skal du justere de datoer, hvor brugeren har tilladelse til at bogføre poster. Du kan finde flere oplysninger her [Fejlmeddelelse: "Bogføringsdatoen er ikke inden for intervallet af tilladte bogføringsdatoer"](design-details-inventory-adjustment-value-entry-allowed-posting-dates.md).

### <a name="posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><a name="posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Bogføringsdato på reguleringsværdipost og bogføringsdatoen på post, der forårsager reguleringen, f.eks. værdiregulering eller varegebyr

Du kan finde flere oplysninger her [Bogføringsdatoen for regulerings værdiposten sammenlignet med kildeposten](design-details-inventory-adjustment-value-entry-source-entry.md).

## <a name="see-also"></a><a name="see-also"></a>Se også

[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  
[Designoplysninger: Vareudligning](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
