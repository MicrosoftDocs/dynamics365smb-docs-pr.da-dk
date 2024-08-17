---
title: Plukke til interne operationer i avancerede lageropsætninger
description: 'Hvis lokationerne bruger pluk og levering, kan du plukke komponenter til produktions-, montage- og projektaktiviteter på siden Pluk (logistik).'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 08/12/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="pick-for-production-assembly-or-projects-in-advanced-warehouse-configurations"></a>Plukke til produktion, montage eller projekter i avancerede lagerkonfigurationer

Hvordan du plukker komponenter til produktion, projekter eller montageordrer, afhænger af, hvordan lagerstedet er sat op som en lokation. Flere oplysninger i [Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md).

Brug følgende indstillinger i en avanceret lagerkonfiguration for det udgående flow (pluk) på **siden Lokation kort**  for lokationen:

* Produktion, i produktionsforbruget **.** vælge **Pluk (valgfrit)**  eller **Pluk (obligatorisk)**.
* Forsamling, i **Asm. Forbrug Whse. vælge**  **Pluk (valgfrit)**  eller **Pluk (obligatorisk).**
* Projektledelse i Projektforbrugslager **. vælge**  **Pluk (valgfrit)**  eller **Pluk (obligatorisk).**

Når lokationen kræver lagerpluk, skal du bruge lagerplukdokumenter til at oprette og behandle plukoplysninger, før du bogfører forbrug eller forbrug af komponenter.  

Du kan ikke oprette lagerplukdokumenter fra bunden. Pluk er en del af en arbejdsgang, hvor en person, der behandler en ordre, opretter dem på en Tryk måde, eller lagermedarbejderen opretter den på en pull-måde:

- Du kan bruge handlingen **Opret pluk** på siden **produktionsordren**, **montageordren**, **projektkortet**. Vælg de linjer, der skal plukkes, og forbered plukkene ved at angive, hvilke placeringer der skal tages fra, hvilke placeringer der skal placeres i, og hvor mange enheder der skal håndteres. Placeringerne kan være foruddefineret ved opsætning af lagerstedslokationen eller ressourcen.
- Når du frigiver **produktionsordrer**, **montageordre**, **projektkort** til lagerstedet, er varerne disponible til pluk. På siden **Plukkladde** kan lagerstedsmedarbejderne bruge handlingen **Hent lagerstedsdokumenter** til at få tildelt de tildelte pluk.

Hvis du vil plukke eller flytte komponenter til kildedokumenter på en pull-måde, skal du frigive kildedokumentet for at gøre det klar til pluk. Frigiv kildedokumenter for interne operationer på følgende måder.  

|Kildedokument|Frigivelsesmetode|  
|---------------------|--------------------|  
|Produktionsordre|Ændre ordrens status til frigivet eller oprette en frigivet produktionsordre med det samme.|  
|Montageordre|Skift status til Frigivet.|
|Projekter | Skift status til Åbn eller opret projekt med status Åben med det samme.|  

## <a name="production"></a>Produktion

Brug **Lagerpluk**-dokumenter til at plukke produktionskomponenter i forløbet til produktion.

For en lokation, der bruger placeringer til at flytte varer til åbne produktionsplaceringer, kan du bruge følgende fremgangsmåder:

* For en lokation, hvor der bruges styret læg-på-lager og pluk, skal du følge trinnene i artiklen [Flyt varer i avancerede logistik konfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md).
* For andre lokationer skal du følge trinnene i artiklen [Flyt varer internt i grundlæggende lager konfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

## <a name="assembly"></a>Montage

Bruge **Flytning (lager)**-dokumenter af varer til at flytte montagekomponenter til montageområdet.

[!INCLUDE [prod_short](includes/prod_short.md)] understøtter montage efter lager-og montage efter ordre-montage processer. Hvis du vil vide mere om montage efter ordre i den udgående lagergang, skal du gå til [Håndtering af ordremontagevarer i lagerleverancer](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## <a name="project-management"></a>Projektstyring

Brug **Warehouse Pluk-dokumenter** til at plukke projektkomponenter i flowet til projektstyring.

> [!NOTE]
> Project understøtter ikke avancerede konfigurationer, hvor til/fra-knappen **Styret pluk og læg-på-lager** er slået til.

## <a name="check-whether-items-are-available-for-picking"></a>Kontrollere, om varer er tilgængelige til pluk

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Sådan oprettes plukdokumenter samlet med plukkladden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Plukkladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Hent lagerdokumenter**.  

    Listen viser de frigivne produktions-, projekt- og montageordrer, der er blevet overført til plukfunktionen. Ordrerne omfatter ordrer, som der allerede er oprettet plukinstruktioner til. Dokumenter med læg-på-lager-linjer, der fuldt ud er blevet lagt på plads og er blevet registreret, vises ikke i oversigten.  
3. Vælg de ordrer, som du vil forberede en plukliste til.

    > [!NOTE]  
    > Hvis du vælger et dokument, der allerede indeholder instruktioner for alle linjer, informerer [!INCLUDE [prod_short](includes/prod_short.md)] om, at der ikke er noget at håndtere. Hvis plukinstruktionerne for lagerstedet allerede er oprettet, og du vil kombinere dem til én effektiv plukinstruktion, skal du slette de enkelte pluklister for lagerstedet.

4. Udfyld feltet **Sorteringsmetode** for at sortere linjerne efter behov.  

    > [!NOTE]  
    > Den måde, som linjerne sorteres på i kladden, overføres ikke automatisk til plukinstruktionen. Men de samme sorteringsværktøjer er tilgængelige sammen med placeringsniveau. Du kan derfor nemt genskabe samme linjerækkefølge, når du opretter læg-på-lager-instruktionerne eller ved efterfølgende at sortere dem.

5. Udfyld feltet **Håndteringsantal**. Vælg handlingen **Autofyld håndteringsantal**, eller udfyld felterne manuelt.  

    Siden viser de antal, der kan bruges til direkte afsendelsesplaceringer, som er nyttige i forbindelse med planlægning af arbejdsopgaver i forbindelse med direkte afsendelse. [!INCLUDE[prod_short](includes/prod_short.md)] foreslår altid først pluk fra en direkte afsendelsesplacering.

6. Du kan redigere linjerne efter behov. Du kan også slette nogle af linjerne og derved oprette en mere effektiv plukliste. Hvis der f.eks. er flere linjer med varer i direkte afsendelsesplaceringer, kan du vælge at oprette pluklister til alle linjerne. Varerne i de direkte afsendelsesplaceringer forsendes sammen med de andre varer i kildeforsendelsen, og de direkte afsendelsesplaceringer har plads til flere indkommende varer.

    > [!NOTE]  
    >  Linjerne slettes kun fra kladden, ikke fra læg-på-lager-oversigten.  

7. Vælg handlingen **Opret pluk**. Siden **Opret pluk** åbnes, hvor du kan tilføje yderligere oplysninger til plukket.  

    Angiv, hvordan pluklinjer sorteres i de oprettede plukbilag, ved at vælge en af følgende indstillinger.  

    |Indstilling|Beskrivlse|
    |-|-|
    |Pr. lagerdokument. Bilag|Opretter separate plukdokumenter til kladdelinjer med samme lagerkildedokument.|
    |Pr. deb./kred./lok.|Opretter separate plukdokumenter for hver kunde (projekt)|
    |Pr. vare|Opretter separate plukdokumenter for hver vare i plukkladden.|
    |Pr. fra-zone|Opretter separate plukdokumenter for hver zone, du tager varerne fra.|
    |Pr. placering|Opretter separate plukdokumenter for hver placering, du tager varerne fra.|
    |Pr. forfaldsdato|Opretter separate plukdokumenter for kildedokumenter, der har samme forfaldsdato.|

    Brug følgende indstillinger til at angive, hvordan plukdokumenterne skal oprettes.  

    |Indstilling|Beskrivelse|
    |-|-|
    |Maks. Nej af pluklinjer|Opretter plukdokumenter, der ikke har mere end det angivne antal linjer i hvert dokument.|
    |Maks. antal plukkildedok.|Opretter plukdokumenter, der hver især ikke dækker mere end det angivne antal kildedokumenter.|
    |Tildelt bruger-id|Opretter plukdokumenter, der kun er til kladdelinjer, som er tildelt til den valgte lagermedarbejder.|
    |Sorteringsmåde for pluklinjer|Vælg mellem de tilgængelige indstillinger for at sortere linjer i det oprettede plukbilag.|
    |Angiv nedbrydningsfilter|Skjuler mellemliggende nedbrydningspluklinjer, når en større enhed konverteres til en mindre enhed og plukkes fuldstændigt.|
    |Udfyld ikke håndteringsantal|Lader feltet **Håndteringsantal** stå tomt på de oprettede pluklinjer.|
    |Udskriv pluk|Udskriver plukdokumenterne, når de er oprettet. Du kan også udskrive fra de oprettede plukdokumenter.|

8. Vælg knappen **OK**.  

## <a name="to-pick-items-for-a-production-order-assembly-order-or-project"></a>Sådan plukkes varer til en produktionsordre, en montageordre eller et projekt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk**, og vælg derefter det relaterede link.  

    Hvis du skal arbejde med et bestemt pluk, skal du vælge plukket på listen eller filtrere oversigten for at finde de pluk, der er blevet tildelt til dig. Åbn plukkortet.  
2. Hvis feltet **Tildelt bruger-ID** er tomt, skal du skrive dit id for at identificere dig selv, hvis det er nødvendigt.  
3. Plukke varer.  

    Hvis lageret er indstillet til at bruge placeringer, bruges varernes standardplacering til at foreslå, hvor varerne skal hentes fra. Instruktionerne indeholder mindst to separate linjer, mindst én for hver type handling, Hent og Placer.  

    Operationsområder som f. eks. produktionsanlæg kan have en standardplacering for de komponenter, de kræver. Hvis det er tilfældet, føjes standardplaceringskoden til lagerplukdokumentet for at angive, hvor varerne skal lægges til. Du kan finde flere oplysninger i værktøjstip til felterne **Produktionsplaceringskode**, **Til montageplaceringskode** og **Projektplaceringskode** .

    Hvis lageret er indstillet til at bruge styret læg-på-lager og pluk, bruges placeringsniveauet til at beregne de bedste placeringer, der skal plukkes fra, og disse placeringer foreslås derefter på pluklinjerne. disse placeringer foreslås på pluklinjerne. Instruktionerne indeholder mindst to separate linjer, mindst én for hver type handling, Hent og Placer.  

    * Den første linje med **handlingstypen** **Hent** angiver, hvor varerne er placeret i modtagelsesområdet. Hvis du modtager et stort antal varer på en modtagelseslinje, skal de evt. lægges på lager på flere forskellige placeringer, så der er en Placer-linje for hver placering.
    * Den næste linje med **Placer** i feltet **Handlingstype** viser, hvor du skal placere varerne på lageret. Du kan ikke ændre felterne for zone og placering på denne linje.

    > [!NOTE]
    > Hvis det er nødvendigt at placere varerne for en enkelt linje på mere end én placering, f.eks. fordi den angivne placering er fuld, skal du bruge funktionen **Opdel linje** i oversigtspanelet **Linjer**. Handlingen opretter en linje for det resterende antal til ekspedition.

      Du kan sortere pluklinjerne ud fra forskellige kriterier, f.eks. efter vare, placeringsnummer eller forfaldsdato. Sortering kan hjælpe med at optimere læg-på-lager-processen, f. eks.:

    * Hvis hent- og placer-linjerne til hver leveringslinje ikke står umiddelbart efter hinanden, og du gerne vil have det sådan, kan du sortere linjerne ved at vælge **Vare** i feltet **Sorteringsmetode**.  
    * Hvis placeringsniveauerne afspejler det fysiske lager for lagerstedet, skal du bruge sorteringsmetoden **Placeringsniveau** til at organisere omgåelsen af placeringerne.

  > [!NOTE]  
  > Linjer sorteres i stigende rækkefølge efter valgte kriterier. Hvis du sorterer efter dokument, foretages sorteringen først efter dokumenttype baseret på feltet **Lageraktivitetskildedokument**. Hvis du sorterer efter levering, foretages sorteringen først efter destinationstype baseret på feltet **Lagerdestinationstype**.

4. Når du har plukket og placeret varerne i produktions-, montage- eller projektområdet eller -placeringen, skal du vælge handlingen Registrer **pluk** .  

    Du kan nu overføre varerne til området og bogføre forbruget eller forbruget for de plukkede komponenter ved at bogføre forbrugskladden, montageordren eller projektkladden. Du kan finde flere oplysninger i følgende artikler:

    * [Registrere forbrug og afgang for én frigivet produktionsordrelinje](production-how-to-register-consumption-and-output.md)
    * [Montere varer](assembly-how-to-assemble-items.md)
    * [Registrere forbrug eller anvendelse af projekter](projects-how-record-job-usage.md)

## <a name="flushing-production-components-in-an-advanced-warehouse-configuration"></a>Træk af komponenter til produktion i en avanceret lageropsætning

Trækmetoder påvirker også flowet af komponenter i produktionen. Flere oplysninger i [Udtrække komponenter i henhold til operationsafgang](production-how-to-flush-components-according-to-operation-output.md). Afhængigt af den valgte Trækmetode kan du plukke komponenter til produktions objekterne på følgende måder:

* Brug et **pluk (logistik)**-dokument til at registrere plukningen for varer, der bruger den **manuelle** Trækmetode. Du har brug for at registrere forbruget separat. Flere oplysninger i [Massebogføre produktionsforbrug](production-how-to-post-consumption.md).
* Brug et **Pluk (logistik)**-dokument til at registrere plukningen for varer, der bruger den **Pluk + Forlæns**, **Pluk + Baglæns**-trækmetoden. Forbruget af komponenterne sker automatisk, når du ændrer status for produktionsordren eller ved at starte eller afslutte en operation. Alle nødvendige komponenter skal være tilgængelige. Ellers stopper den udtrukne forbrugsbogføring for den pågældende komponent.
* Bruge et **lagerbevægelse**-dokument uden en reference til et kildedokument eller andre måder at registrere flytning af komponenter på, der bruger trækmetoden **forlæns** eller **baglæns**. Komponenterne forbruges automatisk, når du ændrer status for produktionsordren eller ved at starte eller afslutte en operation. Alle nødvendige komponenter skal være tilgængelige. Ellers stopper den udtrukne forbrugsbogføring for den pågældende komponent. Flere oplysninger i [Montage af varer](warehouse-move-items.md).

### <a name="example"></a>Eksempel

Der findes en produktionsordre for 15 stk. af vare SP-SCM1004. Nogle af varerne på komponentlisten skal trækkes manuelt i en forbrugskladde. Andre varer kan plukkes og trækkes automatisk ved hjælp af metoden **pluk + baglæns**-træk.  

De følgende trin beskriver de handlinger, der er involveret for forskellige brugere, og de relaterede svar:  

1. Den tilsynsførende frigiver produktionsordren. Elementer med **Fremad** som trækmetode og ingen rutebindingskode bliver fratrukket åben produktionsplacering.  
2. Den tilsynsførende vælger knappen **Opret pluk (logistik)** på produktionsordren. Der oprettes et lagerplukdokument for varer med trækmetoderne **Manuel**, **Pluk + Baglæns** og **Pluk + Forlæns**. Disse varer placeres på produktionsplaceringen.  
3. Lagerchefen tildeler pluk til en lagermedarbejder.  
4. Lagermedarbejderen plukker varerne fra relevante placeringer og placerer dem på produktionsplaceringen eller på placeringen, der er angivet på lagerplukket, hvilket kan være et arbejdscenter- eller en produktionsressourceplacering. Placeringen kan muligvis være et arbejdscenter eller en produktionsressource.
5. Lagermedarbejderen registrerer plukket. Antallet overføres fra plukplaceringerne og føjes til forbrugsplaceringen. Feltet **Plukket antal** på komponentlisten for alle de plukkede varer opdateres.

    > [!NOTE]  
    >  Kun det antal, der er plukket, kan forbruges.  
6. Maskinoperatøren oplyser produktionschefen om, at færdigvarerne er klar.
7. Den tilsynsførende bruger forbrugskladden eller produktionskladden til at bogføre forbruget af komponentvarer, som enten bruger en **Manuel** trækmetode.
8. I Shop Floor supervisor bruges afgangskladden eller produktionskladden til at bogføre afgangen. Den mængde komponentvarer, der bruger **Pluk + Fremad**- eller **Pluk + Baglæns**-trækmetode med rutebindinger, trækkes fra til produktions placeringen.
9. Produktionschefen bogfører afgang for produktionsordren og ændrer status til **Udført**. Antallet af komponentvarer, der bruger **baglæns**-trækmetoden, trækkes fra den åbne produktionsplacering, og antallet af komponentvarer, der bruger **pluk + baglæns**-trækmetoden trækkes fra produktionsplaceringen.  

Følgende illustration viser, når feltet **Placeringskode** på komponentlisten udfyldes i overensstemmelse med konfiguration af din lokation eller maskine/arbejdscenter.  

:::image type="content" source="media/binflow.png" alt-text="Oversigt over, hvornår/hvordan feltet Placeringskode skal udfyldes.":::

## <a name="make-to-order-mto-production-components-in-an-advanced-warehouse-configuration"></a>Fremstil til ordre (MTO)-komponenter til produktion i en avanceret lageropsætning

I scenarier, hvor en produceret vare består af råmaterialer og halvfabrikata, hvor produktionsmetoden er angivet til **Fremstil-til-ordre**, føjes lagerplukket for disse halvfabrikata til den samme produktionsordre, og feltet **Planlægningsniveaukode** er udfyldt. Det forventes, at halvfabrikata er klar til forbrug med det samme og ikke kræver pluk, så de medtages ikke i lagerplukdokumentet. De oprettede lagerpluk omfatter kun råvarer til producerede varer og halvfabrikata.

Men hvis der er halvfabrikata på lager op, foreslår planlægningssystemet, at du forbruger dem i stedet for at producere hele antallet. En produceret vare kræver f.eks. fem halvfabrikata, men tre er allerede på lager. I dette tilfælde vises fem halvfabrikata i produktionsordrekomponenterne, men kun to produceres i samme produktionsordre som en separat produktionsordrelinje.
En sådan opsætning er ikke kompatibel med lagerpluk, og afhængigt af hyppigheden skal du enten ændre produktionsmetoden for halvfabrikata til **Fremstil-til-lager** eller manuelt opdele produktionsordrekomponentlinjen, når du skal plukke de halvfabrikata, der er produceret tidligere.


## <a name="see-also"></a>Se også

- [Administrere lager](inventory-manage-inventory.md)  
- [Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
- [Montagestyring](assembly-assemble-items.md)  
- [Oversigt over Warehouse Management](design-details-warehouse-management.md)
- [Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
