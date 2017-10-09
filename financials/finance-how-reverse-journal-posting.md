---
title: "Fortryde en postering ved at bogføre en tilbageføringspost | Microsoft Docs"
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
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 802171d4f421270cb7e9b4f9dfedec9b9fe5ddc6
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reverse-postings"></a>Sådan tilbageføres poster
Hvis du vil tilbageføre en fejlpostering i en kladde, skal du vælge posten og oprette en modpost (poster, der er identiske med den originale post, men med modsat fortegn i beløbsfeltet) med det samme bilagsnummer og den samme bogføringsdato som den oprindelige post. Når du har tilbageført en post, skal du oprette den korrekte post.

Du kan kun tilbageføre poster, der er bogført fra en finanskladdelinje. En post kan kun tilbageføres én gang.

Du kan finde flere oplysninger om bogføring fra en finanskladde i [Fremgangsmåde: Bogfør transaktioner direkte i finansposter](finance-how-post-transactions-directly.md).

Hvis du har oprettet en bogføring af et forkert negativt antal, som f.eks. en købsordre med det forkerte antal varer og bogført dem som modtaget, men ikke faktureret, kan du annullere bogføringen.

Hvis du har oprettet en bogføring af et forkert positivt antal, som f.eks. en købsreturvareordre med det forkerte antal varer og bogført dem som leveret, men ikke faktureret, kan du annullere bogføringen.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Sådan tilbageføres kladdepost på en finanspost
Du kan tilbageføre poster fra alle **Poster**-vinduer: Følgende procedure er baseret på vinduet **Finansposter**.
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finansposter**, og vælg derefter det relaterede link.
2. Marker den post, du vil tilbageføre, og vælg derefter handlingen **Tilbagefør transaktion**. Bemærk, at den skal stamme fra en kladdepost.
3. I vinduet **Tilbagefør transaktionsposter** skal du vælge den relevante post og derefter vælge handlingen **Tilbagefør**.
4. Vælg knappen **Ja** i bekræftelsesmeddelelsen.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Sådan fortrydes et bogført antal på en bogført købsmodtagelse  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogførte købsmodtagelser**, og vælg derefter det relaterede link.  
2.  Åbn den bogført modtagelse, du vil fortryde.  
3.  Vælg den eller de linjer, der skal fortrydes.  
4.  Vælg handlingen **Annuller modtagelse**.

    Der indsættes en korrektionslinje under den valgte modtagelseslinje.  

    Hvis mængden blev modtaget i en lagermodtagelse, indsættes der en korrektionslinje i den bogførte lagermodtagelse.  

    Felterne **Modtaget (antal)** og **Modt. antal (ufakt.)** på den relaterede købsordre , der er angivet til nul.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Sådan fortryder du og derefter annullerer et bogført antal på en bogført returvareleverance

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogførte købsmodtagelser**, og vælg derefter det relaterede link.  
2.  Åbn den bogførte returvareleverance, du vil fortryde.
3. Vælg den eller de linjer, der skal fortrydes.  

4.  Vælg handlingen **Annuller returvareleverance**.  

    En rettelseslinje indsættes i det bogførte dokument, og felterne **Antal sendt retur** og **Afs. ret.vare - ikke fakt.** på returvareordren nulstilles.  

    Gå nu tilbage til købsreturvareordren for at annullere Fortryd bogføring.  

5.  Notér tallet i feltet **Returvareordrenr.** i vinduet **Bogført returvareleverance** .  
6.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsreturvareordrer**, og vælg derefter det relaterede link.  
7.  Åbn den pågældende returordre, og vælg derefter handlingen **Genåbn**.  
8.  Ret antallet i feltet **Antal**, og bogfør købsreturvareordren igen.  

## <a name="see-also"></a>Se også
[Fremgangsmåde: Bogføre transaktioner direkte i finansposterne](finance-how-post-transactions-directly.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

