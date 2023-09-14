---
title: 'Fremgangsmåde: Oprette serviceartikler'
description: 'Læse om de forskellige måder, du kan oprette serviceartikler på i Business central, f. eks. i en serviceordre eller ved levering af varer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# Oprette serviceartikler

I [!INCLUDE[prod_short](includes/prod_short.md)] refererer termen "serviceartikel" til udstyr eller varer, der kræver service. Når du opretter en serviceordre, kan du angive de varer, der har brug for service. I ordren kan du knytte en serviceartikel til en vare på lageret eller en serviceartikelgruppe.    

Når du modtager en vare, der kræver service, kan du registrere den som en serviceartikel. Dette kan gøres på flere måder. Du kan f.eks. oprette en serviceartikel på siden **Serviceartikler** eller som en del af en anden proces, f.eks. når du arbejder med en serviceordre.   

## Oprette en serviceartikel

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceartikler** og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Sådan oprettes serviceartikler fra serviceordrer

Når du modtager artikler, som du vil registrere som serviceartikler, kan du oprette dem som serviceartikler på siderne **Serviceordre** eller **Servicetilbud**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Vælg handlingen **Opret serviceartikel**.  

    Der tildeles et nummer til serviceartiklen, og der oprettes et serviceartikelkort. Feltet **Serviceartikelnr.** udfyldes med nummeret på den nye serviceartikel.

## Oprette en serviceartikel ved levering af varer

Når du leverer varer enten ved at bogføre salgsordrer eller salgsfakturaer, registreres de leverede varer automatisk som serviceartikler, hvis følgende betingelser er opfyldt. Varerne skal høre til en serviceartikelgruppe, hvor afkrydsningsfeltet **Opret serviceartikel** er markeret. Hvis varerne har serienumre registreret på siden Varesporingslinje, kopieres disse oplysninger automatisk til feltet **Serienr.** på serviceartikelkortet ved oprettelse af serviceartikler.  

Nedenstående fremgangsmåde viser, hvordan du kan oprette serviceartikler, når du leverer varer i salgsordrer.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Åbn den relevante Salgsordre.  
3. Vælg handlingen **Bogfør** eller **Bogfør og udskriv**.  
4. Vælg handlingen **Lever** eller **Lever og fakturer**.  
5. Der oprettes automatisk serviceartikler for varerne i ordren, forudsat at disse hører til en serviceartikelgruppe, som du har defineret for at oprette serviceartikler. Hvis der er registreret specifikke serienumre på siden **Varesporingslinjer**, tildeles de til disse serviceartikler.  

> [!NOTE]  
>  Hvis en vare er en stykliste, og du har udfoldet styklisten, bliver styklistevarerne behandlet på samme måde som almindelige varer. Der oprettes serviceartikler baseret på samme betingelser for serviceartikelgruppe og eventuelt betingelser for serienummer. Hvis der oprettes en serviceartikel for en udfoldet styklistevare, som består af andre styklistekomponenter, oprettes disse varer desuden som serviceartikelkomponenter for den udfoldede styklisteartikel.  
>   
>  Hvis varen er en stykliste, og du ikke har udfoldet styklisten, oprettes der en serviceartikel til den på de samme betingelser for serviceartikelgruppen og eventuelt betingelsen for serienumre.  

## Sådan indsættes startgebyrer for serviceartikler

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceopgaver** og vælg derefter det relaterede link.
2. Vælg handlingen **Varekladde**.
3. Vælg servicelinjen, og vælg derefter **Handlinger**, vælg **Funktioner**, og vælg derefter handlingen **Indsæt startgebyr**.  

    Der indsættes en servicelinje af typen **Omkostning** med startgebyr. Startgebyret gælder den valgte serviceartikel.

## Se relateret [Microsoft-træning](/training/modules/create-items/)

## Se også

[Konfigurere serviceartikler og serviceartikelkomponenter](service-how-setup-service-items.md)  
[Konfigurere Service](service-setup-service.md)  
[Service Management](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
