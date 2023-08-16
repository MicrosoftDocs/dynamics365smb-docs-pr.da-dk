---
title: Flytte varer ad hoc i ikke-planlagte lageropsætninger
description: I denne artikel forklares ikke planlagte interne overførsler mellem placeringer uden behov fra kildedokumenter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '393, 7382'
---
# Flytte varer internt i grundlæggende konfigurationer af lagersteder

Du kan flytte varer mellem placeringer uden et behov fra et kildedokument. F. eks. som en del af følgende aktiviteter:

* Reorganiser lagerstedet.
* Flytte varer til et kontrolområde.
* Flytte ekstra varer til og fra et produktionsområde. 

Hvordan du flytter varer afhænger af den måde, som lagerstedet er sat op på som en lokation. Flere oplysninger i [Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md).

I lageropsætninger, hvor indstillingen til til/fra **placering obligatorisk**-opsætning er aktiveret, men ikke **styret pluk og læg-på-lager**, kan du registrere ikke-planlagte bevægelser på følgende sider:  

* På siden **Intern flytning**.
* Med siden **Vareomposteringskladde**.  

## Interne flytninger

Du kan bruge siden **interne overførsler** til at angive Hent-og Placer-linjer, når der ikke er behov fra et kildedokument. Den interne overførsel fungerer som et regneark til organisering af ting. Du kan ikke behandle den aktuelle bevægelse direkte fra den. Når en linje er udfyldt, skal du bruge handlingen **Opret lagerbevægelse** til at sende linjen til siden **flytning (lager)**, hvor du behandler og registrerer bevægelsen.

### Sådan flyttes varer som en intern overførsel

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Intern flytning**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Sørg for, at feltet **Nr.** er udfyldt i oversigtspanelet **Generelt**.
3. I feltet **Lokationskode** skal du indtaste den lokation, hvor flytningen finder sted.  

    Hvis lokationen er angivet som din standardlokation som lagermedarbejder, tilføjes lokationskoden automatisk.  
4. I feltet **Til placeringskode** skal du indtaste en kode for den placering, du vil flytte elementet til.

    Til produktionsformål kunne dette f.eks. være koden for den åbne produktionsplacering som defineret på lokationskort eller i arbejdscenteret.  
5. I feltet **Forfaldsdato** skal du indtaste den dato, som bevægelsen skal være udført inden.  
6. Udfyld felterne på linjen efter behov. Interne overførsels dokumenter har én linje pr. bevægelse. Linjen indeholder både Hent-og Placer-handlinger.
7. Vælg **Varenr.** for at åbne siden med **Placeringsindhold**. Vælg den vare, der skal flyttes, afhængigt af dets tilgængelighed, på placeringer. Du kan også vælge **Hent aktions indhold** for at udfylde de interne overførselslinjer på basis af dine filtre.  

    Når du har valgt varen, udfyldes feltet **Fra placeringskode** automatisk i overensstemmelse med det valgte placeringsindhold. Du kan vælge en placering, hvor varen er disponibel. Feltet **Varenr.** og **Fra placeringskode** relaterede felter. Hvis du ændrer værdien i et felt, ændres værdien i det andet felt muligvis.  

    Feltet **Til placeringskode** udfyldes med den værdi, du har angivet i hovedet. Du kan ændre den på linjen til en anden placeringskode, der ikke er spærret eller dedikeret til specielle formål. Få mere at vide i [Feltet dedikeret](warehouse-how-to-create-individual-bins.md#the-dedicated-field).  

8. Når du har defineret, hvilke placeringer du vil flytte elementet fra og til, skal du angive det antal, der skal flyttes, i feltet **Antal**.  

    > [!NOTE]  
    > Antallet skal være tilgængeligt på den placering, der er angivet i feltet **Fra placeringskode** .  

9. Når du er klar til at behandle den interne overførsel, skal du vælge handlingen **Opret flytning (lager)**.  

    > [!NOTE]  
    >  Når du har oprettet lagerflytningen, slettes de interne overførselslinjer.  

Du udfører resten af ad hoc-bevægelsen på siden **Flytning (lager)** på samme måde som i en bevægelse, der er baseret på kildedokumenter.

### Sådan registreres læg-på-lager-aktiviteten

1. Åbn det dokument, der skal registreres bevægelser for, på siden **Flytning (lager)**.  
2. I feltet **Placeringskode** på pluklinjerne, foreslås den placering, som varerne skal plukkes fra, pr. varens standardplacering. Om nødvendigt kan du ændre placeringen.
3. Udfør plukaktiviteten, og angiv oplysningerne for den faktiske mængde, der er lagt på lager, i feltet **Håndteringsantal**. Værdien i Hent- og Placer-linjerne skal være den samme. Ellers kan du ikke registrere bevægelsen.

    Hvis det er nødvendigt at placere varerne for en enkelt linje på mere end én placering, f.eks. fordi den angivne placering er fuld, skal du bruge funktionen **Opdel linje** i oversigtspanelet **Linjer**. Handlingen opretter en linje for det resterende antal til ekspedition.  
4. Vælg handlingen **Opret bevægelse**.  

Der sker følgende under bogføringsprocessen:

* Lagerposter angiver, at antallet overføres fra flytte placeringer til placeringerne.

## Sådan flyttes varer i vareomposteringskladden

I stedet for at bruge lagerbevægelsesdokument kan du registrere flytningen af varer ved at ompostere deres placeringskoder. Flere oplysninger i [Tælle, justere og ompostere lagerbeholdning ved hjælp af kladder](inventory-how-count-adjust-reclassify.md)

> [!NOTE]  
> Bevægelser, der er bogført med omposterings kladder, gør ikke bevægelses dokumenterne klar til flytning.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vareomposteringskladder**, og vælg derefter det relaterede link.  
2. På hver kladdelinje skal du definere placeringer, og som du vil flytte elementer til og fra, ved at udfylde felterne **Placeringskode** og **Ny placeringskode**.  

    1. Hvis du vil flytte hele indholdet i en placering til en anden placering, skal du klikke på handlingen og vælge handlingen **Hent placeringsindh.**.  
    2. Udfyld filtrene for at finde den placering, hvis indhold du vil flytte, og klik derefter på knappen **OK**. Kladdelinjerne udfyldes med indholdet af placeringen.  
3. Udfyld resten af felterne på de enkelte kladdelinjer.
4. Bogfør omposteringskladden.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Se relateret [Microsoft-træning](/training/modules/manage-internal-warehouse-processes/)

## Se også

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
