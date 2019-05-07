---
title: Sådan arbejder du med servicekontrakter og servicekontrakttilbud | Microsoft Docs
description: Du kan oprette en servicekontrakt manuelt eller ud fra et servicekontrakttilbud. Du kan oprette en kontrakt baseret på et servicekontrakttilbud.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: d3c3a460cd13d0af16e38564d4b2fb0de367ed53
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "930991"
---
# <a name="work-with-service-contracts-and-service-contract-quotes"></a>Arbejde med servicekontrakter og servicekontrakttilbud
Du kan oprette en servicekontrakt manuelt eller ud fra et servicekontrakttilbud. Du kan bruge et servicekontrakttilbud som en forløber for en servicekontrakt, hvor din virksomhed giver kunden et tilbud og opnår kundens godkendelse, inden du kan konvertere det til en servicekontrakt. Proceduren for oprettelse af en servicekontrakt eller et servicekontrakttilbud er meget ens.  

## <a name="to-create-a-service-contract-or-service-contract-quote"></a>Sådan oprettes en servicekontrakt eller et servicekontrakttilbud  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekontrakter** eller **Servicekontrakttilbud**, og vælg derefter det relaterede link.  
2. Opret en ny servicekontrakt eller et servicekontrakttilbud.  
3. Udfyld feltet **Nummer**. . Der åbnes en dialogboks, hvor du bliver bedt om at udfylde fælles data ud fra en kontraktskabelon. Hvis du vil oprette sådan en servicekontrakt eller et servicekontrakttilbud, skal du vælge knappen **Ja**. Siden **Serv.kontraktskab. - oversigt** åbnes.  
4. Marker den relevante skabelon, og vælg derefter **OK** for at oprette servicekontrakten eller servicekontrakttilbuddet.  
5. I feltet **Debitornr.** skal du vælge debitoren.  
6. Marker afkrydsningsfeltet **Tillad beløb, der ikke stemmer**, hvis du ikke ønsker en årlig beløbsdifference, der skal fordeles automatisk. Værdierne i felterne **Årlige beløb** og **Årligt. Årlige beløb** udlignes ikke automatisk. Hvis du ønsker, at programmet automatisk skal fordele de årlige beløbsdifferencer, der kan opstå ved ændring i den servicekontrakt, skal du lade afkrydsningsfeltet **Tillad beløb, der ikke stemmer** stå tomt.  
7. Føj kontraktlinjer til servicekontrakten eller servicekontrakttilbuddet.  
8. Udfyld resten af felterne efter behov.  

## <a name="to-convert-a-service-contract-quote-to-service-contract"></a>Sådan konverteres servicekontrakttilbud til servicekontrakter  
Når en kunde har accepteret et servicekontrakttilbud, skal du konvertere det til en servicekontrakt. Samtidigt kan du oprette en servicefaktura for kontraktens startperiode, hvis kontraktens startdato ligger før begyndelsen af den næste fakturaperiode.

Når du gennemfører følgende fremgangsmåde, oprettes en servicekontrakt med status **Underskrevet**. Hvis der oprettes en servicefaktura for kontraktens startperiode, beregnes det fakturerede beløb på følgende måde, afhængigt af om kontrakten er detaljeret eller ej.  

Det fakturerede beløb beregnes på følgende måde for detaljerede kontrakter:  

* Faktureret beløb = summen af de fakturerede beløb for hver kontraktlinje.  
* Faktureret beløb for hver kontraktlinje = ((tilbudsværdi ÷ 12) x antal måneder i startperiode) + ((tilbudsværdi ÷ antal dage om året) x antallet af dage, der er tilbage i startperioden).  
* Hvis kontraktlinjen udløber, inden startperioden slutter, bliver udløbsdatoen til slutdato i startperioden for linjen.  

For kontrakter, der ikke er detaljerede, beregnes det fakturerede beløb på følgende måde:  

* Faktureret beløb = (årligt beløb ÷ antal dage i året) x antallet af dage i startperioden.  
* Hvis kontraktlinjen udløber, inden startperioden slutter, bliver udløbsdatoen til slutdato i startperioden.    

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekontrakttilbud**, og vælg derefter det relaterede link.  
2. Åbn det servicekontrakttilbud, der skal konverteres til en servicekontrakt.  
3. Vælg handlingen **Opret kontakt**.  
4. Hvis kontraktens startdato ligger før begyndelsen af den næste fakturaperiode, bliver du spurgt, om du vil oprette en faktura for kontraktens startperiode. Vælg **Ja**.  

 Servicefakturaen bogføres automatisk på kontraktens servicekonto, selvom kontrakten er forudbetalt.

