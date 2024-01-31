---
title: Udvidelsen til momsgruppe styring for Storbritannien
description: 'Du kan arbejde med andre virksomheder for at danne en momsgruppe, hvor alle medlemmer rapporterer moms i en enkelt returnering.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: soalex
ms.topic: conceptual
ms.search.keywords: 'VAT, value added tax, report'
ms.search.form: '4700, 4701, 4703, 4704, 4705, 4706, 4707, 4708, 4709,'
ms.date: 12/12/2023
ms.service: dynamics-365-business-central
---

# Udvidelsen til momsgruppe styring for Storbritannien

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Du kan forbinde en eller flere virksomheder i Storbritannien for at konsolidere momsrapporteringen under et enkelt registreringsnummer. Denne type arrangement er kendt som en *momsgruppe*. Du kan deltage i gruppen som medlem eller gruppens repræsentant.

## Danner en momsgruppe

Medlemmer af momsgruppen og grupperepræsentanten kan bruge **Opsætning af den assisterede opsætning af momsgruppe styring** til at definere deres ansættelse med gruppen og oprette en forbindelse mellem deres [!INCLUDE[prod_short](includes/prod_short.md)]-lejere. Gruppemedlemmerne bruger forbindelsen til at sende deres moms tilbage til gruppens repræsentant. Repræsentanten sender en enkelt momsangivelse til skattemyndighederne på koncernens vegne ved hjælp af en enkelt moms Returvare.

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter afsendelser af Fællesskabs retur indgange for virksomheder, der bruger [!INCLUDE[prod_short](includes/prod_short.md)] on-premises eller online, i enhver kombination, der har indflydelse på kommunikations opsætningen mellem virksomheder. Denne artikel beskriver forskellige gruppeopsætninger.

### Licenskrav

