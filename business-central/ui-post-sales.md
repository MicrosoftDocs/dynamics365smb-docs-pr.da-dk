---
title: Bogføring af salgsdokumenter | Microsoft Docs
description: Lære mere om de forskellige bogføringsfunktioner til bogføring af salgsdokumenter, og hvordan du kan opdatere bogførte dokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 12/03/2020
ms.author: edupont
ms.openlocfilehash: e0d1bd7770eb3bb44a2e9b3203ffa158a246cfa9
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392045"
---
# <a name="posting-sales"></a>Bogføring af salg

I menuen **Bogføring** i et salgsdokument kan du vælge mellem følgende bogføringsfunktioner:

* **Bogfør**
* **Bogfør og ny**
* **Bogfør og send**
* **Vis bogføring**
* **Massebogfør**
* **Testrapport**

> [Bemærk!] I forbindelse med salgsordrer kan du også se indstillinger, der vedrører forudbetalingsfunktionen. Du kan finde flere oplysninger i [Fakturere forudbetalinger](finance-invoice-prepayments.md). 

Når du har udfyldt alle linjer og har indsat alle oplysninger i salgsordren, kan du bogføre den. Dette opretter en leverance og en faktura.

Når en salgsordre bogføres, opdateres kreditorens konto, regnskabet og vareposterne.

For hver salgsordre oprettes der en salgspost i tabellen **Finanspost**. Der oprettes også en post i debitorkontoen i tabellen **Debitorpost**, og der oprettes en finanspost i den relevante samlekonto. Desuden kan der eventuelt blive dannet en momspost og en finanspost for rabatbeløbet. Om der bogføres en post med rabat, afhænger af oplysningerne i feltet **Bogføring med rabat** på siden **Salgsopsætning**.

For hver salgsordrelinje oprettes der en varepost i tabellen **Varepost** (hvis salgslinjerne indeholder varenumre) eller en finanspost i tabellen **Finanspost** (hvis der er indsat en finanskonto på salgslinjerne). Salgsordrer bliver desuden altid registreret i tabellerne **Salgsleverancehoved** og **Salgsfakturahoved**.

> [!IMPORTANT]  
> Når du bogfører en ordre, har du mulighed for både at oprette en leverance og en faktura. Det kan gøres på samme tid eller hver for sig. Du kan også oprette en delleverance og en delfaktura ved at udfylde felterne **Lever (antal)** og **Fakturer (antal)** på de enkelte salgsordrelinjer, før du bogfører. Bemærk, at du ikke kan oprette en faktura for noget, der ikke er leveret. Dvs., før du kan fakturere, skal der være registreret en leverance, eller du skal vælge at sende og fakturere på samme tid.

Du kan enten bogføre eller bogføre og sende. Hvis du vælger at bogføre og sende, genereres der en PDF-fil, som du derefter kan sende. Du kan også vælge funktionen **Massebogfør**, der giver mulighed for at bogføre flere ordrer samtidig. Du kan finde flere oplysninger i [Bogføre flere dokumenter på én gang](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Visning af finansposter

Når bogføringen er gennemført, fjernes de bogførte salgslinjer fra ordren. Der vises en meddelelse, når bogføringen er gennemført. Herefter kan du se de bogførte poster på forskellige sider, der indeholder bogførte poster, f.eks. **Debitorposter**, **Finansposter**, **Vareposter**, **Bogf. salgsleverancer** og **Bogf. salgsfakturaer**.  

I de fleste tilfælde kan du åbne finansposter fra det berørte kort eller dokument. Du kan f.eks. på siden **Debitorkort** vælge handlingen **Finansposter**.

## <a name="editing-ledger-entries"></a>Redigering af finansposter

Du kan redigere bestemte felter i bogførte købsdokumenter, f. eks **Pakkesporingsnr.** . Du kan finde flere oplysninger under [Redigere bogførte dokumenter](across-edit-posted-document.md). Er det mere kritiske felter, der påvirker overvågningssporet, skal du tilbageføre eller annullere bogføring. Du kan finde flere oplysninger i [Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Bogføre flere dokumenter på én gang](ui-batch-posting.md)  
[Redigere bogførte dokumenter](across-edit-posted-document.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Rette eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]