---
title: "Anvende og ændre gemte indstillinger i rapporter | Microsoft Docs"
description: Beskriver foruddefinerede indstillinger og filtre, der bruges til at tilpasse en rapport og til at generere de korrekte data.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 9fd086831c0d145570d87c33c62a003c166aca87
ms.contentlocale: da-dk
ms.lasthandoff: 11/22/2018

---
# <a name="managing-saved-settings-on-reports"></a>Administrere gemte indstillinger i rapporter
Når brugerne kører en rapport, får de normalt vist en side, hvor de kan angive bestemte indstillinger og filtre for at ændre, hvilke data der skal medtages i den genererede rapport. Denne side kaldes rapportanmodningssiden. En rapport kan medtage én eller flere *gemte indstillinger*, som brugerne kan anvende til rapporten fra anmodningssiden. *Gemte indstillinger* er grundlæggende foruddefinerede indstillinger og filtre. Med gemte indstillinger kan du hurtigt og pålideligt generere ensartede rapporter, der indeholder de korrekte data. Du kan finde flere oplysninger om, hvordan gemte indstillinger bruges, under [Bruge gemte indstillinger](ui-work-report.md#SavedSettings).

Hvis du har de nødvendige tilladelser, kan du få vist, oprette og redigere de gemte indstillinger for alle rapporter for alle brugere i virksomheden. Du kan tildele gemte indstillinger for en rapport til enkelte brugere eller alle brugere i virksomheden.

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a>Oprette og redigere gemte indstillinger for alle brugere
Du administrerer gemte indstillinger fra siden **1560 Rapportindstillinger**. Du kan åbne siden på to måder:
-   Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rapportindstillinger**, og vælg derefter det relaterede link.
-   Åbn en rapport, vælg opslaget ud for feltet **Brug standardværdier fra:** og vælg **Vælg fra komplet liste**.

Siden viser alle eksisterende Gem indstillinger-poster for alle brugere. Hvis der er et brugernavn i kolonnen **Tildelt til**, er det kun denne bruger, der kan bruge de gemte indstillinger for den tilknyttede rapport. Hvis der er en markering i kolonnen **Del med alle brugere**, kan alle brugere anvende de gemte indstillinger for rapporten.

Fra siden **Rapportindstillinger** kan du:
-   Vælge **Ny** for at oprette en ny post for gemte indstillinger fra bunden.
-   Vælg en post for gemte indstillinger på listen, og vælg **Kopier** for at oprette en kopi.
-   Vælg en post for gemte indstillinger på listen, og vælg **Rediger** for at ændre en post for gemte indstillinger.


> [!Important]
> Overvej, hvilket navn du giver en post for gemte indstillinger. Hvis du opretter en post for gemte indstillinger for alle brugere, og du giver den samme navn som en eksisterende post for gemte indstillinger, som er tildelt til en bestemt bruger, kan den pågældende bruger ikke anvende den post for gemte indstillinger, der er tildelt til alle.  Under **Gemte indstillinger** på rapportanmodningssiden får brugeren vist to poster for gemte indstillinger med det samme navn. Men uanset hvilken indstilling brugeren vælger, anvendes den brugerspecifikke post for gemte indstillinger.

> [!NOTE]
> Funktionen for gemte indstillinger for rapporter er kun tilgængelig, når [egenskaben SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) for rapportens anmodningsside er indstillet til `Yes`. Egenskaben **SaveValues** indstilles i udviklingsmiljøet.  

## <a name="see-also"></a>Se også
[Arbejde med rapporter](ui-work-report.md)  

