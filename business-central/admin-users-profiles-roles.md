---
title: Administrere brugere og roller | Microsoft Docs
description: "Lære at administrere brugere og rollecentre i Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="b03d3-103">Forstå brugere, profiler og rollecentre</span><span class="sxs-lookup"><span data-stu-id="b03d3-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="b03d3-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)] tilføjes brugerne af en administrator, der giver også brugerne adgang til de områder i [!INCLUDE[d365fin](includes/d365fin_md.md)], de skal bruge i deres arbejde.</span><span class="sxs-lookup"><span data-stu-id="b03d3-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="b03d3-105">Adgangen til funktionen styres via *brugergrupper* og *profiler*.</span><span class="sxs-lookup"><span data-stu-id="b03d3-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="b03d3-106">Som administrator, kan du tilføje og fjerne brugere som en del af dit [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnement, og du kan tildele brugertilladelser gennem brugergrupper.</span><span class="sxs-lookup"><span data-stu-id="b03d3-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="b03d3-107">Tilføje brugere</span><span class="sxs-lookup"><span data-stu-id="b03d3-107">Adding Users</span></span>

<span data-ttu-id="b03d3-108">Når du vil tilføje brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)] online, skal din virksomheds Office 365-administrator først oprette brugerne i Office 365 Administration.</span><span class="sxs-lookup"><span data-stu-id="b03d3-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="b03d3-109">Du kan finde flere oplysninger under [Føje brugere til Office 365 til virksomheder](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="b03d3-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="b03d3-110">Administratoren kan derefter tildele tilladelser til hver bruger og grupper af brugere.</span><span class="sxs-lookup"><span data-stu-id="b03d3-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="b03d3-111">Du kan finde flere oplysninger i [Administrere brugere og rettigheder](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="b03d3-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="b03d3-112">Brugere af lokale installationer</span><span class="sxs-lookup"><span data-stu-id="b03d3-112">Users of on-premises deployments</span></span>

<span data-ttu-id="b03d3-113">Ved lokale installationer af [!INCLUDE[d365fin](includes/d365fin_md.md)] kan administratoren vælge mellem forskellige godkendelse af legitimationsoplysninger for brugere.</span><span class="sxs-lookup"><span data-stu-id="b03d3-113">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="b03d3-114">Når du derefter opretter en bruger, angiver du forskellige oplysninger, afhængigt af den type legitimationsoplysninger, du bruger i den specifikke [!INCLUDE[server](includes/server.md)]-forekomst.</span><span class="sxs-lookup"><span data-stu-id="b03d3-114">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="b03d3-115">Du kan finde flere oplysninger i [Godkendelse og typer af legitimationsoplysninger](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i sektionen Administration af udvikler- og ITPro-indholdet til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b03d3-115">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="b03d3-116">Profiler</span><span class="sxs-lookup"><span data-stu-id="b03d3-116">Profiles</span></span>

<span data-ttu-id="b03d3-117">Personer i virksomheden, der har adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)] tildeles alle en *profil*, som giver dem adgang til et *rollecenter*.</span><span class="sxs-lookup"><span data-stu-id="b03d3-117">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="b03d3-118">Profiler er samlinger af [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere, der deler det samme rollecenter.</span><span class="sxs-lookup"><span data-stu-id="b03d3-118">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="b03d3-119">Et rollecenter er indgangspunktet og startsiden til [!INCLUDE[d365fin](includes/d365fin_md.md)], der giver dig hurtig adgang til dine vigtigste opgaver og viser forskellig indsigt og nøgletal (KPI'er) om dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="b03d3-119">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b03d3-120">I den aktuelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] online kan du ikke tilføje, redigere eller slette profiler.</span><span class="sxs-lookup"><span data-stu-id="b03d3-120">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="b03d3-121">Konfiguration og brugertilpasning</span><span class="sxs-lookup"><span data-stu-id="b03d3-121">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
<span data-ttu-id="b03d3-122">Brugene tilpasser brugergrænsefladen i deres personlige version ved at tilpasse brugergrænsefladen under deres egne brugerlogon.</span><span class="sxs-lookup"><span data-stu-id="b03d3-122">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="b03d3-123">Denne tilpasning kan slettes af administratoren.</span><span class="sxs-lookup"><span data-stu-id="b03d3-123">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="b03d3-124">Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="b03d3-124">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="b03d3-125">Se også</span><span class="sxs-lookup"><span data-stu-id="b03d3-125">See Also</span></span>  
[<span data-ttu-id="b03d3-126">Administrere brugere og deres rettigheder</span><span class="sxs-lookup"><span data-stu-id="b03d3-126">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="b03d3-127">Administrere tilpasning som administrator</span><span class="sxs-lookup"><span data-stu-id="b03d3-127">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="b03d3-128">Tilpasse dit arbejdsområde</span><span class="sxs-lookup"><span data-stu-id="b03d3-128">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

