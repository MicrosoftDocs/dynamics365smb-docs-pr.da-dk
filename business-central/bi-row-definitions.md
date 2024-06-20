---
title: Rækkedefinitioner i Financial Reporting
description: 'Beskriver, hvordan rækkedefinitioner i Financial Reporting fungerer.'
author: kennieNP
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# Rækkedefinitioner i Financial Reporting

Rækkedefinitioner i finansielle rapporter udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti. Du kan f. eks. oprette subtotaler for grupper af konti og derefter medtage denne total i andre totaler. Du kan også beregne mellemliggende trin, der ikke vises i den endelige rapport.

## Oprette eller redigere en rækkedefinition

Opret eller rediger en rækkedefinition ved at følge disse trin:

1. På siden **Finansielle rapporter** skal du vælge den relevante finansielle rapport og vælge **Rediger kolonnedefinition**.
1. Vælg handlingerne **Indsæt finanskonti**, **Indsæt CF-konti** og **Indsæt omkostningstype** for at oprette en række for hvert økonomiske element, du vil analysere. Du kan f. eks. have én række til det aktuelle anlægsaktiv og en anden række til anlægsaktiver. Du kan finde inspiration ved at udforske finansrapporterne i CRONUS-demoregnskabet.

    > [!NOTE]
    > **Rækkenummer** feltet viser de første 10 tegn i et id, f.eks. et kontonummer. Hvis du tilføjer elementer med id'er, der starter med de samme 10 tegn, vil du have dubletter i feltet **Rækkenr.** . Hvis det er nødvendigt, kan du redigere id'er manuelt, efter at du har indsat elementerne. De fulde id'er vises i feltet **Sammentælling**.

> [!NOTE]
> De kolonner, som du definerer i hver række, i rækkedefinitionen repræsenterer kolonnerne tre og op på siden **Finansiel rapport**. De to første kolonner **Rækkenr.** og **Beskrivelse** er faste.  

## Indbyggede rækkedefinitioner

[!INCLUDE[prod_short](includes/prod_short.md)] Indeholder eksempler på rækkedefinitioner, der kan hjælpe dig med hurtigt at komme i gang med at oprette finansrapporter, der passer til dine behov.

<!-- update this when we release the new templates in 24.1
| Row definition code | Description | How to use this row definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 | 
-->

> [!NOTE]
> Eksempelfinansrapporterne i er ikke klar til brug som [!INCLUDE[prod_short](includes/prod_short.md)] standard. Afhængigt af den måde, du konfigurerer finanskonti, dimensioner, finanskontokategorier og budgetter på, skal du justere definitionerne af række- og kolonneeksempler og de finansrapporter, de bruges i, så de passer til din opsætning.

## Brug finanskontokategorier til at ændre layoutet af regnskabet

Du kan bruge finanskontokategorier til at ændre layoutet af regnskabet. Når du f.eks. har oprettet kontokategorierne på siden **Finanskontokategorier**, kan du vælge handlingen **Generér finansielle rapporter** og opdatere de underliggende finansielle rapporter for de grundlæggende finansielle rapporter. Næste gang du kører en af disse rapporter, f.eks. rapporten **Saldoopgørelse**, tilføjes nye totaler og underordnede linjer.

En anden fordel ved at bruge finanskontokategorier frem for de rå finanskonti i rækkedefinitionerne er, at en ændring i kontoplanens struktur ikke påvirker dine økonomiske rapporter.

> [!NOTE]
> De øverste kontokategorier, f.eks. **Gæld**-noden, er faste, og du kan ikke tilføje dine egne. Du kan dog slette og tilføje kontokategorier på lavere niveauer og ændre strukturen for at definere, hvordan den finansielle rapport vises i rapporter.
>
> Du bør oprette og opbygge dine egne finanskontokategorier på lavere niveauer fra bunden i et hierarki, hvis det er nødvendigt, i stedet for at prøve at omarrangere de eksisterende. Du kan f.eks. omstrukturere noden **Gæld**, så den indeholder en ny **Egenkapital**-node efterfulgt af noderne **Aktuelle passiver** og **Langfristet gæld**. Få flere oplysninger under [Knytte finanskonti til kontokategorier](finance-general-ledger.md#account-categories).

## Bedste fremgangsmåder for arbejde med rækkedefinitioner

Rækkedefinitioner versioneres ikke. Når du ændrer en rækkedefinition, erstattes den gamle version, når ændringen gemmes i databasen. Følgende liste indeholder nogle anbefalede fremgangsmåder til at arbejde med rækkedefinitioner:

- Hvis du tilføjer rækkedefinitioner, skal du vælge en god kode og udfylde beskrivelsesfeltet med en meningsfuld tekst, mens du stadig ved, hvad du bruger rækkedefinitionen til. Disse oplysninger hjælper dine kolleger (og dit fremtidige jeg) med at arbejde med Financial Reporting og måske ændre rækkedefinitionen.
- Før du ændrer en rækkedefinition, kan du overveje at tage en kopi af den som sikkerhedskopi, hvis ændringen ikke fungerer som forventet. Du kan enten bare kopiere definitionen (give den et godt navn) eller eksportere den. Hvis du vil lære mere, skal du gå til [Importere eller eksportere rækkedefinitioner](#import-or-export-financial-reporting-row-definitions).
- Hvis du har brug for en ny kopi af en definition, som [!INCLUDE[prod_short](includes/prod_short.md)] leverer, er en nem måde at få en på at oprette et nyt regnskab, der kun indeholder opsætningsdata. Du kan derefter eksportere definitionen og importere den i det regnskab, hvor definitionen skal opdateres.

## Importere eller eksportere rækkedefinitioner for Financial Reporting

Du kan importere og eksportere finansrækkedefinitioner som RapidStart-konfigurationspakker. Konfigurationspakker er f. eks. nyttige, når du vil dele oplysninger med andre firmaer. Pakken oprettes i en .rapidstart-fil, som komprimerer indholdet.

> [!NOTE]
> Når du importerer rækkedefinitioner til Financial Reporting, erstattes eksisterende poster med samme navn som dem, der importeres, med nye definitioner. Konfigurationspakken til en rapportdefinition overskriver ikke eksisterende række- eller kolonnedefinitioner, der bruges i rapportdefinitionen.

Følg disse trin for at importere eller eksportere rækkedefinitioner af økonomiske rapporter:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Rækkedefinitioner** og vælg derefter det relaterede link.
1. Vælg rækkedefinitionen, og vælg derefter **Importer rækkedefinition** eller **Eksporter rækkedefinition**, afhængigt af hvad du vil gøre.

## Se også

[Kolonnedefinitioner i Financial Reporting](bi-column-definitions.md)  
[Klargøre Financial Rapportering](bi-how-work-account-schedule.md)  
[Økonomisk Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
