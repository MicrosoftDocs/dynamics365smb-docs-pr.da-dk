---
title: Integration med Dynamics 365 Sales
description: 'Få at vide, hvordan du gør Dynamics 365 Business Central klar til integration med Dynamics 365 Sales.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'sales, crm, integration, integrating'
ms.date: 09/28/2023
ms.author: bholtorf
ms.custom: bap-template
---
# Integration med Dynamics 365 Sales

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Rollen Sælger betragtes ofte som et af de mest udadvendte i en virksomhed. Det kan imidlertid være en fordel for sælgere at kunne se indad i virksomheden og se, hvad der foregår i back end. Når du integrerer [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)], kan du give dine salgsmedarbejdere den indsigt. Integrationen kan hjælpe med at se oplysninger i [!INCLUDE[prod_short](includes/prod_short.md)], når der arbejdes i [!INCLUDE[crm_md](includes/crm_md.md)]. Ved udarbejdelse af et salgstilbud kan det f.eks. være nyttigt at vide, om der er tilstrækkelig lagerbeholdning til at opfylde ordren. Du kan finde flere oplysninger i [Brug Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Dette emne beskriver processen med at integrere onlineversionerne af [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Du kan finde oplysninger om konfiguration af det lokale miljø under [Forberede Dynamics 365 Sales til integration i det lokale miljø](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## Integration via Dataverse

Med henblik på at gøre det lettere at oprette forbindelse og synkronisere data med andre Dynamics 365-programmer, kan [!INCLUDE[prod_short](includes/prod_short.md)] også integreres med [!INCLUDE[prod_short](includes/cds_long_md.md)]. Du kan f. eks. oprette forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)] eller endda apps, som du selv bygger. Hvis det er første gang, du integrerer, skal du gøre det ved hjælp af [!INCLUDE[prod_short](includes/cds_long_md.md)]. Få flere oplysninger i [Integration med Dataverse](admin-common-data-service.md).

Hvis du allerede har integreret [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)], kan du fortsætte med at synkronisere data ved hjælp af din installation. Men hvis du opgraderer eller deaktiverer din [!INCLUDE[crm_md](includes/crm_md.md)]-integration, skal du oprette forbindelse igen via [!INCLUDE[prod_short](includes/cds_long_md.md)] for at aktivere den igen. Du kan få flere oplysninger i [Opgradering af en integration med Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Hvis du genopretter forbindelsen via [!INCLUDE[prod_short](includes/cds_long_md.md)], anvendes standardindstillingerne for synkroniseringen, og alle konfigurationer, du har angivet, tilsidesættes. Standard-tabeltilknytningerne anvendes for eksempel.

## Integrationsindstillinger, der er specifikke for en [!INCLUDE[crm_md](includes/crm_md.md)]-integration

Integration med [!INCLUDE[prod_short](includes/prod_short.md)] foregår via [!INCLUDE[prod_short](includes/cds_long_md.md)], og der er mange standardindstillinger og -tabeller, som stilles til rådighed af integrationen. Ud over standardindstillingerne er der nogle, der er specifikke for [!INCLUDE[crm_md](includes/crm_md.md)]. I følgende afsnit vises disse indstillinger.

## Tilladelser og sikkerhedsroller for brugerkonti i Sales

Når du installerer integrationsløsningen, konfigureres tilladelser til integrationsbrugerkontoen. Hvis disse tilladelser ændres, skal du muligvis nulstille dem. Det kan du gøre ved at geninstallere integrationsløsningen ved at vælge **Geninstaller integrationsløsning** på siden **Opsætning af Dynamics 365-forbindelse**. Følgende sikkerhedsroller installeres:

* Dynamics 365 Business Central-integrationsadministrator
* Dynamics 365 Business Central-integrationsbruger
* Dynamics 365 Business Central-produkttilgængelighedsbruger

### Forbindelsesindstillinger i installationsvejledningen

Du kan bruge en assisteret opsætningsvejledning til at konfigurere forbindelsen hurtigt og angive avancerede funktioner som f.eks. sammenkædning mellem poster.

1. Vælg **Installation og udvidelser**, og vælg derefter **Assisteret opsætning**.
2. Vælg **Konfigurer Dynamics 365 Sales-forbindelsen** for at starte den assisterede opsætningsvejledning.
3. Udfyld felterne efter behov.
4. Eventuelt er der avancerede indstillinger, som kan forbedre sikkerheden og aktivere flere funktioner. Den følgende tabel beskriver de avancerede indstillinger.  

| Felt | Beskrivelse |
|--|--|
| **Importér Dynamics 365 Sales-løsning** | Installer og konfigurer integrationsløsningen i [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
|**Synkroniser automatisk varetilgængelighed**|Angiver, at varetilgængeligheden i sagskøen skal planlægges. Opgavekøen køres hvert 30. minut og opdaterer tilgængeligheden af de sammenkoblede varer.|
| **Aktivér integration af ældre salgsordrer** | Når der oprettes salgsordrer i [!INCLUDE[crm_md](includes/crm_md.md)] og opfyldes ordrer i [!INCLUDE[prod_short](includes/prod_short.md)], integreres denne indstilling processen i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Aktivere integration af salgsordrebehandling](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).<br><br>**Bemærk:** Du kan ikke bruge denne indstilling, hvis du bruger indstillingen **Tovejs synkronisering af salgsordrer**. De to indstillinger udelukker hinanden. Du kan få mere at vide om denne indstilling ved at gå til [Enkelt og tovejssynkronisering af salgsordrer](#single-and-bi-directional-synchronization-of-sales-orders). |
|**Aktivér Dynamics 365 Sales-forbindelse** | Aktivér forbindelsen til [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Dynamics 365 SDK-version** | Det er kun relevant, hvis du integrerer med en lokal version af [!INCLUDE[crm_md](includes/crm_md.md)]. Denne SDK er det Dynamics 365 software development kit (også kaldet Xrm), du bruger til at forbinde [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]. Versionen skal være kompatibel med den version af SDK, som bruges af [!INCLUDE[crm_md](includes/crm_md.md)], og være lig med eller nyere end den version, der bruges af [!INCLUDE[crm_md](includes/crm_md.md)]. |
|**Tovejs synkronisering af salgsordrer**|Synkronisere salgsordrer i begge retninger. Du kan få mere at vide om denne indstilling ved at gå til [Enkelt og tovejssynkronisering af salgsordrer](#single-and-bi-directional-synchronization-of-sales-orders).<br><br>**Bemærk:** Du kan ikke bruge denne indstilling, hvis du bruger indstillingen **Aktivér integration af ældre salgsordrer**. De to indstillinger udelukker hinanden.|

### Forbindelsesindstillinger på siden Microsoft Dynamics 365-konfiguration af forbindelse

Indtast følgende oplysninger vedrørende forbindelsen fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)].

| Felt | Beskrivelse |
|--|--|
|**URL-adresse til Dynamics 365 Sales**|URL-adressen for din [!INCLUDE[crm_md](includes/crm_md.md)]-forekomst. Med denne indstilling kan brugere åbne de poster i [!INCLUDE[prod_short](includes/prod_short.md)], der svarer til poster i [!INCLUDE[crm_md](includes/crm_md.md)]. F. eks. en konto eller et produkt. [!INCLUDE[prod_short](includes/prod_short.md)]-poster åbnes i [!INCLUDE[prod_short](includes/prod_short.md)].|
|**Synkroniser automatisk varetilgængelighed**|Angiver, at varetilgængeligheden i sagskøen skal planlægges. Opgavekøen køres hvert 30. minut og opdaterer tilgængeligheden af de sammenkoblede varer.|
|**Dynamics 365 SDK-version**|Hvis du integrerer med en lokal version af [!INCLUDE[crm_md](includes/crm_md.md)], er det Dynamics 365 software development kit (også kaldet Xrm), du bruger til at forbinde [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]. Den version, du har valgt, skal være kompatibel med den version af SDK, som bruges af [!INCLUDE[crm_md](includes/crm_md.md)]. Versionen er lig med eller nyere end den version, der bruges af [!INCLUDE[crm_md](includes/crm_md.md)].|

Udover indstillingerne ovenfor skal du angive følgende indstillinger for [!INCLUDE[crm_md](includes/crm_md.md)].

| Felt | Beskrivelse |
|--|--|
| **Salgsordreintegration er aktiveret** | Brugerne skal kunne afsende salgsordrer og aktiverede tilbud i [!INCLUDE[crm_md](includes/crm_md.md)] og derefter få vist og behandle dem i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne indstilling integrerer processen i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Aktivere integration af salgsordrebehandling](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Opret salgsordrer automatisk** | Opret en salgsordre i [!INCLUDE[prod_short](includes/prod_short.md)], når en bruger opretter og sender en i [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Behandl salgstilbud automatisk** | Behandl et salgstilbud i [!INCLUDE[prod_short](includes/prod_short.md)], når en bruger opretter og aktiverer et i [!INCLUDE[crm_md](includes/crm_md.md)]. Der er flere oplysninger i [Håndtere data i salgstilbud](/dynamics365/business-central/marketing-integrate-dynamicscrm?tabs=new-experience#handling-sales-quotes-data). |
|**Tovejs synkronisering af salgsordrer**|Synkronisere salgsordrer i begge retninger. Du kan få mere at vide om denne indstilling ved at gå til [Enkelt og tovejssynkronisering af salgsordrer](#single-and-bi-directional-synchronization-of-sales-orders).|
<!--
### User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->
### Enkelt- og tovejs synkronisering af salgsordrer

Når du konfigurerer integrationen, enten i opsætningsvejledningen eller på siden Microsoft Dynamics 365-forbindelseskonfiguration, er der indstillinger, der styrer, i hvilken retning du synkroniserer salgsordrer, og hvordan du sender dem.

Med indstillingen **Tovejs synkronisering af salgsordrer** kan du synkronisere salgsordrer fra Sales til [!INCLUDE [prod_short](includes/prod_short.md)] og omvendt. Hvis en kunde f. eks. ændrer deres mening om produktet eller det antal, der er bestilt i [!INCLUDE[crm_md](includes/crm_md.md)], kan du arkivere salgsdokumentet og oprette et nyt i [!INCLUDE[prod_short](includes/prod_short.md)]. Det samme gælder for ændringer i [!INCLUDE[prod_short](includes/prod_short.md)]. F.eks. når priser, skattebeløb eller forventede leveringsdatoer ændrer sig, synkroniseres ændringerne til [!INCLUDE[crm_md](includes/crm_md.md)]. Tovejs synkronisering gør det nemmere at holde dine sælgere opdaterede med de seneste ændringer og status for salgsordrer.

Ved tovejssynkronisering gør du salgsordrer tilgængelige til synkronisering, når du ændrer deres status til **Sendt** i Salg. Når du angiver denne status, kan du ikke længere ændre oplysningerne på ordrens linjer. Når du synkroniserer, overføres ordren til [!INCLUDE [prod_short](includes/prod_short.md)] med status **Frigivet**. Hvis der er en fejl, kan du gendanne ordren til **Åben** (i [!INCLUDE [prod_short](includes/prod_short.md)]) eller **Aktiv** (i Salg) og derefter tilføje eller slette linjer for at rette fejlen og sende ordren igen.

> [!TIP]
> Når du aktiverer indstillingen **Tovejssynkronisering af salgsordrer**, oprette [!INCLUDE [prod_short](includes/prod_short.md)] en post på siden **Salgsordrearkiv**, når du bogfører eller ændrer oplysninger om en ordre. De arkiverede versioner kan f.eks. være nyttige, når du vil udforske en ordres historik.

Indstillingen **Aktivér integration af ældre salgsordrer** synkroniseres kun fra Salg til [!INCLUDE [prod_short](includes/prod_short.md)]. Til denne indstilling skal du bruge handlingen **Send** i Salg til at gøre ordrer tilgængelige til synkronisering. Når du angiver denne status, kan du ikke længere ændre oplysningerne på ordren. Når du synkroniserer, overføres ordren til [!INCLUDE [prod_short](includes/prod_short.md)] med status **Frigivet**.

Vil du bruge denne indstilling, skal du angive legitimationsoplysninger for en administratorbrugerkonto i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Håndtering af salgsordredata](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!NOTE]
> Indstillingerne **Tovejssynkronisering af salgsordrer** og **Aktivér integration af ældre salgsordrer** udelukker hinanden. Du kan ikke bruge begge indstillinger på samme tid.

For begge indstillinger [!INCLUDE [prod_short](includes/prod_short.md)] vises alle salgsordrer med statussen **Sendt** på siden **Ordrer - Microsoft Dynamics 365 Sales**.

### Standardenhedstilknytning i Sales til synkronisering

Objekter i [!INCLUDE[crm_md](includes/crm_md.md)], f.eks. ordrer, er integreret med tabeller af samme type i [!INCLUDE[prod_short](includes/prod_short.md)], som f.eks. salgsordrer. For at arbejde med [!INCLUDE[crm_md](includes/crm_md.md)]-data, opretter du links, kaldet sammenkædninger mellem tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].

Følgende tabel viser standardtilknytningen mellem tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)], som [!INCLUDE[prod_short](includes/prod_short.md)] leverer.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synkroniseringsretning | Standardfilter |
|--|--|--|--|
| Måleenhed | Enhedsgruppe | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Vare | Produkt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-kontaktfilter: **Produkttype** er **Salg lager** |
| Ressource | Produkt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-kontaktfilter: **Produkttype** er **Tjenester** |
| Vareenhed | CRM-ENHED |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
| Ressourceenhed | CRM-ENHED |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]||
| Enhedsgruppe | CRM-enhedsplan | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ||
| Debitorprisgruppe | Prisliste | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Salgspris | Produktprisliste | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)]-kontaktfilter: **Salgskode** er ikke tom, **Salgstype** er **Debitorprisgruppe** |
| Lead | Lead | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Salgsfakturahoved | Faktura | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Salgsfakturalinje | Fakturaprodukt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Salgsordrehovedet | Salgsordre | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] <br><br> Hvis du vil synkronisere i begge retninger, skal du slå den **tovejs synkronisering af salgsordrer** til og fra på siden **Opsætning af Dynamics 365-forbindelse**.| [!INCLUDE[prod_short](includes/prod_short.md)] Filter for salgshoved: **Dokumenttype** er Ordre, **Status** er Frigivet |
| Bemærkninger til salgsordre | Bemærkninger til salgsordre | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

