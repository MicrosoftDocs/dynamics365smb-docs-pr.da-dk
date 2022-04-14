---
title: Overføre bankbeløb
description: Du kan overføre beløb fra én bankkonto til en anden, herunder forskellige valutaer, ved at bogføre transaktionen i finanskladden.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.search.form: 39
ms.date: 04/29/2021
ms.author: edupont
ms.openlocfilehash: 632f802678de33e7c00fa95dab38530a1364ff3b
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511723"
---
# <a name="transfer-bank-funds"></a>Overføre bankbeløb

Undertiden kan du have brug for at overføre et beløb fra én bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] til en anden. Hvis du vil gøre dette, skal du bogføre på en transaktion på siden **Finanskladde**. Opgaven afhænger af, om bankkontiene bruger samme valuta eller forskellige valutaer.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Sådan bogføres overførsler mellem bankkonti med samme valutakode

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Finanskladde**, og vælg derefter det relaterede link.
2. Udfyld **Bogføringsdato** og **Bilagsnr.** på en kladdelinje.
3. Klik på feltet **Kontotype**, og vælg **Bankkonto**.
4. I feltet **Kontonr.** skal du vælge den bank, hvorfra du vil overføre beløbet.
5. Angiv det beløb, der skal overføres, i feltet **Beløb**.

    Derefter skal du angive modkontoen. Hvis du ikke kan se de relevante felter, skal du vælge handlingen **Vis flere kolonner** for at få vist alle tilgængelige felter.
6. I feltet **Modkontotype** skal du vælge **Bankkonto**.
7. I feltet **Modkontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.
8. Bogfør journalen.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Sådan bogføres overførsler mellem bankkonti med forskellige valutakoder

Hvis du vil overføre beløb mellem bankkonti, der bruger forskellige valutaer, skal du bogføre to finanskladdelinjer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Finanskladde**, og vælg derefter det relaterede link.
2. Opret to kladdelinjer, og udfyld felterne **Bogføringsdato** og **Bilagsnr.**
3. På den første kladdelinje skal du vælge **Bankkonto** i feltet **Type**.
4. I feltet **Kontonr.** skal du vælge den bankkonto, hvorfra du vil overføre beløbet.
5. I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen med eller uden et minustegn.

    > [!TIP]
    > Et beløb uden fortegn er debet, og et beløb med et minustegn er kredit.

    > [!NOTE]
    > Nogle virksomheder foretrækker at overføre konti på separate kladdelinjer. Andre virksomheder foretrækker at bogføre alt på én kladdelinje vha. en modkonto. Kontakt din lokale ekspert, hvis du ikke er sikker på, hvad du skal gøre.
    >
    > Hvis virksomheden foretrækker at bruge en modkonto, skal du angive feltet **Modkontotype** til **Bankkonto** og derefter sætte feltet **Modkonto** til den bankkonto, som du vil overføre fondene til. Gå derefter til trin 9 eller 10.
    >
    > Hvis din virksomhed foretrækker at bruge en separat kladdelinje, skal du gå videre til næste trin.
6. På den anden kladdelinje skal du vælge **Bankkonto** i feltet **Type**.
7. I feltet **Kontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.
8. I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen med eller uden et minustegn.

    > [!TIP]
    > Et beløb uden fortegn er debet, og et beløb med et minustegn er kredit.
9. Hvis den anvendte valutakurs i kladden er en anden en kursen på siden **Valutakurser**, skal du oprette en ny linje til kurstab og -gevinster.  

    1. Indtast **Finanskonto** i feltet **Kontotype**.  

    2. Angiv finanskontonummeret for kurstab og -gevinster i feltet **Kontonummer**.  

    3. Angiv kurstab eller-gevinst i feltet **Beløb** med eller uden et minustegn.

    > [!TIP]
    > Et beløb uden fortegn er debet, og et beløb med et minustegn er kredit.
10. Bogfør journalen.

## <a name="see-also"></a>Se også

[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]