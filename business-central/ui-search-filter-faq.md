---
title: Om søgning og filtrering i Business Central
description: Svar på ofte stillede spørgsmål om søgning og filtrering.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 04/05/2019
ms.author: mikebc
ms.openlocfilehash: 0f9f5db0e7031156848a5bd15c711d3108f3490b
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2019
ms.locfileid: "969851"
---
# <a name="searching-and-filtering-faq"></a>Ofte stillede spørgsmål om søgning og filtrering
Denne artikel indeholder svar på almindelige spørgsmål om søgning og filtrering.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Der er forskel på søgning og filtrering?
Ja.
- Søgning er enkel og bred. Søgninger matcher records, der indeholder søgeteksten på tværs synlige felter på siden, og der skelnes mellem små og store bogstaver.
- Filtrering er meget fleksibel og kan anvendes på bestemte felter, herunder dem, der ikke er synlige på siden. Filtreringer viser records med præcise forekomster, der skelner mellem små og store bogstaver, men de kan redigeres med effektive søgesymboler, tokens og formler. Du kan finde flere oplysninger om, hvordan disse funktioner bruges, i [Sortering, søgning og filtrering på lister](ui-enter-criteria-filters.md).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Findes der en tastaturoplevelse til søgning og filtrering?
Søgning og filtrering er blevet stærkt optimeret for brugere, der ønsker at kunne arbejde effektivt med deres data uden brug af mus. Der findes en række genvejstaster, som kan bruges i rækkefølge, så arbejdet kan udføres med høj hastighed. Du kan finde flere oplysninger i [Tastaturgenveje](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Findes filterruden på alle lister?
Filterruden findes på sider, hvor listen udgør det primære indhold på siden, f.eks. regneark og oversigtssider, herunder lister kan åbnes fra navigationslinjen. Filterruden er endnu ikke tilgængelig for integrerede lister, f.eks. salgslinjer på salgsordrer eller lister med dynamiske kolonner (såkaldte matrixsider).

## <a name="how-can-i-save-my-filters"></a>Hvordan kan jeg gemme min filtre?

Dine filtre og reguleringer af foruddefinerede filtre, gemmes i hele sessionen (så længe du er logget på), også selvom du navigerer væk fra siden. Det er endnu ikke muligt at gemme filtre permanent. I modsætning til filtre gemmes søgetekst ikke, når du navigerer væk fra en side.

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Er dette det samme som avancerede filtre og begrænsning af totaler i Microsoft Dynamics NAV?

[!INCLUDE[d365fin](includes/d365fin_md.md)] bygger på disse almindelige funktioner og leverer en moderne og meget brugbar oplevelse til søgning efter og analyse af dine data. Med flere tastaturgenveje og introduktionen af søgning overgår [!INCLUDE[d365fin](includes/d365fin_md.md)] funktionaliteten i Dynamics NAV.  

Se også [Kan rapporter filtreres i filterruden?](#is-the-filter-pane-available-for-filtering-reports).  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>Kan jeg søge og filtrere ved hjælp af ledsagerapps og Outlook-tilføjelsesprogrammet?
På forskellige visningsmål, f.eks. mobilenheder eller i Outlook, kan du søge i lister, men du kan ikke filtrere på de enkelte felter i de fleste tilfælde.

## <a name="is-the-filter-pane-available-for-filtering-reports"></a>Kan rapporter filtreres i filterruden?
Nej. Dialogboksen til rapportfiltrering, som også kaldes anmodningssiden, bruger en anden oplevelse, der anvender nogle, men ikke alle funktionerne fra filterruden.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Vil Microsoft udvide filterrudeoplevelsen?
Hos Microsoft lytter vi hele tiden til feedback fra vores forskellige grupper af brugere og handler på de mest interessante forslag. Hvis du er interesseret i at udvide filterruden med to eller flere formfaktorer, flere typer af lister og rapporter, eller har en god idé til forbedringer, kan du tilføje en ide eller stemme for eksisterende idéer på [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Kan jeg gøre noget ved meddelelsen "Søgningen efter rækker tager for lang tid"?

Der er en frist for, hvor lang tid en søgehandling kan tage. Du skal først forsøge at ændre søgekriterierne og søge igen. Hvis du bruger [!INCLUDE[prodshort](includes/prodshort.md)] i dit lokale miljø, kan du kontakte systemadministratoren, fordi en administrator kan øge fristen for søgninger.

Som lokal administrator kan du øge fristen på søgninger ved at ændre indstillingen **Timeout for søgning** for [!INCLUDE[prodshort](includes/prodshort.md)]-serveren. Du kan finde flere oplysninger i [Konfiguration af Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) i hjælpen til Business Central-udviklere og it-eksperter.

## <a name="see-also"></a>Se også

[Introduktion](product-get-started.md)  
[Sortering, søgning og filtrering i lister](ui-enter-criteria-filters.md)  
