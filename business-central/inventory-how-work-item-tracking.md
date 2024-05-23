---
title: 'Spore varer med serie-, lot- og pakkenumre'
description: 'Du kan tilføje serie-, lot- og pakkenumre til ethvert udgående eller indgående bilag, og dets posterede varesporing vises i de relaterede vareposter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 03/13/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Spore varer med serie-, lot- og pakkenumre

Du kan tildele serie-, lot- og pakkenumre til ethvert udgående eller indgående bilag, og dets posterede varesporing vises i de relaterede vareposter. Du kan spore varer på siden **Varesporingslinjer**, som du kan åbne fra et indgående eller udgående dokumenter.

Mængdefelterne øverst på siden **Varesporingslinjer** viser mængder og summer for de varesporingsnumre, der defineres på linjerne. Mængderne skal svare til mængderne på dokumentlinjerne, der er angivet med 0 i felterne **Udefineret**.

[!INCLUDE [prod_short](includes/prod_short.md)] opdaterer disponeringsoplysningerne på siden **Varesporingslinjer**, når du åbner siden. Det opdaterer ikke oplysningerne, mens du har siden åben, selvom der sker ændringer i lageret eller i andre dokumenter.

> [!NOTE]  
> Hvis du vil arbejde med de funktioner, der er beskrevet i denne artikel, skal du først oprette varesporing. Du kan lære mere i [Konfigurere varesporing med serie-, lot og pakkenumre](inventory-how-setup-item-tracking.md).

## Tilgængelighed af varesporing

Når du arbejder med serie-, lot- og pakkenumre, beregner [!INCLUDE[prod_short](includes/prod_short.md)] tilgængelighedsoplysningerne og viser dem på de forskellige sider for varesporing. Det viser, hvor meget af et lot-, pakke- eller serienummer der er anvendt i andre dokumenter. Disse oplysninger hjælper med at reducere fejl og usikkerhed, der skyldes dobbelte tildelinger.

På siden **Varesporingslinjer** vises der muligvis et advarselsikon i feltet **Disponering, lotnr.** eller **Disponering, serienr.** af følgende årsager:

* Hvis nogle eller alle af det valgte antal allerede bruges i andre dokumenter.
* Hvis lot- eller serienummeret ikke er tilgængeligt.

**Lotnr./serienummer-liste**, **Lotnr./serienummer-tilgængelighed** og siderne **Varesporing - vælg poster** viser oplysninger om, hvor mange af en vare der er i brug. I følgende tabel vises de relevante felter.

|Felt|Beskrivelse|
|-----|-----------|  
|**Antal i alt**|Det samlede antal varer på lager.|
|**Ønsket antal i alt**|Det samlede antal varer, der ønskes til brug i dette og andre dokumenter.|
|**Aktuelt ventende antal**|Det antal varer, der anmodes om i det aktuelle dokument, men som ikke blev bogført.|
|**Aktuelt bestilt antal**|Det antal varer, der vil blive brugt i det aktuelle dokument|
|**Beholdning i alt**|Det samlede antal varer på lager minus det antal af varen, der ønskes brugt i dette og andre dokumenter (ønsket antal i alt) minus det antal, der ønskes, men som endnu ikke er bogført i dette dokument (aktuelt ventende antal).|

Hvis du arbejder på siden **Varesporingslinjer** i lang tid, eller hvis der er stor aktivitet omkring den vare, du arbejder med, kan du vælge handlingen **Opdater disponering**. Varedisponeringen kontrolleres også automatisk, når du lukker siden, så det kontrolleres, at der ikke er nogen disponeringsproblemer.

## Sådan tildeles serie- eller lotnumre under indgående transaktioner

Det kan være en god idé at spore varer fra det øjeblik, de ankommer. I det tilfælde er købsordren ofte det centrale dokument. Du kan dog gennemføre varesporing fra ethvert indgående dokument, og de posterede varer vises i de tilknyttede vareposter.

