---
title: Ofte stillede spørgsmål til forslag til marketingtekst
description: 'Ofte stillede spørgsmål om AI indeholder oplysninger om den AI-teknologi, der bruges i forslag til marketingtekster i Business Central, sammen med vigtige overvejelser og detaljer om, hvordan AI''en bruges, hvordan den blev testet og evalueret og eventuelle specifikke begrænsninger.'
ms.date: 10/07/2023
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.collection:
  - bap-ai-copilot
---

# Ofte stillede spørgsmål om tekstforslag med Copilot

Disse ofte stillede spørgsmål beskriver AI-effekten af [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]-funktionen i [!INCLUDE[prod_short](includes/prod_short.md)].

## Hvad er forslag til varemarketingtekst?

Copilot yder skrivehjælp til brugere, der er ansvarlige for at oprette marketingtekst (også kaldet kopi) på varer i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne funktion er kendt som [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]. Funktionen [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] yder skrivehjælp til brugere, der er ansvarlige for at oprette marketingtekst (også kaldet *kopi*) på varer i [!INCLUDE[prod_short](includes/prod_short.md)].

Funktionen er tilgængelig på alle varekort i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil bruge det, skal du blot åbne et element og derefter vælge **Marketingtekst** > **Kladde med Copilot**. Denne handling genererer automatisk et tekstforslag, der er engagerende, kreativt og specifikt for det element, der vises. Forslag er baseret på forskellige input, herunder:

- Varens attributter, kategori og navn.
- Personlige skrivestilspræferencer, som samtalens tone, fremhævet kvalitet, format og længde.

Du kan ændre værdien af disse inputindstillinger til at påvirke resultatet af den AI-genererede tekst. Før du gemmer et forslag, kan du nemt gennemgå og redigere det for nøjagtighed eller prøve et andet forslag.

Nogle af de vigtigste fordele ved denne funktion omfatter:

- Reducerer den tid, der bruges på Kopiskrivning, hvilket kan accelerere tid til salg for varer, der sælges på onlinebutikker.
- Oplåsning af kreativitet for at kunne levere mere spændende produktbeskrivelser.
- Forbedrer konsistensen af marketingmaterialer til produktlinjer.

## Hvad er systemets muligheder?

Funktionen [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] bruger [Microsoft Azure OpenAI-tjeneste](/azure/cognitive-services/openai/overview) til at få adgang til avancerede sprogmodeller, der analyserer og genererer naturligt sprog. Disse modeller er blevet oplært på en bred brødtekst af tekstdatasæt. Derfor kan Copilot generere foreslåede svar, der er tilpasset på engelsk, og som er baseret på minimalt inputdata, som f. eks. en vares attributter, kategori eller beskrivelse. 

## Hvad er systemets tiltænkte brug?

Denne funktion er beregnet til at hjælpe brugerne med at oprette marketingtekst til varer i [!INCLUDE[prod_short](includes/prod_short.md)]. Forfattere bruger funktionen til hurtigt at få overbevisende og engagerende tekstforslag, som derefter gennemgås og redigeres for nøjagtighed. 

## Hvordan blev tekst til varemarkedsføring evalueret? Hvilke metrikværdier bruges til at måle ydeevnen?

