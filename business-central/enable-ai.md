---
title: Konfigurer Copilot- og AI-funktioner
description: 'Denne artikel forklarer, hvordan du aktiverer Copilot i et miljø.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 04/16/2024
ms.custom: bap-template
ms.search.form: 7775
ms.collection:
  - bap-ai-copilot
---

# Konfigurere Copilot- og AI-funktioner 

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

I denne artikel forklares det, hvordan du styrer brugernes adgang til Copilot og andre AI-funktioner i Business Central. Denne opgave udføres af en administrator. Copilot er en systemfunktion og en integreret del af Business Central. I lighed med de fleste systemfunktioner giver du ikke adgang til individuelle brugere, og du kan heller ikke slå Copilot til eller fra. Copilot tilbyder dog datastyringskontrol og mulighed for at deaktivere individuelle Copilot- og AI-funktioner for hvert miljø. Der er forskellige niveauer af adgangskontrol til AI-funktioner, afhængigt af funktionen:

- Tillad dataflytning på tværs af geografiske områder.

  Denne opgave kræves kun, hvis dit Business Central-miljø er i et andet geografisk område end den Azure OpenAI-tjeneste, det bruger. [Få mere at vide](#allow-data-movement-across-geographies)

- Aktivér funktionen på siden **Copilot- og AI-funktioner**. [Få mere at vide](#activate-features)

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
- Enable the specific feature if it's governed by **Feature Management**.

  Check whether  of 2024 release wave 1, chat with Copilot, marketing text suggestions, and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)
<!-- 
- Enable the specific feature, if it's still governed by **Feature Management**.

  In 2023 release wave 2, both the marketing text suggestions and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)-->

Hvis nogle af disse krav ikke er opfyldt, kan funktionen ikke bruges.

## Forudsætninger

