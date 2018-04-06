---
title: "Sådan oprettes placeringsindhold | Microsoft Docs"
description: "Når du har oprettet placeringerne, kan du oprette placeringsindholdet. Du kan med andre ord sætte de varer op, som du vil opbevare på en bestemt placering, og angive regler, der styrer anbringelse af en bestemt vare på placeringen."
services: project-madeira
documentationcenter: 
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
ms.openlocfilehash: ec7a0c7c34e164b6ca6c8e65938a8c5e53e65514
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-bin-contents"></a>Oprette placeringsindhold
Når du har oprettet placeringerne, kan du oprette placeringsindholdet. Du kan med andre ord sætte de varer op, som du vil opbevare på en bestemt placering, og angive regler, der styrer anbringelse af en bestemt vare på placeringen. Du kan gøre dette manuelt i vinduet **Placeringsindhold** eller automatisk med vinduet **Opret placeringsindholdskladde**.

## <a name="to-create-bin-content-manually"></a>Sådan oprettes placeringsindhold manuelt  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg derefter det relaterede link.  
2.  Marker den lokation, hvor du vil konfigurere placeringsindhold, og vælg derefter handlingen **Placeringer**.  
3.  Marker den placering, hvor du vil konfigurere indholdet, og vælg derefter handlingen **Indhold**.  
4.  For hvert element, du vil gemme i placeringen, skal du udfylde en linje i vinduet **Placeringsindhold** med de relevante oplysninger. Nogle felter er allerede udfyldt med oplysninger om placeringen.  
5.  Udfyld først feltet **Varenr.**, og – hvis du bruger styret læg-på-lager og pluk – udfyld derefter de andre felter som f.eks. feltet **Enhedskode**, felterne **Maks. antal** og **Min. antal**.  

Vælg feltet **Fast**, hvis det er nødvendigt. Hvis placeringen skal fungere som standardplacering for varen, skal du markere feltet **Standardplacering**.  

Hvis du bruger styret læg-på-lager og pluk, og du har angivet de korrekte dimensionsoplysninger for hver vares måleenhed, kontrolleres det maksimale antal, du har angivet i vinduet **Placeringsindhold**, i forhold til placeringens fysiske kapacitet. Herefter benyttes minimums- og maksimumsantallet, når der beregnes genopfyldning, og der foreslås læg-på-lager-aktiviteter.  

Hvis du markerer feltet **Fast**, knytter du permanent varen til placeringen, hvilket betyder, at [!INCLUDE[d365fin](includes/d365fin_md.md)] altid vil forsøge at lægge den pågældende vare på placeringen, hvis der er plads til den, og at registreringen af tilknytningen bevares, selvom det aktuelle antal på placeringen er 0. Der kan anbringes andre varer på placeringen, selvom en bestemt vare er fast tilknyttet placeringen.  

> [!NOTE]  
>  Du kan oprette flere placeringsindhold ad gangen i vinduet **Opr.kladde til placeringsindh.**.  

## <a name="to-create-bin-content-with-a-worksheet"></a>Sådan oprettes placeringsindhold med en kladde  
Når du har oprettet placeringer, kan du angive, hvilke varer der skal opbevares på hver placering vha. en kladde.

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opr.kladde til placeringsindh.**, og vælg derefter det relaterede link.  
2.  Klik i feltet **Navn** i kladdehovedet, og vælg kladden for den lokation, hvor du vil oprette placeringsindhold.  
3.  Vælg koden for den placering, hvis indhold du vil definere, i feltet **Placeringskode**.   

    Hvis du bruger styret læg-på-lager og pluk på denne lokation, udfyldes de felter, der vedrører den pågældende placering, automatisk, f.eks. **Placeringstype**, **Lagerklassekode** og **Placeringsniveau**. Det er oplysninger, du skal overveje, når du definerer placeringsindholdet.  
4.  Vælg den vare, der skal knyttes til placeringen, og udfyld felterne vedrørende placeringsindhold. Udfyld felterne **Maks. antal** og **Min. antal**, hvis du bruger styret læg-på-lager og pluk, og du planlægger at bruge funktionen **Beregn placeringsgenopfyldning**.  

    Hvis du vil angive denne placering som den foretrukne placering for varen, selvom det placeringsantallet er **0**, og alle andre læg-på-lager-kriterier er de samme, skal du vælge feltet **Fast**.  
5.  Gentag trin 3-4 for hver vare, du vil tildele til en placering.  
6.  Vælg handlingen **Udskriv** for at få vist og udskrive det placeringsindhold, du har angivet i kladden. Fortsæt med at redigere placeringsindholdet, indtil du er tilfreds.  
7.  Når du er klar, skal du vælge handlingen **Opret placeringsindhold**.  

I denne kladde kan du arbejde med placeringsindholdslinjer for flere placeringer ad gangen og på den måde få et godt overblik over, hvilke varer der lægges på de forskellige placeringer i en given zone, række eller hylde.  

## <a name="see-also"></a>Se også
[Beregn genopfyldning](warehouse-how-to-calculate-bin-replenishment.md)    
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

