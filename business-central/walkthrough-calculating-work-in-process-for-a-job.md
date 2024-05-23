---
title: Gennemgang – Beregning af igangværende arbejder for et projekt
description: 'Få mere at vide om, hvordan du sporer forbruget af medarbejdertimer, maskintimer, lagervarer og andre brugstyper, efterhånden som et projekt skrider frem.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 12/13/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Gennemgang: Beregning af igangværende arbejder for et projekt

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Du kan bruge et projekt til at planlægge brugen af virksomhedens ressourcer og holde styr på de forskellige omkostninger, der er forbundet med brugen af ressourcerne på et bestemt projekt. Projekter inkluderer forbruget af medarbejdertimer, maskintimer, lagervarer og andre brugstyper, der skal registreres, efterhånden som et projekt skrider frem. Hvis et projekt kører over en længere periode, kan du have brug for at overføre disse omkostninger til en konto for igangværende arbejde på balancen, mens projektet færdiggøres. Du kan derefter godkende omkostningerne og salget på resultatopgørelseskontiene, når det er relevant.  

## Om denne gennemgang

 Denne gennemgang illustrerer følgende opgaver:  

-   Beregning af VIA.  
-   Valg af en VIA-beregningsmetode.  
-   Ekskludering af en del af et projekt fra igangværende arbejde.  
-   Bogføring af VIA i regnskabet.  
-   Tilbageførsel af en VIA-bogføring.  

 Hvert trin i processen beregner værdien og flytter projekttransaktionerne til regnskabet. Beregnings- og bogføringstrinnene er adskilte, så du bedre kan gennemse dataene og foretage ændringer før bogføringen i regnskabet. Du skal derfor kontrollere, at alle oplysninger er korrekte, når du har udført beregningen, og før du udfører kørslerne med bogføringen.  

## Roller

 I denne gennemgang bruges projektteammedlemmet (Tricia) som person.  

## Forudsætninger

 Før du kan udføre opgaverne i denne gennemgang, skal du installere [!INCLUDE[prod_short](includes/prod_short.md)] på din computer.  

## Historie

 I denne gennemgang fokuseres der på CRONUS Danmark A/S, en design- og konsulentvirksomhed, der designer og tilpasser nye infrastrukturer, f.eks. konferencerum og kontorer, med møbler, tilbehør og lagerenheder. Det meste af arbejdet hos CRONUS er projektorienteret, og Tricia, som er med i projektteamet, bruger projekter til at få en oversigt over hvert igangværende projekt, som CRONUS har startet samt de projekter, der er afsluttet. Nogle af projekterne kan være langvarige og løbe over flere måneder. Tricia kan bruge en konto for igangværende arbejde til at registrere igangværende arbejde og spore omkostningerne hele vejen gennem projektet.  

## Beregne VIA

 CRONUS har påtaget sig et længerevarende projekt, der nu har løbet over flere rapporteringsperioder. Tricia, der er projektgruppemedlem, beregner Igangværende arbejde for at sikre, at virksomhedens regnskabsopgørelse er nøjagtig.  

 Som del af denne procedure vælger Tricia en bestemt gruppe opgaver, der skal inkluderes i beregning af igangværende arbejde. På siden **Projektopgavelinjer** kan Tricia angive disse linjer i kolonnen **Igangværende arbejde i alt**.  

 Følgende tabel beskriver tre indstillinger.  

|Felt|Beskrivelse|  
|-------------------------------------|---------------------------------------|  
|**\<blank\>**|Lad stå tomt, hvis projektopgaven er del af en gruppe opgaver.|  
|**I alt**|Definerer det område eller den gruppe af opgaver, der er medtaget i beregningen af VIA og registrering. Inden for gruppen vil alle projektopgaver med **Projektopgavetype** indstillet til **Bogføring** blive inkluderet i Igangværende arbejde i alt, medmindre feltet **Igangværende arbejde i alt** er indstillet til **Ekskluderet**.|  
|**Ikke medtaget**|Gælder kun for opgaver med **Projektopgavetype** indstillet til **Bogføring**. Opgaven medtages ikke ved beregningen af igangværende arbejde og registrering.|  

 I følgende gennemgang anvender Tricia kostværdimetoden, der er standard i virksomheden, til at beregne igangværende arbejde. Tricia angiver, hvilken del af projektet, der skal medtages i beregningen af igangværende arbejde ved at tildele forskellige værdier for Igangværende arbejde i alt til forskellige projektlinjer.  

