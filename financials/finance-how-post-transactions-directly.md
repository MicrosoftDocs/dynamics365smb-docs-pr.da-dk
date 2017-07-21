---
title: "Registrere udgifter eller indtægter direkte i Finans | Microsoft Docs"
description: "Du kan oprette relaterede transaktioner for aktiviteter, der ikke er repræsenteret af et dokument, f.eks. mindre udgifter eller indbetalinger, ved at bogføre kladdelinjer i vinduet Finanskladde."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7fa0d6b604a60e000208287546d831690a914931
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-post-transactions-directly-to-the-general-ledger"></a>Fremgangsmåde: Bogføre transaktioner direkte i finansposterne
De fleste finansposteringer bogføres i finansregnskabet ved hjælp af dedikerede forretningsdokumenter, f.eks. købsfakturaer og salgsordrer. Du kan oprette relaterede transaktioner for aktiviteter, der ikke er repræsenteret af et dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. mindre udgifter eller indbetalinger, ved at bogføre kladdelinjer i vinduet **Finanskladde**.

Finanskladder bogfører finansposteringer direkte på finanskonti og andre konti, f.eks. bank-, debitor- og kreditorkonti. Når du bogfører via en finanskonto, oprettes der altid poster i finanskonti. Det gælder også, når du bogfører f.eks. en kladdelinje på en debitorkonto, fordi der bogføres en post på en finanskonto for tilgodehavende via en bogføringsgruppe. Du kan tilpasse din version af en finanskladde ved at oprette et kladdenavn eller en skabelon. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).

I modsætning til poster, der bogføres med dokumenter, som kræver en kreditnotaproces, kan du korrekt tilbageføre poster, der bogføres i finanskladden. Du kan finde flere oplysninger i [Sådan tilbageføres en kladdepost](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Sådan bogføres en transaktion direkte på en finanspostkonto
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladder**, og vælg derefter det relaterede link.
2. Åbn det relevante finanskladdenavn. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).
3. Udfyld felterne efter behov på en ny kladdelinje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Gentag trin 3 for alle separate transaktioner, du vil bogføre.

    > [!TIP]  
    > Hvis du vil angive flere transaktionslinjer over én modkontolinje, f.eks. for én bankkonto, skal du markere afkrydsningsfeltet **Foreslå modkontobeløb** på linjen for kørslen i vinduet **Finanskladdenavne**. Feltet **Beløb** på modkontolinjen er forudfyldt automatisk med den værdi, der skal bruges til at afstemme posteringerne.
5. Vælg handlingen **Bogfør** for at registrere transaktionerne på de angivne konti i Finans.

## <a name="see-also"></a>Se også
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Sådan tilbageføres en kladdepost](finance-how-reverse-journal-posting.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

