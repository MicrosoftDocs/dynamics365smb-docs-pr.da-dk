---
title: Manuel synkronisering af tabeltilknytninger | Microsoft Docs
description: Synkroniseringen kopierer data mellem Microsoft Dataverse-tabeller og Business Central for at holde begge systemer opdateret.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: e9cd03df1e26eca92f5a69d02d73caac902d2b6b
ms.sourcegitcommit: 1508643075dafc25e9c52810a584b8df1d14b1dc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/28/2022
ms.locfileid: "8049558"
---
# <a name="manually-synchronize-table-mappings"></a>Synkroniser tabeltilknytninger manuelt


En integreret tabeltilknytning knytter en [!INCLUDE[prod_short](includes/prod_short.md)] tabel (record-type), f.eks. kunde, med en [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabel, f.eks. en konto. Synkronisering af en integreret tabeltilknytning muliggør synkronisering af data i alle records i [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabellen, der er sammenkædet. Afhængigt af konfigurationen af tabeltilknytningen kan synkronisering skabe og sammenkæde nye records i destinationsløsningen til records i ikke sammenkædede records i kilden.  

Manuel synkronisering af integrationstabeltilknytninger kan være nyttigt under den første indstilling af en integration, og når der diagnosticeres synkroniseringsfejl.  

Denne artikel beskrives tre metoder til manuel synkronisering af integrationstilknytningstabeller. Hver metode leverer et forskelligt synkroniseringsniveau.

## <a name="run-a-full-synchronization"></a>Kør en fuldstændig synkronisering
En fuldstændig synkronisering kører alle standardsynkroniseringsjobs til integration for synkronisering af [!INCLUDE[prod_short](includes/prod_short.md)]-records og [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabeller, der er angivet på siden for **Integrationstabeltilknytninger**. 

En fuldstændig synkronisering udfører følgende handlinger til [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[prod_short](includes/cds_long_md.md)] records, der er:

* Ikke sammenkædet, en ny tilsvarende række vil blive oprettet og sammenkædet i den modsatte løsning.
Om der bliver oprettet en række, og hvor, den evt. oprettes, afhænger af synkroniseringsretningen. Når du f.eks. synkroniserer data fra [!INCLUDE[prod_short](includes/prod_short.md)] debitorer til [!INCLUDE[prod_short](includes/cds_long_md.md)]-konti, oprettes en ny konto automatisk i [!INCLUDE[prod_short](includes/cds_long_md.md)] og sammenkædes med debitoren i [!INCLUDE[prod_short](includes/prod_short.md)], hvis der er en debitor, der ikke er sammenkædet med en konto. Det modsatte gælder, når synkroniseringsretningen er fra [!INCLUDE[prod_short](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)]. For hver konto, der ikke allerede er sammenkædet med en kunde, oprettes en ny tilsvarende debitor i [!INCLUDE[prod_short](includes/prod_short.md)] og sammenkædes med kontoen i [!INCLUDE[prod_short](includes/cds_long_md.md)].  

     > [!NOTE]  
     >  For at opnå dette fjerner den fuldstændige synkronisering midlertidigt valgmuligheden **Synkronisering. Kun sammenkædede records** på integrationstilknytningstabellen, der benyttes af synkroniseringsjobbet. Ved afslutningen af den fuldstændige synkroniseringsproces bliver du spurgt, om du vil bevare denne valgmulighed for alle jobs.  

* Efter sammenkædning er synkroniseringsretningen (f.eks., fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[prod_short](includes/cds_long_md.md)] eller fra [!INCLUDE[prod_short](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)]) fastlagt af integrationstilknytningstabellerne. Få flere oplysninger i [Standard-tabeltilknytning til synkronisering](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).  

> [!IMPORTANT]  
>  Du benytter typisk kun fuldstændig synkronisering, når du første gang konfigurerer integration mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)], og kun én af løsningerne indeholder data, som du vil kopiere til den anden løsning. En fuldstændig synkronisering kan være nyttig i et demo-miljø. Da fuldstændig synkronisering oprettes automatisk og forbinder records mellem løsningerne, gør det hurtigere at begynde at arbejde med synkronisering af data mellem records. På den anden side bør du kun udføre en fuldstændig synkronisering, hvis du ønsker en række i [!INCLUDE[prod_short](includes/prod_short.md)] for hver række i [!INCLUDE[prod_short](includes/cds_long_md.md)] for de givne tabeltilknytninger. Ellers kan der opstå uønskede eller dobbeltoprettede records i enten [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[prod_short](includes/cds_long_md.md)].  

