---
title: Håndtering af manglende indstillingsværdier
description: Få mere at vide om, hvordan du forhindrer, at fuld synkronisering mislykkes, fordi indstillingerne er forskellige i tilknyttede felter.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.openlocfilehash: 65911039894d1f0eb81aeb1160a6b2aafc2fae0c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752871"
---
# <a name="handling-missing-option-values"></a>Håndtering af manglende indstillingsværdier
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

[!INCLUDE[prod_short](includes/cds_long_md.md)]indeholder kun tre felter med grupperede indstillinger, der indeholder indstillingsværdier, som du kan knytte til [!INCLUDE[prod_short](includes/prod_short.md)]-felter af typen Indstilling<!-- Option type, not enum? @Onat can you vertify this? --> til automatisk synkronisering. Under synkroniseringen ignoreres ikke-tilknyttede indstillinger, og de manglende indstillinger vedhæftes til den relaterede [!INCLUDE[prod_short](includes/prod_short.md)]-tabel og føjes til systemtabellen **CDS-indstillingstilknytning**, så de kan håndteres manuelt senere. For eksempel ved at tilføje de manglende indstillinger i hvert produkt og derefter opdatere tilknytningen. Dette afsnit handler om, hvordan det fungerer.

Siden **Integrationstabeltilknytning** indeholder tre kort til felter, der indeholder en eller flere tilknyttede indstillingsværdier. Efter en fuld synkronisering indeholder siden **CDS-indstillingstilknytning** de ikke-tilknyttede indstillinger i de tre respektive felter.

|         Post             | Indstillingsværdi | Billedtekst til indstillingsværdi |
|----------------------------|--------------|----------------------|
| Betalingsbetingelser: NET30       | 1            | Netto 30               |
| Betalingsbetingelser: 2%10NET30   | 2            | 2 % 10: Netto 30        |
| Betalingsbetingelser: NET45       | 3            | Netto 45               |
| Betalingsbetingelser: NET60       | 4            | Netto 60               |
| Leveringsmetode: FOB       | 1            | FOB                  |
| Leveringsmetode: NOCHARGE  | 2            | Uden beregning            |
| Speditør: AIRBORNE   | 1            | Luftfragt             |
| Speditør: DHL        | 2            | DHL                  |
| Speditør: FEDEX      | 3            | FedEx                |
| Speditør: UPS        | 4            | UPS                  |
| Speditør: POSTALMAIL | 5            | Alm. post          |
| Speditør: FULLLOAD   | 6            | Fuld belastning            |
| Speditør: WILLCALL   | 7            | Vil ringe            |

Indholdet på siden **CDS-indstillingstilknytning** er baseret på fasttekstværdier i tabellen **CDS-konto**. I [!INCLUDE[prod_short](includes/cds_long_md.md)] er følgende felter på kontotabellen knyttet til felter i kunde- og leverandørposterne:

- **Adresse 1: Fragtbetingelser** for datatypen Fasttekst, hvor værdierne defineres som følger:

```
enum 5335 "CDS Shipment Method Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "FOB") { Caption = 'FOB'; }
    value(2; "NoCharge") { Caption = 'No Charge'; }
}
```

- **Adresse 1: Fragtmetode** for datatypen Fasttekst, hvor værdierne defineres som følger:

```
enum 5336 "CDS Shipping Agent Code"
enum 5336 "CDS Shipping Agent Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Airborne") { Caption = 'Airborne'; }
    value(2; "DHL") { Caption = 'DHL'; }
    value(3; "FedEx") { Caption = 'FedEx'; }
    value(4; "UPS") { Caption = 'UPS'; }
    value(5; "PostalMail") { Caption = 'Postal Mail'; }
    value(6; "FullLoad") { Caption = 'Full Load'; }
    value(7; "WillCall") { Caption = 'Will Call'; }
}
```

- **Betalingsbetingelser** for datatypen Fasttekst, hvor værdierne defineres som følger:

```
enum 5334 "CDS Payment Terms Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Net30") { Caption = 'Net 30'; }
    value(2; "2%10Net30") { Caption = '2% 10; Net 30'; }
    value(3; "Net45") { Caption = 'Net 45'; }
    value(4; "Net60") { Caption = 'Net 60'; }
}
```

Alle førnævnte [!INCLUDE[prod_short](includes/prod_short.md)]-fasttekster er knyttet til grupperede indstillinger i [!INCLUDE[prod_short](includes/cds_long_md.md)].

### <a name="extending-option-sets-in-prod_short"></a>Udvide grupperede indstillinger i [!INCLUDE[prod_short](includes/prod_short.md)]
1. Opret en ny AL-udvidelse.

2. Tilføj en Fasttekst-udvidelse for de indstillinger, du vil udvide. Sørg for at bruge samme værdi. 

