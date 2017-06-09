---
title: "Fremgangsmåde: Foretage kørsler | Microsoft Docs"
description: "Få at vide, hvordan kørsler fungerer i Dynamics 365 for Financials."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1f4678ce0cfb18a746374226bb33020f70bf874d
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-run-batch-jobs"></a>Fremgangsmåde: Foretage kørsler
En kørsel er en rutine, hvor data behandles i bundter, f.eks. kørslen **Kursreguler valutabeholdninger**. Der findes kørsler, som udfører periodiske regnskabsaktiviteter, som f.eks. opgørelse af resultatopgørelsen ved afslutning af regnskabsåret. Mange kørsler udfører beregninger, som f.eks. beregningen af rentenotaer, kursjusteringer og beregning af salgspriser.

En kørsel minder om en rapport med den undtagelse, at kørslen bruger resultatet af sit arbejde til at opdatere oplysningerne direkte i stedet for at udskrive resultaterne.

## <a name="to-run-a-batch-job"></a>Sådan foretages en kørsel
1. For at åbne vinduet til den ønskede kørsel skal du i øverste højre hjørne vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive navnet på kørslen og derefter vælge det relaterede link.
2. Hvis der er et oversigtspanel med **Indstillinger** for kørslen, skal du udfylde felterne for at angive, hvad kørslen skal gøre.
3. Vinduet kan indeholde mere end et oversigtspanel med filtre, som du kan bruge til at begrænse de data, der inkluderes i kørslen. Du kan angive kriterier i de foreslåede filtre eller tilføje flere filtre.
4. Vælg **OK** for at starte kørslen.

## <a name="see-also"></a>Se også
[Indtaste kriterier i filtre](ui-enter-criteria-filters.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

