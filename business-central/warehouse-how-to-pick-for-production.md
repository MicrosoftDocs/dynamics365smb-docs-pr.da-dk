---
title: 'Plukke eller flytte varer til produktion, montage eller jobs i grundlæggende lageropsætninger'
description: 'Når lagerlokationen kræver pluk, men ikke leverance, skal du bruge siden Pluk (lager) til at organisere og registrere pluk af komponenter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.forms: '9330, 931, 990008, 89, 900, 902'
---
# <a name="pick-for-production-assembly-or-projects-in-basic-warehouse-configurations"></a>Plukke til produktion, montage eller jobs i grundlæggende lageropsætninger

Hvordan du skal lægge komponenter på lager til produktions-. sags eller montageordrer afhænger af den måde, som lagerstedet er sat op på som en lokation. Flere oplysninger i [Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md).

I en avanceret lageropsætning for den udgående flow (pluk), skal du slå til/fra **Kræv pluk** og **Kræv leverance** på siden **Lokationskort** for lokationen.

Brug følgende dokumenter for interne operationer:

* Pluk
* Flytning (lager)

## <a name="inventory-picks"></a>Lagerpluk

* Når du registrerer et pluk for en intern handling, såsom produktion eller en sag, bogføres forbrug af de komponenter, der er plukket på samme tid.
* Afkrydsningsfeltet **Tvungen placering** på **lokationskortet** er markeret.
* Når du bruger pluk fra lager definerer feltet **Placeringskode** på en produktionsordrekomponentlinje eller projektplanlægningslinjer *hente*-placeringen. Komponenterne formindskes i vinduet Hent, når du bogfører forbrug.

## <a name="inventory-movements"></a>Flytninger (lager)

* Hvis du vil bruge pluk fra lager til sager, skal du aktivere funktionen **Tvungen placering** på siden **Lokationskortet** for lokationen.
* Lagerbevægelser fungerer kun med produktionsordrekomponentlinjer og montageordrelinjer.
* Når du registrerer en flytning (lager) for en intern handling, registrerer du kun fysisk flytning af nødvendige komponenter til en placering i handlingsområdet. Du ikke bogfører forbrug.
* Når du bruger pluk fra lager definerer feltet **Placeringskode** på en produktionsordrekomponentlinje den *hente*-placering, som komponenter tages fra, når forbruget posteres. Placeringen er stedet, hvor lagermedarbejdere skal placere komponenterne.
* Registrere forbruget af de plukkede komponenter separat ved at bogføre en forbrugskladde eller montageordre.

>[!NOTE]
> Selvom funktionen **Kræv pluk** er slået fra, kan du bruge et **lagerpluk**-dokument. Lagerpluk svarer til **pluk (lager)**-dokumenter. Dette er nyttigt, hvis du vil bruge pluk i operationer og levering i udgående lagerflows.

### <a name="production"></a>Produktion

Brug **Lagerpluk**-dokumenter til at plukke produktionskomponenter i forløbet til produktion.

