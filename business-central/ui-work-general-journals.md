---
title: 'Arbejde med finanskladder, der skal bogføres direkte til Finans'
description: 'Lær, hvordan du kan bruge kladder til at bogføre økonomisk transaktioner på finanskonti og andre konti, f.eks. bank- og kreditorkonti.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/27/2022
ms.custom: bap-template
ms.search.keywords: 'journals, recurring, accrual, renumber, bulk-post'
ms.search.form: '39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022'
---
# <a name="work-with-general-journals"></a><a name="work-with-general-journals"></a>Arbejde med finanskladder

De fleste finansposteringer bogføres i finansregnskabet ved hjælp af dokumenter, f.eks. købsfakturaer og salgsordrer. Du kan dog også behandle forretningsaktiviteter som f. eks.:

* Indkøb
* Udbetaling kladde
* Bruge gentagelseskladder til at bogføre periodiseringer
* Genfinansiere medarbejderudgifter ved at bogføre kladdelinjer i kladder  

De fleste kladder er baseret på finanskladde, og du kan behandle alle transaktioner på siden **Finanskladde**. Flere oplysninger i [Bogføre transaktioner direkte i finansposterne](finance-how-post-transactions-directly.md).  

Du kan f. eks. bruge medarbejderudgifter i forbindelse med refusion. Flere oplysninger i [Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md).

Men [!INCLUDE [prod_short](includes/prod_short.md)] tilbyder også de kladder, der er optimeret til bestemte typer transaktioner, som **Udbetalingskladde** for at registrere betalinger. Du kan finde flere oplysninger i [Registrere indbetalinger og refusioner i udbetalingskladden](payables-how-post-payments-refunds.md).  

Du kan bruge finanskladder til at bogføre finanstransaktioner til finanskonti og andre konti. De andre konti omfatter bank-, debitor-, kreditor-og medarbejderkonti. Når du bogfører en finanskladde, oprettes der poster på finanskonti, selvom du f. eks. bogfører en kladdelinje til en debitorkonto. Posten bogføres på en finanskonto via en bogføringsgruppe.

De oplysninger, du angiver i en kladde, er midlertidige og kan ændres, mens de er i kladden. Når du bogfører kladden, overføres oplysningerne til poster på individuelle konti, hvor de ikke kan ændres. Du kan imidlertid annullere udligningen af bogførte poster, og du kan bogføre tilbageførsels- eller rettelsesposter. Flere oplysninger i [Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="use-journal-templates-and-batches"></a><a name="use-journal-templates-and-batches"></a>Bruge kladdeskabeloner og -batches

Der er forskellige finanskladdetyper. Hver kladdetype er repræsenteret af en dedikeret side med bestemte funktioner og de felter, der kræves for at understøtte disse funktioner, f.eks. vinduet **Betalingsudligningskladde** til behandling af bankbetalinger og siden **Udbetalingskladde** til betaling af kreditorer eller refusion af medarbejdere. Du kan finde flere oplysninger i [Foretage indbetalinger](payables-make-payments.md) og [Afstemme betalinger fra debitorer med indbetalingskladden eller fra debitorposter](receivables-how-apply-sales-transactions-manually.md).

For hver kladdetype kan du angive din egen private kladde som kladdenavn. F.eks. kan du angive din egen kladdetype som udbetalingskladden med dit personlige layout og dine indstillinger. Følgende tip er et eksempel på, hvordan du kan tilpasse en kladde.

> [!TIP]  
> Hvis du markerer afkrydsningsfeltet **Foreslå modkontobeløb** på linjen for dit kladdenavn på siden **Finanskladdenavne**, udfyldes feltet **Beløb** på f.eks. finanskladdelinjer for samme bilagsnummer automatisk med den værdi, der er nødvendig for at afstemme dokumentet. Få mere at vide i [Lade [!INCLUDE[prod_short](includes/prod_short.md)] foreslå værdier](ui-let-system-suggest-values.md).

> [!TIP]
> Du kan tilføje eller fjerne felter i kladder ved at tilpasse dem. Flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

### <a name="validating-general-journal-batches"></a><a name="validating-general-journal-batches"></a>validering af Finanskladdenavne

Du kan aktivere en baggrundskontrol, som medvirker til at forhindre forsinkelser ved bogføring. Checken giver dig besked, når en fejl i den finanskladde, som du arbejder i, ikke kan bogføre kladden. På siden **Finanskladdenavn** kan du vælge **Baggrundsfejlkontrol** for at [!INCLUDE[prod_short](includes/prod_short.md)] validerer finanskladder som f.eks. generelle eller udbetalingskladder, mens du arbejder på dem.

Når du aktiverer valideringen, viser faktaboksen **Kladdekontrol** problemer på den aktuelle linje og på hele kørslen. Validering sker, når du indlæser et Finanskladdenavn, og når du vælger en anden kladdelinje. Det **samlede antal problemer** i faktaboksen viser det samlede antal problemer, som [!INCLUDE[prod_short](includes/prod_short.md)] har fundet, og du kan vælge den for at åbne en oversigt over problemerne.

Du kan bruge handlingerne **Vis linjer med problemer** og **Vis alle linjer** til at skifte mellem de kladdelinjer, der har eller ikke har problemer. Faktaboksen med de nye **kladdelinjedetaljer** giver hurtig oversigt og adgang til data fra kladdelinjer, f.eks. finanskonto, debitor eller kreditor, samt bogføringsopsætning for specifikke konti.

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]  

