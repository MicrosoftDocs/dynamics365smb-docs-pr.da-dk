---
title: Oprette finansrapporter ved hjælp af kontoskemaer
description: Beskriver, hvordan du kan bruge kontoskemaer til at oprette forskellige visninger og rapporter til analyse af data for finansiel ydeevne.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 02/12/2020
ms.author: edupont
ms.openlocfilehash: 21e83f37405c01d5df00e6b392ded3ce3996d0c2
ms.sourcegitcommit: c78df3aefb3e2ed8c28e5ac8340d56ab787212e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071954"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Forberede finansrapporter med kontoskemaer og kontokategorier
Du kan bruge kontoskemaer til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan. Kontoskemaer analyserer tal i finanskonti og sammenligner finansposter med finansbudgetposter. Resultaterne vises i diagrammer på rollecenteret, f.eks. tabellen Likviditet, og i rapporter, f.eks. resultatopgørelsen og balancerapporterne.

Du kan få adgang til disse to rapporter, f.eks. med handlingen **Regnskabsopgørelser** i rollecentrene Virksomhedsleder og Bogholder.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder et par eksempelkontoskemaer, som du kan bruge det samme, eller du kan konfigurere dine egen rækker og kolonner for at angive de tal, du vil sammenligne. Du kan f.eks. oprette kontoskemaer for at beregne avancer på dimensioner som afdelinger eller debitorgrupper. Du kan oprette så mange tilpassede kontoudtog, som du har behov for.  

Oprettelse af kontoskemaer kræver en forståelse af de finansielle data i kontoplanen. Du kan f.eks. få vist finansposter som procenter af budgetposterne. Dette kræver, at der er oprettet budgetter. Du kan finde flere oplysninger i [Oprette finansbudgetter](finance-how-create-budgets.md).

## <a name="account-schedules"></a>Kontoskemaer
Kontoskemaer bruges til at arrangere konti, der er angivet i kontoplanen, på en måde, der egner sig til præsentation af oplysninger om de pågældende konti. Du kan oprette forskellige layout for at definere de oplysninger, du vil uddrage af kontoplanen. En af de vigtigste funktioner ved kontoskemaer er at give plads til beregninger, der ikke kan foretages direkte i kontoplanen, f.eks. oprettelse af subtotaler for grupper af konti, som igen kan medtages i nye totaler og derefter kan bruges i andre totaler. Brugere kan f.eks. oprette kontoskemaer for at beregne avancer på dimensioner som afdelinger eller debitorgrupper. Desuden kan finansposter og finansbudgetposter filtreres, f.eks. efter bevægelse eller debitbeløb.

Du kan også sammenligne to eller flere kontoskemaer og kolonnelayout ved hjælp af formler. Med denne type sammenligning kan du:

* Oprette tilpassede finansrapporter.
* Oprette så mange skemaer, der er brug for, hvert med et entydigt navn.
* Oprette forskellige rapportlayout og udskrive rapporterne med de aktuelle tal.

## <a name="gl-account-categories"></a>Finanskontokategorier
Du kan bruge finanskontokategorier til at ændre layoutet af regnskabet. Når du har oprettet kontokategorierne på siden **Finanskontokategorier**, og du vælger handlingen **Opret kontoskemaer** opdateres de underliggende kontoskemaer for de grundlæggende regnskabsrapporter. Næste gang du kører en af disse rapporter, f.eks. rapporten **Saldoopgørelse**, tilføjes nye totaler og underordnede linjer, baseret på dine ændringer.

> [!NOTE]
> De øverste kontokategorier, f.eks. **Gæld**-noden, er faste, og du kan ikke tilføje dine egne. Du kan dog slette og tilføje kontokategorier på lavere niveauer og ændre strukturen for at definere, hvordan det relaterede kontoskema vises i rapporter.<br /><br />
> Det anbefales, at du opretter og opbygger dine egne finanskontokategorier på lavere niveauer fra bunden i et hierarki, hvis det er nødvendigt, i stedet for at prøve at omarrangere de eksisterende. Du kan f.eks. omstrukturere noden **Gæld**, så den indeholder en ny **Egenkapital**-node efterfulgt af noderne **Aktuelle passiver** og **Langfristet gæld**.

## <a name="to-create-a-new-account-schedule"></a>Sådan oprettes et nyt kontoskema  
Du bruger kontoskemaer til at analysere tal i finanskonti eller til at sammenligne finansposter med finansbudgetposter. Du kan f.eks. få vist finansposter som procenter af budgetposter.

Kontoskemaerne i standardversionen af [!INCLUDE[d365fin](includes/d365fin_md.md)] er grundlaget for de økonomiske standardrapporter, som muligvis ikke er egnet til din virksomheds behov. Du kan starte ved at kopiere et eksisterende kontoskema for hurtigt at oprette din egne regnskabsrapporter. Se trin 3 herunder.

