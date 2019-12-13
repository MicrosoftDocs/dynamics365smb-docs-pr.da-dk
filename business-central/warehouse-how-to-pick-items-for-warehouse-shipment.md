---
title: 'Fremgangsmåde: Plukke varer til lagerleverance | Microsoft Docs'
description: Når lokationen kræver lagerpluk og lagerleverance, skal du bruge lagerplukdokumenterne til at oprette og behandle plukoplysningerne, inden du bogfører den pågældende lagerleverance.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d35c6dec3eee09ec72a09325dcc527c18dc9b8c4
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876675"
---
# <a name="pick-items-for-warehouse-shipment"></a>Plukke varer til lagerleverance
Når lokationen kræver lagerpluk og lagerleverance, skal du bruge lagerplukdokumenterne til at oprette og behandle plukoplysningerne, inden du bogfører den pågældende lagerleverance.  

Du kan ikke oprette et lagerplukdokument fra bunden, fordi en plukaktivitet altid er en del af en arbejdsproces, enten i et pull- eller push-scenario.  

Du kan oprette lagerplukdokumenterne på en pull-måde ved at åbne et tomt lagerleverencedokumentet, registrere kildedokumenter, der er frigivet til levering, og derefter oprette lagerpluklinjer for leverancerne. Du kan bruge funktionen **Hent kildedokumenter** eller funktionen **Brug filter til at hente kildedokumenter** til at registrere kildedokumenter, der er klar til levering.

Du kan også bruge siden **Plukkladde** til at trække og oprette pluklinjerne i batchtilstand. Du kan finde flere oplysninger i [Planlægge pluk i kladder](warehouse-how-to-plan-picks-in-worksheets.md).  

Du kan også oprette lagerplukdokumenter på en push-måde fra siden **Lagerleverance** ved at vælge **Opret pluk**.  

> [!NOTE]  
>  Pluk til lagerleverance af varer, der monteres til salgsordren, der leveres, følger de samme trin som for normale lagerpluk til leverance, som det er beskrevet i dette emne. Antallet af pluklinjer pr. antal til levering kan være mange til en, da du plukker komponenterne og ikke montageelementet.  
>   
>  Lagerpluklinjerne oprettes for værdien i feltet **Restantal** på linjerne for den montageordre, der er knyttes til salgsordren, der leveres. Dette sikrer, at alle komponenter plukkes i én handling.  
>   
>  Du kan finde flere oplysninger i afsnittet "Håndtere montageordrevarer i lagerleverancer".  
>   
>  Se [Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md) for at få oplysninger om pluk af komponenter til montageordrer generelt, herunder situationer, hvor montageelementet ikke er forfaldent på en salgsleverance.  

## <a name="to-pick-items-for-warehouse-shipment"></a>Sådan plukkes varer til lagerleverance  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Pluk**, og vælg derefter det relaterede link.  

    Hvis du skal arbejde med et bestemt pluk, skal du vælge plukket på listen eller filtrere oversigten for at finde de pluk, der er blevet tildelt specielt til dig. Åbn plukkortet.  
2.  Hvis feltet **Tildelt bruger-ID** er tomt, skal du skrive dit id for at identificere dig selv, hvis det er nødvendigt.  
3.  Udføre den faktiske plukning af varer.  

    Hvis lageret er indstillet til at bruge placeringer, bruges varernes standardplacering til at foreslå, hvor varerne skal hentes fra. Instruktionerne vises på to separate linjer, mindst én for hver type handling, Hent og Placer.  

    Hvis lageret er indstillet til at bruge styret læg-på-lager og pluk, bruges placeringsniveauet til at beregne de bedste placeringer, der skal plukkes fra, og disse placeringer foreslås derefter på pluklinjerne. Instruktionerne vises på to separate linjer, mindst én for hver type handling, Hent og Placer.  

4.  Når du har foretaget plukket og har placeret varerne på rette sted, skal du vælge handlingen **Registrer pluk**.  

Den person, der er ansvarlig for leveringen, kan nu bringe varerne til forsendelseshavnen og bogføre leverancen, herunder det relaterede kildedokument, på siden **Lagerleverance**. Du kan finde flere oplysninger i [Sende varer](warehouse-how-ship-items.md).   

Foruden pluk for kildedokumenter, som beskrevet i dette emne, kan du hente og placere varer mellem placeringer uden at bruge kildedokumenter. Du kan finde flere oplysninger i [Plukke og lægge på lager uden kildedokument](warehouse-how-to-create-put-aways-from-internal-put-aways.md).  

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Håndtering af montageordrevarer i lagerleverancer
I montageordrescenarier bruges feltet **Lever (antal)** på lagerleverancelinjerne til at registrere, hvor mange enheder der monteres. Den angivne mængde bogføres derefter som montageoutput, når er bogført lagerleverance.

For andre lagerleverancelinjer er værdien i feltet **Lever (antal)** nul fra start.

Når medarbejdere, der er ansvarlige for montering, afslutter monteringsdele eller montage til ordre-mængde, registrerer de det i feltet **Levér antal** på lagerleverancelinjen og vælger handlingen **Bogfør lev.**. Resultatet er, at tilsvarende montageafgang er bogført, herunder komponentforbrug. En salgsleverance for mængden, bogføres for salgsordre.

Fra montageordren kan du vælge **Ordremont.lagerleverancelinje** for at gå til lagerleverancelinjen. Dette er nyttigt for arbejdstagere, der ikke normalt bruger siden **Lagerleverance**.

Når lagerleverance bogføres, opdateres forskellige felter på salgsordrelinjen for at vise fremskridt på lageret. Følgende felter opdateres også for at vise, hvor mange montageordrer der mangler at blive monteret og leveret:

- **Udes. lagerantal for MTO**
- **Udes. lagerantal for MTO (basis)**

> [!NOTE]
> I kombinationsscenarier, hvor en del af mængden først skal samles, og en anden skal leveres fra lageret, oprettes minimum to lagerleverancelinjer. En er til montage efter ordre-antal, og den anden er til beholdningsantal.

> I dette tilfælde håndteres montage efter ordre-antal som beskrevet i dette emne, og beholdningsantal håndteres som enhver anden lagerleverancelinje. Du kan finde flere oplysninger om kombinationsscenarier i [Om Montage til ordre og Montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
