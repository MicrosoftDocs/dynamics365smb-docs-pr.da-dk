---
title: Rediger tabeltilknytninger til synkronisering | Microsoft Docs
description: Lær, hvordan du ændrer de tilknytninger til tabeller, der bruges til synkronisering af data mellem Business Central og Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 505c1427c63a0a6f9e68980ea0ff05c93918ea60
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308066"
---
# <a name="modify-table-mappings-for-synchronization"></a>Rediger tabeltilknytninger til synkronisering
En integrationstabeltilknytning kæder en tabel i [!INCLUDE[d365fin](includes/d365fin_md.md)] sammen med en integrationstabel for [!INCLUDE[crm_md](includes/crm_md.md)] enheden. For hver enhed i [!INCLUDE[crm_md](includes/crm_md.md)] du vil synkronisere med tilsvarende data i [!INCLUDE[d365fin](includes/d365fin_md.md)]], skal der være en tilsvarende integrationstabeltilknytning. En integrationstabeltilknytning indeholder flere indstillinger, som du kan bruge til at styre, hvordan records i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel og en [!INCLUDE[crm_md](includes/crm_md.md)]-enhed synkroniseres med de tilsvarende integrationssynkroniseringsjobs.  

## <a name="filtering-records"></a>Filtrering af records  
 Hvis du ikke vil synkronisere alle records for en bestemt enhed i [!INCLUDE[crm_md](includes/crm_md.md)] eller tabel i [!INCLUDE[d365fin](includes/d365fin_md.md)], du kan indstille filtre for at begrænse antallet af records, der synkroniseres. Du indstiller filtre på siden **Integrationstilknytninger til tabeller**.  

#### <a name="to-filter-records-for-synchronization"></a>Sådan filtrerer du records til synkronisering  
1. Vælg ![elpære-ikonet, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig")-ikon, gå til **Integration af tabeltilknytning**, og vælg derefter det tilhørende link.

2.  Du filtrerer [!INCLUDE[d365fin](includes/d365fin_md.md)] records ved at indstille feltet **Tabelfiltrering**.  

3.  Du filtrerer [!INCLUDE[crm_md](includes/crm_md.md)] records ved at indstille feltet **Integration af tabelfilter**.  

## <a name="creating-new-records"></a>Sådan oprettes nye records  
 Som standard synkroniseres kun records i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)], der er sammenkædet gennem integrationssynkroniseringsjob. Du kan konfigurere tabeltilknytninger, så nye records oprettes på destinationen (f.eks. [!INCLUDE[d365fin](includes/d365fin_md.md)]) for hver record i kilden (f.eks. [!INCLUDE[crm_md](includes/crm_md.md)]), der ikke allerede er sammenkædet.  

 SÆLGERE – Dynamics 365 Sales-synkroniseringsjob bruger f.eks. tabeltilknytningen SÆLGERE. Synkroniseringsjobbene kopierer data fra bruger-records i [!INCLUDE[crm_md](includes/crm_md.md)] til sælger-records i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du har konfigureret tabeltilknytningen til at oprette nye records for hver bruger i [!INCLUDE[crm_md](includes/crm_md.md)], der ikke allerede er sammenkædet med en sælger i [!INCLUDE[d365fin](includes/d365fin_md.md)], oprettes en ny sælger-record i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Sådan oprettes nye records under synkronisering  
1. Vælg ![elpære-ikonet, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig")-ikon, gå til **Integration af tabeltilknytning**, og vælg derefter det tilhørende link.

2.  Fjern markeringen i feltet **Synkroniser kun sammenkædede records** i tabeltilknytningsposten på listen.  

## <a name="using-configuration-templates-on-table-mappings"></a>Brug af konfigurationsskabeloner på tabeltilknytninger
Du kan tildele konfigurationsskabeloner til tabeltilknytninger og bruge dem til nye records, der oprettes i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)]. For hver tabeltilknytning kan du angive en konfigurationsskabelon, som skal bruges til nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-records, og en anden skabelon, du vil bruge til nye [!INCLUDE[crm_md](includes/crm_md.md)]-records.  

Hvis du installerer standardsynkroniseringsopsætningen, oprettes og bruges for det meste to skabeloner automatisk i tabeltilknytningen for [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder og [!INCLUDE[crm_md](includes/crm_md.md)]-konti: **CRMCUST** og **CRMACCOUNT**.  

-   **CRMCUST** bruges til at oprette og synkronisere nye kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)], baseret på en konto i [!INCLUDE[crm_md](includes/crm_md.md)].  

     Skabelonen oprettes ved at kopiere en eksisterende konfigurationsskabelon for kunder i programmet. **CRMCUST** oprettes kun, hvis der er en eksisterende konfigurationsskabelon, og feltet **Valutakode** i skabelonen er tomt. Hvis et felt i konfigurationsskabelonen indeholder en værdi, bruges værdien i stedet for værdien i det tilknyttede felt for [!INCLUDE[crm_md](includes/crm_md.md)]-kontoen. Hvis f.eks. feltet **Land/område** på en konto i [!INCLUDE[crm_md](includes/crm_md.md)] indeholder *U.S.*, og feltet **Land/område** i konfigurationsskabelonen er *GB*, bruges *GB* som **Land/område** på den oprettede kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CRMACCOUNT** bruges til at oprette og synkronisere nye konti i [!INCLUDE[crm_md](includes/crm_md.md)], baseret på en konto i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Sådan angiver du konfigurationsskabeloner i en tabeltilknytning  
1. Vælg ![elpære-ikonet, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig")-ikon, gå til **Integration af tabeltilknytning**, og vælg derefter det tilhørende link.

2.  I tabeltilknytningsposten på listen i feltet **Kode til tabelkonfigurationsskabelon**, skal du vælge den konfigurationsskabelon, der skal bruges til nye records i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Konfigurer feltet **Kode for int. tbl. konfigurationsskabelon** til den konfigurationsskabelon, der skal bruges til nye records i [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Se også  
[Om integration af Dynamics 365 Business Central med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Synkronisering af Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Planlæg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
