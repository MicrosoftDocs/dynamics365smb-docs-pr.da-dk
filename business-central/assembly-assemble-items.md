---
title: Montagestyring | Microsoft Docs
description: Støt virksomheder, som leverer produkter til deres kunder, ved at kombinere komponenter i enkle processer uden brug af produktionsfunktioner, men med funktioner til montage af varer, der kan integreres med eksisterende funktioner som salg, planlægning, reservationer og opbevaring.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3eb071a04f6bcb9d9ce02df79c5489e4e79aaf43
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307728"
---
# <a name="assembly-management"></a>Montagestyring
For at støtte virksomheder, som leverer produkter til deres kunder ved at kombinere komponenter i enkle processer uden brug af produktionsfunktioner, indeholder [!INCLUDE[d365fin](includes/d365fin_md.md)] funktioner til montage af varer, der kan integreres med eksisterende funktioner som salg, planlægning, reservationer og opbevaring.  

 Et montageelement er defineret som et salgbart element, der indeholder en montagestykliste. Du kan finde flere oplysninger under [Arbejde med styklister](inventory-how-work-BOMs.md).

 Montageordrer er interne ordrer, ligesom produktionsordrer, der bruges til at administrere montageprocessen og til at forbinde salgskravene med de involverede lageraktiviteter. Montageordrer adskiller sig fra andre ordretyper, da de omfatter både afgang og forbrug, når de bogføres. Montageordrehovedet fungerer på samme måde en salgsordrelinje, og montageordrelinjerne fungerer på samme måde som forbrugskladdelinjer.  

 For at støtte en for JIT-lagerstrategi og muligheden for at tilpasse produkter til debitorkrav, kan montageordrer automatisk oprettes og kædes sammen, så snart salgsordrelinjen er oprettet. Sammenkædningen mellem salgsbehovet og montageleveringen gør det muligt for salgsordrebehandleren at tilpasse montageelementet løbende, love leveringsdatoer ifølge komponenttilgængeligheden og bogføre afgang og levering af montageelementet direkte fra deres salgsordregrænseflade. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

 På en salgsordrelinje kan du sælge et antal, der er tilgængeligt, og som skal plukkes fra lageret sammen med et montage efter ordre-antal. Der findes visse regler for fordelingen af disse mængder for at sikre, at montage efter ordre-mængder har højere prioritet end lagerantal i delvis levering. Du kan finde flere oplysninger i afsnittet "Kombinationsscenarier" i [Om Montage til ordre og Montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

 Der findes specialfunktioner til styring af leveringen af montage efter ordre-mængder. Når en montage efter ordre-mængde er klar til at blive leveret, bogfører den ansvarlige lagermedarbejder et lagerpluk for de pågældende salgsordrelinjer. Dette opretter derefter en flytning (lager) for komponenterne, bogfører montageoutputtet og salgsordreleverancen. Du kan finde flere oplysninger i afsnittet "Håndtere montage til ordre-varer i Pluk (lager)" i [Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Få mere at vide om forskellen mellem at montere elementer korrekt, før levering af salgsordrer og montering af varer, der er bestemt til oplagring.|[Om montage til ordre og montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Udfyld felter på lokationskort og lageropsætning for at definere, hvordan varer strømmer til og fra montageafdelingen.|[Oprette grundlæggende lagersteder med handlingsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Tilpas et montageelement til en kundes anmodning under salgsprocessen, og konverter til et salg ved accept.|[Oprette tilbud på montage til ordre-salg](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Kombiner komponenter for at oprette et element i en enkel proces, til bestilling eller til lager.|[Montere varer](assembly-how-to-assemble-items.md)|  
|Sælg montageelementer, der ikke er tilgængelige i øjeblikket, ved at oprette en tilknyttet montageordre for at levere den fulde eller delvise salgsordremængde.|[Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md)|
|Når nogle montage til ordre-elementer allerede findes i lageret, kan du fratrække mængden fra montageordren og reservere den fra lageret.|[Sælge lagervarer i montage til ordre-forløb](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Når du sælger montageelementer fra lageret, og alle elementer ikke er tilgængelige, kan du starte en montageordre til automatisk at levere en del af eller hele salgsordremængden.|[Sælge montage til ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Oprette tilpassede montageelementer til rammesalgsordrer, før du regelmæssigt opretter faktiske salgsordrer i overensstemmelse med rammeordreaftale.|[Oprette rammemontageordrer](assembly-how-to-create-blanket-assembly-orders.md)|
|Annuller en bogført montageordre, for eksempel fordi ordren er bogført med fejl, der skal rettes.|[Fortryde bogføring af montage](assembly-how-to-undo-assembly-posting.md)|
|Få mere at vide om forskellen mellem montagestyklister og produktionsstyklister og de involverede behandlingsforskelle.|[Arbejde med styklister](inventory-how-work-BOMs.md)|
|Lær, hvordan montageforbrug og afgang håndteres, når du bogfører montageordrer, og hvordan de afledte omkostninger for varen og ressourcen behandles og fordeles i regnskabet.|[Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md)|  

## <a name="see-also"></a>Se også  
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
