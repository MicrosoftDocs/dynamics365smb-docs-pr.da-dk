---
title: Administrere brugerindstillinger og-præferencer som administrator
description: Administrere brugerindstillinger og præferencer i Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: 'user settings, preferences, language, region, time zone, regional settings'
ms.search.form: '9204,'
ms.date: 04/01/2021
ms.author: soalex
---
# Administrere brugerindstillinger og præferencer

Som administrator kan du konfigurere brugerindstillinger i [!INCLUDE[prod_short](includes/prod_short.md)] på samme måde, som de enkelte brugere kan administrere deres egne indstillinger på siden **Mine indstillinger**.  

Få vist en oversigt over alle brugere på listen **Brugere**, og rediger individuelle indstillinger ved at vælge handlingen **Brugerindstillinger** for den relevante bruger.

> [!TIP]
> Listen **Brugerindstillinger** viser de aktuelle indstillinger for hver bruger. Hvis du vil have vist eller redigere individuelle brugere, skal du vælge handlingen **Vis** eller **Rediger**.

Siden **Brugerindstillingskort** svarer til ruden **Mine indstillinger**, som hver bruger har adgang til. Den er et effektivt værktøj for dig som administrator, hvor du f.eks. kan angive standardindstillinger og rydde tilpassede sider.  

## Typer af brugerindstillinger

*Brugerindstillinger* er ikke det samme som *brugeropsætning*, som er om brugeren som enhed og brugerens adgang til systemet. Desuden har brugerindstillinger intet at gøre med en brugers personlige tilpasning, f.eks. en lettere ændring af brugergrænsefladen. Brugerindstillinger bestemmer de foruddefinerede indstillinger for hver bruger i forhold til de forskellige måder, programmet vises på over for brugeren. I følgende afsnit vises de fem typer brugerindstillinger og præferencer, som kan angives af den enkelte eller centralt af administratoren.

* **Virksomhed**  

  Denne indstilling bestemmer, hvilken virksomhed der skal logges på ved næste logon. En bruger kan få adgang til flere virksomheder og kan være aktiv i flere virksomheder.

* **Rolle**  

  Rollen eller profilen beskriver brugerens funktion i virksomheden, f.eks. *Salgschef*, *Bogholder* eller *Indkøber*. Profilen bestemmer derefter brugerens rollecenter, den startside, som brugerne får vist, når de logger på. Profilen har ingen indflydelse på adgangsrettighederne til funktionalitet i [!INCLUDE[prod_short](includes/prod_short.md)].  

* **Sprog**  

  Definerer det programsprog, som [!INCLUDE[prod_short](includes/prod_short.md)] viser tekst, billedtekster og fejlmeddelelser på. Hvis [!INCLUDE[prod_short](includes/prod_short.md)]-brugerne synkroniseres fra Microsoft 365, bruges sprogindstillinger fra Microsoft 365, hvis brugeren vil have de samme indstillinger i Office-produkter og [!INCLUDE[prod_short](includes/prod_short.md)]. Administratoren kan ændre standardindstillingen, og hver bruger kan vælge mellem de tilgængelige sprog på siden Mine indstillinger. Men indstillinger bliver nulstillet til værdien fra Microsoft 365, når den næste synkronisering udføres.

  Hvis sprogindstillingen fra Microsoft 365 passer til et sprog, der understøttes i [!INCLUDE[prod_short](includes/prod_short.md)], vil dette sprog blive valgt for brugeren.  

  > [!NOTE]
  > Du skal muligvis installere en sprogapp til [!INCLUDE[prod_short](includes/prod_short.md)] for at få vist sproget korrekt. Det er derfor en god idé at installere de nødvendige sprogapps, før nogen bruger logger på første gang, så de får en god oplevelse fra den første dag. Du kan finde flere oplysninger på listen over [understøttede sprog](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
* **Område**  

  Definerer, hvordan datoer og tal præsenteres i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten, f.eks. om der skal bruges europæiske eller amerikanske datoformater, eller hvordan decimaltegnet og tusindtalsseparatorer vises i beløb. Hvis [!INCLUDE[prod_short](includes/prod_short.md)]-brugerne synkroniseres fra Microsoft 365, bruges de internationale indstillinger fra Microsoft 365, hvis brugeren vil have de samme indstillinger i Office-produkter og [!INCLUDE[prod_short](includes/prod_short.md)]. En administrator eller bruger kan ændre disse indstillinger manuelt i [!INCLUDE[prod_short](includes/prod_short.md)], men de vil blive nulstillet til værdien fra Microsoft 365, så snart næste synkronisering udføres.

* **Tidszone**  

  Definerer den tidszone, hvor brugeren opholder sig. Denne bliver i øjeblikket ikke synkroniseret fra Microsoft 365 og skal angives manuelt.  

* **Undervisningstip**

  [!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)] Som administrator kan du slå undervisningstip fra for alle brugere, f.eks. hvis du arbejder på at onboarde brugere, der allerede kender [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Hvis der udføres en Microsoft 365-brugersynkronisering, mens brugerne er logget på [!INCLUDE[prod_short](includes/prod_short.md)], skal disse brugere opdatere browseren eller logge af og på igen [!INCLUDE[prod_short](includes/prod_short.md)] for at få vist et potentielt andet sprog, der er angivet i synkroniseringshandlingen.

## Oversigt over alle brugerspecifikke ændringer

Som administrator kan du få en oversigt over de individuelle ændringer af [!INCLUDE [prod_short](includes/prod_short.md)], som den enkelte bruger har foretaget på forskellige sider i [!INCLUDE [prod_short](includes/prod_short.md)]. Efterhånden som brugerne foretager ændringer af deres oplevelse i [!INCLUDE [prod_short](includes/prod_short.md)], afspejles disse ændringer på listen **Brugertilpasninger**. <!--Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.-->

<!-- >[!NOTE]
> User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.-->

## Sådan gennemser eller sletter du brugertilpasninger

1. Vælg ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") ikon, skriv **Tilpassede sider**, og vælg derefter det relaterede link.
2. Dette viser listen over brugere og deres tilpassede sider. Hvis du vil rydde en brugers tilpassede indstillinger, skal du klikke på den relevante række eller vælge **Administrer** og derefter vælge **Slet**.

Derved slettes personlige indstillinger, og brugerens oplevelse af den relevante side vender tilbage til standardtilstanden.

## Se også

[Blive køreklar](ui-get-ready-business.md)  
[Tilgængelighed i land/område og understøttede sprog](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Ændre sprog og landestandard](about-locale-language.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
