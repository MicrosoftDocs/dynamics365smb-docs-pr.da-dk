---
title: "Sådan oprettes serviceartikler | Microsoft Docs"
description: "Når du modtager en ikke-registreret vare til reparation, kan du registrere den som en serviceartikel."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2c9c7796b80d77d3a879ecf9ce2a8af26a0ca5aa
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-service-items"></a>Oprette serviceartikler
I [!INCLUDE[d365fin](includes/d365fin_md.md)] refererer termen "serviceartikel" til udstyr eller varer, der kræver service. Når du opretter en serviceordre, kan du angive de varer, der har brug for service. I ordren kan du knytte en serviceartikel til en vare på lageret eller en serviceartikelgruppe.    

Når du modtager en vare, der kræver service, kan du registrere den som en serviceartikel. Dette kan gøres på flere måder. Du kan f.eks. oprette en serviceartikel på siden **Serviceartikler** eller som en del af en anden proces, f.eks. når du arbejder med en serviceordre.   

## <a name="to-create-a-service-item"></a>Oprette en serviceartikel  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceartikler**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Sådan oprettes serviceartikler fra serviceordrer  
Når du modtager artikler, som du vil registrere som serviceartikler, kan du oprette dem som serviceartikler i vinduerne **Serviceordre** eller **Servicetilbud**.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceordrer**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Vælg handlingen **Opret serviceartikel**.  

    Der tildeles et nummer til serviceartiklen, og der oprettes et serviceartikelkort. Feltet **Serviceartikelnr.** udfyldes med nummeret på den nye serviceartikel.

## <a name="to-create-a-service-item-when-shipping-items"></a>Oprette en serviceartikel ved levering af varer  
Når du leverer varer enten ved at bogføre serviceordrer eller servicefakturaer, registreres de leverede varer automatisk som serviceartikler, hvis følgende betingelser er opfyldt. Varerne skal høre til en serviceartikelgruppe, hvor afkrydsningsfeltet **Opret serviceartikel** er markeret. Hvis varerne har serienumre registreret i vinduet Varesporingslinje, kopieres disse oplysninger automatisk til feltet **Serienr.** på serviceartikelkortet ved oprettelse af serviceartikler.  

Nedenstående fremgangsmåde viser, hvordan du kan oprette serviceartikler, når du leverer varer i serviceordrer.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceordrer**, og vælg derefter det relaterede link.  
2. Åbn den relevante serviceordre.  
3. Vælg handlingen **Bogfør** eller **Bogfør og udskriv**.  
4. Vælg handlingen **Lever** eller **Lever og fakturer**.  
5. Der oprettes automatisk serviceartikler for varerne i ordren, forudsat at disse hører til en serviceartikelgruppe, som du har defineret for at oprette serviceartikler. Hvis der er registreret specifikke serienumre i vinduet **Varesporingslinjer**, tildeles de til disse serviceartikler.  

> [!NOTE]  
>  Hvis en vare er en stykliste, og du har udfoldet styklisten, bliver styklistevarerne behandlet på samme måde som almindelige varer. Der oprettes serviceartikler baseret på samme betingelser for serviceartikelgruppe og eventuelt betingelser for serienummer. Hvis der oprettes en serviceartikel for en udfoldet styklistevare, som består af andre styklistekomponenter, oprettes disse varer desuden som serviceartikelkomponenter for den udfoldede styklisteartikel.  
>   
>  Hvis varen er en stykliste, og du ikke har udfoldet styklisten, oprettes der en serviceartikel til den på de samme betingelser for serviceartikelgruppen og eventuelt betingelsen for serienumre.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Sådan indsættes startgebyrer for serviceartikler
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceopgaver**, og vælg derefter det relaterede link.
2. Vælg handlingen **Varekladde**.
3. Vælg servicelinjen, og vælg derefter **Handlinger**, vælg **Funktioner**, og vælg derefter handlingen **Indsæt startgebyr**.  

    Der indsættes en servicelinje af typen **Omkostning** med startgebyr. Startgebyret gælder den valgte serviceartikel.

## <a name="see-also"></a>Se også  
[Konfigurere serviceartikler og serviceartikelkomponenter](service-how-setup-service-items.md)  
[Konfigurere Service](service-setup-service.md)  
[Service Management](service-service.md)  

