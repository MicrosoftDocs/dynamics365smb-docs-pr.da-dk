---
title: Administration af OneDrive-integration med Business Central
description: Få mere at vide om, hvad du kan gøre for at administrere en integration mellem Business Central og OneDrive for Business.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, share, browser
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: c55abae59196d896b48a7b656e7fb7c4c7734fa8
ms.sourcegitcommit: 2396dd27e7886918d59c5e8e13b8f7a39a97075d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524489"
---
# <a name="managing-onedrive-integration-with-business-central"></a>Administration af OneDrive-integration med Business Central

Denne artikel giver en oversigt over, hvad en administrator kan gøre for at kontrollere OneDrive for Business-integration med [!INCLUDE[prod_short](includes/prod_short.md)]. [!INCLUDE[prod_short](includes/prod_short.md)]-onlinekunder drager fordel af automatisk integration, uden at der kræves ekstra opsætning for at bruge disse funktioner. 

## <a name="minimum-requirements"></a>Minimumkrav

* Hver bruger skal have en licens til [!INCLUDE[prod_short](includes/prod_short.md)] og OneDrive som en del af en Microsoft 365-plan.
* OneDrive skal konfigureres for hver bruger.

## <a name="governance"></a>Styreformer

SharePoint Administrationen giver omfattende kontrol over politikker, der styrer brugen af OneDrive i hele organisationen. Globale administratorer eller brugere, der har SharePoint-rollen Administrator, kan konfigurere politikker, der bestemmer, hvem der kan få adgang til OneDrive, hvor data er placeret, indholdslivscyklussen og meget mere. Følgende links indeholder oplysninger om ofte anvendte funktioner og indstillinger, der kan forbedre integrationen med [!INCLUDE[prod_short](includes/prod_short.md)]. 

