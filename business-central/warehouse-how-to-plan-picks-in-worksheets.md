---
title: 'Fremgangsmåde: Planlægge pluk i kladder'
description: Få mere at vide om, hvordan linjer på leverancedokumenter kan gøres tilgængelige i plukkladder for lagermedarbejdere.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/13/2021
ms.author: edupont
ms.openlocfilehash: 667aa2702d064e44b9b52dc167e2372f98d7944f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530401"
---
# <a name="plan-picks-in-worksheets"></a>Planlægge pluk i kladder

Hvis lagerstedet kræver både pluk og leverance, kan du vælge at gøre linjerne på leverance dokumenterne tilgængelige i plukkladder i stedet for plukinstruktioner.  

> [!NOTE]  
> Hvis plukinstruktionerne for lagerstedet allerede er oprettet, og du vil kombinere dem til én effektiv plukinstruktion, skal du slette de enkelte pluklister for lagerstedet. De linjer, der skal plukkes, kan nu anføres i plukkladden.  

På siden **Plukkladder** kan du oprette pluklister, som hjælpe medarbejderen kan bruge til at samle varer på lagerstedet. Siden viser de antal, der kan bruges til direkte afsendelsesplaceringer, som er nyttige i forbindelse med planlægning af arbejdsopgaver i forbindelse med direkte afsendelse. [!INCLUDE[prod_short](includes/prod_short.md)] foreslår altid først pluk fra en direkte afsendelsesplacering. Linjerne i kladden kan hentes fra flere kildedokumenter. De kan f. eks. komme fra mere end én salgsordre. 

> [!NOTE]  
> Pluk af varer, der samles til salgsordren, der leveres, følger de samme trin som for normale lagerpluk til leverance, som det er beskrevet for forsendelsen. Antallet af pluklinjer pr. antal til levering kan være mange til en, da du plukker komponenterne og ikke montageelementet.  
>
> Lagerpluklinjerne oprettes for værdien i feltet **Restantal** på linjerne for den montageordre, der er knyttes til salgsordren, der leveres. Dette sikrer, at alle komponenter plukkes i én handling. Du kan finde flere oplysninger i [Sælge lagervarer i montage til ordre-flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  
>
> Se [Plukke til montage eller produktion i avancerede lageropsætninger](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md) for at få oplysninger om pluk af komponenter til montageordrer generelt, herunder situationer, hvor montageelementet ikke er forfaldent på en salgsleverance.  

## <a name="sorting-lines-on-a-pick-worksheet"></a>Sortere linjer i en plukkladde

Du kan sortere linjer efter vare, placeringsnummer, kildedokument, forfaldsdato eller destination. Her følger et par eksempler på hvordan sortering kan være nyttig.

* Hvis du sorterer efter forfaldsdato, kan du vælge at slette alle linjer undtagen dem, der kræver øjeblikkelig behandling. De mindre hastende linjer slettes ikke som sådan, men sendes blot tilbage til **Plukkladden**. Når du opretter pluklisten, er linjerne allerede sorteret efter forfaldsdato, og du kan vælge at tildele pluklisten til en medarbejder.
* Hvis placeringerne er nummererede, så de svarer til lagerstedets fysiske layout, kan sorterings linjer efter placeringsnummer gøre det nemmere at plukke til flere leverancer på samme tid. 
* Hvis du bruger placeringsniveau, kan du spare tid ved at sortere efter placering. 
* Du kan sortere efter destination, hvilket giver dig mulighed for at samle og afsende ordrer pr. kunde.

## <a name="to-plan-picks-in-the-worksheet"></a>Sådan planlægges pluk i plukkladden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Plukkladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Hent lagerdokumenter**.  
3. Vælg de leverancer, som du vil forberede en plukliste til. Du kan sortere linjerne, men sorteringen anvendes ikke til plukinstruktionen. Du kan også slette nogle af linjerne og derved oprette en mere effektiv plukliste. Hvis der f.eks. er flere linjer med varer i direkte afsendelsesplaceringer, kan du vælge at oprette pluklister til alle linjerne. Varerne i de direkte afsendelsesplaceringer forsendes sammen med de andre varer i forsendelsen, og de direkte afsendelsesplaceringer har plads til flere indkommende varer.  
4. Vælg handlingen **Opret pluk**, og udfyld anmodningssiden **Opret pluk**. Den sortering, du anmoder om her, sorterer de pluklinjer, du opretter. Du kan f.eks. oprette en linje for hver zone og sortere linjerne efter placeringsorden inden for hvert pluk.  
5. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk (logistik)**, og vælg derefter det relaterede link. Siden **Pluk (logistik)** åbnes.  
6. Du kan nu se de pluktildelinger, du har oprettet, ved at vælge det pluk, der har det højeste nummer.  
7. Hvis det er nødvendigt, kan du tildele en anden bruger eller sortere linjerne forskelligt.  
8. Hvis du vil udskrive plukvejledningen, skal du vælge handlingen **Udskriv**.  
9. Når du har plukket varerne, skal du vælge handlingen **Registrer**.  

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/pick-ship-items-warehouse/)

## <a name="see-also"></a>Se også

[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
