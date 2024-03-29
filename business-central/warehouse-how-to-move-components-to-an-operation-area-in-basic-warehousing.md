---
title: Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger
description: Hvis der forekommer varebehandlingsprocesser på lagerlokationen, skal du evt. flytte varer mellem interne placeringer som reaktion på interne kildedokumenter, f.eks. produktion, montage eller serviceordrer på lokationen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7351, 7382, 9330
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: da2f937c50e5634a5f4e3abe6d1eae9064916f52
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8513259"
---
# <a name="move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger
Hvis der forekommer varebehandlingsprocesser på lagerlokationen, skal du evt. flytte varer mellem interne placeringer som reaktion på interne kildedokumenter, f.eks. produktion, montage eller serviceordrer på lokationen.  

> [!NOTE]  
>  Du kan finde oplysninger om flytning af varer mellem placeringer uden kildedokumenter i Intern flytning.  

I avancerede lageropsætninger, som er lokationer, der bruger opsætningsfeltet **Styret læg-på-lager og pluk**, kan du bruge siden **Bevægelseskladde** til at flytte varer mellem placeringer. Du kan finde flere oplysninger i [Flytte varer i avancerede lageropsætninger](warehouse-how-to-move-items-in-advanced-warehousing.md).  

I grundlæggende lageropsætninger, som er lokationer, der bruger opsætningsfeltet **Tvungen placering** og opsætningsfeltet **Kræv pluk**, kan du registrere flytning af varer til interne operationsområder baseret på interne kildedokumenter på følgende måder:  

-   På siden **Flytning (lager)**.  
-   Med siden **Pluk (lager)**.  

> [!NOTE]  
>  Lagerpluk bogfører også negative vareposter som forbrug og understøttes kun for produktionskomponenter. Du kan finde flere oplysninger på siden Pluk (lager).  

Du kan finde detaljerede oplysninger om lagerbevægelser på siden Flytning (lager).  

To forskellige roller kan oprette den første flytning (lager). En montagearbejder kan for eksempel oprette rollen fra en frigivet montageordre, så den vises i lagermedarbejderens liste over arbejde, der skal udføres. For at oprette en lagerbevægelse for montageordrelinjer, der er klar til, at komponenter flyttes til deres angivne placeringer, bruger montagearbejderen funktionen **Opret flytning (lager)**.  

En lagermedarbejder kan også oprette den ved at pege på den pågældende frigivne montageordre. Dette beskrives i følgende fremgangsmåde:  

> [!NOTE]  
>  Hvis flytningen gælder en montageordre, hvor varen er monteret til en salgsordre, kan du definere, at dokumentet for flytning (lager) skal oprettes automatisk, når du opretter det lagerplukdokument, der tager det færdige montageelement og bogfører leverancen. Du kan angive dette ved at vælge feltet **Opret bevægelser automatisk** på siden **Montagekonfiguration**  
>   
>  Du kan finde flere oplysninger om montageordrer og grundlæggende lageropsætninger i [Håndtering af montage til ordre-varer med pluk (lager)](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Denne fremgangsmåde viser, hvordan du opretter en flytning (lager) fra siden **Flytning (lager)** ved at referere til en frigivet montageordre som et kildedokument. Fremgangsmåden er den samme, når du flytter komponenter til produktionsordrer og serviceordrer.  

## <a name="to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Sådan flyttes komponenter til et handlingsområde i grundlæggende lageropsætninger  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Flytning (lager)**, og vælg derefter det relaterede link.  
2.  Udfyld feltet **Nummer** i oversigtspanelet **Generelt**. . Du kan trykke på Enter-tasten for at vælge fra nummerserien.  
3.  I feltet **Lokationskode** skal du indtaste den lokation, hvor flytningen finder sted.  
4.  Vælg handlingen **Hent kildedokumenter**. Du kan også udfylde feltet **Kildedokumentet** og derefter vælge knappen **AssistEdit** i feltet **Kildenr.**.  
5.  På siden **Kildedokumenter** skal du vælge den montageordre, du vil flytte komponenter for, og derefter vælge knappen **OK**.  

    For hver nødvendig komponent, der kan flyttes, oprettes én hent-linje og én placer-linje på siden **Flytninger (lager)**. Alle felter undtagen feltet **Håndteringsantal** er udfyldt på forhånd i henhold til kildedokumentlinjerne. Feltet **Håndteringsantal** er indstillet til nul, indtil du angiver det antal, du rent faktisk har flyttet.  

    Du kan ændre placeringskoden på linjen Hent, men kun i henhold til tilgængelighed. Hvis du vælger knappen **AssistEdit** i feltet **Placeringskode** på linjen Hent, åbnes siden **Placeringsindhold** og viser de placeringer, hvor komponenten er tilgængelig.  

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
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]