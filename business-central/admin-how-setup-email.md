---
title: Konfigurere mail i Business Central (indeholder video)
description: Beskriver, hvordan e-mail-konti sluttes til Business Central, så du kan sende udgående meddelelser uden at skulle åbne en anden app.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, email, Office 365, connector
ms.search.form: 1805, 9813, 9814, 1262, 1263
ms.date: 02/06/2022
ms.author: bholtorf
ms.openlocfilehash: 8357659f42976c7e3bc9b64a3c0aa10fe5b32364
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950458"
---
# <a name="set-up-email"></a>Konfigurer mail
Personer i virksomheder sender oplysninger og dokumenter, f.eks. salgs-og købsordrer og fakturaer, pr. e-mail hver dag. Administratorer kan nemmere oprette forbindelse mellem en eller flere e-mail-konti [!INCLUDE[prod_short](includes/prod_short.md)], så du kan sende dokumenter uden at skulle åbne en e-mail-app. Du kan skrive hver enkelt meddelelse individuelt med grundlæggende formateringsværktøjer, f.eks. skrifttyper, typografier, farver osv., og føje vedhæftede filer til op til 100 MB. Administratorer kan desuden rapportlayout lade administratorer omfatte nøgleoplysninger fra dokumenter. Du kan finde flere oplysninger i [Sende dokumenter via mail](ui-how-send-documents-email.md).

E-mailfunktionerne i [!INCLUDE[prod_short](includes/prod_short.md)] er kun til udgående meddelelser. Du kan ikke modtage svar, dvs. der er ingen "indbakke" side i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Du kan kun bruge e-mail-faciliteterne [!INCLUDE[prod_short](includes/prod_short.md)] online sammen med Exchange Online. Vi understøtter ikke hybrid scenarier, f. eks. tilslutning af [!INCLUDE[prod_short](includes/prod_short.md)]-online til en lokal version af Exchange.
> 
> Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, skal du oprette en app-registrering til i Azure-portalen, før du kan konfigurere mail [!INCLUDE[prod_short](includes/prod_short.md)]. App-registreringen gør det muligt [!INCLUDE[prod_short](includes/prod_short.md)] at godkende og godkende din e-mail-udbyder. Du kan finde flere oplysninger i [Opsætning af e-mail til Business Central lokalt](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). I [!INCLUDE[prod_short](includes/prod_short.md)] online håndteres dette for dig.

## <a name="required-permissions"></a>Nødvendige tilladelser
Hvis du vil konfigurere mail, skal du have tilladelsen **EMAIL-OPSÆTNING** indstillet. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md). 

## <a name="adding-email-accounts"></a>Tilføje e-mailkonti
Du kan tilføje e-mailkonti via udvidelser, der gør det muligt at oprette konti fra forskellige providere [!INCLUDE[prod_short](includes/prod_short.md)]. Med standard filtyper kan du bruge konti fra Microsoft Exchange Online. Andre udvidelser, som giver dig mulighed for at oprette forbindelse mellem konti fra andre leverandører, f. eks. Gmail, er muligvis tilgængelige.

