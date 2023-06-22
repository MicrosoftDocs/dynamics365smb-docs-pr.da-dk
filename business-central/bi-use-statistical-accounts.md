---
title: Bruge statistiske konti til at analysere ikke-transaktionsdata
description: 'Beskriver, hvordan du bruger statistiske konti som en anden datakilde til dine analyser.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/07/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, financial report'
ms.search.form: '2632, 2631, 2633, 2623, 2634'
---
# <a name="analyze-data-with-statistical-accounts" />Analysere data med statistiske konti

Brug statistiske konti til at supplere oplysninger i regnskabsrapporter. Med statistiske konti kan du tilføje målinger, der er baseret på ikke-transaktionsdata. Du tilføjer ikke-transaktionsdata som nummerbaserede enheder, f.eks.:

* Antal medarbejderansatte
* Firkantet optagelse
* Det antal debitorer, der har forfaldne konti

Du kan f. eks. måle omsætning eller omkostninger baseret på antallet af personer i en afdeling. Afdelingens medarbejdernummer er enheden for den statistiske konto. Følgende billede viser et eksempel på en rapport, hvor der bruges en statistik konto til at vise omsætning pr. medarbejder.

:::image type="content" source="media/statistical account report example.png" alt-text="Et eksempel på en rapport, der indeholder data fra en statistisk konto":::

Når de arbejder, svarer de statistiske konti til bogføringskonti. De gemmer transaktioner, som du bogfører vha. statistiske konto kladder, så du kan bruge transaktionerne som data til finansrapporter. Flere oplysninger om finansrapporter i [Forberede Financial Reporting med finansdata og kontokategorier](bi-how-work-account-schedule.md). 

Der er et par vigtige forskelle mellem de statistiske konti og bogføringskonti. Statistiske konti er separate enheder og medtages ikke i rapporter om råbalance. Du behøver heller ikke at afstemme debet-og kreditbeløb, når du bruger statistiske konto kladder til at bogføre poster til en statistisk konto. Du skal blot bogføre beløbet.

## <a name="set-up-a-statistical-account" />Sådan oprettes en statistisk konto

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Statistiske konti**, og vælg derefter det relaterede link.
1. Udfyld felterne i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="post-amounts-to-a-statistical-account" />Bogføre beløb på en statistisk konto

1. Hvis du vil bogføre de beløb, der skal spores, skal du vælge handlingen **Kladde til statistiske konti** på siden **Statistiske konti**.
1. I feltet **Bogføringsdato** skal du angive den sidste dato i den bogføringsperiode, du vil bogføre beløb for.
1. Valgfrit: Hvis du vil spore beløb for et bestemt dokument, skal du i feltet **Bilagsnr.** skal du angive dokumentets ID.
1. I feltet **Statistisk kontonr.** skal du vælge det statistiske kontonummer, som du vil bogføre beløb til.
1. I feltet **Beskrivelse** kan du indtaste en kort beskrivelse af, hvad du måler.  
1. Angiv det beløb, der skal tilbagebetales, i feltet **Beløb**. 
1. Valgfrit: Hvis du vil medtage den statistiske konto i mere avancerede analyser, skal du angive dimensioner i felterne **Afdelingskode** og **Debitorgruppekode**. Hvis du vil vide mere om dimensioner, skal du gå til [Analyse af data for dimensioner](bi-how-analyze-data-dimension.md).

## <a name="verify-statistical-account-amounts" />Kontrollere statistiske kontobeløb

Brug handlingen **Statistisk kontoafstemning** på siden **Statistiske konti** for at kontrollere, at de registrerede beløb er korrekte for hver periode.  

## <a name="include-the-statistical-account-in-a-financial-report" />Medtage den statistiske konto i en finansiel rapport

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
1. Opret en ny økonomisk rapport på en af følgende måder:
    1. Klik på **Ny** for at starte fra bunden. Hvis du vil vide mere om oprettelse af regnskabsrapporter, skal du gå til [Oprette en ny økonomisk rapport](bi-how-work-account-schedule.md#create-a-new-financial-report).
    1. Hvis du vil bruge indstillinger fra en lignende rapport, som du allerede har, skal du vælge den rapport, du vil kopiere, og derefter vælge handlingen **Kopier finansrapport**. Du kan redigere de indstillinger, du kopierer, i den nye rapport.
1. TIlføj statistisk konto:
    1. Hvis du starter fra bunden, skal du vælge handlingen **Rediger rækkedefinition**.
    1. Hvis du vil bruge række definition fra en eksisterende rapport, skal du vælge den rapport, du vil kopiere, og derefter vælge handlingen **Kopier rækkedefinition**.
1. I **Rækkenr.** på siden **Rækkedefinition** felt, skal du du angive, hvor rækken skal vises i rækkefølgen af rækker i rapporten.
1. I feltet **Beskrivelse** kan du indtaste den tekst, der angiver, hvad du måler.
1. Vælg **Statistiske konti** i feltet **Sammentællingstype**.
1. Vælg en statistisk konto i feltet **Sammentælling**.
1. I feltet **rækketype** skal du vælge, om saldoen på bogføringsdatoen eller begyndelsen af bogføringsperioden skal vises, eller om der skal vises en ændring i beløbet i perioden.
1. Udfyld de resterende felter. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also" />Se også

[Financial Business Intelligence](bi.md)  
[Finansrapporter og analyser i Business Central](finance-reports.md)