Sporingsnumrene overføres automatisk til alle udgående lageraktiviteter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.  
2. Åbn en eksisterende købsordre eller opret en ny.
3. Markér dokumentlinjen, og vælg handlingen **Linje** i oversigtspanelet **Linjer**, og vælg derefter handlingen **Varesporingslinjer** for at åbne siden **Rediger - varesporingslinjer**.  

   Du kan tildele serie- eller lotnumre på følgende måder:  
   * Automatisk ved at vælge **Behandle** og derefter **Tildel serienr.** eller **Tildel lotnr.** for at tildele serienumre/lotnumre fra foruddefinerede nummerserier.  
   * Automatisk ved at vælge **Behandle** og derefter **Oprette brugerdefineret serienr.** for at tildele serienumre/lotnumre baseret på de parametre, du definerer for de ankomne varer.  
   * Manuelt ved at angive serie- eller lotnumre direkte, f.eks. kreditornumrene.  
   * Manuelt ved at tildele et specifikt nummer til hver vareenhed.  

4. Hvis du vil tildele automatisk, skal du vælge handlingen **Opret brugerdef. serienr.**.  
5. Angiv startnummeret i en beskrivende serienummerserie i feltet **Brugerdef. serienr.**. For eksempel **S/N-Kred0001**.  
6. Indtast 1 i feltet **Forøgelse** for at angive, at hvert fortløbende nummer stiger med 1.  

    Feltet **Antal, der skal oprettes** indeholder standardlinjeantallet, men dette kan ændres.  

7. Marker afkrydsningsfeltet **Opret nyt lotnr.** for at organisere de nye serienumre i en bestemt lot.  
8. Vælg knappen **OK**.  

[!INCLUDE [prod_short](includes/prod_short.md)] opretter et lotnummer med individuelle serienumre i overensstemmelse med vareantallet på dokumentlinjen. Nummeret indledes med den værdi, du har angivet i feltet **Brugerdef. serienr**. For eksempel med start fra **S/N-Kred0001**.  

Mængdefelterne i overskriften viser dynamisk mængder og summer for de varesporingsnumre, du angiver på siden. Mængderne skal svare til mængderne på dokumentlinjerne, der er angivet med **0** i feltet **Udefineret**.  

Når du bogfører dokumentlinjen, overføres varesporingsposterne til vareposterne.

### Sådan håndteres serie- og lotnumre, når der hentes modtagelseslinjer fra en købsfaktura

Når du bogfører modtagelses- eller afsendelseslinjer fra relaterede fakturaer eller kreditnotaer, så overføres alle varesporingslinjer på lagerdokumenter automatisk. De behandles dog på en særlig måde.

Funktionen understøtter følgende indgående processer:  

* **Hent købsleverancelinjer** – fra en købsfaktura.  
* **Hent returvarelev.linjer** – fra en købskreditnota.  

Funktionen understøtter følgende udgående processer:  

* **Hent salgsleverancelinjer** – fra en salgsfaktura eller kombinerede leverancer.  
* **Hent returvaremodt.linjer** – fra en salgskreditnota.  

I disse tilfælde overføres varesporingslinjer til fakturaen eller kreditnotaen, men siden **Varesporingslinjer** tillader ikke, at serie- eller lotnumre ændres. Du kan kun ændre mængderne.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. Åbn en købsfaktura for varer, der er køb med serienumre eller lotnumre.  
3. Fra en købsfakturalinje skal du i oversigtspanelet **Linjer** vælge handlingen **Hent købsleverancelinjer**.  
4. Vælg en modtagelseslinje, der har varesporingslinjer på siden **Hent købsleverancelinjer**, og vælg derefter knappen **OK**.  

    Kildedokumentet kopieres til købsfakturaen som en ny linje, og dets varesporingslinjer overføres uændret til den underliggende side **Varesporingslinjer**.  

5. Vælg den overførte modtagelseslinje i købsfakturaen.  
6. I oversigtspanelet **Linjer** skal du vælge handlingen **Linje** og derefter vælge handlingen **Varesporingslinjer** for at få vist de overførte varesporingslinjer.  

Du kan ikke ændre felterne **Serienr.** og **Lotnr.**. Du kan imidlertid slette hele linjer eller ændre mængder, så de svarer til ændringerne på kildelinjen.  

## Sådan tildeles serie- eller lotnumre under en udgående transaktion

Udgående håndtering af serie eller lotnumre er en almindeligt forekommende opgave i mange forskellige lagerprocesser. Serie- og lotnumre kan føjes til udgående transaktioner på to måder:  

