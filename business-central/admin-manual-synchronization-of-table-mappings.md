---
title: Manuel synkronisering af tabeltilknytninger | Microsoft Docs
description: Synkroniseringen kopierer data mellem Dynamics 365 for Sales-records og Business Central for at holde begge systemer opdateret.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 368bfc191aea4ae00c53d0c7ee892f3cc82c0ff7
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2019
ms.locfileid: "940062"
---
# <a name="manually-synchronize-table-mappings"></a>Synkroniser tabeltilknytninger manuelt
En integreret tabeltilknytning knytter en [!INCLUDE[d365fin](includes/d365fin_md.md)] tabel (record-type), f.eks. kunde, med en [!INCLUDE[crm_md](includes/crm_md.md)] enhed, f.eks. en konto. Synkronisering af en integreret tabeltilknytning muliggør synkronisering af data i alle records i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen [!INCLUDE[crm_md](includes/crm_md.md)]-enheden, der er sammenkædet. Afhængigt af konfigurationen af tabeltilknytningen kan synkronisering skabe og sammenkæde nye records i destinationsløsningen til records i ikke sammenkædede records i kilden.  

Manuel synkronisering af integrationstabeltilknytninger kan være nyttigt under den første indstilling af en integration, og når der diagnosticeres synkroniseringsfejl.  

Denne artikel beskrives tre metoder til manuel synkronisering af integrationstilknytningstabeller. Hver metode leverer et forskelligt synkroniseringsniveau.

## <a name="run-a-full-synchronization"></a>Kør en fuldstændig synkronisering
En fuldstændig synkronisering kører alle standardsynkroniseringsjobs til integration for synkronisering af [!INCLUDE[d365fin](includes/d365fin_md.md)]-records og [!INCLUDE[crm_md](includes/crm_md.md)]-enheder, der er angivet på siden for **Integrationstabeltilknytninger**. 

En fuldstændig synkronisering udfører følgende handlinger til [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)] records, der er:

* Ikke sammenkædet, en ny tilsvarende record vil blive oprettet og sammenkædet i den modsatte løsning.
Om der bliver oprettet en record, og hvor, den evt. oprettes, afhænger af synkroniseringsretningen. Når du f.eks. synkroniserer data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] debitorer til [!INCLUDE[crm_md](includes/crm_md.md)]-konti, oprettes en ny konto automatisk i [!INCLUDE[crm_md](includes/crm_md.md)] og sammenkædes med debitoren i [!INCLUDE[d365fin](includes/d365fin_md.md)], hvis der er en debitor, der ikke er sammenkædet med en konto. Det modsatte gælder, når synkroniseringsretningen er fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]. For hver konto, der ikke allerede er sammenkædet med en kunde, oprettes en ny tilsvarende debitor i [!INCLUDE[d365fin](includes/d365fin_md.md)] og sammenkædes med kontoen i [!INCLUDE[crm_md](includes/crm_md.md)].  

     > [!NOTE]  
     >  For at opnå dette fjerner den fuldstændige synkronisering midlertidigt valgmuligheden **Synkronisering. Kun sammenkædede records** på integrationstilknytningstabellen, der benyttes af synkroniseringsjobbet. Ved afslutningen af den fuldstændige synkroniseringsproces bliver du spurgt, om du vil bevare denne valgmulighed for alle jobs.  

* Efter sammenkædning er synkroniseringsretningen (f.eks., fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)] eller fra [!INCLUDE[crm_md](includes/crm_md.md)]til [!INCLUDE[d365fin](includes/d365fin_md.md)]) fastlagt af integrationstilknytningstabellerne. Du kan finde flere oplysninger i [Standard salgsenhedstilknytning til synkronisering](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization).  

Jobbene køres i følgende rækkefølge for at undgå sammenkædning af afhængigheder mellem enheder.  

1.  VALUTA - Dynamics 365 for Sales-synkroniseringsjob  
2.  SÆLGERE – Dynamics 365 for Sales-synkroniseringsjob  
3.  MÅLEENHED - Dynamics 365 for Sales-synkroniseringsjob  
4.  DEBITOR - Dynamics 365 for Sales-synkroniseringsjob  
5.  KONTAKTER - Dynamics 365 for Sales-synkroniseringsjob  
6.  RESSOURCE-PRODUKT - Dynamics 365 for Sales-synkroniseringsjob  
7.  VARE-PRODUKT - Dynamics 365 for Sales-synkroniseringsjob  

> [!IMPORTANT]  
>  Du benytter typisk kun fuldstændig synkronisering, når du første gang konfigurerer integration mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)], og kun én af løsningerne indeholder data, som du vil kopiere til den anden løsning. En fuldstændig synkronisering kan være nyttig i et demo-miljø. Da fuldstændig synkronisering oprettes automatisk og forbinder records mellem løsningerne, gør det hurtigere at begynde at arbejde med synkronisering af data mellem records. På den anden side bør du kun udføre en fuldstændig synkronisering, hvis du ønsker en record i [!INCLUDE[d365fin](includes/d365fin_md.md)] for hver record i [!INCLUDE[crm_md](includes/crm_md.md)] for de givne tabeltilknytninger. Ellers kan der opstå uønskede eller dobbeltoprettede records i enten [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)].  

