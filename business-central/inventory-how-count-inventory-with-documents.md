---
title: Optæl varelager med dokumentbaserede funktioner
description: Beskriver, hvordan du udfører optælling af varelager ved hjælp af siderne ordreopgørelse og lagerbeholdningsregistrering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, status, negative, positive, increase, decrease
ms.date: 10/20/2020
ms.author: edupont
ms.openlocfilehash: 3403d0536b195517f6924a803342b4301e39591a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750176"
---
# <a name="count-inventory-using-documents"></a>Varelageroptælling ved hjælp af dokumenter

Du kan udføre en status over dine varer på varelager ved hjælp af varelagerdokumenter og varelageroptællingsdokumenter. Siden **Varelageropgørelse** benyttes til at organisere det fulde varelageroptællingsprojekt, for eksempel en pr. lokation. Siden **Registrering af varelager** benyttes til at kommunikere og registrere den faktiske optælling af varerne. Du kan oprette flere registreringer på en ordre, f.eks. til at distribuere varegrupper til forskellige medarbejdere.

Rapporten **Registrering af varelager** kan udskrives fra hver registrering og indeholder tomme felter til at indtaste optalt varelager. Når en bruger er færdig med optællingen, og beholdningen er indtastet på siden **Registrering af varelager**, vælger du handlingen **Afslut**. Dette overfører beholdningen til de relaterede linjer på siden **Varelager**. Funktionaliteten sikrer, at antallet af elementer ikke kan registreres to gange.  

> [!NOTE]
> Denne procedure beskriver, hvordan du foretager en varelageropgørelse ved hjælp af dokumenter, en metode, der giver mere kontrol og understøtter distribution af optælling til flere medarbejdere. Du kan også udføre opgaven ved hjælp af kladder, siderne **Varelageropgørelseskladder** og **Varelagerkladder for lagerbygning**. Du kan finde flere oplysninger i [Tælle, justere og ompostere inventar ved hjælp af kladder](inventory-how-count-adjust-reclassify.md).<br /><br />
> Bemærk, at hvis du bruger funktionen Placeringer eller Zoner, kan du ikke benytte varelageropgørelser. Benyt i stedet siden **Varelageropgørelseskladde for varelager** for at optælle dine varelagerenheder, før du synkroniserer dem med vareenheder i regnskabet.

Optælling af varelager ved hjælp af dokumenter består af følgende overordnede trin:

1. Opret en varelageropgørelse med forventet antal varer udfyldt på forhånd:
2. Generer en eller flere varelageroptællinger ud fra ordren.
3. Indsæt antallet af optalte varer på nedskrivningen, som f.eks. registreret på udskrifter, og indstil den til **Afsluttet**.
4. Gennemfør, og bogfør varelageropgørelsen.

## <a name="to-create-a-physical-inventory-order"></a>Sådan oprettes en varelageropgørelse
En varelageropgørelse er et komplet dokument, der består af et varelageropgørelsesoverskrift og nogle varelageropgørelseslinjer. Oplysningerne på et varelageropgørelseshoved beskriver, hvordan varelageret statusopgøres. Linjerne på varelageropgørelsen indeholder oplysninger om varerne og deres placeringer.

