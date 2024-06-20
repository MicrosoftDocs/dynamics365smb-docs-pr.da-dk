---
title: 'Angive, hvilke indgående dokumenter der skal vises'
description: 'Tilpas standardvisningen af indgående bilag, f.eks. e-fakturaer, for at forbedre din oversigt over behandlede og ikke-behandlede poster.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Administrere mange indgående bilagsposter

Efterhånden som du opretter eller behandler indgående bilagsposter, kan antal linjer på siden **Indgående bilag** vokse til et omfang, hvor du mister overblikket. Derfor kan du indstille indgående bilagsposter til *Behandlet* for at fjerne dem fra standardvisningen. Når du vælger handlingen **Vis alle**, kan du få vist både behandlede og ikke-behandlede poster.

> [!NOTE]  
> Du kan ikke redigere oplysningerne, vedhæfte filer eller udføre andre processer på indgående bilagsposter, der er indstillet til *Behandlet*. Du skal først indstille dem til *Ikke-behandlet*.

Afkrydsningsfeltet **Behandlet** markeres automatisk på indgående bilagsposter, der er blevet behandlet, men du kan også markere eller fjerne markeringen i feltet manuelt. Afhængigt af din forretningsproces kan en indgående bilagspost blive behandlet, når der er oprettet et relateret bilag til den, eller der er vedhæftet en fil.

> [!NOTE]  
> Når du åbner siden **Indgående bilag** med handlingen **Indgående bilag** i Rollecenter, vises kun ikke-behandlede indgående bilagsposter som standard. I dette emne omtales det som "standardvisningen".

## Sådan fjernes indgående bilagsposter fra standardvisningen

1. På siden **Indgående bilag** skal du vælge en eller flere linjer for indgående bilagsposter, du vil fjerne fra standardvinduet.
2. Vælg handlingen **Indstil til behandlet**.

    Indgående bilagsposter fjernes fra standardvisningen og afkrydsningsfeltet **Behandlet** markeres på linjerne.

> [!NOTE]  
> Du kan også udføre handlingen for den individuelle post på siden **Indgående bilagskort**.

## Sådan vises alle indgående bilagsposter

1. På siden **Indgående bilag** skal du vælge handlingen **Vis alle**.

Alle indgående bilagsposter vises, herunder poster, hvor feltet **Behandlet** ikke er markeret.

## Sådan føjes indgående bilagsposter til standardvisningen

1. På siden **Indgående bilag** skal du vælge handlingen **Vis alle**.
2. Vælg en eller flere linjer for indgående bilagsposter, der skal vises i standardvisningen.
3. Vælg handlingen **Indstil til ikke-behandlet**.  

> [!NOTE]  
> Du kan også udføre handlingen for den individuelle post på siden **Indgående bilagskort**.

## Se også
  
[Oprette indgående bilagsposter](across-how-create-income-document-records.md)
[Oprette indgående bilagsposter direkte fra dokumenter og poster](across-how-connect-disconnect-income-document-records.md)
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
