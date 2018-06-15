---
title: Tildele eller redigere brugertilladelser | Microsoft Docs
description: "Beskriver, hvordan du kan føje Office 365-brugere til Business Central og derefter tildele tilladelser, adgangsrettigheder og sikkerhedsindstillinger."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 05/24/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: 443c04799e9aa2b9aa4ede15006ecb5e9773ce6b
ms.contentlocale: da-dk
ms.lasthandoff: 05/28/2018

---
# <a name="manage-users-and-permissions"></a>Administrere brugere og deres rettigheder
Når du vil tilføje brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal din virksomheds Office 365-administrator først oprette brugerne i Office 365 Administration. Du kan finde flere oplysninger under [Føje brugere til Office 365 til virksomheder](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)

Når brugerne er oprettet i Office 365, kan de importeres i vinduet **Brugere** ved hjælp af handlingen **Hent brugere fra Office 365**. Brugere tildeles rettighedssæt afhængigt af den plan, der er tildelt til brugeren i Office 365.

Du kan derefter fortsætte med at tildele rettighedssæt til brugerne for at definere, hvilke databaseobjekter, og dermed hvilke elementer i brugergrænsefladen, de skal have adgang til, og i hvilke virksomheder. Du kan føje brugere til brugergrupper. Det gør det nemmere at tildele de samme rettighedssæt til flere brugere.

Et rettighedssæt er en samling tilladelser til bestemte objekter i databasen. Alle brugere skal være tildelt et eller flere rettighedssæt, før de kan få adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Der findes som standard et antal foruddefinerede rettighedssæt.  

Administratorer kan bruge vinduet **Brugeropsætning** til at definere perioder, hvor angivne brugere kan bogføre, og de kan også angive, om systemet skal registrere, hvor lang tid brugerne er logget på.

En anden metode, der definerer, hvad brugerne har adgang til, er indstillingen Oplevelse. Du kan finde flere oplysninger i [Ændre, hvilke funktioner der vises](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Sådan tildeles rettigheder til en bruger
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Vælg den bruger, du vil tildele rettigheden til.
Ethvert rettighedssæt, der allerede er tildelt brugeren, vises i faktaboksen **Rettighedssæt**.
3. Vælg handlingen **Rediger** for at åbne vinduet **Brugerkort**.
4. I oversigtspanelet **Brugerrettighedssæt** skal du udfylde felterne efter behov på en ny linje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Sådan grupperes brugere i brugergrupper
Du kan oprette brugergrupper, så du bedre kan administrere rettighedssæt for grupper af brugere i virksomheden.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Du kan også vælge handlingen **Brugergrupper** i vinduet **Brugere**.
3. Du kan også vælge handlingen **Medlemmer af brugergruppe** i vinduet **Brugergruppe**.
6. Vælg handlingen **Tilføj brugere** i vinduet **Medlemmer af brugergruppe**.
7. Hvis du vil tilføje nye eller flere rettighedssæt, skal du vælge handlingen **Rettighedssæt for brugergruppe** i vinduet **Brugergrupper**.
8. I vinduet **Rettighedssæt for brugergruppe** skal du på en ny linje udfylde felterne efter behov ved at vælge mellem eksisterende rettighedssæt.

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Sådan kopierer du en brugergruppe og alle dens rettighedssæt
Hvis du hurtigt vil definere en ny brugergruppe, kan du kopiere alle rettighedssæt fra en eksisterende brugergruppe til den nye brugergruppe.

Brugergruppemedlemmerne kopieres ikke til den nye brugergruppe. Du skal tilføje dem bagefter.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Vælg de brugergrupper, som du vil kopiere, og vælg derefter handlingen **Kopiér brugergruppe**.
3. I feltet **Ny brugergruppekode** skal du angive et navn til gruppen og derefter vælge knappen **OK**.

Den nye gruppe tilføjes i vinduet **Brugergrupper**. Fortsæt for at tilføje brugere. Yderligere oplysninger finder du i afsnittet "Sådan grupperes brugere i brugergrupper".

## <a name="to-set-up-user-time-constraints"></a>Sådan opsættes tidsbegrænsninger for brugere
Administratorer kan definere perioder, hvor angivne brugere kan bogføre, og de kan også angive, om systemet skal registrere, hvor lang tid brugerne er logget på. Administratorer kan også knytte ansvarscentre til brugere. Du kan finde flere oplysninger i [Arbejde med ansvarscentre](inventory-responsibility-centers.md).

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourceopsætning**, og vælg derefter det relaterede link.
2. Når vinduet **Brugeropsætning** åbnes, skal du vælge handlingen **Ny**.
3. I feltet **Bruger-ID** skal du angive ID'et for en bruger, eller vælge feltet for at få vist alle aktuelle Windows-brugere i systemet.
4. Udfyld felterne efter behov.

## <a name="see-also"></a>Se også
[Blive klar til at handle](ui-get-ready-business.md)  
[Opsætning](admin-setup-and-administration.md)  
[Introduktion](product-get-started.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

