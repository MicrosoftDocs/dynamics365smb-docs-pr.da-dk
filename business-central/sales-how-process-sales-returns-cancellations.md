---
title: Behandle salgsreturvarer eller annulleringer | Microsoft Docs
description: Beskriver, hvordan du opretter en salgskreditnota, direkte eller via en salgsreturvareordre, for at behandle en returnering, annullering eller refusion for varer eller tjenester, du har modtaget betaling for.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 1c1bcb570f06719cfbb8930667a2f2847003d93c
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="process-sales-returns-or-cancellations"></a>Behandle salgsreturvarer eller annulleringer
Hvis en debitor ønsker at returnere varer eller få refunderet varer eller serviceydelser, som du har solgt og modtaget betaling for, skal du oprette og bogføre en salgskreditnota, der angiver den ønskede ændring. Du kan oprette salgskreditnotaen direkte fra den bogførte salgsfaktura for at medtage de korrekte salgsfakturaoplysninger, eller du kan oprette en ny salgskreditnota med kopierede fakturaoplysninger.

Hvis du ønsker større kontrol over salgsreturvareprocessen, f.eks. med lagerdokumenter til håndtering af varer eller bedre overblik ved modtagelse af varer fra flere salgsdokumenter i én salgsreturnering, kan du oprette salgsreturvareordrer. En salgsreturvareordre udsteder automatisk den relaterede salgskreditnota og andre returvarerelaterede dokumenter, f.eks. en erstatningssalgsordre, hvis det er nødvendigt. Yderligere oplysninger finder du i afsnittet "Sådan oprettes en salgsreturvareordre baseret på et eller flere bogførte salgsdokumenter".

> [!NOTE]  
>   Hvis en bogført salgsfaktura endnu ikke er betalt, kan du bruge funktionen **Ret** eller **Annuller** på den bogførte salgsfaktura, så du tilbagefører transaktionerne. Disse funktioner fungerer kun for ubetalte fakturaer, og de understøtter ikke delvise returneringer eller annulleringer. Du kan finde flere oplysninger under [Rette eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md).

En returnering eller refusion kan vedrøre nogle af varerne eller tjenesteydelserne på den oprindelige salgsfaktura. Det er tilfældet skal du redigere oplysningerne på linjerne i salgskreditnotaen eller salgsreturvareordren. Når du bogfører salgskreditnotaen eller salgsreturvareordren, tilbageføres de salgsdokumenter, der berøres af ændringen, og der kan oprettes en refusionsbetaling til debitoren. Du kan finde flere oplysninger under [Foretage betalinger](payables-make-payments.md).  

Ud over den oprindelige bogførte salgsfaktura kan du anvende salgskreditnotaen eller salgsreturvareordren på andre salgsdokumenter, for eksempel en anden bogført salgsfaktura, fordi kunden også returnerer varerne fra denne faktura.

Du kan sende den bogførte salgskreditnota til debitoren for at bekræfte returneringen eller annulleringen og kommunikere, at den tilhørende værdi vil blive refunderet, f.eks. når varerne returneres.

Bogføringen af kreditnotaen gendanner også de varegebyrer, der er tildelt til det bogførte dokument, så varens værdiposter er de samme, som før varegebyret blev tildelt.

## <a name="inventory-costing"></a>Lagerkostmetode
Hvis du vil bevare korrekt lagerværdi, skal du typisk placere returnerede varer tilbage i lagerbeholdningen med den kostpris, som de blev solgt til, og ikke til deres aktuelle kostpris. Dette omtales som præcis kostprisudligning.

Der findes to funktioner til at tildele præcis kostprisudligning automatisk.   

|Funktion|Beskrivelse|  
|------------------|---------------------------------------|  
|Funktionen **Hent bogførte bilagslinjer, der skal tilbageføres** på siden **Salgsreturvareordre**|Kopierer linjer for et eller flere bogførte bilag, der skal tilbageføres, til salgsreturvareordren. Yderligere oplysninger finder du i afsnittet "Sådan oprettes en salgsreturvareordre og relateret salgskreditnota til en eller flere bogførte salgsfakturaer".|  
|Funktionen **Kopiér dokument** på siderne **Salgskreditnota** og **Salgsreturvareordre**|Kopierer både sidehoved og linjerne i et og samme bogførte dokument, der skal tilbageføres.<br /><br /> Kræver, at afkrydsningsfeltet **Obl. beløbstilbageførsel** er markeret på siden **Salgsopsætning**.|

