---
title: Udligne betalinger til ubetalte salgsdokumenter
description: 'Du kan udligne beløb, der er betalt af debitorer, til relaterede salgsdokumenter og bogføre betalingen for at opdatere debitor-, finans- og bankposter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts, customer payment'
ms.search.form: '1290, 1294, 1287'
ms.date: 07/08/2024
ms.service: dynamics-365-business-central
---

# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents"></a>Afstemme debitorbetalinger på en liste over ubetalte salgsdokumenter

Når kunderne foretager elektroniske betalinger til din bankkonto, skal du gøre følgende:

* Udlign hver betaling på det relevante bogførte salgsdokument.
* Bogfør betalingen for at opdatere kunden, finanskonto og bankposter.

Afhængigt af dine forretningsmæssige behov kan du registrere betalinger manuelt, automatisk og gennem betalingstjenester.  

> [!NOTE]  
> Du kan udføre de samme opgaver, herunder kreditorbetalinger, på siden **Betalingsudligningskladde** . Du kan f.eks. indlæse bankkontoudtog, bruge automatisk udligning og afstemme bankkonti. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).

Brug siden **Registrer debitorbetalinger** til at balancere interne konti med faktiske kontant tal for at sikre, at betalingerne opsamles. Du kan hurtigt kontrollere og bogføre individuelle betalinger, forbehandle indbetalinger og finde dokumenter, der ikke er betalt.

Du skal bogføre betalinger til forskellige debitorer, der har forskellige betalingsdatoer, som individuelle betalinger. Betalinger til den samme debitor, som har den samme betalingsdato, kan bogføres som en engangsbetaling. Engangsbetalinger er nyttige, når en debitor f.eks. foretog en enkelt betaling, der dækker flere salgsfakturaer.

## <a name="to-set-up-the-payment-registration-journal"></a>Sådan konfigurerer du betalingsregistreringskladden

Fordi du kan bogføre forskellige typer betaling til forskellige modkonti, skal du vælge en modkonto på siden **Opsætning af betalingsregistrering**, før du starte behandlingen af debitorbetalinger. Hvis du altid bogfører på den samme modkonto, kan du angive den pågældende konto som standard og undgå dette trin, hver gang du åbner siden **Registrer debitorbetalinger**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af betalingsregistrering**, og vælg derefter det relaterede link. Du kan også vælge handlingen **Opsætning** på siden **Registrer debitorbetalinger**.
2. Udfyld felterne på siden **Opsætning af betalingsregistrering**. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)].  

> [!TIP]
> Hvis du vil gøre det nemmere senere at identificere poster, der blev bogført via kladden, kan du tildele en bestemt nummerserie til betalingskladden. Nummerserien er nyttig, hvis du bruger betalingsafstemningskladder til at registrere og anvende betalinger.

## <a name="to-register-customer-payments-individually"></a>Sådan registrerer du debitorbetalinger individuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Registrer debitorbetalinger**, og vælg derefter det relaterede link.  

    Siden **Registrer debitorbetalinger** viser alle bogførte dokumenter, som en betaling kan registreres for. Du kan også åbne siden fra siderne **Debitorer** og **Debitorkort**, hvor den filtreres for den angivne kunde.  
2. Marker afkrydsningsfeltet **Betaling foretaget** på den linje, der repræsenterer det bogførte bilag, hvortil der blev foretaget en betaling.
3. I feltet **Dato for modtaget** kan du indtaste den dato, hvor betalingen blev foretaget. Denne dato kan være forskellig fra arbejdsdatoen.  

   Hvis afkrydsningsfeltet **Udfyld Dato for modtaget automatisk** er markeret på siden **Opsætning af betalingsregistrering**, indeholder feltet **Dato for modtaget** arbejdsdatoen.  
4. Indtast det beløb, der blev betalt, i feltet **Beløb modtaget**.

    Ved fuld betaling er dette beløb det samme som beløbet i feltet **Restbeløb** på linjen. Ved delvise betalinger er dette beløb lavere end beløbet i feltet **Restbeløb** på linjen.
5. Gentag trin 2-4 for andre linjer for bogførte bilag, hvortil der er foretaget betalinger.  
6. Vælg handlingen **Bogfør betalinger**.  

