---
title: Synkronisering og dataintegration | Microsoft Docs
description: Synkroniseringen kopierer data mellem Dynamics 365 for Sales-poster og Business Central-records og holder data i begge systemer opdateret.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: a2adf188f616f3a9cbb0e0d3135ee79d238c453b
ms.sourcegitcommit: 92c7b6c5f0a5d8becbef106ab85258906765bc3e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540219"
---
# <a name="synchronizing-data-in-business-central-and-dynamics-365-for-sales"></a>Synkronisering af data i Business Central og Dynamics 365 for Sales
Når du integrerer [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)], bliver du bedt om at synkronisere dataene i bestemte felter i [!INCLUDE[d365fin](includes/d365fin_md.md)]-records (f.eks. kunder, kontakter og sælgere) med tilsvarende records i [!INCLUDE[d365fin](includes/d365fin_md.md)] (f.eks. konti, kontakter og brugere). Afhængigt af record-typen kan du synkronisere data fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)], eller omvendt. Du kan finde flere oplysninger under [Integration med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkroniseringen bruger følgende elementer:

* Integrationstabeltilknytninger
* Integrationsfelttilknytninger
* Synkroniseringsregler
* Sammenkædede records

Når synkroniseringen er konfigureret, du kan sammenkæde [!INCLUDE[d365fin](includes/d365fin_md.md)]-records med [!INCLUDE[crm_md](includes/crm_md.md)]-records for at synkronisere deres data. Du kan starte en synkronisering manuelt eller ud fra en tidsplan. Følgende tabel indeholder i overblik over de måder, hvorpå du kan synkronisere records.  

|  Type  |  Metode  |  Skal du se  |  
|--------|----------|-------|  
|Manuel synkronisering|Synkronisering på grundlag af record efter record.<br /><br /> Du kan synkronisere individuelle records i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. en debitor, med en tilsvarende [!INCLUDE[crm_md](includes/crm_md.md)]-record, f.eks. en konto. Dette er typisk, hvordan brugere vil arbejde med [!INCLUDE[crm_md](includes/crm_md.md)]-data i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Sammenkæd og synkroniser records manuelt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronisering på grundlag af tabeltilknytning.<br /><br /> Du kan synkronisere alle records i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel med en enhed i [!INCLUDE[crm_md](includes/crm_md.md)]-enhed.|[Synkroniser individuelle tabeltilknytninger](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synkroniser alle ændrede records for alle tabeltilknytninger.<br /><br /> Du kan synkronisere alle de records, der er ændret i [!INCLUDE[d365fin](includes/d365fin_md.md)]- tabeller siden sidste synkronisering.|[Synkroniser alle ændrede records](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Fuld synkronisering af alle data for alle tabeltilknytninger.<br /><br /> Du kan synkronisere alle data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller og [!INCLUDE[crm_md](includes/crm_md.md)]-enheder, der er tilknyttet, og oprette nye records i destinationsløsningen til ikke sammenkædede records i kildeløsningen.<br /><br /> Fuld synkronisering synkroniserer alle data og ignorerer sammenkædning. Typisk udfører du en fuld synkronisering, når du konfigurerer integrationen og kun én af løsningerne indeholder data. En fuld synkronisering kan også være nyttig i et demo-miljø.|[Kør en fuld synkronisering](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Planlagt synkronisering|Synkroniser alle ændringer til data for alle tabeltilknytninger.<br /><br /> Du kan synkronisere [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] med planlagte intervaller ved at konfigurere jobs i jobkøen.|[Planlæg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Standardenhedstilknytning i Sales til synkronisering
Enheder i [!INCLUDE[crm_md](includes/crm_md.md)], f.eks. konti, er integreret med enheder af samme type i [!INCLUDE[d365fin](includes/d365fin_md.md)], som f.eks. kunder. For at arbejde med [!INCLUDE[crm_md](includes/crm_md.md)]-data, opretter du links, kaldet sammenkædninger mellem enheder i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].

Følgende tabel viser standardtilknytningen mellem enheder i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)], som [!INCLUDE[d365fin](includes/d365fin_md.md)] leverer.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[crm_md](includes/crm_md.md)]|Synkroniseringsretning|Standardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Sælger/indkøber|Bruger|[!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontaktfilter: **Status** er **Nej**, **Brugerlicenseret** er **Ja** og integrationsbrugertilstand er **Nej**|
|Debitor|Konto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontofilter: **Relationstype** er **Debitor**, og **Status** er **Aktiv**.|
|Kontakt|Kontakt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-kontaktfilter: **Type** er **Person**, og kontakten er knyttet til en virksomhed. Sales-kontaktfilter: Kontakten er tildelt til en virksomhed, og den overordnede debitortype er **Konto**.|
|Valuta|Transaktionsvaluta|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Enhe.|Enhedsgruppe|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Vare|Produkt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontaktfilter: **Produkttype** er **Salg lager**|
|Ressource|Produkt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontaktfilter: **Produkttype** er **Tjenester**|
|Debitorprisgruppe|Prisliste|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Salgspris|Produktprisliste|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-kontaktfilter: **Salgskode** er ikke tom, **Salgstype** er **Debitorprisgruppe**|
|Salgsmulighed|Salgsmulighed|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |
|Salgsfakturahoved|Faktura|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Salgsfakturalinje|Fakturaprodukt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Salgsordrehovedet|Salgsordre|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] Filter for salgshoved: **Dokumenttype** er Ordre, **Status** er Frigivet|
|Bemærkninger til salgsordre|Bemærkninger til salgsordre|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |

### <a name="tip-for-admins-viewing-entity-mappings"></a>Tip til administratorer: visning af enhedstilknytninger
Du kan få vist tilknytningen mellem enhederne i [!INCLUDE[crm_md](includes/crm_md.md)] og tabellerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] på siden **Integrationstabeltilknytninger**, hvor du kan også anvende filtre. Du definerer tilknytningen mellem felterne i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller og felterne i [!INCLUDE[crm_md](includes/crm_md.md)]-enheder på siden **Integreret felttilknytning**, hvor du kan tilføje yderligere tilknytningslogik. Det kan f.eks. være nyttigt, hvis du har brug for fejlfinding i forbindelse med synkronisering.

