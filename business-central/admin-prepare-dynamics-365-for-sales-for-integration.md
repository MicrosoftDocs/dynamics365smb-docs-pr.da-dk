---
title: Integrere med Dynamics 365 Sales | Microsoft Docs
description: Få at vide, hvordan du gør Dynamics 365 Business Central klar til integration med Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 136a96c880c7abf9b082d7f8859e484be54da4e1
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777313"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integration med Dynamics 365 Sales
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Rollen Sælger betragtes ofte som et af de mest udadvendte i en virksomhed. Det kan imidlertid være en fordel for sælgere at kunne se indad i virksomheden og se, hvad der foregår i back end. Ved at integrere [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] kan du give dine sælgere denne indsigt ved at gøre det muligt for dem at få vist oplysninger i [!INCLUDE[prod_short](includes/prod_short.md)], når de arbejder i [!INCLUDE[crm_md](includes/crm_md.md)]. Ved udarbejdelse af et salgstilbud kan det f.eks. være nyttigt at vide, om der er tilstrækkelig lagerbeholdning til at opfylde ordren. Du kan finde flere oplysninger i [Bruge Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Dette emne beskriver processen med at integrere onlineversionerne af [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Du kan finde oplysninger om konfiguration af det lokale miljø under [Forberede Dynamics 365 Sales til integration i det lokale miljø](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-dataverse"></a>Integration via Dataverse
[!INCLUDE[prod_short](includes/prod_short.md)] kan også integreres med [!INCLUDE[prod_short](includes/cds_long_md.md)], hvilket gør det nemt at forbinde og synkronisere data med andre Dynamics 365-programmer såsom [!INCLUDE[crm_md](includes/crm_md.md)] eller endda apps, som du selv opbygger. Hvis det er første gang, du integrerer, anbefaler vi, at du gør det ved hjælp af [!INCLUDE[prod_short](includes/cds_long_md.md)]. Få flere oplysninger i [Integration med Dataverse](admin-common-data-service.md).

Hvis du allerede har integreret [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)], kan du fortsætte med at synkronisere data ved hjælp af din installation. Men hvis du opgraderer eller deaktiverer din [!INCLUDE[crm_md](includes/crm_md.md)]-integration, skal du oprette forbindelse igen via [!INCLUDE[prod_short](includes/cds_long_md.md)] for at aktivere den igen. Du kan få flere oplysninger i [Opgradering af en integration med Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Hvis du genopretter forbindelsen via [!INCLUDE[prod_short](includes/cds_long_md.md)], anvendes standardindstillingerne for synkroniseringen, og alle konfigurationer, du har angivet, tilsidesættes. Standard-tabeltilknytningerne anvendes for eksempel.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Integrationsindstillinger, der er specifikke for en [!INCLUDE[crm_md](includes/crm_md.md)]-integration
Integration med [!INCLUDE[prod_short](includes/prod_short.md)] foregår via [!INCLUDE[prod_short](includes/cds_long_md.md)], og der er mange standardindstillinger og -tabeller, som stilles til rådighed af integrationen. Ud over standardindstillingerne er der nogle, der er specifikke for [!INCLUDE[crm_md](includes/crm_md.md)]. I følgende afsnit vises disse.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Tilladelser og sikkerhedsroller for brugerkonti i Sales
Når du installerer integrationsløsningen, konfigureres tilladelser til integrationsbrugerkontoen. Hvis disse tilladelser ændres, skal du muligvis nulstille dem. Det kan du gøre ved at geninstallere integrationsløsningen ved at vælge **Geninstaller integrationsløsning** på siden **Opsætning af Dynamics 365-forbindelse**. Følgende sikkerhedsroller installeres:

* Dynamics 365 Business Central-integrationsadministrator
* Dynamics 365 Business Central-integrationsbruger
* Dynamics 365 Business Central-produkttilgængelighedsbruger

### <a name="connection-settings-in-the-setup-guide"></a>Forbindelsesindstillinger i installationsvejledningen

Du kan bruge en assisteret opsætningsvejledning til at konfigurere forbindelsen hurtigt og angive avancerede funktioner som f.eks. sammenkædning mellem poster.

1. Vælg **Installation og udvidelser**, og vælg derefter **Assisteret opsætning**.
2. Vælg **Konfigurer Dynamics 365 Sales-forbindelsen** for at starte den assisterede opsætningsvejledning.
3. Udfyld felterne efter behov.
4. Der er også avancerede indstillinger, der kan forbedre sikkerhed og aktivere ekstra funktioner, f.eks. behandling af salgsordrer og visning af lagerniveauer. Den følgende tabel beskriver de avancerede indstillinger.  

| Felt | Beskrivelse |
|--|--|
| **Importér Dynamics 365 Sales-løsning** | Aktivér denne for at installere og konfigurere integrationsløsningen i [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
| **Udgiv webtjeneste Varedisponering** | Aktivér brugere, der bruger [!INCLUDE[crm_md](includes/crm_md.md)] til at få vist tilgængeligheden af varer (produkter) på lager i [!INCLUDE[prod_short](includes/prod_short.md)]. Dette kræver en [!INCLUDE[prod_short](includes/prod_short.md)]-brugerkonto med en adgangsnøgle til webtjenester. Tildeling af nøglen er en totrinsproces. I brugerkontoen i [!INCLUDE[prod_short](includes/prod_short.md)] skal du vælge handlingen **Ændr webtjenestenøgle**. I den assisterede opsætningsvejledning Konfigurer Dynamics 365 Sales-forbindelse skal du angive URL-adresse til Dynamics 365 Business Central OData-webtjeneste og angive [!INCLUDE[prod_short](includes/prod_short.md)]-brugeroplysninger for at få adgang til tjenesten. Du kan finde flere oplysninger i [OData-webtjenester](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). |
| **URL-adresse til Business Central OData-webtjeneste** | Hvis du aktiverer webtjenesten til visning af varetilgængelighed, er URL-adressen for OData-webtjenesten udfyldt. |
| **Brugernavn til Business Central OData-webtjeneste** | Navnet på [!INCLUDE[prod_short](includes/prod_short.md)]-brugerkontoen, som [!INCLUDE[crm_md](includes/crm_md.md)] bruger til at hente oplysninger om varetilgængelighed i [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af OData-webtjenesten. |
| **Adgangsnøgle til Business Central OData-webtjeneste** | Adgangsnøglen til brugerkontoen, som [!INCLUDE[crm_md](includes/crm_md.md)] bruger til at hente oplysninger om varetilgængelighed fra [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af OData-webtjenesten. Nøglen er knyttet til den bruger, der er valgt i feltet **Brugernavn til Business Central OData OData-webtjeneste**. For at få nøglen skal du vælge knappen **Slå værdi op** ved siden af brugernavnet, vælge brugeren, vælge **Administrer** og derefter **Rediger**. På brugerkortet skal du vælge **Handlinger**, **Godkendelse** og derefter klikke på **Ændr webtjenestenøgle**. |
| **Aktivér integration af salgsordrer** | Når der oprettes salgsordrer i [!INCLUDE[crm_md](includes/crm_md.md)] og opfyldes ordrer i [!INCLUDE[prod_short](includes/prod_short.md)], integreres processen i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Aktivere integration af salgsordrebehandling](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Dette kræver, at du angiver legitimationsoplysninger for en administratorbrugerkonto i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Håndtering af salgsordredata](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
| **Aktivér CDS-forbindelse** | Aktivér forbindelsen til [!INCLUDE[prod_short](includes/cds_long_md.md)]. |
| **Dynamics 365 SDK-version** | Det er kun relevant, hvis du integrerer med en lokal version af [!INCLUDE[crm_md](includes/crm_md.md)]. Det er det Dynamics 365 software development kit (også kaldet Xrm), du bruger til at forbinde [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]. Versionen skal være kompatibel med den version af SDK, som bruges af [!INCLUDE[crm_md](includes/crm_md.md)], og være lig med eller nyere end den version, der bruges af [!INCLUDE[crm_md](includes/crm_md.md)]. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Forbindelsesindstillinger på siden Microsoft Dynamics 365-konfiguration af forbindelse

Indtast følgende oplysninger vedrørende forbindelsen fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)].

| Felt | Description |
|--|--|
| **URL-adresse til Dynamics 365 Sales** | URL-adressen for din [!INCLUDE[crm_md](includes/crm_md.md)]-forekomst. Dette gør det muligt for brugere at åbne tilsvarende poster i [!INCLUDE[prod_short](includes/prod_short.md)] fra poster i [!INCLUDE[crm_md](includes/crm_md.md)], f.eks. et firma eller produkt. [!INCLUDE[prod_short](includes/prod_short.md)]-poster åbnes i [!INCLUDE[prod_short](includes/prod_short.md)]. |
|**URL-adresse til Dynamics 365 Sales**|URL-adressen for din [!INCLUDE[crm_md](includes/crm_md.md)]-forekomst. Dette gør det muligt for brugere at åbne tilsvarende poster i [!INCLUDE[prod_short](includes/prod_short.md)] fra poster i [!INCLUDE[crm_md](includes/crm_md.md)], f.eks. et firma eller produkt. [!INCLUDE[prod_short](includes/prod_short.md)]-poster åbnes i [!INCLUDE[prod_short](includes/prod_short.md)].|
|**Webtjenesten Varedisponering er aktiveret**|Giv brugere, der benytter [!INCLUDE[crm_md](includes/crm_md.md)], mulighed for at se tilgængeligheden af varer (produkter) på lager i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du aktiverer dette, skal du også angive et brugernavn og en adgangsnøgle, som [!INCLUDE[crm_md](includes/crm_md.md)] skal bruge til at forespørge OData-webtjenesten om tilgængelighed af varer (produkter). Du kan finde flere oplysninger i [OData-webtjenester](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**URL-adresse til Dynamics 365 Business Central OData-webtjeneste**|Hvis du aktiverer Webtjenesten Varedisponering, er URL-adressen for OData-webtjenesten udfyldt. Indstil dette felt til URL-adressen på den [!INCLUDE[prod_short](includes/prod_short.md)]-forekomst, der skal bruges.<br /><br /> Du kan nulstille feltet til standard-URL-adressen for [!INCLUDE[prod_short](includes/prod_short.md)] ved at vælge handlingen **Nulstil URL-adresse til webklient**.<br /><br /> Dette felt er kun relevant, hvis [!INCLUDE[prod_short](includes/prod_short.md)]-integrationsløsningen er installeret i [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Brugernavn til Dynamics 365 Business Central OData-webtjeneste**|Navnet på den brugerkonto, som [!INCLUDE[crm_md](includes/crm_md.md)] bruger til at hente oplysninger om varetilgængelighed fra [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af OData-webtjenesten.|
|**Adgangsnøgle til Dynamics 365 Business Central OData-webtjeneste**|Adgangsnøglen til brugerkontoen, som [!INCLUDE[crm_md](includes/crm_md.md)] bruger til at hente oplysninger om varetilgængelighed fra [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af OData-webtjenesten. Nøglen er knyttet til den bruger, der er valgt i feltet **Brugernavn til Dynamics 365 Business Central OData-webtjeneste**. For at få nøglen skal du vælge knappen **Slå værdi op** ved siden af brugernavnet, vælge brugeren, vælge **Administrer** og derefter **Rediger**. På brugerkortet skal du vælge **Handlinger**, **Godkendelse** og derefter klikke på **Ændr webtjenestenøgle**.|
|**Dynamics 365 SDK-version**|Hvis du integrerer med en lokal version af [!INCLUDE[crm_md](includes/crm_md.md)], er det Dynamics 365 software development kit (også kaldet Xrm), du bruger til at forbinde [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]. Den version, du har valgt, skal være kompatibel med den version af SDK, som bruges af [!INCLUDE[crm_md](includes/crm_md.md)]. Versionen er lig med eller nyere end den version, der bruges af [!INCLUDE[crm_md](includes/crm_md.md)].|

Udover indstillingerne ovenfor skal du angive følgende indstillinger for [!INCLUDE[crm_md](includes/crm_md.md)].

| Felt | Description |
|--|--|
| **Salgsordreintegration er aktiveret** | Brugerne skal kunne afsende salgsordrer og aktiverede tilbud i [!INCLUDE[crm_md](includes/crm_md.md)] og derefter få vist og behandle dem i [!INCLUDE[prod_short](includes/prod_short.md)]. Dette integrerer processen i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Aktivere integration af salgsordrebehandling](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Opret salgsordrer automatisk** | Opret en salgsordre i [!INCLUDE[prod_short](includes/prod_short.md)], når en bruger opretter og sender en i [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Behandl salgstilbud automatisk** | Behandl et salgstilbud i [!INCLUDE[prod_short](includes/prod_short.md)], når en bruger opretter og aktiverer et i [!INCLUDE[crm_md](includes/crm_md.md)]. |

<!--
### User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Standardenhedstilknytning i Sales til synkronisering

Objekter i [!INCLUDE[crm_md](includes/crm_md.md)], f.eks. ordrer, er integreret med tabeller af samme type i [!INCLUDE[prod_short](includes/prod_short.md)], som f.eks. salgsordrer. For at arbejde med [!INCLUDE[crm_md](includes/crm_md.md)]-data, opretter du links, kaldet sammenkædninger mellem tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].

Følgende tabel viser standardtilknytningen mellem tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)], som [!INCLUDE[prod_short](includes/prod_short.md)] leverer.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synkroniseringsretning | Standardfilter |
|--|--|--|--|
| Enhe. | Enhedsgruppe | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Vare | Produkt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-kontaktfilter: **Produkttype** er **Salg lager** |
| Ressource | Produkt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-kontaktfilter: **Produkttype** er **Tjenester** |
| Debitorprisgruppe | Prisliste | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Salgspris | Produktprisliste | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)]-kontaktfilter: **Salgskode** er ikke tom, **Salgstype** er **Debitorprisgruppe** |
| Salgsmulighed | Salgsmulighed | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Salgsfakturahoved | Faktura | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Salgsfakturalinje | Fakturaprodukt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Salgsordrehovedet | Salgsordre | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] Filter for salgshoved: **Dokumenttype** er Ordre, **Status** er Frigivet |
| Bemærkninger til salgsordre | Bemærkninger til salgsordre | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

### <a name="synchronization-rules"></a>Synkroniseringsregler

Følgende tabel viser de regler, der styrer synkroniseringen mellem [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)]. Dette er foruden de regler, der er defineret for Dataverse, der også gælder. Få flere oplysninger i [Standardobjekttilknytning](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

> [!NOTE]  
> Ændringer af data i , der blev foretaget af integrationsbrugerkontoen, synkroniseres ikke. Derfor anbefales det, at du ikke ændrer data, når du benytter denne konto. Du kan finde flere oplysninger i [Konfigurere brugerkonti til integration med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Sortbord|Regel|
|-----|----|
|Enheder|Måleenheder synkroniseres med enhedsgrupper i [!INCLUDE[crm_md](includes/crm_md.md)]. Der kan kun være én måleenhed defineret i enhedsgruppen.|
|Varer|Når du synkroniserer varer med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter, opretter [!INCLUDE[prod_short](includes/prod_short.md)] automatisk en prisliste i [!INCLUDE[crm_md](includes/crm_md.md)]. For at undgå synkroniseringsfejl bør du ikke ændre denne prisliste manuelt.|
|Ressourcer|Ressourcer synkroniseres med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter, har produkttypen Service.|
|Debitorprisgrupper|Debitorprisgrupper synkroniseres med prislister i Sales.|
|Salgspriser|Priser i Sales, der har salgstypen Debitorprisgruppe og har en salgskode defineret, synkroniseres med [!INCLUDE[crm_md](includes/crm_md.md)]-prislistelinjer|
|Salgsmuligheder|Salgsmuligheder synkroniseres med [!INCLUDE[crm_md](includes/crm_md.md)]-salgsmuligheder. Værdien Sælgerkode definerer ejeren af den sammenkædede tabel i [!INCLUDE[crm_md](includes/crm_md.md)].|
|Bogførte salgsfakturaer|Bogførte salgsfakturaer synkroniseres med salgsfakturaer. Før en faktura kan synkroniseres, er det bedre at synkronisere alle andre tabeller, der kan indgå i fakturaen, fra sælgere til prislister. Værdien Sælgerkode i fakturahovedet definerer ejeren af den sammenkoblede tabel i Sales.|
|Salgsordrer|Når salgsordreintegration er aktiveret, synkroniseres salgsordrer i [!INCLUDE[prod_short](includes/prod_short.md)], der er oprettet fra sendte salgsordrer i [!INCLUDE[crm_md](includes/crm_md.md)], med salgsordrer i INKLUDER SALG, når de frigives. Inden du synkroniserer ordrer, anbefales det, at du først synkroniserer alle de tabeller, der indgår i ordren, f.eks. sælgere og prislister. Feltet Sælgerkode i ordrehovedet definerer ejeren af den sammenkædede tabel i [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Synkroniseringsjob for en salgsintegration

Jobbene køres i følgende rækkefølge for at undgå sammenkædning af afhængigheder mellem tabeller. Du kan vælge yderligere job i Dataverse. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](./admin-job-queues-schedule-tasks.md).

1. MÅLEENHED – Dynamics 365 Sales-synkroniseringsjob  
2. RESSOURCE-PRODUKT – Dynamics 365 Sales-synkroniseringsjob  
3. VARE - PRODUKT – Dynamics 365 Sales-synkroniseringsjob  
4. KUNDEPRISGRUPPE -PRIS – Dynamics 365 Sales-synkroniseringsjob.
5. SALGSPRIS- PRODUKTPRIS – Dynamics 365 Sales-synkroniseringsjob.
6. BOGFØRTE SALGSFAKTURAER-FAKTURAER – Dynamics 365 Sales-synkroniseringsjob.

### <a name="default-synchronization-job-queue-entries"></a>Poster for standardsynkroniseringsjobkø

I følgende tabel beskrives standardsynkroniseringsjobbene for Salg.  

|Post for jobkø|Description|Retning|Integrationstabeltilknytning|Standardhyppighed for synkronisering (min.)|Standardangivelse for dvale ved inaktivitet (min.)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|MÅLEENHED – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-enhedsgrupper med [!INCLUDE[prod_short](includes/prod_short.md)]-måleenheder.|Fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|MÅLEENHED|30|720<br> (12 timer)|
|RESSOURCE-PRODUKT – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[prod_short](includes/prod_short.md)]-ressourcer.|Fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE-PRODUKT|30|720<br> (12 timer)|
|VARE - PRODUKT – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[prod_short](includes/prod_short.md)]-varer.|Fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|VARE-PRODUKT|30|1440<br> (24 timer)|
|KUNDEPRISGRUPPE -PRIS – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-salgsprislister med [!INCLUDE[prod_short](includes/prod_short.md)]-debitorprisgrupper.| |DEBITORPRISGRUPPER-SALGSPRISLISTER|30|1440<br> (24 timer)|
|SALGSPRIS- PRODUKTPRIS – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produktpriser med [!INCLUDE[prod_short](includes/prod_short.md)]-salgspriser.||PRODUKTPRIS-SALGSPRIS|30|1440<br> (24 timer)|
|BOGFØRTE SALGSFAKTURAER-FAKTURAER – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)] fakturaer med [!INCLUDE[prod_short](includes/prod_short.md)] bogførte salgsfakturaer.|Fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|FAKTURAER-BOGFØRTE SALGSFAKTURAER|30|1440<br> (24 timer)|
|Debitorstatistik - Dynamics 365 Sales-synkroniseringsjob|Opdaterer [!INCLUDE[crm_md](includes/crm_md.md)] konti med seneste [!INCLUDE[prod_short](includes/prod_short.md)] debitordata. I [!INCLUDE[crm_md](includes/crm_md.md)] vises disse oplysninger i **Business Central kontostatistik** i hurtigvisningsformat over konti, der er sammenkædet med [!INCLUDE[prod_short](includes/prod_short.md)]-debitorer.<br /><br /> Disse data skal også opdateres manuelt fra hver debitor-record. Du kan finde flere oplysninger i [Sammenkæd og synkroniser poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Bemærk:**  denne jobkøpost er kun relevant, hvis [!INCLUDE[prod_short](includes/prod_short.md)] integrationsløsningen er installeret i [!INCLUDE[crm_md](includes/crm_md.md)]. |Ikke tilgængelig|Ikke tilgængelig|30|Ikke tilgængelig| 

## <a name="connecting-business-central-on-premises-versions-earlier-than-version-16"></a>Tilslutning af lokale Business Central-versioner, der er ældre end version 16
Microsoft Power Platform-teamet har [meddelt](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse), at det fraråder Office365-godkendelsestypen. Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, der er ældre end version 16, skal du bruge godkendelsestypen OAuth for at oprette forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)]-online. Fremgangsmåden i dette afsnit beskriver, hvordan du opretter forbindelsen.