> [!NOTE]
> Tilknytningerne for enheds-, ressource enheds-og enhedsgruppe tabeller er kun tilgængelige, hvis administratoren har aktiveret **Funktionsopdatering: Synkronisering af flere enheder med funktionen Dynamics 365 Sales** på siden **Funktionsadministration**. Du kan finde flere oplysninger i [Synkronisere varer og ressourcer med produkter i forskellige enheder](admin-prepare-dynamics-365-for-sales-for-integration.md#synchronizing-items-and-resources-with-products-with-different-units-of-measure).

## Synkronisere varer og ressourcer med produkter med forskellige måleenheder

Virksomheder opretter eller køber ofte varerne i en enhed og sælger dem i en anden. Hvis du vil synkronisere varer, der bruger flere enheder, skal du aktivere **Funktionsopdatering: Synkronisering af flere enheder med brug af Dynamics 365 Sales** på siden **Funktionsadministration**. 

Når du aktiverer funktionsopdatering, oprettes der en ny enhedsgruppe tabel, som tildeles til hver vare og ressource i [!INCLUDE[prod_short](includes/prod_short.md)]. Ved hjælp af tabellerne kan du knytte enhedsgruppe-, vareenheds-og ressourceenhedstabellerne i [!INCLUDE[prod_short](includes/prod_short.md)] til Dynamics 365 Sales-enhedsgruppen i [!INCLUDE[crm_md](includes/crm_md.md)]. Følgende billede viser tilknytningerne.

:::image type="content" source="media/unit group 1.png" alt-text="Tabeltilknytninger for enhedsgrupper":::

Du kan oprette flere måleenheder for hver enhedsgruppe og tildele grupper til produkter i [!INCLUDE[crm_md](includes/crm_md.md)]. Derefter kan du synkronisere produkterne med varer og ressourcer i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan manuelt koble vareenheder eller ressourceenheder til en enhedsgruppe. Hvis du gør det, vil enhedsgruppen for varen eller ressourcen ikke være koblet til en enhedsgruppe i [!INCLUDE[crm_md](includes/crm_md.md)], f. eks. fordi enhedsgruppen ikke eksisterer, [!INCLUDE[prod_short](includes/prod_short.md)] opretter enhedsgruppen automatisk i [!INCLUDE[crm_md](includes/crm_md.md)].

### Tilknytning af varer og ressourcer til produkter

Når du aktiverer **Funktionsopdatering: Synkronisering af flere måleenheder med Dynamics 365 Sales**, sker der følgende:

* Der oprettes nye tilknytninger for varer og ressourcer.
* Eksisterende tilknytninger slettes. <!--which mappings?-->
* En dataopgradering opretter enhedsgrupper for varer og ressourcer.

Hvis du vil bruge de nye tilknytninger, skal du synkronisere enhedsgrupper, vareenheder og ressourceenheder. Du skal også gensynkronisere varer og ressourcer. 

> [!NOTE]
> [!INCLUDE[crm_md](includes/crm_md.md)] tillader ikke, at du ændrer en enhedsgruppe for et produkt. Du skal derfor trække produkterne ud og koble dem og ressourcerne op og derefter synkronisere ved at oprette nye produkter i [!INCLUDE[crm_md](includes/crm_md.md)]. 

I følgende trin beskrives trinnene til start af tilknytning af enhedsgrupper:

1. Kontroller, at produkter i [!INCLUDE[crm_md](includes/crm_md.md)] ikke er kombineret med varer eller ressourcer i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis det er, skal du gå til siderne **Varer** og/eller **Ressourcer**, bruge filterindstillingerne til at vælge de sammenkoblede poster. Vælg derefter **Dynamics 365 Sales**-handlingen, og vælg **Fjern sammenkædning**. Denne handling planlægger et baggrundsjob for at opkoble posterne. Mens opgaven kører, kan du kontrollere dets status ved at bruge handlingen **Synkroniseringslogfil**. Du kan finde flere oplysninger under [Kobling og synkronisering](admin-how-to-couple-and-synchronize-records-manually.md). 
2. Når der oprettes nye produkter i [!INCLUDE[crm_md](includes/crm_md.md)] med nye enhedsgrupper, skal du gøre et af følgende for at undgå identiske navne:
    
  * Omdøb produkterne, og lad dem udgå i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Lade produkter udgå (Salgshub)](/dynamics365/sales-enterprise/retire-product). Hvis du vil masseredigere dine produkter i Microsoft Excel, skal du logge på Power Apps, vælge dit miljø, gå til **Produkt**-tabel og derefter vælge **Data**-fanen. Fjern de filtre, der er anvendt. I gruppen **Data** skal du vælge **Rediger data i Excel**. Føj et præfiks eller suffiks til de sammenkoblede produkter, og lad dem derefter udgå.
    * Lad produkterne udgå og slette dem. 

