---
title: Bogføre salgsdokumenter
description: 'Lære mere om de forskellige bogføringsfunktioner til bogføring af salgsdokumenter, og hvordan du kan opdatere bogførte dokumenter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.reviewer: bholtorf
ms.search.form: '130, 142, 1350'
ms.date: 02/13/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="posting-sales"></a>Bogføre salg

I menuen **Bogføring** i et salgsdokument kan du vælge mellem følgende bogføringsfunktioner:

* **Bogfør**
* **Bogfør og ny**
* **Bogfør og send**
* **Vis bogføring**
* **Massebogfør**
* **Testrapport**

> [!NOTE]
> I forbindelse med salgsordrer kan du også se indstillinger, der vedrører forudbetalingsfunktionen. Du kan finde flere oplysninger i [Fakturere forudbetalinger](finance-invoice-prepayments.md).

Når du har udfyldt alle linjer og har indsat alle oplysninger i salgsordren, kan du bogføre den. Dette opretter en leverance og en faktura.

Når en salgsordre bogføres, opdateres kreditorens konto, regnskabet og vareposterne.

For hver salgsordre oprettes der en salgspost i tabellen **Finanspost**. Der oprettes også en post i debitorkontoen i tabellen **Debitorpost**, og der oprettes en finanspost i den relevante samlekonto. Desuden kan der eventuelt blive dannet en momspost og en finanspost for rabatbeløbet. Om der bogføres en post med rabat, afhænger af oplysningerne i feltet **Bogføring med rabat** på siden **Salgsopsætning**.

For hver salgsordrelinje oprettes der en varepost i tabellen **Varepost** (hvis salgslinjerne indeholder varenumre) eller en finanspost i tabellen **Finanspost** (hvis der er indsat en finanskonto på salgslinjerne). Salgsordrer bliver desuden altid registreret i tabellerne **Salgsleverancehoved** og **Salgsfakturahoved**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Du kan enten bogføre eller bogføre og sende. Hvis du vælger at bogføre og sende, genereres der en PDF-fil, som du derefter kan sende. Du kan også vælge funktionen **Massebogfør**, der giver mulighed for at bogføre flere ordrer samtidig. Du kan finde flere oplysninger i [Bogføre flere dokumenter på én gang](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Visning af finansposter

Når bogføringen er gennemført, fjernes de bogførte salgslinjer fra ordren. Der vises en meddelelse, når bogføringen er gennemført. Herefter kan du se de bogførte poster på forskellige sider, der indeholder bogførte poster, f.eks. **Debitorposter**, **Finansposter**, **Vareposter**, **Bogf. salgsleverancer** og **Bogf. salgsfakturaer**.  

I de fleste tilfælde kan du åbne finansposter fra det berørte kort eller dokument. Du kan f.eks. på siden **Debitorkort** vælge handlingen **Finansposter**.

## <a name="editing-ledger-entries"></a>Redigering af finansposter

Du kan redigere bestemte felter i bogførte købsdokumenter, f. eks **Pakkesporingsnr.** . Du kan finde flere oplysninger i [Redigere bogførte dokumenter](across-edit-posted-document.md). Er det mere kritiske felter, der påvirker overvågningssporet, skal du tilbageføre eller annullere bogføring. Du kan finde flere oplysninger i [Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md).

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Bogføre flere dokumenter på én gang](ui-batch-posting.md)  
[Udskrive bogførte dokumenter](across-edit-posted-document.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Rette eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
