---
title: Opsætning og brug af workflow for godkendelse af køb
description: 'Denne gennemgang fører dig gennem alle de faser, der er involveret i oprettelse og brug af en arbejdsgang til købsgodkendelse, i Business central.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: edupont
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a><a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Gennemgang: Opsætning og brug af workflow for godkendelse af køb

Du kan automatisere processen med at godkende nye eller ændrede poster, f.eks dokumenter, kladdelinjer og debitorkort, ved at oprette arbejdsgange med fremgangsmåder for de pågældende godkendelser.

Før du opretter godkendelsesarbejdsgange, skal du oprette en godkender og erstatte godkenderen for hver godkendelsesbruger. Du kan også angive beløbsgrænser for godkendere for at definere, hvilke salgs- og købsposter, som de er kvalificerede til at godkende. Godkendelsesanmodninger og andre meddelelser kan sendes som mail eller intern note. For hver godkendelsesbrugeropsætning kan du også angive, hvornår der skal modtages notifikationer.

> [!NOTE]
> Ud over Workflow-funktionaliteten i [!INCLUDE[prod_short](includes/prod_short.md)] kan du bruge Power Automate til at definere workflows for hændelser i [!INCLUDE[prod_short](includes/prod_short.md)]. Vær opmærksom på, selvom det er to separate workflowsystemer, tilføjes en flow-skabelon, du opretter med Power Automate, på listen over workflowskabeloner i [!INCLUDE[prod_short](includes/prod_short.md)]. Flere oplysninger i [Bruge Business Central i et automatisk workflow](across-how-use-financials-data-source-flow.md).  

Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin. Flere oplysninger i [Workflow](across-workflow.md).  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>Om denne gennemgang

Denne gennemgang er et scenarie, der illustrerer følgende opgaver:  

- Angive indstillinger for godkendelsesbrugere  
- Oprette notifikationer til godkendelsesbrugere  
- Ændre og aktivere en godkendelsesarbejdsgang  
- Anmoder om godkendelse af en købsordre (som Alicia)  
- Modtager en besked og godkender derefter anmodningen (som Sean)  

## <a name="story"></a><a name="story"></a>Historie

Søren er superbruger hos CRONUS. Han opretter to godkendelsesbrugere. Den ene er Anna, der repræsenterer en indkøber. Den anden er ham selv, som repræsenterer Annas godkender. Søren giver derefter sig selv ubegrænsede indkøbsgodkendelsesrettigheder og angiver, at han skal modtage notifikationer via intern note, så snart en relevant hændelse finder sted. Til sidst opretter Sean den krævede godkendelsesarbejdsgang som en kopi af den eksisterende arbejdsgangskabelon *Workflow for godkendelse af købsordre*, lader alle eksisterende hændelsesbetingelser og svarmuligheder være uændrede og aktiverer arbejdsprocessen.  

For at kontrollere godkendelsesworkflowet logger Sean først på [!INCLUDE[prod_short](includes/prod_short.md)] som Alicia og anmoder derefter om godkendelse af en købsordre. Derefter logger Sean på som sig selv, ser noten i sit Rollecenter, følger linket til godkendelsesanmodningen for købsordren og godkender derefter anmodningen.  

## <a name="users"></a><a name="users"></a>Brugere

