---
title: Tilknytning af tabeller og felter til synkronisering | Microsoft Docs
description: Få mere at vide om, hvordan du kan tilknytte tabeller og felter til synkronisering af data mellem Business central og Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 12/18/2019
ms.author: bholtorf
ms.openlocfilehash: 371bd80c04917495ea1b35f214d10d716ed5f9ad
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943109"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Tilknytning af tabeller og felter til synkronisering
Grundlaget for synkronisering af data i [!INCLUDE[d365fin](includes/d365fin_md.md)] med data i [!INCLUDE[crm_md](includes/crm_md.md)] er at tilknytte de tabeller og felter, der indeholder dataene, til hinanden. Tilknytningen sker via integrationstabeller. 

## <a name="mapping-integration-tables"></a>Integrationstabeller til tilknytning
En integrationstabel er en tabel i databasen [!INCLUDE[d365fin](includes/d365fin_md.md)], der repræsenterer en enhed som f.eks. en konti i [!INCLUDE[crm_md](includes/crm_md.md)]. Integrationstabeller omfatter felter, der svarer til felterne i tabellen for enheden [!INCLUDE[crm_md](includes/crm_md.md)]. Integrationstabellen Konto opretter f.eks. forbindelse til objektet Konti i [!INCLUDE[crm_md](includes/crm_md.md)]. Der skal være en integrationstabel, der tilknytter hver enhed i [!INCLUDE[crm_md](includes/crm_md.md)], som du vil synkronisere med data i [!INCLUDE[d365fin](includes/d365fin_md.md)]].

Når du opretter forbindelsen mellem appsene, opretter [!INCLUDE[d365fin](includes/d365fin_md.md)] nogle standardtabel- og felttilknytninger. Hvis du vil, kan du ændre tabelknytningerne. Du kan finde flere oplysninger i [Standard salgsenhedstilknytning til synkronisering](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization). Hvis du har ændret standardtilknytningerne og vil gendanne dine ændringer, skal du på siden **Opsætning af Dynamics 365-forbindelse** vælge **Brug standardopsætning af synkronisering**.

> [!Note]
> Hvis du bruger en lokal version af [!INCLUDE[d365fin](includes/d365fin_md.md)], gemmes integrationstabellens tilknytninger i tabellen 5335 Integrationstabeltilknytninger og kan ses og redigeres fra side 5335 Integrationstabeltilknytninger. Komplekse tilknytninger og synkroniseringsregler defineres i codeunit 5341. 

