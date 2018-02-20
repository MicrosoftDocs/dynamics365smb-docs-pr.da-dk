---
title: "Sådan planlægges ordre for ordre | Microsoft Docs"
description: "Denne planlægningsopgave kan udføres i vinduet **Ordreplanlægning**, hvor alle nye behov vises sammen med tilgængelighedsoplysninger og forsyningsforslag. Vinduet giver det fornødne overblik og de nødvendige værktøjer til at planlægge behovet effektivt ud fra salgslinjer og komponentlinjer og derefter direkte oprette forskellige typer af forsyningsordrer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a7266eddba4293807a1e7e2a187c5002be771499
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="plan-for-new-demand-order-by-order"></a>Planlægge efter nyt behov ordre for ordre
Denne planlægningsopgave kan udføres i vinduet **Ordreplanlægning**, hvor alle nye behov vises sammen med tilgængelighedsoplysninger og forsyningsforslag. Vinduet giver det fornødne overblik og de nødvendige værktøjer til at planlægge behovet effektivt ud fra salgslinjer og komponentlinjer og derefter direkte oprette forskellige typer af forsyningsordrer.  

Du kan gå ind i vinduet **Ordreplanlægning** på to måder afhængigt af arbejdsopgaven: Fra en ordre, du vil planlægge specifikt, eller i batchtilstand, fordi du vil planlægge efter alle nye behov.  


## <a name="to-plan-for-new-production-order-demand"></a>Planlægge en specifik produktionsordre  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Planlagte produktionsordrer**, og vælg derefter det relaterede link. (Du kan udføre disse trin for planlagte, fastlagte eller frigivne produktionsordrer).
2.  Åbn den produktionsordre, du vil planlægge, og vælg derefter handlingen **Planlægning**.  
3.  Vælg handlingen **Beregn plan** i vinduet **Ordreplanlægning**.  

Der vises planlægningslinjer i vinduet i overensstemmelse med filteret **Produktionsbehov**, dvs. uopfyldte komponentlinjer for alle eksisterende produktionsordrer. Behovet for kun denne ene produktionsordre er ikke vist, fordi det er nødvendigt at planlægge til en produktionsordre med et overblik over behovet for eventuelle tidligere komponentlinjer. Planlægningslinjer for produktionsordren i kontekst udvides.  

## <a name="to-plan-for-any-new-demand"></a>Sådan planlægges til alle nye behov  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ordreplanlægning**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Beregn plan** i vinduet **Ordreplanlægning**.
3.  Vælg knappen **Udvid (+)** foran datoen i feltet **Behovsdato** for at få vist de underliggende planlægningslinjer, der repræsenterer behovslinjer med manglende tilgængelighed.  
4.  For hver udvidet planlægningslinje, dvs. behovslinje, vises der værdier i oplysningsfelterne nederst i vinduet.  

    |Indstilling|Description|  
    |----------------------------------|---------------------------------------|  
    |**Mængde på andre lokationer**|Viser, om varen findes på en anden lokation. Du kan derefter søge efter og vælge den.|  
    |**Erstatning findes**|Viser om der produceres en erstatningsvare for varen. Du kan derefter søge efter og vælge den. Bemærk, at denne funktion kun gælder for komponenter, dvs. behovslinjer af typen **Produktion**.|  
    |**Disponibelt antal**|Viser den samlede tilgængelighed for varen, dvs. Planlagt disponibel balance.|  
    |**Tidligste disponible dato**|Viser ankomstdatoen for en indgående leveringsordre, der kan dække den nødvendige mængde på en dato, der er senere end behovsdatoen.|  

5.  Vælg, hvilken type forsyningsordre der skal oprettes, i feltet **Genbestillingssystem**.  

    Standardværdien er værdien på varekortet, eller lagerkortet, men du kan ændre den til en af disse tre indstillinger:  

    |Indstilling|Description|  
    |----------------------------------|---------------------------------------|  
    |**Køb**|Opretter en købsordre.|  
    |**Overførsel**|Opretter en overflytningsordre.|  
    |**Prod.ordre**|Opretter en produktionsordre.|  

    I feltet **Forsyning fra** skal du vælge en værdi, der svarer til det valgte genbestillingssystem.  

    > [!NOTE]  
    >  Hvis feltet ikke udfyldes, viser systemet en fejlmeddelelse, når du bruger funktionen **Opret forsyningsordrer**, og derefter oprettes der ikke nogen forsyningsordre til den pågældende planlægningslinje. Dette dog gælder ikke, hvis genbestillingssystemet er **Prod.ordre**.  