## <a name="understanding-main-accounts-and-balancing-accounts"></a><a name="understanding-main-accounts-and-balancing-accounts"></a>Om hovedkonti og modkonti

Hvis du har oprettet modkonti for kladdenavnene, udfyldes modkontoen automatisk på siden **Finanskladder**, når du udfylder feltet **Kontonr.**. Hvis ikke, skal du udfylde både feltet **Kontonr.** og feltet **Modkontonr.** manuelt. Et positivt beløb i feltet **Beløb** debiteres på hovedkontoen og krediteres på modkontoen. Et negativt beløb krediteres på hovedkontoen og debiteres på modkontoen.

> [!NOTE]  
> Moms beregnes separat for hovedkontoen og modkontoen, så der kan bruges forskellige momsprocentsatser.

## <a name="work-with-recurring-journals"></a><a name="work-with-recurring-journals"></a>Arbejde med gentagelseskladder

En gentagelseskladde er en finanskladde med særlige felter til styring af transaktioner, som bogføres ofte med få eller ingen ændringer. F.eks. transaktioner for udgifter som f. eks. husleje, abonnementer, elektricitet og varme. Du kan bruge gentagelseskladder til at bogføre faste og variable beløb og angive automatisk tilbageførte poster for dagen efter bogføringsdatoen. Med fordelingsnøgler kan du opdele de gentagne poster mellem forskellige konti. Flere oplysninger i [Tildeling af tilbagevendende kladdebeløb til flere konti](#allocating-recurring-journal-amounts-to-several-accounts).

Med gentagelseskladder kan du oprette de poster, der bogføres regelmæssigt, én gang. F.eks. bliver de konti, dimensioner og dimensionsværdier og så videre, du indtaster i felterne, i kladden efter bogføringen. Hvis det er nødvendigt at foretage ændringer, kan du gøre det, hver gang du bogfører.

### <a name="recurring-method-field"></a><a name="recurring-method-field"></a>Feltet Gentagelsesmetode

Feltet **Gentagelsesmetode** er vigtigt. Dette felt bestemmer, hvordan beløbet på kladdelinjen bliver behandlet efter bogføringen. Hvis du f.eks. bogfører det samme beløb, hver gang du bogfører linjen, kan du vælge at lade beløbet stå. Eller du kan vælge at lade det slette, fordi konti og tekst i linjen kan genbruges ved hver bogføring, men beløbet hver gang varierer.

| Hvis du vil | Skal du se |
| --- | --- |
|F Fast|Beløbet på kladdelinjen vil blive stående i posten efter bogføring.|
|V Variabel|Beløbet på kladdelinjen slettes efter bogføring.|
|B Saldo|Det bogførte beløb på kontoen på linjen bliver fordelt mellem de konti, der er defineret for linjen i tabellen Fordeling. Saldoen på kontoen bliver derfor angivet til nul. Husk at udfylde feltet **Fordelingspct.** på siden **Fordelinger**. Du kan finde yderligere oplysninger i [Fordeling af gentagelsesposter på flere konti](#allocating-recurring-journal-amounts-to-several-accounts).|
|RF Fast tilbageførsel|Beløbet i kladdelinjen bliver stående på linjen efter bogføringen, og der bliver bogført en modpost den følgende dag.|
|RV Variabel til tilbageførsel|Beløbet i kladdelinjen bliver slettet efter bogføringen, og der bliver bogført en modpost den følgende dag.|
|RB Saldo til tilbageførsel|Det bogførte beløb på kontoen på linjen bliver fordelt mellem de konti, der er defineret for linjen på siden **Fordelinger**. Saldoen på kontoen angives til nul, og der posteres en modpost den følgende dag.|
|BD Saldo efter dimension|Kladdelinjen tildeler omkostninger, der er baseret på finanskontoens saldo pr. dimension. Du bliver bedt om at angive, hvilke dimensionsfiltre der skal bruges til at beregne finanskontoens saldo efter dimension, hvorfra der skal allokeres omkostninger. Du kan også vælge handlingen **Angiv dimensionsfiltre** senere.|
|RBD Tilbageført saldo pr. dimension|Kladdelinjen tildeler omkostninger, der er baseret på finanskontoens saldo med tilbageføring pr. dimension. Du bliver bedt om at angive, hvilke dimensionsfiltre der skal bruges til at beregne finanskontoens saldo efter dimension, hvorfra der skal allokeres omkostninger. Du kan også vælge handlingen **Angiv dimensionsfiltre** senere.|

> [!NOTE]  
> Momsfelter kan kun være udfyldt på gentagelseskladdelinjen eller på allokeringkladdelinjen. Det vil sige, at dette felt kun kan udfyldes på siden **Fordelinger**, hvis det tilsvarende felt på gentagelseskladden ikke er udfyldt.

### <a name="recurring-frequency-field"></a><a name="recurring-frequency-field"></a>Feltet Gentagelsesinterval

Dette datoformel angiver, hvor ofte posten på kladdelinjen skal bogføres, og det skal udfyldes. Flere oplysninger i [Bruge datoformler](ui-enter-date-ranges.md#use-date-formulas).

#### <a name="examples"></a><a name="examples"></a>Eksempler

Hvis kladdelinjen skal bogføres hver måned, skal du angive "1M". Efter hver bogføring bliver datoen i feltet **Bogføringsdato** opdateret til samme dato i den efterfølgende måned.

Hvis du vil bogføre en post den sidste dag i hver måned, kan du vælge én af følgende muligheder:

* Bogfør den første post på den sidste dag i måneden ved at indtaste 1D+1M-1D (dvs. 1 dag plus 1 måned minus 1 dag). Med denne formel beregnes posteringsdatoen korrekt, uanset antallet af dage i måneden.

* Bogfør den første post på en hvilken som helst dag i en måned ved at indtaste 1M+LM. Med denne formel vil posteringsdatoen være efter én hel måned plus de resterende dage i den indeværende måned.

### <a name="expiration-date-field"></a><a name="expiration-date-field"></a>Feltet Udløbsdato

Dette felt bestemmer, på hvilken dato kladdelinjen bliver bogført for sidste gang. Linjen bogføres ikke efter denne dato.

Fordelen ved at bruge feltet Udløbsdato er, at linjen ikke slettes fra kladden med det samme. Du kan angive en senere dato, så du kan bruge linjen i fremtiden.

Hvis feltet er tomt, bogføres linjen, hver gang du bogfører, indtil den slettes fra kladden.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a><a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Tildeling af tilbagevendende kladdebeløb til flere konti

På siden **Finansgentagelseskladde**, kan du vælge handlingen **Fordelinger** for at se eller styre, hvordan beløbene i gentagelseskladdelinjen fordeles på flere konti og dimensioner. Fordelinger fungerer som en modkontolinje til gentagelseskladdelinjen.

På samme måde som med en gentagelseskladde kan du angive en allokering én gang, og den forbliver i fordelingskladden efter bogføringen. Du behøver ikke at angive beløb og allokeringer, hver gang du bogfører gentagelseskladdelinjen.

Hvis gentagelsesmetoden i gentagelseskladden er sat til **Saldo** eller **Saldo med tilbageføring**, bliver der ikke taget hensyn til dimensionsværdikoder i gentagelseskladden, når kontoen nulstilles. Hvis du fordeler en gentagelseslinje på forskellige globale dimensionsværdier på siden **Fordelinger**, så vil der kun blive lavet en tilbageførselspost.

> [!NOTE]
> Hvis du fordeler en gentagelseskladdelinje, som indeholder en dimensionsværdikode, må du ikke indtaste den samme kode på siden **Fordelinger**. Hvis du gør det, vil dimensionsværdierne ikke blive korrekte.  

Hvis du vil fordele tilbagevendende kladdebeløb baseret på dimensioner, skal du i stedet angive feltet **Gentagelsesmetode** til **Balancere efter dimension** eller **Tilbageført saldo pr. dimension**. Hvis gentagelsesmetoden i gentagelseskladden er sat til **Saldo efter dimension** eller **Tilbageført saldo pr. dimension**, bliver der ikke taget hensyn til eventuelle dimensionsværdikoder i gentagelseskladden, når kontoen nulstilles. Hvis du allokerer en gentagelses linje til forskellige dimensionsværdier på siden **Fordelinger**, oprettes der tilbageførte poster, der svarer til det antal kombinationer af dimensionsværdier, som saldoen består af. Hvis du allokerer kontosaldo via en gentagelseskladde, der indeholder en dimensionsværdikode, skal du huske at bruge **Saldo efter dimension** eller **Tilbageført saldo pr. dimension** for at sikre, at dimensionsværdierne er korrekt afstemt eller tilbageført fra kildekontoen.  

Din virksomhed har f.eks. nogle forretningsenheder og en hånd af afdelinger, som dine controllere har sat op som dimensioner. For at gøre købsordre processen hurtigere skal du beslutte, om du vil kræve, at kreditorassistenten kun indtaster dimensionerne for koncernvirksomheden. Da hver koncernvirksomhed har specifikke allokeringsnøgler for dimensionen afdeling, f.eks. baseret på antallet af medarbejdere, kan du bruge gentagelsesmetoderne **BD Saldo efter dimension** eller **RBD Tilbageført saldo pr. dimension** til at genfordele omkostningerne for hver koncernvirksomhed til de rigtige afdelinger på grundlag af fordelingsnøglerne.  

> [!NOTE]
> Dimensioner, som du angiver på fordelingslinjer, beregnes ikke automatisk, og du skal angive, hvilke dimensionsværdier der skal angives på fordelingskontiene. Hvis du vil bevare tilknytningen mellem dimensionen kildekonto og allokerings kontodimensionen, anbefales det, at du bruger funktionen til [Omkostningsberegning](finance-about-cost-accounting.md) i stedet.

#### <a name="example-allocating-rent-payments-to-different-departments"></a><a name="example-allocating-rent-payments-to-different-departments"></a>Eksempel: Fordeling af huslejebetalinger til forskellige afdelinger

Du betaler månedlig husleje, så du har indtastet huslejen i indbetalingskonto på en gentagelseskladdelinje. På siden **Fordelinger** kan du bruge afdelingsdimensionen til at opdele udgiften på flere afdelinger. Afhængigt af det antal kvadratmeter, som hver afdeling optager. Beregningen er baseret på allokeringsprocenten på hver linje. Du kan fordele dem på forskellige måder:

* Angive forskellige konti på forskellige fordelingslinjer for at opdele udlejnings udgifter mellem flere konti.
* Angiv den samme konto, men brug forskellige dimensionsværdikoder til Afdelingsdimensionen på hver linje.

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

### <a name="calculate-the-reversal-date"></a><a name="calculate-the-reversal-date"></a>Beregne annulleringsdatoen

Når du bruger gentagelseskladder til at bogføre periodiseringer i slutningen af en periode, er det vigtigt, at du har fuld kontrol over de tilbageførte poster. På siden **Gentagelseskladder** kan du i feltet **Tilbagefør datoberegning** styre den dato, hvor de tilbageførte poster skal bogføres, når der bruges tilbagevendende gentagelsesmetoder.

#### <a name="example"></a><a name="example"></a>Eksempel

Periodiseringer bogføres typisk med gentagende **Faste**, **Variable** eller **Saldo** metoder på kladdelinjen. Bogføringsdatoen for det bogførte beløb på kontoen på kladdelinjen beregnes vha. gentagelsesinterval. Bogføringsdatoen for modposten beregnes ved hjælp af feltet **Tilbagefør datoberegning** følgende måde:

* Hvis feltet er tomt, bogføres modposten efterfølgende dag.
* Hvis feltet indeholder en datoformel (f.eks. **5D** for fem dage), vil modposten blive bogført med en bogføringsdato, der er beregnet vha. beregningen af annulleringsdatoen.

> [!NOTE]
> Som standard er feltet **Tilbagefør datoberegning** ikke tilgængeligt på siden **Tilbagevendende finanskladder**. Hvis du vil bruge feltet, skal du tilføje det ved at tilpasse siden. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

## <a name="work-with-standard-journals"></a><a name="work-with-standard-journals"></a>Arbejde med standardkladder

Når du har oprettet kladdelinjer, som du ved, at du sandsynligvis skal oprette igen senere, kan du gemme dem som en standardkladde, inden du bogfører kladden. Det samme gælder for varekladder og finanskladder.

> [!NOTE]
> Standardkladderne indeholder muligvis ikke alle de felter, du vil medtage i de oprettede poster. Hvis du f. eks. bruger en standard kassekladde til at registrere en betaling, indeholder posterne ikke feltet Betalingsformskode.

> [!NOTE]  
> Følgende procedure beskriver varekladden, men oplysningerne gælder også for finanskladden.

### <a name="to-save-a-standard-journal"></a><a name="to-save-a-standard-journal"></a>Sådan gemmes en standardkladde

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varekladder**, og vælg derefter det relaterede link.
2. Indsæt en eller flere kladdelinjer.
3. Vælg de kladdelinjer, der skal genbruges.
4. Vælg handlingen **Gem som standardkladde**.
5. På siden **Gem som standardvarekladde** skal du definere en ny eller eksisterende standardvarekladde, som linjerne skal gemmes i.

    Hvis du allerede har oprettet en eller flere standardvarekladder og vil erstatte en af dem med det nye sæt varekladdelinjer, skal du vælge den varakladden i feltet **Kode**.
6. Vælg **OK** for at bekræfte, at du vil erstatte indholdet af den eksisterende standardvarekladde.
7. Hvis du vil gemme værdierne i feltet **Pris** for standardvarekladden, skal du vælge feltet **Gem pris**.
8. Hvis du vil gemme værdierne i feltet **Antal**, skal du vælge feltet **Gem antal**.
9. Vælg **OK** for at gemme standardvarekladden.

Når du gemmer standardvarekladden, vises siden med varekladden, så du kan bogføre den.

### <a name="to-reuse-a-standard-journal"></a><a name="to-reuse-a-standard-journal"></a>Sådan genbruges en standardkladde

> [!NOTE]
> Standardkladder har ikke altid de samme felter som finanskladder. Når du bruger handlingen Hent standardkladder til at kopiere felterne til finanskladden, kan finanskladden indeholde færre oplysninger, end hvis du har oprettet den manuelt. 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varekladder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Hent standardkladder**.
3. Vælg handlingen **Vis kladde**, hvis du vil gennemse en standardvarekladde, inden du vælger den til genbrug.

    De ændringer, du foretagert i en standardvarekladde, gemmes med det samme, og de vises næste gang, du åbner eller genbruger standardvarekladden. Sørg for at ændringerne er vigtige nok til, at de skal gælde generelt. Hvis det ikke er tilfældet, kan du foretage ændringerne i varekladden, efter at linjerne i standardvarekladden er indsat. Se trin 4.
4. Vælg den standardvarekladde på siden **Standardvarekladder**, du vil genbruge, og vælg derefter knappen **OK**.

    Varekladden indeholder de linjer, du har gemt. Hvis varekladden allerede indeholder linjer, vises de nye linjer efter dem.

    Hvis du ikke aktiverer til/fra-feltet **Gem pris**, vil feltet **Pris** på linjer, der indsættes fra standardkladden, indeholde værdien fra feltet **Kostpris** på varekortet.

    > [!NOTE]  
    > Hvis du aktiverede til/fra-feltet **Gem pris** eller **Gem antal**, skal du kontrollere, at de nye værdier er korrekte, inden du bogfører varekladden.
    >
    > Hvis indsatte varekladdelinjer indeholder gemte kostpriser, som du ikke vil bogføre, kan du hurtigt ændre dem til varernes aktuelle værdi på følgende måde:

5. Vælg de varekladdelinjen, som du vil regulere, og vælg derefter handlingen **Genberegn pris**. Denne handling opdaterer feltet Pris med varens aktuelle pris.
6. Vælg handlingen **Bogfør**.

## <a name="to-renumber-document-numbers-in-journals"></a><a name="to-renumber-document-numbers-in-journals"></a>Omnummerere bilagsnumre i kladder

Du kan undgå bogføringsfejl pga. bilagets nummerrækkefølge ved at bruge handlingen **Omnummerer bilagsnumre**, før du bogfører en kladde.

I alle kladder, der er baseret på finanskladden, kan feltet **Bilagsnr** redigeres, så du kan angive forskellige bilagsnumre til forskellige kladdelinjer eller det samme bilagsnummer til relaterede kladdelinjer.

Hvis feltet **Nummerserie** i kladdenavnet er udfyldt, kræver bogføringsfunktionen i finanskladder, at bilagsnummeret på individuelle eller grupperede kladdelinjer er i rækkefølge. Du skal blot vælge funktionen **Omnummerer bilagsnumre**, og relevante **Bilagsnr.**-felterne opdateres derefter. Hvis relaterede kladdelinjer er grupperet efter bilagsnummer, før du har brugt funktionen, forbliver de grupperet men kan være tildelt et andet bilagsnummer.  

Denne funktion fungerer også i filtrerede visninger.

Ved enhver omnummerering af bilagsnumre respekteres relaterede udligninger, f.eks. en betalingsudligning fra bilaget på kladdelinjen til en kreditorkonto. Derfor opdateres felterne **Udligningsid** og **Udligningsbilagsnr.** i berørte finansposteringerne.

### <a name="to-renumber-documents-in-journals"></a><a name="to-renumber-documents-in-journals"></a>Omnummerere bilag i kladder

Følgende procedure er baseret på siden **Kassekladde**, men gælder for alle andre kladder, der er baseret på finanskladden, f.eks. siden **Udbetalingskladde**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Finanskladder**, og vælg derefter det relaterede link.
2. Når du er klar til at bogføre kladden, skal du vælge handlingen **Omnummerer bilagsnumre**.

Værdier i feltet **Bilagsnr.** ændres, hvor det kræves, så bilagsnummeret på individuelle eller grupperede journallinjer er i rækkefølge. Når bilag omnummereres, kan du bogføre kladden.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Bogføre transaktioner direkte i finansposterne](finance-how-post-transactions-directly.md)  
[Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md)  
[Fordele omkostninger og indtægter](year-allocate-costs-income.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Lukke åbne vareposter, der fremkommer ved fast udligning i varekladden](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Regulere lagerbeholdning i værdireguleringskladden](inventory-how-revalue-inventory.md)  
[Tælle, justere og ompostere inventar ved hjælp af kladder](inventory-how-count-adjust-reclassify.md)  
[Afstemme betalinger fra debitorer med indbetalingskladden eller fra debitorposter](receivables-how-apply-sales-transactions-manually.md)  
[Afstemme kreditorbetalinger med udbetalingskladden eller fra kreditorposter](payables-how-apply-purchase-transactions-manually.md)  
[Arbejde med koncerninterne dokumenter og kladder](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