Før du kan konfigurere godkendelsesbrugere og deres notifikationsmetode, skal du kontrollere, at disse brugere findes i [!INCLUDE[prod_short](includes/prod_short.md)]: en bruger, der repræsenterer Alicia. Den anden bruger, dig selv, repræsenterer Søren. Flere oplysninger i [Oprette brugere ifølge licenser](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a><a name="setting-up-approval-users"></a>Angive indstillinger for godkendelsesbrugere

Når du er logget på som dig selv, skal du indstille Alicia som godkendelsesbruger, og hendes godkender er dig selv. Indstil dine godkendelsesrettigheder, og angiv, hvordan og hvornår du skal have besked om godkendelsesanmodninger.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a><a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Sådan opretter du dig selv og Anna som godkendelsesbrugere

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Godkendelse af brugerkonfiguration**, og vælg derefter det relaterede link.  
2. På siden **Brugeropsætning af godkendelser** skal du vælge handlingen **Ny**.  

    > [!NOTE]  
    >  Du skal oprette en godkender, før du kan konfigurere brugere, der kræver denne godkenders godkendelse. Det betyder, at du skal oprette dig selv, før du opretter Alicia.  

3. Oprette de to godkendelsesbrugere ved at udfylde felterne som beskrevet i følgende tabel.  

    |Bruger-id|Godkender-id|Ubegrænset godkendelse af køb|  
    |-------|-----------|---------------------------|  
    |DIG||Valgt|
    |ANNA|DIG||

### <a name="setting-up-notifications"></a><a name="setting-up-notifications"></a>Opsætning af meddelelser

I denne gennemgang får brugeren en besked i form af en intern note om anmodninger, der skal godkendes. Godkendelsesnotifikationer kan også sendes via mail, og du kan tilføje et trin i arbejdsgangs svaret, som giver afsenderen besked, når en anmodning godkendes eller afvises. Flere oplysninger [Angive, hvornår og hvordan notifikationer modtages](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### <a name="to-set-up-how-and-when-you-are-notified"></a><a name="to-set-up-how-and-when-you-are-notified"></a>Sådan angiver du, hvordan og hvornår du skal have besked

1. På siden **Brugeropsætning af godkendelser** skal du vælge linjen til dig selv og derefter vælge handlingen **Konfiguration af notifikation**.  
2. På siden **Konfiguration af notifikation** i feltet **Notifikationstype** skal du vælge **Godkendelse**.  
3. I feltet **Notifikationsmetode** skal du vælge **Note**.  
4. På siden **Konfiguration af notifikation** skal du vælge handlingen **Notifikationsplan**.  
5. I feltet **Gentagelse** på siden **Notifikationsplan** skal du vælge **Øjeblikkeligt**.  

## <a name="creating-the-approval-workflow"></a><a name="creating-the-approval-workflow"></a>Oprette godkendelsesworkflow

Opret godkendelsesarbejdsgangen for købsordren ved at kopiere trinnene fra skabelonen **Godkendelsesworkflow for købsordre**. Lad de eksisterende trin i arbejdsgangen være uændrede, og aktiver derefter arbejdsgangen.  

> [!TIP]
> Alternativ kan du tilføje et trin i arbejdsgangs svaret for at give afsenderen besked, når anmodningen er godkendt eller afvist. Flere oplysninger [Angive, hvornår og hvordan notifikationer modtages](across-how-to-specify-when-and-how-to-receive-notifications.md).

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a><a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Sådan oprettes og aktiveres en godkendelsesarbejdsgang for en købsordre

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflows**, og vælg derefter det relaterede link.  
2. Vælg **Handlinger** på siden **arbejdsprocesser**, vælg **Ny**, og vælg derefter den **nye arbejdsgang fra skabelon**-handling.  
3. På siden **Workflowskabeloner** skal du vælge workflowskabelonen **Workflow for godkendelse af købsordre**.  

   Siden **Workflow** åbnes for et nyt workflow, der indeholder alle oplysninger fra den valgte skabelon. Værdien i feltet **Kode** er udvidet med *-01* for at angive, at dette er det første workflow, som oprettes ud fra skabelonen **Godkendelsesworkflow for købsordre**.  
4. I hovedet af siden **Workflow** skal du markere afkrydsningsfeltet **Aktiveret**.  

## <a name="use-the-approval-workflow"></a><a name="use-the-approval-workflow"></a>Bruge godkendelsesworkflow

Brug det nye workflow Godkendelsesworkflow for købsordre ved først at logge på [!INCLUDE[prod_short](includes/prod_short.md)] som Alicia for at anmode om godkendelse af en købsordre. Log derefter ind som dig selv, åbn noten i rollecenteret, følg linket til godkendelsesanmodningen, godkend derefter anmodningen.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a><a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Sådan anmoder du om godkendelse af en købsordre, som Anna

1. Log ind som Anna.
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsordrer**, og vælg derefter det relaterede link.  
3. Marker linjen for at åbne *indkøbsordre 106001*.  
4. Vælg **Handlinger** på siden **Indkøbsordre**, derefter **Anmod om godkendelse**, og vælg derefter handlingen **Send godkendelsesanmodning**.  

Bemærk, at værdien i feltet **Status** er ændret til **Afventer godkendelse**.  

### <a name="to-approve-the-purchase-order-as-sean"></a><a name="to-approve-the-purchase-order-as-sean"></a>Sådan godkender du købsordren, som Søren

1. Log ind som Søren.
2. Vælg feltet **Anmodninger til godkendelse** i rollecenteret i området **Selvbetjening**.
3. På siden **Anmodninger til godkendelse** skal du markere linjen om købsordren fra Alicia og derefter vælge handlingen **Godkend**.  

Værdien i feltet **Status** i Annas købsordre ændres til **Frigivet**.  

Du har nu oprettet og testet en simpel godkendelsesarbejdsgang baseret på de to første trin i **Godkendelsesworkflow for godkendelse af købsordre**. Du kan nemt udvide denne arbejdsgang for at bogføre Annas købsordre automatisk, når Søren har godkendt den. For at gøre dette skal du aktivere arbejdsgangen **Købsfakturaworkflow**, så svaret på en frigivet købsfaktura er at bogføre den. Først skal du ændre hændelsesbetingelsen i det første trin i arbejdsgangen fra (køb) **Faktura** til **Ordre**.  

Den generelle version af [!INCLUDE[prod_short](includes/prod_short.md)] indeholder mange workflowskabeloner til scenarier, der understøttes af programkoden. De fleste af disse skabeloner er til godkendelsesworkflows.  

Du definerer arbejdsgangsvariationer ved at udfylde felter om arbejdsganglinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden. Flere oplysninger i [Oprette workflows](across-how-to-create-workflows.md).  

[!INCLUDE[workflow](includes/workflow.md)]

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/use-approval-workflows/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
[Konfiguration af workflownotifikationer](across-setting-up-workflow-notifications.md)  
[Opret godkendelsesworkflows](across-how-to-create-workflows.md)  
[Bruge godkendelsesworkflows](across-how-use-approval-workflows.md)  
[Workflow](across-workflow.md)  
[Bruge Business Central i et automatisk workflow](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
