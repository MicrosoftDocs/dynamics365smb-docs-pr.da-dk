---
title: 'Fremgangsmåde: Oprette brugere til arbejdsgange'
description: Før du kan oprette arbejdsgange, skal du konfigurere de brugere, der indgår i arbejdsgangen på siden med brugergruppe.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.search.form: 1533
ms.date: 09/09/2022
ms.author: edupont
ms.openlocfilehash: 4dbe4217720ddd0bfe976560331329537577cfeb
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585941"
---
# <a name="set-up-workflow-users"></a>Oprette brugere til arbejdsgange

Før du kan oprette godkendelsesworkflows, skal du konfigurere de brugere, der indgår i arbejdsgangene. Dette er nødvendigt f.eks. for at angive, hvem der skal modtage en besked om at udføre trin i en arbejdsgang.  

På siden **Brugergrupper for workflow** kan du konfigurere brugere i workflowbrugergrupper, og du kan angive brugernes nummer i en procesrækkefølge, f.eks. en godkenderkæde. 

Workflowbrugere, der fungerer som godkendelsesbrugere, både godkendelsesanmodere og godkendere, skal også først konfigureres som workflowbrugere på siden **Konfiguration af godkendelsesbruger**. Flere oplysninger i [Konfigurere godkendte brugere](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Hvis du vil definere en godkendelsesanmodning som ikke-godkendt, før flere brugere har godkendt den, skal du konfigurere den i et hierarki. For godkendertypen **Godkender** skal du konfigurere godkendere på siden **Konfiguration af godkendelsesbruger**. For godkendertypen **Brugergruppe for workflow** skal du konfigurere godkendere på siden **Brugergrupper for workflow** og definere hierarkiet ved at tildele trinvise tal til hver enkelt godkender i feltet **Rækkefølgenr.** . Flere oplysninger herunder og i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md). 

## <a name="to-set-up-a-workflow-user"></a>Sådan oprettes en arbejdsgangsbruger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflow brugergrupper**, vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Siden **Brugergruppe for workflow** åbnes.  
3. I feltet **Kode** skal du angive op til 20 tegn for at identificere workflowet.  
4. I feltet **Beskrivelse** skal du beskrive workflowet.  
5. I oversigtspanelet **Medlemmer af brugergruppe for arbejdsgang** skal du udfylde felterne på den første linje som beskrevet i følgende tabel.  

   |Felt|Beskrivelse|
   |-----|-----------|
   |**Brugernavn**|Angiv den bruger, der skal indgå i workflows.<br /><br /> Brugeren skal findes på siden **Brugeropsætning**. Flere oplysninger i [Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md).|
   |**Rækkefølgenr.**|Angiv den rækkefølge, som arbejdsgangsbruger deltager i en arbejdsgang i forhold til andre brugere. Dette felt kan specificere, hvornår brugeren godkender i forhold til andre godkendere ved at konfigurere indstillingen **Brugergruppe for workflow** i feltet **Godkendertype** i den relaterede workflowrespons.| 

   > [!TIP]
   > For at definere, at en godkendelsesanmodning kræver godkendelse fra flere lige godkendere, uanset et godkendelseshierarki, skal du oprette en simpel arbejdsganggruppe ved at tildele det samme nummer i rækkefølgen til alle relevante godkendere.

6. Gentag trin 5 for at føje flere workflowbrugere til workflowbrugergruppen.  
7. Gentag trin 2 til 6 for at tilføje flere arbejdsgangbrugergrupper.  

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
[Konfigurere godkendelsesworkflows](across-set-up-workflows.md)  
[Bruge godkendelsesworkflows](across-use-workflows.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
