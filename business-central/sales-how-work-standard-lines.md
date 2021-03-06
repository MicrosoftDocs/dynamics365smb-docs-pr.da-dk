---
title: Oprette standardlinjer til tilbagevendende salg og køb | Microsoft Docs
description: Du kan oprette salgslinjer og købslinjer, som du ofte bruger, og derefter indsætte dem i salgs- og købsdokumenter, som du kan hurtigt udfylde linjerne med standardoplysninger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 40af4b0010b46938a9ce53a12dd95f1b2a687cc9
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748165"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Oprette gentagne salgs- og købslinjer
Hvis du ofte har brug at oprette salgs- og købslinjer med næsten ens oplysninger, kan du oprette standardlinjer, som du derefter kan indsætte i tilbagevendende salgs- og købsdokumenter, f.eks. for tilbagevendende genbestillingsordrer.  

Følgende procedure viser, hvordan du arbejder med standardsalgslinjer på en salgsfaktura. Det fungerer på samme måde for alle andre salgsdokumenter og for alle købsdokumenter.  

## <a name="to-set-up-recurring-sales-lines"></a>Sådan opretter du gentagne salgslinjer

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Gentagne salgslinjer**, og vælg derefter det relaterede link.  
2. På siden **Gentagne salgslinjer** skal du vælge **Ny**.  
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. I oversigtspanelet **Linjer** skal du angive oplysninger i felterne for at forberede salgslinjer, der afspejler de standardlinjer, du forventer at bruge som tilbagevendende linjerne på salgsdokumenter.  

> [!NOTE]
> Du kan ikke definere priser på gentagne salgslinjer, fordi priser, rabatter osv. beregnes ud fra de faktiske salgsdokumenter, når du har indsat de gentagne salgslinjer.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="to-assign-recurring-sales-lines-to-a-customer"></a>Sådan tildeles en gentagne salgslinjer til en debitor

Tildele en eller flere gentagne salgslinjer til en debitor, så de kan indsættes i salgsdokumenter for den pågældende debitor.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn jobkortet for den relevante debitor.
3. Vælg handlingen **Tilbagevendende salgslinjer**.
4. På siden **Tilbagevendende salgslinjer** skal du vælge koder for de gentagne salgslinjer, som du vil kunne indsætte i salgsdokumenter for kunden.
5. Udfyld de ekstra felter for at definere, hvornår, hvordan og hvor de gentagne salgslinjer skal bruges.  

    Hvis du vil bruge de tilbagevendende salgslinjer, der er indstillet, sammen med kørslen **Opret tilbagevendende salgsfakturaer**, skal du også udfylde felterne **Datoen Gyldig fra** og **Datoen Gyldig til** for at begrænse, hvornår tilbagevendende salgslinjer bruges til oprettelse af fakturaer. Du kan finde flere oplysninger i [Sådan opretter du flere salgsfakturaer baseret på standardsalgslinjer](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-recurring-sales-lines).

    Du kan også angive en Direct Debit-betalingsform og Direct Debit-betalingsaftale. Salgsfakturaer, der er oprettet med kørslen **Opret tilbagevendende salgsfakturaer**, vil derefter indeholde oplysninger, der skal bruges til at opkræve betaling for salgsfakturaer med SEPA-Direct Debit. Du kan finde flere oplysninger i [Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).

6. I de fire felter hvor du vælger, hvordan linjerne indsættes på fire dokumenttyper, skal du vælge en af følgende indstillinger:

|Indstilling|Beskrivelse|
|------|-----------|
|**Manuelt**|Du skal manuelt søge efter og indsætte en gentaget salgslinje, som findes for debitoren.|
|**Automatisk**|Hvis der findes flere gentagne salgslinjer for debitoren, får du en notifikation om, hvorfra du kan vælge den, der skal indsættes. Hvis der kun findes én gentagen salgslinje, indsættes den automatisk.<br /><br />Bemærk, at dette kun fungerer, hvis det nye dokument blev oprettet fra en bilagsliste, f.eks. ved at vælge handlingen **Ny** på siden **Salgsordrer**. Det fungerer ikke, hvis dokumentet blev oprettet på f.eks. et debitorkort.|
|**Spørg altid**|Der vises en meddelelse, og alle eksisterende tilbagevendende salgslinjer vises, så du kan vælge én af dem.

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Sådan indsættes tilbagevendende salgslinjer i en salgsfaktura

Hvis der findes gentagne salgslinjerne for debitoren, kan du indsætte dem eller få dem indsat i alle typer salgsdokumenter, f.eks. en salgsfaktura. Hvis du har aktiveret indstillingen **Spørg altid** , får du besked, hvis der findes gentagne salgslinjer.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fakturaer**, og vælg derefter det relaterede link.
2. Åbn den salgsfaktura, som du vil indsætte en eller flere standardsalgslinjer i.
3. Vælg handlingen **Hent tilbagevendende salgslinjer**.
4. På siden **Tilbagevendende salgslinjer** skal du vælge på opslagsknappen i feltet **Kode** og derefter vælge en række standardsalgslinjer.
5. Vælg knappen **OK** for at indsætte standardsalgslinjerne på fakturaen, hvor du kan genbruge dem eller redigere oplysningerne.

## <a name="to-create-multiple-sales-invoices-based-on-recurring-sales-lines"></a>Sådan opretter du flere salgsfakturaer baseret på tilbagevendende salgslinjer
Du kan bruge kørslen **Opret tilbagevendende salgsfakturaer** til at oprette salgsfakturaer i overensstemmelse med standardsalgslinjer, som er knyttet til kunderne og med bogføringsdatoer inden for de gyldige fra- og til-datoer, som du angiver i standardsalgslinjerne.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opret tilbagevendende salgsfakturaer**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov på siden **Opret tilbagevendende salgsfakturaer**.
3. I filterfeltet **Kode** skal du angive den kode for standardsalgslinjer, der er knyttet til en debitor, som du vil oprette salgsfakturaer for.
4. Vælg knappen **OK**.

Salgsfakturaer oprettes for kunder med den angivne standarddebitorsalgskode og eventuelle angivne oplysninger om direkte debitering for bogføring på den angivne dato.

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]