Deltagerne i gruppen skal have licens til brug af [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan ikke bruge gæstekonti i momsgrupper.

* Hvis en bruger skal beregne og sende moms, skal den være en central [!INCLUDE[prod_short](includes/prod_short.md)]-bruger.
* Hvis du vil logge på og udføre grundlæggende opgaver, f. eks. oprette konti, kan du have [!INCLUDE[prod_long](includes/prod_long.md)]-licensen Team medlem.

## Opsætning af momsgruppe

Følgende liste viser den anbefalede rækkefølge for trinene til oprettelse af en momsgruppe:

1. Opret opsætningen [Microsoft Entra ID-opsætning for gruppemedlemmer](#microsoft-entra-id-setup-for-group-members).
2. Dele de tekniske oplysninger, som momsgruppe medlemmerne og repræsentanten skal bruge for at tilslutte deres [!INCLUDE[prod_short](includes/prod_short.md)]-leje. Momsgrupperepræsentanten har som regel disse oplysninger, f.eks. [API URL](#group-api-setup) og navnet på den momsgruppe, som medlemmerne af MOMS-gruppen skal indsende moms til.
3. Oprette brugere, som momsgruppens repræsentanter kan bruge til at godkende, når du forbindes til momsgruppens repræsentanters [!INCLUDE[prod_short](includes/prod_short.md)] Brugeren skal have en fuld gyldig licens til [!INCLUDE[prod_short](includes/prod_short.md)].
4. Kør guiden **Konfigurer momsgruppestyring** for at forbinde medlemmerne af momsgruppen.

   Momsgruppe repræsentanten skal angive visse oplysninger for at gruppere medlemmerne for at fuldføre opsætningen. (Få mere at vide i [Opsætning af momsgruppe medlemmer](#set-up-vat-group-members) nedenfor.) Noter **gruppemedlems-id'et** for hvert momsgruppemedlem. Repræsentanten skal bruge disse id'er for at føje regnskaberne til momsgruppen.
5. Du kan konfigurere udvidelsen af momsgruppestyringen i momsgrupperepræsentanternes [!INCLUDE[prod_short](includes/prod_short.md)] vha vejledningen **Opsætning af momsgruppestyring**.

> [!NOTE]
> Hvis du vil oprette forbindelse til momsgruppens repræsentant, skal gruppemedlemmerne bruge en bruger med adgang til momsgruppens repræsentants [!INCLUDE[prod_short](includes/prod_short.md)]. MOMS-gruppens repræsentant skal oprette mindst én bruger til dette. Af sikkerhedsgrunde anbefales det imidlertid, at der oprettes en bruger for hvert momsgruppe medlem, som kan være en systembrugerkonto, som ikke er relateret til en faktisk person. Sørg for at distribuere legitimationsoplysningerne for disse brugere til momsgruppemedlemmer på en sikker måde.

### Microsoft Entra ID-opsætning af gruppemedlemmer

Når repræsentanten for momsgruppen bruger [!INCLUDE[prod_short](includes/prod_short.md)] online eller lokalt, bruger momsgruppemedlemmerne Microsoft Entra ID til at godkende brugere, når de sender momsreturvarer til den ansvarlige momsgruppe. For [!INCLUDE[prod_short](includes/prod_short.md)]-lokale brugere skal medlemmerne konfigurere Single Sign-on. Du kan finde flere oplysninger i [Konfigurere Microsoft Entra-godkendelse med WS-Federation](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool).

Hvis medlemmerne af momsgruppen også bruger [!INCLUDE[prod_short](includes/prod_short.md)] online, kan medlemmet af momsgruppen godkende vha. de angivne legitimationsoplysninger og slutpunktoplysningerne. Få mere at vide i afsnittet om [Opsætning af momsgruppemedlemmer](#set-up-vat-group-members) herunder.

Medlemmer af momsgruppe, der har [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, skal konfigurere en app-registrering i Microsoft Entra ID for momsgruppemedarbejderens [!INCLUDE[prod_short](includes/prod_short.md)]-lejer. App-registreringen gør det muligt for momsgruppens repræsentants [!INCLUDE[prod_short](includes/prod_short.md)] online at godkende Gruppemedlemmet. Du kan finde flere oplysninger om registrering af et program i [Hurtig start: Registrere et program på Microsoft-identitetsplatformen](/azure/active-directory/develop/quickstart-register-app).

Når administratoren af momsgruppens medlem opretter app-registreringen i Microsoft Entra ID, skal du angive følgende oplysninger.

* I afsnittet **Godkendelse** tilføjes **Web** som platform, og følgende **URL-adresse til omdirigering**: `https://businesscentral.dynamics.com/OAuthLanding.htm` bruges.
* Afsnittet **Godkendelse** i indstillingen til at vælge **Understøttede kontotyper** skal du vælge **Konti i en hvilken som helst organisations mappe (vilkårlig Microsoft Entra-mappe - multi lejer)**.
* Opret en ny klienthemmelighed, og læg mærke til værdien i sektionen **Certifikater & hemmeligheder**. Momsgruppemedlemmerne skal bruge hemmeligheden, når de konfigurerer forbindelsen til gruppens repræsentant.
* Tilføj tilladelser i afsnittet **API-tilladelser** [!INCLUDE[prod_short](includes/prod_short.md)]. Aktivér uddelegeret adgang til **Financials.ReadWrite.All** og **user_impersonation**.
* I afsnittet **Oversigt** bemærkes **Program-id (klient)**. Momsgruppemedlemmerne skal bruge id, når de konfigurerer forbindelsen til gruppens repræsentant.

### Opsætning af momsgruppemedlem

Repræsentanten for momsgruppen opretter og leverer en API til gruppemedlemmerne. Medlemmerne bruger API'EN til at oprette forbindelse til medarbejderens [!INCLUDE[prod_short](includes/prod_short.md)]-lejer og sende momsreturneringer. Medlemmerne af momsgruppen vil ofte bruge [!INCLUDE[prod_short](includes/prod_short.md)] i separate Microsoft Entra-lejere. Derfor skal mere opsætning være nødvendig, hvis der skal oprettes forbindelse mellem momsgruppemedlemmet og repræsentantens [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Denne opsætning kræver, at du angiver legitimationsoplysninger for en administratorbrugerkonto med fuld brugerlicens til [!INCLUDE[prod_short](includes/prod_short.md)].

1. Vælg fanen **miljøer** i Business central administration til medarbejderens lejer.
1. Vælg repræsentatens miljø.
1. Kopier **URL-adressen** i sektionen **Detaljer**.
1. Åbn Notesblok, og indsæt URL-adressen. Erstat `https://businesscentral.dynamics.com` med `https://api.businesscentral.dynamics.com/v2.0`.

## Opsætning af momsgruppemedlemmer

Medlemmerne af momsgruppen tilkobler repræsentanten ved at kalde en webtjeneste på den sælger ansvarlige for momsgruppen. Brugeren skal godkendes ved brug af OAuth2. Når udvidelsen til momsgruppestyring er sat op, bliver du bedt om at godkende momsgruppens repræsentant for at hente og gemme en adgangstoken. Dette adgangstoken bruges ved afsendelse af moms tilbage til momsgruppens repræsentant.

> [!IMPORTANT]
> Medlemsfirmaerne i momsgruppen behøver ikke at oprette forbindelse til HMRC, fordi de rapporterer gennem gruppens repræsentant.

Før momsgruppemedlemmer starter opsætningen (vist nedenfor), skal de kontakte den ansvarlige for momsgruppen for at få følgende oplysninger om deres [!INCLUDE[prod_short](includes/prod_short.md)]-lejer:

* API URL
* Navn på virksomheden
* Logonoplysninger til den dedikerede bruger

1. I øverste højre hjørne under menuen skal du vælge **Indstillinger** ![Indstillinger](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter"). ikon, og derefter handlingen **Assisteret opsætning**.
2. Vælg handlingen **Konfigurer moms-gruppestyring**.
3. Vælg i feltet **Momsgrupperolle** **Medlem** og derefter **Næste**.
4. Kopier værdien i feltet **Gruppemedlems-id**, og del det med momsgruppens repræsentant, så de kan tilføje din virksomhed som godkendt medlem af gruppen.
5. Angiv den version af [!INCLUDE[prod_short](includes/prod_short.md)], som repræsentanten bruger, i feltet **Grupperepræsentantproduktversion** for gruppen.
6. Angiv det API URL, som repræsentanten for momsgruppen har opgivet, i feltet **API URL**. Normalt er URL-adressen formateret på følgende måde: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Eksempel `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.
7. I feltet **Grupperepræsentativ virksomhed** skal du angive den repræsentative momsgruppes firmanavn, f.eks. **CRONUS UK Ltd**.
8. Vælg indstillingen **OAuth2** i feltet **Godkendelsestype**. Hvis repræsentanten for momsgruppen bruger [!INCLUDE[prod_short](includes/prod_short.md)] online, skal du angive, at **Grupperepræsentanten bruger Business central online**, og derefter skal du vælge **Næste**.

   Følg derefter trinnene i enten [momsgrupperepræsentant bruger Business Central online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) eller [momsgrupperepræsentant bruger Business Central On-premises](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premises)-sektionen herunder.

### Moms-grupperepræsentant bruger Business Central online

1. Angiv de brugerlegitimationsoplysninger, som er blevet leveret af momsgruppe beviset, og tilføj de nødvendige tilladelser.
2. Vælg den momsrapportkonfiguration, der aktuelt bruges til at sende moms-returvarer til UK-skattemyndighederne. 

Når du har fuldført opsætningen, opretter [!INCLUDE[prod_short](includes/prod_short.md)] en ny konfiguration baseret på dette valg, og du kan bruge konfigurationen til at sende moms returvarer til den ansvarlige momsgruppe.

### Moms-grupperepræsentant bruger Business Central On-premises

1. Angiv brugerlegitimationsoplysningerne fra momsgrupperepræsentanten, og vælg **næste**.
2. I feltet **Klient-ID** skal du angive klient-id fra app-registreringen i [Microsoft Entra ID-opsætning for gruppemedlemmer](#microsoft-entra-id-setup-for-group-members).
3. I feltet **Klient-hemmelighed** skal du angive klient-hemmeligheden fra programregistreringen i Microsoft Entra ID.
4. I feltet **OAuth 2.0 Myndighedsslutpunkt**-feltet skal du angive `https://login.microsoftonline.com/common/oauth2`.
5. I feltet **OAuth 2.0 URL-adresse til ressource** skal du angive `https://api.businesscentral.dynamics.com/`.
6. I feltet **OAuth 2.0 URL-adresse til omdirigering** skal du angive `https://businesscentral.dynamics.com/OAuthLanding.htm`.
7. Når du har angivet de forskellige felter, skal du vælge **næste** og derefter bekræfte godkendelses forbindelsen for at oprette dette adgangstoken.
8. Vælg den momsrapportkonfiguration, der aktuelt bruges til at sende moms-returvarer til UK-skattemyndighederne.

## Oprette repræsentanten for momsgruppen

> [!NOTE]
> Til on-premises understøtter [!INCLUDE[prod_short](includes/prod_short.md)] kun en enkelt lejer forekomst af en grupperepræsentant.

> [!IMPORTANT]
> Det repræsentative regnskab skal aktivere **HMRC for moms installationstjenesten** på siden **serviceforbindelser**. Repræsentanter skal også hente moms-returperioder fra HMRC.

1. I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter"), og derefter vælge handlingen **Assisteret opsætning**.
2. Vælg handlingen **Konfigurer moms-gruppestyring**.
3. Vælg i feltet **Momsgrupperolle** den **Repræsentant**, der skal fungere som repræsentant for momsgruppe, og vælg derefter **næste**.
4. I feltet **gruppe afregningskonto** skal du angive den afregningskonto, der skal bruges til gruppemedlems momsbeløb. Denne konto skal have **Aktiver** som **kontokategorien**.
5. I feltet **moms-afregningskonto** skal du angive den konto, du bruger til momsudligninger. Denne konto skal have **Passiver** som **kontokategorien**.
6. I feltet **moms forfaldent** angives den boks, der repræsenterer det samlede skyldige momsbeløb fra en afsendt momsgruppe.
7. Brug feltet **Finanskladdetype for gruppeafregning** til at angive den Finanskladdetype, der er anvendt til dokumentet, for at bogføre gruppe momsen på afregningskontoen.
8. Feltet **Godkendte medlemmer** viser antallet af gruppemedlemmer, der er angivet til at sende momsopgørelser til repræsentanten. Tilføj følgende oplysninger på siden **momsgrupper for godkendte medlemmer** for at tilføje nye medlemmer:
    1. Angiv et id for Gruppemedlemmet i feltet **gruppemedlem-id**, som vist under opsætningen af gruppemedlemmer (få mere at vide i afsnittet [opsætning af momsgruppe](#set-up-vat-group-members)-afsnittet ovenfor).
    2. I feltet **gruppemedlemsnavn** skal du angive navnet på Gruppemedlemmet.
    3. Angiv i feltet **Firma** den virksomhed, hvorfra gruppemedlemmet vil sende momsreturneringer i [!INCLUDE[prod_short](includes/prod_short.md)], f.eks. **CRONUS UK Ltd**.
    4. Angiv din virksomheds kontaktoplysninger.

## Bruge funktionerne til momsgruppestyring

Medlemmer af momsgruppen bruger standardprocesserne til at oprette momsreturneringer. Den eneste forskel er at vælge rapportversionen **Momsgruppe** på siden **Returmoms** for at sende moms retur til momsgrupperepræsentanten i stedet for myndighederne. Få mere at vide på [rapporten Momsopgørelse](finance-how-report-vat.md#vatreturn).

> [!NOTE]
> Medlemmer af momsgruppen kan rette i afsendte momsmeldinger, så længe gruppens repræsentant ikke har frigivet momsreturværdien for gruppen. Hvis du vil foretage en rettelse, skal momsgruppemedlemmet oprette en ny momsreturnering for momsafleveringsperioden og sende den til den ansvarlige for momsgruppen. Momsgruppens repræsentant vil medtage den seneste momsleverance på siden **Momsopgørelse**.

I følgende afsnit beskrives de opgaver, som momsgrupperepræsentanter skal udføre for at registrere momsgruppeopgørelse.

### Gennemse indsendelse af gruppemedlem

På siden **Momsgruppemeddelser** vises momsreturneringer, som medlemmerne har indsendt. Siden tjener som en kladde placering til indsendelserne, indtil repræsentanten for momsgruppen medtager dem i en momsreturnering for gruppen. Repræsentanten kan åbne indsendelserne for at gennemgå momsen for de enkelte felter, der er rapporteret af momsgruppemedlemmet.

> [!TIP]
> På siden **momsangivelsesperioder** viser felterne **Indsendelse af gruppemedlem**, hvor mange returmedlemmer der er sendt. Hvis du vil sikre dig, at nummeret er opdateret, skal du vælge handlingen **Hent momsreturvarer**.

### Oprette en gruppemomsretur

Hvis du vil rapportere moms på vegne af gruppen, skal du kun oprette en momsreturnering til virksomheden på siden **momsreturneringer**. Derefter skal du medtage de seneste momsafsendelser fra momsgruppemedlemmer ved at vælge handlingen **Medtag gruppemoms**.  

Når momsgruppens momsgruppe er blevet sendt til myndighederne på vegne af hele koncernen, skal du normalt udføre handlingen **Afregn moms**. Handlingen lukker åbne momsposter og overfører købs- og salgsmomsbeløb til momsafregningskontoen. I øjeblikket medtager denne handling ikke gruppeindgangene i gruppen. Kun momsposter fra repræsentative momsgrupper bogføres. Beløbene i momsgruppemedarbejderne skal bogføres på MOMS-afregningsbeløbet manuelt, så momsgruppemedarbejders momskonto vil afspejle det ansvar, der er indberettet til myndighederne. Denne funktionsmåde ændres i en kommende opdatering af [!INCLUDE[prod_short](includes/prod_short.md)], så hele gruppemomsen (det samlede beløb på momsreturneringen) udlignes.

> [!IMPORTANT]
> Momsgruppefunktionen understøttes kun på de markeder, hvor [!INCLUDE[prod_short](includes/prod_short.md)], der bruger en momsramme, som består af momsopgørelser og momsreturperioder. Du kan ikke bruge momsgrupper på andre markeder, der har andre implementeringer af lokal momsrapportering, f.eks. Østrig, Tyskland, Italien, Spanien og Schweiz.

## Problem med aktivering af Multifactor Authentication (MFA)

Hvis du får en fejlmeddelelse vedrørende godkendelse under fornyelsen af **OAuth2-tokenet** på siden **Opsætning af momsrapport**, efter du har aktiveret MFA, skal du udføre følgende trin.  

1. Log på **Azure Portal** som godkendelsesadministrator.  
2. Gå til **Microsoft Entra ID**.   
3. Gå til **Brugere**, og vælg den bruger, der skal udføre en handling.  
4. Vælg **godkendelsesmetoderne** , og vælg **Kræv multifaktorgodkendelse** igen øverst på siden. 
5. Gå tilbage til Dynamics 365 Business Central, og vælg at forny tokenet fra **momsrapportopsætningen**.  

Dette bør være en engangsopsætning, når du har aktiveret multifaktorgodkendelse for den bruger, der er valgt i **Momsrapportopsætning**.  

## Se også

[Lokal funktionalitet for Storbritannien i den britiske version](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Overførsel af moms digitalt i Storbritannien](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Arbejde med moms af salg og køb](finance-work-with-vat.md)  
[Konfigurere moms](finance-setup-vat.md)  
[Arbejde med moms af salg og køb](finance-work-with-vat.md)  
[Konsolidering af finansielle oplysninger fra flere regnskaber](finance-consolidated-company-reporting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
