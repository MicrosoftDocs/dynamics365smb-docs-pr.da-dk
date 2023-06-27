---
title: 'Spore varer med serie-, lot- og pakkenumre'
description: 'Du kan tilføje serie-, lot- og pakkenumre til ethvert udgående eller indgående bilag, og dets posterede varesporing vises i de relaterede vareposter.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 08/31/2021
ms.author: edupont
---
# <a name="track-items-with-serial-lot-and-package-numbers"></a>Spore varer med serie-, lot- og pakkenumre

Du kan tildele serie-, lot- og pakkenumre til ethvert udgående eller indgående bilag, og dets posterede varesporing vises i de relaterede vareposter. Du kan udføre arbejdet på siden **Varesporingslinjer**, som du kan åbne fra et indgående eller udgående dokument.

Matrixen for mængdefelter øverst på siden **Varesporingslinjer** viser mængder og summer for de varesporingsnumre, der defineres på linjerne. Mængderne skal svare til mængderne på dokumentlinjen, der er angivet med 0 i felterne **Udefineret**.

Af hensyn til ydeevnen indsamler programmet kun disponeringsoplysninger på siden **Varesporingslinjer** én gang, når du åbner siden. Det betyder, at programmet ikke opdaterer disponeringsoplysningerne, mens du har siden åben – heller ikke selvom der sker ændringer i lageret eller i andre dokumenter.

> [!NOTE]  
>  Hvis du vil arbejde med de funktioner, der er beskrevet i denne artikel, skal du først oprette varesporing. Se [Konfigurere varesporing med serie-, lot og pakkenumre](inventory-how-setup-item-tracking.md) for at få yderligere information.

## <a name="item-tracking-availability"></a>Tilgængelighed af varesporing

Når du arbejder med serie-, lot- og pakkenumre, beregner [!INCLUDE[prod_short](includes/prod_short.md)] tilgængelighedsoplysningerne og viser dem på de forskellige sider for varesporing. På denne måde kan du se, hvor meget af et lot-, pakke- eller serienummer der i øjeblikket er anvendt i andre dokumenter. Dette reducerer fejl og usikkerhed, der skyldes dobbelte tildelinger.

På siden **Varesporingslinjer** vises et advarselsikon i feltet **Lotnr.disponering** eller feltet **Serienr.disponering**, hvis nogle eller alle af det valgte antal allerede bruges i andre dokumenter, eller hvis lot- eller serienummeret ikke er tilgængeligt.

På siden **Serienr./lotnr. - liste**, siden **Serienr./lotnr. - disponering** og siden **Varesporing - vælg poster** vises oplysninger om, hvor mange af en vare der bruges. Dette omfatter følgende oplysninger.

|Felt|Beskrivelse|
|-----|-----------|  
|**I alt**|Det samlede antal varer på lager|
|**Ønsket antal i alt**|Det samlede antal varer, der ønskes til brug i dette og andre dokumenter|
|**Aktuelt ventende antal**|Det antal varer, der ønskes brugt i det aktuelle dokument, men som endnu ikke er sendt til databasen|
|**Aktuelt bestilt antal**|Det antal varer, der vil blive brugt i det aktuelle dokument|
|**Beholdning i alt**|Det samlede antal varer på lager minus det antal af varen, der ønskes brugt i dette og andre dokumenter (ønsket antal i alt) minus det antal, der ønskes, men som endnu ikke er sendt i dette dokument (aktuelt ventende antal)|

Hvis du arbejder på siden **Varesporingslinjer** i lang tid, eller hvis der er stor aktivitet omkring den vare, du arbejder med, kan du vælge handlingen **Opdater disponering**. Varedisponeringen kontrolleres også automatisk, når du lukker siden, så det kontrolleres, at der ikke er nogen disponeringsproblemer.

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Sådan tildeles serie- eller lotnumre under indgående transaktioner

Mange virksomheder ønsker at holde styr på varer, lige så snart de modtager dem. I denne situation er købsordren ofte det centrale dokument, selvom varesporing kan håndteres fra alle indgående bilag, og de tilhørende poster kan ses i de tilknyttede vareposter.

