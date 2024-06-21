---
title: Importere mange varebilleder fra en zip-fil
description: 'Du kan importere flere varebilleder svarende til dine varenumre ved at komprimere dem til en zip-fil, og benyt siden Importer varebilleder for at styre, hvilke varebilleder, der skal importeres.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'product, image'
ms.search.form: '30, 461'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Importer flere varebilleder
Du kan importere flere varebilleder på en gang. Navngiv blot dine billedfiler svarende til dine varenumre, komprimer dem til en zip-fil, og benyt siden Importer varebilleder for at styre, hvilke varebilleder, der skal importeres.

Alle standardfilformater er understøttet.

## Navngivning af billedfiler efter varenavne og klargøring af zip-filen
1. Navngiv hver fil i henhold til den pågældende vares nummer på lokationen, hvor du dine varebilleder er gemt. Eksempler:

    |Varenr.|Filnavn|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Saml alle filerne i en zip-fil. F.eks.: I Windows Explorer vælger du filerne, og derefter vælger du **Send til**, **Komprimeret (zipped) mappe**.     

## Importer varebilleder
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af Lager**, og vælg derefter det relaterede link.
2. Vælg handlingen **Importer billeder**.
3. Find feltet **Vælg en zip-fil**, vælg den relevante zip-mappe, og vælg dernæst knappen **Åbn**.

    Der oprettes en linje for hver vare og billede på siden **Importer varebilleder**.

    > [!NOTE]
    > For varekort, der allerede har et billede, vælges afkrydsningsfeltet **Billede findes allerede**. Hvis du ikke ønsker, at eksisterende billeder erstattes, fravælges afkrydsningsfeltet **Erstat billeder**. Hvis du ikke ønsker, at individuelle eksisterende billeder erstattes, skal du slette de pågældende linjer.

3. Vælg handlingen **Importer billeder**.

Feltet **Importstatus** opdateres for at vise, om billedimporten blev annulleret eller gennemført.       

## Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Oprette nummerserie](ui-create-number-series.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]