---
title: Opbygge finansrapporter med finansdata og kontokategorier
description: Beskriver, hvordan du kan bruge finansrapporter til at oprette forskellige visninger og rapporter til analyse af data for finansiel ydeevne.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI, account schedule, financial report
ms.search.form: 103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766
ms.date: 08/12/2022
ms.author: edupont
ms.openlocfilehash: 3b71bec5ca7f1c903913b4244eb176dbf1c53c86
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605241"
---
# <a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a>Forberede Financial Reporting med finansdata og kontokategorier

Du kan bruge finansrapporter til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan. Finansrapporter analyserer tal i finanskonti og sammenligner finansposter med budgetposter. Resultaterne vises i diagrammer og rapporter på rollecenteret, f.eks. likviditetsdiagrammet og resultatopgørelsen og balancerapporterne.

Du kan få adgang til disse to rapporter, f.eks. med handlingen **Regnskabsopgørelser** i rollecentrene Virksomhedsleder og Bogholder.  

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder eksempler på finansrapporter, som du kan bruge med det samme. Du kan også oprette dine egne rækker og kolonner for at angive de tal, der skal sammenlignes. Du kan f.eks. oprette finansrapporter for at beregne avancer med dimensioner som afdelinger eller debitorgrupper. Du kan oprette det antal tilpassede kontoudtog, som du har behov for.  

Oprettelse af finansrapporter kræver en forståelse af de finansielle data i kontoplanen. Du kan f.eks. få vist finansposter som procenter af budgetposter, men det kræver, at du har oprettet budgetter. Flere oplysninger i [Oprette finansbudgetter](finance-how-create-budgets.md).

## <a name="financial-reports"></a>Finansielle rapporter

Finansielle rapporter arrangerer konti fra din kontoplan på en måde, der gør det nemmere at præsentere data. Du kan oprette forskellige layout for at definere de oplysninger, du vil uddrage af kontoplanen. Finansielle rapporter udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti. Du kan f. eks. oprette subtotaler for grupper af konti og derefter medtage denne total i andre totaler. Et andet eksempel er at beregne avancer på dimensioner som afdelinger eller debitorgrupper. Desuden kan finansposter og budgetposter filtreres, f.eks. efter nettobevægelse eller debitbeløb.

Du kan også sammenligne to eller flere finansielle rapporter og kolonnedefinitioner ved hjælp af formler, som giver mulighed for følgende handlinger:

* Oprette tilpassede finansrapporter.
* Oprette lige så mange finansielle rapporter, der er brug for, hver med et entydigt navn.
* Oprette forskellige rapportlayout og udskrive rapporterne med de aktuelle tal.

## <a name="gl-account-categories"></a>Finanskontokategorier

Du kan bruge finanskontokategorier til at ændre layoutet af regnskabet. Når du f.eks. har oprettet kontokategorierne på siden **Finanskontokategorier**, kan du vælge handlingen **Generér finansielle rapporter** og opdatere de underliggende finansielle rapporter for de grundlæggende finansielle rapporter. Næste gang du kører en af disse rapporter, f.eks. rapporten **Saldoopgørelse**, tilføjes nye totaler og underordnede linjer.

> [!NOTE]
> De øverste kontokategorier, f.eks. **Gæld**-noden, er faste, og du kan ikke tilføje dine egne. Du kan dog slette og tilføje kontokategorier på lavere niveauer og ændre strukturen for at definere, hvordan den finansielle rapport vises i rapporter.
>
> Du bør oprette og opbygge dine egne finanskontokategorier på lavere niveauer fra bunden i et hierarki, hvis det er nødvendigt, i stedet for at prøve at omarrangere de eksisterende. Du kan f.eks. omstrukturere noden **Gæld**, så den indeholder en ny **Egenkapital**-node efterfulgt af noderne **Aktuelle passiver** og **Langfristet gæld**.

## <a name="create-a-new-financial-report"></a>Oprette en ny finansiel rapport

Du bruger finansielle rapporter til at analysere finanskonti eller sammenligne finansposter med budgetposter. Du kan f.eks. få vist finansposter som procenter af budgetposter.

De finansielle rapporter i standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] passer muligvis ikke til dine forretningsbehov. Du kan starte med at kopiere en eksisterende finansiel rapport for hurtigt at oprette dine egne rapporter som beskrevet i trin 3 nedenfor.

