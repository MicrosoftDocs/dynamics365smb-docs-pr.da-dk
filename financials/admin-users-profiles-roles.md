---
title: Administrere brugere og roller | Microsoft Docs
description: "Lære at administrere brugere og rollecentre i Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e8989767618962a2db861b2df60aa03a2ca2b484
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="users-profiles-and-role-centers-in-dynamics-365-for-financials"></a><span data-ttu-id="2e72c-103">Brugere, profiler og rollecentre i Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="2e72c-103">Users, Profiles, and Role Centers in Dynamics 365 for Financials</span></span>
<span data-ttu-id="2e72c-104">Personer i virksomheden, der har adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)] tildeles alle en *profil*, som giver dem adgang til et *rollecenter*.</span><span class="sxs-lookup"><span data-stu-id="2e72c-104">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span> <span data-ttu-id="2e72c-105">Som administrator, kan du tildele og ændre profiler i [!INCLUDE[d365fin](includes/d365fin_md.md)], og du kan tilføje og fjerne brugere som en del af dit [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnement.</span><span class="sxs-lookup"><span data-stu-id="2e72c-105">As an administrator, you can assign and change profiles in [!INCLUDE[d365fin](includes/d365fin_md.md)], and you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="2e72c-106">Tilføje brugere</span><span class="sxs-lookup"><span data-stu-id="2e72c-106">Adding Users</span></span>
<span data-ttu-id="2e72c-107">Når du vil tilføje brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal din virksomheds Office 365-administrator først oprette brugerne i Office 365 Administration.</span><span class="sxs-lookup"><span data-stu-id="2e72c-107">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)], your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="2e72c-108">Du kan finde flere oplysninger i [Fremgangsmåde: Administrere brugere og rettigheder](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="2e72c-108">For more information, see [How to: Manage Users and Permissions](ui-how-users-permissions.md).</span></span>  

## <a name="profiles"></a><span data-ttu-id="2e72c-109">Profiler</span><span class="sxs-lookup"><span data-stu-id="2e72c-109">Profiles</span></span>
<span data-ttu-id="2e72c-110">Profiler er samlinger af [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere, der deler det samme rollecenter.</span><span class="sxs-lookup"><span data-stu-id="2e72c-110">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="2e72c-111">Et rollecenter er en sidetype, hvor du kan indsætte forskellige dele.</span><span class="sxs-lookup"><span data-stu-id="2e72c-111">A Role Center is a type of page on which you can place different parts.</span></span> <span data-ttu-id="2e72c-112">Hver del er en beholder, hvor du kan være vært for andre sider eller foruddefinerede systemdele, f.eks. Outlook-del eller dele, som tilføjer opgaver, notifikationer eller noter.</span><span class="sxs-lookup"><span data-stu-id="2e72c-112">Each part is a container in which you can host other pages or pre-defined system parts, such as an Outlook part or parts for adding tasks, notifications, or notes.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2e72c-113">I den aktuelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du ikke tilføje, redigere eller slette profiler.</span><span class="sxs-lookup"><span data-stu-id="2e72c-113">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="2e72c-114">Konfiguration og brugertilpasning</span><span class="sxs-lookup"><span data-stu-id="2e72c-114">Configuration and Personalization</span></span>
<span data-ttu-id="2e72c-115">Begrebet tilpasning af brugergrænsefladen i [!INCLUDE[d365fin](includes/d365fin_md.md)] er opdelt i to:</span><span class="sxs-lookup"><span data-stu-id="2e72c-115">The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:</span></span>  

-   <span data-ttu-id="2e72c-116">Konfiguration, der udføres af administratoren</span><span class="sxs-lookup"><span data-stu-id="2e72c-116">Configuration, performed by the administrator</span></span>  

-   <span data-ttu-id="2e72c-117">Tilpasning, som udføres af brugere</span><span class="sxs-lookup"><span data-stu-id="2e72c-117">Personalization, performed by users</span></span>  

<span data-ttu-id="2e72c-118">Administratoren konfigurerer brugergrænsefladen til flere brugere ved at tilpasse brugergrænsefladen for en profil, som brugerne er tildelt.</span><span class="sxs-lookup"><span data-stu-id="2e72c-118">The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.</span></span>  

<span data-ttu-id="2e72c-119">Brugene tilpasser brugergrænsefladen i deres personlige version ved at tilpasse brugergrænsefladen under deres egne brugerlogon.</span><span class="sxs-lookup"><span data-stu-id="2e72c-119">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="2e72c-120">Denne tilpasning kan slettes af administratoren.</span><span class="sxs-lookup"><span data-stu-id="2e72c-120">This personalization can be deleted by the administrator.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2e72c-121">Se også</span><span class="sxs-lookup"><span data-stu-id="2e72c-121">See Also</span></span>  
[<span data-ttu-id="2e72c-122">Fremgangsmåde: Administrere brugere og rettigheder</span><span class="sxs-lookup"><span data-stu-id="2e72c-122">How to: Manage Users and Permissions</span></span>](ui-how-users-permissions.md)  
<!-- [Customize the User Interface](../customize-the-user-interface.md)   
 [Security Overview](../Security%20Overview.md)-->

