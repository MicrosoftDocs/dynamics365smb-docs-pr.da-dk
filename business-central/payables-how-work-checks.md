---
title: Udstede, udskrive og annullere checks | Microsoft Docs
description: "Beskriver, hvordan du udsteder checks ved hjælp af udbetalingskladden, udskriver checks og annullerer eller får vist checkposter i Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 0c1b37616b4aafc9535f2d3fbf60b915c490dd0b
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-checks"></a>Arbejde med checks
Du kan udstede elektroniske og manuelle check [!INCLUDE[d365fin](includes/d365fin_md.md)]. Udbetalingskladden bruges i begge tilfælde, når der udstedes checks til leverandører/kreditorer. Du kan også annullere checks og se checkposter.

Under proceduren til udstedelse af checks foreslås der betalinger, der oprettes poster, og der udskrives computerchecks.

> [!NOTE]  
>   Du kan kontrollere, at din bank kun afregner validerede checks og beløb, ved at sende banken en fil, der indeholder kreditor- check- og betalingsoplysninger. Du kan finde flere oplysninger under [Eksportere en Positive Pay-fil](finance-how-positive-pay.md).

Printeren skal være konfigureret korrekt med checkformater, og du skal definere hvilket checklayout, der skal bruges. Du kan finde flere oplysninger under [Definere checklayouts](finance-how-define-check-layouts.md)

## <a name="to-issue-checks"></a>Sådan udsteder du checks
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. Udfyld kladden med relevante betalinger, f.eks. ved hjælp af funktionen Lav kreditorbetalingsforslag. Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).
3. I feltet **Bankbetalingstype** på kladdelinjer til betaling, du vil foretage med check, skal du vælge en af følgende indstillinger:

   * **Computercheck**: Vælg denne mulighed, hvis du vil udskrive en check på beløbet fra udbetalingskladdelinjen. Du skal udskrive checkene, før du kan bogføre kladdelinjerne. Du kan kun vælge **Computercheck**, hvis **Modkontotype** eller **Kontotype** er **Bankkonto**.
   * **Manuel check**: Vælg denne mulighed, hvis du har oprettet en check manuelt og vil oprette en tilsvarende checkpost på beløbet. Du kan ikke udskrive check fra [!INCLUDE[d365fin](includes/d365fin_md.md)] med denne indstilling. Du kan kun vælge **Manuel check**, hvis **Modkontotype** eller **Kontotype** er **Bankkonto**.

     > [!NOTE]  
     >   Du skal udskrive computerchecks, før du bogfører de relaterede kladdelinjer.
4. I tilfælde af computercheck skal du vælge **Udskriv check**.
5. I vinduet **Check** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Vælg knappen **Udskriv**.

> [!NOTE]  
>   Hvis du vil udskrive check i mere end én valuta fra forskellige bankkonti, skal du udføre kørslen **Udskriv check** separat for hver valuta og angive den korrekte bankkonto.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Sådan annulleres udskrevne checks, der ikke er blevet bogført
Du kan annullere ikke-bogførte checks, når de er blevet udskrevet, ved hjælp af handlingen **Annuller check** i vinduet **Udbetalingskladde**.

1. I vinduet **Udbetalingskladde** skal du vælge **Annuller Check**, og vælg derefter hvilke checks der skal annulleres.

## <a name="to-void-checks"></a>Sådan annulleres checks
Når checkbetalingen er blevet bogført, kan du kun annullere checks fra de resulterende bankposter.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Vælg den relevante bankkonto, vælg handlingen **Rediger**, og vælg derefter handlingen **Checkposter**.
3. I vinduet **Checkposter** skal du vælge handlingen **Annuller check**.
4. Markér afkrydsningsfeltet **Kun annulleringskontrol**.
5. Vælg knappen **OK**.

## <a name="see-also"></a>Se også
[Administrere skyldige beløb](payables-manage-payables.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Eksportere en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

