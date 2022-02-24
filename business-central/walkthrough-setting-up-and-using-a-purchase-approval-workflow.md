---
title: Opsætning og brug af workflow for godkendelse af køb | Microsoft Docs
description: Du kan automatisere processen med at godkende nye eller ændrede poster, f.eks dokumenter, kladdelinjer og debitorkort, ved at oprette arbejdsgange med fremgangsmåder for de pågældende godkendelser. Før du opretter godkendelsesarbejdsgange, skal du oprette en godkender og erstatte godkenderen for hver godkendelsesbruger. Du kan også angive beløbsgrænser for godkendere for at definere, hvilke salgs- og købsposter, som de er kvalificerede til at godkende. Godkendelsesanmodninger og andre meddelelser kan sendes som mail eller intern note. For hver godkendelsesbrugeropsætning kan du også angive, hvornår der skal modtages notifikationer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 74f8d9dcb309581681e6161a12e7e52fac066726
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193367"
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Gennemgang: Opsætning og brug af workflow for godkendelse af køb
Du kan automatisere processen med at godkende nye eller ændrede poster, f.eks dokumenter, kladdelinjer og debitorkort, ved at oprette arbejdsgange med fremgangsmåder for de pågældende godkendelser. Før du opretter godkendelsesarbejdsgange, skal du oprette en godkender og erstatte godkenderen for hver godkendelsesbruger. Du kan også angive beløbsgrænser for godkendere for at definere, hvilke salgs- og købsposter, som de er kvalificerede til at godkende. Godkendelsesanmodninger og andre meddelelser kan sendes som mail eller intern note. For hver godkendelsesbrugeropsætning kan du også angive, hvornår der skal modtages notifikationer.