- Vælg fra eksisterende serienumre eller lotnumre. Bruges, når der allerede er blevet tildelt varesporingsnumre i forbindelse med en indgående transaktion.
- Tildel nye serie- eller lotnumre under udgående transaktioner. Dette gælder, når varesporingsnumre ikke skal tildeles til varer, før de er solgt og klar til at blive afsendt.

### Sådan vælges der fra eksisterende serienumre eller lotnumre  

Når du arbejder med varer, der kræver varesporing, og du opretter udgående transaktioner, skal du som regel vælge lot- eller serienumrene ud fra dem, der allerede findes på lageret.

1. Marker den linje, du vil vælge et lot- eller serienummer til, i et hvilket som helst udgående dokument.  
2. I oversigtspanelet **Linjer** skal du vælge handlingen **Linje**, derefter **Relaterede oplysninger** og derefter **Varesporingslinjer**.  
3. På siden **Varesporingslinjer** har du tre muligheder for at vælge lot- eller serienumre:  

   * Klik på feltet **Serienr.**, og vælg derefter et nummer på siden **Serienummerliste**.
   * Klik på feltet **Lotnr.**, og vælg derefter et nummer på siden **Lotnummerliste**. Vælg feltet **Serienr.**, og vælg derefter et nummer på siden **Serienummerliste**.
   * Vælg handlingen **Behandle** og derefter **Angiv poster**. Siden **Marker poster** viser alle lot- og serienumre sammen med disponeringsoplysninger.

4. I feltet **Valgt antal** skal du angive antallet for hvert af de lot- eller serienumre, der skal bruges.
5. Vælg knappen **OK**. Varesporingsoplysningerne overføres til siden **Varesporingslinjer**.  

Mængdefelterne i overskriften viser dynamisk mængder og summer for de varesporingsnumre, du angiver på siden. Mængderne skal svare til mængderne på dokumentlinjen, der er angivet med **0** i **Udefineret**-feltet.  

Når du bogfører dokumentlinjen, overføres varesporingsoplysningerne til de tilknyttede vareposter.

### Sådan tildeles nye serie- eller lotnumre  

Denne proces gælder, når varer ikke har serie- eller lotnumre, mens de er på lager. I stedet kan du tildele varesporingsnumre, når varerne er solgt og klar til at blive afsendt. I dette tilfælde tildeles numre typisk fra en foruddefineret nummerserie.

1. Vælg det relevante dokument, f. eks en salgsfaktura eller salgsordre, og vælg **Linje** på oversigtspanelet **Linjer**, derefter **Relaterede oplysninger**, og vælg derefter handlingen **Varesporingslinjer**.  

    Du kan tildele varesporingsnumre på følgende måder:  
    * Automatisk fra en foruddefineret nummerserie: Vælg handlingen **Tildel serienr.** eller **Tildel lotnr.**.  
    * Automatisk, på basis af de parametre, du definerer for den udgående vare: Vælg handlingen **Opret brugerdef. serienr.**.  
    * Manuelt ved at angive serie- eller lotnumre uafhængigt af nummerserier.  

2. For denne fremgangsmåde skal du tildele et serienummer automatisk ved at vælge **Tildel serienr.**  

    Feltet **Antal, der skal oprettes** indeholder standardlinjeantallet, men du kan ændre det.  
3. Vælg feltet **Opret nyt lotnr.** for at organisere de nye serienumre i en bestemt lot.  
4. Klik på **OK** for at oprette et lotnummer og nye individuelle serienumre i overensstemmelse med det antal, der skal håndteres på den tilsvarende dokumentlinje.  

Mængdefelterne vises i øverste visning dynamisk de mængder og summer for de varesporingsnumre, du angiver på siden. Mængderne skal svare til mængderne på dokumentlinjen, der er angivet med **0** i **Udefineret**-feltet.  

Når du bogfører dokumentlinjen, overføres varesporingsposterne til vareposterne.

### Tildel sporingsnumre på kildedokumenter

Nogle virksomheder definerer specifikke serie- eller lotnumre på kildedokumentet, f.eks. salgsordrer. Det kan f.eks. være, hvis en kunde anmoder om et bestemt lot. Når du opretter lagerplukket eller lagerplukdokumentet fra et udgående kildedokument, hvor der allerede er defineret serie- eller lotnumre, kan du ikke ændre felterne på siden **Varesporingslinjer** under lagerplukket. Den eneste undtagelse er feltet **Håndteringsantal**. I så fald angiver pluklinjerne for lageret varesporingsnumrene på de enkelte Hent- og Placer-linjer. Antallet er allerede opdelt i entydige serie- eller lotnummerkombinationer, fordi salgsordren angiver de varesporingsnumre, der skal leveres.

