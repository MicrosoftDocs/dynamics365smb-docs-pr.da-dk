---
title: AI-styret marketingtekst med element (forhåndsversion) med Copilot Ofte stillede spørgsmål
description: Få svar på ofte stillede spørgsmål om de AI-genererede tekstfunktioner med Copilot.
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: faq
ms.date: 04/03/2023
ms.custom: bap-template
author: jswymer
ms.service: dynamics365-business-central
---

# AI-styret marketingtekst med element (forhåndsversion) med Copilot Ofte stillede spørgsmål

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Denne artikel bruger spørgsmål og svar til at forklare vigtige aspekter om AI-teknologien bag Copilot og den tekst, den genererer.

## [Generelt](#tab/general)

### Hvad er Copilot?

Copilot leverer AI-genererede tekstforslag til varer i Business central. Den er beregnet til brugere, der skriver marketingtekst for varer, så de kan producere fængslende og bevisende indhold. Nogle vigtige fordele omfatter:

- Reducerer den tid, der bruges på Kopiskrivning, hvilket kan accelerere tid til salg for varer, der sælges på onlinebutikker.
- Oplåsning af kreativitet for at kunne levere mere spændende produktbeskrivelser.
- Forbedrer konsistensen af marketingmaterialer til produktlinjer.

Brugerne skal overveje den AI-genererede tekst som et forslag, som skal gennemses og redigeres, før den er offentligt tilgængelig.

### Hvorfor er Copilot ikke tilgængelig for marketingtekst på mine varer i Business central?

Hvis Copilot skal være tilgængelig, skal følgende krav være opfyldt:

- Det sprog, du bruger i Business central, skal være engelsk. Alle de tilgængelige engelske landestandarder fungerer, som f. eks. engelsk (amerikansk), engelsk (Storbritannien) eller engelsk (Sydafrika).

  Hvis du vil skifte sprog, skal du i øverste højre hjørne vælge ikonet **Indstillinger** ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") > **Mine indstillinger** > **Sprog**. Du kan finde flere oplysninger i [Ændre grundlæggende indstillinger](ui-change-basic-settings.md#language).
- Hvis du bruger Business Central Online version 22 eller en nyere version (hvis du er er eksisterende kunde) eller en prøveversion.  <!--**22.0.54157.54311 (Preview - Copilot edition)**-->.

   Hvis du vil kontrollere versionen, skal du vælge spørgsmålstegnet i øverste højre hjørne og derefter **Hjælp og support**. Kig efter programversionen under **Fejlfinding**. Du kan finde flere oplysninger om, hvordan du får den korrekte forhåndsversion, ved at gå til [Introduktionen til Business Central, forhåndsversion](ai-preview-getstarted.md).