3. Benyt følgende fremgangsmåde for at synkronisere **Enhedsgrupper**, **Måleenheder**, **Varer** og **Ressourcer**:
    1. I [!INCLUDE[prod_short](includes/prod_short.md)] åbnes siden **Dynamics 365 Sales-forbindelseskonfiguration**.
    2. Brug handlingen **Udfør fuldstændig synkronisering** for at åbne siden **Fuld Dataverse-synkroniseringsgennemgang**.
    3. For **VAREENHEDS**-, **RESSOURCEENHEDS**- OG **ENHEDSGRUPPE**-tilknytningerne skal du vælge handlingen **Anbefalet fuldført synkronisering**.
    4. Vælg handlingen **Synkroniser alle**.

    > [!NOTE]
    > For tilknytninger, der endnu ikke er fuldt synkroniserede, synkroniseres disse handlinger helt. Hvis du vil forhindre, at tilknytningerne synkroniseres, skal du slette tilknytningerne fra siden. Derved fjernes de kun fra den aktuelle fulde synkronisering, og tilknytningerne slettes ikke.
    
5. Vælg tilknytningen **VARE-PRODUKT**, og vælg derefter knappen **Genstart**. En genstart opretter nye produkter ud fra varerne i [!INCLUDE[crm_md](includes/crm_md.md)], og der tildeles en ny enhedsgruppe, der er specifik for varen.
6. Vælg tilknytningen **RESSOURCEPRODUKT**, og vælg derefter knappen **Genstart**. En genstart opretter nye produkter ud fra ressourcerne i [!INCLUDE[crm_md](includes/crm_md.md)], og der tildeles en ny enhedsgruppe, der er specifik for ressourcerne.

