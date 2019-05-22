---
title: Sammenkæd og synkroniser records manuelt| Microsoft Docs
description: Synkronisering af en integreret tabeltilknytning muliggør synkronisering af data i alle records i en tabel i Business Central og Dynamics 365 for Sales-enheden, der er sammenkædet.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 36f1a0fe8c50744d9ce13d1e6c3c899f4ceaf5e4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245400"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="9e9be-103">Sammenkæd og synkroniser records manuelt</span><span class="sxs-lookup"><span data-stu-id="9e9be-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="9e9be-104">Dette emne beskriver, hvordan du sammenkæder en eller flere records i [!INCLUDE[d365fin](includes/d365fin_md.md)] med poster i [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9e9be-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="9e9be-105">Sammenkædning af records lader dig se [!INCLUDE[crm_md](includes/crm_md.md)]-oplysninger i [!INCLUDE[d365fin](includes/d365fin_md.md)] og omvendt.</span><span class="sxs-lookup"><span data-stu-id="9e9be-105">Coupling records lets you view [!INCLUDE[crm_md](includes/crm_md.md)] information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="9e9be-106">Sammenkædningen gør det også muligt at synkronisere data mellem records.</span><span class="sxs-lookup"><span data-stu-id="9e9be-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="9e9be-107">Du kan sammenkæde eksisterende records eller oprette og sammenkæde nye records.</span><span class="sxs-lookup"><span data-stu-id="9e9be-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="9e9be-108">Sammenkædning og synkronisering af data med [!INCLUDE[crm_md](includes/crm_md.md)] er kun tilgængelig, hvis din systemadministrator har oprettet en forbindelse mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9e9be-108">Coupling and synchronizing data with [!INCLUDE[crm_md](includes/crm_md.md)] is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="9e9be-109">Dette kan hurtigt kontrolleres ved at åbne **debitor**-kortet og søge efter handlingen **Konfigurer sammenkædning**.</span><span class="sxs-lookup"><span data-stu-id="9e9be-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="9e9be-110">Hvis handlingen er tilgængelig, er programmerne forbundet.</span><span class="sxs-lookup"><span data-stu-id="9e9be-110">If the action is available, the apps are connected.</span></span>   

## <a name="to-couple-a-record"></a><span data-ttu-id="9e9be-111">Sådan sammenkædes en record</span><span class="sxs-lookup"><span data-stu-id="9e9be-111">To couple a record</span></span>  
1.  <span data-ttu-id="9e9be-112">Åbn kortet i [!INCLUDE[d365fin](includes/d365fin_md.md)] til den record, du ønsker at sammenkæde.</span><span class="sxs-lookup"><span data-stu-id="9e9be-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="9e9be-113">F.eks. debitor- eller kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="9e9be-113">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="9e9be-114">Du kan også blot åbne listesiden og vælge den record, du vil sammenkæde.</span><span class="sxs-lookup"><span data-stu-id="9e9be-114">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="9e9be-115">Vælg handlingen **Konfigurer sammenkædning**.</span><span class="sxs-lookup"><span data-stu-id="9e9be-115">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="9e9be-116">Udfyld felterne, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e9be-116">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="9e9be-117">Sådan synkroniseres en enkelt record</span><span class="sxs-lookup"><span data-stu-id="9e9be-117">To synchronize a single record</span></span>  
1.  <span data-ttu-id="9e9be-118">Åbn kortet i [!INCLUDE[d365fin](includes/d365fin_md.md)] til den record, du ønsker at sammenkæde.</span><span class="sxs-lookup"><span data-stu-id="9e9be-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="9e9be-119">F.eks. debitor- eller kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="9e9be-119">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="9e9be-120">Vælg handlingen **Synkroniser nu**.</span><span class="sxs-lookup"><span data-stu-id="9e9be-120">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="9e9be-121">Hvis en record kan synkroniseres fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)] eller fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du vælge den valgmulighed, der angiver retningen for dataopdateringen, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e9be-121">If a record can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="9e9be-122">Sådan synkroniseres flere records</span><span class="sxs-lookup"><span data-stu-id="9e9be-122">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="9e9be-123">Åbn listesiden i [!INCLUDE[d365fin](includes/d365fin_md.md)] den record, f.eks. listesiderne for kunder (debitorer) eller kontakter.</span><span class="sxs-lookup"><span data-stu-id="9e9be-123">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="9e9be-124">Vælg de records, du vil synkronisere, og vælg derefter handlingen **Synkroniser nu**.</span><span class="sxs-lookup"><span data-stu-id="9e9be-124">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="9e9be-125">Hvis records kan synkroniseres fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)] eller fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du vælge den valgmulighed, der angiver retningen for dataopdateringen, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e9be-125">If records can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9e9be-126">Se også</span><span class="sxs-lookup"><span data-stu-id="9e9be-126">See Also</span></span>  
[<span data-ttu-id="9e9be-127">Brug af Dynamics 365 for Sales fra Business Central</span><span class="sxs-lookup"><span data-stu-id="9e9be-127">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
