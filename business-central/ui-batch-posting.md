---
title: Bogføre flere dokumenter på én gang
description: 'Få mere at vide om, hvordan du vælger flere ikke-bogførte dokumenter på en liste til umiddelbar eller planlagt massebogføring i Business central.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: null
ms.reviewer: edupont
ms.date: 06/25/2021
ms.author: edupont
---
# Bogføre flere dokumenter på én gang

I stedet for at bogføre individuelle dokumenter ét ad gangen, kan du vælge flere ikke-bogførte dokumenter i en oversigt til bogføring med det samme eller til baggrundsbogføring i henhold til en plan, f.eks. ved dagens slutning. Dette kan være nyttigt, hvis det kun er en supervisor, der kan bogføre dokumenter, der er oprettet af andre brugere, eller for at undgå, at der opstår problemer med systemydeevnen under bogføring i arbejdstiden.

## Sådan bogføres flere købsordrer med det samme

Følgende procedure beskriver, hvordan flere købsordrer kan bogføres med det samme. Trinene er de samme for alle købs- og salgsdokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.
2. Fortsæt med at vælge alle de ordrer, der skal bogføres, på siden **Købsordrer**:
3. I feltet **Nummer** skal du vælge de tre lodrette prikker for at åbne genvejsmenuen og derefter vælge handlingen **Markér flere**.
4. Marker afkrydsningsfeltet for alle de linjer, der repræsenterer ordrer, som du vil bogføre på samme tid.
5. Vælg handlingen **Bogføring**, og vælg derefter handlingen **Bogfør**.
6. Vælg knappen **Ja** i bekræftelsesmeddelelsen.

## Sådan massebogføres flere købsordrer

Følgende procedure beskriver, hvordan du kan massebogføre flere købsordrer. Fremgangsmåden er den samme for alle købs- og salgsdokumenter, hvor handlingen **Massebogfør** er tilgængelig.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.  
2. Fortsæt med at vælge alle de ordrer, der skal bogføres, på siden **Købsordrer**:
3. I feltet **Nummer** skal du vælge de tre lodrette prikker for at åbne genvejsmenuen og derefter vælge handlingen **Markér flere**.
4. Marker afkrydsningsfeltet for alle de linjer, der repræsenterer ordrer, som du vil bogføre på samme tid.
5. Vælg handlingen **Bogføring**, og vælg derefter handlingen **Massebogfør**.
6. Udfyld felterne efter behov på siden **Massebogfør købsordre**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Vælg knappen **OK**.
8. Hvis du vil have vist potentielle problemer, der er opstået under massebogføring af dokumenter, skal du åbne siden **Registrer over fejlmeddelelser**.

> [!NOTE]
> Det kan tage noget tid at bogføre flere dokumenter, og andre brugere vil blive blokeret. Overvej at aktivere baggrundsbogføring. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

## Sådan konfigureres baggrundsbogføring med opgavekøer
Opgavekøer er et effektivt værktøj til planlægning af kørsel af forretningsprocesser i baggrunden, f.eks. når mange brugere prøver at bogføre salgsordrer, men kun én ordre kan behandles ad gangen.  

Nedenstående fremgangsmåde beskriver, hvordan du konfigurerer baggrundsbogføring af salgsordrer. Trinnene er lignende for indkøb.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salgsopsætning**, og vælg derefter det relaterede link.
2. På siden **Salgsopsætning** skal du markere afkrydsningsfeltet **Bogfør med opgavekøen**.
3. Vælg feltet **Opgavekøkategorikode**, og angiv derefter koden **SALGSBOGF**.

    > [!NOTE]
    > Nogle job ændrer de samme data og bør ikke køres på samme tid, fordi det kan forårsage konflikter. Baggrundsopgaver for salgsdokumenter vil f.eks. forsøge at ændre de samme data på samme tid. Jobkøkategorier er med til at forhindre denne type konflikter ved at sikre, at et andet job, der tilhører den samme opgavekø, ikke køres, før den afsluttes. Et job, der tilhører en salgsjobkøkategori, vil f.eks. vente på, at alle andre salgsrelaterede job er udført. Du angiver en jobkøstrategi i oversigtspanelet **Baggrundsbogføring** på siden **Salgsopsætning**.
    >
    > [!INCLUDE[prod_short](includes/prod_short.md)] viser jobkøkategorier for salg, køb og bogføring i Finans. Det anbefales, at du altid angiver en af disse eller en af dem, du opretter. Hvis der opstår fejl pga. konflikter, skal du overveje at oprette en kategori for alle de forskellige salgs-, købs- og finanskladder.

    Hvis også salgsdokumenter skal udskrives, når de er bogført, skal du markere afkrydsningsfeltet **Bogfør og udskriv med opgavekøen** på siden **Salgsopsætning**.  
    Hvis du vælger **PDF** i feltet **Rapportresultattype**, er alle købsordrer, der er blevet bogført, tilgængelige i delen **Rapportindbakke** i rollecenteret.

    > [!IMPORTANT]  
    > Hvis du konfigurerer et opgave, der bogfører og udskriver dokumenter, og printeren viser en dialogboks, f.eks. en anmodning om legitimationsoplysninger eller en advarsel om næsten tom blækpatron, bogføres dit dokument, men det udskrives ikke. Den tilsvarende opgavekøpost får på et tidspunkt timeout og feltet **Status** indstilles til **Fejl**. Derfor anbefaler vi, at du ikke bruger en printeropsæting, der kræver interaktion med visningen af printerdialogbokse i forbindelse med baggrundsbogføring.

    Næste gang du bogfører salgsdokumenter, opretter [!INCLUDE [prod_short](includes/prod_short.md)] automatisk en opgavekøpost for hvert dokument, og der køres job i baggrunden, ét efter ét.

