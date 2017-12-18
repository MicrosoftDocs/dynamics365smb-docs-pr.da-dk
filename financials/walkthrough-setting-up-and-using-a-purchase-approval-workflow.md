---
title: "Gennemgang - Opsætning og brug af workflow for godkendelse af køb | Microsoft Docs"
description: "Du kan automatisere processen med at godkende nye eller ændrede poster, f.eks dokumenter, kladdelinjer og debitorkort, ved at oprette arbejdsgange med fremgangsmåder for de pågældende godkendelser. Før du opretter godkendelsesarbejdsgange, skal du oprette en godkender og erstatte godkenderen for hver godkendelsesbruger. Du kan også angive beløbsgrænser for godkendere for at definere, hvilke salgs- og købsposter, som de er kvalificerede til at godkende. Godkendelsesanmodninger og andre meddelelser kan sendes som mail eller intern note. For hver godkendelsesbrugeropsætning kan du også angive, hvornår der skal modtages notifikationer."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 09d48e230291524e7771d4b4305c4290bd567eb9
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Gennemgang: Opsætning og brug af workflow for godkendelse af køb
Du kan automatisere processen med at godkende nye eller ændrede poster, f.eks dokumenter, kladdelinjer og debitorkort, ved at oprette arbejdsgange med fremgangsmåder for de pågældende godkendelser. Før du opretter godkendelsesarbejdsgange, skal du oprette en godkender og erstatte godkenderen for hver godkendelsesbruger. Du kan også angive beløbsgrænser for godkendere for at definere, hvilke salgs- og købsposter, som de er kvalificerede til at godkende. Godkendelsesanmodninger og andre meddelelser kan sendes som mail eller intern note. For hver godkendelsesbrugeropsætning kan du også angive, hvornår der skal modtages notifikationer.  

 Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin. Du kan finde flere oplysninger i [Workflow](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
Denne gennemgang illustrerer følgende opgaver:  

-   Opsætning af godkendelsesbrugere (inkl. oprettelse af en bruger i Windows og [!INCLUDE[d365fin](includes/d365fin_md.md)]).  
-   Oprette notifikationer til godkendelsesbrugere.  
-   Ændre og aktivere en godkendelsesarbejdsgang.  
-   Starter opgavekøen, der afsender notifikationer.  
-   Anmoder om godkendelse af en købsordre, som Anna.  
-   Modtager en besked og godkender derefter anmodningen, som Søren.  

## <a name="prerequisites"></a>Forudsætninger  
For at gennemføre denne gennemgang skal du have demovirksomheden CRONUS Danmark A/S.

## <a name="story"></a>Historie  
Søren er superbruger hos CRONUS på sin egen computer.  

Han opretter to godkendelsesbrugere. Den ene er Anna, der repræsenterer en indkøber. Den anden er ham selv, som repræsenterer Annas godkender. Søren giver derefter sig selv ubegrænsede indkøbsgodkendelsesrettigheder og angiver, at han skal modtage notifikationer via intern note, så snart en relevant hændelse finder sted. Til sidst opretter Søren den krævede godkendelsesarbejdsgang som en kopi af den eksisterende arbejdsgangskabelon Workflow for godkendelse af købsordre, lader alle eksisterende hændelsesbetingelser og svarmuligheder være uændrede og aktiverer arbejdsprocessen.  

For at kontrollere godkendelsesworkflowet logger Søren først på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Anna og anmoder om godkendelse af en købsordre. Derefter logger Søren på som sig selv, ser noten i sit Rollecenter, følger linket til godkendelsesanmodningen for købsordren og godkender derefter anmodningen.  

## <a name="setting-up-the-sample-data"></a>Oprette eksempeldata  
Du skal oprette en ny bruger på den lokale computer og [!INCLUDE[d365fin](includes/d365fin_md.md)], der repræsenterer Anna, som du senere skal vælge som godkendelsesbruger. Din egen brugerkonto repræsenterer Søren.  

### <a name="to-add-alicia-as-a-user-on-the-local-computer"></a>Sådan tilføjes Anna som bruger på den lokale computer  

1.  Vælg **Start**, og i boksen **Søgeprogrammer og filer** skal du indtaste **Rediger lokale brugere og grupper**, og derefter vælge det relaterede link.  
2.  Åbn mappen **Brugere**.  
3.  Under fanen **Handlinger** skal du vælge **Ny bruger**.  
4.  Skriv Anna i feltet **Brugernavn**.  
5.  I felterne **Adgangskode** og **Bekræft adgangskode** skal du angive en gyldig adgangskode.  
6.  Fjern markeringen i afkrydsningsfeltet **Brugeren skal skifte adgangskode ved næste logon**.  
7.  Luk vinduet **Lokale brugere og grupper**.  

### <a name="to-add-alicia-as-a-user-in-included365finincludesd365finmdmd"></a>Sådan tilføjes Anna som bruger i [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugere**, og vælg derefter det relaterede link.  
2.  I vinduet **Windows-brugere** under fanen **Startside** i gruppen **Ny** skal du vælge **Ny**.  
3.  I vinduet **Brugerkort** i feltet **Brugernavn** skal du skrive Anna.  
4.  Vælg knappen AssistEdit i feltet **Windows-brugernavn**.  
5.  I feltet **Angiv det objektnavn, der skal vælges** i vinduet **Vælg bruger eller gruppe**, angiv Anna, og vælg derefter knappen **Kontroller navne**.  
6.  Når [COMPUTERNAVN]ANNA vises i feltet, skal du vælge knappen **OK**.  
7.  I feltet **Rettighedssæt** i oversigtspanelet **Brugerrettighedssæt** skal du vælge **SUPER**.  
8.  I feltet **Virksomhed** skal du vælge **CRONUS International Ltd.**  
9. Vælg knappen **OK**.  

## <a name="setting-up-approval-users"></a>Angive indstillinger for godkendelsesbrugere  
Ved hjælp af den Windows-bruger, du lige har oprettet, skal du oprette Anna som en godkendelsesbruger, hvis godkender er dig selv. Indstil dine godkendelsesrettigheder, og angiv, hvordan og hvornår du skal have besked om godkendelsesanmodninger.  

### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Sådan opretter du dig selv og Anna som godkendelsesbrugere  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugeropsætning af godkendelser**, og vælg derefter det relaterede link.  
2.  I vinduet **Godkendelsesopsætning** under fanen **Start** i gruppen **Ny** skal du vælge **Ny**.  

    > [!NOTE]  
    >  Du skal oprette en godkender, før du kan konfigurere brugere, der kræver denne godkenders godkendelse. Derfor skal du oprette dig selv, før du opretter Anna.  

3.  Oprette de to godkendelsesbrugere ved at udfylde felterne som beskrevet i følgende tabel.  

    |Bruger-id|Godkender-id|Ubegrænset godkendelse af køb|  
    |-------------|-----------------|---------------------------------|  
    |[COMPUTERNAVN][DIG]||Valgt|  
    |[COMPUTERNAVN]ANNA|[COMPUTERNAVN][DIG]||  

## <a name="setting-up-notifications"></a>Opsætning af meddelelser.  
Angiv, hvordan og hvornår du skal have besked om godkendelsesanmodninger.  

### <a name="to-set-up-how-and-when-you-are-notified"></a>Sådan angiver du, hvordan og hvornår du skal have besked  
1.  I vinduet **Brugeropsætning af godkendelser** skal du vælge linjen til dig selv og derefter vælge **Konfiguration af notifikation** i gruppen **Proces** under fanen **Startside**.  
2.  I vinduet **Konfiguration af notifikation** i feltet **Notifikationstype** skal du angive **Godkendelse**.  
3.  Vælg feltet **Notifikationsskabelonkode**, og vælg derefter knappen **Avanceret**.  
4.  I vinduet **Notifikationsskabeloner** under fanen **Startside** skal du i gruppen **Administrer** vælge **Rediger liste**.  
5.  På linjen for skabelonen GODKENDELSE skal du angive **Note** i feltet **Notifikationsmetode**.  
6.  Vælg knappen **OK**.  
7.  I vinduet **Konfiguration af notifikation** under fanen **Startside** i gruppen **Proces** skal du vælge **Notifikationsplan**.  
8.  I feltet **Forekomst** i vinduet **Notifikationsplan** skal du vælge **Straks**.  
9. Vælg knappen **OK**.  

## <a name="creating-the-approval-workflow"></a>Oprette godkendelsesarbejdsgangen  
 Opret godkendelsesarbejdsgangen for købsordren ved at kopiere trinnene fra skabelonen Arbejdsgang for godkendelse af købsordre. Lad de eksisterende trin i arbejdsgangen være uændrede, og aktiver derefter arbejdsgangen.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Sådan oprettes og aktiveres en godkendelsesarbejdsgang for en købsordre  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Workflows**, og vælg derefter det relaterede link.  
2.  I vinduet **Workflows** skal du under fanen **Handlinger** i gruppen **Generelt** vælge **Opret workflow fra skabelon**.  
3.  Under fanen **Handlinger** i gruppen **Generelt** skal du vælge **Opret workflow fra skabelon**. Vinduet **Workflowskabeloner** åbnes.  
4.  Vælg workflowskabelonen Workflow for godkendelse af købsordre, og vælg derefter knappen **OK**.  

    Vinduet **Workflow** åbnes for et nyt workflow, der indeholder alle oplysninger fra den valgte skabelon. Værdien i feltet **Kode** er udvidet med "-01" for at angive, at dette er det første workflow, som oprettes ud fra skabelonen Workflow for godkendelse af købsordre.  
5.  I hovedet af vinduet **Workflow** skal du markere afkrydsningsfeltet **Aktiveret**.  

## <a name="starting-a-notification-job-queue"></a>Start af en notifikationsopgavekø  
Kontroller, at opgavekøen i installationen er indstillet til at håndtere arbejdsgangsnotifikationer.  

### <a name="to-start-the-notify-job-queue"></a>Sådan starter du opgavekøen INFORMER  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opgavekøer**, og vælg derefter det relaterede link.  
2.  I vinduet **Opgavekøer** skal du vælge linjen til jobkøen INFORMER og derefter vælge **Start jobkø** i gruppen **Proces** under fanen **Startside**.  

## <a name="using-the-approval-workflow"></a>Bruge arbejdsgangen for godkendelse  
Brug det nye workflow Godkendelsesworkflow for købsordre ved første at logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Anna for at anmode om godkendelse af en købsordre. Derefter log ind som dig selv, åbn noten i rollecenteret, følg linket til godkendelsesanmodningen, og godkend derefter anmodningen.  

Hvis du vil logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] som andre brugere, skal du bruge **Kør som en anden bruger**-funktionen.  

