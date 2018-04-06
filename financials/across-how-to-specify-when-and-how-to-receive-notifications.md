---
title: "Sådan angiver du, hvornår og hvordan notifikationer modtages | Microsoft Docs"
description: "Når du konfigurerer brugere i godkendelsesarbejdsgange, skal du angive i vinduet Konfiguration af notifikation og Notifikationsplan, hvordan og hvornår de enkelte brugere får besked om godkendelsestrin i arbejdsprocessen. Individuelle brugere kan også ændre deres opsætning ved at klikke på knappen Rediger notifikationsindstillinger i en vilkårlig notifikation."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 1c514178ef65b78ad74256834b962e7018ac3864
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="specify-when-and-how-to-receive-notifications"></a>Angive, hvornår og hvordan notifikationer modtages
Når du konfigurerer brugere i godkendelsesarbejdsgange, skal du angive i vinduet **Konfiguration af notifikation** og **Notifikationsplan**, hvordan og hvornår de enkelte brugere får besked om godkendelsestrin i arbejdsprocessen. Individuelle brugere kan også ændre deres opsætning ved at klikke på knappen **Rediger notifikationsindstillinger** i en vilkårlig notifikation.  

 Før du kan konfigurere en godkendelsesbrugers notifikationsindstillinger, skal du konfigurere brugeren som godkendelsesbruger. Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  

 Du definerer layout og indhold for notifikationer ved at konfigurere notifikationsskabeloner. Du kan finde flere oplysninger i [Administrere notifikationsskabeloner](across-how-to-manage-notification-templates.md).  

 Mange trin i en godkendelsesarbejdsgang vedrører notifikationer til brugere om, at der er forekommet en hændelse, som de skal reagere på. I ét arbejdsgangstrin kan hændelsen f.eks. være, at bruger 1 anmoder om godkendelse af en ny post. Det relaterede svar er, at der er sendt en notifikation til bruger 2, godkenderen. På det næste trin i arbejdsgangen kan hændelsen være, at bruger 2 godkender posten. Det relaterede svar er, at er sendt en notifikation til bruger 3 om at starte en proces med den godkendte post. For trin i arbejdsgangen, der vedrører godkendelse, er hver notifikation knytet til en godkendelsespost. Du kan finde flere oplysninger i [Workflow](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Angive, hvornår og hvordan brugere modtager notifikationer  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugeropsætning af godkendelser**, og vælg derefter det relaterede link.  
2.  Vælg linjen med den bruger, du vil konfigurere notifikationsindstillinger for, og vælg derefter handlingen **Konfiguration af notifikation**.  
3.  I vinduet **Konfiguration af notifikation** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Notifikationstype**|Angiv, hvilken type hændelse notifikationen drejer sig om.<br /><br /> Vælg en af følgende indstillinger:<br /><br /> -   **Ny post** angiver, at notifikationen drejer sig om en ny post, f.eks. et dokument, som brugeren skal reagere på.<br />-   **Godkendelse** angiver, at notifikationen drejer sig om en eller flere godkendelsesanmodninger.<br />-   **Forfalden** angiver, at notifikationen skal bruges til at minde brugerne om, at fristen for at reagere på en hændelse er overskredet.|  
    |**Notifikationsskabelonkode**|Angiv koden på den notifikationsskabelon, der bruges til at oprette notifikationer for brugeren.|  
    |**Ikke-aggregerede notifikationer**|Angiv, om brugeren får en notifikation for hver hændelse eller samlede notifikationer.<br /><br /> Hvis afkrydsningsfeltet **Ikke-aggregerede notifikationer** ikke er markeret, modtager brugeren notifikationer, der samler oplysninger om hændelser, som forekommer i samme gentagelsesmønsteret i notifikationsplanen.|  

     Du har nu angivet, hvordan brugeren får notifikationer. Fortsæt med at angive, hvor brugeren får notifikationer.  

4.  Vælg handlingen **Notifikationsplan**.  
5.  I vinduet **Notifikationsplan** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Gentagelse**|Angiv gentagelsesmønsteret, som brugeren modtager notifikationer efter.|  
    |**Tidspunkt**|Angiv det tidspunkt på dagen, hvor brugeren modtager notifikationer, når værdien i feltet **Gentagelse** er forskellig fra **Øjeblikkeligt**.|  
    |**Daglig frekvens**|Angiv, hvilken type dage brugeren får notifikationer, når værdien i feltet **Gentagelse** er **Dagligt**.<br /><br /> Vælg **Ugedag** for at modtage notifikationer hver arbejdsdag i ugen. Vælg **Dagligt** for at modtage notifikationer hver arbejdsdag i ugen inklusive weekender.|  
    |**Mandag** til **søndag**|Angiv, hvilken type dage brugeren får notifikationer, når værdien i feltet **Gentagelse** er **Ugentligt**.|  
    |**Dato i måned**|Angiv, om brugeren får vist meddelelser på første, sidste eller en bestemt dato i måneden.|  
    |**Månedlig notifikationsdato**|Angiv den dato i måneden, hvor brugeren modtager notifikationer, når værdien i feltet **Dato i måned** er **Brugerdefineret**.|  

## <a name="change-when-and-how-you-receive-notifications"></a>Rediger, hvornår og hvordan du modtager notifikationer  
1.  På en af de notifikationer, du har modtaget, enten som mail eller note, skal du klikke på knappen **Rediger notifikationsindstillinger**.  
2.  I feltet **Konfiguration af notifikation** skal du ændre dine indstillinger som beskrevet ovenfor.  

## <a name="see-also"></a>Se også  
 [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)   
 [Administrere notifikationsskabeloner](across-how-to-manage-notification-templates.md)   
 [Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)   
 [Opsætte workflows](across-set-up-workflows.md)   
 [Anvende workflows](across-use-workflows.md)

