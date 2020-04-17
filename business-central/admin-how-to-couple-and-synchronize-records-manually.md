---
title: Sammenkæd og synkroniser records manuelt| Microsoft Docs
description: Synkronisering af en integreret tabeltilknytning muliggør synkronisering af data i alle records i en tabel i Business Central og Dynamics 365 Sales-enheden, der er sammenkædet.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: fdc407ef26d238ba54a2566cdd9003c29da2eeb3
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196659"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="69504-103">Sammenkæd og synkroniser records manuelt</span><span class="sxs-lookup"><span data-stu-id="69504-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="69504-104">Dette emne handler om, hvordan du sammenkæder en eller flere poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] med poster i Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="69504-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="69504-105">Sammenkædning af records lader dig se Common Data Service-oplysninger i [!INCLUDE[d365fin](includes/d365fin_md.md)] og omvendt.</span><span class="sxs-lookup"><span data-stu-id="69504-105">Coupling records lets you view Common Data Service information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="69504-106">Sammenkædningen gør det også muligt at synkronisere data mellem records.</span><span class="sxs-lookup"><span data-stu-id="69504-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="69504-107">Du kan sammenkæde eksisterende records eller oprette og sammenkæde nye records.</span><span class="sxs-lookup"><span data-stu-id="69504-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="69504-108">Sammenkædning og synkronisering af data er kun mulig, hvis din systemadministrator har oprettet en forbindelse mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="69504-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="69504-109">Dette kan hurtigt kontrolleres ved at åbne **debitor**-kortet og søge efter handlingen **Konfigurer sammenkædning**.</span><span class="sxs-lookup"><span data-stu-id="69504-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="69504-110">Hvis handlingen er tilgængelig, er programmerne forbundet.</span><span class="sxs-lookup"><span data-stu-id="69504-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="69504-111">Videoeksempel</span><span class="sxs-lookup"><span data-stu-id="69504-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="69504-112">Sådan sammenkædes en record</span><span class="sxs-lookup"><span data-stu-id="69504-112">To couple a record</span></span>  
1.  <span data-ttu-id="69504-113">Åbn kortet i [!INCLUDE[d365fin](includes/d365fin_md.md)] til den record, du ønsker at sammenkæde.</span><span class="sxs-lookup"><span data-stu-id="69504-113">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="69504-114">F.eks. debitor- eller kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="69504-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="69504-115">Du kan også blot åbne listesiden og vælge den record, du vil sammenkæde.</span><span class="sxs-lookup"><span data-stu-id="69504-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="69504-116">Vælg handlingen **Konfigurer sammenkædning**.</span><span class="sxs-lookup"><span data-stu-id="69504-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="69504-117">Udfyld felterne, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="69504-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="69504-118">Sådan synkroniseres en enkelt record</span><span class="sxs-lookup"><span data-stu-id="69504-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="69504-119">Åbn kortet i [!INCLUDE[d365fin](includes/d365fin_md.md)] til den record, du ønsker at sammenkæde.</span><span class="sxs-lookup"><span data-stu-id="69504-119">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="69504-120">F.eks. debitor- eller kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="69504-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="69504-121">Vælg handlingen **Synkroniser nu**.</span><span class="sxs-lookup"><span data-stu-id="69504-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="69504-122">Hvis en post kan synkroniseres i én retning, skal du vælge den valgmulighed, der angiver retningen for dataopdateringen, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="69504-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="69504-123">Sådan synkroniseres en enkelt post fra [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="69504-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="69504-124">Åbn formularen til den post, du vil sammenkæde, i [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="69504-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="69504-125">Det kan f.eks. være Kontokort- eller Kontaktkort-formularen.</span><span class="sxs-lookup"><span data-stu-id="69504-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="69504-126">Vælg handlingen **[!INCLUDE[d365fin](includes/d365fin_md.md)]** på båndet for at åbne og sammenkæde posten automatisk.</span><span class="sxs-lookup"><span data-stu-id="69504-126">Choose the **[!INCLUDE[d365fin](includes/d365fin_md.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="69504-127">Du kan kun synkronisere en enkelt post fra [!INCLUDE[crm_md](includes/crm_md.md)] automatisk, når **Synkroniser kun sammenkædede poster** er deaktiveret, og synkroniseringsretningen angives til Tovejs eller Fra integrationstabel på siden **Integrationstabelknytning** for posten.</span><span class="sxs-lookup"><span data-stu-id="69504-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="69504-128">Få flere oplysninger i [Tilknytning af tabeller og felter, der skal synkroniseres](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="69504-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="69504-129">Sådan synkroniseres flere records</span><span class="sxs-lookup"><span data-stu-id="69504-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="69504-130">Åbn listesiden i [!INCLUDE[d365fin](includes/d365fin_md.md)] den record, f.eks. listesiderne for kunder (debitorer) eller kontakter.</span><span class="sxs-lookup"><span data-stu-id="69504-130">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="69504-131">Vælg de records, du vil synkronisere, og vælg derefter handlingen **Synkroniser nu**.</span><span class="sxs-lookup"><span data-stu-id="69504-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="69504-132">Hvis poster kan synkroniseres i én retning, skal du vælge den valgmulighed, der angiver retningen for dataopdateringen, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="69504-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="69504-133">Se også</span><span class="sxs-lookup"><span data-stu-id="69504-133">See Also</span></span>  
[<span data-ttu-id="69504-134">Bruge Dynamics 365 Sales fra Business Central</span><span class="sxs-lookup"><span data-stu-id="69504-134">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
