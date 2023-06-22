---
title: Se tabeloplysninger
description: 'Få mere at vide om, hvordan du kan få vist oplysninger om databasetabeller i Business Central.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 8700
ms.date: 08/23/2022
ms.author: jswymer
---

# <a name="viewing-table-information" />Sådan ser du tabeloplysninger

Siden **8700-tabeloplysninger** indeholder oplysninger om antallet af poster i alle system-og forretningstabeller i [!INCLUDE[prod_short](includes/prod_short.md)], og hvor mange data tabellen indeholder.

Disse oplysninger kan være nyttige til fejlfinding i forbindelse med ydeevnen, da du kan se fordelingen af datastørrelse på tværs af tabeller.

## <a name="viewing-table-information" />Sådan ser du tabeloplysninger

Hvis du vil åbne denne side, skal du vælge ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") ikon, åbn **Tabeloplysninger**, og vælg derefter det relaterede link.

Følgende tabel indeholder en beskrivelse af de oplysninger, der er angivet for hver tabel:

|Kolonne|Description|
|------|-----------|
|Virksomhedsnavn|Navnet på den virksomhed, som tabellen tilhører (hvis det er relevant).|
|Tabelnavn|Navnet på tabellen.|
|Tabel-nr.|Tabellens ID.|
|Nej Poster|Det samlede antal poster, der er gemt i tabellen.|
|Poststørrelse|Den gennemsnitlige poststørrelse i KB/post. Værdien beregnes ved hjælp af følgende formel: 1024 (størrelse)/(antal poster). |
|Størrelse (KB)|Samlet mængde plads, som tabellen optager i databasen. Denne værdi er summen af værdierne i felterne Datastørrelse og Indeksstørrelse.|
|Datastørrelse (KB)|Hvor meget plads data i tabellen optager i databasen.|
|Indeksstørrelse (KB)|Hvor meget plads tabelindekser (nøgler) optager i databasen.|
|Komprimering|Den type komprimering, **Række**, **Side** eller **Ingen**, der anvendes på tabellen i databasen. Du kan finde flere oplysninger under [Datakomprimering](/sql/relational-databases/data-compression/data-compression?).|

> [!NOTE]
> Hvis du sletter data i en tabel, starter [!INCLUDE[prod_short](includes/prod_short.md)] flere processer i baggrunden for at sikre, at alt ryddes op i din database. Værdierne på siden med oplysninger om tabellen opdateres først, når processerne er færdige, hvilket kan tage noget tid. Den tid, du skal vente, kan variere afhængigt af databasens størrelse.

## <a name="see-also" />Se også

[Inspicere sider](across-inspect-page.md)  
[Artikler om ydeevne til udviklere](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