De angivne betalingsoplysninger bogføres for bilag på linjer, hvor afkrydsningsfeltet **Betaling foretaget** er markeret. Betalingsposter bogføres til finans, bank og debitorkonti.

## <a name="to-reconcile-lump-sum-payments"></a>Sådan afstemmer du engangsbetalinger

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Registrer debitorbetalinger**, og vælg derefter det relaterede link.
2. Marker afkrydsningsfeltet **Betaling foretaget** på linjerne for bogførte bilag til den samme debitor, og som engangsbeløbet blev betalt til.  

    > [!NOTE]  
    > Debitoren i feltet **Navn** skal være den samme i alle linjer, der skal medtages i engangsbetalingen.  

    Hvis afkrydsningsfeltet **Udfyld Dato for modtaget automatisk** er markeret på siden **Opsætning af betalingsregistrering**, indeholder feltet **Dato for modtaget** arbejdsdatoen.  
3. I feltet **Dato for modtaget** kan du indtaste den dato, hvor betalingen blev foretaget. Denne dato kan være forskellig fra arbejdsdatoen.  

    > [!NOTE]  
    > Denne dato skal være ens på alle linjer, der skal bogføres som engangsbetaling.  
4. I feltet **Beløb modtaget** kan du indtaste beløb på flere linjer, der i alt er lig med engangsbetalingsbeløbet.  

    > [!TIP]  
    > Prøv at bogføre så mange fulde betalinger som muligt med engangsbeløbet. Indtast beløb, der er det samme som beløbet i feltet **Restbeløb** på så mange linjer som muligt.  
5. Gentag trin 2-4 for andre linjer, der repræsenterer bogførte dokumenter for den samme debitor, hvortil der blev foretaget en engangsbetaling.  
6. Vælg handlingen **Bogfør som engangsbetaling**.

   De angivne betalingsoplysninger bogføres for bilag på linjer, hvor afkrydsningsfeltet **Betaling foretaget** er markeret. Betalingsposter bogføres til finans, bank og debitorkonti. Hver betaling anvendes på det relevante bogførte salgsdokument.  

