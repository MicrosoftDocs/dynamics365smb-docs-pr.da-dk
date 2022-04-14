---
title: Konfigurer maillogføring
description: Få at vide, hvordan du ændrer mailinteraktioner mellem sælgere og kunder til reelle salgs-leads.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 03/22/2022
ms.search.form: 1680, 1811, 5076
ms.author: bholtorf
ms.openlocfilehash: fc755362a5b29cca9eb8e8e403374e173cff3630
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516131"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Spore udveksling af mails mellem sælgere og kontakter
Få mere ud af kommunikationen mellem sælgerne og kunder ved at omdanne udveksling af mails til handlingsrettede salgsmuligheder. [!INCLUDE[prod_short](includes/prod_short.md)] kan bruges sammen med Exchange Online til at føre en log over indgående og udgående meddelelser. Du kan få vist og analysere indholdet af hver meddelelse på siden **Interaktionslogposter**.

> [!NOTE]
> I 2022 udgivelsesbølge 1 har vi strømlinet processer til konfiguration af e-maillogføring for at øge fleksibilitet og sikkerhed. Hvis du er ny kunde, der bruger den version, bruger du den nye oplevelse. Hvis du allerede bruger den nye oplevelse, afhænger det af, om din administrator har aktiveret funktionsopdateringen **Maillogføring ved hjælp af Microsoft Graph API** på siden **Funktionsadministration**. Du kan finde flere oplysninger i [Aktivere Upcoming Features Ahead of Time](/dynamics365/business-central/dev-itpro/administration/feature-management).

