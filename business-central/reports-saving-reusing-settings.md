---
title: Anvende og ændre gemte indstillinger i rapporter | Microsoft Docs
description: Beskriver foruddefinerede indstillinger og filtre, der bruges til at tilpasse en rapport og til at generere de korrekte data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6d83597057975757354da06668a7e71e94e5273f
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435759"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Administrere gemte indstillinger for rapporter og kørsler
Når brugerne kører rapporter, får de normalt vist en side, hvor de kan vælge indstillinger og angive filtre for at ændre, hvilke data der skal medtages i den genererede rapport. Denne side kaldes anmodningssiden. En rapport kan medtage én eller flere *gemte indstillinger*, som brugerne kan anvende til rapporten fra anmodningssiden. *Gemte indstillinger* er grundlæggende foruddefinerede indstillinger og filtre. Med gemte indstillinger kan du hurtigt og pålideligt generere ensartede rapporter, der indeholder de korrekte data. Du kan finde flere oplysninger i [Bruge gemte indstillinger](ui-work-report.md#SavedSettings).

> [!NOTE]
> I dette emne omtales hovedsageligt "rapport", men lignende oplysninger gælder for kørsler.

Hvis du har de nødvendige tilladelser, kan du få vist, oprette og redigere de gemte indstillinger for alle rapporter for alle brugere i en virksomhed. Du kan tildele gemte indstillinger for en rapport til enkelte brugere eller til alle brugere i virksomheden.

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a>Sådan oprettes og redigeres gemte indstillinger for alle brugere
Du administrerer gemte indstillinger på siden **Rapportindstillinger**. Du kan åbne siden på to måder:
-   Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Rapportindstillinger**, og vælg derefter det relaterede link.
-   Åbn en rapport, vælg opslaget i feltet **Brug standardværdier fra**, og vælg derefter handlingen **Vælg fra komplet liste**.

Siden viser alle eksisterende poster for gemte indstillinger for alle brugere. Hvis der er et brugernavn i feltet **Tildelt til**, er det kun denne bruger, der kan bruge de gemte indstillinger for den tilknyttede rapport. Hvis der er en markering i feltet **Del med alle brugere**, kan alle brugere anvende de gemte indstillinger for rapporten.

Fra siden **Rapportindstillinger** kan du:
-   Vælge handlingen **Ny** for at oprette en ny post for gemte indstillinger fra bunden.
-   Vælg en post for gemte indstillinger på listen, og vælg handlingen **Kopiér** for at oprette en kopi.
-   Vælg en post for gemte indstillinger på listen, og vælg handlingen **Rediger** for at ændre en post for gemte indstillinger.

> [!Important]
> Overvej, hvilket navn du giver en post for gemte indstillinger. Hvis du opretter en post for gemte indstillinger for alle brugere, og du giver den samme navn som en eksisterende post for gemte indstillinger, som er tildelt til en bestemt bruger, kan den pågældende bruger ikke anvende den post for gemte indstillinger, der er tildelt til alle.  I sektionen **Gemte indstillinger** på rapportanmodningssiden får brugeren vist to poster for gemte indstillinger med det samme navn. Men uanset hvilken indstilling brugeren vælger, anvendes den brugerspecifikke post for gemte indstillinger.

> [!NOTE]
> Funktionen Gemte indstillinger for rapporter er kun tilgængelig, når egenskaben [SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) for rapportens anmodningsside er indstillet til **Ja**. Egenskaben **SaveValues** indstilles i udviklingsmiljøet.  

## <a name="see-also"></a>Se også
[Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]