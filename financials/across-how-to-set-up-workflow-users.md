---
title: "Sådan konfigurerer du brugere til arbejdsgange | Microsoft Docs"
description: "Før du kan oprette arbejdsgange, skal du konfigurere de brugere, der indgår i arbejdsgangene. Dette er nødvendigt f.eks. for at angive, hvem der skal modtage en besked om at udføre trin i en arbejdsgang."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b4ce5a807923cd052e97215118fa21c9da82abf2
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-workflow-users"></a>Oprette brugere til arbejdsgange
Før du kan oprette arbejdsgange, skal du konfigurere de brugere, der indgår i arbejdsgangene. Dette er nødvendigt f.eks. for at angive, hvem der skal modtage en besked om at udføre trin i en arbejdsgang.  

I vinduet **Brugergruppe for workflow** kan du konfigurere brugere under workflowbrugergrupper, og du kan angive brugernes nummer i en procesrækkefølge, f.eks. en godkenderkæde.  

Workflowbrugere, der fungerer som godkendelsesbrugere, både godkendelsesanmodere og godkendere, skal også først konfigureres som workflowbrugere i vinduet **Konfiguration af godkendelsesbruger**. Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  

> [!NOTE]  
>  Hvis du vil angive, at en godkendelsesanmodning ikke er godkendt, før flere godkendere i en godkendelseskæde har godkendt den, skal du konfigurere godkendere i et hierarki. For godkendertypen **Godkender** skal du konfigurere godkendere i vinduet **Konfiguration af godkendelsesbruger**. For godkendertypen **Brugergruppe for workflow** skal du konfigurere godkendere i vinduet **Brugergrupper for workflow** og definere hierarkiet ved at tildele trinvise tal til hver enkelt godkender i feltet **Rækkefølgenr.**. . Du kan finde flere oplysninger i dette emne og i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md) og i dette emne.  
>   
>  Hvis du vil angive, at en godkendelsesanmodning ikke er godkendt, før flere lige godkendere har godkendt den, uanset et hierarki, skal du oprette en simpel brugergruppe til en arbejdsgang. For godkendertypen **Brugergruppe for workflow** skal du konfigurere godkendere i vinduet **Brugergrupper for workflow** og tildele det samme nummer til hver godkender feltet **Rækkefølgenr.**. . Du kan finde flere oplysninger i dette emne.  

### <a name="to-set-up-a-workflow-user"></a>Sådan oprettes en arbejdsgangsbruger  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugergrupper for arbejdsgang**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Vinduet **Brugergruppe for workflow** åbnes.  
3. I feltet **Kode** skal du angive op til 20 tegn for at identificere workflowet.  
4. I feltet **Beskrivelse** skal du beskrive workflowet.  
5. I oversigtspanelet **Medlemmer af brugergruppe for arbejdsgang** skal du udfylde felterne på den første linje som beskrevet i følgende tabel.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Brugernavn**|Angiv den bruger, der skal indgå i arbejdsgange.<br /><br /> Brugeren skal findes i **Brugeropsætning** vindue. Du kan finde flere oplysninger i [Administrere brugere og rettigheder](ui-how-users-permissions.md).|  
    |**Rækkefølgenr.**|Angiv den rækkefølge, som arbejdsgangsbruger deltager i en arbejdsgang i forhold til andre brugere. Dette felt kan bruges, f.eks. til at angive, hvornår brugeren godkender i forhold til andre godkendere, når du bruger indstillingen **Brugergruppe for workflow** i feltet **Godkendertype** i den relaterede workflowrespons. **TIP:** For at definere, at en godkendelsesanmodning ikke godkendes, før flere lige godkendere har godkendt den, uanset et godkendelseshierarki, skal du oprette en simpel arbejdsganggruppe ved at tildele det samme nummer i rækkefølgen til de relevante godkendere.|  
6. Gentag trin 5 for at føje flere arbejdsgangbrugere til brugergruppen.  
7. Gentag trin 2 til 6 for at tilføje flere arbejdsgangbrugergrupper.  

## <a name="see-also"></a>Se også  
[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)   
[Opsætte workflows](across-set-up-workflows.md)   
[Anvende workflows](across-use-workflows.md)   
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Workflow](across-workflow.md)   

