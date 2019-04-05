---
title: Sådan angiver du, hvornår og hvordan notifikationer modtages | Microsoft Docs
description: Når du konfigurerer brugere i godkendelsesworkflows, skal du angive på siderne Konfiguration af notifikation og Notifikationsplan, hvordan og hvornår de enkelte brugere får besked om godkendelsestrin i workflowet. Individuelle brugere kan også ændre deres opsætning ved at klikke på knappen Rediger notifikationsindstillinger i en vilkårlig notifikation.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/08/2018
ms.author: sgroespe
ms.openlocfilehash: 8bb1b2815740e3acfeb984c1b7cbad160dcd1016
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792827"
---
# <a name="specify-when-and-how-to-receive-notifications"></a>Angive, hvornår og hvordan notifikationer modtages
Når du konfigurerer brugere i godkendelsesworkflows, skal du angive på siderne **Konfiguration af notifikation** og **Notifikationsplan**, hvordan og hvornår de enkelte brugere får besked om godkendelsestrin i workflowet. Individuelle brugere kan også ændre deres opsætning ved at klikke på knappen **Rediger notifikationsindstillinger** i en vilkårlig notifikation.  

 Før du kan konfigurere en godkendelsesbrugers notifikationsindstillinger, skal du konfigurere brugeren som godkendelsesbruger. Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  

 Du kan definere layoutet af e-mailmeddelelserne ved at tilpasse rapporten 1320, Notifikationsmail. Du kan finde flere oplysninger under [Oprette og ændre et brugerdefineret rapport- eller dokumentlayout](ui-how-create-custom-report-layout.md).  

 Mange trin i en godkendelsesarbejdsgang vedrører notifikationer til brugere om, at der er forekommet en hændelse, som de skal reagere på. I ét arbejdsgangstrin kan hændelsen f.eks. være, at bruger 1 anmoder om godkendelse af en ny post. Det relaterede svar er, at der er sendt en notifikation til bruger 2, godkenderen. På det næste trin i arbejdsgangen kan hændelsen være, at bruger 2 godkender posten. Det relaterede svar er, at er sendt en notifikation til bruger 3 om at starte en proces med den godkendte post. For trin i arbejdsgangen, der vedrører godkendelse, er hver notifikation knytet til en godkendelsespost. Du kan finde flere oplysninger i [Workflow](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Angive, hvornår og hvordan brugere modtager notifikationer  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugeropsætning af godkendelser**, og vælg derefter det relaterede link.  
2.  Vælg linjen med den bruger, du vil konfigurere notifikationsindstillinger for, og vælg derefter handlingen **Konfiguration af notifikation**.  
3.  På siden **Konfiguration af notifikation** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Notifikationstype**|Angiv, hvilken type hændelse notifikationen drejer sig om.<br /><br /> Vælg en af følgende indstillinger:<br /><br /> -   **Ny post** angiver, at notifikationen drejer sig om en ny post, f.eks. et dokument, som brugeren skal reagere på.<br />-   **Godkendelse** angiver, at notifikationen drejer sig om en eller flere godkendelsesanmodninger.<br />-   **Forfalden** angiver, at notifikationen skal bruges til at minde brugerne om, at fristen for at reagere på en hændelse er overskredet.|  
    |**Notifikationsmetode**|Angiv, om notifikationen er en mail eller en intern note.|

    Du kan definere layoutet af e-mailmeddelelserne ved at tilpasse rapporten 1320, Notifikationsmail. Du kan finde flere oplysninger under [Oprette og ændre et brugerdefineret rapport- eller dokumentlayout](ui-how-create-custom-report-layout.md).

    Du har nu angivet, hvordan brugeren får notifikationer. Fortsæt med at angive, hvor brugeren får notifikationer.  

4.  Vælg handlingen **Notifikationsplan**.  
5.  På siden **Notifikationsplan** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Gentagelse**|Angiv gentagelsesmønsteret, som brugeren modtager notifikationer efter.|  
    |**Tidspunkt**|Angiv det tidspunkt på dagen, hvor brugeren modtager notifikationer, når værdien i feltet **Gentagelse** er forskellig fra **Øjeblikkeligt**.|  
    |**Daglig frekvens**|Angiv, hvilken type dage brugeren får notifikationer, når værdien i feltet **Gentagelse** er **Dagligt**.<br /><br /> Vælg **Ugedag** for at modtage notifikationer hver arbejdsdag i ugen. Vælg **Dagligt** for at modtage notifikationer hver arbejdsdag i ugen inklusive weekender.|  
    |**Mandag** til **søndag**|Angiv, hvilken type dage brugeren får notifikationer, når værdien i feltet **Gentagelse** er **Ugentligt**.|  
    |**Dato i måned**|Angiv, om brugeren får vist meddelelser på første, sidste eller en bestemt dato i måneden.|  
    |**Månedlig notifikationsdato**|Angiv den dato i måneden, hvor brugeren modtager notifikationer, når værdien i feltet **Dato i måned** er **Brugerdefineret**.|  

## <a name="change-when-and-how-you-receive-notifications"></a>Rediger, hvornår og hvordan du modtager notifikationer  
1.  På en af de notifikationer, du har modtaget, enten som mail eller note, skal du klikke på knappen **Rediger notifikationsindstillinger**.  
2.  På siden **Konfiguration af notifikation** skal du ændre dine indstillinger som beskrevet ovenfor.  

## <a name="see-also"></a>Se også  
 [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)   
 [Oprette og ændre et brugerdefineret rapport- eller dokumentlayout](ui-how-create-custom-report-layout.md)   
 [Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)   
 [Opsætte workflows](across-set-up-workflows.md)   
 [Anvende workflows](across-use-workflows.md)
