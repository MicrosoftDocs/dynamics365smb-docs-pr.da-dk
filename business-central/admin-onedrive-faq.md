---
title: OneDrive for Business, ofte stillede spørgsmål
description: Få svar på nogle typiske spørgsmål om arbejde med OneDrive for Business og Business Central.
author: bholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, integration, share, browser
ms.date: 05/19/2021
ms.author: bholtorf
ms.openlocfilehash: f54e8b6290e9dd653180b3ea05246255b84dc2ae
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144046"
---
# <a name="onedrive-for-business-faq"></a>OneDrive for Business, ofte stillede spørgsmål

[!INCLUDE [online_only](includes/online_only.md)]

I denne artikel besvares nogle af de spørgsmål, du kan have om at arbejde med OneDrive og [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="does-this-work-with-all-prod_short-clients"></a>Fungerer dette sammen med alle [!INCLUDE[prod_short](includes/prod_short.md)]-klienter?

Ja. Du kan åbne filer i OneDrive fra [!INCLUDE[prod_short](includes/prod_short.md)]-mobil-apps, når du får vist kortdetaljer i Microsoft Teams eller endda fra Outlook-tilføjelsesprogrammet.  

## <a name="is-onedrive-the-same-as-sharepoint-for-storing-files"></a>Svarer OneDrive til SharePoint i forbindelse med at gemme filer?

Som en del af dit Microsoft 365-abonnement giver din virksomhed dig OneDrive, dit fillager i skyen. OneDrive er som standard privat, hvor du organiserer indholdet og vælger, hvilke filer eller mapper du vil dele med. SharePoint indeholder derimod et arkivlager med den sky, som deles med andre i din organisation.  

## <a name="does-prod_short-support-consumer-onedrive"></a>Understøtter [!INCLUDE[prod_short](includes/prod_short.md)] forbruger OneDrive?

Nummer Denne integration er udelukkende beregnet til OneDrive for Business og understøtter kun din arbejdskonto. 

## <a name="are-all-onedrive-for-business-plans-supported"></a>Understøttes OneDrive for Business alle forretningsplaner?

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter ikke enkeltstående planer for OneDrive for Business. OneDrive skal købes som en del af Microsoft 365 Business- eller Enterprise-plan. Du kan finde flere oplysninger i [sammenligne OneDrive-skyens lagerpriser og planer](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## <a name="where-can-i-see-onedrive-service-health"></a>Hvor kan jeg se OneDrive-servicetilstand?

Administratorer kan få adgang til dette Dashboard servicetilstand som en del af Microsoft 365 Administration. Dashboardet omfatter OneDrive-service tilgængelighed. 
 
## <a name="is-onedrive-integration-available-to-prod_short-on-premises"></a>Er OneDrive-integration tilgængelig for [!INCLUDE[prod_short](includes/prod_short.md)] lokalt?

Ja, men i modsætning til [!INCLUDE[prod_short](includes/prod_short.md)]-online betyder det, at der kræves yderligere opsætning. Du kan finde flere oplysninger i [Tilpasning af Business Central i det lokale miljø](admin-onedrive-integration.md#configuring-business-central-on-premises).  

## <a name="does-prod_short-on-premises-connect-with-sharepoint-server"></a>Opretter [!INCLUDE[prod_short](includes/prod_short.md)] lokal forbindelse til SharePoint-serveren?

Nummer Denne installationskombination understøttes ikke, selvom SharePoint-serveren har aktiveret mit websted.  

## <a name="does-prod_short-online-connect-with-sharepoint-server"></a>Opretter [!INCLUDE[prod_short](includes/prod_short.md)] online forbindelse til SharePoint-serveren?

Nummer Denne installationskombination understøttes ikke, selvom SharePoint-serveren har aktiveret mit websted.  

## <a name="how-does-this-work-in-an-organization-with-multiple-environments"></a>Hvordan fungerer dette i en organisation med flere miljøer?

Integrationen forudsætter, at firmanavne er entydige på tværs af [!INCLUDE[prod_short](includes/prod_short.md)]-miljøer. Hvis virksomhedens navne er entydige på tværs af organisationen, vil åbning af en fil i OneDrive kopiere filen til en mappe, der kaldes efter det aktuelle regnskab. Hvis firmanavne ikke er entydige på tværs af miljøer, kan filer fra identiske virksomhedsnavne placeres i samme mappe.  

## <a name="weve-changed-company-name-what-happens-to-my-previous-files"></a>Vi har ændret virksomhedsnavnet. Hvad sker der med mine tidligere filer?

[!INCLUDE[prod_short](includes/prod_short.md)] overflytter ikke automatisk filer, du tidligere har åbnet i OneDrive, til den nye mappe. Når du har omdøbt virksomheden, vil funktionen Åbn i OneDrive-handling kopiere filer til en mappe, der har det nye firmanavn.   

## <a name="when-attaching-files-to-prod_short-how-do-i-pick-a-file-from-onedrive"></a>Ved tilknytning af filer til [!INCLUDE[prod_short](includes/prod_short.md)], hvordan tilknytter jeg filer fra OneDrive? 
[!INCLUDE[prod_short](includes/prod_short.md)] angiver ikke en skyfilvælger. Du skal hente filen fra OneDrive til din enhed og derefter overføre den til [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="i-want-to-open-files-in-sharepoint-instead-how-do-i-do-this"></a>Jeg vil åbne filer i SharePoint i stedet. Hvordan gør jeg det?

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder ikke funktioner, der kan bruges til at kopiere filer til SharePoint og åbne dem fra et SharePoint-bibliotek. Kontakt din Microsoft-partner for at få et overblik over dine muligheder, eller Søg efter apps på AppSource.  

## <a name="how-do-i-turn-off-integration-to-onedrive"></a>Hvordan slår jeg integration til OneDrive?

[!INCLUDE[prod_short](includes/prod_short.md)] Online giver ikke mulighed for at aktivere eller deaktivere integration OneDrive.  

## <a name="should-i-use-the-sharepoint-connection-setup-page-to-connect-to-sharepoint"></a>Skal jeg bruge SharePoint-siden Forbindelsesopsætning til at oprette forbindelse til SharePoint?

Dette er en ældre funktion, hvor alle [!INCLUDE[prod_short](includes/prod_short.md)]-filer fra alle brugere sendes til en enkelt SharePoint-mappe. Det anbefales, at du ikke konfigurerer oversigtspanelet delte dokumenter på SharePoint-siden til opsætning af forbindelse, da vi arbejder på at anbefale denne funktion.  

## <a name="which-version-of-prod_short-supports-onedrive"></a>Hvilken version af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter OneDrive?

Integration med OneDrive blev tilgængelig i 2021 Release Wave 2.  

## <a name="will-microsoft-continue-to-improve-the-integration-to-onedrive"></a>Fortsætter Microsoft med at forbedre integration til OneDrive?

Hos Microsoft lytter vi hele tiden til feedback fra vores forskellige grupper af brugere og handler på de mest interessante forslag. Du kan finde flere oplysninger om, hvad der er det næste for integrationer med Microsoft 365-apps, i [frigivelsesplanen for Dynamics 365](/dynamics365-release-plan/2021wave1).  

Hvis du vil deltage i forbedring af OneDrive-integrationen eller have en idé, der kan forbedre fildeling og samarbejde i [!INCLUDE[prod_short](includes/prod_short.md)], kan du tilføje en idé eller stemme for eksisterende ideer på [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="troubleshooting"></a>Fejlfinding

Dette afsnit indeholder oplysninger om, hvordan du identificerer og løser problemer, der kan opstå, når du bruger OneDrive sammen med [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="i-have-to-sign-in-each-time-i-open-a-file"></a>Jeg skal logge på, hver gang jeg åbner en fil

Vi beklager, men det er et kendt problem, og vi arbejder på det. Vi forventer at give en mere problemfri oplevelse med en kommende opdatering.  

### <a name="business-central-cant-find-my-onedrive"></a>Business central kan ikke finde OneDrive

Når denne meddelelse vises, kan du ikke fastslå placeringen af din OneDrive for Business, skal du kontakte din partner for at konfigurere det. ", kontroller, om brugeren har haft adgang til OneDrive mindst én gang. Hvis de ikke har det, skal du bede personen om at gå til portal.office.com/onedrive for at konfigurere den. Det kan tage lidt tid. Hvis meddelelsen stadig vises efter 24 timer, skal du kontakte support.  
 

## <a name="see-also"></a>Se også
[Business Central og OneDrive-integration](across-onedrive-overview.md)  
[Administration af OneDrive-integration med Business Central](admin-onedrive-integration.md)  
[Åbner Business Central-filer i OneDrive](across-share-onedrive.md)  
