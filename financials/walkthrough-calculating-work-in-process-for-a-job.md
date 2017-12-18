---
title: "Gennemgang - Beregning af igangværende arbejder for en sag | Microsoft Docs"
description: "Du kan bruge modulet Sager til at planlægge brugen af virksomhedens ressourcer og holde styr på de forskellige omkostninger, der er forbundet med brugen af ressourcerne på et bestemt projekt. Sager inkluderer forbruget af medarbejdertimer, maskintimer, lagervarer og andre brugstyper, der skal registreres, efterhånden som en sag skrider frem."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2c043a33e02d197281877a8287df7008377d52e4
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-calculating-work-in-process-for-a-job"></a>Gennemgang: Beregning af igangværende arbejder for en sag
Du kan bruge modulet Sager til at planlægge brugen af virksomhedens ressourcer og holde styr på de forskellige omkostninger, der er forbundet med brugen af ressourcerne på et bestemt projekt. Sager inkluderer forbruget af medarbejdertimer, maskintimer, lagervarer og andre brugstyper, der skal registreres, efterhånden som en sag skrider frem. Hvis en sag kører over en længere periode, kan du have brug for at overføre disse omkostninger til en konto for igangværende arbejde (VIA) på balancen, mens sagen færdiggøres. Du kan derefter godkende omkostningerne og salget på resultatopgørelseskontiene, når det er relevant.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
 Denne gennemgang illustrerer følgende opgaver:  

-   Beregning af VIA.  
-   Valg af en VIA-beregningsmetode.  
-   Ekskludering af en del af sagen fra VIA.  
-   Bogføring af VIA i regnskabet.  
-   Tilbageførsel af en VIA-bogføring.  

 Hvert trin i processen beregner værdien og flytter sagstransaktionerne til regnskabet. Beregnings- og bogføringstrinnene er adskilte, så du bedre kan gennemse dataene og foretage ændringer før bogføringen i regnskabet. Du skal derfor kontrollere, at alle oplysninger er korrekte, når du har udført beregningen, og før du udfører kørslerne med bogføringen.  

## <a name="roles"></a>Roller  
 I denne gennemgang bruges projektteammedlemmet (Tina) som person.  

## <a name="prerequisites"></a>Forudsætninger  
 Før du kan udføre opgaverne i denne gennemgang, skal du installere [!INCLUDE[d365fin](includes/d365fin_md.md)] på din computer.  

## <a name="story"></a>Historie  
 I denne gennemgang fokuseres der på CRONUS Danmark A/S, en design- og konsulentvirksomhed, der designer og tilpasser nye infrastrukturer, f.eks. konferencerum og kontorer, med møbler, tilbehør og lagerenheder. Det meste af arbejdet hos CRONUS er projektorienteret, og Tina, som er med i projektteamet, bruger sager til at få en oversigt over hver igangværende sag, som CRONUS har startet samt de sager, der er afsluttet. Nogle af sagerne kan være meget langvarige og løbe over flere måneder. Tina kan bruge en VIA-konto til at registrere igangværende arbejde og spore omkostningerne hele vejen gennem sagen.  

## <a name="calculating-wip"></a>Beregne VIA  
 CRONUS har påtaget sig et længerevarende projekt, der nu har løbet over flere rapporteringsperioder. Tina, der er projektgruppemedlem, beregner Igangværende arbejde (VIA) for at sikre, at virksomhedens regnskabsopgørelse er nøjagtig.  

 Som del af denne procedure vælger Tina en bestemt gruppe opgaver, der skal inkluderes i VIA-beregningen. I vinduet **Sagsopgavelinjer** kan hun angive disse linjer i kolonnen **VIA i alt**.  

 Følgende tabel beskriver tre indstillinger.  

|Felt|Description|  
|-------------------------------------|---------------------------------------|  
|**<blank>**|Lad stå tomt, hvis sagsopgaven er del af en gruppe opgaver.|  
|**Total**|Definerer det område eller den gruppe af opgaver, der er medtaget i beregningen af VIA og registrering. Inden for gruppen vil alle sagsopgaver med **Sagsopgavetype** indstillet til **Bogføring** blive inkluderet i VIA i alt, medmindre feltet **VIA i alt** er indstillet til **Ekskluderet**.|  
|**Udelukket**|Gælder kun for opgaver med **Sagsopgavetype** indstillet til **Bogføring**. Opgaven medtages ikke ved beregningen af VIA og registrering.|  

 I følgende gennemgang anvender Tina kostværdimetoden, der er standard i virksomheden, til at beregne igangværende arbejde. Hun angiver, hvilken del af sagen, der skal medtages i beregningen af igangværende arbejde ved at tildele forskellige VIA i alt-værdier til forskellige sagslinjer.  