Du kan angive foruddefinerede forretningsscenarier, hvor du kan bruge kontoen til at sende mails. Du kan f.eks. angive, at alle brugere skal sende salgsdokumenter fra én konto til købsdokumenter fra en anden konto. Du kan finde flere oplysninger i [Tildele e-mailscenarier til e-mailkonti](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

I følgende tabel beskrives de e-mail-udvidelser, der som standard er tilgængelige.

|Udvidelse  |Beskrivlse  |Eksempler på, hvornår du skal bruge  |
|---------|---------|---------|
|**Microsoft 365-connector**|Alle sender mails fra en delt postkasse i Exchange Online.|Når alle meddelelser kommer fra samme afdeling, sender salgsorganisationen f.eks. meddelelser fra en sales@cronus.com konto. Dette kræver, at du opretter en delt postkasse i Microsoft 365 Administration. Du kan finde flere oplysninger i [Delte postkasser](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Aktuel brugerforbindelse**|Alle sender mail fra den konto, som de bruges til at logge på [!INCLUDE[prod_short](includes/prod_short.md)].|Tillad kommunikation fra individuelle konti.|
|**SMTP Connector**|Brug SMTP-protokollen til at sende mails.|Tillad kommunikation via din SMTP-mailserver. |

> [!NOTE]
> Udvidelserne **Microsoft 365-connector** og **Aktuel bruger-connector** bruger de konti, du konfigurere til brugere i Microsoft 365 Administration til dit Microsoft 365-abonnement. Hvis du vil sende e-mail ved hjælp af udvidelser, skal brugere have en gyldig licens til Exchange Online. Derudover kræver disse udvidelser, at indstillingen **Tillad HttpClient-anmodninger** er aktiveret. Hvis du vil kontrollere, om det er aktiveret for disse udvidelser, skal du gå til siden **Udvidelsesstyring**, vælge udvidelsen og derefter vælge indstillingen **Konfigurer**.

> Eksterne brugere, f. eks. uddelegerede administratorer og eksterne bogholdere, kan heller ikke bruge disse udvidelser til at sende e-mail-meddelelser fra [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="using-smtp"></a>Brug af SMTP
Hvis du vil bruge SMTP-protokollen til at sende e-mails fra [!INCLUDE[prod_short](includes/prod_short.md)], kan du bruge SMTP-forbindelses udvidelsen. Når du opretter en konto, der bruger SMTP, er afsendertypen et vigtigt felt. Hvis du vælger en bestemt bruger, sendes der e-mails med navnet og andre oplysninger fra den konto, du opretter. Men hvis du vælger aktuel bruger, sendes e-mails fra den e-mail-konto, der er angivet for hver enkeltbrugerkonto. Den aktuelle bruger svarer til funktionen Send som. Du kan finde flere oplysninger i [Brug en erstatningsafsenderadresse på udgående mailmeddelelser](admin-how-setup-email.md#use-a-substitute-sender-address-on-outbound-email-messages). 

> [!IMPORTANT]
> Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø, kan du ikke bruge OAuth 2.0 til godkendelse. Du skal oprette en programregistrering i Azure-portalen og derefter køre vejledningen **Opsætning af Azure Active Directory**-assisteret installation i [!INCLUDE[prod_short](includes/prod_short.md)] for at oprette forbindelse til Azure AD. Du kan finde flere oplysninger i [Oprette en appregistrering til Business Central i Azure Portal](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).

## <a name="add-email-accounts"></a>Tilføj e-mailkonti
**Installationsvejledningen til opsætning af e-mail**-support kan hjælpe dig med at komme hurtigt i gang med e-mails.

> [!NOTE]
> Du skal have en e-mail-standardkonto, selvom du kun tilføjer én konto. Standardkontoen bruges til alle e-mail-scenarier, der ikke er tildelt til en konto. Du kan finde flere oplysninger i [Tildele e-mailscenarier til e-mailkonti](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Konfiguration af e-mailkonti**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Tildel e-mailscenarier til e-mailkonti
E-mail-scenarier er processer, der involverer afsendelse af et dokument. En salgs-eller købsordre eller en notifikation, f. eks. en invitation til en ekstern bogholder. Bestemte e-mail-konti kan anvendes til bestemte scenarier. Du kan f.eks. angive, at alle brugere altid skal sende salgsdokumenter fra én konto, købsdokumenter fra en anden konto, et lagersted eller et produktions dokument fra en tredje konto. Du kan tildele, gentildele og fjerne scenarier efter behov. Et scenarie kan kun tildeles én e-mail-konto ad gangen. Standard-mailkontoen bruges til alle scenarier, der ikke er tildelt til en konto.
 
<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-view-policies"></a>Konfigurer visnings politikker
Du kan styre de e-mails, som en bruger kan se på siderne i e-mail-Udbakke og sendte mails.

Vælg en bruger på listen over **Politikker for visning af brugermail**, og vælg derefter en af følgende indstillinger i feltet **Vis mailpolitik**:

* **Vis egne mails** - brugeren kan kun få vist deres egne e-mail-meddelelser.
* **Vis alle mails** - brugeren kan få vist alle e-mails, herunder e-mails, der er sendt af andre brugere.
* **Vis, hvis der er adgang til alle relaterede poster** -denne visnings politik bruges, hvis der ikke er angivet andre politikker. En bruger kan få vist e-mail-meddelelser, som andre brugere har sendt, hvis brugeren har adgang til den post, der er sendt, og alle relaterede poster. F. eks. har en bruger, der har sendt en bogført-salgsfaktura til en kunde. Bruger B kan få vist e-mail-meddelelsen, hvis de har adgang til både fakturaen og kunden.
* **Vis, hvis der er adgang til relaterede poster** - brugeren kan få vist mails, der er sendt af andre personer, hvis brugeren har adgang til mindst én post, der er relateret til den post, der blev sendt. F. eks. har en bruger, der har sendt en bogført-salgsfaktura til en kunde. Bruger B kan få vist e-mail-meddelelsen, hvis de har adgang til både fakturaen og kunden.

> [!NOTE]
>  Hvis du lader feltet **bruger-ID** være tomt og derefter vælger handlingen e-mail-visnings politik, gælder den politik, du angiver for alle brugere.

## <a name="set-up-reusable-email-texts-and-layouts"></a>Konfigurere genanvendelige e-mailtekster og -layout
Du kan bruge rapporter til at medtage nøgleoplysninger fra salgs-og købsdokumenter i tekst til e-mails. Denne procedure beskriver, hvordan du opretter rapporten **Salg-faktura** for bogførte salgsfakturaer, men processen svarer til andre rapporter.

> [!NOTE]
> Hvis du vil bruge layoutet til at oprette indhold til e-mailmeddelelser, skal du bruge Word-filtypen til dit layout.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsrapportvalg**, og vælg derefter det relaterede link.
2. På siden **Rapportvalg - salg** skal du vælge **faktura** i feltet **Forbrug**.
3. På en ny linje i feltet **Rapport-ID** skal du vælge f.eks. standardrapport 1306.
4. Markér afkrydsningsfeltet **Brug til brødtekst i mail**.
5. Vælg feltet **Layoutbeskrivelse for brødtekst i mail**, og vælg derefter et layout på rullelisten.

    Rapportlayout definerer typografien og indholdet af teksten i e-mailen. Dette omfatter f.eks. også tekst til indhold som en hilsen eller vejledning, der står foran dokumentoplysningerne. Hvis din organisation har mange layout, kan du se alle tilgængelige rapportlayout, hvis du vælger knappen **Vælg fra komplet liste**.
6. For at få vist eller redigere layoutet, som teksten i mailen er baseret på, skal du vælge layoutet på siden **Brugerdefinerede rapportlayouts** og derefter vælge handlingen **Opdater layouts**.
7. Hvis du vil lade debitorer bruge en betalingstjeneste, f. eks. PayPal, skal du konfigurere servicen. Derefter indsættes PayPal-oplysningerne og linket i e-mail-teksten. Du kan finde flere oplysninger i [Aktivere debitorbetalinger via PayPal](sales-how-enable-payment-service-extensions.md).
8. Vælg knappen **OK**.

Nu, når du vælger, f.eks. **Send**-handlingen på siden **Bogført salgsfaktura**, indeholder brødtekst i mail dokumentoplysningerne i rapporten 1306 med foranstående standardtekst, hvor typografierne er i overensstemmelse med det rapportlayout, som du valgte under trin 5.

## <a name="use-a-substitute-sender-address-on-outbound-email-messages"></a>Brug en erstatningsafsenderadresse på udgående mailmeddelelser
Hvis du bruger SMTP Connector-udvidelse, kan du bruge funktionerne **Send som** eller **Send på vegne af** fra Microsoft Exchange for at ændre afsenderadressen i udgående meddelelser. [!INCLUDE[prod_short](includes/prod_short.md)] bruger SMTP-kontoen til at godkende til Exchange, men den vil enten erstatte afsenderadressen med den, du angiver, eller ændre den med "på vegne af."

Når du opretter en konto, og du vil bruge funktionerne Send som eller Send på vegne af Exchange, skal du vælge **Bestemt bruger** i feltet **Afsendertype**.

Alternativt kan du vælge **den aktuelle bruger**, så andre kan sende meddelelser via SMTP-forbindelsen. E-mailen ser ud til at være sendt fra den e-mail-konto, der er angivet i feltet kontaktperson (e-mail) på bruger kortet for den bruger, som har logget på. Den fungerer imidlertid på samme måde som funktionen Send som og sendes fra den konto, der er angivet i opsætningen af SMTP-connectoren.

Følgende er eksempler på, hvordan Send som og Send på vegne af bruges i [!INCLUDE[prod_short](includes/prod_short.md)]:

 * Du ønsker evt. de købs- eller salgsordrer, du sender til kreditorer og debitorer, kan det være en god ide at få dem vist til at komme fra en _noreply@yourcompanyname.com_-adresse.
 * Når arbejdsprocessen sender en anmodning om godkendelse pr. mail med anmoderens mailadresse.

> [!Note]
> Du kan kun bruge én konto til at erstatte afsenderadresser. Det vil sige, at du ikke kan have én erstatningsadresse til indkøbsprocesser og en anden til salgsprocesser.

<!--
### To set up the substitute sender address for all outbound email messages
1. In the **Exchange admin center** for your Microsoft 365 account, find the mailbox to use as the substitute address, and then copy or make a note of the address. If you need a new address, go to your Microsoft 365 admin center to create a new user and set up their mailbox.
2. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
3. In the **Send As** field, enter the substitute address.
4. Copy or make a note of the address in the **User ID** field.
5. In the **Exchange admin center**, find the mailbox to use as the substitute address, and then enter the address from the **User ID** field in the **Send As** field. For more information, see [Use the EAC to assign permissions to individual mailboxes](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### To use the substitute address in approval workflows
1. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Copy or make a note of the address in the **User ID** field.
3. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Approval User Setup**, and then choose the related link.
4. In the **Exchange admin center**, find the mailboxes for each user listed in the **Approval User Setup** page, and in the **Send As** field enter the address from the **User ID** field of the **SMTP Email Setup** page in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Manage permissions for recipients](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
6. To enable substitution, turn on the **Allow Sender Substitution** toggle.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] will determine which address to display in the following order: <br><br> 1. The address specified in the **E-Mail** field on the **Approval User Setup** page for messages in a workflow. <br> 2. The address specified in the **Send As** field in the **SMTP Email Setup** page. <br> 3. The address specified in the **User ID** field in the **SMTP Email Setup** page. -->

## <a name="set-up-document-sending-profiles"></a>Konfigurere dokumentafsendelsesprofiler
Du kan spare tid ved at oprette en foretrukken metode til afsendelse af salgsdokumenter for hver debitor. Hvis du gør det, behøver du ikke at vælge en afsender indstilling, f. eks. om du vil sende dokumentet via e-mail eller som et elektronisk dokument, hver gang du sender et dokument. Du kan finde flere oplysninger i [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).

## <a name="optional-set-up-email-logging-in-exchange-online"></a>Eventuelt: Konfigurer maillogføring i Exchange Online
Få mere ud af kommunikationen mellem sælgere og eksisterende eller potentielle kunder. Du kan spore e-mailudvekslinger og derefter ændre dem til dine leads. Du kan finde flere oplysninger i [Spore udveksling af mails mellem sælgere og kontakter](marketing-set-up-email-logging.md).  
<!--
[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Next, you connect [!INCLUDE[prod_short](includes/prod_short.md)] with Exchange Online. For more information, see [Track Email Message Exchanges Between Salespeople and Contacts](marketing-set-up-email-logging.md).  -->

## <a name="setting-up-email-for-business-central-on-premises"></a>Opsætte E-mail til Business Central lokalt 
[!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan integreres med tjenester, der er baseret på Microsoft Azure. Du kan f.eks. bruge Cortana Intelligence til mere intelligente pengestrømme for at Power BI visualiserer din virksomhed og at Exchange Online sender e-mail. Integrationen med disse tjenester er baseret på en app-registrering i Azure Active Directory. App-registreringen leverer godkendelses-og autorisations tjenester til kommunikation. Hvis du vil bruge e-mail-funktionerne i [!INCLUDE[prod_short](includes/prod_short.md)] lokal adresse, skal du registrerer [!INCLUDE[prod_short](includes/prod_short.md)] som en app i Azure-portalen og derefter oprette forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)] App-registreringen. Følgende afsnit beskriver, hvordan.

### <a name="create-an-app-registration-for-business-central-in-azure-portal"></a>Oprette en appregistrering til Business Central i Azure-portal
De trin, der skal registreres [!INCLUDE[prod_short](includes/prod_short.md)] i Azure-portalen, er beskrevet i [Registrer et program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). De indstillinger, der er specifikke for e-mailegenskaberne, er de delegerede rettigheder, som du tildeler din app-registrering. I følgende tabel vises minimum tilladelserne.

|Navn på API / tilladelse  |Type  |Beskrivelse  |
|---------|---------|---------|
|Microsoft Graph/User. Read |Delegeret|Log på, og Læs brugerprofil.         |
|Microsoft Graph/mail. skrivebeskyttet |Delegeret|Opret mailmeddelelser.         |
|Microsoft Graph/mail.Send|Delegeret|Send mail         |
|Microsoft Graph/offline_access|Delegeret|Vedligehold dataadgangssamtykke.|

Hvis du bruger en ældre SMTP Connector og vil bruge OAuth 2.0 til godkendelse, er tilladelserne lidt anderledes. Følgende tabel viser tilladelserne.

|Navn på API / tilladelse  |Type  |Beskrivelse  |
|---------|---------|---------|
|Microsoft Graph/offline_access|Delegeret|Vedligehold dataadgangssamtykke.|
|Microsoft Graph/openid|Delegeret|Log brugere på.|
|Microsoft Graph/User. Read |Delegeret|Log på, og Læs brugerprofil.         |
|Microsoft Graph/SMTP.Send|Delegeret|Send mails fra postkasser ved hjælp af SMTP-godkendelse.         |
|Office 365 Exchange Online/User.Read |Delegeret|Log på, og læs brugerprofil.         |

Når du opretter app-registreringen i , skal du angive følgende. Du skal bruge den for at oprette forbindelse [!INCLUDE[prod_short](includes/prod_short.md)] til din app-registrering.
 
* Program-ID (klient) 
* Omdirigerings-URI (valgfri)
* Klienthemmelighed

Du kan finde flere oplysninger om registrering af en app i [Hurtig start: registrere et program på Microsoft-identitetsplatformen](/azure/active-directory/develop/quickstart-register-app). 

> [!NOTE]
Hvis du har problemer med at bruge den ældre SMTP-protokollen til at sende mail, efter at du har forbundet [!INCLUDE[prod_short](includes/prod_short.md)] med din app-registrering, kan det skyldes, at SMTP-godkendelse ikke er aktiveret for din lejer. Det anbefales, at du i stedet bruger mailforbindelser for Microsoft 365 og Aktuel bruger, fordi de bruger mail-API'er for Microsoft Graph. Hvis du skal bruge SMTP-protokollen, kan du dog aktivere SMTP-godkendelse. Du kan finde oplysninger i [Aktivere eller deaktivere godkendt SMTP-afsendelse for klient (SMTP-godkendelse) i Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### <a name="connect-prod_short-to-your-app-registration"></a>Forbinde [!INCLUDE[prod_short](includes/prod_short.md)] med din appregistrering
Når du har registreret programmet i Azure-portalen i [!INCLUDE[prod_short](includes/prod_short.md)], skal du bruge **e-mail-programmets AAD-registrering** vejledning til registrering, der kan oprette forbindelse [!INCLUDE[prod_short](includes/prod_short.md)] til den.

1. I [!INCLUDE[prod_short](includes/prod_short.md)] kan du vælge ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **e-mail-programmets AAD-registrering**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Hvis du opretter forbindelse første gang, kan du køre guiden **Konfigurer e-mail**-opsætning. Guiden kræver, at der er oplysninger til at oprette forbindelse til din app-registrering. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Azure Active Directory, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Azure AD Directory - Multitenant)** or **Accounts in any organizational directory (Any Azure AD Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Azure Active Directory, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/set-up-email/)

## <a name="see-also"></a>Se også

[Delte postkasser i Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Brug [!INCLUDE[prod_short](includes/prod_short.md)] som din virksomheds Indbakke i Outlook](admin-outlook.md)  
[Få [!INCLUDE[prod_short](includes/prod_short.md)] på min mobilenhed](install-mobile-app.md)
[Få [!INCLUDE[prod_short](includes/prod_short.md)] på min mobilenhed](install-mobile-app.md)
[Analysere mailtelemetri (administrationsindhold)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