### Sådan beregnes VIA  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projekt**, og vælg derefter det relaterede link.  
2. På listen **Projekter** skal du vælge projektet **Kvalitetsmøbler** og derefter vælge handlingen **Rediger**. Dermed åbnes projektkortet i redigeringstilstand.  

     VIA kan beregnes ud fra Kostværdi, Salgsværdi, Salgsomkostning, Færdiggørelsesgrad og Afsluttet kontrakt. I dette eksempel bruger CRONUS kostværdimetoden.  

3. Gå til oversigtspanelet **Bogføring** og feltet **VIA-metode**, og vælg derefter **Kostværdi**.  
4. Vælg handlingen **Projektopgavelinjer**, og angiv følgende værdier i feltet **Igangværende arbejde i alt**.  

     Den følgende tabel beskriver værdierne.  

    |Projektopgavenr.|Feltet VIA i alt|  
    |------------------|----------------------|  
    |1130|Ikke medtaget|  
    |1190|Totalbeløb|  
    |1210|Ikke medtaget|  
    |1310|Ikke medtaget|  

5. Vælg handlingen **VIA**, og vælg derefter handlingen **Beregn VIA**.  
6. På siden **Beregn igangværende arbejde for projekt** skal du vælge et projekt, du vil beregne igangværende arbejde for. Gå til oversigtspanelet **Projekt**, vælg **Kvalitetsmøbler** i feltet **Nummer** .  
7. I feltet **Bogføringsdato** skal du angive en dato, der ligger efter arbejdsdatoen.
8. Skriv **1** i feltet **Bilagsnr.** Dette opretter et dokument, som du kan referere til, hvis du vil spore senere.  
9. Vælg **OK** for at eksekvere kørslen. Der vises en meddelelse. Vælg knappen **OK** for at forsætte. Luk siden **Projektopgavelinjer**.  

    > [!NOTE]  
    >  Der vises en meddelelse om, at der er advarsler, der er knyttet til beregningen af igangværende arbejde. Du vil gennemgå advarslerne i den næste procedure.  

10. Gå til siden **Projektkort**, og udvid oversigtspanelet **Igangværende arbejde og registrering** for at se de beregnede værdier. Du kan også se **VIA-bogføringsdato** og de eventuelle værdier, der er bogført i regnskabet.  

 Bemærk, at værdien for **Realiseret kostbeløb** er 215,60 i kolonnen **Til bogføring**. Dette afspejler den samlede kostpris for to af varerne i gruppen af projektopgaver 1110 – 1130. Den tredje vare var angivet til **udelukket**, og medtages derfor ikke i beregningen af igangværende arbejde.  

### Gennemgå VIA -advarsler  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektcockpit til igangværende arbejde**, og vælg derefter det relaterede link.  
2.  Markér projektet **Kvalitetsmøbler**, og vælg derefter handlingen **Vis advarsler**.  
3.  Gennemse den advarsel, der er knyttet til projektet, på siden **Advarsler om projektets igangværende arbejde (WIP)**.  

 Når denne regnskabsperiode slutter, skal Tricia genberegne VIA for at inkludere det færdige arbejde op til det pågældende tidspunkt.  

### Sådan genberegnes VIA  

1. På siden **Projektkort** skal du vælge handlingen **Poster for igangværende arbejde** for at få vist beregningen af igangværende arbejde.  

     Siden **Projektposter for igangværende arbejde** viser de poster for igangværende arbejde, der blev beregnet for et projekt, også selvom igangværende arbejde endnu ikke er bogført i regnskabet.  

2. Du kan følge trinnene i proceduren, der forklarer, hvordan du beregner igangværende arbejde for at genberegne igangværende arbejde. Hver gang igangværende arbejde genberegnes, oprettes der en post på siden **Projektposter for igangværende arbejde**.  
3. Luk siden.  

> [!NOTE]  
> Igangværende arbejde og registrering beregnes, men bogføres ikke i finansregnskabet. For at gøre dette skal du udføre kørslen **Bogfør igangværende arbejde til finans**, efter at du har beregnet igangværende arbejde og registrering.

## Bogføre igangværende arbejde i regnskab

 Nu, hvor Tricia har beregnet igangværende arbejde for dette projekt, kan hun bogføre det i regnskabet.  

### Sådan bogføres VIA til finanspost  