## <a name="to-create-contract-service-credit-memos"></a>Sådan oprettes kontraktservicekreditnotaer
Du kan bruge en kontraktservicekreditnota, når en debitor annullerer en forudbetalt servicekontrakt eller fjerner en serviceartikel fra en forudbetalt kontrakt. Du kan også bruge den til at korrigere en fejlagtig servicefaktura.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekreditnotaer**, og vælg derefter det relaterede link.  
2. Opret en ny servicekreditnota.  
3. Udfyld feltet **Nummer**. .  
4. I feltet **Debitornr.** skal du angive nummeret på debitoren i servicekontrakten.  

     I oversigtspanelet **Fakturering** vises de oplysninger, der blev kopieret fra kortet **Debitor**. Hvis du vil bogføre kreditnotaen på en anden debitor end den, der er angivet i oversigtspanelet **Generelt**, skal du skrive kundenummeret i feltet **Faktureres til kundenr.** .  

    > [!NOTE]  
    >  Du kan sammenligne kreditnotaen med det oprindelige bogførte dokument på siden **Bogførte servicefakturaer**. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte servicefakturaer**, og vælg derefter det relaterede link.  

5. Udfyld felterne **Bogføringsdato** og **Bilagsdato** .  
6. På kreditnotalinjerne skal du angive oplysninger om de varer, der er blevet returneret eller fjernet, eller om den salgsdekort, der bliver sendt. Du kan også bruge kørslen **Hent forudbet. kontraktposter**.  

 Hvis du automatisk vil oprette en kreditnota, når du fjerner linjer fra en servicekontrakt, skal du vælgeafkrydsningsfeltet **Kreditnotaer automatisk** i oversigtspanelet **Fakturadetaljer** på siden **Servicekontrakt**.  

 Hvis du manuelt vil oprette en kreditnota, når du fjerner linjer fra en servicekontrakt på siden **Servicekontrakt** under fanen **Handlinger** i gruppen **Funktioner** skal du vælge **Kreditnota**.  

## <a name="updating-and-evaluating-contracts"></a>Opdatere og evaluere kontrakter
Nogle gange skal du ændre betingelserne i en kontrakt, efter at den er blevet oprettet. I de fleste tilfælde skal du åbne den relevante kontrakt på siden **Servicekontrakt** og ændre den efter behov.  

Du kan ændre kontraktens status, der som udgangspunkt angives til **Låst**, tilføje og fjerne kontraktlinjer og annullere en kontrakt. Hvis du vil se, hvordan virksomheden klarer sig målt i avance og tab, kan du udføre en hurtig forretningsanalyse ved hjælp af funktionen Kontrakt - Trendscape.

## <a name="to-add-a-contract-line-to-a-service-contract-or-contract-quote"></a>Sådan føjes en kontraktlinje til en servicekontrakt eller et kontrakttilbud  
Når en kunde køber en ny vare og vil have den med på en eksisterende servicekontrakt eller et kontrakttilbud, kan du registrere varen som en serviceartikel og derefter føje den til kontrakten eller kontrakttilbuddet som en ny kontraktlinje.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekontrakter**, og vælg derefter det relaterede link.  
2. Åbn den relevante servicekontrakt eller det relevante servicekontrakttilbud, hvor der skal tilføjes en ny kontraktlinje.  
3. Vælg handlingen **Åbn kontrakt** for at åbne servicekontrakten eller servicekontrakttilbuddet til redigering.  
4. Markér feltet **Tillad beløb, der ikke stemmer** på oversigtspanelet **Fakturadetaljer**, hvis du vil ændre det årlige beløb og fordele differencen i det årlige beløb manuelt på kontraktlinjerne. Ellers skal du fjerne markeringen fra afkrydsningsfeltet **Tillad beløb, der ikke stemmer**. Dette fordeler differencen i det årlige beløb automatisk på kontraktlinjerne, når du har ændret det årlige beløb.  
5. På oversigtspanelet **Linjer** skal du tilføje en serviceartikel eller vare eller tekstbeskrivelse på hver kontraktlinje. Du kan også tilføje kontrakttilbudslinjer. Bemærk, at du kan oprette flere kontrakter pr. serviceartikel, så den tages med i flere servicekontrakter eller kontrakttilbud på samme tid.  
6. Kontroller, og ret tallene i felterne **Linjerabatpct.**, **Linjerabatbeløb**, **Svartid**, **Serviceperiode** og de øvrige felter efter behov.