Hvis en betaling i banken ikke repræsenteres af en linje på siden **Registrer debitorbetalinger**, kan det muligvis skyldes, at det relaterede bilag ikke er bogført. I dette tilfælde kan du bruge en søgefunktion til hurtigt at finde bilaget og bogføre det for at behandle betalingen. Du kan finde flere oplysninger i [Sådan finder du et bestemt salgsdokument, der ikke er fuldt faktureret](#to-find-a-specific-sales-document-that-isnt-fully-invoiced).  

Hvis en betaling i banken ikke repræsenteres af nogen bilag, kan du åbne en finanskladdelinje, som er udfyldt på forhånd, på siden **Registrer debitorbetalinger** for at bogføre betalingen direkte på modkontoen uden at knytte betalingen til et bilag. Du kan også registrere betalingen i kladden, indtil den betalingens oprindelse er blevet løst. Du kan finde flere oplysninger i [Sådan registrerer eller bogfører du en betaling uden et relateret dokument](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Sådan behandler du debitorbetalinger med rabatter manuelt

Hvis du accepterer en kontantrabat med debitoren, kan de indbetalte beløb være mindre end fakturabeløbene, hvis betalingen finder sted inden den aftalte rabatdato.  

I følgende fremgangsmåder beskrives måder til at bogføre fratrukne betalinger på siden **Betalingsregistrering**.  

* Det indbetalte beløb er lig med det resterende beløb, og betalingsdatoen ligger før rabatdatoen. Du bogfører betalingen, som den er.  
* Det indbetalte beløb er lig med det resterende fratrukne beløb, men betalingsdatoen ligger efter rabatdatoen. Du bogfører betalingen delvis. Bilaget forbliver åbent, så restbeløbet kan opkræves/betales. Du kan også angive rabatdatoen til at tillade fuld betaling.  
* Betalingsbeløbet er lavere end det resterende fratrukne beløb. Du bogfører betalingen delvis. Bilaget forbliver åbent, så restbeløbet kan opkræves/betales.  
* Betalingsbeløbet er højere end det resterende fratrukne beløb. Du bogfører betalingerne, som de er. Kun det resterende beløb bogføres. Det ekstra beløb krediteres til debitoren.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Sådan behandler du et betalingsbeløb, der er lig med det fratrukne beløb, og hvor betalingsdatoen ligger før rabatdatoen

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Registrer debitorbetalinger**, og vælg derefter det relaterede link.  
2. Angiv betalingsbeløbet i feltet **Beløb modtaget**. Beløbet er lig med beløbet i feltet **Restbeløb inkl. rabat**.

    Afkrydsningsfeltet **Betaling foretaget** markeres automatisk, og feltet **Dato for modtaget** udfyldes med arbejdsdatoen.
3. Angiv betalingsdatoen i feltet **Dato for modtaget**. Datoen er inden datoen i feltet **Kont.rabatdato**.
4. Kontrollér, at feltet **Restbeløb** indeholder et nul (0).  
5. Vælg handlingen **Bogfør betalinger** for at bogføre hele betalingen til finans-, bank- og debitorkonti.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Sådan behandler du et betalingsbeløb, der er lig med det fratrukne beløb, men hvor betalingsdatoen ligger efter rabatdatoen

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Registrer debitorbetalinger**, og vælg derefter det relaterede link.  
2. Angiv betalingsbeløbet i feltet **Beløb modtaget**. Beløbet er lig med beløbet i feltet **Restbeløb inkl. rabat**.

    Afkrydsningsfeltet **Betaling foretaget** markeres automatisk, og feltet **Dato for modtaget** udfyldes med arbejdsdatoen.
3. I feltet **Dato for modtaget** kan du indtaste en betalingsdato, som ligger efter datoen i feltet **Kont.rabatdato**.

   Datofelter ændres til rød skrift, og en fejlmeddelelse vises nederst på siden. De næste to trin løser det.
4. Vælg handlingen **Detaljer**.  
5.  **Angiv en dato efter**  **·**  **datoen i feltet Kont.rabatdato** i **oversigtspanelet** Betalingsrabat **på siden Oplysninger om betalingsregistrering.**   

    Fejlmeddelelsen og den røde skrift forsvinder, og du kan fortsætte med at behandle den fratrukne betaling.
6. Kontrollér, at feltet **Restbeløb** indeholder det beløb, der resterer, før det fulde fakturabeløb er betalt.  
7. Vælg handlingen **Bogfør betalinger** for at bogføre delbetalingen til finans-, bank- og debitorkonti.  

Det relaterede bilag forbliver åbent.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Sådan behandler du en betaling, der er lavere end det resterende fratrukne beløb

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Registrer debitorbetalinger**, og vælg derefter det relaterede link.  
2. Angiv betalingsbeløbet i feltet **Beløb modtaget**. Beløbet er lavere end beløbet i feltet **Restbeløb inkl. rabat**.

    Afkrydsningsfeltet **Betaling foretaget** markeres automatisk, og feltet **Dato for modtaget** udfyldes med arbejdsdatoen.  
3. Angiv betalingsdatoen i feltet **Dato for modtaget**. Datoen er inden datoen i feltet **Kont.rabatdato**.
4. Kontrollér, at feltet **Restbeløb** indeholder det beløb, der resterer, før rabatbeløbet er betalt.  
5. Vælg handlingen **Bogfør betalinger** for at bogføre delbetalingen til finans-, bank- og debitorkonti.  

Det relaterede bilag forbliver åbent.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Sådan behandler du en betaling, der er højere end det resterende fratrukne beløb

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Registrer debitorbetalinger**, og vælg derefter det relaterede link.  
2. Angiv betalingsbeløbet i feltet **Beløb modtaget**. Beløbet er højere end beløbet i feltet **Restbeløb inkl. rabat**.  

    Afkrydsningsfeltet **Betaling foretaget** markeres automatisk, og feltet **Dato for modtaget** udfyldes med arbejdsdatoen.
3. Angiv betalingsdatoen i feltet **Dato for modtaget**. Datoen er inden datoen i feltet **Kont.rabatdato**.
4. Kontrollér, at feltet **Restbeløb** indeholder et nul (0).  
5. Vælg handlingen **Bogfør betalinger** for at bogføre hele betalingen til finans-, bank- og debitorkonti.  

Det relaterede bilag er lukket, og debitoren krediteres det overskydende betalingsbeløb.  

## <a name="to-find-a-specific-sales-document-that-isnt-fully-invoiced"></a>Sådan finder du et bestemt salgsdokument, der ikke er fuldt faktureret

Siden **Registrer debitorbetalinger** understøtter dig i opgaver, der er nødvendige for at afstemme interne konti med aktuelle tal for at sikre effektiv opkrævning fra debitorer. Den viser udestående indgående betalinger som linjer, der repræsenterer salgsdokumenter, hvor et beløb er forfaldent til betaling.  

Når der foretages en betaling, som registreres i banken eller på anden måde, vises salgs- eller købsdokumentet typisk som en linje på siden **Registrer debitorbetalinger** . Dokumentet venter på, at du bogfører betalingen på det udestående beløb. Ind imellem blev der dog en udført betaling, som ikke repræsenteres af en linje på siden **Registrer debitorbetalinger**, typisk fordi det pågældende bilag ikke er fuldt faktureret.

Brug handlingen **Søg i dokumenter** til at søge efter bilag, der ikke er fuldt faktureret. Du kan søge baseret på et eller flere af følgende kriterier:  

* Bilagsnr.  
* Beløb eller beløbområde  

Den følgende procedure beskriver, hvordan du finder et bestemt dokument ved at bruge begge søgekriterier.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Registrer debitorbetalinger**, og vælg derefter det relaterede link.
2. Placer markøren på en linje, og vælg handlingen **Søg i dokumenter**.
3. På siden **Dokumentsøgning** skal du indtaste en værdi i feltet **Dokumentnr.**.  

    > [!NOTE]  
    > Den værdi, du indtaster i dette felt, er omsluttet af skjulte jokertegn. Dette betyder, at handlingen søger efter alle dokumentnumre, der indeholder den angivne værdi.
4. I feltet **Beløb** skal du indtaste det specifikke beløb på det bilag, du ønsker at finde.  
5. I feltet **Tolerancebeløb %** skal du angive en procentværdi for at angive det beløbsinterval, som du vil søge i, for at finde det åbne bilag.  

    Hvis du indtaster 10, søges der efter beløb i et interval på plus eller minus 10 procent af værdien i feltet **Beløb** .
6. Vælg handlingen **Søg**.  

Hvis et eller flere bilag matcher kriterierne, åbnes siden **Resultat af dokumentsøgning** for at vise linjer, der repræsenterer disse bilag. Hver linje indeholder et bilagsnummer, en beskrivelse og et beløb.

Hvis en betaling i banken ikke repræsenteres af nogen bilag, kan du åbne en finanskladdelinje, som er udfyldt på forhånd, på siden **Registrer debitorbetalinger** for at bogføre betalingen direkte på modkontoen uden at knytte betalingen til et bilag. Du kan også registrere betalingen i kladden, indtil den betalingens oprindelse er blevet løst.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Sådan registrerer eller bogfører du en betaling uden et relateret dokument

Hvis en betaling i banken ikke er repræsenteret af et dokument, kan du bruge handlingen **Finanskladde** til at åbne en forudfyldt finanskladdelinje fra siden **Registrer debitorbetalinger** . Bruge kladden til at bogføre betalingen direkte på modkontoen uden at udligne betalingen med et bilag. Du kan også registrere betalingen i kladden, indtil den betalingens oprindelse er blevet løst.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Registrer debitorbetalinger**, og vælg derefter det relaterede link.
2. Vælg handlingen **Finanskladde**.  

    Siden **Finanskladde** åbnes med en linje med, der er udfyldt på forhånd med modkontoen for den kladde, der er konfigureret på siden **Opsætning af betalingsregistrering**.  
3. Udfyld resten af felterne på finanskladdelinjen. Du kan f. eks. angive beløb, kundenummer eller oplysninger fra bankens kontoudtog. Du kan finde flere oplysninger i [Bogføre transaktioner direkte i finansregnskabet](finance-how-post-transactions-directly.md).  

Du kan bogføre kladdelinjen for at opdatere det samlede beløb på modkontoen. Du kan også lade kladdelinjen være ikke-bogført og måske knytte den til en note, om at betalingen skal bruge flere analyser.  

Hvis du ikke bogfører kladdelinjen, føjes værdien til værdien i feltet **Restbeløb inkl. rabat** på siden **Betalingsregistrering** .  

## <a name="see-also"></a>Se også

[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
