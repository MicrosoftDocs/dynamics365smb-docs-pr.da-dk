---
title: Dele Business Central-poster i Microsoft Teams
description: Sådan bruger du Business central-app til Microsoft Teams.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records
ms.date: 09/22/2022
ms.author: jswymer
ms.openlocfilehash: 17be576dad0eaf31918951e4e11a73acdd0ae70e
ms.sourcegitcommit: b4da421c19c3aa3031b0344ec2829d2038be6642
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617789"
---
# <a name="sharing-business-central-records-and-page-links-in-microsoft-teams"></a>Dele Business Central-poster og Sidelinks i Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] giver dig mulighed for at dele data fra Business central direkte i en Microsoft Teams-samtale.

<!-- 
## Overview
In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.
The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:
[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries. In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.

-->
- Når [!INCLUDE [prod_short](includes/prod_short.md)]-appen er installeret i Teams, kan du medtage et interaktivt kort fra en Business Central-post i en Teams-samtale.

<!--   Copy a link from any Business Central record, like a customer or sales order, then paste the link into a Teams conversation. The app connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)]. It then expands the link into a compact, interactive card that displays information about the record. Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.

  [![Teams integration with Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)-->

- Med eller uden [!INCLUDE [prod_short](includes/prod_short.md)]-app'en installeret kan du dele et link fra sider i Business central til en Teams-samtale.

  <!-- ![!The Share menu displayed on a card.](media/teams-share-link.png "The Share menu displayed on a card.")-->

I de følgende afsnit beskrives det, hvordan du bruger de forskellige metoder.

## <a name="include-and-view-a-business-central-card-in-a-teams-conversation"></a>Medtage og se et Business Central-kort i en Teams-samtale

Med Business central-appen til Teams kan du kopiere et link fra en hvilken som helst Business Central-post, som f. eks. en kunde eller salgsordre, og indsætte linket i en Teams-samtale. Appen forbinder Microsoft Teams til dine forretningsdata i [!INCLUDE [prod_short](includes/prod_short.md)]\. Derefter udvides linket til et kompakt, interaktivt kort, der viser oplysninger om posten. Når du er i samtalen, kan du og dine kolleger få vist flere oplysninger om posten, redigere data og handle - uden at forlade&mdash;Teams.

[![Teams-integration med Business Central.](media/teams-intro-vBC20.png)](media/teams-intro-vBC20.png#lightbox)

### <a name="prerequisites"></a>Forudsætninger

- Du har adgang til Microsoft Teams.
- Du har installeret [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams. Du kan finde flere oplysninger i [Installere [!INCLUDE [prod_short](includes/prod_short.md)]-app til Microsoft Teams](across-install-app-for-teams.md).

> [!NOTE]
> Alle deltagerne i en samtale med Teams vil kunne få vist kort til Business Central-poster, som du sender til samtalen. Men hvis du vil have vist flere detaljer om poster, bruge **Detaljer** eller **Pop-op**-knapper på et kort, skal de have adgang til [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Administrere Microsoft Teams-integration](admin-teams-integration.md#minimum-requirements-1).

### <a name="include-a-business-central-card-in-a-teams-conversation"></a>Medtage et Business Central-kort i en samtale med Teams

1. Log ind [!INCLUDE [prod_short](includes/prod_short.md)] for at bruge browseren.
2. Åbn den post, du vil dele.

    Appen er designet til at vise sider med korttyper fra næsten alle typer [!INCLUDE [prod_short](includes/prod_short.md)]-sider. Men det giver den bedste oplevelse, når du bruges til sider, hvor der vises en enkelt post, f. eks. en vare, en kunde eller en salgsordre.
3. Kopier linket til siden.

    Der er to måder at kopiere linket på. Den nemmeste og foretrukne måde er at vælge ikonet **Del** ![Del-ikon i Business Central](media/share-icon.png) > **Kopier link**. Du kan også kopiere URL-adressen direkte fra browserens adressefelt.

    [![Kopiere Business Central URL-adresse fra browser.](media/teams-copy-link.png)](media/teams-copy-link.png#lightbox)
4. Gå til Teams, og start en samtale, som kan chatte med en person, en gruppe personer eller en team-kanal.
5. Indsætte linkets URL-adresse i den meddelelsesboks, hvor du samler en meddelelse.

    ![Indsætte Business Central URL-adresse i Teams.](media/teams-paste-url-v2.png)

    > [!TIP]
    > Hvis der vises en meddelelse som f. eks *Business Central vil vise en forhåndsversion af dette link.*, det betyder, at du ikke har installeret Business central-appen til teams. Hvis du vil installere denne app, skal du vælge **Vis forhåndsversion** og følge instruktionerne.
6. Første gang du indsætter et hyperlink til en samtale, bliver du bedt om at logge på [!INCLUDE [prod_short](includes/prod_short.md)] og give appen tilladelse til at hente data. Du skal blot følge vejledningen på skærmen.

    > [!NOTE]
    > Du behøver kun at udføre dette trin én gang.
7. Vent et øjeblik, mens der genereres et kort i meddelelsesboksen.
8. Når kortet vises, skal kortets indhold gennemgås omhyggeligt for alle følsomme oplysninger, før du sender meddelelsen. Dette trin er vigtigt, fordi alle i samtalen kan se kortet, når du har sendt meddelelsen.
9. Hvis kortet ser flot ud, skal vælge **Send** for at sende det til samtalen.

    > [!TIP]
    > Når kortet vises, og før du vælger **Send**, kan du slette den indsatte URL-adresse, hvis du vil.
10. Hvis du vil have vist flere detaljer eller foretage ændringer i posten, skal du vælge **Detaljer**. Der er flere oplysninger i næste sektion.

### <a name="view-card-details"></a>Vis kortdetaljer

Når et kort er sendt til en samtale, kan alle deltagere med de [rette tilladelser](admin-teams-integration.md#permissions) vælge **Detaljer** for at åbne et vindue, der indeholder flere oplysninger om posten&mdash;og muligvis foretage ændringer af posten. Det betyder ikke noget, hvis du er det, der afsender kortet, eller den, der modtagerkortet. Funktionen **Detaljer** er især nyttig for modtagere, da den hurtigt leverer præcise, målrettede oplysninger om posten i modsætning til at skulle scanne hele posten.

Vinduet detaljer svarer til det, du kan se i [!INCLUDE [prod_short](includes/prod_short.md)], men det er fokuseret på siden eller posten, som kortet vedrører. Når du er færdig med at gennemse og foretage ændringer, skal du lukke vinduet for at vende tilbage til samtalerne med team.

Her er et par ting, du skal være opmærksom på, når du arbejder med kort detaljer:

- Hvis du vil åbne kortoplysninger, skal brugere have tilladelse på siden og data i [!INCLUDE [prod_short](includes/prod_short.md)]\.
- Kort i Teams-chats opdateres ikke automatisk til ændringer. Alle de ændringer, du gemmer i en post i vinduet detaljer, gemmes i [!INCLUDE [prod_short](includes/prod_short.md)]\. Men kortet i Teams viser ikke ændringerne i konverteringen, før du indsætter kæden igen.

Du kan få mere at vide om, hvordan du arbejder med kort og kort detaljer, i [Teams, ofte stillede spørgsmål](teams-faq.md).

## <a name="share-a-link-to-page-from-business-central-to-teams"></a><a name="share-link"></a>Dele links med sider i Business central til Teams

Direkte fra de fleste samlinger-sider, f. eks. siden **Varer** og detaljesider, som f. eks **Vare**-kort kan du sende et link til siden til bestemte modtagere i en Teams-samtale. Du kan f. eks. dele et hyperlink til en filtreret visning af dine poster. Modtagerne kan derefter vælge hyperlinket for at åbne siden i [!INCLUDE [prod_short](includes/prod_short.md)]\.

[![!Menuen Del vist på et kort.](media/teams-share-link-v2.png "Menuen Del vises på et kort.")](media/teams-share-link-v2.png#lightbox)

### <a name="prerequisites"></a>Forudsætninger

- Du har adgang til Microsoft Teams.
- (Valgfrit) Du har installeret [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams. 

  Når appen er installeret, vil de meddelelser, du sender med linket, også indeholde et kompakt kort for siden. Du kan finde flere oplysninger om, hvordan du installerer appen, i [Installation af [!INCLUDE [prod_short](includes/prod_short.md)]-app til Microsoft Teams](across-install-app-for-teams.md).

### <a name="share-a-link"></a>Del et link

1. I [!INCLUDE [prod_short](includes/prod_short.md)]\, åbnes den side, du vil dele.
2. Vælg på toppen af siden ![Del med andre app-handlinger på sider.](media/share-icon.png) ikonet og derefter **Del med Teams**.
3. Hvis du bliver bedt om det, skal du logge på Teams med dit brugernavn og din adgangskode.
4. På siden **Del med Teams** skal du skrive navnet på en person, gruppe eller kanal, som du vil sende meddelelsen til.
5. Meddelelsesboksen indeholder et link til siden. Hvis [!INCLUDE [prod_short](includes/prod_short.md)]-appen til Teams er installeret, vises der også et kort for den sammenkædede post eller side i meddelelsesboksen.

   Du kan tilføje flere oplysninger, hvis du vil, og derefter vælge **Del**.
6. Linket er nu blevet delt. Hvis du vil gå til samtalen, skal du vælge **Gå til Teams**.

## <a name="see-also"></a>Se også

[Oversigt over integrationen af Business Central og Microsoft Teams](across-teams-overview.md)  
[Installere appen [!INCLUDE [prod_short](includes/prod_short.md)] til Microsoft Teams](across-install-app-for-teams.md)  
[Teams, ofte stillede spørgsmål](teams-faq.md)  
[Søgning efter debitorer, kreditorer og andre kontakter fra Microsoft Teams](across-search-contacts-teams.md)  
[Ændring af virksomhed og andre indstillinger i Teams](across-teams-settings.md)  
[Fejlfinding i Teams](admin-teams-troubleshooting.md)  
[Udvikling af Teams-integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
