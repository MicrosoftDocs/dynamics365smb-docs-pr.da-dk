---
title: Oprette standardlinjer til tilbagevendende salg og køb | Microsoft Docs
description: Du kan oprette salgslinjer og købslinjer, som du ofte bruger, og derefter indsætte dem i salgs- og købsdokumenter, som du kan hurtigt udfylde linjerne med standardoplysninger.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 04/24/2019
ms.author: sgroespe
ms.openlocfilehash: 83f6a24fc066faef49de456e18673f8059a9831d
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252247"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Oprette gentagne salgs- og købslinjer
Hvis du ofte har brug at oprette salgs- og købslinjer med næsten ens oplysninger, kan du oprette standardlinjer, som du derefter kan indsætte i tilbagevendende salgs- og købsdokumenter, f.eks. for tilbagevendende genbestillingsordrer.  

Følgende procedure viser, hvordan du arbejder med standardsalgslinjer på en salgsfaktura. Det fungerer på samme måde for alle andre salgsdokumenter og for alle købsdokumenter.  

## <a name="to-set-up-standard-sales-lines"></a>Sådan opretter du standardsalgslinjer  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Standardsalgslinjer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** på siden **Standardsalgslinjer**.  
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. I oversigtspanelet **Linjer** skal du angive oplysninger i felterne for at forberede salgslinjer, der afspejler de standardlinjer, du forventer at bruge som tilbagevendende linjerne på salgsdokumenter.  

> [!NOTE]
> Du kan ikke definere priser på standardsalgslinjer, fordi priser, rabatter osv. beregnes ud fra de faktiske salgsdokumenter, når du har indsat standardsalgslinjerne.

## <a name="to-assign-standard-sales-lines-to-a-customer"></a>Sådan tildeles en debitor standardsalgslinjer
Tildele en eller flere standardsalgslinjer til en debitor, så de kan indsættes i salgsdokumenter for den pågældende debitor.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn jobkortet for den relevante debitor.
3. Vælg handlingen **Tilbagevendende salgslinjer**.
4. På siden **Tilbagevendende salgslinjer** skal du vælge koder for de gentagne salgslinjer, som du vil kunne indsætte i salgsdokumenter for kunden.
5. Udfyld de ekstra felter for at definere, hvornår, hvordan og hvor de gentagne salgslinjer skal bruges.
6. I de fire felter hvor du vælger, hvordan linjerne indsættes på fire dokumenttyper, skal du vælge en af følgende indstillinger:

|Indstilling|Description|
|-|-|
|**Manuelt**|Du skal manuelt søge efter og indsætte en gentaget salgslinje, som findes for debitoren.|
|**Automatisk**|Hvis der findes flere gentagne salgslinjer for debitoren, får du en notifikation om, hvorfra du kan vælge den, der skal indsættes. Hvis der kun findes én gentagen salgslinje, indsættes den automatisk.|
|**Spørg altid**|Der vises en meddelelse, og alle eksisterende tilbagevendende salgslinjer vises, så du kan vælge én af dem.

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Sådan indsættes tilbagevendende salgslinjer i en salgsfaktura
Hvis der findes tilbagevendende salgslinjerne for debitoren, kan du indsætte dem i alle typer salgsdokumenter, f.eks. en salgsfaktura. Hvis du har aktiveret den pågældende meddelelse, får du besked, hvis der findes tilbagevendende salgslinjer.
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fakturaer**, og vælg derefter det relaterede link.
2. Åbn den salgsfaktura, som du vil indsætte en eller flere standardsalgslinjer i.
3. Vælg handlingen **Hent tilbagevendende salgslinjer**.
4. På siden **Tilbagevendende salgslinjer** skal du vælge på opslagsknappen i feltet **Kode** og derefter vælge en række standardsalgslinjer.

    > [!NOTE]
    > For at bruge de tilbagevendende salgslinjer, der er indstillet, sammen med kørslen **Opret tilbagevendende salgsfakturaer**, skal du også udfylde felterne **Datoen Gyldig fra** og **Datoen Gyldig til** på siden **Tilbagevendende salgslinjer**. Du kan finde flere oplysninger i [Sådan opretter du flere salgsfakturaer baseret på standardsalgslinjer](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-standard-sales-lines).

5. Vælg knappen **OK** for at indsætte standardsalgslinjerne på fakturaen, hvor du kan genbruge dem eller redigere oplysningerne.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Sådan opretter du flere salgsfakturaer baseret på standardsalgslinjer
Du kan bruge kørslen **Opret tilbagevendende salgsfakturaer** til at oprette salgsfakturaer i overensstemmelse med standardsalgslinjer, som er knyttet til kunderne og med bogføringsdatoer inden for de gyldige fra- og til-datoer, som du angiver i standardsalgslinjerne.

> [!NOTE]
> På siden **Tilbagevendende salgslinjer** kan du også angive en Direct Debit-betalingsform og Direct Debit-betalingsaftale. Salgsfakturaer, der er oprettet med kørslen **Opret tilbagevendende salgsfaktura**, vil derefter indeholde oplysninger, der skal bruges til at opkræve betaling for salgsfakturaer med SEPA-Direct Debit. Du kan finde flere oplysninger i [Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opret tilbagevendende salgsfakturaer**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov på siden **Opret tilbagevendende salgsfakturaer**.
3. I filterfeltet **Kode** skal du angive den kode for standardsalgslinjer, der er knyttet til en debitor, som du vil oprette salgsfakturaer for.
4. Vælg knappen **OK**.

Salgsfakturaer oprettes for kunder med den angivne standarddebitorsalgskode og eventuelle angivne oplysninger om direkte debitering for bogføring på den angivne dato.

## <a name="see-also"></a>Se også  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
