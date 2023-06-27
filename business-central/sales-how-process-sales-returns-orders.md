---
title: Gennemgå salgsreturvareordrer
description: 'Beskriver, hvordan du opretter en salgsreturordre for at behandle en returnering, annullering eller refusion for varer eller tjenester, du har modtaget betaling for.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return, order'
ms.search.form: '44, 134, 144, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/08/2021
ms.author: edupont
---
# <a name="process-sales-return-orders" />Gennemgå salgsreturvareordrer

Hvis du ønsker større kontrol over salgsreturvareprocessen, f.eks. med lagerdokumenter til håndtering af varer eller bedre overblik ved modtagelse af varer fra flere salgsdokumenter i én salgsreturnering, kan du oprette salgsreturvareordrer. En salgsreturvareordre udsteder automatisk den relaterede salgskreditnota og andre returvarerelaterede dokumenter, f.eks. en erstatningssalgsordre, hvis det er nødvendigt.

Ud over den oprindelige bogførte salgsfaktura kan du anvende salgskreditnotaen eller salgsreturvareordren på andre salgsdokumenter, for eksempel en anden bogført salgsfaktura, fordi kunden også returnerer varerne fra denne faktura.

## <a name="create-a-sales-return-order-based-on-one-or-more-posted-sales-documents" />Oprette en salgsreturvareordre baseret på et eller flere bogførte salgsdokumenter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsreturvareordrer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**.
4. I oversigtspanelet **Linjer** skal du udfylde linjerne manuelt eller kopiere oplysninger fra andre dokumenter for at udfylde linjerne automatisk:

    - Brug funktionen **Hent bogførte bilagslinjer, der skal tilbageføres**, hvis du vil kopiere en eller flere bogførte bilagslinjer fra et eller flere bogførte dokumenter. Denne funktion tilbagefører altid de eksakte beløb fra den bogførte bilagslinje. Denne funktion beskrives i følgende trin.    
    - Brug funktionen **Kopiér fra dokument**, så et eksisterende dokument kopieres til returvareordren. Du kan kopiere hele dokumentet med denne funktion. Det kan være et bogført dokument eller et dokument, der endnu ikke er bogført. Funktionen muliggør kun præcis kostprisudligning, når afkrydsningsfeltet **Obl. beløbstilbageførsel** er markeret på siden **Salgsopsætning**.  

5. Vælg handlingen **Behandle**, og vælg derefter **Hent bogførte bilagslinjer, der skal tilbageføres**.
6. Marker afkrydsningsfeltet **Vis kun linjer, der kan tilbageføres** øverst på siden **Bogførte salgsdokumentlinjer**, hvis du kun vil se linjer med antal, der endnu ikke er returneret, eller hvis det er købslinjer. Hvis et antal i en bogført salgsfaktura f.eks. allerede er returneret, vil du måske ikke returnere det antal i et nyt salgsreturvaredokument.

    > [!NOTE]  
    >  Dette felt kan kun bruges til bogførte leverancer og bogførte fakturalinjer. Det kan ikke bruges til bogførte returvarelinjer eller bogførte kreditnotalinjer.

    De forskellige bilagstyper er angivet i venstre side af siden, og tallet i parentes angiver antallet af tilgængelige bilag for hver bilagstype.

7. Vælg den type bogførte bilagslinjer, du vil bruge, i feltet **Dokumenttypefilter**.  
8. Vælg de linjer, som du vil kopiere til det nye dokument.  

    > [!NOTE]  
    >  Hvis du markerer alle linjer med <kbd>Ctrl</kbd>+<kbd>A</kbd>, kopieres alle linjer, der opfylder de filtreringskriterier, du har angivet, men der ses bort fra filteret **Vis kun linjer, der kan tilbageføres**. Du kan f.eks. have filtreret linjerne til et bestemt dokumentnummer med to linjer, hvoraf den ene allerede er returneret. Selv om afkrydsningsfeltet **Vis kun linjer, der kan tilbageføres** er markeret, kopieres der to linjer, i stedet for kun den ene, som endnu ikke er tilbageført, når du trykker på <kbd>Ctrl</kbd>+<kbd>A</kbd> for at kopiere alle linjer.  

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

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order" />Sådan oprettes en erstatningssalgsordre fra en salgsreturvareordre
Antag, at du har besluttet at kompensere en kunde ved at udskifte den vare, som er solgt. Udskiftningsvaren kan være den samme type vare eller en anden type. Sidstnævnte situation kan f.eks. være tilfældet, hvis der er leveret en forkert vare.  

1. På siden **Salgsreturvareordre** for en aktiv returproces skal du på en tom linje angive en negativ postering for erstatningsvaren ved at indsætte et negativt beløb i feltet **Antal**.  
2. Vælg handlingen **Flyt negative linjer**.
3. På siden **Flyt negative salgslinjer** skal du udfylde felterne efter behov.
4. Vælg knappen **OK**. Den negative linje for erstatningsvaren slettes fra salgsreturvareordren og indsættes på en ny **Salgsordre**-side. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order" />Sådan oprettes returvarerelaterede dokumenter med udgangspunkt i en salgsreturvareordre
Salgsordrer på erstatningsvarer, købsreturvareordrer og erstatningskøbsordrer kan oprettes automatisk under salgsreturvareprosssen. Dette er nyttigt f.eks. i situationer, hvor du vil håndtere varer med garantier fra leverandører.

1. På siden **Salgsreturvareordre** for en aktiv returneringsproces skal du vælge handlingen **Opret returrelaterede dokumenter**.
2. I feltet **Kreditornummer** skal du angive nummeret på en kreditor, hvis du vil oprette kreditorbilag automatisk.
3. Hvis en returneret vare skal returneres til leverandøren, skal du markere afkrydsningsfeltet **Opret købsreturv.ordre**.
4. Hvis en returneret vare bestilles hos leverandøren, skal du markere afkrydsningsfeltet **Opret købsordre**.
5. Hvis der skal oprettes en salgsordre på en erstatningsvare, skal du markere afkrydsningsfeltet **Opret salgsordre**.

## <a name="to-create-a-restock-charge" />Sådan gør du: Oprette et reklamationsgebyr
Der kan være tilfælde, hvor en kunde skal opkræves et gebyr for omkostningerne ved den fysiske håndtering af en vare. Det kan f.eks. være fordi, at kunden har bestilt en forkert vare ved en fejltagelse eller skifter mening efter modtagelsen af varen.

Du kan bogføre den forøgede omkostning som et varegebyr i en kreditnota eller returvareordre og tildele den til den bogførte levering. Nedenfor beskrives dette for en salgsreturvareordre, men samme fremgangsmåde anvendes ved en salgskreditnota.

1. Åbn siden **Salgsreturvareordre** for en aktiv returproces.
2. På en ny linje skal du vælge **Gebyr (Vare)** i feltet **Type**.  
3. Udfyld felterne som ved enhver varegebyrlinje. Du kan finde flere oplysninger i [Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md).  

Når du bogfører salgsreturvareordren, føjes reklamationsgebyret til den relevante salgspost. Det gør det muligt at opretholde en præcis lagerværdi.  

## <a name="see-related-microsoft-training" />Se relateret [Microsoft-træning](/training/paths/return-items-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
