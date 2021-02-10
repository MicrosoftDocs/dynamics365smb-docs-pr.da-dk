---
title: Registrere udgifter eller indtægter direkte i Finans | Microsoft Docs
description: Du kan oprette relaterede transaktioner for aktiviteter, der ikke er repræsenteret af et dokument, f.eks. mindre udgifter eller indbetalinger, ved at bogføre kladdelinjer på siden Finanskladde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 72e2851ee60d6cb79f722d12e16ddcb30e95fdbe
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746937"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a>Bogføre transaktioner direkte i finansposterne

Du bruger finanskladder til at bogføre økonomiske transaktioner direkte på finanskonti og andre konti, f.eks. bank-, debitor-, kreditor- og medarbejderkonti.  

En typisk anvendelse af finanskladden er at bogføre medarbejdernes brug af egne penge under forretningsaktiviteter for senere refusion. Du kan finde flere oplysninger i [Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md).

Finanskladder bogfører finansposteringer direkte på finanskonti og andre konti, f.eks. bank-, debitor-, kreditor- og medarbejderkonti. Når du bogfører via en finanskonto, oprettes der altid poster i finanskonti. Det gælder også, når du bogfører f.eks. en kladdelinje på en debitorkonto, fordi der bogføres en post på en finanskonto for tilgodehavende via en bogføringsgruppe. Du kan tilpasse din version af en finanskladde ved at oprette et kladdenavn eller en skabelon. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).

I modsætning til poster, der bogføres med dokumenter, som kræver en kreditnotaproces, kan du korrekt tilbageføre poster, der bogføres i finanskladden. Du kan finde flere oplysninger i [Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Sådan bogføres en transaktion direkte på en finanspostkonto

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladder**, og vælg derefter det relaterede link.
2. Åbn det relevante finanskladdenavn. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).
3. Udfyld felterne efter behov på en ny kladdelinje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Gentag trin 3 for alle separate transaktioner, du vil bogføre.

    > [!TIP]  
    > Hvis du vil angive flere transaktionslinjer over én modkontolinje, f.eks. for én bankkonto, skal du markere afkrydsningsfeltet **Foreslå modkontobeløb** på linjen for kørslen på siden **Finanskladdenavne**. Feltet **Beløb** på modkontolinjen er forudfyldt automatisk med den værdi, der skal bruges til at afstemme posteringerne.
5. Vælg handlingen **Bogfør** for at registrere transaktionerne på de angivne konti i Finans.

## <a name="see-also"></a>Se også

[Arbejde med finanskladder](ui-work-general-journals.md)  
[Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md)  
[Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