### Synkroniseringsregler

Følgende tabel viser de regler, der styrer synkroniseringen mellem [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)]. Disse regler er foruden de regler, der er defineret for Dataverse, der også gælder. Få flere oplysninger i [Standardobjekttilknytning](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

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
|Salgsordrer|Når salgsordreintegration er aktiveret, synkroniseres salgsordrer i [!INCLUDE[prod_short](includes/prod_short.md)], der er oprettet fra sendte salgsordrer i [!INCLUDE[crm_md](includes/crm_md.md)], med salgsordrer i [!INCLUDE[crm_md](includes/crm_md.md)], når de frigives. Inden du synkroniserer ordrer, anbefales det, at du først synkroniserer alle de tabeller, der indgår i ordren, f.eks. sælgere og prislister. Feltet Sælgerkode i ordrehovedet definerer ejeren af den sammenkædede tabel i [!INCLUDE[crm_md](includes/crm_md.md)].|

### Synkroniseringsjob for en Sales-integration

Jobbene køres i følgende rækkefølge for at undgå sammenkædning af afhængigheder mellem tabeller. Der er flere tilgængelig jobs i Dataverse. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](./admin-job-queues-schedule-tasks.md).

1. MÅLEENHED – Dynamics 365 Sales-synkroniseringsjob  
2. RESSOURCE-PRODUKT – Dynamics 365 Sales-synkroniseringsjob  
3. VARE - PRODUKT – Dynamics 365 Sales-synkroniseringsjob  
4. KUNDEPRISGRUPPE -PRIS – Dynamics 365 Sales-synkroniseringsjob.
5. SALGSPRIS- PRODUKTPRIS – Dynamics 365 Sales-synkroniseringsjob.
6. BOGFØRTE SALGSFAKTURAER-FAKTURAER – Dynamics 365 Sales-synkroniseringsjob.

