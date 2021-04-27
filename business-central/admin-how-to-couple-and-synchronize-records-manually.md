---
title: Kobling og synkronisering | Microsoft Docs
description: Synkronisering af en integreret tabeltilknytning muliggør synkronisering af data i alle records i en tabel i Business Central og Dynamics 365 Sales-tabellen, der er sammenkædet.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 53b12b6ab7e53a20bb1b8fcc659b2f1454e85321
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779928"
---
# <a name="coupling-and-synchronizing"></a><span data-ttu-id="c881c-103">Kobling og synkronisering</span><span class="sxs-lookup"><span data-stu-id="c881c-103">Coupling and Synchronizing</span></span>
<span data-ttu-id="c881c-104">Dette emne handler om, hvordan du sammenkæder en eller flere poster i [!INCLUDE[prod_short](includes/prod_short.md)] med poster i Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c881c-104">This topic describes how to couple one or more records in [!INCLUDE[prod_short](includes/prod_short.md)] with records in Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="c881c-105">Sammenkædning af records lader dig se Dataverse-oplysninger i [!INCLUDE[prod_short](includes/prod_short.md)] og omvendt.</span><span class="sxs-lookup"><span data-stu-id="c881c-105">Coupling records lets you view Dataverse information from [!INCLUDE[prod_short](includes/prod_short.md)], and vice versa.</span></span> <span data-ttu-id="c881c-106">Sammenkædningen gør det også muligt at synkronisere data mellem records.</span><span class="sxs-lookup"><span data-stu-id="c881c-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="c881c-107">Du kan sammenkæde eksisterende records eller oprette og sammenkæde nye records.</span><span class="sxs-lookup"><span data-stu-id="c881c-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="c881c-108">Sammenkædning og synkronisering af data er kun mulig, hvis din systemadministrator har oprettet en forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c881c-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[prod_short](includes/prod_short.md)] and Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="c881c-109">Dette kan hurtigt kontrolleres ved at åbne **debitor**-kortet og søge efter handlingen **Konfigurer sammenkædning**.</span><span class="sxs-lookup"><span data-stu-id="c881c-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="c881c-110">Hvis handlingen er tilgængelig, er programmerne forbundet.</span><span class="sxs-lookup"><span data-stu-id="c881c-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="c881c-111">Videoeksempel</span><span class="sxs-lookup"><span data-stu-id="c881c-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="c881c-112">Sådan sammenkædes en record</span><span class="sxs-lookup"><span data-stu-id="c881c-112">To couple a record</span></span>  
1.  <span data-ttu-id="c881c-113">Åbn kortet i [!INCLUDE[prod_short](includes/prod_short.md)] til den record, du ønsker at sammenkæde.</span><span class="sxs-lookup"><span data-stu-id="c881c-113">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="c881c-114">F.eks. debitor- eller kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="c881c-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="c881c-115">Du kan også blot åbne listesiden og vælge den record, du vil sammenkæde.</span><span class="sxs-lookup"><span data-stu-id="c881c-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="c881c-116">Vælg handlingen **Konfigurer sammenkædning**.</span><span class="sxs-lookup"><span data-stu-id="c881c-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="c881c-117">Udfyld felterne, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="c881c-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="c881c-118">Sådan synkroniseres en enkelt record</span><span class="sxs-lookup"><span data-stu-id="c881c-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="c881c-119">Åbn kortet i [!INCLUDE[prod_short](includes/prod_short.md)] til den record, du ønsker at sammenkæde.</span><span class="sxs-lookup"><span data-stu-id="c881c-119">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="c881c-120">F.eks. debitor- eller kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="c881c-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="c881c-121">Vælg handlingen **Synkroniser nu**.</span><span class="sxs-lookup"><span data-stu-id="c881c-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="c881c-122">Hvis en post kan synkroniseres i én retning, skal du vælge den valgmulighed, der angiver retningen for dataopdateringen, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="c881c-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="c881c-123">Sådan synkroniseres en enkelt post fra [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="c881c-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="c881c-124">Åbn formularen til den post, du vil sammenkæde, i [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c881c-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="c881c-125">Det kan f.eks. være Kontokort- eller Kontaktkort-formularen.</span><span class="sxs-lookup"><span data-stu-id="c881c-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="c881c-126">Vælg handlingen **[!INCLUDE[prod_short](includes/prod_short.md)]** på båndet for at åbne og sammenkæde posten automatisk.</span><span class="sxs-lookup"><span data-stu-id="c881c-126">Choose the **[!INCLUDE[prod_short](includes/prod_short.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="c881c-127">Du kan kun synkronisere en enkelt post fra [!INCLUDE[crm_md](includes/crm_md.md)] automatisk, når **Synkroniser kun sammenkædede poster** er deaktiveret, og synkroniseringsretningen angives til Tovejs eller Fra integrationstabel på siden **Integrationstabelknytning** for posten.</span><span class="sxs-lookup"><span data-stu-id="c881c-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="c881c-128">Få flere oplysninger i [Tilknytning af tabeller og felter, der skal synkroniseres](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="c881c-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="c881c-129">Sådan synkroniseres flere records</span><span class="sxs-lookup"><span data-stu-id="c881c-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="c881c-130">Åbn listesiden i [!INCLUDE[prod_short](includes/prod_short.md)] den record, f.eks. listesiderne for kunder (debitorer) eller kontakter.</span><span class="sxs-lookup"><span data-stu-id="c881c-130">In [!INCLUDE[prod_short](includes/prod_short.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="c881c-131">Vælg de records, du vil synkronisere, og vælg derefter handlingen **Synkroniser nu**.</span><span class="sxs-lookup"><span data-stu-id="c881c-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="c881c-132">Hvis poster kan synkroniseres i én retning, skal du vælge den valgmulighed, der angiver retningen for dataopdateringen, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="c881c-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="uncoupling-records"></a><span data-ttu-id="c881c-133">Ophævelse af sammenkædning af poster</span><span class="sxs-lookup"><span data-stu-id="c881c-133">Uncoupling Records</span></span>
<span data-ttu-id="c881c-134">Du kan fjerne frakoble en eller flere poster fra listesider eller siden **Koblede datasynkroniseringsfejl** ved at vælge en eller flere linjer og vælge **Slet kobling**.</span><span class="sxs-lookup"><span data-stu-id="c881c-134">You can uncouple one or more records from list pages or the **Coupled Data Synchronization Errors** page by choosing one or more lines and choosing **Delete Coupling**.</span></span> <span data-ttu-id="c881c-135">Du kan også fjerne alle koblinger for en eller flere tabeltilknytninger på siden **Tilknytninger til integrationstabel**.</span><span class="sxs-lookup"><span data-stu-id="c881c-135">You can also remove all couplings for one or more table mappings on the **Integration Table Mappings** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="c881c-136">Se også</span><span class="sxs-lookup"><span data-stu-id="c881c-136">See Also</span></span>  
[<span data-ttu-id="c881c-137">Bruge Dynamics 365 Sales fra Business Central</span><span class="sxs-lookup"><span data-stu-id="c881c-137">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]