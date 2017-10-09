---
title: "Fremgangsmåde: Plukke varer til lagerleverance | Microsoft Docs"
description: "Når lokationen kræver lagerpluk og lagerleverance, skal du bruge lagerplukdokumenterne til at oprette og behandle plukoplysningerne, inden du bogfører den pågældende lagerleverance."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e4568214469e80dce7ea91ff7574d1be8ca9ac7a
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-pick-items-for-warehouse-shipment"></a>Fremgangsmåde: Plukke varer til lagerleverance
Når lokationen kræver lagerpluk og lagerleverance, skal du bruge lagerplukdokumenterne til at oprette og behandle plukoplysningerne, inden du bogfører den pågældende lagerleverance.  

Du kan ikke oprette et lagerplukdokument fra bunden, fordi en plukaktivitet altid er en del af en arbejdsproces, enten i et pull- eller push-scenario.  

Du kan oprette lagerplukdokumenterne på en pull-måde ved at åbne et tomt lagerleverencedokumentet, registrere kildedokumenter, der er frigivet til levering, og derefter oprette lagerpluklinjer for leverancerne. Du kan bruge funktionen **Hent kildedokumenter** eller funktionen **Brug filter til at hente kildedokumenter** til at registrere kildedokumenter, der er klar til levering.

Du kan også bruge vinduet **Plukkladde** til at trække og oprette pluklinjerne i batchtilstand. Du kan finde flere oplysninger i [Fremgangsmåde: Planlægge pluk i kladder](warehouse-how-to-plan-picks-in-worksheets.md).  

Du kan også oprette lagerplukdokumenter på en push-måde fra vinduet **Lagerleverance** ved at vælge **Opret pluk**.  

> [!NOTE]  
>  Pluk til lagerleverance af varer, der monteres til salgsordren, der leveres, følger de samme trin som for normale lagerpluk til leverance, som det er beskrevet i dette emne. Antallet af pluklinjer pr. antal til levering kan være mange til en, da du plukker komponenterne og ikke montageelementet.  
>   
>  Lagerpluklinjerne oprettes for værdien i feltet **Restantal** på linjerne for den montageordre, der er knyttes til salgsordren, der leveres. Dette sikrer, at alle komponenter plukkes i én handling.  
>   
>  Du kan finde flere oplysninger i afsnittet "Håndtere montageordrevarer i lagerleverancer".  
>   
>  Se [Fremgangsmåde: Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md) for at få oplysninger om pluk af komponenter til montageordrer generelt, herunder situationer, hvor montageelementet ikke er forfaldent på en salgsleverance.  

## <a name="to-pick-items-for-warehouse-shipment"></a>Sådan plukkes varer til lagerleverance  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Pluk**, og vælg derefter det relaterede link.  

    Hvis du skal arbejde med et bestemt pluk, skal du vælge plukket på listen eller filtrere oversigten for at finde de pluk, der er blevet tildelt specielt til dig. Åbn plukkortet.  
2.  Hvis feltet **Tildelt bruger-ID** er tomt, skal du skrive dit id for at identificere dig selv, hvis det er nødvendigt.  
3.  Udføre den faktiske plukning af varer.  

    Hvis lageret er indstillet til at bruge placeringer, bruges varernes standardplacering til at foreslå, hvor varerne skal hentes fra. Instruktionerne vises på to separate linjer, mindst én for hver type handling, Hent og Placer.  

    Hvis lageret er indstillet til at bruge styret læg-på-lager og pluk, bruges placeringsniveauet til at beregne de bedste placeringer, der skal plukkes fra, og disse placeringer foreslås derefter på pluklinjerne. Instruktionerne vises på to separate linjer, mindst én for hver type handling, Hent og Placer.  

4.  Når du har foretaget plukket og har placeret varerne på rette sted, skal du vælge handlingen **Registrer pluk**.  

Den person, der er ansvarlig for leveringen, kan nu bringe varerne til forsendelseshavnen og bogføre leverancen, herunder det relaterede kildedokument, i vinduet **Lagerleverance**. Du kan finde flere oplysninger i [Fremgangsmåde: Sende varer](warehouse-how-ship-items.md).   

Foruden pluk for kildedokumenter, som beskrevet i dette emne, kan du hente og placere varer mellem placeringer uden at bruge kildedokumenter. Du kan finde flere oplysninger i [Fremgangsmåde: Plukke og lægge på lager uden kildedokument](warehouse-how-to-create-put-aways-from-internal-put-aways.md).  

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Håndtering af montageordrevarer i lagerleverancer
I montageordrescenarier bruges feltet **Lever (antal)** på lagerleverancelinjerne til at registrere, hvor mange enheder der monteres. Den angivne mængde bogføres derefter som montageoutput, når er bogført lagerleverance.

For andre lagerleverancelinjer er værdien i feltet **Lever (antal)** nul fra start.

Når medarbejdere, der er ansvarlige for montering, afslutter monteringsdele eller montage til ordre-mængde, registrerer de det i feltet **Levér antal** på lagerleverancelinjen og vælger handlingen **Bogfør lev.**. Resultatet er, at tilsvarende montageafgang er bogført, herunder komponentforbrug. En salgsleverance for mængden, bogføres for salgsordre.

Fra montageordren kan du vælge **Ordremont.lagerleverancelinje** for at gå til lagerleverancelinjen. Dette er nyttigt for arbejdstagere, der ikke normalt bruger vinduet **Lagerleverance**.

Når lagerleverance bogføres, opdateres forskellige felter på salgsordrelinjen for at vise fremskridt på lageret. Følgende felter opdateres også for at vise, hvor mange montageordrer der mangler at blive monteret og leveret:

- **Udes. lagerantal for MTO**
- **Udes. lagerantal for MTO (basis)**

> [!NOTE]
> I kombinationsscenarier, hvor en del af mængden først skal samles, og en anden skal leveres fra lageret, oprettes minimum to lagerleverancelinjer. En er til montage efter ordre-antal, og den anden er til beholdningsantal.

> I dette tilfælde håndteres montage efter ordre-antal som beskrevet i dette emne, og beholdningsantal håndteres som enhver anden lagerleverancelinje. Du kan finde flere oplysninger om kombinationsscenarier i [Om montage til ordre og montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

