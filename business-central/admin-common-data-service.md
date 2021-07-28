---
title: Brug af Microsoft Dataverse
description: Introduktion til integration og brug af Microsoft Dataverse og komponenter til at oprette forbindelse til andre Dynamics 365-programmer.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 06/14/2021
ms.openlocfilehash: 34e274b32fbf8cf04a40cf4db884c156e2115416
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/30/2021
ms.locfileid: "6320959"
---
# <a name="integrating-with-microsoft-dataverse"></a>Integration med Microsoft Dataverse
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Forretningsapps bruger ofte data fra mere end én kilde. [!INCLUDE[prod_short](includes/cds_long_md.md)] kombinerer data til et enkelt sæt logik, som gør det nemmere at forbinde andre Dynamics 365-programmer, f.eks. [!INCLUDE[crm_md](includes/crm_md.md)] eller dit eget program, som er oprettet oven på [!INCLUDE[prod_short](includes/cds_long_md.md)], til [!INCLUDE[prod_short_md](includes/prod_short.md)]. Du kan få flere oplysninger om [!INCLUDE[prod_short](includes/cds_long_md.md)] i [Hvad er Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)

Nedenfor følger en oversigt over trinnene til integration af [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Disse opgaver kræver sikkerhedsrollen **Systemadministrator** i [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Tildel licenser til [!INCLUDE[prod_short](includes/cds_long_md.md)] til de [!INCLUDE[prod_short](includes/prod_short.md)]-brugere, der skal bruge de integrerede apps.

2. Opret en forbindelse til [!INCLUDE[prod_short](includes/cds_long_md.md)]. Du kan få flere oplysninger i [Forbind til Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synkroniser data mellem programmer. Du kan finde flere oplysninger i [Synkronisering af Business Central og Dataverse](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-prod_short"></a>Introduktion til [!INCLUDE[prod_short](includes/cds_long_md.md)]
For at komme i gang med [!INCLUDE[prod_short](includes/cds_long_md.md)] skal du have en Microsoft Power Apps-konto. Hvis du ikke allerede har en Power Apps-konto, kan du få en gratis adresse ved at besøge [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) og vælge hyperlinket **Kom gratis i gang**. Hvis du vil have mere at vide om, hvordan du kommer i gang med [!INCLUDE[prod_short](includes/cds_long_md.md)], skal du se [Kom i gang med Dataverse](/learn/modules/get-started-with-powerapps-common-data-service/)-modulet fra Microsoft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Tovejs eller etvejs datasynkronisering
Afhængigt af virksomhedens behov kan du konfigurere integrationen til at synkronisere data enten til eller fra en Dynamics 365-forretningsapp til en anden eller i begge retninger og næsten i realtid via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Hvis du f.eks. integrerer [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] via [!INCLUDE[prod_short](includes/cds_long_md.md)], kan en sælger oprette en salgsordre i [!INCLUDE[crm_md](includes/crm_md.md)], hvorefter ordren synkroniseres til [!INCLUDE[prod_short](includes/prod_short.md)]. Fra [!INCLUDE[crm_md](includes/crm_md.md)] kan sælgeren ligeledes se oplysninger fra [!INCLUDE[prod_short](includes/prod_short.md)] om, hvorvidt varen i ordren er på lager. 

## <a name="standard-and-custom-entities"></a>Standardobjekter og brugerdefinerede objekter
[!INCLUDE[prod_short](includes/cds_long_md.md)] gemmer data sikkert i en række tabeller, som er postsæt, der svarer til, hvordan en tabel gemmer data i en database. [!INCLUDE[prod_short](includes/cds_long_md.md)] indeholder et grundlæggende sæt standardtabeller, der dækker typiske scenarier, men du kan også oprette brugerdefinerede tabeller, der er specifikke for din virksomhed. I [!INCLUDE[prod_short](includes/prod_short.md)] kan du se de standardobjekter og brugerdefinerede tabeller, der synkroniseres, på siden Integrationstabeltilknytninger.

## <a name="about-the-business-central-base-integration-solution"></a>Om Business Central-basisintegrationsløsningen

Business Central-basisintegrationsløsningen er en nøglekomponent i integrationen. Løsningen føjer de nødvendige roller og adgangsniveauer til brugerkontiene for integrationen og opretter de tabeller, der kræves for at knytte [!INCLUDE[prod_short](includes/prod_short.md)]-virksomheden til en afdeling i [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Som standard vil vejledningen til **Opsætning af [!INCLUDE[prod_short](includes/cds_long_md.md)]-forbindelse** med assisteret opsætning importere løsningen. For at gøre dette bruger opsætningsvejledningen en administratorbrugerkonto, som du angiver. Denne konto skal være en gyldig bruger i [!INCLUDE[prod_short](includes/cds_long_md.md)] med følgende sikkerhedsrolle:

* Systemadministrator  

Du kan få flere oplysninger i [Opsætning af brugerkonti til integration med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) og [Oprettelse af brugere i Microsoft Dynamics 365 (online) og tildeling af sikkerhedsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Administratorkontoen bruges kun én gang i løbet af opsætningen til de konfigurationsændringer, som Business Central-basisintegrationsløsningen udfører i [!INCLUDE[prod_short](includes/cds_long_md.md)]. Når løsningen er importeret, er kontoen ikke længere nødvendig. Integrationen fortsætter med at bruge den brugerkonto, der er automatisk oprettet specielt til integrationen.

Ud over at tilpasse [!INCLUDE[prod_short](includes/cds_long_md.md)] opretter løsningen desuden følgende roller i [!INCLUDE[prod_short](includes/cds_long_md.md)] til integrationen:

* **Integrationsadministrator** – gør det muligt at styre forbindelsen mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]. Dette knyttes som regel kun til den automatisk oprettede brugerkonto til synkronisering.  
* **Integrationsbruger** – gør det muligt at få adgang til synkroniserede data. Dette knyttes typisk til den automatisk oprettede brugerkonto til synkronisering og alle andre brugere, der skal se eller have adgang til de synkroniserede data.

Du kan finde flere oplysninger om de enkelte roller, f.eks. tilladelser og adgangsniveauer, i [Oprette brugerkonti til integration med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Når forbindelsen opsættes, oprettes de integrationstabeltilknytninger, der er nødvendige for at synkronisere data. Objekter i [!INCLUDE[prod_short](includes/cds_long_md.md)] knyttes til tabeller og tabelfelter i Business Central ved hjælp af integrationstabeller. Få flere oplysninger i [Standard-objekttilknytning til synkronisering](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="see-also"></a>Se også
[Modeller for ejerskab af data](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->





[!INCLUDE[footer-include](includes/footer-banner.md)]