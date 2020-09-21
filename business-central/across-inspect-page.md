---
title: Inspektion af sider i Business Central
description: Brug sideinspektionsfunktionen til at zoome ind på oplysninger om sideopsætningen og datakilden. Sideinspektion er velegnet til fejlfinding af problemer med dine data.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
author: jswymer
ms.author: jswymer
ms.date: 04/01/2020
ms.openlocfilehash: ab5ebb0dcc654badd16ef3f9954b8f926bde5384
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778241"
---
# <a name="inspecting-pages-in-business-central"></a>Inspektion af sider i Business Central

Sideinspektionsfunktionen giver mulighed at få oplysninger om en side, giver dig indsigt i sideopsætningen, de forskellige elementer, der udgør siden, og kilden bag de data, der vises. Sideinspektion er specielt beregnet til administratorer, superbrugere, supportmedarbejdere og udviklere. Den er velegnet til læring af datamodellen bag en side og fejlfinding. Hvis der f.eks. opstår et problem med en side, kan du bruge sideinspektion til at hente oplysninger,der skal videregives til systemadministratoren eller supportmedarbejderne.

## <a name="working-with-page-inspection"></a>Arbejde med sideinspektion

Du starter sideinspektion fra siden **Hjælp og Support**. Vælg spørgsmålstegnet i øverste højre hjørne, vælg **Hjælp og support**, og vælg derefter **Undersøg sider og data**. Du kan også bare bruge tastaturgenvejen **Ctrl+Alt+F1**.

Ruden **Sideinspektion** åbnes på siden. Følgende figur illustrerer ruden **Sideinspektion** på siden **Salgsordre**.

![Sideinspektion](media/page-inspection-example.png)

Når ruden **Sideinspektion** åbnes første gang, indeholder den oplysninger, der vedrører hovedsidens objekt.

Bruge tastaturgenvejen eller pegeredskabet til at flytte fokus til forskellige elementer på siden. Når du vælger en faktaboks eller et element på hovedsiden, er det omgivende område fremhævet med en kant, og ruden **Sideinspektion** viser oplysninger om det valgte element. Den foregående figur viser f.eks. oplysninger om oversigtsdelen på siden **Salgsordre**. Når du navigerer til andre sider i programmet, opdateres ruden **Sideinspektion** automatisk med sideoplysningerne, mens du bevæger dig videre.

Du kan finde flere oplysninger om, hvad der vises i sideinspektionen, i [Inspektion og fejlfinding af sider](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) i hjælpen til Business Central-udviklere og it-eksperter.

Hvis du ikke kan se de oplysninger, du forventer at se, i ruden **Sideinspektion**, har du sandsynligvis ikke de nødvendige rettigheder som beskrevet i næste afsnit.

## <a name="controlling-access-to-page-inspection-details"></a>Styring af adgang til oplysninger om sideinspektion

Som administrator kan du styre adgang til alle detaljer, der vises i ruden **Sideinspektion**, ved at konfigurere de rettigheder, som brugere har. Hvis du vil tildele en bruger rettigheder til alle detaljer, skal du give vedkommende rettigheden **Udfør** til **System** objekt **5330**. Du kan give denne rettighed ved hjælp af et rettighedssæt (f.eks. **D365-fejlfinding**) eller en brugergruppe (f.eks. **D365-fejlfinding**). Du kan finde flere oplysninger om rettigheder i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).

Brugere, der ikke tildeles rettigheder i **Systemobjekt 5330**, kan stadig få adgang til ruden **Sideinspektion**, men de får kun vist felterne **Side** og **Tabel**, der viser grundlæggende oplysninger, som de kan videregive til deres supportteam.

## <a name="see-also"></a>Se også

[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