### <a name="to-run-a-full-synchronization"></a>Sådan kører du en fuldstændig synkronisering  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Dataverse-forbindelseskonfiguration**, og vælg derefter det relaterede link.

    > [!NOTE]
    > Hvis du vil køre en komplet synkronisering for tabeller via Dynamics 365 Sales, skal du bruge siden **Opsætning af Microsoft Dynamics 365 Sales-forbindelse** i stedet.

2.  Vælg handlingen **Kør fuld synkronisering,** og derefter vælge knappen **Ja**.  
3.  Når fuld synkronisering er fuldført, kan du angive, om du vil tillade, at alle planlagte synkroniseringsjobs opretter nye records?  

    Hvis du ønsker, at alle synkroniseringsjobs opretter nye records i på destinationen for ikke sammenkædede records i kilden, skal du vælge **Ja**. Dette konfigurerer feltet **Synkroniser kun sammenkædede records** på de tabeltilknytninger, der benyttes af synkroniseringsjobs.  

    Hvis du ønsker, at synkroniseringsjobs skal køre som de gjorde inden fuld synkronisering for så vidt angår oprettelse af nye records, skal du vælge **Nej**. Dette konfigurerer feltet **Kun sammenkædede records** til den indstilling, den havde før fuld synkronisering.  

Du kan få vist resultaterne af fuld synkronisering på siden **Integrationssynkroniseringsjobs**. Du kan finde flere oplysninger i [Se status på en synkronisering](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Synkroniser alle ændrede records
Du kan benytte siden **Common Data Service Forbindelseskonfiguration** for at synkronisere ændringer af data i alle integrationstabeltilknytninger. Dette er det samme som en fuld synkronisering. Det vil synkronisere data i alle sammenkædede records i [!INCLUDE[prod_short](includes/prod_short.md)] tabeller og [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabeller, der er defineret i tabeltilknytningerne. Som standard synkroniseres kun data, der er blevet ændret siden sidste gang, de blev synkroniseret. Synkroniseringsjob synkroniserer tabeltilknytninger i denne rækkefølge for at undgå sammenkædning af afhængigheder mellem tabellerne:  

1.  VALUTA  
2.  SÆLGERE  
3.  KREDITOR  
4.  KUNDE  
5.  KONTAKTER  

Du kan få vist resultaterne af den fulde synkronisering på siden **Integrationssynkroniseringsjobs**. Du kan finde flere oplysninger i [Se status på en synkronisering](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Ved at ændre integrationstabeltilknytningen på forhånd kan du oprette filtre, der skal styre de data, der skal synkroniseres, eller konfigurere tilknytninger for at oprette data i destinationsløsningen til ikke sammenkædede rækker i kilden. Du kan finde flere oplysninger i [Rediger tabeltilknytninger til synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-data-for-all-tables"></a>Synkroniser data for alle tabeller  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Microsoft Dynamics 365 Sales-forbindelseskonfiguration**, og vælg derefter det relaterede link.
2.  Vælg handlingen **Synkroniser ændrede records**, og vælg derefter **Ja**.  

## <a name="synchronize-individual-table-mappings"></a>Synkroniser individuelle tabeltilknytninger
Du kan benytte siden **Integrationstabeltilknytninger** for at køre et synkroniseringsjob på specifikke tabeltilknytninger. Det vil synkronisere data for alle sammenkædede records og rækker i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabellerne, der er defineret af tabeltilknytningen. Som standard synkroniseres kun data, der er blevet ændret siden sidste gang, de blev synkroniseret.  

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Synkroniser records fra en integrationstabeltilknytning  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Vælg ikonet , åbn **Integrationstabeltilknytninger**, og vælg derefter det relaterede link.
2.  Vælg handlingen **Synkroniser ændrede records**, og vælg derefter **Ja**.  

## <a name="see-also"></a>Se også  
[Synkronisering af Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Opsætning af brugerkonti til integration med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]