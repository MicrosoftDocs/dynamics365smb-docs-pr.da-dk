---
title: "Oprette standardlinjer til tilbagevendende salg og køb | Microsoft Docs"
description: "Du kan oprette salgslinjer og købslinjer, som du ofte bruger, og derefter indsætte dem i salgs- og købsdokumenter, som du kan hurtigt udfylde linjerne med standardoplysninger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: df4f093ded0a55d45c40be15c5888035d6e3b2df
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a>Oprette gentagne salgs- og købslinjer
Hvis du ofte har brug at oprette salgs- og købslinjer med næsten ens oplysninger, kan du oprette standardlinjer, som du derefter kan indsætte i tilbagevendende salgs- og købsdokumenter, f.eks. for tilbagevendende genbestillingsordrer.  

Følgende procedure viser, hvordan du arbejder med standardsalgslinjer. Det fungerer på samme måde for standardkøbslinjer.  

## <a name="to-set-up-standard-sales-lines"></a>Sådan opretter du standardsalgslinjer  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Standardsalgslinjer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** i vinduet **Standardsalgslinjer**.  
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. I oversigtspanelet **Linjer** skal du angive oplysninger i felterne for at forberede salgslinjer, der afspejler de standardlinjer, du forventer at bruge som tilbagevendende linjerne på salgsdokumenter.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Sådan indsættes standardsalgslinjer i en salgsfaktura
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fakturaer**, og vælg derefter det relaterede link.
2. Åbn den salgsfaktura, som du vil indsætte en eller flere standardsalgslinjer i.
3. Vælg handlingen **Hent tilbagevendende salgslinjer**.
4. I vinduet **Tilbagevendende salgslinjer** skal du vælge på opslagsknappen i feltet **Kode** og derefter vælge en række standardsalgslinjer.

    > [!NOTE]
    > For at bruge de tilbagevendende salgslinjer, der er indstillet, sammen med kørslen **Opret tilbagevendende salgsfakturaer**, skal du også udfylde felterne **Datoen Gyldig fra** og **Datoen Gyldig til** i vinduet **Tilbagevendende salgslinjer**. Du kan finde flere oplysninger i "Sådan opretter du flere salgsfakturaer baseret på standardsalgslinjer".

5. Vælg knappen **OK** for at indsætte standardsalgslinjerne på fakturaen, hvor du kan genbruge dem eller redigere oplysningerne.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Sådan opretter du flere salgsfakturaer baseret på standardsalgslinjer
Du kan bruge kørslen **Opret tilbagevendende salgsfakturaer** til at oprette salgsfakturaer i overensstemmelse med standardsalgslinjer, som er knyttet til kunderne og med bogføringsdatoer inden for de gyldige fra- og til-datoer, som du angiver i standardsalgslinjerne.

> [!NOTE]
> I vinduet **Tilbagevendende salgslinjer** kan du også angive en Direct Debit-betalingsform og Direct Debit-betalingsaftale. Salgsfakturaer, der er oprettet med kørslen **Opret tilbagevendende salgsfaktura**, vil derefter indeholde oplysninger, der skal bruges til at opkræve betaling for salgsfakturaer med SEPA-Direct Debit. Du kan finde flere oplysninger i [Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opret tilbagevendende salgsfakturaer**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov i vinduet **Opret tilbagevendende salgsfakturaer**.
3. I filterfeltet **Kode** skal du angive den kode for standardsalgslinjer, der er knyttet til en debitor, som du vil oprette salgsfakturaer for.
4. Vælg knappen **OK**.

Salgsfakturaer oprettes for kunder med den angivne standarddebitorsalgskode og eventuelle angivne oplysninger om direkte debitering for bogføring på den angivne dato.

## <a name="see-also"></a>Se også  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

