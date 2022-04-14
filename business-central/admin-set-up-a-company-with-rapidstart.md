---
title: Konfigurere en virksomhed med RapidStart Services
description: Du kan oprette en ny virksomhed i Business Central med RapidStart Services for at forbedre produktiviteten ved at automatisere og forenkle tilbagevendende opgaver.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 8610, 8614, 8615, 8620, 8632
ms.date: 03/28/2022
ms.author: edupont
ms.openlocfilehash: b2d3378e9c06221bc91977883a53bba8514c6afc
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518307"
---
# <a name="set-up-a-company-with-rapidstart-services"></a>Konfigurere en virksomhed med RapidStart Services

Du kan oprette en ny virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)] med RapidStart Services, som er et værktøj, der er udviklet til at afkorte installationstiden, forbedre implementeringens kvalitet, introducere en tilgang til implementeringer, der kan gentages, og forbedre produktiviteten ved at automatisere og forenkle tilbagevendende opgaver.  

Du kan bruge disse funktioner til at skalere din virksomhed som forhandler. De fleste af de relevante sider gælder både [!INCLUDE [prod_short](includes/prod_short.md)] online og lokalt. Nogle processer er imidlertid afhængige af adgang til filer på disken og er for komplekse til at kunne bruges i [!INCLUDE [prod_short](includes/prod_short.md)] onlinetilstand. Til [!INCLUDE [prod_short](includes/prod_short.md)] på stedet vil du sikkert gerne bruge Windows PowerShell til at hjælpe dig med at installere. Du kan finde flere oplysninger i [Administration af Business Central på stedet](/dynamics365/business-central/dev-itpro/administration/administration) og [Administration af Business Central online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).  

RapidStart Services hjælper med at få et overblik over konfigurationen af din nye virksomhed ved hjælp af et regneark, hvor du kan konfigurere de tabeller, der ofte er involveret i konfigurationsprocessen for nye virksomheder. Når du gør dette, kan du oprette et spørgeskema til at hjælpe dine kunder gennem indsamlingen af konfigurationsoplysninger. Dine kunder har mulighed for at bruge spørgeskemaet til at konfigurere programområder, eller de kan åbne konfigurationssiden direkte og foretage konfigurationen der. Det vigtigste er, at RapidStart Services hjælper dig som debitor med at forberede virksomheden med standardopsætningsdata, som du kan finjustere og tilpasse. Endelig kan du, når du bruger RapidStart Services, konfigurere og overflytte eksisterende debitordata, f.eks. en liste over kunder eller varer, til den nye virksomhed.

Du kan bruge følgende komponenter til at sætte skub i opsætningen af din virksomhed:  

- Guiden Konfiguration  
- Konfigurationsregneark  
- Konfigurationspakker  
- Konfigurationsskabeloner  
- Konfigurationsspørgeskema  

> [!Note]  
> Der er områder af [!INCLUDE[prod_short](includes/prod_short.md)], som du skal konfigurere manuelt. Disse omfatter tilføjelse af brugere, konfiguration af regnskabsperioder og konfiguration af dimensioner for business intelligence. Du kan finde flere oplysninger i [Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Oprette en ny virksomhed og importere grundlæggende opsætningsdata og skabeloner.|[Konfigurere virksomhedskonfiguration](admin-set-up-company-configuration.md)|  
|Installér den konfigurerede pakke hos din kunde til implementering.|[Anvende konfigurationer på nye virksomheder](admin-apply-configuration-to-new-companies.md)|
|Definer og valider kundens opsætningsværdier for alle centrale områder, f.eks. firmaoplysninger, finans, lager, salg eller produktion.|[Indsaml debitoropsætningsværdier](admin-gather-customer-setup-values.md)|  
|Konfigurer kerneposter i masterdata ved brug af skabeloner for at forberede overflytning af eksisterende debitordata.|[Forberede overflytning af debitordata](admin-use-templates-to-prepare-customer-data-for-migration.md)|  
|Definere tabeller og felter, validere eksisterende debitordata og overflytte data til databasen i [!INCLUDE[prod_short](includes/prod_short.md)].|[Overflytte debitordata](admin-migrate-customer-data.md)|
|Forbered genbrug af virksomhedens konfigurationer i andre virksomheder (i indholdet til udviklere og administration).|[Oprette brugerdefinerede virksomhedsskabeloner](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)|
|Finde løsninger på kendte problemer i værktøjssættet i RapidStart Services.|[Tip: RapidStart Services](admin-tips-and-tricks-rapidstart-services.md)|  

## <a name="see-also"></a>Se også

[Opsætning](admin-setup-and-administration.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Opret komplekse moduler ved hjælp af bedste praksis](set-up-complex-application-areas-using-best-practices.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]