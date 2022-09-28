---
title: Konfiguration af arbejdsgangsnotifikationer
description: Denne artikel beskriver, hvordan du opretter arbejdsgangs notifikationer for at advare en bruger om, at en hændelse skal reagere på - der kræves et svar fra arbejdsprocessen.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 9405af9c52b17ab34fded263692e3294ed8aaf11
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533963"
---
# <a name="workflow-notifications"></a>Arbejdsgangsnotifikationer

Konfigurere arbejdsgange, så brugerne automatisk får besked, når de skal være opmærksomme på et trin i den arbejdsgang. Mange arbejdsgangssvar vedrører notifikationer til en bruger om, at der er forekommet en hændelse, som brugeren skal reagere på.

Du kan f. eks. angive, at brugeren 2, godkender brugeren, modtager en besked, hver gang bruger 1 anmoder om godkendelse af en ny post. I det næste trin i arbejdsprocessen får bruger 3 besked, efter at bruger 2 har godkendt posten for at starte en relateret behandling af posten. Med trin i workflowgodkendelse er hver notifikation knyttet til en godkendelsespost. Du kan finde flere oplysninger i [Workflow](across-workflow.md).  

> [!NOTE]  
> Standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter notifikationer som mail og som interne noter.  

> [!IMPORTANT]  
> Alle arbejdsgangsnotifikationer sendes via en opgavekø. Kontrollér, at opgavekøen i installationen er konfigureret til at håndtere arbejdsgangsnotifikationer, og at afkrydsningsfeltet **Start automatisk fra server** er markeret. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Opsætning af notifikationer.

Du kan konfigurere forskellige aspekter af arbejdsgangsnotifikationer følgende steder:  

* Godkender notifikation

    For godkendelsesarbejdsgange konfigurerer du modtagerne af arbejdsgangsnotifikationer ved at udfylde en linje på siden **Konfiguration af godkendelsesbruger** for hver bruger, der indgår i arbejdsprocessen.  

    Hvis f.eks. bruger 2 angives i feltet **Godkender-id** på linjen for bruger 1, sendes notifikationen for godkendelsesanmodningen til bruger 2. Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
* Notifikationsplaner

    Du kan konfigurere, hvornår og hvordan brugere får arbejdsgangsnotifikationer, ved at udfylde siden **Notifikationsplan** for hver bruger i arbejdsgangen. Du kan finde flere oplysninger i [Angive, hvornår og hvordan notifikationer modtages](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Tilpas e-mailnotifikationer

    Hvis du vil, kan du tilpasse indholdet af e-mailmeddelelserne ved at tilpasse Rapport 1320, Notifikationsmail. Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md).  

    > [!NOTE]
    > Hvis du vil bruge e-mail som beskedmetode, skal du konfigurere e-mail til både afsender og modtager i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Konfigurere e-mail](admin-how-setup-email.md).

* Svarmuligheder

    Du konfigurerer det specifikke indhold og de specifikke regler for en arbejdsgangsnotifikation, når du opretter den pågældende arbejdsgang. Vælg tilpasningsindstillinger på siden **Workflowsvar** for det workflowsvar, der repræsenterer notifikationen. Du kan finde flere oplysninger i trin 9 i [Oprette workflows](across-how-to-create-workflows.md#to-create-a-workflow).  

* Giv afsender besked

    I forbindelse med godkendelsesarbejdsprocesser skal du tilføje et trin i arbejdsgangs svaret for at give afsenderen besked, når anmodningen er godkendt eller afvist. Du kan finde flere oplysninger i trin 9 i [Oprette workflows](across-how-to-create-workflows.md#to-create-a-workflow).  

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
[Oprette brugere til workflow](across-how-to-set-up-workflow-users.md)  
[Angive, hvornår og hvordan notifikationer modtages](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Oprette arbejdsgange](across-how-to-create-workflows.md)  
[Sådan opretter og ændrer du Brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md)  
[Du kan bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md)  
[Konfigurere mail](admin-how-setup-email.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
