---
title: Arbejde med Business Central-data i Microsoft Teams| Microsoft Docs
description: Sådan bruger du Business central-app til Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 0f7c1e8016a1bc1915d7d6a54a183aa0e8cea2ea
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046450"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Arbejde med Business Central-data i Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] tilbyder en app, der har forbindelse Microsoft Teams til dine forretningsdata [!INCLUDE [prod_short](includes/prod_short.md)], så du hurtigt kan dele detaljer på tværs af gruppemedlemmer og reagere hurtigere på forespørgsler. I denne artikel lærer du, hvordan du kan bruge appen til at dele [!INCLUDE [prod_short](includes/prod_short.md)] data med kolleger i en samtale med grupper.

## <a name="overview"></a>Oversigt

Med [!INCLUDE [prod_short](includes/prod_short.md)]-appen kan du:

- Kopiere et hyperlink til en hvilken som helst Business Central-post og sætte den ind i en Teams-samtale, som du kan dele med dine kolleger. Appen udvider derefter linket til et kompakt, interaktivt kort, der viser oplysninger om posten.
- Når du er i samtalen, kan du og dine kolleger få vist flere oplysninger om posten, redigere data og handle - uden at forlade&mdash;Teams.

[![Teams-integration med Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Forudsætninger

- Du har adgang til Microsoft Teams.
- Du har installeret [!INCLUDE [prod_short](includes/prod_short.md)]-appen i grupper. Du kan finde flere oplysninger under [Installere [!INCLUDE [prod_short](includes/prod_short.md)]-app til Microsoft Teams](across-install-app-for-teams.md).

> [!NOTE]
> Alle deltagerne i en samtale med Teams vil kunne få vist kort til Business Central-poster, som du sender til samtalen. Men hvis du vil have vist flere detaljer om poster, bruge **Detaljer** eller **Pop-op**-knapper på et kort, skal de have adgang til [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger under [Administrere Microsoft Teams-integration](admin-teams-integration.md#minimum-requirements-1).

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Medtage et Business Central-kort i en samtale med Teams

1. Log ind [!INCLUDE [prod_short](includes/prod_short.md)] for at bruge browseren.
2. Åbn den post, du vil dele.

    Appen er designet til at vise sider med korttyper fra [!INCLUDE [prod_short](includes/prod_short.md)]. Åbne en side, hvor der vises en enkelt post, f. eks. en vare, kunde eller salgsordre. Du kan ikke bruge den til rollecentre eller sider, hvor der vises flere poster på en liste.

3. Kopiere hele URL-adressen fra browserens adresselinje.

   ![Kopiere Business Central URL-adresse fra browser](media/teams-url-v2.png)
4. Gå til Teams, og start en samtale, som kan chatte med en person, en gruppe personer eller en team-kanal.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Indsætte URL-adressen i den meddelelsesboks, hvor du samler en meddelelse.

   ![Indsætte Business Central URL-adresse i Teams](media/teams-paste-url-v2.png)
6. Første gang du indsætter et hyperlink til en samtale, bliver du bedt om at logge på [!INCLUDE [prod_short](includes/prod_short.md)] og give appen tilladelse til at hente data. Du skal blot følge vejledningen på skærmen.

    > [!NOTE]
    > Du behøver kun at udføre dette trin én gang.

7. Vent et øjeblik, mens der genereres et kort i meddelelsesboksen.

8. Når kortet vises, skal kortets indhold gennemgås omhyggeligt for alle følsomme oplysninger, før du sender meddelelsen. Dette trin er vigtigt, fordi alle i samtalen kan se kortet, når du har sendt meddelelsen.

9. Hvis kortet ser flot ud, skal vælge **Send** for at sende det til samtalen.

    > [!TIP]
    > Når kortet vises, og før du vælger **Send**, kan du slette den indsatte URL-adresse, hvis du vil.

10. Hvis du vil have vist flere detaljer eller foretage ændringer i posten, skal du vælge **Detaljer**. Der er flere oplysninger i næste sektion.

## <a name="view-card-details"></a>Vis kortdetaljer

Når et kort er sendt til en samtale, kan alle deltagere med de [rette tilladelser](admin-teams-integration.md#permissions) vælge **Detaljer** for at åbne et vindue, der indeholder flere oplysninger om posten&mdash;og muligvis foretage ændringer af posten. Det betyder ikke noget, hvis du er det, der afsender kortet, eller den, der modtagerkortet. Funktionen **Detaljer** er især nyttig for modtagere, da den hurtigt leverer præcise, målrettede oplysninger om posten i modsætning til at skulle scanne hele posten.

Vinduet Detaljer svarer til det, du kan se i posten [!INCLUDE [prod_short](includes/prod_short.md)]. Men det er en smule beskåret for grupper. Når du er færdig med at gennemse og foretage ændringer, skal du lukke vinduet for at vende tilbage til samtalerne med team.

Her er et par ting, du skal være opmærksom på, når du arbejder med kort detaljer:

- Hvis du vil åbne kortoplysninger, skal brugere have tilladelse på siden og data i [!INCLUDE [prod_short](includes/prod_short.md)].
- Kort i Teams-chats opdateres ikke automatisk til ændringer. Alle de ændringer, du gemmer i en post i vinduet detaljer, gemmes i [!INCLUDE [prod_short](includes/prod_short.md)]. Men kortet i Teams viser ikke ændringerne i konverteringen, før du indsætter kæden igen.

Du kan få mere at vide om, hvordan du arbejder med kort og kort detaljer, i [Teams, ofte stillede spørgsmål](teams-faq.md).

## <a name="see-also"></a>Se også

[Business Central og Microsoft Teams Oversigt over integration](across-teams-overview.md)  
[Installér appen [!INCLUDE [prod_short](includes/prod_short.md)] til Microsoft Teams](across-install-app-for-teams.md)  
[Teams, ofte stillede spørgsmål](teams-faq.md)  
[Fejlfinding i Teams](admin-teams-troubleshooting.md)  
[Udvikling af Teams-integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
