---
title: Afsende varer direkte
description: 'Lære, hvordan du modtager og leverer varer uden at lægge dem på lager.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 10/09/2023
ms.custom: bap-template
ms.search.form: '15, 5703, 7302, 7332, 5768'
---
# <a name="cross-dock-items"></a>Afsende varer direkte

Varer til direkte afsendelse er varer, som du modtager og leverer, uden at lægge dem på lager. Læg-på-lager-og pluk processerne kræver begrænset håndtering af varer. Du kan afsende varer direkte i forbindelse med leverancer og produktionsordrer.

## <a name="cross-dock-bins-and-zones"></a>Dir.afs.placeringer og zoner

Hvis du bruger placeringer, skal du oprette mindst én direkte afsendelsesplacering og derefter angive placeringen i feltet **dir. afs. placeringskode** på dine lokationer. Opret en direkte afsendelseszone, hvis du bruger styret læg-på-lager og pluk.

Når du opretter en leverance eller plukker varer til produktion, og du bruger placeringer, plukkes varen automatisk fra en direkte afsendelsesplacering, før den plukkes fra andre placeringer. Du skal kontrollere området med varer til direkte afsendelse for at se, om de relevante varer er disponible der, før du henter dem på de sædvanlige lagerplaceringer.  

Hvis du har beregnet mængder til direkte afsendelse, oprettes der læg-på-lager-linjer for den direkte afsendelsesplacering for det beregnede antal, når du bogfører modtagelsen. De andre læg-på-lager-linjer oprettes som normalt.  

## <a name="cross-dock-select-lines-for-a-receipt"></a>Vælge linjer til direkte afsendelse for en tilgang

Hvis du vil bogføre de direkte afsendte varer med det samme for at gøre dem disponible til pluk, skal du også registrere en læg-på-lager-aktivitet for de andre varer, der stammer fra modtagelseslinjen, dvs. dem der skal lægges på plads på lageret. Hvis det kun er nogle varer på en modtagelseslinje, der afsendes direkte, skal du derfor sørge for, at resten af varerne lægges på plads så hurtigt som muligt. Lagermetoderne i virksomheden kan alternativt gå ud på, at alle varer på modtagelseslinjer afsendes direkte i så stor udstrækning som muligt.

I læg-på-lager-instruktionen skal du slette instruktions linjerne Hent og Placer for hver modtagelseslinje for de varer, der skal lægges på lager. Disse linjer kan senere oprettes som læg-på-lager-linjer fra læg-på-lager-kladden eller fra den bogførte modtagelse. Efter linjerne er slettet, kan du derefter ekspedere og registrere de linjer, som vedrører varerne til direkte afsendelse.  

## <a name="about-the-put-away-worksheet-page"></a>Om læg-på-lager-kladde-siden

Hvis du har markeret feltet **Brug læg-på-lager-kladde** på **lokationskortet** og har bogført modtagelsen med beregnet direkte afsendelse, bliver alle modtagelseslinjerne tilgængelige i kladden. Oplysninger om direkte afsendelser går tabt og kan ikke genskabes. Hvis du ønsker at bruge funktioner i forbindelse med direkte afsendelse, skal du derfor overføre linjer til læg-på-lager-kladden ved at slette læg-på-lager-instruktioner i stedet for at bruge den automatiske overførselsfunktion via feltet **Brug læg-på-lager-kladde**.  

Hvis du bogfører lagermodtagelsen og ikke har markeret feltet **Brug læg-på-lager-kladde**, vises varerne til direkte afsendelse som separate linjer på læg-på-lager-instruktionen. Feltet **Oplysn. om dir. afsend.** på hver læg-på-lager-linje viser, om linjen indeholder følgende:

* Afsende varer direkte
* Alle varerne fra en modtagelse skal gemmes.
* Nogle varer fra en modtagelse skal opbevares, og nogle skal afsendes direkte.

[!INCLUDE [prod_short](includes/prod_short.md)] fører ikke separate poster til varer, der kan afsendes direkte. Den registrerer dem som almindelige læg-på-lager-instruktioner.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a>Sådan sættes lagerstedet op til direkte afsendelse:

