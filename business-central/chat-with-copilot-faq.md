---
title: Ofte stillede spørgsmål til chat med Copilot
description: I denne artikel besvares nogle almindelige spørgsmål angående chat med Copilot i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 02/27/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Ofte stillede spørgsmål til chat med Copilot

[!INCLUDE[preview-banner](includes/preview-banner.md)]

I denne artikel besvares nogle almindelige spørgsmål angående chat med Copilot i [!INCLUDE[prod_short](includes/prod_short.md)]. For spørgsmål relateret til AI og chat, se [Ofte stillede spørgsmål om ansvarlig AI for chat med Copilot](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>Kan administratorer give eller nægte individuelle brugere tilladelse til at få adgang til chat?

Nej, der er ikke angivet nogen tilladelse eller tilladelse til chat. Hvis chat er aktiveret på siden [Copilot- og AI-funktioner](enable-ai.md), har alle brugere i et miljø adgang til chat.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>Er chat tilgængelig på tablet, telefon eller andre formfaktorer?

Nej, chatruden er kun tilgængelig på webklienten [!INCLUDE[web_client](includes/web_client.md)].

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>Jeg bruger ikke Business Central på engelsk. Hvilke muligheder har jeg?

På nuværende tidspunkt er chat kun tilgængelig på engelsk. Du kan ændre dit brugersprog til engelsk i [Mine indstillinger](ui-change-basic-settings.md#language).

## <a name="which-business-central-version-do-i-need-to-experience-chat"></a>Hvilken Business Central-version skal jeg bruge for at opleve chat?

Chat er tilgængelig som offentlig prøveversion fra version 24.0 (2024 udgivelsesbølge 1).

## <a name="does-chat-work-with-my-customizations"></a>Fungerer chat med mine tilpasninger?

Det afhænger af den type spørgsmål, du stiller Copilot. Eksempler:

- Når du stiller spørgsmål for at finde poster, kan Copilot finde poster i dine brugerdefinerede tabeller, der identificeres ved hjælp af brugerdefinerede felter.
- Når du beder om en forklaring eller vejledning, har Copilot ikke adgang til oplysninger om dine tilpasninger eller dokumentation til dine tilføjelser.

## <a name="copilot-never-seems-to-open-the-record-or-page-i-asked-for-what-am-i-doing-wrong"></a>Copilot ser aldrig ud til at åbne den post eller side, jeg bad om. Hvad gør jeg forkert?

Når du beder Copilot om at finde poster i [!INCLUDE[prod_short](includes/prod_short.md)], viser den alle poster, den finder, som felter eller links, der kan vælges, i chatruden. Mens Copilot er i forhåndsversion, navigerer den ikke automatisk til nogen side.

## <a name="the-answers-i-get-from-copilot-vary-even-though-i-ask-the-same-question-is-it-a-bug"></a>De svar, jeg får fra Copilot, varierer, selvom jeg stiller det samme spørgsmål. Er det en fejl?

Copilot kan lejlighedsvis svare på forskellige måder. Svarene er ikke nødvendigvis identiske.

## <a name="when-should-i-use-the-copy-function-on-chat-messages"></a>Hvornår skal jeg bruge kopifunktionen på chatbeskeder?

Du kan bruge knappen Kopiér til at kopiere en meddelelse fra tidligere i din samtale med Copilot, indsætte den i indtastningsfeltet for at prøve igen eller prøve en variant af din meddelelse til Copilot.

## <a name="how-do-i-customize-or-extend-chat"></a>Hvordan tilpasser eller udvider jeg chat?

Mens den er i prøveversion, kan chatruden og Copilots svar ikke ændres på nogen måde via tilpasning, tilføjelsesprogrammer eller tilpasning.

## <a name="does-copilot-find-data-in-other-companies-or-environments"></a>Finder Copilot data i andre virksomheder eller miljøer?

Selvom din organisation bruger flere miljøer eller virksomheder til at adskille data, søger Copilot kun efter poster i den virksomhed, du aktuelt er logget ind på.

## <a name="the-copilot-chat-pane-doesnt-show-what-can-i-do"></a>Chatruden Copilot vises ikke. Hvad kan jeg gøre?

Kontroller, at dit brugersprog i Mine indstillinger er indstillet til engelsk, og at dit miljø er version 24.0 eller nyere. På siden Copilot og AI-funktioner skal du sørge for, at administratorer har aktiveret samtykke til data på tværs af geografiske områder og har aktiveret chat. Sørg for, at din miljølokalisering ikke er Canada.

Hvis du stadig ikke kan se chatten med Copilot-funktionen, er det muligt, at Microsoft stadig ruller dette ud til din region. Copilot ruller først ud til amerikanske kunder i april 2024 og vil derefter i løbet af uger blive rullet ud til andre landelokaliseringer.

## <a name="next-steps"></a>Næste trin

[Chat med Copilot (forhåndsversion)](chat-with-copilot.md)