### Poster i standardsynkroniseringsjobkø

Følgende tabel viser standardsynkroniseringsjobbene for [!INCLUDE[crm_md](includes/crm_md.md)].  

|Post for jobkø|Description|Retning|Integrationstabeltilknytning|Standardhyppighed for synkronisering (min.)|Standardangivelse for dvale ved inaktivitet (min.)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|MÅLEENHED – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-enhedsgrupper med [!INCLUDE[prod_short](includes/prod_short.md)]-måleenheder.|Fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|MÅLEENHED|30|720<br> (12 timer)|
|RESSOURCE-PRODUKT – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[prod_short](includes/prod_short.md)]-ressourcer.|Fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE-PRODUKT|30|720<br> (12 timer)|
|VARE - PRODUKT – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[prod_short](includes/prod_short.md)]-varer.|Fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|VARE-PRODUKT|30|1440<br> (24 timer)|
|KUNDEPRISGRUPPE -PRIS – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-salgsprislister med [!INCLUDE[prod_short](includes/prod_short.md)]-debitorprisgrupper.| |DEBITORPRISGRUPPER-SALGSPRISLISTER|30|1440<br> (24 timer)|
|SALGSPRIS- PRODUKTPRIS – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produktpriser med [!INCLUDE[prod_short](includes/prod_short.md)]-salgspriser.||PRODUKTPRIS-SALGSPRIS|30|1440<br> (24 timer)|
|BOGFØRTE SALGSFAKTURAER-FAKTURAER – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)] fakturaer med [!INCLUDE[prod_short](includes/prod_short.md)] bogførte salgsfakturaer.|Fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|FAKTURAER-BOGFØRTE SALGSFAKTURAER|30|1440<br> (24 timer)|
|Debitorstatistik - Dynamics 365 Sales-synkroniseringsjob|Opdaterer [!INCLUDE[crm_md](includes/crm_md.md)] konti med seneste [!INCLUDE[prod_short](includes/prod_short.md)] debitordata. I [!INCLUDE[crm_md](includes/crm_md.md)] vises disse oplysninger i **Business Central kontostatistik** i hurtigvisningsformat over konti, der er sammenkædet med [!INCLUDE[prod_short](includes/prod_short.md)]-debitorer.<br /><br /> Disse data skal også opdateres manuelt fra hver debitor-record. Du kan finde flere oplysninger i [Sammenkæd og synkroniser poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Bemærk:**  denne jobkøpost er kun relevant, hvis [!INCLUDE[prod_short](includes/prod_short.md)] integrationsløsningen er installeret i [!INCLUDE[crm_md](includes/crm_md.md)]. |Ikke tilgængelig|Ikke tilgængelig|30|Ikke tilgængelig| 

## Oprette forbindelse til lokale versioner af Business central 2019-udgivelsesbølge 1 og Microsoft Dynamics NAV 2018

Microsoft Power Platform-teamet har [meddelt](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse), at det fraråder Office365-godkendelsestypen. Hvis du bruger en version af [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, der er ældre end Business Central 2019 udgivelsesbølge 1, skal du bruge godkendelsestypen OAuth for at oprette forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)]-online. Fremgangsmåden i dette afsnit beskriver, hvordan du opretter forbindelse til følgende produktversioner:

