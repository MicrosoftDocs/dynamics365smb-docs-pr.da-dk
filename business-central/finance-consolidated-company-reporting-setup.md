---
title: Konfigurere virksomhedskonfiguration
description: Få mere at vide om, hvordan du kan konfigurere, hvordan data fra forskellige firmaer i Business Central skal rapporteres til et konsolideret regnskab.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.search.form: 1826, 1827
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 453cebcddb1fdfd2f3127fd08548deccc8fe1876
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512200"
---
# <a name="set-up-company-consolidation"></a>Konfigurere virksomhedskonsolidering

Før du kan konsolidere finansposterne fra to eller flere separate regnskaber (datterselskaber) til et konsolideret regnskab, skal du forberede kontoplanerne og det konsoliderede regnskab.  

Afhængigt af kompleksiteten af virksomhederne kan konsolideringen konfigureres på to måder:

* Hvis du ikke har brug for avancerede indstillinger, f.eks. inklusion af et regnskab, som du kun er en del af, kan du bruge den assisterede opsætningsvejledning **Virksomhedskonsolidering** til hurtigt at oprette en konsolidering. Guiden hjælper dig gennem de grundlæggende trin.
* Hvis du har brug for mere avancerede indstillinger, kan du oprette det konsoliderede regnskab og koncernvirksomhederne selv.
  * I hver koncernvirksomhed skal du angive, hvilke finanskonti der skal indgå i konsolideringen samt konsolideringstransaktionsmetoden for hver konto.
  * I det konsoliderede regnskab skal du konfigurere et koncernvirksomhedskort for hvert regnskab, der skal medtages i konsolideringen. Dette kort indeholder oplysninger som f.eks. datoerne for koncernvirksomhedens regnskabsår, den procent af hvert regnskab, der skal indgå i konsolideringen og den version af , som koncernvirksomheden er registreret i.

## <a name="simple-consolidation-setup"></a>Simpel konsolideringsopsætning

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]
Hvis din konsolidering er enkel, f.eks. fordi du er eneejer af de koncernvirksomheder, der skal konsolideres, hjælper den assisterede opsætningsvejledning **Virksomhedskonsolidering** dig gennem følgende trin:

* Vælg, om du vil oprette et nyt konsolideret regnskab, eller om du vil konsolidere data i et regnskab, som du allerede har oprettet til konsolideringen. Regnskabet må ikke indeholde transaktioner.
* Få vist resultaterne. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer, at masterdata og transaktioner kan overføres til det konsoliderede regnskab.

Hvis du vil bruge den assisterede opsætningsvejledning, skal du gøre følgende:

1. I Rollecenteret **Bogholder** skal du vælge handlingen **Assisteret opsætning**.
2. Vælg **Konfigurer konsolideringsrapportering**, og udfør derefter de enkelte trin i den assisterede opsætningsvejledning.

## <a name="advanced-consolidation-setup"></a>Avanceret konsolideringskonfiguration

Hvis du har brug for mere avancerede indstillinger til din konsolidering, kan du oprette konsolideringen manuelt. Hvis du f.eks. har virksomheder, som du kun ejer delvist, eller virksomheder, som du ikke vil have med i konsolideringen.  

### <a name="set-up-the-consolidated-company"></a>Konfigurere det konsoliderede regnskab

Du skal først konfigurere den konsoliderede virksomhed. Du opretter det konsoliderede regnskab på samme måde, som du opretter andre regnskaber. Du kan finde flere oplysninger i [Blive klar til at handle](ui-get-ready-business.md).  

Følgende liste illustrerer nøgleaspekter i det konsoliderede regnskab.