På den måde overføres numrene automatisk gennem alle udgående lageraktiviteter uden interaktion af lagermedarbejdere.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.  
2. Åbn en eksisterende købsordre eller opret en ny.
3. Markér den relevante dokumentlinje, og vælg handlingen **Linje** i oversigtspanelet **Linjer**, og vælg derefter handlingen **Varesporingslinjer** for at åbne siden **Rediger - varesporingslinjer**.  

    Du kan tildele serie- eller lotnumre på følgende måder:  
    -   Automatisk ved at vælge **Behandle** og derefter **Tildel serienr.** eller **Tildel lotnr.** for at tildele serienumre/lotnumre fra foruddefinerede nummerserier.  
    -   Automatisk ved at vælge **Behandle** og derefter **Oprette brugerdefineret serienr.** for at tildele serienumre/lotnumre baseret på de parametre, du definerer for de ankomne varer.  
    -   Manuelt ved at angive serie- eller lotnumre direkte, f.eks. kreditornumrene.  
    -   Manuelt ved at tildele et specifikt nummer til hver vareenhed.  

4. Hvis du vil tildele automatisk, skal du vælge handlingen **Opret brugerdef. serienr.**.  
5. Angiv startnummeret i en beskrivende serienummerserie, f.eks. **S/N-Vend0001**, i feltet **Brugerdef. serienr.**.  
6. Indtast 1 i feltet **Forøgelse** for at angive, at hvert fortløbende nummer stiger med 1.  

    Feltet **Antal, der skal oprettes** indeholder standardlinjeantallet, men dette kan ændres.  

7. Marker afkrydsningsfeltet **Opret nyt lotnr.** for at organisere de nye serienumre i en bestemt lot.  
7. Vælg knappen **OK**.  

Der oprettes nu et lotnummer med individuelle serienumre i overensstemmelse med vareantallet på dokumentlinjen, startende med **S/N-Vend0001**.  

Matrixen for mængdefelter på hovedet viser, dynamisk, mængder og summer for de varesporingsnumre, du angiver på siden. Mængderne skal svare til mængderne på dokumentlinjen, der er angivet med 0 i felterne **Udefineret**.  

Når dokumentet er bogført, overføres varesporingsposterne til de tilknyttede vareposter.

### <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Sådan håndteres serie- og lotnumre, når der hentes modtagelseslinjer fra en købsfaktura

Hvis du bruger funktioner til at få bogførte modtagelses- eller afsendelseslinjer fra relaterede fakturaer eller kreditnotaer, så overføres alle varesporingslinjer på lagerdokumenter automatisk, men de behandles de på en særlig måde.

Funktionen understøtter følgende indgående processer:  
-   **Hent købsleverancelinjer** – fra en købsfaktura.  
-   **Hent returvarelev.linjer** – fra en købskreditnota.  

Funktionen understøtter følgende udgående processer:  
-   **Hent salgsleverancelinjer** – fra en salgsfaktura eller kombinerede leverancer.  
-   **Hent returvaremodt.linjer** – fra en salgskreditnota.  

I disse situationer kopieres de eksisterende varesporingslinjer automatisk til fakturaen eller kreditnotaen, men siden **Varesporingslinjer** tillader ikke, at serie- eller lotnumre ændres. Det er kun mængderne, der kan ændres.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. Åbn en købsfaktura for varer, der er køb med serienumre eller lotnumre.  
3. Fra en købsfakturalinje skal du i oversigtspanelet **Linjer** vælge handlingen **Hent købsleverancelinjer**.  
4. Vælg en modtagelseslinje, der har varesporingslinjer på siden **Hent købsleverancelinjer**, og vælg derefter knappen **OK**.  

    Kildedokumentet kopieres til købsfakturaen som en ny linje, og dets varesporingslinjer overføres uændret til den underliggende side **Varesporingslinjer**.  

5. Vælg den overførte modtagelseslinje i købsfakturaen.  
6. I oversigtspanelet **Linjer** skal du vælge handlingen **Linje** og derefter vælge handlingen **Varesporingslinjer** for at få vist de overførte varesporingslinjer.  

Du kan ikke ændre felterne **Serienr.** og **Lotnr.** Du kan imidlertid slette hele linjer eller ændre mængder, så de svarer til de ændringer, der er foretaget på kildelinjen.  

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Sådan tildeles serie- eller lotnumre under en udgående transaktion

