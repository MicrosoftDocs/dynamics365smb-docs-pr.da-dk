---
title: Udvidelsen til momsgruppe styring for Storbritannien
description: Du kan arbejde med andre virksomheder for at danne en momsgruppe, hvor alle medlemmer rapporterer moms i en enkelt returnering.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, value added tax, report
ms.search.forms: ''
ms.date: 05/24/2022
ms.author: bholtorf
ms.openlocfilehash: c5757a78a44e3cdc2f6100c42b5105734928837b
ms.sourcegitcommit: 7a6efcbae293c024ca4f6622c82886decf86c176
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/02/2022
ms.locfileid: "8841916"
---
# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>Udvidelsen til momsgruppe styring for Storbritannien

Du kan forbinde en eller flere virksomheder i dit land for at konsolidere momsrapporteringen under et enkelt registreringsnummer. Denne type arrangement er kendt som en *momsgruppe*. Du kan deltage i gruppen som medlem eller gruppens repræsentant.

## <a name="forming-a-vat-group"></a>Danner en momsgruppe
Medlemmer af momsgruppen og grupperepræsentanten kan bruge **Opsætning af den assisterede opsætning af momsgruppe styring** til at definere deres ansættelse med gruppen og oprette en forbindelse mellem deres [!INCLUDE[prod_short](includes/prod_short.md)]-lejere. Gruppemedlemmerne bruger forbindelsen til at sende deres moms tilbage til gruppens repræsentant. Repræsentanten sender en enkelt momsangivelse til skattemyndighederne på koncernens vegne ved hjælp af en enkelt moms Returvare. 

