---
title: Fortryde en postering ved at bogføre en tilbageføringspost | Microsoft Docs
description: Hvis du har oprettet en forkert bogføring i finanskladden, kan du bruge funktionen Tilbagefør transaktion til at fortryde bogføringen med et korrekt revisionsspor.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 01/27/2020
ms.author: sgroespe
ms.openlocfilehash: 0e38ec4c70fdbf81b29d96ad9db80cd7efdd2c82
ms.sourcegitcommit: 1c286468697d403b9e925186c2c05e724d612b88
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2020
ms.locfileid: "2999851"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Tilbageføre kladdeposteringer og annullere modtagelser/leverancer
Hvis du vil tilbageføre en fejlpostering i en kladde, skal du vælge posten og oprette en modpost (poster, der er identiske med den originale post, men med modsat fortegn i beløbsfeltet) med det samme bilagsnummer og den samme bogføringsdato som den oprindelige post. Når du har tilbageført en post, skal du oprette den korrekte post.

Du kan kun tilbageføre poster, der er bogført fra en finanskladdelinje. En post kan kun tilbageføres én gang.

Hvis du vil annullere bogføringen af en modtagelse eller leverance, før de bogføres som faktureret, kan du bruge funktionen **Fortryd** i det bogførte dokument. Du kan annullere antal af typen **Vare** og **Ressource**.

Hvis du har oprettet en bogføring af et forkert negativt antal, som f.eks. en købsordre med det forkerte antal varer og bogført dem som modtaget, men ikke faktureret, kan du annullere bogføringen.

Hvis du har oprettet en bogføring af et forkert positivt antal som f.eks. en salgsleverance eller købsreturvare med det forkerte antal varer og bogført dem som leveret, men ikke faktureret, kan du annullere bogføringen.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Sådan tilbageføres kladdepost på en finanspost
Du kan tilbageføre poster fra alle **Poster**-sider: Følgende procedure er baseret på siden **Finansposter**.
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finansposter**, og vælg derefter det relaterede link.
2. Marker den post, du vil tilbageføre, og vælg derefter handlingen **Tilbagefør transaktion**. Bemærk, at den skal stamme fra en kladdepost.
3. Vælg handlingen **Tilbagefør** på siden **Tilbagefør transaktionsposter**.
4. Vælg knappen **Ja** i bekræftelsesmeddelelsen.

> [!NOTE]
> Du kan ikke tilbageføre poster, der er bogført med oplysninger fra en sag, eller som har realiserede gevinster og tab inden for samme transaktion.

## <a name="to-post-a-negative-entry"></a>Sådan bogføres en negativ post  
Du kan bruge feltet **Rettelse** til at bogføre en negativ debet i stedet for kredit eller til at bogføre en negativ kredit i stedet for en debet på en konto. Dette felt kan ses som standard i alle kladder for at imødekomme lovgivningsmæssige krav. Felterne **Debetbeløb** og **Kreditbeløb** indeholdet både den oprindelige post og den rettede post. Disse felter har ingen indflydelse på kontosaldoen.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladder**, og vælg derefter det relaterede link  
2.  Vælg det krævede kladdenavn i feltet **Kladdenavn**.  
3.  Angiv oplysningerne i de relevante felter.  
4.  I den kladdelinje, som du vil aktivere for negative poster, skal du markere afkrydsningsfeltet **Rettelse**.  
5.  Hvis du vil postere kladden, skal du vælge handlingen **Bogfør** og derefter vælge knappen **Ja**.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Sådan fortrydes et bogført antal på en bogført købsmodtagelse  
Følgende beskriver, hvordan du kan fortryde en bogført modtagelse af vare eller ressourcer. Fremgangsmåden er tilsvarende for bogførte leverancer.

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte købsmodtagelser**, og vælg derefter det relaterede link.  
2.  Åbn den bogført modtagelse, du vil fortryde.  
3.  Vælg den eller de linjer, der skal fortrydes.  
4.  Vælg handlingen **Annuller modtagelse**.

Der indsættes en korrektionslinje under den valgte modtagelseslinje. Hvis mængden blev modtaget i en lagermodtagelse, indsættes der en korrektionslinje i den bogførte lagermodtagelse.  

Felterne **Modtaget (antal)** og **Modt. antal (ufakt.)** på den relaterede købsordre , der er angivet til nul.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Sådan fortryder du og derefter annullerer et bogført antal på en bogført returvareleverance
Følgende beskriver, hvordan du kan fortryde en bogført returvareleverance af varer eller ressourcer og derefter bogføre købsreturvaren igen med et nyt antal. Fremgangsmåden er tilsvarende for bogførte returvaremodtagelser.

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte returvareleverancer**, og vælg derefter det relaterede link.  
2.  Åbn den bogførte returvareleverance, du vil fortryde.
3. Vælg den eller de linjer, der skal fortrydes.  

4.  Vælg handlingen **Annuller returvareleverance**.  

    En rettelseslinje indsættes i det bogførte dokument, og felterne **Antal sendt retur** og **Afs. ret.vare - ikke fakt.** på returvareordren nulstilles.  

    Gå nu tilbage til købsreturvareordren for at annullere Fortryd bogføring.  

5.  Notér tallet i feltet **Returvareordrenr.** på siden **Bogført returvareleverance** .  
6.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsreturvareordrer**, og vælg derefter det relaterede link.  
7.  Åbn den pågældende returordre, og vælg derefter handlingen **Genåbn**.  
8.  Ret antallet i feltet **Antal**, og bogfør købsreturvareordren igen.  

## <a name="see-also"></a>Se også
[Fortryde bogføring af montage](assembly-how-to-undo-assembly-posting.md)  
[Bogføre transaktioner direkte i finansposterne](finance-how-post-transactions-directly.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
