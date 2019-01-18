---
title: "Sådan forberedes en konfigurationspakke | Microsoft Docs"
description: "Når du konfigurerer en ny virksomhed, genkendes og behandles tabelrelationer. Data importeres og anvendes i den rigtige rækkefølge. Dimensionstabeller importeres også, hvis de er inkluderet i konfigurationspakken."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: ea4a7671788ba5c4bd251a83dab1f2616cfbe706
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="prepare-a-configuration-package"></a>Forberede en konfigurationspakke
Når du konfigurerer en ny virksomhed, genkendes og behandles tabelrelationer. Data importeres og anvendes i den rigtige rækkefølge. Dimensionstabeller importeres også, hvis de er inkluderet i konfigurationspakken.  

For at hjælpe din kunde med at bruge konfigurationspakken, kan du føje et spørgeskema eller et spørgeskemasæt til pakken. Spørgeskemaet kan hjælpe kunden med at forstå de forskellige konfigurationsindstillinger. Typisk oprettes spørgeskemaer for større konfigurationstabeller, hvor en kunde muligvis kræver yderligere vejledning om, hvordan der vælges en relevant indstilling. Du kan finde flere oplysninger i [Indsaml debitoropsætningsværdier](admin-gather-customer-setup-values.md).

Sørg for, at du er på rollecenteret RapidStart Services-implementering. Du kan finde flere oplysninger i [Bruge rollecenteret RapidStart Services-implementering](admin-how-to-use-the-rapidstart-services-role-center-to-track-progress.md)

> [!IMPORTANT]  
>  Ved eksport og import af konfigurationspakker mellem to virksomhedsdatabaser, skal databaserne har samme skema for at sikre, at alle data er blevet overført. Dette betyder, at databaserne skal have den samme tabel- og feltstruktur, hvor tabellerne har samme primære nøgler, og felter har samme id'er og datatyper.  
>   
>  Du kan indlæse konfigurationspakker, der er eksporteret fra en database med et andet skema end måldatabasen. Men tabeller eller felter i konfigurationspakken, der mangler i måldatabasen, importeres ikke. Tabeller med forskellige primære nøgler og felter med forskellige datatyper importeres heller ikke korrekt. Hvis konfigurationspakken indeholder tabellen **50000 kunder**, hvor primærnøglen er **Code20**, og databasen, som du importerer pakken til, indeholder tabellen **50000 debitorbankkonto**, der har primærnøglen **Code20 + Code 20**, så importeres data ikke.  