### <a name="prerequisites"></a>Forudsætninger

- Du skal have et Microsoft Azure-abonnement. En prøvekonto kan bruges til registrering af programmer.
- [!INCLUDE[crm_md](includes/crm_md.md)] er konfigureret til at bruge en af følgende godkendelsestyper:

   - Office365 (ældre)

     > [!IMPORTANT]
     > Fra april 2022 vil Office365 (ældre) ikke længere være understøttet. Du kan finde flere oplysninger i [Vigtige ændringer (udfasninger) på vej i Power Apps, Power Automate og Customer Engagement-apps](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   - OAuth

### <a name="to-connect-a-version-of-business-central-earlier-than-version-16"></a>Opret forbindelse af en version af Business Central, der er ældre end version 16

1. Importér Microsoft Dynamics 365 Business Central-integrationsløsningen til dit [!INCLUDE[crm_md](includes/crm_md.md)]-miljø. Integrationsløsningen findes i mappen CrmCustomization på dvd'en med Business Central-installation. Der er flere versioner af løsningen, f.eks. DynamicsNAVIntegrationSolution_v8 eller DynamicsNAVIntegrationSolution_v9 eller DynamicsNAVIntegrationSolution_v91. Den løsning, du skal importere, afhænger af den version af [!INCLUDE[crm_md](includes/crm_md.md)], du opretter forbindelse til. [!INCLUDE[crm_md](includes/crm_md.md)] online kræver løsningen DynamicsNAVIntegrationSolution_v91 integration.
2. Opret en bruger, der ikke er interaktiv for integration [!INCLUDE[crm_md](includes/crm_md.md)], i miljøet, og tildel brugeren følgende sikkerhedsroller. Du kan finde flere oplysninger i [Oprette en ikke-interaktiv brugerkonto](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Dynamics 365 Business Central-integrationsadministrator
   * Dynamics 365 Business Central-integrationsbruger

   > [!Important]
   > Brugeren må ikke have sikkerhedsrollen Systemadministrator. Du kan heller ikke bruge systemadministratorkontoen som integrationsbruger.

3.  Opret en app-registrering til [!INCLUDE[prod_short](includes/prod_short.md)] i Azure-portalen. Du kan finde fremgangsmåden i [Registrere et program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). De indstillinger, der er specifikke for oprettelse af forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)], er de uddelegerede tilladelser. I følgende tabel vises og beskrives tilladelserne.

   |Navn på API / tilladelse |Type  |Description  |
   |---------|---------|---------|
   |Financials.ReadWrite.All     |Delegeret|Påkrævet til [!INCLUDE[prod_short](includes/prod_short.md)].    |
   |user_impersonation     |Delegeret|Påkrævet til [!INCLUDE[crm_md](includes/crm_md.md)].|
   
