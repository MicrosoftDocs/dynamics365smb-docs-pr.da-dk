---
title: Administrere produktvarianter
description: 'Få mere at vide om, hvordan du kan registrere produkter, der er næsten identiske, men varierer i farver, størrelse eller materiale som varevarianter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---

# <a name="manage-product-variants"></a>Administrere produktvarianter

Varevarianter er en smart måde at holde listen over produkter under kontrol på. Det kan være nyttigt, hvis du f.eks. har et stort antal varer, der kun adskiller sig fra hinanden ved farven. Du kan definere hver variant som en separat vare. Du kan imidlertid også vælge at oprette en vare og angive de forskellige farver som varianter af varen.  

> [!TIP]
> Hvis du vil have en praktisk introduktion til brugen af varianter i produktionen, kan du se [Gennemgang: varianter](contoso-coffee/manufacturing/variants.md) af demonstrationsdataene for Contoso Coffee.  

## <a name="add-variants-to-an-item"></a>Føje varianter til en vare

Det er nemt nok at definere varianter for en vare.  

### <a name="to-add-variants"></a>Sådan tilføjes varianter

1. Åbn [siden **Vareliste**](https://businesscentral.dynamics.com/?page=31), og åbn den relevante vare.  
2. Vælg handlingen Relateret på Vare **kort, vælg** derefter Vare **, og vælg derefter handlingen** Varianter **.** **·**   
3.  **Angiv varianterne på siden Varevarianter** .  

Når du derefter opretter et salgsdokument og tilføjer varen, kan du angive varianten af varen i feltet **Variantkode** . Det samme gælder for indkøbsdokumenter.  

## <a name="item-availability-by-variant"></a>Varetilgængelighed pr. variant

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="require-use-of-variants"></a>Kræver brug af varianter

Fra 2022 Udgivelsesbølge 2 kan administratorer kræve, at brugere angiver varianten i dokumenter og kladder for varer, der har varianter. Hvis du vil aktivere egenskaben, skal du gå til siden **Lageropsætning** og vælge feltet **Variantobligatorisk, hvis feltet findes**. Du kan tilsidesætte denne globale indstilling for bestemte varer.  

På varekort har feltet **Variant obligatorisk, hvis der findes** følgende muligheder:

|Feltværdi |Beskrivelse|
|---------|----|
|Standard (Nej)| Indstillingen fra **Lageropsætning** gælder for varen.|
|Nr.| Brugere behøver ikke at angive en variant for denne vare.|
|Ja| Hvis varen har en eller flere varianter, skal de angive varianten. Hvis de ikke gør det, vil de være spærret for bogføring af transaktionen.|

> [!NOTE]
> Disse indstillinger påvirker ikke elementer, der ikke har nogen varianter.

Hvis faciliteten er aktiveret, kan du ikke bogføre en post, hvis varianten ikke er angivet.

## <a name="categories-attributes-and-variants"></a>Kategorier, attributter og varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Se også

[Registrer nye varer](inventory-how-register-new-items.md)    
[Oprette generelle lageroplysninger](inventory-how-setup-general.md)    
[Gennemgang: Varianter](contoso-coffee/manufacturing/variants.md)    
