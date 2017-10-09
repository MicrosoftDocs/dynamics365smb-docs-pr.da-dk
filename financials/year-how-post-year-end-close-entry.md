---
title: "Gennemse og bogføre årsafslutningsposten | Microsoft Docs"
description: "Beskriver, hvordan du åbner den kladde, du angav i kørslen Nulstil resultatopgørelse, og derefter gennemser og bogfører årsafslutningsposten."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 68017b8b031ee4bd368936b6fb4de157328d7030
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-the-year-end-closing-entry"></a>Fremgangsmåde: Bogføre årsafslutningsposten
Når du har udført kørslen **Nulstil resultatopgørelse** for at oprette årsafslutningens lukkepost eller -poster, skal du åbne den kladde, du angav i kørslen, og derefter gennemse og bogføre posterne.

## <a name="to-post-the-year-end-closing-entry"></a>Sådan bogføre årsafslutningsposten
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladde**, og vælg derefter det relaterede link.
2. I vinduet **Kassekladde** skal du i feltet **Kladdenavn** vælge den kørsel, der indeholder lukkeposterne.
3. Gennemse posterne.
4. Vælg handlingen **Bogfør** for at bogføre kladden.

> [!NOTE]  
>   Hvis der opstår en fejl, vises der en fejlmeddelelse. Hvis bogføringen lykkes, fjernes de bogførte poster fra kladden. Når bogføringen er fuldført, bogføres en post til alle resultatopgørelseskonti, så saldoen går i nul, og årsresultatet overføres til balancen.

## <a name="see-also"></a>Se også
[Fremgangsmåde: Afslutte regnskabsperioder](year-close-account-periods.md)  
[Afslutningregnskab](year-close-books.md)  
[Nulstil resultatopgørelse](year-close-income-statement.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