## <a name="license-requirements"></a>Licenskrav
Deltagerne i gruppen skal have licens til brug af [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan ikke bruge gæstekonti i momsgrupper. 

* Hvis en bruger skal beregne og sende moms, skal den være en central Business Central-bruger.
* Hvis du vil logge på og udføre grundlæggende opgaver, f. eks. oprette konti, kan du have Dynamics 365 Business Central-licensen Team medlem.

## <a name="vat-group-constellations"></a>Momsgruppe-konstellationer
Kommunikation sker fra gruppemedlemmer til repræsentanten. Grupperepræsentanten udviser et API URL, som gør det muligt for medlemmerne at sende deres moms tilbage til momsgruppens repræsentant. 
[!INCLUDE[prod_short](includes/prod_short.md)] understøtter indleveringer på tværs af grupper til virksomheder [!INCLUDE[prod_short](includes/prod_short.md)], der bruger lokalt eller online, og i enhver kombination. Opsætningen af kommunikationen afhænger af konstellationen. Denne artikel beskriver forskellige gruppekonstellationer.

Følgende liste viser den anbefalede rækkefølge for trinene til oprettelse af en momsgruppe:

1. Opret den nye momsopsætning i Azure Active Directory. Du kan finde flere oplysninger i [Krav til godkendelse](ui-extensions-vat-group.md#requirements-for-authentication).
2. Dele de tekniske oplysninger, som momsgruppe medlemmerne og repræsentanten skal bruge for at tilslutte deres [!INCLUDE[prod_short](includes/prod_short.md)]-leje. Momsgrupperepræsentanten har som regel disse oplysninger, f.eks. navnet på den momsgruppe, som medlemmerne af MOMS-gruppen skal indsende moms til.
3. Oprette brugere, som momsgruppens repræsentanter kan bruge til at godkende, når du forbindes til momsgruppens repræsentanters [!INCLUDE[prod_short](includes/prod_short.md)] Brugeren skal have en fuld gyldig licens til [!INCLUDE[prod_short](includes/prod_short.md)].
4. Kør guiden **Konfigurer momsgruppestyring** for at forbinde medlemmerne af momsgruppen.

  Guiden kræver nogle oplysninger fra den ansvarlige momsgruppe. Du kan finde flere oplysninger i afsnittet [Opsætning af momsgruppemedlemmer](#set-up-vat-group-members). Noter **gruppemedlems-id** for hvert momsgruppemedlem. Repræsentanten skal bruge disse id'er for at føje regnskaberne til momsgruppen.
5. Du kan konfigurere udvidelsen af momsgruppestyringen i momsgrupperepræsentanternes [!INCLUDE[prod_short](includes/prod_short.md)] vha vejledningen **Opsætning af momsgruppestyring**. 

> [!NOTE]
> Hvis du vil oprette forbindelse til momsgruppens repræsentant, skal gruppemedlemmerne bruge en bruger med adgang til momsgruppens repræsentants [!INCLUDE[prod_short](includes/prod_short.md)]. Repræsentanten for momsgruppen skal imidlertid oprette mindst én bruger af sikkerhedsmæssige årsager. Det anbefales dog, at du opretter en bruger for hvert momsgruppemedlem. Sørg for at distribuere legitimationsoplysningerne for disse brugere til momsgruppemedlemmer på en sikker måde. Det er en systembrugerkonto, som ikke er relateret til en aktuel person.

## <a name="about-the-vat-group-management-setup"></a>Forståelse af opsætning af momsgruppestyring

Repræsentanten for momsgruppen udviser en API for at gruppere medlemmerne. Medlemmerne bruger API'EN til at oprette forbindelse til medarbejderens [!INCLUDE[prod_short](includes/prod_short.md)]-lejer og sende momsreturneringer. Medlemmerne af momsgruppen vil ofte bruge [!INCLUDE[prod_short](includes/prod_short.md)] i separate Azure Active Directory-lejere. Derfor skal mere opsætning være nødvendig, hvis der skal oprettes forbindelse mellem momsgruppemedlemmet og repræsentantens [!INCLUDE[prod_short](includes/prod_short.md)]. 
  
Medlemmerne af momsgruppen tilkobler repræsentanten ved at kalde en webtjeneste på den sælger ansvarlige for momsgruppen. Brugeren skal godkendes ved brug af OAuth2. Når udvidelsen til momsgruppestyring er sat op, bliver du bedt om at godkende momsgruppens repræsentant for at hente og gemme en adgangstoken. Dette adgangstoken bruges ved afsendelse af moms tilbage til momsgruppens repræsentant. 

## <a name="construct-the-api-url"></a>Konstruer API-URL-adressen
1. Vælg fanen **miljøer** i Business central administration til medarbejderens lejer.
2. Kopier **URL-adressen** i sektionen **Detaljer**.
3. Åbn Notesblok, og indsæt URL-adressen. Erstat **https://businesscentral.dynamics.com** med **https://api.businesscentral.dynamics.com/v2.0**.

## <a name="requirements-for-authentication"></a>Krav til godkendelse 
> [!NOTE]
> Dette kræver, at du angiver legitimationsoplysninger for en administratorbrugerkonto med fuld brugerlicens til [!INCLUDE[prod_short](includes/prod_short.md)].

Når repræsentanten for momsgruppen bruger [!INCLUDE[prod_short](includes/prod_short.md)] online eller on-premises, bruger momsgruppemedlemmerne Azure Active Directory til at godkende brugere, når de sender momsreturvarer til den ansvarlige momsgruppe. For [!INCLUDE[prod_short](includes/prod_short.md)]-lokale brugere skal medlemmerne konfigurere Single Sign-on. Du kan finde flere oplysninger i [Konfigurere Azure Active Directory-godkendelse med WS-Federation](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool). Hvis medlemmerne af momsgruppen også bruger [!INCLUDE[prod_short](includes/prod_short.md)] online, kan medlemmet af momsgruppen godkende vha. de angivne legitimationsoplysninger og slutpunktoplysningerne. Du kan finde flere oplysninger i afsnittet [Opsætning af momsgruppemedlemmer](ui-extensions-vat-group.md#set-up-vat-group-members).

Medlemmer af momsgruppe, der har [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, skal konfigurere en app-registrering i Azure Active Directory for momsgruppemedarbejderens [!INCLUDE[prod_short](includes/prod_short.md)]-lejer. App-registreringen gør det muligt for momsgruppens repræsentants [!INCLUDE[prod_short](includes/prod_short.md)] online at godkende Gruppemedlemmet. Du kan finde flere oplysninger om registrering af et program i [Hurtig start: Registrere et program på Microsoft-identitetsplatformen](/azure/active-directory/develop/quickstart-register-app).

Når du opretter app-registreringen i Azure Active Directory, skal du angive følgende oplysninger.

* I afsnittet **Godkendelse** tilføjes **Web** som platform, og følgende **URL-adresse til omdirigering**: https://businesscentral.dynamics.com/OAuthLanding.htm bruges.
* Afsnittet **Godkendelse** i indstillingen til at vælge **Understøttede kontotyper** skal du vælge **Konti i en hvilken som helst organisations mappe (vilkårlig Azure AD-mappe - multi lejer)**.
* Opret en ny klienthemmelighed, og læg mærke til værdien i sektionen **Certifikater & hemmeligheder**. Momsgruppemedlemmerne skal bruge hemmeligheden, når de konfigurerer forbindelsen til gruppens repræsentant.
* Tilføj tilladelser i afsnittet **API-tilladelser** [!INCLUDE[prod_short](includes/prod_short.md)]. Aktivér uddelegeret adgang til **Financials.ReadWrite.All** og **user_impersonation**.
* I afsnittet **Oversigt** bemærkes **Program-id (klient)**. Momsgruppemedlemmerne skal bruge id, når de konfigurerer forbindelsen til gruppens repræsentant. 

## <a name="set-up-vat-group-members"></a>Opsætning af momsgruppemedlemmer
> [!IMPORTANT]
> Medlemsfirmaerne i momsgruppen behøver ikke at oprette forbindelse til HMRC, fordi de rapporterer gennem gruppens repræsentant.

Før du begynder, skal du kontakte momsgruppesælgeren for at få følgende oplysninger om deres [!INCLUDE[prod_short](includes/prod_short.md)]-lejer:

* API URL
* Navn på virksomheden 
* Klient-id
* Klienthemmelighed
* Logonoplysninger til den dedikerede bruger 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfigurer momsgruppestyring**, og vælg derefter det relaterede link.
2. Angiver, om du er medlem af gruppen eller grupperepræsentanten i feltet **Momsgrupperolle**. Vælg **Medlem** til at fungere som gruppemedlem og sende moms tilbage til grupperepræsentanten i stedet for skattemyndighederne, og vælg **Næste**.
3. Kopier værdien i feltet **Gruppemedlems-id**, og del det med momsgruppens repræsentant, så de kan tilføje din virksomhed som godkendt medlem af gruppen.
4. Angiv den version af [!INCLUDE[prod_short](includes/prod_short.md)], som repræsentanten bruger, i feltet **Grupperepræsentantproduktversion** for gruppen.
5. I feltet **Grupperepræsentativ virksomhed** skal du angive den repræsentative momsgruppes firmanavn. F. eks **CRONUS UK Ltd**.
6. Vælg indstillingen **OAuth2** i feltet **Godkendelsestype**. Hvis repræsentanten for momsgruppen bruger [!INCLUDE[prod_short](includes/prod_short.md)] online, skal du angive, at **Grupperepræsentanten bruger Business central online**, og derefter skal du vælge **Næste**. Afhængigt af, om repræsentanten bruger [!INCLUDE[prod_short](includes/prod_short.md)] online eller on-premises, skal du følge fremgangsmåden for enten [moms-grupperepræsentant bruger Business Central online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) eller [Moms-grupperepræsentant bruger Business Central online-premesis](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premesis).

### <a name="vat-group-representative-uses-business-central-online"></a>Moms-grupperepræsentant bruger Business Central online
1. Angiv de brugerlegitimationsoplysninger, som er blevet leveret af momsgruppe beviset, og Tilføj de nødvendige tilladelser.
2. Vælg den momsrapport konfiguration, der aktuelt bruges til at sende moms returvarer til skattemyndighederne. Når du har fuldført opsætningen, opretter [!INCLUDE[prod_short](includes/prod_short.md)] en ny konfiguration baseret på dette valg, og du kan bruge konfigurationen til at sende moms returvarer til den ansvarlige momsgruppe.  
3. Tilføj **API URL-adressen** fra momsgrupperepræsentanten. Normalt er URL-adressen formateret på følgende måde: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Eksempel `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.

### <a name="vat-group-representative-uses-business-central-on-premesis"></a>Moms-grupperepræsentant bruger Business Central On-premesis
1. I feltet **Klient-id** skal du angive klient-id'et fra programregistreringen i Azure Active Directory.
2. I feltet **Klient-hemmelighed** skal du angive klient-hemmeligheden fra programregistreringen i Azure Active Directory.
3. I feltet **OAuth 2.0 Myndighedsslutpunkt**-feltet skal du angive `https://login.microsoftonline.com/common/oauth2`.
4. I feltet **OAuth 2.0 URL-adresse til ressource** skal du angive `https://api.businesscentral.dynamics.com/`.
5. I feltet **OAuth 2.0 URL-adresse til omdirigering** skal du angive `https://businesscentral.dynamics.com/OAuthLanding.htm`.
6. Når du har angivet de forskellige felter, skal du vælge **Næste** og derefter angive de brugerlegitimationsoplysninger, som repræsentanten for momsgruppen har stillet til rådighed.
7. Vælg den momsrapport konfiguration, som du kan bruge til at rapportere moms til myndigheder i dit land.

## <a name="set-up-the-vat-group-representative"></a>Oprette repræsentanten for momsgruppen
> [!NOTE]
> Til on-premesis understøtter vi kun en enkelt lejer forekomst af en grupperepræsentant.

> [!IMPORTANT]
> Det repræsentative regnskab skal aktivere **HMRC for moms installationstjenesten** på siden **serviceforbindelser**. Repræsentanter skal også hente moms-returperioder fra HMRC.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfigurer momsgruppestyring**, og vælg derefter det relaterede link.
2. Angiver, om du er medlem af gruppen eller grupperepræsentanten i feltet **Momsgrupperolle**. Vælg **Repræsentant** til at fungere som moms-gruppemedlem og sende moms tilbage til grupperepræsentanten for gruppen, og derefter vælge **Næste**.
3. I feltet **moms-afregningskonto** skal du angive den konto, du bruger til momsudligninger.
4. I feltet **moms forfaldent** angives den boks, der repræsenterer det samlede skyldige momsbeløb fra en afsendt momsgruppe.
5. Brug feltet **Finanskladdetype for gruppeafregning** til at angive den Finanskladdetype, der er anvendt til dokumentet, for at bogføre gruppe momsen på afregningskontoen.
6. Feltet **Godkendte medlemmer** viser antallet af gruppemedlemmer, der er angivet til at sende momsopgørelser til repræsentanten. Hvis du vil tilføje medlemmer, skal du åbne siden **Godkendte medlemmer**.
7. Tilføj følgende oplysninger på siden **momsgrupper for godkendte medlemmer** for at tilføje nye medlemmer:
    1. Angiv et id for Gruppemedlemmet i feltet **gruppemedlems-id**.
    2. I feltet **gruppemedlemsnavn** skal du angive navnet på Gruppemedlemmet. 
    3. Angiver i feltet **Firma** den virksomhed, hvorfra gruppemedlemmet vil sende momsreturneringer i [!INCLUDE[prod_short](includes/prod_short.md)]. F. eks **CRONUS UK Ltd**.
    4. Angiv din virksomheds kontaktoplysninger.

## <a name="use-the-vat-group-management-features"></a>Bruge funktionerne til momsgruppestyring
Medlemmer af momsgruppen bruger standardprocesserne til at oprette momsreturneringer. Den eneste forskel er at vælge rapportversionen **MOMSGRUPPE**, som sender momsen tilbage til momsgruppens repræsentant i stedet for myndighederne. Du kan finde flere oplysninger i [Om rapporten Momsopgørelse](finance-how-report-vat.md#vatreturn).

I følgende afsnit beskrives de opgaver, som momsgrupperepræsentanter skal udføre.

### <a name="vat-group-submissions"></a>Indsendelser til momsgruppe

På siden **Momsgruppemeddelser** vises momsreturneringer, som medlemmerne har indsendt. Siden tjener som en kladde placering til indsendelserne, indtil repræsentanten for momsgruppen medtager dem i en momsreturnering for gruppen. Du kan åbne indsendelserne for at gennemgå momsen for de enkelte felter, der er rapporteret af momsgruppemedlemmet. 

> [!TIP]
> På siden **momsangivelsesperioder** viser felterne **Indsendelse af gruppemedlem**, hvor mange returmedlemmer der er sendt. Hvis du vil sikre dig, at nummeret er opdateret, skal du vælge handlingen **Hent momsreturvarer**.

### <a name="creating-a-group-vat-return"></a>Oprette en gruppemomsretur

Hvis du vil rapportere moms på vegne af gruppen, skal du kun oprette en momsreturnering til virksomheden på siden **momsreturneringer**. Derefter skal du medtage de seneste momsafsendelser fra momsgruppemedlemmer ved at vælge handlingen **Medtag gruppemoms**.  

Når momsgruppens momsgruppe er blevet sendt til myndighederne på vegne af hele koncernen, skal du normalt udføre handlingen **Afregn moms**. Handlingen lukker åbne momsposter og overfører købs- og salgsmomsbeløb til momsafregningskontoen. I øjeblikket medtager denne handling ikke gruppeindgangene i gruppen. <!--Has this changed?--> Kun momsposter fra repræsentative momsgrupper bogføres. Beløbene i momsgruppemedarbejderne skal bogføres på MOMS-afregningsbeløbet manuelt, så momsgruppemedarbejders momskonto vil afspejle det ansvar, der er indberettet til myndighederne. Denne funktionsmåde ændres i en kommende opdatering af [!INCLUDE[prod_short](includes/prod_short.md)], så hele gruppemomsen (det samlede beløb på momsreturneringen) udlignes. <!--Has this behavior changed?-->

> [!NOTE]
> Medlemmer af momsgruppen kan rette i afsendte momsmeldinger, så længe gruppens repræsentant ikke har frigivet momsreturværdien for gruppen. Hvis du vil foretage en rettelse, skal momsgruppemedlemmet oprette en ny momsreturnering for momsafleveringsperioden og sende den til den ansvarlige for momsgruppen. Momsgruppens repræsentant vil medtage den seneste momsleverance på siden **Momsreturneringer**. 

> [!IMPORTANT]
> Momsgruppefunktionen understøttes kun på de markeder, hvor [!INCLUDE[prod_short](includes/prod_short.md)], der bruger en momsramme, som består af momsopgørelser og momsreturperioder. Du kan ikke bruge momsgrupper på andre markeder, der har andre implementeringer af lokal momsrapportering, f.eks. Østrig, Tyskland, Italien, Spanien og Schweiz. 

## <a name="see-also"></a>Se også
[Lokal funktionalitet for Storbritannien i den britiske version](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Overførsel af moms digitalt i Storbritannien](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Arbejde med moms af salg og køb](finance-work-with-vat.md)  
[Konfigurere moms](finance-setup-vat.md)  
[Arbejde med moms af salg og køb](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
