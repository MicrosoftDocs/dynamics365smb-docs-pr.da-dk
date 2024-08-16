---
title: Indsend momsrapporter til skattemyndighederne
description: 'Få flere oplysninger om, hvordan du udarbejder rapporter med moms fra salg i en periode eller fra salg og køb og indsender rapporten til en skattemyndighed.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'VAT, tax, report, EC sales list, statement'
ms.search.form: '321, 322, 323, 474, 475, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 9401'
ms.date: 08/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="report-vat-to-tax-authorities"></a>Indberet moms til skattemyndighederne

I denne artikel beskrives de rapporter [!INCLUDE[prod_short](includes/prod_short.md)] , som du kan bruge til at sende oplysninger om momsbeløb for salg og køb til skattemyndighederne i dit område. Afhængigt af det specifikke land/område kan rapporterne indeholde specifikke oplysninger, eller der kan være flere rapporter, som du skal indsende. Se artiklen for dit land/område under den [lokale funktion](about-localization.md).  

Du kan bruge følgende standardrapporter:

* **Oversigt over EU-salg**-rapporten  

    Rapportlisterne Oversigt over EU-salg fra det Europæiske Fællesskab (EU) viser de momsbeløb, du har indsamlet for salg til momsregistrerede debitorer i EU-lande/områder.  
* Rapporten **Momsopgørelse**  

    Rapporten Momsangivelse inkluderer moms for salg og køb til kunder og fra leverandører i alle lande/områder, der bruger moms.  

I begge tilfælde (som i andre momsrelaterede rapporter) beregnes moms på basis af momsbogføringsopsætningen og de momsbogføringsgrupper, du har oprettet. [!INCLUDE[prod_short](includes/prod_short.md)] viser altid momsposter baseret på **momsdato** som en primær rapporteringsdato.  

> [!NOTE]
> Alle momsrelaterede rapporter køres nu med **momsdatoen** for at filtrere relevante poster. Selvom du konfigurerer **momsdatoforbrug** som **Brug ikke momsdatofunktion** vil [!INCLUDE[prod_short](includes/prod_short.md)] skjule alle forekomster af **momsdato** på tværs af ansøgningen. Men **Momsdatoen** bruges dog stadig til alle rapporter og udfyldes automatisk med **bogføringsdatoen**.

