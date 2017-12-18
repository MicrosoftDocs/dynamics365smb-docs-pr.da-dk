---
title: "Tildele brugertilladelser og oprette eller redigere tilladelsessæt | Microsoft Docs"
description: "Beskriver, hvordan du kan føje Office 365-brugere til Dynamics 365 Business edition og derefter tildele tilladelser, adgangsrettigheder og sikkerhedsindstillinger."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: f1b43879d6dafd238b593c6d17d2322943d75a89
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-manage-users-and-permissions"></a>Fremgangsmåde: Administrere brugere og rettigheder
Når du vil tilføje brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal din virksomheds Office 365-administrator først oprette brugerne i Office 365 Administration. Du kan finde flere oplysninger under [Føje brugere til Office 365 til virksomheder](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)

Når brugerne er oprettet i Office 365, kan de importeres i vinduet **Brugere** ved hjælp af handlingen **Hent brugere fra Office 365**. Brugere tildeles rettighedssæt afhængigt af den plan, der er tildelt til Brugere i Office 365.

Du kan derefter fortsætte med at tildele rettighedssæt til brugerne for at definere, hvilke databaseobjekter, og dermed hvilke elementer i brugergrænsefladen, de skal have adgang til, og i hvilke virksomheder.

Et rettighedssæt er en samling tilladelser til bestemte objekter i databasen. Alle brugere skal være tildelt et eller flere rettighedssæt, før de kan få adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Der findes som standard et antal foruddefinerede rettighedssæt. Du kan bruge disse tilladelsessæt, som allerede er defineret, ændre standardtilladelsessættene eller oprette flere tilladelsessæt.

Du kan føje brugere til brugergrupper. Det gør det nemmere at tildele de samme rettighedssæt til flere brugere.

Administratorer kan bruge vinduet **Brugeropsætning** til at definere perioder, hvor angivne brugere kan bogføre, og de kan også angive, om systemet skal registrere, hvor lang tid brugerne er logget på.

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til Suite. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Sådan tildeles rettigheder til en bruger
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Vælg den bruger, du vil tildele rettigheden til.
Ethvert rettighedssæt, der allerede er tildelt brugeren, vises i faktaboksen **Rettighedssæt**.
3. Vælg handlingen **Rediger** for at åbne vinduet **Brugerkort**.
4. I oversigtspanelet **Brugerrettighedssæt** skal du udfylde felterne efter behov på en ny linje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Sådan grupperes brugere i brugergrupper
Du kan oprette brugergrupper, så du bedre kan administrere rettighedssæt for grupper af brugere i virksomheden. Du kan bruge en funktion til at kopiere alle rettighedssæt fra en eksisterende brugergruppe til den nye brugergruppe. Brugergruppemedlemmerne kopieres ikke.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Du kan også vælge handlingen **Brugergrupper** i vinduet **Brugere**.
3. I vinduet **Brugergrupper** skal du vælge en eksisterende gruppe, du vil kopiere, og derefter vælge handlingen **Kopiér brugergruppe**.
4. I feltet **Ny brugergruppekode** skal du angive navnet på den nye gruppe og derefter vælge knappen **OK**.

    I stedet for at kopiere kan du også vælge handlingen Ny for at oprette en ny linje til en tom brugergruppe, som du derefter udfylder manuelt.
5. Hvis du vil tilføje nye eller flere brugere, skal du vælge handlingen **Medlemmer af brugergruppe** i vinduet **Brugergruppe**.
6. I vinduet **Medlemmer af brugergruppe** skal du på en ny linje udfylde felterne efter behov ved at vælge mellem eksisterende brugere.
7. Hvis du vil tilføje nye eller flere rettighedssæt, skal du vælge handlingen **Rettighedssæt for brugergruppe** i vinduet **Brugergruppe**.
8. I vinduet **Rettighedssæt for brugergruppe** skal du på en ny linje udfylde felterne efter behov ved at vælge mellem eksisterende rettighedssæt.

## <a name="to-set-up-user-time-constraints"></a>Sådan opsættes tidsbegrænsninger for brugere
Administratorer kan definere perioder, hvor angivne brugere kan bogføre, og de kan også angive, om systemet skal registrere, hvor lang tid brugerne er logget på. Administratorer kan også knytte ansvarscentre til brugere. Du kan finde flere oplysninger i [Fremgangsmåde: Arbejde med ansvarscentre](inventory-responsibility-centers.md).

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourceopsætning**, og vælg derefter det relaterede link.
2. Når vinduet **Brugeropsætning** åbnes, skal du vælge handlingen **Ny**.
3. I feltet **Bruger-ID** skal du angive ID'et for en bruger, eller vælge feltet for at få vist alle aktuelle Windows-brugere i systemet.
4. Udfyld felterne efter behov.

## <a name="see-also"></a>Se også
[Blive klar til at handle](ui-get-ready-business.md)  
[Installation og administration i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](admin-setup-and-administration.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbejde med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  