Siden **Kontoskemaoversigt** er der, hvor du kan få vist den finansrapport, som kontoskemaet definerer. I det følgende er det vigtigt at forstå, at det, du definerer som kontoskemarækker og -kolonner, kun kan ses og godkendes på siden **Kontoskemaoversigt**, som du kan åbne fra et kontoskema ved at vælge handlingen **Oversigt**. Selve siden **Kontoskema** er kun et opsætningsområde.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.  
2. På siden **Kontoskemaer** skal du vælge handlingen **Ny** for at oprette et nyt kontoskemanavn.
3. Du kan også vælge handlingen **Kopiér kontoskema**, udfylde de to felter efter behov, og derefter vælge knappen **OK**.
4. Udfyld felterne efter behov. I feltet **Standard kolonneformat** skal du vælge et eksisterende layout. Du kan redigere det senere, hvis der er behov for det.

    Du kan bruge kolonneformater til at definere kolonner for forskellige parametre, som de finansielle data i rækkerne vises efter. Du kan f.eks. udforme et kolonneformat til sammenligning af bevægelse og saldo til dato for den samme periode dette år og sidste år med fire kolonner. Du kan finde flere oplysninger i [Sådan oprettes et kolonneformat](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Vælg handlingen **Rediger kontoskema**.
6. Opret en række for hvert finansielle element, der skal vises i rapporten, f.eks. en række til aktuelle aktiver og en anden række til anlægsaktiver. Du kan finde inspiration i eksisterende kontoskemaer i CRONUS-demoregnskabet.
7. Vælg handlingen **Oversigt** for at få vist den oprettede finansrapport.
8. På siden **Kontoskemaoversigt** i feltet **Kolonneformatnavn** skal du vælge et andet kolonneformat for at kunne se regnskaber efter andre parametre.
9. Vælg knappen **OK**.

Du har nu angivet grundlaget for kontoskemaet, rækkerne med finansielle data, der skal vises, og et eksisterende kolonneformat, der viser dataene i rækkerne ud fra forskellige parametre. Hvis det standardkolonneformat, du har valgt i trin 4, ikke er egnet til dit formål, skal du følge fremgangsmåden nedenfor.

### <a name="to-edit-a-column-layout"></a>Sådan redigeres et kolonneformat
Du kan bruge kolonneformater til at angive, hvilke kolonner der skal med i den rapport, der oprettes. Du kan f.eks. udforme et format til sammenligning af bevægelse og saldo til dato for den samme periode dette år og sidste år.

> [!NOTE]
> En udskrevet/vist/gemt version af et kontoskema kan vise højst fem kolonner. Hvis kontoskemaet kun er beregnet til analyse på siden **Kontoskemaoversigt**, kan du oprette så mange kolonner, du vil.

1. På siden **Kontoskemaer** skal du vælge det relevante kontoskema og derefter vælge handlingen **Rediger opsætning af kolonneformat**.
2. På siden **Kolonneformater** skal du oprette en række til hver kolonne, som finansielle data vises efter i finansrapporten. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vælg knappen **OK**.
4. Åbn siden **Kontoskemaoversigt** fra tid til anden for at kontrollere, at det nye kolonneformat fungerer korrekt.

> [!NOTE]
> De kolonner, som du definerer i hver række, repræsenterer kolonner 3 og op efter på siden **Kontoskemaoversigt**. De to første kolonner **Rækkenr.** og **Beskrivelse** er faste.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Sådan oprettes en kolonne, hvor procenten beregnes  
Du vil muligvis gerne medtage en kolonne i et kontoskema for at beregne procenter af et totalbeløb. Hvis du f.eks. har et antal rækker, som specificerer salg efter dimension, kan du have en kolonne, som angiver procenten af det samlede salg, som hver række repræsenterer.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.
2. Vælg et kontoskema på siden **Kontoskemanavne**.  
3. Vælg handlingen **Rediger kontoskema** for at konfigurere en kontoskemarække til beregning af den total, som procentdelene baseres på.  
4. Indsæt en linje lige over den første række, som du vil vise en procent for.  
5. Udfyld felterne på linjen på følgende måde: I feltet **Sammentællingstype** skal du angive **Angiv grundlag for procent**. I feltet **Sammentælling** skal du indtaste en formel for den total, som procentdelen skal baseres på. Hvis række 11 f.eks. indeholder det samlede salg, indtastes **11**.  
6. Vælg handlingen **Rediger opsætning af kolonneformat** for at oprette en kolonne.  
7. Udfyld felterne på linjen på følgende måde: I feltet **Kolonnetype** skal du vælge **Formel**. I feltet **Formel** skal du indtaste en formel for det beløb, som du vil beregne en procentdel for, efterfulgt af %. Hvis kolonnenummer N f.eks. indeholder bevægelsen, indtastes **N %**.  
8. Gentag trin 4 til 7 for alle de grupper af rækker, du vil specificere efter procent.

## <a name="to-set-up-account-schedules-with-overviews"></a>Sådan oprettes kontoskemaer med oversigter  
Du kan bruge et kontoskema til at oprette en opgørelse, hvor tallene i finansposter sammenlignes med tallene i finansbudgettet.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.
2. Vælg et kontoskema på siden **Kontoskemanavne**.  
3. Vælg handlingen **Rediger kontoskema**  
4. På siden **Kontoskema** skal du vælge standardkontoskemanavnet i feltet **Navn**.
5. Vælg handlingen **Indsæt konti**.  
6. Marker de konti, som du ønsker at medtage i opgørelsen, og vælg derefter knappen **OK**.

    Kontiene indsættes i kontoskemaet. Hvis du vil, kan du også ændre kolonneformatet.  
7. Vælg handlingen **Oversigt**.  
8. På siden **Kontoskemaoversigt** i oversigtspanelet **Dimensionsfiltre** skal du indstille budgetfilteret til det ønskede filternavn.  
9. Vælg knappen **OK**.  

Du kan nu kopiere og indsætte budgetoversigten i et regneark..  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Sammenligne regnskabsperioder ved hjælp af periodeformler
Kontoskemaet kan sammenligne resultaterne af forskellige regnskabsperioder, f.eks. denne måned sammenlignet med samme måned sidste år. For at gøre det skal du tilføje en kolonne i feltet **Sammenligningsperiodeformel** og derefter indstille dette felt til en periodeformel.  

En regnskabsperiode skal ikke følge kalenderåret, men hvert regnskabsår skal have det samme antal regnskabsperioder, selvom hver periode kan variere i længde.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] bruger periodeformlen til at beregne beløbet fra sammenligningsperioden i relation til den periode, som er defineret af datofiltret i rapportanmodningen. Sammenligningsperioden er baseret på perioden fra startdatoen i datofilteret. Periodeangivelserne forkortes på følgende måde:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Forkortelse</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>P</p></td>
<td><p>Periode</p></td>
</tr>
<tr class="even">
<td><p>FP</p></td>
<td><p>Forrige periode i et regnskabsår, halvår eller kvartal.</p></td>
</tr>
<tr class="odd">
<td><p>NP</p></td>
<td><p>Nuværende periode i et regnskabsår, halvår eller kvartal.</p></td>
</tr>
<tr class="even">
<td><p>RÅ</p></td>
<td><p>Regnskabsår. RÅ[1..3] betegner f.eks. det første kvartal i det indeværende regnskabsår.</p></td>
</tr>
</tbody>
</table>

