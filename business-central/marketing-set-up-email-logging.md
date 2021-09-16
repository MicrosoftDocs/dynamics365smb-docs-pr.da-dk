---
title: Konfigurer maillogføring | Microsoft Docs
description: Få at vide, hvordan du ændrer mailinteraktioner mellem sælgere og kunder til reelle salgs-leads.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: c1e47dba1c10b994cb43c21afbfdd548f85c774b
ms.sourcegitcommit: 04055135ff13db551dc74a2467a1f79d2953b8ed
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2021
ms.locfileid: "7482341"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Spore udveksling af mails mellem sælgere og kontakter

Få mere ud af kommunikationen mellem sælgerne og dine eksisterende eller potentielle kunder ved at spore udveksling af mails og derefter ændre dem til handlingsrettede leads. [!INCLUDE[prod_short](includes/prod_short.md)] kan bruges sammen med Exchange Online til at føre en log over indgående og udgående meddelelser. Du kan få vist og analysere indholdet af hver meddelelse på siden **Interaktionslogposter**.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Konfigurere offentlige mapper og regler maillogføring i Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Derefter opretter du forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online.

## <a name="setting-up-prod_short-to-log-email-messages"></a>Oprette [!INCLUDE[prod_short](includes/prod_short.md)] til logføring af mails

Introduktion til maillogføring i to lette trin:

1. Opret forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online til dit Microsoft 365-abonnement. Exchange Online håndterer dine mails. Vi har gjort dette trin lettilgængeligt med en vejledning til assisteret opsætning. Du skal blot bruge dine administratorrettigheder til din administratorkonto i Microsoft 365. Start vejledningen ved at gå til **Assisteret opsætning**, og vælg derefter vejledningen **Konfigurer maillogføring**.  

2. Kontrollér, at der er angivet gyldige mailadresser i [!INCLUDE[prod_short](includes/prod_short.md)] for dine sælgere og kontakter, afhængigt af om de er potentielle eller eksisterende kunder. Hvis du vil gøre det, skal du for hver debitor eller sælger åbne kortet **Kontakt** eller **Sælger/indkøber** og se feltet **Mailadresse**.

> [!Tip]
> Når du har udført trinnene i programguiden, kan du kontrollere, om forbindelsen er oprettet. Søg efter **Marketingopsætning**, vælg **Aktivere**, derefter **Funktioner** og derefter **Valider opsætning af maillogføring**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Få vist udveksling af mails i interaktionslogposten

[!INCLUDE[prod_short](includes/prod_short.md)] opretter en post på siden **Interaktionslog**, hver gang en sælger og en kontakt udveksler en mail. Du kan få vist interaktionsloggen ved at åbne kortet **Kontakt** for personen, vælge **Relaterede**, og derefter vælge **Historik** og **Interaktionslogposter**. Der er nogle få ting, der kan udføres for hver indtastning i logfilen, f.eks.:

