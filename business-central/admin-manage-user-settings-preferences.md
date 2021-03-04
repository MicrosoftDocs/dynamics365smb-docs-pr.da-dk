---
title: Administrere brugerindstillinger og præferencer i Dynamics 365 Business Central
description: Administrere brugerindstillinger og præferencer i Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.date: 10/01/2020
ms.author: soalex
ms.openlocfilehash: 25b3c8a795c1a3f9d08ae0971da88b78e4d29b25
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752571"
---
# <a name="manage-user-settings-and-preferences"></a>Administrere brugerindstillinger og præferencer

Som administrator kan du bruge indstillinger i [!INCLUDE[prod_short](includes/prod_short.md)] på samme måde, som de enkelte brugere kan administrere deres egne indstillinger på siden **Mine indstillinger**.  

## <a name="types-of-user-settings"></a>Typer af brugerindstillinger

*Brugerindstillinger* er ikke det samme som *brugeropsætning*, som er om brugeren som enhed og brugerens adgang til systemet. Desuden har brugerindstillinger intet at gøre med en brugers personlige tilpasning, f.eks. en lettere ændring af brugergrænsefladen. Brugerindstillingerne bestemmer brugerens præferencer i forskellige aspekter af den måde, som programmet præsenterer sig for brugeren på. I følgende afsnit vises de fem typer brugerindstillinger og præferencer, som kan angives af den enkelte eller centralt af administratoren.

- **Virksomhed**  

  Denne indstilling bestemmer, hvilken virksomhed der skal logges på ved næste logon. En bruger kan få adgang til flere virksomheder og kan være aktiv i flere virksomheder.

- **Profil (roller)**  

  Profilen beskriver brugerens funktion i virksomheden, f.eks. *Salgschef*, *Bogholder* eller *Indkøber*. Profilen bestemmer derefter brugerens rollecenter, den startside, som brugerne får vist, når de logger på. Profilen har ingen indflydelse på adgangsrettighederne til funktionalitet i [!INCLUDE[prod_short](includes/prod_short.md)].  

- **Landestandard-id (internationale indstillinger)**  

  Definerer, hvordan datoer og tal præsenteres i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten, f.eks. om der skal bruges europæiske eller amerikanske datoformater, eller hvordan decimaltegnet og tusindtalsseparatorer vises i beløb. Hvis [!INCLUDE[prod_short](includes/prod_short.md)]-brugerne synkroniseres fra Microsoft 365, bruges de regionale indstillinger fra Microsoft 365, hvis brugeren vil have de samme indstillinger i Office-produkter og [!INCLUDE[prod_short](includes/prod_short.md)]. En administrator eller bruger kan ændre disse indstillinger manuelt i [!INCLUDE[prod_short](includes/prod_short.md)], men de vil blive nulstillet til værdien fra Microsoft 365, så snart næste synkronisering udføres.

- **Sprog**  

  Definerer det programsprog, som [!INCLUDE[prod_short](includes/prod_short.md)] viser tekst, billedtekster og fejlmeddelelser på. Hvis [!INCLUDE[prod_short](includes/prod_short.md)]-brugerne synkroniseres fra Microsoft 365, bruges de sprogindstillinger fra Microsoft 365, hvis brugeren vil have de samme indstillinger i Office-produkter og [!INCLUDE[prod_short](includes/prod_short.md)]. En administrator eller bruger kan ændre disse indstillinger manuelt i [!INCLUDE[prod_short](includes/prod_short.md)], men de vil blive nulstillet til værdien fra Microsoft 365, så snart næste synkronisering udføres.

  Hvis sprogindstillingen fra Microsoft 365 passer til et sprog, der understøttes i [!INCLUDE[prod_short](includes/prod_short.md)], vil dette sprog blive valgt for brugeren.  

  > [!NOTE]
  > Du skal muligvis installere en sprogapp til [!INCLUDE[prod_short](includes/prod_short.md)] for at få vist sproget korrekt. Det er derfor en god idé at installere de nødvendige sprogapps, før nogen bruger logger på første gang, så de får en god oplevelse fra den første dag. Du kan finde flere oplysninger på listen over [understøttede sprog](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
- **Tidszone**  

  Definerer den tidszone, hvor brugeren opholder sig. Denne bliver i øjeblikket ikke synkroniseret fra Microsoft 365 og skal angives manuelt.  

> [!NOTE]
> Hvis der udføres en Microsoft 365-brugersynkronisering, mens brugerne er logget på [!INCLUDE[prod_short](includes/prod_short.md)], skal disse brugere opdatere browseren eller logge af og på igen [!INCLUDE[prod_short](includes/prod_short.md)] for at få vist et potentielt andet sprog, der er angivet i synkroniseringshandlingen.

## <a name="overview-of-all-user-settings"></a>Oversigt over alle brugerindstillinger

Administratorer har mulighed for at angive eller ændre disse indstillinger for brugere i enhver virksomhed. Dette gøres på siden **Brugertilpasninger**. Poster på denne side afspejler den enkelte brugers valg af ovenstående indstillinger, dvs. én post pr. bruger. Efterhånden som brugerne foretager ændringer af indstillingerne på siden **Mine indstillinger**, afspejles disse ændringer på listen **Brugertilpasninger**. Administratorer kan også angive disse indstillinger for brugere, før de logger på første gang, så brugere ikke behøver at gøre det selv, hvilket giver dem en bedre *introduktion*.

> [!NOTE]
> Brugertilpasninger har ikke noget at gøre med de små *personlige* ændringer, som en bruger kan foretage af brugeroplevelsen.

## <a name="to-review-or-make-changes-to-user-settings"></a>Sådan gennemses eller ændres brugerindstillinger

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), åbn **Brugertilpasninger**, og vælg derefter det relaterede link.
2. Dette viser listen over brugere og deres indstillinger. Hvis du vil redigere en brugers indstillinger, skal du klikke på **Bruger-id** eller vælge **Administrer** og derefter **Rediger**.
3. Kortet **Brugertilpasning** til den specifikke brugers indstillinger vises, og de ønskede ændringer kan foretages.  

## <a name="see-also"></a>Se også

[Introduktion](product-get-started.md)  
[Tilgængelighed i land/område og understøttede sprog](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Ændre sprog og landestandard](about-locale-language.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]