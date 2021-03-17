---
title: Opgradering af en integration med Dynamics 365 Sales
description: Få mere at vide om, hvordan du kan flytte Dynamics 365 Business Central-integrationen med Dynamics 365 Sales til den nyeste version.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 69ffe6cea05cc28d1950481a07b064a3365f404e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386695"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Opgradering af en integration med Dynamics 365 Sales
[!INCLUDE[prod_short](includes/prod_short.md)] kan integreres med [!INCLUDE[prod_short](includes/cds_long_md.md)], hvilket gør det nemt at forbinde og synkronisere data med andre Dynamics 365-programmer såsom [!INCLUDE[crm_md](includes/crm_md.md)] eller endda apps, som du selv opbygger. Hvis det er første gang, du integrerer, anbefaler vi, at du gør det ved hjælp af [!INCLUDE[prod_short](includes/cds_long_md.md)]. Få flere oplysninger i [Integration med Dataverse](admin-common-data-service.md).

Hvis du allerede har integreret [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)], kan du fortsætte med at synkronisere data ved hjælp af din installation. Men hvis du opgraderer [!INCLUDE[prod_short](includes/prod_short.md)] eller deaktiverer din [!INCLUDE[crm_md](includes/crm_md.md)]-integration, skal du oprette forbindelse igen via [!INCLUDE[prod_short](includes/cds_long_md.md)] for at aktivere den igen. 

> [!NOTE]
> Hvis du genopretter forbindelsen via [!INCLUDE[prod_short](includes/cds_long_md.md)], anvendes standardindstillingerne for synkroniseringen, og alle konfigurationer, du har angivet, tilsidesættes. Standard-tabeltilknytningerne anvendes for eksempel.

## <a name="to-upgrade-your-connection-to-use-dataverse"></a>Sådan opgraderer du din forbindelse til at bruge Dataverse
1. Åbn siden **Microsoft Dynamics 365-forbindelsesopsætning**, og tryk på knappen **Aktiveret** for at afbryde forbindelse fra [!INCLUDE[crm_md](includes/crm_md.md)].
2. Åbn siden **Dataverse-forbindelsesopsætning**, og tryk på **Aktiveret** for at aktivere forbindelsen til [!INCLUDE[prod_short](includes/cds_long_md.md)].
  
   > [!NOTE]
   > Når du har aktiveret forbindelsen, installeres Business Central-basisintegrationsløsningen til Dataverse.
3. Vælg **Geninstaller integrationsløsning** for at geninstallere og konfigurere Business Central-integrationsløsning.
4. På siden **Konfiguration af Microsoft Dynamics 365-forbindelse** skal du slå **Aktiveret** til for at genoprette forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)].
  
   > [!NOTE]
   > Når du har aktiveret forbindelsen, installeres Business Central-basisintegrationsløsningen til [!INCLUDE[prod_short](includes/prod_short.md)]. Dette muliggør integration med tabeller, der er specifikke for [!INCLUDE[crm_md](includes/crm_md.md)], f. eks. salgsordrer, tilbud og fakturaer.
5. Vælg **Geninstaller integrationsløsning** for at geninstallere og konfigurere Business Central-integrationsløsning.
6. På siden **Opsætning af Sales-forbindelse** skal du vælge **Brug standard-synkroniseringsopsætning** for at starte integrationstabeltilknytninger for [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Se også
[Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integration med Microsoft Dataverse](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]