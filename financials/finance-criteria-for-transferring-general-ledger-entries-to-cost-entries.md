---
title: "Kriterier for overførsel af finansposter til omkostningsposter | Microsoft Docs"
description: "Det er vigtigt at forstå kriterierne for overførsel af finansposter til prisposter. Under overførslen bruger kørslen **Overfør finansposter til CA** følgende kriterier til at fastslå, om og hvordan finansposterne overføres."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 59faad50504bff05e6cdb1c78d00553e85faf47e
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

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
 [Sådan overføres finansposter til omkostningsposter](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md)   
 [Om omkostningsregnskab](finance-about-cost-accounting.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

