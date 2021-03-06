---
title: Konfigurere mail i Business Central | Microsoft Docs
description: Beskriver, hvordan e-mail-konti sluttes til Business Central, så du kan sende udgående meddelelser uden at skulle åbne en anden app.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, email, Office 365, connector
ms.date: 06/15/2020
ms.author: bholtorf
ms.openlocfilehash: 44fb1f467b0b44c41456a64c8de3f5ae9dc85786
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752746"
---
# <a name="set-up-email"></a>Konfigurer mail
Personer i virksomheder sender oplysninger og dokumenter, f. eks. salgs-og købsordrer og fakturaer, pr. e-mail hver dag. Administratorer kan gøre det nemmere at gøre ved at oprette forbindelse mellem en eller flere e-mail-konti [!INCLUDE[prod_short](includes/prod_short.md)], så du kan sende dokumenter uden at skulle åbne en e-mail-app. Du kan skrive hver enkelt meddelelse individuelt med grundlæggende formateringsværktøjer, f. eks. skrifttyper, typografier, farver osv., og føje vedhæftede filer til op til 100 MB. Administratorer kan også konfigurere rapportlayout, der kun indeholder nøgleoplysninger fra dokumenter. Du kan finde flere oplysninger under [Sende dokumenter via mail](ui-how-send-documents-email.md).

E-mail-funktionerne i [!INCLUDE[prod_short](includes/prod_short.md)] er kun til udgående meddelelser. Du kan ikke modtage svar, dvs. der er ingen indbakke side i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, skal du oprette en app-registrering til i Azure-portalen, før du kan konfigurere mail [!INCLUDE[prod_short](includes/prod_short.md)]. App-registreringen gør det muligt [!INCLUDE[prod_short](includes/prod_short.md)] at godkende og godkende din e-mail-udbyder. Du kan finde flere oplysninger i [Opsætning af e-mail til Business Central lokalt](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). I [!INCLUDE[prod_short](includes/prod_short.md)] online håndteres dette for dig.

## <a name="required-permissions"></a>Nødvendige tilladelser
Hvis du vil konfigurere mail, skal du have tilladelsen **EMAIL-OPSÆTNING** indstillet. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md). 

## <a name="adding-email-accounts"></a>Tilføje e-mailkonti
Du kan tilføje e-mailkonti via udvidelser, der gør det muligt at oprette konti fra forskellige providere [!INCLUDE[prod_short](includes/prod_short.md)]. Standard udvidelserne bruges til at bruge konti fra Microsoft Exchange Online tilstand, men andre udvidelser kan være tilgængelige, så du kan oprette forbindelse mellem konti fra andre leverandører, f. eks. gmail.