### <a name="to-calculate-wip"></a>Sådan beregnes VIA  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sager**, og vælg derefter det relaterede link.  
2.  På listen **Sager** skal du vælge sagen **Kvalitetsmøbler** og derefter vælge handlingen **Rediger**. Dermed åbnes sagskortet i redigeringstilstand.  

     VIA kan beregnes ud fra Kostværdi, Salgsværdi, Salgsomkostning, Færdiggørelsesgrad og Afsluttet kontrakt. I dette eksempel bruger CRONUS kostværdimetoden.  

3.  Gå til oversigtspanelet **Bogføring** og feltet **VIA-metode**, og vælg derefter **Kostværdi**.  
4.  Vælg handlingen **Sagsopgavelinjer**, og angiv følgende værdier i feltet **VIA i alt**.  

     Den følgende tabel beskriver værdierne.  

    |Sagsopgavenr.|Feltet VIA i alt|  
    |------------------|----------------------|  
    |1130|Ikke medtaget|  
    |1190|Total|  
    |1210|Ikke medtaget|  
    |1310|Ikke medtaget|  

5.  Vælg handlingen **VIA**, og vælg derefter handlingen **Beregn VIA**.  
6.  I vinduet **Beregn VIA - finansafstemning** kan du vælge den sag, du vil beregne VIA for. Gå til oversigtspanelet **Sag**, vælg **Kvalitetsmøbler** i feltet **Nummer** .  
7.  I feltet **Bogføringsdato** skal du angive en dato, der ligger efter arbejdsdatoen.
8.  Skriv **1** i feltet **Bilagsnr.** Dette opretter et dokument, som du kan referere til, hvis du vil spore senere.  
9. Vælg **OK** for at eksekvere kørslen. Der vises en meddelelse. Vælg knappen **OK** for at forsætte. Luk vinduet **Sagsopgavelinjer**.  

    > [!NOTE]  
    >  Der vises en meddelelse om, at der er advarsler, der er knyttet til beregningen af igangværende arbejde. Du vil gennemgå advarslerne i den næste procedure.  

10. Gå til kortet **Sag**, og udvid oversigtspanelet **VIA og registrering** for at se de beregnede værdier. Du kan også se **VIA-bogføringsdato** og de eventuelle værdier, der er bogført i regnskabet.  

 Bemærk, at værdien for **Realiseret kostbeløb** er 215,60 i kolonnen **Til bogføring**. Dette afspejler den samlede kostpris for to af varerne i gruppen af sagsopgaver 1110 – 1130. Den tredje vare var angivet til **udelukket**, og medtages derfor ikke i VIA-beregningen.  

### <a name="to-review-wip-warnings"></a>Gennemgå VIA -advarsler  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **VIA-cockpit for job**, og vælg derefter det relaterede link.  
2.  Markér sagen **Kvalitetsmøbler**, og vælg derefter handlingen **Vis advarsler**.  
3.  Gennemse den advarsel, der er knyttet til sagen i vinduet **Advarsler om igangværende arbejde**.  

 Når denne regnskabsperiode slutter, skal Tina genberegne VIA for at inkludere det færdige arbejde op til det pågældende tidspunkt.  

### <a name="to-recalculate-wip"></a>Sådan genberegnes VIA  

1.  På kortet **Sag** skal du vælge handlingen **VIA-poster** for at få vist VIA-beregningen.  

     Vinduet **VIA-poster for sag** viser de VIA-poster, der blev beregnet for en sag, også selvom VIA endnu ikke er bogført i regnskabet.  

2.  Du kan følge trinnene i proceduren, der forklarer, hvordan du beregner igangværende arbejde for at genberegne igangværende arbejde. Hver gang VIA genberegnes, oprettes der en post i vinduet **VIA-poster**.  
3.  Luk vinduet.  

> [!NOTE]  
>  Det er kun igangværende arbejde og registrering, der bregnes Det bogføres ikke i finansmodulet. For at gøre dette skal du udføre kørslen **Bogfør VIA**, når du har beregnet VIA og registrering.

## <a name="posting-wip-to-general-ledger"></a>Bogføre VIA i regnskab  
 Nu, hvor Tina har beregnet VIA for denne sag, kan hun bogføre det i regnskabet.  

### <a name="to-post-wip-to-general-ledger"></a>Sådan bogføres VIA til finanspost  

