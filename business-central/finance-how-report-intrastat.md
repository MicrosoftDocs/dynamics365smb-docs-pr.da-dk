---
title: Arbejde med Intrastat-rapportering
description: 'Få at vide, hvordan du rapporterer handel med virksomheder i andre EU-lande/områder med Intrastat-systemet.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
ms.date: 04/08/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---
# <a name="work-with-intrastat-reporting"></a>Arbejde med Intrastat-rapportering

Alle virksomheder i EU skal rapportere deres handel med andre EU-lande/områder. Du skal rapportere bevægelsen af varer til statistikmyndighederne i Danmark hver måned, og rapporten skal indleveres til skattemyndighederne. Intrastat er det system, der bruges til indsamling af handelsstatistik for varer inden for disse lande/områder. Du kan bruge **Intrastat-rapporten** til at udfærdige regelmæssig Intrastat-rapportering (typisk månedligt), indsamling, registrering og rapportering af handel med varer i henhold til den lokale lovgivning.

Intrastat-rapportering er baseret på de grundlæggende EU-forordninger, der gælder for alle lande/områder. I praksis er der imidlertid visse forskelle i de enkelte lande/områder. Hvert land/område har regler for, hvad der nøjagtigt skal rapporteres og hvordan.

> [!IMPORTANT]  
> I denne artikel beskrives den nye Intrastat-oplevelse i [!INCLUDE[prod_short](includes/prod_short.md)], som starter i 2022 udgivelsesbølge 2, der indeholder udvidede funktioner og [skal være aktiveret for eksisterende virksomheder](finance-how-setup-report-intrastat.md#enable-the-new-intrastat-experience). Kontakt administratoren for at aktivere og konfigurere den nye funktion.
>
> Læs den forrige versions artikel om Intrastat-opsætning og brugsoplysninger ved i [Konfigurere og rapportere Intrastat](finance-how-setup-report-intrastat-v20.md).

> [!NOTE]  
> Intrastat-oplysninger gælder ikke for flytning af tjenester mellem lande/områder, men kun handelsvarer (varer og anlægsaktiver). Hvis den lokale regering kræver registrering af tjenesteydelser mellem lande/områder, kan det gøres ved hjælp af funktionen **Serviceerklæring**.
>
> Vi forventer, at denne funktion er tilgængelig fra november 2022 som en app på [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). På nuværende tidspunkt skal du først installere den på siden **Udvidelsesstyring**.

## <a name="fill-in-the-intrastat-report"></a>Udfylde Intrastat-rapporten

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Intrastat-liste**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny** for at oprette en ny **Intrastat-rapport**.
3. Hvis du har brug for at angive interne oplysninger om **Intrastat-rapporten**, skal du udfylde disse oplysninger i feltet **Beskrivelse**.
4. Angiv den måned, der skal rapporteres data for, i feltet **Statistikperiode**. Angiv perioden som et fircifret tal uden mellemrum eller symboler. Afhængigt af dit land/område skal du angive enten måneden først og derefter året eller omvendt. Skriv f.eks. enten *2206* eller *0622* for juni 2022.
5. Vælg handlingen **Foreslå linjer**. Felterne **Startdato** og **Slutdato** indeholder allerede datoerne for statistikperioden i Intrastat-rapporthovedet.
6. I feltet **Reguleringspct.** kan du angivet et procenttal til dækning af transport og forsikring. Hvis du angiver en procent, er indholdet af feltet **Statistisk værdi** i kladden forholdsmæssigt højere. Men hvis du vil bruge denne funktion, skal du ændre feltet **Beløb inkl. varegebyrer** til **Ja**.
7. Du kan oprette ekstra konfigurationer i oversigtspanelet **Yderligere**.
   1. **Spring over genberegning af nul-beløb**, hvis du vil angive, at linjer uden beløb ikke skal genberegnes under kørslen.
   2. **Spring over nul-beløb** for at angive, at varefinansposter uden beløb ikke skal inkluderes i kørslen.
   3. **Spring over ikke-fakturerede poster** for at angive, om vareposter, der er leveret eller modtaget, men endnu ikke er faktureret, skal udelukkes fra processen.
8. Vælg **OK** for at starte kørslen.

Kørslen henter alle vareposter i statistikperioden og indsætter dem som linjer i **Intrastat-rapport**-linjer. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="modify-the-intrastat-report"></a>Redigere Intrastat-rapporten

Hvis det er nødvendigt, kan du ændre linjerne, men når du ændrer en værdi på Intrastat-rapportlinjen, udfyldes feltet **Rettelse** automatisk som **Ja**. Til sidst kan du tilføje en ny linje manuelt, hvis der er grund til det. Sådan tilføjer du en ny linje manuelt:

1. På siden **Intrastat-rapport** skal du i oversigtspanelet **Linjer** vælge handlingen **Ny linje**.
2. Vælg indstillingen **Modtagelse** eller **Afsendelse** i feltet **Type**.
3. I feltet **Kildetype** skal du vælge en af kilderne: **Varepost**, **Anlægspost** eller **Sagspost**.
4. Afhængigt af den valgte **Kildetype** i feltet **Varenr.**, kan du vælge en **Vare** (i begge tilfælde **Varepost** eller **Sagspost**) eller **Anlægsaktiver**.
5. Udfyld de øvrige felter, som du har brug for til Intrastat-rapportering.

> [!NOTE]  
> Når du manuelt føjer en ny linje til Intrastat-rapporten, skal feltet **Dato** på linjen ligge inden for den **Statistikperiode**, du tilføjede i hovedet.

## <a name="validate-intrastat-lines"></a>Validere Intrastat-linjer

Når du har udfyldt **Intrastat-rapporten**, kan du køre handlingen **Kontrollisterapport** for at kontrollere, at alle oplysninger i **Intrastat-rapport** er korrekte. Obligatoriske felter, du har angivet på siden i Tjekliste til Intrastat-rapport, som mangler værdier, vises i **Fejl og advarsler**-faktaboksen på siden **Intrastat-rapport**.

Kør rapporten **Tjekliste til Intrastat-rapport** for at kontrollere Intrastat-linjer, før de udlæses til det krævede format. Checket udføres i **Intrastat-rapporten**.

## <a name="recalculating-weight-or-supplementary-unit-of-measure"></a>Genberegne vægt eller supplerende måleenhed

Hvis fejlmeddelelsen *"Samlet vægt" på Intrastat-rapportlinje må ikke være tom*, vises, skyldes det sikkert, at du ikke har angivet feltet **Nettovægt** på den anvendte kilde, vare eller anlægsaktiv. Hvis det er tilfældet, skal du søge efter varen eller anlægskortet og tilføje den påkrævede værdi. Derefter skal du blot åbne **Intrastat-rapporten** igen og følge disse trin:

1. Vælg funktionen **Beregn vægt/supplerende enhed igen** for at genberegne den **Samlede vægt** og/eller **Supplerende mængde**.
2. Vælg en af følgende indstillinger:

    1. **Vægt** – Hvis du kun vil genberegne den **Samlede vægt**, baseret på de aktuelle oplysninger om **Nettovægt** på varen og anlægskortene.
    2. **Supplerende enhedsmængde** – for kun at genberegne det **Supplerende antal** på **Intrastat-rapportens** linje, hvis den findes, baseret på de aktuelle oplysninger om **Supplerende enhed** på varen og anlægskortene.
    3. **Begge** – for at genberegne den **Samlede vægt** og **Supplerende antal** baseret på de aktuelle oplysninger om varen og anlægskortene.
3. Vælg **OK** for at starte kørslen.

## <a name="report-intrastat-in-a-file"></a>Rapportere Intrastat i en fil

Du kan sende Intrastat-rapporten som en fil, der er baseret på andre lokale myndighedskrav. Før du opretter filen, skal du køre **Kontrollisterapporten** for at kontrollere, om alle linjer indeholder alle nødvendige og gyldige oplysninger. Sådan opretter du en fil:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Intrastat-liste**, og vælg derefter det relaterede link.
2. Vælg **Intrastat-rapport**, som du vil rapportere som en fil.
3. Hvis du ikke allerede har gjort det, skal du udfylde **Intrastat-rapport** manuelt eller vælge handlingen **Foreslå linjer**.
4. Vælg handlingen **Opret fil**.
5. Intrastat-filen gemmes i det påkrævede format.

Når du har oprettet filen, vil [!INCLUDE[prod_short](includes/prod_short.md)] automatisk udfylde følgende oplysninger om rapportering:

* **Eksportdato** angiver den dato, hvor rapporten blev eksporteret.
* **Eksporttidspunkt** angiver det tidspunkt, hvor rapporten blev eksporteret.

> [!NOTE]  
> Næste gang du opretter en fil, bevarer felterne **Eksportdato** og **Eksporttidspunkt** kun oplysninger om den sidste fil, du har oprettet.

## <a name="intrastat-rules"></a>Intrastat-regler

### <a name="grouping-lines"></a>Gruppering af linjer

I **Intrastat-rapportens** linjer er der ingen gruppering af felter. Alle poster kopieres fra den oprindelige kilde, så du hurtigt kan finde dem på basis af kombinationen af **Kildetype** og **Kildepostnr**.

Gruppering, der kræves af myndighederne, leveres i den eksporterede fil. Du skal konfigurere dette i **dataudvekslingsdefinitionen**, som kan konfigureres med det hele. Flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

### <a name="fixed-assets-reporting"></a>Rapportering af anlægsaktiver

Anlægsaktiver vises kun på Intrastat-linjerne, hvis:

* **Anlægsbogføringstypen** i feltet **Anlægsfinanspost** er **Anskaffelsespris**, og hvis **Dokumenttype** er **Faktura** i forbindelse med køb, og
* **Anlægsbogføringstypen** i feltet **Anlægsfinanspost** er **Disponibelt salg**, og hvis **Dokumenttype** er **Faktura** i forbindelse med salg.

### <a name="intrastat-report-statuses"></a>Intrastat-rapportstatusser

Når du arbejder med **Intrastat-rapporten**, får du vist et **Status**-felt på dokumenthovedet. Du kan finde følgende statusser sammen med relaterede regler:

* **Åben**: Denne status oprettes automatisk, når du opretter en ny Intrastat-rapport, og du kan udføre alle operationer i denne status.
* **Frigivet**: [!INCLUDE[prod_short](includes/prod_short.md)] ændrer automatisk status til *Frigivet*, når du opretter en fil. Fra dette tidspunkt kan du ikke ændre **Intrastat-rapporten**. Hvis du har brug for at ændre noget og rapportere igen, kan du bruge handlingen **Genåbn** til at genåbne Intrastat-rapporten. Når dokumentet genåbnes, kan du bruge handlingen **Frigiv** igen til at frigive dokumentet igen.
* **Rapporteret**: Angiver, om posten tidligere har været rapporteret til SKAT. Dette er ikke en fast status, men et uafhængigt felt, og selvom du har genåbnet Intrastat-rapporten, vil den stadig vise, at filen allerede er oprettet til rapporten.

### <a name="locations-in-intrastat-reporting"></a>Lokationer i Intrastatrapportering

[!INCLUDE[prod_short](includes/prod_short.md)] bruger altid oplysningerne i feltet **Lande-/områdekode** på siden **Lokationskort** som land for **afsende fra** eller **modtage** til varer. Når disse oplysninger ikke findes, eller lokationen ikke blev brugt, bruger systemet oplysningerne fra siden **Virksomhedsoplysninger**.   

> [!NOTE]  
> Hvis virksomheden opererer fra mere end ét land, fungerer Intrastatrapportering ikke i alle lande, hvor lokationer er konfigureret. Rapportering er kun baseret på hovedlandet, da det i øjeblikket ikke er muligt at bruge rapportering fra flere lande.  

### <a name="triangular-trade-in-intrastat"></a>Trekantshandel med Intrastat

Trekantshandel indebærer handel mellem tre lande eller områder, hvor varer ikke over for rapporteringsvirksomheden har sit eget land. I Business Central kan dette gøres nemmere via funktionen [Direkte levering](sales-how-drop-shipment.md). Hvis du vil aktivere denne indstilling, skal du aktivere feltet **Medtag direkte levering** i vinduet **Intrastat-rapportopsætning**.  

Hvis du aktiverer denne indstilling, bruger systemet følgende regler, men kun hvis **Direkte levering** er markeret **salgsordren**: 

| Modtager fra | Leverer til | Forventet Intrastat-resultat |
|----------|------------|----------------------|
| Land som i **Virksomhedsoplysninger** | Land som i **Virksomhedsoplysninger** | Ingen intrastat-linjer |  
| Land som i **Virksomhedsoplysninger** | EU-land, der er forskelligt fra landet i **Virksomhedsoplysninger** | Intrastat-leveringslinje | 
| Land som i **Virksomhedsoplysninger** | Uden for EU-lande | Ingen intrastat-linjer |   
| EU-land, der er forskelligt fra landet i **Virksomhedsoplysninger** | Land som i **Virksomhedsoplysninger** | Intrastat-modtagelinje | 
| EU-land, der er forskelligt fra landet i **Virksomhedsoplysninger** | EU-land, der er forskelligt fra landet i **Virksomhedsoplysninger** | Ingen intrastat-linjer |
| EU-land, der er forskelligt fra landet i **Virksomhedsoplysninger** | Uden for EU-lande | Ingen intrastat-linjer | 
| Uden for EU-lande | Land som i **Virksomhedsoplysninger** | Ingen intrastat-linjer |  
| Uden for EU-lande | EU-land, der er forskelligt fra landet i **Virksomhedsoplysninger** | Ingen intrastat-linjer |
| Uden for EU-lande | Uden for EU-lande | Ingen intrastat-linjer |   

## <a name="see-also"></a>Se også

[Konfigurere intrastat-rapportering](finance-how-setup-report-intrastat.md)  
[Økonomistyring](finance.md)  
[Direkte forsendelse](sales-how-drop-shipment.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