### <a name="synchronization-rules"></a>Synkroniseringsregler
En integrationstabeltilknytning indeholder også regler, der styrer, hvordan integrationssynkroniseringsjob synkroniserer poster i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel og et objekt i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger under [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md#synchronization-rules). 

## <a name="mapping-integration-fields"></a>Felter til integrationstilknytning
Tilknytningstabeller er kun det første trin. Du skal også tilknytte felterne i tabellerne. Integrationsfelttilknytninger sammenkæder felter i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller med tilsvarende felter i [!INCLUDE[crm_md](includes/crm_md.md)] og bestemmer, om data skal synkroniseres i hver tabel. Den standardtabeltilknytning, som [!INCLUDE[d365fin](includes/d365fin_md.md)] giver, omfatter felttilknytninger, men du kan ændre dem, hvis du vil. Du kan finde flere oplysninger i  [Visning af enhedstilknytninger](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Hvis du bruger en lokal version af [!INCLUDE[d365fin](includes/d365fin_md.md)], defineres integrationsfelttilknytninger i tabellen 5336 Integrationsfelttilknytning.

## <a name="coupling-records"></a>Sammenkæde poster
Sammenkædning knytter poster i [!INCLUDE[crm_md](includes/crm_md.md)] til poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]. F.eks. sammenkædes [!INCLUDE[crm_md](includes/crm_md.md)]-konti typisk med kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Sammenkædning af poster giver følgende fordele:

* Den gør synkroniseringen mulig.
* Brugere kan åbne poster i én forretningsapp på den anden. Dette kræver, at [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrationsløsningen er installeret i [!INCLUDE[crm_md](includes/crm_md.md)].

Sammenkædninger kan konfigureres automatisk ved hjælp af synkroniseringsjob eller manuelt ved at redigere posten i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du finder flere oplysninger under [Synkronisering af data i [!INCLUDE[d365fin](includes/d365fin_md.md)]i [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md) og [Sammenkæd og synkroniser records manuelt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)manuelt.

## <a name="filtering-records"></a>Filtrering af records  
Hvis du ikke vil synkronisere alle records for en bestemt enhed i [!INCLUDE[crm_md](includes/crm_md.md)] eller tabel i [!INCLUDE[d365fin](includes/d365fin_md.md)], du kan indstille filtre for at begrænse antallet af records, der synkroniseres. Du indstiller filtre på siden **Integrationstilknytninger til tabeller**.  

#### <a name="to-filter-records-for-synchronization"></a>Sådan filtrerer du records til synkronisering  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Integrationstabeltilknytninger**, og vælg derefter det relaterede link.

2.  Du filtrerer [!INCLUDE[d365fin](includes/d365fin_md.md)] records ved at indstille feltet **Tabelfiltrering**.  

3.  Du filtrerer [!INCLUDE[crm_md](includes/crm_md.md)] records ved at indstille feltet **Integration af tabelfilter**.  

## <a name="creating-new-records"></a>Sådan oprettes nye records  
 Som standard synkroniseres kun records i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)], der er sammenkædet gennem integrationssynkroniseringsjob. Du kan konfigurere tabeltilknytninger, så nye records oprettes på destinationen (f.eks. [!INCLUDE[d365fin](includes/d365fin_md.md)]) for hver record i kilden (f.eks. [!INCLUDE[crm_md](includes/crm_md.md)]), der ikke allerede er sammenkædet.  

 SÆLGERE – Dynamics 365 Sales-synkroniseringsjob bruger f.eks. tabeltilknytningen SÆLGERE. Synkroniseringsjobbene kopierer data fra bruger-records i [!INCLUDE[crm_md](includes/crm_md.md)] til sælger-records i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du har konfigureret tabeltilknytningen til at oprette nye records for hver bruger i [!INCLUDE[crm_md](includes/crm_md.md)], der ikke allerede er sammenkædet med en sælger i [!INCLUDE[d365fin](includes/d365fin_md.md)], oprettes en ny sælger-record i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Sådan oprettes nye records under synkronisering  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Integrationstabeltilknytninger**, og vælg derefter det relaterede link.

2.  Fjern markeringen i feltet **Synkroniser kun sammenkædede records** i tabeltilknytningsposten på listen.  

## <a name="using-configuration-templates-on-table-mappings"></a>Brug af konfigurationsskabeloner på tabeltilknytninger
Du kan tildele konfigurationsskabeloner til tabeltilknytninger og bruge dem til nye records, der oprettes i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)]. For hver tabeltilknytning kan du angive en konfigurationsskabelon, som skal bruges til nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-records, og en anden skabelon, du vil bruge til nye [!INCLUDE[crm_md](includes/crm_md.md)]-records.  

Hvis du installerer standardsynkroniseringsopsætningen, oprettes og bruges for det meste to skabeloner automatisk i tabeltilknytningen for [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder og [!INCLUDE[crm_md](includes/crm_md.md)]-konti: **CRMCUST** og **CRMACCOUNT**.  

-   **CRMCUST** bruges til at oprette og synkronisere nye kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)], baseret på en konto i [!INCLUDE[crm_md](includes/crm_md.md)].  

     Skabelonen oprettes ved at kopiere en eksisterende konfigurationsskabelon for kunder i programmet. **CRMCUST** oprettes kun, hvis der er en eksisterende konfigurationsskabelon, og feltet **Valutakode** i skabelonen er tomt. Hvis et felt i konfigurationsskabelonen indeholder en værdi, bruges værdien i stedet for værdien i det tilknyttede felt for [!INCLUDE[crm_md](includes/crm_md.md)]-kontoen. Hvis f.eks. feltet **Land/område** på en konto i [!INCLUDE[crm_md](includes/crm_md.md)] indeholder *U.S.*, og feltet **Land/område** i konfigurationsskabelonen er *GB*, bruges *GB* som **Land/område** på den oprettede kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CRMACCOUNT** bruges til at oprette og synkronisere nye konti i [!INCLUDE[crm_md](includes/crm_md.md)], baseret på en konto i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Sådan angiver du konfigurationsskabeloner i en tabeltilknytning  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Integrationstabeltilknytninger**, og vælg derefter det relaterede link.

2.  I tabeltilknytningsposten på listen i feltet **Kode til tabelkonfigurationsskabelon**, skal du vælge den konfigurationsskabelon, der skal bruges til nye records i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Konfigurer feltet **Kode for int. tbl. konfigurationsskabelon** til den konfigurationsskabelon, der skal bruges til nye records i [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Se også  
[Om integration af Dynamics 365 Business Central med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Synkronisering af Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Planlæg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