### <a name="to-log-into-included365finincludesd365finmdmd-as-alicia"></a>Sådan logger du på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Anna  

1.  For [!INCLUDE[d365fin](includes/d365fin_md.md)]-webklienten skal du trykke på Skift + Højreklik på browserens startknap, og vælg derefter **Kør som en anden bruger**.  

    For [!INCLUDE[d365fin](includes/d365fin_md.md)]-Windows-klienten skal du trykke på Skift + Højreklik på programmets startknap, og vælg derefter **Kør som en anden bruger**.  

2.  I vinduet **Windows sikkerhed** skal angive [COMPUTERNAVN]ANNA og den nødvendige adgangskode.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Sådan anmoder du om godkendelse af en købsordre, som Anna  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsordrer**, og vælg derefter det relaterede link.  
2.  Markér linjen for den åbne købsordre 104001, og vælg derefter **Rediger** i gruppen **Administrer** under fanen **Startside**.  
3.  I vinduet **Købsordre** under fanen **Handlinger** i gruppen **Godkendelse** skal du vælge **Send godkendelsesanmodning**.  

    Bemærk, at værdien i feltet **Status** er ændret til **Afventer godkendelse**.  

4.  Luk [!INCLUDE[d365fin](includes/d365fin_md.md)].  

### <a name="to-approve-the-purchase-order-as-sean"></a>Sådan godkender du købsordren, som Søren  

