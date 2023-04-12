---
title: Oprette brugere i henhold til licenser
description: 'Beskriver, hvordan brugere føjes til Business Central online eller on-premises baseret på licenser.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173'
ms.date: 03/24/2023
ms.author: jswymer
ms.reviewer: jswymer
---
# Oprette brugere i henhold til licenser

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Denne artikel beskriver, hvordan administratorer opretter brugere og definerer, hvem der kan logge på [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan også se, hvordan du kan tildele tilladelser til forskellige brugere i henhold til produktlicenserne.

Når du opretter brugere i [!INCLUDE[prod_short](includes/prod_short.md)], giver du tilladelse til dem via tilladelsessæt. Du kan også organisere brugere i brugergrupper. Brugergrupper gør det nemmere at administrere tilladelser og andre indstillinger for flere brugere på én gang. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).  

Du kan finde flere oplysninger om de forskellige typer licenser, og hvordan licenser fungerer i [!INCLUDE[prod_short](includes/prod_short.md)] ved at hente [Licensvejledning til Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Processen med at administrere brugere og licenser afhænger af, om [!INCLUDE[prod_short](includes/prod_short.md)] er installeret online eller i det lokale miljø. For [!INCLUDE [prod_short](includes/prod_short.md)] online skal du tilføje brugere fra Microsoft 365. I lokale installationer kan du oprette, redigere og slette brugere direkte.  

## Administrere brugere og licenser i onlinelejere

Brugerkonti i [!INCLUDE[prod_short](includes/prod_short.md)] skal oprettes først i Microsoft 365 Administration. Disse brugerkonti er ikke udelukkende til Business Central. Hvis du abonnerer på andre planer, kan de bruges til at logge på andre programmer, f.eks. Power BI. Du kan finde oplysninger om oprettelse af brugere i Microsoft 365 Administration ved at gå til [Tilføj brugere i Microsoft Administration](/microsoft-365/admin/add-users/add-users).

I onlineversionen af [!INCLUDE[prod_short](includes/prod_short.md)] definerer dit abonnement antallet af tilladte [!INCLUDE[prod_short](includes/prod_short.md)]-brugerlicenser, du har tilladelse til. Der føjes brugere til din lejer i Microsoft Partner Center, som regel af din Microsoft-partner. Du kan finde flere oplysninger i [Administration af Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Du tildeler licenser til brugere i henhold til den arbejdsgang, hver bruger vil bruge i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan tildele licenser på flere måder:

- Virksomhedens Microsoft 365-administrator kan gøre det i [Microsoft 365 Administration](https://admin.microsoft.com).. Du kan finde flere oplysninger i [Tilføje brugere enkeltvis eller samlet i Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- En Microsoft-partner kan tildele licenser i Microsoft 365 Administration eller i Microsoft Partnercenter. Du kan finde flere oplysninger i [Brugeradministrationsopgaver for debitorkonti](/partner-center/assign-licenses-to-users) i Hjælp til Microsoft Partnercenter.

Du kan finde flere oplysninger i [Administration af Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i administrationens Hjælp.

Når brugerkonti er oprettet i Microsoft 365 Administration er der to måder at importere dem til Business Central på:

- En brugerkonto indlæses automatisk, når brugeren logger på [!INCLUDE [prod_short](includes/prod_short.md)] første gang.

- Administratoren kan importere brugere ved at vælge handlingen  **Opdater brugere fra Microsoft 365**  på siden **Brugere* .

Begge metoder har deres egne fordele, og du kan bruge dem samtidig. Hver fremgangsmåde tillader administratorer proaktivt at konfigurere [!INCLUDE [prod_short](includes/prod_short.md)] til at tildele starttilladelser, brugergrupper og brugerprofiler. Ved at bruge funktionen **Opdater brugere fra Microsoft 365** får administratorer mere kontrol til at justere tilladelser, brugergrupper og profiler. Det er en ideel fremgangsmåde, når du konfigurerer [!INCLUDE [prod_short](includes/prod_short.md)] første gang, før en bruger logger på, eller når du tilføjer en ny gruppe brugere.

> [!NOTE]
> Når du har tilføjet brugere i Microsoft 365 Administration, anbefaler vi, at du opdaterer bruger oplysningerne i [!INCLUDE[prod_short](includes/prod_short.md)] så tidligt som muligt. Det er nemt at holde brugeroplysninger opdateret, og det er med til at sikre, at brugerne altid kan logge på. Du kan finde flere oplysninger i [Sådan tilføjer du en bruger eller opdaterer brugeroplysninger og licenstildelinger i Business Central](#adduser).<br>
>
> Opdatering af brugeroplysninger er særligt vigtige, hvis du har tilpasset tilladelsessæt til licensen. Hvis en ny bruger prøver at logge på [!INCLUDE[prod_short](includes/prod_short.md)], før du har tilføjet dem, kan de muligvis ikke. Du kan finde flere oplysninger i [konfigurere tilladelser på baggrund af licenser](#licensespermissions).
>
> Brugere, som oplever dette problem, er dog ikke blevet blokeret. Du kan enten bruge handlingen **Gå tilbage til hjemmesiden** eller logge på igen for at løse problemet.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Du kan finde flere oplysninger i [Delegeret administratoradgang til Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

### <a name="licensespermissions"></a>Konfigurer tilladelser baseret på licenser

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Administratorer kan konfigurere tilladelsessæt og brugergrupper for hver licens.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Den almindeligt benyttede licens, *Dynamics 365 Business Central Team-medlem*, har som standard følgende tilladelser:

- D365 LÆSE
- D365 TEAMMEDLEM
- REDIGER I EXCEL-VISNING
- EKSPORTERE RAPPORT-EXCEL
- LOKAL

Andre tilladelsessæt tilføjes automatisk på grundlag af de brugergrupper, der er tildelt licensen. Når du opretter en ny bruger, der er baseret på denne licens, tildeler [!INCLUDE[prod_short](includes/prod_short.md)] de tilladelsessæt, der stammer fra brugergrupperne, og tilladelsessættet fra licensen. De samme starttilladelser tildeles brugeren, hvis deres brugerkonto oprettes automatisk i [!INCLUDE[prod_short](includes/prod_short.md)] , eller hvis administratoren brugte handlingen **Opdater brugere fra Microsoft 365** på siden **Brugere**.

Hvis denne standardkonfiguration ikke er den korrekte opsætning for et bestemt miljø, kan administratoren ændre denne konfiguration. Tilpassede tilladelser har imidlertid kun indflydelse på nye brugere, som har fået tildelt licensen. Tilladelser til eksisterende brugere, der har fået tildelt licens, påvirkes ikke.  

1. Log på [!INCLUDE[prod_short](includes/prod_short.md)] som administrator.  
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Licenskonfiguration**, og vælg derefter det relaterede link.  

    <!--Alternatively, if you're already in the **Users** page, you can run the **Update Users from Microsoft 365** guide, and then, on the first page of the guide, choose the **Configure permissions per license** link.-->  
3. På siden **Licenskonfiguration** skal du vælge den licens, du vil tilpasse, og derefter skal du vælge handlingen **Konfigurer**.  
4. Vælg feltet **Tilpas tilladelser**, som du vil skifte til tilpasning af, og foretag derefter de relevante ændringer.  

    I eksemplet vil administratoren gerne fjerne tilladelsen til redigering i Excel, så de fjerner brugergruppen *Excel-eksporthandling* fra Team-medlemslicens. Nye brugere, der får tildelt licensen Team medlem, får ikke mulighed for at eksportere data til Excel. Hvis organisationen ændrer deres opfattelse af dette emne, kan du blot gå tilbage til siden **Licenskonfiguration** og deaktivere tilpasningen for den pågældende licenstype.  

> [!IMPORTANT]
> Denne tilpasning af tilladelser træder kun i kraft for nye brugere, som du tildeler den relevante licens. Eksisterende brugere opdateres ikke. Det anbefales, at du tilpasser tilladelserne, inden du begynder at tildele brugere licenser i Microsoft 365 Administrationscenter.

### <a name="adduser"></a>Sådan tilføjer du en bruger eller opdaterer brugeroplysninger og licenstildelinger i Business Central

Når du har tilføjet brugere eller ændret brugeroplysninger i Microsoft 365 Administration, kan du hurtigt importere bruger oplysningerne til [!INCLUDE[prod_short](includes/prod_short.md)]. Importen omfatter licenstildelinger.  

1. Log på [!INCLUDE[prod_short](includes/prod_short.md)] som administrator.
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugere**, og vælg derefter det relaterede link.  
3. Vælg **Opdater brugere fra Microsoft 365**.

> [!IMPORTANT]  
> Hvis du bruger synkroniseringen af brugere fra Microsoft 365, der bruger vejledningen **Opdater brugere fra Microsoft 365** , kræves SUPER-tilladelsen.

> [!NOTE]
> Vejledningen **Opdater brugere fra Microsoft 365** opdaterer ikke brugere, der ikke er tildelt en licens, f. eks. en person, der er Global administrator og Dynamics 365 administrator. Disse brugere opdateres næste gang, de logger på miljøet.

For nye brugere er næste trin at tildele brugergrupper og tilladelser. Du kan finde flere oplysninger i [Tildele rettigheder til brugere og grupper](ui-define-granular-permissions.md). Hvis du opdaterer en bruger, og opdateringen indeholder en licens ændring, tildeles brugerne til den relevante brugergruppe, og deres tilladelsessæt bliver opdateret. Du kan finde flere oplysninger i [Administrere rettigheder gennem brugergrupper](ui-define-granular-permissions.md).  

> [!NOTE]
> Alle brugere i et miljø skal tildeles den samme licens, enten Essentials eller Premium. Hvis du vil have flere oplysninger om licenser, skal du gå til webstedet [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Du kan få flere oplysninger om synkronisering af brugeroplysninger med Microsoft 365 i afsnittet [Synkronisering med Microsoft 365](#m365).

> [!NOTE]
> Hvis du bruger en ekstern revisor til at administrere dine regnskaber og regnskabsaflæggelse, kan du invitere ham eller hende indenfor i din [!INCLUDE[prod_short](includes/prod_short.md)], så de kan samarbejde med dig om dine regnskabsdata. Du kan finde flere oplysninger i [Inviter din eksterne revisor til at deltage i din Business Central](finance-accounting.md#inviteaccountant).

### Sådan fjernes en brugers adgang til systemet

I onlineinstallationer kan du fjerne en brugers adgang til [!INCLUDE[prod_short](includes/prod_short.md)]. Alle referencer til brugeren bevares. Men brugeren kan ikke logge på og aktive sessioner for brugeren stoppes.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugere**, og vælg derefter det relaterede link.
2. Åbn siden **Brugerkort** for den relevante bruger, og vælg derefter **Deaktiveret** i feltet **Status**.
3. Hvis du vil give brugeren adgang igen, skal du angive feltet **Status** til **Aktiveret**.

Du kan også fjerne licensen fra en bruger i Microsoft 365 Administration. Brugeren kan derefter ikke logge på. Du kan få flere oplysninger i [Fjerne licenser fra brugere](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="m365"></a>Synkronisering med Microsoft 365

Når du fjerner tildelingen af en licens til [!INCLUDE[prod_short](includes/prod_short.md)] for en bruger i Microsoft 365, kan du oprette brugeren i [!INCLUDE[prod_short](includes/prod_short.md)] på to måder.  

- Administratoren kan tilføje brugeren ved at vælge handlingen **Opdater brugere fra Microsoft 365** på siden **Brugere** som beskrevet i afsnittet [Sådan tilføjer du en bruger eller opdaterer brugeroplysninger i Business Central](#adduser).
- Licensoplysningerne opdateres automatisk, når brugeren logger på for første gang.

I begge tilfælde anvendes der automatisk flere indstillinger. Disse indstillinger er angivet i den anden og tredje kolonne i nedenstående tabel.

Hvis du ændrer brugeroplysningerne i Microsoft 365, kan du opdatere [!INCLUDE[prod_short](includes/prod_short.md)], så de afspejler ændringen. Afhængigt af hvad du vil opdatere, skal du bruge en af handlingerne på siden **Brugere**. Handlingerne er beskrevet i de sidste to kolonner i nedenstående tabel.

|Hvad sker der, når:|Første bruger, første login|Brugere opdateres fra Microsoft 365|Brugerens standardbrugergrupper gendannes|
|-|-|-|-|
|Omfang:|Aktuelle bruger|Flere markerede brugere|Enkelt valgte bruger (undtagen aktuel)|
|Opret den nye bruger, og tildel rettighedssættet SUPER.<br /><br /><!--Platform-->|**X**|**X** | | 
|Opdater brugeren ud fra oplysninger i Microsoft 365: Status, Fulde navn, Kontaktens mailadresse, Godkendelsesmail.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|
|Synkroniser brugerplaner (licenser) med licenser og roller tildelt i Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|
|Føj brugeren til brugergruppen i henhold til de aktuelle brugerplaner. Fjern SUPER-tilladelsessættet for alle andre brugere end den første bruger, der skal logge på, og [administratorer](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Der kræves mindst én SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**<br /><br />Fjerner manuelt tildelte brugergrupper og tilladelser.|

Brugere kan få adgang til [!INCLUDE[prod_short](includes/prod_short.md)]-poster i Teams ved hjælp af deres Microsoft 365-licens. Når adgang aktiveres for et miljø, inkluderer synkronisering med **Opdater brugere Microsoft 365**-handlingen ikke brugere, der kun har en Microsoft 365-licens. Hvis du vil medtage disse brugere i synkroniseringen, skal du først opdatere miljø indstillingerne ved at tildele en sikkerhedsgruppe, der indeholder brugere med en [!INCLUDE[prod_short](includes/prod_short.md)]-licens, og brugere med kun en Microsoft 365-licens.

Få mere at vide om at sikre adgang til miljøer med sikkerhedsgrupper i [Administrer adgang med Azure Active Directory-grupper](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

Få et overblik over, hvordan du åbner [!INCLUDE[prod_short](includes/prod_short.md)] i Teams med Microsoft 365-licenser i [admin-access-with-m365-license](admin-access-with-m365-license.md).

## Administrere brugere og licenser i Installationer på stedet

I installationer i det lokale miljø er der angivet et antal brugerlicenser i licensfilen (.bclicense or .flf). Når en administrator eller Microsoft-partneren overfører licensfilen, kan de angive, hvilke brugere der kan logge på [!INCLUDE[prod_short](includes/prod_short.md)].

I forbindelse med installationer i det lokale miljø opretter redigerer og sletter administratoren brugere direkte fra siden **Brugere.**

### Sådan redigeres eller slettes en bruger i en lokal installation

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugere**, og vælg derefter det relaterede link.
2. Vælg den bruger, som du vil redigere, og vælg derefter handlingen **Rediger**.
3. På siden **Brugerkort** kan du ændre oplysningerne efter behov.  
4. Hvis du vil slette en bruger, skal du markere den pågældende bruger og derefter vælge handlingen **Slet**.

> [!NOTE]
> I lokale installationer skal en administrator angive, hvordan en brugers legitimationsoplysninger skal godkendes i forekomsten af [!INCLUDE[server](includes/server.md)] . Når du opretter en bruger, skal du angive den type legitimationsoplysninger, som du bruger.
>
> Du kan finde flere oplysninger i [Godkendelse og typer af legitimationsoplysninger](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i administrationens Hjælp til [!INCLUDE[prod_short](includes/prod_short.md)].

## Se også

[Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Tilpasning [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Opsætning](admin-setup-and-administration.md)  
[Licensering i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Føje brugere til Microsoft 365 til virksomheder](/microsoft-365/admin/add-users/add-users)  
[Sikkerhed og beskyttelse i Business Central (administration)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Tildele brugere en telemetri-id](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]