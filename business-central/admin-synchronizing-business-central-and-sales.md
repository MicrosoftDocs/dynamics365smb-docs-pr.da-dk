---
title: Synkronisering og dataintegration
description: Synkroniseringen kopierer data mellem Microsoft Dataverse-tabeller og Business Central-poster og holder data i begge systemer opdateret.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 05/07/2024
ms.custom: bap-template
ms.search.keywords: 'Dataverse, integration, sync, synchronize, mapping'
ms.saerch.form: 5372_Primary
ms.service: dynamics-365-business-central
---

# Synkronisering af data i Business Central med Microsoft Dataverse

Når du integrerer [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)], bliver du bedt om at synkronisere dataene i bestemte felter i [!INCLUDE[prod_short](includes/prod_short.md)]-records (f.eks. kunder, kontakter og sælgere) med tilsvarende rækker i [!INCLUDE[prod_short](includes/cds_long_md.md)] (f.eks. konti, kontakter og brugere). Afhængigt af række-typen kan du synkronisere data fra [!INCLUDE[prod_short](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)], eller omvendt. Du kan finde flere oplysninger i [Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkroniseringen bruger følgende elementer:

* Integrationstabeltilknytninger
* Integrationsfelttilknytninger
* Synkroniseringsregler
* Sammenkædede records

Når synkroniseringen er konfigureret, du kan sammenkæde [!INCLUDE[prod_short](includes/prod_short.md)]-records med [!INCLUDE[prod_short](includes/cds_long_md.md)]-rækker for at synkronisere deres data. Du kan starte en synkronisering manuelt eller ud fra en tidsplan. Følgende tabel indeholder et overblik over metoder til synkronisering.  

|  Type  |  Metode  |  Skal du se  |  
|--------|----------|-------|  
|Manuel synkronisering|Synkronisering på grundlag af række efter række.<br /><br /> Du kan synkronisere individuelle poster i [!INCLUDE[prod_short](includes/prod_short.md)], f.eks. en debitor, med en tilsvarende [!INCLUDE[prod_short](includes/cds_long_md.md)]-række, f.eks. en konto. Dette er typisk, hvordan brugere vil arbejde med [!INCLUDE[prod_short](includes/cds_long_md.md)]-data i [!INCLUDE[prod_short](includes/prod_short.md)].|[Sammenkæde og synkronisere poster manuelt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronisering på grundlag af tabeltilknytning.<br /><br /> Du kan synkronisere alle records i en [!INCLUDE[prod_short](includes/prod_short.md)]-tabel med en tabel [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabel.|[Synkroniser individuelle tabeltilknytninger](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synkroniser alle ændrede records for alle tabeltilknytninger.<br /><br /> Du kan synkronisere alle de records, der er ændret i [!INCLUDE[prod_short](includes/prod_short.md)]- tabeller siden sidste synkronisering.|[Synkroniser alle ændrede records](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Fuld synkronisering af alle data for alle tabeltilknytninger.<br /><br /> Du kan synkronisere alle data i [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller og [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabeller, der er tilknyttet, og oprette nye records eller rækker i destinationsløsningen til ikke sammenkædede records i kildeløsningen.<br /><br /> Fuld synkronisering synkroniserer alle data og ignorerer sammenkædning. Typisk udfører du en fuld synkronisering, når du konfigurerer integrationen og kun én af løsningerne indeholder data. En fuld synkronisering kan også være nyttig i et demo-miljø.|[Kør en fuld synkronisering](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Planlagt synkronisering|Synkroniser alle ændringer til data for alle tabeltilknytninger.<br /><br /> Du kan synkronisere [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)] med planlagte intervaller ved at konfigurere jobs i jobkøen.|[Planlæg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

> [!NOTE]
> Synkroniseringen mellem [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] er baseret på den planlagte kørsel af opgavekøposter og garanterer ikke data konsistens i realtid mellem to tjenester. I forbindelse med realtidsdata conistency du lære om [Virtuelle Business Central-tabeller](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-overview) eller Business Central API'er.   

## Standard-tabeltilknytning til synkronisering

Tabeller i [!INCLUDE[prod_short](includes/cds_long_md.md)], f.eks. konti, er integreret med tabeller af samme type i [!INCLUDE[prod_short](includes/prod_short.md)], som f.eks. kunder. For at arbejde med [!INCLUDE[prod_short](includes/cds_long_md.md)]-data, opretter du links, kaldet sammenkædninger mellem tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)].

Følgende tabel viser standardtilknytningen mellem tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)].

> [!TIP]
> Du kan nulstille konfigurationsændringer, der er foretaget af integrations tabel-og felttilknytninger, til standardindstillingerne ved at vælge tilknytningerne og derefter vælge **Brug standardopsætning for synkronisering**.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Synkroniseringsretning | Standardfilter |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Sælger/indkøber | Bruger | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontaktfilter: **Status** er **Nej**, **Brugerlicenseret** er **Ja** og integrationsbrugertilstand er **Nej** |
| Debitor | Konto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontofilter: **Relationstype** er **Debitor**, og **Status** er **Aktiv**. [!INCLUDE[prod_short](includes/prod_short.md)]-filter: **Spærret** er tomt (debitor er ikke spærret). |
| Kreditor | Konto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontofilter: **Relationstype** er **Kreditor**, og **Status** er **Aktiv**. [!INCLUDE[prod_short](includes/prod_short.md)]-filter: **Spærret** er tomt (kreditor er ikke spærret). |
| Kontakt | Kontakt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/prod_short.md)]-kontaktfilter: **Type** er **Person**, og kontakten er knyttet til en virksomhed. [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontaktfilter: Kontakten er tildelt en virksomhed, og den overordnede debitortype er **Kunde**. |
| Valuta | Transaktionsvaluta | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |

> [!NOTE]
> Disse **Dataverse**-handlinger vil ikke være tilgængelige på sider, f. eks. siden debitorkort, for poster, der ikke overholder tabel filteret i integrations tabel tilknytningen.

### Tip til administratorer: Visning af tabeltilknytninger

Du kan få vist tilknytningen mellem tabellerne i [!INCLUDE[prod_short](includes/cds_long_md.md)] og tabellerne i [!INCLUDE[prod_short](includes/prod_short.md)] på siden **Integrationstabeltilknytninger**, hvor du kan også anvende filtre. Du definerer tilknytningen mellem felterne i [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller og kolonnerne i [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabeller på siden **Integreret felttilknytning**, hvor du kan tilføje yderligere tilknytningslogik. Det kan f.eks. være nyttigt, hvis du har brug for fejlfinding i forbindelse med synkronisering.

## Brug virtuelle tabeller til at få flere data

Når du konfigurerer din integration, kan du bruge virtuelle tabeller til at gøre flere data tilgængelige i [!INCLUDE[prod_short](includes/cds_long_md.md)] uden hjælp fra en udvikler.

En virtuel tabel er en brugerdefineret tabel, der har kolonner og rækker, der indeholder data fra en ekstern datakilde, f.eks. [!INCLUDE [prod_short](includes/prod_short.md)]. Kolonnerne og rækkerne i en virtuel tabel ligner en almindelig tabel, men dataene gemmes ikke i en fysisk tabel i databasen [!INCLUDE[prod_short](includes/cds_long_md.md)] . I stedet hentes dataene på kørselstidspunktet.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] Indeholder objekter, der også kaldes virtuelle tabeller. Disse tabelobjekter er ikke relateret til de virtuelle tabeller, du bruger sammen med [!INCLUDE[prod_short](includes/cds_long_md.md)].

Hvis du vil vide mere om virtuelle tabeller, skal du gå til følgende artikler:

* [Oprette og redigere virtuelle tabeller, der indeholder data fra en ekstern datakilde](/power-apps/maker/data-platform/create-edit-virtual-entities) (Power Apps-dokumentation)
* [Business Central-virtuel tabel til Microsoft Dataverse administratorreference](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-admin-reference) ([!INCLUDE [prod_short](includes/prod_short.md)]-dokumentation)

Hvis du vil bruge virtuelle tabeller, skal du installere **Business Central Virtual Entity-appen** fra [AppSource](https://appsource.microsoft.com/en-US/product/dynamics-365/microsoftdynsmb.businesscentral_virtualentity). 

Når du har installeret appen, kan du aktivere virtuelle tabeller fra en af følgende sider i [!INCLUDE [prod_short](includes/prod_short.md)]:

* Når du kører den assisterede opsætningsvejledning til **Konfigurer Dataverse-forbindelse**, kan du bruge siden **Dataverse-tilgængelige virtuelle tabeller** til at vælge flere virtuelle tabeller. Derefter er tabellerne tilgængelige i [!INCLUDE[prod_short](includes/cds_long_md.md)] og PowerApps Maker Portal. 
* Fra siderne **Dataverse Forbindelsesopsætning**, **Virtuelle tabeller** og **Tilgængelige virtuelle tabeller**.  
* Fra Power App Maker Portal.

## Synkronisere data fra flere firmaer eller miljøer

Du kan synkronisere data fra flere [!INCLUDE [prod_short](includes/prod_short.md)] firmaer eller miljøer med et [!INCLUDE[prod_short](includes/cds_long_md.md)] miljø. I synkroniseringsscenarier med flere firmaer er der flere ting, du skal overveje.

### Angive firma-id'er

Når du synkroniserer poster, angiver vi et firma-id på [!INCLUDE[prod_short](includes/cds_long_md.md)] objektet for at tydeliggøre, hvilket [!INCLUDE [prod_short](includes/prod_short.md)] firma posterne stammer fra. Integrationstabeltilknytninger har integrationstabelfilterfelter, der tager højde for firma-id'et. Hvis du vil medtage en tabeltilknytning i en opsætning af flere virksomheder, skal du markere afkrydsningsfeltet **Synkronisering aktiveret med flere firmaer på** siden **Integrering af tabeltilknytning**. Indstillingen optimerer den måde, integrationstabelfilterfelter filtrerer firma-id'er på i en opsætning med flere firmaer.

Hvis du markerer afkrydsningsfeltet Synkronisering aktiveret med flere firmaer, tages der kun hensyn til enheder, der har det aktuelle firma-id, hvis du markerer afkrydsningsfeltet **Synkronisering aktiveret for flere firmaer** [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil synkronisere dokumenter, f.eks. mellem Business Central og Sales, skal brugere i Sales angive regnskabs-id'et på dokumenterne. Ellers synkroniseres dokumenterne ikke.  

For alle andre integrationstabeltilknytninger fjernes filteret på firma-id'et, hvis du markerer afkrydsningsfeltet **Synkronisering aktiveret flere firmaer**. Ved synkroniseringen tages der højde for relaterede enheder, uanset deres firma-id.

### Angiv synkroniseringsretningen

Hvis du aktiverer understøttelse af flere virksomheder på en integrationstabeltilknytning, anbefales det, at du angiver retningen for tilknytningen til **FromIntegration**. Hvis du angiver retningen **ToIntegration** eller **Tovejs**, er det en god ide at bruge **Tabelfilter** og **Tabelfilter til integration** til at styre, hvilke enheder der synkroniseres med hvilken virksomhed. Det er også en god ide at bruge matchbaseret kobling for at undgå at oprette dublerede poster. Hvis du vil vide mere om matchbaseret sammenkædning, skal du gå til [Tilpas matchbaseret sammenkædning](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#customize-the-match-based-coupling).

### Brug entydige numre

Hvis din nummerserie ikke garanterer, at de primære nøgleværdier er unikke for hver virksomhed, anbefaler vi, at du bruger præfikser. Hvis du vil begynde at bruge præfikser, skal du oprette en transformationsregel for tilknytningen af integrationsfeltet. Du kan få mere at vide om transformationsregler ved at gå til [Håndtere forskelle i feltværdier](admin-how-to-modify-table-mappings-for-synchronization.md#handle-differences-in-field-values).

## Se også  

[Sammenkæde og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Planlægge en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