1.  På listen **Sager**, vælges sagen **Kvalitetsmøbler**.  
2.  Vælg handlingen **VIA**, og vælg derefter handlingen **Bogfør VIA**.  
3.  Gå til vinduet **Bogfør VIA - finansafstemning** og oversigtspanelet **Sag**, og vælg **Kvalitetsmøbler** i feltet **Nr.** .  
4.  Gå til oversigtspanelet **Indstillinger** og feltet **Tilbageførselsdokumentnr.**, og indtast **1**.  
5.  Vælg knappen **OK** for at bogføre igangværende arbejde i regnskabet.  
6.  Vælg knappen **OK** for at gemme og lukke bekræftelsesvinduet.  

     Når du har fuldført bogføringen, kan du få vist bogføringsoplysningen i vinduet **VIA-finansposter**.  

7.  På listen **Sager** skal du vælge sagen **Kvalitetsmøbler** og derefter vælge handlingen **VIA-finansposter**.  

     I vinduet **VIA-finansposter**, skal du kontrollere, at VIA er bogført i regnskabet.  

8.  Luk vinduet.  
9. Åbn kortet **Sag** for sagen **Kvalitetsmøbler**.  
10. Bemærk, at feltet **Realiseret bogført kostbeløb** i kolonnen **Bogført** i oversigtspanelet **VIA og registrering** nu er udfyldt, hvilket angiver, at igangværende arbejde blev korrekt bogført i regnskab.  
11. Vælg knappen **OK** for at lukke kortet.  

## <a name="reversing-a-wip-posting"></a>Tilbageføre en VIA-bogføring  
 Tina bestemmer, at de arbejdsopgaver, der blev udeladt fra beregningen af igangværende arbejde, skulle have været beregnet i igangværende arbejde. Hun kan tilbageføre forkerte bogføringer uden at skulle bogføre nye VIA-bogføringer.  

### <a name="to-reverse-a-wip-posting"></a>Sådan tilbageføres en VIA-bogføring.  

1.  På listen **Sager**, vælges sagen **Kvalitetsmøbler**.  
2.  Vælg handlingen **VIA**, og vælg derefter handlingen **Bogfør VIA**.  
3.  Gå til vinduet **Bogfør VIA - finansafstemning** og oversigtspanelet **Sag**, og vælg **Kvalitetsmøbler** i feltet **Nr.** .  
4.  Gå til oversigtspanelet **Indstillinger** og feltet **Tilbageførselsdokumentnr.**, og indtast **1**.  
5.  Indtast den oprindelige bogføringsdato i feltet **Tilbageførselsdato**. Det bør være den samme dato, som du brugte til at beregne igangværende arbejde første gang.  
6.  Markér afkrydsningsfeltet **Kun tilbageførsel**. Dermed tilbageføres den tidligere bogførte VIA, uden at der bogføres en ny VIA i regnskabet.  
7.  Vælg knappen **OK** for at foretage kørslen, og vælg knappen **OK** for at lukke bekræftelsesvinduet.  
8.  Åbn kortet **Sag** for **Kvalitetsmøbler**.  
9. Kontrollér, at der ikke er nogen bogførte poster for igangværende arbejde i oversigtspanelet **VIA**.  
10. Luk vinduet.  
11. Markér sagen **Kvalitetsmøbler** på listen **Sager**, vælg handlingen **VIA**, og vælg derefter handlingen **VIA-finansposter**. Poster for igangværende arbejde har afkrydsningsfeltet **Tilbageførte** markeret.  
12. Luk vinduet.  
13. Åbn **Sagsopgavelinjer** til sagen, inkluder de dele af sagen, der skal medtages i VIA-beregningen, og genberegn og bogfør derefter den nye værdi i regnskabet.  

    > [!NOTE]  
    >  Antag, at Tina beregnede og bogførte igangværende arbejde for en sag med forkerte datoer. Ved at følge de tidligere beskrevne metode kan hun tilbageføre de forkerte bogføringer, rette datoerne og genposterer i regnskabet.  

## <a name="next-steps"></a>Efterfølgende trin  
 Denne gennemgang har taget dig gennem trinnene til beregning af igangværende arbejde i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I større sager kan det være nyttigt regelmæssigt at overføre omkostningerne til en konto for igangværende arbejde, mens sagen fuldføres. Denne gennemgang har vist dig, hvordan du kan udelade opgavelinjerne i en beregning. Den viser også, hvornår du skal genberegne. Endelig viser denne gennemgang, hvordan du bogfører igangværende arbejde i regnskab. Der er også et eksempel på, hvordan du tilbagefører en bogføring for igangværende arbejde i regnskab .  

## <a name="see-also"></a>Se også  
 [Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Gennemgang: Administration af projekter med sager](walkthrough-managing-projects-with-jobs.md)   
 [Forstå VIA -metoder](projects-understanding-wip.md)   
 [Overvåge status og udførelse](projects-how-monitor-progress-performance.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

