---
title: Opgradering af en integration med Dynamics 365 Sales | Microsoft Docs
description: Få at vide, hvordan du gør Dynamics 365 Business Central klar til integration med Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 84e335bacbfec965968d6a6839fe1eb407ab089d
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324122"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="c10d0-103">Opgradering af en integration med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="c10d0-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="c10d0-104">kan integreres med [!INCLUDE[d365fin](includes/cds_long_md.md)], hvilket gør det nemt at forbinde og synkronisere data med andre Dynamics 365-programmer såsom [!INCLUDE[crm_md](includes/crm_md.md)] eller endda apps, som du selv opbygger.</span><span class="sxs-lookup"><span data-stu-id="c10d0-104">integrates with [!INCLUDE[d365fin](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="c10d0-105">Hvis det er første gang, du integrerer, anbefaler vi, at du gør det ved hjælp af [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c10d0-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <span data-ttu-id="c10d0-106">Få flere oplysninger i [Integration med Common Data Service](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="c10d0-106">For more information, see [Integration with Common Data Service](admin-common-data-service.md).</span></span>

<span data-ttu-id="c10d0-107">Hvis du allerede har integreret [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du fortsætte med at synkronisere data ved hjælp af din installation.</span><span class="sxs-lookup"><span data-stu-id="c10d0-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="c10d0-108">Men hvis du opgraderer [!INCLUDE[d365fin](includes/d365fin_md.md)] eller deaktiverer din [!INCLUDE[crm_md](includes/crm_md.md)]-integration, skal du oprette forbindelse igen via [!INCLUDE[d365fin](includes/cds_long_md.md)] for at aktivere den igen.</span><span class="sxs-lookup"><span data-stu-id="c10d0-108">However, if you upgrade [!INCLUDE[d365fin](includes/d365fin_md.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="c10d0-109">Hvis du genopretter forbindelsen via [!INCLUDE[d365fin](includes/cds_long_md.md)], anvendes standardindstillingerne for synkroniseringen, og alle konfigurationer, du har angivet, tilsidesættes.</span><span class="sxs-lookup"><span data-stu-id="c10d0-109">Reconnecting through [!INCLUDE[d365fin](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="c10d0-110">Standard-tabeltilknytningerne anvendes for eksempel.</span><span class="sxs-lookup"><span data-stu-id="c10d0-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a><span data-ttu-id="c10d0-111">Sådan opgraderer du din forbindelse til at bruge Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c10d0-111">To upgrade your connection to use Common Data Service</span></span>
1. <span data-ttu-id="c10d0-112">Åbn siden **Opsætning af Microsoft Dynamics 365-forbindelse**, og tryk på knappen **Aktivér** for at deaktivere din nuværende forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c10d0-112">Open the **Microsoft Dynamics 365 Connection Setup** page, choose the **Enable** toggle to turn off your existing connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="c10d0-113">Åbn siden **Opsætning af Common Data Service-forbindelse**, og tryk på knappen **Aktivér** for at aktivere forbindelsen.</span><span class="sxs-lookup"><span data-stu-id="c10d0-113">Open the **Common Data Service Connection Setup** page, and choose the **Enable** toggle to turn on the connection.</span></span>
  
   <span data-ttu-id="c10d0-114">Når du har aktiveret CDS-forbindelsen, installeres Business Central CDS-basisintegrationsløsningen til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c10d0-114">After you enable the CDS connection, the Business Central CDS Base Integration Solution is deployed to Common Data Service.</span></span>
3. <span data-ttu-id="c10d0-115">Tryk på knappen Aktivér på siden til opsætning af Microsoft Dynamics 365-forbindelse for at aktivere forbindelsen til [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c10d0-115">On the Microsoft Dynamics 365 Connection Setup page, choose the Enable toggle to turn on the connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   <span data-ttu-id="c10d0-116">Når du har aktiveret Sales-forbindelsen, installeres Business Central CDS-basisintegrationsløsningen til Sales.</span><span class="sxs-lookup"><span data-stu-id="c10d0-116">After you enable the Sales connection, the Business Central Integration Solution is deployed to Sales.</span></span> <span data-ttu-id="c10d0-117">Dette muliggør integration med objekter, der er specifikke for [!INCLUDE[crm_md](includes/crm_md.md)], f. eks. salgsordrer, tilbud og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="c10d0-117">This enables integration with entities that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
4. <span data-ttu-id="c10d0-118">Vælg **Geninstaller integrationsløsning** for at installere og konfigurere den opgraderede Business Central-integrationsløsning.</span><span class="sxs-lookup"><span data-stu-id="c10d0-118">Choose **Redeploy Integration Solution** to install and configure the upgraded Business Central Integration Solution.</span></span>
5. <span data-ttu-id="c10d0-119">På siden **Opsætning af Sales-forbindelse** skal du vælge **Brug standard-synkroniseringsopsætning** for at starte integrationstabeltilknytninger for [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c10d0-119">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="c10d0-120">Se også</span><span class="sxs-lookup"><span data-stu-id="c10d0-120">See Also</span></span>
[<span data-ttu-id="c10d0-121">Integration med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="c10d0-121">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="c10d0-122">Integration med Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c10d0-122">Integrating with Common Data Service</span></span>](admin-common-data-service.md)