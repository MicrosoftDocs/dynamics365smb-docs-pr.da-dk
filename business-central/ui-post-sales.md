---
title: "Om bogføring af salgsdokumenter | Microsoft Docs"
description: "Få mere at vide om de forskellige bogføringsfunktioner, der bruges til at bogføre salgsdokumenter."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7ada688f7946d7f857dc6d4a6518b8bcb4e5c707
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="posting-sales"></a>Bogføring af salg
I **Prod.bogf.gruppe** på et salgsdokument kan du vælge mellem følgende bogføringsfunktioner:

* **Bogfør**
* **Testrapport**
* **Bogfør og send**
* **Bogfør og udskriv**
* **Bogfør og mail**
* **Massebogfør**
* **Vis bogføring**

Når du har udfyldt alle linjer og har indsat alle oplysninger i salgsordren, kan du bogføre den. Dette opretter en leverance og en faktura.

Når en salgsordre bogføres, opdateres kreditorens konto, regnskabet og vareposterne.

For hver salgsordre oprettes der en salgspost i tabellen **Finanspost**. Der oprettes også en post i debitorkontoen i tabellen **Debitorpost**, og der oprettes en finanspost i den relevante samlekonto. Desuden kan der eventuelt blive dannet en momspost og en finanspost for rabatbeløbet. Om der bogføres en post med rabat, afhænger af oplysningerne i feltet **Bogføring med rabat** på siden **Salgsopsætning**.

For hver salgsordrelinje oprettes der en varepost i tabellen **Varepost** (hvis salgslinjerne indeholder varenumre) eller en finanspost i tabellen **Finanspost** (hvis der er indsat en finanskonto på salgslinjerne). Salgsordrer bliver desuden altid registreret i tabellerne **Salgsleverancehoved** og **Salgsfakturahoved**.

> [!IMPORTANT]  
>   Når du bogfører en ordre, har du mulighed for både at oprette en leverance og en faktura. Det kan gøres på samme tid eller hver for sig. Du kan også oprette en delleverance og en delfaktura ved at udfylde felterne **Lever (antal)** og **Fakturer (antal)** på de enkelte salgsordrelinjer, før du bogfører. Bemærk, at du ikke kan oprette en faktura for noget, der ikke er leveret. Dvs., før du kan fakturere, skal der være registreret en leverance, eller du skal vælge at sende og fakturere på samme tid.

Når bogføringen er gennemført, fjernes de bogførte salgslinjer fra ordren. Der vises en meddelelse, når bogføringen er gennemført. Herefter kan du se de bogførte poster på forskellige sider, der indeholder bogførte poster, f.eks. **Debitorposter**, **Finansposter**, **Vareposter**, **Bogf. salgsleverancer** og **Bogf. salgsfakturaer**.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


