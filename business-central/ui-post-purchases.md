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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 78657265e45aa9eb01d56a65aab8366c24b3d39a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756738"
---
# <a name="posting-purchases"></a>Bogføring af køb
På et købsdokument kan du vælge mellem følgende bogføringshandlinger:

* **Bogfør**
* **Vis bogføring**
* **Bogfør og udskriv**
* **Testrapport**
* **Massebogfør**

Når et købsdokument bogføres, opdateres kreditorens konto, regnskabet og vareposterne, og ressourceposterne opdateres.

For hvert købsdokument oprettes der en købspost i tabellen **Finanspost**. Der oprettes også en post i kreditorkontoen i tabellen **Kreditorpost**, og der oprettes en finanspost i den relevante samlekonto. Desuden kan bogføring af købet medføre oprettelse af en moms- og en finanspost med rabat. Om der bogføres en post med rabat, afhænger af oplysningerne i feltet **Bogføring med rabat** i tabellen **Købsopsætning**.

For hver købslinje oprettes følgende poster:
- En post i tabellen **Varepost**, hvis købslinjen er af typen **Vare**.
- En post i tabellen **Finansport**, hvis købslinjerne er af typen **Finanskonto**
- En post i tabellen **Ressourcepost**, hvis købslinjen er af typen **Ressource**.

Købsdokumenter registreres desuden altid i tabellerne **Købsleverancehoved** og **Købsfakturahoved**.

Inden du starter på selve bogføringen, kan du udskrive en kontrolrapport med alle oplysninger i købsordren og eventuelle fejl. Hvis du vil udskrive rapporten, skal du vælge **Bogføring** og derefter vælge **Kontrollér rapport**.

> [!IMPORTANT]  
>   Når du bogfører en købsordre for varer, kan du både oprette en kvittering og en faktura. Det kan gøres samtidigt eller hver for sig. Du kan også oprette en delkvittering og en delfaktura ved at udfylde felterne **Modtag (antal)** og **Fakturer (antal)** på de enkelte købsordrelinjer, før du bogfører. Bemærk, at du ikke kan oprette en faktura for noget, der ikke er modtaget. For at kunne fakturere er det altså nødvendigt, at du på forhånd har registreret en modtagelse, eller at du nu vælger at modtage og fakturere samtidigt.

Du kan enten bogføre eller bogføre og udskrive. Hvis du vælger at bogføre og udskrive, udskrives der en rapport, når ordren bogføres. Du kan også vælge funktionen **Massebogfør**, der giver mulighed for at bogføre flere ordrer samtidig. Du kan finde flere oplysninger i [Bogføre flere dokumenter på én gang](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Visning af finansposter
Når bogføringen er gennemført, fjernes de bogførte købslinjer fra ordren. Der vises en meddelelse, når bogføringen er gennemført. Herefter kan du se de bogførte poster på forskellige sider, der indeholder bogførte poster, f.eks. **Kreditorposter**, **Finansposter**, **Vareposter**, **Ressourceposter til finans**, **Købsmodtagelser** og sider til Bogførte **købsfakturaer**.

I de fleste tilfælde kan du åbne finansposter fra det berørte kort eller dokument. Du kan f.eks. på siden **Kreditorkort** vælge handlingen **Poster**.

## <a name="editing-ledger-entries"></a>Redigering af finansposter
Du kan redigere bestemte felter i bogførte købsdokumenter, f. eks feltet **Betalingsreference**. Du kan finde flere oplysninger under [Redigere bogførte dokumenter](across-edit-posted-document.md). Er det mere kritiske felter, der påvirker overvågningssporet, skal du tilbageføre eller annullere bogføring. Du kan finde flere oplysninger i [Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Se også
[Redigere bogførte dokumenter](across-edit-posted-document.md)  
[Bogføre flere dokumenter på én gang](ui-batch-posting.md)  
[Køb](purchasing-manage-purchasing.md)  
[Bogføring af dokumenter og kladder](ui-post-documents-journals.md)  
[Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
