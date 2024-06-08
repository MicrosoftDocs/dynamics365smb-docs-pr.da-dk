---
title: Opbygge finansrapporter med finansdata og kontokategorier
description: 'Beskriver, hvordan du kan bruge finansrapporter til at oprette forskellige visninger og rapporter til analyse af data for finansiel ydeevne.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---
# Forberede Financial Reporting med finansdata og kontokategorier

Du kan bruge **finansrapporter** til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan (COA). Du kan konfigurere finansrapporter til at analysere tal i finanskonti og sammenligner finansposter med budgetposter. Resultaterne vises i diagrammer og rapporter på rollecenteret, f.eks. tabellen Likviditet og resultatopgørelsen og balancerapporterne. Du kan få adgang til disse to rapporter, f.eks. med handlingen **Regnskabsopgørelser** på hjemmesider Business Manager og Revisor.  

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder eksempler på finansrapporter, som du kan bruge med det samme som skabeloner. Du kan også oprette dine egne rapporter for at angive de tal, der skal sammenlignes. Du kan f.eks. oprette finansrapporter for at beregne avancer med dimensioner som afdelinger eller debitorgrupper. Antallet af finansielle rapporter, du kan oprette, er ubegrænset og kræver ingen involvering af en udvikler.  

## Forudsætninger for regnskabsaflæggelse

Oprettelse af finansrapporter kræver en forståelse af strukturen i din kontoplan. Der er tre nøglebegreber, som du sandsynligvis skal være opmærksom på, før du designer dine økonomiske rapporter:

- Knyt finansbogføringskonti til finanskontokategorier.
- Design, hvordan du bruger dimensioner.
- Konfigurere finansbudgetter.

Finanskontokategorier forenkler definitionerne af finansielle rapporter og gør dem mere modstandsdygtige over for ændringer i kontoplanens struktur. Få mere at vide i [Brug finanskontokategorier til at ændre layoutet af regnskabet](bi-row-definitions.md#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

Når du konfigurerer dimensioner, kan du opdele dine økonomiske data på måder, der giver mening for din organisation. Flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md). 

Du kan f.eks. få vist finansposter som procenter af budgetposter, men det kræver, at du har oprettet budgetter. Flere oplysninger i [Oprette finansbudgetter](finance-how-create-budgets.md).

## Finansielle rapporter

Finansielle rapporter arrangerer konti fra din kontoplan på en måde, der gør det nemmere at præsentere data. Du kan oprette forskellige layout for at definere de oplysninger, du vil uddrage af kontoplanen. Finansielle rapporter udfører også beregninger, der ikke kan foretages direkte i diagrammet for kassekonti. Du kan f. eks. oprette subtotaler for grupper af konti og derefter medtage denne total i andre totaler. Et andet eksempel er at beregne avancer på dimensioner som afdelinger eller debitorgrupper. Desuden kan finansposter og budgetposter filtreres, f.eks. efter nettobevægelse eller debitbeløb.

> [!NOTE] 
> Tænk matematisk på en finansiel rapport som defineret af to ting:
>
> - En vektor af rækkedefinitioner, der definerer, hvad der skal beregnes.
> - En vektor af kolonnedefinitioner, der definerer dataene til beregningen.
>
> Den økonomiske rapport er så det ydre produkt af disse to vektorer, hvor hver celleværdi beregnes i henhold til formlen i den række, der anvendes på datadefinitionen fra kolonnen.

:::image type="content" source="media/financial-report-definition.svg" alt-text="Viser, hvordan en økonomisk rapport er opbygget ud fra en rækkedefinition og en kolonnedefinition." lightbox="media/financial-report-definition.svg":::

Siden **Finansrapporter** viser, hvordan alle økonomiske rapporter følger et mønster, der består af følgende attributter:

- Navn (kode)
- Beskrivelse
- Rækkedefinition
- Kolonnedefinition

:::image type="content" source="media/financial-reports.png" alt-text="Viser, hvordan alle økonomiske rapporter er opbygget ud fra en rækkedefinition og en kolonnedefinition." lightbox="media/financial-reports.png":::

> [!NOTE]
> Eksempelfinansrapporterne i er ikke klar til brug som [!INCLUDE[prod_short](includes/prod_short.md)] standard. Afhængigt af den måde, du konfigurerer finanskonti, dimensioner, finanskontokategorier og budgetter på, skal du justere definitionerne af række- og kolonneeksempler og de finansrapporter, de bruges i, så de passer til din opsætning.

Du kan også bruge formler til at sammenligne to eller flere finansielle rapporter og kolonnedefinitioner. Sammenligninger kan gøre følgende ting:

- Oprette tilpassede finansrapporter.
- Oprette lige så mange finansielle rapporter, der er brug for, hver med et entydigt navn.
- Oprette forskellige rapportlayout og udskrive rapporterne med de aktuelle tal.

## Læringssti: Oprette finansrapporter i Microsoft Dynamics 365 Business Central

Vil du lære at oprette budgetter og derefter bruge finansielle rapporter, dimensioner og række- og kolonnedefinitioner til at generere de økonomiske rapporter, der typisk er nødvendige for de fleste virksomheder?

Start med at lære i læringsstien [Oprette finansrapporter i Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central).

## Oprette en ny finansiel rapport

Du bruger finansielle rapporter til at analysere finanskonti eller sammenligne finansposter med budgetposter. Du kan f.eks. få vist finansposter som procenter af budgetposter.

De finansielle rapporter i standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] passer muligvis ikke til dine forretningsbehov. Du kan starte med at kopiere en eksisterende finansiel rapport for hurtigt at oprette dine egne rapporter som beskrevet i trin 3 nedenfor.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.  
1. På siden **Finansielle rapporter** skal du vælge **Ny** for at oprette et nyt navn til den finansielle rapport. Du kan også genbruge indstillinger fra en eksisterende finansiel rapport ved at vælge handlingen **Kopiér finansiel rapport**.
1. Udfyld rapportens korte navn (du kan ikke ændre navnet senere) og beskrivelsen.
1. Vælg en rækkedefinition og en kolonnedefinition.
1. Du kan også vælge analyser for række- og kolonnedefinitionerne.
1. Vælg handlingen **Rediger finansiel rapport** for at få adgang til flere egenskaber i den finansielle rapport.
1. I oversigtspanelet **Indstillinger** kan du redigere rapportbeskrivelsen, ændre række- og kolonnedefinitionerne og definere, hvordan datoer skal vises. Datoer kan være et dag/uge/måned/kvartal/år-hierarki eller kan vises med regnskabsperioder. Du kan lære mere i [Sammenligne regnskabsperioder ved hjælp af periodeformler](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas).
1. I oversigtspanelet **Dimensioner** kan du angive dimensionsfiltre for rapporten.
1. Du kan få vist et eksempel på rapporten i området under oversigtspanelet **Dimensioner**.

> [!TIP]
> Når du har oprettet en finansiel rapport, kan du bruge siden **Finansiel rapport** til at se og validere den. Vælg handlingen **Vis finansiel rapport** for at åbne siden.  

> [!NOTE]
> Når du åbner en økonomisk rapport i tilstanden Vis/Rediger, er filter ruden tilgængelig. Brug ikke Filterruden til at filtrere for data i rapporten. Sådanne filtre kan forårsage fejl, eller de filtrerer muligvis ikke dataene. Brug i stedet felterne i oversigtspanelerne **Indstillinger** og **Dimensioner** til at oprette filtre til rapporten.

### Oprette eller redigere en rækkedefinition

Rækkedefinitioner i finansielle rapporter udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti. Du kan f. eks. oprette subtotaler for grupper af konti og derefter medtage denne total i andre totaler. Du kan også beregne mellemliggende trin, der ikke vises i den endelige rapport.

Du kan få mere at vide ved at gå til [Rækkedefinitioner i finansrapportering](bi-row-definitions.md).

### Oprette eller redigere en kolonnedefinition

Brug kolonnedefinitioner til at angive, hvilke kolonner der skal med i den rapport, der oprettes. Du kan f.eks. udforme en rapport til sammenligning af bevægelse og saldo til dato for den samme periode dette år og sidste år. Du kan have op til 15 kolonner i en kolonnedefinition. Du kan f.eks. bruge flere kolonner til visning af budgetter for 12 måneder med en kolonne, der viser totalen.

Du kan få mere at vide ved at gå til [Kolonnedefinitioner i finansrapportering](bi-column-definitions.md).

## Brug af dimensioner i økonomiske rapporter

I finansielle analyser er en dimension data, som du kan føje til en post som en slags markør. Disse data bruges til at gruppere poster med ens karakteristika, f.eks. debitorer, regioner, produkter og sælger, og disse grupper kan nemt hentes frem til analyse. Du kan bruge dimensioner til poster i kladder, dokumenter og budgetter.

