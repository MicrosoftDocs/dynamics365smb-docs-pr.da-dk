---
title: Administrere brugere og roller | Microsoft Docs
description: Lære at administrere brugere og rollecentre i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ca0ca5f756d0d7423c92ca25034038fa1fb05727
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4745979"
---
# <a name="manage-profiles"></a>Administrere profiler

Alle brugere af [!INCLUDE[prod_short](includes/prod_short.md)] tildeles en profil, der afspejler deres forretningsrolle, den afdeling, de arbejder i, eller en anden kategorisering. Med profilerne kan administratorer definere og styre centralt, hvad forskellige brugertyper der kan se og foretage sig i brugergrænsefladen, så de kan udføre deres forretningsopgaver på en effektiv måde.

> [!NOTE]
> Den typiske forretningsbrug af en profil er en rolle. En profil har derfor navnet *Profil (rolle)* i brugergrænsefladen.

Som administrator kan du oprette og administrere profiler på siden **Profiler (roller)**. Hver profil har et kort, hvor du kan administrere forskellige indstillinger for den relaterede rolle, f.eks. rollenavnet, brugerindstillingerne, og hvilket rollecenter profilen bruger. Du kan finde flere oplysninger om brugerindstillinger og rollecentre i [Ændre grundlæggende indstillinger](ui-change-basic-settings.md).

Når du vil administrere brugerprofiler, skal de pågældende brugere først være oprettet og tilføjet via Microsoft 365 Administration. Du kan derefter tildele rettigheder til hver bruger eller brugergruppe for at definere, hvilke funktioner de har tilladelse til at få vist og/eller redigere. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).

