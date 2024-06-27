---
title: Registrere køb med købsfakturaer
description: 'Beskriver, hvordan du køber lagervarer, varer, der ikke er på lager, eller ressourcer ved at oprette og bogføre købsfakturaer eller ordrer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: procurement
ms.search.form: '50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="record-purchases-with-purchase-invoices-and-orders"></a>Registrere køb med købsfakturaer og ordrer

Du kan oprette en købsfaktura eller købsordre for at registrere omkostningerne ved køb og spore gæld. Købsfakturaer og købsordrer anvendes også til at opdatere lagerniveauer dynamisk, så du kan minimere lageromkostningerne og yde bedre kundeservice. Købsomkostningerne, herunder serviceudgifter og lagerværdier, der stammer fra bogføring af købsfakturaer eller ordrer, bidrager til avancebeløb og andre finansielle nøgletal (KPI'er) i dit Rollecenter.

## <a name="record-purchases-with-purchase-invoices"></a>Registrere køb med købsfakturaer

Når du modtager lagervarerne, eller når den købte tjeneste er fuldført, skal du bogføre købsfakturaen for at opdatere lager- og finansposter og aktivere betaling til kreditor i henhold til betalingsbetingelserne. [Foretage betaling](payables-make-payments.md)

> [!CAUTION]  
> Bogfør ikke en købsfaktura for fysiske varer, før du har modtaget varerne og kender de endelige omkostninger for købet, herunder eventuelle ekstra gebyrer. Ellers kan din lagerværdi og avancetal blive skævt.

### <a name="create-and-post-a-purchase-invoice"></a>Oprette og bogføre en købsfaktura

Følgende afsnit handler om, hvordan du opretter en købsfaktura. Fremgangsmåden er den samme for en købsordre. Den væsentligste forskel er, at købsordrer har yderligere felter og handlinger til fysisk håndtering af varer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. I feltet **Kreditornavn** skal du indtaste navnet på en eksisterende kreditor.

    Andre felter på siden **Købsfaktura** er nu udfyldt med standardoplysningerne for den valgte kreditor. Hvis kreditoren ikke er registreret, skal du følge disse trin:

    1. I feltet **Kreditornavn** skal du indtaste navnet på den nye kreditor.
    2. I dialogboksen, hvor du registrerer den nye kreditor, skal du trykke på knappen **Ja**.
    3. Du kan finde flere oplysninger om, hvordan du udfylder kreditorkortet, i [Registrere nye kreditorer](purchasing-how-register-new-vendors.md).  
    4. Når du er færdig med kreditorkortet, skal du vælge **OK** for at vende tilbage til siden **Købsfaktura**.

3. Udfylde de resterende felter efter behov på siden **Købsfaktura**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Du er nu klar til at udfylde købsfakturalinjerne med varer eller ressourcer, som du har købt af kreditoren.

    > [!NOTE]  
    > Hvis du har konfigureret de tilbagevendende købslinjer for kreditoren, f.eks en månedlig genbestillingsordre, kan du indsætte disse linjer i fakturaen ved at vælge handlingen **Hent tilbagevendende købslinjer**.
4. I oversigtspanelet **Linjer** skal du i feltet **Varenr.** indsætte nummeret på en vare eller en service.
5. Angiv antal varer, der skal købes, i feltet **Antal**.

    Feltet **Linjebeløb** opdateres, så det viser værdien i feltet **Købspris** ganget med værdien i feltet **Antal**.

    Prisen og linjebeløbet vises med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på kreditorkortet.

    Totalfelterne under linjerne opdateres automatisk, når du opretter eller redigerer linjer for at få vist de beløb, der skal bogføres i finansposterne.

6. I feltet **Fakturarabatbeløb** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms** nederst i fakturaen.

    > [!NOTE]  
    > Hvis du har konfigureret fakturarabatter til kreditoren, indsættes den angivne procentværdi automatisk i feltet **Leverandørfakturarabat i %**, hvis kriterierne opfyldes. Det relaterede beløb indsættes derefter i feltet **Fakturarabatbeløb**.
7. Når du modtager de købte varer eller servicer, skal du vælge **Bogfør**.

Købet afspejles nu i lagerposter, ressourceposter og finansposter, og kreditorbetalingen aktiveres. Købsfakturaen fjernes fra listen over købsfakturaer og erstattes med et nyt bilag i oversigten over bogførte købsfakturaer. Yderligere oplysninger om, hvad der sker, når du bogfører købsdokumenter, finder du under [Bogføring af køb](purchasing-how-record-purchases.md#posting-purchases).

> [!NOTE]
> I sjældne tilfælde kan de bogførte beløb afvige fra det, der er vist i totalfelterne. Dette skyldes typisk afrundingsberegninger i relation til moms eller salgsskat.
>
> Hvis du vil kontrollere de beløb, der faktisk bogføres, skal du gå til siden **Statistik**, som tager højde for afrundingsberegningerne. Hvis du vælger handlingen **Frigiv**, opdateres totalfelterne, så de omfatter afrundingsberegninger.

## <a name="posted-invoices"></a>Bogførte fakturaer

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Du kan nemt rette eller annullere en bogført købsfaktura, før du betaler kreditoren. Hvis du f.eks. skal rette en skrivefejl eller ændre købet tidligt i ordreprocessen. Flere oplysninger i [Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Hvis du allerede har betalt for varer eller tjenester på den bogførte købsfaktura, skal du oprette en købskreditnota for at tilbageføre købet. Flere oplysninger i [Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

[Åbne listen **Bogførte købsfakturaer**](https://businesscentral.dynamics.com/?page=146) i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="purchasing-noninventory-items"></a>Køb af varer, der ikke er lagervarer

Linjerne på en købsfaktura kan være af **ressource**- eller **vare**-typen. Varekortet kan desuden være klassificeret som **Lager**, **Service** eller **Ikke-lager** for at angive, om varekortet repræsenterer en fysisk lagerenhed, en arbejdstidsenhed (også tilgængelig for ressourcer) eller en fysisk enhed, der ikke opbevares på lageret. Flere oplysninger i [Registrere nye emner](inventory-how-register-new-items.md). Købsfakturaprocessen er den samme for alle nævnte typer.

> [!NOTE]
> Du kan også købe eksterne ressourcer med købslinjetypen **Ressource**, f.eks. for at fakturere en kreditor for udført arbejde. Flere oplysninger i [Konfigurere ressourcer](projects-how-setup-resources.md).
>
> Hvis du vil bruge en købt ressource, skal du muligvis angive ressourcens kapacitet og knytte den til et projekt manuelt. Når en ressource købes, oprettes en ressourcepost, men ressourceposternes antal og værdi spores ikke, ligesom det f.eks. er tilfældet med varer. Hvis antal og værdi skal spores, skal du overveje at bruge andre typer linjeelementer.

## <a name="when-to-use-purchase-orders"></a>Hvornår skal købsordrer bruges?

Brug købsordrer, hvis du har brug for at registrere delleverancer af et ordreantal. Det kan f.eks. være, at hele antallet ikke er tilgængeligt hos leverandøren. Hvis du leverer salgte varer direkte fra leverandøren til kunden som en direkte levering, skal du også bruge købsordrer. Flere oplysninger i [Foretage direkte leveringer](sales-how-drop-shipment.md).

I alle andre henseender fungerer købsordrer på samme måde som købsfakturaer. Følgende procedure er baseret på en købsfaktura. Fremgangsmåden er den samme for en købsordre.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="receive-items-with-a-purchase-order"></a>Modtage varer med en købsordre

Nedenfor kan du se, hvordan du modtager varer med en købsordre. 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsordrer**, og vælg derefter det relaterede link.
2. Åbn en eksisterende købsordre eller opret en ny.
3. Angiv det modtagne antal i feltet **Modtag (antal)**.

   > [!NOTE]
   > Hvis det modtagne antal er større end det, der er bestilt på købsordren ifølge feltet Antal, og kreditoren må tillade overmodtagelser, skal du bruge feltet **Overmodtagelse** til at håndtere mere end det maksimale antal. Flere oplysninger i afsnittet [Sådan modtager du flere varer end det bestilte antal](purchasing-how-record-purchases.md#receive-more-items-than-you-ordered).
4. Vælg handlingen **Bogfør**.

  Værdien i feltet **Modtaget antal** opdateres. Hvis det er en delvis modtagelse, er værdien lavere end værdien i feltet **Antal**.

> [!NOTE]
> Hvis du bruger et lagerdokument til at bogføre modtagelsen, kan du ikke bruge handlingen **Bogfør** i købsordren. I stedet har en lagermedarbejder allerede bogført antallet på købsordren som modtaget. Flere oplysninger i [Designoplysninger - Indgående lagerstedsflow](design-details-inbound-warehouse-flow.md).

## <a name="receive-more-items-than-you-ordered"></a>Sådan modtager du flere varer end det bestilte antal

Når du modtager flere varer, end du har bestilt, kan det være en god idé at modtage dem i stedet for at annullere modtagelsen. Det kan f.eks. være billigere at lade de overskydende varer indgå i lagerbeholdningen frem for at returnere dem, eller også kan leverandøren måske tilbyde en rabat mod, at du beholder dem.

Følgende video viser, hvordan du arbejder med overmodtagelser.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1l2PE]

<!--move the over-receipt setup info to an article about purchasing. Keep the concept info here and link to the steps-->
### <a name="set-up-over-receipts"></a>Konfigurere overmodtagelser

Oprette koder for over modtagelse for at definere en procent, hvor et modtaget antal kan overstige det bestilte antal. I feltet **Tolerance-% for overmodtagelse** specificeres i rabatprocenten. Derefter kan du tildele koden på varekortet eller siden med kreditorkort for varer og leverandører.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Overmodtagelseskoder**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="assign-the-over-receipt-code-to-an-item"></a>Overmodtagelseskoden knyttes til varen

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn vinduet **Varekort** til den tilhørende vare.
3. Du kan definere dette under en overmodtagelseskode, som indeholder procentdelen i feltet **Overmodtagelseskode**.

Overmodtagelseskoden knyttes til varen. Købsordrer eller lagerstedsmodtagelse for varen giver nu mulighed for at modtage mere end det bestilte antal i henhold til den angivne toleranceprocent for overlevering.

> [!NOTE]
> Du kan oprette en godkendelsesproces for at kræve, at overmodtagelser skal godkendes, før de kan behandles. Hvis det er tilfældet, skal du markere afkrydsningsfeltet **Godkendelse kræves** på siden **Overmodtagelseskoder**. Flere oplysninger i [Oprette workflows](across-how-to-create-workflows.md).

### <a name="over-receive-an-order"></a>Modtagelse af flere ordrer

På købslinjer og lagermodtagelseslinjer bruges feltet **Overmodtagelsesantal** til at registrere overmodtagne mængder, dvs. mængder, der overstiger værdien i feltet **Antal**, det bestilte antal.

Når du håndterer en overmodtagelse, kan du enten øge værdien i feltet **Modtag (antal)** til det faktisk modtagne antal. Feltet **Overmodtagelsesantal** opdateres derefter, så det overskydende antal vises. Du kan også angive det overskydende antal i feltet **Overmodtagelsesantal**. Feltet **Modtag (antal)** opdateres derefter, så det bestilte antal plus det overskydende antal vises. Følgende fremgangsmåde beskriver, hvordan du udfylder feltet **Modtag (antal)**.  

1. På en købsordre eller et lagermodtagelsesdokument, hvor det modtagne antal er højere end det bestilte, skal du angive det faktisk modtagne antal i feltet **Modtag (antal)**.

    Hvis stigningen ligger inden for den tolerance, der er angivet i overmodtagelseskoden, opdateres feltet **Overmodtagelsesantal**, så det viser det antal, der angiver, hvilken værdi i feltet **Antal**, der overskrides.

    Hvis forøgelsen er større end den angivne tolerance, er overmodtagelse ikke tilladt. Undersøg, om en anden overlevering-kode tillader den. Ellers er det kun det bestilte antal, der kan modtages, og overskydende antal skal håndteres på en anden måde, f.eks. ved at returnere den til leverandøren.

2. Bogfør modtagelsen ligesom enhver anden modtagelse.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] håndterer ikke automatisk finansielle aspekter af overleveringer. Du skal håndtere dette manuelt efter aftale med leverandøren, f.eks. ved at leverandøren videresender en ny eller opdateret faktura.

## <a name="external-document-number"></a>Eksterne bilagsnumre

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="posting-purchases"></a>Bogføring af køb

På et købsdokument kan du vælge mellem følgende bogføringshandlinger:

* **Bogfør**
* **Vis bogføring**
* **Bogfør og udskriv**
<!--* **Test Report**-->
* **Massebogfør**

Når et købsdokument bogføres, opdateres kreditorens konto, regnskabet og vareposterne, og ressourceposterne opdateres.

For hvert købsdokument oprettes der en købspost i tabellen **Finanspost**. Der oprettes også en post i kreditorkontoen i tabellen **Kreditorpost**, og der oprettes en finanspost i den relevante samlekonto. Desuden kan bogføring af købet medføre oprettelse af en moms- og en finanspost med rabat. Om der bogføres en post med rabat, afhænger af oplysningerne i feltet **Bogføring med rabat** i tabellen **Købsopsætning**.

For hver købslinje oprettes følgende poster i:

* Tabellen **Varepost**, hvis købslinjen er af typen **Vare**.
* En post i tabellen **Finansport**, hvis købslinjerne er af typen **Finanskonto**.
* En post i tabellen **Ressourcepost**, hvis købslinjen er af typen **Ressource**.

Købsdokumenter registreres desuden altid i tabellerne **Købsleverancehoved** og **Købsfakturahoved**.

Du kan altid gennemse forskellige poster, der oprettes som resultat af bogføring. Vælg **Vis bogføring** for at validere dokumentet og gennemse forventede poster.


> [!IMPORTANT]  
> Når du bogfører en købsordre for varer, kan du både oprette en kvittering og en faktura. Det kan gøres samtidigt eller hver for sig. Du kan også oprette en delkvittering og en delfaktura ved at udfylde felterne **Modtag (antal)** og **Fakturer (antal)** på de enkelte købsordrelinjer, før du bogfører. Bemærk, at du ikke kan oprette en købsfaktura fra en købsordre for produkter eller servicer, der ikke er modtaget. For at kunne fakturere er det altså nødvendigt, at du på forhånd har registreret en modtagelse, eller at du nu vælger at modtage og fakturere samtidigt.

Du kan enten bogføre eller bogføre og udskrive. Hvis du vælger at bogføre og udskrive, udskrives der en rapport, når ordren bogføres. Du kan også vælge funktionen **Massebogfør**, der giver mulighed for at bogføre flere ordrer samtidig. Flere oplysninger i [Bogføre flere dokumenter på én gang](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Visning af finansposter

Når bogføringen er gennemført, fjernes de bogførte købslinjer fra ordren. Der vises en meddelelse, når bogføringen er gennemført. Herefter kan du se de bogførte poster på forskellige sider, der indeholder bogførte poster, f.eks. **Kreditorposter**, **Finansposter**, **Vareposter**, **Ressourceposter**, **Købsmodtagelser** og sider til **Bogførte købsfakturaer**.

I de fleste tilfælde kan du åbne finansposter fra det berørte kort eller dokument. Du kan f.eks. på siden **Kreditorkort** vælge handlingen **Poster**.

## <a name="editing-ledger-entries"></a>Redigering af finansposter

Du kan redigere bestemte felter i bogførte købsdokumenter, f. eks feltet **Betalingsreference**. Flere oplysninger i [Rediger bogførte dokumenter](across-edit-posted-document.md). Er det mere kritiske felter, der påvirker overvågningssporet, skal du tilbageføre eller annullere bogføring. Flere oplysninger i [Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md).

## <a name="see-also"></a>Se også

[Anmode om tilbud](purchasing-how-request-quotes.md)  
[Købe varer til et salg](purchasing-how-purchase-products-sale.md)  
[Forberede direkte leveringer](sales-how-drop-shipment.md)  
[Køb](purchasing-manage-purchasing.md)  
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Konfigurere ressourcer](projects-how-setup-resources.md)  
[Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Redigere bogførte dokumenter](across-edit-posted-document.md)  
[Bogføre flere dokumenter på én gang](ui-batch-posting.md)  
[Køb](purchasing-manage-purchasing.md)  
[Bogføring af dokumenter og kladder](ui-post-documents-journals.md)  
[Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
