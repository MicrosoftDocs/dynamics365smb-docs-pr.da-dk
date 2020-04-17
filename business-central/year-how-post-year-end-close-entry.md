---
title: Gennemse og bogføre årsafslutningsposten | Microsoft Docs
description: Beskriver, hvordan du åbner den kladde, du angav i kørslen Nulstil resultatopgørelse, og derefter gennemser og bogfører årsafslutningsposten.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1fa624ecda5914c0ba4e395025f051bc5d8cc457
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191730"
---
# <a name="post-the-year-end-closing-entry"></a>Bogføre årsafslutningsposten
Når du har udført kørslen **Nulstil resultatopgørelse** for at oprette årsafslutningens lukkepost eller -poster, skal du åbne den kladde, du angav i kørslen, og derefter gennemse og bogføre posterne.

## <a name="to-post-the-year-end-closing-entry"></a>Sådan bogføre årsafslutningsposten
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladde**, og vælg derefter det relaterede link.
2. På siden **Kassekladde** skal du i feltet **Kladdenavn** vælge den kørsel, der indeholder lukkeposterne.
3. Gennemse posterne.
4. Vælg handlingen **Bogfør** for at bogføre kladden.

> [!NOTE]  
>   Hvis der opstår en fejl, vises der en fejlmeddelelse. Hvis bogføringen lykkes, fjernes de bogførte poster fra kladden. Når bogføringen er fuldført, bogføres en post til alle resultatopgørelseskonti, så saldoen går i nul, og årsresultatet overføres til balancen.

## <a name="see-also"></a>Se også
[Afslutte regnskabsperioder](year-close-account-periods.md)  
[Afslutningregnskab](year-close-books.md)  
[Nulstil resultatopgørelse](year-close-income-statement.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