## Sådan håndteres serie- og lotnumre på overflytningsordrer

Procedurerne for håndtering af serie- og lotnumre, der overføres mellem forskellige lokationer, ligner de procedurer, der bruges, når varer sælges eller købes.  

Overførselsordrer er imidlertid entydige i den pågældende leverance, og begge modtagelser sker fra samme overførselslinje og bruger den samme forekomst på siden **Varesporingslinjer**. Varesporingslinjer, der sendes fra en lokation, skal modtages uændret på en anden lokation.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **overførselsordrer**, og vælg derefter det relaterede link.  
2. Åbn den overflytningsordre, du vil behandle. I oversigtspanelet **Linjer**, skal du vælge handlingen **Linje**, vælge handlingen **Varesporingslinjer** og derefter vælge handlingen **Leverance**.  
3. Tilknyt eller vælg serienumre/lotnumre på siden **Varesporingslinjer** som for enhver anden udgående varetransaktion.  

    Når du håndterer serie- og lotnumre for overflytningsvarer, er der normalt allerede tildelt numre til varerne. Derfor kan du ofte vælge mellem eksisterende serie- eller lotnumre.  

4. Bogfør overflytningsordren (leverance og modtagelse) for at registrere, at varerne er blevet overført med deres specifikke varesporingsposter.  

Under overførslen kan ud ikke ændre værdier på siden **Varesporingslinjer**.  

## Sådan registreres yderligere oplysninger om serie- eller lotnumre

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

## Sådan ændres eksisterende serie-/lotnummeroplysninger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2. Vælg en vare, der har en varesporingskode og har serie- eller lotnummeroplysninger.
3. På siden **Varekort** skal du vælge handlingen **Poster** og derefter klikke på **Poster**.
4. Vælg feltet **Lotnr.** eller **Serienr.**. Hvis der findes oplysninger for varesporingsnummeret, åbnes siden **Oversigt over lotnr.oplysninger** eller **Oversigt over serienr.oplysninger**.  
5. Vælg et kort, og vælg derefter handlingen **Lotnr.oplysningskort/Serienr.oplysningskort**.  
6. Rediger den korte beskrivelsestekst, kommentarposten eller feltet **Spærret**.  

Du kan ikke ændre serienumre, lotnumre eller mængder. For at gøre det skal du ompostere den pågældende varepost. Hvis du vil vide mere om genklassificering, skal du gå til [Genklassificere lot- eller serienumre](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## Sådan omposteres serie- eller lotnumre

Ompostering af varesporing for en vare betyder, at et lot- eller serienummer ændres til et nyt lot- eller serienummer, eller at udløbsdatoen ændres til en ny udløbsdato. Hvis du bruger lots, kan du også samle flere lots i en enkelt lot. Brug en genklassificeringskladde af varer for at gennemføre disse opgaver.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] Kontrollerer, at hver linje har en unik kombination af serie-, lot- og/eller pakkenumre. Hvis du vil opdele et lot, en pakke eller et lot og pakke i flere lotter eller pakker, skal du bruge flere kladdelinjer.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vareomposteringskladder**, og vælg derefter det relaterede link.  
2. Udfyld linjen med de relevante oplysninger. Du kan finde flere oplysninger i [Lageroptælling ved hjælp af dokumenter](inventory-how-count-inventory-with-documents.md) eller [Tælle, justere og ompostere inventar ved hjælp af kladder](inventory-how-count-adjust-reclassify.md).
3. Vælg handlingen **Varesporingslinjer**.  
4. Vælg det aktuelle serie- eller lotnummer i feltet **Serienr.** eller **Lotnr.**.  
5. Hvis du vil angive et nyt varesporingsnummer, skal du angive det i feltet **Nyt serienummer** eller **Nyt lotnr.**. Du kan flette en eller flere lotter til en ny eller en eksisterende lot.  

    > [!NOTE]  
    > Hvis du omposterer udløbsdatoer, skal varer med den tidligste udløbsdato for udgående transaktioner foreslås først. Du kan få mere at vide ved at gå til [Plukke efter FEFO](warehouse-picking-by-fefo.md).  