## <a name="to-create-a-configuration-package"></a>Oprette en konfigurationspakke  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationspakker**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. På oversigtspanelet **Generelt** skal du udfylde resten af felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Hvis du vil udelukke konfigurationsspørgeskemaer, konfigurationsskabeloner og konfigurationsregnearkstabeller fra pakken, skal du markere afkrydsningsfeltet **Udeluk konfigurationstabeller**. Ellers føjes disse tabeller automatisk til listen over pakketabeller, når du eksporterer pakken.  
5. Vælg handlingen **Hent tabeller**. Kørselssiden **Hent pakketabeller** åbnes.  
6. Vælg feltet **Vælg tabeller**. Siden **Konfigurationsvalg** åbnes.  
7. Vælg handlingen **Markér alt** for at føje alle tabellerne til pakken, eller markere afkrydsningsfeltet **Markeret** for hver tabel på den liste, du vil tilføje.
8. Vælg knappen **OK**. Antallet af tabeller, du har valgt, er angivet i feltet **Vælg tabeller**. Angiv yderligere indstillinger, og vælg derefter knappen **OK**. [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller føjes til linjerne på siden **Konfig.pakke**.  

    > [!NOTE]  
    >  Du kan også gøre dette i konfigurationsarket. Markér de tabeller, du ønsker at medtage i pakken, og vælg derefter handlingen **Tildel pakke**.

9. For at vælge de felter du vil medtage fra en tabel, skal du vælge tabellen, og derefter under fanen **Linjer** vælge handlingen **Felter**.
Angiv, hvilke felter der er inkluderet i pakken. Alle felter er inkluderet som standard.

    - For kun at vælge de felter du vil medtage, skal du vælge handlingen **Ryd inkluderede**. Hvis du vil tilføje alle felter, skal du vælge handlingen **Angiv inkluderede**.  
    - Hvis du vil angive, at feltdata ikke skal valideres, skal du fjerne markeringen af afkrydsningsfeltet **Valider felt** for feltet.  

10. Kontrollér, om du har indført potentielle fejl ved at vælge handlingen **Valider pakke**. Dette kan ske, når du ikke medtager tabeller, der er afhængige af din konfiguration.  
11. Vælg knappen **OK**.  

Når du har finjusteret listen over felter, der skal medtages i en tabel, kan du kontrollere dine resultater i Excel.  

### <a name="to-filter-and-review-your-dataset"></a>Filtrere og gennemgå dit datasæt  
1. For at filtrere efter et bestemt sæt poster, der skal medtages i pakken, skal du under fanen **Linjer** vælge handlingen **Filtre** og derefter angive de ønskede filterværdier.  
2. På pakkekortet skal du under fanen **Linjer** vælge handlingen **Udlæs til Excel**.  
3. Bekræft de meddelelser, der aktiverer eksport af data til Excel. Den navngivne .xlsx-fil åbnes. Gennemse de poster, der er blevet udlæst.  
4. Luk Excel.  

### <a name="to-include-a-template-for-application-to-a-table"></a>Medtage en skabelon til ansøgning til en tabel  
For visse tabeller som f.eks. en tabel, der skal indeholde masterdata, kan du angive en skabelon, der skal anvendes til data. Skabelonen kan medtage de ønskede felter, du vil anvende på alle masterdata, og som du aldrig vil variere. F.eks. kan du oprette en skabelon, der kan bruges sammen med debitordata. Skabelonen kan indeholde alle de obligatoriske felter, som derefter giver mulighed for ensartet import af standardiserede oplysninger. Oplysninger, der ikke kan standardiseres, som f.eks. debitornavn, behandles derefter, når du foretager en import af debitordata.

1. På siden **Konfig.pakkekort** skal du vælge en tabel, og derefter vælge feltet **Dataskabelon**. Der vises en liste over skabeloner, der er baseret på den viste tabel.
2. Vælg en skabelon, og vælg derefter knappen **OK**.  

Når pakken er fuldført, skal du følge den næste procedure for at gemme pakken til en fil. Derefter kan du give pakken til en kunde eller partner, der kan bruge den.

### <a name="to-save-and-export-a-configuration-package"></a>Gemme og eksportere en konfigurationspakke  
- På siden **Konfig.pakkekort** skal du vælge handlingen **Udlæs pakke**.  

Pakken oprettes i en .rapidstart-fil, som leverer pakkens indhold i komprimeret format. Konfigurationsspørgeskemaer, konfigurationsskabeloner og konfigurationsregneark føjes automatisk til pakken, medmindre du udtrykkeligt vælger at udelukke dem.  

Du kan gemme filen med et navn, der er beskrivende for dig, men du kan ikke ændre filtypenavnet. Den skal være .rapidstart.  

### <a name="to-copy-a-configuration-package"></a>Kopiere en konfigurationspakke  
Når du har oprettet en pakke, der opfylder de fleste af dine behov, kan du bruge den som grundlag for oprettelse af tilsvarende pakker. Dette kan øge gennemførselstiden og forbedre gentagelserne i RapidStart Services.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationspakker**, og vælg derefter det relaterede link.  
2. Vælg en pakke på listen, og vælg derefter handlingen **Kopiér pakke**.  
3. Angiv en kode for den nye pakke i feltet **Ny pakkekode**.  
4. Markér afkrydsningsfeltet **Kopiér data**, hvis du også vil kopiere databasedata fra den eksisterende pakke.  
5. Vælg knappen **OK**.

## <a name="to-customize-a-configuration-package"></a>Sådan tilpasses en konfigurationspakke
Brug konfigurationsregnearket til at indsamle og kategorisere de oplysninger, du vil bruge til at konfigurere en ny virksomhed og arrangere tabeller på en logisk måde. Formateringen i regnearket er baseret på et enkelt hierarki: Områder indeholder grupper, som til gengæld indeholder tabeller. Områder og grupper er valgfri, men er nødvendige, hvis du vil have en oversigt over konfigurationsprocessen i rollecenteret RapidStart Services.

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationskladde**, og vælg derefter det relaterede link.  
2.  I feltet **Linjetype** skal du vælge **Område**. I feltet **Navn** skal du angive et beskrivende navn.  
3.  I feltet **Linjetype** skal du vælge **Gruppe**. I feltet **Navn** skal du angive et beskrivende navn.  
4.  I feltet **Linjetype** skal du vælge **Tabel**. I feltet **Tabel-id** skal du vælge den tabel, du vil medtage i regnearket.  

Du kan nu tildele tabeller til bestemte konfigurationspakker, du har oprettet eller planlægger at oprette. Du kan finde flere oplysninger i afsnittet "Tildele en tabel til en konfigurationspakke".

## <a name="to-work-with-promoted-tables"></a>Arbejde med opgraderede tabeller  
1. Markér afkrydsningsfeltet **Opgraderet tabel** for at angive en tabel, der ofte bruges under installationen af en typisk kunde, f.eks. tabellen **Finanskonto**. Når en tabel har denne betegnelse, kan en kunde let filtrere sit regneark for at se listen over netop opgraderede tabeller, der kræver opmærksomhed.  
2. Hvis du vil se den filtrerede visning af handlingen **Kun opdateret**. Liste over tabeller indeholder de tabeller, der har afkrydsningsfeltet markeret.  

## <a name="to-assign-a-table-to-a-configuration-package"></a>Tildele en tabel til en konfigurationspakke  
Når du har defineret de tabeller, der skal behandles som en del af konfigurationen, kan du let tildele tabellerne til konfigurationspakkerne. Du kan kun tildele en tabel til én pakke. I følgende procedure kan du tildele pakken inden for rammerne af konfigurationsregnearket.  

> [!NOTE]  
>  Du kan også oprette en pakke direkte og føje tabeller til den. Du kan finde flere oplysninger i afsnittet "Oprette en konfigurationspakke".

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationskladde**, og vælg derefter det relaterede link.
2. I konfigurationsregnearket skal du vælge en linje eller gruppe af linjer, du vil tildele til en konfigurationspakke, og derefter vælge handlingen **Tildel pakke**.  
3.  Vælg en pakke på listen, eller vælg handlingen **Ny** for at oprette en ny pakke, og vælg derefter knappen **OK**.  

    Hvis en tabel ikke allerede er indeholdt i pakken, føjes den nu til den. Pakkekodefeltet på kladdelinjen udfyldes med koden for den pakke, som tabellen er tildelt til.  
4. Hvis du vælger en eksisterende pakke, kan du se, hvor mange tabeller der allerede findes i pakken ved at gennemgå oplysningerne i feltet **Antal tabeller**.

## <a name="to-review-or-customize-existing-database-data"></a>Sådan gennemgår eller tilpasser du de eksisterende databasedata
Efterhånden som du opretter en konfigurationspakke for en løsning, kan du få vist og tilpasse tilgængelige databasedata, så de passer til debitorens behov. Databasetabellen skal have en tilknyttet side.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationskladde**, og vælg derefter det relaterede link.
2. I konfigurationsregnearket skal du identificere de tabeller, hvis data du ønsker at se eller tilpasse.  

    > [!NOTE]  
    >  Sørg for, at hver enkelt tabel har fået tildelt et side-id. For standardtabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] angives værdien automatisk. For brugerdefinerede tabeller skal du angive id'et.