- Få vist indholdet af den mail, der blev udvekslet, ved at vælge **Behandle** og derefter **Vis vedhæftede filer**.
- Omdanne en mailudveksling til et salgs-lead – hvis en post ser lovende ud, kan du gøre den til en lead og derefter styre forløbet hen imod et salg. Det gør du ved at vælge posten og derefter vælge **Behandle** og derefter **Oprette lead**. Du kan finde flere oplysninger i [Administrere salgsleads](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>Tilslutning af lokale versioner til Microsoft Exchange

Du kan oprette forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange on-premises eller Exchange Online til e-maillogføring. For begge versioner af Exchange er indstillingerne for forbindelsen tilgængelige på siden **Marketingopsætning**. I Exchange Online kan du også bruge en assisteret installationsvejledning.

### <a name="connecting-to-exchange-on-premises"></a>Oprettelse af forbindelse til On-premises

Hvis du vil tilslutte [!INCLUDE[prod_short](includes/prod_short.md)] on-premises til Exchange on-premises på siden **Marketingopsætning** kan du bruge **Basis** som **Godkendelsestype** og derefter angive legitimationsoplysninger til brugerkontoen for Exchange on-premises. Aktiver derefter **Aktiveret** til/fra for at starte logføring af e-mails.

### <a name="connecting-to-exchange-online"></a>Forbindelse til Exchange Online

Hvis du vil oprette forbindelse til Exchange Online, skal du bruge **OAuth2** som **godkendelsestype**. Du kan også registrere et program i Azure Active Directory og angive program-id, key vault-hemmeligheden og omdirigere den URL-adresse, der skal bruges. URL-adressen til omdirigering er forudindstillet og bør fungere for de fleste installationer. Du kan finde flere oplysninger i Sådan registreres et program i Azure AD for at oprette forbindelse fra Business Central til Exchange Online herunder.

Du skal konfigurere installationen til at bruge HTTPS. Du kan finde flere oplysninger i [Konfigurere SSL for at sikre forbindelsen til Business Central-webklienten](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Hvis du konfigurerer serveren, så den har en anden startside, kan du altid ændre URL-adressen. Klientens hemmelighed gemmes som en krypteret streng i din database.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Sådan registrerer du et program i Azure AD for at oprette forbindelse fra Business Central til Exchange Online

I følgende trin antages det, at du bruger Azure Active Directory til at administrere identiteter og adgangsrettigheder. Du kan finde flere oplysninger om registrering af et program i [Hurtig start: Registrere et program på Microsoft-identitetsplatformen](/azure/active-directory/develop/quickstart-register-app). Hvis du ikke bruger Azure Active Directory, kan du se [Bruge en anden tjeneste til identitets- og adgangsstyring](marketing-set-up-email-logging.md#using-another-identity-and-access-management-service). 

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
8. Vælg **Oversigt**, og find derefter **Program-id (klient)**-værdien . Dette er programmets klient-id. Du skal enten angive det på siden **Marketingopsætning**, i feltet **Klient-id** eller gemme det i et sikkert lager og angive det i en hændelsesabonnent.
9. I [!INCLUDE[prod_short](includes/prod_short.md)] skal du oprette maillogføring på siden **Marketingopsætning** eller bruge guiden **Assisteret opsætning af maillogføring** til at få hjælp.
    * Angiv mailkonto for brugeren, på hvis vegne den planlagte sag vil oprette forbindelse til Exchange Online og behandle mails. Brugeren skal have en gyldig licens til Exchange Online.
    * Angiv URL-adressen til din Exchange Online. Dette er normalt det domæne, som du har angivet i brugerens e-mail-adresse.
    * Angiv **Kømappesti** og **lagringsmappesti**.
10. Start logføring af e-mails ved at aktivere **Aktiveret** til/fra.
11. Log på med din administratorkonto til Azure Active Directory (kontoen skal have en gyldig licens til Exchange og være administrator i Exchange Online). Når du er logget på, bliver du bedt om at tillade, at dit registrerede program logger på Exchange Online på vegne af organisationen. Du skal give samtykke for at fuldføre installationen.

   > [!NOTE]
   > Hvis du ikke bliver bedt om at logge på med din administratorkonto, skyldes det sandsynligvis, at pop op-vinduer er blokeret. Du kan logge på ved at tillade pop op-vinduer fra https://login.microsoftonline.com.

### <a name="using-another-identity-and-access-management-service"></a>Bruge en anden tjeneste til identitets- og adgangsstyring
Hvis du ikke bruger Azure Active Directory til at administrere identiteter og adgangsrettigheder, skal du have hjælp fra en udvikler. Hvis du foretrækker at gemme app-id'et og hemmeligheden et andet sted, kan du lade felterne Klient-id og Klienthemmelighed være tomme og skrive en udvidelse for at hente id'et og hemmeligheden fra placeringen. Du kan levere hemmeligheden på kørselstidspunktet ved at abonnere på OnGetEmailLoggingClientId- og OnGetEmailLoggingClientSecret-hændelserne i codeunit 1641 "Opsætning af e-mail".

### <a name="to-stop-logging-email"></a>Sådan stoppes logføring af e-mails
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Marketingopsætning**, og vælg derefter det relaterede link.
2. Deaktiver **Aktiveret** til/fra.

## <a name="see-also"></a>Se også
[Styre relationer](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]