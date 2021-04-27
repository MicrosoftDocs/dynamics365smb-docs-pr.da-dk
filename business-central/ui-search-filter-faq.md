---
title: Om søgning og filtrering i Business Central
description: Svar på ofte stillede spørgsmål om søgning og filtrering.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 04/01/2021
ms.author: mikebc
ms.openlocfilehash: 7ed2b43a1269e97e22de78ff3c6a9a1e0666eb3a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772225"
---
# <a name="searching-and-filtering-faq"></a>Ofte stillede spørgsmål om søgning og filtrering
Denne artikel indeholder svar på almindelige spørgsmål om søgning og filtrering.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Der er forskel på søgning og filtrering?
Ja.
- Søgning er enkel og bred. Søgninger matcher records, der indeholder søgeteksten på tværs synlige felter på siden, og der skelnes mellem små og store bogstaver.
- Filtrering er meget fleksibel og kan anvendes på bestemte felter, herunder dem, der ikke er synlige på siden. Filtreringer viser records med præcise forekomster, der skelner mellem små og store bogstaver, men de kan redigeres med effektive søgesymboler, tokens og formler. Du kan finde flere oplysninger om, hvordan disse funktioner bruges, i [Sortering, søgning og filtrering](ui-enter-criteria-filters.md).

## <a name="exactly-which-fields-are-matched-when-searching"></a>Præcis hvilke felter matches, når der søges?
[!INCLUDE[prod_short](includes/prod_short.md)] anvender søgekriterierne på alle felter, der er synlige på siden. Hvis et felt er blevet skjult, f.eks. ved hjælp af personlige indstillinger, finder en søgning ikke dette felt. Søgekriterier anvendes kun på felter, hvis deres datatype svarer til søgekriteriernes. Hvis du for eksempel søger efter ordet i dag, søges *I dag* i alle tekst- og kodefelter efter den bogstavelige værdi "i dag" og også alle datofelter, hvor *i dag* evalueres som et udtryk for dags dato, men ikke søger i numeriske felter. Du kan finde flere oplysninger i [Sorterings-, søgnings- og filtreringsoversigter](ui-enter-criteria-filters.md#-filter-criteria-and-operators).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Findes der en tastaturoplevelse til søgning og filtrering?
Søgning og filtrering er blevet stærkt optimeret for brugere, der ønsker at kunne arbejde effektivt med deres data uden brug af mus. Der findes en række genvejstaster, som kan bruges i rækkefølge, så arbejdet kan udføres med høj hastighed. Du kan finde flere oplysninger i [Tastaturgenveje](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Findes filterruden på alle lister?
Filterruden findes på sider, hvor listen udgør det primære indhold på siden, f.eks. regneark og oversigtssider, herunder lister kan åbnes fra navigationslinjen. Filterruden er endnu ikke tilgængelig for lister, der vises som dele, f.eks. FactBoxes eller rollecenterdele eller lister, der vises som dialogbokse, s.eks. som opslag. Når en liste integreres på en side, f.eks. salgslinjer i en salgsordre, er filterruden tilgængelig, når der fokuseres på den pågældende liste med knappen fokustilstand. Du kan finde flere oplysninger i [Fokusere på linjevarer](ui-enter-data.md#Focus).

## <a name="how-can-i-save-my-filters"></a>Hvordan kan jeg gemme min filtre?
Dine filtre og reguleringer af foruddefinerede filtre, gemmes i hele sessionen (så længe du er logget på), også selvom du navigerer væk fra siden. Du kan gemme filtre permanent som en navngivet visning af listen ved at vælge ikonet ![Gem visning](media/save_view_icon.png "Gem visning") i filterruden. Du kan finde flere oplysninger i [Ofte stillede spørgsmål om listevisninger](ui-views-faq.md). Bemærk, at i modsætning til filtre huskes søgeteksten ikke, når du navigerer væk fra en side, og gemmes ikke, når du gemmer en visning.

På rapportanmodningssider kan du også gemme filtre eller bruge foruddefinerede filtre. Du kan finde flere oplysninger i [Bruge gemte indstillinger](ui-work-report.md#SavedSettings).

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Er dette det samme som avancerede filtre og begrænsning af totaler i Microsoft Dynamics NAV?
[!INCLUDE[prod_short](includes/prod_short.md)] bygger på disse almindelige funktioner og leverer en moderne og meget brugbar oplevelse til søgning efter og analyse af dine data. Med flere tastaturgenveje og introduktionen af søgning overgår [!INCLUDE[prod_short](includes/prod_short.md)] funktionaliteten i Dynamics NAV.  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-add-ins-for-microsoft-365"></a>Kan jeg søge og filtrere ved hjælp af ledsagerapps og tilføjelsesprogrammet til Microsoft 365?
På forskellige visningsmål, f.eks. mobilenheder eller i Outlook, kan du søge i lister, men du kan ikke filtrere på de enkelte felter i de fleste tilfælde. I appen [!INCLUDE[prod_short](includes/prod_short.md)] til Microsoft Teams er både søgning og filter tilgængelige på lister.

## <a name="how-do-i-view-how-my-search-terms-have-been-applied-to-fields-in-the-list"></a>Hvordan får jeg vist, hvordan mine søgeord er blevet anvendt på felter på listen?
Når du har indtastet søgeord i søgefeltet, kan du få vist de nøjagtige søgekriterier, og hvilke felter de er blevet anvendt til, ved at åbne sideinspektionsruden (**Ctrl+Alt+F1**) og vælge fanen **Sidefiltre**.

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Kan jeg gøre noget ved meddelelsen "Søgningen efter rækker tager for lang tid"?

Der er en frist for, hvor lang tid en søgehandling kan tage. Du skal først forsøge at ændre søgekriterierne og søge igen. Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] i dit lokale miljø, kan du kontakte systemadministratoren, fordi en administrator kan øge fristen for søgninger.

Som lokal administrator kan du øge fristen på søgninger ved at ændre indstillingen **Timeout for søgning** for [!INCLUDE[prod_short](includes/prod_short.md)]-serveren. Du kan finde flere oplysninger i [Konfiguration af Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) i hjælpen til Business Central-udviklere og it-eksperter.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Vil Microsoft udvide filterrudeoplevelsen?
Hos Microsoft lytter vi hele tiden til feedback fra vores forskellige grupper af brugere og handler på de mest interessante forslag. Hvis du er interesseret i at udvide filterruden med to eller flere formfaktorer og flere typer af lister, eller har en god idé til forbedringer, kan du tilføje en ide eller stemme for eksisterende idéer på [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="see-also"></a>Se også
[Sortering, søgning og filtrering](ui-enter-criteria-filters.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Søge efter sider med Rollestifinder](ui-role-explorer.md)  
[Blive køreklar](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]