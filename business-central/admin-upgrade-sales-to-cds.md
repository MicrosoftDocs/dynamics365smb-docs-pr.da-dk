---
title: Opgradering af en integration med Dynamics 365 Sales | Microsoft Docs
description: Få at vide, hvordan du gør Dynamics 365 Business Central klar til integration med Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 95098397bd9554be6c993b6107963eba9a99c067
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196838"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Opgradering af en integration med Dynamics 365 Sales
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan også integreres med [!INCLUDE[d365fin](includes/cds_long_md.md)], hvilket gør det nemt at forbinde og synkronisere data med andre Dynamics 365-programmer såsom [!INCLUDE[crm_md](includes/crm_md.md)] eller endda apps, som du selv opbygger. Hvis det er første gang, du integrerer, anbefaler vi, at du gør det ved hjælp af [!INCLUDE[d365fin](includes/cds_long_md.md)]. Få flere oplysninger i [Integration med Common Data Service](admin-common-data-service.md).

Hvis du allerede har integreret [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du fortsætte med at synkronisere data ved hjælp af din installation. Men hvis du opgraderer [!INCLUDE[d365fin](includes/d365fin_md.md)] eller deaktiverer din [!INCLUDE[crm_md](includes/crm_md.md)]-integration, skal du oprette forbindelse igen via [!INCLUDE[d365fin](includes/cds_long_md.md)] for at aktivere den igen. 

> [!NOTE]
> Hvis du genopretter forbindelsen via [!INCLUDE[d365fin](includes/cds_long_md.md)], anvendes standardindstillingerne for synkroniseringen, og alle konfigurationer, du har angivet, tilsidesættes. Standard-tabeltilknytningerne anvendes for eksempel.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Sådan opgraderer du din forbindelse til at bruge Common Data Service
1. Åbn siden **Opsætning af Microsoft Dynamics 365-forbindelse**, og tryk på knappen **Aktivér** for at deaktivere din nuværende forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)].
2. Åbn siden **Opsætning af Common Data Service-forbindelse**, og tryk på knappen **Aktivér** for at aktivere forbindelsen.
3. Når du har aktiveret CDS-forbindelsen, installeres Business Central CDS-basisintegrationsløsningen til Common Data Service.
4. Tryk på knappen Aktivér på siden til opsætning af Microsoft Dynamics 365-forbindelse for at aktivere forbindelsen til [!INCLUDE[crm_md](includes/crm_md.md)].
5. Når du har aktiveret Sales-forbindelsen, installeres Business Central CDS-basisintegrationsløsningen til Sales. Dette muliggør integration med objekter, der er specifikke for [!INCLUDE[crm_md](includes/crm_md.md)], f. eks. salgsordrer, tilbud og fakturaer.
6. På siden **Opsætning af Sales-forbindelse** skal du vælge **Brug standard-synkroniseringsopsætning** for at starte integrationstabeltilknytninger for [!INCLUDE[crm_md](includes/crm_md.md)].
7. Vælg derefter **Geninstaller integrationsløsning** for at installere og konfigurere den opgraderede Business Central-integrationsløsning.

## <a name="see-also"></a>Se også
[Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integration med Common Data Service](admin-common-data-service.md)