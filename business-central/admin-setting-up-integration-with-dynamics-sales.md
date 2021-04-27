---
title: Konfigurere brugerkonti til integration med Microsoft Dataverse | Microsoft Docs
description: Få at vide, hvordan du konfigurerer brugerkonti, som apps bruger til at udveksle data, og som brugere anvender til at få adgang til og synkronisere data i de pågældende apps.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 2717196a170aede43bfb56d796b1da9307ff8d3f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777187"
---
# <a name="setting-up-user-accounts-for-integrating-with-microsoft-dataverse"></a><span data-ttu-id="78f50-103">Konfigurere brugerkonti til integration med Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="78f50-103">Setting Up User Accounts for Integrating with Microsoft Dataverse</span></span>
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

<span data-ttu-id="78f50-104">Denne artikel indeholder en oversigt over opsætning af de brugerkonti, der kræves til at integrere [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="78f50-104">This article provides an overview of how to set up the user accounts that are required to integrate [!INCLUDE[prod_short](includes/cds_long_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="setting-up-the-administrator-user-account"></a><span data-ttu-id="78f50-105">Opsætning af administratorbrugerkontoen</span><span class="sxs-lookup"><span data-stu-id="78f50-105">Setting Up the Administrator User Account</span></span>
<span data-ttu-id="78f50-106">Du skal tilføje din administratorbrugerkonto for [!INCLUDE[prod_short](includes/prod_short.md)] som en bruger i [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="78f50-106">You must add your administrator user account for [!INCLUDE[prod_short](includes/prod_short.md)] as a user in [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="78f50-107">Når du konfigurerer forbindelsen mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)], skal vi bruge denne konto én gang for at installere og konfigurere nogle påkrævede komponenter.</span><span class="sxs-lookup"><span data-stu-id="78f50-107">When you set up the connection between [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[prod_short](includes/cds_long_md.md)] we will use this account one time to install and configure some required components.</span></span> 

## <a name="permissions-and-security-roles-for-user-accounts-in-prod_short"></a><span data-ttu-id="78f50-108">Tilladelser og sikkerhedsroller for brugerkonti i [!INCLUDE[prod_short](includes/cds_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="78f50-108">Permissions and Security Roles for User Accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)]</span></span>
<span data-ttu-id="78f50-109">Når du installerer CDS-basisintegrationsløsningen, konfigureres tilladelser til integrationsbrugerkontoen.</span><span class="sxs-lookup"><span data-stu-id="78f50-109">When you install the CDS Base Integration Solution, permissions for the integration user account are configured.</span></span> <span data-ttu-id="78f50-110">Hvis disse tilladelser ændres manuelt, kan du nulstille dem.</span><span class="sxs-lookup"><span data-stu-id="78f50-110">If those permissions are changed manually you can reset them.</span></span> <span data-ttu-id="78f50-111">Det kan du gøre ved at geninstallere CDS-basisintegrationsløsningen ved at vælge **Geninstaller integrationsløsning** på siden **Opsætning af Common Data Service-forbindelse**.</span><span class="sxs-lookup"><span data-stu-id="78f50-111">You can do that by reinstalling the CDS Base Integration Solution by choosing **Redeploy Integration Solution** on the **Common Data Service Connection Setup** page.</span></span> <span data-ttu-id="78f50-112">Business Central CDS-integrationssikkerhedsrollen er installeret.</span><span class="sxs-lookup"><span data-stu-id="78f50-112">The Business Central CDS Integration security role is deployed.</span></span>

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

### Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

##### Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## <a name="see-also"></a><span data-ttu-id="78f50-113">Se også</span><span class="sxs-lookup"><span data-stu-id="78f50-113">See Also</span></span>  
[<span data-ttu-id="78f50-114">Integration med Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="78f50-114">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)  
[<span data-ttu-id="78f50-115">Integration med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="78f50-115">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]