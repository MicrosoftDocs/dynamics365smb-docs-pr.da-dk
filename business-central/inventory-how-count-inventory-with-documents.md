---
title: Tælle og justere lageropgørelse
description: 'Beskriver, hvordan du kan optælle lageropgørelse og bruge lagerdokumenter til at regulere den disponible lagerbeholdning.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: 'adjustment, status, negative, positive, increase, decrease, inventory'
ms.search.forms: '5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783'
ms.date: 03/11/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Tælle og regulere lageropgørelse ved hjælp af dokumenter

Du kan udføre en status over dine varer på varelager ved hjælp af varelagerdokumenter og varelageroptællingsdokumenter. Siden **Varelageropgørelse** benyttes til at organisere det fulde varelageroptællingsprojekt, for eksempel en pr. lokation. Brug siden **Opgørelse af fysisk lager** til at registrere og kommunikere den faktiske optælling af varer. Du kan oprette flere registreringer på en ordre, f.eks. for at distribuere varegrupper til forskellige medarbejdere.

Du kan udskrive rapporten **Opgørelse af fysisk lager** fra hver registrering, og den indeholder tomme mængdefelter, hvor du kan indtaste optalt varelager. Når du er færdig med optællingen, og mængderne er indtastet på siden **Opgørelse af fysisk lager**, skal du vælge handlingen **Afslut**. Denne handling overfører beholdningen til de relaterede linjer på siden **Lageropgørelsesordre**. [!INCLUDE [prod_short](includes/prod_short.md)] sikrer, at du ikke kan registrere et vareantal to gange.  

> [!NOTE]
> Brug af dokumenter til at udføre en fysisk lageropgørelse giver mere kontrol og understøtter distribution af optælling til flere medarbejdere. Du kan også bruge kladderne til at udføre opgaven, f.eks. siderne **Varelageropgørelseskladder** og **Lagerplaceringsopgørelseskladder**. Du kan få mere at vide ved at gå til [Tælle, justere og ompostere lagerbeholdning ved hjælp af kladder](inventory-how-count-adjust-reclassify.md) Denne artikel beskriver, hvordan du bruger dokumenter til at udføre en fysisk lageropgørelse.
>
> Hvis du bruger zoner på dit lagersted, kan du ikke bruge fysiske lageropgørelsesordrer. Benyt i stedet siden **Varelageropgørelseskladde for varelager** til at optælle dine varelagerenheder, før du synkroniserer dem med vareposter.

Optælling af varelager ved hjælp af dokumenter består af følgende overordnede trin:

1. Opret en varelageropgørelse med forventet antal varer udfyldt på forhånd:
2. Generer en eller flere varelageroptællinger ud fra ordren.
3. Indsæt antallet af optalte varer på nedskrivningen, som f.eks. registreret på udskrifter, og indstil den til **Afsluttet**.
4. Gennemfør, og bogfør varelageropgørelsen.

## Sådan oprettes en varelageropgørelse

En varelageropgørelse er et komplet dokument, der består af et varelageropgørelsesoverskrift og ordrelinjer. Oplysningerne på et varelageropgørelseshoved beskriver, hvordan varelageret statusopgøres. Ordrelinjerne indeholder oplysninger om varerne og deres placeringer.

