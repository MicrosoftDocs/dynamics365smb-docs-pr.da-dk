---
title: "Spore brugeraktivitet i en ændringslog | Microsoft Docs"
Description: "Du kan aktivere en brugerlog for at få en oversigt over ændringer af data i registrerede tabeller."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c27c63ae26f2f97dd15d31978b967f6a08dd55b7
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="logging-changes-in-dynamics-365-for-financials"></a>Logføring af ændringer i Dynamics 365 for Financials
Du kan aktivere ændringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)], så du har en oversigt over aktiviteter. Loggen er baseret på ændringer, der foretages i data i de tabeller, du sporer. I ændringsloggen står posterne i kronologisk rækkefølge og viser de ændringer, der er foretaget i felterne på de angivne tabeller. Ændringsloggen indsamler alle ændringer, der foretages i tabellen.  

## <a name="working-with-the-change-log"></a>Arbejde med ændringsloggen
Et almindeligt problem i mange økonomisystemer er at finde årsagen til fejl og ændringer i data. Det kan være alt fra et forkert kundetelefonnummer til en forkert postering i regnskabet. Du kan bruge funktionaliteten i ændringsloggen til at spore alle direkte modifikationer, som en bruger foretager af data i databasen. Du skal for hver tabel og hvert felt angive, hvad der skal registreres i loggen. Derefter skal du aktivere ændringsloggen.  

Du aktiverer og deaktiverer ændringsloggen i vinduet **Opsætning af ændringslog**. Når du aktiverer eller deaktiverer ændringsloggen, logføres denne aktivitet, så du altid kan se, hvilken bruger der har deaktiveret eller aktiveret ændringsloggen. Denne funktion kan ikke deaktiveres.  

Hvis du i vinduet **Opsætning af ændringslog** vælger handlingen **Tabeller**, kan du angive, hvilke tabeller du vil spore ændringer for, og hvilke ændringer du vil spore. [!INCLUDE[d365fin](includes/d365fin_md.md)] registrerer også en række systemtabeller.

Når du har konfigureret ændringsloggen, aktiveret den og ændret data, kan du få vist og filtrere ændringerne i vinduet **Ændringslogposter**. Hvis du vil slette poster, kan du gøre det i vinduet **Slet ændringslogposter**, hvor du kan angive filtre baseret på datoer og tidspunkter.  

## <a name="see-also"></a>Se også
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
[Sortering](ui-sorting.md)  
[Brug af Søg efter side eller rapport](ui-search.md)  
[Fremgangsmåde: Administrere brugere og rettigheder](ui-how-users-permissions.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

