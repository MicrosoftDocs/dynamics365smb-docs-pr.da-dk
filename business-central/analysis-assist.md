---
title: Analysere data på lister med hjælp fra Copilot (forhåndsversion)
description: 'Få mere at vide om, hvordan du kan bruge Copilot i Business Central til at analysere data.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/13/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# Analysere data på lister med hjælp fra Copilot (forhåndsversion)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

I denne artikel forklares det, hvordan du kan bruge *analyseassistenten* som en hjælp til at analysere data på listesider.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Om analyseassistent

Analyseassistent er en Copilot for [analysetilstanden](analysis-mode.md) på listesider i Business Central. Analysetilstand er en interaktiv og alsidig måde at beregne, opsummere og gennemgå data på. Hvis du vil analysere data i analysetilstand, skal du oprette en *analysefane*, hvor du transformerer dataene, så de viser de ønskede sammenlægninger og opsummeringer. Du kan f.eks. arrangere felter i rækker og kolonner, angive filtre, sortere kolonner og pivotere felter. Med analysehjælp opnår du i stedet for at udføre denne opgave manuelt meget af det samme&mdash;eller mindst som en start&mdash;ved at bruge ord. Ved at udtrykke den ønskede struktur i naturligt sprog, f.eks. "sorter efter mængde fra mindste til største" eller "vis gennemsnitlig pris pr. kategori", bruger analyseassistenten AI til at generere et foreslået layout på en analysefane.

## Tilgængelige sprog

[!INCLUDE[analysis-assist-language-support](includes/analysis-assist-language-support.md)]

## Forudsætninger

- Analyseassistentfunktionen er aktiveret, og du får tilladelse til at bruge den. Denne opgave er udføres typisk af en administrator. [Du kan finde flere oplysninger i konfigurere Copilot og AI-funktioner](enable-ai.md).
<!-- - The display language in Business Central is set to one the following English locales: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Learn how to change the language](ui-change-basic-settings.md#language)-->
<!-- - Your Business Central environment is in any country/region except Canada (this feature isn't yet available in Canada).-->

## Kom i gang

1. Åbn den listeside, du vil analysere.

   Hvis du f. eks. vil arbejde med siden **Varer**, skal du vælge ![Forstørrelsesglas, der åbner funktionen Fortæl mig](media/ui-search/search_small.png). ikon (<kbd>Alt</kbd>+<kbd>Q</kbd>), enter *varer*, og vælg derefter det relaterede link.

1. Du kan begynde at analysere data med Copilot direkte fra listesiden eller ved først at gå ind i analysetilstand. Brug et af følgende trin til at komme i gang:

    - På handlingslinjen øverst på siden skal du vælge ![Viser copilotikonet](media/copilot-icon.png) **Copilot** > **Analyze-listen**.
    - På handlingslinjen øverst på siden skal du vælge ![Viser ikonet for indtastningsanalysetilstand](media/analysis-mode-icon.png) **Skift til analysetilstand**, og vælg derefter ![Vis copilotikonet](media/copilot-icon.png) **Copilot** > **Opret ny analyse**.

1. I vinduet **Analysér varer** med Copilot skal du indtaste en beskrivelse af det ønskede layout. Denne beskrivelse kaldes en *prompt*.

    ![Viser analyseassistenten Copilot](media/analysis-assist.png)

    > [!TIP]
    > Hvis du vil have hjælp til at skrive en prompt, skal du vælge ![Viser visningspromptikonet](media/prompt-guide-icon.png) **Promptguide** og vælge en af mulighederne for at komme i gang. Teksten i parentes `[ ]` vises kun som et eksempel og vises ikke i vinduet Copilot.

1. Vælg **Generer**, og vent derefter, mens Copilot genererer layoutet på den nye analysefane.
1. Gennemse resultaterne på den nye analysefane.

   > [!NOTE]
   > Hvis du navigerer væk fra den nye analysefane (f.eks. går til en anden analysefane eller -side) eller foretager layoutændringer på fanen (f.eks. sorterer kolonner eller ændrer indstillinger under fanerne **Kolonner** og **Analysefiltre**), gemmes den nye analysefane automatisk, og Copilot lukkes.

1. Hvis du vil ændre den genererede analyse, kan du udføre et af disse trin:

   - Hvis du vil bygge videre på de tidligere instruktioner, skal du angive oplysningerne i feltet **Tilføj flere oplysninger om analysen** og derefter vælge ![Vis justeringspilen](media/analysis-assist-adjust-button.png) **Juster**-pilen. Copilot husker dine tidligere instruktioner og bruger dem til at foretage justeringer.

   - Hvis du vil starte fra bunden med at tilføje nye instruktioner, skal du vælge ![ikonet Viser blyantikonet](media/edit-pencil.png) **Rediger prompt:**, føje oplysningerne til prompten og derefter vælge **Generer**.

1. Hvis du vil gemme analysefanen, skal du vælge **Behold den**. Hvis du ikke vil gemme den, skal du vælge **Kassér**.

## Prompt-tips og eksempler

Det er vigtigt at oprette effektive prompter til Copilot for at få nøjagtige og relevante analyseforslag. Du kan også minimere tekst, du tilføjer i prompter, så den bliver hurtigere, når du skriver. Her er nogle tips og retningslinjer efterfulgt af nogle eksempler:

- Vær kortfattet og undgå lange sætninger eller flere sætninger.
- Sørg for, at feltnavne, der bruges i prompter, ligger nogenlunde tæt på de faktiske feltnavne på siden.
- Brug naturligt sprog, der udtrykker den ønskede datastruktur på en venlig og konverserende måde.
- Brug almindelige nøgleord, udtryk og udtryk, der bruges i dataanalyse, f.eks. `group by` `sum` `sort by`. osv.
- Hvis det første svar ikke er, hvad du ønsker, skal du tilføje opfølgningsinstruktioner eller omformulere den sidste instruktion.
- Almindelige forkortelser er acceptable.
- Brevkasse er ikke vigtigt.

### Eksempler

Følgende prompteksempler bruger analyseassistenten på listen **Elementer**. Siden med varer indeholder tre oversigtsfelter til analyse: **Varebeholdning**, **Kostpris**, **Salgspris**.

Prompt: `Show items by brand and unit of measure`

Denne prompt forsøger at vise totaler for alle sumfelter, grupperet efter mærke og feltet **Basisenhed**. Men i dette tilfælde stemmer "brand" ikke overens med noget feltnavn, så Copilot kan sandsynligvis ikke finde et tilsvarende felt. Derefter bliver du bedt om at omformulere prompten og prøve igen.

Prompt: `Show items by type and uom`

Denne prompt viser totaler for alle sumfelter, grupperet efter **Type** og **Basisenhed**. Men i stedet for at skrive "måleenhed" bruges forkortelsen `uom`.

Prompt: `Show total quantity per type per UoM`

Denne prompt opretter en pivottabel i feltet **Disponibelt** antal pr. **Basisenhed** pr. **Type**.

## Se også

[Ofte stillede spørgsmål om ansvarlig AI til analysehjælp](faqs-analysis-assist.md)  
[Ad hoc-dataanalyse](reports-adhoc-analysis.md)  