* [Administrere delingsindstillinger](/sharepoint/turn-external-sharing-on-or-off)
* [Brug informationsbarrierer med SharePoint](/sharepoint/information-barriers)
* [Få mere at vide om forhindring af datatab](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Angive standardlagerplads for OneDrive-brugere](/onedrive/set-default-storage-space)
* [Tilføje og fjerne administratorer for en brugers OneDrive](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Deaktiver OneDrive-oprettelse for nogle brugere](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Multi-Geo-funktioner i OneDrive og SharePoint-online](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Nogle funktioner er muligvis kun tilgængelige for bestemte planer.

## <a name="managing-privacy"></a>Administration af beskyttelse af personlige oplysninger

Administratorer og slutbrugere styrer det indhold, der er gemt i OneDrive, og disse data ejes udelukkende af organisationen. Du kan finde flere oplysninger under [Sådan beskytter SharePoint og OneDrive dine data i skyen](/sharepoint/safeguarding-your-data). Du kan også besøge vores [Microsoft Erklæring om beskyttelse af personlige oplysninger fra](https://privacy.microsoft.com/en-us/privacystatement), som forklarer de data, som Microsoft behandler, hvordan Microsoft behandler dem, og til hvilke formål.

## <a name="restoring-onedrive-and-prod_short"></a>Gendannelse af OneDrive og [!INCLUDE[prod_short](includes/prod_short.md)]

Som en del af en øvelse i genoprettelse efter nedbrud skal administratorer muligvis gendanne et [!INCLUDE[prod_short](includes/prod_short.md)]-miljø til en sikkerhedskopi fra et tidspunkt tidligere og synkronisere OneDrive-lageret til det samme tidspunkt. OneDrive indeholder forskellige værktøjer til dette, f. eks. gendannelse af en brugers OneDrive til en tidligere tidsperiode, gendannelse af en tidligere version af en enkelt fil eller gendannelse af slettede filer. Du kan finde flere oplysninger i følgende artikler:

* For [!INCLUDE[prod_short](includes/prod_short.md)], se [Gendanne et miljø i Administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* For OneDrive, se [Gendanne din OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="configuring-business-central-on-premises"></a>Konfigurere Business Central lokalt

En administrator skal oprette forbindelsen mellem [!INCLUDE[prod_short](includes/prod_short.md)] lokalt og OneDrive. Til forskel fra [!INCLUDE[prod_short](includes/prod_short.md)]-online er forbindelsen ikke automatisk. Hvis forbindelsen ikke er konfigureret, kan brugere ikke bruge funktionerne til OneDrive.

[!INCLUDE[prod_short](includes/prod_short.md)] On-Premises kan kun være tilsluttet OneDrive, der er hostet af Microsoft i skyen. Tilslutning af [!INCLUDE[prod_short](includes/prod_short.md)] på stedet til lageret for mit websted for SharePoint-serveren understøttes ikke.

> [!IMPORTANT]
> Ved at konfigurere denne funktion kan du også aktivere ældre funktioner, som sender filer til OneDrive.  
>
>* Funktionen Åbn i Excel kopierer automatisk Excel-filen til OneDrive og åbner den i Excel online. 
>* Når du eksporterer en rapport til en fil, vil filen automatisk blive kopieret til OneDrive og derefter åbne den i Excel online, Word online eller OneDrive. 
>* Andre funktioner kan også blive åbnet automatisk i OneDrive.

### <a name="prepare-prod_short-on-premises-for-connecting-to-onedrive"></a>Forbered [!INCLUDE[prod_short](includes/prod_short.md)] lokalt til oprettelse af forbindelse til OneDrive

<!-- 
1. For the best experience Configure Azure Active Directory (AD) authentication.

   For more information, see [Authenticating Business Central Users with Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory)-->

Tilføj et registreret program til Business Central i din Azure AD-lejer med din Microsoft 365-plan. Ligesom andre Azure-tjenester, der fungerer sammen med Business Central, OneDrive, kræves en appregistrering i Azure Active Directory (Azure AD). Appregistreringen leverer godkendelses- og autorisationstjenester mellem Business Central og SharePoint, der anvendes af OneDrive.

Konfigurer det registrerede program med følgende uddelegerede tilladelser til SharePoint-API:

- AllSites.FullControl
- User.ReadWrite.All 

For Business central 2021 udgivelsesbølge 2 (version 19) skal du angive disse tilladelser i stedet for:

- AllSites.Write
- MyFiles.Write
- User.Read.All 

Du kan gøre dette i Azure-portalen. Sørg for at kopiere den applikation (klient-ID) og klienthemmelighed, der bruges af det registrerede program. Du skal bruge disse oplysninger i næste opgave.

Du kan finde flere oplysninger om kontoforudsætninger, registrering af et program og konfiguration af tilladelser i [Registrere et program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory)-hjælp til udviklere og it-fagfolk.

> [!TIP]
> Hvis du allerede har registreret et program som en del af integrationen med et andet Microsoft-produkt, f. eks. Power BI, kan du genbruge denne app-registrering. I så fald skal du blot angive SharePoint-tilladelserne.

### <a name="set-up-the-connection-in-prod_short-on-premises"></a>Konfigurer forbindelsen i [!INCLUDE[prod_short](includes/prod_short.md)] lokalt

<!--
> [!NOTE]
> This requires the following types of authentication credentials:
>
> * Windows
> * NavUserPassword
> * Azure Active Directory
-->
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikonet, skriv **Microsoft SharePoint-forbindelseskonfiguration**, og vælg derefter det relaterede link.
2. Indtast i feltet **Beskrivelse** en beskrivelse til forbindelsen, f.eks. **OneDrive**.
3. Skriv **Business Central** i feltet **Mappe**.
4. Angiv URL-adressen til OneDrive i feltet **Placering**.

    URL-adressen til a OneDrive er normalt i følgende format: `https://<tenant name>-my.sharepoint.com`. Du kan finde flere oplysninger i [OneDrive-URL-adresser for brugere i organisationen](/onedrive/list-onedrive-urls) i OneDrive-dokumentationen.
5. I feltet **Klient-id** skal du angive klient-id'et fra programregistreringen.
6. I feltet **Klienthemmelighed** skal du angive hemmeligheden fra programregistreringen. 
   <!-- 
   For information about how to find the URLs, see the following:
   * [How to find your SharePoint server URL]
   * [How to find your OneDrive URL]-->

> [!IMPORTANT]
> Siden SharePoint Connection setup bruges til at konfigurere flere ældre funktioner. I sektionen **Generelt** konfigureres forbindelsen til OneDrive, og afsnittet **Delte dokumenter** omdirigerer filerne til SharePoint i stedet for. Funktionen ældre SharePoint er forældet i den nærmeste fremtid. Det anbefales, at du ikke konfigurerer afsnittet **Delte dokumenter**.

## <a name="see-also"></a>Se også

[Business Central og OneDrive for Business Integration](across-onedrive-overview.md)  
[Åbner Business Central-filer i OneDrive](across-share-onedrive.md)  
[OneDrive Ofte stillede spørgsmål](admin-onedrive-faq.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
