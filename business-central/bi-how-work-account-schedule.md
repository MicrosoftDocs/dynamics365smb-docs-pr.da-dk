---
title: Oprette finansrapporter ved hjælp af kontoskemaer
description: Beskriver, hvordan du kan bruge kontoskemaer til at oprette forskellige visninger og rapporter til analyse af data for finansiel ydeevne.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 103, 104, 197, 196, 195, 198, 490, 764, 765, 766
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8984d007f2082c6a21a3d2226a20f2ad585b131a
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129728"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Forberede Financial Reporting med kontoskemaer og kontokategorier

Du kan bruge kontoskemaer til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan. Kontoskemaer analyserer tal i finanskonti og sammenligner finansposter med finansbudgetposter. Resultaterne vises i diagrammer og rapporter på rollecenteret, f.eks. tabellen Likviditet og resultatopgørelsen og balancerapporterne.

Du kan få adgang til disse to rapporter, f.eks. med handlingen **Regnskabsopgørelser** i rollecentrene Virksomhedsleder og Bogholder.  

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder eksempler på kontoskemaer, som du kan bruge med det samme. Du kan også oprette dine egne rækker og kolonner for at angive de tal, der skal sammenlignes. Brugere kan f.eks. oprette kontoskemaer for at beregne avancer på dimensioner som afdelinger eller debitorgrupper. Du kan oprette det antal tilpassede kontoudtog, som du har behov for.  

Oprettelse af kontoskemaer kræver en forståelse af de finansielle data i kontoplanen. Du kan f.eks. få vist finansposter som procenter af budgetposter, men det kræver, at du har oprettet budgetter. Du kan finde flere oplysninger i [Oprette finansbudgetter](finance-how-create-budgets.md).

## <a name="account-schedules"></a>Kontoskemaer

Kontoskemaer arrangerer konti fra din kontoplan på en måde, der gør det nemt at præsentere data. Du kan oprette forskellige layout for at definere de oplysninger, du vil uddrage af kontoplanen. Kontoskemaer udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti. Du kan f. eks. oprette subtotaler for grupper af konti og derefter medtage denne total i andre totaler. Et andet eksempel er at beregne avancer på dimensioner som afdelinger eller debitorgrupper. Desuden kan finansposter og finansbudgetposter filtreres, f.eks. efter bevægelse eller debitbeløb.

Du kan også sammenligne to eller flere kontoskemaer og kolonnelayout ved hjælp af formler, som giver mulighed for følgende handlinger:

* Oprette tilpassede finansrapporter.
* Oprette så mange skemaer, der er brug for, hvert med et entydigt navn.
* Oprette forskellige rapportlayout og udskrive rapporterne med de aktuelle tal.

## <a name="gl-account-categories"></a>Finanskontokategorier

Du kan bruge finanskontokategorier til at ændre layoutet af regnskabet. Når du har oprettet kontokategorierne på siden **Finanskontokategorier**, og du vælger handlingen **Opret kontoskemaer** opdateres de underliggende kontoskemaer for de grundlæggende regnskabsrapporter. Næste gang du kører en af disse rapporter, f.eks. rapporten **Saldoopgørelse**, tilføjes nye totaler og underordnede linjer, baseret på dine ændringer.

> [!NOTE]
> De øverste kontokategorier, f.eks. **Gæld**-noden, er faste, og du kan ikke tilføje dine egne. Du kan dog slette og tilføje kontokategorier på lavere niveauer og ændre strukturen for at definere, hvordan det relaterede kontoskema vises i rapporter.
>
> Det anbefales, at du opretter og opbygger dine egne finanskontokategorier på lavere niveauer fra bunden i et hierarki, hvis det er nødvendigt, i stedet for at prøve at omarrangere de eksisterende. Du kan f.eks. omstrukturere noden **Gæld**, så den indeholder en ny **Egenkapital**-node efterfulgt af noderne **Aktuelle passiver** og **Langfristet gæld**.

