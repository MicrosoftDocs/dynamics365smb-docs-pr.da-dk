---
title: Udvidelsen til momsgruppestyring | Microsoft Docs
description: Du kan handle med andre virksomheder for at danne en momsgruppe og enten være medlem eller en repræsentant for gruppen, når du indberetter moms.
author: bholtorf
manager: annbe
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: VAT, value added tax, report
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: ebe3c8748da04a2552f8f3d10967303459ba23c4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757038"
---
# <a name="the-vat-group-management-extension"></a>Udvidelsen til momsgruppestyring

Du kan forbinde en eller flere virksomheder i dit land for at konsolidere momsrapporteringen under et enkelt registreringsnummer. Denne type arrangement er kendt som en *momsgruppe*. Du kan deltage i gruppen som medlem eller gruppens repræsentant.

## <a name="forming-a-vat-group"></a>Danner en momsgruppe
Medlemmer af momsgruppen og grupperepræsentanten kan bruge **Opsætning af den assisterede opsætning af momsgruppe styring** til at definere deres ansættelse med gruppen og oprette en forbindelse mellem deres [!INCLUDE[prod_short](includes/prod_short.md)]-lejere. Gruppemedlemmerne bruger forbindelsen til at sende deres moms tilbage til gruppens repræsentant. Repræsentanten sender moms til skattemyndighederne på koncernens vegne ved hjælp af en enkelt moms Returvare. 

## <a name="vat-group-constellations"></a>Momsgruppe-konstellationer
Kommunikation sker fra gruppemedlemmer til repræsentanten. Grupperepræsentanten udviser et API, som gør det muligt for medlemmerne at sende deres moms tilbage til momsgruppens repræsentant. 
[!INCLUDE[prod_short](includes/prod_short.md)] understøtter indleveringer på tværs af grupper til virksomheder [!INCLUDE[prod_short](includes/prod_short.md)], der bruger lokalt eller online, og i enhver kombination. Opsætningen af kommunikationen afhænger af konstellationen. I følgende afsnit beskrives, hvordan du kan oprette forskellige gruppekonstellationer.

Følgende liste viser den anbefalede rækkefølge for trinene til oprettelse af en momsgruppe:

1. Opret den nye momsopsætning i Azure Active Directory. Du kan finde flere oplysninger i [Krav til godkendelse](ui-extensions-vat-group.md#requirements-for-authentication).
2. Dele de tekniske oplysninger, som momsgruppe medlemmerne og repræsentanten skal bruge for at tilslutte deres [!INCLUDE[prod_short](includes/prod_short.md)]-leje. Momsgrupperepræsentanten har som regel disse oplysninger, f. eks. navnet på den momsgruppe, som medlemmerne af MOMS-gruppen skal indsende moms til.
3. Oprette brugere i momsgruppens repræsentanters [!INCLUDE[prod_short](includes/prod_short.md)], at momsgruppemedlemmerne kan bruge til at godkende og oprette forbindelse.
4. Kør guiden **Konfigurer momsgruppestyring** for at forbinde medlemmerne af momsgruppen.

  Guiden kræver nogle oplysninger fra den ansvarlige momsgruppe. Du kan finde flere oplysninger i afsnittet [Opsætning af momsgruppemedlem](#vat-group-member-setup). Noter **gruppemedlems-id** for hvert momsgruppemedlem. Repræsentanten skal bruge disse id'er for at føje regnskaberne til momsgruppen.
5. Du kan konfigurere udvidelsen af momsgruppe styringen i moms gruppens repræsentant [!INCLUDE[prod_short](includes/prod_short.md)] vha vejledningen **Opsætning af momsgruppestyring**. 

> [!NOTE]
> Hvis du vil oprette forbindelse til momsgruppens repræsentant, skal gruppemedlemmerne bruge en bruger med adgang til momsgruppens repræsentants [!INCLUDE[prod_short](includes/prod_short.md)]. Repræsentanten for momsgruppen skal imidlertid oprette mindst én bruger af sikkerhedsmæssige årsager. Det anbefales dog, at du opretter en bruger for hvert momsgruppemedlem. Sørg for at distribuere legitimationsoplysningerne for disse brugere til momsgruppemedlemmer på en sikker måde.

## <a name="understanding-the-vat-group-management-setup"></a>Forståelse af opsætning af momsgruppestyring

Repræsentanten for momsgruppen udviser et API, som momsgruppe medlemmerne kan bruge til at oprette forbindelse til deres [!INCLUDE[prod_short](includes/prod_short.md)]-lejer og sende moms tilbage. Medlemmerne af momsgruppen vil ofte bruge [!INCLUDE[prod_short](includes/prod_short.md)] i separate Azure Active Directory-lejer. Derfor skal mere opsætning være nødvendig, hvis der skal oprettes forbindelse mellem momsgruppemedlemmet og repræsentantens [!INCLUDE[prod_short](includes/prod_short.md)]. 
  
Medlemmerne af momsgruppen tilkobler repræsentanten ved at kalde en webtjeneste på den sælger ansvarlige for momsgruppen. Brugeren skal godkendes ved brug af OAuth. Når udvidelsen til momsgruppestyring er sat op, bliver du bedt om at godkende momsgruppens repræsentant for at hente og gemme en adgangstoken. Dette adgangstoken bruges ved afsendelse af moms tilbage til momsgruppens repræsentant. 

Godkendelse håndteres af Azure Active Directory, så du skal oprette forbindelse i momsgruppens repræsentant Azure Active Directory for at tillade forbindelser. En Azure Active Directory-appregistrering skal konfigureres med adgang til momsgruppens repræsentant [!INCLUDE[prod_short](includes/prod_short.md)]. Dette gælder også, hvis repræsentanten for momsgruppen bruger [!INCLUDE[prod_short](includes/prod_short.md)] on-premises. Derudover skal du konfigurere Single Sign-on, hvis den ansvarlige momsgruppe bruger [!INCLUDE[prod_short](includes/prod_short.md)] on-premises.

> [!NOTE]
> I en begrænset periode understøttes også godkendelse vha. webtjenesteadgangsnøgle. Du kan finde flere oplysninger i [Frarådede funktioner i 2021 release wave 1](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#deprecated-features-in-2021-release-wave-1).

## <a name="requirements-for-authentication"></a>Krav til godkendelse 
Når repræsentanten for momsgruppen bruger [!INCLUDE[prod_short](includes/prod_short.md)] online eller on-premises, bruger momsgruppemedlemmerne Azure Active Directory til at godkende, når de sender momsreturvarer til den ansvarlige momsgruppe. Hvis medlemmerne af momsgruppen også bruger [!INCLUDE[prod_short](includes/prod_short.md)] online, kan medlemmet af momsgruppen godkende vha. de angivne legitimationsoplysninger og slutpunktoplysningerne. Du kan finde flere oplysninger i afsnittet [Opsætning af momsgruppemedlem](ui-extensions-vat-group.md#vat-group-member-setup).

Medlemmer af momsgruppe, der har [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, skal konfigurere en app-registrering i Azure Active Directory for momsgruppemedarbejderens [!INCLUDE[prod_short](includes/prod_short.md)]-lejer. App-registreringen gør det muligt for momsgruppens repræsentants [!INCLUDE[prod_short](includes/prod_short.md)] online at godkende Gruppemedlemmet. Du kan finde flere oplysninger om registrering af et program i [Hurtig start: Registrere et program på Microsoft-identitetsplatformen](/azure/active-directory/develop/quickstart-register-app).

Når du opretter app-registreringen i Azure Active Directory, skal du angive følgende.

* I afsnittet **Godkendelse** tilføjes **Web** som platform, og følgende **URL-adresse til omdirigering**: https://businesscentral.dynamics.com/OAuthLanding.htm bruges.
* Afsnittet **Godkendelse** i indstillingen til at vælge **Understøttede kontotyper** skal du vælge **Konti i en hvilken som helst organisations mappe (vilkårlig Azure AD-mappe - multi lejer)**.
* Opret en ny klienthemmelighed, og læg mærke til værdien i sektionen **Certifikater & hemmeligheder**. Momsgruppemedlemmerne skal bruge hemmeligheden, når de konfigurerer forbindelsen til gruppens repræsentant.
* Tilføj tilladelser i afsnittet **API-tilladelser** [!INCLUDE[prod_short](includes/prod_short.md)]. Aktivér uddelegeret adgang til **Financials.ReadWrite.All** og **user_impersonation**.
* I afsnittet **Oversigt** bemærkes **Program-id (klient)**. Momsgruppemedlemmerne skal bruge id, når de konfigurerer forbindelsen til gruppens repræsentant. 

## <a name="vat-group-member-setup"></a>Opsætning af momsgruppemedlem
Konfigurer momsgruppemedlem ved at starte med Kør guiden **Konfigurer momsgruppestyring**. 

> [!NOTE]
> Før du begynder, skal du kontakte momsgruppesælgeren for at få følgende oplysninger om deres [!INCLUDE[prod_short](includes/prod_short.md)]-lejer:
>
> * API URL
> * Navn på virksomheden 
> * Klient-id
> * Klienthemmelighed
> * Logonoplysninger til den dedikerede bruger 

1. Hvis du vil definere virksomhedens momsgruppe rolle, skal du vælge **Medlem** og derefter vælge **Næste**.
2. Kopier værdien i feltet **Gruppemedlems-id**, og del det med momsgruppens repræsentant, så de kan tilføje din virksomhed som godkendt medlem af gruppen.
3. Tilføj **API URL-adressen** fra momsgrupperepræsentanten. Normalt er URL-adressen formateret på følgende måde: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Eksempel `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`. 
4. Tilføj [!INCLUDE[prod_short](includes/prod_short.md)]-firmanavnet for momsgrupperepræsentanten, f. eks *CRONUS.UK Ltd*.
5. Vælg **Godkendelsestype**, vælg **OAuth2** og vælg derefter **Næste**.
6. Angiv det id, som repræsentanten for momsgruppen har opgivet, i feltet **Klient-id**.
7. Indtast den hemmelighed, som repræsentanten for momsgruppen har stillet til rådighed, i feltet **repræsentant for momsgruppe**.
8. I **feltet OAuth 2,0 Authority Endpoint**-feltet skal du angive *https://login.microsoftonline.com/common/oauth2*.
9. I feltet **OAuth 2,0 Resource URL** skal du angive *https://api.businesscentral.dynamics.com/*.
10. I feltet **OAuth 2,0 Redirect URL** skal du angive *https://businesscentral.dynamics.com/OAuthLanding.htm*. 
11. Når du har angivet de forskellige felter, skal du vælge **Næste** og derefter angive de brugerlegitimationsoplysninger, som repræsentanten for momsgruppen har stillet til rådighed.
12. Vælg den momsrapport konfiguration, som du kan bruge til at rapportere moms til myndigheder i dit land.

  I Storbritannien vil konfigurationen af momsrapporten f. eks. blive indstillet til at rapportere moms til HMRC. Momsgruppe styrings udvidelsen kopierer denne opsætning, men erstatter codeunit for indsendelse med en, der understøtter afsendelse til momsgruppens repræsentant snarere end skattemyndighederne. Codeunit leveres af Microsoft. Vælg **Næste**, når du er færdig.

## <a name="using-the-vat-group-management-features"></a>Bruge funktionerne til momsgruppestyring

Medlemmer af momsgruppen bruger standardprocesserne til at oprette momsreturneringer. Den eneste forskel er at vælge rapportversionen **MOMSGRUPPE**, som sender momsen tilbage til momsgruppens repræsentant i stedet for myndighederne. Du kan finde flere oplysninger i [Om rapporten Momsopgørelse](finance-how-report-vat.md#about-the-vat-return-report).

I følgende afsnit beskrives de opgaver, som momsgrupperepræsentanter skal udføre.

### <a name="vat-group-submissions"></a>Indsendelser til momsgruppe

På siden **Momsgruppemeddelser** vises momsreturneringer, som medlemmerne har indsendt. Siden tjener som en kladde placering til indsendelserne, indtil repræsentanten for momsgruppen medtager dem i en momsreturnering for gruppen. Du kan åbne indsendelserne for at gennemgå momsen for de enkelte felter, der er rapporteret af momsgruppemedlemmet.

### <a name="creating-a-group-vat-return"></a>Oprette en gruppemomsretur

Hvis du vil rapportere moms på vegne af gruppen, skal du kun oprette en momsreturnering til virksomheden på siden **momsreturneringer**. Derefter skal du medtage de seneste momsafsendelser fra momsgruppemedlemmer ved at vælge handlingen **Medtag gruppemoms**.  

Når moms gruppens momsgruppe er blevet sendt til myndighederne på vegne af hele koncernen, skal du normalt udføre handlingen **Afregn moms**. Handlingen lukker åbne momsposter og overfører købs- og salgsmomsbeløb til momsafregningskontoen. I øjeblikket medtager denne handling ikke gruppeindgangene i gruppen. Det betyder, at det kun er momsposter fra repræsentative momsgrupper, der bogføres. Beløbene i momsgruppe medarbejderne skal bogføres på MOMS-afregningsbeløbet manuelt, så momsgruppemedarbejders momskonto vil afspejle det ansvar, der er indberettet til myndighederne. Denne funktionsmåde ændres i en kommende opdatering af [!INCLUDE[prod_short](includes/prod_short.md)], så hele gruppemomsen (det samlede beløb på momsreturneringen) udlignes. 

> [!NOTE]
> Medlemmer af momsgruppen kan rette i afsendte momsmeldinger, så længe gruppens repræsentant ikke har frigivet momsreturværdien for gruppen. Hvis du vil foretage en rettelse, skal momsgruppemedlemmet oprette en ny momsreturnering for momsafleveringsperioden og sende den til den ansvarlige for momsgruppen. Momsgruppens repræsentant vil medtage den seneste momsleverance på siden **Momsreturneringer**. 

## <a name="see-also"></a>Se også
[Arbejde med moms af salg og køb](finance-work-with-vat.md)  
[Konfigurere moms](finance-setup-vat.md)
