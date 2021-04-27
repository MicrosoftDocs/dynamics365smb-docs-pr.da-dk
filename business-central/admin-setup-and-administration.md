---
title: Administrative opgaver i Business Central | Microsoft Docs
description: Nogle af opgaverne i Business Central kræver central administration og installation. Se, hvilke opgaver det er, og få at vide, hvad du skal gøre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 13f713756fc1f771243686c549c22f3ce0974b6b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777212"
---
# <a name="administration"></a>Opsætning

Centrale administrationsopgaver udføres som regel af én rolle i firmaet. Omfanget af disse opgaver kan afhænge af firmaets størrelse og administratorens jobansvar. Disse opgaver kan omfatte styring af databasesynkronisering af job og e-mail-køer, oprettelse af brugere og tilpasning af brugergrænsefladen.  

Det er vigtigt, at der indtastes korrekte opsætningsværdier fra starten, for at ny forretningssoftware kan fungere effektivt. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en række opsætningsvejledninger, som hjælper dig med opsætningen af basisoplysninger. Du kan finde flere oplysninger i [Konfigurere Business Central](setup.md).

Uanset om du bruger RapidStart Services til at implementere opsætningsværdier, eller du angiver dem manuelt i den nye virksomhed, kan du basere dine opsætningsbeslutninger på generelle anbefalinger for udvalgte opsætningsfelter, der erfaringsmæssigt kan gøre løsningen ineffektiv, hvis de defineres forkert.  

Superbruger eller administrator kan konfigurere Data Exchange Framework så brugere kan eksportere og importere data i bank og løn filer, f.eks. til forskellige likviditetsstyringsprocesser. Du kan finde flere oplysninger i [Udveksle data elektronisk](across-data-exchange.md).

> [!NOTE]
> Du kan oprette en ny virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)] med RapidStart Services, som er et værktøj, der er udviklet til at afkorte installationstiden, forbedre implementeringens kvalitet, introducere en tilgang til implementeringer, der kan gentages, og forbedre produktiviteten ved at automatisere og forenkle tilbagevendende opgaver. Du kan finde flere oplysninger i [Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Angiv, hvem der kan logge på [!INCLUDE[prod_short](includes/prod_short.md)], ved at oprette brugere i Microsoft 365 Administration i henhold til produktlicenserne.|[Oprette brugere i henhold til licenser](ui-how-users-permissions.md)|
|Tildele tilladelser til brugere, ændre tilladelsessæt og gruppere brugere for at opnå nem styring af tilladelser.|[Tildele tilladelser til brugere og grupper](ui-how-users-permissions.md)|
|Tilføj brugere, administrer tilladelser og få adgang til data og tildel roller.|[Administrere profiler](admin-users-profiles-roles.md)|
|Administrere brugerindstillinger, f.eks. virksomhed, rolle, sprog, område og tidszone.|[Brugerindstillinger](admin-manage-user-settings-preferences.md)|
|Opsættelse af printere og angivelse af, hvilke rapporter der skal udskrives på hvilke printere.|[Installation af printere](ui-specify-printer-selection-reports.md)|
|Klassificere datafølsomheder for felter så du kan svare på anmodninger fra dataemner vedrørende deres personlige oplysninger.|[Klassificere datafølsomhed](admin-classifying-data-sensitivity.md)|
|Svare på anmodninger fra dataemner vedrørende deres personlige oplysninger.|[Svare på anmodninger om personlige oplysninger](admin-responding-to-requests-about-personal-data.md)|
|Oprette en ny koncernvirksomhed ved hjælp af skabeloner|[Oprettelse af nye virksomheder](about-new-company.md)|
|Spore alle de direkte modifikationer, som brugere foretager af data i databasen for at identificere oprindelsen til fejl og dataændringer.|[Logføre ændringer](across-log-changes.md)|  
|Angive engangsanmodninger eller gentagne anmodninger om at køre rapporter eller kodeenheder.|[Brug af opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md)|  
|Administrere, slette eller komprimere dokumenter|[Slette dokumenter](admin-manage-documents.md)|  
|Vis sider, kodeenheder og forespørgsler som webtjenester.|[Udgive en webtjeneste](across-how-publish-web-service.md)|
|Som en del af oprettelsen af Connect Apps mellem [!INCLUDE[prod_short](includes/prod_short.md)] og tredjepartsløsninger via REST API'erne skal du definere skabeloner, der bruges til at udfylde tomme egenskaber for en enhed, når du opretter en BOGF-handling via et API.|[Konfiguration af API-skabeloner](admin-configuring-api-template.md)|
|Krypter data på [!INCLUDE[prod_short](includes/prod_short.md)] Server ved at oprette nye eller importere eksisterende krypteringsnøgler, som du aktiverer på serveren.|[Administration af datakryptering](admin-manage-data-encryption.md)|
|Opret forbindelse fra Dynamics 365 Sales til [!INCLUDE[prod_short](includes/prod_short.md)] for at opnå problemfri integration mellem debitorrelationer og ordrebehandling i lead-til-kontant-processen.|[Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Ændre, hvilke felter og handlinger der vises i brugergrænsefladen, så det passer til virksomhedens forretningsprocesser, og så løsningen kan udvides med apps.|[Tilpasning [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|
|Overvåge brug og foretage fejlfinding af sessioner.|[Miljøtelemetri i Business Central Administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Administrere brugersessioner, herunder annullering af en session, hvis brugeren er spærret.|[Administration af sessioner](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions)|  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Forretningsfunktioner](across-business-functionality.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Blive køreklar](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]