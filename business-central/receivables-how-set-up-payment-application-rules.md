---
title: Bruge automatisk udligning til at afstemme betalinger | Microsoft Docs
description: Gå til siden Regler for betalingsudligning, og konfigurer regler til at styre, hvordan betalinger/banktransaktioner skal udlignes automatisk til deres relaterede åbne poster, når du bruger funktionen Udlign automatisk på siden Betalingsudligningskladde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 64756cdc1a95cc0bb866fa4b7f87ecea0f1282ff
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191927"
---
# <a name="set-up-rules-for-automatic-application-of-payments"></a>Konfigurere regler for automatisk udligning af betalinger
På siden **Regler for betalingsudligning** skal du konfigurere regler, der styrer, hvordan betalingstekst (på en banktransaktion) automatisk matches med tekst på åbne poster i følgende to processer:
- Udlign automatisk betalinger til deres relaterede åbne (ubetalte) fakturaer, kreditnotaer eller andre poster, når du bruger funktionen **Udlign automatisk** på siden **Betalingsudligningskladde**. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).

- Afstem automatisk banktransaktioner med deres relaterede interne bankkontoposter, når du vælger handlingen **Afstem automatisk** på siden **Bankkontoafstemning.** Du kan finde flere oplysninger i [Afstemme bankkonti](bank-how-reconcile-bank-accounts-separately.md).

Du kan oprette nye regler for betalingsudligning ved at vælge, hvilke typer data på en betalingsafstemningskladde, der skal matche data på en eller flere åbne poster, før den tilhørende betaling udlignes automatisk på de åbne poster. Kvaliteten af hver automatisk udligning vises som en værdi af **Lav** til **Høj** i feltet **Matchtillid** på siden **Betalingsudligningskladde** ifølge den betalingsudligningsregel, der blev anvendt.

Hver række på siden **Regler for betalingsudligning** repræsenterer en betalingsudligningsregel. Regler anvendes i den rækkefølge, der er angivet af feltet **Sorteringsrækkefølge**. Hvis flere regler bruges samtidig, bruges den højeste sorterede regels udligningstillid.

Den automatiske udligningsfunktion er baseret på prioriterede afstemningskriterier. Funktionen prøver først, i prioriteret rækkefølge, at matche teksten i de fem **Relateret part**-felter på en kladdelinje med tekst på bankkontoen, navnet eller adressen på debitorer eller kreditorer med ubetalte dokumenter, der repræsenterer åbne poster. Derefter forsøger funktionen at matche tekst i felterne **Transaktionstekst** og **Flere transaktionsoplysninger** på en kladdelinje med tekst i felterne **Eksternt bilagsnr.** og **Bilagsnr.** på åbne poster. Endelig forsøger funktionen at finde beløbet i feltet **Kontoudtogsbeløb** på en kladdelinje med beløbet på åbne poster.

> [!NOTE]
> Tekstmatchning er kun muligt for tekst, der er længere end fire tegn.

Udover afstemningskriterierne gælder følgende vedrørende fortegnet foran det indbetalte beløb:

- I forbindelse med negative beløb foretages først en afstemning mod åbne poster, der repræsenterer debitorfakturaer, og derefter mod kreditnotaer for kreditorer.
- I forbindelse med positive beløb foretages først en afstemning mod åbne poster, der repræsenterer kreditorfakturaer, og derefter mod kreditnotaer for debitorer.

## <a name="to-set-up-a-payment-application-rule"></a>Sådan opretter du en udligningsregel for betaling
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Regler for betalingsudligning**, og vælg derefter det relaterede link.
2. Definer en ny eller redigeret regel for betalingsudligning ved at udfylde felterne på en linje, som beskrevet i følgende tabel.