```
enumextension 50100 "CDS Payment Terms Code Extension" extends "CDS Payment Terms Code"
{
    value(779800001; "Cash Payment") { Caption = 'Cash Payment'; }
    value(779800002; "Transfer") { Caption = 'Transfer'; }
}
```

> [!IMPORTANT]  
> Du skal bruge det samme indstillings-ID fra [!INCLUDE[prod_short](includes/cds_long_md.md)], når du udvider fastteksten [!INCLUDE[prod_short](includes/prod_short.md)]. Ellers mislykkes synkroniseringen.

> [!IMPORTANT]  
> Brug ikke tegnet "," i fasttekstværdier og billedtekster. Dette understøttes ikke i øjeblikket af [!INCLUDE[prod_short](includes/prod_short.md)]-kørslen.

> [!NOTE]
> De første ti tegn i den nye indstillingsværdi og billedteksterne skal være entydige. De to indstillinger med navnet "Overfør 20 arbejdsdage" og "Overfør 20 kalenderdage" vil for eksempel forårsage en fejl, fordi begge har de samme første ti tegn, "Overførsel 2". Du kan f.eks. kalde dem for "TRF20 WD" og "TRF20 CD".

### <a name="update-prod_short-option-mapping"></a>Opdater [!INCLUDE[prod_short](includes/cds_long_md.md)]-indstillingstilknytning
Nu kan du gendanne tilknytningen mellem [!INCLUDE[prod_short](includes/cds_long_md.md)]-indstillingerne og [!INCLUDE[prod_short](includes/prod_short.md)]-posterne.

På siden **Integrationstabeltilknytning** skal du vælge linjen for tilknytningen **Betalingsbetingelser** og vælge handlingen **Synkroniser ændrede records**. Siden **CDS-indstillingstilknytning** opdateres med de yderligere poster nedenfor.

|         Post                 | Indstillingsværdi   | Billedtekst til indstillingsværdi |
|--------------------------------|----------------|----------------------|
| Betalingsbetingelser: NET30           | 1              | Netto 30               |
| Betalingsbetingelser: 2%10NET30       | 2              | 2 % 10: Netto 30        |
| Betalingsbetingelser: NET45           | 3              | Netto 45               |
| Betalingsbetingelser: NET60           | 4              | Netto 60               | 
| **Betalingsbetingelser: CASH PAYME**  | **779800001**  | **Kontantbetaling**     |
| **Betalingsbetingelser: TRANSFER**    | **779800002**  | **Overførsel**         |

Tabellen **Betalingsbetingelser** i [!INCLUDE[prod_short](includes/prod_short.md)] vil herefter have nye poster for [!INCLUDE[prod_short](includes/cds_long_md.md)]-indstillingerne. I følgende tabel er de nye indstillinger angivet med fed skrift. Rækker med kursiv er alle indstillinger, der nu kan synkroniseres. De resterende rækker angiver indstillinger, der ikke anvendes, og de ignoreres under synkroniseringen. Du kan fjerne dem eller udvide CDS-indstillinger med de samme navne.)

| Kode       | Forfaldsdatoberegning | Kont.rabat datoform | Rabat % | Beregn kont.rabat på kred.notaer | Beskrivelse       |
|------------|----------------------|---------------------------|------------|-------------------------------|-------------------|
| 10 DAGE    | 10D                  |                           | 0.         | FALSK                         | Netto 10 dage       |
| 14 DAGE    | 14D                  |                           | 0.         | FALSK                         | Netto 14 dage       |
| 15 DAGE    | 15D                  |                           | 0.         | FALSK                         | Netto 15 dage       |
| 1M(8D)     | 1M                   | 8D                        | 2.         | FALSK                         | 1 måned/2 % 8 dage |
| 2 DAGE     | 2D                   |                           | 0.         | FALSK                         | Netto 2 dage        |
| *2%10NET30* |                      |                           | 0.         | FALSK                         |                   |
| 21 DAGE    | 21D                  |                           | 0.         | FALSK                         | Netto 21 dage       |
| 30 DAGE    | 30D                  |                           | 0.         | FALSK                         | Netto 30 dage       |
| 60 DAGE    | 60D                  |                           | 0.         | FALSK                         | Netto 60 dage       |
| 7 DAGE     | 7D                   |                           | 0.         | FALSK                         | Netto 7 dage        |
| ***KONTANT BETAL** _ |                      |                           | 0.         | FALSK                         |                   |
| LM         | LM                   |                           | 0.         | FALSK                         | Aktuel måned     |
| COD        | 0D                   |                           | 0.         | FALSK                         | Kontant ved levering  |
| _NET30*      |                      |                           | 0.         | FALSK                         |                   |
| *NET45*      |                      |                           | 0.         | FALSK                         |                   |
| *NET60*      |                      |                           | 0.         | FALSK                         |                   |
| ***OVERFØRSEL*** |                      |                           | 0.         | FALSK                         |                   |

## <a name="see-also"></a>Se også
[Tilknytning af tabeller og felter til synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]