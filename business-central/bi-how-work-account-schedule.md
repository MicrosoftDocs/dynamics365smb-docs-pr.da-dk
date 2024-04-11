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

Finanskontokategorier forenkler definitionerne af finansielle rapporter og gør dem mere modstandsdygtige over for ændringer i kontoplanens struktur. Få mere at vide i [Brug finanskontokategorier til at ændre layoutet af regnskabet](#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

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

* Navn (kode)
* Beskrivelse
* Rækkedefinition
* Kolonnedefinition

:::image type="content" source="media/financial-reports.png" alt-text="Viser, hvordan alle økonomiske rapporter er opbygget ud fra en rækkedefinition og en kolonnedefinition." lightbox="media/financial-reports.png":::

> [!NOTE]
> Eksempelfinansrapporterne i er ikke klar til brug som [!INCLUDE[prod_short](includes/prod_short.md)] standard. Afhængigt af den måde, du konfigurerer finanskonti, dimensioner, finanskontokategorier og budgetter på, skal du justere definitionerne af række- og kolonneeksempler og de finansrapporter, de bruges i, så de passer til din opsætning.

Du kan også bruge formler til at sammenligne to eller flere finansielle rapporter og kolonnedefinitioner. Sammenligninger kan gøre følgende ting:

* Oprette tilpassede finansrapporter.
* Oprette lige så mange finansielle rapporter, der er brug for, hver med et entydigt navn.
* Oprette forskellige rapportlayout og udskrive rapporterne med de aktuelle tal.

## Læringssti: Oprette finansrapporter i Microsoft Dynamics 365 Business Central

Vil du lære at oprette budgetter og derefter bruge finansielle rapporter, dimensioner og række- og kolonnedefinitioner til at generere de økonomiske rapporter, der typisk er nødvendige for de fleste virksomheder?

Start med at lære i læringsstien [Oprette finansrapporter i Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central)

## Oprette en ny finansiel rapport

Du bruger finansielle rapporter til at analysere finanskonti eller sammenligne finansposter med budgetposter. Du kan f.eks. få vist finansposter som procenter af budgetposter.

De finansielle rapporter i standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] passer muligvis ikke til dine forretningsbehov. Du kan starte med at kopiere en eksisterende finansiel rapport for hurtigt at oprette dine egne rapporter som beskrevet i trin 3 nedenfor.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.  
1. På siden **Finansielle rapporter** skal du vælge **Ny** for at oprette et nyt navn til den finansielle rapport. Du kan også genbruge indstillinger fra en eksisterende finansiel rapport ved at vælge handlingen **Kopiér finansiel rapport**.
1. Udfyld rapportens korte navn (dette kan ikke ændres) og beskrivelsen.
1. Vælg en rækkedefinition og en kolonnedefinition.
1. Du kan også vælge analyser for række- og kolonnedefinitionerne.
1. Vælg handlingen **Rediger finansiel rapport** for at få adgang til flere egenskaber i den finansielle rapport.
1. I oversigtspanelet **Indstillinger** kan du redigere rapportbeskrivelsen, ændre række- og kolonnedefinitionerne og definere, hvordan datoer skal vises. Datoer kan være et dag/uge/måned/kvartal/år-hierarki eller kan vises med regnskabsperioder. Du kan lære mere i [Sammenligne regnskabsperioder ved hjælp af periodeformler](#comparing-accounting-periods-using-period-formulas).
1. I oversigtspanelet **Dimensioner** kan du angive dimensionsfiltre for rapporten.
1. Du kan få vist et eksempel på rapporten i området under oversigtspanelet **Dimensioner**.

> [!TIP]
> Når du har oprettet en finansiel rapport, kan du bruge siden **Finansiel rapport** til at se og validere den. Vælg handlingen **Vis finansiel rapport** for at åbne siden.  

> [!NOTE]
> Når du åbner en økonomisk rapport i tilstanden Vis/Rediger, er filter ruden tilgængelig. Brug ikke Filterruden til at filtrere for data i rapporten. Sådanne filtre kan forårsage fejl, eller de filtrerer muligvis ikke dataene. Brug i stedet felterne i oversigtspanelerne **Indstillinger** og **Dimensioner** til at oprette filtre til rapporten.

### Oprette eller redigere en rækkedefinition

Rækkedefinitioner i finansielle rapporter udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti. Du kan f. eks. oprette subtotaler for grupper af konti og derefter medtage denne total i andre totaler. Du kan også beregne mellemliggende trin, der ikke vises i den endelige rapport.

1. På siden **Finansielle rapporter** skal du vælge den relevante finansielle rapport og vælge **Rediger kolonnedefinition**.
1. Vælg handlingerne **Indsæt finanskonti**, **Indsæt CF-konti** og **Indsæt omkostningstype** for at oprette en række for hvert økonomiske element, du vil analysere. Du kan f. eks. have én række til det aktuelle anlægsaktiv og en anden række til anlægsaktiver. Du kan finde inspiration ved at udforske finansrapporterne i CRONUS-demoregnskabet.

    > [!NOTE]
    > **Rækkenummer** feltet viser de første 10 tegn i et id, f.eks. et kontonummer. Hvis du tilføjer elementer med id'er, der starter med de samme 10 tegn, vil du have dubletter i feltet **Rækkenr.** . Hvis det er nødvendigt, kan du redigere id'er manuelt, efter at du har indsat elementerne. De fulde id'er vises i feltet **Sammentælling**.

> [!NOTE]
> De kolonner, som du definerer i hver række, i rækkedefinitionen repræsenterer kolonnerne tre og op på siden **Finansiel rapport**. De to første kolonner **Rækkenr.** og **Beskrivelse** er faste.  

### Oprette eller redigere en kolonnedefinition

Brug kolonnedefinitioner til at angive, hvilke kolonner der skal med i den rapport, der oprettes. Du kan f.eks. udforme en rapport til sammenligning af bevægelse og saldo til dato for den samme periode dette år og sidste år. Du kan have op til 15 kolonner i en kolonnedefinition. Du kan f.eks. bruge flere kolonner til visning af budgetter for 12 måneder med en kolonne, der viser totalen.

> [!NOTE]
> En udskrevet/vist/gemt version af en finansiel rapport viser højst fem kolonner. Hvis en finansiel rapport kun er beregnet til analyse på siden **Finansiel rapport**, kan du derimod oprette så mange kolonner, du vil.

1. På siden **Finansielle rapporter** skal du vælge den relevante finansielle rapport, du har oprettet, og vælge **Rediger kolonnedefinition**.
1. På siden **Kolonnedefinition** skal du oprette en række til hver kolonne med finansielle data, der vises efter i finansrapporten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Vælg **OK**.
1. Åbn siden **Finansiel rapport** fra tid til anden for at kontrollere, at den nye kolonnedefinition fungerer korrekt.

### Opret en kolonnedefinition for at beregne procenten

Du vil muligvis gerne medtage en kolonne i en finansiel rapport for at beregne procenter af et totalbeløb. Hvis du f.eks. har et antal rækker, som specificerer salg efter dimension, kan du have en kolonne, som angiver procenten af det samlede salg i hver række.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
1. Vælg en finansiel rapport på siden **Finansielle rapporter**.  
1. Vælg handlingen **Rediger finansiel rapport** for at konfigurere en finansiel rapportrække til beregning af den total, som procentdelene baseres på.  
1. indsæt en linje lige over den første række, som du vil vise en procent for.  
1. Udfyld felterne på linjen på følgende måde: I feltet **Sammentællingstype** skal du angive **Angiv grundlag for procent**. I feltet **Sammentælling** skal du indtaste en formel for den total, som procentdelen skal baseres på. Hvis række 11 f.eks. indeholder det samlede salg, indtastes **11**.  
1. Vælg handlingen **Rediger kolonnedefinition** for at oprette en kolonne.  
1. Udfyld felterne på linjen som angivet. I feltet **Kolonnetype** skal du vælge **Formel**. I feltet **Formel** skal du indtaste en formel for det beløb, som du vil beregne en procentdel for, efterfulgt af procenttegnet (%). Hvis kolonnenummer N f.eks. indeholder nettoændringen, indtastes **N %**.  
1. Gentag trin 4 til 7 for alle de grupper af rækker, du vil specificere efter procent.

## Brug finanskontokategorier til at ændre layoutet af regnskabet

Du kan bruge finanskontokategorier til at ændre layoutet af regnskabet. Når du f.eks. har oprettet kontokategorierne på siden **Finanskontokategorier**, kan du vælge handlingen **Generér finansielle rapporter** og opdatere de underliggende finansielle rapporter for de grundlæggende finansielle rapporter. Næste gang du kører en af disse rapporter, f.eks. rapporten **Saldoopgørelse**, tilføjes nye totaler og underordnede linjer.

En anden fordel ved at bruge finanskontokategorier frem for de rå finanskonti i rækkedefinitionerne er, at en ændring i kontoplanens struktur ikke påvirker dine økonomiske rapporter.

> [!NOTE]
> De øverste kontokategorier, f.eks. **Gæld**-noden, er faste, og du kan ikke tilføje dine egne. Du kan dog slette og tilføje kontokategorier på lavere niveauer og ændre strukturen for at definere, hvordan den finansielle rapport vises i rapporter.
>
> Du bør oprette og opbygge dine egne finanskontokategorier på lavere niveauer fra bunden i et hierarki, hvis det er nødvendigt, i stedet for at prøve at omarrangere de eksisterende. Du kan f.eks. omstrukturere noden **Gæld**, så den indeholder en ny **Egenkapital**-node efterfulgt af noderne **Aktuelle passiver** og **Langfristet gæld**. Få flere oplysninger under [Knytte finanskonti til kontokategorier](finance-general-ledger.md#account-categories).

## Brug af dimensioner i økonomiske rapporter

I finansielle analyser er en dimension data, som du kan føje til en post som en slags markør. Disse data bruges til at gruppere poster med ens karakteristika, f.eks. debitorer, regioner, produkter og sælger, og disse grupper kan nemt hentes frem til analyse. Du kan bruge dimensioner til poster i kladder, dokumenter og budgetter.

Hver dimension beskriver analysens fokus. En todimensional analyse kan f.eks. være pr. område. Hvis du bruger mere end to dimensioner, når du opretter en post, kan du udføre en mere kompleks analyse. Et eksempel på en kompleks analyse er at undersøge salg pr. salgskampagne pr. kundegruppe pr. område. Så får du større indsigt i din forretning, så du kan evaluere oplysningerne, f.eks. om hvor godt din forretning kører, hvor den blomster og hvor det ikke gør det, og hvor der bør allokeres flere ressourcer. Denne indsigt hjælper dig med at træffe mere informerede forretningsbeslutninger. Flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

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

## Sammenligne regnskabsperioder ved hjælp af periodeformler

Din finansielle rapport kan sammenligne resultaterne af forskellige regnskabsperioder, f.eks. sidste måned sammenlignet med samme måned sidste år. Hvis du vil gøre det, skal du åbne siden **Kolonnedefinition** og tilpasse den ved at tilføje feltet **Sammenligningsperiodeformel** som en kolonne. Flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md). Du kan derefter angive det pågældende felt til en periodeformel.  

En regnskabsperiode behøver ikke at følge kalenderen. En regnskabsperiode skal ikke følge kalenderåret, men hvert regnskabsår skal have det samme antal regnskabsperioder, selvom hver periode kan variere i længde.  

[!INCLUDE[prod_short](includes/prod_short.md)] bruger periodeformlen til at beregne varigheden af sammenligningsperioden i relation til den periode, som er defineret af datofiltret i rapportanmodningen. Sammenligningsperioden er baseret på perioden fra startdatoen i datofilteret. Periodeangivelserne forkortes på følgende måde:

| Forkortelse | Beskrivelse                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode.                                                                                |
| FP           | Forrige periode i et regnskabsår, halvår eller kvartal.                                   |
| CP           | Nuværende periode i et regnskabsår, halvår eller kvartal. Brug CP i formler til at angive den periode, der starter eller afslutter formlen. F.eks. angiver RÅ \[1.NP\] tiden fra begyndelsen af det aktuelle regnskabsår til den aktuelle periode.|
| RÅ           | Regnskabsår. RÅ\[1..3\] betegner f.eks. det første kvartal i det indeværende regnskabsår. |

Eksempler på formler:

| Formel         | Beskrivelse                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Aktuel periode.                                                                                  |
| \-1P            | Forrige periode.                                                                                 |
| \-1RÅ\[1..FP\]  | Hele forrige regnskabsår.                                                                     |
| \-1RÅ           | Den aktuelle periode i forrige regnskabsår.                                                          |
| \-1RÅ\[1..3\]   | Først kvartal i forrige regnskabsår.                                                           |
| \-1RÅ\[1..NP\]  | Fra starten af forrige regnskabsår til den nuværende periode i forrige regnskabsår, begge perioder inklusive. |
| \-1RÅ\[NP..FP\] | Fra den nuværende periode i forrige regnskabsår til sidste periode i forrige regnskabsår, begge perioder inklusive.   |

Hvis du vil foretage beregninger efter almindelige tidsperioder, skal du angive en formel i feltet **Sammenligningsdatoformel** i stedet. Hvis feltet f.eks. er indstillet til -1Å, sammenligner [!INCLUDE [prod_short](includes/prod_short.md)] med samme periode ét år tidligere.

> [!NOTE]
> Det er ikke altid gennemskueligt, hvilke perioder der sammenlignes, fordi du kan indstille et datofilter i en rapport, der dækker andre datoer end de regnskabsperioder, der afspejles i kontoplanen. Hvis du f.eks. vil oprette en finansiel rapport, hvor du vil sammenligne denne periode med samme periode sidste år, skal du indstille feltet **Sammenligningsdatoformel** til *-1RÅ*. Derefter skal du køre rapporten den 28. februar og indstille datofilteret til januar og februar. Den finansielle rapport sammenligner nu januar og februar i indeværende år med januar sidste år, som er den eneste afsluttede regnskabsperiode af de to for sidste år.  

Du kan finde flere oplysninger i [Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md).

## Udskrive og gemme finansielle rapporter

Du kan udskrive finansielle rapporter ved at bruge enhedens udskrivningsservice. [!INCLUDE[prod_short](includes/prod_short.md)] giver også mulighed for at gemme rapporter som Excel-projektmapper, Word-dokumenter, PDF-filer og XML-filer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
1. På siden **Finansielle rapporter** skal du vælge den rapport, du vil udskrive, og vælge **Udskriv**.
1. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Vælg den enhed, som rapporten skal sendes til, i feltet **Printer**.
    1. Indstillingen **(Håndteres af browseren)** angiver, at der ikke er en udvalgt printer til rapporten. I dette tilfælde vil browseren håndtere udskriften og vise en standardoplevelse, hvor du kan vælge en lokal printer, der er tilsluttet enheden. **(Håndteres af browseren)** er ikke tilgængelig i mobilappen [!INCLUDE[prod_short](includes/prod_short.md)] eller appen til Teams.
1. Vælg handlingen **Udskriv**.

### Planlægge en finansiel rapport eller gemme som et PDF-, Word-eller Excel-dokument

En finansiel rapport kan gemmes som en fil i forskellige formater, f. eks. PDF, XML, Word eller Excel. Du kan også konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til at oprette gentagne finansielle rapporter:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
1. På siden **Finansielle rapporter** skal du vælge handlingen **Udskriv**.
1. Angiv rapporten tilsvarende, og vælg derefter handlingen **Send til**.
1. Vælg filformatet eller handlingen **Planlægning**, og vælg **OK**.
1. Udfyld felterne for at oprette en planlagt eller tilbagevendende finansiel rapport. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>For tilbagevendende finansielle rapporter skal du angive felterne **Tidligste startdato/-klokkeslæt** og **Udløbsdato/-klokkeslæt** med den første og sidste dato for at oprette den finansielle rapport. Du kan også vælge, hvilke dage rapporten oprettes, ved at angive feltet **Datoformel for næste kørsel** efter det format, der er forklaret i sektionen [Bruge datoformler](ui-enter-date-ranges.md#use-date-formulas).

## Importere eller eksportere finansielle rapportdefinitioner

Du kan importere og eksportere finansielle rapport-/rækkedefinitioner som RapidStart-konfigurationspakker, som kan være nyttige, når du vil dele oplysninger med andre virksomheder. Pakken oprettes i en .rapidstart-fil, som komprimerer indholdet.

> [!NOTE]
> Når du importerer finansielle rapport-/rækkedefinitioner, erstattes eksisterende poster med samme navn som dem, der importeres, med nye definitioner. Bemærk, at konfigurationspakken til en rapportdefinition ikke overskriver eksisterende række- eller kolonnedefinitioner, der bruges i rapportdefinitionen.

Følg disse trin for at importere eller eksportere definitioner af økonomiske rapporter:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
1. Vælg den finansielle rapport, og vælg derefter **Indlæs finansiel rapport** eller **Udlæs finansiel rapport**, afhængigt af hvad du vil gøre.

Følg disse trin for at importere eller eksportere rækkedefinitioner af økonomiske rapporter:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Rækkedefinitioner** og vælg derefter det relaterede link.
1. Vælg rækkedefinitionen, og vælg derefter **Importer rækkedefinition** eller **Eksporter rækkedefinition**, afhængigt af hvad du vil gøre.

## Se også

[Køre og udskrive rapporter](ui-work-report.md)  
[Økonomisk Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
