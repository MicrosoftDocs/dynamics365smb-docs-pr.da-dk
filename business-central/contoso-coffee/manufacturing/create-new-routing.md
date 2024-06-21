---
title: Opret en ny rute
description: 'Gennemgang for at få mere at vide om, hvordan du angiver alle oplysninger om en ny rute manuelt i Business central.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---
# <a name="walkthrough-create-a-new-routing"></a>Gennemgang: Opret en ny rute

I denne artikel kommer vi igennem de trin, du skal benytte, når du skal arbejde med Contoso Coffee-demodata til manuelt at opsætte ny produktionsrute i [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## <a name="scenario"></a>Scenarie

Oscar, procesteknikeren hos Contoso Coffee beslutter at oprette en ny rute med navnet *Ny sti*. Da denne rute ikke svarer til nogen anden rute hos Contoso Coffee, skal Oscar manuelt angive alle oplysninger til ruten.  

## <a name="steps"></a>Trin

1. Opret rutehovedet.  

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rute**, og vælg derefter det relaterede link.  

    2. Vælg handlingen **Ny**, og udfyld derefter felterne som beskrevet i følgende tabel.  

        |Felt  |Værdi  |
        |---------|---------|
        |**Nummer** |1099|
        |**Beskrivelse** |Ny sti|
2. Sådan oprettes rutelinjer.

    1. Rediger eller udfyld felterne i oversigtspanelet **Linjer** som beskrevet i følgende tabel.  

        |Felt  |Værdi  |
        |---------|---------|
        |**Operationsnr.** |10|
        |**Type** |Arbejdscenter|
        |**Nummer** |100|
        |**Opstillingstid** |20|
        |**Kørselstid** |15|

    2. Tilføj en ny linje, eller udfyld felterne i oversigtspanelet Linjer som beskrevet i følgende tabel.  

        |Felt  |Værdi  |
        |---------|---------|
        |**Operationsnr.** |20|
        |**Type** |Arbejdscenter|
        |**Nummer** |200|
        |**Opstillingstid** |30|
        |**Kørselstid** |5|
3. Godkend ruten.

    1. Vælg **Godkendt** i feltet *Status*.  

Den nye rute er nu oprettet.  

## <a name="see-also"></a>Se også

[Introduktion til demonstrationsdata for Contoso Coffee](../contoso-coffee-intro.md)  