## <a name="to-remove-contract-lines"></a>Sådan fjernes kontraktlinjer  
Du kan få brug for at fjerne kontraktlinjer fra servicekontrakten, hvis du fjerner de tilsvarende serviceartikler fra servicekontrakten. Som regel skal du fjerne kontraktlinjer, der er udløbet, eller som svarer til en serviceartikel, der er ikke virker.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekontrakter**, og vælg derefter det relaterede link.  
2. Åbn den servicekontrakt, der skal fjernes kontraktlinjer fra.  
3. Vælg handlingen **Åbn kontrakt** for at åbne servicekontrakten til redigering.  
4. Vælg den kontraktlinje, du vil fjerne. Udfyld feltet **Udløbsdato for kontrakt** med datoen for, hvornår du vil fjerne linjen. Du kan f.eks. indtaste den dato, hvor serviceartiklen brød sammen.  
5. Vælg handlingen **Fjern kontraktlinjer**. Siden **Fjern linjer fra kontrakt** åbnes.  
6. Udfyld standardfiltrene: **Kontraktnr.**, **Serviceartikelnr.** og **Kontrakttype**. Du kan evt. tilføje flere filtre eller ændre eksisterende filtre.  
7. Udfyld felterne i oversigtspanelet **Indstillinger**. Vælg **Slet linjer** i feltet **Handling**.  

> [!NOTE]  
>  Hvis kontrakten ikke er detaljeret, skal du opdatere værdien i feltet **Årligt beløb** i oversigtspanelet **Fakturadetaljer** på siden **Servicekontrakt** for at afspejle fjernelsen af serviceartiklen fra kontrakten.  
>   
>  Hvis kontrakten er detaljeret og forudbetalt, og du har bogført fakturaer for kontrakten, kan du oprette en kreditnota for kontrakten. Under fanen **Handlinger** i gruppen **Funktion** skal du vælge **Opret kreditnota**. Dette er unødvendigt, hvis afkrydsningsfeltet **Kreditnotaer automatisk** i oversigtspanelet **Fakturadetaljer** er markeret. I dette tilfælde oprettes der automatisk en kreditnota, når du fjerner en kontraktlinje.

## <a name="service-line-cost-and-value"></a>Omkostninger og værdi for servicelinje
På en servicekontraktlinje beregnes beløbene i **Linjekostpris** og **Linjeværdi** som beskrevet i følgende tabeller.

| Indstillinger for linjekostpris | Beskrivelse|
|----------------------------------|---------------------------------------|  
|**Serviceartikel** | Kostprisen hentes automatisk fra feltet **Kontraktkostpris (standard)** i tabellen **Serviceartikel** og kopieres til feltet **Linjekostpris**. Følgende formel bruges til at beregne linjekostprisen:<br /><br /> Enhedsomkostninger × Kontraktværdipct - 100|  
|**Vare** | Kostprisen hentes automatisk fra feltet **Kostpris** i tabellen **Vare** og fra værdien i feltet **Kontraktværdipct.** i tabellen **Serviceopsætning**. Følgende formel bruges til at beregne linjekostprisen:<br /><br /> Kostpris × Kontraktværdipct. - 100|  
|**Tekstbeskrivelse** | Værdien i feltet **Linjekostpris** angives til nul.|  

| Indstillinger for linjeværdi | Beskrivelse|
|----------------------------------|---------------------------------------|  
|**Serviceartikel** | Prisen hentes automatisk fra feltet **Standardkontraktværdi** i tabellen **Serviceartikel** og kopieres til feltet **Linjeværdi**.|  
|**Vare** | Afhængigt af værdien i feltet **Beregning af kontraktværdi** i tabellen **Serviceopsætning** hentes værdien enten fra feltet **Salgspris** eller fra feltet **Kostpris** i tabellen **Vare**. Derefter ganges værdien med indholdet af feltet **Kontraktværdipct.** i tabellen **Serviceopsætning** og divideres med 100. Beløbet kopieres til feltet **Linjeværdi**.<br /><br /> **BEMÆRK!** Hvis feltet **Beregning af kontraktværdi** er indstillet til **Ingen**, beregnes indholdet af feltet **Linjeværdi** ikke.|  
|**Tekstbeskrivelse** | Indholdet af feltet **Linjeværdi** indstilles til nul.|  

