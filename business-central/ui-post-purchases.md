---
title: Om bogføring af købsdokumenter | Microsoft Docs
description: Lære mere om de forskellige bogføringsfunktioner til bogføring af købsdokumenter, og hvordan du kan opdatere bogførte dokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: fe7d9406f07eeadc0a6fb052556735eb7efeb815
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953175"
---
# <a name="posting-purchases"></a>Bogføring af køb
I **Prod.bogf.gruppe** på et købsdokument kan du vælge mellem følgende bogføringsfunktioner:

* **Bogfør**
* **Vis bogføring**
* **Bogfør og udskriv**
* **Testrapport**
* **Massebogfør**

Når du har udfyldt alle linjer og har indsat alle oplysninger i købsordren, kan du bogføre den, dvs. modtage og fakturere.

Når en købsordre bogføres, opdateres kreditorens konto, regnskabet og vareposterne.

For hver købsordre bliver der oprettet en købspost i tabellen **Finanspost**. Der oprettes også en post i kreditorkontoen i tabellen **Kreditorpost**, og der oprettes en finanspost i den relevante samlekonto. Desuden kan der eventuelt blive dannet en momspost og en finanspost med rabat. Om der bogføres en post med rabat, afhænger af oplysningerne i feltet **Bogføring med rabat** i tabellen **Købsopsætning**.

For hver købsordrelinje bliver der oprettet en varepost i tabellen **Varepost** (hvis købslinjerne indeholder varenumre) eller en finanspost i tabellen **Finanspost** (hvis der er indsat en finanskonto på købslinjerne). Købsordrer bliver desuden altid registreret i tabellerne **Købsleverancehoved** og **Købsfakturahoved**.

Inden du starter på selve bogføringen, kan du udskrive en kontrolrapport med alle oplysninger i købsordren og eventuelle fejl. Hvis du vil udskrive rapporten, skal du vælge **Bogføring** og derefter vælge **Kontrollér rapport**.

> [!IMPORTANT]  
>   Når du bogfører en ordre, har du mulighed for både at modtage og fakturere. Det kan gøres samtidigt eller hver for sig. Du kan også oprette en delkvittering og en delfaktura ved at udfylde felterne **Modtag (antal)** og **Fakturer (antal)** på de enkelte købsordrelinjer, før du bogfører. Bemærk, at du ikke kan oprette en faktura for noget, der ikke er modtaget. For at kunne fakturere er det altså nødvendigt, at du på forhånd har registreret en modtagelse, eller at du nu vælger at modtage og fakturere samtidigt.

Du kan enten bogføre eller bogføre og udskrive. Hvis du vælger at bogføre og udskrive, udskrives der en rapport, når ordren bogføres. Du kan også vælge funktionen **Massebogfør**, der giver mulighed for at bogføre flere ordrer samtidig. Du kan finde flere oplysninger i [Bogføre flere dokumenter på én gang](ui-batch-posting.md).

Når bogføringen er gennemført, fjernes de bogførte købslinjer fra ordren. Der vises en meddelelse, når bogføringen er gennemført. Herefter kan du se de bogførte poster på forskellige sider, der indeholder bogførte poster, f.eks. **Kreditorposter**, **Finansposter**, **Vareposter**, **Købsleverance** og **Bogf. købsfakturaer**.

Du kan redigere bestemte felter i bogførte købsdokumenter, f. eks feltet **Betalingsreference**. Du kan finde flere oplysninger under [Redigere bogførte dokumenter](across-edit-posted-document.md).

## <a name="see-related-training-at-microsoft-learnlearnmodulesreceive-invoice-dynamics-d365-business-centralindex"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Se også
[Redigere bogførte dokumenter](across-edit-posted-document.md)  
[Bogføre flere dokumenter på én gang](ui-batch-posting.md)  
[Køb](purchasing-manage-purchasing.md)  
[Bogføring af dokumenter og kladder](ui-post-documents-journals.md)  
[Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