Udgående håndtering af serie eller lotnumre er en almindeligt forekommende opgave i mange forskellige lagerprocesser. Serie- og lotnumre kan føjes til udgående transaktioner på to måder:  

-   Vælg fra eksisterende serie- eller lotnumre. Bruges, når der allerede er blevet tildelt varesporingsnumre i forbindelse med en indgående transaktion.
-   Tildeling af nye serie- eller lotnumre under udgående transaktioner. Dette gælder, når varesporingsnumre ikke skal tildeles til varer, før de er solgt og klar til at blive afsendt.

### <a name="to-select-from-existing-serial-or-lot-numbers"></a>Sådan vælges der fra eksisterende serienumre eller lotnumre

Når du arbejder med varer, der kræver varesporing, og du opretter udgående transaktioner, hvor varerne forlader lageret, skal du som regel vælge lot- eller serienumrene ud fra dem, der allerede findes på lageret.

1. Marker den linje, du vil vælge et lot- eller serienummer til, i et hvilket som helst udgående dokument.  
2. I oversigtspanelet **Linjer** skal du vælge handlingen **Linje**, derefter **Relaterede oplysninger** og derefter **Varesporingslinjer**.  
3. På siden **Varesporingslinjer** har du tre muligheder for at vælge lot- eller serienumre:  

    - Klik på feltet **Serienr.**, og vælg derefter et nummer på siden **Serienummerliste**.
    - Klik på feltet **Lotnr.**, og vælg derefter et nummer på siden **Lotnummerliste**. Klik derefter på feltet **Serienr.**, og vælg derefter et nummer på siden **Serienummerliste**.
    - Vælg handlingen **Behandle** og derefter **Angiv poster**. Siden **Marker poster** viser alle lot- og serienumre sammen med disponeringsoplysninger.

4. I feltet **Valgt antal** skal du angive antallet for hvert af de lot- eller serienumre, du vil bruge.
5. Klik på **OK**, hvorefter programmet overfører de valgte varesporingsoplysninger på siden **Varesporingslinjer**.  

Matrixen for mængdefelter på hovedet viser, dynamisk, mængder og summer for de varesporingsnumre, du angiver på siden. Mængderne skal svare til mængderne på dokumentlinjen, der er angivet med **0** i felterne **Udefineret**.  

Når du bogfører dokumentlinjen, overføres varesporingsoplysningerne til de tilknyttede vareposter.

### <a name="to-assign-new-serial-or-lot-numbers"></a>Sådan tildeles nye serie- eller lotnumre

Dette alternativ gælder, når lagervarerne ikke indeholder serie-eller lotnumre og i stedet varesporingsnumrene, når varerne sælges og klar til at blive afsendt. I dette scenarie er numrene typisk tildelt fra en foruddefineret nummerserie.

1. Vælg det relevante dokument, f. eks en salgsfaktura eller salgsordre, og vælg **Linje** på oversigtspanelet **Linjer**, derefter **Relaterede oplysninger**, og vælg derefter handlingen **Varesporingslinjer**.  

    Du kan tildele varesporingsnumre på følgende måder:  
    -   Automatisk fra foruddefineret nummerserie: Vælg handlingen **Tildel serienr.** eller **Tildel lotnr.**.  
    -   Automatisk, på basis af de parametre, du definerer for den udgående vare: Vælg handlingen **Opret brugerdef. serienr.**.  
    -   Manuelt ved at angive serie- eller lotnumre uafhængigt af nummerserier.  

2. For denne fremgangsmåde skal du tildele et serienummer automatisk ved at vælge **Tildel serienr.**  

    Feltet **Antal, der skal oprettes** indeholder standardlinjeantallet, men dette kan ændres.  
3. Vælg feltet **Opret nyt lotnr.** for at organisere de nye serienumre i en bestemt lot.  
4. Klik på **OK** for at oprette et lotnummer og nye individuelle serienumre i overensstemmelse med det antal, der skal håndteres på den tilsvarende dokumentlinje.  

Matrixen for mængdefelter i den øverste visning viser, dynamisk, mængder og summer for de varesporingsnumre, du angiver på siden. Mængderne skal svare til mængderne på dokumentlinjen, der er angivet med **0** i felterne **Udefineret**.  

Når dokumentet er bogført, overføres varesporingsposterne til de tilknyttede vareposter.

