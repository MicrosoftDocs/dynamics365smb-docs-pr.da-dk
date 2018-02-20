---
title: Oprette og rapportere Intrastat | Microsoft Docs
description: "Få at vide, hvordan du opsætter Intrastat-rapporteringsfunktioner og rapporterer handel med virksomheder i andre EU-lande."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4b4fde6f005c992b63856ec4afadbb689532ac16
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="how-to-set-up-and-report-intrastat"></a>Fremgangsmåde: Konfigurere og rapportere Intrastat
Alle virksomheder i EU skal rapportere deres handel med andre EU-lande/områder. Du skal rapportere bevægelsen af varer til statistikmyndighederne i Danmark hver måned, og rapporten skal indleveres til skattemyndighederne. Dette omtales Intrastatrapportering. Du skal bruge siden **Intrastatkladde** til at udfærdige periodiske Intrastatrapporter.  

## <a name="required-and-optional-setups"></a>Krævede og valgfrie opsætninger
Før du kan bruge Intrastatkladden til at rapportere Intrastatoplysninger, er der flere ting, du skal konfigurere:  

* **Intrastatkladdetyper**: Du skal konfigurere de Intrastatkladdetyper og -kørsler, du skal bruge. Da Intrastat rapporteres månedsvis, skal du oprette 12 Intrastatkladdenavne af samme type.  
* **Varekoder**: Told- og skattemyndigheder har defineret numeriske koder, der klassificerer varer og serviceydelser. Du kan angive disse koder for varer.
* **Koder for transaktionsarter**: Lande og områder har forskellige koder for de typer Intrastattransaktioner, som almindeligt køb og salg, ombytning af returnerede varer og ombytning af ikke-returnerede varer. Oprette alle de koder, der gælder for dit land/område. Du kan bruge disse koder på salgs- og købsdokumenter, og når du behandler returneringer.  
* **Transportmåder**: Der er syv encifrede koder til Intrastattransportmåder. **1** for vand, **2** for jernbane, **3** for vej, **4** for fly, **5** for bogføring, **7** for faste installationer og **9** for egen fremdrift (f.eks. transport af en bil ved at køre den). [!INCLUDE[d365fin](includes/d365fin_md.md)] kræver ikke disse koder, men det anbefales, at beskrivelserne indeholder den samme betydning.  

Du kan også konfigurere:

* **Transaktionsspecifikationer**: Du kan bruge disse som supplement til beskrivelsen fra transaktionsarten.  
* **Områder**: Du kan bruge disse som supplement til oplysninger om lande og områder.  
* **Indførsels-/ udførselssteder**: Brug disse til at angive de lokationer, hvor du kan sende eller modtage varer til eller fra andre lande. Københavns Lufthavn er et eksempel på et indførsels-/udførselssted. Du kan angive indførsels-/udførselssteder i salgs- og købsdokumenter i oversigtspanelet **Udenrigshandel**. Oplysningerne kopieres også fra vareposterne, når du opretter Intrastatkladden.  

### <a name="to-set-up-intrastat-templates-and-batches"></a>Sådan oprettes Intrastatkladdetyper og -kladdenavne
I Intrastatkørslen medtages udelukkende vareposter, og ikke finansposter. Hvis du har finansposter, der bør Intrastatrapporteres, skal du indtaste dem manuelt. Hvis du f.eks. køber en computer fra et andet EU-land/en anden EU-region, placeres computeren ikke på lager, men bogføres på en finanskonto. Du skal indtaste denne type post manuelt i Intrastatkladden.  

Du kan eksportere posterne til en fil, du kan sende til Intrastat-myndighederne. Du kan også udskrive en rapport, angive oplysningerne manuelt på formularer fra myndighederne og derefter sende oplysningerne.

>  [!Note]
> Vi anbefaler, at du opretter en Intrastatkladde for hver måned.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Intrastatkladdetyper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Oprette en skabelon for hver Intrastatblanket, du bruger.  
3. Hvis du vil oprette kladdenavne, skal du vælge fanen **Naviger** og derefter vælge **Navne**.  
4. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Opret en skabelon for hver Intrastatblanket, du bruger.  

> [!Note]
> Angiv statistiskperioden i feltet **Statistikperiode** som et firecifret nummer, hvor de første to cifre angiver året og de næste to måneden. Skriv f.eks. 1706 for juni 2017.

### <a name="to-set-up-commodity-codes"></a>Sådan angives varekoder
Alle varer, du køber eller sælger, skal have en varekode.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varekoder**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Hvis du vil tildele en varekode til en vare, skal du gå til siden **Varekort**, udvide oversigtspanelet **Omkostninger og bogføring** og derefter angive koden i feltet **Varekode**.   

