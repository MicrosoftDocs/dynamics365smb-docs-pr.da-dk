---
title: Kriterier for overførsel af finansposter til omkostningsposter | Microsoft Docs
description: Det er vigtigt at forstå kriterierne for overførsel af finansposter til prisposter. Under overførslen bruger kørslen **Overfør finansposter til CA** følgende kriterier til at fastslå, om og hvordan finansposterne overføres.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 62d19b5ff112871f7f44f0945bdcfd38306ed8b3
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "931647"
---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a>Kriterier for overførsel af finansposter til omkostningsposter.
Det er vigtigt at forstå kriterierne for overførsel af finansposter til prisposter. Under overførslen bruger kørslen **Overfør finansposter til CA** følgende kriterier til at fastslå, om og hvordan finansposterne overføres.  

Finansposter overføres i følgende tilfælde:  

-   Posterne har dimensionsværdier, der svarer til enten et omkostningssted eller et omkostningsobjekt.  
-   Posterne har dimensionsværdier, der svarer til et omkostningssted og et omkostningsobjekt. For disse poster har omkostningsstedet forrang. Dette hjælper med at undgå en situation, hvor en omkostningstype vises i både et omkostningsobjekt og et omkostningssted og derfor tælles to gange i statistikken.  
-   Dokumentnummeret i posterne er tomt, så det vises med dokumentnummeret 0000 i omkostningsposterne.  
-   Posterne overføres til en omkostningstype, der giver mulighed for samlede poster, og disse poster overføres som en samlet post enten hver måned eller hver dag.  

Finansposter overføres ikke i følgende tilfælde:  

-   Posterne har dimensionsværdier, der ikke svarer til et omkostningssted eller et omkostningsobjekt.  
-   Posterne har værdien nul.  
-   Posterne har en finanskonto, der er blevet slettet.  
-   Posterne har en finanskonto, der ikke er af typen **Resultatopgørelse**.  
-   Posterne har en finanskonto, der ikke er tildelt en omkostningstype.  
-   Posterne har en bogføringsdato før **Startdato for finansoverførsel**.  
-   Posterne er blevet bogført med en ultimodato. De er typisk poster, der fører resultatopgørelsens saldo tilbage i slutningen af året.  

## <a name="see-also"></a>Se også  
[Regnskab for omkostninger](finance-manage-cost-accounting.md)  
 [Overføre finansposter til omkostningsposter](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md)   
 [Om omkostningsregnskab](finance-about-cost-accounting.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
