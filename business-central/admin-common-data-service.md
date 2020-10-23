---
title: Brug af Common Data Service
description: Introduktion til Common Data Service og dets komponenter.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.openlocfilehash: 85823e93b1d239bf4e59ec6a8872cdc4a2cef9c1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911576"
---
# <a name="integrating-with-common-data-service"></a>Integration med Common Data Service

Forretningsapps bruger ofte data fra mere end én kilde. [!INCLUDE[d365fin](includes/cds_long_md.md)] kombinerer data til et enkelt sæt logik, som gør det nemmere at forbinde andre Dynamics 365-programmer, f.eks. [!INCLUDE[crm_md](includes/crm_md.md)] eller dit eget program, som er oprettet oven på [!INCLUDE[d365fin](includes/cds_long_md.md)], til [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Du kan få flere oplysninger om [!INCLUDE[d365fin](includes/cds_long_md.md)] i [Hvad er Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

Nedenfor følger en oversigt over trinnene til integration af [!INCLUDE[d365fin](includes/cds_long_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Disse opgaver kræver sikkerhedsrollen **Systemadministrator** i [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Tildel licenser til [!INCLUDE[d365fin](includes/cds_long_md.md)] til de [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere, der skal bruge de integrerede apps.

2. Opret en forbindelse til [!INCLUDE[d365fin](includes/cds_long_md.md)]. Du kan få flere oplysninger i [Forbind til Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synkroniser data mellem programmer. Du kan finde flere oplysninger under [Synkronisering af Business Central og Common Data Service](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-d365fin"></a>Introduktion til [!INCLUDE[d365fin](includes/cds_long_md.md)]
For at komme i gang med [!INCLUDE[d365fin](includes/cds_long_md.md)] skal du have en Microsoft Power Apps-konto. Hvis du ikke allerede har en Power Apps-konto, kan du få en gratis adresse ved at besøge [powerapps.com](https://web.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) og vælge hyperlinket **Kom gratis i gang**. Du kan få mere at vide om, hvordan du kommer i gang med [!INCLUDE[d365fin](includes/cds_long_md.md)] i modulet [Kom i gang med Common Data Service](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/) fra Microsoft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Tovejs eller etvejs datasynkronisering
Afhængigt af virksomhedens behov kan du konfigurere integrationen til at synkronisere data enten til eller fra en Dynamics 365-forretningsapp til en anden eller i begge retninger og næsten i realtid via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Hvis du f. eks. integrerer [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] via [!INCLUDE[d365fin](includes/cds_long_md.md)], kan en sælger oprette en salgsordre i [!INCLUDE[crm_md](includes/crm_md.md)], hvorefter ordren synkroniseres til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Fra [!INCLUDE[crm_md](includes/crm_md.md)] kan sælgeren ligeledes se oplysninger fra [!INCLUDE[d365fin](includes/d365fin_md.md)] om, hvorvidt varen i ordren er på lager. 

## <a name="standard-and-custom-entities"></a>Standardobjekter og brugerdefinerede objekter
[!INCLUDE[d365fin](includes/cds_long_md.md)] gemmer data sikkert i en række enheder, som er postsæt, der svarer til, hvordan en tabel gemmer data i en database. [!INCLUDE[d365fin](includes/cds_long_md.md)] indeholder et grundlæggende sæt standardobjekter, der dækker typiske scenarier, men du kan også oprette brugerdefinerede objekter, der er specifikke for din virksomhed. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du se de standardobjekter og brugerdefinerede objekter, der synkroniseres, på siden Integrationstabeltilknytninger.

## <a name="about-the-base-cds-integration-solution"></a>Om Basis-CDS-integrationsløsningen

Basis-CDS-integrationsløsningen er en nøglekomponent i integrationen. Løsningen føjer de nødvendige roller og adgangsniveauer til brugerkontiene for integrationen og opretter de objekter, der kræves for at knytte [!INCLUDE[d365fin](includes/d365fin_md.md)]-virksomheden til en afdeling i [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

Som standard vil vejledningen til **Opsætning af [!INCLUDE[d365fin](includes/cds_long_md.md)]-forbindelse** med assisteret opsætning importere løsningen. For at gøre dette bruger opsætningsvejledningen en administratorbrugerkonto, som du angiver. Denne konto skal være en gyldig bruger i [!INCLUDE[d365fin](includes/cds_long_md.md)] med følgende sikkerhedsrolle:

* Systemadministrator  

Du kan få flere oplysninger i [Opsætning af brugerkonti til integration med [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) og [Oprettelse af brugere i Microsoft Dynamics 365 (online) og tildeling af sikkerhedsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Administratorkontoen bruges kun én gang i løbet af opsætningen på grund af konfigurationsændringer, som Basis-CDS-løsningen udfører i [!INCLUDE[d365fin](includes/cds_long_md.md)]. Når løsningen er importeret, er kontoen ikke længere nødvendig. Integrationen fortsætter med at bruge den brugerkonto, der er automatisk oprettet specielt til integrationen.

Ud over at tilpasse [!INCLUDE[d365fin](includes/cds_long_md.md)] opretter løsningen desuden følgende roller i [!INCLUDE[d365fin](includes/cds_long_md.md)] til integrationen:

* **Integrationsadministrator** – gør det muligt at styre forbindelsen mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)]. Dette knyttes som regel kun til den automatisk oprettede brugerkonto til synkronisering.  
* **Integrationsbruger** – gør det muligt at få adgang til synkroniserede data. Dette knyttes typisk til den automatisk oprettede brugerkonto til synkronisering og alle andre brugere, der skal se eller have adgang til de synkroniserede data.

Du kan finde flere oplysninger om de enkelte roller, f.eks. tilladelser og adgangsniveauer, i [Oprette brugerkonti til integration med [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Når forbindelsen opsættes, oprettes de integrationstabeltilknytninger, der er nødvendige for at synkronisere data. Objekter i Common Data Service knyttes til tabeller og tabelfelter i Business Central ved hjælp af integrationstabeller. Få flere oplysninger i [Standard-objekttilknytning til synkronisering](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).

## <a name="see-also"></a>Se også
[Modeller for ejerskab af data](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Common Data Service](docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration) -->