- Funktionen gennemgik omfattende test, hvor adskillige tekster på forskellige sprog blev evalueret af sprogeksperter i forhold til forskellige kriterier. Testen var baseret på [!INCLUDE[prod_short](includes/prod_short.md)]-demonstrationsdata og andre fiktive produktkataloger.
- Denne funktion er bygget i overensstemmelse med ansvarlig brug af AI-standard i Microsoft. [Få mere at vide om ansvarlig AI fra Microsoft](https://aka.ms/RAI).

## Hvordan overvåger Microsoft kvaliteten af genereret indhold?

Microsoft har forskellige systemer på plads for at sikre, at Copilot-funktionerne forbliver operationelle og genererer indhold af højeste kvalitet.

- Brugere har mulighed for at give feedback for at rapportere upassende indhold og forbedre funktionaliteten.

  - Hvis du støder på upassende genereret indhold, skal du rapportere det til Microsoft ved hjælp af denne feedbackformular: [Rapportér misbrug](https://go.microsoft.com/fwlink/?linkid=2249810). 

    Microsoft deaktiverer muligvis de Copilot-drevne funktioner for udvalgte kunder, hvis der registreres misbrug af funktionaliteten. 

  - Vi sporer brugerfeedback i [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] for at hjælpe os med at forbedre forslagene. 

    Du giver feedback ved at bruge ikonet synes godt om (tommelfinger op) eller antipati (tommelfinger ned) på **Copilot-siden** i [!INCLUDE[prod_short](includes/prod_short.md)]. Vi indsamler telemetrien af disse bevægelser for hvert AI-output, som du sender feedback til.

    ![Viser et varekort med marketing tekstrude](media/create-with-copilot-window-feedback.svg)

- Azure OpenAI-tjenesten gemmer anmodninger og afslutninger fra tjenesten for at overvåge, om der er stødende brug og for at udvikle og forbedre kvaliteten af Azure OpenAI-indholdsstyringssystemer. [Få mere at vide om indholdsadministration og -filtrering](/azure/cognitive-services/openai/concepts/content-filter). Dine virksomhedsdata bruges ikke til at træne AI-modeller i Azure OpenAI-tjenesten.

   Godkendte Microsoft-medarbejdere kan få adgang til dine spørgsmål og data, som har udløst vores automatiserede systemer, med henblik på at undersøge og kontrollere potentielle misbrug. For de kunder, der bruger [!INCLUDE[prod_short](includes/prod_short.md)] i den Europæiske Union, vil de autoriserede Microsoft-medarbejdere ligge i EU. Disse data kan bruges til at forbedre vores indholdsadministrationssystemer. I tilfælde af en bekræftet overtrædelse af politikken beder vi dig muligvis om at foretage øjeblikkelige foranstaltninger for at afhjælpe problemet til og for at forhindre yderligere misbrug. Hvis problemet ikke løses, kan det medføre, at Azure OpenAI-ressourcer er suspenderet eller ophævet.

   Du kan finde flere oplysninger i [Data, beskyttelse af personlige oplysninger og sikkerhed for Azure OpenAI-tjeneste](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

## Er der en logføringsproces og en proces til manuel gennemgang som en del af Azure OpenAI-tjeneste, og kan jeg i så fald fravælge det?  

Som en del af levering af Azure OpenAI-tjeneste vil Microsoft behandle og gemme kundedata, der er sendt til tjenesten, samt output-indhold, med henblik på overvågning af og forebyggelse af misbrug eller skadelig brug eller ydelse af tjenesteydelser, og udvikling, afprøvning og forbedring af de funktioner, der er beregnet til at forebygge misbrug af og/eller skadelige udgange fra tjenesten. 

Autoriserede Microsoft-medarbejdere kan gennemse data, som har udløst vores automatiserede systemer, til at undersøge og bekræfte potentielle misbrug, og de kan i begrænset omfang få udtagning af betingelser, som ikke er markeret af vores automatiserede systemer for at sikre, at systemerne fungerer korrekt. Autoriserede Microsoft-medarbejdere kan også få adgang til og bruge disse data til at forbedre de systemer, der overvåger, for at forhindre stødende eller skadelig brug eller output fra tjenesten. Yderligere oplysninger om [termer i forhåndsversion](https://go.microsoft.com/fwlink/?linkid=2189520).

For at Microsoft kan beskytte tjenesten og dens kunder, er det ikke muligt at fravælge logføring og menneskelige gennemgangsprocesser.

## Hvilke data indsamler funktionen? Hvordan bruges dataene?

Funktionen til forslag til marketingtekst indsamler de data, der som minimum kræves af Business Central for at kunne tilbyde tjenesten. Du kan finde flere oplysninger i [Dynamics 365-vilkår for Azure OpenAI-drevne funktioner](https://go.microsoft.com/fwlink/?linkid=2236010).

Funktionen indsamler også data fra den feedback, brugeren kan give, ved hjælp af ikonerne synes godt om (tommelfinger op) eller antipati (tommelfinger ned) øverst på siden **Copilot**. Dataene er anonyme og omfatter valget af synes om eller synes ikke om, hvis den leveres, og Copilot-funktionen, som feedbacken gælder for. Vi bruger disse data til at evaluere og forbedre kvaliteten af funktionen.

## Hvad er nuværende begrænsninger for [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]? Hvordan kan brugere minimere påvirkningen af [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]-begrænsningerne, når de bruger systemet?

- Da den underliggende teknologi bag funktionen bruger AI, som er uddannet på en lang række kilder, er det genererede indhold ikke altid faktuelt eller egnet. Nogle forslag kan endog indeholde tvivlsomt eller upassende indhold. Du har ansvaret for at gennemgå og redigere genererede forslag for at sikre, at det er nøjagtigt og hensigtsmæssigt.

- Tilgængelige sprog
  
   [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

## Hvilke driftsmæssige faktorer og indstillinger gør det muligt at bruge systemet på en effektiv og ansvarlig måde?

Der er nogle ting, du kan gøre for at få det optimale ud af funktionen:

- Føje flere attributter til et element for at kunne fremme de specifikke funktioner og egenskaber, du er interesseret i.
- Ændre indstillingerne for samtalens tone og fremhævning af kvalitet, så den passer til dine personlige præferencer.
- Forbedre varens beskrivelse.
- Sørg for, at varen er tildelt den mest velegnede kategori.

Du kan finde flere oplysninger i [forbedrende og skræddersyede tekstforslag](item-marketing-text.md#improve-and-tailor-text-suggestions).

> [!TIP]
> Gennemgå altid forslagene for nøjagtighed, før du gemmer dem og offentliggør dem til offentligt forbrug.


## Se også

- [Forslag til marketingtekst](ai-overview.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
