---
title: "Opsætning af urealiseret moms | Microsoft Docs"
description: "Hvis du bruger bogføring, der er baseret på kontanter, kan du angive, hvordan urealiseret moms for salg og køb skal håndteres."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 09/08/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 79851c90a2a2fd8ac2e744173a04b7eda50b98e8
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-unrealized-vat-for-cash-based-accounting"></a>Fremgangsmåde: Konfigurere urealiseret moms i forbindelse med bogføring baseret på kontanter
Hvis du bruger bogføringsmetoder, der er baseret på kontanter, kan du konfigurere [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] til at håndtere urealiseret moms.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Sådan bruges finanskonti for urealiseret moms
Du kan vælge, at momsbeløb beregnes og bogføres til en midlertidig finanskonto, når en faktura bogføres. Når den faktiske betaling af fakturaen bogføres, kan momsbeløbet så bogføres til den korrekte finanskonto og medtages i momsangivelsen. Du skal først færdiggøre momsbogføringsopsætning.

Når du vil bruge konti for urealiseret moms, skal du gøre følgende:
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Opsætning af Finans**. 
2. På siden **Opsætning af Finans** i oversigtspanelet **Generelt** skal du vælge **Vis mere** og derefter markere afkrydsningsfeltet **Urealiseret moms**.
3. Luk siden.
4. Vælg ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") og angive **Opsætning af momsbogføring**. 
5. På siden **Opsætning af momsbogføring** skal du vælge momsbogføringsgruppen og derefter vælge **Rediger**. 
6. I feltet **Urealiseret moms - type** skal du vælge en indstilling for at angive, hvordan betalinger skal tildeles til fakturabeløbet (uden moms) og selve momsbeløbet, og hvordan momsbeløb skal overføres fra den urealiserede momskonto til den realiserede momskonto. Den følgende tabel beskriver indstillingerne.

| Indstilling | Beskrivelse |
| --- | --- |
| Tom | Vælg denne indstilling, hvis du ikke vil bruge funktionen for urealiseret moms. |
| Procent | Betalinger dækker både moms og fakturabeløbet i forhold til den procentmæssige andel af det samlede fakturabeløb. Det betalte momsbeløb overføres fra den urealiserede momskonto til den realiserede momskonto. |
| Første | Betalingerne dækker først moms og derefter fakturabeløb. I dette tilfælde svarer beløbet, der overføres fra kontoen for urealiseret moms til momskontoen, til betalingsbeløbet, indtil hele momsbeløbet er betalt. |
| Sidste | Betalingerne dækker fakturabeløbet først moms og derefter moms. I dette tilfælde overføres intet beløb fra kontoen for urealiseret moms til momskontoen, før hele fakturabeløbet eksklusive moms er betalt. |
| Først (betalt) | Betalingerne skal først dække momsbeløbet (som ved indstillingen _Først_), men der overføres ikke noget beløb til momskontoen, før det fulde momsbeløb er betalt. |
| Sidst (betalt) | Betalingerne skal først dække fakturabeløbet (som ved indstillingen _Sidst_), men der overføres ikke noget beløb til momskontoen, før det fulde momsbeløb er betalt. |

6. I feltet **Urealiseret salgsmomskonto** skal du vælge finanskontoen for urealiseret salgsmoms.

    > [!NOTE]  
>   Momsbeløbet bogføres på denne konto og bliver stående der, indtil debitors indbetaling er bogført. Derefter overføres beløbet til finanskontoen for salgsmoms.
7. Angiv finanskontoen for urealiseret købsmoms i feltet **Urealiseret købsmomskonto**.

    > [!NOTE]  
>   Momsbeløbet bogføres på denne konto og bliver stående der, indtil debitors indbetaling er bogført. Derefter overføres beløbet til finanskontoen for salgsmoms.

## <a name="see-also"></a>Se også
[Opsætning af moms](finance-setup-vat.md)
