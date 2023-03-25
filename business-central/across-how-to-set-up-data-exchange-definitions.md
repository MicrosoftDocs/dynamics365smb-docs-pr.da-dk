---
title: 'Definere, hvordan data udveksles elektronisk'
description: 'Definer, hvordan Business Central-data udveksles med eksterne filer som elektroniske dokumenter, bankdata, varekataloger og meget mere.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.search.form: '1210, 1211, 1213, 1214, 1215, 1216, 1217'
ms.date: 11/03/2022
ms.author: bholtorf
---
# Konfigurere dataudvekslingsdefinitioner

Du kan indstille [!INCLUDE[prod_short](includes/prod_short.md)] til at udveksle data i bestemte tabeller med data på eksterne filer. Du kan f.eks. sende og modtage elektroniske dokumenter, importere og eksportere bankoplysninger eller andre data, f.eks. løn og varekataloger. Flere oplysninger i [Udveksle data elektronisk](across-data-exchange.md).  

Til oprettelse af en dataudvekslingsdefinition for en datafil eller -stream kan du bruge det relaterede XML-skema til at definere, hvilke dataelementer der skal indgå, i oversigtspanelet **Kolonnedefinitioner**. Se trin 6 i [Sådan beskrives formateringen af linjer og kolonner i filen](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Flere oplysninger i [Brug XML-skemaer til at forberede dataudvekslingsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Normalt angives dataudvekslingsdefinitioner på siden **Dataudvekslingsdefinition**. I forbindelse med opdatering af valutakurser er det imidlertid hurtigere at bruge en valutakursservice. Flere oplysninger i [Opdatere valutakurser](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

> [!NOTE]  
> Hvis den fil, der konverteres, er i XML-format, skal udtrykket *"kolonne"* i denne artikel fortolkes som et *"XML-element, der indeholder data"*.  

Denne artikel indeholder følgende procedurer:  

* Opret en dataudvekslingsdefinition.
* Eksportér en dataudvekslingsdefinition som en XML-fil, som andre kan bruge.
* Importér en XML-fil til en eksisterende dataudvekslingsdefinition.

## Oprette en dataudvekslingsdefinition

Opretter en dataudvekslingsdefinition, der omfatter to opgaver:  

1. På siden **Dataudvekslingsdefinition** skal du beskrive formateringen af linjer og kolonner i filen. Flere oplysninger i [Sådan beskrives formateringen af linjer og kolonner i filen](#formatlinescolumns).  
2. På siden **Dataudvekslingskobling** skal du knytte kolonner i datafilen til felter i [!INCLUDE[prod_short](includes/prod_short.md)]. Flere oplysninger i [Sådan tilknyttes kolonner i datafilen til felter i [!INCLUDE[prod_short](includes/prod_short.md)]](#mapfields).  

### <a name=formatlinescolumns></a>Sådan beskrives formateringen af linjer og kolonner i filen

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Dataudvekslingsdefinitioner** og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Brug oversigtspanelet **Generelt** til at beskrive dataudvekslingsdefinitionen og datafiltypen ved at udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Definition|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Angiv en kode, der identificerer dataudvekslingsdefinitionen.|  
    |**Navn**|Angiv et navn for dataudvekslingsdefinitionen.|  
    |**Filtype**|Angiv hvilken filtype, som dataudvekslingsdefinitionen bruges til. Du kan vælge mellem fire filtyper:<br /><br /> -   **XML**: Lagdelte strenge bestående af indhold og markeringer omgivet af koder, der angiver funktionen.<br />-   **Variabeltekst**: Poster har variabel længde og adskilles af et tegn, f.eks komma eller \-semikolon, også kaldet *afgrænset fil*.<br />-   **Fast tekst**: Poster har samme længde ved brug af numeriske tegn, og hver post er placeret på en separat linje, også kaldet *fil med fast bredde*.<br />- **JSON**: Lagdelte strenge bestående af indhold i JavaScript.|  
    |**Type**|Angiv, hvilken type forretningsaktiviteter dataudvekslingsdefinitionen bruges til, f.eks. **eksport af betaling**.|  
    |**Codeunit til datahåndtering**|Angiv den kodeenhed, der overfører data til og fra tabellerne i [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Valideringscodeunit**|Angiv den kodeenhed, der bruges til at validere data mod foruddefinerede forretningsregler.|  
    |**Læser/skriver codeunit**|Angiv den kodeenhed, der behandler importerede data før tilknytning og eksporterede data efter tilknytning.|  
    |**Læser/skriver XMLport**|Angiv den XMLport, hvor en importeret datafil eller tjeneste indsættes før tilknytning, og hvor de eksporterede data findes, når de skrives til en datafil eller tjeneste efter tilknytning.|  
    |**Codeunit til ekstern datahåndtering**|Angiv den kodeenhed, der overfører eksterne data ind og ud af dataudvekslingsstrukturen.|  
    |**Codeunit til brugerfeedback**|Angiv den kodeenhed, der udfører forskellige rensning efter tilknytning, f.eks markerer linjerne som eksporteret og sletter midlertidige poster.|  
    |**Filkodning**|Angiv kodning af filen. **Bemærk:** Dette felt er kun relevant for import.|  
    |**Kolonneseparator**|Angiv, hvordan kolonner adskilles i datafilen, hvis filen er af typen **Variabel tekst**.|  
    |**Antal linjer i filhoved**|Angiv, hvor mange hovedlinjer der findes i filen.<br /><br /> Dette sikrer, at sidehoveddataene ikke importeres. **Bemærk:** Dette felt er kun relevant for import.|  
    |**Identifikation af hovedlinje**|Hvis der findes en sidehovedlinje i flere positioner i filen, skal du indtaste teksten i den første kolonne på linjen i sidehovedet.<br /><br /> Dette sikrer, at sidehoveddataene ikke importeres. **Bemærk:** Dette felt er kun relevant for import.|  
    |**Identifikation af fodlinje**|Hvis der findes en sidefodslinje i flere positioner i filen, skal du indtaste teksten i den første kolonne på linjen i sidefoden.<br /><br /> Dette sikrer, at sidefodsdataene ikke importeres. **Bemærk:** Dette felt er kun relevant for import.|  

   > [!TIP]
   > Hvis du vil se, hvilke codeunits Microsoft bruger i eksisterende definitioner i standardproduktet, kan du gennemgå de tre **Codeunit** på siden **Feltkobling** i oversigtspanelet **Generelt** for hver definition.  

4. Brug oversigtspanelet **Linjedefinitioner** til at beskrive formatering af linjer i datafilen ved at udfylde felterne som beskrevet i følgende tabel.  

    > [!NOTE]  
    > I forbindelse med import af kontoudtog kan du kun oprette én linje for det enkelte format for bankkontoudtogsfilen, som du vil importere.  
    >
    > I forbindelse med eksport betalinger kan du oprette en linje for hver betalingstype, du vil eksportere. I så fald viser oversigtspanelet **Kolonnedefinitioner** forskellige kolonner for hver betalingstype.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Linjetype**|Angiver linjetypen i filen.|  
    |**Kode**|Angiv en kode, der identificerer linjen i filen.|  
    |**Navn**|Angiv et navn, der beskriver linjen i filen.|  
    |**Antal kolonner**|Angiv, hvor mange kolonner linjen i datafilen har. **Bemærk:** Dette felt er kun relevant for import.|  
    |**Identifikation af datalinje**|Angiv placeringen i det tilknyttede XML-skema for det element, der repræsenterer hovedposten i datafilen. **Bemærk:** Dette felt er kun relevant for import.|  
    |**Navneområde**|Angiv det navneområde, der forventes i filen, for at aktivere validering af navneområde. Du kan lade dette felt være tomt, hvis du ikke vil aktivere validering af navneområdet.|  
    |**Overordnet kode**|Angiv linjens overordnede, som vist i feltet **Kode** i tilfælde, hvor opsætningen af dataudvekslingen gælder filer med overordnede og underordnede poster såsom et bilagshoved og bilagslinjer.

5. Gentag trin 4 for at oprette en linje for hver type fildata, du vil eksportere.  

     Fortsæt til at beskrive formateringen af kolonner i datafilen ved at udfylde felterne i oversigtspanelet **Kolonnedefinitioner**, som beskrevet i nedenstående tabel. Du kan bruge strukturfilen, f.eks en .xsd-fil, så datafilen forhåndsudfylder oversigtspanelet med de relevante elementer. Flere oplysninger i [Brug XML-skemaer til at forberede dataudvekslingsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).

6. I oversigtspanelet **Kolonnedefinitioner** skal du vælge handlingen **Hent filstruktur**.  
7. På siden **Hent filstruktur** skal du vælge den relaterede strukturfil og derefter vælge **OK**. Linjerne i oversigtspanelet **Kolonnedefinitioner** udfyldes i overensstemmelse med datafilens struktur.  
8. Rediger eller udfyld felterne i oversigtspanelet **Kolonnedefinitioner** som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kolonnenr.**|Angiv det nummer, der afspejler kolonnens placering på linjen i filen.<br /><br /> For XML-filer, skal du angive det tal, der afspejler elementtypen i den fil, der indeholder dataene.|  
    |**Navn**|Angiv navnet på kolonnen.<br /><br /> For XML-filer skal du angive koden, der markerer de data, der skal udveksles.|  
    |**Datatype**|Angiv, om data, der skal udveksles, er af typen **Tekst**, **Dato** eller **Decimal**.|  
    |**Dataformat**|Angiv dataformatet, hvis relevant. Det kan f.eks. være **MM-dd-åååå**, hvis datatypen er **Dato**. **Bemærk:** Hvis du vil eksportere, skal du angive dataformatet i overensstemmelse med [!INCLUDE[prod_short](includes/prod_short.md)]. I forbindelse med import skal du angive dataformatet i overensstemmelse med .NET Framework. Der er flere oplysninger i [Standarddato- og tidsformatstrenge](/dotnet/standard/base-types/standard-date-and-time-format-strings).|  
    |**Dataformatering**|Angiv regionalt dataformat, hvis relevant. Det kan f.eks. være **en-US**, hvis datatypen er **Decimal**, så du sikrer, at komma bruges som .000-separator i henhold til det amerikanske format. Der er flere oplysninger i [Standarddato- og tidsformatstrenge](/dotnet/standard/base-types/standard-date-and-time-format-strings). **Bemærk:** Dette felt er kun relevant for import.|  
    |**Længde**|Angiv længden af fast bredde for linjen, der indeholder kolonnen, hvis datafilen er af typen **Fast tekst**.|  
    |**Beskrivelse**|Angiver en beskrivelse af kolonnen til orientering.|  
    |**Sti**|Angiv placeringen af elementet i det tilknyttede XML-skema.|  
    |**Identifikator for minustegn**|Angiv den værdi, der bruges i datafilen til at identificere negative beløb i datafiler, der ikke kan indeholde negative tegn. Dette id bruges derefter til at tilbageføre de identificerede beløb til negative tegn under import. **Bemærk:** Dette felt er kun relevant for import.|  
    |**Konstant**|Angiv de data, du vil eksportere i denne kolonne, som f.eks. ekstra oplysninger om betalingstypen. **Bemærk:** Dette felt er kun relevant for eksport.|  
    |**Tekstudfyldning påkrævet**|Angiv, at dataene skal omfatte tekstudfyldning.|  
    |**Udfyldningstegn**|Angiv tekstens udfyldningstegn.|  
    |**Justering**|Angiv, om kolonnejusteringen er til venstre eller højre.|  

9. Gentag trin 8 for hver kolonne eller hvert XML-element i den datafil, der indeholder data, du vil udveksle med [!INCLUDE[prod_short](includes/prod_short.md)].  

Det næste trin i oprettelsen af en definition til udveksling af data er at beslutte, hvilke kolonner eller XML-elementer i datafilen, der skal knyttes til hvilke felter i [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Den bestemte tilknytning afhænger af forretningsformålet med den datafil, der skal udveksles, og af lokale variationer. Selv SEPA-bankstandarden har lokale variationer. [!INCLUDE[prod_short](includes/prod_short.md)] understøtter import af SEPA CAMT-bankkontoudtogsfiler out\-of\-the\-box. Dette repræsenteres ved registreringskoden til dataudvekslingsdefinitionen **SEPA CAMT** på siden **Dataudvekslingsdefinitioner**. Du kan finde oplysninger om den specifikke felttilknytning for denne SEPA CAMT-understøttelse i [Feltkobling, når du importerer SEPA-CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md).  

### <a name=mapfields></a>Sådan tilknyttes kolonner i datafilen til felter i [!INCLUDE[prod_short](includes/prod_short.md)]

> [!TIP]
> Nogle gange er værdierne i de felter, du vil tilknytte, forskellige. For eksempel er sprogkoden for USA i én forretningsapp "U.S.", mens den i den anden er "US". Det betyder, at du skal transformere værdien, når du udveksler data. Dette sker gennem transformationsregler, som du definerer for felterne. Få mere at vide under [Transformationsregler](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

Fra og med 2022 udgivelsesbølge 2 kan du også gruppere efter et hvilket som helst felt, bruge nøgleindekset til at sortere resultaterne, og de nye transformations typer **Afrunding** og **Feltopslag**.

1. Brug oversigtspanelet **Linjedefinitioner** til at vælge den linje, du vil knytte kolonner til felter for, og vælg derefter **Feltkobling**. Siden **Dataudvekslingskobling** åbnes.  
2. På oversigtspanelet **Generelt** skal du angive tilknytningsopsætningen ved at udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Tabel-id**|Angiv den tabel, der indeholder felterne, til eller fra hvilke data udveksles i henhold til tilknytningen.|  
    |**Brug som midlertidig tabel**|Angiv, om den tabel, du vælger i feltet **Tabel-id**, er en midlertidig tabel, hvor de importerede data gemmes, før de knyttes til måltabellen.<br /><br /> Du kan bruge en midlertidige tabel, når dataudvekslingsdefinitionen bruges til at importere og konvertere elektroniske dokumenter, f.eks kreditorfakturaer til købsfakturaer i [!INCLUDE[prod_short](includes/prod_short.md)]. Flere oplysninger i [Udveksle data elektronisk](across-data-exchange.md).|  
    |**Navn**|Angiv et navn for tilknytningsopsætningen.|  
    |**Nøgleindeks**|Angiv det nøgleindeks, der sorterer kildeposterne inden eksport.|
    |**Codeunit til førtilknytning**|Angiv den kodeenhed, der klargør tilknytningen mellem felter i [!INCLUDE[prod_short](includes/prod_short.md)] og eksterne data.|  
    |**Koblings-codeunit**|Angiv den kodeenhed, der bruges til at knytte de angivne kolonner eller XML-dataelementer til felter i [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Codeunit til eftertilknytning**|Angiv den kodeenhed, der fuldfører tilknytningen mellem felter i [!INCLUDE[prod_short](includes/prod_short.md)] og eksterne data. **Bemærk:** Når AMC Banking 365 Fundamentals-udvidelsen anvendes, konverterer codeunit eksporterede data fra [!INCLUDE[prod_short](includes/prod_short.md)] til et generisk format, der er klar til eksport. I forbindelse med import konverterer kodeenheden eksterne data til et format, der er klar til import i [!INCLUDE[prod_short](includes/prod_short.md)].|
3. I oversigtspanelet **Feltkobling** kan du angive, hvilke kolonner der skal knyttes til hvilke felter i [!INCLUDE[prod_short](includes/prod_short.md)] ved at udfylde felterne som beskrevet i følgende tabeller, afhængigt af om feltet **Brug som midlertidig tabel** er aktiveret eller ej.  
   * Med funktionen **Brug som midlertidig tabel** slået fra:

     |Felt|Beskrivelse|  
     |--------------------------------- |---------------------------------------|  
     |**Kolonnenr.**|Angiv, hvilken kolonne i datafilen, som du vil definere en tilknytning til.<br /><br /> Du kan kun vælge de kolonner, der repræsenteres af linjer, i oversigtspanelet **Kolonnedefinitioner** på siden **Dataudvekslingsdefinition**.|
     |**Kolonnetitel**|Angiver titlen på kolonnen i den eksterne fil, der er tilknyttet feltet i feltet **Måltabel-id**, når du bruger en midlertidig tabel til dataimport.|
     |**Felt-id**|Angiv, hvilket felt kolonnen i feltet **Kolonnenr.** er tilknyttet.<br /><br /> Du kan kun vælge felter, der findes i den tabel, du angav i feltet **Tabel-id** i oversigtspanelet **Generelt**.|
     |**Felttitel**|Angiv titlen på feltet i den eksterne fil, der er tilknyttet feltet i feltet **Måltabel-id**, når du bruger en midlertidig tabel til dataimport.|
     |**Eventuelt**|Angiv, om tilknytningen skal ignoreres, hvis feltet er tomt. Hvis du ikke vælger denne indstilling, opstår der en fejl i eksporten, hvis feltet er tomt.|  
     |**Transformationsregel**|Angiv den regel, der omdanner importeret tekst til en understøttet værdi, før den kan knyttes til et angivet felt. Når du vælger en værdi i dette felt, angives den samme værdi i feltet **Transformationsregel** i feltet tilknytning af **Koblingsbuffer for feltet Dataudveksling**. og omvendt. Se næste afsnit for at få flere oplysninger om tilgængelige transformationsregler, der kan anvendes.|
     |**Overskriv værdi**|Angiv, at den aktuelle værdi overskrives af en ny værdi.|
     |**Prioritet**|Angiv den rækkefølge, som feltkoblingerne skal behandles i. Feltkoblingen med det højeste prioritetsnummer behandles først.|
     |**Multiplikator**|Angiv en multiplikator for numeriske data, herunder negative værdier.|

   * Med funktionen **Brug som midlertidig tabel** aktiveret:

     |Felt|Beskrivelse|  
     |---------------------------------|---------------------------------------|  
     |**Kolonnenr.**|Angiv, hvilken kolonne i datafilen, som du vil definere en tilknytning til.<br /><br /> Du kan kun vælge de kolonner, der repræsenteres af linjer, i oversigtspanelet **Kolonnedefinitioner** på siden **Dataudvekslingsdefinition**.|
     |**Kolonnetitel**|Angiver titlen på kolonnen i den eksterne fil, der er tilknyttet feltet i feltet **Måltabel-id**, når du bruger en midlertidig tabel til dataimport.|
     |**Måltabel-id**|Angiv den tabel, som værdien i feltet **Kolonnetitel** er knyttet til, når du bruger en midlertidig tabel til dataimport.|
     |**Tabeltitel**|Angiv navnet på den tabel i feltet **Måltabel-id**, som er den tabel, som værdien i feltet **Kolonnetitel** er knyttet til, når du bruger en midlertidig tabel til dataimport.|
     |**Målfelt-id**|Angiv det felt i måltabellen, som værdien i feltet **Kolonnetitel** er knyttet til, når du bruger en midlertidig tabel til dataimport.|
     |**Felttitel**|Angiv det navn i feltet i måltabellen, som værdien i feltet **Kolonnetitel** er knyttet til, når du bruger en midlertidig tabel til dataimport.|
     |**Validér kun**|Angiv, at element-til-feltkoblingen ikke bruges til at konvertere data, men kun til at validere data.|
     |**Transformationsregel**|Angiv den regel, der omdanner importeret tekst til en understøttet værdi, før den kan knyttes til et angivet felt. Når du vælger en værdi i dette felt, angives den samme værdi i feltet **Transformationsregel** i feltet tilknytning af **Koblingsbuffer for feltet Dataudveksling**. og omvendt. Se næste afsnit for at få flere oplysninger om tilgængelige transformationsregler, der kan anvendes.|
     |**Prioritet**|Angiv den rækkefølge, som feltkoblingerne skal behandles i. Feltkoblingen med det højeste prioritetsnummer behandles først.|

4. I oversigtspanelet **Feltgruppering** skal du angive de regler, du vil bruge til at gruppere felterne, når du opretter filen ved at udfylde felterne som beskrevet i følgende tabel.  

     |Felt|Beskrivelse|  
     |--------------------------------- |---------------------------------------|  
     |**Felt-id**|Angiv nummeret på det felt i den eksterne fil, der bruges til gruppering, og feltet skal angives af brugeren.|
     |**Felttitel**|Angiv titlen på feltet i den eksterne fil, der bruges til gruppering.|

## Transformationsregler

Hvis værdierne i de felter, du tilknytter, er forskellige, skal du bruge transformationsregler til dataudvekslingsdefinitioner for at gøre dem ens. Du kan definere transformationsregler for dataudvekslingsdefinitioner ved at åbne en eksisterende definition eller oprette en ny definition og derefter i oversigtspanelet **Linjedefinitioner** vælge **Administrer** og derefter **Felttilknytning**. Der findes foruddefinerede regler, men du kan også oprette dine egne. I følgende tabel beskrives de typer af transformationer, du kan udføre.

|Indstilling|Beskrivelse|
|---------|---------|
|**Store bogstaver**|Skriv alle bogstaver med stort.|
|**Små bogstaver**|Gør alle bogstaver små.|
|**Store eller små bogstaver i titel**|Skriv det første bogstav i hvert ord med stort.|
|**Trim**|Fjern tomme mellemrum før og efter værdien.|
|**Understreng**|Transformere en bestemt del af en værdi. Hvis du vil angive, hvor transformationen skal starte, skal du enten vælge en **Startposition** eller **Starttekst**. Startpositionen er et tal, som repræsenterer det første tegn, der skal transformeres. Startteksten er bogstavet umiddelbart før det bogstav, der skal udskiftes. Hvis du vil starte med det første bogstav i værdien, skal du bruge en startposition i stedet. Hvis du vil angive, hvor transformationen skal stoppes, skal du enten vælge **Længde**, hvilket er antallet af tegn der skal erstattes, eller **Sluttekst**, som er det tegn, der er umiddelbart efter det sidste tegn, der skal transformeres.|
|**Erstat**|Find en værdi, og erstat den med en anden. Denne transformation er nyttig til at erstatte simple værdier, f.eks. et bestemt ord.|
|**Regulært udtryk – erstat**|Brug et regulært udtryk som en del af en søg og erstat-handling. Denne transformation er nyttig til at erstatte flere eller måske mere komplekse værdier.|
|**Fjern tegn, der ikke er alfanumeriske**|Slet tegn, der ikke er bogstaver eller tal, f.eks. symboler eller specialtegn.|
|**Datoformatering**|Angiv, hvordan datoer skal vises. Du kan f.eks. transformere DD-MM-ÅÅÅÅ til ÅÅÅÅ-MM-DD.|
|**Formatering af decimaler**|Definer regler for placering af decimaler og afrundingspræcision.|
|**Regulært udtryk – match**|Brug et regulært udtryk til at finde en eller flere værdier. Denne regel ligner indstillingerne **Understreng** og **Regulært udtryk – Erstat**.|
|**Brugerdefineret**|Denne transformationsregel er en avanceret indstilling, der kræver assistance fra en udvikler. Den muliggør en integrationshændelse, som du kan abonnere på, hvis du vil bruge din egen transformationskode. Hvis du er udvikler og vil bruge denne indstilling, skal du se afsnittet nedenfor.|
|**Formatering af dato/klokkeslæt**|Definer, hvordan dags dato og tidspunktet på dagen skal vises.|
|**Feltopslag**|Brug felter fra forskellige tabeller. Hvis du vil bruge det, skal du følge nogle regler. Brug først **Tabel-id** til at angive id for den tabel, der indeholder posten til feltopslaget. Angiv derefter i feltet **ID for kildefelt** ID for feltet, der indeholder posten for feltopslaget. Angiv til sidst i feltet **ID for destinationsfelt** ID for feltet for at finde posten til feltopslaget. Du kan også bruge feltet **Feltopslagsregel** til at angive feltopslagets type. I forbindelse med feltet **Destination** bruges værdien fra **Destinationsfelt-id**, selvom feltet er tomt. Hvis **værdien i feltet er tom**, bruges den oprindelige værdi, hvis destinationen er tom.|
|**Afrund**|Afrund værdien i feltet ved hjælp af nogle yderligere regler. Først skal du angive en afrundingspræcision i feltet **Præcision**. Angiv derefter afrundingsretningen i feltet **Retning**.|

> [!NOTE]  
> Få mere at vide om formatering af dato og klokkeslæt i [Standarddato- og tidsformatstrenge](/dotnet/standard/base-types/standard-date-and-time-format-strings).

### Tip til udviklere: eksempel på brugerdefineret indstilling

Følgende eksempel viser, hvordan du implementerer din egen transformationskode.

```AL
codeunit 60100 "Hello World"
{
    [EventSubscriber(ObjectType::Table, Database::"Transformation Rule", 'OnTransformation', '', false, false)]
    procedure OnTransformation(TransformationCode: Code[20]; InputText: Text; var OutputText: Text)
    begin
        if TransformationCode = 'CUST' then
            OutputText := InputText + ' testing';
    end;
}
```

Når du har defineret dine regler, kan du teste dem. I oversigtspanelet **Test** skal du angive et eksempel på en værdi, du vil transformere, og derefter kontrollere resultaterne ved at vælge **Opdater**.

## Eksportere en dataudvekslingsdefinition som en XML-fil, som andre kan bruge

Når du har oprettet dataudvekslingsdefinitionen for en bestemt datafil, kan du eksportere dataudvekslingsdefinitionen som en XML-fil, som du kan importere. Denne opgave beskrives i følgende fremgangsmåde.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Dataudvekslingsdefinitioner** og vælg derefter det relaterede link.  
2. Vælg den dataudvekslingsdefinition, som du vil udlæse.  
3. Vælg handlingen **Eksporter dataudvekslingsdefinition**.  
4. Gem den XML-fil, der repræsenterer dataudvekslingsdefinitionen i en passende lokation.  

    Hvis en definition til udveksling af data allerede er oprettet, skal du kun importere XML-filen til Data Exchange Framework. Denne opgave beskrives i følgende fremgangsmåde.  

## Importere en eksisterende dataudvekslingsdefinition

1. Gem den XML-fil, der repræsenterer dataudvekslingsdefinitionen i en passende lokation.  
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Dataudvekslingsdefinitioner** og vælg derefter det relaterede link.  
3. Vælg handlingen **Importer dataudvekslingsdefinition**.  
4. Vælg den fil, du gemte i trin 1.  

## Se også

[Opsætning af dataudveksling](across-set-up-data-exchange.md)  
[Konfigurere afsendelse og modtagelse af elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)  
[Foretage betalinger med AMC Banking 365 Fundamentals-udvidelsen eller SEPA-kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Indgående bilag](across-income-documents.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
