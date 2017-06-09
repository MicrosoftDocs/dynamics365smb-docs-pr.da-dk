---
title: "Opsætning af marketingkampagner i Financials | Microsoft Docs"
description: Beskriver, hvordan du kan konfigurere og styre marketingkampagner i Dynamics 365 for Financials
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 03/08/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8f616382e28e29aab1ce7d9b45b8efb4ad374b96
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="managing-marketing-campaigns"></a>Administration af marketingkampagner
Når du har fastlagt en stærk marketingplan, kan du identificere og tiltrække kunder og holde på dem. En marketingplan består af forskellige kampagner og andre interaktioner i forbindelse med salgs- og marketingaktiviteter. Mens du planlægger en kampagne, skal du beslutte, hvilke kontaktpersoner der skal være målet, hvilken type kampagne kampagnen skal være (f.eks. en messe eller direct mail), og hvilke sælgere der skal udføre de enkelte opgaver.

<!-- Each campaign consists of various activities or to-dos. Activities are large tasks that can be broken down into several smaller tasks or to-dos. To-dos are individual or team tasks that can be created within activities or individually and then be assigned to individual salespeople or groups of salespeople.-->

## <a name="defining-individual-campaigns"></a>Definere individuelle kampagner
Når du vil oprette en kampagne, skal du først definere *statuskoder for kampagnen*. Via. disse koder kan du styre dine kampagner ved at tildele kampagnen en status. Efterhånden som du arbejder dig gennem faserne i en kampagne, kan du se, hvilket trin en kampagne er på, og hvilket trin der følger efter. Du kan definerer statuskoder for kampagner i vinduet **Kampagnestatus**.

Du kan oprette et *kampagnekort* til hver kampagne, som du vil holde styr på. Du kan også få vist disse kampagnekort, så du kan se generelle oplysninger om dine kampagner.
Du kan slette kampagneposter, f.eks. hvis de registrerer en handling, der er annulleret. Kun annullerede kampagneposter kan slettes.

### <a name="selecting-the-target-audience"></a>Vælge målgruppen
Når du har oprettet en kampagne, kan du begynde at oprette segmenter, der specificerer målgruppen for kampagnen. Der kan finde flere oplysninger under [Administrere målgrupper](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Registrere rabatprocenter
Når du har oprettet en kampagne, besluttet, hvilken målgruppe kampagnen skal rettes mod, og angivet start- og slutdato, skal du registrere den rabatprocent, som kunden får på de individuelle varer på linjerne i vinduet **Salgslinjerabatter**. Du kan også registrere salgsprisen for de enkelte varer på linjerne i vinduet **Salgspriser**. Du kan få adgang til begge vinduer fra kampagnekortet.

 Når du har angivet salgspriserne/linjerabatterne og målgrupperne på kampagnekortet, skal de aktiveres, så kampagnepriserne og -rabatterne vises på linjerne.

> [!NOTE]  
>  Hvis du vil aktivere salgspriserne/linjerabatterne, skal du angive, om kampagnen er henvendt til hele målgruppen eller kun bestemte kontakter. Hvis salgspriserne/linjerabatterne dækker alle kontakter i målgruppen, skal du markere feltet **Kampagnemålgruppe** i oversigtspanelet **Kampagne** på **målgruppekortet**.
Hvis salgspriserne/linjerabatterne ikke skal tilbydes til alle kontakter i målgruppen, skal markeringen fjernes fra feltet **Kampagnemålgruppe** for de relevante kontakter. Hvis feltet ikke vises, kan du føje det til visningen. Du kan finde flere oplysninger under [Brugertilpasning](ui-user-personalization.md).

<!-- ## Conducting campaigns
As a campaign runs, all interactions with your contacts, or segment, are recorded so that you can get statistics and other information about the costs and success rates of the campaign.

Campaigns are conducted by salespeople, and you must create activities to represent each task and assign them to the relevant salespeople.  -->

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Administrere målgrupper](marketing-segments.md)  
[Administrere salgsleads](marketing-manage-sales-opportunities.md)  
[Arbejde med Financials](ui-work-product.md)  

