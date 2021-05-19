---
title: Opgradering af en integration med Dynamics 365 Sales
description: Få mere at vide om, hvordan du kan flytte Dynamics 365 Business Central-integrationen med Dynamics 365 Sales til den nyeste version.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 772052fc88e0b8be7ec5276600b0c237e2d2f8b2
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025804"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="00aa6-103">Opgradering af en integration med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="00aa6-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="00aa6-104">kan integreres med [!INCLUDE[prod_short](includes/cds_long_md.md)], hvilket gør det nemt at forbinde og synkronisere data med andre Dynamics 365-programmer såsom [!INCLUDE[crm_md](includes/crm_md.md)] eller endda apps, som du selv opbygger.</span><span class="sxs-lookup"><span data-stu-id="00aa6-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="00aa6-105">Hvis det er første gang, du integrerer, anbefaler vi, at du gør det ved hjælp af [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00aa6-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="00aa6-106">Få flere oplysninger i [Integration med Dataverse](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="00aa6-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="00aa6-107">Hvis du allerede har integreret [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)], kan du fortsætte med at synkronisere data ved hjælp af din installation.</span><span class="sxs-lookup"><span data-stu-id="00aa6-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="00aa6-108">Men hvis du opgraderer [!INCLUDE[prod_short](includes/prod_short.md)] eller deaktiverer din [!INCLUDE[crm_md](includes/crm_md.md)]-integration, skal du oprette forbindelse igen via [!INCLUDE[prod_short](includes/cds_long_md.md)] for at aktivere den igen.</span><span class="sxs-lookup"><span data-stu-id="00aa6-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="00aa6-109">Hvis du genopretter forbindelsen via [!INCLUDE[prod_short](includes/cds_long_md.md)], anvendes standardindstillingerne for synkroniseringen, og alle konfigurationer, du har angivet, tilsidesættes.</span><span class="sxs-lookup"><span data-stu-id="00aa6-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="00aa6-110">Standard-tabeltilknytningerne anvendes for eksempel.</span><span class="sxs-lookup"><span data-stu-id="00aa6-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="00aa6-111">Sådan opgraderer du din forbindelse til at bruge Dataverse</span><span class="sxs-lookup"><span data-stu-id="00aa6-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="00aa6-112">Åbn siden **Microsoft Dynamics 365-forbindelsesopsætning**, og tryk på knappen **Aktiveret** for at afbryde forbindelse fra [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00aa6-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="00aa6-113">Åbn siden **Dataverse-forbindelsesopsætning**, og tryk på **Aktiveret** for at aktivere forbindelsen til [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00aa6-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="00aa6-114">Når du har aktiveret forbindelsen, installeres Business Central-basisintegrationsløsningen til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="00aa6-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="00aa6-115">Vælg **Geninstaller integrationsløsning** for at geninstallere og konfigurere Business Central-integrationsløsning.</span><span class="sxs-lookup"><span data-stu-id="00aa6-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="00aa6-116">På siden **Konfiguration af Microsoft Dynamics 365-forbindelse** skal du slå **Aktiveret** til for at genoprette forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00aa6-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="00aa6-117">Når du har aktiveret forbindelsen, installeres Business Central-basisintegrationsløsningen til [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="00aa6-117">After you enable the connection, the Business Central Integration Solution is deployed to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="00aa6-118">Dette muliggør integration med tabeller, der er specifikke for [!INCLUDE[crm_md](includes/crm_md.md)], f.eks. salgsordrer, tilbud og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="00aa6-118">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="00aa6-119">Vælg **Geninstaller integrationsløsning** for at geninstallere og konfigurere Business Central-integrationsløsning.</span><span class="sxs-lookup"><span data-stu-id="00aa6-119">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
6. <span data-ttu-id="00aa6-120">På siden **Opsætning af Sales-forbindelse** skal du vælge **Brug standard-synkroniseringsopsætning** for at starte integrationstabeltilknytninger for [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00aa6-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="00aa6-121">Når du bruger handlingen **Brug standardsynkronisering af opsætning**, anvendes standardtilknytningerne for integrationstabellen.</span><span class="sxs-lookup"><span data-stu-id="00aa6-121">Using the **Use Default Synchronization Setup** action will apply the default integration table mappings.</span></span> <span data-ttu-id="00aa6-122">Alle brugerdefinerede tilknytninger overskrives.</span><span class="sxs-lookup"><span data-stu-id="00aa6-122">All custom mappings will be overwritten.</span></span> <span data-ttu-id="00aa6-123">Hvis du har brugerdefinerede tilknytninger, som du vil bevare, anbefales det, at du eksporterer dem til Excel eller taler med din Microsoft-partner om andre metoder til at holde styr på dine egne tilknytninger.</span><span class="sxs-lookup"><span data-stu-id="00aa6-123">If you have custom mappings that you want to keep, we recommend that you export them to Excel or talk to your Microsoft partner about other ways to keep your custom mappings.</span></span>    

## <a name="see-also"></a><span data-ttu-id="00aa6-124">Se også</span><span class="sxs-lookup"><span data-stu-id="00aa6-124">See Also</span></span>
[<span data-ttu-id="00aa6-125">Integration med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="00aa6-125">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="00aa6-126">Integration med Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="00aa6-126">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]