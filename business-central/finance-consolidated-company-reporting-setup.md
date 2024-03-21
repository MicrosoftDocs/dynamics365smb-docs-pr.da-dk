---
title: Konfigurere virksomhedskonfiguration
description: 'Få mere at vide om, hvordan du kan konfigurere, hvordan data fra forskellige firmaer i Business Central skal rapporteres til et konsolideret regnskab.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 09/25/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# Konfigurere virksomhedskonsolidering

Før du kan konsolidere finansposterne fra to eller flere regnskaber (datterselskaber) til et konsolideret regnskab, skal du forberede kontoplanerne og det konsoliderede regnskab.  

Afhængigt af kompleksiteten af virksomhederne kan konsolideringen konfigureres på to måder:

* Hvis du ikke har brug for avancerede indstillinger, f.eks. inklusion af et regnskab, som du kun er en del af, kan du bruge opsætningsvejledningen **Virksomhedskonsolidering** til hurtigt at oprette en konsolidering. Guiden hjælper dig gennem de grundlæggende trin.
* Hvis du har brug for mere avancerede indstillinger, kan du oprette det konsoliderede regnskab og koncernvirksomhederne selv.
  * I hver koncernvirksomhed skal du angive, hvilke finanskonti der skal indgå i konsolideringen samt konsolideringstransaktionsmetoden for hver konto.
  * Oprette et koncernvirksomhedskort i det konsoliderede regnskab for hvert regnskab, der skal medtages i konsolideringen. Dette kort indeholder oplysninger som f.eks. datoerne for koncernvirksomhedens regnskabsår, den procent af hvert regnskab, der skal indgå i konsolideringen.

## Simpel konsolideringsopsætning

Hvis din konsolidering er enkel, f.eks. fordi du er eneejer af de koncernvirksomheder, der skal konsolideres, hjælper den assisterede opsætningsvejledning **Virksomhedskonsolidering** dig gennem følgende trin:

* Oprette et nyt konsolideret regnskab eller konsolidere et regnskab, du allerede har oprettet. Regnskabet må ikke indeholde transaktioner.
* Få vist resultaterne. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer, at du kan overføre masterdata og transaktioner til det konsoliderede regnskab.

Hvis du vil bruge den assisterede opsætningsvejledning, skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Assisteret opsætning** og vælg derefter det relaterede link.
2. Vælg **Behandl konsolideringer**, og udfør derefter de enkelte trin i den assisterede opsætningsvejledning for firmakonsolidering.

## Avanceret konsolideringskonfiguration

Hvis du har brug for mere avancerede indstillinger til din konsolidering, kan du oprette konsolideringen manuelt. Hvis du f.eks. har virksomheder, som du kun ejer delvist, eller virksomheder, som du ikke vil have med i konsolideringen.  

### Konfigurer det konsoliderede regnskab

Du skal først konfigurere den konsoliderede virksomhed. Du opretter det konsoliderede regnskab på samme måde, som du opretter andre regnskaber. Du kan få mere at vide om, hvordan du konfigurerer en virksomhed, ved at gå til [Bliv klar til at gøre forretninger](ui-get-ready-business.md).  

Følgende liste illustrerer nøgleaspekter i det konsoliderede regnskab.