For at oprette linjer til varelageropgørelse benytter du typisk funktionen **Beregn linjer** for at afspejle den nuværende lagerstatus som linjer på opgørelsen. Alternativt kan du bruge funktionen **"Kopiér fra dokument** for at udfylde linjerne med indholdet fra en anden åben eller bogført varelageropgørelse. Den følgende procedure beskriver kun, hvordan du benytter funktionen **Beregn linjer**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lageropgørelsesordrer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld de obligatoriske felter i **Generel** Oversigtspanel. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg handlingen **Beregn linjer**.
5. Vælg påkrævede indstillinger .
6. Indstil f.eks. filtre til kun at omfatte en delmængde af varer, der skal tælles med i den første optælling.

    > [!TIP]
    > For at planlægge, at flere medarbejdere foretager varelageroptælling, er det tilrådeligt at konfigurere forskellige filtre hver gang du benytter handlingen **Beregn linjer** for kun at udfylde ordren med den delmængde af lagervarer, som en bruger optæller. Således minimerer du risikoen for at varer tælles to gange, efterhånden som du generere flere varelageroptællinger for flere medarbejdere. Se sektionen [Sådan oprettes varelageroptælling](#to-create-a-physical-inventory-recording)-sektionen.

7. Vælg knappen **OK**.

En linje for hver vare, der findes på den valgte placering og per opsatte filtre og indstillinger indsættes på ordren. For varer, der er konfigureret til sporing af vare, vælges afkrydsningsfeltet **Benyt sporing af vare** og oplysninger om det forventede antal af serie- og lot-numre er tilgængelige ved at vælge handlingen **Linjer**, og derefter handlingen **Linjer til sporing af varer**. Se sektionen [Håndtering af varesporing i forbindelse med varelageroptælling](#handling-item-tracking-when-counting-inventory) for yderligere oplysninger.

Du kan nu fortsætte med at oprette en eller flere optællinger, som er instruktioner til medarbejderne, som udfører den aktuelle optælling.  

## <a name="to-create-a-physical-inventory-recording"></a>Sådan oprettes en varelageroptælling.
For hver varelageropgørelse kan du oprette et eller flere lageroptællingsdokumenter, på hvilke medarbejderne indsætter de optalte mængder, enten manuelt eller gennem en integreret scanningsenhed.

Som standard oprettes en registrering for alle linjerne på den relaterede varelageropgørelse. For at undgå, at to medarbejdere tæller de samme varer i tilfælde af distribueret optælling, er det tilrådeligt gradvist at udfylde varelageropgørelsen ved at konfigurere filtre på **Beregn linjer**-batchjobbet (se sektionen "Sådan oprettes en lageropgørelsesliste"), og opret så lageroptællingen, og vælg afkrydsningsfeltet **Kun linjer, der ikke findes i registreringer**. Denne indstilling sikrer, at hver ny registrering, som oprettes, kun indeholder varer, der er forskellige varer end andre registreringer.

I tilfælde af manuel optælling kan du printe en liste, rapporten: **Lageroptælling**, som har en tom kolonne, hvor det optalte antal kan skrives. Indtast det optalte antal på de tilhørende linjer på siden **Varelageroptælling**, når optællingen er gennemført. Til sidst overfører du de registrerede antal til den tilhørende varelageropgørelse ved at sætte status til **Afsluttet**.

1. På en side for **Varelageropgørelse**, der indeholder linjer til varerne, der skal tælles, i en optælling, vælger du handlingen **Foretag ny optælling**.
2. Vælg påkrævede indstillinger og konfigurering af filtre.
3. Vælg knappen **OK**.

    Et dokument til varelageregistrering oprettes.

4. For hvert sæt varer, der tælles, loader du dem på en tilhørende varelageropgørelse, og gentag trinnene 1 til 3 med afkrydsningsfeltet **Kun linjer, der ikke findes i registreringer** valgt.

5. Vælg handlingen **Registreringer** for at åbne siden **Liste over varelageropgørelse**.
6. Åbn den relevant registrering.
7. Udfyld felterne efter behov i oversigtspanelet **Generelt**.
8. Opret yderligere en linje for hvert lot-nummer eller serienummerkode for varer, der benytter varesporing, ved at vælge handlingen **Funktioner**, og derefter handlingen **Kopier linje**. Se sektionen [Håndtering af varesporing i forbindelse med varelageroptælling](#handling-item-tracking-when-counting-inventory) for yderligere oplysninger.  
9. Vælg handlingen **Print** for at forberede det fysiske dokument, som medarbejdere skal benytte til at skrive antal optalte varer ned på.

## <a name="to-finish-a-physical-inventory-recording"></a>Sådan afsluttes en varelageroptælling.

Når medarbejderne har optalt varelagerbeholdningerne, skal du klargøre dem til registrering i systemet.

1. Vælg lageroptællingen, som du vil afslutte fra siden **Varelageroptælling**, og vælg så handlingen **Rediger**.
2. Udfyld det aktuelt optalte antal i feltet **Antal** for hver linje på **Linjer** i oversigtspanelet.
3. For varer med serie- eller lotnumre (afkrydsningsfeltet **Benyt varesporing** er valgt), angives det optalte antal på de dertil beregnede linjer for henholdsvis varens serie- og lotnumre. Se sektionen [Håndtering af varesporing i forbindelse med varelageroptælling](#handling-item-tracking-when-counting-inventory) for yderligere oplysninger.
4. Markér afkrydsningsfeltet **Optalt** på hver linje.
5. Når du har indtastet alle data for en varelageroptælling, vælger du handlingen **Afslut**. Bemærk, at alle linjer skal have afkrydsningsfeltet **Registreret** valgt.

> [!NOTE]
> Når du afslutter en varelageroptælling, overføres hver linje til linjen på den tilhørende lageropgørelsesliste, der matcher den nøjagtigt. Værdierne i felterne **Varenr.**, **Variantkode**, **Lokationskode** og **Placeringskode** skal være de samme på registreringen og ordrelinjerne for at matche.<br /><br />
> Hvis der ikke findes nogen varelagerlinjer, og hvis afkrydsningsfeltet **Tillad registrering uden Ordre** er valgt, vil en ny linje automatisk blive indsat, og afkrydsningsfeltet **Registreret uden ordre"** på den tilhørende lageropgørelsesordrelinje vælges. Eller vises en fejlmeddelelse, og processen annulleres.<br /><br />
> Hvis mere end en varelageroptællingslinje matcher en linje på lageroptællingsordren, vises en meddelelse, og processen annulleres. Hvis to identiske varelageropgørelseslinjer af en eller anden grund ender på lageropgørelsesordren, kan du benytte en funktion for at løse dette. Se sektionen [Sådan findes to ens varelageropgørelseslinjer](#to-find-duplicate-physical-inventory-order-lines) for yderligere information.

## <a name="to-complete-a-physical-inventory-order"></a>Sådan afsluttes en varelageropgørelse
Når du har afsluttet en varelageroptælling, opdateres feltet **Optælling af antal (basis)** på den tilhørende varelageropgørelse med de optalte (registrerede) værdier, og afkrydsningsfeltet **Registreret** er valgt. Hvis en optalt værdi afviger fra det forventede, vises den difference henholdsvis i feltet **Positivt antal (basis)** og **Negativt antal (basis)**.

For at se forventet antal og enhver registreret difference for varer med varesporing, vælges handlingen **Linjer**, og derefter vælges handlingen **Varesporingslinje** for at udvælge forskellige visninger for serie- og lotnumre, der er findes i varelageroptællingen.

Du kan også vælge handlingen **Difference i lageropgørelsesordre** for at få vist eventuelle forskelle mellem det forventede antal og det optalte antal.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a>Sådan findes dobbeltoprettede linjer til varelageropgørelse

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lageropgørelsesordrer**, og vælg derefter det relaterede link.
2. Åbn varelageropgørelsen, som du ønsker at se dobbelt oprettede linjer for.
3. Vælg handlingen **Vis dobbelt oprettede linjer**.

Alle dobbelt oprettede varelageropgørelseslinjer vises, så du kan slette dem og kun beholde en linje med et unikt værdisæt for de fire felter **Varenr.**, **Variantkode**, **Lokationskode**, og **Placeringskode**.

### <a name="to-post-a-physical-inventory-order"></a>Sådan bogføres en varelageropgørelse
Når du har færdigudarbejdet en varelageropgørelse og ændret dens status til **Afsluttet**, kan du postere den. Du kan kun ændre en status for varelageropgørelse til **Afsluttet**, hvis følgende er sandt:

- Alle relaterede registreringer for varelageropgørelse har status **Afsluttet**.
- Hver lageropgørelseslinje er blevet optalt af mindst en varelagerregistreringslinje.
- Afkrydsningsfelterne **I registreringslinjer** og **Antal forventet beregnet** er valgt for alle linjer i varelageropgørelsesordren.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lageropgørelsesordrer**, og vælg derefter det relaterede link.
2. Vælg den varelageropgørelse, som du vil afslutte, og vælg derefter handlingen **Rediger**.

    På siden **Varelageropgørelse** kan du se det registrerede antal i feltet **Antal registreret (basis)**.
3. Vælg handlingen **Afslut**.

    Værdien i feltet **Status** ændres til **Afsluttet**, og du kan nu kun ændre opgørelsen ved først at vælge handlingen **Genåbn**.
4. Vælg handlingen **Bogfør** for at bogføre ordren, og vælg derefter knappen **OK**.

De aktuelle vareposter i regnskabet opdateres sideløbende med alle aktuelle varesporingsposter.

### <a name="to-view-posted-physical-inventory-orders"></a>Sådan vises bogførte varelageropgørelser
Efter bogføringen vil varelageropgørelsen blive slettet, og du kan få vist og vurdere dokumentet som en bogført lageropgørelsesordre med dets lageropgørelsesregistreringer og enhver kommentar, der er evt. er tilføjet.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte lageropgørelsesordrer**, og vælg derefter det relaterede link.
2. Vælg den bogførte lageropgørelsesordre, som du vil se, på siden **Bogførte varelageropgørelser**, og vælg så handlingen **Vis**.
3. Vælg handlingen **Registreringer** for at åbne en liste over relaterede registreringer af varelageropgørelser.

## <a name="handling-item-tracking-when-counting-inventory"></a>Håndtering af varesporing ved optælling af varelager
Varesporing angår serie- eller lotnumrene, der er tildelt varer Når en vare tælles, som angivet i varelagerbeholdningen som f.eks. 10 forskellige lotnumre, skal medarbejderne kunne registrere, hvilke og hvor mange enheder af hver lotnummer, der er på lager. Se [Arbejde med serie- eller lotnumre](inventory-how-work-item-tracking.md) for at få yderligere information om varesporingsfunktion.

Afkrydsningsfeltet **Benyt varesporing** på varelageropgørelseslinjer vælges automatisk, hvis en varesporingskode er konfigureret til varen, men du kan også vælge eller fravælge den manuelt.

### <a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a>Eksempel - Klargør en registrering af varelageropgørelse for en vare-sporet vare
En varelageropgørelse for vare A, der er lagerført som ti forskellige serienumre.
1. Vælg afkrydsningsfeltet **Benyt varesporing** på registreringslinjen for varen.
2.  Vælg feltet **Serienr.**, vælg det første serienummer, der findes på lager for varen, og vælg derefter knappen **OK**.

    Kopier dernæst linjen for den første "vare-sporet" vare for at indsætte yderligere linjer svarende til nummeret for serienumre, der er angivet i varelagerbeholdningen.

3. Vælg handlingen **Funktioner**, og vælg derefter handlingen **Kopier linje**.
4. Indsæt 9 i feltet **Antal kopier** på siden **Kopier lageropgørelsesregistreringslinje**, og vælg dernæst knappen **OK**.
5. Vælg feltet **Serienr.** på den første kopilinje, og vælg det næste serienummer for varen.
6. Gentag trin 5 for de resterende otte serienumre, og vær opmærksom på ikke at vælge det samme to gange.
7. Vælg handlingen **Print** for at forberede det fysiske dokument, som medarbejdere skal benytte til at skrive antal optalte varer og serie/lotnumre ned på.

Bemærk, at rapporten **Lageropgørelsesregistrering** indeholder ti linjer for vare A, en for hvert serienummer.

### <a name="example---record-and-post-counted-lot-number-differences"></a>Eksempel - Registrer og bogfør optalte differencer i lotnumre
En lot-sporet vare er angivet i varelagerbeholdningen med "LOT"-nummerserier.

**Forventet varelager**.

|Lotnr.|Antal|
|-|-|
|LOT1001|80|
|LOT1003|30|
|LOT1006|10|
|Total|120|

**Rapporteret antal**:

|Lotnr.|Antal|
|-|-|
|LOT1001|80|
|LOT0002|12|
|LOT1003|20|
|LOT1006|10|
|Total|112|

**Antal til bogføring**:

|Lotnr.|Forventet antal|Registreret beholdning|Beholdning til bogføring|
|-|-|-|-|
|LOT1001|80|80|0|
|LOT1002|0|12|+12|
|LOT1003|30|20|-10|
|LOT1006|10|0|-10|
|Total|120|112|-8|

På siden **Varelageropgørelse** indeholder feltet **Negativ beholdning (basis)** *8*. Siden **Varesporingsliste for lageropgørelse** indeholder den positive eller negative beholdning for de individuelle lotnumre for den pågældende ordrelinje.

## <a name="see-also"></a>Se også

[Tælle, justere og ompostere inventar ved hjælp af kladder](inventory-how-count-adjust-reclassify.md)  
[Arbejde med serienumre og lotnumre](inventory-how-work-item-tracking.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Logistik](warehouse-manage-warehouse.md)    
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]