Eksempler på formler:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Formel</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;Tomt&gt;</p></td>
<td><p>Nuværende periode</p></td>
</tr>
<tr class="even">
<td><p>-1P</p></td>
<td><p>Forrige periode</p></td>
</tr>
<tr class="odd">
<td><p>-1RÅ[1..FP]</p></td>
<td><p>Hele forrige regnskabsår</p></td>
</tr>
<tr class="even">
<td><p>-1RÅ</p></td>
<td><p>Den aktuelle periode i forrige regnskabsår</p></td>
</tr>
<tr class="odd">
<td><p>-1RÅ[1..3]</p></td>
<td><p>Først kvartal i forrige regnskabsår</p></td>
</tr>
<tr class="even">
<td><p>-1RÅ[1..NP]</p></td>
<td><p>Fra starten af forrige regnskabsår til den nuværende periode i forrige regnskabsår, begge inklusive</p></td>
</tr>
<tr class="odd">
<td><p>-1RÅ[NP..FP]</p></td>
<td><p>Fra den nuværende periode i det forrige regnskabsår til den sidste periode i det sidste regnskabsår, begge inklusive</p></td>
</tr>
</tbody>
</table>

Hvis du vil foretage beregninger efter almindelige tidsperioder, skal du angive en formel i feltet **Sammenligningsdatoformel** i stedet.

> [!NOTE]
> Det er ikke altid gennemskueligt, hvilke perioder der sammenlignes, fordi du kan indstille et datofilter i en rapport, der dækker andre datoer end de regnskabsperioder, der afspejles i dataene i kontoplanen. Hvis du f.eks. vil oprette et kontoskema, hvor du vil sammenligne denne periode, hvor den samme periode sidste år, skal du indstille feltet **Filter for sammenligningsdatoperiode** til *-1FY*. Derefter skal du køre rapporten den 28. februar og indstille datofilteret til januar og februar. Kontoskemaet sammenligner nu januar og februar i indeværende år med januar sidste år, som er den eneste afsluttede regnskabsperiode af de to for sidste år.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
