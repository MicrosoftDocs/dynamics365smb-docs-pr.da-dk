---
title: Deling af data
description: Få mere at vide om de forskellige måder, du kan dele forretningsdata fra Business central.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 09/21/2022
ms.author: jswymer
ms.openlocfilehash: e54cabd331253a40b160a6cc89b4ab170bd1db89
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607468"
---
# <a name="sharing-business-data-from-business-central"></a>Dele forretnings data fra Business central

Samarbejde mellem personer i og uden for en organisation er integreret del af de fleste virksomheder. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder flere funktioner til deling af forretningsdata, som f. eks. en liste over poster, specifikke poster eller dokumenter. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Med alle disse funktioner er adgangen til data beskyttet af licensen og tilladelserne fra Business central.

## <a name="copying-a-link"></a>Kopiering af link

![Understøttet](media/check.png) Business Central Online ![Understøttet](media/check.png) Business Central i det lokale miljø

Du kan kopiere sidens URL-adresse fra en hvilken som helst side, indsætte den og distribuere den i andre former for medier, f. eks. mails, team chats eller SMS-beskeder. Den nemmeste måde at kopiere et hyperlink på er ved at vælge **del** > **Kopier link** øverst på siden. Du kan også kopiere URL-adressen direkte fra browserens adressefelt.

### <a name="modify-the-page-link"></a>Rediger side hyperlinket

Når du har kopieret et hyperlink, kan du ændre URL-adressen til, hvad der vises, når siden åbnes, inden du sender det. Du kan f. eks. tilføje filtre eller angive et andet regnskab.

Du kan finde flere oplysninger på [webstedet](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### <a name="about-filtered-lists"></a>Om filtrerede lister

Ved hjælp af filterruden på listesider kan du indsætte filtre for at begrænse de poster, der vises på listen. Hvis du bruger handlingen **Kopier link** eller kopierer URL-adressen fra browseren, indeholder side hyperlinket ikke filter ændringerne. Brugere, der åbner linket, får vist hele samlingen. På den måde kan du bevare filtreringen på en samlings side kæde ved først at gemme den filtrerede side som en **visning**. Derefter skal du åbne visningen og kopiere hyperlinket derfra.

Du kan finde flere oplysninger i [Sortering, søgning og filtrering](ui-enter-criteria-filters.md).

## <a name="sharing-to-teams"></a>Dele med Teams

![Understøttet](media/check.png) Business Central Online ![Ikke understøttet](media/x-icon.png) Business Central i det lokale miljø

Direkte fra de fleste samlingssider og detaljesider kan du sende et link til siden til personer, gruppechats eller kanaler. Du kan f. eks. dele et hyperlink til en filtreret visning af dine poster. Hvis du har installeret [!INCLUDE[prod_short](includes/prod_short.md)]-appen for Teams, udvides linket automatisk til et kompakt kort, så du kan medtage det i din meddelelse. Modtagerne kan derefter vælge linket eller kortet for at åbne siden i Business Central.

Du kan finde flere oplysninger i [Dele poster og sidelinks i Teams](across-working-with-teams.md).

## <a name="sharing-through-onedrive"></a>Deling via OneDrive

![Understøttet](media/check.png) Business Central Online ![Understøttet](media/check.png) Business Central i det lokale miljø

Business Central gør det nemt at gemme, administrere og dele filer med andre personer via OneDrive for Business. På de fleste sider, hvor filer er tilgængelige, som f.eks. Rapportindbakke eller filer, der er vedhæftet til poster, finder du en he **Åbn i OneDrive**- og **Dele**-handling. Begge handlinger gemmer en kopi af en fil i OneDrive. Når du er i OneDrive, kan du bruge programmets delings- og bidragsfunktioner på filen. Forskellen i handlingerne er, at **Åbn i OneDrive** åbner filen i OneDrive. **Del** åbner en side, hvor du kan vælge, hvem du vil dele filen med. Modtagerne får en notifikationsmail for at få adgang til filen fra din OneDrive.

Du kan finde flere oplysninger i [Dele filer i OneDrive](across-share-onedrive.md).

## <a name="opening-in-excel"></a>Åbne i Excel

![Understøttet](media/check.png) Business Central Online ![Understøttet](media/check.png) Business Central i det lokale miljø

Du kan bruge handlingen **Åbn i Excel** til listesider og lister, der er integreret på en side. Denne handling eksporterer listen over poster til en Excel-projektmappe (.xlsx-fil), som du kan dele med andre. Du kan også bruge funktionen share, som er en del af Excel, i projektmappen.

Du kan finde flere oplysninger i [Vise og redigere i Excel](across-work-with-excel.md).

## <a name="sharing-rows-or-tables"></a>Dele rækker eller tabeller

![Understøttet](media/check.png) Business Central Online ![Understøttet](media/check.png) Business Central i det lokale miljø

Du kan dele en eller flere poster på en liste. Tryk på genvejstasten CTRL + C for at kopiere til Udklipsholder. Indsæt derefter det, du har kopieret, til et andet program ved at trykke på CTRL + V. Hvis du kopierer tre salgsordrer og indsætter dem i en e-mail, vises ordrerne f. eks. i en nicely formateret tabel.

Du kan finde flere oplysninger i [Ofte stillede spørgsmål om kopiering og indsætning](faq-copy-paste.yml).

## <a name="see-also"></a>Se også

[Business Central og OneDrive-integration](across-onedrive-overview.md)  
[Administration af OneDrive-integration med Business Central](admin-onedrive-integration.md)  
[OneDrive Ofte stillede spørgsmål](admin-onedrive-faq.md)