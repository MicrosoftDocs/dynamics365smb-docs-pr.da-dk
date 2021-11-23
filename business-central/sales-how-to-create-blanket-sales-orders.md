---
title: Arbejde med rammesalgsordrer eller købsordrer
description: Rammeordrer bruges typisk, når en kunde har indvilliget i at købe et stort antal varer, der skal leveres i flere mindre portioner i løbet af en bestemt periode. Det samme gælder indkøb.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 507, 509, 6620, 6622, 6623, 9303, 9310
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4299924a1845245eb8b73192bb14232bad25d80b
ms.sourcegitcommit: a9e2aaee735870af566db68532cfa697347d68e0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752576"
---
# <a name="work-with-blanket-sales-orders-or-blanket-purchase-orders"></a>Arbejde med rammesalgsordrer eller rammekøbsordrer

En rammesalgsordre udgør rammen om en langsigtet aftale mellem dig og en kunde. På samme måde kan du bruge rammekøbsordrer til at styre langsigtede aftaler mellem dig og leverandøren.

Der indgås ofte en rammeaftale, hvor en kunde har forpligtet sig til at købe et stort antal varer, der skal leveres i flere mindre portioner i løbet af en bestemt periode. En rammeordre omfatter ofte kun en enkelt vare med leveringsdatoer, der er fastsat på forhånd. Den væsentligste årsag til at bruge en rammeordre i stedet for en salgsordre er, at de antal, der angives i en rammeordre, ikke påvirker varedisponeringen, og at oplysningerne dermed kan bruges til overvågnings-, prognose- og planlægningsformål.

I rammeordren kan hver enkelt leverance oprettes som en ordrelinje, der derefter kan konverteres til en salgsordre på leveringstidspunktet.

Det kan f.eks. være relevant at bruge en rammesalgsordre, når en kunder ringer og bestiller 1000 enheder af en vare, som skal leveres i portioner på 250 enheder en gang om ugen i løbet af den næste måned.

> [!NOTE]
> Rammekøbsordrer fungerer på samme måde som rammesalgsordrer. Denne dokumentation dækker kun rammesalgsordrer.

## <a name="to-create-a-blanket-sales-order"></a>Sådan oprettes en rammesalgsordre.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rammesalgsordrer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Lad feltet **Ordredato** være tomt. Når de enkelte salgsordrer oprettes på basis af rammeordren, angives salgsordrens ordredato til den faktiske arbejdsdato.
5. I oversigtspanelet **Linjer** skal du oprette separate linjer for hver enkelt leverance. Hvis kunden f.eks. skal have 1000 enheder fordelt jævnt over fire uger, kan du angive fire separate linjer på 250 enheder hver.  

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a>Sådan oprettes en salgsordre med udgangspunkt i en rammesalgsordre  

1. Når du skal oprette en ordre til en af linjerne i rammesalgsordren, skal du fjerne antallet i feltet **Lever (antal)** på alle de linjer, som ikke skal leveres på nuværende tidspunkt.  
2. Når du er klar til at oprette ordrer, skal du vælge handlingen **Lav ordre** og derefter vælge **Ja**. Der vises en meddelelse med besked om, at rammeordren har fået tildelt et ordrenummer. Bemærk, at rammeordren ikke er slettet.  
3. Vælg knappen **OK**.  
4. Hvis du vil se resultatet af de foregående trin, skal du vælge handlingen **Linje**, vælge handlingen **Ikkebogførte linjer** og derefter vælge handlingen **Ordrer**.  
5. Markér den relevante salgsordre på siden **Salgslinjer**, vælg handlingen **Linje** og derefter vælge handlingen **Vis dokument**.  

Følgende gælder for salgsordrer, når de er oprettet ud fra rammesalgsordrer:  

