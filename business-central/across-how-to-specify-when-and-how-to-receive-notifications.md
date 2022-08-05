---
title: Angive, hvornår og hvordan arbejdsgangsnotifikationer modtages
description: Når du konfigurerer brugere i godkendelsesarbejdsgange, kan du angive, hvordan og hvornår hver godkendelsesbruger modtager beskeder.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 5c6f480bff2244fac66b996a81ada8e3e318c150
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130033"
---
# <a name="specify-when-and-how-to-receive-workflow-notifications"></a>Angive, hvornår og hvordan arbejdsgangsnotifikationer modtages

Når du opretter godkendelses brugere i arbejdsprocesser, hvor du vil have, at en anden bruger skal kunne godkende ændringer, f. eks. når der oprettes nye poster, eller når en bruger anmoder om godkendelse, skal du angive, hvordan og hvornår godkendelsesbrugeren skal have besked. Du kan f. eks. angive, at en godkendelsesbruger straks skal modtage en e-mail, når nogen opretter en ny kunde. Du kan også vælge at planlægge, at notifikationer skal leveres, f. eks. en gang om måneden.

Brugere kan også ændre deres opsætning ved at klikke på knappen **Rediger notifikationsindstillinger** i en vilkårlig notifikation.  

> [!NOTE]
> Notifikationer leveres i overensstemmelse med beskedindstillingerne for modtageren, ikke afsenderen. Dette er en vigtig forskel, fordi det betyder, at når en bruger anmoder om godkendelse som en del af en arbejdsproces, sendes deres anmodning ikke med det samme. Den leveres i stedet i henhold til den notifikationsplan, der er angivet i meddelelsesindstillingerne for godkenderen.

Før du kan konfigurere en godkendelsesbrugers notifikationsindstillinger, skal du konfigurere brugeren som godkendelsesbruger. Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  

> [!NOTE]
> Hvis du vil bruge e-mail som beskedmetode, skal du konfigurere e-mail til både afsender og modtager i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Konfigurere e-mail](admin-how-setup-email.md).

## <a name="steps-in-workflows"></a>Trin i Workflowtrin

Mange trin i en godkendelsesarbejdsgang vedrører notifikationer til brugere om, at der er forekommet en hændelse, som de skal reagere på. I ét arbejdsgangstrin kan hændelsen f.eks. være, at bruger 1 anmoder om godkendelse af en ny post. Det relaterede svar er, at der er sendt en notifikation til bruger 2, godkenderen. På det næste trin i arbejdsgangen kan hændelsen være, at bruger 2 godkender posten. Det relaterede svar er, at er sendt en notifikation til bruger 3 om at starte en proces med den godkendte post. For trin i arbejdsgangen, der vedrører godkendelse, er hver notifikation knytet til en godkendelsespost. Du kan finde flere oplysninger i [Workflow](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Angive, hvornår og hvordan brugere modtager notifikationer  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Godkendelse af brugerkonfiguration**, og vælg derefter det relaterede link.  
2. Vælg linjen med den bruger, du vil konfigurere notifikationsindstillinger for, og vælg derefter handlingen **Konfiguration af notifikation**.  
3. På siden **Konfiguration af notifikation** skal du udfylde felterne som beskrevet i følgende tabel.  

    > [!NOTE]
    > Hvis du åbner siden med **Konfiguration af notifikation** fra siden **Brugeropsætning af godkendelser**, er notifikationsopsætningen knyttet til godkendelsesbrugeren. Godkendelsesbrugeren vil altid modtage beskeder om arbejdsgangen ifølge denne Notifikationsopsætning. Hvis du bruger Fortæl mig til at åbne siden **Notifikationsopsætning**, vil notifikationsopsætningen gælde for alle brugere.  

    |Felt|Beskrivlse|  
    |---------------------------------|---------------------------------------|  
    |**Notifikationstype**|Angiv, hvilken type hændelse notifikationen drejer sig om.<br /><br /> Vælg en af følgende indstillinger:<br /><br /> -   **Ny post** angiver, at notifikationen drejer sig om en ny post, f.eks. et dokument, som brugeren skal reagere på.<br />-   **Godkendelse** angiver, at notifikationen drejer sig om en eller flere godkendelsesanmodninger.<br />-   **Forfalden** angiver, at notifikationen skal bruges til at minde brugerne om, at fristen for at reagere på en hændelse er overskredet.|  
    |**Notifikationsmetode**|Angiv, om notifikationen er en mail eller en intern note.|

    Du kan definere layoutet af e-mailmeddelelserne ved at tilpasse rapporten 1320, Notifikationsmail. Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md).

    Du har nu angivet, hvordan brugeren får notifikationer. Fortsæt med at angive, hvor brugeren får notifikationer.  

4. Vælg handlingen **Notifikationsplan**.  
5. På siden **Notifikationsplan** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Gentagelse**|Angiv gentagelsesmønsteret, som brugeren modtager notifikationer efter.|  
    |**Tidspunkt**|Angiv det tidspunkt på dagen, hvor brugeren modtager notifikationer, når værdien i feltet **Gentagelse** er forskellig fra **Øjeblikkeligt**.|  
    |**Daglig frekvens**|Angiv, hvilken type dage brugeren får notifikationer, når værdien i feltet **Gentagelse** er **Dagligt**.<br /><br /> Vælg **Ugedag** for at modtage notifikationer hver arbejdsdag i ugen. Vælg **Dagligt** for at modtage notifikationer hver arbejdsdag i ugen inklusive weekender.|  
    |**Mandag** til **søndag**|Angiv, hvilken type dage brugeren får notifikationer, når værdien i feltet **Gentagelse** er **Ugentligt**.|  
    |**Dato i måned**|Angiv, om brugeren får vist meddelelser på første, sidste eller en bestemt dato i måneden.|  
    |**Månedlig notifikationsdato**|Angiv den dato i måneden, hvor brugeren modtager notifikationer, når værdien i feltet **Dato i måned** er **Brugerdefineret**.|  

## <a name="change-when-and-how-you-receive-notifications"></a>Rediger, hvornår og hvordan du modtager notifikationer

1. På en af de notifikationer, du har modtaget, enten som mail eller note, skal du klikke på knappen **Rediger notifikationsindstillinger**.  
2. På siden **Konfiguration af notifikation** skal du ændre dine indstillinger som beskrevet ovenfor.  

## <a name="see-also"></a>Se også

[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
[Sådan opretter og ændrer du Brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md)  
[Konfiguration af workflownotifikationer](across-setting-up-workflow-notifications.md)  
[Opsætte workflows](across-set-up-workflows.md)  
[Bruge arbejdsgange](across-use-workflows.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]