|Felt|Description|
|-|-|
|**Matchtillid**|Angiver din tillid til udligningsreglen, du definerer på linjen. <br /></br>En værdi, du angiver i dette felt, vises i feltet i vinduet **Matchtillid** på siden **Betalingsudligningskladde** i henhold til kvaliteten af det automatiske betalingsprogram på kladdelinjen.|
|**Prioritet**|Angiver prioriteten af udligningsreglen i forhold til andre udligningsregler, der er defineret som linjer på siden **Regler for betalingsudligning**. 1 repræsenterer den højeste prioritet.|
|**Relateret part er matchet**|Angiver, hvor mange oplysninger om debitoren eller kreditoren, f.eks. adresse, bynavn og bankkontonummer, på kladdelinjen for betalingsafstemning, der skal matche oplysninger om den åbne post, før udligningsreglen bruges til automatisk at udligne betalingen til den åbne post.|
|**Bilagsnr./Eksternt bilagsnr. er matchet**|Angiver, om teksten på betalingsudligningskladde skal stemme overens med værdien i feltet **Bilagsnr.** eller **Eksternt bilagsnr.** på den åbne post, før udligningsreglen udligner betalingen med den åbne post.|
|**Matchende beløb inkl. tolerance**|Angiver, hvor mange poster for en debitor eller kreditor skal svare til beløbet, herunder betalingstolerance, før udligningsreglen skal bruges til automatisk at udligne en betaling til den åbne post.|

Følgende tabel viser, hvilke betalingsudligningsregler, der er angivet i den generelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Important]
> Betalingsudligningsregler kan være anderledes i din implementering af [!INCLUDE[d365fin](includes/d365fin_md.md)].

| Matchtillid | Prioritet | Relateret part er matchet | Bilagsnr./Eksternt bilagsnr. Matchet | Matchende beløb inkl. tolerance |
|------------------|----------|-----------------------|--------------------------------|--------------------------------|
| Høj             | 1        | Fuldt ud                 | Ja - flere                 | En afstemning                      |
| Høj             | 2        | Fuldt ud                 | Ja - flere                 | Flere afstemninger               |
| Høj             | 3        | Fuldt ud                 | Ja                            | En afstemning                      |
| Høj             | 4        | Fuldt ud                 | Ja                            | Flere afstemninger               |
| Høj             | 5        | Delvist             | Ja - flere                 | En afstemning                      |
| Høj             | 6        | Delvist             | Ja - flere                 | Flere afstemninger               |
| Høj             | 7        | Delvist             | Ja                            | En afstemning                      |
| Høj             | 8        | Fuldt ud                 | Nej                             | En afstemning                      |
| Høj             | 9        | Nej                    | Ja - flere                 | En afstemning                      |
| Høj             | 10       | Nej                    | Ja - flere                 | Flere afstemninger               |
| Mellem           | 1        | Fuldt ud                 | Ja - flere                 | Ikke i betragtning                 |
| Mellem           | 2        | Fuldt ud                 | Ja                            | Ikke i betragtning                 |
| Mellem           | 3        | Fuldt ud                 | Nej                             | Flere afstemninger               |
| Mellem           | 4        | Delvist             | Ja - flere                 | Ikke i betragtning                 |
| Mellem           | 5        | Delvist             | Ja                            | Ikke i betragtning                 |
| Mellem           | 6        | Nej                    | Ja                            | En afstemning                      |
| Mellem           | 7        | Nej                    | Ja - flere                   | Ikke i betragtning                 |
| Mellem           | 8        | Delvist             | Nej                             | En afstemning                      |
| Mellem           | 9        | Nej                    | Ja                            | Ikke i betragtning                 |
| Lav              | 1        | Fuldt ud                 | Nej                             | Ingen afstemninger                     |
| Lav              | 2        | Delvist             | Nej                             | Flere afstemninger               |
| Lav              | 3        | Delvist             | Nej                             | Ingen afstemninger                     |
| Lav              | 4        | Nej                    | Nej                             | En afstemning                      |
| Lav              | 5        | Nej                    | Nej                             | Flere afstemninger               |

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/reconciliation-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