1. Konfigurere kontoplanen

    Du kan finde flere oplysninger i [Konfigurere eller ændre kontoplanen](finance-setup-chart-accounts.md).  

    Kontoplanerne kan være identiske på tværs af en koncernvirksomhed og i det konsoliderede regnskab, eller det konsoliderede regnskab kan have en anden kontoplan. Hvis en koncernvirksomheds kontoplan er forskellig fra den i det konsoliderede regnskab, skal du angive tilknytningen mellem konti på kontiene i koncernvirksomheden. Du kan finde flere oplysninger i afsnittet [Forberede finanskonti til konsolidering](#glacc).

2. Tilføj virksomhedsenheder

    Hvis du vil konsolidere flere regnskabers finansielle data i et konsolideret regnskab, skal du skrive oplysninger om de datterselskaber som koncernvirksomheder, der skal medtages, og om, hvilke tal der skal medtages.

    Du kan finde flere oplysninger i afsnittet [Tilføj afdelinger](#busunit).
3. Du kan angive valutakurser, når du konsoliderer regnskabsopgørelsen for koncernvirksomhederne, hvis den er i en udenlandsk valuta.

    De tre valutakurser, som bruges, er **Gennemsnitskurs (manuel)**, **Ultimokurs** og **Sidste ultimokurs**. Du kan finde flere oplysninger i afsnittet [Angiv valutakurser for konsolidering](#exchrates).
4. Du kan konsolidere dimensionsoplysninger og finanskonti.

    Du kan finde flere oplysninger i afsnittet [Medtag og udeluk dimensioner](#dim).

### <a name="add-business-units"></a><a name="busunit"></a>Tilføj virksomhedsenheder

[!INCLUDE[prod_short](includes/prod_short.md)] giver dig mulighed for at oprette en liste over de virksomhedsenheder, der skal konsolideres, kontrollere regnskabsdataene, før du konsoliderer dem, importere filer og oprette konsolideringsrapporter.  

1. Log på det konsoliderede regnskab.
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forretningsenheder**, og vælg derefter det relaterede link.  
3. Vælg **Ny**, og udfyld de påkrævede felter. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Når du udfylder felterne **Startdato** og **Slutdato**, skal du kontrollere, at du overholder GAAP-regler for regnskabsperioderne for koncernvirksomheden kontra moderselskabet.
4. Gentag trin 3 for hver yderligere afdeling

Hvis koncernvirksomheden bruger en fremmed valuta, skal du angive kursen, der skal anvendes i konsolideringen. Du skal også angive konsolideringsoplysninger om koncernvirksomhedens finanskonti. Disse processer beskrives i de følgende afsnit.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Klargøre finanskonti til konsolidering

Kontoplanen for en virksomhed, der skal konsolideres, skal angive konti for konsolidering. Du skal angive den finanskonto i det konsoliderede regnskab, som saldoen skal overføres til ved konsolideringen, for alle bogføringsfinanskonti i de enkelte regnskaber. Dette er en tilknytning, som gør det muligt at konsolidere regnskaber med forskellige kontoplaner.

Hvis kontoplanen i koncernvirksomheden er anderledes end det konsoliderede regnskab, skal du forberede finanskonti til konsolidering. Du kan angive de konti, hvor debet og kredit skal posteres, og metoden, der skal bruges til at oversætte valutaer i det konsoliderede regnskab. Det er f.eks. nyttigt, hvis du ofte udfører rapporten.

1. I de enkelte koncernvirksomheder [!INCLUDE [prod_short](includes/prod_short.md)] skal du vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
2. Åbn kortet for kontoen, og udfyld derefter felterne på oversigtspanelet **Konsolidering**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a>Angiv kurser for konsolideringer

Hvis en koncernvirksomhed bruger en anden valuta end det konsoliderede regnskab, skal du angive valutakursmetoder for hver konto, før du konsoliderer. For hver konto bestemmer indholdet af feltet **Konsol. oversættelsesmetode** valutakursen. I den konsoliderede virksomhed skal du for hvert koncernvirksomhedskort angive i feltet **Valutakurstabel**, om konsolideringen skal bruge valutakurser fra koncernvirksomhedens regnskab eller det konsoliderede regnskab. Hvis du bruger valutakurser fra det konsoliderede regnskab, kan du ændre kurserne for en koncernvirksomhed. For koncernvirksomheder gælder: Hvis der i feltet **Valutakurstabel** på koncernvirksomhedskortet står **Lokal**, kan du ændre valutakursen fra koncernvirksomhedskortet. Valutakurserne kopieres fra tabellen **Valutakurs**, men du kan ændre dem inden kosolideringen.

I følgende tabel beskrives de valutakursmetoder, du kan bruge til konti.

|Valutakurs | Typisk anvendelse |
|---|---|
|Gennemsnitskurs (manuel) | Du kan manuelt beregne den gennemsnitlige kurs for konsolideringsperioden. Beregn enten gennemsnittet som et aritmetisk gennemsnit eller som et kvalificeret estimat, og angiv resultatet for hver koncernvirksomhed. Bruges til resultatopgørelseskonti.|
|Ultimokurs | Bruges til konti på balancen.|
|Sidste ultimokurs | Den gældende kurs på valutamarkedet på den dato, hvor balancen eller resultatopgørelsen udarbejdes. Angiv denne kurs for hver koncernvirksomhed. Bruges til konti på balancen.|
|Historisk kurs | Den valutakurs, der var gældende, da transaktionen fandt sted.|
|Sammensat kurs | Beløbene i den aktuelle periode oversættes til gennemsnitskursen og føjes til den tidligere registrerede balance i det konsoliderede regnskab. Denne metode bruges typisk til resultatkonti, fordi disse omfatter beløb overført fra forskellige perioder og derfor er sammensat af beløb, der er oversat med forskellige valutakurser.|
|Aktiekurs | Dette svarer til **sammensat**. Differencerne bogføres på separate finanskonti.|

Gør følgende for at angive valutakurser for koncernvirksomheder:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forretningsenheder**, og vælg derefter det relaterede link.  
2. Vælg koncernvirksomheden på siden **Koncernvirksomhedsoversigt**, og vælg derefter handlingen **Gennemsnitskurs (manuel)**.  
3. På siden **Ret valutakurs** er indholdet af feltet **Associeret valutakurs** blevet kopieret fra tabellen **Valutakurs**, men du kan ændre oplysningerne efter behov. Luk siden.  
4. Vælg handlingen **Ultimokurs**.  
5. I feltet **Associeret valutakursbeløb** skal du angive valutakursen.

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Medtag eller Udelad dimensioner

Du kan konsolidere dimensionsoplysninger og finanskonti.

* Angiv feltet **Konsolideringskode** i de relevante dimensioner, eller lad feltet være tomt
  * Hvis du vil udelade en dimension i konsolideringen, skal **du lade feltet Konsolideringskode** være tomt for dimensionen og ikke vælge dimensioner i felterne **Kopier dimensioner** i nogen af konsolideringsfunktionerne eller -rapporterne.
  * Hvis du vil medtage dimensionsoplysninger i konsolideringen, skal feltet **Konsolideringskode** være tomt. Men konsolideringen vil kun fungere, hvis dimensionsværdierne i koncernvirksomheden er de samme som i det konsoliderede regnskab.
  * Du skal kun udfylde feltet **Konsolideringskode**, når dimensionsværdikoden i koncernvirksomheden skal anses som værende forskellig fra dimensionsværdikoden i det konsoliderede regnskab.  
* Føj de relevante dimensioner til de relevante finanskonti

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Udelukke en virksomhed fra konsolideringen

Hvis du ikke vil medtage en koncernvirksomhed i konsolideringen, kan du udelukke den. Gå til koncernvirksomhedskortet for at gøre dette, og fjern markeringen af afkrydsningsfeltet **Konsolideres**.

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Inkludere en delvis ejet virksomhed i konsolideringen

Hvis du kun ejer en del af en virksomhed, kan du medtage en procentdel af hver transaktion, der svarer til den procentdel af virksomheden, du ejer. Hvis du f.eks. ejer 70 % af virksomheden, inkluderer konsolideringen $70 af en faktura på $100. Du angiver den procentdel af virksomheden, du ejer, ved at gå til koncernvirksomhedskortet og angive procentdelen i feltet **Konsolideringspct.**.  

## <a name="see-also"></a>Se også

[Konsolidering af finansielle oplysninger fra flere regnskaber](finance-consolidated-company-reporting.md)  
[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eksportere forretningsdata til Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]