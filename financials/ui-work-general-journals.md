---
title: "Bruge finanskladder, der skal bogføres direkte til Finans | Microsoft Docs"
description: "Lær, hvordan du kan bruge finanskladder til at bogføre økonomisk transaktioner på finanskonti og andre konti, f.eks. bank- og kreditorkonti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b573bb55c29de329e5d9a804b49a91687dc369ff
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-general-journals"></a>Arbejde med finanskladder
De fleste finansposteringer bogføres i finansregnskabet ved hjælp af dedikerede forretningsdokumenter, f.eks. købsfakturaer og salgsordrer. Du kan oprette relaterede transaktioner for aktiviteter, der ikke er repræsenteret af et dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. mindre udgifter eller indbetalinger, ved at bogføre kladdelinjer i vinduet **Finanskladde**. Du kan finde flere oplysninger i [Fremgangsmåde: Bogføre transaktioner direkte i finansregnskabet](finance-how-post-transactions-directly.md).

For eksempel kan du bogføre medarbejdernes udgifter af egne penge på forretningsrelaterede udgifter for senere refusion. Du kan finde flere oplysninger i [Fremgangsmåde: Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md).

Du bruger finanskladder til at bogføre økonomiske transaktioner direkte på finanskonti og andre konti, f.eks. bank-, debitor-, kreditor- og medarbejderkonti. Når du bogfører via en finanskonto, oprettes der altid poster i finanskonti. Det gælder også, når du bogfører f.eks. en kladdelinje på en debitorkonto, fordi der bogføres en post på en finanskonto for tilgodehavende via en bogføringsgruppe.

De oplysninger, du angiver i en kladde, er midlertidige og kan ændres, mens de er i kladden. Når du bogfører kladden, overføres oplysningerne til poster på individuelle konti, hvor de ikke kan ændres. Du kan imidlertid annullere udligningen af bogførte poster, og du kan bogføre tilbageførsels- eller rettelsesposter. Du kan finde flere oplysninger i [Sådan tilbageføres poster](finance-how-reverse-journal-posting.md).

## <a name="using-journal-templates-and-batches"></a>Bruge kladdetyper og -navne
Der er forskellige finanskladdetyper. Hver kladdetype er repræsenteret af et dedikeret vindue med bestemte funktioner og de felter, der kræves for at understøtte disse funktioner, f.eks. vinduet **Betalingsudligningskladde** til behandling af bankbetalinger og vinduet **Udbetalingskladde** til betaling af kreditorer eller refusion af medarbejdere. Du kan finde flere oplysninger i [Foretage indbetalinger](payables-make-payments.md) og [Fremgangsmåde: Udligne debitorbetalinger manuelt](receivables-how-apply-sales-transactions-manually.md).

For hver kladdetype kan du angive din egen private kladde som kladdenavn. F.eks. kan du angive din egen kladdetype som udbetalingskladden med dit personlige layout og dine indstillinger. Følgende tip er et eksempel på, hvordan du kan tilpasse en kladde.