### <a name="assign-tracking-numbers-on-source-documents"></a>Tildel sporingsnumre på kildedokumenter

I visse situationer vedr. lagervare med serie - eller lotnumre defineres bestemte serie- eller lotnumre på kildedokumentet, f.eks. en salgsordre, som lagermedarbejderen skal respektere under den udgående lageradministration. Dette kan skyldes, at debitor har anmodet om et bestemt lot under ordreprocessen. Når lagerplukdokumentet er oprettet fra et udgående kildedokument, hvor der allerede er defineret serie- eller lotnumre, er alle felterne på siden **Varesporingslinjer** under lagerpluk skrivebeskyttede, undtagen feltet **Håndteringsantal**. I så fald angiver pluklinjerne for lageret varesporingsnumrene på de enkelte Hent- og Placer-linjer. Antallet er allerede opdelt i entydige serie- eller lotnummerkombinationer, fordi salgsordren angiver de varesporingsnumre, der skal leveres.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Sådan håndteres serie- og lotnumre på overflytningsordrer

Procedurerne for håndtering af serie- og lotnumre, der overføres mellem forskellige lokationer, ligner de procedurer, der bruges, når varer sælges eller købes.  

Overførselsordren er imidlertid entydig i den pågældende leverance, og begge modtagelser sker fra samme overførselslinje og bruger derfor den samme forekomst på siden **Varesporingslinjer**. Det betyder, at varesporingslinjer, der sendes fra en lokation, skal modtages uændret på en anden.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **overførselsordrer**, og vælg derefter det relaterede link.  
2. Åbn den overflytningsordre, du vil behandle. I oversigtspanelet **Linjer**, skal du vælge handlingen **Linje**, vælge handlingen **Varesporingslinjer** og derefter vælge handlingen **Leverance**.  
3. Tilknyt eller vælg serienumre/lotnumre på siden **Varesporingslinjer** som for enhver anden udgående varetransaktion.  

    Når du arbejder med serie- og lotnumre for overflytningsvarer, er der normalt allerede tildelt numre til varerne. Derfor består proceduren oftest af at vælge fra de eksisterende serie- eller lotnumre.  

4. Bogfør overflytningsordren (leverance og modtagelse) for at registrere, at varerne er blevet overført med deres specifikke varesporingsposter.  

Under overførslen er siden **Varesporingslinjer** låst for skrivning.  

## <a name="to-record-additional-serial-or-lot-number-information"></a>Sådan registreres yderligere oplysninger om serie- eller lotnumre

Hvis du vil knytte specielle oplysninger til et bestemt varesporingsnummer, f.eks. for kvalitetssikring, kan du gøre dette på serie- eller lotnr.oplysningskortet.

1. Åbn et dokument, der har tildelte serie- eller lotnumre.
2. Åbn siden **Varesporingslinjer** for den vare, du vil angive oplysninger om.
3. Vælg handlingen **Linje**, og klik f. eks. på handlingen **Serienr. Oplysningskort**.  
4. Vælg plustegnet **(+)** øverst på listen for at oprette en ny post. Felterne **Serienr.** og **Lotnr.** er udfyldt på forhånd fra varesporingslinjen.
5. Angiv korte oplysninger i feltet **Beskrivelse**, for eksempel om varens tilstand.  
6. Vælg den **relaterede** handling, vælg handlingen **Serienr.**, og vælg derefter **Bemærkningen** for at oprette en separat bemærkningspost.  
7. Markér afkrydsningsfeltet **Spærret** for at udelade serienummeret eller lotnummeret i alle transaktioner.  

<!--If you create serial numbers in bulk by using the **Create Customized SN** or **Assign Serial No.** actions, you can enable **Create SN Information** and an information card will be created for each tracking line.

Alternatively, you can create an information card when you post journals or documents. On the **Item Tracking Code** page, turn on the **Create SN Info. on posting** or **Create SN Info. on posting** toggles. -->

