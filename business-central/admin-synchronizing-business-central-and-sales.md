---
title: Synkronisering og dataintegration | Microsoft Docs
description: Synkroniseringen kopierer data mellem Common Data Service-objekter og Business Central-poster og holder data i begge systemer opdateret.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 01629cb7e881de1c679d8c6925eaacc3a5639597
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196467"
---
# <a name="synchronizing-data-in-business-central-with-common-data-service"></a>Synkronisering af data i Business Central med Common Data Service
Når du integrerer [!INCLUDE[d365fin](includes/cds_long_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)], bliver du bedt om at synkronisere dataene i bestemte felter i [!INCLUDE[d365fin](includes/d365fin_md.md)]-records (f.eks. kunder, kontakter og sælgere) med tilsvarende records i [!INCLUDE[d365fin](includes/cds_long_md.md)] (f.eks. konti, kontakter og brugere). Afhængigt af record-typen kan du synkronisere data fra [!INCLUDE[d365fin](includes/cds_long_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)], eller omvendt. Du kan finde flere oplysninger under [Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkroniseringen bruger følgende elementer:

* Integrationstabeltilknytninger
* Integrationsfelttilknytninger
* Synkroniseringsregler
* Sammenkædede records

Når synkroniseringen er konfigureret, du kan sammenkæde [!INCLUDE[d365fin](includes/d365fin_md.md)]-records med [!INCLUDE[d365fin](includes/cds_long_md.md)]-records for at synkronisere deres data. Du kan starte en synkronisering manuelt eller ud fra en tidsplan. Følgende tabel indeholder i overblik over de måder, hvorpå du kan synkronisere records.  

|  Type  |  Metode  |  Skal du se  |  
|--------|----------|-------|  
|Manuel synkronisering|Synkronisering på grundlag af record efter record.<br /><br /> Du kan synkronisere individuelle records i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. en debitor, med en tilsvarende [!INCLUDE[d365fin](includes/cds_long_md.md)]-record, f.eks. en konto. Dette er typisk, hvordan brugere vil arbejde med [!INCLUDE[d365fin](includes/cds_long_md.md)]-data i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Sammenkæd og synkroniser records manuelt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronisering på grundlag af tabeltilknytning.<br /><br /> Du kan synkronisere alle records i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel med en enhed i [!INCLUDE[d365fin](includes/cds_long_md.md)]-enhed.|[Synkroniser individuelle tabeltilknytninger](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synkroniser alle ændrede records for alle tabeltilknytninger.<br /><br /> Du kan synkronisere alle de records, der er ændret i [!INCLUDE[d365fin](includes/d365fin_md.md)]- tabeller siden sidste synkronisering.|[Synkroniser alle ændrede records](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Fuld synkronisering af alle data for alle tabeltilknytninger.<br /><br /> Du kan synkronisere alle data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller og [!INCLUDE[d365fin](includes/cds_long_md.md)]-enheder, der er tilknyttet, og oprette nye records i destinationsløsningen til ikke sammenkædede records i kildeløsningen.<br /><br /> Fuld synkronisering synkroniserer alle data og ignorerer sammenkædning. Typisk udfører du en fuld synkronisering, når du konfigurerer integrationen og kun én af løsningerne indeholder data. En fuld synkronisering kan også være nyttig i et demo-miljø.|[Kør en fuld synkronisering](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Planlagt synkronisering|Synkroniser alle ændringer til data for alle tabeltilknytninger.<br /><br /> Du kan synkronisere [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[d365fin](includes/cds_long_md.md)] med planlagte intervaller ved at konfigurere jobs i jobkøen.|[Planlæg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-entity-mapping-for-synchronization"></a>Standard-objekttilknytning til synkronisering
Enheder i [!INCLUDE[d365fin](includes/cds_long_md.md)], f.eks. konti, er integreret med enheder af samme type i [!INCLUDE[d365fin](includes/d365fin_md.md)], som f.eks. kunder. For at arbejde med [!INCLUDE[d365fin](includes/cds_long_md.md)]-data, opretter du links, kaldet sammenkædninger mellem enheder i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)].

Følgende tabel viser standardtilknytningen mellem enheder i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)], som [!INCLUDE[d365fin](includes/d365fin_md.md)] leverer.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/cds_long_md.md)]|Synkroniseringsretning|Standardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Sælger/indkøber|Bruger|[!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontaktfilter: **Status** er **Nej**, **Brugerlicenseret** er **Ja** og integrationsbrugertilstand er **Nej**|
|Debitor|Konto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontofilter: **Relationstype** er **Debitor**, og **Status** er **Aktiv**.|
|Kreditor|Konto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontofilter: **Relationstype** er **Leverandør**, og **Status** er **Aktiv**.|
|Kontakt|Kontakt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-kontaktfilter: **Type** er **Person**, og kontakten er knyttet til en virksomhed. Sales-kontaktfilter: Kontakten er tildelt til en virksomhed, og den overordnede debitortype er **Konto**.|
|Valuta|Transaktionsvaluta|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |


### <a name="tip-for-admins-viewing-entity-mappings"></a>Tip til administratorer: visning af enhedstilknytninger
Du kan få vist tilknytningen mellem enhederne i [!INCLUDE[d365fin](includes/cds_long_md.md)] og tabellerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] på siden **Integrationstabeltilknytninger**, hvor du kan også anvende filtre. Du definerer tilknytningen mellem felterne i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller og felterne i [!INCLUDE[d365fin](includes/cds_long_md.md)]-enheder på siden **Integreret felttilknytning**, hvor du kan tilføje yderligere tilknytningslogik. Det kan f.eks. være nyttigt, hvis du har brug for fejlfinding i forbindelse med synkronisering.

## <a name="see-also"></a>Se også  
[Sammenkæd og synkroniser records manuelt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Planlæg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