6.  Du kan slå op i den relevante liste i feltet **Forsyning fra**, og vælge, hvor forsyningen skal komme fra:  

    - Hvis genforsyningssystemet er **Køb**, kan du bruge opslagsknappen i dette felt til at slå op i vinduet **Vare/leverandører**.  
    - Hvis genforsyningssystemet er **Overførsel**, kan du bruge opslagsknappen i dette felt til at slå op i vinduet **Lokationsoversigt**.  

    Hvis varen findes på en anden lokation, vises der en værdi i feltet **Mængde på anden placering** forneden, og du kan derefter søge efter og vælge den lokation, varen skal forsynes fra, når du opretter overflytningsordren.  

    Hvis der findes en erstatning for den ønskede vare, er feltet **Erstatning findes** nederst i vinduet indstillet til **Ja**, og du kan derefter slå op i vinduet **Erstatningsvareposter** og vælge en erstatningsvare.  

7.  Marker feltet **Reserver**, hvis der skal foretages en reservation mellem den forsyningsordre, du opretter, og den behovslinje, som den oprettes til. Feltet er som standard tomt.  

    > [!NOTE]  
    >  Du kan kun markere dette afkrydsningsfelt, hvis varen har **Eventuelt** eller **Altid** i feltet **Reserver** på dets varekort.  

8.  I feltet **Antal til ordre** kan du angive det antal, der skal bestilles på den oprettede forsyningsordre.   
    Standardværdien er det samme antal som i feltet **Nødvendigt antal**. Men du kan beslutte at bestille mere eller mindre end dette antal på grundlag af din viden om behovet. Hvis du f.eks. i vinduet **Ordreplanlægning** kan se, at der er flere ikke-relaterede behovslinjer for den samme købte vare, og de forfalder omkring den samme dato, kan du konsolidere disse ved at indtaste det samlede nødvendige antal i feltet **Antal til ordre** i én linje og derefter slette de andre, forældede planlægningslinjer for den pågældende vare.  

9.  I felterne **Forfaldsdato** og **Ordredato** kan du skrive de datoer, der skal gælde for de oprettede forsyningsordrer.  

    Disse to felter er afhængige af hinanden i overensstemmelse med feltet **Standardsikkerhedstid**, som du kan finde i vinduet **Produktionsopsætning**. Forfaldsdatoen er som standard den samme som behovsdatoen, men du kan ændre dem efter eget ønske.  

> [!NOTE]  
>   Hvis du skriver en senere dato end behovsdatoen, modtager du en advarselsmeddelelse.  

## <a name="to-make-supply-orders"></a>Sådan laves forsyningsordrer  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Planlagte produktionsordrer**, og vælg derefter det relaterede link. Du kan udføre disse trin for en planlagt, fastlagt eller frigivet produktionsordre.  
2.  Åbn den produktionsordre, du vil planlægge, og vælg derefter handlingen **Planlægning**.  
3.  Placer markøren på en relevant planlægningslinje, og vælg derefter handlingen **Lav ordrer**.  
4.  Vælg en af følgende indstillinger i feltet **Lav ordrer for** i oversigtspanelet **Ordreplanlægning** i vinduet **Opret forsyningsordrer**.  

    |Indstilling|Description|  
    |----------------------------------|---------------------------------------|  
    |**Den aktive linje**|Lav en forsyningsordre kun for den linje, markøren er placeret på.|  
    |**Den aktive ordre**|Lav en forsyningsordre for alle linje i den ordre, hvor markøren er placeret.|  
    |**Alle linjer**|Lav forsyningsordrer for alle linjer i vinduet **Ordreplanlægning**.|  

5.  Angiv, hvilken type forsyningsordrer, eller indkøbskladdelinjer, der skal oprettes, i oversigtspanelet **Indstillinger**.  

    > [!NOTE]  
    >  De indstillinger, du senest har foretaget i vinduet **Opret forsyningsordrer**, gemmes under dit bruger-id, så de vises igen, næste gang du benytter vinduet.  

6.  Klik på **OK** for at oprette de angivne forsyningsordrer eller indkøbskladdelinjer.  

Du har nu foretaget planlægning for et uopfyldt behov ved at oprette de respektive forsyningsordrer. De detaljerede oplysninger om bestemte arbejdsgange, når du benytter vinduet **Ordreplanlægning**, afhænger af virksomhedens interne forretningsgange.  

Når du er færdig med planlægningsarbejdet i vinduet **Ordreplanlægning**, og du f.eks. har angivet en alternativ måde at forsyne det korrekte antal på, kan du fortsætte med at oprette forsyningsordrer for en eller flere planlægningslinjer.  

> [!NOTE]  
>  De forsyningsordrer, du opretter, kan medføre nye afhængige behov, f.eks. for underliggende produktionsordrer. Du bør derfor vælge **Beregn plan** igen for at finde og løse dem, før du går nedad på listen.  

## <a name="see-also"></a>Se også  
[Skabelon](production-planning.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