Når du har tilføjet en e-mailkonto, kan du angive foruddefinerede forretningsscenarier, hvor du kan bruge kontoen til at sende mails. Du kan f. eks. angive, at alle brugere skal sende salgsdokumenter fra én konto til købsdokumenter fra en anden konto. Du kan finde flere oplysninger i [Tildele e-mailscenarier til e-mailkonti](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

I følgende tabel beskrives de e-mail-udvidelser, der som standard er tilgængelige.

|Udvidelse  |Description  |Eksempler på, hvornår du skal bruge  |
|---------|---------|---------|
|**Microsoft 365**|Alle sender mails fra en delt postkasse i Exchange Online.|Når alle meddelelser kommer fra samme afdeling, sender salgsorganisationen f. eks. meddelelser fra en sales@cronus.com konto. Dette kræver, at du opretter en delt postkasse i Office 365-administrationscenter. Du kan finde flere oplysninger i [Delte postkasser](/Exchange/collaboration/shared-mailboxes/shared-mailboxes.md).|
|**Aktuel bruger**|Alle sender mail fra den konto, som de bruges til at logge på [!INCLUDE[prod_short](includes/prod_short.md)].|Tillad kommunikation fra individuelle konti.|
|**Andet (SMTP)**|Brug SMTP-protokollen til at sende mails.|Tillad kommunikation via din SMTP-mailserver. |

> [!NOTE]
> **Microsoft 365** og de **Aktuelle bruger**-udvidelser bruger de konti, du har oprettet til brugere i Microsoft 365 Administration Center til dit Office 365-abonnement. Hvis du vil sende e-mail ved hjælp af udvidelser, skal brugere have en gyldig licens til Exchange Online. 

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="legacy-smtp-settings-and-the-email---smtp-connector-extension"></a>Ældre SMTP-indstillinger og e-mail-SMTP-forbindelsesudvidelsen
Hvis du allerede bruger [!INCLUDE[prod_short](includes/prod_short.md)] og har konfigureret mails via den ældre SMTP-opsætning, kan du fortsætte med at bruge installationsprogrammet parallelt med e-mail-SMTP-forbindelsesudvidelsen. Når vi opdaterer din [!INCLUDE[prod_short](includes/prod_short.md)] til den næste version, vil vi kopiere dine gamle SMTP-indstillinger til udvidelsen e-mail-SMTP-Connector. Når administratoren er klar, kan den aktivere de forbedrede e-mail-funktioner, og du skal begynde at bruge e-mail-SMTP-forbindelsesudvidelsen. Du kan finde flere oplysninger i [Om Funktionsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management.md#about-feature-management). Der sker imidlertid ingen synkronisering mellem SMTP-forbindelses udvidelsen og de ældre indstillinger. Hvis du ændrer SMTP-indstillingerne i filtypenavnet, skal du foretage de samme ændringer i den ældre SMTP-opsætning eller omvendt.

> [!NOTE]
> Hvis du har tilpasninger, som er afhængige af den ældre konfiguration af SMTP-mail, er der risiko for, at noget går galt med dine tilpasninger, hvis du begynder at bruge e-mail-udvidelser. Det anbefales, at du opsætter og tester udvidelserne, før du aktiverer funktions parameteren til forbedrede e-mail-funktioner.

## <a name="add-email-accounts"></a>Tilføj e-mailkonti
**Installationsvejledningen til opsætning af e-mail**-support kan hjælpe dig med at komme hurtigt i gang med e-mails.

> [!NOTE]
> Du skal have en e-mail-standardkonto, selvom du kun tilføjer én konto. Standardkontoen bruges til alle e-mail-scenarier, der ikke er tildelt til en konto. Du kan finde flere oplysninger i [Tildele e-mailscenarier til e-mailkonti](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurer e-mailkonti**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Office 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Tildel e-mailscenarier til e-mailkonti
E-mail-scenarier er processer, der involverer afsendelse af et dokument, f. eks. en salgs-eller købsordre, eller en notifikation, f. eks. en invitation til en ekstern bogholder. Du kan bruge bestemte e-mail-konti til bestemte scenarier. Du kan f. eks. angive, at alle brugere altid skal sende salgsdokumenter fra én konto, købsdokumenter fra en anden konto, et lagersted eller et produktions dokument fra en tredje konto. Du kan tildele, gentildele og fjerne scenarier, når du vil, men du kan kun knytte et scenario til én e-mail-konto ad gangen. Standardmailkontoen bruges til alle e-mail-scenarier, der ikke er tildelt til en konto.
 
<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents"></a>Angiv genanvendelig e-mailtekst og layout til salgs-og købsdokumenter
Du kan bruge rapporter til at medtage nøgleoplysninger fra salgs-og købsdokumenter i tekst til e-mails. Denne procedure beskriver, hvordan du opretter rapporten **Salg-faktura** for bogførte salgsfakturaer, men processen svarer til andre rapporter.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rapportvalg - Salg**, og vælg derefter det relaterede link.
2. På siden **Rapportvalg - salg** skal du vælge **faktura** i feltet **Forbrug**.
3. På en ny linje i feltet **Rapport-ID** skal du vælge f.eks. standardrapport 1306.
4. Markér afkrydsningsfeltet **Brug til brødtekst i mail**.
5. Vælg feltet **Layoutkode for brødtekst i mail**, og vælg derefter et layoutformat på rullelisten.

    Rapportlayout angiver formatet og indholdet af brødteksten i mailen, herunder tekst, som indeholder en hilsen eller instruktion forud for dokumentoplysninger. Du kan se alle tilgængelige rapportlayout, hvis du vælger knappen **Vælg fra komplet liste**.
6. For at få vist eller redigere layoutet, som teksten i mailen er baseret på, skal du vælge layoutet på siden **Rediger Layout** og derefter vælge handlingen **Tilpassede rapportlayouts**.
7. Hvis du vil tilbyde kunderne at betale for salg elektronisk, kan du konfigurere den relaterede betalingstjeneste, f.eks PayPal, og derefter kan du også automatisk få PayPal oplysninger og hyperlink indsat i selve mailen. Du kan finde flere oplysninger i [Aktivere debitorbetalinger via PayPal](sales-how-enable-payment-service-extensions.md).
8. Vælg knappen **OK**.

Nu, når du vælger, f.eks. **Send**-handlingen på siden **Bogført salgsfaktura**, indeholder brødtekst i mail dokumentoplysningerne i rapporten 1306 med foranstående standardtekst, hvor typografierne er i overensstemmelse med det rapportlayout, som du valgte under trin 5.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Bruge en erstatningsafsenderadresse på udgående mailmeddelelser
Hvis du bruger ældre SMTP-indstillinger, kan du bruge funktionerne **Send som** eller **Send på vegne af** på Microsoft Exchange for at ændre afsenderadressen i udgående meddelelser. [!INCLUDE[prod_short](includes/prod_short.md)] bruger SMTP-kontoen til at godkende til Exchange, men den vil enten erstatte afsenderadressen med den, du angiver, eller ændre den med "på vegne af."

Følgende er eksempler på, hvordan Send som og Send på vegne af bruges i [!INCLUDE[prod_short](includes/prod_short.md)]:

 * Når du sender dokumenter, f.eks. købs-eller salgsordrer, til kreditorer og debitorer, kan det være en god ide at få dem vist til at komme fra en _noreply@yourcompanyname.com_-adresse.
 * Når arbejdsprocessen sender en anmodning om godkendelse pr. mail med anmoderens mailadresse.

> [!Note]
> Du kan kun bruge én konto til at erstatte afsenderadresser. Det vil sige, at du ikke kan have én erstatningsadresse til indkøbsprocesser og en anden til salgsprocesser.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Sådan opsættes erstatningsafsenderadressen for alle udgående mailmeddelelser
1. Find den postkasse, der skal bruges som erstatningsadresse, i **Exchange Administrationscenter** til din Microsoft 365-konto, og kopiér eller notér adressen. Hvis du har brug for en ny adresse, skal du gå til Microsoft 365 administration for at oprette en ny bruger og oprette postkassen.
2. I [!INCLUDE[prod_short](includes/prod_short.md)] skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **SMTP-mailopsætning** og dernæst vælge det relaterede link.
3. Angiv erstatningsadressen i feltet **Send som**.
4. Kopiér eller notér adressen i feltet **bruger-id**.
5. Find den postkasse, der skal bruges som erstatningsadresse, i **Exchange Administrationscenter**, og angiv derefter adressen fra feltet **bruger-id** i feltet **Send som**. Du kan finde flere oplysninger under [Brug af EAC til at tildele tilladelser til individuelle postkasser](/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Sådan bruges erstatningsadressen i godkendelsesarbejdsgange
1. I [!INCLUDE[prod_short](includes/prod_short.md)] skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **SMTP-mailopsætning** og dernæst vælge det relaterede link.
2. Kopiér eller notér adressen i feltet **bruger-id**.
3. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugeropsætning af godkendelser**, og vælg derefter det relaterede link.
4. I **Exchange Administrationscenter** skal du finde postkasserne for hver bruger angivet på siden **Brugeropsætning af godkendelser** og i feltet **Send som** indtaste adressen fra feltet **bruger-id** på siden **SMTP-mailopsætning** i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Administrere tilladelser for modtagere](/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. I [!INCLUDE[prod_short](includes/prod_short.md)] skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **SMTP-mailopsætning** og dernæst vælge det relaterede link.
6. Hvis du vil aktivere erstatning, skal du aktivere funktionen til skift af **Tillad afsendererstatning**.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] bestemmer, hvilken adresse der skal vises i følgende rækkefølge: <br><br> 1. Den adresse, der er angivet i feltet **Mail** på siden **Brugeropsætning af godkendelser** for meddelelser i en arbejdsgang. <br> 2. Den adresse, der er angivet i feltet **Send som** på siden **SMTP-mailopsætning**. <br> 3. Den adresse, der er angivet i feltet **Bruger-id** på siden **SMTP-mailopsætning**.

## <a name="set-up-document-sending-profiles"></a>Konfigurere dokumentafsendelsesprofiler
Du kan oprette en foretrukken metode til afsendelse af salgsdokumenter for hver af dine kunder, så du ikke behøver at vælge en afsender indstilling, som f. eks. om der skal sendes et dokument via e-mail eller som et elektronisk dokument, hver gang du sender et dokument. Du kan finde flere oplysninger under [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Konfigurere offentlige mapper og regler maillogføring i Exchange Online
Få mere ud af kommunikationen mellem sælgerne og dine eksisterende eller potentielle kunder ved at spore udveksling af mails og derefter ændre dem til handlingsrettede leads. Du kan finde flere oplysninger under [Spore udveksling af mails mellem sælgere og kontakter](marketing-set-up-email-logging.md).  

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Derefter opretter du forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online. Du kan finde flere oplysninger under [Spore udveksling af mails mellem sælgere og kontakter](marketing-set-up-email-logging.md).  

## <a name="setting-up-email-for-business-central-on-premises"></a>Opsætte E-mail til Business Central lokalt 
[!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan integreres med tjenester, der er baseret på Microsoft Azure. Du kan f. eks. bruge Cortana Intelligence til mere intelligente pengestrømme for at Power BI visualiserer din virksomhed og at Exchange Online sender e-mail. Integrationen med disse tjenester er baseret på en app-registrering i Azure Active Directory. App-registreringen leverer godkendelses-og autorisations tjenester til kommunikation. Hvis du vil bruge e-mail-funktionerne i [!INCLUDE[prod_short](includes/prod_short.md)] lokal adresse, skal du registrerer [!INCLUDE[prod_short](includes/prod_short.md)] som en app i Azure-portalen og derefter oprette forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)] App-registreringen. Følgende afsnit beskriver, hvordan.

### <a name="create-an-app-registration-for-prod_short-in-azure-portal"></a>Opret en app-registrering til [!INCLUDE[prod_short](includes/prod_short.md)] i Azure-portalen
De trin, der skal registreres [!INCLUDE[prod_short](includes/prod_short.md)] i Azure-portalen, er beskrevet i [Registrer et program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). De indstillinger, der er specifikke for e-mailegenskaberne, er de delegerede rettigheder, som du tildeler din app-registrering. I følgende tabel vises minimum tilladelserne.

|Navn på API / tilladelse  |Type  |Description  |
|---------|---------|---------|
|Microsoft Graph/User. Read |Delegeret|Log på, og Læs brugerprofil.         |
|Microsoft Graph/mail. skrivebeskyttet |Delegeret|Opret mailmeddelelser.         |
|Microsoft Graph/mail.Send|Delegeret|Send mail         |
|Microsoft Graph/offline_access|Delegeret|Vedligehold dataadgangssamtykke. <!--need to verify this-->|

> [!TIP]
> Når du opretter app-registreringen i , skal du angive følgende. Du skal bruge den for at oprette forbindelse [!INCLUDE[prod_short](includes/prod_short.md)] til din app-registrering.
> 
> * Program-ID (klient) 
> * Omdirigerings-URI (valgfri)
> * Klienthemmelighed

Du kan finde flere oplysninger om registrering af en app i [Hurtig start: registrere et program på Microsoft-identitetsplatformen](/azure/active-directory/develop/quickstart-register-app.md). 

### <a name="connect-prod_short-to-your-app-registration"></a>Forbinde [!INCLUDE[prod_short](includes/prod_short.md)] med din appregistrering
Når du har registreret programmet i Azure-portalen i [!INCLUDE[prod_short](includes/prod_short.md)], skal du bruge **e-mail-programmets AAD-registrering** vejledning til registrering, der kan oprette forbindelse [!INCLUDE[prod_short](includes/prod_short.md)] til den.

1. I [!INCLUDE[prod_short](includes/prod_short.md)] skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **E-mailansøgning til AAD-registrering** og dernæst vælge det relaterede link.
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

## <a name="see-also"></a>Se også
[Delte postkasser i Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Bruge [!INCLUDE[prod_short](includes/prod_short.md)] som din virksomheds Indbakke i Outlook](admin-outlook.md)  
[Få [!INCLUDE[prod_short](includes/prod_short.md)] på min mobilenhed](install-mobile-app.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]