1. På listen **Projekter** skal du vælge projektet **Kvalitetsmøbler**.  
2. Vælg handlingen **VIA**, og vælg derefter handlingen **Bogfør VIA**.  
3. Gå til siden **Bogfør projektets igangværende arbejde til finans** og oversigtspanelet **Projekter**, og vælg **Kvalitetsmøbler** i feltet **Nr.** .  
4. Gå til oversigtspanelet **Indstillinger** og feltet **Tilbageførselsdokumentnr.**, og indtast **1**.  
5. Vælg knappen **OK** for at bogføre igangværende arbejde i regnskabet.  
6. Vælg knappen **OK** for at gemme og lukke bekræftelsessiden.  

     Når du har fuldført bogføringen, kan du få vist bogføringsoplysningen på siden **VIA-finansposter**.  

7.  På listen **Projekter** skal du vælge projektet **Kvalitetsmøbler** og derefter vælge handlingen **Finansposter for igangværende arbejde**.  

     På siden **Projektfinansposter for igangværende arbejde** skal du kontrollere, at igangværende arbejde er bogført i regnskabet.  

8. Luk siden.  
9. Åbn siden **Projektkort** for projektet **Kvalitetsmøbler**.  
10. Bemærk, at feltet **Realiseret bogført kostbeløb** i kolonnen **Bogført** i oversigtspanelet **VIA og registrering** nu er udfyldt, hvilket angiver, at igangværende arbejde blev korrekt bogført i regnskab.  
11. Vælg knappen **OK** for at lukke kortet.  

## Tilbageføre en bogføring for igangværende arbejde

 Tricia bestemmer, at de projektopgaver, der blev udeladt fra beregningen af igangværende arbejde, skulle have været beregnet i igangværende arbejde. Tricia kan tilbageføre forkerte bogføringer uden at skulle bogføre nye VIA-bogføringer.  

### Sådan tilbageføres en VIA-bogføring.  

1. På listen **Projekter** skal du vælge projektet **Kvalitetsmøbler**.  
2. Vælg handlingen **Igangværende arbejde**, og vælg derefter handlingen **Bogfør igangværende arbejde til finans**.  
3. Gå til siden **Bogfør projektets igangværende arbejde til finans** og oversigtspanelet **Projekter**, og vælg **Kvalitetsmøbler** i feltet **Nr.** .  
4. Gå til oversigtspanelet **Indstillinger** og feltet **Tilbageførselsdokumentnr.**, og indtast **1**.  
5. Indtast den oprindelige bogføringsdato i feltet **Tilbageførselsdato**. Det bør være den samme dato, som du brugte til at beregne igangværende arbejde første gang.  
6. Markér afkrydsningsfeltet **Kun tilbageførsel**. Dermed tilbageføres den tidligere bogført igangværende arbejde, uden at der bogføres nyt igangværende arbejde i regnskabet.  
7. Vælg knappen **OK** for at foretage kørslen, og vælg knappen **OK** for at lukke bekræftelsessiden.  
8. Åbn siden **Projektkort** for **Kvalitetsmøbler**.  
9. Kontrollér, at der ikke er nogen bogførte poster for igangværende arbejde i oversigtspanelet **VIA**.  
10. Luk denne side.  
11. Markér projektet **Kvalitetsmøbler** på listen **Projekter**, vælg handlingen **Igangværende arbejde**, og vælg derefter handlingen **Finansposter for igangværende arbejde**. Poster for igangværende arbejde har afkrydsningsfeltet **Tilbageførte** markeret.  
12. Luk denne side.  
13. Åbn **Projektopgavelinjer** for projektet, inkluder de dele af projektet, der skal medtages i beregningen af igangværende arbejde, og genberegn og bogfør derefter den nye værdi i regnskabet.  

    > [!NOTE]  
    >  Antag, at Tricia beregnede og bogførte igangværende arbejde for et projekt med forkerte datoer. Ved at følge de tidligere beskrevne metode kan Tricia tilbageføre de forkerte bogføringer, rette datoerne og genposterer i regnskabet.  

## Næste trin

 Denne gennemgang har taget dig gennem trinnene til beregning af igangværende arbejde i [!INCLUDE[prod_short](includes/prod_short.md)]. I større projekter kan det være nyttigt regelmæssigt at overføre omkostningerne til en konto for igangværende arbejde, mens projektet fuldføres. Denne gennemgang har vist dig, hvordan du kan udelade opgavelinjerne i en beregning. Den viser også, hvornår du skal genberegne. Endelig viser denne gennemgang, hvordan du bogfører igangværende arbejde i regnskab. Der er også et eksempel på, hvordan du tilbagefører en bogføring for igangværende arbejde i regnskab .  

## Se også

 [Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Gennemgang: Administration af projekter](walkthrough-managing-projects-with-jobs.md)  
 [Forstå VIA-metoder](projects-understanding-wip.md)  
 [Overvåge status og udførelse](projects-how-monitor-progress-performance.md)  
 [Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