### <a name="see-the-process-for-a-full-synchronization"></a>Se processen i forbindelse med en fuldstændig synkronisering
> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085502]

### <a name="to-run-a-full-synchronization"></a>Sådan kører du en fuldstændig synkronisering  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Microsoft Dynamics 365 for Sales Konfiguration af forbindelse,** og vælg derefter det tilhørende link.
2.  Vælg handlingen **Kør fuld synkronisering,** og derefter vælge knappen **Ja**.  
3.  Når fuld synkronisering er fuldført, kan du angive, om du vil tillade, at alle planlagte synkroniseringsjobs opretter nye records?  

    Hvis du ønsker, at alle synkroniseringsjobs opretter nye records i på destinationen for ikke sammenkædede records i kilden, skal du vælge **Ja**. Dette konfigurerer feltet **Synkroniser kun sammenkædede records** på de tabeltilknytninger, der benyttes af synkroniseringsjobs.  

    Hvis du ønsker, at synkroniseringsjobs skal køre som de gjorde inden fuld synkronisering for så vidt angår oprettelse af nye records, skal du vælge **Nej**. Dette konfigurerer feltet **Kun sammenkædede records** til den indstilling, den havde før fuld synkronisering.  

Du kan få vist resultaterne af fuld synkronisering på siden **Integrationssynkroniseringsjobs**. Du kan finde flere oplysninger under [Se status på en synkronisering](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Synkroniser alle ændrede records
Du kan benytte siden **Microsoft Dynamics 365 for Sales Forbindelseskonfiguration** for at synkronisere ændringer af data i alle integrationstabeltilknytninger. Dette er det samme som en fuld synkronisering. Det vil synkronisere data i alle sammenkædede records i [!INCLUDE[d365fin](includes/d365fin_md.md)] tabeller og [!INCLUDE[crm_md](includes/crm_md.md)] enheder, der er defineret i tabeltilknytningerne. Som standard synkroniseres kun records, der er blevet ændret siden sidste gang, de blev synkroniseret. Tabeltilknytningerne synkroniseres i følgende rækkefølge for at undgå sammenkædning af afhængigheder mellem enhederne:  

1.  VALUTA - Dynamics 365 for Sales-synkroniseringsjob  
2.  SÆLGERE – Dynamics 365 for Sales-synkroniseringsjob  
3.  MÅLEENHED - Dynamics 365 for Sales-synkroniseringsjob  
4.  DEBITOR - Dynamics 365 for Sales-synkroniseringsjob  
5.  KONTAKTER - Dynamics 365 for Sales-synkroniseringsjob  
6.  RESSOURCE-PRODUKT \- Dynamics 365 for Sales-synkroniseringsjob  
7.  VARE-PRODUKT - Dynamics 365 for Sales-synkroniseringsjob  

Du kan få vist resultaterne af den fulde synkronisering på siden **Integrationssynkroniseringsjobs**. Du kan finde flere oplysninger under [Se status på en synkronisering](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Ved at ændre integrationstabeltilknytningen på forhånd kan du konfigurere synkroniseringen med filtre til at styre, hvilke records der skal synkroniseres, eller konfigurere den til at oprette nye records i destinationsløsningen til ikke sammenkædede records i kilden. Du kan finde flere oplysninger i [Rediger tabeltilknytninger til synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-records-for-all-tables"></a>Synkroniser records for alle tabeller  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Microsoft Dynamics 365 for Sales Konfiguration af forbindelse,** og vælg derefter det tilhørende link.
2.  Vælg handlingen **Synkroniser ændrede records**, og vælg derefter **Ja**.  

## <a name="synchronize-individual-table-mappings"></a>Synkroniser individuelle tabeltilknytninger
Du kan benytte siden **Integrationstabeltilknytninger** for at køre et synkroniseringsjob på specifikke tabeltilknytninger. Det vil synkronisere data i alle sammenkædede records i [!INCLUDE[d365fin](includes/d365fin_md.md)] tabellen og [!INCLUDE[crm_md](includes/crm_md.md)] enheden, der er defineret af tabeltilknytningen. Som standard synkroniseres kun records, der er blevet ændret siden sidste gang, de blev synkroniseret.  

Ved at ændre integrationstabeltilknytningen på forhånd kan du konfigurere synkroniseringsjobbet til at oprette nye records i destinationsløsningen for ikke sammenkædede records kilden.

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Synkroniser records fra en integrationstabeltilknytning  
1.  Vælg ![elpære-ikonet, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig")-ikon, gå til **Integration af tabeltilknytning**, og vælg derefter det tilhørende link.
2.  Vælg handlingen **Synkroniser ændrede records**, og vælg derefter **Ja**.  

## <a name="see-also"></a>Se også  
[Synkronisering af Business Central og Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)   
[Konfigurere Dynamics 365 for Sales-integration i Business Central](admin-setting-up-integration-with-dynamics-sales.md)   
