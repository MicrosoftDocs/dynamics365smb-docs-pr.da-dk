---
title: Hent kunder ind i Dynamics 365-revisioroplevelsen | Microsoft Docs
description: Få at vide, hvordan du føjer eksisterende kunder til Accountant Hub til Dynamics 365.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/23/2018
ms.author: edupont
ms.openlocfilehash: c7f0af8d3535f558567cd40c841909cd151ce313
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1237850"
---
# <a name="add-clients-to-your-dashboard-in-include-d365acclongincludesd365acclongmdmd"></a>Tilføje kunder til dit dashboard i [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Du kan tilføje en kunde på siden **Kunde**, som du kan åbne ved at vælge handlingen **Administrer kunder** på båndet. Vælg **Ny**, og udfyld felterne.  

> [!div class="mx-imgBorder"]
> ![Tilføje en kunde](./media/accountant-add-client/manage-client.png)

Du angiver dataene i kortet for hver kunde, og du kan ændre dem efter behov. Men feltet **Kundens URL-adresse** er vigtigt – det er her, du kan få adgang til den enkelte kundes [!INCLUDE [d365fin](includes/d365fin_md.md)]. Brug handlingen **Valider kundens URL-adresse** på båndet til at kontrollere, at du har angivet det rigtige link. Den URL-adresse, du skal angive, peger på kundens [!INCLUDE [d365fin](includes/d365fin_md.md)] og omfatter deres domæneadresse. Hvis de har angivet et domæne, f.eks. MyBusiness.com, så er linket til deres [!INCLUDE [d365fin](includes/d365fin_md.md)] *https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1*.  

> [!NOTE]
>  Før opdateringen maj 2018 havde den URL-adresse, du angav, et andet format med navnet på kundens firmanavn i begyndelsen. I den aktuelle version af [!INCLUDE [d365fin](includes/d365fin_md.md)] er formatet ```https://businesscentral.dynamics.com/clientdomain?redirectedfromsignup=1```, hvor ```clientdomain``` repræsenterer kundens domæne.  

Kundens URL-adresse bruges, når du vælger menupunktet **Gå til virksomhed** i [!INCLUDE [d365acc](includes/d365acc_md.md)]-dashboardet.  

### <a name="get-invited-to-a-clients-include-d365finlongincludesd365finlongmdmd"></a>Blive inviteret indenfor i en kundes [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]
En virksomhed, der bruger [!INCLUDE [d365fin](includes/d365fin_md.md)], kan invitere dig indenfor i [!INCLUDE [d365fin](includes/d365fin_md.md)] som deres eksterne regnskabsmedarbejder. Hvis du vil inviteres, skal du give dem mailadresse, du bruger i forbindelse med [!INCLUDE [d365acc](includes/d365acc_md.md)], f.eks. <em>mig@bogholder.com</em>. Kundens administratoren kan derefter føje dig til deres system ved at køre guiden **Inviter ekstern revisor**.  

Derefter vil du modtage en mail fra din kunde med links til deres [!INCLUDE [d365fin](includes/d365fin_md.md)]. Det første link er en invitation til at få adgang til virksomheden – åbn linket, og acceptere trinene, der føjer dig til kundens [!INCLUDE [d365fin](includes/d365fin_md.md)]. Det andet link bruges til at føje denne kunde til dashboardet i [!INCLUDE [d365acc](includes/d365acc_md.md)], som beskrevet ovenfor.  

Når du har accepteret invitationen, er du logget på, og har adgang til kundens regnskabsdata fra rollecenteret **Revisor**. Du kan finde flere oplysninger i [Bogholderoplevelser i [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).  

## <a name="see-also"></a>Se også
[Kom i gang med [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Fejlfinding [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)  
