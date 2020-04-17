---
title: Oprette forbindelse til Dynamics 365 Sales | Microsoft Docs
description: Du kan integrere andre programmer med Business Central via Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3375db0208d1a0275011f0efbfce4a13102c522e
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196635"
---
# <a name="connect-to-common-data-service"></a>Opret forbindelse til Common Data Service
Dette emne beskriver, hvordan du konfigurerer en forbindelse mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)]. Virksomheder opretter typisk forbindelsen for at integrere og synkronisere data med en anden Dynamics 365-forretningsapp såsom [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Før du starter
Der er et par oplysninger, som du skal have klar, før du opretter forbindelsen:  

* URL-adressen til det [!INCLUDE[d365fin](includes/cds_long_md.md)]-miljø, som du vil oprette forbindelse til. Hvis du bruger vejledningen **Opsætning af CDS-forbindelse** med assisteret opsætning til at oprette forbindelsen, registrerer vi dine miljøer, men du kan også angive URL-adressen til et andet miljø i din lejer.  
* Et brugernavn og adgangskode for en brugerkonto, der udelukkende bruges til integrationen. Denne konto kaldes "integrationsbruger"-kontoen. 
* Brugernavn og adgangskode til en konto, der har administratorrettigheder i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)].  

> [!Note]
> I fremgangsmåden nedenfor beskrives proceduren for onlineversionen af [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-a-connection-to-d365fin"></a>Oprette forbindelse til [!INCLUDE[d365fin](includes/cds_long_md.md)]  
For alle andre godkendelsestyper end Office 365-godkendelse kan du konfigurere din forbindelse til [!INCLUDE[d365fin](includes/cds_long_md.md)] på siden **Opsætning af CDS-forbindelse**. For Office 365-godkendelse anbefaler vi, at du bruger vejledningen **Opsætning af CDS-forbindelse** med assisteret opsætning. Denne vejledning gør det nemmere at oprette forbindelsen og angive avancerede funktioner, f. eks. sammenkædning mellem poster.  

### <a name="to-use-the-cds-connection-setup-assisted-setup-guide"></a>Sådan bruger du vejledningen Opsætning af CDS-forbindelse med assisteret opsætning 
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Assisteret opsætning**, og vælg derefter det relaterede link.
2. Vælg **Konfigurer CDS-basisintegrationsforbindelse** for at starte den assisterede opsætningsvejledning.
3. Udfyld felterne efter behov.

> [!Note]
> Vejledningen **Opsætning af CDS-forbindelse** med assisteret opsætning tildeler **Integrationsadministrator**- og **Integrationsbruger**-sikkerhedsroller til den brugerkonto, der bruges til integration, og indstiller adgangstilstanden for kontoen til **ikke-interaktiv**.

### <a name="to-create-or-maintain-the-connection-manually"></a>Sådan oprettes eller vedligeholdes forbindelsen manuelt
Følgende procedure beskriver, hvordan du kan opsætte forbindelsen manuelt på siden **Opsæt CDS-forbindelse**. Det er også den side, hvor du administrerer indstillingerne til integration.

1. Vælg ikonet ![Elpære, der åbner ikonet til funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsæt CDS-forbindelse**, og vælg det relaterede link.
2. Indtast følgende oplysninger vedrørende forbindelsen fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[d365fin](includes/cds_long_md.md)].

|Felt|Description|
|-----|-----|
|**URL-adresse til miljø**|Hvis du ejer miljøer i [!INCLUDE[d365fin](includes/cds_long_md.md)], finder vi dem for dig, når du kører installationsvejledningen. Hvis du vil oprette forbindelse til et andet miljø i en anden lejer, kan du angive administrator-legitimationsoplysninger til miljøet, og dem vil vi registrere. |
|**Brugernavn** og **Adgangskode**|Legitimationsoplysninger for den brugerkonto, der er dedikeret til integration. Du kan finde flere oplysninger i [Konfigurere brugerkonti til integration med [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).|
|**Aktiveret**|Begynd at bruge integrationen. Hvis du ikke kan aktivere forbindelse nu, gemmes forbindelsesindstillingerne, men brugerne vil ikke kunne få adgang til [!INCLUDE[d365fin](includes/cds_long_md.md)] data fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan vende tilbage til denne side og aktivere forbindelsen senere.  |

3. I feltet **Ejerskabsmodel** skal du vælge, om du vil have et teamobjekt i [!INCLUDE[d365fin](includes/cds_long_md.md)], der skal eje nye poster, eller om der skal være en eller flere bestemte brugere. Hvis du vælger **Person**, skal du angive hver enkelt bruger. Hvis du vælger **Team**, vises standard-koncernvirksomheden BCI_Company i feltet **Sammenkædet koncernvirksomhed**.

<!--Need to verify the details in this table, are these specific to Sales maybe?
Enter the following advanced settings.

|Field|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts must have a matching user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]. The **Office 365 Authentication Email** of the [!INCLUDE[d365fin](includes/d365fin_md.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[d365fin](includes/d365fin_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[d365fin](includes/d365fin_md.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[d365fin](includes/d365fin_md.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
|**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Du kan teste forbindelsesindstillingerne ved at vælge **Forbindelse** og derefter **Test forbindelse**.  

    > [!NOTE]  
    >  Hvis datakryptering ikke er aktiveret i [!INCLUDE[d365fin](includes/d365fin_md.md)], bliver du spurgt, om du vil aktivere den. Du aktiverer datakryptering ved at vælge **Ja** og angive de nødvendige oplysninger. Ellers skal du vælge **Nej**. Du kan aktivere datakryptering senere. Du kan finde flere oplysninger i [Kryptere data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data.md) i hjælp til udviklere og it-eksperter.  

5. Hvis [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkronisering ikke allerede er konfigureret, bliver du spurgt, om du vil bruge standardkonfigurationen for synkronisering. Afhængigt af om du vil bevare poster justeret i [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du vælge **Ja** eller **Nej**.

> [!Note]
> Når du opretter forbindelse til [!INCLUDE[d365fin](includes/cds_long_md.md)] ved hjælp af siden **Opsæt CDS-forbindelse**, kan det være nødvendigt, at du tildeler Integrationsadministrator- og Integrationsbruger-sikkerhedsroller til den konto, der bruges til integration i Dynamics 365 Sales. Du kan finde flere oplysninger i [Tildele en sikkerhedsrolle til en bruger](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user.md).

### <a name="to-disconnect-from-d365fin"></a>Sådan afbrydes forbindelsen fra [!INCLUDE[d365fin](includes/cds_long_md.md)]  
1. Vælg ikonet ![Elpære, der åbner ikonet til funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsæt CDS-forbindelse**, og vælg det relaterede link.
2. På siden **Opsæt CDS-forbindelse** skal du slå **Aktiveret** fra.  

## <a name="see-also"></a>Se også  
[Se status på en synkronisering](admin-how-to-view-synchronization-status.md)  
