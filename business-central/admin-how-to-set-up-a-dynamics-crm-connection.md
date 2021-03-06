---
title: Oprette forbindelse til Microsoft Dataverse | Microsoft Docs
description: Du kan integrere andre programmer med Business Central via Microsoft Dataverse.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/20/2020
ms.author: bholtorf
ms.openlocfilehash: e0713de255aabc599fbc80cf29f1bfa618a29003
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753913"
---
# <a name="connect-to-microsoft-dataverse"></a>Opret forbindelse til Microsoft Dataverse
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Dette emne beskriver, hvordan du konfigurerer en forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Virksomheder opretter typisk forbindelsen for at integrere og synkronisere data med en anden Dynamics 365-forretningsapp såsom [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Før du starter

Der er et par oplysninger, som du skal have klar, før du opretter forbindelsen:  

* URL-adressen til det [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljø, som du vil oprette forbindelse til. Hvis du bruger vejledningen **Common Data Service-forbindelsesopsætning** til at oprette forbindelsen, registrerer vi dine miljøer, men du kan også angive URL-adressen til et andet miljø i din lejer.  
* Brugernavn og adgangskode til en konto, der har administratorrettigheder i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Hvis du har en lokal [!INCLUDE[prod_short](includes/prod_short.md)] 2020 Release Wave 1, version 16,5, skal du læse [Kendte problemer](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services)-artikler. Du skal fuldføre den beskrevne løsning, før du kan oprette forbindelsen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

> [!Note]
> I fremgangsmåden nedenfor beskrives proceduren for onlineversionen af [!INCLUDE[prod_short](includes/prod_short.md)].
> Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] on-premises og ikke bruger en Azure Active Directory-konto til at oprette forbindelse til [!INCLUDE [cds_long_md](includes/cds_long_md.md)], skal du også angive brugernavn og adgangskode for en brugerkonto til integrationen. Denne konto kaldes "integrationsbruger"-kontoen. Hvis du bruger en Azure Active Directory-konto, er integrationsbrugerkontoen ikke påkrævet og vises ikke. Integrationsbrugeren konfigureres automatisk og kræver ikke en licens.

## <a name="set-up-a-connection-to-cds_long_md"></a>Oprette forbindelse til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

For alle andre godkendelsestyper end Microsoft 365-godkendelse kan du konfigurere din forbindelse til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på siden **Common Data Service-forbindelsesopsætning**. For Microsoft 365-godkendelse anbefaler vi, at du bruger den assisterede opsætningsvejledning **Common Data Service-forbindelsesopsætning**. Denne vejledning gør det nemmere at oprette forbindelsen og angive avancerede funktioner, f.eks. ejerskabsmodel og indledende synkronisering.  

> [!IMPORTANT]
> Under konfigurationen af forbindelsen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] bliver administratoren bedt om at give følgende tilladelser til det registrerede Azure-program, der hedder [!INCLUDE[prod_short](includes/prod_short.md)]-integration med [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * **Få adgang til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] som** nødvendig tilladelse, så du [!INCLUDE[prod_short](includes/prod_short.md)] kan, på vegne af administratoren, automatisk oprette en ikke-licenseret, ikke-interaktiv [!INCLUDE[prod_short](includes/prod_short.md)]-integrationsprogrambruger, tildele sikkerhedsroller til denne bruger og installere [!INCLUDE[prod_short](includes/prod_short.md)] Basis-CDS-integrationsløsningen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Denne tilladelse bruges kun én gang under oprettelse af forbindelse til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * **Fuld adgang til Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** er en nødvendig tilladelse, så en automatisk oprettet [!INCLUDE[prod_short](includes/prod_short.md)]-integrationsprogrambruger kan få adgang til [!INCLUDE[prod_short](includes/prod_short.md)]-data, der skal synkroniseres.  
> * **Logge på og læse din profil** er en nødvendig tilladelse for at kontrollere, at brugeren, som logger på, faktisk er tildelt Systemadministrator som sikkerhedsrolle i [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Ved at give samtykke på vegne af organisationen giver administratoren det registrerede Azure-program, der hedder [!INCLUDE[prod_short](includes/prod_short.md)]-integration til [!INCLUDE[cds_long_md](includes/cds_long_md.md)], ret til at synkronisere data ved hjælp af den automatisk oprettede [!INCLUDE[prod_short](includes/prod_short.md)]-integrationsprogrambrugers legitimationsoplysninger.

### <a name="to-use-the-common-data-service-connection-setup-assisted-setup-guide"></a>Sådan bruger du vejledningen Common Data Service-forbindelsesopsætning med assisteret opsætning
Common Data Service-forbindelsesopsætningsvejledning kan gøre det nemmere at oprette forbindelse til programmerne, og det kan også være en hjælp til at starte en første synkronisering. Hvis du vælger at køre første synkronisering, [!INCLUDE[prod_short](includes/prod_short.md)]gennemgås dataene i begge programmer, og der gives anbefalinger om, hvordan den første synkronisering nærmer sig. Den følgende tabel beskriver de forskellige anbefalinger.

|Anbefaling  |Description  |
|---------|---------|
|**Fuld synkronisering**|Dataene findes kun i [!INCLUDE[prod_short](includes/prod_short.md)], eller kun i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Det anbefales at synkronisere alle data fra den tjeneste, der har den til den anden tjeneste.|
|**Ingen synkronisering**|Dataene findes i begge programmer, og hvis du udfører fuld synkronisering, duplikeres dataene. Det anbefales at koble registreringer.|
|**Afhængighed er ikke opfyldt**|Der findes data i begge programmer, men rækken eller tabellen kan ikke synkroniseres, fordi den afhænger af en række eller en tabel, der ikke har nogen synkroniserings anbefaling. Hvis kunder f. eks. ikke kan synkroniseres, kan data til kontakter, der afhænger af kundedata, ikke synkroniseres.|

> [!IMPORTANT]
> Du bruger som regel kun fuld synkronisering, når du integrerer programmerne første gang, og kun ét program indeholder data. Fuld synkronisering kan være nyttig i et demonstrationsmiljø, da det automatisk opretter og forbinder poster i hvert program, hvilket gør det hurtigere at starte med at arbejde med synkroniserede data. Men du bør kun udføre en fuldstændig synkronisering, hvis du ønsker en række i [!INCLUDE[prod_short](includes/prod_short.md)] for hver række i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] for de givne tabeltilknytninger. Ellers kan resultatet være duplikerede poster.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Assisteret opsætning**, og vælg derefter det relaterede link.
2. Vælg **Konfigurer Dataverse-forbindelse** for at starte den assisterede opsætningsvejledning.
3. Udfyld felterne efter behov.

