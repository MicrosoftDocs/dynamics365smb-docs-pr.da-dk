---
title: Ofte stillede spørgsmål til chat med Copilot
description: 'Få mere at vide om, hvordan du chatter med Copilot, en virtuel assistent, der hjælper dig med at bruge Business Central. Find svar på almindelige spørgsmål om chatfunktioner, indstillinger og begrænsninger.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Ofte stillede spørgsmål til chat med Copilot

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

I denne artikel besvares nogle almindelige spørgsmål angående chat med Copilot i [!INCLUDE[prod_short](includes/prod_short.md)]. For spørgsmål relateret til AI og chat, se [Ofte stillede spørgsmål om ansvarlig AI for chat med Copilot](faqs-chat-with-copilot.md).

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>Kan administratorer give eller nægte individuelle brugere tilladelse til at få adgang til chat?

Nej, der er ikke angivet nogen tilladelse eller tilladelse til chat. Hvis chat er aktiveret på siden [Copilot- og AI-funktioner](enable-ai.md), har alle brugere i et miljø adgang til chat.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>Er chat tilgængelig på tablet, telefon eller andre formfaktorer?

Nej, chatruden er kun tilgængelig på webklienten [!INCLUDE[web_client](includes/web_client.md)].

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>Jeg bruger ikke Business Central på engelsk. Hvilke muligheder har jeg?

I øjeblikket er chat kun tilgængelig på engelsk. Du kan ændre dit brugersprog til engelsk i [Mine indstillinger](ui-change-basic-settings.md#language).

## <a name="what-version-of-business-central-do-i-need-for-chat"></a>Hvilken version af Business Central skal jeg bruge til at chatte?

Chat er tilgængelig som offentlig prøveversion fra version 24.0 (2024 udgivelsesbølge 1).

## <a name="does-chat-work-with-my-customizations"></a>Fungerer chat med mine tilpasninger?

Det afhænger af den type spørgsmål, du stiller Copilot. Eksempler:

- Hvis du stiller spørgsmål for at finde poster, kan der findes poster i dine brugerdefinerede tabeller, der bruger brugerdefinerede felter.
- Når du beder Copilot om en forklaring eller vejledning, har den ikke adgang til oplysninger om dine tilpasninger eller dokumentation til dine tilføjelser.

## <a name="how-do-i-open-a-record-or-page-with-chat"></a>Hvordan åbner jeg en post eller side med chat?

Når du beder Copilot om at finde poster i [!INCLUDE[prod_short](includes/prod_short.md)], viser den alle poster, den finder, som felter eller links, der kan vælges, i chatruden. Mens Copilot er i forhåndsversion, navigerer den ikke automatisk til nogen side.

## <a name="why-do-i-get-different-answers-from-copilot-for-the-same-question"></a>Hvorfor får jeg forskellige svar fra Copilot på det samme spørgsmål?

Copilot kan lejlighedsvis svare på forskellige måder. Svarene er ikke altid identiske.

## <a name="how-do-i-use-the-copy-function-on-chat-messages"></a>Hvordan bruger jeg kopifunktionen på chatbeskeder?

Du kan bruge knappen Kopiér til at kopiere en meddelelse fra tidligere i din samtale med Copilot, indsætte den i indtastningsfeltet for at prøve igen eller prøve en variant af din meddelelse til Copilot.

## <a name="can-i-customize-or-extend-chat"></a>Kan jeg tilpasse eller udvide chat?

Mens den er i prøveversion, kan chatruden og Copilots svar ikke ændres på nogen måde via tilpasning, tilføjelsesprogrammer eller tilpasning.

## <a name="does-copilot-search-for-data-in-other-companies-or-environments"></a>Søger Copilot efter data i andre virksomheder eller miljøer?

Copilot søger kun efter poster i den virksomhed, du aktuelt er logget ind på. Den søger ikke efter data på tværs af flere miljøer eller virksomheder.

## <a name="what-can-i-do-if-the-chat-pane-doesnt-show"></a>Hvad kan jeg gøre, hvis chatruden ikke vises?

Kontroller, at dit brugersprog i **Mine indstillinger** er indstillet til engelsk, og at dit miljø er version 24.0 eller nyere. På siden Copilot og AI-funktioner skal du sørge for, at administratorer har aktiveret samtykke til data på tværs af geografiske områder og har aktiveret chat. Sørg også for, at din miljølokalisering ikke er Canada.

Hvis du stadig ikke kan se chatten med Copilot-funktionen, er det muligt, at Microsoft stadig ruller funktionen ud til din region. Copilot ruller først ud til amerikanske kunder i april 2024 og vil derefter i løbet af uger blive rullet ud til andre lande/område-lokaliseringer.

## <a name="why-does-copilot-only-show-three-records-in-the-chat-pane"></a>Hvorfor viser Copilot kun tre poster i Chat-ruden?

Når du beder Copilot om at finde poster, bestemmer den måde, du formulerer spørgsmålet på, hvordan Copilot identificerer og anvender filtre på sider for at finde det, du leder efter. For at holde svarene kortfattede viser Chatruden maksimalt tre postfelter, selv når Copilot finder mere relevante poster.

## <a name="why-does-copilot-give-incorrect-answers-to-calculations"></a>Hvorfor giver Copilot forkerte svar på beregninger?

Mens den er i prøveversion, kan Chat med Copilot hjælpe dig med at finde poster, forklare begreber og vejlede dig i, hvordan du udfører opgaver i Business Central. Andre use cases understøttes ikke, f.eks. sammenlægning af et felt på tværs af poster eller beregning af det gennemsnitlige månedlige beløb. Vi håber at tilføje grundlæggende matematiske evner til Copilot i fremtiden.

## <a name="can-i-use-speech-instead-of-typing-my-prompts"></a>Kan jeg bruge tale i stedet for at skrive mine prompter?

Du kan chatte med Copilot ved at bruge stemmeskrivning til at tale i stedet for at skrive dine ord i chatruden. Stemmeskrivning bruger online talegenkendelse og er tilgængelig med Windows. Hvis du vil bruge stemme, skal du aktivere chatmeddelelsesfeltet, derefter bruge genvejen <kbd>Windows</kbd>+<kbd>H</kbd> og begynde at tale. Du kan finde flere oplysninger under [Brug stemmeskrivning til at tale i stedet for at skrive på din pc](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## <a name="next-steps"></a>Næste trin

- [Chat med Copilot (forhåndsversion)](chat-with-copilot.md)
