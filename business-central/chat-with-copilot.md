---
title: Chat med Copilot (forhåndsversion)
description: 'Få mere at vide om, hvordan du bruger chat med Copilot til at finde data og få hjælp i Business Central.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/13/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
  - get-started
---

# Chat med Copilot (forhåndsversion)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

I denne artikel forklares det, hvordan du chatter med Copilot for at få svar om dine virksomhedsdata og hjælp til opgaver og emner, der er relateret til Business Central.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Om chat med Copilot

Microsoft Copilot er den AI-drevne assistent, der hjælper med at sætte gang i kreativiteten, øge produktiviteten og eliminere kedelige opgaver. Ved at chatte med Copilot i Business Central kan du stille spørgsmål og finde forretningsdata ved hjælpe af naturligt sprog. Hvad kan du kan gøre:

- Finde forretningsdata for din virksomhed i Business Central. Brug chat til at søge efter (og åbne) data om objekter/poster, der er relateret til forretningsprocesser, f.eks. debitorer, kreditorer, salgsordrer og varer med mere. Spørg f.eks. Copilot: "Vis mig den seneste salgsordre for Adatum."
- Få forklaringer eller trin-for-trin vejledning om forskellige opgaver. Spørg f.eks. "Hjælp mig med at forstå dimensioner" eller "Hvordan bogfører jeg en salgsordre?
- Forstå formålet med og den typiske brug af de enkelte felter. Når du vælger **Spørg Copilot** i et værktøjstip til et felt, åbnes chatten med prompten Forklar for feltnavnet, og Copilot giver oplysninger om det. Copilot linker til de artikler, den refererer til, så det er nemt at verificere beskrivelsen.

Copilots kilder svar fra de officielle oplysninger, der er tilgængelige på Microsoft Learn dokumentationen [Dynamics 365 Business Central ](/dynamics365/business-central/).
  
Brug af chat med Copilot strømliner din arbejdsgang ved at omgå traditionel navigation og produkthjælp.
  
