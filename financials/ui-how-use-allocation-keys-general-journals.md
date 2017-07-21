---
title: "Fremgangsmåde: Bruge fordelingsnøgler i finanskladder | Microsoft Docs"
description: "Få at vide, hvordan du kan bruge fordelingsnøgler i kladder."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bbacf9b5634d51478dd4d54ac4b587ea9bfaaf99
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-use-allocation-keys-in-general-journals"></a>Fremgangsmåde: Bruge fordelingsnøgler i kladder
Du kan allokere en post i en finanskladde til flere forskellige konti, når du bogfører kladden. Allokeringen kan foretages efter antal, procent eller beløb.

## <a name="to-set-up-allocation-keys"></a>Sådan konfigureres fordelingsnøgler
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finansgentagelseskladde**, og vælg derefter det relaterede link.
2. Vælg feltet **Kladdenavn** for at åbne vinduet **Finanskladdenavne**.
3. Du kan ændre fordelinger for et eksisterende navn på listen eller oprette et nyt navn med fordelinger.
   * Du kan oprette en ny kladde ved at vælge handlingen **Ny** og gå til næste trin.
   * Vælg kladden og gå til trin 7, hvis du vil ændre fordelingerne af en eksisterende kladde.    
4. Angiv navnet på en ny kladde i feltet **Navn**, f.eks. Rengøring. Angiv en beskrivelse i feltet **Beskrivelse**, f.eks. Kladde til rengøringsudgifter.
5. Når du er færdig, skal du lukke vinduet. Der åbnes en ny tom gentagelseskladde.
6. Udfyld felterne på linjen.
7. Vælg handlingen **Fordelinger**.
8. Tilføj en linje for hver fordeling. Du skal udfylde et af følgende felter: **Allokeringspct.**, **Andel i antal** eller **Beløb**. Du skal også udfylde **Kontonr.** og desuden felterne for globale dimensioner, hvis du allokerer transaktionen mellem globale dimensioner.
9. Hvis du angiver en procent på en linje, beregnes beløbet i feltet **Beløb** automatisk. Disse beløb har det modsatte tegn af tegnet fra det totale beløb i feltet **Beløb** i gentagelseskladden.
10. Når du har angivet linjerne med fordelinger, skal du vælge **OK** for at gå tilbage til vinduet **Finansgentagelseskladde**. Feltet **Fordelt beløb (RV)** udfyldes og svarer til feltet **Beløb**.
11. Bogfør journalen.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Sådan ændres en fordelingsnøgle, der allerede er oprettet
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finansgentagelseskladde**, og vælg derefter det relaterede link.
2. Vælg kladden med allokeringen i vinduet **Finansgentagelseskladde**.
3. Vælg linjen med fordelingen og vælg derefter handlingen **Fordelinger**.
4. Rediger de relevante felter, og vælg derefter knappen **OK**.

## <a name="see-also"></a>Se også
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Bogføring af dokumenter og kladder](ui-post-documents-journals.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

