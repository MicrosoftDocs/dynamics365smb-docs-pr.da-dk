---
title: Styre tilpasningen som en administrator i Business Central | Microsoft Docs
description: Få at vide, hvordan du kan tilpasse brugergrænsefladen, så den passer til din måde at arbejde på.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 08/16/2019
ms.author: jswymer
ms.openlocfilehash: 268d61e05f84643abe8eeeb283bd035e0247fe1c
ms.sourcegitcommit: 81b6062194bf04d8052a3cd394cc0b41e3f53e6d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/20/2019
ms.locfileid: "1887733"
---
# <a name="managing-personalization-as-an-administrator"></a>Administrere tilpasning som administrator

Brugere kan tilpasse deres arbejdsområde, så det passer til deres egne præferencer. Som administrator kan du styre og administrere tilpasning ved at:

-   Aktivere eller deaktivere tilpasningsfunktionen for hele programmet (kun for lokal installation).
-   Aktivere eller deaktivere tilpasningsfunktionen for brugere med en bestemt profil.
-   Fjerne eventuelle sidetilpasninger, som brugere har foretaget.

## <a name="EnablePersonalization"></a>Sådan aktiveres eller deaktiveres tilpasning (kun lokalt)

Tilpasning er som standard ikke aktiveret på klienten. Du kan aktivere eller deaktivere tilpasning ved at ændre konfigurationsfilen (navsettings.json) på den Business Central Web Server-forekomst, der betjener klienterne.

1. Hvis du vil aktivere tilpasning, skal du tilføje følgende linje i filen navsettings.json:

    ```
    "PersonalizationEnabled": "true"
    ```

    Hvis du vil deaktivere tilpasning, skal du fjerne linjen eller ændre den til:

    ```
    "PersonalizationEnabled": "false"
    ```

    Du kan finde flere oplysninger om, hvordan du kan ændre filen navsettings.json, i [Redigere navsettings.json-filen direkte](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).

2. Oprette og hente programsymboler.

    Dette trin er valgfrit og er ikke påkrævet for at aktivere brugertilpasning. Men det sikrer, at nye sider, der er oprettet af udviklere, kan tilpasses.

    1. Først skal du oprette symbolerne ved at køre finsql.exe med kommandoen `generatesymbolreference`. Filen finsql.exe er placeret i installationsmappen til [!INCLUDE[server](includes/server.md)] og Dynamics NAV-udviklingsmiljøet (CSIDE). Opret symbolerne ved at åbne en kommandoprompt, skift til den mappe, hvor filen er gemt, og kør følgende kommando:

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    Eksempler:

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    Du kan finde flere oplysninger i [Kørsel af C/SIDE og AL Side om side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).

    2. Konfigurer [!INCLUDE[nav_server_md](includes/nav_server_md.md)]-forekomsten til **Aktivér indlæsning af programsymbolreferencer ved serverstart** (EnableSymbolLoadingAtServerStartup). Du kan finde flere oplysninger under [Konfiguration af Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).

## <a name="to-disable-personalization-for-a-profile"></a>Sådan deaktiveres tilpasning for en profil

Du kan forhindre alle brugere, der tilhører en bestemt profil, i at tilpasse deres sider.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Profiler**, og vælg derefter det relaterede link.
2. Vælg den profil på listen, der skal ændres.
3. Markér afkrydsningsfeltet **Deaktiver tilpasning**, og vælg derefter knappen **OK**.

> [!NOTE]  
> I Business Central online kan du kun deaktivere tilpasning for en lejerprofil, ikke for systemprofiler. 

## <a name="to-clear-user-personalizations"></a>Sådan fjernes brugertilpasninger

Når sidetilpasninger fjernes, går siden tilbage til det oprindelige layout, før der blev foretaget nogen tilpasning. Tilpasninger, som brugere har foretaget af sider, kan fjernes på to måder: ved brug af siden **Slet brugertilpasning** side og ved brug af siden **Brugertilpasningskort**.

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Sådan fjernes brugertilpasninger ved brug af siden Slet brugertilpasning

Siden **Slet brugertilpasning** giver dig mulighed for at slette tilpasning på sidebasis for hver enkelt bruger.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet brugertilpasning**, og vælg derefter det relaterede link.

    Siden viser alle de sider, der er blevet tilpasset, og den bruger, de tilhører.

    >[!NOTE]
    > En markering i kolonnerne **Ældre tilpasning** angiver, at tilpasningen blev udført i en ældre version af [!INCLUDE[d365fin](includes/d365fin_md.md)], som håndterede tilpasning anderledes end nu. Brugere, som forsøger at tilpasse siderne, er blokeret fra at gøre det, medmindre de vælger at låse siden op. Du kan finde flere oplysninger i [Derfor er en side spærret for tilpasning](ui-personalization-locked.md).

2. Marker den post, du vil slette, og vælg derefter handlingen **Slet**.

    Brugerne vil se ændringerne, næste gang de logger på.

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Sådan fjernes brugertilpasninger ved brug af siden Brugertilpasningskort

Siden **Brugertilpasningskort** giver dig mulighed for at slette tilpasningen på alle sider for en specifik bruger. Det kræver skrivetilladelse til tabel 2000000072 **Profil**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugertilpasning**, og vælg derefter det relaterede link.

    Siden **Brugertilpasning** viser alle brugere, der muligvis kan have personlige sider. Hvis du ikke kan finde en bruger på listen, betyder det, at vedkommende ikke har nogen tilpassede sider.

2. Vælg brugeren på listen, og vælg derefter handlingen **Rediger**.

3. Under fanen **Handlinger** skal du vælge **Fjern tilpassede sider**.

    Brugerne vil se ændringerne, næste gang de logger på.

## <a name="see-also"></a>Se også
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
