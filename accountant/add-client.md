---
title: Hent kunder ind i Dynamics 365-revisioroplevelsen | Microsoft Docs
description: "Få at vide, hvordan du føjer eksisterende kunder til Accountant Hub til Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 6543eb4210a64802660189e5060975a327d71099
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="add-clients-to-your-dashboard-in-included365acclongincludesd365acclongmdmd"></a><span data-ttu-id="8948c-103">Tilføje kunder til dit dashboard i [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="8948c-103">Add Clients to Your Dashboard in [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span></span>
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

<span data-ttu-id="8948c-104">Du kan tilføje en kunde i vinduet **Kunde**, som du kan åbne ved at vælge handlingen **Administrer kunder** på båndet.</span><span class="sxs-lookup"><span data-stu-id="8948c-104">You can add a client by using the **Clients** window, which you can open by choosing the **Manage Clients** action in the ribbon.</span></span> <span data-ttu-id="8948c-105">Vælg **Ny**, og udfyld felterne.</span><span class="sxs-lookup"><span data-stu-id="8948c-105">Simply choose **New** and then fill in the fields.</span></span>  

![Tilføje en kunde](./media/accountant-add-client/manage-client.png)

<span data-ttu-id="8948c-107">Du angiver dataene i kortet for hver kunde, og du kan ændre dem efter behov.</span><span class="sxs-lookup"><span data-stu-id="8948c-107">The data in the card for each client is specified by you, and you can change it as needed.</span></span> <span data-ttu-id="8948c-108">Men feltet **Kundens URL-adresse** er vigtigt – det er her, du kan få adgang til den enkelte kundes [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8948c-108">However, the **Client URL** field is critical - this is how you can access each client's [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8948c-109">Brug handlingen **Kontrollér kundens URL-adresse** på båndet til at kontrollere, at du har angivet det rigtige link.</span><span class="sxs-lookup"><span data-stu-id="8948c-109">Use the **Test Client URL** action in the ribbon to test that you entered the right link.</span></span> <span data-ttu-id="8948c-110">Den URL-adresse, du skal angive, peger på kundens [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. *https://mybusiness.financials.dynamics.com*. Denne URL-adresse bruges derefter, når du klikker på menupunktet **Gå til virksomhed** i [!INCLUDE[d365acc](includes/d365acc_md.md)]-dashboardet.</span><span class="sxs-lookup"><span data-stu-id="8948c-110">The URL that you must enter points at the client's [!INCLUDE[d365fin](includes/d365fin_md.md)], such as *https://mybusiness.financials.dynamics.com*. This URL is then used when you choose the **Go To Company** menu item in the [!INCLUDE[d365acc](includes/d365acc_md.md)] dashboard.</span></span>  

### <a name="get-invited-to-a-clients-included365finlongincludesd365finlongmdmd"></a><span data-ttu-id="8948c-111">Blive inviteret indenfor i en kundes [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="8948c-111">Get Invited to a Client's [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="8948c-112">En virksomhed, der bruger [!INCLUDE[d365fin](includes/d365fin_md.md)], kan invitere dig indenfor i [!INCLUDE[d365fin](includes/d365fin_md.md)] som deres eksterne regnskabsmedarbejder.</span><span class="sxs-lookup"><span data-stu-id="8948c-112">A company who use [!INCLUDE[d365fin](includes/d365fin_md.md)] can invite you to [!INCLUDE[d365fin](includes/d365fin_md.md)] as their external accountant.</span></span> <span data-ttu-id="8948c-113">For at blive inviteret skal du give dem den mailadresse, du bruger i forbindelse med [!INCLUDE[d365acc](includes/d365acc_md.md)], f.eks. *me@accountant.com*. Kundens administrator kan derefter føje dig til deres system ved at køre guiden **Inviter ekstern revisor**.</span><span class="sxs-lookup"><span data-stu-id="8948c-113">To get invited, you must give them the email that you use with [!INCLUDE[d365acc](includes/d365acc_md.md)], such as *me@accountant.com*. Your client's administrator can then add you to their system by running the **Invite External Accountant** wizard.</span></span>  

<span data-ttu-id="8948c-114">Derefter vil du modtage en mail fra din kunde med links til deres [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8948c-114">As a result, you will receive email from your client with links to their [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8948c-115">Det første link er en invitation til at få adgang til virksomheden – åbn linket, og acceptere trinene, der føjer dig til kundens [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8948c-115">The first link is an invitation to get access to their company - open the link and accept the steps that adds you to your client's [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8948c-116">Det andet link bruges til at føje denne kunde til dashboardet i [!INCLUDE[d365acc](includes/d365acc_md.md)], som beskrevet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="8948c-116">The second link is for adding this client to your dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)] as described above.</span></span>  

<span data-ttu-id="8948c-117">Når du har accepteret invitationen, er du logget på, og har adgang til kundens regnskabsdata fra rollecenteret **Revisor**.</span><span class="sxs-lookup"><span data-stu-id="8948c-117">When you have accepted the invitation, you are logged in and can access the client's financial data from the **Accountant** Role Center.</span></span> <span data-ttu-id="8948c-118">Du kan finde flere oplysninger i [Bogholderoplevelser i [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/financials/finance-accounting?toc=/dynamics365/accountants/toc.json).</span><span class="sxs-lookup"><span data-stu-id="8948c-118">For more information, see [Accountant Experiences in [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/financials/finance-accounting?toc=/dynamics365/accountants/toc.json).</span></span>  

## <a name="see-also"></a><span data-ttu-id="8948c-119">Se også</span><span class="sxs-lookup"><span data-stu-id="8948c-119">See Also</span></span>
<span data-ttu-id="8948c-120">[Kom i gang med [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="8948c-120">[Get Started with [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span></span>  
<span data-ttu-id="8948c-121">[Fejlfinding [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)</span><span class="sxs-lookup"><span data-stu-id="8948c-121">[Troubleshooting [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)</span></span>  

