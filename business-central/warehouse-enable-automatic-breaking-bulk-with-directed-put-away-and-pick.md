---
title: Automatisk nedbrydning med styret læg-på-lager og pluk | Microsoft Docs
description: På lokationer, hvor der bruges styret læg-på-lager og pluk, kan du nedbryde større enheder til mindre enheder, når der oprettes lagerinstruktioner, som opfylder behovet for kildedokumenter, produktionsordrer eller interne pluk og læg-på-lager.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8d3ce697bb627bcc8acebc2392fe86b6af4b370b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759963"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Aktivere automatisk nedbrydning med styret læg-på-lager og pluk
På lokationer, hvor der bruges styret læg-på-lager og pluk, kan [!INCLUDE[prod_short](includes/prod_short.md)] i visse tilfælde foretage automatisk nedbrydning. Dermed nedbrydes større enheder til mindre enheder, når der oprettes lagerinstruktioner, som opfylder behovet for kildedokumenter, produktionsordrer eller interne pluk og læg-på-lager. Nedbrydning kan også betyde indsamling af mindre enheder, hvis det er nødvendigt for at efterkomme udgående anmodninger, ved at nedbryde den største enhed i kildedokumentet eller produktionsordren i mindre enheder, der er tilgængelig på lageret. -nedbrydninger som følger.   

## <a name="breakbulking-in-picks"></a>Nedbrydning under pluk  
Hvis du vil lagre varer i flere forskellige enheder og lader dem blive automatisk kombineret efter behov i plukprocessen, skal du markere feltet **Tillad nedbrydning** på lokationskortet.  

Når programmet skal fuldføre en opgave, leder det automatisk efter en vare fra samme enhed. Men hvis programmet ikke kan finde denne type vare, og du har markeret dette felt, foreslår programmet, at du nedbryder en stor enhed til den størrelse enhed, der er nødvendig.  

Hvis systemet kun kan finde mindre enheder, foreslår det, at du samler varerne for at opfylde antallet på leverance- eller produktionsordren. I praksis nedbryder det større enheder på kildedokumentet til mindre enheder, der kan plukkes.  

## <a name="breakbulking-in-put-aways"></a>Nedbrydning i læg-på-lager  
I lagerstedets læg-på-lager foreslår programmet automatisk at placere handlingslinjer i læg-på-lager-enheder, for eksempel stykker, selvom varerne leveres i en anden form for enhed.  

## <a name="breakbulking-in-movements"></a>Nedbrydning i bevægelse  
Programmet foretager også automatisk nedbrydning i genopfyldningsbevægelser, hvis feltet **Tillad nedbrydning** er markeret i oversigtspanelet **Indstillinger** på siden **Beregn placeringsgenopfyldning**.  

Du kan få vist resultaterne af konverteringsprocessen fra en enhed til en anden som midlertidige nedbrydningslinjer i læg-på-lager-, pluk- eller bevægelsesinstruktionerne.  

> [!NOTE]  
>  Hvis du markerer feltet **Angiv nedbrydningsfilter** i lagerinstruktionshovedet, skjuler programmet nedbrydningslinjer, hver gang en større enhed vil blive brugt fuldstændig. Hvis en palle f.eks. består af 12 stykker, og du skal bruge alle 12, anmoder plukket dig om at tage en palle og placere 12 stykker der. Hvis du på den anden side kun plukker ni stykker, skjules nedbrydningslinjerne ikke, selvom du har markeret feltet **Nedbrydningsfilter**, da de resterende tre stykker stadig skal placeres et sted på lagerstedet.  

> [!NOTE]  
>  Hvis enhederne skal fungere optimalt på lagerstedet – også i forbindelse med nedbrydningsfunktionen – bør du altid tilstræbe at:  
>   
> - indstille basisenheden for en vare til at være den mindste enhed, som du forventer at skulle håndtere under lagerprocessen.  
> - Indstil alternative enheder for varen som flere forekomster af basisenheden.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]