1. Opret mindst én direkte afsendelsesplacering, hvis du bruger placeringer. Opret en direkte afsendelseszone, hvis du bruger styret læg-på-lager og pluk.  

    En direkte afsendelsesplacering har feltet **Dir. afs.placering** markeret og skal have både placeringstypen **Modtag** og **Pluk** markeret. Hvis du vil vide mere om placeringer, skal du gå til [Oprette placeringer](warehouse-how-to-create-individual-bins.md) og [Oprette placeringstyper](warehouse-how-to-set-up-bin-types.md).  

    Hvis du bruger zoner, kan du oprette en zone til direkte afsendelsesplaceringer og markere feltet **Dir.afs.placeringszone**. Du kan få mere at vide om zoner ved at gå til [Konfigurere lokationer til at bruge placeringer](warehouse-how-to-set-up-locations-to-use-bins.md).  

2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokation**, og vælg derefter det relaterede link.  
3. På siden **Lokation** skal du vælge den lokation, hvor du vil opsætte lagerstedet til direkte afsendelse og derefter vælge handlingen **Rediger**.  
4. I oversigtspanelet **Lager** skal du markere afkrydsningsfeltet **Brug dir. afsendelse** og udfylde feltet **Beregn forfaldsdato - dir. afsend** med den tid, der skal søges efter muligheder for direkte afsendelse.

    Indstillingen **Brug dir. afsendelse** er kun tilgængelig, hvis du har markeret felterne **Kræv kvittering**, **Kræv leverance**, **Kræv pluk** og **Kræv læg-på-lager**.  

5. Hvis du bruger placeringer, skal du angive koden for den placering, der som standard skal bruges som direkte afsendelsesplacering, i feltet **Dir.afs.placeringskode** i oversigtspanelet **Placeringer**.  
6. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagervareoversigt**, og vælg derefter det relaterede link.  
7. For hver vare eller lagervare, som du vil kunne afsende direkte, skal du vælg varen og derefter vælge handlingen **Rediger**.
8. På siden **Lagervarekort** skal du markere afkrydsningsfeltet **Brug dir. afsendelse**.  

> [!NOTE]  
>  Direkte afsendelse kan kun udføres, hvis lokationen kræver lagermodtagelse og læg-på-lager.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a>Sådan afsendes varer direkte uden at få vist muligheder

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermodtagelse**, og vælg derefter det relaterede link.  
2. Opret en lagermeddelelse for de varer, der er modtaget, og som måske kan afsendes direkte. Hvis du vil vide mere om modtagelse, skal du gå til [Modtage varer](warehouse-how-receive-items.md).  
3. Udfyld feltet **Modtag (antal)**, og vælg derefter handlingen **Beregn direkte afsendelse**.  

    Udgående kildedokumenter med bestilling på de varer, der er planlagt til afsendelse fra lagerstedet inden for tidsrummet i datoformlen, identificeres. [!INCLUDE[prod_short](includes/prod_short.md)] beregner antal, så du kan afsende så meget som muligt direkte og undgå at lægge varerne på lager. Værdien i feltet **Antal til dir. afsend.** er derfor summen af alle de udgående linjer med bestilling på varen inden for tidshorisonten minus det antal varer, der allerede er blevet placeret i området til direkte afsendelse, eller det er værdien i feltet **Modtag (antal)** på modtagelseslinjen, alt efter hvilken af disse værdier der er mindst. Du kan ikke afsende flere varer direkte, end du har modtaget.  

4. Hvis du vil afsende det foreslåede antal direkte, skal du bogføre modtagelsen. Du kan også øge eller nedsætte vareantallet til direkte afsendelse til en højere eller lavere værdi, før du bogfører modtagelsen.  

    De mængder, der skal afsendes direkte, vises nu som linjer i læg-på-lager-instruktionen, forudsat at feltet **Brug læg-på-lager-kladde** ikke er markeret. De varemængder, der ikke skal afsendes direkte, bliver også til linjer i instruktionen.  

    Hvis du benytter placeringer, er varerne til direkte afsendelse automatisk blevet tildelt den standardplacering, der er defineret på lokationskortet.  