> [!IMPORTANT]
> For [!INCLUDE[prod_short](includes/prod_short.md)] at være online kræver den nye oplevelse, at [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online er på samme lejer.

## <a name="to-set-up-email-logging"></a>Sådan konfigureres maillogføring
Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Maillogføring ved hjælp af Microsoft Graph API** til. Hvis funktionsopdateringen ikke er aktiveret, skal du følge fremgangsmåden under fanen **Aktuel oplevelse**.

## <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience)

### <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Konfigurere offentlige mapper og regler maillogføring i Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Derefter opretter du forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online.

## <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience)
### <a name="set-up-a-shared-mailbox-and-rules-for-email-logging-in-exchange-online"></a>Konfigurere en delt postkasse og regler for e-maillogføring i Exchange Online

> [!NOTE]
> Disse trin kræver administratoradgang til Exchange Online.

Oprette en delt postkasse i Exchange Administration. Du kan også bruge Exchange Online PowerShell. Du kan finde flere oplysninger i [Oprette en delt postkasse](/microsoft-365/admin/email/create-a-shared-mailbox) eller [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Hvis du bruger Exchange Management PowerShell, bliver ændringerne synlige i Exchange Administration efter en forsinkelse. Forsinkelsen kan være flere timer.

### <a name="add-a-user-account-for-members-of-the-shared-mailbox"></a>Tilføje en brugerkonto for medlemmer af den delte postkasse
Den konto, du skal bruge til e-maillogføring, er en Exchange Online-konto. Det planlagte job kan anvende kontoen til at oprette forbindelse til den delte postkasse og behandle mails. Denne konto må ikke knyttes til en bestemt person. Føj e-mailkontoen til medlemmerne af den delte postkasse. Du kan finde flere oplysninger i [Brug EAC til at redigere delt postkassedelegering](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### <a name="allow-other-users-to-see-logged-emails"></a>Tillad andre brugere at se logførte e-mails
Du kan tillade, at en anden bruger åbner en e-mailmeddelelse i Exchange, som er relateret til en Interaktions-logpost fra [!INCLUDE[prod_short](includes/prod_short.md)]. For at gøre dette skal du give brugeren ``Read``-tilladelse til **Arkiv**-mappen i den delte postkasse. Du kan også finde yderligere oplysninger under [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### <a name="create-mail-flow-rules"></a>Oprette regler for mail flow
Regler for e-mailflow undersøger, om der er specifikke betingelser for meddelelser, og agerer efterfølgende. Opret to regler for mailflow på grundlag af oplysningerne i følgende tabel. Du kan finde flere oplysninger i [Administrere regler for mailflow i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) og [Handlinger for mailflowregel i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Formål  |Name  |Anvend denne regel, hvis...  |Benyt følgende fremgangsmåde...  |
|---------|---------|---------|---------|
|En regel for indgående mail     |Logfør mails, der er sendt til denne organisation|Afsenderen er placeret uden for organisationen, og modtageren er placeret inde i organisationen|BCC den mailkonto, der er angivet for den delte postkasse.|
|En regel for udgående mail     |Logfør mails, der er sendt fra denne organisation|Afsenderen er placeret inde i organisationen, og modtageren er placeret uden for organisationen.|BCC den mailkonto, der er angivet for den delte postkasse.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] behandler kun meddelelser i mappen Indbakke i den delte postkasse. Hvis en regel flytter meddelelser fra indbakken til en anden mappe, bliver disse meddelelser ikke behandlet. Meddelelser i mappen Uønsket post ignoreres desuden. 

---

## <a name="setting-up-prod_short-to-log-email-messages"></a>Oprette [!INCLUDE[prod_short](includes/prod_short.md)] til logføring af mails
Disse trin er de samme for både aktuelle og nye erfaringer.

Introduktion til maillogføring i to lette trin:

1. Opret forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online for dit Microsoft 365-abonnement. Exchange Online håndterer dine mails. Vi har gjort dette trin lettilgængeligt med en vejledning til assisteret opsætning. Du skal blot bruge dine administratorrettigheder til din administratorkonto i Microsoft 365. Start vejledningen ved at gå til **Assisteret opsætning**, og vælg derefter vejledningen **Konfigurer maillogføring**.  

2. Kontroller, at e-mail-adresserne for dine sælgere og kontakter i [!INCLUDE[prod_short](includes/prod_short.md)] er gyldige. Hvis du vil gøre det, skal du for hver debitor eller sælger åbne kortet **Kontakt** eller **Sælger/indkøber** og se feltet **Mailadresse**.

> [!Tip]
> Når du har udført trinnene i programguiden, kan du kontrollere, om forbindelsen er oprettet. Afhængigt af om du bruger den aktuelle eller nye exerience, skal du benytte en af følgende fremgangsmåder: 
>
> * **Aktuel oplevelse**: Søg efter **Marketingopsætning**, vælg **Adgang**, derefter **Funktioner** og til sidst **Valider opsætning af mail-logføring**.
> * **Ny oplevelse**: Søg efter **E-mail-logføring**, vælg **Handlinger** og derefter **Valider opsætning**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Få vist udveksling af mails i interaktionslogposten

[!INCLUDE[prod_short](includes/prod_short.md)] opretter en post på siden **Interaktionslog**, hver gang en sælger og en kontakt udveksler en mail. Du kan få vist interaktionsloggen ved at åbne kortet **Kontakt** for personen, vælge **Relaterede**, og derefter vælge **Historik** og **Interaktionslogposter**. Der er nogle få ting, der kan udføres for hver indtastning i logfilen, f.eks.:

- Få vist indholdet af den mail, der blev udvekslet, ved at vælge **Behandle** og derefter **Vis vedhæftede filer**.
- Omdanne en e-mailudveksling til en salgsmulighed. Hvis en post ser lovende ud, kan du gøre den til en lead og derefter styre forløbet hen imod et salg. Hvis du vil aktivere en e-mail-udveksling til en salgsmulighed, skal du vælge posten, derefter **Behandle** og derefter **Opret en salgsmulighed**. Du kan finde flere oplysninger i [Administrere salgsleads](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>Tilslutning af lokale versioner til Microsoft Exchange

Du kan oprette forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange on-premises eller Exchange Online til e-maillogføring. For begge versioner af Exchange er indstillingerne for forbindelsen tilgængelige på siden **Marketingopsætning**. I Exchange Online kan du også bruge en assisteret installationsvejledning.

> [!IMPORTANT]
> Den nye oplevelse understøtter ikke en forbindelse til Exchange on-premises. Hvis du skal bruge Exchange på stedet, skal du ikke aktivere funktions opdateringen til den nye oplevelse.

## <a name="connecting-to-exchange-on-premises"></a>Oprettelse af forbindelse til On-premises
## <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience)
Hvis du vil tilslutte [!INCLUDE[prod_short](includes/prod_short.md)] on-premises til Exchange on-premises på siden **Marketingopsætning** kan du bruge **Basis** som **Godkendelsestype** og derefter angive legitimationsoplysninger til brugerkontoen for Exchange on-premises. Aktiver derefter **Aktiveret** til/fra for at starte logføring af e-mails.

## <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience)
Den nye oplevelse understøtter ikke forbindelser til Exchange on-premises.

---

## <a name="connecting-to-exchange-online"></a>Forbindelse til Exchange Online
Hvis du vil oprette forbindelse til Exchange Online, skal du registrere et program i Azure Active Directory. Angiv program-id, key vault-hemmeligheden og omdirigere den URL-adresse, der skal bruges til registrering. URL-adressen til omdirigering er forudindstillet og bør fungere for de fleste installationer. Du kan finde flere oplysninger i [Sådan registreres et program i Azure AD for at oprette forbindelse fra Business Central til Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Du skal også bruge **OAuth2** som **Godkendelsestype**. Du skal også registrere et program i Azure Active Directory. Angiv program-id, key vault-hemmeligheden og omdirigere den URL-adresse, der skal bruges til registrering. URL-adressen til omdirigering er forudindstillet og bør fungere for de fleste installationer. Du kan finde flere oplysninger i Sådan registreres et program i Azure AD for at oprette forbindelse fra Business Central til Exchange Online herunder.

Du skal konfigurere installationen til at bruge HTTPS. Du kan finde flere oplysninger i [Konfigurere SSL for at sikre forbindelsen til Business Central-webklienten](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Hvis du konfigurerer serveren, så den har en anden startside, kan du altid ændre URL-adressen. Klientens hemmelighed gemmes som en krypteret streng i din database.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Sådan registrerer du et program i Azure AD for at oprette forbindelse fra Business Central til Exchange Online
I følgende trin antages det, at du bruger Azure Active Directory til at administrere identiteter og adgangsrettigheder. Du kan finde flere oplysninger om registrering af et program i [Hurtig start: Registrere et program på Microsoft-identitetsplatformen](/azure/active-directory/develop/quickstart-register-app). 

## <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience) 
I følgende trin antages det, at du bruger Azure Active Directory til at administrere identiteter og adgangsrettigheder. Du kan finde flere oplysninger om registrering af et program i [Hurtig start: Registrere et program på Microsoft-identitetsplatformen](/azure/active-directory/develop/quickstart-register-app). Hvis du ikke bruger Azure Active Directory, kan du se [Bruge en anden tjeneste til identitets- og adgangsstyring](marketing-set-up-email-logging.md#use-another-identity-and-access-management-service). 

1. Vælg **Godkend** under **Administrer** i på Azure-portalen.
2. Tilføj under **Omdirigerer URL-adresse**, og omdiriger den URL-adresse, der er angivet på siden **Marketingopsætning** i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis URL-adressen til omdirigering på siden Marketingopsætning er tom, skal du finde den foreslåede URL-adresse til omdirigering på siden **Assisteret opsætning af maillogføring**.

    > [!NOTE]
    > Hvis du ikke angiver URL-adressen til omdirigering, kan du gøre det senere ved at vælge **Tilføj en platform** og derefter vælge **Web**-sted for at tilføje webprogrammet og URL-adressen til omdirigering. 

3. Vælg **Manifest** under **Administrer**.
4. Find egenskaben **requiredResourceAccess** i manifestet, og tilføj følgende kode i kantede parenteser ([]) for at tilføje de nødvendige tilladelser. Du kan finde flere oplysninger i [Registrere dit program](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth#register-your-application).

```
{
    "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    "resourceAccess": [
        {
            "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
            "type": "Scope"
        },
        {
            "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
            "type": "Role"
        }
    ]
}
```

5. Vælg **Gem**.
6. Vælg **API-tilladelser** under **Vælg**, og bekræft derefter, at følgende tilladelser er angivet:  

    * EWS.AccessAsUser.All
    * full_access_as_app

7. Vælg **Certifikater og hemmeligheder** under **Administrer**, og opret derefter en ny hemmelighed til din app. Du skal enten angive hemmeligheden på [!INCLUDE[prod_short](includes/prod_short.md)], i feltet **Klienthemmelighed** på siden **Marketingopsætning** eller gemme det i et sikkert lager og angive det i en hændelsesabonnent.
8. Vælg **Oversigt**, og find derefter **Program-id (klient)**-værdien . **Program (klient)-ID**-værdien er klient-id for dit program. Du skal angive klient-id på siden **Marketingopsætning**, i feltet **Klient-id** eller gemme det i et sikkert lager og angive det i en hændelsesabonnent.
9. I [!INCLUDE[prod_short](includes/prod_short.md)] skal du oprette maillogføring på siden **Marketingopsætning** eller bruge guiden **Assisteret opsætning af maillogføring** til at få hjælp.
    * Angiv mailkonto for brugeren, på hvis vegne den planlagte sag vil oprette forbindelse til Exchange Online og behandle mails. Brugeren skal have en gyldig licens til Exchange Online.
    * Angiv URL-adressen til din Exchange Online. Denne URL-adresse er normalt det domæne, som du har angivet i brugerens e-mail-adresse.
    * Angiv **Kømappesti** og **lagringsmappesti**.
10. Start logføring af e-mails ved at aktivere **Aktiveret** til/fra.
11. Log på med din administratorkonto til Azure Active Directory (kontoen skal have en gyldig licens til Exchange og være administrator i Exchange Online). Når du er logget på, bliver du bedt om at tillade, at dit registrerede program logger på Exchange Online på vegne af organisationen. Du skal give samtykke for at fuldføre installationen.

   > [!NOTE]
   > Hvis du ikke bliver bedt om at logge på med din administratorkonto, skyldes det sandsynligvis, at pop op-vinduer er blokeret. Du kan logge på ved at tillade pop op-vinduer fra https://login.microsoftonline.com.

## <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience)
1. Vælg **Godkend** under **Administrer** i på Azure-portalen.
2. Tilføj under **Omdirigerer URL-adresse**, og omdiriger den URL-adresse, der er angivet på siden **E-mail-logføring** i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis URL-adressen til omdirigering på siden E-mail-logføring er tom, skal du finde den foreslåede URL-adresse til omdirigering på siden **Assisteret opsætning**. Hvis du vil åbne siden, skal du på siden **E-mail-logføring** vælge **Handlinger** og derefter **Assisteret opsætning**.

    > [!NOTE]
    > Hvis du ikke angiver URL-adressen til omdirigering, kan du gøre det senere ved at vælge **Tilføj en platform** og derefter vælge **Web**-sted for at tilføje webprogrammet og URL-adressen til omdirigering.

3. Vælg **API-tilladelser** under **Administrer**, og vælg **Microsoft Graph** og derefter **Delegerede tilladelser**.
4. Brug søgefeltet til at finde og vælge **E-mail**, og tilføj derefter tilladelsen **Mail.ReadWrite.Shared**. 
5. Vælg **Certifikater og hemmeligheder** under **Administrer**, og opret derefter en ny hemmelighed til din app. Du skal bruge hemmeligheden enten i feltet **Klienthemmelighed** på siden **E-mail-logføring** i [!INCLUDE[prod_short](includes/prod_short.md)].
6. Vælg **Oversigt**, og find derefter **Program-id (klient)**-værdien . Dette er programmets klient-id. Du skal angive enten i feltet **Klient-id** på siden **E-mail-logføring**.
7. I [!INCLUDE[prod_short](includes/prod_short.md)] skal du oprette e-mail-logføring på siden **E-mail-logføring** eller bruge guiden **Assisteret opsætning** til at få hjælp.

### <a name="use-another-identity-and-access-management-service"></a>Bruge en anden tjeneste til identitets- og adgangsstyring
Hvis du ikke bruger Azure Active Directory til at administrere identiteter og adgangsrettigheder, skal du have hjælp fra en udvikler. Hvis du foretrækker at gemme app-id'et og hemmeligheden et andet sted, kan du lade felterne Klient-id og Klienthemmelighed være tomme og skrive en udvidelse for at hente id'et og hemmeligheden fra placeringen. Du kan levere hemmeligheden på kørselstidspunktet ved at abonnere på OnGetEmailLoggingClientId- og OnGetEmailLoggingClientSecret-hændelserne i codeunit 1641 "Opsætning af e-mail".

---

## <a name="to-start-logging-email"></a>Sådan startes logføring af e-mails
1. Start logføring af e-mail ved at aktivere til/fra-feltet **Aktiveret** på siden **E-mail-logføring**.
2. Log på med Exchange Online-kontoen, som det planlagte job kan anvende kontoen til at oprette forbindelse til den delte postkasse og behandle mails.

    > [!NOTE]
    > Hvis du ikke bliver bedt om at logge på Exchange Online-kontoen, skyldes det sandsynligvis, at din browser blokerer pop op-vinduer. Du kan logge på ved at tillade pop op-vinduer fra https://login.microsoftonline.com.

## <a name="to-stop-logging-email"></a>Sådan stoppes logføring af e-mails
## <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience)
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Marketingopsætning**, og vælg derefter det relaterede link.
1. Deaktiver **Aktiveret** til/fra.

## <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience)
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **E-mail-logføring**, og vælg derefter det relaterede link.
2. Deaktiver **Aktiveret** til/fra.

---

## <a name="to-change-the-user-account-used-for-email-logging"></a>Sådan ændres den brugerkonto, der bruges til e-mail-logføring
Hvis du bruger den nye oplevelse, kan du ændre den brugerkonto, der bruges til e-mail-logføring. Den aktuelle oplevelse understøtter ikke denne.

## <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience) 
Deaktiver den aktuelle opsætning, Skift brugeren på siden **E-mail-logføring**, og aktiver e-mail-logføring igen. Du kan også bruge en assisteret installationsvejledning igen.

## <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience)
### <a name="prod_short-online"></a>[!INCLUDE[prod_short](includes/prod_short.md)] Online
1. Log på [!INCLUDE[prod_short](includes/prod_short.md)]-kontoen, med den konto, som det planlagte job kan anvende til at oprette forbindelse til den delte postkasse og behandle mails. Denne konto skal have adgang til både [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online.
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **E-mail-logføring**, og vælg derefter det relaterede link. 
3. Vælg **Relateret**, og klik derefter på **Opgavekøpost**.
4. Genstart **E-mail-logføring**-opgave.

### <a name="prod_short-on-premises"></a>[!INCLUDE[prod_short](includes/prod_short.md)] lokalt
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **E-mail-logføring**, og vælg derefter det relaterede link. 
2. Vælg **Handlinger**, og derefter **Forny token**.
3. Log på med Exchange Online-kontoen, som det planlagte job kan anvende kontoen til at oprette forbindelse til den delte postkasse og behandle mails.

## <a name="see-also"></a>Se også
[Styre relationer](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]