3. Vælg handlingen **Databasedata**. Siden for den relaterede side åbnes.
4. Gennemse de tilgængelige oplysninger. Rediger dem efter behov ved at slette poster, der ikke er relevante, eller ved tilføje nye.    

## <a name="to-copy-data-from-a-test-environment-to-a-production-environment"></a>Sådan kopieres data fra et testmiljø til et produktionsmiljø  
Når du har undersøgt og afprøvet alle konfigurationsoplysninger, kan du fortsætte med at kopiere data til produktionsmiljøet. Du kan oprette en ny virksomhed i samme database.

1. Åbn og initialiser den nye virksomhed.  
2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationskladde**, og vælg derefter det relaterede link.  
3. Vælg handlingen **Kopiér data fra virksomhed**.  
4. På siden **Kopiér virksomhedsdata** skal du vælge feltet **Kopiér fra**. Siden **Virksomheder** åbnes.  
5. Marker den virksomhed, du vil kopiere data fra, og vælg derefter knappen **OK**. En liste over tabeller, der er valgt under konfigurationsregnearket, åbnes. Det er kun tabeller, der indeholder poster, der medtages på denne liste.
6. Vælg de tabeller, som du ønsker at kopiere data fra, og vælg derefter handlingen **Kopiér data**. På siden **Kopiér virksomhedsdata** skal du vælge knappen **OK**.  

## <a name="see-also"></a>Se også  
[Indsaml debitoropsætningsværdier](admin-gather-customer-setup-values.md)  
[Konfigurere virksomhedskonfiguration](admin-set-up-company-configuration.md)  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)

