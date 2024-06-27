---
title: Ofte stillede spørgsmål om ansvarlig kunstig intelligens til chat med Copilot (forhåndsversion)
description: 'Disse ofte stillede spørgsmål indeholder oplysninger om den AI-teknologi, der bruges til at chatte med Copilot i Business Central. De indeholder vigtige overvejelser og detaljer om, hvordan AI bruges, hvordan det blev testet og evalueret, og eventuelle specifikke begrænsninger.'
ms.date: 06/13/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI, chat'
---
# Ofte stillede spørgsmål om ansvarlig kunstig intelligens til chat med Copilot (forhåndsversion)

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

Disse ofte stillede spørgsmål beskriver AI-effekten af Chat med Copilot i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du er interesseret i generelle spørgsmål om brugen af funktionen, skal du gå til [Ofte stillede spørgsmål til chat med Copilot](chat-with-copilot-faq.md).

## Hvad er Chat med Copilot?

Microsoft Copilot er en AI-drevet assistent, der hjælper dig med at være mere kreativ, produktiv og effektiv. Du kan chatte med Copilot i Business Central for at få svar og indsigt om [!INCLUDE[prod_short](includes/prod_short.md)] og dine forretningsdata ved at skrive det, du leder efter, i et naturligt sprog.

Chat med Copilot, også kaldet chat, er en interaktiv funktion, der besvarer dine spørgsmål, uden at brugerne behøver at navigere i brugergrænsefladen eller produktdokumentationen. Copilot-ruden er tilgængelig overalt i klienten [!INCLUDE[prod_short](includes/prod_short.md)].

Du kan stille spørgsmål i naturligt sprog, som "Hvordan leverer jeg varer til mine kunder direkte fra mine leverandører?" Eller "Har vi nogen kontorstole på lager til under $600?" Som svar giver Copilot svar i naturligt sprog. Afhængigt af spørgsmålene kan svarene omfatte almindelig tekst, links til poster eller sider i [!INCLUDE[prod_short](includes/prod_short.md)] og links til [!INCLUDE[prod_short](includes/prod_short.md)] hjælpeartikler om Microsoft Learn.

## Hvad er mulighederne i Chat med Copilot?

Du kan chatte med Copilot for at få svar på følgende klasser af spørgsmål:

### Forklar og vejlede

Du kan bede Copilot om at forklare et specifikt koncept, der er relateret til [!INCLUDE[prod_short](includes/prod_short.md)], f.eks. hvad er dimensioner, eller give vejledning i, hvordan man udfører en opgave, f.eks. hvordan man bogfører en salgsordre. Copilot søger i den officielle [!INCLUDE[prod_short](includes/prod_short.md)] dokumentation, der er udgivet af Microsoft, og giver et svar baseret på dokumentationen.

- Copilot bruger viden om Microsoft Learn (ikke en bred websøgning) til semantisk kun at søge i Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]-dokumentation om Microsoft Learn.

- Copilot foretager ikke handlinger, opretter ikke nye data eller ændrer nogen konfiguration. Det opsummerer simpelthen alle afsnit, det finder på Microsoft Learn, der matcher spørgsmålet eller prompten i chat.

### Find virksomhedsdata og relaterede sider

Du kan bede Copilot om at finde sider efter navn eller bede om poster baseret på deres felter og begrænsninger. Hvis Copilot finder et match, svarer det med et link til den relevante post eller side, som du derefter kan vælge at åbne.

- Copilot konverterer det naturlige sproginput til en forespørgsel, der består af et tabelsøgnings-, sorterings- og filterkriterium.

  Funktionen bruger [!INCLUDE[prod_short](includes/prod_short.md)] de oprindelige datasøgningsfunktioner til at finde matchende data fra tabeller i firmadatabasen. Søgningen kører under din egen identitet for sikkerhed og overholdelse. Der søges ikke uden for [!INCLUDE[prod_short](includes/prod_short.md)] databasen.

- Copilot foretager ikke handlinger, opretter ikke nye data eller ændrer nogen konfiguration. Det opsummerer kun de poster, der er modtaget fra den [!INCLUDE[prod_short](includes/prod_short.md)] oprindelige datasøgning. 

## Hvad er den tilsigtede brug af Chat med Copilot?

Chat er designet til virksomhedsbrug og besvarelse af spørgsmål, der vedrører [!INCLUDE[prod_short](includes/prod_short.md)] og de forretningsdata, den indeholder. Funktionen hjælper dig med at løse almindelige opgaver, f.eks. søgning efter poster eller vejledning. Du kan udtrykke dig med dine egne ord, hvilket gør dit arbejde lettere og mere tilgængeligt, når du arbejder med [!INCLUDE[prod_short](includes/prod_short.md)].

## Hvordan blev Chat med Copilot evalueret? Hvilke metrikværdier bruges til at måle ydeevnen?

- Funktionen gennemgik omfattende test, hvor adskillige engelsksprogede tekster, der dækkede en bred vifte af emner og måder at udtrykke hensigt på, blev givet til Copilot. Resultaterne blev evalueret i forhold til nøjagtighed, relevans og sikkerhed.
  
