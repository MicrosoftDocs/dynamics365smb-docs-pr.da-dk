---
title: Administrative opgaver i Business Central | Microsoft Docs
description: "Nogle af opgaverne i Business Central kræver central administration og installation. Se, hvilke opgaver det er, og få at vide, hvad du skal gøre."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/08/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 46a37fb00319647ea1c4b4630e4d9369687dd7cf
ms.openlocfilehash: 26057b4838681b4b6036c4a56aab4fd6d49ac1dd
ms.contentlocale: da-dk
ms.lasthandoff: 11/12/2018

---
# <a name="administration"></a>Opsætning
Centrale administrationsopgaver udføres som regel af én rolle i firmaet. Omfanget af disse opgaver kan afhænge af firmaets størrelse og administratorens jobansvar. Disse opgaver kan omfatte styring af databasesynkronisering af job og e-mail-køer, oprettelse af brugere og tilpasning af brugergrænsefladen.  

Det er vigtigt, at der indtastes korrekte opsætningsværdier fra starten, for at ny forretningssoftware kan fungere effektivt. [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en række opsætningsvejledninger, som hjælper dig med opsætningen af basisoplysninger. Du kan finde flere oplysninger under [Konfigurere Business Central](setup.md).

Uanset du bruger RapidStart Services til at implementere opsætningsværdier, eller du angiver dem manuelt i den nye virksomhed, kan du basere dine opsætningsbeslutninger på generelle anbefalinger for udvalgte opsætningsfelter, der erfaringsmæssigt kan gøre løsningen ineffektiv, hvis de konfigureres forkert.  

Superbruger eller administrator kan konfigurere Data Exchange Framework så brugere kan eksportere og importere data i bank og løn filer, f.eks. til forskellige likviditetsstyringsprocesser.

> [!NOTE]
> Du kan oprette en ny virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)] med RapidStart Services, der er et værktøj, der er udviklet til at afkorte installationstiden, forbedre implementeringens kvalitet, introducere en tilgang til implementeringer, der kan gentages, og forbedre produktiviteten ved at automatisere og forenkle tilbagevendende opgaver. Du kan finde flere oplysninger i [Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Tilføj brugere, administrer tilladelser og få adgang til data og tildel roller.|[Forstå profiler og rollecentre](admin-users-profiles-roles.md)|  
|Tildele tilladelser til brugere, ændre tilladelsessæt og gruppere brugere pr. tilladelser.|[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)|
|Klassificere datafølsomheder for felter så du kan svare på anmodninger fra dataemner vedrørende deres personlige oplysninger.|[Klassificere datafølsomhed](admin-classifying-data-sensitivity.md)|
|Svare på anmodninger fra dataemner vedrørende deres personlige oplysninger.|[Svare på anmodninger om personlige oplysninger](admin-responding-to-requests-about-personal-data.md)|
|Oprette en ny koncernvirksomhed ved hjælp af skabeloner|[Oprettelse af nye virksomheder](about-new-company.md)|
|Ændre, hvilke felter og handlinger der vises i brugergrænsefladen, så det passer til virksomhedens forretningsprocesser. |[Tilpasning [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md) |
|Spore alle de direkte modifikationer, som brugere foretager af data i databasen for at identificere oprindelsen til fejl og dataændringer.|[Logføre ændringer](across-log-changes.md)|  
|Angive engangsanmodninger eller gentagne anmodninger om at køre rapporter eller kodeenheder.|[Brug af opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md)|  
|Administrere, slette eller komprimere dokumenter|[Slette dokumenter](admin-manage-documents.md)|  
|Vis sider, kodeenheder og forespørgsler som webtjenester.|[Udgive en webtjeneste](across-how-publish-web-service.md)|
|Som en del af oprettelsen af Connect-apps mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og tredjepartsløsninger via REST API'erne skal du definere skabeloner, der bruges til at udfylde tomme egenskaber for en enhed, når du opretter en BOGF-handling via et API.|[Konfiguration af API-skabeloner](admin-configuring-api-template.md)|
|Krypter data på [!INCLUDE[d365fin](includes/d365fin_md.md)] Server ved at oprette nye eller importere eksisterende krypteringsnøgler, som du aktiverer på serveren.|[Administration af datakryptering](admin-manage-data-encryption.md)|

## <a name="see-also"></a>Se også
[Forretningsfunktioner](across-business-functionality.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Introduktion](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