4. I [!INCLUDE[prod_short](includes/prod_short.md)] søges efter **Microsoft Dynamics 365-forbindelsesopsætning**, og vælg derefter det relaterede link. 
5. På siden **Microsoft Dynamics 365-forbindelsesopsætning** i feltet **Godkendelsestype** skal du vælge indstillingen til OAuth. 
6. Vælg den CRM SDK-version, der passer til den løsningsversion, du har importeret i trin 1.
7. I feltet **Serveradresse** skal du angive URL-adressen til dit [!INCLUDE[crm_md](includes/crm_md.md)]-miljø og derefter angive brugernavnet og adgangskoden for integrationsbrugeren.
8. I feltet **Forbindelsesstreng** skal du angive id for app-registrering. Dette felt indeholder to tokens, hvor ID'ET for programmet skal angives.

   |Token           |Description  |
   |----------------|-------------|
   |**AppId**       |Angivet til program-id'et.      |
   |**RedirectUri** |Indstil til program-id, men tilføj **app://**-præfikset.         |

    **Eksempel** Viser en tilslutningsstreng i følgende eksempel.

    ```
    AuthType=OAuth;Username=jsmith@contoso.onmicrosoft.com;Password=****;Url=https://contosotest.crm.dynamics.com;AppId=<your AppId>;RedirectUri=app://<your AppId>;TokenCacheStorePath=;LoginPrompt=Auto
    ```
9. Aktivér forbindelse.

> [!Note]
> Hvis du konfigurerer en forbindelse til en [!INCLUDE[crm_md](includes/crm_md.md)] med en forekomst af en bestemt godkendelsestype, skal du udfylde felterne i oversigtspanelet **Detaljer om godkendelsestype**. Du kan finde flere oplysninger i [Godkendelse med Microsoft Dataverse-webtjenester](/powerapps/developer/data-platform/authentication). Dette trin er ikke obligatorisk, når du opretter forbindelse for en onlineversion af [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Se også

[Konfigurere brugerkonti til integration med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Oprette en forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Synkronisere Business Central og [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Forberedelse af Dynamics 365 Sales til integration i det lokale miljø](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]