- Denne funktion er bygget i overensstemmelse med ansvarlig brug af AI-standard i Microsoft. [Få mere at vide om ansvarlig AI fra Microsoft](https://aka.ms/RAI).

## Hvordan overvåger Microsoft kvaliteten af genereret indhold?

Microsoft har forskellige systemer på plads for at sikre, at indhold, der genereres af Copilot, er af højeste kvalitet, registrerer misbrug og sikrer sikkerheden for vores kunder og deres data.

Du kan give feedback til alle Copilot-svar og rapportere unøjagtigt eller upassende indhold for at hjælpe Microsoft med at forbedre denne funktion. 

- Du kan give feedback ved at bruge ikonet synes godt om (tommelfinger op) eller antipati (tommelfinger ned) på **Copilot-ruden** i [!INCLUDE[prod_short](includes/prod_short.md)].
  
- Vi analyserer og bruger din feedback på funktionen til at hjælpe os med at forbedre svarene.
  
- Hvis du støder på upassende genereret indhold, skal du rapportere det til Microsoft ved hjælp af denne feedbackformular: [Rapportér misbrug](https://go.microsoft.com/fwlink/?linkid=2249810).
  
- Microsoft deaktiverer muligvis de Copilot-drevne funktioner for udvalgte kunder, hvis der registreres misbrug af funktionaliteten.

## Hvad er begrænsningerne for Chat med Copilot? Hvordan kan brugerne minimere virkningen af Chat med Copilot-begrænsningerne, når de bruger systemet?

- Generelle AI-begrænsninger

  AI-systemer er værdifulde værktøjer, men de er ikke-deterministiske. Det indhold, de genererer, er muligvis ikke nøjagtigt. Så det er vigtigt at bruge din dømmekraft til at gennemgå og verificere svar Copilot, før du træffer beslutninger, der kan påvirke interessenter som kunder og partnere. For de fleste svar vil Copilot også inkludere citater eller referencelinks, som du kan bruge til hurtigt at kontrollere, om Copilot er kommet til det rigtige svar. For eksempel, når du bliver spurgt, hvordan du udfører en opgave, inkluderer Copilot links til kildeartiklen. Når Copilot bliver bedt om at finde en post baseret på specifikke kriterier, inkluderer den links, der beskriver den listeside, den identificerede som samtaleemne. Den indeholder også oplysninger om eventuelle filtre eller sorteringer, der blev anvendt for at nå frem til et svar.

- Sproglige begrænsninger

  - Chat understøttes kun på engelsk i følgende landestandarder: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA.

    Hvis visningssproget i [!INCLUDE[prod_short](includes/prod_short.md)] ikke er et af disse landestandarder, er chat ikke tilgængelig.

  - Kvaliteten af svarene kan være lavere under følgende forhold:
    - Sproglandestandarden er noget andet end en-US.
    - Sprogindstillingen for brugeren i [!INCLUDE[prod_short](includes/prod_short.md)] adskiller sig fra det primære sprog for forretningsdataene i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen.

- Specifikke branche-, produkt- og emnebegrænsninger

   Chat indeholder indbyggede sikkerhedsmekanismer, der forhindrer uønsket generering af skadeligt indhold, f.eks. eksplicit seksuelt indhold eller tilskyndelse til vold. Nogle gange opererer kunder i brancher, sælger produkter og tjenester eller arbejder med processer, der naturligt overlapper det, der kan betragtes som upassende i andre sammenhænge, eller arbejder med data, der kan udløse disse sikkerhedsforanstaltninger. Chat fungerer muligvis ikke så godt i disse tilfælde.

<!--## What operational factors and settings allow for effective and responsible use of the feature?-->

## Hvilke data indsamler Chat med Copilot, og hvordan bruges den

Microsoft bruger ikke dine virksomhedsdata, herunder den tekst, du sender til Copilot, til at træne de grundlæggende AI-modeller til gavn for andre. Virksomhedsadministratorer har fuld kontrol til at styre disse data, der er en del af deres Azure-abonnement. Da administratorer eller andre i din virksomhed kan have adgang til disse data som bestemt af din arbejdsgiver, anbefaler vi, at du ikke indtaster følsomme data, f.eks. adgangskoder eller andre hemmeligheder.

## Hvad tilbyder Chat med Copilot for sikkerhed

Chat er designet til at være sikker og udføres under brugerens identitet, arver alle sikkerhedstilladelser og andre begrænsninger og fungerer aldrig uden for [!INCLUDE[prod_short](includes/prod_short.md)]-platformens sikkerhed. Det betyder, at Copilot kun kan tilgå data, som du har adgang til.

For brugere med SUPER-tilladelse kan chat lettere finde usikrede data, der typisk er sværere at få adgang til for andre brugere. Organisationer, der ikke anvender [!INCLUDE[prod_short](includes/prod_short.md)]-sikkerhedsmodellen til at begrænse, hvilke tabeller og objekter hver bruger eller brugerrolle har adgang til, kan være udsat for forhøjet risiko, når de bruger chat. Derfor anbefaler vi, at din organisation enten implementerer [!INCLUDE[prod_short](includes/prod_short.md)]-sikkerhedsmodellen eller deaktiverer chat.

## Se også

- [Chat med Copilot (forhåndsversion)](chat-with-copilot.md)