- Du bruger Business Central Online.
- Du er [administrator](#requirements-for-being-an-administrator) i Business Central.

## Tillade dataflytning på tværs af geografiske områder

Denne opgave gælder kun, hvis kontakten **Tillad dataflytning** vises øverst på siden **Copilot- og AI-funktioner**. Hvis linket **Hvordan styrer jeg mine copilotdata?** vises i stedet for **Tillad databevægelse** kontakten, skal du springe over dette trin.

![Viser et skærmbillede af knappen Tillad databevægelse på Copilot & AI-egenskaber side.](media/allow-data-movement-v2.png)

Kontakten **Tillad dataflytning** angiver, at placeringen af dit Business Central-miljø - dvs. det geografiske område, hvor data behandles og lagres - ikke er det samme som det Azure OpenAI-tjenestegeografiske område, der bruges af Copilot. Hvis du vil aktivere Copilot, skal du tillade dataflytning mellem geografiske områder. Du kan få mere at vide om dataflytning ved at gå til [Copilot-dataflytning på tværs af geografiske områder](ai-copilot-data-movement.md). 

Hvis du vil tillade dataflytning uden for dit geografiske område, skal du udføre følgende trin:

1. Søg, og åbn siden **Copilot- og AI-funktioner** i Business central.
1. Aktivér kontakten **Tillad dataflytning**.

   Kontakten **Tillad dataflytning** er som standard aktiveret for miljøer i Azure-områderne Vesteuropa og Nordeuropa.

Du kan fravælge dataflytning ved at slå kontakten **Tillad dataflytning** fra. Når en Azure OpenAI-tjeneste bliver tilgængelig i dit Business Central-miljøgeografi, forbindes dit miljø automatisk til den, og kontakten er ikke længere tilgængelig.

<!-- Don't review
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

<!-- don't review 

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
## Enable feature in Feature Management

When individual Copilot capabilities are released in Business Central minor updates, these capabilities are optional until the next major update. **Feature Management** is used to turn on or off features that are in preview, like bank reconciliation, and some features that are generally available, like marketing text suggestions. [Learn more about feature management](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. In Business Central, search for and open the **Feature Management** page.
2. To enable a feature, set the **Enabled for** column to **All users**. To disable a feature, set the **Enabled for** column to **None**. Use the following table to help you determine the switch that applies to the Copilot and AI capability you want to enable:

   - **Feature Preview: Bank account reconciliation with Copilot** enables the bank account reconciliation assist feature.
   - **Feature Preview: Chat with Copilot** enables the chat with Copilot feature.
   - **Feature preview: Create AI-powered product descriptions with Copilot** enables the marketing text suggestions feature.

   For more information about feature management in general, go to [Feature Management](/dynamics365/business-central/dev-itpro/administration/feature-management).-->

## Tildele brugeradgang

Copilot- og AI-funktioner kan tilbyde funktionalitet beregnet til alle brugere på tværs af din organisation eller til specifikke brugerroller. De fleste Copilot- og AI-funktioner tilbyder adgangskontrol ved hjælp af tilladelser og tilladelsessæt i Business Centrals tilladelsesstyringssystem. [Få mere at vide om tilladelser og tilladelsessæt](ui-define-granular-permissions.md).

Følgende tabel viser de tilladelser, der kræves for at bruge Copilot-funktioner, der leveres af Business Central.

|Copilot-funktioner|Nødvendige tilladelser|
|-|-|
|Analyseassistance|**DATA ANALYSIS - EXEC** tilladelsessæt eller udfør tilladelse til systemobjektet 9640 **Tillad dataanalysetilstand**. Det er de samme tilladelser, der kræves for at få adgang til analysetilstanden.|
|Assistance til bankafstemning|Tilladelse på side 7250 **Bank Acc. Rec. AI Forslag** og side 7252 **Trans. Til GL Acc. AI-forslag**.|
|Chat |Der er ingen tilladelser eller tilladelsessæt, der styrer adgangen til chat pr. bruger. Hvis chat er aktiveret, er den tilgængelig for alle brugere.|
|Tilknyt e-dokumenter |Tilladelse på side 6166 **PO Copilot-forslag til e-dokument**|
|Forslag til marketingtekst |Tilladelse på side 5836 **Copilot Marketing Text**|
|Salgslinjeforslag |Tilladelse på side 7275 **Salgslinje AI-forslag** og side 7276 **Salgslinje AI-forslag Sub**|

For at give eller nægte adgang til specifikke ikke-Microsoft Copilot- og AI-funktioner skal du konsultere dokumentationen eller udgiveren af den funktion for at identificere, hvilke tilladelser der kræves.

## Krav til at være administrator

Du skal enten have SUPER-tilladelser i Business Central-brugerkontoen eller en af følgende Business Central-licenser:

- Stedfortræderadministrator
- Delegeret helpdesk
- Global administrator
- BC-administrator
- D365 Administrator

Business Central tilbyder endnu ikke detaljerede tilladelser på objektniveau, så kun bestemte administratorer kan konfigurere Copilot.

## Næste trin

Når du har aktiveret og givet dit samtykke til funktionerne, er du klar til at prøve dem. Gå til:

- [Tilføje marketingtekst til varer med Copilot](item-marketing-text.md)
- [Analysere listedata med Copilot](analysis-assist.md)  
- [Chatte med Copilot](chat-with-copilot.md)
- [Knytte e-dokumenter til indkøbsordrelinjer med Copilot](map-edocuments-with-copilot.md)
- [Afstemme bankkonti med Copilot](bank-reconciliation-with-copilot.md)
- [Foreslå linjer på salgsordrer med Copilot](sales-suggest-sales-lines-with-copilot.md)  

## Se også

[Fejlfinde Copilot- og AI-funktioner](ai-copilot-troubleshooting.md)  
[Ofte stillede spørgsmål om analyseassistance](faqs-analysis-assist.md)  
[Ofte stillede spørgsmål om hjælp til bankafstemning](faqs-bank-reconciliation.md)  
[Ofte stillede spørgsmål om chatte med Copilot](faqs-chat-with-copilot.md)  
[Ofte stillede spørgsmål om tilknytning af e-dokumenter med købsordrer](faqs-map-edocuments.md)  
[Ofte stillede spørgsmål om forslag til marketingtekst](faqs-marketing-text.md)  
[Ofte stillede spørgsmål til forslag til salgslinje](faq-sales-suggest-sales-lines-with-copilot.md)  

[Oversigt over forslag til marketingtekst](ai-overview.md)  