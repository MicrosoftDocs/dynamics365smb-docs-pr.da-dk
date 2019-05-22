---
title: Oprette forbindelse til Dynamics 365 for Sales | Microsoft Docs
description: Du kan foretage integration med Dynamics 365 for Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 28ce599b2067faa904f917f8fce7390202c98d7b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245753"
---
# <a name="set-up-a-connection-to-dynamics-365-for-sales"></a>Oprette forbindelse til Dynamics 365 for Sales
Hvis der skal integreres med [!INCLUDE[crm_md](includes/crm_md.md)], skal du konfigurere en forbindelse mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)]. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085501]

## <a name="before-you-start"></a>Før du starter
Før du begynder at oprette forbindelse til programmerne, er der nogle oplysninger, der kan være nyttige at have ved hånden:  

* En URL-adresse til din [!INCLUDE[crm_md](includes/crm_md.md)]-app. Du kan hurtigt få URL-adressen ved at åbne [!INCLUDE[crm_md](includes/crm_md.md)] og kopiere URL-adressen og indsætte den i feltet **Dynamics 365 for Sales URL** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. [!INCLUDE[d365fin](includes/d365fin_md.md)] retter formateringen for dig.  
* Et brugernavn og adgangskode for en brugerkonto, der udelukkende bruges til integrationen.  
* Brugernavn og adgangskode til den konto, der har administratorrettigheder.  
  