> [!NOTE]
> Ud over Workflow-funktionaliteten i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du integreret med Microsoft Flow for at definere workflows for hændelser i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vær opmærksom på, selvom det er to separate workflowsystemer, tilføjes en Flow-skabelon, du opretter med Microsoft Flow, på listen over workflowskabeloner i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Bruge Business Central i et automatisk workflow](across-how-use-financials-data-source-flow.md).   

 Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin. Du kan finde flere oplysninger i [Workflow](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
Denne gennemgang illustrerer følgende opgaver:  

-   Angive indstillinger for godkendelsesbrugere.  
-   Oprette notifikationer til godkendelsesbrugere.  
-   Ændre og aktivere en godkendelsesarbejdsgang.  
-   Anmoder om godkendelse af en købsordre, som Anna.  
-   Modtager en besked og godkender derefter anmodningen, som Søren.  

## <a name="story"></a>Historie  
Søren er superbruger hos CRONUS. Han opretter to godkendelsesbrugere. Den ene er Anna, der repræsenterer en indkøber. Den anden er ham selv, som repræsenterer Annas godkender. Søren giver derefter sig selv ubegrænsede indkøbsgodkendelsesrettigheder og angiver, at han skal modtage notifikationer via intern note, så snart en relevant hændelse finder sted. Til sidst opretter Søren den krævede godkendelsesarbejdsgang som en kopi af den eksisterende arbejdsgangskabelon Workflow for godkendelse af købsordre, lader alle eksisterende hændelsesbetingelser og svarmuligheder være uændrede og aktiverer arbejdsprocessen.  

For at kontrollere godkendelsesworkflowet logger Søren først på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Anna og anmoder derefter om godkendelse af en købsordre. Derefter logger Søren på som sig selv, ser noten i sit Rollecenter, følger linket til godkendelsesanmodningen for købsordren og godkender derefter anmodningen.  

## <a name="setting-up-sample-data"></a>Oprette eksempeldata
Før du kan konfigurere godkendelsesbrugere og deres notifikationsmetode, skal du kontrollere, at der findes to brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)]: en bruger, der repræsenterer Anna. Den anden bruger, dig selv, repræsenterer Søren. Du kan finde flere oplysninger i [Oprette brugere i henhold til licenser](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a>Angive indstillinger for godkendelsesbrugere  
Når du er logget på som dig selv, skal du indstille Anna som godkendelsesbruger, og hendes godkender er dig selv. Indstil dine godkendelsesrettigheder, og angiv, hvordan og hvornår du skal have besked om godkendelsesanmodninger.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Sådan opretter du dig selv og Anna som godkendelsesbrugere  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugeropsætning af godkendelser**, og vælg derefter det relaterede link.  
2.  På siden **Brugeropsætning af godkendelser** skal du vælge handlingen **Ny**.  

    > [!NOTE]  
    >  Du skal oprette en godkender, før du kan konfigurere brugere, der kræver denne godkenders godkendelse. Derfor skal du oprette dig selv, før du opretter Anna.  

3.  Oprette de to godkendelsesbrugere ved at udfylde felterne som beskrevet i følgende tabel.  

    |Bruger-id|Godkender-id|Ubegrænset godkendelse af køb|  
    |-------------|-----------------|---------------------------------|  
    |DIG||Valgt|  
    |ANNA|DIG||  

### <a name="setting-up-notifications"></a>Opsætning af meddelelser.  
I denne gennemgang får brugeren en besked i form af en intern note om anmodninger, der skal godkendes. Godkendelsesmeddelelsen kan også komme via e-mail. Du kan finde flere oplysninger i [Angive, hvornår og hvordan notifikationer modtages](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### <a name="to-set-up-how-and-when-you-are-notified"></a>Sådan angiver du, hvordan og hvornår du skal have besked  
1.  På siden **Brugeropsætning af godkendelser** skal du vælge linjen til dig selv og derefter vælge handlingen **Konfiguration af notifikation**.  
2.  På siden **Konfiguration af notifikation** i feltet **Notifikationstype** skal du vælge **Godkendelse**.  
3.  I feltet **Notifikationsmetode** skal du vælge **Note**.  
6.  På siden **Konfiguration af notifikation** skal du vælge handlingen **Notifikationsplan**.  
7.  I feltet **Gentagelse** på siden **Notifikationsplan** skal du vælge **Øjeblikkeligt**.  

## <a name="creating-the-approval-workflow"></a>Oprette godkendelsesarbejdsgangen  
 Opret godkendelsesarbejdsgangen for købsordren ved at kopiere trinnene fra skabelonen Arbejdsgang for godkendelse af købsordre. Lad de eksisterende trin i arbejdsgangen være uændrede, og aktiver derefter arbejdsgangen.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Sådan oprettes og aktiveres en godkendelsesarbejdsgang for en købsordre  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Arbejdsgange**, og vælg derefter det relaterede link.  
2.  På siden **Workflows** skal du vælge handlingen **Nyt workflow fra skabelon**.  
3.  På siden **Workflowskabeloner** skal du vælge workflowskabelonen Workflow for godkendelse af købsordre og derefter vælge knappen **OK**.  

    Siden **Workflow** åbnes for et nyt workflow, der indeholder alle oplysninger fra den valgte skabelon. Værdien i feltet **Kode** er udvidet med "-01" for at angive, at dette er det første workflow, som oprettes ud fra skabelonen Workflow for godkendelse af købsordre.  
5.  I hovedet af siden **Workflow** skal du markere afkrydsningsfeltet **Aktiveret**.  

## <a name="using-the-approval-workflow"></a>Bruge arbejdsgangen for godkendelse  
Brug det nye workflow Godkendelsesworkflow for købsordre ved først at logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Anna for at anmode om godkendelse af en købsordre. Log derefter ind som dig selv, åbn noten i rollecenteret, følg linket til godkendelsesanmodningen, og godkend derefter anmodningen.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Sådan anmoder du om godkendelse af en købsordre, som Anna  
1. Log ind som Anna.
2.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsordre**, og vælg derefter det relaterede link.  
3.  Vælg linjen for den åbne købsordre 106001, og vælg derefter handlingen **Rediger**.  
4.  På siden **Indkøbsordre** skal du vælge handlingen **Send godkendelsesanmodning**.  

Bemærk, at værdien i feltet **Status** er ændret til **Afventer godkendelse**.  

### <a name="to-approve-the-purchase-order-as-sean"></a>Sådan godkender du købsordren, som Søren  
1. Log ind som Søren.
2. Vælg feltet **Anmodninger til godkendelse** i rollecenteret i området **Selvbetjening**.
3. På siden **Anmodninger til godkendelse** skal du markere linjen om købsordren fra Anna og derefter vælge handlingen **Godkend**.  

Værdien i feltet **Status** i Annas købsordre ændres til **Frigivet**.  

Du har nu oprettet og testet en simpel godkendelsesarbejdsgang baseret på de to første trin i arbejdsgang Arbejdsgang for godkendelse af købsordre. Du kan nemt udvide denne arbejdsgang for at bogføre Annas købsordre automatisk, når Søren har godkendt den. For at gøre dette skal du aktivere arbejdsgangen Købsfakturaarbejdsgang, hvor svaret på en frigivet købsfaktura er at bogføre den. Først skal du ændre hændelsesbetingelsen i det første trin i arbejdsgangen fra (køb) **Faktura** til **Ordre**.  

Den generelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en række arbejdsgangskabeloner til scenarier, der understøttes af programkoden. De fleste af disse er til godkendelsesarbejdsgange.  

Du definerer arbejdsgangsvariationer ved at udfylde felter om arbejdsganglinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden. Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).  

Hvis et virksomhedsscenarie kræver en workflowhændelse eller et svar, der ikke understøttes, skal en Microsoft-partner implementere dem ved at tilpasse programkoden. Du kan finde flere oplysninger i [Gennemgang: Implementering af nye workflowhændelser og -responser](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) i hjælpen til udviklere og it-eksperter.  

## <a name="see-also"></a>Se også  
[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)   
[Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)   
[Oprette arbejdsgange](across-how-to-create-workflows.md)   
[Bruge godkendelsesworkflows](across-how-use-approval-workflows.md)   
[Workflow](across-workflow.md)  
[Bruge Business Central i et automatisk workflow](across-how-use-financials-data-source-flow.md)