1.  Åbn [!INCLUDE[d365fin](includes/d365fin_md.md)] som normalt. Programmet åbnes med dig som bruger.  
2.  I rollecentret i vinduet **Mine notifikationer** skal du se efter en ny note fra Anna.  

    > [!NOTE]  
    >  Selvom notifikationsgentagelsen er indstillet til **Straks**, ankommer noten ca. 1 min. efter, at Anna sendte godkendelsesanmodningen. Dette skyldes standardgentagelsesfrekvensen for funktionen Opgavekø.  

3.  Hvis noten skal vises i vinduet **Mine notifikationer** skal du vælge værdien **Godkendelsespost: XX, XX** i feltet **Side**. Vinduet **Anmodninger til godkendelse** åbnes med Annas anmodning om købsordren fremhævet.  
4.  I vinduet **Anmodninger til godkendelse** under fanen **Startside** i gruppen **Behandl** skal du vælge **Godkend**.  

    Værdien i feltet **Status** i Annas købsordre ændres til **Frigivet**.  

Du har nu oprettet og testet en simpel godkendelsesarbejdsgang baseret på de to første trin i arbejdsgang Arbejdsgang for godkendelse af købsordre. Du kan nemt udvide denne arbejdsgang for at bogføre Annas købsordre automatisk, når Søren har godkendt den. For at gøre dette skal du aktivere arbejdsgangen Købsfakturaarbejdsgang, hvor svaret på en frigivet købsfaktura er at bogføre den. Først skal du ændre hændelsesbetingelsen i det første trin i arbejdsgangen fra (køb) **Faktura** til **Ordre**.  

Den generelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en række arbejdsgangskabeloner til scenarier, der understøttes af programkoden. De fleste af disse er til godkendelsesarbejdsgange. Du kan finde flere oplysninger i Workflowskabeloner  

Du definerer arbejdsgangsvariationer ved at udfylde felter om arbejdsganglinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md).  

Hvis et virksomhedsscenarie kræver en workflowhændelse eller et svar, der ikke understøttes, skal en Microsoft-partner implementere dem ved at tilpasse programkoden. Du kan finde flere oplysninger i [Gennemgang: implementering af nye arbejdsgangshændelser og -svar](https://msdn.microsoft.com/en-us/library/mt574349.aspx) på MSDN.  

## <a name="see-also"></a>Se også  
[Fremgangsmåde: Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)   
[Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)   
[Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md)   
[Fremgangsmåde: Bruge godkendelsesworkflows](across-how-use-approval-workflows.md)   
[Workflow](across-workflow.md)

