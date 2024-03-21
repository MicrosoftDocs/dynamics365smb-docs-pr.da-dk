---
title: 'OneDrive for Business, ofte stillede spørgsmål'
description: Få svar på nogle typiske spørgsmål om arbejde med OneDrive for Business og Business Central.
author: brentholtorf
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'OneDrive, integration, share, browser'
ms.date: 09/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# OneDrive for Business, ofte stillede spørgsmål

[!INCLUDE [online_only](includes/online_only.md)]

I denne artikel besvares nogle af de spørgsmål, du kan have om at arbejde med OneDrive og [!INCLUDE [prod_short](includes/prod_short.md)].

## Fungerer dette sammen med alle [!INCLUDE[prod_short](includes/prod_short.md)]-klienter?

Ja. Du kan åbne filer i OneDrive fra [!INCLUDE[prod_short](includes/prod_short.md)]-mobil-apps, når du får vist kortdetaljer i Microsoft Teams eller endda fra Outlook-tilføjelsesprogrammet.  

## Svarer OneDrive til SharePoint i forbindelse med at gemme filer?

Som en del af dit Microsoft 365-abonnement giver din virksomhed dig OneDrive, dit fillager i skyen. OneDrive er som standard privat, hvor du organiserer indholdet og vælger, hvilke filer eller mapper du vil dele med. SharePoint indeholder derimod et arkivlager med den sky, som deles med andre i din organisation.  

## Understøtter [!INCLUDE[prod_short](includes/prod_short.md)] forbruger OneDrive?

Nej. Denne integration er udelukkende beregnet til OneDrive for Business og understøtter kun din arbejdskonto. 

