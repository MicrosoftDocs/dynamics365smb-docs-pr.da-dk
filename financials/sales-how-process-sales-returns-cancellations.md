---
title: "Fremgangsmåde: Behandle salgsreturvarer eller annulleringer | Microsoft Docs"
description: "Fremgangsmåde: Behandle salgsreturvarer eller annulleringer"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: cf471e0c3a13a954ab7604a8b1d0f715f664722d
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-process-sales-returns-or-cancellations"></a>Fremgangsmåde: Behandle salgsreturvarer eller annulleringer
Hvis en debitor ønsker at returnere eller få refunderet varer eller serviceydelser, som du har solgt og modtaget betaling for, skal du oprette og bogføre en salgskreditnota, der angiver den ønskede ændring. For at medtage de korrekte salgsfakturaoplysninger kan du oprette salgskreditnotaen fra den bogførte salgsfaktura eller bruge funktionen Kopier.  

**Bemærk!** Hvis en bogført salgsfaktura endnu ikke er betalt, kan du bruge funktionen **Ret** eller **Annuller** på den bogførte salgsfaktura, så du tilbagefører transaktionerne. Disse funktioner fungerer kun for ubetalte fakturaer, og de understøtter ikke delvise returneringer eller annulleringer. Du kan finde flere oplysninger under [Fremgangsmåde: Rette eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md).

Ud over den oprindelige bogførte salgsfaktura kan du anvende salgskreditnotaen på andre salgsdokumenter, for eksempel en anden bogført salgsfaktura, fordi kunden også returnerer varerne fra denne faktura.

En returnering eller refusion kan vedrøre nogle af varerne eller tjenesteydelserne på den oprindelige salgsfaktura. Det er tilfældet skal du redigere oplysningerne på linjerne i salgskreditnotaen. Når du bogfører salgskreditnotaen, tilbageføres de salgsdokumenter, der berøres af ændringen, og der kan oprettes en refusionsbetaling til debitoren.  

Du kan sende den bogførte salgskreditnota til debitoren for at bekræfte returneringen eller annulleringen og kommunikere, at den tilhørende værdi vil blive refunderet, f.eks. når varerne returneres.  

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Sådan oprettes en salgskreditnota fra en bogført salgsfaktura
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Bogførte salgsfakturaer** og derefter vælge det relaterede link.  
2. I vinduet **Bogf. salgsfakturaer** skal du vælge den bogførte salgsfaktura, der skal tilbageføres, og derefter vælge handlingen **Opret rettelseskreditnota**.

    Salgskreditnotahovedet indeholder nogle oplysninger fra den bogførte salgsfaktura. Du kan redigere disse oplysninger f.eks med nye oplysninger, der afspejler returneringsaftalen.  
3. Rediger oplysningerne på linjerne i overensstemmelse med aftalen, f.eks antallet af returnerede varer eller beløbet, der skal refunderes.
4. Vælg handlingen **Udlign**.
5. I vinduet **Udlign debitorposter** skal du vælge linjen med det bogførte salgsdokument, du vil udligne salgskreditnotaen til, og vælg derefter handlingen **Udlignings-id**.

    Salgskreditnotaens id vises i feltet **Udlignings-id**.
6. I feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne, hvis det er mindre end det oprindelige beløb.  

    Nederst i vinduet **Udlign debitorposter** kan du se det samlede beløb, der skal udlignes for at tilbageføre alle involverede poster, dvs. når værdien i feltet **Saldo** er nul.
7. Vælg knappen **OK**. Når du bogfører salgskreditnotaen, bliver den udlignet til de bogførte salgsdokumenter.

    Når du har oprettet eller redigeret de ønskede salgskreditnotalinjer, og anvendelse på enkelt eller flere er angivet, kan du bogføre salgskreditnotaen.   
8. Vælg handlingen **Bogfør og send**.  

Dialogboksen **Bekræftelse af bogfør og send** åbnes og viser den foretrukne afsendelsesmetode til kunden. Du kan ændre afsendelsesmetoden ved at vælge opslagsknappen for feltet **Send bilag til**. Du kan finde flere oplysninger under [Fremgangsmåde: Konfigurerer dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).  

De bogførte salgsdokumenter, som du tilknytter kreditnotaen, tilbageføres nu, og der kan oprettes en refusionsbetaling til debitoren. Salgskreditnotaen fjernes og erstattes med et nyt bilag i oversigten over bogførte salgskreditnotaer.

## <a name="to-create-a-sales-credit-memo-from-scratch"></a>Sådan oprettes en salgskreditnota fra bunden
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Bogførte salgsfakturaer** og derefter vælge det relaterede link.
2. Vælg handlingen **Ny** for at åbne en ny tom salgskreditnota.
3. I feltet **Debitor** skal du indtaste navnet på en eksisterende debitor.
4. Vælg handlingen **Kopier linjer**.
5. I vinduet **Kopier salgsdokument** skal du vælge **Bogført faktura** i feltet **Dokumenttype**.
6. Vælg feltet **Bilagsnr.** for at åbne vinduet **Bogf. salgsfakturaer**, og vælg derefter den bogførte salgsfaktura, der skal tilbageføres.
7. Marker afkrydsningsfeltet **Genberegn linjer**, hvis du vil opdatere de kopierede bogførte salgsfakturalinjer med eventuelle ændringer i varepris og kostpris, siden fakturaen blev bogført.
8. Vælg knappen **OK**. De kopierede fakturalinjer skal indsættes i salgskreditnotaen.
9. Udfyld salgskreditnotaen, som beskrevet i afsnittet "Sådan oprettes en salgskreditnota fra en bogført salgsfaktura" i dette emne.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Fremgangsmåde: Sende dokumenter via mail](ui-how-send-documents-email.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