### <a name="tip-for-developers-mapping-fields-in-business-central-to-the-option-sets-in-sales"></a>Tip til udviklere: Tilknytning af felter i Business Central til Indstillingsgrupper i Salg
Hvis du er udvikler, og du vil tilføje valgmuligheder til indstillingsgrupperne i [!INCLUDE[crm_md](includes/crm_md.md)], skal du vide dette. Tre tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] er tilknyttet til **Konto**-enhedens indstillingsfelter i [!INCLUDE[crm_md](includes/crm_md.md)]. Records i de tabeller, der ikke er knyttet til indstillinger i [!INCLUDE[crm_md](includes/crm_md.md)], synkroniseres ikke. Dette betyder, at feltet **Indstilling** er tomt i [!INCLUDE[crm_md](includes/crm_md.md)].

Følgende tabel viser tilknytninger fra [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller til feltet **Indstilling** i enheden **Konto** i [!INCLUDE[crm_md](includes/crm_md.md)]

|Sortbord|Indstillingsfelt i kontoenheden|
|----------------------|-------------------------------------------|
|Betalingsbetingelser|Betalingsbetingelser|
|Leveringsform|Adresse 1: Fragtbetingelser|
|Speditør|Adresse 1: Forsendelsesmetode|

### <a name="synchronization-rules"></a>Synkroniseringsregler
I følgende tabel beskrives de regler, der styrer synkroniseringen mellem programmerne,

> [!NOTE]  
> Ændringer af data i [!INCLUDE[crm_md](includes/crm_md.md)], der blev foretaget af [!INCLUDE[crm_md](includes/crm_md.md)]-forbindelsesbrugerkontoen synkroniseres ikke. Derfor anbefales det, at du ikke ændrer data, når du benytter denne konto. Du kan finde flere oplysninger under [Konfiguration af integration med Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Sortbord|Regel|
|-----|----|
|Kunder (Debitorer)|Før du kan synkronisere en debitor med en konto, skal den sælger, der er tildelt debitoren, være sammenkædet med en bruger i [!INCLUDE[crm_md](includes/crm_md.md)]. Når du derfor kører KUNDER – Dynamics 365 for Sales-synkroniseringsjobbet, og du konfigurerer det til at oprette nye records, skal du sørge for at synkronisere sælgere med [!INCLUDE[crm_md](includes/crm_md.md)]-brugere, før du synkroniserer debitorer med konti [!INCLUDE[crm_md](includes/crm_md.md)]. <br /> <br />KUNDER – Dynamics 365 for Sales-synkroniseringsjobbet synkroniserer kun Sales-konti, der har relationstypen Debitor.|
|Kontakter|Kun kontakter i [!INCLUDE[crm_md](includes/crm_md.md)], der er knyttet til en konto, oprettes i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Værdien Sælgerkode definerer ejeren af det sammenkædede enhed i [!INCLUDE[crm_md](includes/crm_md.md)].|
|Valutaer|Valutaer sammenkædes med transaktionsvalutaer i [!INCLUDE[crm_md](includes/crm_md.md)], baseret på ISO-koder. Kun valutaer, der har en ISO-standardkoder, sammenkædes og synkroniseres med transaktionsvalutaer.|
|Enheder|Måleenheder synkroniseres med enhedsgrupper i [!INCLUDE[crm_md](includes/crm_md.md)]. Der kan kun være én måleenhed defineret i enhedsgruppen.|
|Varer|Når du synkroniserer varer med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter, opretter [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk en prisliste i [!INCLUDE[crm_md](includes/crm_md.md)]. For at undgå synkroniseringsfejl bør du ikke ændre denne prisliste manuelt.|
|Sælgere|Sælgere er sammenkædet med systembrugere i [!INCLUDE[crm_md](includes/crm_md.md)]. Brugeren skal være aktiveret og licenseret og må ikke være integrationsbrugeren. Bemærk, at dette er den første tabel, der skal synkroniseres, fordi den bruges i kunder, kontakter, salgsmuligheder og salgsfakturaer.|
|Ressourcer|Ressourcer synkroniseres med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter, har produkttypen Service.|
|Debitorprisgrupper|Debitorprisgrupper synkroniseres med prislister i Sales.|
|Salgspriser|Priser i Sales, der har salgstypen Debitorprisgruppe og har en salgskode defineret, synkroniseres med [!INCLUDE[crm_md](includes/crm_md.md)]-prislistelinjer|
|Salgsmuligheder|Salgsmuligheder synkroniseres med [!INCLUDE[crm_md](includes/crm_md.md)]-salgsmuligheder. Værdien Sælgerkode definerer ejeren af det sammenkædede enhed i [!INCLUDE[crm_md](includes/crm_md.md)].|
|Bogførte salgsfakturaer|Bogførte salgsfakturaer synkroniseres med salgsfakturaer. Før en faktura kan synkroniseres, er det bedre at synkronisere alle andre enheder, der kan indgå i fakturaen, fra sælgere til prislister. Værdien Sælgerkode i fakturahovedet definerer ejeren af det sammenkoblede objekt i Sales.|
|Salgsordrer|Frigivet salgsordre (hoveder) synkroniseres med salgsordre. Før en ordre kan synkroniseres, er det bedre at synkronisere alle andre enheder, der kan indgå i ordren, fra sælgere til prislister. Værdien Sælgerkode i ordrehovedet definerer ejeren af den sammenkædede enhed i Sales.|  

## <a name="see-also"></a>Se også  
[Sammenkæd og synkroniser records manuelt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Planlæg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integration med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
