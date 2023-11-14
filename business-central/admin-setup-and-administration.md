---
title: Administrative opgaver i Business Central
description: 'Nogle af opgaverne i Business Central kræver central administration og installation. Se, hvilke opgaver det er, og få at vide, hvad du skal gøre.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/11/2023
ms.custom: bap-template
---
# Administrationsopgaver

Centrale administrationsopgaver udføres som regel af én rolle i firmaet. Omfanget af disse opgaver kan afhænge af firmaets størrelse og administratorens jobansvar. Disse opgaver kan omfatte styring af databasesynkronisering af job og e-mail-køer, oprettelse af brugere og tilpasning af brugergrænsefladen.  

Det er vigtigt, at der indtastes korrekte opsætningsværdier fra starten, for at ny forretningssoftware kan fungere effektivt. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en række opsætningsvejledninger, som hjælper dig med opsætningen af basisoplysninger. Du kan finde flere oplysninger i [Konfigurere Business Central](setup.md).

> [!NOTE]
> Du kan bruge dataoverførselsværktøjerne til at overflytte eksisterende data til [!INCLUDE [prod_short](includes/prod_short.md)] online. Du kan oprette en ny virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)] med konfigurationspakker, der afkorter installationstiden, forbedrer implementeringens kvalitet, introducerer en tilgang til implementeringer, der kan gentages, og forbedrer produktiviteten ved at automatisere og forenkle tilbagevendende opgaver. Du kan finde flere oplysninger i [Overførsel af lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data).

Du kan understøtte dine opsætningsbeslutninger med anbefalinger for udvalgte konfigurationsfelter, der er kendt for potentielt at gøre løsning ineffektiv, hvis de opsættes forkert.  

Superbruger eller administrator kan konfigurere Data Exchange Framework så brugere kan eksportere og importere data i bank og løn filer, f.eks. til forskellige likviditetsstyringsprocesser. Du kan finde flere oplysninger i [Udveksle data elektronisk](across-data-exchange.md).

Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.  

|**Hvis du vil**|**Se**|  
|------------|-------------|
|Definere, hvem der kan logge på [!INCLUDE[prod_short](includes/prod_short.md)], ved at oprette brugere i Microsoft 365 Administration i henhold til produktlicenserne.|[Oprette brugere i henhold til licenser](ui-how-users-permissions.md)|
|Tildele tilladelser til brugere, ændre tilladelsessæt og gruppere brugere for at opnå nem styring af tilladelser.|[Tildele tilladelser til brugere og grupper](ui-how-users-permissions.md)|
|Tilføj brugere, administrer tilladelser og få adgang til data og tildel roller.|[Administrere profiler](admin-users-profiles-roles.md)|
|Administrere brugerindstillinger, f.eks. virksomhed, rolle, sprog, område og tidszone.|[Brugerindstillinger](admin-manage-user-settings-preferences.md)|
|Opsættelse af printere og angivelse af, hvilke rapporter der skal udskrives på hvilke printere.|[Installation af printere](ui-specify-printer-selection-reports.md)|
|Klassificere datafølsomheder for felter så du kan svare på anmodninger fra dataemner vedrørende deres personlige oplysninger.|[Klassificere datafølsomhed](admin-classifying-data-sensitivity.md)|
|Svare på anmodninger fra dataemner vedrørende deres personlige oplysninger.|[Svare på anmodninger om personlige oplysninger](admin-responding-to-requests-about-personal-data.md)|
|Oprette en ny koncernvirksomhed ved hjælp af skabeloner|[Opret nye virksomheder](about-new-company.md)|
|Spore alle de direkte modifikationer, som brugere foretager af data i databasen for at identificere oprindelsen til fejl og dataændringer.|[Logføre ændringer](across-log-changes.md)|  
|Angive engangsanmodninger eller gentagne anmodninger om at køre rapporter eller kodeenheder.|[Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md)|  
|Administrere, slette eller komprimere dokumenter|[Slet dokumenter](admin-manage-documents.md)|  
|Vis sider, kodeenheder og forespørgsler som webtjenester.|[Udgive en webtjeneste](across-how-publish-web-service.md)|
|Som en del af oprettelsen af Connect Apps mellem [!INCLUDE[prod_short](includes/prod_short.md)] og tredjepartsløsninger via REST API'erne skal du definere skabeloner, der bruges til at udfylde tomme egenskaber for en enhed, når du opretter en BOGF-handling via et API.|[Konfigurere API-skabeloner](admin-configuring-api-template.md)|
|Krypter data på [!INCLUDE[prod_short](includes/prod_short.md)] Server ved at oprette nye eller importere eksisterende krypteringsnøgler, som du aktiverer på serveren.|[Administrere datakryptering](admin-manage-data-encryption.md)|
|Opret forbindelse fra Dynamics 365 Sales til [!INCLUDE[prod_short](includes/prod_short.md)] for at opnå problemfri integration mellem debitorrelationer og ordrebehandling i lead-til-kontant-processen.|[Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Ændre, hvilke felter og handlinger der vises i brugergrænsefladen, så det passer til virksomhedens forretningsprocesser, og så løsningen kan udvides med apps.|[Tilpas [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|

## Administration i administrationscenteret

Interne og uddelegerede administratorer har adgang til [!INCLUDE [prod_short](includes/prod_short.md)] Administration, hvor de kan konfigurere, overvåge og foretage fejlfinding i [!INCLUDE [prod_short](includes/prod_short.md)]-miljøer. Den følgende tabel indeholder nogle af de vigtige opgaver med links til artikler med beskrivelser af dem.  

|**Hvis du vil**|**Se**|  
|------------|-------------|
|Få mere at vide om de værktøjer, du kan bruge til fejlfinding.|[Teknisk support](/dynamics365/business-central/dev-itpro/technical-support)|
|Overvåge brug og foretage fejlfinding af sessioner|[Miljøtelemetri i Business Central Administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Administrere brugersessioner, herunder annullering af en session, hvis brugeren er spærret.|[Administrere sessioner](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions)|
|Konfigurere lejeren til at sende telemetridata til Azure Application Insights for at opnå bedre analyse og fejlfinding.|[Aktivere afsendelse af telemetri til Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights)|

## Se også

[Forretningsfunktioner](across-business-functionality.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Blive køreklar](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
