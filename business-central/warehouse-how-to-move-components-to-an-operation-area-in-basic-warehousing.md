---
title: "Sådan flyttes komponenter til et handlingsområde i grundlæggende lageropsætninger | Microsoft Docs"
description: "Hvis der forekommer varebehandlingsprocesser på lagerlokationen, skal du evt. flytte varer mellem interne placeringer som reaktion på interne kildedokumenter, f.eks. produktion, montage eller serviceordrer på lokationen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5e271b160d8a4969be296861f6746163fcfea6ba
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger
Hvis der forekommer varebehandlingsprocesser på lagerlokationen, skal du evt. flytte varer mellem interne placeringer som reaktion på interne kildedokumenter, f.eks. produktion, montage eller serviceordrer på lokationen.  

> [!NOTE]  
>  Du kan finde oplysninger om flytning af varer mellem placeringer uden kildedokumenter i Intern flytning.  

I avancerede lageropsætninger, som er lokationer, der bruger opsætningsfeltet **Styret læg-på-lager og pluk**, kan du bruge vinduet **Bevægelseskladde** til at flytte varer mellem placeringer. Du kan finde flere oplysninger i [Flytte varer i avancerede lageropsætninger](warehouse-how-to-move-items-in-advanced-warehousing.md).  

I grundlæggende lageropsætninger, som er lokationer, der bruger opsætningsfeltet **Tvungen placering** og opsætningsfeltet **Kræv pluk**, kan du registrere flytning af varer til interne operationsområder baseret på interne kildedokumenter på følgende måder:  

-   I vinduet **Flytning (lager)**.  
-   Med vinduet **Pluk (lager)**.  

> [!NOTE]  
>  Lagerpluk bogfører også negative vareposter som forbrug og understøttes kun for produktionskomponenter. Du kan finde flere oplysninger i vinduet Pluk (lager).  

Du kan finde detaljerede oplysninger om lagerbevægelser i vinduet Flytning (lager).  

To forskellige roller kan oprette den første flytning (lager). En montagearbejder kan for eksempel oprette rollen fra en frigivet montageordre, så den vises i lagermedarbejderens liste over arbejde, der skal udføres. For at oprette en lagerbevægelse for montageordrelinjer, der er klar til, at komponenter flyttes til deres angivne placeringer, bruger montagearbejderen funktionen **Opret flytning (lager)**.  

En lagermedarbejder kan også oprette den ved at pege på den pågældende frigivne montageordre. Dette beskrives i følgende fremgangsmåde:  

> [!NOTE]  
>  Hvis flytningen gælder en montageordre, hvor varen er monteret til en salgsordre, kan du definere, at dokumentet for flytning (lager) skal oprettes automatisk, når du opretter det lagerplukdokument, der tager det færdige montageelement og bogfører leverancen. Du kan angive dette ved at vælge feltet **Opret bevægelser automatisk** i vinduet **Montagekonfiguration**  
>   
>  Du kan finde flere oplysninger om montageordrer og grundlæggende lageropsætninger i afsnittet "Håndtere montageordrevarer med pluk (lager)" i [Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md).  

Denne fremgangsmåde viser, hvordan du opretter en flytning (lager) fra vinduet **Flytning (lager)** ved at referere til en frigivet montageordre som et kildedokument. Fremgangsmåden er den samme, når du flytter komponenter til produktionsordrer og serviceordrer.  

## <a name="to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Sådan flyttes komponenter til et handlingsområde i grundlæggende lageropsætninger  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Flytning (lager)**, og vælg det relevante link.  
2.  Udfyld feltet **Nummer** i oversigtspanelet **Generelt**. . Du kan trykke på Enter-tasten for at vælge fra nummerserien.  
3.  I feltet **Lokationskode** skal du indtaste den lokation, hvor flytningen finder sted.  
4.  Vælg handlingen **Hent kildedokumenter**. Du kan også udfylde feltet **Kildedokumentet** og derefter vælge knappen **AssistEdit** i feltet **Kildenr.**.  
5.  I vinduet **Kildedokumenter** skal du vælge den montageordre, du vil flytte komponenter for, og derefter vælge knappen **OK**.  

    For hver nødvendig komponent, der kan flyttes, oprettes én hent-linje og én placer-linje i vinduet **Flytninger (lager)**. Alle felter undtagen feltet **Håndteringsantal** er udfyldt på forhånd i henhold til kildedokumentlinjerne. Feltet **Håndteringsantal** er indstillet til nul, indtil du angiver det antal, du rent faktisk har flyttet.  

    Du kan ændre placeringskoden på linjen Hent, men kun i henhold til tilgængelighed. Hvis du vælger knappen **AssistEdit** i feltet **Placeringskode** på linjen Hent, åbnes vinduet **Placeringsindhold** og viser de placeringer, hvor komponenten er tilgængelig.  

    Du kan ikke ændre en placeringskode på en Placer-linje. Kun den placeringskode, der er defineret på komponentlinjen i kildedokument, accepteres. Dette understøtter princippet om, at den rolle, dvs. en montagearbejder i denne procedure, der anmoder om en komponent, ved, hvor komponenten skal placeres. Hvis du vil anbringe komponenterne på en anden placering, skal du først ændre placeringskoden på komponentlinjen og derefter genoprette flytning(lager)-linjerne.  
6.  Indtast det fulde eller delvise antal, du rent faktisk har flyttet, i feltet **Håndteringsantal**. Værdien i Hent- og Placer-linjerne skal være den samme. Ellers kan du ikke registrere bevægelsen.  

    > [!NOTE]  
    >  Som i andre lageraktiviteter kan du opdele linjen Placer ved at vælge handlingen **Handlinger** og derefter vælge handlingen **Opdel linje**. I dette tilfælde skal summen af de to opdelte Placer-linjer være lig med antallet på linjen Hent.  

7.  Når du er klar til at registrere de bevægelser, du har udført, skal du vælge handlingen **Registrer flytning (lager)**.  

    Der oprettes lagerposter som tegn på, at komponenterne nu findes på de placeringer, der er angivet i montageordrelinjerne.  

    > [!NOTE]  
    >  I modsætning til når du flytter komponenter med et lagerpluk, bogføres forbrug ikke, når du registrerer en flytning (lager). Det trin skal foregå særskilt ved at bogføre montageordreafgang og -forbrug. Du kan finde flere oplysninger i Montageordre.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

