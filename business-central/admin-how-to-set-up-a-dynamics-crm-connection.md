---
title: Oprette forbindelse til Common Data Service | Microsoft Docs
description: Du kan integrere andre programmer med Business Central via Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/24/2020
ms.author: bholtorf
ms.openlocfilehash: e6ee18367ad229ab56d694d0bbac23e1959b1a5f
ms.sourcegitcommit: edad0d0b129e916c2cfdfa9c4f8d9d83513f4fd1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/24/2020
ms.locfileid: "3619405"
---
# <a name="connect-to-common-data-service"></a>Opret forbindelse til Common Data Service

Dette emne beskriver, hvordan du konfigurerer en forbindelse mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Virksomheder opretter typisk forbindelsen for at integrere og synkronisere data med en anden Dynamics 365-forretningsapp såsom [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Før du starter

Der er et par oplysninger, som du skal have klar, før du opretter forbindelsen:  

* URL-adressen til det [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljø, som du vil oprette forbindelse til. Hvis du bruger vejledningen **Opsætning af CDS-forbindelse** med assisteret opsætning til at oprette forbindelsen, registrerer vi dine miljøer, men du kan også angive URL-adressen til et andet miljø i din lejer.  
* Brugernavn og adgangskode til en konto, der har administratorrettigheder i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

> [!Note]
> I fremgangsmåden nedenfor beskrives proceduren for onlineversionen af [!INCLUDE[d365fin](includes/d365fin_md.md)].
> Hvis du bruger Business Central on-premises og ikke bruger en Azure Active Directory-konto til at oprette forbindelse til [!INCLUDE [cds_long_md](includes/cds_long_md.md)], skal du også angive brugernavn og adgangskode for en brugerkonto til integrationen. Denne konto kaldes "integrationsbruger"-kontoen. Hvis du bruger en Azure Active Directory-konto, er integrationsbrugerkontoen ikke påkrævet og vises ikke. Integrationsbrugeren konfigureres automatisk og kræver ikke en licens.

## <a name="set-up-a-connection-to-cds_long_md"></a>Oprette forbindelse til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

For alle andre godkendelsestyper end Office 365-godkendelse kan du konfigurere din forbindelse til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på siden **Opsætning af CDS-forbindelse**. For Office 365-godkendelse anbefaler vi, at du bruger den assisterede opsætningsvejledning **Konfigurer Common Data Service-forbindelse**. Denne vejledning gør det nemmere at oprette forbindelsen og angive avancerede funktioner, f.eks. ejerskabsmodel og indledende synkronisering.  

> [!IMPORTANT]
> Under konfigurationen af forbindelsen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] bliver administratoren bedt om at give følgende tilladelser til det registrerede Azure-program, der hedder [!INCLUDE[d365fin](includes/d365fin_md.md)]-integration med [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * **Få adgang til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] som** nødvendig tilladelse, så du [!INCLUDE[d365fin](includes/d365fin_md.md)] kan, på vegne af administratoren, automatisk oprette en ikke-licenseret, ikke-interaktiv [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrationsprogrambruger, tildele sikkerhedsroller til denne bruger og installere [!INCLUDE[d365fin](includes/d365fin_md.md)] Basis-CDS-integrationsløsningen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Denne tilladelse bruges kun én gang under oprettelse af forbindelse til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * **Fuld adgang til Dynamics 365 [!INCLUDE[d365fin](includes/d365fin_md.md)]** er en nødvendig tilladelse, så en automatisk oprettet [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrationsprogrambruger kan få adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)]-data, der skal synkroniseres.  
> * **Logge på og læse din profil** er en nødvendig tilladelse for at kontrollere, at brugeren, som logger på, faktisk er tildelt Systemadministrator som sikkerhedsrolle i [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Ved at give samtykke på vegne af organisationen giver administratoren det registrerede Azure-program, der hedder [!INCLUDE[d365fin](includes/d365fin_md.md)]-integration til [!INCLUDE[cds_long_md](includes/cds_long_md.md)], ret til at synkronisere data ved hjælp af den automatisk oprettede [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrationsprogrambrugers legitimationsoplysninger.

### <a name="to-use-the-set-up-common-data-service-connection-assisted-setup-guide"></a>Sådan bruger du vejledningen Konfigurer Common Data Service-forbindelse med assisteret opsætning

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Assisteret opsætning**, og vælg derefter det relaterede link.
2. Vælg **Konfigurer Common Data Service-forbindelse** for at starte den assisterede opsætningsvejledning.
3. Udfyld felterne efter behov.

### <a name="to-create-or-maintain-the-connection-manually"></a>Sådan oprettes eller vedligeholdes forbindelsen manuelt

Følgende procedure beskriver, hvordan du kan opsætte forbindelsen manuelt på siden **Opsæt CDS-forbindelse**. Det er også den side, hvor du administrerer indstillingerne til integration.

1. Vælg ikonet ![Elpære, der åbner ikonet til funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsæt CDS-forbindelse**, og vælg det relaterede link.
2. Indtast følgende oplysninger vedrørende forbindelsen fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Felt|Description|
    |-----|-----|
    |**URL-adresse til miljø**|Hvis du ejer miljøer i [!INCLUDE[cds_long_md](includes/cds_long_md.md)], finder vi dem for dig, når du kører installationsvejledningen. Hvis du vil oprette forbindelse til et andet miljø i en anden lejer, kan du angive administrator-legitimationsoplysninger til miljøet, og dem vil vi registrere. |
    |**Aktiveret**|Begynd at bruge integrationen. Hvis du ikke kan aktivere forbindelse nu, gemmes forbindelsesindstillingerne, men brugerne vil ikke kunne få adgang til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] data fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan vende tilbage til denne side og aktivere forbindelsen senere.  |

3. I feltet **Ejerskabsmodel** skal du vælge, om du vil have et teamobjekt i [!INCLUDE[cds_long_md](includes/cds_long_md.md)], der skal eje nye poster, eller om der skal være en eller flere bestemte brugere. Hvis du vælger **Person**, skal du angive hver enkelt bruger. Hvis du vælger **Team**, vises standard-koncernvirksomheden BCI_Company i feltet **Sammenkædet koncernvirksomhed**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?-->
    Angiv følgende avancerede indstillinger.

    |Felt|Description|
    |-----|-----|
    |**[!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere skal tilknyttes CDS-brugere**|Hvis du bruger din ejerskabsmodellen Person, skal du angive, om [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugerkonti skal have tilsvarende brugerkonti i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. **Office 365-godkendelsesmailadresse** for [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugeren skal være den samme som **Primær mail** for [!INCLUDE[crm_md](includes/crm_md.md)]-brugeren.<br /><br /> Hvis du angiver værdien til **Ja**, har [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere, der ikke har en tilsvarende [!INCLUDE[crm_md](includes/crm_md.md)]-brugerkonto, ikke [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrationsfunktioner i brugergrænsefladen. Adgang til [!INCLUDE[crm_md](includes/crm_md.md)]-data direkte fra [!INCLUDE[d365fin](includes/d365fin_md.md)] udføres på vegne af [!INCLUDE[crm_md](includes/crm_md.md)]-brugerkontoen.<br /><br /> Hvis du angiver værdien til **Nej**, har alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere [!INCLUDE[crm_md](includes/crm_md.md)]-integrationsfunktioner i brugergrænsefladen. Adgang til [!INCLUDE[crm_md](includes/crm_md.md)]-data udføres på vegne af [!INCLUDE[crm_md](includes/crm_md.md)]-forbindelsesbrugeren (integrations).|
    |**Den aktuelle Business Central-sælger er tilknyttet en bruger**|Angiver, om din brugerkonto er tilknyttet en konto i [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Du kan teste forbindelsesindstillingerne ved at vælge **Forbindelse** og derefter **Test forbindelse**.  

    > [!NOTE]  
    > Hvis datakryptering ikke er aktiveret i [!INCLUDE[d365fin](includes/d365fin_md.md)], bliver du spurgt, om du vil aktivere den. Du aktiverer datakryptering ved at vælge **Ja** og angive de nødvendige oplysninger. Ellers skal du vælge **Nej**. Du kan aktivere datakryptering senere. Du kan finde flere oplysninger i [Kryptere data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) i hjælp til udvikleren og administrationen.  

5. Hvis [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-synkronisering ikke allerede er konfigureret, bliver du spurgt, om du vil bruge standardkonfigurationen for synkronisering. Afhængigt af om du vil bevare poster justeret i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du vælge **Ja** eller **Nej**.

## <a name="show-me-the-process"></a>Vis processen

Følgende video viser fremgangsmåden for at oprette forbindelse til [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

## <a name="connecting-on-premises-versions"></a>Tilslutning af lokale versioner

Hvis du vil forbinde [!INCLUDE[d365fin](includes/d365fin_md.md)] i det lokale miljø med [!INCLUDE[cds_long_md](includes/cds_long_md.md)], skal du angive nogle oplysninger på siden **Konfiguration af Common Data Service-forbindelse**.

Hvis du vil oprette forbindelse ved hjælp af en Azure Active Directory-konto (Azure AD), skal du registrere et program i Azure AD og angive program-id'et, Key Vault-hemmeligheden og den omdirigerings-URL-adresse, der skal bruges. URL-adressen til omdirigering er forudindstillet og bør fungere for de fleste installationer. Du skal konfigurere installationen til at bruge HTTPS. Du kan finde flere oplysninger under [Konfigurere SSL for at sikre forbindelsen til Business Central-webklienten](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Hvis du opsætter serveren, så den har en anden startside, kan du altid ændre URL-adressen. Klientens hemmelighed gemmes som en krypteret streng i din database.  

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-common-data-service"></a>Sådan registrerer du et program i Azure AD for at oprette forbindelse fra Business Central til Common Data Service

I følgende trin antages det, at du bruger Azure AD til at administrere identiteter og adgangsrettigheder. Du kan finde flere oplysninger om registrering af et program i Azure AD under [Hurtig start: registrere et program på Microsoft-identitetsplatformen](/azure/active-directory/develop/quickstart-register-app). Hvis du ikke bruger Azure AD, kan du se [Bruge en anden tjeneste til identitets- og adgangsstyring](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-identity-and-access-management-service).  

1. Vælg **Godkendelse** under **Administrer** i navigationsruden på Azure-portalen.  
2. Tilføj under **URL-adresse til omdirigering** den URL-adresse til omdirigering, der foreslås på siden til **Konfiguration af Common Data Service-forbindelse** i [!INCLUDE[d365fin](includes/d365fin_md.md)].
3. Vælg **API-tilladelser** under **Administrer**.
4. Vælg **Tilføj en tilladelse** under **Konfigurerede tilladelser**, og tilføj derefter delegerede tilladelser under fanen **Microsoft API'er** på følgende måde:
    * For Business Central skal du tilføje tilladelserne **Financials.ReadWrite.All**.
    * For Dynamics CRM skal du tilføje tilladelserne **user_impersonation**.  

    > [!NOTE]
    > Navnet på Dynamics CRM-API'en ændres muligvis.

5. Vælg **Certifikater og hemmeligheder** under **Administrer**, og opret derefter en ny hemmelighed til din app. Du skal enten bruge hemmeligheden i [!INCLUDE[d365fin](includes/d365fin_md.md)], i feltet **Klienthemmelighed** på siden til **Konfiguration af Common Data Service-forbindelse** eller gemme den i et sikkert lager og angive den i en hændelsesabonnent som beskrevet tidligere i dette emne.
6. Vælg **Oversigt**, og find derefter **Program-id (klient)**-værdien . Dette er programmets klient-id. Du skal enten angive det på siden **Konfiguration af Common Data Service-forbindelse** i feltet **Klient-id** eller gemme det i et sikkert lager og angive det i en hændelsesabonnent.
7. I [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du på siden **Konfiguration af Common Data Service-forbindelse** i feltet **URL-adresse for miljø** angive URL-adressen til dit [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljø.
8. Du skal aktivere forbindelsen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ved at slå **Aktiveret** til.
9. Log på med din administratorkonto til Azure Active Directory (kontoen skal have en gyldig licens til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og være administrator i dit [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljø). Når du er logget på, bliver du bedt om at tillade, at dit registrerede program logger på [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på vegne af organisationen. Du skal give samtykke for at fuldføre installationen.

   > [!NOTE]
   > Hvis du ikke bliver bedt om at logge på med din administratorkonto, skyldes det sandsynligvis, at pop op-vinduer er blokeret. Du kan logge på ved at tillade pop op-vinduer fra `https://login.microsoftonline.com`.

#### <a name="using-another-identity-and-access-management-service"></a>Bruge en anden tjeneste til identitets- og adgangsstyring

Hvis du ikke bruger Azure Active Directory til at administrere identiteter og adgangsrettigheder, skal du have hjælp fra en udvikler. Hvis du foretrækker at gemme app-id'et og hemmeligheden et andet sted, kan du lade felterne Klient-id og Klienthemmelighed være tomme og skrive en udvidelse for at hente id'et og hemmeligheden fra placeringen. Du kan levere hemmeligheden på kørselstidspunktet ved at abonnere på OnGetCDSConnectionClientId- og OnGetCDSConnectionClientSecret-hændelserne i codeunit 7201 "CDS Integration Impl."

### <a name="to-disconnect-from-cds_long_md"></a>Sådan afbrydes forbindelsen fra [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Vælg ikonet ![Elpære, der åbner ikonet til funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsæt CDS-forbindelse**, og vælg det relaterede link.
2. På siden **Opsæt CDS-forbindelse** skal du slå **Aktiveret** fra.  

## <a name="see-also"></a>Se også

[Se status på en synkronisering](admin-how-to-view-synchronization-status.md)  
