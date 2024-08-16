---
title: Opret bankindskud
description: 'Du kan foretage indskud for at vedligeholde en transaktionspost, der indeholder oplysninger, som kan anvendes på udestående fakturaer og kreditnotaer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'bank, deposit'
ms.search.form: '10140, 10141, 10143, 10144, 10146, 10147, 10148, 36646'
ms.date: 07/25/2024
ms.custom: bap-template
---

# <a name="create-bank-deposits"></a>Opret bankindskud

> [!NOTE]
> Muligheden for at oprette bankindskud er ny i Business central 2022 udgivelsesbølge 1 til mange lande/område-versioner. Hvis du bruger Business central i USA, Canada eller Mexico før denne udgivelse, bruger du muligvis de tidligere funktioner. Du kan fortsætte, men de nye funktioner erstatter de gamle filer i en fremtidig udgivelse. Hvis du vil begynde at bruge de nye funktioner, der beskrives i denne artikel, kan administratoren gå til siden **Funktionsadministration** og aktivere **Funktionsopdatering: Standardiseret bankafstemning og indskud**.  

Du kan bruge siden **Bankindskud** til at registrere indskud som et enkelt dokument, der bogfører en eller flere poster på en bankkonto. Bankindbetalinger bruges som regel til at registrere indbetalinger. Siden bank indbetalinger er tilgængelige i menuen **Likviditetsstyring** i Rollecenter for virksomhedsleder og i andre rollecentre, der vedrører likviditetsstyring.

Beløb på bankindskud kan komme fra flere forskellige kilder:

* Salg, med en finanskonto til omsætning.
* Kunders betalinger.
* Kontantrefusion af kreditorer eller kontantindbetalinger til dem. 

Bankindbetalingslinjer indeholder oplysninger om individuelle indbetalinger, f. eks. check fra debitorer. Summen af beløbene på linjerne skal lægges sammen til det samlede beløb i indbetalingen.

Når du har udfyldt indbetalingsoplysninger og -linjer, skal du bogføre den. Bogføringen opdaterer de relevante finansposter. Finansposterne omfatter finanskonti og bank-, debitor- og kreditorposter. Bogførte indskud gemmes til senere brug på siden **Bogførte bankindbetalinger**.

rapporten **Bankindbetalinger** viser debitor- og kreditor indskud med det oprindelige indbetalings beløb, det depositumbeløb, der er åbent, og det udlignede beløb. Rapporten viser også det samlede bogførte depositumbeløb, der skal afstemmes.

## <a name="before-you-start"></a>Før du starter

Men, der er et par ting, du skal konfigurere, før du kan bruge bankindskud. Du skal have en nummerserie og kassekladdeskabelon klar. Du skal også angive, om bankindbetalingsbeløb skal bogføres som et engangsbeløb. Det er som summen af alle beløbene på indbetalingslinjerne. Ellers bogføres hver linje som en individuel post. Bogføring af en indbetaling som en enkelt bankpost kan gøre det nemmere at foretage bankafstemninger.

### <a name="number-series-and-lump-sum-deposits"></a>Nummerserie og indskud på engangsbeløb

Du skal oprette en nummerserie til bankindbetalinger og derefter angive serien i feltet **Bankindbetalingsnumre** på **Salgsopsætning**-siden. Du kan finde flere oplysninger om nummerserier under [Oprette nummerserier](ui-create-number-series.md).

På siden **Salgsopsætning** skal bogføre indskud som engangsbeløb i stedet for de enkelte linjer, skal du aktivere **Bogfør bankindskud som engangsbeløb**. Når en indbetaling bogføres som et engangsbeløb, og der oprettes en bankpost for det samlede depositum, kan det være nemmere at foretage bankafstemninger.

### <a name="general-journal-templates-for-bank-deposits"></a>Finanskladdeskabeloner til bankindskud

Du skal også oprette en Finanskladdetype for indskud. Du kan bruge finanskladder til at bogføre transaktioner til finans-, bank-, debitor-, kreditor- og anlægskonti. Kladdetyperne bruges til at designe finanskladden, så den passer til dit arbejde. Det vil sige, at felterne på kladdetypen er netop dem, du har brug for.

Indskud bliver indbetalinger, så det kan være en god ide at genbruge nummerserien til indbetalingskladder. Hvis du har brug for at skelne mellem bankindbetalinger og indbetalingskladdeposter, skal du bruge en anden nummerserie.

