---
title: Planlægge efter nyt behov ordre for ordre
description: 'Denne planlægningsopgave kan udføres på siden Ordreplanlægning, hvor alle nye behov vises sammen med tilgængelighedsoplysninger og forsyningsforslag, herunder vareerstatning.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '5522, 5524, 5526'
ms.date: 07/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Planlægge efter nyt behov ordre for ordre

Denne planlægningsopgave kan udføres på siden **Ordreplanlægning**, hvor alle nye behov vises sammen med tilgængelighedsoplysninger og forsyningsforslag. Vinduet giver det fornødne overblik og de nødvendige værktøjer til at planlægge behovet effektivt ud fra salgslinjer og komponentlinjer og derefter direkte oprette forskellige typer af forsyningsordrer.  

Du kan gå ind på siden **Ordreplanlægning** på to måder afhængigt af arbejdsopgaven: Fra en ordre, du vil planlægge specifikt, eller i batchtilstand, fordi du vil planlægge efter alle nye behov.  


## Planlægge en specifik produktionsordre

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Planlagte produktionsordrer**, og vælg derefter det relaterede link. (Du kan udføre disse trin for planlagte, fastlagte eller frigivne produktionsordrer).
2. Åbn den produktionsordre, du vil planlægge, og vælg derefter handlingen **Planlægning**.  
3. Vælg handlingen **Beregn plan** på siden **Ordreplanlægning**.  

Der vises planlægningslinjer på siden i overensstemmelse med filteret **Produktionsbehov**, dvs. uopfyldte komponentlinjer for alle eksisterende produktionsordrer. Behovet for kun denne ene produktionsordre er ikke vist, fordi det er nødvendigt at planlægge til en produktionsordre med et overblik over behovet for eventuelle tidligere komponentlinjer. Planlægningslinjer for produktionsordren i kontekst udvides.  

## Sådan planlægges til alle nye behov

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ordreplanlægning**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Beregn plan** på siden **Ordreplanlægning**.
3. Vælg knappen **Udvid (+)** foran datoen i feltet **Behovsdato** for at få vist de underliggende planlægningslinjer, der repræsenterer behovslinjer med manglende tilgængelighed.  
4. For hver udvidet planlægningslinje, dvs. behovslinje, vises der værdier i oplysningsfelterne nederst på siden.  

    |Indstilling|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Mængde på andre lokationer**|Viser, om varen findes på en anden lokation. Du kan derefter søge efter og vælge den.|  
    |**Erstatning findes**|Viser om der produceres en erstatningsvare for varen. Du kan derefter søge efter og vælge den. Bemærk, at denne funktion kun gælder for komponenter, dvs. behovslinjer af typen **Produktion**.|  
    |**Disponibelt antal**|Viser den samlede tilgængelighed for varen, dvs. Planlagt disponibel balance.|  
    |**Tidligste disponible dato**|Viser ankomstdatoen for en indgående leveringsordre, der kan dække den nødvendige mængde på en dato, der er senere end behovsdatoen.|  

5. Vælg, hvilken type forsyningsordre der skal oprettes, i feltet **Genbestillingssystem**.  

    Standardværdien er værdien på varekortet, eller lagerkortet, men du kan ændre den til en af disse tre indstillinger:  

    |Indstilling|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Køb**|Opretter en købsordre.|  
    |**Overførsel**|Opretter en overflytningsordre.|  
    |**Prod.ordre**|Opretter en produktionsordre.|  

    I feltet **Forsyning fra** skal du vælge en værdi, der svarer til det valgte genbestillingssystem.  

    > [!NOTE]  
    >  Hvis feltet ikke udfyldes, viser systemet en fejlmeddelelse, når du bruger funktionen **Opret forsyningsordrer**, og derefter oprettes der ikke nogen forsyningsordre til den pågældende planlægningslinje. Dette dog gælder ikke, hvis genbestillingssystemet er **Prod.ordre**.  

