---
title: "Overføre bankbeløb | Microsoft Docs"
description: "Du kan overføre beløb fra én bankkonto til en anden, herunder forskellige valutaer, ved at bogføre transaktionen i finanskladden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 20661cce60bc9007adb9767388bf5af6f9c3acb9
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-transfer-bank-funds"></a>Fremgangsmåde: Overføre bankbeløb
Undertiden kan du have brug for at overføre et beløb fra én bankkonto til en anden. Hvis du vil gøre dette, skal du bogføre på en transaktion i finanskladden. Opgaven afhænger af, om bankkontiene bruger samme valuta eller forskellige valutaer.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Sådan bogføres overførsler mellem bankkonti med samme valutakode
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladde**, og vælg derefter det relaterede link.
2. Udfyld **Bogføringsdato** og **Bilagsnr.** på en kladdelinje. .
3. Klik på feltet **Kontotype**, og vælg **Bankkonto**.
4. I feltet **Kontonr.** skal du vælge den bank, du vil overføre beløbet fra.
5. Angiv det beløb, der skal overføres, i feltet **Beløb**.
6. I feltet **Modkontotype** skal du vælge **Bankkonto**.
7. I feltet **Modkonto** skal du vælge den bankkonto, du vil overføre beløbet til.
8. Bogfør journalen.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Sådan bogføres overførsler mellem bankkonti med forskellige valutakoder
Hvis du vil overføre beløb mellem bankkonti, der bruger forskellige valutaer, skal du bogføre to finanskladdelinjer.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladde**, og vælg derefter det relaterede link.
2. Opret to kladdelinjer, og udfyld **Bogføringsdato** og **Bilagsnr.** .
3. På den første kladdelinje skal du vælge **Bankkonto** i feltet **Type**.
4. I feltet **Kontonr.** skal du vælge den bankkonto, du vil overføre beløbet fra.
5. I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen. Angiv kreditbeløb med et minus-tegn. Angiv debetbeløb uden et minus-tegn.
6. I feltet **Modkontotype** skal du vælge **Bankkonto**.
7. I feltet **Modkonto** skal du vælge den bankkonto, du vil overføre beløbet til.
8. På den anden kladdelinje skal du vælge **Bankkonto** i feltet **Type**.
9. I feltet **Kontonr.** skal du vælge den bankkonto, du vil overføre beløbet til.
10. I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen. Angiv kreditbeløb med et minus-tegn. Angiv debetbeløb uden et minus-tegn.
11. I feltet **Modkontotype** skal du vælge **Bankkonto**.  
12. I feltet **Modkonto** skal du vælge den bankkonto, du vil overføre beløbet fra.

    > [!NOTE]  
>   Hvis den anvendte valutakurs i kladden er en anden en kursen i vinduet **Valutakurser**, skal du oprette en tredje linje til kurstab og -gevinster. Indtast **Finanskonto** i feltet **Kontotype**. Angiv finanskontonummeret for kurstab og -gevinster i feltet **Kontonummer** . Angiv kurstab eller -tab i feltet **Beløb** henholdsvis med og uden et minustegn foran kredit og debet.
13. Bogfør journalen.

## <a name="see-also"></a>Se også
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

