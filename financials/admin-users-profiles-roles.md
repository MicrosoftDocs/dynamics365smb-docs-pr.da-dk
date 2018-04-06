---
title: Administrere brugere og roller | Microsoft Docs
description: "Lære at administrere brugere og rollecentre i Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/02/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f8f00e7db1f7594d66e1cae5ed98271e25295472
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="b5327-103">Forstå brugere, profiler og rollecentre</span><span class="sxs-lookup"><span data-stu-id="b5327-103">Understanding Users, Profiles, and Role Centers</span></span>
<span data-ttu-id="b5327-104">Personer i virksomheden, der har adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)] tildeles alle en *profil*, som giver dem adgang til et *rollecenter*.</span><span class="sxs-lookup"><span data-stu-id="b5327-104">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span> <span data-ttu-id="b5327-105">Som administrator, kan du tildele og ændre profiler i [!INCLUDE[d365fin](includes/d365fin_md.md)], og du kan tilføje og fjerne brugere som en del af dit [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnement.</span><span class="sxs-lookup"><span data-stu-id="b5327-105">As an administrator, you can assign and change profiles in [!INCLUDE[d365fin](includes/d365fin_md.md)], and you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="b5327-106">Tilføje brugere</span><span class="sxs-lookup"><span data-stu-id="b5327-106">Adding Users</span></span>
<span data-ttu-id="b5327-107">Når du vil tilføje brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal din virksomheds Office 365-administrator først oprette brugerne i Office 365 Administration.</span><span class="sxs-lookup"><span data-stu-id="b5327-107">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)], your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="b5327-108">Du kan finde flere oplysninger i [Administrere brugere og rettigheder](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="b5327-108">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

## <a name="profiles"></a><span data-ttu-id="b5327-109">Profiler</span><span class="sxs-lookup"><span data-stu-id="b5327-109">Profiles</span></span>
<span data-ttu-id="b5327-110">Profiler er samlinger af [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere, der deler det samme rollecenter.</span><span class="sxs-lookup"><span data-stu-id="b5327-110">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="b5327-111">Et rollecenter er en sidetype, hvor du kan indsætte forskellige dele.</span><span class="sxs-lookup"><span data-stu-id="b5327-111">A Role Center is a type of page on which you can place different parts.</span></span> <span data-ttu-id="b5327-112">Hver del er en beholder, hvor du kan være vært for andre sider eller foruddefinerede systemdele, f.eks. Outlook-del eller dele, som tilføjer opgaver, notifikationer eller noter.</span><span class="sxs-lookup"><span data-stu-id="b5327-112">Each part is a container in which you can host other pages or pre-defined system parts, such as an Outlook part or parts for adding tasks, notifications, or notes.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b5327-113">I den aktuelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du ikke tilføje, redigere eller slette profiler.</span><span class="sxs-lookup"><span data-stu-id="b5327-113">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="b5327-114">Konfiguration og brugertilpasning</span><span class="sxs-lookup"><span data-stu-id="b5327-114">Configuration and Personalization</span></span>
<span data-ttu-id="b5327-115">Begrebet tilpasning af brugergrænsefladen i [!INCLUDE[d365fin](includes/d365fin_md.md)] er opdelt i to:</span><span class="sxs-lookup"><span data-stu-id="b5327-115">The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:</span></span>  

-   <span data-ttu-id="b5327-116">Konfiguration, der udføres af administratoren</span><span class="sxs-lookup"><span data-stu-id="b5327-116">Configuration, performed by the administrator</span></span>  

-   <span data-ttu-id="b5327-117">Tilpasning, som udføres af brugere</span><span class="sxs-lookup"><span data-stu-id="b5327-117">Personalization, performed by users</span></span>  

<span data-ttu-id="b5327-118">Administratoren konfigurerer brugergrænsefladen til flere brugere ved at tilpasse brugergrænsefladen for en profil, som brugerne er tildelt.</span><span class="sxs-lookup"><span data-stu-id="b5327-118">The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.</span></span>  

<span data-ttu-id="b5327-119">Brugene tilpasser brugergrænsefladen i deres personlige version ved at tilpasse brugergrænsefladen under deres egne brugerlogon.</span><span class="sxs-lookup"><span data-stu-id="b5327-119">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="b5327-120">Denne tilpasning kan slettes af administratoren.</span><span class="sxs-lookup"><span data-stu-id="b5327-120">This personalization can be deleted by the administrator.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b5327-121">Se også</span><span class="sxs-lookup"><span data-stu-id="b5327-121">See Also</span></span>  
[<span data-ttu-id="b5327-122">Administrere brugere og deres rettigheder</span><span class="sxs-lookup"><span data-stu-id="b5327-122">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
<!-- [Customize the User Interface](../customize-the-user-interface.md)   
 [Security Overview](../Security%20Overview.md)-->