Du kan få vist en komplet oversigt over momsposter ved hver bogføring, der indebærer moms, hvor der oprettes en post på siden **Momsposter**. Disse poster bruges til at beregne momsafregningsbeløb, f.eks. betaling og refusion, for en bestemt periode. Du kan få vist VAT-poster ved at vælge den ![lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **VAT-poster**, og vælg derefter det relaterede link.

> [!NOTE]
> Hvert [!INCLUDE[prod_short](includes/prod_short.md)]-miljø skal behandle lovpligtig rapportering i ét enkelt land/område. Den hollandske version af [!INCLUDE[prod_short](includes/prod_short.md)] håndterer momsrapportering i Holland, men ikke i andre lande/områder. På samme måde håndterer den amerikanske version af [!INCLUDE[prod_short](includes/prod_short.md)] 1099 rapportering i USA og understøtter ikke krav om momsindberetning i andre lande/områder, medmindre de er indført via en udvidelse, der leveres af vores partnerøkosystem eller en kundespecifik kodeændring.

## <a name="about-the-ec-sales-list-report"></a><a name="ecsaleslist"></a>Om rapporten Oversigt over EU-salg

I EU og i Storbritannien skal alle virksomheder, der sælger varer og tjenester til momsregistrerede kunder, herunder kunder i andre EU-lande/områder, sende en elektronisk udgave af rapporten Oversigt over EU-salg til Told og Skat. Rapporten **Oversigt over EU-salg** kan kun bruges til EU-lande/områder.

Rapporten indeholder én linje for hver type transaktion med kunden og viser det samlede beløb for hver transaktionstype. Rapporten kan indeholde tre typer transaktioner:  

* B2B-varer  
* B2B-tjenester  
* B2B triangulerede varer  

*B2B*-varer og -tjenesteydelser angiver, om du har solgt en vare eller en tjeneste, og de styres af indstillingen **EU Service** i momsbogføringsopsætningen. *B2B-triangulerede varer* angiver, om du har drevet handel med tredjepart, og styres af indstillingen **EU-trekantshandel** i salgsdokumenter, f.eks. salgsordrer, fakturaer, kreditnotaer osv.  

Når skattemyndighederne har gennemgået din rapport, sender de en mail til kontaktpersonen for din virksomhed. I [!INCLUDE[prod_short](includes/prod_short.md)] angives kontaktpersonen på siden **Virksomhedsoplysninger**. Før du sender rapporten, skal du kontrollere, at der er valgt en kontaktperson.  

### <a name="submit-an-ec-sales-list-report"></a>Indsend en Liste over EU-salg-rapport

[!INCLUDE [finance-ecsaleslist](includes/finance-ecsaleslist.md)]

## <a name="about-the-vat-return-report"></a><a name="vatreturn"></a>Om rapporten Momsopgørelse

Du kan bruge denne rapport til at sende moms for salgs- og købsdokumenter, f.eks. købs- og salgsordrer, fakturaer og kreditnotaer. Oplysningerne i rapporten er opstillet på samme måde som i listeangivelsen fra SKAT.  

For momsopgørelsen kan du angive, at posterne skal omfatte:

* Send kun åbne transaktioner, eller åbne og lukkede. Dette er f.eks. nyttigt, når du forbereder din endelige årlige momsopgørelse.
* Send kun poster fra de angivne perioder, eller medtag også poster fra tidligere perioder. Dette er nyttigt for at opdatere en momsopgørelse, som du allerede har sendt, f.eks. hvis en leverandør sender dig en forsinket faktura.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Sådan opretter du forbindelse til din skattemyndigheds webtjeneste
[!INCLUDE[prod_short](includes/prod_short.md)] indeholder serviceforbindelser til skattemyndighedernes websteder. Hvis du f.eks. befinder dig i Storbritannien, kan du aktivere serviceforbindelsen **GovTalk** for at sende rapporterne Oversigt over EU-salg og Momsopgørelsen elektronisk. Hvis du vil indsende rapporten manuelt, f.eks. ved at indtaste dine data på skattemyndighedens websted, er dette ikke påkrævet.   

Når du vil rapportere moms til en skattemyndighed elektronisk, skal du forbinde [!INCLUDE[prod_short](includes/prod_short.md)] med skattemyndighedens webtjeneste. Dette kræver, at du opretter en konto hos skattemyndighederne. Når du har en konto, kan du aktivere en tjenesteforbindelse, som vi leverer i [!INCLUDE[prod_short](includes/prod_short.md)].

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Serviceforbindelser**, og vælg derefter det relevante link.
2. Udfyld de påkrævede felter. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Det er en god ide at teste forbindelsen. For at gøre dette skal du vælge afkrydsningsfeltet **Testtilstand**. Forbered og send derefter momsrapporten, som beskrevet i afsnittet [Sådan forbereder og sender du en momsrapport](#to-prepare-and-submit-a-vat-report). I Testtilstand kontrollerer tjenesten, om skattemyndighederne kan modtage rapporten, og statussen for rapporten angiver, om testafsendelsen blev udført. Det er vigtigt at huske, at det ikke er en faktisk afsendelse. For at sende rapporten rigtigt skal du fjerne markeringen i afkrydsningsfeltet **Testtilstand** og derefter gentage afsendelsesprocessen.

## <a name="to-set-up-vat-reports-in-"></a>Sådan opsættes momsrapporter i [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

### <a name="to-set-up-vat-return-periods"></a>Sådan defineres momsreturperioder

Hvis din virksomhed ikke er placeret i Storbritannien, kan du eventuelt bruge **siden Momsangivelsesperioder** til at oprette planlagte momsangivelser. Hvis din virksomhed er beliggende i Storbritannien, skal du se [Gør skat digital i Storbritannien](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsangivelsesperioder**, og vælg derefter det relaterede link.  
2. Udfyld felterne på siden **Momsreturnperioder** for at angive den første periode. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)].  
3. Gentag trin 2 for eventuelle yderligere perioder, du vil tilføje.  

Når tiden først skal sendes til en momsrapport for en moms afleverings periode, skal du vælge perioden på siden **Momsreturperioder** og derefter vælge funktionen **Opret VAR retur**. Vælg derefter handlingen **Foreslå linjer** som beskrevet i trin 3 i følgende procedure på **momsretur**-kortet.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Sådan forbereder og sender du en momsrapport

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **EF-salgsliste** eller **Momsangivelser**, og vælg derefter den relaterede sammenkæde.  
2. Vælg **Ny**, og udfyld de påkrævede felter. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. For at generere oplysningerne i rapporten skal du vælge handlingen **Foreslå linjer**.  

    > [!NOTE]  
    >  For rapporten Oversigt over EU-salg kan du gennemse transaktionerne i rapportlinjerne, inden du sender rapporten. Det gør du ved at vælge linjen og derefter vælge handlingen **Vis momsposter**.  

4. Hvis du vil validere og forberede rapporten til afsendelse, skal du vælge handlingen **Frigiv**.  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer, om rapporten er konfigureret korrekt. Hvis valideringen ikke lykkes, vises fejlene under **Fejl og advarsler**, så du ved, hvad du skal rette. Hvis meddelelsen typisk drejer sig om en manglende indstilling i [!INCLUDE[prod_short](includes/prod_short.md)], kan du klikke på meddelelsen for at åbne siden med de oplysninger, der skal rettes.  
5. Du sender rapporten ved at vælge handlingen **Send**.  

Når du sender rapporten, overvåger [!INCLUDE[prod_short](includes/prod_short.md)] tjenesten og registrerer din kommunikation. Feltet **Status** angiver, hvor rapporten er i processen. F.eks. når myndighederne behandler rapporten, ændres status for rapporten til **Fuldført**. Hvis skattemyndighederne finder fejl i den rapport, du har sendt, bliver status for rapporten **Mislykkedes**. Du kan se fejlene under **Fejl og advarsler**, rette dem og derefter sende rapporten igen. For at få vist en liste over alle EU-salgslisterapporter, skal du gå til siden **Rapporter over EU-salg**.  

### <a name="vat-return-statuses"></a>Status for momsangivelse

Momsangivelse kan have forskellige statusangivelser som beskrevet i følgende tabel.

| Status | Beskrivlse |
|------------|-------------------------|
| Åben | Når du opretter en ny momsangivelse. Du kan køre handlingen **Foreslå linjer**. Hvis du har brug for at rette værdier, kan du udføre handlingen **Foreslå linjer** igen. Du kan ikke indsende en momsangivelse, der har denne status. |
| Frigivet | Status ændres, når du bruger handlingen **Frigiv**. [!INCLUDE[prod_short](includes/prod_short.md)] viser oversigtspanelet **Fejl og advarsler**. Du kan ikke foretage ændringer eller bruge handlingen **Foreslå linjer**. Hvis du vil foretage ændringer, skal du genåbne momsangivelsen. |
| Afvist | Hvis din indsendelse ikke lykkedes, f.eks. hvis godkendelsen mislykkedes), ændres status til **Afvist**. Du kan ikke genåbne momsangivelse, der har denne status. |
| Indsendt | Momsangivelsen indsendes ved hjælp af handlingen **Send** eller markeres som sendt ved hjælp af funktionen **Marker som sendt**. |
| Accepteret | Momsangivelsen har denne status, hvis rapporten er markeret som accepteret ved hjælp af handlingen **Markér som accepteret** . Hvis **momsangivelsen** er markeret som **Accepteret**, kan du udføre handlingen **Beregn og bogfør momsafregning**. |