> [!NOTE]
> Hvis du ikke bliver bedt om at logge på med din administratorkonto, skyldes det sandsynligvis, at pop op-vinduer er blokeret. Du kan logge på ved at tillade pop op-vinduer fra `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Sådan oprettes eller vedligeholdes forbindelsen manuelt

Følgende procedure beskriver, hvordan du kan opsætte forbindelsen manuelt på siden **Common Data Service-forbindelsesopsætning**. Det er også den side, hvor du administrerer indstillingerne til integration.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfiguration af Common Data Service-forbindelse** og vælg dernæst det relaterede link.
2. Indtast følgende oplysninger vedrørende forbindelsen fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Felt|Beskrivelse|
    |-----|-----|
    |**URL-adresse til miljø**|Hvis du ejer miljøer i [!INCLUDE[cds_long_md](includes/cds_long_md.md)], finder vi dem for dig, når du kører installationsvejledningen. Hvis du vil oprette forbindelse til et andet miljø i en anden lejer, kan du angive administrator-legitimationsoplysninger til miljøet, og dem vil vi registrere. |
    |**Aktiveret**|Begynd at bruge integrationen. Hvis du ikke kan aktivere forbindelse nu, gemmes forbindelsesindstillingerne, men brugerne vil ikke kunne få adgang til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] data fra [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan vende tilbage til denne side og aktivere forbindelsen senere.  |

3. I feltet **Ejerskabsmodel** skal du vælge, om du vil have en teamtabel i [!INCLUDE[cds_long_md](includes/cds_long_md.md)], der skal eje nye poster, eller om der skal være en eller flere bestemte brugere. Hvis du vælger **Person**, skal du angive hver enkelt bruger. Hvis du vælger **Team**, vises standard-koncernvirksomheden i feltet **Sammenkædet koncernvirksomhed**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

   <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field-->|

4. Du kan teste forbindelsesindstillingerne ved at vælge **Forbindelse** og derefter **Test forbindelse**.  

    > [!NOTE]  
    > Hvis datakryptering ikke er aktiveret i [!INCLUDE[prod_short](includes/prod_short.md)], bliver du spurgt, om du vil aktivere den. Du aktiverer datakryptering ved at vælge **Ja** og angive de nødvendige oplysninger. Ellers skal du vælge **Nej**. Du kan aktivere datakryptering senere. Du kan finde flere oplysninger i [Kryptere data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) i hjælp til udvikleren og administrationen.  

5. Hvis [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-synkronisering ikke allerede er konfigureret, bliver du spurgt, om du vil bruge standardkonfigurationen for synkronisering. Afhængigt af om du vil bevare poster justeret i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)], skal du vælge **Ja** eller **Nej**.
<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="connecting-on-premises-versions"></a>Tilslutning af lokale versioner

Hvis du vil forbinde [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø med [!INCLUDE[cds_long_md](includes/cds_long_md.md)], skal du angive nogle oplysninger på siden **Konfiguration af Common Data Service-forbindelse**.

Hvis du vil oprette forbindelse ved hjælp af en Azure Active Directory-konto (Azure AD), skal du registrere et program i Azure AD og angive program-id'et, Key Vault-hemmeligheden og den omdirigerings-URL-adresse, der skal bruges. URL-adressen til omdirigering er forudindstillet og bør fungere for de fleste installationer. Du skal konfigurere installationen til at bruge HTTPS. Du kan finde flere oplysninger under [Konfigurere SSL for at sikre forbindelsen til Business Central-webklienten](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Hvis du opsætter serveren, så den har en anden startside, kan du altid ændre URL-adressen. Klientens hemmelighed gemmes som en krypteret streng i din database.  

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-dataverse"></a>Sådan registrerer du et program i Azure AD for at oprette forbindelse fra Business Central til Dataverse

I følgende trin antages det, at du bruger Azure AD til at administrere identiteter og adgangsrettigheder. Du kan finde flere oplysninger om registrering af et program i Azure AD under [Hurtig start: registrere et program på Microsoft-identitetsplatformen](/azure/active-directory/develop/quickstart-register-app). Hvis du ikke bruger Azure AD, kan du se [Bruge en anden tjeneste til identitets- og adgangsstyring](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-idtable-and-access-management-service).  

1. Vælg **Godkendelse** under **Administrer** i navigationsruden på Azure-portalen.  
2. Tilføj under **URL-adresse til omdirigering** den URL-adresse til omdirigering, der foreslås på siden til **Konfiguration af Common Data Service-forbindelse** i [!INCLUDE[prod_short](includes/prod_short.md)].
3. Vælg **API-tilladelser** under **Administrer**.
4. Vælg **Tilføj en tilladelse** under **Konfigurerede tilladelser**, og tilføj derefter delegerede tilladelser under fanen **Microsoft API'er** på følgende måde:
    * For Business Central skal du tilføje tilladelserne **Financials.ReadWrite.All**.
    * For Dynamics CRM skal du tilføje tilladelserne **user_impersonation**.  

    > [!NOTE]
    > Navnet på Dynamics CRM-API'en ændres muligvis.

5. Vælg **Certifikater og hemmeligheder** under **Administrer**, og opret derefter en ny hemmelighed til din app. Du skal enten bruge hemmeligheden i [!INCLUDE[prod_short](includes/prod_short.md)], i feltet **Klienthemmelighed** på siden til **Konfiguration af Common Data Service-forbindelse** eller gemme den i et sikkert lager og angive den i en hændelsesabonnent som beskrevet tidligere i dette emne.
6. Vælg **Oversigt**, og find derefter **Program-id (klient)**-værdien . Dette er programmets klient-id. Du skal enten angive det på siden **Konfiguration af Common Data Service-forbindelse** i feltet **Klient-id** eller gemme det i et sikkert lager og angive det i en hændelsesabonnent.
7. I [!INCLUDE[prod_short](includes/prod_short.md)] skal du på siden **Konfiguration af Common Data Service-forbindelse** i feltet **URL-adresse for miljø** angive URL-adressen til dit [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljø.
8. Du skal aktivere forbindelsen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ved at slå **Aktiveret** til.
9. Log på med din administratorkonto til Azure Active Directory (kontoen skal have en gyldig licens til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og være administrator i dit [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljø). Når du er logget på, bliver du bedt om at tillade, at dit registrerede program logger på [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på vegne af organisationen. Du skal give samtykke for at fuldføre installationen.

   > [!NOTE]
   > Hvis du ikke bliver bedt om at logge på med din administratorkonto, skyldes det sandsynligvis, at pop op-vinduer er blokeret. Du kan logge på ved at tillade pop op-vinduer fra `https://login.microsoftonline.com`.

#### <a name="using-another-idtable-and-access-management-service"></a>Bruge en anden tjeneste til identitets- og adgangsstyring

Hvis du ikke bruger Azure Active Directory til at administrere identiteter og adgangsrettigheder, skal du have hjælp fra en udvikler. Hvis du foretrækker at gemme app-id'et og hemmeligheden et andet sted, kan du lade felterne Klient-id og Klienthemmelighed være tomme og skrive en udvidelse for at hente id'et og hemmeligheden fra placeringen. Du kan levere hemmeligheden på kørselstidspunktet ved at abonnere på OnGetCDSConnectionClientId- og OnGetCDSConnectionClientSecret-hændelserne i codeunit 7201 "CDS Integration Impl."

### <a name="to-disconnect-from-cds_long_md"></a>Sådan afbrydes forbindelsen fra [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfiguration af Common Data Service-forbindelse** og vælg dernæst det relaterede link.
2. På siden **Common Data Service-forbindelsesopsætning** skal du slå **Aktiveret** fra.  

## <a name="see-also"></a>Se også

[Se status på en synkronisering](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]