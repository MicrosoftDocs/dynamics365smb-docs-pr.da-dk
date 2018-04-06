---
title: "Sådan opretter du workflows | Microsoft Docs"
description: "Du kan oprette arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cab6546e152ad91c1b3264fa8bd10c0fd668636d
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-workflows"></a>Oprette arbejdsgange
Du kan oprette arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.  

I vinduet **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en workflowhændelse, begrænset af hændelsesbetingelser, og et workflowrespons med responsmuligheder. Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden.  

Når du opretter workflows, kan du kopiere trinene fra eksisterende workflows eller workflowskabeloner. Workflowskabeloner repræsenterer workflows, som ikke kan redigeres, og som findes i den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)]. Koden for arbejdsgangsskabeloner, som er tilføjet af Microsoft, har "MS" foran som f.eks. i "MS PIW". Du kan finde flere oplysninger i [Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).  

Hvis et virksomhedsscenarie kræver workflowhændelser eller et respons, der ikke understøttes, skal en Microsoft-partner implementere dem ved at tilpasse programkoden.  
  
> [!NOTE]  
>  Alle notifikationer om arbejdsgangstrin sendes via en opgavekø. Kontrollér, at opgavekøen i installationen er konfigureret til at håndtere arbejdsgangsnotifikationer, og at afkrydsningsfeltet **Start automatisk fra NAS** er markeret. Du kan finde flere oplysninger i [Brug af opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-workflow"></a>Sådan oprettes en arbejdsgang  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Workflows**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Vinduet **Workflow** åbnes.  
3. I feltet **Kode** skal du angive op til 20 tegn for at identificere workflowet.  
4. Når du vil oprette workflowet fra en workflowskabelon i vinduet **Workflows**, skal du vælge handlingen **Opret workflow fra skabelon**. Du kan finde flere oplysninger i [Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).  
5. I feltet **Beskrivelse** skal du beskrive workflowet.  
6. I feltet **Kategori** kan du angive, hvilken kategori workflowet hører under.  
7. I feltet **Når hændelse** skal du angive den hændelse, der skal udføres for at starte trinnet i workflowet.  

    Når du vælger feltet, åbnes vinduet **Workflowhændelser**, hvor du kan vælge mellem alle workflowhændelser, der findes.  
8. I feltet **Betingelse** skal du angive en eller flere betingelser, der skal opfyldes, før hændelsen i feltet **Når hændelse** kan udføres.  

    Når du vælger feltet, åbnes vinduet **Hændelsesbetingelser**, hvor du kan vælge på en liste over filterfelter, der er relevante som betingelser for den pågældende hændelse. Du kan tilføje nye filterfelter, du vil bruge som hændelsesbetingelser. Du kan angive hændelsesbetingelsesfiltre, ligesom du angiver filtre for rapportanmodningssider.  

    Hvis workflowhændelsen er ændringen af et bestemt felt i en post, åbnes vinduet **Hændelsesbetingelser**, hvor du kan vælge feltet og ændringstypen.  

    1.  Hvis du vil angive feltændringen for hændelsen, skal du i feltet **Felt** i vinduet **Hændelsesbetingelser** markere det felt, der ændres.  
    2.  I feltet **Operator** skal du vælge enten **Reduceret**, **Forøget** eller **Ændret**.  
9. Angiv den respons, der skal følge, når workflowhændelsen forekommer, i feltet **Så svar**.  

     Når du vælger feltet, åbnes vinduet **Workflowrespons**, hvor du kan vælge mellem alle workflowresponser, der findes, og angive indstillinger for respons for den valgte respons.  
10. I oversigtspanelet **Indstillinger for den valgte workflowrespons** skal du angive indstillinger for workflowet ved at vælge værdier i de forskellige felter, der vises, på følgende måde:  

    1.  Hvis du vil angive indstillinger for et workflowrespons, der involverer afsendelse af en notifikation, skal du udfylde felterne som beskrevet i følgende tabel.  

        |Felt|Description|  
        |----------------------------------|---------------------------------------|  
        |**Modtagers bruger-id**|Angiv den bruger, som notifikationen skal sendes til. Bemærk: Denne indstilling er kun tilgængelig for workflowrespons med en pladsholder for en bestemt bruger. Notifikationsmodtageren defineres typisk af godkendelsesbrugeropsætningen, når det drejer sig om arbejdsgangssvar uden pladsholdere for brugere.|  
        |**Side, der linkes til**|Angiv en anden side i [!INCLUDE[d365fin](includes/d365fin_md.md)], som linket i notifikationen åbner i stedet for standardsiden.|  
        |**Brugerdefineret link**|Angiv URL-adressen på et link, der føjes til notifikationen ud over standardlinket til en side i [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    2.  Hvis du vil angive indstillinger for et workflowrespons, der involverer oprettelse af en godkendelsesanmodning, skal du udfylde felterne som beskrevet i følgende tabel.  

        |Felt|Description|  
        |----------------------------------|---------------------------------------|  
        |**Formular for forfaldsdato**|Angiv, inden hvor mange dage godkendelsesanmodningen skal løses fra den dato, hvor den blev sendt.|  
        |**Uddeleger efter**|Angiv, om og hvornår en godkendelsesanmodning uddelegeres automatisk til den relevante stedfortræder. Du kan vælge, at der automatisk skal uddelegeres én, to eller fem dage efter den dato, hvor der blev anmodet om godkendelse.|  
        |**Godkendertype**|Angiv, hvem godkenderen er, i overensstemmelse med opsætningen af godkendelses- og arbejdsgangsbrugere.<br /><br /> Der findes følgende indstillinger:<br /><br /> -   **Sælger/indkøber** angiver, at den bruger, der er angivet i feltet **Sælger/indkøbskode** i vinduet **Brugeropsætning af godkendelser**, bestemmer godkenderen. Derefter oprettes der godkendelsesanmodningsposter ud fra værdien i feltet **Godkenders grænsetype**.<br />     Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-workflow-users.md)|  
        |**Vis bekræftelsesmeddelelse**|Angiv, om en bekræftelsesmeddelelse vises for brugere, når de anmoder om en godkendelse.|  
        |**Godkenders grænsetype**|Angiv, hvordan godkenderes godkendelsesgrænser påvirker, hvornår godkendelsesanmodningsposter oprettes for dem. En kvalificeret godkender er en person, hvis godkendelsesgrænse er større end værdien i anmodningen, der sendes.<br /><br /> Der findes følgende indstillinger:<br /><br /> 1. **Godkenderkæde** angiver, at godkendelsesanmodningsposter oprettes for alle anmoderens godkendere til og med den første kvalificerede godkender.<br />2. **Direkte godkender** angiver, at en godkendelsesanmodningspost kun oprettes for anmoderens umiddelbare godkender, uanset godkenderens godkendelsesgrænse.<br />3. **Første kvalificerede godkender** angiver, at en godkendelsesanmodningspost kun oprettes for anmoderens første kvalificerede godkender.<br />|  
    3.  Hvis du vil angive indstillinger for et arbejdsgangssvar, der involverer oprettelse af kladdelinjer, skal du udfylde felterne som beskrevet i følgende tabel.  

        |Felt|Description|  
        |----------------------------------|---------------------------------------|  
        |**Finanskladdetypes navn**|Angiv navnet på den finanskladdetype, som de angivne kladdelinjer oprettes i.|  
        |**Finanskladdenavn**|Angiv det finanskladdenavn, som de angivne kladdelinjer oprettes i.|  

11. Vælg knapperne **Forøg indrykning** og **Reducer indrykning** for at indrykke hændelsesnavnet i feltet **Når** for at definere trinnets placering i workflowet.  
    1.  Angiv, at trinnet er næste i arbejdsgangrækkefølgen ved at indrykke hændelsesnavnet under hændelsesnavnet på det foregående trin.  
    2.  Angiv, at trinnet er et af flere alternative trin, der kan starte, afhængigt af dets tilstand, ved at placere hændelsesnavnet på den samme indrykning som de andre alternative trin. Ranger sådanne valgfrie trin i overensstemmelse med prioritet ved at placere det vigtigste først.  

    > [!NOTE]  
    >  Du kan kun ændre indrykningen af et trin, der ikke har et efterfølgende trin.  

12. Gentag trin 7 til 11 for at tilføje flere arbejdsgang trin, før eller efter det trin, du lige har oprettet.  
13. Markér afkrydsningsfeltet **Aktiveret** for at angive, at workflowet starter, så snart hændelsen på det første trin af typen **Startpunkt** nås. Der er flere oplysninger i [Anvende workflows](across-use-workflows.md).  

> [!NOTE]  
>  Undlad at aktivere en arbejdsgang, før du er sikker på, at arbejdsgangen er fuldført, og at arbejdsgangstrin involveret kan begynde.  

> [!TIP]  
>  For at se relationer mellem de tabeller, der bruges i workflows, skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "ikonet Søg efter side eller rapport"), og angiv derefter **Workflow – tabelrelationer**.  

## <a name="see-also"></a>Se også  
[Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md)   
[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)   
[Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)   
[Vise arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md)   
[Slette arbejdsgange](across-how-to-delete-workflows.md)   
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Opsætte workflows](across-set-up-workflows.md)   
[Anvende workflows](across-use-workflows.md)   
[Workflow](across-workflow.md)      