1. Konfigurere kontoplanen.

    Få mere at vide om oprettelse af kontoplanen ved at gå til [Konfigurere eller ændre kontoplaner](finance-setup-chart-accounts.md).  

    Kontoplanerne kan være identiske på tværs af en koncernvirksomhed og i det konsoliderede regnskab, eller det konsoliderede regnskab kan have en anden kontoplan. Hvis en koncernvirksomheds kontoplan er forskellig fra den i det konsoliderede regnskab, skal du angive tilknytningen mellem konti på kontiene i koncernvirksomheden. Du kan finde flere oplysninger i afsnittet [Forberede finanskonti til konsolidering](#glacc).

2. Tilføj virksomhedsenheder.

    Hvis du vil konsolidere flere regnskabers data, skal du oprette datterselskaberne som koncernvirksomheder og angive, hvor stor en del af deres saldi der skal medtages. Du kan få mere at vide om koncernvirksomheder ved at gå [til afsnittet Tilføj koncernvirksomheder](#busunit).

3. Angiv valutakurser, hvis det er nødvendigt.

    Angiv valutakurser, hvis du vil konsolidere data for koncernvirksomheder, der bruger forskellige valutaer. De tre valutakurser, som bruges, er **Gennemsnitskurs (manuel)**, **Ultimokurs** og **Sidste ultimokurs**. Du kan få mere at vide om valutakurser i afsnittet [Angiv valutakurser for konsolideringer](#exchrates).

4. Du kan konsolidere dimensionsoplysninger og finanskonti.

    Du kan finde flere oplysninger i afsnittet [Medtag og udeluk dimensioner](#dim).

### <a name="busunit"></a>Tilføj virksomhedsenheder

Oprette (i det konsoliderede regnskab) et koncernvirksomhedskort for hvert regnskab, der skal medtages i konsolideringen. Før du udfører en konsolidering og genererer konsolideringsrapporten, er det en god ide at kontrollere de økonomiske data i hver enkelt koncernvirksomhed.

En stor del af opsætningen af koncernvirksomheden er at angive, hvordan enheden skal dele sine finansielle data med det konsoliderede regnskab. Der er manuelle og automatiserede indstillinger:

* Hvis du vil bruge en manuel proces til [!INCLUDE [prod_short](includes/prod_short.md)] online og lokalt, kan du eksportere en .xml-fil, der indeholder enhedens finansposter. Derefter skal du importere filen i det konsoliderede regnskab.
* Hvis du vil automatisere dataudvekslingen, kan du for [!INCLUDE [prod_short](includes/prod_short.md)] online bruge en API, der [!INCLUDE [prod_short](includes/prod_short.md)] giver mulighed for at dele data på tværs af miljøer. Hvis regnskaberne befinder sig i det samme miljø, kan du bruge indstillingen **Database**.

> [!NOTE]
> API-indstillingen giver dig også mulighed for at dele finansposter fra andre [!INCLUDE [prod_short](includes/prod_short.md)]-miljøer. Hvis du vil bruge API-indstillingen, skal den bruger, der konfigurerer konsolideringen, have tilladelse til at få adgang til finansposter. Tilladelsessættene D365 Basic og D365 Read giver f.eks. adgang.

1. Log på det konsoliderede regnskab.
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forretningsenheder**, og vælg derefter det relaterede link.  
3. Vælg handlingen **Ny handling**, og udfyld felterne på oversigtspanelerne **Generelt** og **Finanskonti** efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Når du udfylder felterne **Startdato** og **Slutdato**, skal du kontrollere, at du overholder GAAP-regler for regnskabsperioderne for koncernvirksomheden kontra moderselskabet.
4. I oversigtspanelet **Dataimport** skal du i feltet **Standarddataimport** angive, hvordan du vil dele finansposter med det konsoliderede regnskab:

   * Hvis du vil dele data mellem firmaer i det samme miljø, skal du vælge **Database**.
   * Hvis du vil dele data mellem virksomheder i forskellige miljøer, skal du vælge **API** og derefter udfylde feltet **Slutpunkt for API**.
        
        Hvis du vil hente URL-adressen til slutpunktet i koncernvirksomhedsfirmaet [!INCLUDE [prod_short](includes/prod_short.md)], skal du åbne siden **Koncernvirksomhedskort** og vælge handlingen **Opsætning**. 
   * Hvis du vil eksportere en .xml-fil og dele den manuelt, skal du vælge **Filformat**.

### <a name="glacc"></a>Klargøre finanskonti til konsolidering

Kontoplanen for et regnskab, der skal konsolideres, skal angive konti for konsolidering. Du skal angive den finanskonto i det konsoliderede regnskab, som saldoen skal overføres til ved konsolideringen, for alle bogføringsfinanskonti i de enkelte regnskaber. Med denne tilknytning kan du konsolidere regnskaber med forskellige kontoplaner.

Hvis kontoplanen i koncernvirksomheden er anderledes end det konsoliderede regnskab, skal du forberede finanskonti til konsolidering. Du kan angive de konti, hvor debet og kredit skal posteres, og metoden, der skal bruges til at oversætte valutaer i det konsoliderede regnskab.

1. I de enkelte koncernvirksomheder [!INCLUDE [prod_short](includes/prod_short.md)] skal du vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
2. Åbn kortet for kontoen, og udfyld derefter felterne på oversigtspanelet **Konsolidering**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="exchrates"></a>Angiv kurser for konsolideringer

Hvis en koncernvirksomhed bruger en anden valuta end det konsoliderede regnskab, skal du angive valutakursmetoder for hver konto, før du konsoliderer. For hver konto bestemmer indholdet af feltet **Konsol. oversættelsesmetode** valutakursen. I den konsoliderede virksomhed skal du for hvert koncernvirksomhedskort angive i feltet **Valutakurstabel**, om konsolideringen skal bruge valutakurser fra koncernvirksomhedens regnskab eller det konsoliderede regnskab. Hvis du bruger valutakurser fra det konsoliderede regnskab, kan du ændre kurserne for en koncernvirksomhed. For koncernvirksomheder gælder: Hvis der i feltet **Valutakurstabel** på koncernvirksomhedskortet står **Lokal**, kan du ændre valutakursen fra koncernvirksomhedskortet. Valutakurserne kopieres fra tabellen **Valutakurs**, men du kan ændre dem inden kosolideringen.

I følgende tabel beskrives de valutakursmetoder, du kan bruge til konti.

|Valutakurs | Typisk anvendelse |
|---|---|
|Gennemsnitskurs (manuel) | Du kan manuelt beregne den gennemsnitlige kurs for konsolideringsperioden. Beregn enten gennemsnittet som et aritmetisk gennemsnit eller som et kvalificeret estimat, og angiv resultatet for hver koncernvirksomhed. Bruges til resultatopgørelseskonti.|
|Ultimokurs | Bruges til konti på balancen.|
|Sidste ultimokurs | Den gældende kurs på valutamarkedet på den dato, hvor balancen eller resultatopgørelsen udarbejdes. Angiv denne kurs for hver koncernvirksomhed. Brug til konti på balancen.|
|Historisk kurs | Den valutakurs, der var gældende, da transaktionen fandt sted.|
|Sammensat kurs | Beløbene i den aktuelle periode oversættes til gennemsnitskursen og føjes til den tidligere registrerede balance i det konsoliderede regnskab. Du bruger typisk denne metode til resultatkonti. Disse konti indeholder beløb fra forskellige perioder, så de indeholder beløb, der er oversat med forskellige valutakurser.|
|Aktiekurs | Dette svarer til **sammensat**. Differencerne bogføres på separate finanskonti.|

Gør følgende for at angive valutakurser for koncernvirksomheder:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forretningsenheder**, og vælg derefter det relaterede link.  
2. Vælg koncernvirksomheden på siden **Koncernvirksomhedsoversigt**, og vælg derefter handlingen **Gennemsnitskurs (manuel)**.  
3. På siden **Ret valutakurs** er indholdet af feltet **Associeret valutakurs** blevet kopieret fra tabellen **Valutakurs**, men du kan ændre oplysningerne efter behov. Luk siden.  
4. Vælg handlingen **Ultimokurs**.  
5. I feltet **Associeret valutakursbeløb** skal du angive valutakursen.

### <a name="dim"></a>Medtag eller Udelad dimensioner

Du kan konsolidere dimensionsoplysninger og finanskonti.

* Angiv feltet **Konsolideringskode** i de relevante dimensioner, eller lad feltet være tomt.
  * Hvis du vil udelade en dimension i konsolideringen, skal **du lade feltet Konsolideringskode** være tomt for dimensionen og ikke vælge dimensioner i felterne **Kopier dimensioner** i nogen af konsolideringsfunktionerne eller -rapporterne.
  * Hvis du vil medtage dimensionsoplysninger i konsolideringen, skal feltet **Konsolideringskode** være tomt. Men konsolideringen vil kun fungere, hvis dimensionsværdierne i koncernvirksomheden er de samme som i det konsoliderede regnskab.
  * Du skal kun udfylde feltet **Konsolideringskode**, når dimensionsværdikoden i koncernvirksomheden skal anses som værende forskellig fra dimensionsværdikoden i det konsoliderede regnskab.  
* Føj de relevante dimensioner til de relevante finanskonti.

### <a name="exclude"></a>Udelukke en virksomhed fra konsolideringen

Hvis du ikke vil medtage en koncernvirksomhed i konsolideringen, kan du udelukke den. Gå til koncernvirksomhedskortet for at gøre dette, og fjern markeringen af afkrydsningsfeltet **Konsolideres**.

### <a name="include"></a>Inkludere en delvis ejet virksomhed i konsolideringen

Hvis du kun ejer en del af en virksomhed, kan du medtage en procentdel af hver transaktion, der afspejler til den procentdel, du ejer. Hvis du f.eks. ejer 70 % af virksomheden, inkluderer konsolideringen $70 af en faktura på $100. Du angiver den procentdel af virksomheden, du ejer, ved at gå til koncernvirksomhedskortet og angive procentdelen i feltet **Konsolideringspct.**.  

## Se også

[Konsolidering af finansielle oplysninger fra flere regnskaber](finance-consolidated-company-reporting.md)  
[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eksportere forretningsdata til Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]