4. Du kan kontrollere, at opgavekøen fungerer som forventet ved at bogføre en salgsordre. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).
    Salgsordrerne føjes nu til en dedikeret opgavekøpost, der definerer, hvornår dokumenterne bliver bogført. 

### Sådan vises status fra et salgs- eller købsdokument
Hvis opgavekøen ikke kan bogføre salgsordren, ændres status til **Fejlmeddelelse**, og salgsordren føjes til listen over salgsordrer, som brugeren skal håndtere manuelt.
1. I det dokument, du har forsøgt at bogføre med baggrundsbogføring, skal du vælge feltet **Opgavekøstatus**, der indeholder **Fejl**.
2. Gennemgå fejlmeddelelsen, og løs problemet.

Du kan også gennemgå siden **Logposter i opgavekø**, hvis salgsordren blev bogført korrekt. Du kan finde flere oplysninger i afsnittet [Overvåge opgavekøen](#monitor-the-job-queue).

## Sådan oprettes en opgavekøpost for baggrundsbogføring af salgsordrer

Alternativt kan du udsætte posteringer, når det er belejligt for din organisation. F.eks. giver det måske mening i din virksomhed at køre visse rutiner, når de fleste af dataindtastningerne for den pågældende dag er afsluttede. Du kan opnå dette ved at indstille opgavekøen til at køre forskellige massebogføringsrapporter, f.eks. rapporterne **Massebogfør salgsordrer**, **Massebogfør salgsfakturaer** og lignende rapporter. [!INCLUDE[prod_short](includes/prod_short.md)] understøtter baggrundsbogføring for alle salg, køb og servicedokumenter.

Følgende procedure viser, hvordan du kan indstille rapporten **Massebogfør salgsordrer** til automatisk bogføring af salgsordrer kl. 16 på hverdage.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Poster for jobkøer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. I feltet **Objekttype, der skal aktiveres** skal du vælge **Rapport**.  
4. I feltet **Objekt-id, der skal køres** skal du vælge 296, **Massebogfør salgsordrer**.

   Du kan også bruge følgende rapporter:
  
   * 900 **Massebogfør montageordrer**
   * 497 **Massebogfør købsfakturaer**
   * 496 **Massebogfør købsordrer**
   * 498 **Massebogfør købskreditnotaer**
   * 6665 **Massebogfør købsreturv.ordrer**
   * 298 **Massebogfør salgskreditnotaer**
   * 297 **Massebogfør salgsfakturaer**
   * 296 **Massebogfør salgsordrer**
   * 6655 **Massebogfør salgsreturvareordrer**
   * 6005 **Massebogfør servicekreditnotaer**
   * 6004 **Massebogfør servicefakturaer**
   * 6001 **Kørsel - bogfør serviceordrer**

5. Marker **Siden Rapportanmodning** afkrydsningsfeltet.
6. På siden **Massebogfør salgsordrer** skal du definere, hvad der skal medtages under den automatiske bogføring af salgsordrer, og derefter vælge **OK** knappen.

    > [!IMPORTANT]
    > Husk at angive strenge filtre. Ellers vil [!INCLUDE [prod_short](includes/prod_short.md)] bogføre alle dokumenterne, selvom de ikke er klar. Overvej at angive et filter på feltet **Status** for værdien *Frigivet* og et filter på feltet **Bogføringsdato** for værdien *..i dag*. Du kan finde flere oplysninger i [Sortering, søgning og filtrering](ui-enter-criteria-filters.md).
7. Marker alle afkrydsningsfelter fra **Aktiver hver mandag** til og med **Aktiver hver fredag**.
8. I feltet **Starttidspunkt** skal du angive kl. 16.
9. Vælg handlingen **Angiv status til Klar**.

Salgsordrer, der falder inden for de definerede filtre, bogføres alle hverdage kl. 16.

## Overvåge opgavekøen

Hvis du konfigurerer baggrundsbogføring med opgavekøer, skal du gøre det til en fast opgave at overvåge opgavekøen for at fange eventuelle problemer. Du kan spore status på siden **Poster for opgavekøer**. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).  

Som administrator kan du bruge [Application Insights](/azure/azure-monitor/app/app-insights-overview) til at indsamle og analysere telemetri, som du kan bruge til at identificere problemer. Du kan finde flere oplysninger i [Overvågning og analyse af telemtri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) i indholdet til udviklere og administration.  

## Se også

[Bogføring af dokumenter og kladder](ui-post-documents-journals.md)  
[Du kan bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md)  
[Redigere bogførte dokumenter](across-edit-posted-document.md)  
[Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]