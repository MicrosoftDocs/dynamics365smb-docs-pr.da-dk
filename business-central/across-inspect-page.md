---
title: Inspektion af sider i Business Central
description: Brug sideinspektionsfunktionen til at zoome ind på oplysninger om sideopsætningen og datakilden. Sideinspektion er velegnet til fejlfinding af problemer med dine data.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.topic: conceptual
author: jswymer
ms.author: jswymer
ms.date: 09/15/2023
ms.service: dynamics-365-business-central
---

# Inspektion af sider i Business Central

Sideinspektionsfunktionen giver mulighed at få oplysninger om en side, giver dig indsigt i sideopsætningen, de forskellige elementer, der udgør siden, og kilden bag de data, der vises. Sideinspektion er specielt beregnet til administratorer, superbrugere, supportmedarbejdere og udviklere. Den er velegnet til læring af datamodellen bag en side og fejlfinding. Hvis der f.eks. opstår et problem med en side, kan du bruge sideinspektion til at hente oplysninger,der skal videregives til systemadministratoren eller supportmedarbejderne.

> [!NOTE]  
> Med [!INCLUDE [prod_short](includes/prod_short.md)] udgivelsesbølge 2 i 2023 kan du gennem sideinspektion starte Visual Studio Code inde fra webklienten for yderligere at undersøge og fejlfinde kildekoden til en udvidelse. Du kan finde flere oplysninger i [Fejlfinding i Visual Studio Code direkte fra webklienten](/dynamics365/business-central/dev-itpro/developer/devenv-troubleshoot-vscode-webclient) i hjælpen til Business Central Developer and IT Pro.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]

## Arbejde med sideinspektion

Du starter sideinspektion fra siden **Hjælp og Support**. Vælg spørgsmålstegnet i øverste højre hjørne, vælg **Hjælp og support**, og vælg derefter **Undersøg sider og data**. Du kan også bare bruge tastaturgenvejen <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>F1</kbd>.

Ruden **Sideinspektion** åbnes på siden. Når ruden åbnes første gang, indeholder den oplysninger, der vedrører hovedsidens objekt.

Bruge tastaturgenvejen eller pegeredskabet til at flytte fokus til forskellige elementer på siden. Når du vælger en faktaboks eller et element på hovedsiden, er det omgivende område fremhævet med en kant, og ruden **Sideinspektion** viser oplysninger om det valgte element. Den foregående figur viser f.eks. oplysninger om oversigtsdelen på siden **Salgsordre**. Når du navigerer til andre sider i programmet, opdateres ruden **Sideinspektion** automatisk med sideoplysningerne, mens du bevæger dig videre.

Du kan finde flere oplysninger om, hvad der vises i sideinspektionen, i [Inspektion og fejlfinding af sider](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) i hjælpen til Business Central-udviklere og it-eksperter.

Hvis du ikke kan se de oplysninger, du forventer at se, i ruden **Sideinspektion**, har du sandsynligvis ikke de nødvendige rettigheder som beskrevet i næste afsnit.

## Styring af adgang til oplysninger om sideinspektion

Som administrator kan du styre adgang til alle detaljer, der vises i ruden **Sideinspektion**, ved at konfigurere de rettigheder, som brugere har. Hvis du vil tildele en bruger rettigheder til alle detaljer, skal du give vedkommende rettigheden **Udfør** til **System** objekt **5330**. Du kan give denne rettighed ved hjælp af et rettighedssæt (f.eks. **D365-fejlfinding**) eller en brugergruppe (f.eks. **D365-fejlfinding**). Du kan finde flere oplysninger om rettigheder i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).

Brugere, der ikke tildeles rettigheder i **Systemobjekt 5330**, kan stadig få adgang til ruden **Sideinspektion**, men de får kun vist felterne **Side** og **Tabel**, der viser grundlæggende oplysninger, som de kan videregive til deres supportteam.

## Se også

[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
