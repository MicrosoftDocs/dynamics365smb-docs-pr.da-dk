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
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989412"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Arbejde med Business Central-data i Microsoft Teams

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

[!INCLUDE [prodshort](includes/prodshort.md)] tilbyder en app, der har forbindelse Microsoft Teams til dine forretningsdata [!INCLUDE [prodshort](includes/prodshort.md)], så du hurtigt kan dele detaljer på tværs af gruppemedlemmer og reagere hurtigere på forespørgsler. I denne artikel lærer du, hvordan du kan bruge appen til at dele [!INCLUDE [prodshort](includes/prodshort.md)] data med kolleger i en samtale med grupper.

## <a name="overview"></a>Oversigt

Med [!INCLUDE [prodshort](includes/prodshort.md)]-appen kan du:

- Kopiere et hyperlink til en hvilken som helst Business Central-post og sætte den ind i en Teams-samtale, som du kan dele med dine kolleger. Hyperlinket vil vise et kompakt, interaktivt kort, der viser oplysninger om posten.
- Når du er i samtalen, kan du og dine kolleger få vist flere oplysninger om posten, redigere data og handle uden at forlade Teams.

[![Teams-integration med Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Forudsætninger

- Du har adgang til Microsoft Teams.
- Du har installeret [!INCLUDE [prodshort](includes/prodshort.md)]-appen i grupper. Du kan finde flere oplysninger under [Installere [!INCLUDE [prodshort](includes/prodshort.md)]-app til Microsoft Teams](across-install-app-for-teams.md).

> [!NOTE]
> Alle deltagerne i en samtale med Teams vil kunne få vist kort til Business Central-poster, som du sender til samtalen. Men hvis du vil have vist flere detaljer om poster, bruge **Detaljer** eller **Pop-op**-knapper på et kort, skal de have adgang til [!INCLUDE [prodshort](includes/prodshort.md)]. Du kan finde flere oplysninger under [Administrere Microsoft Teams-integration](admin-teams-integration.md#minimum-requirements-1).
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Medtage et Business Central-kort i en samtale med Teams

1. Log ind [!INCLUDE [prodshort](includes/prodshort.md)] for at bruge browseren.
2. Åbn den post, du vil dele.

    Appen er designet til at vise sider med korttyper fra [!INCLUDE [prodshort](includes/prodshort.md)]. Åbne en side, hvor der vises en enkelt post, f. eks. en vare, kunde eller salgsordre. Du kan ikke bruge den til rollecentre eller sider, hvor der vises flere poster på en liste.

3. Kopiere hele URL-adressen fra browserens adresselinje.

   ![Kopiere Business Central URL-adresse fra browser](media/teams-url.png)
4. Gå til Teams, og start en samtale, som kan chatte med en person, en gruppe personer eller en team-kanal.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Indsætte URL-adressen i den boks, hvor du tilføjer en meddelelse.

   ![Indsætte Business Central URL-adresse i Teams](media/teams-paste-url.png)
6. Første gang du indsætter et hyperlink til en samtale, bliver du bedt om at logge på [!INCLUDE [prodshort](includes/prodshort.md)] og give appen tilladelse til at hente data. Du skal blot følge vejledningen på skærmen.

    > [!NOTE]
    > Du behøver kun at udføre dette trin én gang.

7. Vent et øjeblik, mens der genereres et kort i meddelelsesboksen.

8. Når kortet vises, skal kortets indhold gennemgås omhyggeligt for alle følsomme oplysninger, før du sender meddelelsen. Dette trin er vigtigt, fordi alle i samtalen kan se kortet, når du har sendt meddelelsen.

9. Hvis kortet ser flot ud, skal vælge **Send** for at sende det til samtalen.

    > [!TIP]
    > Når kortet vises, og før du vælger **Send**, kan du slette den indsatte URL-adresse, hvis du vil.

10. Hvis du vil have vist flere detaljer eller foretage ændringer i posten, skal du vælge **Detaljer**.

    Siden detaljer svarer til det, du kan se i [!INCLUDE [prodshort](includes/prodshort.md)]. Men det er en smule beskåret for grupper. Når du er færdig med at gennemse og foretage ændringer, skal du lukke vinduet for at vende tilbage til samtalerne med team.

    > [!NOTE]
    > De ændringer, du foretager, afspejles ikke på kortet, før næste gang du indsætter et hyperlink til en samtale.

## <a name="see-also"></a>Se også

[Business Central og Microsoft Teams Oversigt over integration](across-teams-overview.md)  
[Installér appen [!INCLUDE [prodshort](includes/prodshort.md)] til Microsoft Teams](across-install-app-for-teams.md)  
[Udvikling af Teams-integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Introduktion](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
