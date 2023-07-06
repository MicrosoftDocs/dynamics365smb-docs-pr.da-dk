---
title: Konfigurere og bruge udvidelsen af Servicedeklaration
description: 'Få at vide, hvordan du opsætter og bruger Servicedeklaration (Intrastat for Services) og rapporterer servicehandel med virksomheder i andre EU-lande.'
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/21/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, service, declaration,'
ms.search.form: '30, 76, 5010, 5022, 5023, 5024, 5800'
---
# <a name="the-service-declaration-extension"></a><a name="the-service-declaration-extension"></a><a name="the-service-declaration-extension"></a>Udvidelsen af Servicedeklaration

I nogle EU-lande kræver myndigheder, at virksomheder rapporterer eksport af tjenester til andre EU-lande. Udvidelsen **Servicedeklaration** giver dig mulighed for at indsamle oplysninger om service handel i EU og rapportere det til myndighederne. Selvom der er navngivet **serviceerklæring**, kan du også bruge den som **Intrastat for services**. Dette lokalnummer er tilgængeligt for alle EU-lande som en W1-version, og den kan bruges i Belgien. For andre lande kræves der en landebaseret udvidelse. Hvis et land kun har brug for et andet format, kan du bruge rapport konfigurationen i **Data Exchange-strukturen** til at ændre formatet.

## <a name="enable-the-service-declaration-extension"></a><a name="enable-the-service-declaration-extension"></a><a name="enable-the-service-declaration-extension"></a>Aktivere udvidelsen af Servicedeklaration

Når du har installeret udvidelsen i dit miljø, skal du aktivere den.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Funktionsstyring**, og vælg derefter det relaterede link.
2. Find **Funktion: Aktiver brug af service erklæring (Intrastat for service)**, og vælg **Alle brugere** i feltet **Aktiveret for**. Få flere oplysninger om funktionsstyring i [Aktivering af kommende funktioner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management) i administrationsindholdet.
3. Når du aktiverer denne funktion, skal du følge trinene i installationsprocessen gennem guiden Installation. De fleste felter er skjult som standard.
4. Tilføj kun **servicetransaktionstyper** på andet trin ved at vælge siden **Åbn servicetransaktionstyper for at angive listen over koder** .
5. Inden du starter, skal du kontrollere det **samlede antal koder** for at forstå, hvor mange Services-transaktionstyper der allerede er angivet.
6. Vælg **Udfør** i sidste trin for at afslutte konfigurationen.

## <a name="set-up-the-service-declaration-extension"></a><a name="set-up-the-service-declaration-extension"></a><a name="set-up-the-service-declaration-extension"></a>Konfigurere udvidelsen af Servicedeklaration

Du kan konfigurere udvidelsen manuelt eller ved hjælp af en rapporteringsfil i definitioner af dataudveksling.

### <a name="to-set-up-service-declaration-manually"></a><a name="to-set-up-service-declaration-manually"></a><a name="to-set-up-service-declaration-manually"></a>Konfigurere servicedeklaration manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af Servicedeklaration**, og vælg derefter det relaterede link.
2. På oversigtspanelet **Generelt** skal du udfylde felterne som beskrevet i følgende tabel:

    |Felt  |Beskrivelse  |
    |---------|---------|
    |**Deklarationsnr. serie**     | Angiver den nummerserie, der skal bruges til at tildele id'er til nye poster.        |
    |**Rapportér varegebyrer**  | Angiver, om der skal rapporteres varegebyrer. Hvis dette er aktiveret, kontrollerer [!INCLUDE [prod_short](includes/prod_short.md)] servicetransaktionskoden for varegebyrer, og de medtages i serviceerklæringer.        |
    |**Sælg-til/fakturer-til-debitornr.**     | Angiver den debitor, der skal bruges til at sammenligne landekoden med landekoden på siden **Firmaoplysninger**. Det er kun dokumenter, hvor disse to koder er forskellige, som medtages i servicedeklarationen.<br><br>* **Fakturer til.**: Brug landekoden fra **faktura til kunde** <br<br>* **Sælg til.**: Brug landekoden fra **Sælg til kunde**.        |
    |**Køb-fra/betal-til-kreditornr.**  | Angiver den debitor, der skal bruges til at sammenligne landekoden med landekoden på siden **Firmaoplysninger**. Det er kun dokumenter, hvor disse to koder er forskellige, som medtages i servicedeklarationen.<br><br> * **Køb fra.**: Brug landekoden fra **Køb fra leverandør**. <br><br> * **Betal til.**: Brug landekoden fra **Betal til leverandør**.         |
    |**Definitionskode for dataudveksling**  | Angiver den dataudvekslingsdefinitionskode, der bruges til at generere den eksporterede fil for servicedeklarationen.        |
    |**Aktivér momsregistreringsnr.**     |  Angiver, om feltet **Tax Registration No.** er aktiveret for servicedeklarationen.       |

3. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Servicetransaktionstyper**, og vælg derefter det relaterede link.
4. Angiv **koder** og **beskrivelser** for de servicetransaktionstyper, du vil bruge, på linjerne.

### <a name="set-up-a-reporting-file"></a><a name="set-up-a-reporting-file"></a><a name="set-up-a-reporting-file"></a>Konfigurere en rapporteringsfil

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Dataudvekslingsdefinitioner**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Brug oversigtspanelet **Generelt** til at beskrive dataudvekslingsdefinitionen, datafiltypen, kolonneseparator, relaterede codeunits, XMLport og andre felter ved at udfylde felterne.
4. I oversigtspanelet **Linjedefinitioner** kan du beskrive formateringen af linjer i datafilen ved at udfylde felterne på grundlag af feltet **Linjetype**, og hvor du vil angive antallet af kolonner for denne linje.
5. Udfyld linjen for hver planlagt kolonne i oversigtspanelet **Kolonnedefinitioner**.
6. Vælg handlingen **Felttilknytning** i oversigtspanelet **Linjedefinitioner** for at åbne siden **Felttilknytning**.
7. Opret en ny post, og i oversigtspanelet **Generelt** skal du vælge det relevante **Tabel-id** (for **Servicedeklarationslinje** skal du vælge **5024**) og derefter udfylde flere felter:
   1. Angiv **nøgleindeks**, angiv nøgleindekset for at sortere kildeposterne inden eksport.
   2. Vælg den korrekte **Koblings-codeunit**.
8. Tilføj de kolonner, du tidligere har konfigureret i oversigtspanelet **Kolonnedefinitioner**, i oversigtspanelet **Felttilknytning**, og tilføj derefter følgende:
   1. Angiv **Felt-id** for hver kolonne.
   2. Angiv **Transformationsregel** for hver enkelt kolonne, du har brug for. Angiv den regel, der omdanner importeret tekst til en understøttet værdi, før den kan knyttes til et angivet felt i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du vælger en værdi i dette felt, angives den nøjagtige værdi i feltet **Transformationsregel** i feltet tabellen **Koblingsbuffer for feltet Dataudveksling** tabel og omvendt.
