---
title: Styre tilpasningen som en Administrator i Financials | Microsoft Docs
description: "Få at vide, hvordan du kan tilpasse brugergrænsefladen, så den passer til din måde at arbejde på."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 854dddab2d958e128309aa201b53234d87d2c049
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="managing-personalization-as-an-administrator"></a>Administrere tilpasning som administrator
<!--NAV in the Web client-->
Brugere kan tilpasse deres arbejdsområde, så det passer til deres egne præferencer. Som administrator kan du kan styre og administrere tilpasning ved at deaktivere brugernes mulighed for at tilpasse sider og ved at fjerne alle sidetilpasninger, som brugere har foretaget.

## <a name="disable-personalization-for-a-profile"></a>Deaktivere tilpasning for en profil
Du kan forhindre alle brugere, der tilhører en bestemt profil, i at tilpasse deres sider.
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Profiler**, og vælg derefter det relaterede link.
2.  Vælg den profil på listen, der skal ændres.
3. Markér afkrydsningsfeltet **Deaktiver tilpasning**, og vælg derefter knappen **OK**.

## <a name="clear-user-personalizations"></a>Fjern brugertilpasninger

Når sidetilpasninger fjernes, går siden tilbage til det oprindelige layout, før der blev foretaget nogen tilpasning. Tilpasninger, som brugere har foretaget af sider, kan fjernes på to måder: ved brug af siden **Slet brugertilpasning** side og ved brug af siden **Brugertilpasningskort**.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Slette brugertilpasninger ved brug af siden Slet brugertilpasning

Siden **Slet brugertilpasning** giver dig mulighed for at slette tilpasning på sidebasis for hver enkelt bruger.

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Slet brugertilpasning**, og vælg derefter det relaterede link.

    Siden viser alle de sider, der er blevet tilpasset, og den bruger, de tilhører.

    >[!NOTE]
    > En markering i kolonnerne **Ældre tilpasning** angiver, at tilpasningen blev udført i en ældre version af [!INCLUDE[d365fin](includes/d365fin_md.md)], som håndterede tilpasning anderledes end nu. Brugere, som forsøger at tilpasse siderne, er blokeret fra at gøre det, medmindre de vælger at låse siden op. Du kan finde flere oplysninger i [Derfor er en side spærret for tilpasning](ui-personalization-locked.md).

2. Marker den post, du vil slette, og vælg derefter handlingen **Slet**.

    Brugerne vil se ændringerne, næste gang de logger på.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Slette brugertilpasninger ved brug af siden Brugertilpasningskort

Siden **Brugertilpasningskort** giver dig mulighed for at slette tilpasningen på alle sider for en specifik bruger. Det kræver skrivetilladelse til tabel 2000000072 **Profil**.

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugertilpasning**, og vælg derefter det relaterede link.

    Siden **Brugertilpasning** viser alle brugere, der muligvis kan have personlige sider. Hvis du ikke kan finde en bruger på listen, betyder det, at vedkommende ikke har nogen tilpassede sider.

2. Vælg brugeren på listen, og vælg derefter handlingen **Rediger**.

3.  Under fanen **Handlinger** skal du vælge **Fjern tilpassede sider**.

    Brugerne vil se ændringerne, næste gang de logger på.

## <a name="see-also"></a>Se også
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
[Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md)  

