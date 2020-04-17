---
title: Bogføre koncerninterne dokumenter og kladder | Microsoft Docs
description: Bruge Intercompany-dokumenter til at bogføre transaktioner med dine Intercompany-partnere.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 55f7e0f58634ad56d88d6e826f42eafdc92c6a6a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182416"
---
# <a name="work-with-intercompany-documents-and-journals"></a>Arbejde med koncerninterne dokumenter og kladder
Du bruger koncerninterne dokumenter eller kladder til at bogføre transaktioner med koncerninterne partnere. Når du bogfører et koncerninternt dokument eller koncernintern kladde i regnskabet, oprettes der et tilsvarende dokument eller en tilsvarende kladde i din koncerninterne udbakke, som du kan overføre til partneren. Din partner kan derefter bogføre den tilsvarende transaktion direkte i sit eget regnskab uden at skulle indtaste oplysningerne igen.

For salgs- og købsdokumenter sikrer den koncerninterne partnerkode på den involverede debitor eller kreditor, at alle ordrer og fakturaer, der oprettes på baggrund af transaktioner med disse virksomheder, vil resultere i tilsvarende dokumenter i partnervirksomheden, hvilket resulterer i korrekt afstemning af kontiene.

For koncerninterne finanskladdelinjer behøver du ikke at angive kontiene for et individuelt sæt af profiler, men blot oplyse partnervirksomhedens id. Der oprettes derefter koncerninterne finanskladdelinjer i partnervirksomheden, som resulterer i afstemning af profilerne i de to virksomheder, der er involveret i en transaktion.

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a>Sådan udfyldes og sendes en IC-salgsordre
Du kan sende salgs- og købsordrer og returordrer, før du bogfører dem. Fakturaer og kreditnotaer kan ikke sendes, før de er blevet bogført.

Den følgende procedure beskriver, hvordan du udfylder og sender en IC-salgsordre. Samme fremgangsmåde anvendes på koncerninterne købsordrer og returordrer og bogførte IC-fakturaer og kreditnotaer.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.  
2. Vælg **Ny** for at oprette en ny salgsordre. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Sørg for, at debitoren er en koncernintern partner.
5. Hvis du vil sende salgsordren, før du bogfører den, skal du vælge handlingen **Send IC-salgsordre**.

> [!NOTE]
> Hvis du udfører trin 4, flyttes salgsordren derefter til din koncerninterne udbakke, hvor kan du sende den senere. Du kan finde flere oplysninger i [Administrere IC-indbakken og -udbakken](intercompany-how-manage-intercompany-inbox.md).

## <a name="to-fill-in-and-post-an-intercompany-journal"></a>Sådan udfyldes og bogføres en IC-kladde
Når du bogfører en koncernintern finanskladdelinje i regnskabet, oprettes der en tilsvarende finanskladdelinje i din koncerninterne udbakke, som du kan overføre til partneren. Din partner kan derefter bogføre den tilsvarende transaktion direkte i sit eget regnskab uden at skulle indtaste oplysningerne igen.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Koncerninterne finanskladder**, og vælg derefter det relaterede link.  
2. Åbn det relevante kladdenavn. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).
3. Udfyld felterne efter behov.
4. I feltet **IC-partner finanskontonr.** skal du angive den koncerninterne finanskonto , som beløbet skal bogføres til i partnerens virksomhed.

    > [!NOTE]
    > Feltet kan kun udfyldes på en linje med en bankkonto eller finanskonto i feltet **Kontonr.** eller **Modkonto**.  
5. Vælg handlingen **Bogfør**.

De involverede poster bogføres i regnskabet, og der oprettes en kladde med de tilsvarende poster i din koncerninterne udbakke, som du kan sende til din partnervirksomhed. Du kan finde flere oplysninger i [Administrere IC-indbakken og -udbakken](intercompany-how-manage-intercompany-inbox.md).

## <a name="see-also"></a>Se også
[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