9. Hvis du har brug for at gruppere poster baseret på nogle kolonner, skal du i oversigtspanelet **Feltgruppering** vælge de felter, du vil bruge til gruppering.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] indeholder den forudkonfigurerede dataudvekslingsdefinition for **Serviceerklæring** Intrastat til alle lokaliserede lande/områder. Du kan finde flere oplysninger om oprettelse af en dataudvekslingsdefinition i artiklen [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

## <a name="other-related-configurations"></a><a name="other-related-configurations"></a><a name="other-related-configurations"></a>Andre relaterede konfigurationer

Inden du bruger udvidelsen serviceerklæringen, skal du konfigurere nogle felter for varer, ressourcer og varegebyrer.

### <a name="items"></a><a name="items"></a><a name="items"></a>Varer

Konfigurer oplysninger med relation til serviceerklæring på varekortsider:

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Varer**, og vælg derefter det relaterede link.
2. Vælg den vare, du vil konfigurere.
3. Udvid oversigtspanelet **Vare**, og udfyld derefter felterne:
   1. Vælg **Service** i feltet **Type**.
   2. Angiv en kode for **servicetransaktionstype** i feltet **servicetransaktionstypekode**.
   3. Hvis du ikke vil medtage denne serviceartikel i service erklæringer, skal du vælge feltet **Udeluk fra servicedeklaration** .

### <a name="resources"></a><a name="resources"></a><a name="resources"></a>Ressourcer

Konfigurer oplysninger med relation til serviceerklæring på Ressourcekortsider:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourcer**, og vælg derefter det relaterede link.
2. Vælg den ressource, du vil konfigurere.
3. Udvid oversigtspanelet **Generelt**, og udfyld derefter felterne:
   1. Angiv en kode for **servicetransaktionstype** i feltet **servicetransaktionstypekode**.
   2. Hvis du ikke vil medtage denne ressource i serviceerklæringer, skal du vælge feltet **Udeluk fra servicedeklaration** .

### <a name="item-charges"></a><a name="item-charges"></a><a name="item-charges"></a>Varegebyrer

Konfigurer oplysninger med relation til serviceerklæring på varegebyrer:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **varegebyrer**, vælg derefter det relaterede link.
2. Vælg det varegebyr, du vil konfigurere.
3. Angiv en kode for **servicetransaktionstype** i feltet **servicetransaktionstypekode**.
4. Hvis du ikke vil medtage dette varegebyr i serviceerklæringer, skal du vælge feltet **Udeluk fra servicedeklaration** .

## <a name="create-new-service-declaration"></a><a name="create-new-service-declaration"></a><a name="create-new-service-declaration"></a>Opret en ny serviceerklæring

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceerklæringer** og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld følgende felterne i oversigtspanelet **Generelt**.
    1. I feltet **Konfig. Kode** skal du angive den konfigurationskode, der skal bruges til at foreslå linjer og oprette filer. Du skal vælge én som **serviceerklæring**.
    2. I felterne **startdato** og **slutdato** skal du angive start--og slutdatoer for den periode, der skal medtages i serviceopgørelsen.
4. Vælg handlingen **Foreslå linjer** for at starte en kørsel, der samler linjer fra-bilag og udfylder linjerne i service rapporten.

Kørslen henter alle poster fra gældende købs-og salgsdokumenter i den krævede periode og indsætter dem på serviceerklæringslinjerne. Placer markøren over felterne på linjerne for at se en kort beskrivelse.

## <a name="modify-a-service-declaration"></a><a name="modify-a-service-declaration"></a><a name="modify-a-service-declaration"></a>Tilpas en serviceerklæring

Hvis det er nødvendigt, kan du ændre linjerne eller tilføje nye.

1. På siden **Serviceerklæring** skal du i oversigtspanelet **Linjer** vælge handlingen **Ny linje**.
2. Vælg den handling, du vil bruge, i feltet **Dokumenttype**.
3. Baseret på **Dokumenttype** skal du udfylde feltet **Dokumentnr.**.
4. Udfyld de resterende felter.

## <a name="overview-the-service-declaration-lines"></a><a name="overview-the-service-declaration-lines"></a><a name="overview-the-service-declaration-lines"></a>Oversigt over serviceerklæringslinjer

Når du har oprettet en service deklaration, skal du bruge handlingen **oversigt** til at få et overblik over linjerne i serviceerklæringen. Du kan gruppere og opsummere linjerne på samme måde som den eksporterede fil. Du kan også åbne linjerne i Excel.

## <a name="report-service-declaration-in-a-file"></a><a name="report-service-declaration-in-a-file"></a><a name="report-service-declaration-in-a-file"></a>Rapporten serviceerklæring i en fil

Du kan sende serviceerklæringen som en fil, der er baseret på andre lokale myndighedskrav. Sådan opretter du en fil:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Serviceerklæringer**, og vælg derefter det relaterede link.
2. Vælg den serviceerklæring, du vil rapportere som en fil.
3. Hvis du ikke allerede har gjort det, skal du udfylde serviceerklæringen manuelt eller vælge handlingen **Foreslå linjer**.
4. Vælg handlingen **Opret fil**.
5. Serviceerklæringen gemmes i det påkrævede format.

## <a name="other-considerations"></a><a name="other-considerations"></a><a name="other-considerations"></a>Andre overvejelser

Når du bruger filtypenavnet til **serviceerklæringen**, er der flere ting, du skal overveje. Det er f. eks. vigtigt, at dine grupper matcher kravene fra myndighederne. Det er også vigtigt, at tjenester er medtaget korrekt på salgs-og købsdokumenter.

### <a name="grouping-lines"></a><a name="grouping-lines"></a><a name="grouping-lines"></a>Gruppering af linjer

På serviceerklæringslinjerne er der ingen af felterne, der er grupperet efter. Alle poster kopieres fra det oprindelige dokument som en kilde.

Gruppering, der kræves af myndighederne, leveres i den eksporterede fil. Du skal konfigurere grupperne i **dataudvekslingsdefinitionen**, som kan konfigureres med det hele. Flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

### <a name="using-services-in-document-lines"></a><a name="using-services-in-document-lines"></a><a name="using-services-in-document-lines"></a>Bruge servicer i dokumentlinjer

Når du opretter en købs-, salgs eller servicefaktura, finder du to felter med relation til serviceerklæringer på deres linjer. Begge felter udfyldes med standardværdierne fra din vare, ressource eller varegebyropsætning.

- Angiv en kode for servicetransaktionstype i feltet **Servicetransaktionstypekode**.
- **Gælder for serviceerklæring** - Angiver, om en vare eller ressource gælder for en servicedeklaration.

Du kan ændre værdierne i disse felter, men hvis du markerer feltet **Gælder for serviceerklæring**, skal du angive en værdi i feltet **Servicetransaktionstypekode** . Hvis du ikke gør det, kan du ikke sende dokumentet.

Hvis du angiver en værdi i feltet **Servicetransaktionstypekode**, men ikke vælger feltet **Gælder for serviceerklæring** kan du bogføre dokumentet, men linjen bliver ikke beregnet.

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Oprette Intrastat-rapportering](finance-how-setup-report-intrastat.md)
[Intrastat-rapportering i Business central](finance-how-report-intrastat.md)  
[Økonomistyring](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