## <a name="to-create-a-new-account-schedule"></a>Sådan oprettes et nyt kontoskema

Du bruger kontoskemaer til at analysere tal i finanskonti eller til at sammenligne finansposter med finansbudgetposter. Du kan f.eks. få vist finansposter som procenter af budgetposter.

Kontoskemaerne i standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] er grundlaget for de økonomiske standardrapporter, som muligvis ikke er egnet til din virksomheds behov. Du kan starte ved at kopiere et eksisterende kontoskema for hurtigt at oprette din egne regnskabsrapporter som beskrevet i trin 3.

> [!TIP]
> Når du har oprettet et kontoskema, kan du bruge siden **Kontoskemaoversigt** til at få vist og validere den finansrapport, kontoskemaet definerer. Vælg handlingen **Oversigt** for at åbne siden.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoskemaer**, og vælg derefter det relaterede link.  
2. På siden **Kontoskemaer** skal du vælge handlingen **Ny** for at oprette et nyt kontoskemanavn.
3. Hvis du vil genbruge indstillinger fra et eksisterende Kontoskema, kan du også vælge handlingen **Kopier kontoskema**.
4. Udfyld felterne efter behov. I feltet **Standard kolonneformat** skal du vælge et eksisterende layout. Du kan redigere det senere, hvis der er behov for det.

    Kolonneformater definerer kolonner for forskellige parametre, som de finansielle data i rækkerne vises efter. Du kan f.eks. udforme et kolonneformat med fire kolonner, hvor du kan sammenligne bevægelse og saldo for den samme periode dette år og sidste år. Du kan finde flere oplysninger i [Sådan oprettes et kolonneformat](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Vælg handlingen **Rediger kontoskema**.
6. Afhængigt af hvad du vil analysere, skal du vælge **Indsæt finanskonti**, **Indsæt CF-konti** og **Indsæt omkostningstype**-handlinger for at oprette en række for hvert økonomisk element. Du kan f. eks. have én række til det aktuelle anlægsaktiv og en anden række til anlægsaktiver. Du kan finde inspiration i eksisterende kontoskemaer i CRONUS-demoregnskabet.

    > [!NOTE]
    > **Rækkenummer** feltet indeholder de første 10 tegn i et id, f. eks. et kontonummer. Hvis du tilføjer elementer med id'er, der starter med de samme 10 tegn, vil du have dubletter i feltet **Rækkenr.** . Hvis det er nødvendigt, kan du redigere identfiers manuelt, efter at du har indsat elementerne. De fulde id'er vises i feltet **Sammentælling**.

7. Vælg handlingen **Oversigt** for at få vist den oprettede finansrapport.
8. På siden **Kontoskemaoversigt** i feltet **Kolonneformatnavn** skal du vælge et andet kolonneformat for at kunne se regnskaber efter andre parametre.
9. Vælg knappen **OK**.

Du har nu angivet grundlaget for kontoskemaet, rækkerne med finansielle data, der skal vises, og et eksisterende kolonneformat, der viser dataene i rækkerne ud fra forskellige parametre. Hvis det standardkolonneformat, du har valgt i trin 4, ikke er egnet til dit formål, skal du følge fremgangsmåden nedenfor.

### <a name="to-edit-a-column-layout"></a>Sådan redigeres et kolonneformat

Du kan bruge kolonneformater til at angive, hvilke kolonner der skal med i den rapport, der oprettes. Du kan f.eks. udforme et format til sammenligning af bevægelse og saldo til dato for den samme periode dette år og sidste år. Du kan bruge op til 15 kolonner, som f. eks. kan være nyttige til visning af budgetter på 12 måneder med en kolonne, der viser totalen.

> [!NOTE]
> En udskrevet/vist/gemt version af et kontoskema kan vise højst fem kolonner. Hvis kontoskemaet kun er beregnet til analyse på siden **Kontoskemaoversigt**, kan du oprette så mange kolonner, du vil.

1. På siden **Kontoskemaer** skal du vælge det relevante kontoskema og derefter vælge handlingen **Rediger opsætning af kolonneformat**.
2. På siden **Kolonneformater** skal du oprette en række til hver kolonne, som finansielle data vises efter i finansrapporten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vælg knappen **OK**.
4. Åbn siden **Kontoskemaoversigt** fra tid til anden for at kontrollere, at det nye kolonneformat fungerer korrekt.

> [!NOTE]
> De kolonner, som du definerer i hver række, repræsenterer kolonner 3 og op efter på siden **Kontoskemaoversigt**. De to første kolonner **Rækkenr.** og **Beskrivelse** er faste.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Sådan oprettes en kolonne, hvor procenten beregnes

Du vil muligvis gerne medtage en kolonne i et kontoskema for at beregne procenter af et totalbeløb. Hvis du f.eks. har et antal rækker, som specificerer salg efter dimension, kan du have en kolonne, som angiver procenten af det samlede salg i hver række.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoskemaer**, og vælg derefter det relaterede link.
2. Vælg et kontoskema på siden **Kontoskemanavne**.  
3. Vælg handlingen **Rediger kontoskema** for at konfigurere en kontoskemarække til beregning af den total, som procentdelene baseres på.  
4. Indsæt en linje lige over den første række, som du vil vise en procent for.  
5. Udfyld felterne på linjen på følgende måde: I feltet **Sammentællingstype** skal du angive **Angiv grundlag for procent**. I feltet **Sammentælling** skal du indtaste en formel for den total, som procentdelen skal baseres på. Hvis række 11 f.eks. indeholder det samlede salg, indtastes **11**.  
6. Vælg handlingen **Rediger opsætning af kolonneformat** for at oprette en kolonne.  
7. Udfyld felterne på linjen på følgende måde: I feltet **Kolonnetype** skal du vælge **Formel**. I feltet **Formel** skal du indtaste en formel for det beløb, som du vil beregne en procentdel for, efterfulgt af %. Hvis kolonnenummer N f.eks. indeholder bevægelsen, indtastes **N %**.  
8. Gentag trin 4 til 7 for alle de grupper af rækker, du vil specificere efter procent.

## <a name="to-set-up-account-schedules-with-overviews"></a>Sådan oprettes kontoskemaer med oversigter

Du kan bruge et kontoskema til at oprette en opgørelse, hvor tallene i finansposter sammenlignes med tallene i finansbudgettet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoskemaer**, og vælg derefter det relaterede link.
2. Vælg et kontoskema på siden **Kontoskemanavne**.  
3. Vælg handlingen **Rediger kontoskema**  
4. På siden **Kontoskema** skal du vælge standardkontoskemanavnet i feltet **Navn**.
5. Vælg handlingen **Indsæt finanskonti**.  
6. Marker de konti, som du ønsker at medtage i opgørelsen, og vælg derefter knappen **OK**.

    Kontiene indsættes i kontoskemaet. Hvis du vil, kan du også ændre kolonneformatet.  
7. Vælg handlingen **Oversigt**.  
8. På siden **Kontoskemaoversigt** i oversigtspanelet **Dimensionsfiltre** skal du indstille budgetfilteret til det ønskede filternavn.  
9. Vælg knappen **OK**.  

Du kan nu kopiere og indsætte budgetoversigten i et regneark..  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Sammenligne regnskabsperioder ved hjælp af periodeformler

Kontoskemaet kan sammenligne resultaterne af forskellige regnskabsperioder, f.eks. denne måned sammenlignet med samme måned sidste år. Hvis du vil gøre det, skal du åbne siden **Kolonnelayout** og tilpasse den ved at tilføje feltet **Sammenligningsperiodeformel** som en kolonne. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md). Du kan derefter angive det pågældende felt til en periodeformel.  

