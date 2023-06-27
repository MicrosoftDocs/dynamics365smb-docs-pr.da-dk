---
title: Plukke varer til lagerleverance
description: 'Få mere at vide om, hvordan du bruger lagerplukdokumenterne til at oprette og behandle plukoplysninger, inden lagerleverancen bogføres.'
author: bholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '7335, 7339, 7345,'
---
# <a name="pick-items-for-warehouse-shipment" />Plukke varer til lagerleverance

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du modtage varer og indsætte dem på en af fire måder som beskrevet i følgende tabel.

|Metode|Udgående proces|Kræv pluk|Kræv leverance|Sværhedsgrad (få mere at vide på [Warehouse Management-oversigt](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bogfør pluk og leverance fra ordrelinjen|||Ingen dedikeret lageraktivitet.|  
|B|Bogfør pluk og leverance fra et lagerplukdokument|Aktiveret||Basis: Ordre for ordre.|  
|U|Bogfør pluk og leverance fra et lagerstedsleverancedokument||Aktiveret|Basis: Konsolideret modtagelse/levering for flere ordrer.|  
|D|Bogfør pluk fra et lagerstedsplukdokument, og bogfør leverance fra et lagerstedsleverancedokument|Aktiveret|Aktiveret|Avanceret|  

Få mere at vide på [Udgående lagerstedsflow](design-details-outbound-warehouse-flow.md).

Denne artikel henviser til metode D i den foregående tabel. Hvis du vil vide mere om montageelementer, skal du gå til [montagevarer](warehouse-how-ship-items.md).

Når lokationen kræver lagerpluk og lagerleverance, skal du bruge lagerplukdokumenterne til at oprette og behandle plukoplysningerne, inden du bogfører den pågældende lagerleverance.  

Du kan ikke oprette lagerplukdokumenter fra bunden. Pluk er en del af en arbejdsgang, hvor en person, der behandler en ordre, opretter dem på en Tryk måde, eller lagermedarbejderen opretter den på en pull-måde:

- Når du skal bruge handlingen **Opret pluk** på **lagerleverance** siden, når du trykker. Vælg de linjer, der skal plukkes, og forbered plukkene ved at angive, hvilke placeringer der skal tages fra, hvilke placeringer der skal placeres i, og hvor mange enheder der skal håndteres. Placeringerne kan være foruddefineret ved opsætning af lagerstedslokationen eller ressourcen.
- På en pull-måde, hvor du kan bruge handlingen **Frigiv** på **lagerleverance**-siden for at gøre varerne disponible til pluk. På siden **Plukkladde** kan lagerstedsmedarbejderne bruge handlingen **Hent lagerstedsdokumenter** til at få tildelt de tildelte pluk.

> [!NOTE]  
> Pluk til lagerleverance af varer, der monteres til salgsordren, der leveres, følger de samme trin som for normale lagerpluk til leverance, som det er beskrevet i denne artikel. Antallet af pluklinjer pr. antal til levering kan være mange til en, da du plukker komponenterne og ikke montageelementet.  
>
> Lagerpluklinjerne oprettes for værdien i feltet **Restantal** på linjerne for den montageordre, der er knyttes til salgsordren, der leveres. Alle komponenter plukkes i én handling. Flere oplysninger i [Håndtering af montageordrevarer i lagerleverancer](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).  
>  
> Se [Plukke til montage eller produktion i avancerede lageropsætninger](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md) for at få oplysninger om pluk af komponenter til montageordrer generelt, herunder situationer, hvor montageelementet ikke er forfaldent på en salgsleverance.  

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet" />Sådan oprettes plukdokumenter samlet med plukkladden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Plukkladde**, og vælg derefter det relaterede link.  

2. Vælg handlingen **Hent lagerdokumenter**.  

    Oversigten indeholder alle leverancer, der er frigivet til plukning, inklusive dem, som der allerede er oprettet plukinstruktioner for. Dokumenter med læg-på-lager-linjer, der fuldt ud er blevet lagt på plads og er blevet registreret, vises ikke i oversigten.  
3. Vælg de leverancer, som du vil forberede en plukliste til.

    > [!NOTE]  
    >  Hvis du prøver at vælge et modtagelses- eller intern læg-på-lager-dokument, som der allerede er oprettet instruktioner for til samtlige linjer, får du besked på, at der ingenting er at håndtere. Hvis plukinstruktionerne for lagerstedet allerede er oprettet, og du vil kombinere dem til én effektiv plukinstruktion, skal du slette de enkelte pluklister for lagerstedet.

4. Udfyld feltet **Sorteringsmetode** for at sortere linjerne efter behov.  

    > [!NOTE]  
    >  Den måde, som linjerne sorteres på i kladden, overføres ikke automatisk til plukinstruktionen. De samme muligheder for sortering og placeringsrangering findes dog. Du kan derfor nemt genskabe samme linjerækkefølge, når du opretter læg-på-lager-instruktionerne eller ved efterfølgende at sortere dem.

5. Udfyld feltet **Håndteringsantal** enten manuelt eller ved hjælp af handlingen **AutoFyld Qty.to** .  

    Siden viser de antal, der kan bruges til direkte afsendelsesplaceringer, som er nyttige i forbindelse med planlægning af arbejdsopgaver i forbindelse med direkte afsendelse. [!INCLUDE[prod_short](includes/prod_short.md)] foreslår altid først pluk fra en direkte afsendelsesplacering.
6. Du kan redigere linjerne efter behov. Du kan også linjerne og derved oprette en mere effektiv plukliste. Hvis der f.eks. er flere linjer med varer i direkte afsendelsesplaceringer, kan du vælge at oprette pluklister til alle linjerne. Varerne i de direkte afsendelsesplaceringer forsendes sammen med de andre varer i forsendelsen, og de direkte afsendelsesplaceringer har plads til flere indkommende varer.  

    > [!NOTE]  
    >  Hvis du sletter linjer, bliver de kun slettet fra kladden. De slettes ikke fra pluklisten.  

7. Vælg handlingen **Opret pluk**. Siden **Opret pluk** åbnes, hvor du kan tilføje yderligere oplysninger til plukket. Angiv, hvordan pluklinjer sorteres i de oprettede plukbilag, ved at vælge en af følgende indstillinger.  

    |Indstilling|Beskrivlse|
    |-|-|
    |Pr. lagerdokument. Bilag|Opretter separate plukdokumenter til kladdelinjer med samme lagerkildedokument.|
    |Pr. deb./kred./lok.|Opret separate plukdokumenter til hver debitor (salgsordrer), leverandør (købsreturvareordrer) og lokation (overflytningsordrer).|
    |Pr. vare|Opret separate plukdokumenter for hver vare i plukkladden.|
    |Pr. fra-zone|Opret separate plukdokumenter for hver zone, du tager varerne fra.|
    |Pr. placering|Opret separate plukdokumenter for hver placering, du tager varerne fra.|
    |Pr. forfaldsdato|Opret separate plukdokumenter for kildedokumenter, der har samme forfaldsdato.|

    Angiv, hvordan plukbilagene oprettes, ved at vælge mellem følgende indstillinger.

    |Indstilling|Beskrivlse|
    |-|-|
    |Maks. Nej af pluklinjer|Opretter plukdokumenter, der ikke har mere end det angivne antal linjer i hvert dokument.|
    |Maks. Nej plukkildedok.|Opretter plukdokumenter, der hver især ikke dækker mere end det angivne antal kildedokumenter.|
    |Tildelt bruger-id|Opretter plukdokumenter, der kun er til kladdelinjer, som er tildelt til den valgte lagermedarbejder.|
    |Sorteringsmåde for pluklinjer|Vælg mellem de tilgængelige indstillinger for at sortere linjer i det oprettede plukbilag.|
    |Angiv nedbrydningsfilter|Skjuler mellemliggende nedbrydningspluklinjer, når en større enhed konverteres til en mindre enhed og plukkes fuldstændigt.|
    |Udfyld ikke håndteringsantal|Lader feltet Håndteringsantal stå tomt på de oprettede pluklinjer.|
    |Udskriv pluk|Udskriver plukdokumenterne, når de er oprettet. Du kan også udskrive fra de oprettede plukdokumenter.|

8. Vælg **OK**. [!INCLUDE [prod_short](includes/prod_short.md)] opretter plukket i overensstemmelse med dine valg.  

## <a name="to-pick-items-for-a-warehouse-shipment" />Sådan plukkes varer til lagerleverance

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk (logistik)**, og vælg derefter det relaterede link.  

    Hvis du skal arbejde med et bestemt pluk, skal du vælge plukket på listen eller filtrere oversigten for at finde de pluk, der er blevet tildelt specielt til dig. Åbn plukkortet.  
2. Hvis feltet **Tildelt bruger-ID** er tomt, skal du skrive dit id for at identificere dig selv, hvis det er nødvendigt.  
3. Plukke varer.  

    Hvis lageret er indstillet til at bruge placeringer, bruges varernes standardplacering til at foreslå, hvor varerne skal hentes fra. Instruktionerne indeholder mindst to separate linjer, mindst én for hver type handling, Hent og Placer.  

    Hvis lageret er indstillet til at bruge styret læg-på-lager og pluk, bruges placeringsniveauet til at beregne de bedste placeringer, der skal plukkes fra, og disse placeringer foreslås derefter på pluklinjerne. disse placeringer foreslås på pluklinjerne. Instruktionerne indeholder mindst to separate linjer, mindst én for hver type handling, Hent og Placer.  

    * Den første linje med **handlingstypen** **Hent** angiver, hvor varerne er placeret i modtagelsesområdet. Hvis du modtager et stort antal varer på en modtagelseslinje, skal de evt. lægges på lager på flere forskellige placeringer, så der er en Placer-linje for hver placering.
    * Den næste linje med **Placer** i feltet **Handlingstype** viser, hvor du skal placere varerne på lageret. Du kan ikke ændre felterne for zone og placering på denne linje.

    > [!NOTE]
    > Hvis det er nødvendigt at placere varerne for en enkelt linje på mere end én placering, f.eks. fordi den angivne placering er fuld, skal du bruge funktionen **Opdel linje** i oversigtspanelet **Linjer**. Handlingen opretter en linje for det resterende antal til ekspedition.

4. Når du har foretaget plukket og har placeret varerne på rette sted, skal du vælge handlingen **Registrer pluk**.  

Den person, der er ansvarlig for leveringen, kan nu bringe varerne til forsendelseshavnen og bogføre leverancen, herunder det relaterede kildedokument, på siden **Lagerleverance**. Flere oplysninger i [Levere varer](warehouse-how-ship-items.md).

## <a name="see-related-microsoft-training" />Se relateret [Microsoft-træning](/training/modules/pick-ship-items-warehouse/)

## <a name="see-also" />Se også

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