Du kan ændre oprettede serie- eller lotnumre på et senere tidspunkt.

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Sådan ændres eksisterende serie-/lotnummeroplysninger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2. Vælg en vare, der har en varesporingskode og har serie- eller lotnummeroplysninger.
3. På siden **Varekort** skal du vælge handlingen **Poster** og derefter klikke på **Poster**.
4. Vælg feltet **Lotnr.** eller **Serienr.**. Hvis der findes oplysninger for varesporingsnummeret, åbnes siden **Oversigt over lotnr.oplysninger** eller **Oversigt over serienr.oplysninger**.  
5. Vælg et kort, og vælg derefter handlingen **Lotnr.oplysningskort/Serienr.oplysningskort**.  
6. Rediger den korte beskrivelsestekst, kommentarposten eller feltet **Spærret**.  

Du kan ikke redigere serienumre, lotnumre eller mængder. For at gøre det skal du ompostere den pågældende varepost. Hvis du vil have yderligere oplysninger om dette, skal du se [Sådan omposteres lot- eller serienumre](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-reclassify-serial-or-lot-numbers"></a>Sådan omposteres serie- eller lotnumre

Ompostering af varesporing for en vare betyder, at et lot- eller serienummer ændres til et nyt lot- eller serienummer, eller at udløbsdatoen ændres til en ny udløbsdato. Hvis du arbejder med lotter, kan du også samle flere lotter i en enkelt lot. Disse opgaver udføres ved hjælp af vareomposteringskladden.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), ikon, skriv **Vareomposteringskladder**, og vælg derefter det relaterede link.  
2. Udfyld linjen med de relevante oplysninger. Du kan finde flere oplysninger i [Lageroptælling ved hjælp af dokumenter](inventory-how-count-inventory-with-documents.md) eller [Tælle, justere og ompostere inventar ved hjælp af kladder](inventory-how-count-adjust-reclassify.md).
3. Vælg handlingen **Varesporingslinjer**.  
4. Vælg det aktuelle serie- eller lotnummer i feltet **Serienr.** eller **Lotnr.**.  
5. Hvis du vil angive et nyt varesporingsnummer, skal du angive det i feltet **Nyt serienummer** eller **Nyt lotnr.**. Du kan flette en eller flere lotter til en ny eller en eksisterende lot.  

    > [!NOTE]  
    >  Når du omposterer udløbsdatoer, skal du være opmærksom på, at varene med den tidligste udløbsdato for udgående transaktioner foreslås først. Du kan finde flere oplysninger i [Plukke efter FEFO](warehouse-picking-by-fefo.md).  

6. Hvis du vil angive en ny udløbsdato for serie- eller lotnummeret, skal du angive det i feltet **Ny udløbsdato**.  

    > [!IMPORTANT]  
    >  Hvis du omposterer en lot til det samme lotnummer, men med en anden udløbsdato, skal du ompostere hele lotten ved hjælp af én vareomposteringskladdelinje. Hvis du omposterer mere end én lot til én ny lot, skal du angive den samme nye udløbsdato for alle lot'ene. Hvis du omposterer én eksisterende lot til en anden eksisterende lot, som har en anden udløbsdato, skal du bruge udløbsdatoen fra den anden lot. Hvis du lader feltet **Ny udløbsdato** være tomt, vil lot- eller serienummeret blive omposteret med en tom udløbsdato.  

7. Hvis du har eksisterende oplysninger om det gamle serie- eller lotnummer, kan du kopiere dem til det nye serie- eller lotnummer.  

    1. På siden **Varesporingslinjer** skal du vælge handlingen **Nye serienr.oplysninger** eller handlingen **Nye lotnr.oplysninger**.  
    2. Hvis du vil kopiere oplysninger fra det gamle lot- eller serienummer, skal du vælge handlingen **Kopier oplysninger**.  
    3. Vælg det lot- eller serienummer, du vil kopiere fra, på siden med oplysninger, og vælg knappen **OK**.  

8. Hvis du vil ændre de eksisterende oplysninger for lot- eller serienummeret, kan du angive lot- eller serieoplysninger.  
9. Bogfør kladden for at linke de ændrede varesporingsnumre eller udløbsdatoerne til den tilknyttede varepost

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/prepare-item-tracking/)

## <a name="see-also"></a>Se også

[Konfigurere varesporing med serie-, lot- og pakkenumre](inventory-how-setup-item-tracking.md)  
[Spore vare via varesporing](inventory-how-to-trace-item-tracked-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Varesporing](design-details-item-tracking.md)  
[Designoplysninger - Varesporing og reservationer](design-details-item-tracking-and-reservations.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