6. Hvis du vil angive en ny udløbsdato for serie- eller lotnummeret, skal du angive det i feltet **Ny udløbsdato**.  

    > [!IMPORTANT]  
    > * Hvis du omposterer et lot til det samme lotnummer, men med en anden udløbsdato, skal du ompostere hele lottet ved hjælp af én vareomposteringskladdelinje.
    > * Hvis du omposterer mere end én lot til én ny lot, skal du angive den samme nye udløbsdato for alle lot'ene. 
    > * Hvis du omposterer én eksisterende lot til en anden eksisterende lot, som har en anden udløbsdato, skal du bruge udløbsdatoen fra den anden lot. 
    > * Hvis du lader feltet **Ny udløbsdato** være tomt, vil lot- eller serienummeret blive omposteret med en tom udløbsdato.  

7. Hvis du har eksisterende oplysninger om det gamle serie- eller lotnummer, kan du kopiere dem til det nye serie- eller lotnummer.  

    1. På siden **Varesporingslinjer** skal du vælge handlingen **Nye serienr.oplysninger** eller handlingen **Nye lotnr.oplysninger**.  
    2. Hvis du vil kopiere oplysninger fra det gamle lot- eller serienummer, skal du vælge handlingen **Kopier oplysninger**.  
    3. Vælg det lot- eller serienummer, du vil kopiere fra, på siden med oplysninger, og vælg knappen **OK**.  

8. Hvis du vil ændre de eksisterende oplysninger for lot- eller serienummeret, kan du angive lot- eller serieoplysninger.  
9. Bogfør kladden for at linke de ændrede varesporingsnumre eller udløbsdatoerne til den tilknyttede varepost

## Scan stregkoder med Business Central-mobilapp

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Hvis du vil scanne adskillige serie-, lot- eller pakkestregkoder på siden **Varesporingslinjer**, kan du bruge handlingen **Scan flere**. Når du har scannet en stregkode, angives dens værdi i feltet på siden, og det næste felt til hurtig indtastning bliver tilgængeligt. Du kan også bruge stregkodescannerikonet til at udfylde et bestemt felt.

Følgende tabeller viser de sider, der understøtter stregkodescanning for varesporing fra mobilappen [!INCLUDE [prod_short](includes/prod_short.md)].

|Side  |Feltværdier, du kan scanne  |
|---------|---------|
|Varesporingslinjer     |* Serienr.<br><br>* Nyt serienr.<br><br>* Partinr.<br><br>* Nyt lotnr.<br><br>* Pakkesporingsnr.<br><br>* Nyt pakkenr.|
|Regul.plac. Varesporingslinjer     |* Serienr.<br><br>* Nyt serienr.<br><br>* Partinr.<br><br>* Nyt lotnr.<br><br>* Pakkesporingsnr.<br><br>* Nyt pakkenr.|
|Varesporing     |* Serienr.filter<br><br>* Partinr.filter<br><br>* Pakkesporingsnr. Filtrer |
|Varekladde     |* Serienr.<br><br>* Partinr.<br><br>* Pakkesporingsnr.     |
|Lageraktivitetslinje     |* Serienr.<br><br>* Partinr.<br><br>* Pakkesporingsnr.<br><br>**Bemærk**: Følgende sider bruger siden Lageraktivitetslinje:<br><br>* side 5780 "Lagersted Vælg underformular"<br><br>* side 7378 "Lager Vælg underformular"<br><br>* side 5771 "Lagersted Læg-på-lager-underformular"<br><br>* side 7316 "Underformular til lagerbevægelse"<br><br>* side 7376 "Lager Læg på lager-underformular"<br><br>* side 7383 "Lagerflytning-underformular"        |
|Regul.plac. Lagerplaceringskladde     |* Serienr.<br><br>* Partinr.<br><br>* Pakkesporingsnr.         |

## Se også

[Konfigurere varesporing med serie-, lot- og pakkenumre](inventory-how-setup-item-tracking.md)  
[Spore vare via varesporing](inventory-how-to-trace-item-tracked-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Varesporing](design-details-item-tracking.md)  
[Designoplysninger - Varesporing og reservationer](design-details-item-tracking-and-reservations.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
