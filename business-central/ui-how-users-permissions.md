---
title: Tildele eller redigere brugertilladelser | Microsoft Docs
description: Beskriver, hvordan du kan føje Office 365-brugere til Business Central og derefter tildele tilladelser, adgangsrettigheder og sikkerhedsindstillinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 12/03/2019
ms.author: sgroespe
ms.openlocfilehash: 1d0b7b7363df88e52631b4ba6e2f495be13f7397
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896153"
---
# <a name="create-users-according-to-licenses"></a>Oprette brugere i henhold til licenser
I det følgende beskrives, hvordan du som administrator opretter brugere og definerer, hvem der kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)], og hvilke grundlæggende rettigheder forskellige brugertyper har i henhold til licenserne.

Når der oprettes brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du fortsætte med at tildele specifikke rettigheder til brugere via rettighedssæt og organisere brugere i brugergrupper, så rettighederne er nemme at administrere. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).  

> [!NOTE]
> Processen med at administrere brugere og licenser afhænger af, om din løsning er installeret online eller i det lokale miljø. I onlineinstallationer kan du f.eks. kun deaktivere og aktivere en bruger, der er føjet til [!INCLUDE[d365fin](includes/d365fin_md.md)]. I lokale installationer kan du oprette, redigere og slette brugere.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Administrere brugere og licenser i onlineinstallationer
I [!INCLUDE[d365fin](includes/d365fin_md.md)] online er antallet af brugere defineret af abonnementet og føjet til din lejer i Microsoft Partnercenter , som regel af din Microsoft-partner. Du kan finde flere oplysninger i [Tilføje en ny kunde](https://docs.microsoft.com/partner-center/add-a-new-customer) og [Oprette, afbryde eller annullere kundeabonnementer](https://docs.microsoft.com/partner-center/create-a-new-subscription) i Hjælp til Microsoft Partnercenter.

Hvis du vil definere, hvem der kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)], skal produktlicenserne tildeles til brugere ifølge de roller, som de skal udføre i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette kan gøres på følgende måder:
- Virksomhedens Office 365-administrator kan gøre det i [Microsoft 365 Administration](https://admin.microsoft.com). Du kan finde flere oplysninger i [Tilføje brugere enkeltvis eller samlet i Office 365](https://aka.ms/CreateOffice365Users).  
- En Microsoft-partner kan tildele licenser i Microsoft 365 Administration eller i Microsoft Partnercenter. Du kan finde flere oplysninger i [Brugeradministrationsopgaver for debitorkonti](https://docs.microsoft.com/partner-center/assign-licenses-to-users) i Hjælp til Microsoft Partnercenter.

Du kan finde flere oplysninger under [Administration af Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i hjælpen til udviklere og it-eksperter.

Når brugere med en [!INCLUDE[d365fin](includes/d365fin_md.md)]-licens er oprettet i Office 365, kan de importeres på siden **Brugere** i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af handlingen **Hent nye brugere fra Office 365**.

### <a name="to-add-a-user-in-business-central"></a>Sådan tilføjes en bruger i Business Central
Hvis du vil føje brugere fra Microsoft 365 Administration til [!INCLUDE[d365fin](includes/d365fin_md.md)] online, skal du bruge en dedikeret importfunktion.  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Vælg handlingen **Hent nye brugere fra Office 365**.

Nye brugere, der er oprettet for dit Office 365-abonnement, tilføjes på siden **Brugere**. Brugere tildeles rettighedssæt i henhold til den licens der er tildelt til brugeren i Office 365. Du kan derefter fortsætte med at give mere detaljerede rettigheder til brugere og organisere dem i brugergrupper, så rettighederne er nemme at administrere. Du kan finde flere oplysninger i [Tildele rettighedssæt til brugere](ui-define-granular-permissions.md#to-assign-permission-sets-to-users).

> [!NOTE]
> Hvis du bruger en ekstern revisor til at administrere dine regnskaber og regnskabsaflæggelse, kan du invitere vedkommende indenfor i din Business Central, så de kan samarbejde med dig om dine regnskabsdata. Du kan finde flere oplysninger i [Inviter din eksterne revisor til at deltage i din Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-remove-a-users-access-to-the-system"></a>Sådan fjernes en brugers adgang til systemet
I onlineinstallationer kan du fjerne en brugers adgang til systemet ved at indstille feltet **Status** til **Deaktiveret**. Alle referencer til brugeren bevares, men brugeren kan ikke længere logge på systemet, og aktive sessioner for brugeren afsluttes.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Åbn siden **Brugerkort** for den relevante bruger, og vælg derefter **Deaktiveret** i feltet **Tilstand**.
3. Hvis du vil give brugeren adgang igen, skal du indstille feltet **Tilstand** til **Aktiveret**.

Ud over at deaktivere en bruger kan du fjerne tildelingen af licensen fra en bruger i Microsoft 365 Administration. Brugeren kan derefter ikke logge på. Du kan finde flere oplysninger i [Fjerne tildeling af licenser fra brugere](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Sådan ændres den tildelte licens for en bruger
Nogle gange kan det være nødvendigt at ændre den licens, som en bruger har fået tildelt. Du beslutter f.eks. at bruge modulet Servicestyring og har derfor brug for at opgradere alle Essential-licenser til Premium. Eller hvis en brugers ansvarsområde er ændret, og du har brug for at erstatte en Teammedlem-licens med Essential.

1. Skift licensen i Microsoft 365 Administration. Du kan finde flere oplysninger i [Tilføje brugere enkeltvis eller samlet i Office 365](https://aka.ms/CreateOffice365Users).
2. Log på [!INCLUDE[d365fin](includes/d365fin_md.md)] som administrator.
3. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
4. Du kan vælge handlingen **Brugergrupper** på siden **Opdater alle brugergrupper**.

Brugerne flyttes til en korrekt brugergruppe, og rettighedssættene opdateres. Du kan finde flere oplysninger i [Administrere rettigheder gennem brugergrupper](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Alle almindelige brugere i en løsning skal tildeles samme licens, Essential eller Premium.
> Du kan finde oplysninger om licenser i [Licensvejledning til Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

### <a name="synchronization-with-office-365"></a>Synkronisering med Office 365
Når en licens er tildelt til en bruger i Office 365, kan du oprette brugeren i [!INCLUDE[d365fin](includes/d365fin_md.md)] på to måder. Systemet vil gøre det automatisk, når brugeren logger på første gang, eller administratoren kan tilføje brugeren ved at vælge handlingen **Hent brugere fra Office 365** på siden **Brugere**.

I begge tilfælde oprettes der automatisk en række ekstra indstillinger. Disse er angivet i den anden og tredje kolonne i nedenstående tabel.

Hvis du ændrer brugeren efterfølgende i Office 365, og du har brug for at synkronisere ændringerne med [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du bruge forskellige handlinger på siden **Brugere**, afhængigt af hvad du vil synkronisere. Disse er angivet i de sidste tre kolonner i nedenstående tabel.

|Hvad sker der, når:|Der logges på første gang|Brugere hentes fra Office 365|Brugere opdateres fra Office 365|Brugerens standardbrugergrupper gendannes|Brugergrupper opdateres|
|-|-|-|-|-|-|
|Omfang:|Aktuelle bruger|Nye brugere i Office 365|Flere markerede brugere|Enkelt valgte bruger (undtagen aktuel)|Flere markerede brugere|
|Opret den nye bruger, og tildel rettighedssættet SUPER.<br /><br />Platform|**X**|**X**| | | |
|Opdater brugerposten baseret på faktiske oplysninger i Office 365: stat, fuldt navn, e-mail-adresse for kontaktperson, godkendelsesmail.<br /><br />Codeunit "Azure AD Graf bruger".UpdateUserFromAzureGraph|**X**|**X**|**X**|**X**| |
|Synkroniser brugerplaner (licenser) med licenser og roller tildelt i Office 365.<br /><br />Codeunit "Azure AD Graf bruger".UpdateUserPlans|**X**|**X**| |**X**|**X**|
|Føj brugeren til brugergruppen i henhold til de aktuelle brugerplaner. Tilbagekald rettighedssættet SUPER. (Der kræves mindst én SUPER. Undlad at tilbagekalde [administratorer](/dynamics365/business-central/dev-itpro/administration/tenant-administration).)<br /><br />Codeunit "Rettighedsadministrator". AddUserToDefaultUserGroups|**X**|**X**| |**X**<br /><br />Overskriv: Fjern brugeren fra andre grupper. Fjern manuelt tildelte rettighedssæt.|**X**<br /><br />Yderligere: Bevar det aktuelle medlemskab i brugergruppen og tildelte rettighedssæt. Føj kun bruger til grupper, hvis det er nødvendigt.|

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Administrer brugere og licenser i Installationer på stedet
I installationer i det lokale miljø er der angivet et antal licenserede brugere i licensfilen (. flf). Når administratoren eller Microsoft-partneren overfører licensfilen, kan administratoren angive, hvilke brugere der kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)].

I forbindelse med installationer i det lokale miljø opretter redigerer og sletter administratoren brugere direkte fra siden **Brugere.**

### <a name="to-edit-or-delete-a-user-on-premises"></a>Sådan redigeres eller slettes en bruger i det lokale miljø
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Vælg den bruger, som du vil redigere, og vælg derefter handlingen **Rediger**.
3. På siden **Brugerkort** kan du ændre oplysningerne efter behov.    
4. Hvis du vil slette en bruger, skal du markere den pågældende bruger og derefter vælge handlingen **Slet**.

> [!NOTE]
> Ved lokale installationer af [!INCLUDE[d365fin](includes/d365fin_md.md)] kan administratoren vælge mellem forskellige godkendelse af legitimationsoplysninger for brugere. Når du derefter opretter en bruger, angiver du forskellige oplysninger, afhængigt af den type legitimationsoplysninger, du bruger i den specifikke [!INCLUDE[server](includes/server.md)]-forekomst.<br /><br />
> Du kan finde flere oplysninger i [Godkendelse og typer af legitimationsoplysninger](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i sektionen Administration af udvikler- og ITPro-indholdet til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se også
[Tildele rettigheder til brugere og grupper](ui-define-granular-permissions.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Tilpasning [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Blive klar til at handle](ui-get-ready-business.md)  
[Opsætning](admin-setup-and-administration.md)  
[Føje brugere til Office 365 til virksomheder](https://aka.ms/CreateOffice365Users)  
[Licensvejledning til Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing)  
[Sikkerhed og beskyttelse i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) i hjælp til udviklere og it-eksperter