Hver dimension beskriver analysens fokus. En todimensional analyse kan f.eks. være pr. område. Hvis du bruger mere end to dimensioner, når du opretter en post, kan du udføre en mere kompleks analyse. Et eksempel på en kompleks analyse er at undersøge salg pr. salgskampagne pr. kundegruppe pr. område. Så får du større indsigt i din forretning, så du kan evaluere oplysningerne, f.eks. om hvor godt din forretning kører, hvor den blomster og hvor det ikke gør det, og hvor der bør allokeres flere ressourcer. Denne indsigt hjælper dig med at træffe mere informerede forretningsbeslutninger. Hvis du vil vide mere, skal du gå til [Arbejde med dimensioner](finance-dimensions.md).

## Oprette finansielle rapporter med oversigter

Du kan bruge en financiel rapport til at oprette en opgørelse, hvor tallene i finansposter sammenlignes med tallene i finansbudgettet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
1. Vælg en finansiel rapport på siden **Finansielle rapporter**.  
1. Vælg handlingen **Rediger rækkedefinition**  
1. På siden **Rækkedefinition** skal du vælge standardnavnet til den finansielle rapport i feltet **Navn**.
1. Vælg handlingen **Indsæt finanskonti**.  
1. Vælg de konti, du vil medtage i udtoget, og vælg **OK**.

    Kontiene indsættes i din finansielle rapport. Hvis du vil, kan du også ændre kolonnedefinitionen.  
1. Vælg handlingen **Rediger finansiel rapport**.  
1. På siden **Finansiel rapport** i oversigtspanelet **Dimensioner** skal du indstille budgetfilteret til det ønskede filternavn.  
1. Vælg **OK**.  

Du kan nu kopiere og indsætte budgetoversigten i et regneark..  

## Integrere finansielle rapporter med Excel

Du kan integrere en økonomisk rapport med en Excel-projektmappeskabelon, justere layoutet, så det passer til dine behov, og derefter opdatere Excel-skabelonen med data fra [!INCLUDE[prod_short](includes/prod_short.md)]. Denne integration gør det f.eks. nemmere at generere dine månedlige og årlige regnskaber i et format, der fungerer for dig.

### Konfigurere Excel-integration for en økonomisk rapport (oprette en Excel-skabelon)

Hvis du vil konfigurere Excel-integration for en økonomisk rapport, skal du følge disse trin for at oprette en Excel-skabelon til en rapport.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansrapporter**, og vælg derefter det relaterede link.
1. På siden **Finansielle rapporter** skal du vælge den relevante finansielle rapport til aktivering med Excel, og vælge **Eksportér til Excel**.
1. Vælg handlingen **Opret nyt dokument**. Denne handling henter en Excel-skabelonprojektmappe med et enkelt regneark, der er opkaldt efter rapportnavnet.
1. Kopiér regnearket, og omdøb det til **Data**.
1. Omdøb rapportregnearket efter eget valg.
1. Markér alle celler, der viser data fra den økonomiske rapport (herunder kolonne- og rækkeoverskrifter), i rapportregnearket. På båndet **Hjem** skal du finde menuen **Tal** og vælge **Generelt** som format.
1. Vælg cellen længst til venstre i området med data fra den økonomiske rapport, og angiv en reference til den tilsvarende celle i dataregnearket. Træk formlen til højre for at udvide den til alle celler i den første række, og træk derefter rækken ned for at dække alle rækker i den økonomiske rapport.
1. Skjul **dataregnearket**.
1. Formatér rapportkladden, så den passer til dine behov.
1. Gem projektmappen på OneDrive eller et lignende sted, hvor filen sikkerhedskopieres og versioneres.
1. Luk projektmappen.

### Køre en økonomisk rapport med en Excel-skabelon

Hvis du vil køre en økonomisk rapport med en Excel-skabelon, skal du følge disse trin:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansrapporter**, og vælg derefter det relaterede link.
1. På siden **Finansielle rapporter** skal du vælge den relevante finansielle rapport til aktivering med Excel, og vælge **Eksportér til Excel**.
1. Vælg handlingen **Opdater kopi af eksisterende dokument**.
1. Overfør din Excel-skabelon (luk Excel-projektmappen, før du overfører den).
1. På siden **Navn/værdiopslag** skal du vælge dataregnearket.
1. [!INCLUDE[prod_short](includes/prod_short.md)] kører den økonomiske rapport og fletter de resulterende data med din Excel-skabelon.

## Udskrive og gemme finansielle rapporter

Du kan udskrive finansielle rapporter ved at bruge enhedens udskrivningsservice. [!INCLUDE[prod_short](includes/prod_short.md)] giver også muligheder for at gemme rapporter som Excel-projektmapper, Word-dokumenter, PDF-filer og XML-filer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
1. På siden **Finansielle rapporter** skal du vælge den rapport, du vil udskrive, og vælge **Udskriv**.
1. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Vælg den enhed, som rapporten skal sendes til, i feltet **Printer**.
    1. Indstillingen **(Håndteres af browseren)** angiver, at der ikke er en udvalgt printer til rapporten. I dette tilfælde vil browseren håndtere udskriften og vise en standard oplevelse, hvor du kan vælge en lokal printer, der er tilsluttet enheden. **(Håndteres af browseren)** er ikke tilgængelig i mobilappen [!INCLUDE[prod_short](includes/prod_short.md)] eller appen til Teams.
