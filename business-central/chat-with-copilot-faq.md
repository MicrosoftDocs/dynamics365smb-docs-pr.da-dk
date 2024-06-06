---
title: Ofte stillede spørgsmål til chat med Copilot
description: I denne artikel besvares nogle almindelige spørgsmål angående chat med Copilot i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 05/17/2024
ms.custom: bap-template jswymer
---
# Ofte stillede spørgsmål til chat med Copilot

[!INCLUDE[preview-banner](includes/preview-banner.md)]

I denne artikel besvares nogle almindelige spørgsmål angående chat med Copilot i [!INCLUDE[prod_short](includes/prod_short.md)]. For spørgsmål relateret til AI og chat, se [Ofte stillede spørgsmål om ansvarlig AI for chat med Copilot](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Kan administratorer give eller nægte individuelle brugere tilladelse til at få adgang til chat?

Nej, der er ikke angivet nogen tilladelse eller tilladelse til chat. Hvis chat er aktiveret på siden [Copilot- og AI-funktioner](enable-ai.md), har alle brugere i et miljø adgang til chat.
 
## Er chat tilgængelig på tablet, telefon eller andre formfaktorer?

Nej, chatruden er kun tilgængelig på webklienten [!INCLUDE[web_client](includes/web_client.md)].

## Jeg bruger ikke Business Central på engelsk. Hvilke muligheder har jeg?

På nuværende tidspunkt er chat kun tilgængelig på engelsk. Du kan ændre dit brugersprog til engelsk i [Mine indstillinger](ui-change-basic-settings.md#language).

## Hvilken Business Central-version skal jeg bruge for at opleve chat?

Chat er tilgængelig som offentlig prøveversion fra version 24.0 (2024 udgivelsesbølge 1).

## Fungerer chat med mine tilpasninger?

Det afhænger af den type spørgsmål, du stiller Copilot. Eksempler:

- Når du stiller spørgsmål for at finde poster, kan Copilot finde poster i dine brugerdefinerede tabeller, der identificeres ved hjælp af brugerdefinerede felter.
- Når du beder om en forklaring eller vejledning, har Copilot ikke adgang til oplysninger om dine tilpasninger eller dokumentation til dine tilføjelser.

## Copilot ser aldrig ud til at åbne den post eller side, jeg bad om. Hvad gør jeg forkert?

Når du beder Copilot om at finde poster i [!INCLUDE[prod_short](includes/prod_short.md)], viser den alle poster, den finder, som felter eller links, der kan vælges, i chatruden. Mens Copilot er i forhåndsversion, navigerer den ikke automatisk til nogen side.

## De svar, jeg får fra Copilot, varierer, selvom jeg stiller det samme spørgsmål. Er det en fejl?

Copilot kan lejlighedsvis svare på forskellige måder. Svarene er ikke nødvendigvis identiske.

## Hvornår skal jeg bruge kopifunktionen på chatbeskeder?

Du kan bruge knappen Kopiér til at kopiere en meddelelse fra tidligere i din samtale med Copilot, indsætte den i indtastningsfeltet for at prøve igen eller prøve en variant af din meddelelse til Copilot.

## Hvordan tilpasser eller udvider jeg chat?

Mens den er i prøveversion, kan chatruden og Copilots svar ikke ændres på nogen måde via tilpasning, tilføjelsesprogrammer eller tilpasning.

## Finder Copilot data i andre virksomheder eller miljøer?

Copilot søger kun efter poster i den virksomhed, du aktuelt er logget på&mdash;, selvom din organisation bruger flere miljøer eller virksomheder til at adskille data.

## Chatruden Copilot vises ikke. Hvad kan jeg gøre?

Kontroller, at dit brugersprog i Mine indstillinger er indstillet til engelsk, og at dit miljø er version 24.0 eller nyere. På siden Copilot og AI-funktioner skal du sørge for, at administratorer har aktiveret samtykke til data på tværs af geografiske områder og har aktiveret chat. Sørg for, at din miljølokalisering ikke er Canada.

Hvis du stadig ikke kan se funktionen Chat med Copilot, er det muligt, at Microsoft stadig ruller funktionen ud til dit område. Copilot ruller først ud til amerikanske kunder i april 2024 og vil derefter i løbet af få uger blive rullet ud til andre lande-/områdelokaliseringer.

## Hvorfor viser Copilot kun tre poster i Chat-ruden?

Når du beder Copilot om at hente poster, bestemmer den måde, du formulerer spørgsmålet på, hvordan Copilot identificerer og anvender filtre på sider for at finde det, du leder efter. For at holde svarene kompakte og præcise viser Chatruden maksimalt tre postfelter, selv når Copilot finder et større antal relevante poster.

## Copilot returnerer forkerte svar på totaler og andre beregninger

Mens den er i prøveversion, kan Chat med Copilot finde poster, forklare begreber og vejlede dig i, hvordan du udfører opgaver i Business Central. Andre use cases understøttes ikke, f.eks. sammenlægning af et felt på tværs af poster eller beregning af det gennemsnitlige månedlige beløb. Vi håber at tilføje grundlæggende matematiske evner til Copilot i fremtiden.

## Kan jeg bruge tale i stedet for at skrive mine prompter?

Du kan chatte med Copilot ved at bruge stemmeskrivning til at tale i stedet for at skrive dine ord i chatruden. Stemmeskrivning bruger online talegenkendelse og er tilgængelig med Windows. For at bruge stemme skal du aktivere chatmeddelelsesboksen, derefter bruge Windows <kbd>H-genvejen</kbd>+<kbd></kbd> og begynde at tale. Du kan finde flere oplysninger under [Brug stemmeskrivning til at tale i stedet for at skrive på din pc](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## Næste trin

[Chat med Copilot (forhåndsversion)](chat-with-copilot.md)