> [Se video](https://go.microsoft.com/fwlink/?linkid=2250609)

## Forudsætninger

- Sørg for, at chat med Copilot-funktionen er aktiveret af en administrator. [Få mere at vide om konfigurering af Copilot- og AI-funktioner](enable-ai.md).
- Indstil dit visningssprog i Business Central til en af følgende engelske landestandarder: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Få flere oplysninger om, hvordan du ændrer sproget](ui-change-basic-settings.md#language).
- Sørg for, at dit Business Central-miljø er i alle lande/områder undtagen Canada (denne funktion er endnu ikke tilgængelig i Canada).

## Kom i gang med at bruge chat med Copilot

1. I øverste højre hjørne af skærmen skal du vælge ikonet ![Viser ikonet for chat med Copilot](media/chat-copilot-icon.png) **Copilot** ![Viser cllour nummer 1](media/callout-number-1.svg).

   Ruden **Copilot** vises som vist på billedet:
   
    ![Viser ikonet for chat med Copilot-ruden med billedforklaringer](media/chat-with-copilot-pane.svg)

1. Skriv dit spørgsmål i feltet **Stil et spørgsmål** nederst ![Viser billedforklaringsnummer 2](media/callout-number-2.svg), og vælg derefter pilespidsen, eller tryk på <kbd>Enter</kbd> for at få et svar.

   Dit input, kendt som en *prompt*, kan være et spørgsmål, en erklæring eller en kommando.

   > [!TIP]
   > Copilot indeholder et par funktioner, der kan hjælpe dig med at skrive spørgsmål:
   > - For at komme i gang med at formulere et spørgsmål skal du vælge en af de prompthjælpelinjer&mdash;**Find**, **Forklar** eller **Guide**&mdash;, der er tilgængelig øverst i ruden ![Viser billedforklaringsnummer 3](media/callout-number-3.svg) eller fra ![Viser promptguide-ikonet](media/prompt-guide-icon.png) **Vis prompter**-ikonet over boksen **Stil et spørgsmål** ![Viser forklaring nr. 4](media/callout-number-4.svg). Hjælpelinjer er foruddefinerede korte sætninger, der starter et spørgsmål eller en prompt. De sparer dig tid, guider Copilots svar mod en kategori af svar og hjælper dig med at lære at formulere spørgsmål for at få de bedste svar.
   > - Vælg promptforslagene over knappen **Vis prompter** ![Viser billedforklaringsnummer 5](media/callout-number-5.svg) for automatisk at stille et foruddefineret spørgsmål for at få indsigt i, hvordan spørgsmålene og svarene fungerer. Hurtige forslag er kun tilgængelige, når du bruger CRONUS-demoregnskabet.

1. Gennemse de svar, der vises i ruden Copilot ![Viser billedforklaring nummer 6](media/callout-number-6.svg).

   Afhængigt af dit spørgsmål kan svaret indeholde tekst, links til poster eller sider i Business Central og links til Business Central-hjælpeartikler om Microsoft Learn.

1. Stil et andet spørgsmål for at indsnævre svaret.

   Chat husker konteksten, hvilket betyder, at du ikke behøver at gentage nøglepunkter fra det oprindelige spørgsmål.

## Rydde chat for at starte forfra

Hvis du vil skifte til et andet samtaleemne med Copilot, skal du vælge ikonet ![Viser ikonet Ryd chat](media/clear-chat-icon.png) **Start en ny Copilot-chatsession**-ikonet nederst i ruden Copilot over spørgsmålsfeltet. Denne handling rydder Copilots hukommelse for dine sidste par beskeder. Det er ofte nyttigt at starte forfra efter en lang samtale med mange beskeder, og det kan hjælpe Copilot med at levere mere præcise svar.

Chatten ryddes også, hvis du lukker eller logger af Business Central.

## Tips til bedre spørgsmål

Her er nogle af de måder til, hvordan du kan forbedre de svar, du får fra Copilot:

- Stil klare og specifikke spørgsmål.
- Vær kortfattet og undgå lange sætninger eller flere sætninger.
- Stil ét spørgsmål ad gangen. <!--Avoid asking about multiple questions in one message.-->
- Brug naturligt sprog, der udtrykker spørgsmål på en venlig og konverserende måde.
- Brug nøgleord, udtryk og udtryk, som du ved bruges i Business Central, enten i appen eller i dokumentationen.
- Hvis det første svar ikke fuldt ud besvarer dine spørgsmål, skal du stille opfølgende spørgsmål eller omformulere det sidste spørgsmål.
- Hvis du stiller et spørgsmål om et andet emne end det forrige spørgsmål, skal du rydde den aktuelle chatsession for at starte forfra.

## Eksempler på prompter

Dine spørgsmål til Copilot varierer afhængigt af din rolle, aktuelle opgave, de processer, som din organisation følger, og hvordan du udtrykker dig med ord. Følgende er eksempler, der viser forskellige måder at stille spørgsmål på i chatruden, som kan inspirere dig til at skrive dine egne spørgsmål baseret på din egen situation.

Prompt: `Find the Item with Description 'ATHENS Desk'`

I dette eksempel giver du klare instruktioner til Copilot om at finde en enkelt post. Du antyder f.eks., at posten findes på listen Element. Du angiver, at feltet 'Beskrivelse' skal være en bestemt tekst, som du har skrevet ved hjælp af anførselstegn og med korrekte store bogstaver. Copilot reagerer normalt præcist, når den får et par præcise tip, men du kan også bruge et mere afslappet sprog som i det næste eksempel.

Prompt: `Give me the latest invoice for adatum`

I dette eksempel beder du Copilot om at finde en post, men spørgsmålet er mindre præcist og kan resultere i et mindre præcist svar. Copilot kan ofte forstå eller gætte på, at den faktura, du leder efter, ikke er en købsfaktura, men en salgsfaktura fra listen Bogført salgsfaktura. Copilot skal også matche `adatum` med `Adatum Corporation`, dvs. det fulde og præcise navn på det kundenavn, der er knyttet til fakturaen.

Prompt: `Show me customer ledger entries for Adatum from about three weeks ago`

I dette eksempel beder du copilot om at løse et fælles datopuslespil, der typisk kræver, at du åbner en kalender som reference eller bruger avancerede datointervalfiltre. Copilot kan normalt forstå almindelige udtryk og forretningsbetingelser.

Prompt: `How does I save my filterrings for later?`

I dette eksempel beder du Copilot om vejledning i, hvordan du udfører en opgave i Business Central. Copilot kan normalt forstå hensigten med dit spørgsmål, selvom der er et par grammatiske fejl, stavefejl eller forkortelser.

## Giv feedback på svar

Du kan bedømme de svar, du får fra Copilot, ved at bruge knappen Synes godt om (tommelfinger op) for god bedømmelse eller knappen Dislike (tommelfinger ned) for en dårlig bedømmelse. Når du vælger knappen Dislike, kan du vælge en årsag, herunder unøjagtig, upassende eller andet. Disse oplysninger kan hjælpe med at forbedre forslagene.

<!--
1. If you want help getting you're question started, select the prompts either from the **Find**, **Explain**, or **Guide** buttons at the top of the Coplit pane or use the **View Prompts** menu above **Ask a question** box at the bottom.

   Prompts are predefined short phrases that start a question. Apart from saving you time, they're designed to target responses to specific categories. They also help you undestand how you can phrase questions to get the responses.-->
   
## Se også

- [Fejlfinde Copilot- og AI-funktioner](ai-copilot-troubleshooting.md)  
- [Konfigurere Copilot- og AI-funktioner](enable-ai.md)  
- [Ofte stillede spørgsmål om ansvarlig kunstig intelligens til chat med Copilot](faqs-chat-with-copilot.md)  
- [Ressourcer til hjælp i Business Central](product-help-and-support.md)  