## Understøttes OneDrive for Business alle forretningsplaner?

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter ikke enkeltstående planer for OneDrive for Business. OneDrive skal købes som en del af Microsoft 365 Business- eller Enterprise-plan. Du kan finde flere oplysninger i [sammenligne OneDrive-skyens lagerpriser og planer](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## Hvor kan jeg se OneDrive-servicetilstand?

Administratorer kan få adgang til dette Dashboard servicetilstand som en del af Microsoft 365 Administration. Dashboardet omfatter OneDrive-service tilgængelighed. Gå til [https://admin.microsoft.com/Adminportal/Home?#/servicehealth](https://admin.microsoft.com/Adminportal/Home?#/servicehealth).
 
## Er OneDrive-integration tilgængelig for [!INCLUDE[prod_short](includes/prod_short.md)] lokalt?

Ja, men i modsætning til [!INCLUDE[prod_short](includes/prod_short.md)]-online kræves yderligere opsætning. Du kan finde flere oplysninger i [Konfigurere Business Central lokalt](admin-onedrive-integration-onpremises.md).  

## Opretter [!INCLUDE[prod_short](includes/prod_short.md)] lokal forbindelse til SharePoint-serveren?

Nej. Denne installationskombination understøttes ikke, selvom SharePoint-serveren har aktiveret mit websted.  

## Opretter [!INCLUDE[prod_short](includes/prod_short.md)] online forbindelse til SharePoint-serveren?

Nej. Denne installationskombination understøttes ikke, selvom SharePoint-serveren har aktiveret mit websted.  

## Hvordan fungerer dette i en organisation med flere miljøer?

Integrationen forudsætter, at firmanavne er entydige på tværs af [!INCLUDE[prod_short](includes/prod_short.md)]-miljøer. Hvis virksomhedens navne er entydige på tværs af organisationen, vil åbning af en fil i OneDrive kopiere filen til en mappe, der kaldes efter det aktuelle regnskab. Hvis firmanavne ikke er entydige på tværs af miljøer, bliver filer fra identiske virksomhedsnavne placeret i samme mappe.  

## Vi har ændret virksomhedsnavnet. Hvad sker der med mine tidligere filer?

[!INCLUDE[prod_short](includes/prod_short.md)] overflytter ikke automatisk filer, du tidligere har åbnet i OneDrive, til den nye mappe. Når du har omdøbt virksomheden, vil funktionen Åbn i OneDrive-handling kopiere filer til en mappe, der har det nye firmanavn.   

## Ved tilknytning af filer til [!INCLUDE[prod_short](includes/prod_short.md)], hvordan tilknytter jeg filer fra OneDrive?

[!INCLUDE[prod_short](includes/prod_short.md)] angiver ikke en skyfilvælger. Du skal hente filen fra OneDrive til din enhed og derefter overføre den til [!INCLUDE[prod_short](includes/prod_short.md)]. 

## Jeg vil åbne filer i SharePoint i stedet. Hvordan gør jeg det?

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder ikke funktioner, der kan bruges til at kopiere filer til SharePoint og åbne dem fra et SharePoint-bibliotek. Kontakt din Microsoft-partner for at få et overblik over dine muligheder, eller Søg efter apps på AppSource.  

## Hvordan slår jeg integration til OneDrive?

Kør **OneDrive-installationens** assisterede opsætningsvejledning, og deaktiver **Brug OneDrive til appfunktioner** og **Brug OneDrive til systemfunktioner**. 

## Skal jeg bruge SharePoint-siden Forbindelsesopsætning til at oprette forbindelse til SharePoint?

Dette er en ældre funktion, hvor alle [!INCLUDE[prod_short](includes/prod_short.md)]-filer fra alle brugere sendes til en enkelt SharePoint-mappe. Det anbefales, at du ikke konfigurerer oversigtspanelet Delte dokumenter på siden **Konfiguration af SharePoint-forbindelse**, da siden er [forældet](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup) og vil blive fjernet i 2023 udgivelsesbølge 2, version 23.0.  Det anbefales, at du bruger **Opsætning af OneDrive** i stedet.  

## Hvilken version af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter OneDrive?

Integration med OneDrive blev tilgængelig i 2021 Release Wave 2.  

## <a name="features"></a>Hvilke funktioner påvirkes af OneDrive-integrationen?

I den assisterede opsætningsvejledning for **Opsætning af OneDrive** til opsætning af OneDrive-integration kan du aktivere eller deaktivere funktioner til håndtering af Business Central-filer i OneDrive. Funktionerne er opdelt i to indstillinger:

|Indstilling|Beskrivelse|
|------|----------|
|**Brug OneDrive for appfunktioner**|Hvis du aktiverer denne indstilling, gøres handlingerne **Åbn i OneDrive** og **Del** tilgængelige på filer i Business Central, ligesom filer vedhæftet dokumenter eller i rapportindbakken. Disse handlinger gør det muligt for brugere at kopiere, åbne og dele filer i OneDrive. Du kan finde flere oplysninger i [Åbning og deling af Business Central-filer i OneDrive](across-share-onedrive.md).
|**Brug OneDrive til systemfunktioner**|Hvis du aktiverer denne funktion, aktiveres følgende funktioner:<ul><li> Funktionen **Åbn i Excel** og **Rediger i Excel** på listesider kopierer automatisk Excel-filen til OneDrive og åbner den i Excel Online. Du kan finde flere oplysninger i [Vise og redigere i Excel](across-work-with-excel.md).</li><li> Når du sender en rapport til en Excel- eller Word-fil, vil filen automatisk blive kopieret til OneDrive og derefter åbnes i Excel eller Word Online. Du kan få flere oplysninger i [Gemme en rapport i en fil](ui-work-report.md#saving-a-report-to-a-file).|

## Fortsætter Microsoft med at forbedre integration til OneDrive?

Hos Microsoft lytter vi hele tiden til feedback fra vores forskellige grupper af brugere og handler på de mest interessante forslag. Du kan finde flere oplysninger om, hvad der er det næste for integrationer med Microsoft 365-apps, i [frigivelsesplanen for Dynamics 365](/dynamics365-release-plan/2021wave1).  

Hvis du vil deltage i forbedring af OneDrive-integrationen eller have en idé, der kan forbedre fildeling og samarbejde i [!INCLUDE[prod_short](includes/prod_short.md)], kan du tilføje en idé eller stemme for eksisterende ideer på [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## Fejlfinding

Dette afsnit indeholder oplysninger om, hvordan du identificerer og løser problemer, der kan opstå, når du bruger OneDrive sammen med [!INCLUDE[prod_short](includes/prod_short.md)].  

### Business central kan ikke finde OneDrive

Når denne meddelelse vises, kan du ikke fastslå placeringen af din OneDrive for Business, skal du kontakte din partner for at konfigurere det. ", kontroller, om brugeren har haft adgang til OneDrive mindst én gang. Hvis de ikke har det, skal du bede personen om at gå til portal.office.com/onedrive for at konfigurere den. Det kan tage lidt tid. Hvis meddelelsen stadig vises efter 24 timer, skal du kontakte support.  
 
### Jeg har problemer med at dele fra Outlook

Se [Kan ikke dele OneDrive-filer fra Outlook.com](https://support.microsoft.com/en-us/office/can-t-share-onedrive-files-from-outlook-com-05d4cb21-40a2-40e3-b111-82cddb82d22f) i Microsoft Support.

### Handlingerne Åbn i OneDrive og Del mangler

Du kan kontrollere et par ting:

- Kontrollér, at programmets funktioner til OneDrive er aktiveret i **OneDrive-konfigurationens** vejledning til assisteret opsætning. Se [Konfigurere OneDrive ved hjælp af OneDrive-konfiguration](admin-onedrive-integration.md#configure-onedrive-using-onedrive-setup).
- Kontrollér, at Microsoft OneDrive er indstillet til **Accepterer** på siden **Status for meddelelser om beskyttelse af personlige oplysninger**. Se [Status for meddelelser om beskyttelse af personlige oplysninger](privacy-notices-status.md).

## Se også

[Business Central og OneDrive-integration](across-onedrive-overview.md)  
[Administration af OneDrive-integration med Business Central](admin-onedrive-integration.md)  
[Åbner Business Central-filer i OneDrive](across-share-onedrive.md)  