6. Du kan slå op i den relevante liste i feltet **Forsyning fra**, og vælge, hvor forsyningen skal komme fra:  

    - Hvis genforsyningssystemet er **Køb**, kan du bruge opslagsknappen i dette felt til at slå op på siden **Vare/leverandører**.  
    - Hvis genforsyningssystemet er **Overførsel**, kan du bruge opslagsknappen i dette felt til at slå op på siden **Lokationsoversigt**.  

    Hvis varen findes på en anden lokation, vises der en værdi i feltet **Mængde på anden placering** forneden, og du kan derefter søge efter og vælge den lokation, varen skal forsynes fra, når du opretter overflytningsordren.  

    Hvis der findes en erstatning for den ønskede vare, er feltet **Erstatning findes** nederst i vinduet indstillet til **Ja**, og du kan derefter slå op på siden **Erstatningsvareposter** og vælge en erstatningsvare.  

    > [!NOTE]  
    > Vær opmærksom på, at erstatningsvarer ikke automatisk medfører, at en vare erstattes af en anden vare, f. eks. når der oprettes en salgsordre eller en stykliste. I stedet bliver du advaret om, at der er en erstatningsvare tilgængelig.

7. Marker feltet **Reserver**, hvis der skal foretages en reservation mellem den forsyningsordre, du opretter, og den behovslinje, som den oprettes til. Feltet er som standard tomt.  

    > [!NOTE]  
    >  Du kan kun markere dette afkrydsningsfelt, hvis varen har **Eventuelt** eller **Altid** i feltet **Reserver** på dets varekort.  

8. I feltet **Antal til ordre** kan du angive det antal, der skal bestilles på den oprettede forsyningsordre.   
    Standardværdien er det samme antal som i feltet **Nødvendigt antal**. Men du kan beslutte at bestille mere eller mindre end dette antal på grundlag af din viden om behovet. Hvis du f.eks. på siden **Ordreplanlægning** kan se, at der er flere ikke-relaterede behovslinjer for den samme købte vare, og de forfalder omkring den samme dato, kan du konsolidere disse ved at indtaste det samlede nødvendige antal i feltet **Antal til ordre** i én linje og derefter slette de andre, forældede planlægningslinjer for den pågældende vare.  

9. I felterne **Forfaldsdato** og **Ordredato** kan du skrive de datoer, der skal gælde for de oprettede forsyningsordrer.  

    Disse to felter er afhængige af hinanden i overensstemmelse med feltet **Standardsikkerhedstid**, som du kan finde på siden **Produktionsopsætning**. Forfaldsdatoen er som standard den samme som behovsdatoen, men du kan ændre dem efter eget ønske.  

> [!NOTE]  
> Hvis du skriver en senere dato end behovsdatoen, modtager du en advarselsmeddelelse.  

## Sådan laves forsyningsordrer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Planlagte produktionsordrer**, og vælg derefter det relaterede link. Du kan udføre disse trin for en planlagt, fastlagt eller frigivet produktionsordre.  
2. Åbn den produktionsordre, du vil planlægge, og vælg derefter handlingen **Planlægning**.  
3. Placer markøren på en relevant planlægningslinje, og vælg derefter handlingen **Lav ordrer**.  
4. Vælg en af følgende indstillinger i feltet **Lav ordrer for** i oversigtspanelet **Ordreplanlægning** på siden **Opret forsyningsordrer**.  

    |Indstilling|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Den aktive linje**|Lav en forsyningsordre kun for den linje, markøren er placeret på.|  
    |**Den aktive ordre**|Lav en forsyningsordre for alle linje i den ordre, hvor markøren er placeret.|  
    |**Alle linjer**|Lav forsyningsordrer for alle linjer på siden **Ordreplanlægning**.|  

5. Angiv, hvilken type forsyningsordrer, eller indkøbskladdelinjer, der skal oprettes, i oversigtspanelet **Indstillinger**.  

    > [!NOTE]  
    >  De indstillinger, du senest har foretaget i på siden **Opret forsyningsordrer**, gemmes under dit bruger-id, så de vises igen, næste gang du benytter siden.  

6. Klik på **OK** for at oprette de angivne forsyningsordrer eller indkøbskladdelinjer.  

Du har nu foretaget planlægning for et uopfyldt behov ved at oprette de respektive forsyningsordrer. De detaljerede oplysninger om bestemte workflows, når du benytter siden **Ordreplanlægning**, afhænger af virksomhedens interne forretningsgange.  

Når du er færdig med planlægningsarbejdet på siden **Ordreplanlægning**, og du f.eks. har angivet en alternativ måde at forsyne det korrekte antal på, kan du fortsætte med at oprette forsyningsordrer for en eller flere planlægningslinjer.  

> [!NOTE]  
> De forsyningsordrer, du opretter, kan medføre nye afhængige behov, f.eks. for underliggende produktionsordrer. Du bør derfor vælge **Beregn plan** igen for at finde og løse dem, før du går nedad på listen.  

## Se også

<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
[Skabelon](production-planning.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)  
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Registrere nye varer](inventory-how-register-new-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
