---
title: "Fremgangsmåde: Behandle købsreturvarer eller annulleringer | Microsoft Docs"
description: "Fremgangsmåde: Behandle købsreturvarer eller annulleringer"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cancel, undo, correct
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f87b51ac746c6586e4ebb3b09aaa8d5ee7ac391d
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-process-purchase-returns-or-cancellations"></a>Fremgangsmåde: Behandle købsreturvarer eller annulleringer
Hvis du skal returnere varer til din kreditor eller annullere serviceydelser, som du har købt, kan du oprette og bogføre en købskreditnota, der angiver den ønskede ændring for den oprindelige købsfaktura. For at medtage de korrekte købsfakturaoplysninger kan du oprette købskreditnotaen fra den bogførte købsfaktura eller bruge funktionen Kopier.

**Bemærk**: Hvis en bogført købsfaktura endnu ikke er betalt, kan du bruge funktionen **Ret** eller **Annuller** på den bogførte købsfaktura, så du automatisk tilbagefører de pågældende transaktioner. Disse funktioner fungerer kun for ubetalte fakturaer, og de understøtter ikke delvise returneringer eller annulleringer. Du kan finde flere oplysninger under [Fremgangsmåde: Rette eller annullere ubetalte salgsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Du opretter typisk en købskreditnota som reaktion på en kreditnota, der er sendt til dig af en kreditor. Købskreditnotaen fungerer som din interne dokumentation i kreditnotaprocessen til regnskabsmæssigt formål.

Ændringen kan være relateret til alle produkterne på den oprindelige købsfaktura eller kun til nogle af produkterne. Tilsvarende kan du delvist returnere modtagne varer eller kræve delvis refusion af modtagne serviceydelser. I dette tilfælde skal du redigere de kopierede købsfakturaoplysninger.

Ud over den oprindelige bogførte købsfaktura kan du anvende købskreditnotaen på andre købsdokumenter, for eksempel en anden bogført købsfaktura, fordi du også returnerer varerne fra denne faktura.

## <a name="to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice"></a>Sådan oprettes en købskreditnota fra en bogført købsfaktura
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Købskreditnotaer** og derefter vælge det relaterede link.  
2. I vinduet **Bogf. købsfakturaer** skal du vælge den bogførte købsfaktura, der skal tilbageføres, og derefter vælge handlingen **Opret rettelseskreditnota**.

    De fleste felter i hovedet på købskreditnotaen er udfyldt med oplysninger fra den bogførte købsfaktura. Du kan redigere alle felterne f.eks med nye oplysninger, der afspejler returneringsaftalen.
3. Rediger oplysningerne på linjerne i overensstemmelse med aftalen, f.eks antallet varer, der er returneret, eller beløbet der skal refunderes.
4. Vælg handlingen **Udlign**.
5. I vinduet **Udlign kred.poster** skal du vælge linjen med det bogførte købsdokument, du vil udligne købskreditnotaen til, og vælg derefter handlingen **Udlignings-id**. Købskreditnotaens nummer indsættes i feltet **Udlignings-id**.
6. I feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne, hvis det er mindre end det oprindelige beløb.

    Nederst i vinduet **Udlign** kan du se det samlede beløb, der skal udlignes for at tilbageføre alle involverede poster, dvs. når værdien i feltet **Saldo** er nul.
7. Vælg knappen **OK**. Når du bogfører købskreditnotaen, bliver den anvendt på de angivne bogførte købsdokumenter.

    Når du har oprettet eller redigeret de ønskede købskreditnotalinjer, og anvendelse på enkelt eller flere er angivet, kan du fortsætte med at bogføre købskreditnotaen.
8. Vælg handlingen **Bogfør**.

De bogførte købsfakturaer, som du udligner kreditnotaen med, tilbageføres nu. Hvis du allerede har betalt den oprindelige faktura, skal leverandøren nu refundere betalingen til dig. Hvis kreditnotaen kun er for en del af produktet på den oprindelige faktura, kan du kun betale det resterende beløb på den originale købsfaktura for at lukke den.

Købskreditnotaen fjernes og erstattes med et nyt bilag i oversigten over bogførte købskreditnotaer.

## <a name="to-create-a-purchase-credit-memo-from-scratch"></a>Sådan oprettes en købskreditnota fra bunden
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Bogførte købsfakturaer** og derefter vælge det relaterede link.
2. Vælg handlingen **Ny** for at åbne en ny tom købskreditnota.
3. I feltet **Kreditor** skal du indtaste navnet på en eksisterende kreditor.
4. Vælg handlingen **Kopier linjer**.
5. I vinduet **Kopier købsdokument** skal du vælge **Bogført faktura** i feltet **Dokumenttype**.
6. Vælg feltet **Bilagsnr.** for at åbne vinduet **Bogf. købsfakturaer**, og vælg derefter den bogførte købsfaktura, der skal tilbageføres.
7. Marker afkrydsningsfeltet **Genberegn linjer**, hvis du vil opdatere de kopierede bogførte købsfakturalinjer med eventuelle ændringer i varepris og kostpris, siden fakturaen blev bogført.
8. Vælg knappen **OK**. De kopierede fakturalinjer skal indsættes i købskreditnotaen.
9. Udfyld købskreditnotaen, som beskrevet i afsnittet "Sådan oprettes en købskreditnota fra en bogført købsfaktura" i dette emne.

## <a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md)  
[Fremgangsmåde: Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

