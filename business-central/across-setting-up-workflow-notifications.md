---
title: Arbejdsgangsnotifikationer
description: Mange arbejdsgangssvar vedrører notifikationer til en bruger om, at der er forekommet en hændelse, som brugeren skal reagere på. F.eks. på kan hændelsen på ét arbejdsgangstrin være, at bruger 1 anmoder om godkendelse af en ny post, og svaret er, at der er sendt en notifikation til bruger 2, godkenderen. På næste arbejdsgangstrin kan hændelsen være, at bruger 2 godkender posten, og svaret er, at der er sendt en notifikation til bruger 3 om at påbegynde en relateret behandling af den godkendte post. For trin i arbejdsgangen, der vedrører godkendelse, er hver notifikation knyttet til en godkendelsespost.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 10/14/2020
ms.author: edupont
ms.openlocfilehash: d11a391a7fd91f6a094dfae9f8908ba4314b357a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378944"
---
# <a name="workflow-notifications"></a>Arbejdsgangsnotifikationer

Konfigurere arbejdsgange, så brugerne automatisk får besked, når de skal være opmærksomme på et trin i den arbejdsgang. Mange arbejdsgangssvar vedrører notifikationer til en bruger om, at der er forekommet en hændelse, som brugeren skal reagere på. F.eks. på kan hændelsen på ét arbejdsgangstrin være, at bruger 1 anmoder om godkendelse af en ny post, og svaret er, at der er sendt en notifikation til bruger 2, godkenderen. På næste arbejdsgangstrin kan hændelsen være, at bruger 2 godkender posten, og svaret er, at der er sendt en notifikation til bruger 3 om at påbegynde en relateret behandling af den godkendte post. For trin i arbejdsgangen, der vedrører godkendelse, er hver notifikation knyttet til en godkendelsespost. Du kan finde flere oplysninger i [Workflow](across-workflow.md).  

> [!NOTE]  
> Den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter notifikationer som mail og som interne noter.  

> [!IMPORTANT]  
> Alle arbejdsgangsnotifikationer sendes via en opgavekø. Kontrollér, at opgavekøen i installationen er konfigureret til at håndtere arbejdsgangsnotifikationer, og at afkrydsningsfeltet **Start automatisk fra server** er markeret. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Opsætning af notifikationer.

Du konfigurerer forskellige aspekter af arbejdsgangsnotifikationer følgende steder:  

* Godkender notifikation

    For godkendelsesarbejdsgange konfigurerer du modtagerne af arbejdsgangsnotifikationer ved at udfylde en linje på siden **Konfiguration af godkendelsesbruger** for hver bruger, der indgår i arbejdsprocessen.  

    Hvis f.eks. bruger 2 angives i feltet **Godkender-id** på linjen for bruger 1, sendes notifikationen for godkendelsesanmodningen til bruger 1. Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
* Notifikationsplaner

    Du kan konfigurere, hvornår og hvordan brugere får arbejdsgangsnotifikationer, ved at udfylde siden **Notifikationsplan** for hver bruger i arbejdsgangen. Du kan finde flere oplysninger i [Angive, hvornår og hvordan notifikationer modtages](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Tilpas e-mailnotifikationer

    Hvis du vil, kan du tilpasse indholdet af e-mailmeddelelserne ved at tilpasse rapport 1320, Notifikationsmail. Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md).  
* Svarmuligheder

    Du konfigurerer det specifikke indhold og de specifikke regler for en arbejdsgangsnotifikation, når du opretter den pågældende arbejdsgang. Det gør du ved at vælge indstillinger på siden **Indstillinger for workflowrespons** for det arbejdsgangssvar, der repræsenterer notifikationen. Du kan finde flere oplysninger i trin 9 i [Oprette arbejdsgange](across-how-to-create-workflows.md).  

* Giv afsender besked

    I forbindelse med godkendelsesarbejdsprocesser skal du tilføje et trin i arbejdsgangs svaret for at give afsenderen besked, når anmodningen er godkendt eller afvist. Du kan finde flere oplysninger i trin 9 i [Oprette arbejdsgange](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Se også

[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
[Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md)  
[Angive, hvornår og hvordan notifikationer modtages](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Oprette arbejdsgange](across-how-to-create-workflows.md)  
[Sådan opretter og ændrer du Brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md)  
[Du kan bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md)  
[Konfigurere mail](admin-how-setup-email.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]