En regnskabsperiode behøver ikke at stemme overens med kalenderen. En regnskabsperiode skal ikke følge kalenderåret, men hvert regnskabsår skal have det samme antal regnskabsperioder, selvom hver periode kan variere i længde.  

[!INCLUDE[prod_short](includes/prod_short.md)] bruger periodeformlen til at beregne beløbet fra sammenligningsperioden i relation til den periode, som er defineret af datofiltret i rapportanmodningen. Sammenligningsperioden er baseret på perioden fra startdatoen i datofilteret. Periodeangivelserne forkortes på følgende måde:

| Forkortelse | Description                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode                                                                                |
| FP           | Forrige periode i et regnskabsår, halvår eller kvartal.                                   |
| NP           | Nuværende periode i et regnskabsår, halvår eller kvartal. Brug CP i formler til at angive den periode, der starter eller afslutter formlen. F.eks. angiver RÅ \[1.NP\] tiden fra begyndelsen af det aktuelle regnskabsår til den aktuelle periode.|
| RÅ           | Regnskabsår. RÅ\[1..3\] betegner f.eks. det første kvartal i det indeværende regnskabsår |

Eksempler på formler:

| Formel         | Description                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Nuværende periode                                                                                  |
| \-1P            | Forrige periode                                                                                 |
| \-1RÅ\[1..FP\]  | Hele forrige regnskabsår                                                                     |
| \-1RÅ           | Den aktuelle periode i forrige regnskabsår                                                          |
| \-1RÅ\[1..3\]   | Først kvartal i forrige regnskabsår                                                           |
| \-1RÅ\[1..NP\]  | Fra starten af forrige regnskabsår til den nuværende periode i forrige regnskabsår, begge perioder inklusive |
| \-1RÅ\[NP..FP\] | Fra den nuværende periode i forrige regnskabsår til sidste periode i forrige regnskabsår, begge perioder inklusive   |