## <a name="to-add-a-contract-discount-to-service-contract-quotes"></a>Sådan føjes en kontraktrabat til servicekontrakttilbud  
Du kan tilføje kontraktrabatter på serviceydelser i forbindelse med kontrakttilbud og servicekontrakter. Rabatterne kan være på reservedele i bestemte serviceartikelgrupper, på ressourceforbruget for ressourcer i bestemte ressourcegrupper og på bestemte serviceomkostninger.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekontrakttilbud**, og vælg det relaterede link.  
2. Vælg det tilbud, du vil tilføje rabatter for.  
3. Vælg handlingen **Servicerabatter**. Siden **Kontrakt/servicerabatter** vises.  
4. Klik på handlingen **Ny** for at oprette en ny kontraktrabat.  
5. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  

> [!Tip]  
>  Hvis du vil føje kontraktrabatter direkte til en servicekontrakt, skal du udføre lignende trin på siden **Servicekontrakt**.  

## <a name="to-change-the-owner-of-a-service-contract"></a>Sådan udskiftes indehaveren af en servicekontrakt  
Du skal måske skifte indehaver af en servicekontrakt. Hvis en serviceartikel i en servicekontrakt er registreret i ikke-annullerede kontrakter, der tilhører den samme debitor, opdateres indehaveren af alle servicekontrakter, der indeholder denne serviceartikel, og af alle andre serviceartikler i disse kontrakter automatisk.  

> [!NOTE]  
>  I dette tilfælde tages kun ikke-annullerede kontrakter i betragtning. Status for kontrakttilbud tages ikke i betragtning.  

> [!IMPORTANT]  
>  Serviceartikler og kontrakter kan være relaterede. Hvis indehaveren af en servicekontrakt ændres, kan det påvirke disse relationer.  
>   
>  Serviceartikel nr. 8 kan f.eks. være medtaget i kontrakterne SC00003 og SC00015. Kontrakten SC00015 indeholder også serviceartikel nr. 15, som også findes i kontrakten SC00080. I dette tilfælde vil indehaveren af alle tre kontrakter og af alle serviceartiklerne blive ændret.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekontrakter**, og vælg derefter det relaterede link. Åbn den relevante servicekontrakt, hvis ejer, du vil ændre.  
2. Vælg handlingen **Åbn kontrakt** for at åbne kontrakten til redigering.  
3. Vælg handlingen **Skift debitor**. Siden **Skift debitor i kontrakt** åbnes.  
4. I felterne **Kontraktnr.** og **Serviceartikelnr.** kan du se numrene på de kontrakter og serviceartikler, der tilhører den valgte debitor. Hvis debitoren har mere end én kontrakt med mere end én serviceartikel, angives værdien i disse felter til **Flere**. Hvis du vil se en liste over relaterede kontrakter eller serviceartikler, skal du markere disse feltværdier.  
5. I feltet **Nyt debitornr.** skal du vælge den nye debitor.  
6. I feltet **Ny lev.adr.kode** skal du vælge adressen.  
7. Vælg **OK** for at skifte debitor og leveringsadressekode i servicekontrakterne.  
8. Vælg handlingen **Lås kontrakt** for at låse kontrakten og sikre, at ændringerne kommer med i kontrakterne.  

## <a name="to-update-a-service-contract-price"></a>Opdateres en servicekontraktpris  
Du kan opdatere priserne på servicekontrakter ved at angive en prisopdateringsprocent.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opdater servicekontraktpriser**, og vælg derefter det relaterede link.
2. Vælg servicekontrakten.  
3. Angiv en dato i feltet **Opdater til dato**. Ved kørslen opdateres priser for kontrakter med de næste prisopdateringsdatoer på eller før denne dato.  
4. Skriv den procent, du vil opdatere priserne med, i feltet **Prisopdateringspct.**.  
5. Klik på **Opdater kontraktpriser** i feltet **Handling**.  