Hvis du vil tildele præcis kostprisudligning manuelt, skal du vælge feltet **Udlign-fra varepost** på en vilkårlig type returdokumentlinje, og derefter vælge nummeret på den oprindelige salgspost. På den måde knyttes salgskreditnotaen eller salgsreturvareordren til den oprindelige salgspost, og varen værdiansættes til den oprindelige kostpris.

Du kan finde flere oplysninger i [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Sådan oprettes en salgskreditnota fra en bogført salgsfaktura
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte salgsfakturaer**, og vælg derefter det relaterede link.  
2. På siden **Bogf. salgsfakturaer** skal du vælge den bogførte salgsfaktura, der skal tilbageføres, og derefter vælge handlingen **Opret rettelseskreditnota**.

    Salgskreditnotahovedet indeholder nogle oplysninger fra den bogførte salgsfaktura. Du kan redigere disse oplysninger f.eks med nye oplysninger, der afspejler returneringsaftalen.  
3. Rediger oplysningerne på linjerne i overensstemmelse med aftalen, f.eks antallet af returnerede varer eller beløbet, der skal refunderes.
4. Vælg handlingen **Udlign**.
5. På siden **Udlign debitorposter** skal du vælge linjen med det bogførte salgsdokument, du vil udligne salgskreditnotaen til, og vælg derefter handlingen **Udlignings-id**.

    Salgskreditnotaens id vises i feltet **Udlignings-id**.
6. I feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne, hvis det er mindre end det oprindelige beløb.  

    Nederst på siden **Udlign debitorposter** kan du se det samlede beløb, der skal udlignes for at tilbageføre alle involverede poster, dvs. når værdien i feltet **Saldo** er nul.
7. Vælg knappen **OK**. Når du bogfører salgskreditnotaen, bliver den udlignet til de bogførte salgsdokumenter.

    Når du har oprettet eller redigeret de ønskede salgskreditnotalinjer, og anvendelse på enkelt eller flere er angivet, kan du bogføre salgskreditnotaen.   
8. Vælg handlingen **Bogfør og send**.  

Dialogboksen **Bekræftelse af bogfør og send** åbnes og viser den foretrukne afsendelsesmetode til kunden. Du kan ændre afsendelsesmetoden ved at vælge opslagsknappen for feltet **Send bilag til**. Du kan finde flere oplysninger under [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).  

De bogførte salgsdokumenter, som du tilknytter kreditnotaen, tilbageføres nu, og der kan oprettes en refusionsbetaling til debitoren. Salgskreditnotaen fjernes og erstattes med et nyt bilag i oversigten over bogførte salgskreditnotaer.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Sådan oprettes en salgskreditnota ved at kopiere en bogført salgsfaktura
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgskreditnotaer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny** for at åbne en ny tom salgskreditnota.
3. I feltet **Debitor** skal du indtaste navnet på en eksisterende debitor.
4. Vælg handlingen **Kopier linjer**.
5. På siden **Kopier salgsdokument** skal du vælge **Bogført faktura** i feltet **Dokumenttype**.
6. Vælg feltet **Bilagsnr.** for at åbne siden **Bogf. salgsfakturaer**, og vælg derefter den bogførte salgsfaktura, der indeholder linjer, som du vil tilbageføre.
7. Marker afkrydsningsfeltet **Genberegn linjer**, hvis du vil opdatere de kopierede bogførte salgsfakturalinjer med eventuelle ændringer i varepris og kostpris, siden fakturaen blev bogført.
8. Vælg knappen **OK**. De kopierede fakturalinjer skal indsættes i salgskreditnotaen.
9. Udfyld salgskreditnotaen, som beskrevet i afsnittet "Sådan oprettes en salgskreditnota fra en bogført salgsfaktura" i dette emne.

## <a name="to-create-a-sales-return-order-based-on-one-or-more-a-posted-sales-documents"></a>Sådan oprettes en salgsreturvareordre baseret på et eller flere bogførte salgsdokumenter.
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsreturvareordrer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**.
4. I oversigtspanelet **Linjer** skal du udfylde linjerne manuelt eller kopiere oplysninger fra andre dokumenter for at udfylde linjerne automatisk:

    - Brug funktionen **Hent bogførte bilagslinjer, der skal tilbageføres**, hvis du vil kopiere en eller flere bogførte bilagslinjer fra et eller flere bogførte dokumenter. Denne funktion tilbagefører altid de eksakte beløb fra den bogførte bilagslinje. Denne funktion beskrives i følgende trin.    
    - Brug funktionen **Kopier dokument**, så et eksisterende dokument kopieres til returvareordren. Du kan kopiere hele dokumentet med denne funktion. Det kan være et bogført dokument eller et dokument, der endnu ikke er bogført. Funktionen muliggør kun præcis kostprisudligning, når afkrydsningsfeltet **Obl. beløbstilbageførsel** er markeret på siden **Salgsopsætning**.  

5. Vælg handlingen **Hent bogførte bilagslinjer, der skal tilbageføres**.
6. Marker afkrydsningsfeltet **Vis kun linjer, der kan tilbageføres** øverst på siden **Bogførte salgsdokumentlinjer**, hvis du kun vil se linjer med antal, der endnu ikke er returneret, eller hvis det er købslinjer. Hvis et antal i en bogført salgsfaktura f.eks. allerede er returneret, vil du måske ikke returnere det antal i et nyt salgsreturvaredokument.

    > [!NOTE]  
    >  Dette felt kan kun bruges til bogførte leverancer og bogførte fakturalinjer. Det kan ikke bruges til bogførte returvarelinjer eller bogførte kreditnotalinjer.

    De forskellige bilagstyper er angivet i venstre side af siden, og tallet i parentes angiver antallet af tilgængelige bilag for hver bilagstype.

7. Vælg den type bogførte bilagslinjer, du vil bruge, i feltet **Dokumenttypefilter**.  
8. Vælg de linjer, som du vil kopiere til det nye dokument.  

    > [!NOTE]  
    >  Hvis du markerer alle linjer med Ctrl+A, kopieres alle linjer, der opfylder de filtreringskriterier, du har angivet, men der ses bort fra filteret **Vis kun linjer, der kan tilbageføres**. Du kan f.eks. have filtreret linjerne til et bestemt dokumentnummer med to linjer, hvoraf den ene allerede er returneret. Selv om afkrydsningsfeltet **Vis kun linjer, der kan tilbageføres** er markeret, kopieres der to linjer, i stedet for kun den ene, som endnu ikke er tilbageført, når du trykker på Ctrl+A for at kopiere alle linjer.  

9. Vælg knappen **OK** for at kopiere linjerne til det nye dokument.  

    Der sker følgende:  

    -   Der oprettes en ny bilagslinje for bogførte bilagslinjer, der er af typen **Vare**. Den nye bilagslinje er en kopi af den bogførte bilagslinje med det antal, der endnu ikke er blevet tilbageført. Feltet **Udlign-fra varepost** udfyldes efter behov med nummeret på vareposten for den bogførte bilagslinje.  

    -   Der oprettes en ny bilagslinje for bogførte bilagslinjer, der ikke er af typen **Vare** f.eks. varegebyrer. Den nye bilagslinje er en kopi af den oprindelige bogførte bilagslinje.  

    -   Værdien i feltet **Kostpris (RV)** på den nye linje beregnes på basis af beløbene i de tilsvarende vareposter.  

    -   Hvis det kopierede dokument omhandler en bogført leverance, bogført modtagelse, bogført returvaremodtagelse eller bogført returvareleverance, beregnes kostprisen automatisk på basis af varekortet.  

    -   Hvis det kopierede dokument er en bogført faktura eller kreditnota, kopieres enhedsprisen, fakturarabatter og linerabatter fra den bogførte bilagslinje.  

    -   Hvis den bogførte bilagslinje indeholder varesporingslinjer, udfyldes feltet **Udlign fra-varepost** på varesporingslinjerne udfyldes med de relevante varepostnumre fra de bogførte varesporingslinjer.  

     Når der kopieres fra en bogført faktura eller en bogført kreditnota, kopieres relevante fakturarabatter og linjerabatter, der var gældende på det tidspunkt, hvor dokumentet blev bogført, fra den bogførte bilagslinje til den nye bilagslinje. Vær dog opmærksom på, at hvis **Beregn fakturarabat** aktiveres på siden **Salg og tilgodehavender**, beregnes fakturarabatten igen, når du bogfører den nye dokumentlinje. Linjebeløbet for den nye linje kan derfor være forskelligt fra Linjebeløb for den oprindelige bilagslinje, alt efter den nye beregning af fakturarabatten.  

     > [!NOTE]  
     >  Hvis en del af antallet på den bogførte bilagslinje allerede er tilbageført, solgt eller forbrugt, oprettes der kun en linje til det antal, der stadig er på lager, eller som endnu ikke er returneret. Hvis hele antallet på den bogførte bilagslinje allerede er tilbageført, oprettes der ikke en ny bilagslinje.  
     >   
     >  Hvis varebevægelserne i det bogførte dokument er de samme som i det nye dokument, oprettes der ganske enkelt en kopi af den oprindelige, bogførte bilagslinje i det nye dokument. Feltet **Udlign fra-varepost** udfyldes ikke, fordi i dette tilfælde, er præcis kostprisudligning ikke muligt. Hvis du f.eks. bruger funktionen **Hent bogførte bilagslinjer, der skal tilbageføres** for at hente en bogført salgskreditnotalinje til en ny salgskreditnota, er det kun den oprindelige, bogførte kreditnotalinje, der kopieres til den nye kreditnota.  

10. På siden **Salgsreturvareordre** i feltet **Returårsagskode** skal du på hver linje vælge årsagen til returneringen.
11. Vælg handlingen **Bogfør**.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>Sådan oprettes en erstatningssalgsordre fra en salgsreturvareordre
Antag, at du har besluttet at kompensere en kunde ved at udskifte den vare, som er solgt. Udskiftningsvaren kan være den samme type vare eller en anden type. Sidstnævnte situation kan f.eks. være tilfældet, hvis der er leveret en forkert vare.  

1. På siden **Salgsreturvareordre** for en aktiv returproces skal du på en tom linje angive en negativ postering for erstatningsvaren ved at indsætte et negativt beløb i feltet **Antal**.  
2. Vælg handlingen **Flyt negative linjer**.
3. På siden **Flyt negative salgslinjer** skal du udfylde felterne efter behov.
4. Vælg knappen **OK**. Den negative linje for erstatningsvaren slettes fra salgsreturvareordren og indsættes på en ny **Salgsordre**-side. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a>Sådan oprettes returvarerelaterede dokumenter med udgangspunkt i en salgsreturvareordre
Salgsordrer på erstatningsvarer, købsreturvareordrer og erstatningskøbsordrer kan oprettes automatisk under salgsreturvareprosssen. Dette er nyttigt f.eks. i situationer, hvor du vil håndtere varer med garantier fra leverandører.

1. På siden **Salgsreturvareordre** for en aktiv returneringsproces skal du vælge handlingen **Opret returrelaterede dokumenter**.
2. I feltet **Kreditornummer** skal du angive nummeret på en kreditor, hvis du vil oprette kreditorbilag automatisk.
3. Hvis en returneret vare skal returneres til leverandøren, skal du markere afkrydsningsfeltet **Opret købsreturv.ordre**.
4. Hvis en returneret vare bestilles hos leverandøren, skal du markere afkrydsningsfeltet **Opret købsordre**.
5. Hvis der skal oprettes en salgsordre på en erstatningsvare, skal du markere afkrydsningsfeltet **Opret salgsordre**.

## <a name="to-create-a-restock-charge"></a>Sådan gør du: Oprette et reklamationsgebyr
Der kan være tilfælde, hvor en kunde skal opkræves et gebyr for omkostningerne ved den fysiske håndtering af en vare. Det kan f.eks. være fordi, at kunden har bestilt en forkert vare ved en fejltagelse eller skifter mening efter modtagelsen af varen.

Du kan bogføre den forøgede omkostning som et varegebyr i en kreditnota eller returvareordre og tildele den til den bogførte levering. Nedenfor beskrives dette for en salgsreturvareordre, men samme fremgangsmåde anvendes ved en salgskreditnota.

1. Åbn siden **Salgsreturvareordre** for en aktiv returproces.
2. På en ny linje skal du vælge **Gebyr (Vare)** i feltet **Type**.  
3. Udfyld felterne som ved enhver varegebyrlinje. Du kan finde flere oplysninger i [Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md).  

Når du bogfører salgsreturvareordren, føjes reklamationsgebyret til den relevante salgspost. Det gør det muligt at opretholde en præcis lagerværdi.  

## <a name="to-create-a-sales-allowance"></a>Sådan oprettes et salgsnedslag
Du kan have brug for at sende en kunde en kreditnota med en prisreduktion, hvis kunden har modtaget en let beskadiget vare eller modtaget varerne for sent.  
Du kan bogføre den reducerede pris som et varegebyr i en kreditnota eller returvareordre og tildele den til den bogførte levering. Nedenfor beskrives dette for en salgskreditnota, men samme fremgangsmåde anvendes ved en salgsreturvareordre.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgskreditnotaer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny** for at åbne en ny tom salgskreditnota.
3. Udfyld hovedet på kreditnotaen med de relevante oplysninger om den kunde, som du vil give salgsdekorten til.  
4. Marker **Gebyr (vare)** i feltet **Type** på oversigtspanelet **Linjer**.  
5.  I feltet **Nummer** skal du markere det relevante varegebyrværdi.  
     Du skal evt. oprette en særligt varegebyrnummer, der dækker salgsdekorten.  
6.  Angiv **1** i feltet **Antal**.  
7.  Angiv beløbet på salgsdekorten i feltet **Salgspris**.  
8.  Tildel salgsnedslaget som et varegebyr på varerne i den bogførte leverance. Du kan finde flere oplysninger i [Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md). Vend derefter tilbage til siden **Salgskreditnota**.  

Når du bogfører salgsreturvareordren, føjes salgsnedslaget til den relevante salgspost. Det gør det muligt at opretholde en præcis lagerværdi.

## <a name="to-combine-return-receipts"></a>Sådan samles returvaremodtagelser
Du kan kombinere returvaremodtagelser, hvis en kunde returnerer varer, som stammer fra forskellige salgsreturvareordrer.  

Når du modtager varerne på lagerstedet, skal du bogføre salgsreturvareordrerne som modtaget. Dette opretter bogførte returvaremodtagelser.  

Når du skal fakturere kunden, kan du i stedet for at fakturere hver salgsreturvareordre særskilt oprette en salgskreditnota og automatisk kopiere de bogførte returvaremodtagelseslinjer til dokumentet. Derefter kan du bogføre salgskreditnotaen og spare tid ved at fakturere alle de åbne salgsreturvareordrer samtidigt.  

Hvis du vil kombinere returvaremodtagelser skal afkrydsningsfeltet **Tillad samlefaktura** være markeret på siden **Debitorkort**.  

### <a name="to-manually-combine-return-receipts"></a>Sådan samles returvaremodtagelser manuelt  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgskreditnota**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**.  
4. Vælg handlingen **Hent returvaremodt.linjer**.  
5. Markér de returvarelinjer, der skal indgå i kreditnotaen:  

    -   Hvis alle linjer skal indsættes, skal du markere samtlige linjer og derefter vælge knappen **OK**.  

    -   Hvis specifikke linjer skal indsættes, skal du markere linjerne og derefter vælge knappen **OK**.  

6.  Hvis du kommer til at vælge en forkert modtagelseslinje eller vil begynde forfra, skal du bare slette linjerne på kreditnotaen og bruge funktionen **Hent returvaremodt.linjer** igen.  
7.  Bogfør fakturaen.  

### <a name="to-automatically-combine-return-receipts"></a>Sådan samles returvaremodtagelser automatisk  
Du kan samle returvaremodtagelser automatisk og også vælge at bogføre kreditnotaerne automatisk med funktionen **Saml returvarekvit**.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Saml returvarekvit.**, og vælg derefter det relaterede link.
2. På siden **Saml returvarekvit** skal du udfylde felterne for at vælge de relevante returvaremodtagelser.
3. Markér afkrydsningsfeltet **Bogfør kreditnotaer**. Hvis ikke, skal du manuelt bogføre de købskreditnotaer, der oprettes.
4.  Vælg knappen **OK**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>Sådan fjernes en modtaget og faktureret returvareordre  
Når du fakturerer returvaremodtagelser på denne måde, findes returvareordrerne, som returvaremodtagelserne er bogført fra, stadig, selvom de er modtaget og faktureret i fuldt omfang.  

Når returvaremodtagelser samles på en kreditnota og bogføres, oprettes der en bogført salgskreditnota for de krediterede linjer. Feltet **Faktureret (antal)** på den oprindelige salgsreturvareordre opdateres på basis af det fakturerede antal.   
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet fakturerede salgsreturvareordrer**, og vælg det relaterede link.  
2.  I feltet **Nummer** skal du angive, hvilke returvareordrer der skal slettes.  
3.  Vælg knappen **OK**.  

Du kan også slette individuelle salgsreturordrer manuelt.   

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