- Når rammeordren konverteres til en salgsordre, indeholder salgsordren samtlige linjer fra rammeordren. Ordren omfatter også de linjer, hvor du slettede antallene i feltet **Lever (antal)**, men **Antal**-felterne er tomme. Du bestemmer selv, om du vil lade linjerne være, redigere dem eller slette dem.  
- Det er vigtigt at huske, at antallet i salgsordren ikke må være større end antallet på den tilhørende rammeordrelinje. Ellers kan salgsordren ikke bogføres.  
- Når salgsordren bogføres som leveret og/eller faktureret, opdateres felterne **Leveret (antal)** og **Faktureret (antal)** i den tilhørende rammeordre.  
- Rammeordrenummeret og linjenummeret registreres som egenskaber for salgslinjerne, når de oprettes på basis af en rammeordre.  
- Hvis salgsordrerne ikke oprettes direkte fra rammeordren, men stadig har forbindelse til den, kan du oprette en forbindelse mellem en salgsordre og en rammeordre ved at angive det tilhørende rammeordrenummer i feltet **Rammeordrenr.** på salgsordrelinjen.  
- Når salgsordren er oprettet på hele antallet på en rammeordrelinje, kan en anden salgsordre ikke oprettes for den samme linje. Brugere kan ikke indtaste et antal i feltet **Lever antal**. Men hvis det er nødvendigt at føje flere enheder til en rammeordre, kan værdien i feltet **Antal** øges, hvorefter der kan oprettes flere ordrer.  
- Den fakturerede rammesalgsordre bliver liggende i systemet, indtil den slettes, enten ved sletning af bestemte rammesalgsordrer eller ved at køre kørslen **Slet fakturerede rammesalgsordrer**.  
- Hvis en kunde også er registreret som kontakt i modulet Marketing, og du har angivet en interaktionsskabelonkode for rammesalgsordrer på siden **Marketingopsætning**, registreres der en interaktion i tabellen Interaktionslogpost, når du vælger **Udskriv** for at udskrive rammesalgsordrerne.

## <a name="to-view-the-status-of-a-blanket-sales-order"></a>Sådan vises en rammesalgsordres status  
Du kan se den aktuelle status for en rammesalgsordre på siden **Statistik over rammesalgsordrer**. Dette kan være relevant, når du begynder at fakturere den ordre, der er oprettet fra rammesalgsordren.  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rammesalgsordrer**, og vælg derefter det relaterede link.  
2.  Vælg en rammesalgsordre, og vælg derefter handlingen **Statistik**.  
3.  I oversigtspanelet **Generelt** på siden **Statistik over rammesalgsordrer** kan du se en oversigt med oplysninger om hele ordren baseret på den samlede mængde i felterne **Antal** på rammesalgsordrelinjerne.  

- I oversigtspanelet **Fakturering** kan du se en oversigt med oplysninger om hele ordren baseret på den samlede mængde i felterne **Fakturer antal** på rammesalgsordrelinjerne.  
- I oversigtspanelet **Afsendelse** kan du se en oversigt med oplysninger baseret på den samlede mængde i felterne **Modtag (antal)** på rammesalgsordrelinjerne.  
- I oversigtspanelet **Forudbetaling** kan du se en oversigt med oplysninger om alle forudbetalte beløb.  
- Oversigtspanelet **Kreditor** indeholder forskellige stamoplysninger om kreditoren.

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a>Sådan vises ikke-bogførte og bogførte rammesalgsordrelinjer   
Sammenkædningen mellem rammesalgsordre og den oprindelige salgsordre og ethvert andet salgsbilag bevares efter bogføring som en liste over bogførte og ikke-bogførte salgsordrefakturalinjer.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rammesalgsordrer**, og vælg derefter det relaterede link.
2. Åbn den rammesalgsordre, du ønsker at se.
3. Du kan få vist poster, der ikke er bogført, ved at vælge linjen, vælge handlingen **Linje** og derefter vælge handlingen **Ikkebogførte linjer**. Vælg en af følgende indstillinger.  

|Indstilling|Beskrivelse|
|--|--|
|**Ordrer**|Angiver åbne ordrer med tilknytning til den valgte linje.|
|**Fakturaer**|Angiver åbne fakturaer, der har været tilknyttet den valgte linje. Udestående fakturaer knyttes manuelt til en rammeordre, når du angiver rammeordrenummeret på salgsfakturalinjen.|
|**Returvareordrer**|Angiver åbne returvareordrer, der har været tilknyttet den valgte linje.|
|**Kreditnotaer**|Angiver åbne kreditnotaer, der har været tilknyttet den valgte linje.|

4. Du kan få vist bogførte poster ved at vælge linjen, vælge handlingen **Linje** og derefter vælge handlingen **Bogførte linjer**. Vælg en af følgende indstillinger.  

|Indstilling|Beskrivelse|
|---|----|
|**Leverancer**|Bogførte leverancer med tilknytning til den valgte linje.|
|**Fakturaer**|Bogførte fakturaer med tilknytning til den valgte linje.|
|**Returvaremodtagelse**|Bogførte returvaremodtagelser med tilknytning til den valgte linje.|
|**Kreditnotaer**|Bogførte kreditnotaer med tilknytning til den valgte linje.|

5. På siden **Salgslinjer** skal du vælge handlingen **Vis dokument** for at få vist posten.

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Oprette rammemontageordrer](assembly-how-to-create-blanket-assembly-orders.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]