> [!Note]
> I fremgangsmåden nedenfor beskrives proceduren for onlineversionen af [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-test-and-enable-a-connection-to-includecrmmdincludescrmmdmd"></a>Konfigurere, teste og aktivere en forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)]  
For alle andre godkendelsestyper end Office 365-godkendelse kan du konfigurere forbindelse til Dynamics 365 for Sales på siden **Konfiguration af Microsoft Dynamics 365 for Sales-forbindelse**. I forbindelse med Office 365-godkendelse kan du også bruge den assisterede opsætningsvejledning **Konfigurer Dynamics 365 for Sales-forbindelse**, som hjælper dig med at angive de nødvendige oplysninger.

### <a name="to-use-an-assisted-setup-guide"></a>Sådan bruges en assisteret opsætningsvejledning
Den assisterede opsætningsvejledning **Konfigurer Dynamics 365 for Sales-forbindelse** kan hjælpe dig med at oprette forbindelsen og angive, om avancerede funktioner som f.eks. sammenkædning mellem poster skal aktiveres. 

1. Vælg **Installation og udvidelser**, og vælg derefter **Assisteret opsætning**.
2. Vælg **Konfigurer Dynamics 365 for Sales-forbindelse** for at starte den assisterede opsætningsvejledning.
3. Udfyld felterne efter behov.
4. Der er også avancerede indstillinger, der kan forbedre sikkerhed og aktivere [!INCLUDE[crm_md](includes/crm_md.md)] ekstra funktioner, f.eks. behandling af salgsordrer og visning af lagerniveauer. Den følgende tabel beskriver de avancerede indstillinger.  

|Felt|Description|
|-----|-----|
|**Importér Dynamics 365 for Sales-løsning**|Aktivér denne for at installere og konfigurere integrationsløsningen i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Om Business Central integrationsløsning](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|
|**Udgiv webtjeneste Varedisponering**|Aktivér brugere, der bruger [!INCLUDE[crm_md](includes/crm_md.md)] til at få vist tilgængeligheden af varer (produkter) på lager i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette kræver [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugerkonto med en adgangsnøgle til webtjenester. Tildeling af nøglen er en totrinsproces. I brugerkontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du vælge handlingen **Ændr webtjenestenøgle**. I den assisterede opsætningsvejledning Konfigurer Dynamics 365 for Sales-forbindelse skal du angive URL-adresse til Dynamics 365 Business Central OData-webtjeneste og angive [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugeroplysninger for at få adgang til tjenesten. Du kan finde flere oplysninger i [OData-webtjenester](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**URL-adresse til Dynamics 365 Business Central OData-webtjeneste**|Hvis du aktiverer Webtjenesten Varedisponering, er URL-adressen for OData-webtjenesten udfyldt.|
|**Brugernavn til Dynamics 365 Business Central OData-webtjeneste**|Navnet på [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugerkontoen, som [!INCLUDE[crm_md](includes/crm_md.md)] bruger til at hente oplysninger om varetilgængelighed i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af OData-webtjenesten.|
|**Adgangsnøgle til Dynamics 365 Business Central OData-webtjeneste**|Adgangsnøglen til brugerkontoen, som [!INCLUDE[crm_md](includes/crm_md.md)] bruger til at hente oplysninger om varetilgængelighed fra [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af OData-webtjenesten. Nøglen er knyttet til den bruger, der er valgt i feltet **Brugernavn til Dynamics 365 Business Central OData-webtjeneste**. For at få nøglen skal du vælge knappen **Slå værdi op** ved siden af brugernavnet, vælge brugeren, vælge **Administrer** og derefter **Rediger**. På brugerkortet skal du vælge **Handlinger**, **Godkendelse** og derefter klikke på **Ændr webtjenestenøgle**.|
|**Aktivér integration af salgsordrer**|Når brugere opretter salgsordrer i [!INCLUDE[crm_md](includes/crm_md.md)], kopieres ordrerne til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette kræver, at du angiver legitimationsoplysninger for en administratorbrugerkonto i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Håndtering af salgsordredata](marketing-integrate-dynamicscrm.md#handling-sales-order-data).|
|**Aktivér Dynamics 365 for Sales-forbindelse**|Aktivér forbindelsen til [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Dynamics 365 SDK Version**|Det er kun relevant, hvis du integrerer med en lokal version af [!INCLUDE[crm_md](includes/crm_md.md)]. Det er det Dynamics 365 software development kit (også kaldet Xrm), du bruger til at forbinde [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]. Versionen skal være kompatibel med den version af SDK, som bruges af [!INCLUDE[crm_md](includes/crm_md.md)], og være lig med eller nyere end den version, der bruges af [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="to-create-or-maintain-the-connection-manually"></a>Sådan oprettes eller vedligeholdes forbindelsen manuelt
Følgende procedure beskriver, hvordan du kan udfylde felterne på siden **Konfiguration af Microsoft Dynamics 365 for Sales-forbindelse** manuelt. Det er også den side, hvor du administrerer indstillingerne til integration.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfiguration af Microsoft Dynamics 365-forbindelse,** og vælg derefter det tilhørende link.
2. Indtast følgende oplysninger vedrørende forbindelsen fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)].

|Felt|Description|
|-----|-----|
|**Dynamics 365 for Sales URL-adresse**|URL-adressen til din forekomst af [!INCLUDE[crm_md](includes/crm_md.md)]. Når du vil hente URL-adressen, skal du åbne [!INCLUDE[crm_md](includes/crm_md.md)], kopiere URL-adressen fra adresselinjen i din webbrowser og derefter indsætte URL-adressen i feltet. [!INCLUDE[d365fin](includes/d365fin_md.md)] sikrer, at formatet er korrekt.|
|**Brugernavn** og **Adgangskode**|Legitimationsoplysninger for den brugerkonto, der er dedikeret til integration. Du kan finde flere oplysninger i [Konfigurere brugerkonti til integration med Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).|
|**Aktiveret**|Begynd at bruge integrationen. Hvis du ikke kan aktivere forbindelse nu, gemmes forbindelsesindstillingerne, men brugerne vil ikke kunne få adgang til [!INCLUDE[crm_md](includes/crm_md.md)] data fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan vende tilbage til denne side og aktivere forbindelsen senere.  |
|**Dynamics 365 SDK Version**|Hvis du integrerer med en lokal version af [!INCLUDE[crm_md](includes/crm_md.md)], er det Dynamics 365 software development kit (også kaldet Xrm), du bruger til at forbinde [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]. Den version, du har valgt, skal være kompatibel med den version af SDK, som bruges af [!INCLUDE[crm_md](includes/crm_md.md)]. Versionen er lig med eller nyere end den version, der bruges af [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> Hvis du forbinder en lokal version af [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)], og du vil konfigurere en forbindelse til en forekomst af [!INCLUDE[crm_md](includes/crm_md.md)] med en bestemt godkendelsestype, skal du udfylde felterne i oversigtspanelet **Detaljer om godkendelsestype**. Du kan finde flere oplysninger i [Brug forbindelsesstrenge i XRM-værktøjer til at oprette forbindelse til Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Dette trin er ikke obligatorisk, når du opretter forbindelse for en onlineversion af [!INCLUDE[d365fin](includes/d365fin_md.md)].

3. Indtast følgende oplysninger vedrørende forbindelsen fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Felt|Description|
|-----|-----|
|**Dynamics 365 Business Central URL-forbindelse til webklient**|URL-adressen for din [!INCLUDE[d365fin](includes/d365fin_md.md)]-forekomst. Dette gør det muligt for brugere i [!INCLUDE[crm_md](includes/crm_md.md)] at åbne tilsvarende poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] fra poster i [!INCLUDE[crm_md](includes/crm_md.md)], f.eks. et firma eller produkt. [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster åbnes i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Indstil dette felt til URL-adressen på den [!INCLUDE[d365fin](includes/d365fin_md.md)]-forekomst, der skal bruges.<br /><br /> Du kan nulstille feltet til standard-URL-adressen for [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at vælge handlingen **Nulstil URL-adresse til webklient**.<br /><br /> Dette felt er kun relevant, hvis [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrationsløsningen er installeret i [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Webtjenesten Varedisponering er aktiveret**|Aktivér brugere, der bruger [!INCLUDE[crm_md](includes/crm_md.md)] til at få vist tilgængeligheden af varer (produkter) på lager i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du aktiverer dette, skal du også angive et brugernavn og en adgangsnøgle, som [!INCLUDE[crm_md](includes/crm_md.md)] skal bruge til at forespørge OData-webtjenesten om tilgængelighed af varer (produkter). Du kan finde flere oplysninger i [OData-webtjenester](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**URL-adresse til Dynamics 365 Business Central OData-webtjeneste**|Hvis du aktiverer Webtjenesten Varedisponering, er URL-adressen for OData-webtjenesten udfyldt.|
|**Brugernavn til Dynamics 365 Business Central OData-webtjeneste**|Navnet på den brugerkonto, som [!INCLUDE[crm_md](includes/crm_md.md)] bruger til at hente oplysninger om varetilgængelighed fra [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af OData-webtjenesten.|
|**Adgangsnøgle til Dynamics 365 Business Central OData-webtjeneste**|Adgangsnøglen til brugerkontoen, som [!INCLUDE[crm_md](includes/crm_md.md)] bruger til at hente oplysninger om varetilgængelighed fra [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af OData-webtjenesten. Nøglen er knyttet til den bruger, der er valgt i feltet **Brugernavn til Dynamics 365 Business Central OData-webtjeneste**. For at få nøglen skal du vælge knappen **Slå værdi op** ved siden af brugernavnet, vælge brugeren, vælge **Administrer** og derefter **Rediger**. På brugerkortet skal du vælge **Handlinger**, **Godkendelse** og derefter klikke på **Ændr webtjenestenøgle**.|

4. Angiv følgende indstillinger for [!INCLUDE[crm_md](includes/crm_md.md)].

|Felt|Description|
|-----|-----|
|**Salgsordreintegration er aktiveret**|Brugerne skal kunne afsende salgsordrer og aktiverede tilbud i [!INCLUDE[crm_md](includes/crm_md.md)] og derefter få vist og behandle dem i [!INCLUDE[d365fin](includes/d365fin_md.md)].|
|**Opret salgsordrer automatisk**|Opret en salgsordre i [!INCLUDE[d365fin](includes/d365fin_md.md)], når en bruger opretter og sender en i [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Behandl salgstilbud automatisk**|Behandl et salgstilbud i [!INCLUDE[d365fin](includes/d365fin_md.md)], når en bruger opretter og aktiverer et i [!INCLUDE[crm_md](includes/crm_md.md)].|

5. Angiv følgende avancerede indstillinger.

|Felt|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Brugere skal tilknyttes Dynamics 365 for Sales-brugere**|Angiv, om [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugerkonti skal have tilsvarende brugerkonti i [!INCLUDE[crm_md](includes/crm_md.md)]. **Office 365-godkendelsesmailadresse**for [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugeren skal være den samme som **Primær mail** for [!INCLUDE[crm_md](includes/crm_md.md)]-brugeren.<br /><br /> Hvis du angiver værdien til **Ja**, har [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere, der ikke har en tilsvarende [!INCLUDE[crm_md](includes/crm_md.md)]-brugerkonto, ikke [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrationsfunktioner i brugergrænsefladen. Adgang til [!INCLUDE[crm_md](includes/crm_md.md)]-data direkte fra [!INCLUDE[d365fin](includes/d365fin_md.md)] udføres på vegne af [!INCLUDE[crm_md](includes/crm_md.md)]-brugerkontoen.<br /><br /> Hvis du angiver værdien til **Nej**, har alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere [!INCLUDE[crm_md](includes/crm_md.md)]-integrationsfunktioner i brugergrænsefladen. Adgang til [!INCLUDE[crm_md](includes/crm_md.md)]-data udføres på vegne af [!INCLUDE[crm_md](includes/crm_md.md)]-forbindelsesbrugeren (integrations).|
|**Den aktuelle Business Central-bruger er knyttet til en Dynamics 365 for Sales-bruger**|Angiver, om din brugerkonto er knyttet til en konto i [!INCLUDE[crm_md](includes/crm_md.md)]|

6. Du kan teste forbindelsesindstillingerne ved at vælge **Afprøv forbindelse**.  

    > [!NOTE]  
    >  Hvis datakryptering ikke er aktiveret i [!INCLUDE[d365fin](includes/d365fin_md.md)], bliver du spurgt, om du vil aktivere den. Du aktiverer datakryptering ved at vælge **Ja** og angive de nødvendige oplysninger. Ellers skal du vælge **Nej**. Du kan aktivere datakryptering senere. Du kan finde flere oplysninger i [Kryptere data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) i hjælp til udviklere og it-eksperter.  

7. Hvis [!INCLUDE[crm_md](includes/crm_md.md)]-synkronisering ikke allerede er konfigureret, bliver du spurgt, om du vil bruge standardkonfigurationen for synkronisering. Afhængigt af om du vil bevare poster justeret i [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du vælge **Ja** eller **Nej**. 

### <a name="to-disconnect-from-includecrmmdincludescrmmdmd"></a>Sådan afbrydes forbindelsen fra [!INCLUDE[crm_md](includes/crm_md.md)]  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Microsoft Dynamics 365 for Sales Konfiguration af forbindelse,** og vælg derefter det tilhørende link.
2. Fjern markeringen i afkrydsningsfeltet **Aktiveret** på siden **Konfiguration af Microsoft Dynamics 365 for Sales-forbindelse**.  

<!--## Install the [!INCLUDE[d365fin](includes/d365fin_md.md) Integration Solution
[!INCLUDE[d365fin](includes/d365fin_md.md)] includes a solution that enables users to access coupled records, such as customers and items, from records in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts and products. The solution adds a link to the pages in [!INCLUDE[crm_md](includes/crm_md.md)] to open the coupled [!INCLUDE[d365fin](includes/d365fin_md.md)] record. The solution also displays information from [!INCLUDE[d365fin](includes/d365fin_md.md)]on certain entities in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts. Installing this solution is optional. <!--"Solution" sounds old school. Is it an app, or an add-in, or an extension? 


1.  From [!INCLUDE[d365fin](includes/d365fin_md.md)] installation media \(DVD\), copy the DynamicsNAVIntegrationSolution.zip file to your computer.  

     The DynamicsNAVIntegrationSolution.zip file is located in the **CrmCustomization** folder. This file is the solution package.   

2.  In [!INCLUDE[crm_md](includes/crm_md.md)], import the DynamicsNAVIntegrationSolution.zip as a solution.  

     This step adds the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity and **[!INCLUDE[d365fin](includes/d365fin_md.md) Account Statistics** entity in the system and additional items such as [!INCLUDE[d365fin](includes/d365fin_md.md)] integration security roles.  

     For more information about how to manage solutions in [!INCLUDE[crm_md](includes/crm_md.md)], [http://go.microsoft.com/fwlink/?LinkID=616519](http://go.microsoft.com/fwlink/?LinkID=616519).  

3.  Optional: Set up the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity to display in the **Settings** area of [!INCLUDE[crm_md](includes/crm_md.md)].  

     This enables [!INCLUDE[crm_md](includes/crm_md.md)] users who are assigned the **[!INCLUDE[d365fin](includes/d365fin_md.md) Admin** role to modify the entity in [!INCLUDE[crm_md](includes/crm_md.md)]. For more information about how to modify entities in [!INCLUDE[crm_md](includes/crm_md.md)], see [View or edit entity information](http://go.microsoft.com/fwlink/?LinkID=616521).  

4.  Assign the **[!INCLUDE[d365fin](includes/d365fin_md.md) Integration Administrator** role to the user account for the connection to [!INCLUDE[d365fin](includes/d365fin_md.md)].  

5.  Assign the **Business Central Integration User** role to all users who will use the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution.  

If you install the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution after you have set up the connection to [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must modify the connection setup to point to the URL.--> 

<!--of the [!INCLUDE[nav_web_md](../developer/includes/nav_web_md.md)]. For more information, see [How to: Set Up a Microsoft Dynamics 365 for Sales Connection]() --> 

<!-- 
# View Item Availability - Support Matrix
For most versions of [!INCLUDE[d365fin](includes/d365fin_md.md) and Dynamics 365 for Sales, you can view availability figures for items across the integrated products. The following table shows which version combinations support viewing item availability.

| |Dynamics 365 for Sales version|2015/Update 1/Online|2016/Update 1/Online|Dynamics 365 for Sales|
|-|---------------------|---------------------|--------------------------|-----------------|
|**Dynamics NAV version**|
|**2016**||Not supported|Not supported|Not supported|
|**2017**||Not supported - Install from 2016|Supported|Supported|
|**Dynamics 365 for Financials**||Not supported - Install from 2016|Supported|Supported|


> [Note]
> You can obtain item availability support for combinations of Dynamics CRM 2015 and Business Central by running the DynamicsNAVIntegrationSolution.zip file on the Business Central product DVD.

For more information, see [System Requirements for Business Central](../deployment/system-requirement-business-central.md).

-->

## <a name="see-also"></a>Se også  
[Se status på en synkronisering](admin-how-to-view-synchronization-status.md)  

