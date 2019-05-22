---
title: Administrere brugere og roller | Microsoft Docs
description: Lære at administrere brugere og rollecentre i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc52d943938616041881c55f70c510e4c63b5de6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245805"
---
# <a name="understanding-users-profiles-and-role-centers"></a>Forstå brugere, profiler og rollecentre

I [!INCLUDE[d365fin](includes/d365fin_md.md)] tilføjes brugerne af en administrator, der giver også brugerne adgang til de områder i [!INCLUDE[d365fin](includes/d365fin_md.md)], de skal bruge i deres arbejde.  

Adgangen til funktionen styres via *brugergrupper* og *profiler*. Som administrator, kan du tilføje og fjerne brugere som en del af dit [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnement, og du kan tildele brugertilladelser gennem brugergrupper.  

## <a name="adding-users"></a>Tilføje brugere

Når du vil tilføje brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)] online, skal din virksomheds Office 365-administrator først oprette brugerne i Office 365 Administration. Du kan finde flere oplysninger under [Føje brugere til Office 365 til virksomheder](https://aka.ms/CreateOffice365Users).

Administratoren kan derefter tildele tilladelser til hver bruger og grupper af brugere. Du kan finde flere oplysninger i [Administrere brugere og rettigheder](ui-how-users-permissions.md).  

De mest effektive rettigheder, en bruger kan have, er rettighedssættet SUPER. Hver virksomhed skal have mindst én bruger med dette rettighedssæt, men det er bedst at give hver bruger rettigheder, der passer til deres arbejdsbehov i [!INCLUDE[prodshort](includes/prodshort.md)] og ikke mere end det. Dette sikrer f.eks, at brugerne kun har adgang til data, der er relevante for deres arbejde.  

> [!TIP]
> Det anbefales at sikre, at Office 365-administratoren også har rettigheden SUPER indstillet i [!INCLUDE[prodshort](includes/prodshort.md)], fordi der letter mange administrative opgaver, herunder konfiguration af integration med andre programmer.

### <a name="users-of-on-premises-deployments"></a>Brugere af lokale installationer

Ved lokale installationer af [!INCLUDE[d365fin](includes/d365fin_md.md)] kan administratoren vælge mellem forskellige godkendelse af legitimationsoplysninger for brugere. Når du derefter opretter en bruger, angiver du forskellige oplysninger, afhængigt af den type legitimationsoplysninger, du bruger i den specifikke [!INCLUDE[server](includes/server.md)]-forekomst. Du kan finde flere oplysninger i [Godkendelse og typer af legitimationsoplysninger](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i sektionen Administration af udvikler- og ITPro-indholdet til [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profiler

Personer i virksomheden, der har adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)] tildeles alle en *profil*, som giver dem adgang til et *rollecenter*.

Profiler er samlinger af [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere, der deler det samme rollecenter. Et rollecenter er indgangspunktet og startsiden til [!INCLUDE[d365fin](includes/d365fin_md.md)], der giver dig hurtig adgang til dine vigtigste opgaver og viser forskellig indsigt og nøgletal (KPI'er) om dit arbejde.  

> [!NOTE]  
>  I den aktuelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] online kan du ikke tilføje, redigere eller slette profiler.  

### <a name="CreateProfile"></a>Oprette en profil

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Profilliste**, og vælg derefter det relaterede link.  

2.  På siden **Profilliste** skal du vælge handlingen **Ny** handling for at åbne siden **Nyt profilkort**.  

3.  I feltet **Profil-id** skal du angive et navn, der beskriver den tiltænkte rolle for brugerne.  

4.  Gå til feltet **Beskrivelse** , og angiv en beskrivelse af profil-id'et, f.eks. **Ordrebehandler**.  

5.  Angiv feltet **Rollecenter-id** for det rollecenter, der skal tildeles til profilen.  

Proceduren for ændring af en eksisterende profil er den samme, bortset fra at du kan vælge en eksisterende profil på siden **Profilliste** i stedet for at vælge handlingen **Ny**.  


### <a name="copy-a-profile"></a>Kopiere en profil
Kopiering af en profil kan spare tid, hvis du vil bruge samme indstillinger på en profil, og du kun vil ændre nogle få indstillinger.

1.  Åbn den profil, du vil kopiere, og vælg derefter handlingen **Kopier profil**.

2.  I feltet **Nyt profil-id** skal du indtaste et navn på den profil, du vil kopiere.

3.  Angiv feltet **Ny profils område** til et af følgende:

    - **System** for at gøre den nye profil tilgængelig for alle lejerdatabaser, der bruger programmet.
    - **Lejer** for at gøre den nye profil tilgængelig for kun den aktuelle lejerdatabase.
4. Tryk på knappen **OK**, når du er færdig.

### <a name="ExportImportProfile"></a>Eksportere og importere profiler

Du kan eksportere og importere profiler som XML-filer til og fra den en [!INCLUDE[d365fin](includes/d365fin_md.md)]-database. Eksport og import af en profil kan spare dig tid, når du konfigurerer brugergrænsefladen, fordi du kan genbruge en eksisterende profil i stedet at konfigurere en profil forfra. Hvis du har en profil, der er konfigureret i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-database, og du vil genbruge alle eller nogle af de samme profilkonfigurationer i en anden database, kan du eksportere profilen til en XML-fil. Du kan derefter importere XML-filen med profilen til anden databasen.

-   For at eksportere en profil kan du enten vælge handlingen **Udlæs profiler** fra siden **Profilliste** eller siden **Profilkort**, eller du kan søge efter og åbne siden **Udlæs profiler**. Gem XML-filen på en placering på computeren eller netværket.

-   For at importere en profil kan du enten vælge handlingen **Indlæs profiler** fra siden **Profilliste**, eller du kan søge efter og åbne siden **Indlæs profiler**. 

    > [!NOTE]  
    >  Du kan ikke importere en profil, der allerede findes i databasen, selvom XML-filen har et andet navn eller har et andet indhold. Før du kan importere den nye profil, skal du slette den eksisterende profil.


## <a name="configuration-and-personalization"></a>Konfiguration og brugertilpasning
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

Brugene tilpasser brugergrænsefladen i deres personlige version ved at tilpasse brugergrænsefladen under deres egne brugerlogon. Denne tilpasning kan slettes af administratoren. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).  

## <a name="see-also"></a>Se også  
[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)  
[Administrere tilpasning som administrator](ui-personalization-manage.md)  
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
