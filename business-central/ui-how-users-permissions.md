---
title: Oprette brugere ifølge licenser | Microsoft Docs
description: Beskriver, hvordan brugere føjes til Business Central online eller on-premises baseret på licenser.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: df34469bc28b081800ddf583e7aa9cf08a15dc27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925643"
---
# <a name="create-users-according-to-licenses"></a>Oprette brugere i henhold til licenser

Denne artikel handler om, hvordan administratorer opretter brugere og definerer, hvem der kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)], og hvilke tilladelser der gives til forskellige brugertyper har ifølge licenserne.

Når du opretter brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du give dem bestemte tilladelser via tilladelsessæt og organisere brugere i brugergrupper. Brugergrupper gør det nemmere at administrere tilladelser for flere brugere på én gang. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).  

> [!NOTE]
> Processen med at administrere brugere og licenser afhænger af, om [!INCLUDE[d365fin](includes/d365fin_md.md)] er installeret online eller i det lokale miljø. For [!INCLUDE [prodshort](includes/prodshort.md)] online skal du tilføje brugere fra Microsoft 365. I lokale installationer kan du oprette, redigere og slette brugere direkte.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Administrere brugere og licenser i onlineinstallationer

I onlineversionen af [!INCLUDE[d365fin](includes/d365fin_md.md)] er antallet af brugere defineret af abonnementet og føjet til din lejer i Microsoft Partnercenter , som regel af din Microsoft-partner. Du kan finde flere oplysninger i [Tilføje en ny kunde](/partner-center/add-a-new-customer) og [Oprette, afbryde eller annullere kundeabonnementer](/partner-center/create-a-new-subscription) i Hjælp til Microsoft Partnercenter.

Hvis du vil definere, hvem der kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du tildele produktlicenserne til brugere i henhold til de roller, som de skal udføre i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette kan gøres på følgende måder:

