---
title: Konfigurere brugerkonti til integration med Dynamics 365 for Sales | Microsoft Docs
description: Få at vide, hvordan du konfigurerer brugerkonti, som apps bruger til at udveksle data, og som brugere anvender til at få adgang til og synkronisere data i de pågældende apps.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: c318346c62b7776a550a77a2947173e33d5f17c0
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2019
ms.locfileid: "940060"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Konfigurere brugerkonti til integration med Dynamics 365 for Sales
Denne artikel indeholder en oversigt over opsætning af de brugerkonti, der kræves til at integrere [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-admininstrator-user-account-in-sales"></a>Konfigurere administratorbrugerkontoen i Salg
Du skal tilføje din administratorbrugerkonto for [!INCLUDE[d365fin](includes/d365fin_md.md)] som en bruger i [!INCLUDE[crm_md](includes/crm_md.md)] og derefter opgradere brugeren til administrator i [!INCLUDE[crm_md](includes/crm_md.md)]. Administratorbrugerkontoen skal også have rollen Systemtilpasser og mindst én anden ikke-administrativ brugerrolle, f.eks. Salgschef, i [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Konfigurere brugerkontoen til integrationen
Du skal oprette en dedikeret brugerkonto i dit Office 365-abonnement, som både [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] kan bruge til at synkronisere dataene. Denne brugerkonto skal kunne logge på [!INCLUDE[crm_md](includes/crm_md.md)], hvilket betyder, at brugeren skal have en licens til [!INCLUDE[crm_md](includes/crm_md.md)]. Denne konto skal også være en ikke-interaktiv konto i [!INCLUDE[crm_md](includes/crm_md.md)]. Yderligere oplysninger om oprettelse af brugere i [!INCLUDE[crm_md](includes/crm_md.md)] finder du i [Administrere sikkerhed, brugere og team](http://go.microsoft.com/fwlink/?LinkID=616518). Når forbindelsen er konfigureret, tildeler [!INCLUDE[d365fin](includes/d365fin_md.md)] brugerkontoen de sikkerhedsroller, der er brug for i [!INCLUDE[d365fin](includes/d365fin_md.md)].

![Den assisterede opsætningsvejledning viser det område, hvor der skal angives brugeroplysninger til synkronisering](media/sync-user-setup.png "Guidesiden til assisteret opsætning af visualisering viser det sted, hvor der skal angives brugeroplysninger til synkronisering")

> [!IMPORTANT]  
> Brug ikke administratorkontoen til [!INCLUDE[crm_md](includes/crm_md.md)] til synkronisering. Hvis du gør det, afbrydes synkroniseringen.
> For at undgå konstant synkronisering synkroniseres ændringer af data, der er foretaget af brugerkontoen til integration, desuden ikke. <!--What changes would this account make?--> Når der er oprettet forbindelse, anbefales det at angive adgangstilstanden til brugerkontoen til integration til ikke-interaktiv tilstand i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Oprette en ikke-interaktiv brugerkonto](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Konfigurere konti for sælgere
Du skal oprette brugerkonti i [!INCLUDE[crm_md](includes/crm_md.md)] for sælgere fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. For at gøre dette nemmere har Microsoft 365 Administration en Excel-skabelon, du kan bruge. På siden **Aktive brugere** skal du vælge **Flere** og derefter **Importér flere brugere**. Vælg **Download en CSV-fil kun med overskrifter**, og angiv derefter oplysningerne til sælgerne. Du kan få vist et eksempel ved at vælge **Download en CSV-fil med overskrifter og eksempler på brugeroplysninger**. Når du angiver oplysninger om brugerne, er næste trin i processen til import at tildele brugerlicenser til Dynamics 365 Customer Engagement-planen.  

Når du importerer brugerne og tildeler dem licenser til Dynamics 365 Customer Engagement, skal du tildele brugerne til rollen **Sælger** i [!INCLUDE[crm_md](includes/crm_md.md)].

![Sammenkædning af sælgere og brugere i Dynamics 365 for Sales](media/couple-salespeople.png "Visualisering af sammenkædning af sælgerne og brugere i Dynamics 365 for Sales")

## <a name="see-also"></a>Se også  
[Integration med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