For at oprette linjer til varelageropgørelse benytter du typisk handlingen **Beregn linjer** til at tilføje den nuværende lagerstatus som linjer på ordren. Du kan også bruge handlingen **Kopier fra dokument** til at udfylde linjerne med indholdet fra en anden åben eller bogført varelageropgørelse. Den følgende procedure beskriver kun, hvordan du benytter handlingen **Beregn linjer**.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **lageropgørelsesordrer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld de obligatoriske felter i **Generel** Oversigtspanel. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg handlingen **Beregn linjer**.
5. Vælg påkrævede indstillinger .
6. Indstil f.eks. filtre til kun at omfatte en delmængde af varer, der skal tælles med i den første optælling.

    > [!TIP]
    > For at planlægge, at flere medarbejdere foretager varelageroptælling, skal du konfigurere forskellige filtre hver gang, du benytter handlingen **Beregn linjer** for at udfylde ordren med den delmængde af lagervarer, som en bruger optæller. Således minimerer du risikoen for at varer tælles to gange, efterhånden som du generere flere varelageroptællinger for flere medarbejdere. Du kan få mere at vide ved at gå til [Sådan oprettes en varelageroptælling](#to-create-a-physical-inventory-recording).

7. Vælg knappen **OK**.

En linje for hver vare, der findes på den valgte placering og pr. opsatte filtre og indstillinger føjes til ordren. For varer, der er konfigureret til sporing af vare, vælges afkrydsningsfeltet **Benyt sporing af vare** og oplysninger om det forventede antal af serie- og lotnumre er tilgængelige ved at vælge handlingen **Linjer** og derefter **Linjer til sporing af varer**. Du kan få mere at vide ved at gå til [Håndtering af varesporing ved optælling af varelager](#handle-item-tracking-when-counting-inventory).

Du kan nu oprette en eller flere optællinger, som er instruktioner til medarbejderne, der udfører optællingen.  

> [!NOTE]
> Hvis du bruger pakkespecifik sporing, kan du også bruge dokumenter til at optælle og regulere lagerbeholdningen med pakkenumre. Hvis du vil begynde at bruge denne funktion, skal du aktivere **Funktionsopdatering: Aktivér brug af pakkesporing i lageropgørelsesordrer** på siden **Funktionsstyring**. Eksisterende lageropgørelsesordrer opdateres, men [!INCLUDE [prod_short](includes/prod_short.md)] kan ikke udfylde **pakkenummeret**. . Du skal genskabe disse linjer ved hjælp af handlingen **Beregn linjer** på siden **Lageropgørelsesordre**.
>
> Du kan angive pakkenummeret for varer, hvor pakkesporing er nødvendig, på siden **Registreringslinjer for fysisk lager**. Vælg **Udfør** for at afslutte registreringen.
>
> Når du har valgt **Udfør** på siden **Lageropgørelsesordre**, beregner [!INCLUDE [prod_short](includes/prod_short.md)] differencer med hensyn til pakken og andre varesporingsdetaljer, og der foretages positive eller negative reguleringer.

## Sådan oprettes en varelageroptælling.

For hver lageropgørelsesordre kan du oprette et eller flere dokumenter til registrering af lageropgørelsen, hvor medarbejderne indtaster de optalte mængder. Mængder kan indtastes manuelt eller vha. en scanningsenhed.

Som standard oprettes en registrering for alle linjerne på den relaterede varelageropgørelse. For at undgå, at to medarbejdere tæller de samme varer, hvis du fordeler optællingen, skal du gradvist udfylde lageropgørelsesordren ved at angive filtre i kørslen **Beregn linjer**. Opret derefter varelageroptællingen med afkrydsningsfeltet **Kun linjer, der ikke findes i registreringer** markeret. Denne indstilling sikrer, at hver ny optælling kun indeholder varer, der ikke findes i andre optællinger.

I tilfælde af manuel optælling kan du udskrive rapporten **Lageroptælling**, som har en tom kolonne, hvor lagerstedsmedarbejdere kan skrive de optalte mængder. Indtast det optalte antal på de tilhørende linjer på siden **Varelageroptælling**, når optællingen er gennemført. Til sidst overfører du de registrerede antal til den tilhørende varelageropgørelse ved at sætte status til **Afsluttet**.

1. På en side for **Varelageropgørelse**, der indeholder linjer til varerne, der skal tælles, i en optælling, vælger du handlingen **Foretag ny optælling**.
2. Vælg påkrævede indstillinger og konfigurering af filtre.
3. Vælg knappen **OK**.
4. For hvert sæt varer, der tælles, skal du indlæse dem på en tilhørende varelageropgørelse og gentage trin 1-3 med afkrydsningsfeltet **Kun linjer, der ikke findes i registreringer** valgt.
5. Vælg handlingen **Registreringer** for at åbne siden **Liste over varelageropgørelse**.
6. Åbn den relevant registrering.
7. Udfyld felterne efter behov i oversigtspanelet **Generelt**.
8. Opret yderligere en linje for hvert lot-nummer eller serienummerkode for varer, der benytter varesporing, ved at vælge handlingen **Funktioner**, og derefter handlingen **Kopier linje**. Du kan få mere at vide ved at gå til [Håndtering af varesporing ved optælling af varelager](#handle-item-tracking-when-counting-inventory).  
9. Vælg handlingen **Udskriv** for at forberede det fysiske dokument, som medarbejdere kan benytte til at skrive det antal, de tæller.

## Sådan afsluttes en varelageroptælling.

Når medarbejderne har optalt antallet, skal du registrere mængderne i [!INCLUDE [prod_short](includes/prod_short.md)].

1. Vælg lageroptællingen, som du vil afslutte fra siden **Varelageroptælling**, og vælg så handlingen **Rediger**.
2. Udfyld det aktuelt optalte antal i feltet **Antal** for hver linje på **Linjer** i oversigtspanelet.
3. For varer med serie- eller lotnumre (afkrydsningsfeltet **Benyt varesporing** er valgt), angives det optalte antal på linjerne for henholdsvis varens serie- og lotnumre. Du kan få mere at vide ved at gå til [Håndtering af varesporing ved optælling af varelager](#handle-item-tracking-when-counting-inventory).
4. Markér afkrydsningsfeltet **Optalt** på hver linje.
5. Når du har indtastet alle data for en varelageroptælling, vælger du handlingen **Afslut**. Bemærk, at alle linjer skal have afkrydsningsfeltet **Registreret** valgt.

    > [!NOTE]
    > Når du afslutter en varelageroptælling, overføres hver linje til linjen på den tilhørende lageropgørelsesliste, der matcher den nøjagtigt. Værdierne i felterne **Varenr.**, **Variantkode**, **Lokationskode** og **Placeringskode** skal være de samme på registreringen og ordrelinjerne for at matche.>
    > 
    > Hvis der ikke findes en matchende varelagerlinje, og hvis afkrydsningsfeltet **Tillad registrering uden ordre** er markeret, tilføjes der en ny linje, og afkrydsningsfeltet **Registreret uden ordre"** på den tilhørende lageropgørelsesordrelinje vælges. Eller vises en fejlmeddelelse, og processen annulleres. Hvis mere end en varelageroptællingslinje matcher en linje på lageroptællingsordren, vises der en meddelelse, og processen annulleres. Hvis to identiske varelageropgørelseslinjer af en eller anden grund ender på lageropgørelsesordren, kan du benytte en handling for at løse dette. Du kan få mere at vide ved at gå til [Sådan findes dobbeltoprettede linjer til varelageropgørelse](#to-find-duplicate-physical-inventory-order-lines).

## Sådan afsluttes en varelageropgørelse

Når du har afsluttet en varelageroptælling, opdateres feltet **Optælling af antal (basis)** på den tilhørende varelageropgørelse med de optalte (registrerede) værdier, og afkrydsningsfeltet **Registreret** er valgt. Hvis en optalt mængde afviger fra den forventede mængde, vises differencen i felterne **Positivt antal (basis)** og **Negativt antal (basis)**.

For at få adgang til det forventede antal og enhver registreret difference for varer med varesporing, skal du vælge handlingen **Linjer**, og derefter skal du vælge **Varesporingslinje** for at vælge forskellige visninger for de serie- og lotnumre, der er findes i varelageroptællingen.

Du kan også vælge handlingen **Difference i lageropgørelsesordre** for at få vist eventuelle forskelle mellem det forventede antal og det optalte antal.

### Sådan findes dobbeltoprettede linjer til varelageropgørelse

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **lageropgørelsesordrer**, og vælg derefter det relaterede link.
2. Åbn varelageropgørelsen, du vil have vist dobbelt oprettede linjer for.
3. Vælg handlingen **Vis dobbelt oprettede linjer**.

Dobbelt fysiske varelageropgørelseslinjer vises, så du kan slette dem og kun beholde en linje med et unikt værdisæt for de fire felter **Varenr.**, **Variantkode**, **Lokationskode**, og **Placeringskode**.

### Sådan bogføres en varelageropgørelse

Når du har færdigudarbejdet en varelageropgørelse og ændret dens status til **Afsluttet**, kan du bogføre den. Du kan kun ændre status for en varelageropgørelse til **Afsluttet** under følgende forhold:

- Alle relaterede registreringer for varelageropgørelse har status **Afsluttet**.
- Hver lageropgørelseslinje er optalt af mindst en varelagerregistreringslinje.
- Afkrydsningsfelterne **I registreringslinjer** og **Antal forventet beregnet** er valgt for alle linjer i varelageropgørelsesordren.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **lageropgørelsesordrer**, og vælg derefter det relaterede link.
2. Vælg den varelageropgørelse, som du vil afslutte, og vælg derefter handlingen **Rediger**.

    På siden **Varelageropgørelse** vises det registrerede antal i feltet **Antal registreret (basis)**.
3. Vælg handlingen **Afslut**.

    Værdien i feltet **Status** er **Afsluttet**. Du kan nu kun ændre rækkefølgen ved at vælge handlingen **Åbn igen**.
4. Vælg handlingen **Bogfør** for at bogføre ordren, og vælg derefter knappen **OK**.

    Vareposterne i regnskabet opdateres sideløbende med alle aktuelle varesporingsposter.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

### Sådan vises bogførte varelageropgørelser

Efter bogføringen slettes varelageropgørelsen, og du kan få vist og vurdere dokumentet som en bogført lageropgørelsesordre. Den bogførte ordre indeholder optællinger af det fysiske lager og eventuelle bemærkninger.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte lageropgørelsesordrer**, og vælg derefter det relaterede link.
2. Vælg den bogførte lageropgørelsesordre, som du vil se, på siden **Bogførte varelageropgørelser**, og vælg så handlingen **Vis**.
3. Vælg handlingen **Registreringer** for at åbne en liste over relaterede registreringer af varelageropgørelser.

## Håndtering af varesporing ved optælling af varelager

Varesporing er relateret til serie- eller lotnumrene, der er tildelt varer. Når du tæller en vare, som opbevares i varelagerbeholdningen, f.eks. 10 forskellige lotnumre, skal medarbejderne kunne registrere, hvilke og hvor mange enheder af hver lotnummer der er på lager. Du kan finde flere oplysninger i [Arbejde med serienumre og lotnumre](inventory-how-work-item-tracking.md).

Afkrydsningsfeltet **Benyt varesporing** på varelageropgørelseslinjer vælges automatisk, hvis en varesporingskode er konfigureret til varen. Du kan markere eller fjerne markeringen i afkrydsningsfeltet manuelt.

### Eksempel - Klargør en varelageroptælling for en vare-sporet vare

En varelageropgørelse for vare A, der er lagerført som ti forskellige serienumre.

1. Vælg afkrydsningsfeltet **Benyt varesporing** på registreringslinjen for varen.
2. Vælg feltet **Serienr.**, vælg det første serienummer, der findes på lager for varen, og vælg derefter knappen **OK**.

    Kopier dernæst linjen for den første "vare-sporet" vare for at indsætte yderligere linjer, der svarer til nummeret for serienumre, der er angivet i varelagerbeholdningen.

3. Vælg handlingen **Funktioner**, og vælg derefter **Kopier linje**.
4. Indsæt **9** i feltet **Antal kopier** på siden **Kopier lageropgørelsesregistreringslinje**, og vælg dernæst knappen **OK**.
5. Vælg feltet **Serienr.** på den første linje, og vælg det næste serienummer for varen.
6. Gentag trin 5 for de resterende otte serienumre. Sørg for, at du ikke vælger det samme nummer to gange.
7. Vælg handlingen **Udskriv** for at forberede det fysiske dokument, som medarbejdere skal benytte til at skrive antal optalte varer og serie/lotnumre ned på.

Bemærk, at rapporten **Lageropgørelsesregistrering** indeholder ti linjer for vare A, en for hvert serienummer.

### Eksempel – Registrer og bogfør differencer i optalte lotnumre

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

På siden **Varelageropgørelse** indeholder feltet **Negativ beholdning (basis)** **8**. Siden **Varesporingsliste for lageropgørelse** viser den positive eller negative beholdning for de enkelte lotnumre for ordrelinjen.

## Lageropgørelsesdokumenter

Følgende dokumenttyper er nyttige til administration af lagerstedet:

* Brug **lagermodtagelser** til at registrere positive reguleringer af varer baseret på kvalitet, antal og kostpris.
* Brug **lagerleverancer** til at afskrive manglende eller beskadigede varer.

Du kan udskrive disse dokumenter på ethvert trin, frigive og åbne dem igen og tildele dem fælles værdier, f.eks. dimensioner, i sidehovedet. Hvis du vil udskrive dokumenterne igen, efter at de er bogført, skal du bruge siderne **Bogført lagermodtagelse** og **Bogført lagerforsendelse**.

> [!NOTE]
> Før du kan bruge disse dokumenter, skal du angive en nummerserie for at oprette deres id'er. Du kan få mere at vide ved at gå til [Sådan oprettes nummerering for lagerdokumenter](#to-set-up-numbering-for-inventory-documents).

### Sådan oprettes nummerering for lagerdokumenter

Følgende procedure viser, hvordan du konfigurerer nummerering for lageropgørelsesdokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af Lager**, og vælg derefter det relaterede link.
2. I oversigtspanelet **Nummerering** skal du angive nummerserier for dokumenter i følgende felter:

   - **Lagermodtagelsesnumre**  
   - **Bogførte lagermodtagelsesnumre**  
   - **Lagerleverancenumre**  
   - **Bogførte lagerleverancenumre**  

### Sådan oprettes og bogføres et lagerdokument

Følgende fremgangsmåde viser, hvordan du kan oprette, udskrive og bogføre en lagertilgang. Fremgangsmåden er den samme som for lagerleverancer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermodtagelser**, og vælg derefter det relaterede link.  
2. Vælg lokationen i feltet **Lokationskode** i sidehovedet for **Lagermodtagelse** , og udfyld derefter de resterende felter efter behov.
3. I oversigtspanelet **Linjer** i feltet **Vare** skal du vælge lagervaren. Angiv det antal varer, du vil tilføje, i feltet **Antal**.
4. Hvis du vil udskrive en rapport for **Lagermodtagelse** fra siden **Lagermodtagelse**, skal du vælge handlingen **Udskriv**.

Du kan vælge mellem følgende funktioner på siden **Lagermodtagelse**:

- Vælg handlingerne **Frigiv** eller **Genåbn** for at angive status for næste behandlingsfase.  
- Vælg handlingen **Bogfør** for at bogføre lagermodtagelsen, eller vælg **Bogfør og udskriv** for at bogføre modtagelsen og udskrive testrapporten.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Udskrivning af lageropgørelsesdokumenter

Du kan angive, hvilke rapporter der skal udskrives i forskellige faser, ved at vælge en af følgende indstillinger i feltet **Forbrug** på siden **Rapportvalg - lager**:

* Lagermodtagelse
* Lagerleverance
* Bogført lagerkvittering
* Bogført lagerforsendelse

> [!NOTE]
> De tilgængelige rapporter kan variere afhængigt af dit lands/områdes lokalisering. Basisprogrammet indeholder ikke layoutelementer.

## Se også

[Tælle, justere og ompostere lagerbeholdning ved hjælp af kladder](inventory-how-count-adjust-reclassify.md)  
[Arbejde med serienumre og lotnumre](inventory-how-work-item-tracking.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Oversigt over logistik](design-details-warehouse-management.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