## <a name="viewing-communications-with-your-tax-authority"></a>Visning af kommunikationen med skattemyndighederne

I nogle lande/områder udveksler du meddelelser med skattemyndighederne, når du sender rapporter. Du kan få vist først og sidste meddelelse, du har sendt eller modtaget, ved at vælge handlingerne **Download afsendelsesmeddelelse** og **Download svarmeddelelse**.  

## <a name="submitting-vat-reports-manually"></a>Sende momsrapporter manuelt
Hvis du bruger en anden metode til at sende rapporten, f.eks. ved at eksportere XML-filen og overføre den til en skattemyndighedens websted, kan du vælge **Marker som sendt** for at afslutte rapporteringsperioden. Når du har markeret rapporten som udgivet, kan den ikke redigeres. Hvis du har brug for at ændre rapporten efter, at den er markeret som udgivet, skal du åbne den.

## <a name="vat-settlement"></a>Momsafregning
Du skal med jævne mellemrum betale nettomomsen til skattemyndighederne. Når du skal afregne moms jævnligt, kan du udføre kørslen **Afregn moms** for at lukke de åbne momsposter og overføre købs- og salgsmomsbeløb til momsafregningskontoen.

Når du overfører momsbeløb til afregningskontoen, bliver købsmomskontoen krediteret, og salgsmomskontoen debiteres de beløb, der er beregnet for den angivne periode. Nettobeløbet krediteres eller debiteres momsafregningskontoen, hvis købsmomsbeløbet er større. Du kan bogføre afregningen med det samme eller udskrive en kontrolrapport først.  

