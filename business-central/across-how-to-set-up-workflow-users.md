---
title: 'Fremgangsmåde: Oprette brugere til arbejdsgange'
description: 'Før du kan oprette arbejdsgange, skal du konfigurere de brugere, der indgår i dem, på siden Brugeropsætning af godkendelser.'
author: brentholtorf
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 05/31/2023
ms.author: bholtorf
---
# <a name="set-up-a-sequence-of-workflow-users" />Konfigurere en række workflowbrugere

Før du kan oprette godkendelsesworkflows, skal du konfigurere de brugere, der skal sende anmodninger, og deres godkendere. Du kan f.eks. angive, hvem der skal modtage en besked om at udføre et workflowtrin. Du kan konfigurere deltagere i godkendelsesworkflow på siden **Brugeropsætning af godkendelser**. Flere oplysninger i [Konfigurere godkendte brugere](across-how-to-set-up-approval-users.md).

På siden **Brugergrupper for workflow** kan du angive, hvor en deltager skal deltage i et godkendelsesworkflow, ved at skrive et tal i feltet **Rækkefølgenr.** . Du kan f.eks. angive, at brugere skal deltage i en rækkefølge, f.eks. en kæde af godkendere. Du kan også angive en flad liste over godkendere ved at indtaste det samme nummer. I sidstnævnte tilfælde er det kun en af godkenderne, der skal godkende en anmodning.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## <a name="to-set-up-a-workflow-user-group" />Sådan oprettes en brugergruppe for workflow

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflow brugergrupper**, vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Siden **Brugergruppe for workflow** åbnes.  
3. I feltet **Kode** skal du angive op til 20 tegn for at identificere workflowet.  
4. I feltet **Beskrivelse** skal du beskrive workflowet.  
5. I oversigtspanelet **Medlemmer af brugergruppe for arbejdsgang** skal du udfylde felterne på den første linje som beskrevet i følgende tabel.  

   |Felt|Beskrivelse|
   |-----|-----------|
   |**Brugernavn**|Angiv den bruger, der skal indgå i et workflow.<br /><br /> Brugeren skal findes på siden **Brugeropsætning**. Flere oplysninger i [Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md).|
   |**Rækkefølgenr.**|Angiv den rækkefølge, som arbejdsgangsbruger deltager i en arbejdsgang i forhold til andre brugere. Dette felt kan specificere, hvornår brugeren godkender i forhold til andre godkendere ved at konfigurere indstillingen **Brugergruppe for workflow** i feltet **Godkendertype** i den relaterede workflowrespons.| 

6. Gentag trin 5 for at føje flere workflowbrugere til workflowbrugergruppen.  

## <a name="see-related-microsoft-training" />Se relateret [Microsoft-træning](/training/modules/create-workflows/)

## <a name="see-also" />Se også

[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
[Konfigurere godkendelsesworkflows](across-set-up-workflows.md)  
[Bruge godkendelsesworkflows](across-use-workflows.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
