---
title: Integration med Dynamics 365 for Sales| Microsoft Docs
description: Få at vide, hvordan du får Dynamics 365 Business Central klar til at integrere med Dynamics 365 for Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 991d8432c24b1963da019e3c8b665f9ad009d077
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247276"
---
# <a name="integrating-with-dynamics-365-for-sales"></a>Integration med Dynamics 365 for Sales
Rollen Sælger betragtes ofte som et af de mest udadvendte i en virksomhed. Det kan imidlertid være en fordel for sælgere at kunne se indad i virksomheden og se, hvad der foregår i back end. Ved at integrere [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] kan du give dine sælgere denne indsigt ved at gøre det muligt for dem at få vist oplysninger i [!INCLUDE[d365fin](includes/d365fin_md.md)], når de arbejder i [!INCLUDE[crm_md](includes/crm_md.md)]. Ved udarbejdelse af et salgstilbud kan det f.eks. være nyttigt at vide, om der er tilstrækkelig lagerbeholdning til at opfylde ordren. Du kan finde flere oplysninger under [Brug af Dynamics 365 for Sales fra Business Central](marketing-integrate-dynamicscrm.md).

> [!Note]
> Følgende fremgangsmåde beskriver processen med at integrere onlineversioner af [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)].

<!--## Software Requirements
You must have an Office 365 subscription, and both [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)] must be part of the same organization.  -->

## <a name="overview-of-the-integration-process"></a>Oversigt over integrationsprocessen
Nedenfor følger en oversigt over trinnene til integration af [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Disse opgaver kræver sikkerhedsrollen **Systemadministrator** i [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. I Office 365-administrationscenteret skal du oprette en brugerkonto til at oprette forbindelse til og synkronisere data med [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger under [Konfiguration af integration med Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

2. Tildel licenser til [!INCLUDE[crm_md](includes/crm_md.md)] til de [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere, der skal bruge de integrerede apps.

3. Opret en forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)]. Der er flere oplysninger under [Oprette forbindelse til Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md).  

4. Valgfrit: Sammenkæd [!INCLUDE[d365fin](includes/d365fin_md.md)]- og [!INCLUDE[crm_md](includes/crm_md.md)]-poster. Du kan finde flere oplysninger i [Sammenkæd og synkroniser poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md).

5. Synkroniser data mellem programmer. Du kan finde flere oplysninger under [Synkronisering af Business Central og Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md).  

## <a name="about-the-business-central-integration-solution"></a>Om Business Central-integrationsløsning
Ved hjælp af løsningen kan brugere få vist oplysninger i [!INCLUDE[d365fin](includes/d365fin_md.md)], når de arbejder i [!INCLUDE[crm_md](includes/crm_md.md)]. Det kan f.eks. give indsigt i debitorstatistik, give brugerne mulighed for at sammenkæde og få vist poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] fra [!INCLUDE[crm_md](includes/crm_md.md)] og gøre det muligt at se, om produkter er tilgængelige i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Som standard importerer den assisterede opsætningsvejledning Konfigurer Dynamics 365 for Sales-forbindelse [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrationsløsningen. Til at gøre dette bruger opsætningsvejledningen en administratorbrugerkonto. Denne konto skal også være en gyldig bruger i [!INCLUDE[crm_md](includes/crm_md.md)] med følgende sikkerhedsroller:

* Systemadministrator  
* Løsningsoptimerer  

Du kan finde flere oplysninger i [Konfigurere brugerkonti til integration med Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md), [Oprette brugere i Microsoft Dynamics 365 (online) og tildele sikkerhedsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles.md), og [Administrere brugere og deres rettigheder](ui-how-users-permissions.md).  

Denne konto bruges kun én gang under opsætningen. Når løsningen er importeret til [!INCLUDE[d365fin](includes/d365fin_md.md)], er kontoen ikke længere nødvendig. Integrationen fortsætter med at bruge den brugerkonto, der er oprettet specielt til integrationen.

Ud over at tilpasse [!INCLUDE[crm_md](includes/crm_md.md)] opretter [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrationsløsningen også følgende roller i [!INCLUDE[crm_md](includes/crm_md.md)] til integrationen:

* **Integrationsadministrator** – gør det muligt at styre forbindelsen mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)]. Er typisk kun tildelt til brugerkontoen til synkronisering.  
* **Integrationsbruger** – gør det muligt at få adgang til synkroniserede data. Er normalt knyttet til brugerkontoen til synkronisering og alle andre brugere, der skal have vist eller have adgang til de synkroniserede data.
* **Produkttilgængelighedsbruger** – giver brugere mulighed for at forespørge om produkttilgængelighed i [!INCLUDE[d365fin](includes/d365fin_md.md)] fra [!INCLUDE[crm_md](includes/crm_md.md)].

I slutningen af opsætningsvejledningen bliver du af [!INCLUDE[d365fin](includes/d365fin_md.md)] bedt om at kæde sælgere sammen med brugere i [!INCLUDE[crm_md](includes/crm_md.md)]. Poster i [!INCLUDE[crm_md](includes/crm_md.md)] har som regel en tildelt ejer (bruger), og hvis sammenkædning mellem brugeren i [!INCLUDE[crm_md](includes/crm_md.md)] og sælgeren i [!INCLUDE[d365fin](includes/d365fin_md.md)] ikke findes, mislykkes synkroniseringen. Du kan også gøre det senere ved hjælp af handlingen **Sammenkædning af sælgere** på siden **Konfiguration af Microsoft Dynamics 365-forbindelse**.

## <a name="see-also"></a>Se også  
[Konfigurere brugerkonti til integration med Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Oprette forbindelse til Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md)
[Synkronisering af Business Central og Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)