Du skal også oprette et batchjob til skabelonen. Hvis du vil oprette et batchjob, skal du vælge **Batchnavne** på siden **Finanskladdetyper**. Du kan få mere at vide om navne ved at gå til [Brug af kladdetyper og -navne](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="dimensions-on-bank-deposit-lines"></a>Dimensioner på bankindbetalingslinjer

Linjerne i bankindbetalingen vil automatisk bruge de standarddimensioner, du har angivet i felterne **Afdelingskode** og **Debitorgruppekode**. Når du vælger **Debitor** eller **Kreditor** i feltet **Kontotype**, vil de dimensioner, der er angivet for debitoren eller kreditoren, erstatte standardindstillingerne. Du kan ændre dimensionerne på linjerne efter behov.

> [!TIP]
> Dimension på linjer angives ifølge standarddimensionsprioriteter. Linjedimensioner tilsidesætter overskriftsdimensioner. For at undgå konflikter kan du oprette regler, der prioriterer, når du skal bruge en dimension, der afhænger af kilden. Hvis du vil ændre den måde, dimensioner prioriteres på, kan du ændre deres niveauer på siden **Standarddimensionsprioriteter**. Du kan finde flere oplysninger i [Konfigurere standarddimensionsprioriteter](finance-dimensions.md#to-set-up-default-dimension-priorities).

## <a name="create-a-bank-deposit"></a>Opret et bankindskud

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankindskud**, og vælg derefter det relaterede link.
2. Vælg **Ny** for at åbne **Bankindbetaling**-siden.
3. Vælg den Finanskladdetype, som du har oprettet til bankindskud.  

    > [!NOTE]
    > Hvis finanskladdetypen indeholder mere end én kladde, bliver du bedt om at vælge en.

4. I feltet **Bankkontonr.** skal du vælge den bankkonto, hvortil du vil foretage bankindskud.

    > [!TIP]
    > Du kan dobbelttjekke, at du indbetaler til den korrekte konto ved hjælp af felterne **Kontokort** og **Kontoposter** for at slå posterne op for den valgte bankkonto. Hvis du f. eks. vil kontrollere, om der er udskrevet tilsvarende indskud på kontoen.

5. I feltet **Samlet indbetalingsbeløb** skal du indtaste det samlede beløb for indbetalingen. Totalen skal være summen af beløbene på alle linjer.
6. Udfyld de resterende felter efter behov. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

    Datoen i **feltet Bogføringsdato** og dimensionerne i felterne **Afdelingskode** og **Debitorgruppekode** knyttes til de linjer, du opretter for bankindbetalingen. Om nødvendigt kan du ændre dem.

7. Afhængigt af om du vil bogføre bank indbetalingen som engangsbeløb eller hver linje til bankposter, skal du aktivere eller deaktivere **Bogføring som engangsbeløb**. Standardindstillingen kommer fra den samme til og fra på siden **Salgsopsætning**.

    > [!NOTE]
    > feltet **Valutakode** angiver den valuta, der er angivet for den bankkonto, du vælger. Du kan ikke vælge en anden valuta.

8. Opret en ny linje for hver indbetaling, du vil betale, i oversigtspanelet **linjer**.
9. Angiv, hvor betalingen stammer fra, i feltet **kontotype**. For bankindbetalinger er typen typisk **Debitor** eller **Kreditor**.

    > [!NOTE]
    > Du kan også registrere en kontant betaling til en kreditor. Det gør du ved at vælge **Kreditor** og derefter angive et betalingsbeløb som et negativt tal i feltet **kreditbeløb** på linjen.

10. Angiv i feltet **Dokumentnr.** det dokumentnummer for fakturaen, som kreditbeløbet stammer fra. Du kan bruge et dokumentnummer til hver linje, eller det samme nummer til alle linjer.

    > [!TIP]
    > Det er som regel ikke nødvendigt at udfylde feltet **Dokumenttype** for finansposter. Hvis du f. eks. deponerer kontanter fra en dags salg, skal du lade feltet være tomt. Hvis du deponerer kontanter fra en debitorbetaling, skal du vælge **betaling**.

11. Hvis du deponerer en kontant betaling for en bestemt debitorfaktura, skal du vælge handlingen **Udlign poster** og derefter indtaste fakturanummeret i feltet **Udlignings-id**.
12. Hvis du er klar til at bogføre bank indbetalingen, skal du vælge handlingen **Bogfør**.

    > [!TIP]
    > Før du bogfører, kan du vælge handlingen **Kontrollér rapport** for at gennemse data. Rapporten viser, om der er problemer, f. eks. manglende data, som vil forhindre bogføring.  

## <a name="find-posted-bank-deposits"></a>Find bogførte bankindskud

På siden **Bogførte bankindbetalinger** vises firmaets forrige indskud. På listen kan du gennemse de bemærkninger og dimensioner, der er angivet for indbetalingerne. Du kan åbne bank indbetalingen for at få vist flere detaljer, og derfra kan du undersøge dette. Du kan f. eks. vælge handlingen **Find poster** for at få vist de bogførte Bankposter. Fra bankposten kan du finde den tilhørende bogførte finanspost.

Hvis du vil slå alle finansposter for de bogførte indbetalingslinjer op, skal du gå til siden **Finansjournal** og bruge handlingen **Finans**. Her finder du alle finansposter, inklusive debitorer og kreditorer.

## <a name="reverse-a-posted-bank-deposit"></a>Tilbageføre en bogført bankindbetaling

Du kan tilbageføre en bogført bankindbetaling på flere måder:

* Vælg indbetalingen på siden **Bogførte bankindskud**, og vælg derefter handlingen **Annuller bogføring** .
* Hvis du vil tilbageføre en bogført indbetaling, skal du gå til siden **Finansjournaler**, finde kasseapparatet og derefter vælge handlingen **Tilbagefør Journal**.

> [!NOTE]
> Du kan kun tilbageføre en Journal, der indeholder en enkelt posttype. Det vil sige, at journalen kun skal indeholde debitorposter eller kreditorposter, men ikke begge dele. Hvis der er indsat et kasseapparat, skal du manuelt tilbageføre indbetalingen.

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Konfigurere Finans](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]



