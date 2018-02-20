---
title: Bruge automatisk udligning til at afstemme betalinger | Microsoft Docs
description: "Beskriver, hvordan du bruger den automatiske udligningsfunktion til at udligne betalinger eller indbetalinger til de relaterede åbne poster og afstemme betalinger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 79e7b23efb22f606351840ad613de9537fe30289
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="reconcile-payments-using-automatic-application"></a>Afstemme betalinger ved hjælp af automatisk udligning
Vinduet **Betalingsudligningskladde** angiver betalinger, enten indgående eller udgående, der er registreret som transaktioner på din onlinebankkonto, og som du kan udligne på deres relaterede åbne debitor-, kreditor- og bankkontoposter. Linjerne i kladden udfyldes ved at importere et bankkontoudtog som et bankfeed eller en fil.

En betalingsudligningskladde er relateret til en bankkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)], der afspejler den onlinebankkonto, hvor betalingstransaktionerne registreres. Eventuelle åbne bankposter vedrørende de udlignede debitor- eller kreditorposter bliver lukket, når du vælger handlingen **Bogfør betalinger og afstem bankkonti**. Det betyder, at bankkontoen automatisk afstemmes for de betalinger, du bogfører, med kladden.

Hvis du vil indlæse bankkontoudtog, som banken sender som feeds, skal du først aktivere tjenesten Envestnet Yodlee Bank Feeds og derefter knytter bankkontoen til den relaterede onlinebankkonto. Betalingsudligningskladden registrerer derefter automatisk bankfeeds, når du klikker på handlingen **Importér banktransaktioner**. Du kan desuden konfigurere en bankkonto til automatisk at indlæse nye feeds til bankkontoudtog hver time. Transaktioner for betalinger, der allerede er bogført som udlignet og/eller afstemt indlæses ikke. Du kan finde flere oplysninger under [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

Med handlingen **Knyt tekst til konto** kan du oprette tilknytninger mellem tekst på betalinger og specifikke debet-, kredit- og modkonti, så disse betalinger bliver bogført på de angivne konti, når du bogfører kladden til betalingsafstemning. Se trin 8. Du kan finde flere oplysninger under [Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

Der findes lignende funktioner til afstemning af overskydende beløb på betalingsudligningskladdelinjer på ad hoc-basis. Du kan finde flere oplysninger i [Afstemme betalinger, der ikke kan udlignes automatisk.](receivables-how-reconcile-payments-cannot-apply-auto.md)

Du kan bruge funktionen **Udlign automatisk** enten automatisk, når du importerer en bankfil eller -feed med betalingstransaktioner, eller når du aktiverer den for at udligne betalinger til deres relaterede åbne poster, der er baseret på en afstemning af data på en kladdelinje med data på en eller flere åbne poster.

På kladdelinjer, hvor betaling er udlignet automatisk til en eller flere åbne poster, har feltet **Matchtillid** en værdi mellem Lav og Høj for at angive kvaliteten af den dataafstemning, som den foreslåede betalingsudligning er baseret på. Derudover bliver felterne **Kontotype** og **Kontonr.** udfyldt med oplysninger om debitoren eller kreditoren, som betalingen udlignes for. Hvis du har oprettet en tekst-til-kontotilknytning, kan automatisk udligning resultere i værdien **Høj – tekst-til-kontotilknytning** som udligningstillid.

For hver kladdelinje i vinduet **Betalingsudligningskladde** kan du åbne vinduet **Betalingsudligning** for at få vist alle åbne kandidatposter for betalingen og se detaljerede oplysninger for hver post om den dataafstemning, som en betalingsudligning er baseret på. Her kan du manuelt udligne betalinger eller udligne betalinger igen, der er udlignet automatisk til en forkert post. Du kan finde flere oplysninger i [Gennemse eller udligne betalinger efter automatisk udligning](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
>   Du kan starte importen af banktransaktioner på samme tid, som du åbner vinduet **Betalingsudligningskladde** for en eksisterende betalingsafstemningskladde i vinduet **Betalingsafstemningskladder**. Følgende procedure beskriver, hvordan du importerer banktransaktioner i vinduet **Betalingsudligningskladde**, når du har oprettet en ny kladde.

## <a name="to-reconcile-payments-using-automatic-application"></a>Sådan afstemmer du betalinger ved hjælp af automatisk udligning
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsudbetalingskladder**, og vælg derefter det relaterede link.
2. Hvis du vil arbejde i en ny betalingsafstemningskladde, skal du vælge handlingen **Ny kladde**.
3. Brug vinduet **Betalingsbankkontooversigt** til at vælge den bankkonto, som du vil afstemme betalinger for, og vælg derefter knappen **OK**.
   Vinduet **Betalingsudligningskladde** åbnes forberedt til den valgte bankkonto.
4. Vælg handlingen **Importer banktransaktioner**.
   Hvis bankkontoen for den valgte kladde ikke er angivet for import af banktransaktioner, åbnes en dialogboks for at hjælpe dig med at udfylde de relevante felter.
5. Brug vinduet **Vælg den fil, der skal importeres** til at vælge den fil, der indeholder banktransaktioner for betalinger, der skal afstemmes, og vælg derefter knappen **Åbn**.  
6. Hvis tjenesten Bankkontoudtog er aktiveret, skal du i vinduet **Bankkontoudtogsfilter**, der åbnes automatisk, angive datointervallet for bankkontoudtog, der skal importeres.

    Vinduet **Betalingsudligningskladde** er fyldt med linjer for betalinger, der repræsenterer banktransaktioner i det importerede bankkontoudtog.

    På linjer, hvor betaling er udlignet automatisk til den relaterede åbne post, har feltet **Matchtillid** en værdi mellem **Lav** og **Høj** for at angive kvaliteten af den dataafstemning, som den foreslåede betalingsudligning er baseret på. Derudover bliver felterne **Kontotype** og **Kontonr.** udfyldt med oplysninger om debitoren eller kreditoren, som betalingen udlignes for.
7. Vælg en kladdelinje, og vælg derefter den **Udlign manuelt**-handling, der skal gennemgås, eller udlign betalingen manuelt i vinduet **Betalingsudligning**. Du kan finde flere oplysninger i [Gennemse eller udligne betalinger efter automatisk udligning](receivables-how-review-apply-payments-auto-application.md).

    Når du er færdig med manuel udligning, indeholder feltet **Matchtillid** på den kladdelinje, du har behandlet manuelt, **Accepteret**.
8. Vælg en ikke-udlignet kladdelinje for en tilbagevendende indbetaling eller en udgift, f.eks køb af benzin, og vælg derefter handlingen **Knyt tekst til konto**. Du kan finde flere oplysninger under [Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
9. Når du er færdig med at knytte betalingstekst til konti, skal du vælge handlingen **Udlign manuelt**.
10. Når du er sikker på, at alle betalinger på kladdelinjerne er korrekt udlignet eller indstillet til direkte bogføring, skal du vælge handlingen **Bogfør**.

Når du bogfører betalingsafstemningskladden, bliver de udlignede åbne poster lukket, og de relaterede debitor-, kreditor- eller finanskonti opdateres. De angivne debitor-, kreditor- og finanskonti opdateres for betalinger på kladdelinjer, der er baseret på tekst-til-kontotilknytning. For alle kladdelinjer oprettes bankposter. Hvis du vælger handlingen **Bogfør betalinger og afstem bankkonti**, bliver eventuelle åbne bankposter vedrører de udlignede debitor- eller kreditorposter lukket. Det betyder, at bankkontoen automatisk afstemmes for de betalinger, du bogfører, med kladden.

Du kan sammenligne værdien i feltet **Saldo på bankkonto efter bogføring** med værdien i feltet **Kontoudtogs slutsaldo** for at spore, hvornår bankkontoen er afstemt baseret på betalinger, du bogfører.

> [!NOTE]  
>   Hvis du ikke vil afstemme bankkontoen fra vinduet **Betalingsudligningskladde**, skal du bruge vinduet **Bankkontoafstemning**. Du kan finde flere oplysninger i [Afstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Se også
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