Hvis du vil foretage beregninger efter almindelige tidsperioder, skal du angive en formel i feltet **Sammenligningsdatoformel** i stedet. Hvis feltet f.eks. er indstillet til -1Å, sammenligner [!INCLUDE [prod_short](includes/prod_short.md)] med samme periode 1 år tidligere.

> [!NOTE]
> Det er ikke altid gennemskueligt, hvilke perioder der sammenlignes, fordi du kan indstille et datofilter i en rapport, der dækker andre datoer end de regnskabsperioder, der afspejles i dataene i kontoplanen. Hvis du f.eks. vil oprette et kontoskema, hvor du vil sammenligne denne periode, hvor den samme periode sidste år, skal du indstille feltet **Sammenligningsdatoformel** til *-1RÅ*. Derefter skal du køre rapporten den 28. februar og indstille datofilteret til januar og februar. Kontoskemaet sammenligner nu januar og februar i indeværende år med januar sidste år, som er den eneste afsluttede regnskabsperiode af de to for sidste år.  

Du kan finde flere oplysninger om datoformler i [Arbejde med kalenderdatoer og-klokkeslæt](ui-enter-date-ranges.md).  

## <a name="import-or-export-account-schedules"></a>Importere eller eksportere kontoskemaer
Du kan importere og eksportere kontoskemaer som RapidStart-konfigurationspakker. Konfigurationspakker er f. eks. nyttige, når du vil dele dem med andre firmaer. Pakken oprettes i en .rapidstart-fil, som leverer pakkens indhold i komprimeret format.

### <a name="to-import-and-export-account-schedules"></a>Importere og eksportere kontoskemaer
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoskemaer**, og vælg derefter det relaterede link.
2. Vælg kontoskemaet, og vælg derefter **Importer kontoskema** eller **Eksporter kontoskema**, afhængigt af hvad du vil gøre. 

> [!NOTE]
> Når du importerer kontoskemaer, slettes eksisterende poster, der har samme navn, som de er ved at blive importeret.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]