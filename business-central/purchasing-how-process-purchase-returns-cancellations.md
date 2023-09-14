---
title: Behandle salgsreturvarer eller annulleringer
description: 'Beskriver, hvordan du kan oprette og bogføre en købskreditnota, når du returnerer varer til en leverandør eller annullerer købte tjenester.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'cancel, undo, correct'
ms.search.form: '6640, 6643, 9307, 9309, 9308, 6652, 145, 147'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Behandle købsreturvarer eller annulleringer

Hvis du skal returnere varer til din kreditor eller annullere serviceydelser, som du har købt, kan du oprette og bogføre en købskreditnota, der angiver den ønskede ændring for den oprindelige købsfaktura. Du kan oprette købskreditnotaen direkte fra den bogførte salgsfaktura for at medtage de korrekte købsfakturaoplysninger, eller du kan oprette en ny købskreditnota med kopierede fakturaoplysninger.

Hvis du ønsker større kontrol over købsreturvareprocessen, f.eks. med lagerdokumenter til håndtering af varer eller bedre overblik ved returnering af varer fra flere købsdokumenter i én købsreturnering, kan du oprette købsreturvareordrer. En købsreturvareordre udsteder automatisk den relaterede købskreditnota. Yderligere oplysninger finder du i [Sådan oprettes en købsreturvareordre baseret på et eller flere bogførte købsdokumenter](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

> [!NOTE]  
> Hvis en bogført købsfaktura endnu ikke er betalt, kan du bruge funktionen **Ret** eller **Annuller** på den bogførte købsfaktura, så du automatisk tilbagefører de pågældende transaktioner. Disse funktioner fungerer kun for ubetalte fakturaer, og de understøtter ikke delvise returneringer eller annulleringer. Du kan heller ikke rette eller annullere købsfakturaer, der er bogført med modtagelser fra mere end én købsordre. Du kan finde flere oplysninger i [Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Du opretter typisk en købskreditnota eller en købsreturvareordre som reaktion på en kreditnota, der er sendt til dig af en kreditor. Købskreditnotaen eller købsreturvareordren fungerer som din interne dokumentation i kreditnotaprocessen ved regnskabsførelse eller ved styring af leveringen af de involverede varer.

Ændringen kan være relateret til alle produkterne på den oprindelige købsfaktura eller kun til nogle af produkterne. Tilsvarende kan du delvist returnere modtagne varer eller kræve delvis refusion af modtagne serviceydelser. I dette tilfælde skal du redigere oplysningerne på købskreditnotaen eller købsreturvareordren.

Ud over den oprindelige bogførte købsfaktura kan du anvende købskreditnotaen eller købsreturvareordren på andre købsdokumenter, for eksempel en anden bogført købsfaktura, fordi du også returnerer varerne fra denne faktura.

Bogføringen af kreditnotaen gendanner også de varegebyrer, der er tildelt det bogførte dokument, så varens værdiposter er de samme, som før varegebyret blev tildelt.

## Lagerkostmetode
Hvis du vil bevare korrekt lagerværdi, skal du typisk plukke returvarer fra lagerbeholdningen med den kostpris, som de blev købt til, og ikke til deres aktuelle kostpris. Dette omtales som præcis kostprisudligning.

Der findes to funktioner til at tildele præcis kostprisudligning automatisk.  

|Funktion|Beskrivelse|  
|------------------|---------------------------------------|  
|Funktionen **Hent bogførte bilagslinjer, der skal tilbageføres** på siden **Købsreturvareordre**|Kopierer linjer for et eller flere bogførte bilag, der skal tilbageføres, til købsreturvareordren. Yderligere oplysninger finder du i [Sådan oprettes en købsreturvareordre baseret på et eller flere bogførte købsdokumenter](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-return-order-based-on-one-or-more-posted-purchase-documents).|  
|Funktionen **Kopiér fra dokument** på siderne **Købskreditnota** og **Købsreturvareordre**|Kopierer både sidehoved og linjerne i et og samme bogførte dokument, der skal tilbageføres.<br /><br /> Kræver, at afkrydsningsfeltet **Obl. beløbstilbageførsel** er markeret på siden **Købsopsætning**.|

Hvis du vil tildele præcis kostprisudligning manuelt, skal du vælge feltet **Udlign-fra varepost** på en vilkårlig type returdokumentlinje, og derefter vælge nummeret på den oprindelige købspost. På den måde knyttes købskreditnotaen eller købsreturvareordren til den oprindelige købspost, og varen værdiansættes til den oprindelige kostpris.

Du kan finde flere oplysninger i [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md).

## Sådan oprettes en købskreditnota fra en bogført købsfaktura

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.  
2. På siden **Bogf. købsfakturaer** skal du vælge den bogførte købsfaktura, der skal tilbageføres, og derefter vælge handlingen **Opret rettelseskreditnota**.

    De fleste felter i hovedet på købskreditnotaen er udfyldt med oplysninger fra den bogførte købsfaktura. Du kan redigere alle felterne f.eks med nye oplysninger, der afspejler returneringsaftalen.
3. Rediger oplysningerne på linjerne i overensstemmelse med aftalen, f.eks antallet varer, der er returneret, eller beløbet der skal refunderes.
4. Vælg handlingen **Udlign**.
5. På siden **Udlign kred.poster** skal du vælge linjen med det bogførte købsdokument, du vil udligne købskreditnotaen til, og vælg derefter handlingen **Udlignings-id**. Købskreditnotaens nummer indsættes i feltet **Udlignings-id**.
6. I feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne, hvis det er mindre end det oprindelige beløb.

    Nederst på siden **Udlign** kan du se det samlede beløb, der skal udlignes for at tilbageføre alle involverede poster, dvs. når værdien i feltet **Saldo** er nul.
7. Vælg knappen **OK**. Når du bogfører købskreditnotaen, bliver den anvendt på de angivne bogførte købsdokumenter.

    Når du har oprettet eller redigeret de ønskede købskreditnotalinjer, og anvendelse på enkelt eller flere er angivet, kan du fortsætte med at bogføre købskreditnotaen.
8. Vælg handlingen **Bogfør**.

De bogførte købsfakturaer, som du udligner kreditnotaen med, tilbageføres nu. Hvis du allerede har betalt den oprindelige faktura, skal leverandøren nu refundere betalingen til dig. Hvis kreditnotaen kun er for en del af produktet på den oprindelige faktura, kan du kun betale det resterende beløb på den originale købsfaktura for at lukke den.

Købskreditnotaen fjernes og erstattes med et nyt bilag i oversigten over bogførte købskreditnotaer.

## Sådan oprettes en købskreditnota ved at kopiere en bogført købsfaktura

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købskreditnotaer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny** for at åbne en ny tom købskreditnota.
3. I feltet **Kreditor** skal du indtaste navnet på en eksisterende kreditor.
4. Vælg handlingen **Kopier fra dokument**.
5. På siden **Kopier købsdokument** skal du vælge **Bogført faktura** i feltet **Dokumenttype**.
6. Vælg feltet **Bilagsnr.** for at åbne siden **Bogf. købsfakturaer**, og vælg derefter den bogførte købsfaktura, der indeholder linjer, som du vil tilbageføre.
7. Marker afkrydsningsfeltet **Genberegn linjer**, hvis du vil opdatere de kopierede bogførte købsfakturalinjer med eventuelle ændringer i varepris og kostpris, siden fakturaen blev bogført.
8. Vælg knappen **OK**. De kopierede fakturalinjer skal indsættes i købskreditnotaen.
9. Udfyld købskreditnotaen, som beskrevet i [Sådan oprettes en købskreditnota fra en bogført købsfaktura](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

## Sådan oprettes en købsreturvareordre baseret på et eller flere bogførte købsdokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsreturvareordrer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**.
4. I oversigtspanelet **Linjer** skal du udfylde linjerne manuelt eller kopiere oplysninger fra andre dokumenter for at udfylde linjerne automatisk:

    - Brug funktionen **Hent bogførte bilagslinjer, der skal tilbageføres**, hvis du vil kopiere en eller flere bogførte bilagslinjer fra et eller flere bogførte dokumenter. Denne funktion tilbagefører altid de eksakte beløb fra den bogførte bilagslinje. Denne funktion beskrives i følgende trin.    
    - Brug funktionen **Kopiér fra dokument**, så et eksisterende dokument kopieres til returvareordren. Du kan kopiere hele dokumentet med denne funktion. Det kan være et bogført dokument eller et dokument, der endnu ikke er bogført. Funktionen muliggør kun præcis kostprisudligning, når afkrydsningsfeltet **Obl. beløbstilbageførsel** er markeret på siden **Salgsopsætning**.  

5. Vælg handlingen **Hent bogførte bilagslinjer, der skal tilbageføres**.
6. Marker afkrydsningsfeltet **Vis kun linjer, der kan tilbageføres** øverst på siden **Bogførte købsdokumentlinjer**, hvis du kun vil se linjer med antal, der endnu ikke er returneret, eller hvis det er købslinjer. Hvis et antal i en bogført købsfaktura f.eks. allerede er returneret, vil du måske ikke medtage det antal i et nyt købsreturvaredokument.

    > [!NOTE]  
    >  Dette felt kan kun bruges til bogførte kvitteringer og bogførte fakturalinjer, ikke til bogførte retur- eller bogførte kreditnotalinjer.  

    De forskellige bilagstyper er angivet i venstre side af siden, og tallet i parentes angiver antallet af tilgængelige bilag for hver bilagstype.

7. Vælg den type bogførte bilagslinjer, du vil bruge, i feltet **Dokumenttypefilter**.  
8. Vælg de linjer, som du vil kopiere til det nye dokument.  

    > [!NOTE]  
    >  Hvis du markerer alle linjer med <kbd>Ctrl</kbd>+<kbd>A</kbd>, kopieres alle linjer, der opfylder de filtreringskriterier, du har angivet, men der ses bort fra filteret **Vis kun linjer, der kan tilbageføres**. Du kan f.eks. have filtreret linjerne til et bestemt dokumentnummer med to linjer, hvoraf den ene allerede er returneret. Selv om afkrydsningsfeltet **Vis kun linjer, der kan tilbageføres** er markeret, kopieres der to linjer, i stedet for kun den ene, som endnu ikke er tilbageført, når du trykker på <kbd>Ctrl</kbd>+<kbd>A</kbd> for at kopiere alle linjer.  

9. Vælg knappen **OK** for at kopiere linjerne til det nye dokument.  

    Der sker følgende:  

    - Der oprettes en ny bilagslinje for bogførte bilagslinjer, der er af typen **Vare**. Den nye bilagslinje er en kopi af den bogførte bilagslinje med det antal, der endnu ikke er blevet tilbageført. Feltet **Udlign-til varepost** udfyldes efter behov med nummeret på vareposten for den bogførte bilagslinje.  

    - Der oprettes en ny bilagslinje for bogførte bilagslinjer, der ikke er af typen **Vare** f.eks. varegebyrer. Den nye bilagslinje er en kopi af den oprindelige bogførte bilagslinje.  

    - Værdien i feltet **Kostpris (RV)** på den nye linje beregnes på basis af beløbene i de tilsvarende vareposter.  

    - Hvis det kopierede dokument omhandler en bogført leverance, bogført modtagelse, bogført returvaremodtagelse eller bogført returvareleverance, beregnes kostprisen automatisk på basis af varekortet.  

    - Hvis det kopierede dokument er en bogført faktura eller kreditnota, kopieres enhedsprisen, fakturarabatter og linerabatter fra den bogførte bilagslinje.  

    - Hvis den bogførte bilagslinje indeholder varesporingslinjer, udfyldes feltet **Udlign til-varepost** på varesporingslinjerne udfyldes med de relevante varepostnumre fra de bogførte varesporingslinjer.  

     Når der kopieres fra en bogført faktura eller en bogført kreditnota, kopieres relevante fakturarabatter og linjerabatter, der var gældende på det tidspunkt, hvor dokumentet blev bogført, fra den bogførte bilagslinje til den nye bilagslinje. Vær dog opmærksom på, at hvis **Beregn fakturarabat** aktiveres på siden **Købsopsætning**, beregnes fakturarabatten igen, når du bogfører den nye dokumentlinje. Linjebeløbet for den nye linje kan derfor være forskelligt fra Linjebeløb for den oprindelige bilagslinje, alt efter den nye beregning af fakturarabatten.  

    > [!NOTE]  
    >  Hvis en del af antallet på den bogførte bilagslinje allerede er tilbageført, solgt eller forbrugt, oprettes der kun en linje til det antal, der stadig er på lager, eller som endnu ikke er returneret. Hvis hele antallet på den bogførte bilagslinje allerede er tilbageført, oprettes der ikke en ny bilagslinje.  
    >
    >  Hvis varebevægelserne i det bogførte dokument er de samme som i det nye dokument, oprettes der ganske enkelt en kopi af den oprindelige, bogførte bilagslinje i det nye dokument. Feltet **Udlign fra-varepost** udfyldes ikke, fordi i dette tilfælde, er præcis kostprisudligning ikke muligt. Hvis du f.eks. bruger funktionen **Hent bogførte bilagslinjer, der skal tilbageføres** for at hente en bogført købskreditnotalinje til en ny købskreditnota, er det kun den oprindelige, bogførte kreditnotalinje, der kopieres til den nye kreditnota.  

10. På siden **Købsreturvareordre** i feltet **Returårsagskode** skal du på hver linje vælge årsagen til returneringen.
11. Vælg handlingen **Bogfør**.

## Sådan oprettes en erstatningskøbsodre fra en købsreturvareordre

Der kan være tilfælde, hvor du er blevet enig med en leverandør om, at denne skal kompensere for en købsvare ved at udskifte varen. Udskiftningsvaren kan være samme slags vare eller en anden vare. Sidstnævnte situation kan f.eks. være tilfældet, hvis du har fået leveret en forkert vare.  

1.  På siden **Købsreturvareordre** for en aktiv returproces skal du på en tom linje angive en negativ postering for erstatningsvaren ved at indsætte et negativt beløb i feltet **Antal**.  
2. Vælg handlingen **Flyt negative linjer**.  
3. På siden **Flyt negative købslinjer** skal du udfylde felterne efter behov.
4. Vælg knappen **OK**. Den negative linje slettes fra købsreturvareordren, og der oprettes en ny købsordre. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md).  

## Sådan oprettes et købsnedslag

Hvis du har modtaget varer, som f.eks. er lettere beskadigede, eller det ikke er de helt rigtige varer, tilbyder leverandøren muligvis en dekort eller et nedslag i prisen.  

Du kan bogføre den nedsatte købspris som et varegebyr på en kreditnota eller en returvareordre og knytte den til den bogførte modtagelse. Nedenfor beskrives dette for en købsreturvareordre, men samme fremgangsmåde anvendes ved en købskreditnota.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købskreditnotaer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny** for at åbne en ny tom købskreditnota.  
3. Udfyld kreditnotahovedet med oplysningerne om den leverandør, som har ydet købsnedslaget.  
4. Marker **Gebyr (vare)** i feltet **Type** på oversigtspanelet **Linjer**.  
5. I feltet **Nummer** skal du markere det relevante varegebyrværdi.  

    Du kan oprette et særligt varegebyrnummer, som dækker købsdekorter.  
6. Angiv **1** i feltet **Antal**.  
7. Indtast beløbet på dekorten i feltet **Købspris**.  
8. Tildel købsnedslaget som et varegebyr på varerne i den bogførte leverance. Du kan finde flere oplysninger i [Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md). Vend derefter tilbage til siden **Købskreditnota**, når du har tildelt nedslaget.

Når du bogfører købsreturvareordren, føjes købsnedslaget til den relevante købspost. Det gør det muligt at opretholde en præcis lagerværdi.  

## Sådan samles returvareleverancer

Hvis du ønsker at returnere varer, der er dækket af forskellige købsreturvareorder, for den samme kreditor, skal du bruge funktionen **Saml returvareleverancer**.  

Når du returnerer varerne, bogfører du de relaterede returvareordrer som leveret og dette opretter bogførte købsreturvareleverancer.  

Når du skal fakturere varerne, kan du i stedet for at fakturere hver købsreturvareordre særskilt oprette en købskreditnota og automatisk kopiere de bogførte returvareleverancelinjer til dokumentet. Derefter kan du bogføre købskreditnotaen og spare tid ved at fakturere alle de åbne købsreturvareordrer samtidigt.  

Når returleverancer er samlet på en faktura og bogført, oprettes der en bogført købskreditnota for de fakturerede linjer. Feltet **Faktureret (antal)** på den oprindelige købsreturvareordre opdateres på basis af det fakturerede antal. Dog slettes den oprindelige købsreturordre ikke, selvom den er blevet fuldt modtaget og faktureret, og du skal derfor slette købsreturvareordren manuelt.

> [!NOTE]  
> I følgende procedure antages det, at der er flere købsreturvareordrer på leverandøren, og de er bogført som leveret.     

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købskreditnotaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**.  
4. Vælg handlingen **Hent returvarelev.linjer**.  
5. Vælg de returvareleverancelinjer, der skal indgå i fakturaen.  

    Hvis du har valgt en forkert leverancelinje, eller hvis du vil begynde forfra, kan du bare slette linjerne på købskreditnotaen og så bruge funktionen **Hent returvareleverancelinjer** igen.  
6. Vælg handlingen **Bogfør**.  

### Fjerne åbne købsreturvareordrer efter bogføring af kombineret returvareleverance  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Slet fakturerede købsreturvareordrer**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov, og vælg derefter knappen **OK**.  
3. Du kan også slette de individuelle købsreturvareordrer manuelt.

## Se relateret [Microsoft-træning](/training/paths/return-items-dynamics-365-business-central/)

## Se også
[Køb](purchasing-manage-purchasing.md)  
[Registrere køb](purchasing-how-record-purchases.md)  
[Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
