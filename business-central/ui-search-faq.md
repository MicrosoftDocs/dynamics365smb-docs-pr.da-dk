---
title: Ofte stillede spørgsmål om Fortæl mig
description: 'Denne artikel indeholder svar på spørgsmål, som vores partnere og kunder ofte stiller om Fortæl mig-funktionen.'
author: brentholtorf
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'find, search, Tell Me'
ms.search.form: TellMe
ms.date: 09/21/2023
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---
# Ofte stillede spørgsmål om Fortæl mig

I denne artikel besvares spørgsmål, som erfarne brugere ofte stiller om funktionen Fortæl mig, hvad du vil gøre.

## Kan alle handlinger fra min aktuelle side registreres i Fortæl mig?

Nej. Handlinger i dele, f.eks. en salgslinjedelen eller faktabokse, vises ikke i Fortæl mig.

## Kan jeg søge efter en bestemt post?

Ja. Hvis du f.eks. hurtigt vil finde en salgsordre, skal du angive dens id og derefter vælge handlingen **Søg i firmadata**. Hvis du kun kender kundens navn, skal du angive det. Fortæl mig arrangerer resultaterne efter type, så du kan finde ordren under kategorien Salgsordrer.

## Filtreres resultaterne i Fortæl mig efter rettigheder?

Hvis brugeren ikke har AccessByPermissions, vises handlinger ikke. Sider og rapporter vises i dog resultaterne, men kræver, at brugeren har rettigheder til at få adgang til dem. Der vises en meddelelse, hvis brugeren ikke har rettigheder til at få vist objektet.

## Viser Fortæl mig indhold fra mine tilpasninger eller installerede udvidelser fra tredjepart?

Handlinger, sider og rapporter, der stammer fra udvidelser, hentes af Fortæl mig. Du kan finde tekniske oplysninger om, hvordan du kan gøre brugerdefinerede sider og rapporter registrerbare, i [Tilføjelse af sider og rapporter til søgning](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

## Hvordan adskiller denne funktion sig fra det, der tidligere blev kaldt sidesøgning?

Sidesøgning er blevet udviklet til Fortæl mig for at hjælpe dig med at få arbejdet gjort hurtigt. Sidesøgning kan kun hjælpe dig med at navigere til sider eller rapporter. På et teknisk plan er Fortæl mig ikke længere baseret på det ældre MenuSuite-princip.

## Jeg bruger [!INCLUDE[prod_short](includes/prod_short.md)] til det lokale miljø. Omfatter det Fortæl mig?

Du kan bruge Fortæl mig i den lokale webklient til at finde handlinger, sider og rapporter, men ikke apps og konsulenttjenester i AppSource.

## Er Fortæl mig tilgængelig for alle formfaktorer?

Ja. Den blev introduceret på telefoner og tablets i Business Central-udgivelsesbølge 2 i 2023, men skal aktiveres i [Funktionsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management) ved hjælp af parameteren **Funktion: Søg efter sider og data i mobilappen**. 

<!-- removed in v20 because of Help pane
### Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

## Vil jeg give mig hjælp til at bruge sider, rapporter og andre ting?

Nej, men du kan nemt få disse oplysninger fra Hjælp-ruden. Du skal blot vælge **Søg i hjælpen** på siden **Fortæl mig, hvad du vil gøre** eller vælge <kbd>Ctrl</kbd>+<kbd>F1</kbd> på tastaturet. Hvis du vil vide mere om hjælperuden, skal du gå til [Hjælp-ruden](product-help-and-support.md#help-pane).

### Hvorfor vises der ikke et bogmærkeikon for mine søgeresultater?

Bogmærkeikonet vises ikke i vinduet Fortæl mig, når tilpasning er deaktiveret for en brugerrolle.

## Se også  

[Gemme og tilpasse listevisninger](ui-views.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Søge efter sider med Rollestifinder](ui-role-explorer.md)  
[Bogmærke en side eller en rapport i rollecenteret](ui-bookmarks.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]