## <a name="to-post-prepaid-contract-entries"></a>Sådan bogføres forudbetalte kontraktposter  
Hvis du arbejder med forudbetalte servicekontrakter, skal du med regelmæssige mellemrum bogføre forudbetalte kontraktposter og dermed overføre de forudbetalte betalinger fra forudbetalingskonti til almindelige kontraktkonti.  

Inden du kan bogføre forudbetalte kontraktposter, skal du angive en nummerserie i feltet **Bogf.bilagsnr. til forudbetal.** på siden **Serviceopsætning**.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogfør forudbet. kontraktposter**, og vælg derefter det relaterede link.  
2. Angiv en dato i feltet **Bogfør indtil dato**. Ved kørslen bogføres forudbetalte serviceposter med bogføringsdato op til denne dato.  
4. I feltet **Bogføringsdato** skal du skrive den dato, du vil bruge som bogføringsdato på finanskladdelinjen.  
5. I feltet **Handling** skal du vælge **Bogfør forudbet. transaktioner**.  
6. Vælg **OK** for at bogføre posterne.

## <a name="changing-the-service-contract-status"></a>Ændring af status for servicekontrakten
Når servicekontrakten er underskrevet, indstilles feltværdien **Skift Status** automatisk til **Låst**. Hvis du vil redigere oplysninger i servicekontrakten eller servicekontrakttilbuddet, skal du først ændre statussen på kontrakten eller kontrakttilbuddet fra **Låst** til **Åben**. Bemærk, at du ikke kan oprette servicefakturaer for servicekontrakten med ændringsstatussen **Åben**. Når kontrakten eller kontrakttilbuddet er ændret, skal du ændre statussen tilbage til **Låst** for at gøre det muligt at oprette servicefakturaer og poster til servicekontrakten, som indeholder de ændringer, du har foretaget af den.  

> [!NOTE]  
>  Feltet **Skift status** er ikke relateret til feltet **Frigivelsesstatus** på serviceordrehovedet, der styrer lagerets håndtering af serviceartikler.  

## <a name="to-cancel-a-service-contract"></a>Sådan annulleres en servicekontrakt  
Det kan være nødvendigt at annullere en servicekontrakt, hvis kontrakten udløber, eller den er blevet annulleret af dig eller debitoren.  

> [!NOTE]  
>  Du kan ikke genåbne en kontrakt, når den er blevet annulleret.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekontrakter**, og vælg derefter det relaterede link.  
2. Åbn den relevante servicekontrakt, der skal annulleres.  
3. Vælg handlingen **Åbn kontrakt** for at åbne servicekontrakten til redigering.  
4. Vælg den relevante fejlårsagskode i feltet **Annulleringsårsagskode**. Hvis du vil tilføje flere årsagskoder, skal du vælge handlingen **Avanceret**.  

     Hvis afkrydsningsfeltet **Angiv årsag til kontraktannul.** på siden **Serviceopsætning** er markeret, skal du angive en annulleringsårsagskode, når kontrakten annulleres.  

5. Vælg **Annulleret** i feltet **Status**.  
6. Hvis der findes fakturaer, kreditnotaer eller åbnede forudbetalte poster til servicekontrakten, der ikke er bogført, vises en bekræftelsesmeddelelse. Vælg **Nej**, hvis du vil tilbage til kontrakten for at bogføre dokumenterne, eller **Ja** for at fortsætte annulleringen.  

## <a name="filing-a-service-contract-or-contract-quote"></a>Arkivere en servicekontrakt eller et kontrakttilbud  
Du kan når som helst arkivere servicekontrakter og kontrakttilbud for at registrere og arkivere en kopi af kontrakten eller kontrakttilbuddet. [!INCLUDE[d365fin](includes/d365fin_md.md)] arkiveret automatisk servicekontrakter, når du konverterer kontrakttilbud til servicekontrakter eller annullerer servicekontrakter. Kan du arkivere en kontrakt eller et tilbud selv ved at vælge handlingen **Arkiver kontrakt** på siden **Servicekontrakter** eller siden **Servicekontrakttilbud**. Hvis du vil se de arkiverede kontrakter på tilbud, skal du søge efter **Arkiverede kontrakter**.

## <a name="see-also"></a>Se også  
[Opsætte servicekontrakter](service-how-setup-service-contracts.md)  
[Service Management](service-service.md)  
[Konvertere servicekontrakter, som omfatter momsbeløb](service-how-to-convert-service-contracts.md)  