* Business Central 2019 release wave 1
* Microsoft Dynamics NAV 2018

### Forudsætninger

* Du skal have et Microsoft Azure-abonnement. En prøvekonto kan bruges til registrering af programmer.
* [!INCLUDE[crm_md](includes/crm_md.md)] er konfigureret til at bruge en af følgende godkendelsestyper:

   * Office365 (ældre)

     > [!IMPORTANT]
     > Fra april 2022 vil Office365 (ældre) ikke længere være understøttet. Du kan finde flere oplysninger i [Vigtige ændringer (udfasninger) på vej i Power Apps, Power Automate og Customer Engagement-apps](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   * OAuth

### Sådan oprettes forbindelse mellem Business Central 2019 Release Wave 1 og Dynamics NAV 2018

1. Importér Microsoft Dynamics 365 Business Central-integrationsløsningen til dit [!INCLUDE[crm_md](includes/crm_md.md)]-miljø. Integrationsløsningen findes i mappen CrmCustomization på [!INCLUDE[prod_short](includes/prod_short.md)] eller Dynamics NAV 2018 installations-dvd'en. Afhængigt af produktversionen skal du indlæse en af følgende løsninger:

   * For [!INCLUDE[prod_short](includes/prod_short.md)] indeholder mappen DynamicsNAVIntegrationSolution_v9 og DynamicsNAVIntegrationSolution_v91. løsninger. Den løsning, du skal importere, afhænger af den version af [!INCLUDE[crm_md](includes/crm_md.md)], du opretter forbindelse til. [!INCLUDE[crm_md](includes/crm_md.md)] online kræver løsningen DynamicsNAVIntegrationSolution_v91 integration.
   * For Dynamics NAV 2018 skal du installere DynamicsNAVIntegrationSolution-løsningen.

2. Opret en bruger, der ikke er interaktiv for integration [!INCLUDE[crm_md](includes/crm_md.md)], i miljøet, og tildel brugeren følgende sikkerhedsroller. Du kan finde flere oplysninger i [Oprette en ikke-interaktiv brugerkonto](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Dynamics 365 Business Central-integrationsadministrator
   * Dynamics 365 Business Central-integrationsbruger

   > [!Important]
   > Brugeren må ikke have sikkerhedsrollen Systemadministrator. Du kan heller ikke bruge systemadministratorkontoen som integrationsbruger.

3. Opret en app-registrering til [!INCLUDE[prod_short](includes/prod_short.md)] i Azure-portalen. Du kan finde flere oplysninger i [Registrere et program i Microsoft Entra ID](/powerapps/developer/data-platform/walkthrough-register-app-azure-active-directory). 
  
   > [!NOTE]
   > Det anbefales, at du registrerer app'en i samme lejer som dit Dataverse-miljø, så du ikke skal have tilladelse til at lade app'en få adgang til miljøet. Hvis du registrerer app'en i et andet miljø, skal du logge på Microsoft Entra ID med administratorkontoen for dit Dataverse-miljø og give samtykke.
   >
   > Derudover må den app, du registrerer, ikke have en hemmelighed. Tilslutning af en app med en hemmelighed til Dataverse er kun tilgængelig i Business Central 2020 Release Wave 1 og nyere.
  
4. Afhængigt af produktversionen skal du gennemføre et af følgende trin:

    * I [!INCLUDE[prod_short](includes/prod_short.md)] søges efter **Microsoft Dynamics 365-forbindelsesopsætning**, og vælg derefter det relaterede link. 
    * I Dynamics NAV 2018 søges efter **Microsoft Dynamics 365 for Sales-forbindelsesopsætning**, og vælg derefter det relaterede link.

5. Vælg indstillingen for OAuth i feltet **godkendelsestype**. 
6. Vælg den CRM SDK-version, der passer til den løsningsversion, du har importeret i trin 1.

   > [!NOTE]
   > Dette trin er kun relevant for [!INCLUDE[prod_short](includes/prod_short.md)].

7. Angiv URL-adressen til dit [!INCLUDE[crm_md](includes/crm_md.md)]-miljø og derefter brugernavn og adgangskode for integrationsbrugeren. 

   * Brug i [!INCLUDE[prod_short](includes/prod_short.md)] feltet **Serveradresse**.
   * I Dynamics NAV 2018 skal du bruge feltet **Dynamics 365 Sales URL**.

8. I feltet **Forbindelsesstreng** skal du angive id for app-registrering. Dette felt indeholder to tokens, hvor ID'ET for programmet skal angives.

   |Token           |Beskrivelse  |
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

## Se også

[Konfigurere brugerkonti til integration med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Oprette en forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Synkronisere Business Central og [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Forberedelse af Dynamics 365 Sales til integration i det lokale miljø](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]