### <a name="to-set-up-transaction-nature-codes"></a>Sådan konfigurerer du koder for transaktionsarter
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koder for transaktionsarter**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Hvis du ofte bruger en bestemt transaktionsartskode, kan du gøre den til standardkode. For at gøre dette skal du gå til siden **Intrastat, opsætning** og vælge koden.

### <a name="to-set-up-transport-methods"></a>Sådan defineres transportmåder
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Transportmåder**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-report-intrastat"></a>Sådan rapporteres Intrastat
Når du har udfyldt Intrastatkladden, kan du udskrive rapporten **Kontrolliste** for at kontrollere, at alle oplysninger i kladden er korrekte. Herefter kan du udskrive en Intrastatrapport som en formular eller oprette en fil, som skal sendes til skattemyndighederne i dit land/område.  

### <a name="to-fill-in-intrastat-journals"></a>Sådan udfyldes Intrastatkladder  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Intrastatkladde**, og vælg derefter det relaterede link.  
2. På siden **Intrastatkladde** skal du vælge den relevante kladde i feltet **Kladdenavn** og derefter vælge **OK**.  
3. Vælg handlingen **Foreslå linjer**. Felterne **Startdato** og **Slutdato** indeholder allerede datoerne for statistikperioden i kladdenavnet.  
4. I feltet **Reguleringspct.** kan du angivet et procenttal til dækning af transport og forsikring. Hvis du angiver en procent, er indholdet af feltet **Statistisk værdi** i kladden forholdsmæssigt højere.  
5. Vælg **OK** for at starte kørslen.  

Kørslen henter alle vareposter i statistikperioden og indsætter dem som linjer i Intrastatkladden. Du kan redigere linjerne efter behov.  

> [!IMPORTANT]  
>  Kørslen henter kun de poster, der indeholder en lande-/regionskode, der er angivet en Intrastatkode for, på siden **Lande/regioner**. Derfor skal du angive Intrastatkoder for den landekode, som du udfører kørslen for.  

### <a name="report-intrastat-on-a-form-or-a-file"></a>Rapportere Intrastat i en formular eller en fil
Hvis du vil hente de oplysninger, der kræves på Intrastatblanketten fra de statistiske myndigheder, skal du udskrive rapporten **Intrastat – blanket**. Før du kan gøre dette, skal du forberede Intrastatkladden og udfylde den. Hvis du har både salgs- og købstransaktioner, skal du udfylde en separat blanket for hver type, så du skal udskrive rapporten to gange.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Intrastatkladde**, og vælg derefter det relaterede link.  
2. På siden **Intrastatkladde** skal du vælge den relevante kladde i feltet **Kladdenavn**.  
3. Hvis du ikke allerede har gjort det, skal du udfylde kladden manuelt eller vælge **Foreslå linjer**.  
4. Vælg handlingen **Udskriver Intrastatkladde**.  
5. I oversigtspanelet **Intrastatkladdelinje** skal du tilføje et **Type** filter og derefter angive, om det er en **Modtagelse** eller **Afsendelse**.  
6. Vælg **Send til** for at udskrive rapporten.  

### <a name="report-intrastat-in-a-file"></a>Rapportere Intrastat i en fil
Du kan sende Intrastatrapporten som en fil. Før du opretter filen, kan du udskrive en kontrolliste, der indeholder de samme oplysninger som filens.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Intrastatkladde**, og vælg derefter det relaterede link.  
2. I vinduet **Intrastatkladde** skal du vælge den relevante kladde i feltet **Kladdenavn**.  
3. Hvis du ikke allerede har gjort det, skal du udfylde kladden manuelt eller ved at vælge **Foreslå linjer**.  
4. Vælg handlingen **Opret fil**.  
5. Vælg **OK** i kørselsvinduet.  
6. Vælg **Gem**.  
7. Gå til det sted, hvor du vil gemme filen, og angiv derefter filnavnet, og vælg **Gem**.

## <a name="reorganize-intrastat-journals"></a>Reorganisere Intrastatkladder
Da du skal sende en Intrastatrapport hver måned, og du opretter en ny kladde for hver rapport, vil du til sidst have mange kladder. Kladdelinjerne slettes ikke automatisk. Du vil muligvis reorganisere kladdenavne periodisk. Det gør du ved at slette kladder, der ikke længere er brug for. Kladdelinjerne i disse kørsler slettes også.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Intrastatkladde**, og vælg derefter det relaterede link.  
2. Vælg feltet **Kladdenavn** for at få vist indstillingerne.  
3. Vælg de kladder, der skal slettes, og vælg derefter **Slet**.  

## <a name="see-also"></a>Se også
[Økonomistyring](finance.md)