> [!TIP]  
> Hvis du markerer afkrydsningsfeltet **Foreslå modkontobeløb** på linjen for dit kladdenavn i vinduet **Finanskladdenavne**, udfyldes feltet **Beløb** på f.eks. finanskladdelinjer for samme bilagsnummer automatisk med den værdi, der er nødvendig for at afstemme dokumentet. Du kan finde flere oplysninger i [Lade [!INCLUDE[d365fin](includes/d365fin_md.md)] foreslå værdier](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Om hovedkonti og modkonti
Hvis du har oprettet modkonti for kladdenavnene, udfyldes modkontoen automatisk på siden **Finanskladder**, når du udfylder feltet **Kontonr.**. Hvis ikke, skal du udfylde både feltet **Kontonr.** og feltet **Modkontonr.** manuelt. Et positivt beløb i feltet **Beløb** debiteres på hovedkontoen og krediteres på modkontoen. Et negativt beløb krediteres på hovedkontoen og debiteres på modkontoen.

> [!NOTE]  
>   Moms beregnes separat for hovedkontoen og modkontoen, så der kan bruges forskellige momsprocentsatser.

## <a name="working-with-recurring-journals"></a>Arbejde med gentagelseskladder
En gentagelseskladde er en finanskladde med særlige felter til administration af transaktioner, som bogføres ofte med få eller ingen ændringer. Med disse felter til gentagelsestransaktioner kan du bogføre både faste og variable beløb. Du kan også angive automatiske tilbageførselsposter for dagen efter bogføringsdatoen og bruge allokeringsnøgler sammen med gentagelsesposterne.

## <a name="working-with-standard-journals"></a>Arbejde med standardkladder
Når du har oprettet kladdelinjer, som du ved, at du sandsynligvis skal oprette igen senere, kan du gemme dem som en standardkladde, inden du bogfører kladden. Denne funktion gælder for varekladder og finanskladder.

> [!NOTE]  
>   Følgende procedure beskriver varekladden, men oplysningerne gælder også for finanskladden.

### <a name="to-save-a-standard-journal"></a>Sådan gemmes en standardkladde
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varekladder**, og vælg derefter det relaterede link.
2. Indsæt en eller flere kladdelinjer.
3. Vælg de kladdelinjer, der skal genbruges.
4. Vælg handlingen **Gem som standardkladde**.
5. I vinduet **Gem som standardvarekladde** skal du definere en ny eller eksisterende standardvarekladde, som linjerne skal gemmes i.

    Hvis du allerede har oprettet en eller flere standardvarekladder og vil erstatte en af dem med det nye sæt varekladdelinjer, skal du vælge den ønskede kode i feltet Kode.
6. Vælg knappen **OK** for at bekræfte, at du vil overskrive den eksisterende standardvarekladde og erstatte alt indholdet.
7. Vælg feltet **Gem pris**, hvis værdierne i feltet **Pris** skal gemmes for standardvarekladden.
8. Vælg feltet **Gem antal**, hvis værdierne i feltet **Antal** skal gemmes.
9. Vælg knappen **OK** for at gemme standardvarekladden.

Når du har gemt standardvarekladden, vises vinduet Varekladde, så du kan bogføre varekladden. Nu kan du hurtigt oprette varekladden, næste gang du har brug for at bogføre de samme eller lignende linjer.

### <a name="to-reuse-a-standard-journal"></a>Sådan genbruges en standardkladde
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varekladder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Hent standardkladder**.

    Vinduet Standardvarekladder åbner med koder og beskrivelser for alle eksisterende standardvarekladder.
3. Vælg handlingen **Vis kladde**, hvis du vil gennemse en standardvarekladde, inden du vælger den til genbrug.

    De ændringer, du foretager i en standardvarekladde implementeres straks. De vil være der, næste gang du åbner eller genbruger standardvarekladden. Den pågældende standardvarekladde vil indeholde ændringerne, næste gang du åbner eller genbruger den. Ændringerne skal derfor være vigtige nok til, at de skal gælde generelt. Hvis det ikke er tilfældet, kan du foretage ændringerne i varekladden, efter at linjerne i standardvarekladden er indsat. Se trin 4 herunder.
4. Vælg den standardvarekladde i vinduet **Standardvarekladder**, du vil genbruge, og vælg derefter knappen **OK**.

    Varekladden udfyldes nu med de linjer, der er gemt i standardvarekladden. Hvis varekladden allerede indeholdt kladdelinjer, placeres de indsatte linjer under de eksisterende kladdelinjer.

    Hvis du ikke markerede feltet **Gem pris**, da du brugte funktionen **Gem som standardkladde**, indsættes varens aktuelle værdi automatisk i feltet **Pris**, værdien kopieres fra feltet **Kostpris** på varekortet.

    > [!NOTE]  
>   Hvis du markerede feltet **Gem pris** eller **Gem antal**, skal du kontrollere, at de indsatte værdier er korrekt for denne lagerregulering, inden du bogfører varekladden.

    Hvis indsatte varekladdelinjer indeholder gemte kostpriser, som du ikke vil bogføre, kan du hurtigt ændre dem til varernes aktuelle værdi på følgende måde:

6. Vælg de varekladdelinjen, som du vil regulere, og vælg derefter handlingen **Genberegn pris**. Derved opdateres feltet Pris med varens aktuelle pris.
7. Vælg handlingen **Bogfør**.

## <a name="to-renumber-document-numbers-in-journals"></a>Omnummerere bilagsnumre i kladder
Hvis du vil sikre dig, at du ikke får bogføringsfejl pga. bilagets nummerrækkefølge, kan du bruge funktionen **Omnummerer bilagsnumre**, før du bogfører en kladde.

I alle kladder, der er baseret på finanskladden, kan feltet **Bilagsnr** redigeres, så du kan angive forskellige bilagsnumre til forskellige kladdelinjer eller det samme bilagsnummer til relaterede kladdelinjer.

Hvis feltet **Nummerserie** i kladdenavnet er udfyldt, kræver bogføringsfunktionen i finanskladder, at bilagsnummeret på individuelle eller grupperede kladdelinjer er i rækkefølge. Hvis du vil sikre dig, at du ikke får bogføringsfejl pga. bilagets nummerrækkefølge, kan du bruge funktionen **Omnummerer bilagsnumre**, før du bogfører kladden. Hvis relaterede kladdelinjer er grupperet efter bilagsnummer, før du har brugt funktionen, forbliver de grupperet men kan være tildelt et andet bilagsnummer.

Denne funktion fungerer også i filtrerede visninger.

Ved enhver omnummerering af bilagsnumre respekteres relaterede udligninger, f.eks. en betalingsudligning, der er foretaget fra bilaget på kladdelinjen til en kreditorkonto. Derfor opdateres felterne **Udligningsid** og **Udligningsbilagsnr.** muligvis i de berørte finansposteringer.

Følgende procedure er baseret på vinduet **Kassekladde**, men gælder for alle andre kladder, der er baseret på finanskladden, f.eks. vinduet **Udbetalingskladde**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladder**, og vælg derefter det relaterede link.
2. Når du er klar til at bogføre kladden, skal du vælge handlingen **Omnummerer bilagsnumre**.

Værdier i feltet **Bilagsnr.** ændres, hvor det kræves, så bilagsnummeret på individuelle eller grupperede journallinjer er i rækkefølge. Når bilag omnummereres, kan du fortsætte med at bogføre kladden.

## <a name="see-also"></a>Se også
[Fremgangsmåde: Bogføre transaktioner direkte i finansposterne](finance-how-post-transactions-directly.md)  
[Sådan tilbageføres poster](finance-how-reverse-journal-posting.md)  
[Fremgangsmåde: Allokere omkostninger og indtægter](year-allocate-costs-income.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

