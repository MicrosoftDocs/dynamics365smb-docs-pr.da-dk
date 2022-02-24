---
title: Overføre bankbeløb | Microsoft Docs
description: Du kan overføre beløb fra én bankkonto til en anden, herunder forskellige valutaer, ved at bogføre transaktionen i finanskladden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: a21cabaf2f3edc9e8f1f261a9f9169c3cb611b61
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186208"
---
# <a name="transfer-bank-funds"></a>Overføre bankbeløb
Undertiden kan du have brug for at overføre et beløb fra én bankkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)] til en anden. Hvis du vil gøre dette, skal du bogføre på en transaktion på siden **Finanskladde**. Opgaven afhænger af, om bankkontiene bruger samme valuta eller forskellige valutaer.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Sådan bogføres overførsler mellem bankkonti med samme valutakode
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladde**, og vælg derefter det relaterede link.
2. Udfyld **Bogføringsdato** og **Bilagsnr.** på en kladdelinje.
3. Klik på feltet **Kontotype**, og vælg **Bankkonto**.
4. I feltet **Kontonr.** skal du vælge den bank, hvorfra du vil overføre beløbet.
5. Angiv det beløb, der skal overføres, i feltet **Beløb**.
6. Vælg handlingen **Vis flere kolonner** for at få vist alle tilgængelige felter.
7. I feltet **Modkontotype** skal du vælge **Bankkonto**.
8. I feltet **Modkontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.
9. Bogfør journalen.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Sådan bogføres overførsler mellem bankkonti med forskellige valutakoder
Hvis du vil overføre beløb mellem bankkonti, der bruger forskellige valutaer, skal du bogføre to finanskladdelinjer.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **FFinanskladde**, og vælg derefter det relaterede link.
2. Opret to kladdelinjer, og udfyld felterne **Bogføringsdato** og **Bilagsnr.**
3. På den første kladdelinje skal du vælge **Bankkonto** i feltet **Type**.
4. I feltet **Kontonr.** skal du vælge den bankkonto, hvorfra du vil overføre beløbet.
5. I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen. Angiv kreditbeløb med et minus-tegn. Angiv debetbeløb uden et minus-tegn.
6. I feltet **Modkontotype** skal du vælge **Bankkonto**.
7. I feltet **Modkontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.
8. På den anden kladdelinje skal du vælge **Bankkonto** i feltet **Type**.
9. I feltet **Kontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.
10. I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen. Angiv kreditbeløb med et minus-tegn. Angiv debetbeløb uden et minus-tegn.
11. I feltet **Modkontotype** skal du vælge **Bankkonto**.  
12. I feltet **Modkontonr.** skal du vælge den bankkonto, hvorfra du vil overføre beløbet.

    > [!NOTE]  
    > Hvis den anvendte valutakurs i kladden er en anden en kursen på siden **Valutakurser**, skal du oprette en tredje linje til kurstab og -gevinster. Indtast **Finanskonto** i feltet **Kontotype**. Angiv finanskontonummeret for kurstab og -gevinster i feltet **Kontonummer**. Angiv kurstab eller -tab i feltet **Beløb** henholdsvis med og uden et minustegn foran kredit og debet.
13. Bogfør journalen.

## <a name="see-also"></a>Se også
[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
