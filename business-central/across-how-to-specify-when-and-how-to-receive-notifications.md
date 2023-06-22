---
title: 'Angive, hvornår og hvordan arbejdsgangsnotifikationer modtages'
description: 'Når du konfigurerer brugere i godkendelsesarbejdsgange, kan du angive, hvordan og hvornår hver godkendelsesbruger modtager beskeder.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '663, 1500, 1512, 1513,'
ms.date: 09/09/2022
ms.author: bholtorf
---
# <a name="specify-when-and-how-to-receive-workflow-notifications" />Angive, hvornår og hvordan arbejdsgangsnotifikationer modtages

Når du opretter godkendelses brugere i arbejdsprocesser, hvor du vil have, at en anden bruger skal kunne godkende ændringer, f. eks. når der oprettes nye poster, eller når en bruger anmoder om godkendelse, skal du angive, hvordan og hvornår godkendelsesbrugeren skal have besked. Du kan f. eks. angive, at en godkendelsesbruger straks skal modtage en e-mail, når nogen opretter en ny kunde. Du kan også vælge at planlægge, at notifikationer skal holdes og leveres sammen, f. eks. en gang om ugen eller måneden.

Brugere kan også ændre deres opsætning ved at klikke på knappen **Rediger notifikationsindstillinger** i en vilkårlig notifikation.  

> [!NOTE]
> Notifikationer leveres i overensstemmelse med beskedindstillingerne for modtageren, ikke afsenderen. Dette er en vigtig forskel, fordi det betyder, at når en bruger anmoder om godkendelse som en del af en arbejdsproces, sendes deres anmodning ikke med det samme. Den leveres i stedet i henhold til den notifikationsplan, der er angivet i meddelelsesindstillingerne for godkenderen.

Før du kan konfigurere en godkendelsesbrugers notifikationsindstillinger, skal du konfigurere brugeren som godkendelsesbruger. Flere oplysninger i [Konfigurere godkendte brugere](across-how-to-set-up-approval-users.md).  

> [!NOTE]
> Hvis du vil bruge e-mail som beskedmetode, skal du konfigurere e-mail til både afsender og modtager i [!INCLUDE [prod_short](includes/prod_short.md)]. Flere oplysninger i [Konfigurer e-mail](admin-how-setup-email.md).

## <a name="steps-in-workflows" />Trin i Workflows

Mange trin i et godkendelsesworkflow vedrører notifikationer til brugere om, at der er en hændelse, som de skal reagere på. I ét arbejdsgangstrin kan hændelsen f.eks. være, at bruger 1 anmoder om godkendelse af en ny post. Det relaterede svar er, at der er sendt en notifikation til bruger 2, godkenderen. På det næste trin i arbejdsgangen kan hændelsen være, at bruger 2 godkender posten. Det relaterede svar er, at er sendt en notifikation til bruger 3 om at starte en proces med den godkendte post. For workflowtrin, der vedrører godkendelse, er hver notifikation knyttet til en godkendelsespost. Flere oplysninger i [Workflow](across-workflow.md).  

## <a name="specify-when-and-how-approval-users-receive-notifications" />Angive, hvornår og hvordan godkendelsesbrugere modtager notifikationer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Godkendelse af brugerkonfiguration**, vælg det relaterede link.  
2. Vælg linjen med den bruger, du vil konfigurere notifikationsindstillinger for, og vælg derefter handlingen **Konfiguration af notifikation**.  
3. På siden **Konfiguration af notifikation om arbejdsgang** skal du udfylde felterne som beskrevet i følgende tabel.  

   > [!NOTE]
   > Hvis du åbner siden med **Konfiguration af notifikation om arbejdsgang** fra siden **Brugeropsætning af godkendelser**, er notifikationsopsætningen knyttet til godkendelsesbrugeren. Godkendelsesbrugeren vil altid modtage beskeder om arbejdsgangen ifølge denne Notifikationsopsætning. Hvis du bruger *Fortæl mig*-funktionen til at åbne siden **Konfiguration af notifikation om arbejdsgang**, vil notifikationskonfigurationen gælde for alle brugere.

   |Felt|Beskrivelse|
   |-----|-----------|
   |**Notifikationstype**|Angiv, hvilken type hændelse notifikationen drejer sig om.<br /><br /> Vælg en af følgende indstillinger:<br /><br /> -   **Ny post** angiver, at notifikationen drejer sig om en ny post, f.eks. et dokument, som brugeren skal reagere på.<br />-   **Godkendelse** angiver, at notifikationen drejer sig om en eller flere godkendelsesanmodninger.<br />-   **Forfalden** angiver, at notifikationen skal bruges til at minde brugerne om, at fristen for at reagere på en hændelse er overskredet.|
   |**Notifikationsmetode**|Angiv, om notifikationen er en mail eller en intern note.|

   Du kan definere layoutet af e-mailmeddelelserne ved at tilpasse rapporten 1320, Notifikationsmail. Flere oplysninger [Opret og ændr brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md).

   Du har nu angivet, hvordan brugeren får notifikationer. Fortsæt med at angive, hvor brugeren får notifikationer.  
4. Vælg handlingen **Notifikationsplan**.  
5. På siden **Notifikationsplan** skal du udfylde felterne som beskrevet i følgende tabel.  

   |Felt|Beskrivelse|
   |-----|-----------|
   |**Gentagelse**|Angiv det gentagelsesmønster, som notifikationer sendes efter.|
   |**Tidspunkt**|Angiv det tidspunkt på dagen, hvor brugeren modtager notifikationer, når værdien i feltet **Gentagelse** er forskellig fra **Øjeblikkeligt**.|
   |**Daglig frekvens**|Angiv, hvilken type dage brugeren får notifikationer, når værdien i feltet **Gentagelse** er **Dagligt**.<br /><br /> Vælg **Ugedag** for at modtage notifikationer hver arbejdsdag i arbejdsugen. Vælg **Dagligt** for at modtage notifikationer hver arbejdsdag i ugen inklusive weekender.|
   |**Mandag** til **søndag**|Angiv, hvilken type dage brugeren får notifikationer, når værdien i feltet **Gentagelse** er **Ugentligt**.|
   |**Dato i måned**|Angiv, om brugeren får vist meddelelser på første, sidste eller en bestemt dato i måneden.|
   |**Månedlig notifikationsdato**|Angiv den dato i måneden, hvor brugeren modtager notifikationer, når værdien i feltet **Dato i måned** er **Brugerdefineret**.|

## <a name="change-when-and-how-you-receive-notifications" />Rediger, hvornår og hvordan du modtager notifikationer

1. På en af de notifikationer, du har modtaget, enten som mail eller note, skal du klikke på knappen **Rediger notifikationsindstillinger**.  
2. På siden **Konfiguration af notifikation om arbejdsgang** skal du ændre dine indstillinger som beskrevet i trin 3-5 ovenfor.
   1. Kontroller, at der er valgt den rette notifikation under feltet **Notifikationstype**.
   2. Vælg, om der skal modtages en mail-eller note under feltet **Notifikationsmetode**.
   3. Vælg en **Notifikationsplan** for at ændre den hyppighed og gentagelse, der sendes beskeder til.

## <a name="see-also" />Se også

[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
[Sådan opretter og ændrer du Brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md)  
[Konfiguration af workflow-godkendelsesnotifikationer](across-setting-up-workflow-notifications.md)  
[Konfigurere godkendelsesworkflows](across-set-up-workflows.md)  
[Bruge godkendelsesworkflows](across-use-workflows.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