- Funktionen : **Opret AI-drevne produktbeskrivelser med Copilot** skal være aktiveret.

   Du kan finde flere oplysninger ved at [Aktivere eller deaktivere funktionen "Opret produktbeskrivelser fra AI-drevet med Copilot"](enable-ai.md#enable-or-disable-the-create-ai-powered-product-descriptions-with-copilot-feature).
- En administrator har accepteret vilkår og betingelser.

   Du kan finde flere oplysninger i [Tilladelse til accept eller afvisning af forhåndsversion og oplysninger om beskyttelse af personlige oplysninger for alle brugere](enable-ai.md#consent-to-or-reject-the-preview-and-privacy-terms-and-conditions-for-all-users).

### Er Copilot tilgængelig til forhåndsversion i Business Central lokalt?

Nej, det understøttes aktuelt ikke i Business Central lokalt.

### Hvordan fungerer Copilot, hvor den foreslåede tekst kommer fra?

Copilot bruger [Microsoft Azure OpenAI service](/azure/cognitive-services/openai/overview) til at få adgang til avancerede sprogmodeller, der analyserer og genererer naturligt sprog. Disse modeller er blevet oplært på en bred brødtekst af tekstdatasæt. Derfor kan Copilot generere foreslåede svar, der er tilpasset på engelsk, og som er baseret på minimalt inputdata, som f. eks. en vares attributter, kategori eller beskrivelse. 

### Hvad er kvaliteten af teksten, der foreslås af Copilot?

Da den underliggende teknologi bag Copilot bruger AI, som er uddannet på en lang række kilder, er det genererede indhold ikke altid faktuelt eller egnet. Nogle forslag kan endog indeholde tvivlsomt eller upassende indhold. Du har ansvaret for at gennemgå og redigere genererede forslag for at sikre, at det er nøjagtigt og hensigtsmæssigt.

Oplysninger om upassende forslag finder du i forbindelse med [Hvad sker der med stødende og skadelige tekstforslag?](/dynamics365/business-central/ai-faq?&tabs=oversight#whats-done-about-abusive-and-harmful-text-suggestions).

### Hvordan kan jeg forbedre de forslag, jeg får fra Copilot?

Der er nogle ting, du kan gøre for at få det optimale forslag fra Copilot:

- Føje flere attributter til et element for at kunne fremme de specifikke funktioner og egenskaber, du er interesseret i
- Ændre indstillingerne for samtalens tone og fremhævning af kvalitet, så den passer til dine personlige præferencer.
- Forbedre varens beskrivelse
- Sørg for, at varen er tildelt den mest velegnede kategori.

Du kan finde flere oplysninger i [forbedrende og skræddersyede tekstforslag](item-marketing-text.md#improve-and-tailor-text-suggestions).

### Hvad gør jeg, hvis jeg ikke er tilfreds med den genererede tekst?

Gør følgende for at hjælpe os med at forbedre teksten ved at vælge **Er det en god løsning?** på siden **Opret med Copilot**, som du kan bruge til at besvare med en tommelfinger op (jeg synes om) eller tommelfinger ned (skal forbedres).

![Viser varekort med marketing tekstrude](media/create-with-copilot-window-feedback.png)

### Kan administratorer deaktivere Copilot? Hvis ja, hvordan?

Business Central tilbyder administratorerne at deaktivere Copilot i forhåndsversionen på to måder:

- Du kan ikke bruge Azure OpenAI til beskyttelse af personlige oplysninger for alle brugere.

  eller

- Deaktiver funktionen **Opret AI-styret produktaktivering med Copilot** på siden **Funktionsstyring**.

Hvis du vil vide mere, skal du gå til [Konfigurer marketingtekst for AI-drevet vare (forhåndsversion) med Copilot som administrator](enable-ai.md).

## [Fairness](#tab/fairness)

### Fungerer Copilot med andre sprog end engelsk?

I øjeblikket understøtter Copilot kun engelsk. Unøjagtige svar kan returneres, når brugere kommunikerer med systemet på andre sprog end engelsk.

## [Humant overblik](#tab/oversight)

### Hvad sker der med stødende og skadelige tekstforslag?

Azure OpenAI-tjenesten gemmer anmodninger og afslutninger fra tjenesten for at overvåge, om der er stødende brug og for at udvikle og forbedre kvaliteten af Azure OpenAIs indholdsstyringssystemer. [Få mere at vide om indholdsadministration og -filtrering](/azure/cognitive-services/openai/concepts/content-filter).

Godkendte Microsoft-medarbejdere kan få adgang til dine spørgsmål og data, som har udløst vores automatiserede systemer, med henblik på at undersøge og kontrollere potentielle misbrug. For de kunder, som har implementeret Azure OpenAI service i den Europæiske Union, vil de autoriserede Microsoft-medarbejdere ligge i EU. Disse data kan bruges til at forbedre vores indholdsadministrationssystemer. I tilfælde af en bekræftet overtrædelse af politikken beder vi dig muligvis om at foretage øjeblikkelige foranstaltninger for at afhjælpe problemet til og for at forhindre yderligere misbrug. Hvis problemet ikke løses, kan det medføre, at Azure OpenAI-ressourcer er suspenderet eller ophævet.

Du kan finde flere oplysninger i [Data, beskyttelse af personlige oplysninger og sikkerhed for Azure OpenAI service](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

### Kan jeg framelde mig og +udføre menneskeligt gennemsyn?  

Som en del af levering af Azure Open AI-forhåndsversioner vil Microsoft behandle og lagre kundedata, der er sendt til tjenesten, samt output-indhold, med henblik på (1) overvågning af og forebyggelse af misbrug eller skadelig brug eller ydelse af tjenesteydelser, og (2) udvikling, afprøvning og forbedring af de funktioner, der er beregnet til at forebygge misbrug af og/eller skadelige udgange fra tjenesten. Autoriserede Microsoft-medarbejdere kan gennemse data, som har udløst vores automatiserede systemer, til at undersøge og bekræfte potentielle misbrug, og de kan i begrænset omfang få udtagning af betingelser, som ikke er markeret af vores automatiserede systemer for at sikre, at systemerne fungerer korrekt. Autoriserede Microsoft-medarbejdere kan også få adgang til og bruge disse data til at forbedre de systemer, der overvåger, for at forhindre stødende eller skadelig brug eller output fra tjenesten. Yderligere oplysninger om [termer i forhåndsversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/)

## [Beskyttelse af personlige oplysninger](#tab/privacy)

### Hvilke data indsamler funktionen? Hvordan bruges dataene?

Funktionen indsamler dit svar til spørgsmålet **Er det en god løsning?** på siden **Opret med Copilot**, som du kan bruge til at besvare med en tommelfinger op (jeg synes om) eller tommelfinger ned (skal forbedres).

Vi bruger disse data til at evaluere og forbedre kvaliteten af funktionen. Yderligere oplysninger om, hvilke data der indsamles, i [vilkår for forhåndsversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

![Viser varekort med marketing tekstrude](media/create-with-copilot-window-feedback.png)

---

## Se også

[Oversigt over AI-styret varemarketingtekst med Copilot](ai-overview.md)  
[Konfigurere marketingtekst med Copilot til AI-styret vare som administrator](enable-ai.md)  
[Oprette marketingtekst til varer vha. Copilot](item-marketing-text.md)  
[AI-drevet varemarketingtekst med Copilot, ofte stillede spørgsmål](ai-faq.md)  