For en lokation, der bruger placeringer, kan du udvide strømmen til produktion ved hjælp af **flytning (lager)**-dokumenter. Lagerbevægelser er især nyttige ved træk med komponenter. Hvis du ønsker yderligere oplysninger om, hvordan komponentforbrug tømmes fra produktionsplaceringen eller den åbne produktionsplacering, kan du se afsnittet [Træk af produktionskomponenter i lageret](#flushing-production-components-in-a-basic-warehouse-configuration).

### <a name="assembly"></a>Montage

Bruge **Flytning (lager)**-dokumenter af varer til at flytte montagekomponenter til montageområdet.

> [!NOTE]
> **Flytning (lager)**-dokumenter kræver placeringer.

[!INCLUDE [prod_short](includes/prod_short.md)] understøtter montage efter lager-og montage efter ordre-montage processer. Hvis du vil vide mere om montage efter ordre i den udgående lagergang, skal du gå til [Håndtering af ordremontagevarer i lagerleverancer](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="project-management"></a>Projektstyring

Brug **Lagerpluk**-dokumenter til at plukke produktionskomponenter i forløbet til produktion.

For en lokation, der bruger placeringer, kan du udvide strømmen til produktion ved hjælp af **flytning (lager)**-dokumenter.

> [!NOTE]
> Muligheden for at plukke komponenter til projektplanlægningslinjer blev tilføjet i [!INCLUDE[d365fin](includes/d365fin_md.md)] i 2022 udgivelsesbølge 2. Hvis du vil starte med at bruge funktionen, skal din administrator aktivere **Funktionsopdatering: Aktivér lagerbeholdning og lagerpluk fra job** på siden **Funktionsstyring**.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] bruger værdien i feltet **Restantal** på projektplanlægningslinjen, når der oprettes pluk (lager). Hvis du vil bruge pluk fra lager til sager, skal du aktivere funktionen **Anvend anvendelseslink** på siden **Projektkort** for sagen. På den måde kan du spore forbruget i forhold til din plan. Hvis du ikke aktiverer til/fra, forbliver restantallet ved **0**, og lagerplukket bliver ikke oprettet. Du kan finde flere oplysninger i [Sådan konfigureres projektforbrugssporing](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-project-usage-tracking).

## <a name="pick-or-move-for-production-assembly-and-projects-in-a-basic-warehouse-configuration"></a>Plukke eller flytte til produktion, montage eller projekter i grundlæggende lageropsætninger

Du kan oprette et lagerpluk eller en lagerflytning på tre måder:  

* Fra selve kildedokumentet.  
* Du kan oprette pluk for mange kildedokumenter samtidig ved hjælp af kørslen.  
* I to trin. Frigiv kildedokumentet for at gøre kildedokumentet klar til plukning. Oprette pluk eller bevægelse for lager ud fra **Lagerpluk** eller **lagerbevægelse**-dokumenter. Lagerpluk eller flytninger er baseret på kildedokument.  

### <a name="to-create-an-inventory-pick-from-the-source-document"></a>Sådan oprettes et pluk på basis af kildedokumentet

1. På kildedokumentet, som kan være en produktionsordre eller et job, skal du vælge handlingen **Opret læg-på-lager/pluk (lager)**.  
2. Markér afkrydsningsfeltet **Opret pluk (lager)**.
3. Vælg knappen **OK**.

### <a name="to-create-an-inventory-movement-from-the-source-document"></a>Sådan oprettes en lagerflytning fra kildedokumentet

1. På kildedokumentet, som kan være en produktionsordre eller et job, skal du vælge handlingen **Opret læg-på-lager/pluk (lager)**.  
2. Markér afkrydsningsfeltet **Opret pluk (lager)**.
3. Vælg knappen **OK**.

### <a name="to-create-multiple-inventory-picks-or-movements-with-a-batch-job"></a>Sådan oprettes flere pluk fra lager eller flytninger med en kørsel

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opret læg-på-lager/pluk (lager)**, og vælg derefter det relaterede link.  
2. Brug felterne **Kildedokument** og **Kildenr.** i oversigtspanelet **Lageranmodning** til at filtrere på bestemte typer dokumenter eller rækker af dokumentnumre. Du kan for eksempel oprette pluk til kun produktionsordrer.
3. Gå til oversigtspanelet **Indstillinger**, og aktiver funktionen **Opret pluk (lager). Pluk** eller **Opret pluk (lager). Bevægelse** .
4. Vælg knappen **OK**.

### <a name="to-create-inventory-picks-or-movements-in-two-steps"></a>Sådan oprettes pluk (lager) eller bevægelser i to trin

Hvis du vil plukke eller flytte komponenter til kildedokumenter på to måder, skal du frigive kildedokumentet for at gøre det klar til pluk. Frigiv kildedokumenter for interne operationer på følgende måder.  

|Kildedokument|Frigivelsesmetode|  
|---------------------|--------------------|  
|Produktionsordre|På siden **Planlagt produktionsordre** skal du ændre status for en ordre til **frigivet** eller bruge siden **frigivet produktionsordre** til at oprette en frigivet produktionsordre.|  
|Montageordre|Ændre status på en produktionsordre til **Frigivet**.|
|Sager | Skift status til **åben** eller Opret job med status åben med.|  

En lagermedarbejder, der er knyttet til pluk varer, kan oprette et læg-på-lager-dokument for kildedokumentet.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk fra lager** eller **Flytning (lager)**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. I feltet **Kildedokumentet** skal du vælge den kildedokumenttype, du lægger på lager for.

    > [!NOTE]
    > Du kan ikke bruge **Lagerpluk**-dokumenter til at plukke montagekomponenter.
4. Vælg kildedokumentet i feltet **Kildenr.**.  
5. Du kan også vælge handlingen **Hent kildedokument** for at vælge kildedokumentet på en liste over indgående kildedokumenter, der er klar til læg-på-lager på lokationen.  
6. Vælg knappen **OK** for at udfylde pluklinjerne i overensstemmelse med det valgte kildedokument.  

## <a name="to-record-the-inventory-pick"></a>Sådan registreres lagerpluk

1. Åbn det dokument, der skal registreres bevægelser for, på siden **Flytning (lager)**.  
2. I feltet **Placeringskode** på pluklinjerne, foreslås den placering, som varerne skal plukkes fra, pr. varens standardplacering. Om nødvendigt kan du ændre placeringen.
3. Pluk varerne, og indtast det antal varer, der er plukket, i feltet **Håndteringsantal**.

    Hvis det er nødvendigt at placere varerne for en enkelt linje på mere end én placering, f.eks. fordi den angivne placering er fuld, skal du bruge funktionen **Opdel linje** i oversigtspanelet **Linjer**. Handlingen opretter en linje for det resterende antal til ekspedition.  
4. Vælg handlingen **Bogfør**.  

Der sker følgende under bogføringsprocessen:

* Bogfør forbruget af de kildedokumentlinjer, der er blevet plukket.
* Hvis lokationen anvender placeringer, oprettes der også lagerposter til bogføring af ændringer af placeringsantallet.

[!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="to-record-the-inventory-movement"></a>Sådan registreres læg-på-lager-aktiviteten

1. Åbn det dokument, der skal registreres bevægelser for, på siden **Flytning (lager)**.  
2. I feltet **Placeringskode** på pluklinjerne, foreslås den placering, som varerne skal plukkes fra, pr. varens standardplacering. Om nødvendigt kan du ændre placeringen.  
3. Pluk varerne, og indtast det antal varer, der er plukket, i feltet **Håndteringsantal**. Værdien i Hent- og Placer-linjerne skal være den samme. Ellers kan du ikke registrere bevægelsen.

    Hvis det er nødvendigt at placere varerne for en enkelt linje på mere end én placering, f.eks. fordi den angivne placering er fuld, skal du bruge funktionen **Opdel linje** i oversigtspanelet **Linjer**. Handlingen opretter en linje for det resterende antal til ekspedition.  
4. Vælg handlingen **Opret bevægelse**.  

Der sker følgende under bogføringsprocessen:

* Der oprettes lagerposter som tegn på, at komponenterne nu findes på de placeringer, der er angivet i montageordrelinjerne. F.eks. montageordre, produktionskomponent eller projektplanlægningslinje.

>[!NOTE]
> I modsætning til når du flytter komponenter med et lagerpluk, bogføres forbrug ikke, når du registrerer en flytning (lager). Du registrerer forbruget som et separat trin ved at bogføre kildedokumentet.

## <a name="flushing-production-components-in-a-basic-warehouse-configuration"></a>Trække komponenter til produktion i en grundlæggende lageropsætning

Trækmetoder påvirker også flowet af komponenter i produktionen. Flere oplysninger i [Udtrække komponenter i henhold til operationsafgang](production-how-to-flush-components-according-to-operation-output.md). Afhængigt af den valgte Trækmetode kan du plukke komponenter til produktions objekterne på følgende måder:

* Brug et **pluk (logistik)**-dokument til at registrere plukningen for varer, der bruger den **manuelle** Trækmetode. Når du registrerer et lagerpluk, bogføres forbruget af de plukkede komponenter. 
* Bruge et **lagerbevægelse**-dokument med en reference til et kildedokument til at registrere pluk for komponenter, der bruger den **manuelle** trækmetode. Du har brug for at registrere forbruget separat. Flere oplysninger i [Massebogføre produktionsforbrug](production-how-to-post-consumption.md). 
* Bruge et **lagerbevægelse**-dokument med en reference til et kildedokument til at registrere pluk for komponenter, der bruger **Pluk + Fremad**, **Pluk + Baglæns**-trækmetoden. Forbruget af komponenterne sker automatisk, når du ændrer status for produktionsordren eller ved at starte eller afslutte en operation. Alle nødvendige komponenter skal være tilgængelige. Ellers stopper den udtrukne forbrugsbogføring for den pågældende komponent.
* Bruge et **lagerbevægelse**-dokument uden en reference til et kildedokument eller andre måder at registrere flytning af komponenter på, der bruger trækmetoden **forlæns** eller **baglæns**. Forbruget af komponenterne sker automatisk, når du ændrer status for produktionsordren eller ved at starte eller afslutte en operation. Alle nødvendige komponenter skal være tilgængelige. Ellers stopper den udtrukne forbrugsbogføring for den pågældende komponent. Du kan finde flere oplysninger i [Flytte varer ad hoc i grundlæggende lageropsætninger](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="example"></a>Eksempel

Der findes en produktionsordre for 15 stk. af vare SP-SCM1004. Nogle af varerne på komponentlisten skal trækkes manuelt i en forbrugskladde, og andre varer på listen kan plukkes og trækkes automatisk ved hjælp af metoden **pluk + baglæns**.  

De følgende trin beskriver de handlinger, der er involveret for forskellige brugere, og de relaterede svar:  

1. Den tilsynsførende frigiver produktionsordren. Elementer med **Fremad** som trækmetode og ingen rutebindingskode bliver fratrukket åben produktionsplacering.  
2. Hoved tilsynet med Shop vælger **Opret læg-på-lager/pluk**-handling på produktionsordren og aktiverer funktionen **Opret pluk (lager). Pluk** og **Opret pluk (lager). Bevægelse**. Der oprettes et plukdokument (lager) for varer med **Manuel** Trækmetode, og der oprettes en flytning (lager) for varer med **Pluk + Bagud** og **Pluk + Forlæns** træk.
3. Lagerchefen tildeler pluk og flytninger til en lagermedarbejder.
4. Lagermedarbejderen plukker varerne fra relevante placeringer og placerer dem på produktionsplaceringen eller på placeringen, der er angivet på lagerbevægelsen. Placeringen kan muligvis være et arbejdscenter eller en produktionsressource.  
5. Lagermedarbejderen registrerer plukket. Antallet trækkes fra placeringerne.
6. Lagermedarbejderen registrerer flytningen. Antallet trækkes fra plukplaceringerne og føjes til forbrugsplaceringen. Feltet **Plukket antal** på komponentlisten for alle de plukkede varer opdateres.  
7. Maskinoperatøren oplyser produktionschefen om, at færdigvarerne er klar.  
8. I Shop Floor supervisor bruges afgangskladden eller produktionskladden til at bogføre afgangen. Den mængde komponentvarer, der bruger **Pluk + Fremad**- eller **Pluk + Baglæns**-trækmetode med rutebindinger, trækkes fra til produktions placeringen.
9. Produktionschefen bogfører afgang for produktionsordren og ændrer status til **Udført**. Antallet af komponentvarer, der bruger **baglæns**-trækmetoden, trækkes fra den åbne produktionsplacering, og antallet af komponentvarer, der bruger **pluk + baglæns**-trækmetoden trækkes fra produktionsplaceringen.  

 Følgende illustration viser, når feltet **Placeringskode** på komponentlisten udfyldes i overensstemmelse med konfiguration af din lokation eller maskine/arbejdscenter.  

:::image type="content" source="media/binflow.png" alt-text="Oversigt over, hvornår/hvordan feltet Placeringskode skal udfyldes.":::

## <a name="see-also"></a>Se også

[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
