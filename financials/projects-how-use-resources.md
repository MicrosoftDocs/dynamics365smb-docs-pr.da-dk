---
title: Registrere og regulere ressourceforbrug og priser | Microsoft Docs
description: "Beskriver, hvordan du kan registrere ressourceforbrug eller forbrug, der er knyttet til en sag, for at holde styr på og styre omkostninger, priser, og arbejdstyper."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: f110f4cc342f5284e3da2641d56dc13f67c3773a
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-use-resources-for-jobs"></a>Fremgangsmåde: Bruge ressourcer for sager
Du registrerer forbruget af ressourcer i jobkladden, for at holde styr på omkostninger, priser og de arbejdstyper, der er knyttet til sagerne. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere Registrere forbrug for sager](projects-how-record-job-usage.md).

Du kan også bogføre forbruget af en ressource i en ressourcekladde. Posteringer i en ressourcekladde har ingen indflydelse på finanskontiene.

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Suite**. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="to-assign-resources-to-jobs"></a>Sådan tildeles ressourcer til sager
Du kan tildele ressourcer til sager ved at oprette sagsplanlægningslinjer for sagen. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette sager](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Sådan registreres ressourceforbrug for en sag
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sagskladder**, og vælg derefter det relaterede link.
2. Åbn en relevante sagskladde, og udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Når kladden er fuldført, skal du vælge handlingen **Bogfør**.

## <a name="to-adjust-resource-prices"></a>Sådan reguleres ressourcepriser
Hvis du vil ændre kost- eller salgspriser for et større antal ressourcer, kan du anvende en kørsel.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Reguler ressourcepriser**, og vælg derefter det relaterede link.
2. Udfyld felterne på linjen efter behov, og vælg derefter knappen **OK**.

> [!NOTE]  
>   Denne kørsel kan ikke bruges til at ændre eller oprette alternative salgs- eller købspriser for ressourcer. Den ændrer kun indholdet af feltet på ressourcekortet for feltet **Reguler felt**, som du har markeret i kørslen. Reguleringen træder i kraft med det samme for ressourcen, så du bør kontrollere reguleringsfaktorerne før kørslen.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Sådan hentes forslag til ændring af ressourcepriser ud fra eksisterende alternative priser
Hvis du allerede har angivet en alternativ ressourcepris for nogle ressourcer, kan du bruge en kørsel til at angive flere alternative ressourcepriser.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourceprisforslag**, og vælg derefter det relaterede link.
2. Vælg handlingen **Foreslå ress.salgspris (pris)**, og udfyld derefter felterne efter behov.
3. Vælg knappen **OK**.  
4. Vinduet **Ressourceprisforslag** viser resultatet af kørslen, når den er færdig.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Sådan henter du forslag til ændring af ressourcepriser ud fra standardpriser
Hvis du vil angive flere alternative ressourcepriser ud fra standardpriserne på ressourcekortet, kan du anvende en kørsel.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourceprisforslag**, og vælg derefter det relaterede link.
2. Vælg handlingen **Foreslå ress.salgspris (ress.)**, og udfyld derefter felterne efter behov.  
3. Vælg knappen **OK**.  
4. Åbn vinduet **Ressourceprisforslag** for at se resultatet af kørslen, når den er færdig.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Sådan henter du forslag til ændring af ressourcepriser ud fra standardpriser
Hvis du allerede har angivet en alternativ ressourcepris for nogle ressourcer, kan du bruge en kørsel til at angive flere alternative ressourcepriser.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Foreslå ress.salgs&pris (ress.)**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.
3. Vælg knappen **OK**.  
4. Åbn vinduet **Ressourceprisforslag** for at se resultatet af kørslen, når den er færdig.

## <a name="see-also"></a>Se også
[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)     
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