## <a name="page-customization"></a>Sidetilpasning
Du kan tilpasse sidelayout for en profil, så alle brugere, som profilen er tildelt til, kan se de tilpassede sider. Som administrator kan du tilpasse sider ved at bruge de samme funktioner som brugerne, når de foretager tilpasning. Du kan finde flere oplysninger under [Tilpasse sider til profiler](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Sådan oprettes en profil
Hvis du ikke kan kopiere en eksisterende profil, kan du oprette en ny profil manuelt.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Profiler (roller)**, og vælg derefter det relaterede link.  
2. På siden **Profiler (roller)** skal du vælge handlingen **Ny**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-a-profile"></a>Sådan kopieres en profil
Du kan spare tid, når du vil oprette en ny profil, ved at kopiere en eksisterende profil. Kopiér en profil med indstillinger, der svarer nogenlunde til den profil, du vil oprette.

> [!NOTE]
> Når du kopierer en profil, kopieres alle de involverede sidetilpasninger også, både brugeroprettede og dem, der er afledt af udvidelser.

1. På siden **Profiler (roller)** skal du vælge linjen for den profil, du vil kopiere, og derefter vælge handlingen **Kopiér profil**.
2. Udfyld felterne **Profil-id** og **Visningsnavn**, og klik derefter på knappen **OK**.
3. Åbn det netop oprettede profilkort på siden **Profiler (roller)**, og rediger evt. andre felter efter behov.

## <a name="to-edit-a-profile"></a>Sådan redigeres en profil
Du kan redigere en profil ved at ændre felterne på siden **Profil (rolle)**. Men ændringerne vil ikke være synlige for den bruger, der har fået tildelt profilen, før vedkommende logger af og på igen.

> [!Caution]
> Du må ikke omdøbe en profil, mens brugere, der har fået tildelt profilen, er logget på, da brugerne kan opleve, at produktet er fastfryses og skal genstartes.

## <a name="to-assign-a-profile-to-a-user"></a>Sådan tildeles en profil til en bruger
Brugerne kan tildele sig selv en rolle (der repræsenterer en profil) ved at vælge feltet **Rolle** på siden **Mine indstillinger**. Som administrator kan du gøre det samme via siden **Profiler (roller)**.

1. På siden **Profiler (roller)** skal du vælge den profil, som du vil tildele, og derefter vælge handlingen **Brugertilpasningsliste**.
2. På siden **Brugertilpasninger** skal du vælge den bruger, som du vil tildele profilen til, og derefter vælge handlingen **Rediger**.
3. Vælg den relevante profil i feltet **Profil-id**.

> [!NOTE]
> Hvis du tildeler en anden profil til en bruger, bevares tilpasninger, der er foretaget af brugeren med den forrige profil.

## <a name="to-define-user-settings-for-a-profile"></a>Sådan defineres brugerindstillinger for en profil
På siden **Mine indstillinger** kan brugere definere grundlæggende funktioner for deres konto, f.eks. rollecenter, sprog, og hvilke notifikationer de vil modtage. Du kan finde flere oplysninger under [Ændre grundlæggende indstillinger](ui-change-basic-settings.md).

Som administrator kan du definere disse indstillinger for en profil og dermed anvende indstillingerne for alle brugere af den relaterede rolle.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Profiler (roller)**, og vælg derefter det relaterede link.
2. Marker linjen for den profil, du vil ændre brugerindstillingerne for, vælg handlingen **Brugertilpasninger**.
3. På siden **Brugertilpasninger** skal du åbne kortet for den bruger, hvis indstillinger du vil ændre.
4. På siden **Brugertilpasningskort** kan du redigere felterne efter behov.

## <a name="to-activate-a-profile"></a>Sådan aktiveres en profil
Når der oprettes en profil, kan du markere forskellige afkrydsningsfelter, der angiver, hvor og hvordan profilen og dens oplysninger skal gøres tilgængelige for brugerne.

* Markér følgende afkrydsningsfelter på siden **Profil (rolle)**:
    - **Aktiveret** for at angive, om den relaterede rolle er synlig, så brugerne kan vælge den, på siden **Tilgængelige roller**.  
    - **Brug som standardprofil** for at angive den profil, der gælder for brugere, som ikke er tildelt en bestemt rolle.
    - **Deaktiver tilpasning** for at angive, om brugere af den relaterede rolle kan tilpasse deres arbejdsområde.
    - **Vis i Rollestifinder** for at angive, om handlinger til forretningsfunktioner, der er medtaget i profilen, skal vises i den udvidede visning af rolle Stifinder, en funktionsoversigt. Du kan finde flere oplysninger i [Søge efter sider med Rollestifinder](ui-role-explorer.md).

## <a name="to-export-profiles"></a>Sådan eksporterer du profiler
Du kan eksportere profiler fra [!INCLUDE[prod_short](includes/prod_short.md)], hvis de for eksempel skal genbruges i en anden lejer. Profilerne eksporteres til en zip-fil, som indeholder .al-filer, der kan genbruges til udvikling af udvidelser. Du kan finde flere oplysninger i [Bruge klienten til at oprette profiler og sidetilpasninger](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* På siden **Profiler (roller)** skal du vælge handlingen **Eksporter profiler**.

En zip-fil med. al-filerne til alle profiler eksporteres.

## <a name="to-import-profiles"></a>Sådan importerer du profiler
Du kan importere profiler, der er blevet eksporteret fra [!INCLUDE[prod_short](includes/prod_short.md)]. Trinnene er mere eller mindre de modsatte af trinene til eksport af profiler. Få flere oplysninger i [Sådan eksporter du profiler](admin-users-profiles-roles.md#to-export-profiles).

1. På siden **Profiler (roller)** skal du vælge handlingen **Importer profiler**.
2. Følg trinene i vejledningen **Importer profiler**.

    Hvis du kun vil importere markerede profiler, skal du bruge feltet **Valgt** til at angive, hvilken der skal importeres.
3. Tryk på knappen **Importer valgt**.

En zip-fil med. al-filerne til de valgte profiler importeres.

## <a name="to-delete-a-profile"></a>Sådan slettes en profil
Du kan slette en profil ved at vælge handlingen **Slet** på siden **Profiler (roller)**. Der gælder dog følgende begrænsninger:

- Du kan ikke slette en profil, der er tildelt til en bruger eller brugergruppe.
- Du kan ikke slette profiler, der stammer fra udvidelser. Udvidelsen skal først fjernes.
- Du kan kun slette én profil ad gangen.

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Sådan slettes alle tilpasninger, der er foretaget af en bruger
Du kan slette alle de ændringer, som en bruger har foretaget på sider, der udgør deres arbejdsområde. Det kan f.eks. være nyttigt, hvis en medarbejder har skiftet rolle og ikke længere har brug for personlige indstillinger. Sletning af brugeres tilpasninger ændrer sidelayoutet tilbage til det, der er defineret af profilen.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugertilpasninger**, og vælg derefter det relaterede link.

    Siden **Brugertilpasninger** viser alle brugere, der har foretaget tilpasninger.

2. Åbn kortet for den bruger, hvis tilpasninger du vil slette.
3. På siden **Brugertilpasningskort** skal du vælge handlingen **Fjern tilpassede sider** og derefter acceptere den meddelelse, der vises.

Brugerne ser ændringerne, næste gang de logger på.

Du kan også slette alle sidetilpasninger for en profil. Du kan finde flere oplysninger i [Sådan slettes alle tilpasninger af en profil](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Sådan slettes tilpasninger for bestemte sider
Du kan slette tilpasninger, som en eller flere brugere har foretaget på bestemte sider, som udgør deres arbejdsområde. Det kan f.eks. være nyttigt, hvis en ændret forretningsproces betyder, at en bruger ikke længere må bruge tilpasningen. Sletning af brugeres tilpasninger ændrer sidelayoutet tilbage til det, der er defineret af profilen.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Tilpasning af brugersider**, og vælg derefter det relaterede link.

    Siden **Tilpasning af brugersider** viser alle de sider, der er blevet tilpasset, og den bruger, de tilhører.

    > [!Note]
    > En markering i feltet **Ældre tilpasning** angiver, at tilpasningen blev udført i en ældre version af [!INCLUDE[prod_short](includes/prod_short.md)], som håndterede tilpasning anderledes. Brugere, som forsøger at tilpasse siderne, er blokeret fra at gøre det, medmindre de vælger at låse siden op. Du kan finde flere oplysninger i [Hvorfor er en side låst mod tilpasning](ui-personalization-locked.md).

2. Marker linjen for den sidetilpasning, du vil slette, og vælg derefter handlingen **Slet**.

Brugerne vil se ændringerne, næste gang de logger på.  

Du kan også slette enkelte sidetilpasninger for en profil. Du kan finde flere oplysninger i [Sådan slettes tilpasning for bestemte sider for en profil](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions"></a>Administrere brugersessioner

Som administrator af [!INCLUDE[prod_short](includes/prod_short.md)] online kan du administrere brugersessioner i administrationen. Du kan finde flere oplysninger i [Administrere sessioner](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions) i administrationsindholdet.  

Til [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø kan du f.eks. administrere sessioner ved hjælp af SQL Server Management Studio. Du kan finde flere oplysninger i den [tekniske dokumentation til SQL Server](/sql/sql-server).  

## <a name="see-also"></a>Se også  
[Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md)  
[Tilpasse sider til profiler](ui-personalization-manage.md)  
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]