> [!Note]
> Når du bruger kørslen **Afregn moms**, hvis du ikke angiver en **Momsvirksomhedsbogf.gruppe** og en **Momsproduktbogf.gruppe**, medtages poster med alle virksomhedsbogføringsgrupper og produktbogføringsgruppekoder.

## <a name="configuring-your-own-vat-reports"></a>Konfigurere dine egne momsrapporter

Du kan bruge standardrapporten **Oversigt over EU-salg**. Du kan dog også oprette dine egne rapporter, hvis du har en udviklingslicens, så du kan oprette kodeenheder. Hvis du har brug for assistance, skal du kontakte en Microsoft-partner.  

I følgende tabel beskrives kodeenheder, du skal oprette til rapporten.  

| Codeunit | Dette skal den gøre |
|----|-----|
|Foreslå linjer| Hente oplysninger fra tabellen **Momsposter** og vise dem i linjerne i momsrapporten.|
|Indhold | Kontrollere rapportens format. For eksempel, om det er XML eller JSON. Formatet afhænger af kravene i din skattemyndigheds webtjeneste. |
|Afsendelse | Styre, hvordan og hvornår du sender rapporten ud fra skattemyndighedernes krav. |
|Svarhandler | Håndtere skattemyndighedernes returnering. Der kan f.eks. blive sendt en e-mail til kontaktpersonen i din virksomhed. |
|Annuller | Sende en annullering af en momsrapport, der tidligere blev sendt til skattemyndighederne. |  

> [!Note]
> Når du opretter kodeenheder til rapporten, skal du være opmærksom på værdien i feltet **Momsrapportversion**. Dette felt skal afspejle versionen af den rapport, der blev/bliver krævet af skattemyndighederne. Du kan f.eks. angive **2021** i feltet for at angive, at rapporten opfylder kravene for dette år. For at finde den aktuelle version skal du kontakte skattemyndighederne.  

## <a name="see-also"></a>Se også

[Oprette beregninger og bogføringsmetoder for moms](finance-setup-vat.md)    
[Arbejde moms af salg og køb](finance-work-with-vat.md)    
[Opsætte salg](sales-setup-sales.md)    
[Fakturere salg](sales-how-invoice-sales.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
