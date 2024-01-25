---
title: Konfigurer Copilot- og AI-funktioner
description: 'Denne artikel forklarer, hvordan du aktiverer Copilot i et miljø.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/29/2023
ms.custom: bap-template
ms.search.form: 7775
ms.collection:
  - bap-ai-copilot
---

# Konfigurere Copilot- og AI-funktioner 

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

I denne artikel forklares det, hvordan du styrer brugernes adgang til Copilot og andre AI-funktioner i Business Central. Denne opgave udføres af en administrator. Copilot er en systemfunktion og en integreret del af Business Central. I lighed med de fleste systemfunktioner giver du ikke adgang til individuelle brugere, og du kan heller ikke slå Copilot til eller fra. Copilot tilbyder dog datastyringskontrol og mulighed for at deaktivere individuelle Copilot- og AI-funktioner for hvert miljø. Der er forskellige niveauer af adgangskontrol til AI-funktioner, afhængigt af funktionen:

- Tillad dataflytning på tværs af geografiske områder

  Denne opgave kræves kun, hvis dit Business Central-miljø er i et andet geografisk område end den Azure OpenAI-tjeneste, det bruger. [Få mere at vide](#allow-data-movement-across-geographies)

- Aktivér funktionen på siden **Copilot- og AI-funktioner**. [Få mere at vide](#activate-features)

- Aktivér den specifikke funktion, hvis den stadig styres af **Funktionsstyring**.

  I udgivelsesbølge 2 i 2023 er både forslagene til marketingtekst og funktionerne til hjælp til bankkontoafstemning inkluderet under **Funktionsstyring**. [Få mere at vide](#enable-feature-in-feature-management)

Hvis nogle af disse krav ikke er opfyldt, kan funktionen ikke bruges.

## Forudsætninger

- Du bruger Business Central online, version 23.1 eller nyere. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Du har administrator- eller supertilladelser i Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## Tillade dataflytning på tværs af geografiske områder

Denne opgave gælder kun, hvis kontakten **Tillad dataflytning** vises øverst på siden **Copilot- og AI-funktioner**. Hvis linket **Hvordan styrer jeg mine copilotdata?** vises i stedet for **Tillad databevægelse** kontakten, skal du springe over dette trin.

![Viser et skærmbillede af knappen Tillad databevægelse på Copilot & AI-egenskaber side.](media/allow-data-movement-v2.png)

Kontakten **Tillad dataflytning** angiver, at placeringen af dit Business Central-miljø - dvs. det geografiske område, hvor data behandles og lagres - ikke er det samme som det Azure OpenAI-tjenestegeografiske område, der bruges af Copilot. Hvis du vil aktivere Copilot, skal du tillade dataflytning mellem geografiske områder. Du kan få mere at vide om dataflytning ved at gå til [Copilot-dataflytning på tværs af geografiske områder](ai-copilot-data-movement.md). 

Hvis du vil tillade dataflytning uden for dit geografiske område, skal du udføre følgende trin:

1. Søg, og åbn siden **Copilot- og AI-funktioner** i Business central.
1. Aktivér kontakten **Tillad dataflytning** .

Du kan fravælge ved at slå kontakten  **Tillad dataflytning** fra. Når en Azure OpenAI-tjeneste bliver tilgængelig i dit Business Central-miljøgeografi, forbindes dit miljø automatisk til den, og kontakten er ikke længere tilgængelig. 


<!--
| Australia, United Kingdom, United States | Within the respective geographical region |
| Europe, France, Germany, Norway, Switzerland  | Sweden or Switzerland |
| Asia Pacific, Brazil, Canada, India, Japan, Singapore, South Africa, South Korea, United Arab Emirates  | United States |-->



<!--Note

If your environment is hosted in North America, Copilot will use an Azure OpenAI endpoint in North America to process your data.
If your environment is hosted in Europe, Copilot will use an Azure OpenAI endpoint in Europe to process your data.
If your environment is hosted anywhere else, Copilot will use an Azure OpenAI endpoint outside of the region in which the environment is hosted.
To opt in 

Copilot and other AI capabilities use Azure OpenAI Service.  and are provided by default to only those customers with environments that have United States as their geography for data processing and storage. While the Azure OpenAI Service is available in multiple geographies including Australia, Canada, United States, France, Japan and UK, Copilot does not follow the same regional rollout schedule.

Meanwhile, customers with environments outside the United States can use Copilot AI features by opting in to share relevant data with the Azure OpenAI Service in United States or Switzerland.

The information in the following table outlines the Azure OpenAI service that's used by the Copilot services based on the geography of their Dynamics 365 environment when they opt-in to share data.-->
## Aktivér funktioner

Alle Copilot- og AI-funktioner er aktive som standard, når de gøres tilgængelige i forhåndsvisning eller bliver almindeligt tilgængelige. Ved hjælp af siden **Copilot- og AI-funktioner** kan du slå individuelle funktioner til eller fra for alle brugere.

1. Søg, og åbn siden **Copilot- og AI-funktioner** i Business central.

1. Siden viser alle tilgængelige Copilot- og AI-relaterede funktioner og deres aktuelle status, som enten kan være aktiv eller inaktiv. Funktionerne er opdelt i to sektioner: En sektion for funktioner i forhåndsversion og en anden for funktioner, der er generelt tilgængelige. 

   [![Viser Business Central-rollecenter og kontrollisten til Copilot](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Hvis du vil slå en funktion til, skal du vælge den på listen og derefter vælge handlingen **Aktivér**.
   - Hvis du vil slå en funktion fra, skal du markere den og derefter vælge handlingen **Deaktivér**. 


## Aktivér funktion i Funktionsstyring

Når individuelle Copilot-funktioner frigives i Business Central mindre opdateringer, er disse funktioner valgfri indtil næste større opdatering. **Funktionsstyring** bruges til at slå funktioner til eller fra i prøveversion, f.eks. bankafstemning, og visse funktioner, der er generelt tilgængelige, f.eks. forslag til varemarketingtekst. [Få mere at vide om funktionsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. I Business Central skal du søge efter og åbne siden **Funktionsstyring**.
2. Hvis du vil aktivere en funktion, skal du angive kolonnen **Aktiveret til** til **Alle brugere**. Hvis du vil deaktivere en funktion, skal du angive kolonnen **Aktiveret til** til **Ingen**. Brug følgende tabel som en hjælp til at bestemme den kontakt, der gælder for den Copilot- og AO-funktion, du vil aktivere:

   - **Forhåndsversionsfunktion: Bankkontoafstemning med Copilot** vedrører funktionen til hjælp til bankkontoafstemning.
   - **Funktionsforhåndsversion: Opret AI-drevne produktbeskrivelser med Copilot** vedrører funktionen til forslag til marketingtekst.

   Du kan finde flere oplysninger om funktionsstyring generelt i [Funktionsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management).

## Tildele brugeradgang 

Copilot- og AI-funktioner kan tilbyde funktionalitet beregnet til alle brugere på tværs af din organisation eller til specifikke brugerroller. De fleste Copilot- og AI-funktioner tilbyder adgangskontrol ved hjælp af tilladelser og tilladelsessæt i Business Centrals tilladelsesstyringssystem. [Få mere at vide om tilladelser og tilladelsessæt](ui-define-granular-permissions.md).

For at give eller nægte adgang til specifikke Copilot- og AI-funktioner skal du konsultere dokumentationen eller udgiveren af ​​den funktion for at identificere, hvilke tilladelser der kræves. 

## Næste trin

Når du har aktiveret og givet dit samtykke til funktionerne, er du klar til at prøve dem. Gå til:

- [Tilføje marketingtekst til varer](item-marketing-text.md) 
- [Afstemme ved hjælp af hjælp til bankkontoafstemning](bank-reconciliation-with-copilot.md) 

## Se også

[Fejlfinde Copilot- og AI-funktioner](ai-copilot-troubleshooting.md)  
[Oversigt over forslag til marketingtekst](ai-overview.md)   
[Ofte stillede spørgsmål om forslag til marketingtekst](faqs-marketing-text.md)  
