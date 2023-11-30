---
title: Copilot-dataflytning på tværs af geografiske områder
description: 'Få mere at vide om, hvordan data, der bruges i copilotfunktioner i Dynamics 365 Business Central, flytter på tværs af geografiske områder, hvor Azure OpenAI-tjenesten ikke er tilgængelig som standard.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection: null
ms.date: 11/15/2023
ms.custom: bap-template
---

# <a name="copilot-data-movement-across-geographies"></a>Copilot-dataflytning på tværs af geografiske områder

Copilot er tilgængelig i alle understøttede [Business Central-geografiske lande/områder](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) i Business Central. Copilot bruger dog Microsoft Azure OpenAI-tjenester, som i øjeblikket kun er tilgængelig for Business Central i nogle geografiske områder. Det betyder, at hvis dit miljø er placeret et andet sted, skal data fra Copilot- og generative AI-funktioner overføres uden for dit geografiske område og kan behandles og gemmes uden for din overholdelsesgrænse. Data omfatter AI-prompter og dine forretningsdata, der bruges af eller genereres af Copilot. I dette tilfælde skal du vælge at tillade dataflytning til en Azure OpenAI-tjeneste i et andet geografisk område. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Hvis dit miljø er placeret i samme Azure-område som Azure OpenAI-tjenesten, og det automatisk opretter forbindelse til Azure OpenAI-tjenesten, er der ingen mulighed, og der kræves ingen en gangs-konfiguration.

> [!NOTE]
> Individuelle Copilot- og generative AI-funktioner er muligvis ikke tilgængelige i alle Business Central-miljølande/områder. Rådfør dig med udgiveren af hver funktion for at forstå tilgængelighed.
> 
> Copilot- og generative AI-funktioner fra udgivere, der ikke er fra Microsoft, f.eks. dem, der stammer fra tilpasninger eller AppSource-apps, du installerer, definerer hver især deres egne specifikke Azure OpenAI-tjenesteområder. Kontakt udgiveren af udvidelsen for at finde ud af, hvilke regionale Azure-tjenester der bruges af udvidelsen. 

### <a name="azure-openai-service-geographies"></a>Geografiske områder for Azure OpenAI-tjeneste

Følgende tabel viser den Azure OpenAI-tjenestes geografi, der bruges af Copilot, baseret på Azure-området i et Business Central-miljø. Disse oplysninger er vigtige, når du beslutter, om du vil tilvælge dataflytning på tværs af geografiske områder. Du kan identificere Azure-området for dit miljø i Business Central Administration, hvor det kaldes Azure-området (se [Administrere miljøer i Administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments))

| Miljø Azure-regionen| Geografiske områder for Azure OpenAI-tjeneste|Admin handling påkrævet for at låse Copilot op| 
| - | - | - |
|Asien (øst, sydøst) |USA|Ja|
|Australien (sydøst)| USA |Ja, indtil opdatering 23.2 |
|Brasilien (syd) |USA|Ja|
|Canada (central, øst)|USA|Ja|
|Europa (vest, nord)| Sverige eller Schweiz |Ja|
|Frankrig (central, syd)| Sverige eller Schweiz |Ja|
|Tyskland (nord, vestlige central)| Sverige eller Schweiz |Ja|
|Indien (central, syd)|USA|Ja|
|Japan (øst, vest)|USA|Ja|
|Korea (central, syd)|USA|Ja|
|Norge (øst, vest)|Sverige eller Schweiz |Ja|
|Sydafrika (nord, vest)|USA|Ja|
|Schweiz (nord, vest) |Sverige eller Schweiz |Ja|
|Arabiske Emirater (nord, vest)|USA|Ja|
|Storbritannien (syd, vest)|Storbritannien|Ja, indtil opdatering 23.2|
|USA (central, øst, nordcentral, sydcentral, vest) |USA|Nej|

> [!NOTE]
> Når en Azure OpenAI-tjeneste bliver tilgængelig i dit Business Central-geografiske område, overgår dit miljø automatisk til at bruge Azure OpenAI-tjenesten, og det er ikke nødvendigt eller endda muligt at tilmelde sig.  
<!--

BC geos base on https://dynamics.microsoft.com/en-us/availability-reports/georeport/
case "AUSTRALIAEAST":
            case "AUSTRALIASOUTHEAST":
                return new CapiRegion("au", 2);
            case "BRAZILSOUTH":
                return new CapiRegion("br", 2);
            case "CANADACENTRAL":
            case "CANADAEAST":
                return new CapiRegion("ca", 2);
            case "CENTRALINDIA":
            case "SOUTHINDIA":
                return new CapiRegion("in", 1);
            case "EASTASIA":
                return new CapiRegion("as", 2);
            case "EASTUS":
            case "EASTUS2":
            case "SOUTHCENTRALUS":
            case "CENTRALUS":
            case "NORTHCENTRALUS":
            case "WESTUS":
            case "US":
                return new CapiRegion("us", 9, HasGpt4InGeo: true, HasTurboInGeo: true);
            case "FRANCECENTRAL":
            case "FRANCESOUTH":
                return new CapiRegion("fr", 1);
            case "GERMANYNORTH":
            case "GERMANYWESTCENTRAL":
                return new CapiRegion("de", 1);
            case "JAPANEAST":
            case "JAPANWEST":
                return new CapiRegion("jp", 1);
            case "KOREACENTRAL":
            case "KOREASOUTH":
                return new CapiRegion("kr", 1);
            case "NORWAYEAST":
            case "NORWAYWEST":
                return new CapiRegion("no", 1);
            case "SOUTHAFRICANORTH":
            case "SOUTHWESTAFRICA":
                return new CapiRegion("za", 1);
            case "SOUTHEASTASIA":
                return new CapiRegion("sg", 1);
            case "SWITZERLANDNORTH":
            case "SWITZERLANDWEST":
                return new CapiRegion("ch", 1, HasTurboInGeo: true);
            case "UKSOUTH":
            case "UKWEST":
                return new CapiRegion("uk", 2);
            case "NORTHEUROPE":
            case "WESTEUROPE":
                return new CapiRegion("eu", 10);
            case "UAENORTH":
            case "UAECENTRAL":
                return new CapiRegion("ae", 1);

-->

## <a name="next-steps"></a>Næste trin

Du vælger at tillade dataflytning på tværs af geografiske områder fra siden [Copilot- og AI-funktioner](https://businesscentral.dynamics.com/?page=7775) . Du kan få mere at vide ved at gå til [Tillad dataflytning på tværs af geografiske områder](enable-ai.md#allow-data-movement-across-geographies).
