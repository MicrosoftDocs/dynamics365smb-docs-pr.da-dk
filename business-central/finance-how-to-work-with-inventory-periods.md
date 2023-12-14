---
title: Arbejde med lagerperioder
description: 'Du kan styre den tidsramme, hvor brugere kan bogføre ændringer af lageret ved at definere lagerperioder.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'inventory, periods'
ms.search.form: 5828
ms.date: 04/01/2021
ms.author: bholtorf
---
# Arbejde med lagerperioder

Lagerperioder definerer en tidsperiode, hvor du kan bogføre ændringer i lageret. En lagerperiode er defineret af periodens slutdato. Når du lukker en lagerperiode kan du ikke bogføre ændringer af lageret, hverken forventede eller fakturerede, før denne slutdato. Desuden kan du ikke bogføre nye værdier til lageret før denne slutdato. Hvis der er åbne poster i den lukkede periode, dvs. positive antal, der endnu ikke er blevet udlignet med udgående transaktioner, kan du stadig udligne udgående antal med disse poster, selvom perioden er lukket.  

Følgende afsnit beskriver, hvordan du kan:

* Opret lagerperioder.  
* Luk lagerperioder.  
* Genåbn lagerperioder.  

## Sådan oprettes en lagerperiode

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerperioder**, og vælg derefter det relaterede link.  
2. Opret en ny linje.  
3. I feltet **Slutdato** skal du angive den sidste dato i den lagerperiode, du vil oprette. Når perioden lukkes, vil du ikke kunne bogføre ændringer til lagerbeholdningen før denne dato.  
4. Indtast et beskrivende navn i feltet **Navn**. Vælg knappen **OK**.  

## Lukke lagerperioder

Feltet **Lukket** angiver, om lagerperioden er lukket eller ej for ændringer af lagerbeholdningsværdien. Du kan ikke redigere feltet.  

Du kan lukke alle lagerperioder, hvis følgende gør sig gældende:  

* Der er ingen åbne udgående vareposter, dvs. negativ lagerbeholdning, i perioden.  
* Kostprisen for alle varer er blevet reguleret med kørslen **Reguler kostværdi - vareposter**.  

Det betyder, at alle udgående transaktionsantal, f.eks. dem fra salgsordrer, udgående overflytninger, salgsfakturaer, købsreturvarer eller købskreditnotaer, skal være anvendt på eksisterende antal i lagerbeholdningen.  

### Sådan lukkes en lagerperiode  

1. Før du lukker en lagerperiode, skal du vælge handlingen **Juster kostpris – vareposter** for at sikre, at alle kostprisreguleringer er bogført.

    Udfør rapporten **Luk lagerperiode - kontrol** for at kontrollere, om der er nogen udgående vareposter i lagerperioden eller nogen varer, hvor kostprisen endnu ikke er blevet reguleret.  
2. Vælg handlingen **Luk lagerperiode – kontrol**.  

    Udfør kørslen **Bogfør lagerregulering** for at sikre, at alle kostpriser er bogført i Finans.  
3. Vælg handlingen **Bogfør lagerbeholdning**.  
4. På siden **Lagerperioder** skal du vælge den lagerperiode, du vil lukke.  
5. Vælg handlingen **Luk periode**. Når lagerperioden er blevet lukket, kan du ikke bogføre ændringer til lagerbeholdningen før slutdatoen. Kostprisen på alle varer skal reguleres med kørslen **Reguler kostværdi - vareposter**, før du kan lukke lagerperioden.  
6. Klik på **Ja** for at bekræfte, at du vil lukke perioden, eller klik på **Nej** for at annullere lukningen.  
7. Lagerperioden lukkes, og der vises en meddelelse, når det er udført.  

## Genåbne lagerperioder  
Når du har lukket lagerperioden, kan du ikke slette den. Du kan dog genåbne den, hvis du vil tillade bogføring før lagerperiodens slutdato. Hvis du genåbner en periode, genåbnes også alle de lagerperioder med slutdatoer, som er efter den periode, du genåbnede.  

### Sådan genåbnes en lagerperiode  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerperioder**, og vælg derefter det relaterede link.  
2. Vælg den lagerperiode, du vil åbne igen.  
3. Vælg handlingen **Åbn periode igen**. Bekræft, at du vil genåbne perioden.  
4. Alle lagerperioder med slutdatoer efter den periode, du valgte, genåbnes.  

## Se også  
[Designoplysninger: Lagerperioder](design-details-inventory-periods.md)  
[Finans](finance.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med Finans](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]