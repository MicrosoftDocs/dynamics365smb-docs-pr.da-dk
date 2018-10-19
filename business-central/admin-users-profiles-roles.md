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
# <a name="understanding-users-profiles-and-role-centers"></a>Forstå brugere, profiler og rollecentre

I [!INCLUDE[d365fin](includes/d365fin_md.md)] tilføjes brugerne af en administrator, der giver også brugerne adgang til de områder i [!INCLUDE[d365fin](includes/d365fin_md.md)], de skal bruge i deres arbejde.  

Adgangen til funktionen styres via *brugergrupper* og *profiler*. Som administrator, kan du tilføje og fjerne brugere som en del af dit [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnement, og du kan tildele brugertilladelser gennem brugergrupper.  

## <a name="adding-users"></a>Tilføje brugere

Når du vil tilføje brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)] online, skal din virksomheds Office 365-administrator først oprette brugerne i Office 365 Administration. Du kan finde flere oplysninger under [Føje brugere til Office 365 til virksomheder](https://aka.ms/CreateOffice365Users).

Administratoren kan derefter tildele tilladelser til hver bruger og grupper af brugere. Du kan finde flere oplysninger i [Administrere brugere og rettigheder](ui-how-users-permissions.md).  

### <a name="users-of-on-premises-deployments"></a>Brugere af lokale installationer

Ved lokale installationer af [!INCLUDE[d365fin](includes/d365fin_md.md)] kan administratoren vælge mellem forskellige godkendelse af legitimationsoplysninger for brugere. Når du derefter opretter en bruger, angiver du forskellige oplysninger, afhængigt af den type legitimationsoplysninger, du bruger i den specifikke [!INCLUDE[server](includes/server.md)]-forekomst. Du kan finde flere oplysninger i [Godkendelse og typer af legitimationsoplysninger](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i sektionen Administration af udvikler- og ITPro-indholdet til [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profiler

Personer i virksomheden, der har adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)] tildeles alle en *profil*, som giver dem adgang til et *rollecenter*.

Profiler er samlinger af [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere, der deler det samme rollecenter. Et rollecenter er indgangspunktet og startsiden til [!INCLUDE[d365fin](includes/d365fin_md.md)], der giver dig hurtig adgang til dine vigtigste opgaver og viser forskellig indsigt og nøgletal (KPI'er) om dit arbejde.  

> [!NOTE]  
>  I den aktuelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] online kan du ikke tilføje, redigere eller slette profiler.  

## <a name="configuration-and-personalization"></a>Konfiguration og brugertilpasning
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
Brugene tilpasser brugergrænsefladen i deres personlige version ved at tilpasse brugergrænsefladen under deres egne brugerlogon. Denne tilpasning kan slettes af administratoren. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).  

## <a name="see-also"></a>Se også  
[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)  
[Administrere tilpasning som administrator](ui-personalization-manage.md)  
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  

