---
title: Administrere Kreditor | Microsoft Docs
description: "Oversigt over, hvordan du administrerer kreditorer (Kreditor), herunder kreditorbetalinger, kreditorerne, gæld og forfalden saldo."
services: project-madeira
documentationcenter: 
author: bholtorf
manager: edupont
editor: 
ms.service: dynamics365-business-central
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2018
ms.author: bholtorf
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 1682db5bd62f980e8789613cd2ca4169f98e839d
ms.contentlocale: da-dk
ms.lasthandoff: 06/01/2018

---
# <a name="managing-payables"></a>Administrere skyldige beløb
[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder det, du behøver for effektivt at administrere kreditorer.  

## <a name="payments"></a>Udbetaling kladde
Det er nemt at prioritere betalinger, tage højde for strafgebyrer for forfaldne betalinger og håndtere kontantrabatter for førtidige betalinger.

Du kan registrere betalinger i en finanskladde og derefter udskrive checks, inden du bogfører udbetalingskladden.

Du kan udligne betalinger for at lukke fakturaer, når du bogfører betalingen, eller efter du har bogført betalingen. Feltet **Udligningsmetode**, som er angivet for kreditoren (på **Kreditorkort**), er bestemmende for, om du skal foretage betalingen manuelt, eller om det sker automatisk. Du kan altid udligne transaktioner manuelt. Men hvis udligningsmetoden for kreditor er **Saldo**, og du ikke angiver et dokument som betalingen skal udlignes til, bliver betalingen udlignet til den ældste åbne post for kreditoren.

## <a name="suggest-vendor-payments"></a>Lav forslag
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan foreslå forskellige betalinger til kreditorer. Det kan f.eks. være betalinger, som snart forfalder, eller som omfatter rabat. Betalingsforslaget kan tage et beløb i betragtning, som du angiver som tilgængelige midler til betaling og berettigelse af kontantrabat.

## <a name="issue-checks"></a>Udstede checks
I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du udstede checks til kreditorer manuelt og elektronisk. Du kan gøre begge dele i vinduet **Udbetalingskladder**, hvor du kan også annullere checks og se checkposter.

## <a name="export-payments-to-a-bank-file"></a>Eksportere betalinger til en bankfil
Når du er klar til at betale en kreditor fra vinduet **Udbetalingskladde**, kan du eksportere en fil med betalingsoplysningerne fra kladdelinjerne. Derefter kan du overføre filen til din elektroniske bank for at behandle pengeoverførslerne.

Hvis du ikke vil bogføre en betalingskladdelinje for en eksporteret betaling, for eksempel fordi du venter på, at banken skal bekræfte transaktionen, kan du bare slette kladdelinjen. Senere, når du opretter en betalingskladdelinje for at betale det resterende beløb på fakturaen, kan du i feltet **Samlet eksporteret beløb** se, hvor meget af betalingsbeløbet der allerede er blevet eksporteret. Du kan også finde detaljerede oplysninger om den eksporterede total ved at vælge knappen **Poster i kreditoverførselsjournal**.

Hvis du venter med at bogføre betalinger, til banken har bekræftet, at den har behandlet transaktionerne, er der to måder, du kan bruge for at undgå at komme til at eksportere betalinger af åbne dokumenter igen ved et uheld:  

* I en betalingskladde med foreslåede betalingslinjer skal du sortere på kolonnen **Eksporteret til betalingsfil** eller kolonnen **Samlet eksporteret beløb** og derefter slette betalingsforslag for åbne fakturaer for betalinger, der allerede er foretaget, og du ikke vil foretage betalinger af.

    **Bemærk** Det være nødvendigt at føje kolonnerne til listen. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).  
* Du kan også i batchjobbet **Lav kreditorbetalingsforslag**, hvor du angiver, hvilke betalinger der indsættes i betalingskladden, angive, at der ikke skal indsættes kladdelinjer for betalinger, der allerede er eksporteret, ved at markere afkrydsningsfeltet **Spring over eksporterede betalinger**.

## <a name="see-also"></a>Se også
[Betalingsformer](finance-payment-methods.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