5. Slet **Hent**- og **Placer**-linjerne for varer, der ikke skal afsendes direkte.  
6. Udskriv læg-på-lager-instruktionen for resten af linjerne, og læg de varer fra modtagelsen, der skal på lager, på de korrekte placeringer eller det korrekte område på lagerstedet. Læg varerne til direkte afsendelse i det korrekte område eller på den korrekte placering. Varerne skal muligvis blot forblive i modtagelsesområdet.  
7. Hvis du vil registrere varerne til direkte afsendelse som lagt på plads og som disponible til pluk, skal du vælge handlingen **Registrer**.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a>Sådan afsendes varer direkte efter kontrol af mulighederne

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermodtagelse**, og vælg derefter det relaterede link.  
2. Opret en lagermeddelelse for de varer, der er modtaget, og som måske kan afsendes direkte.  

    Du vil se de linjer i kildedokument, hvor varen bestilles, før du bogfører modtagelsen.  
3. Vælg handlingen **Beregn direkte afsendelse**.  

   På siden **Mulighed for dir. afsend.** kan du se de vigtigste detaljer om linjerne, f.eks. dokumenttype, antal bestilt og forfaldsdato. Du kan bruge disse oplysninger til at bestemme, hvor meget der skal afsendes direkte, hvor varerne skal lægges i området til direkte afsendelse, og hvordan de skal grupperes.  

4. Vælg handlingen **Indsæt ant. til dir. afsend.** for at se, hvordan antallet blev beregnet på modtagelseslinjerne. Når du ændrer antallet af varer i feltet **Antal til dir. afsend** på hver linje, opdateres beregningen. Opdateringen betyder ikke, at leverance-eller produktionsordren faktisk vil modtage de varer, der foreslås til direkte afsendelse. Den er kun til testformål. Handlingen kan imidlertid være informativ, hvis der f.eks. opereres med mere end én enhed.  
5. Du kan reservere et antal varer til en ordrelinje ved at vælge linjen og derefter vælge handlingen **Reserver**. På siden **Reserver** reserveres den tilgængelig mængde for varen. Denne reservation er ligesom alle andre reservationer og får ikke højere prioritet, fordi den er oprettet i forbindelse med direkte afsendelse. Hvis du vil vide mere om reservationer, skal du gå til [Reservere varer](inventory-how-to-reserve-items.md).   
6. Vælg knappen **OK**, når du er færdig med at beregne eller reservere, for at overføre den reviderede beregning til feltet **Antal til dir. afsend.** på modtagelseslinjen, eller vælg knappen **Annuller**, hvis du vil vende tilbage til lagermodtagelsen og beregne den direkte afsendelse igen.  
7. Bogfør kvitteringen. Bogfør nu modtagelsen, og fortsæt med læg-på-lager-instruktionerne som beskrevet i trin 3 til 7 i afsnittet [Sådan afsendes varer direkte uden at få vist muligheder](#to-cross-dock-items-without-viewing-the-opportunities).  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    > [!NOTE]  
    > I læg-på-lager-instruktionen kan du fortsætte med at ændre det antal, der skal lægges på lager, eller som skal afsendes direkte. Det kan f.eks. være, at du beslutter at afsende et ekstra antal varer direkte for at fremskynde registreringen af den direkte afsendelse.  

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>Sådan får du vist varer til direkte afsendelse i leverancer og plukkladde

Hvis du benytter placeringer, kan du se en opdateret beregning af de enkelte vareantal i de direkte afsendelsesplaceringsopdateringer. Når du kan se, at varen er tilgængelig i den direkte afsendelsesplacering, kan du hurtigt oprette et pluk for alle varerne i leverancen. I plukkladden kan du redigere linjerne efter behov.  

Når en produktionsordre er blevet frigivet, er linjerne tilgængelige i plukkladden, og du kan se i feltet **Ant. på dir. afs. placering**, om de varer, du venter på, er ankommet og er blevet anbragt på de direkte afsendelsesplaceringer. Når du opretter en plukvejledning, foreslår [!INCLUDE [prod_short](includes/prod_short.md)], at du plukker varerne til direkte afsendelse først. Varer på lagerplaceringer foreslås bagefter.  

Hvis du ikke benytter placeringer, skal du selv med mellemrum huske at kontrollere det direkte afsendelsesområde eller have besked fra modtagelsen, om at varerne er ankommet.  

## <a name="see-also"></a>Se også

[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
