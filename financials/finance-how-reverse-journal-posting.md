---
title: "Fortryde en kladdepostering ved at bogføre en tilbageføringspost | Microsoft Docs"
description: "Hvis du har oprettet en forkert bogføring i finanskladden, kan du bruge funktionen Tilbagefør transaktion til at fortryde bogføringen med et korrekt revisionsspor."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-reverse-journal-posting"></a>Sådan tilbageføres en kladdepost
Hvis du vil tilbageføre en fejlpostering i en kladde, skal du vælge posten og oprette en modpost (poster, der er identiske med den originale post, men med modsat fortegn i beløbsfeltet) med det samme bilagsnummer og den samme bogføringsdato som den oprindelige post. Når du har tilbageført en post, skal du oprette den korrekte post.

Du kan kun tilbageføre poster, der er bogført fra en finanskladdelinje. En post kan kun tilbageføres én gang.

Du kan finde flere oplysninger om bogføring fra en finanskladde i [Fremgangsmåde: Bogfør transaktioner direkte i finansposter](finance-how-post-transactions-directly.md).

Du kan tilbageføre poster fra alle **Poster**-vinduer: Følgende procedure er baseret på vinduet **Finansposter**.

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Sådan tilbageføres kladdepost på en finanspost
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finansposter**, og vælg derefter det relaterede link.
2. Marker den post, du vil tilbageføre, og vælg derefter handlingen **Tilbagefør transaktion**. Bemærk, at den skal stamme fra en kladdepost.
3. I vinduet **Tilbagefør transaktionsposter** skal du vælge den relevante post og derefter vælge handlingen **Tilbagefør**.
4. Vælg knappen **Ja** i bekræftelsesmeddelelsen.

## <a name="see-also"></a>Se også
[Fremgangsmåde: Bogføre transaktioner direkte i finansposterne](finance-how-post-transactions-directly.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