> [!TIP]
> Når du har oprettet en finansiel rapport, kan du bruge siden **Finansiel rapport** til at se og validere den netop definerede finansielle rapport. Vælg handlingen **Rediger finansiel rapport** for at åbne siden.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.  
2. På siden **Finansielle rapporter** skal du vælge **Ny** for at oprette et nyt navn til den finansielle rapport.
3. Hvis du vil genbruge indstillinger fra en eksisterende finansiel rapport, kan du også vælge handlingen **Kopiér finansiel rapport**.
4. Udfyld felterne efter behov. Vælg en eksisterende definition i feltet **Kolonnedefinition**, som du senere kan redigere, hvis du vil.

    Kolonnedefinitioner angiver de parametre, som de finansielle data i rækkerne vises efter. F.eks. kan en kolonnedefinition indeholde fire kolonner, hvor du kan sammenligne bevægelse og saldo for den samme periode dette år og sidste år. Få mere at vide i afsnittet [Redigere en kolonnedefinition](bi-how-work-account-schedule.md#edit-a-column-definition).

5. Vælg handlingen **Rediger rækkedefinition**.
6. Vælg handlingerne **Indsæt finanskonti**, **Indsæt CF-konti** og **Indsæt omkostningstype** for at oprette en række for hvert økonomiske element, du vil analysere. Du kan f. eks. have én række til det aktuelle anlægsaktiv og en anden række til anlægsaktiver. Du kan finde inspiration i finansrapporterne i CRONUS-demoregnskabet.

    > [!NOTE]
    > **Rækkenummer** feltet viser de første 10 tegn i et id, f.eks. et kontonummer. Hvis du tilføjer elementer med id'er, der starter med de samme 10 tegn, vil du have dubletter i feltet **Rækkenr.** . Hvis det er nødvendigt, kan du redigere id'er manuelt, efter at du har indsat elementerne. De fulde id'er vises i feltet **Sammentælling**.

7. På siden **Finansielle rapporter** skal du vælge handlingen **Rediger finansiel rapport** for at se den resulterende finansielle rapport.
8. På siden **Finansiel rapport** skal du i feltet **Kolonnedefinition** vælge en anden kolonnedefinition for at undersøge regnskaber efter andre parametre.
9. Vælg **OK**.

Du har nu angivet grundlaget for en finansiel rapport, rækkerne med finansielle data, der skal vises, og et eksisterende kolonneformat, der viser dataene i rækkerne ud fra egne parametre. Hvis den standardkolonnedefinition, du har valgt i trin 4, ikke er egnet til dit formål, skal du følge fremgangsmåden nedenfor.

### <a name="edit-a-column-definition"></a>Redigere en kolonnedefinition

Du kan bruge kolonnedefinitioner til at angive, hvilke kolonner der skal med i den rapport, der oprettes. Du kan f.eks. udforme et format til sammenligning af bevægelse og saldo til dato for den samme periode dette år og sidste år. Du kan bruge op til 15 kolonner, som f.eks. kan være nyttige til visning af budgetter for 12 måneder med en kolonne, der viser totalen.

> [!NOTE]
> En udskrevet/vist/gemt version af en finansiel rapport viser højst fem kolonner. Hvis en finansiel rapport kun er beregnet til analyse på siden **Finansiel rapport**, kan du derimod oprette så mange kolonner, du vil.

1. På siden **Finansielle rapporter** skal du vælge den relevante finansielle rapport, du har oprettet, og vælge **Rediger kolonnedefinition**.
2. På siden **Kolonnedefinition** skal du oprette en række til hver kolonne med finansielle data, der vises efter i finansrapporten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vælg **OK**.
4. Åbn siden **Finansiel rapport** fra tid til anden for at kontrollere, at den nye kolonnedefinition fungerer korrekt.

> [!NOTE]
> De kolonner, som du definerer i hver række, repræsenterer kolonne 3 og opad på siden **Finansiel rapport**. De to første kolonner **Rækkenr.** og **Beskrivelse** er faste.  

### <a name="create-a-column-that-calculates-percentages"></a>Oprette en kolonne, hvor procenten beregnes

Du vil muligvis gerne medtage en kolonne i en finansiel rapport for at beregne procenter af et totalbeløb. Hvis du f.eks. har et antal rækker, som specificerer salg efter dimension, kan du have en kolonne, som angiver procenten af det samlede salg i hver række.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
2. Vælg en finansiel rapport på siden **Finansielle rapporter**.  
3. Vælg handlingen **Rediger finansiel rapport** for at konfigurere en finansiel rapportrække til beregning af den total, som procentdelene baseres på.  
4. Indsæt en linje lige over den første række, som du vil vise en procent for.  
5. Udfyld felterne på linjen på følgende måde: I feltet **Sammentællingstype** skal du angive **Angiv grundlag for procent**. I feltet **Sammentælling** skal du indtaste en formel for den total, som procentdelen skal baseres på. Hvis række 11 f.eks. indeholder det samlede salg, indtastes **11**.  
6. Vælg handlingen **Rediger kolonnedefinition** for at oprette en kolonne.  
7. Udfyld felterne på linjen på følgende måde: I feltet **Kolonnetype** skal du vælge **Formel**. I feltet **Formel** skal du indtaste en formel for det beløb, som du vil beregne en procentdel for, efterfulgt af procenttegnet (%). Hvis kolonnenummer N f.eks. indeholder nettoændringen, indtastes **N %**.  
8. Gentag trin 4 til 7 for alle de grupper af rækker, du vil specificere efter procent.

## <a name="set-up-financial-reports-with-overviews"></a>Oprette finansielle rapporter med oversigter

Du kan bruge en financiel rapport til at oprette en opgørelse, hvor tallene i finansposter sammenlignes med tallene i finansbudgettet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
2. Vælg en finansiel rapport på siden **Finansielle rapporter**.  
3. Vælg handlingen **Rediger rækkedefinition**  
4. På siden **Rækkedefinition** skal du vælge standardnavnet til den finansielle rapport i feltet **Navn**.
5. Vælg handlingen **Indsæt finanskonti**.  
6. Vælg de konti, du vil medtage i udtoget, og vælg **OK**.

    Kontiene indsættes nu i din finansielle rapport. Hvis du vil, kan du også ændre kolonnedefinitionen.  
7. Vælg handlingen **Rediger finansiel rapport**.  
8. På siden **Finansiel rapport** i oversigtspanelet **Dimensioner** skal du indstille budgetfilteret til det ønskede filternavn.  
9. Vælg **OK**.  

Du kan nu kopiere og indsætte budgetoversigten i et regneark..  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Sammenligne regnskabsperioder ved hjælp af periodeformler

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

## <a name="print-and-save-financial-reports"></a>Udskrive og gemme finansielle rapporter

Du kan udskrive finansielle rapporter ved at bruge enhedens udskrivningsservice. [!INCLUDE[prod_short](includes/prod_short.md)] giver også mulighed for at gemme rapporter som Microsoft Excel-projektmapper, Microsoft Word-dokumenter, PDF-filer og XML-filer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
2. På siden **Finansielle rapporter** skal du vælge den rapport, du vil udskrive, og vælge **Udskriv**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg den enhed, som rapporten skal sendes til, i feltet **Printer**.
    1. Indstillingen **(Håndteres af browseren)** angiver, at der ikke er en udvalgt printer til rapporten. I dette tilfælde vil browseren håndtere udskriften og vise en standardoplevelse, hvor du kan vælge en lokal printer, der er tilsluttet enheden. **(Håndteres af browseren)** er ikke tilgængelig i mobilappen [!INCLUDE[prod_short](includes/prod_short.md)] eller appen til Microsoft Teams.
5. Vælg handlingen **Udskriv**.

### <a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a>Planlægge en finansiel rapport eller gemme som et PDF-, Word-eller Excel-dokument

En finansiel rapport kan gemmes som en fil i forskellige formater, f. eks. PDF, XML, Word eller Excel. Du kan også konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til at oprette gentagne finansielle rapporter:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
2. På siden **Finansielle rapporter** skal du vælge handlingen **Udskriv**.
3. Angiv rapporten tilsvarende, og vælg derefter handlingen **Send til**.
4. Vælg filformatet eller handlingen **Planlægning**, og vælg **OK**.
5. Udfyld felterne for at oprette en planlagt eller tilbagevendende finansiel rapport. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
   * For tilbagevendende finansielle rapporter skal du angive felterne **Tidligste startdato/-klokkeslæt** og **Udløbsdato/-klokkeslæt** med den første og sidste dato for at oprette den finansielle rapport. Du kan også vælge, hvilke dage rapporten oprettes, ved at angive feltet **Datoformel for næste kørsel** efter det format, der er forklaret i sektionen [Bruge datoformler](ui-enter-date-ranges.md#use-date-formulas).

## <a name="importing-or-exporting-financial-reports"></a>Importere eller eksportere finansielle rapporter

Du kan importere og eksportere finansielle rapporter som RapidStart-konfigurationspakker, som kan være nyttige, når du vil dele oplysninger med andre virksomheder. Pakken oprettes i en .rapidstart-fil, som komprimerer indholdet.

### <a name="import-and-export-financial-reports"></a>Importere og eksportere finansielle rapporter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.
2. Vælg den finansielle rapport, og vælg derefter **Indlæs finansiel rapport** eller **Udlæs finansiel rapport**, afhængigt af hvad du vil gøre.

> [!NOTE]
> Når du importerer en finansiel rapport, slettes eksisterende poster med samme navn som dem, der importeres.

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/configure-financial-reports-dynamics-365-business-central/index).

## <a name="see-also"></a>Se også

[Køre og udskrive rapporter](ui-work-report.md)  
[Financial Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