1. Vælg handlingen **Udskriv**.

### Planlægge en finansiel rapport eller gemme som et PDF-, Word-eller Excel-dokument

Du kan gemme en finansrapport i filformater som f.eks. PDF, XML, Word eller Excel. [!INCLUDE[prod_short](includes/prod_short.md)] kan også generere gentagne finansrapporter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
1. På siden **Finansielle rapporter** skal du vælge handlingen **Udskriv**.
1. Angiv rapporten tilsvarende, og vælg derefter handlingen **Send til**.
1. Vælg filformatet eller handlingen **Planlægning**, og vælg **OK**.
1. Udfyld felterne for at oprette en planlagt eller tilbagevendende finansiel rapport. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>For tilbagevendende finansielle rapporter skal du angive felterne **Tidligste startdato/-klokkeslæt** og **Udløbsdato/-klokkeslæt** med den første og sidste dato for at oprette den finansielle rapport. Du kan også vælge, hvilke dage rapporten oprettes, ved at angive feltet **Datoformel for næste kørsel** efter det format, der er forklaret i sektionen [Bruge datoformler](ui-enter-date-ranges.md#use-date-formulas).


## Bedste fremgangsmåder for arbejde med definitioner af finansrapporter

Definitioner af finansrapporter versioneres ikke. Når du ændrer en rapportdefinition, erstattes den gamle version, når ændringen gemmes i databasen. Følgende liste indeholder nogle anbefalede fremgangsmåder til at arbejde med definitioner af finansrapporter:

- Hvis du tilføjer rapportdefinitioner, skal du vælge en god kode og udfylde beskrivelsesfeltet med en meningsfuld tekst, mens du stadig ved, hvad du bruger rapporten til. Disse oplysninger hjælper dine kolleger (og dit fremtidige jeg) med at arbejde med rapporten og måske ændre rapportdefinitionen.
- Før du ændrer en rapportdefinition, kan du overveje at tage en kopi af den som sikkerhedskopi, hvis ændringen ikke fungerer som forventet. Du kan enten bare kopiere definitionen (give den et godt navn) eller eksportere den. Hvis du vil lære mere, skal du gå til [Importere eller eksportere definitioner for finansrapporter](#import-or-export-financial-report-definitions).
- Hvis du har brug for en ny kopi af en definition, som [!INCLUDE[prod_short](includes/prod_short.md)] leverer, er en nem måde at få en på at oprette et nyt regnskab, der kun indeholder opsætningsdata. Du kan derefter eksportere definitionen og importere den i det regnskab, hvor definitionen skal opdateres.

## Importere eller eksportere finansrapportdefinitioner

Du kan importere og eksportere finansrapportdefinitioner som RapidStart-konfigurationspakker. Konfigurationspakker er f. eks. nyttige, når du vil dele oplysninger med andre firmaer. Pakken oprettes i en .rapidstart-fil, som komprimerer indholdet.

> [!NOTE]
> Når du importerer finansrapportdefinitioner, erstattes eksisterende poster med samme navn som dem, der importeres, med nye definitioner. Konfigurationspakken til en rapportdefinition overskriver ikke eksisterende række- eller kolonnedefinitioner, der bruges i rapportdefinitionen.

Følg disse trin for at importere eller eksportere definitioner af økonomiske rapporter:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
1. Vælg den finansielle rapport, og vælg derefter **Indlæs finansiel rapport** eller **Udlæs finansiel rapport**, afhængigt af hvad du vil gøre.

Du kan få mere at vide om, hvordan du importerer eller eksporterer definitioner af række- eller kolonnedefinitioner til finansrapporter, i følgende artikler: 

- [Importere eller eksportere rækkedefinitioner for finansrapporter](bi-row-definitions.md#import-or-export-financial-reporting-row-definitions) eller
- [Importere eller eksportere kolonnedefinitioner til finansrapportering](bi-column-definitions.md#import-or-export-financial-report-column-definitions)

## Se også

[Rækkedefinitioner i Financial Reporting](bi-row-definitions.md)  
[Kolonnedefinitioner i Financial Reporting](bi-column-definitions.md)  
[Køre og udskrive rapporter](ui-work-report.md)  
[Økonomisk Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