- Virksomhedens Microsoft 365-administrator kan gøre det i [Microsoft 365 Admin Center](https://admin.microsoft.com). Du kan finde flere oplysninger i [Tilføje brugere enkeltvis eller samlet i Microsoft 365](https://aka.ms/CreateOffice365Users).  
- En Microsoft-partner kan tildele licenser i Microsoft 365 Administration eller i Microsoft Partnercenter. Du kan finde flere oplysninger i [Brugeradministrationsopgaver for debitorkonti](/partner-center/assign-licenses-to-users) i Hjælp til Microsoft Partnercenter.

Du kan finde flere oplysninger under [Administration af Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i administrationens Hjælp.

Når brugere tildeles en [!INCLUDE[d365fin](includes/d365fin_md.md)]-licens i Microsoft 365, kan du importere dem til siden **Brugere** i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af handlingen **Hent nye brugere fra Office 365**.

### <a name="to-add-a-user-or-update-user-information-in-business-central"></a><a name="adduser"></a>Sådan tilføjer du en bruger eller opdaterer brugeroplysninger i Business Central

Du kan bruge dedikerede importfunktioner til at tilføje nye brugere eller opdatere brugeroplysninger i [!INCLUDE[d365fin](includes/d365fin_md.md)] fra Microsoft 365 Administration.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Opdater brugere fra Office 365**.

    Hvis det er første gang, du tilføjer brugere fra Microsoft 365, skal du vælge handlingen **Hent nye brugere fra Office 365**.  
3. Følg trinnene i den viste vejledning.

De nye brugere og brugeroplysninger i dit Microsoft 365-abonnement tilføjes på siden **Brugere** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan nu tildele brugergrupper og tilladelser. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).  

Du kan få flere oplysninger om synkronisering af brugeroplysninger med Microsoft 365 i afsnittet [Synkronisering med Microsoft 365](#m365).

> [!NOTE]
> Hvis du bruger en ekstern revisor til at administrere dine regnskaber og regnskabsaflæggelse, kan du invitere vedkommende indenfor i din Business Central, så de kan samarbejde med dig om dine regnskabsdata. Du kan finde flere oplysninger i [Inviter din eksterne revisor til at deltage i din Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-change-the-assigned-license-for-a-user"></a>Sådan ændres den tildelte licens for en bruger

Nogle gange kan det være nødvendigt at ændre den licens, som en bruger har fået tildelt. Du beslutter f.eks. at bruge modulet Servicestyring og har derfor brug for at opgradere alle Essential-licenser til Premium. Eller hvis en brugers ansvarsområde er ændret, og du har brug for at erstatte en Teammedlem-licens med Essential.

1. Skift licensen i Microsoft 365 Administration. Du kan finde flere oplysninger i [Tilføje brugere enkeltvis eller samlet i Microsoft 365](https://aka.ms/CreateOffice365Users).
2. Log på [!INCLUDE[d365fin](includes/d365fin_md.md)] som administrator.
3. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
4. Vælg handlingen **Brugerens standardbrugergrupper gendannes** på siden **Brugere**.

Brugerne flyttes til en korrekt brugergruppe, og rettighedssættene opdateres. Du kan finde flere oplysninger i [Administrere rettigheder gennem brugergrupper](ui-define-granular-permissions.md).

> [!NOTE]
> Alle brugere skal tildeles den samme licens, enten Essential eller Premium. Du kan få flere oplysninger i Licensvejledning til Microsoft Dynamics 365 Business Central. Denne vejledning kan hentes på webstedet for [Business Central](https://dynamics.microsoft.com/business-central/overview/).

### <a name="to-remove-a-users-access-to-the-system"></a>Sådan fjernes en brugers adgang til systemet

I onlineinstallationer kan du fjerne en brugers adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Alle referencer til brugeren bevares, men brugeren kan ikke logge ind, og aktive sessioner for brugeren stoppes.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Åbn siden **Brugerkort** for den relevante bruger, og vælg derefter **Deaktiveret** i feltet **Tilstand**.
3. Hvis du vil give brugeren adgang igen, skal du indstille feltet **Tilstand** til **Aktiveret**.

Du kan også fjerne licensen fra en bruger i Microsoft 365 Administration. Brugeren kan derefter ikke logge på. Du kan få flere oplysninger i [Fjerne licenser fra brugere](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Synkronisering med Microsoft 365

Når du fjerner tildelingen af en licens til [!INCLUDE[d365fin](includes/d365fin_md.md)] for en bruger i Microsoft 365, kan du oprette brugeren i [!INCLUDE[d365fin](includes/d365fin_md.md)] på to måder.  

- Administratoren kan tilføje brugeren ved at vælge handlingen **Opdater brugere fra Office 365** på siden **Brugere** som beskrevet i afsnittet [Sådan tilføjer du en bruger eller opdaterer brugeroplysninger i Business Central](#adduser).
- Licensoplysningerne opdateres automatisk, når brugeren logger på for første gang.

I begge tilfælde oprettes der automatisk en række indstillinger. Disse er angivet i den anden og tredje kolonne i nedenstående tabel.

Hvis du ændrer brugeroplysningerne i Microsoft 365, kan du opdatere [!INCLUDE[d365fin](includes/d365fin_md.md)], så de afspejler ændringen. Afhængigt af hvad du vil opdatere, skal du bruge en af handlingerne på siden **Brugere**. Handlingerne er beskrevet i de sidste tre kolonner i nedenstående tabel.

|Hvad sker der, når:|Første bruger, første login|Hent brugere fra Microsoft 365|Opdatere brugere fra Microsoft 365|Brugerens standardbrugergrupper gendannes|Brugergrupper opdateres|
|-|-|-|-|-|-|
|Omfang:|Aktuelle bruger|Nye brugere i Microsoft 365|Flere markerede brugere|Enkelt valgte bruger (undtagen aktuel)|Flere markerede brugere|
|Opret den nye bruger, og tildel rettighedssættet SUPER.<br /><br /><!--Platform-->|**X**|| | | |
|Opdater brugerposten baseret på faktiske oplysninger i Microsoft 365: stat, fuldt navn, e-mail-adresse for kontaktperson, godkendelsesmail.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**| |
|Synkroniser brugerplaner (licenser) med licenser og roller tildelt i Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**| |**X**|**X**|
|Føj brugeren til brugergruppen i henhold til de aktuelle brugerplaner. Fjern SUPER-tilladelsessættet for alle andre brugere end den første bruger, der skal logge på, og [administratorer](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Der kræves mindst én SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**| |**X**<br /><br />Fjerner manuelt tildelte brugergrupper og tilladelser.|**X**<br /><br />Opdater brugergruppetildelinger.|

## <a name="the-device-license"></a>Enhedslicensen

Dynamics 365 Business Central-enhedslicensen giver flere brugere mulighed for at benytte en enhed, der er dækket af licensen, på samme tid. Dette kan f. eks. være en salgssteds-, produktionsområde- eller lagerenhed. Når du har købt et antal enhedslicenser, kan op til det pågældende antal brugere, som er knyttet til Dynamics 365 Business Central-gruppen af enhedsbrugere, logge ind på samme tid. Du kan få flere oplysninger i Licensvejledning til Microsoft Dynamics 365 Business Central. Denne vejledning kan hentes på webstedet for [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Din virksomheds Microsoft 365-administrator eller Microsoft-partner kan oprette Dynamics 365 Business Central-gruppen af enhedsbrugere og tilføje enhedsbrugere som medlemmer i [Microsoft 365 Admin Center](https://admin.microsoft.com/) eller på [Azure-portalen](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Begrænsninger på enhedsbrugere

Brugere med enhedslicensen kan ikke udføre følgende opgaver i [!INCLUDE[d365fin](includes/d365fin_md.md)]:

- Konfigurere job, der skal køres som planlagte opgaver i opgavekøen. Enhedsbrugere er samtidige brugere, og vi kan derfor ikke sikre, at den involverede bruger findes i systemet, når en opgave udføres, hvilket er påkrævet.

- En enhedsbruger må ikke være den første bruger, der logger på. En bruger af typen administrator, fuld bruger eller ekstern revisor skal være den første, der logger på, så vedkommende kan konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger under [Administration af Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i administrationens Hjælp.

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Sådan oprettes en gruppe af Dynamics 365 Business Central-enhedsbrugere

1. Gå til siden **Grupper** i Microsoft 365 Administration.
2. Vælg handlingen **Tilføj en gruppe**.
3. Gå til siden **Vælg en gruppetype**, vælg handlingen **Sikkerhed**, og vælg derefter handlingen **Tilføj**.
4. På siden **Grundlæggende** skal du angive **Dynamics 365 Business Central-enhedsbrugere** som navnet på gruppen.
  
   >[!NOTE]
   >Navnet på gruppen skal staves på engelsk, nøjagtigt som det vises i trin 4, også selvom du bruger et andet sprog.
5. Vælg knappen **Luk**.

> [!NOTE]
> Du kan også oprette en gruppe af typen Microsoft 365. Du finder flere oplysninger i [Sammenlign grupper](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Sådan føjes medlemmer til gruppen

1. Gå til Microsoft 365 Administration, og opdater siden **Grupper**, så din nye gruppe vises.
2. Vælg gruppen **Dynamics 365 Business Central-enhedsbrugere**, og vælg derefter handlingen **Vis alle og administrer medlemmer**.
3. Vælg handlingen **Tilføj medlemmer**.
4. Vælg de brugere, som du vil tilføje, og vælg derefter knappen **Gem**.
5. Vælg knappen **Luk** tre gange.

Du kan føje så mange brugere til gruppen Dynamics 365 Business Central-enhedsbrugere, som du har brug for. Men antallet af enheder, som brugerne kan logge på samtidig, er defineret af antallet af købte enhedslicenser.

> [!NOTE]
> Du behøver ikke tildele en [!INCLUDE[d365fin](includes/d365fin_md.md)]-licens til brugere, der er medlemmer af gruppen Dynamics 365 Business Central-enhedsbrugere.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Administrer brugere og licenser i Installationer på stedet

I installationer i det lokale miljø er der angivet et antal brugerlicenser i licensfilen (. flf). Når en administrator eller Microsoft-partneren overfører licensfilen, kan administratoren angive, hvilke brugere der kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)].

I forbindelse med installationer i det lokale miljø opretter redigerer og sletter administratoren brugere direkte fra siden **Brugere.**

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Sådan redigeres eller slettes en bruger i en lokal installation

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Vælg den bruger, som du vil redigere, og vælg derefter handlingen **Rediger**.
3. På siden **Brugerkort** kan du ændre oplysningerne efter behov.  
4. Hvis du vil slette en bruger, skal du markere den pågældende bruger og derefter vælge handlingen **Slet**.

> [!NOTE]
> I lokale installationer skal en administrator angive, hvordan en brugers legitimationsoplysninger skal godkendes i forekomsten af [!INCLUDE[server](includes/server.md)] . Når du opretter en bruger, skal du angive den type legitimationsoplysninger, som du bruger.
>
> Du kan finde flere oplysninger i [Godkendelse og typer af legitimationsoplysninger](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i administrationens Hjælp til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se også

[Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Tilpasning [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Blive klar til at handle](ui-get-ready-business.md)  
[Opsætning](admin-setup-and-administration.md)  
[Føje brugere til Microsoft 365 for Business](https://aka.ms/CreateOffice365Users)  
[Sikkerhed og beskyttelse i Business Central (administration)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
