---
title: Konfigurer maillogføring
description: 'Få at vide, hvordan du ændrer mailinteraktioner mellem sælgere og kunder til reelle salgs-leads.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 09/18/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect, opportunity, email'
ms.search.form: '1680, 1811, 5076'
ms.service: dynamics-365-business-central
---
# Spore udveksling af mails mellem sælgere og kontakter

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Få mere ud af kommunikationen mellem sælgerne og kunder ved at omdanne udveksling af mails til handlingsrettede salgsmuligheder. [!INCLUDE[prod_short](includes/prod_short.md)] kan bruges sammen med Exchange Online til at føre en log over indgående og udgående meddelelser. Du kan få vist og analysere indholdet af hver meddelelse på siden **Interaktionslogposter**.

> [!IMPORTANT]
> Til [!INCLUDE[prod_short](includes/prod_short.md)] online [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online skal være på samme lejer.

## Sådan konfigureres maillogføring

### Konfigurere offentlige mapper og regler for maillogføring i Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Derefter opretter du forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online.

### Konfigurere en delt postkasse og regler for e-maillogføring i Exchange Online

> [!NOTE]
> Disse trin kræver administratoradgang til Exchange Online.

Oprette en delt postkasse i Exchange Administration. Du kan også bruge Exchange Online PowerShell. Du kan finde flere oplysninger i [Oprette en delt postkasse](/microsoft-365/admin/email/create-a-shared-mailbox) eller [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Hvis du bruger Exchange Management PowerShell, bliver ændringerne synlige i Exchange Administration efter en forsinkelse. Forsinkelsen kan være flere timer.

### Tilføje en brugerkonto for medlemmer af den delte postkasse

Den konto, du skal bruge til e-maillogføring, er en Exchange Online-konto. Det planlagte job kan anvende kontoen til at oprette forbindelse til den delte postkasse og behandle mails. Denne konto må ikke knyttes til en bestemt person. Føj e-mailkontoen til medlemmerne af den delte postkasse. Du kan finde flere oplysninger i [Brug EAC til at redigere delt postkassedelegering](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### Tillad andre brugere at se logførte e-mails

Du kan tillade, at en anden bruger åbner en e-mailmeddelelse i Exchange, som er relateret til en Interaktions-logpost fra [!INCLUDE[prod_short](includes/prod_short.md)]. For at gøre dette skal du give brugeren ``Read``-tilladelse til **Arkiv**-mappen i den delte postkasse. Du kan også finde yderligere oplysninger under [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### Oprette regler for mail flow

Regler for e-mailflow undersøger, om der er specifikke betingelser for meddelelser, og agerer efterfølgende. Opret to regler for mailflow på grundlag af oplysningerne i følgende tabel. Du kan finde flere oplysninger i [Administrere regler for mailflow i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) og [Handlinger for mailflowregel i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Formål  |Name  |Anvend denne regel, hvis...  |Benyt følgende fremgangsmåde...  |
|---------|---------|---------|---------|
|En regel for indgående mail     |Logfør mails, der er sendt til denne organisation|Afsenderen er placeret uden for organisationen, og modtageren er placeret inde i organisationen|BCC den mailkonto, der er angivet for den delte postkasse.|
|En regel for udgående mail     |Logfør mails, der er sendt fra denne organisation|Afsenderen er placeret inde i organisationen, og modtageren er placeret uden for organisationen.|BCC den mailkonto, der er angivet for den delte postkasse.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] behandler kun meddelelser i mappen Indbakke i den delte postkasse. Hvis en regel flytter meddelelser fra indbakken til en anden mappe, bliver disse meddelelser ikke behandlet. Meddelelser i mappen Uønsket post ignoreres desuden.

## Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til logføring af mails

Introduktion til maillogføring i to lette trin:

1. Opret forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online for dit Microsoft 365-abonnement. Exchange Online håndterer dine mails. Vi har gjort dette trin lettilgængeligt med en vejledning til assisteret opsætning. Du skal blot bruge dine administratorrettigheder til din administratorkonto i Microsoft 365. Start vejledningen ved at gå til **Assisteret opsætning**, og vælg derefter vejledningen **Konfigurer maillogføring**.  

2. Kontroller, at e-mail-adresserne for dine sælgere og kontakter i [!INCLUDE[prod_short](includes/prod_short.md)] er gyldige. Hvis du vil gøre det, skal du for hver debitor eller sælger åbne kortet **Kontakt** eller **Sælger/indkøber** og se feltet **Mailadresse**.

    > [!Tip]
    > Når du har udført trinnene i programguiden, kan du kontrollere, om forbindelsen er oprettet. Søg efter **E-maillogføring**, vælg **Handlinger** og derefter **Valider opsætning**.

## Vise udveksling af mails i interaktionslogposten

[!INCLUDE[prod_short](includes/prod_short.md)] opretter en post på siden **Interaktionslog**, hver gang en sælger og en kontakt udveksler en mail. Du kan få vist interaktionsloggen ved at åbne kortet **Kontakt** for personen, vælge **Relaterede**, og derefter vælge **Historik** og **Interaktionslogposter**. Der er nogle få ting, der kan udføres for hver indtastning i logfilen, f.eks.:

* Få vist indholdet af den mail, der blev udvekslet, ved at vælge **Behandle** og derefter **Vis vedhæftede filer**.
* Omdanne en e-mailudveksling til en salgsmulighed. Hvis en post ser lovende ud, kan du gøre den til en lead og derefter styre forløbet hen imod et salg. Hvis du vil aktivere en e-mail-udveksling til en salgsmulighed, skal du vælge posten, derefter **Behandle** og derefter **Opret en salgsmulighed**. Du kan finde flere oplysninger i [Administrere salgsleads](marketing-manage-sales-opportunities.md).

## Postkasse og mappegrænser i Exchange Online

Der findes postkasse- og mappe grænser i Exchange Online, f. eks. grænser for mappestørrelser og antallet af meddelelser. Du kan finde flere oplysninger i [Exchange Online-grænser](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) og [Grænser for offentlige mapper i Exchange Server](/Exchange/collaboration/public-folders/limits?view=exchserver-2019&preserve-view=true).

[!INCLUDE[prod_short](includes/prod_short.md)] gemmer registrerede e-mails i en mappe i Exchange Online. [!INCLUDE[prod_short](includes/prod_short.md)] gemmer også et hyperlink til hver enkelt registreret meddelelse. Hyperlinks åbner de registrerede meddelelser i Exchange Online fra interaktionslogposter, kontaktkort og sælgerkort i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis en registreret meddelelse flyttes til en anden mappe, vil kæden være brudt. Du kan f. eks. flytte en meddelelse manuelt eller Exchange Online starter evt. automatisk opsplitning, når du har nået en lagergrænse.

Følgende trin kan være en hjælp til at undgå, at du bryder om meddelelser i Exchange Online.

1. Flyt ikke eksisterende meddelelser til en anden mappe, når du har ændret indstillingerne for opsætningen af e-mail-logføringen. Hvis du beholder eksisterende meddelelser, bliver hyperlinkene bevaret. Links til meddelelser i den nye mappe vil være gyldige.
2. Undgå at få adgang til postkasse-og mappe grænserne. Hvis du er ved at nå en grænse, skal du gøre følgende:
    1. Opret en ny delt postkasse i Exchange Online.
    2. Opdater dine e-mail-flow regler i Exchange Online.
    3. Opdater din opsætning af e-mail-logføring i Business Central

## Tilslut lokale versioner til Microsoft Exchange

Du kan oprette forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange on-premises eller Exchange Online til e-maillogføring. For begge versioner af Exchange er indstillingerne for forbindelsen tilgængelige på siden **Marketingopsætning**. I Exchange Online kan du også bruge en assisteret installationsvejledning.

<!-- [!IMPORTANT]
> The new experience doesn't support a connection to Exchange on-premises. If you must use Exchange on-premises, do not enable the feature update for the new experience.

## Connect to Exchange on-premises
<!--
## [Current Experience](#tab/current-experience)
To connect [!INCLUDE[prod_short](includes/prod_short.md)] on-premises to Exchange on-premises, on the **Marketing Setup** page, you can use **Basic** as the **Authentication Type**, and then enter credentials for the user account for Exchange on-premises. Then turn on the **Enabled** toggle to start logging email.

## [New Experience](#tab/new-experience)
The new experience does not support connections to Exchange on-premises.
-->
## Opret forbindelse til Exchange Online

Hvis du vil oprette forbindelse til Exchange Online, skal du registrere et program i Microsoft Entra ID. Angiv program-id, key vault-hemmeligheden og omdirigere den URL-adresse, der skal bruges til registrering. URL-adressen til omdirigering er forudindstillet og bør fungere for de fleste installationer. Du kan finde flere oplysninger i [Sådan registreres et program i Microsoft Entra ID for at oprette forbindelse fra Business Central til Exchange Online](#to-register-an-application-in-microsoft-entra-id-for-connecting-from-business-central-to-exchange-online). 

Du skal også bruge **OAuth2** som **Godkendelsestype**. Du skal også registrere et program i Microsoft Entra ID. Angiv program-id, key vault-hemmeligheden og omdirigere den URL-adresse, der skal bruges til registrering. URL-adressen til omdirigering er forudindstillet og bør fungere for de fleste installationer. Du kan finde flere oplysninger i Sådan registreres et program i Microsoft Entra ID for at oprette forbindelse fra Business Central til Exchange Online herunder.

Du skal konfigurere installationen til at bruge HTTPS. Du kan finde flere oplysninger i [Konfigurere SSL for at sikre forbindelsen til Business Central-webklienten](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Hvis du konfigurerer serveren, så den har en anden startside, kan du altid ændre URL-adressen. Klientens hemmelighed gemmes som en krypteret streng i din database.

### Sådan registrerer du et program i Microsoft Entra ID for at oprette forbindelse fra Business Central til Exchange Online

I følgende trin antages det, at du bruger Microsoft Entra ID til at administrere identiteter og adgangsrettigheder. Du kan finde flere oplysninger om registrering af et program i [Hurtig start: Registrere et program på Microsoft-identitetsplatformen](/azure/active-directory/develop/quickstart-register-app). 

1. Vælg **Godkend** under **Administrer** i på Azure-portalen.
2. Tilføj under **Omdirigerer URL-adresse**, og omdiriger den URL-adresse, der er angivet på siden **E-mail-logføring** i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis URL-adressen til omdirigering på siden E-mail-logføring er tom, skal du finde den foreslåede URL-adresse til omdirigering på siden **Assisteret opsætning**. Hvis du vil åbne siden, skal du på siden **E-mail-logføring** vælge **Handlinger** og derefter **Assisteret opsætning**.

    > [!NOTE]
    > Hvis du ikke angiver URL-adressen til omdirigering, kan du gøre det senere ved at vælge **Tilføj en platform** og derefter vælge **Web**-sted for at tilføje webprogrammet og URL-adressen til omdirigering.

3. Vælg **API-tilladelser** under **Administrer**, og vælg **Microsoft Graph** og derefter **Delegerede tilladelser**.
4. Brug søgefeltet til at finde og vælge **E-mail**, og tilføj derefter tilladelsen **Mail.ReadWrite.Shared**. 
5. Vælg **Certifikater og hemmeligheder** under **Administrer**, og opret derefter en ny hemmelighed til din app. Du skal bruge hemmeligheden enten i feltet **Klienthemmelighed** på siden **E-mail-logføring** i [!INCLUDE[prod_short](includes/prod_short.md)].
6. Vælg **Oversigt**, og find derefter **Program-id (klient)**-værdien . Dette er programmets klient-id. Du skal angive enten i feltet **Klient-id** på siden **E-mail-logføring**.
7. I [!INCLUDE[prod_short](includes/prod_short.md)] skal du oprette e-mail-logføring på siden **E-mail-logføring** eller bruge guiden **Assisteret opsætning** til at få hjælp.

### Bruge en anden tjeneste til identitets- og adgangsstyring

Hvis du ikke bruger Microsoft Entra ID til at administrere identiteter og adgangsrettigheder, skal du have hjælp fra en udvikler. Hvis du foretrækker at gemme app-id'et og hemmeligheden et andet sted, kan du lade felterne Klient-id og Klienthemmelighed være tomme og skrive en udvidelse for at hente id'et og hemmeligheden fra placeringen. Du kan levere hemmeligheden på kørselstidspunktet ved at abonnere på OnGetEmailLoggingClientId- og OnGetEmailLoggingClientSecret-hændelserne i codeunit 1641 "Opsætning af e-mail".

## Sådan startes logføring af e-mails

1. Start logføring af e-mail ved at aktivere til/fra-feltet **Aktiveret** på siden **E-mail-logføring**.
2. Log på med Exchange Online-kontoen, som det planlagte job kan anvende kontoen til at oprette forbindelse til den delte postkasse og behandle mails.

    > [!NOTE]
    > Hvis du ikke bliver bedt om at logge på Exchange Online-kontoen, skyldes det sandsynligvis, at din browser blokerer pop op-vinduer. Du kan logge på ved at tillade pop op-vinduer fra https://login.microsoftonline.com.

## Sådan stoppes logføring af e-mails

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **E-mail-logføring**, og vælg derefter det relaterede link.
2. Deaktiver **Aktiveret** til/fra.

## Sådan ændres den brugerkonto, der bruges til e-mail-logføring

### [!INCLUDE[prod_short](includes/prod_short.md)] Online

1. Log på [!INCLUDE[prod_short](includes/prod_short.md)]-kontoen, med den konto, som det planlagte job kan anvende til at oprette forbindelse til den delte postkasse og behandle mails. Denne konto skal have adgang til både [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online.
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **E-mail-logføring**, og vælg derefter det relaterede link. 
3. Vælg **Relateret**, og klik derefter på **Opgavekøpost**.
4. Genstart **E-mail-logføring**-opgave.

### [!INCLUDE[prod_short](includes/prod_short.md)] lokalt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **E-mail-logføring**, og vælg derefter det relaterede link.
2. Vælg **Handlinger**, og derefter **Forny token**.
3. Log på med Exchange Online-kontoen, som det planlagte job kan anvende kontoen til at oprette forbindelse til den delte postkasse og behandle mails.

## Se også
[Styre relationer](marketing-relationship-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]