---
title: Aktivere virksomhedens data til Power BI| Microsoft Docs
description: Du kan nemt få indsigt, business intelligence og nøgletal i dine Business Central-data med Business Central-apps for Power BI.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: 0750f1724260eb7767757d947f30dcb074ef1aeb
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879102"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivere virksomhedens data til Power BI

Du kan nemt få indsigt i dine [!INCLUDE[prodshort](includes/prodshort.md)]-data med [!INCLUDE[prodshort](includes/prodshort.md)] apps til Power BI. Power BI henter dine data og opretter derefter et out-of-the-box dashboard og rapporter baseret på dataene.  

Du skal have en gyldig konto til [!INCLUDE[prodshort](includes/prodshort.md)] og til Power BI. Desuden skal du hente [Power BI Desktop](https://powerbi.microsoft.com/desktop/), hvis du vil oprette dine egne Power BI rapporter. Power BI apss kræver tilladelser til de tabeller, hvor data hentes fra. Yderligere oplysninger om kravene beskrives nedenfor.  

> [!IMPORTANT]
> Apps Power BI, der er beskrevet i denne artikel, er designet til at bruge Azure Active Directory som godkendelsesmetode, medmindre andet er angivet. Hvis du vil installere en Power BI-app, skal du også have en Power BI Pro-licens.  Når Power BI-appen er installeret, kan den deles med brugere med en hvilken som helst licenstype.

[!INCLUDE [prodlong](includes/prodlong.md)] har udgivet følgende apps til Power BI:

- [!INCLUDE [prodlong](includes/prodlong.md)] - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Sales  
- [!INCLUDE [prodlong](includes/prodlong.md)](i det lokale miljø) – CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)](i det lokale miljø) – Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)](i det lokale miljø) – Sales  

## <a name="using-the-include-prodshortincludesprodshortmd-dashboards-in-power-bi"></a>Brug af [!INCLUDE [prodshort](includes/prodshort.md)] dashboards i Power BI

Hver app indeholder rapporter, som du kan dykke ned i:

- Vælg en visualisering på dashboardet for at få vist en af de underliggende rapporter.  
- Filtrer rapporten, eller tilføj felter, du vil overvåge.  
- Fastgør denne brugerdefinerede visning til dashboardet for fortsat sporing.  
  Du kan opdatere dataene manuelt, og kan du oprette en tidsplan for opdatering. Du kan finde flere oplysninger i [Konfiguration af planlagt opdatering](/power-bi/refresh-scheduled-refresh).  

Apps er designet til at arbejde med data fra alle de virksomheder, du har i din [!INCLUDE[prodshort](includes/prodshort.md)]. Når du installerer Power BI-app'en, angiver du en eller flere parametre for at oprette forbindelse til din [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> Du kan også oprette dine egne rapporter og dashboards i Power BI baseret på dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Du kan finde flere oplysninger under [Forbinde dine virksomhedsdata med Power BI](across-how-use-financials-data-source-powerbi.md).  

### <a name="to-connect-your-data-in-power-bi"></a>Sådan tilsluttes dinen data i Power BI

1. Åbn browseren, gå til https://powerbi.microsoft.com, og log på din konto.
2. Vælg **Hent data** nederst i venstre navigationsrude.  

    ![Navigere til Hent data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Du kan også komme i gang inde fra [!INCLUDE [prodshort](includes/prodshort.md)]. Naviger til **Rapportvalg** i afsnittet Power BI fra startsiden. Vælg enten **Service** eller **Min virksomhed** på båndet. Hvis en af disse handlinger er markeret, åbnes enten galleriet Organisation i Power BI eller i Microsoft AppSource, som også bliver filtreret, så det kun viser apps, der er relateret til [!INCLUDE[prodshort](includes/prodshort.md)].

3. I feltet **Tjenester** skal du vælge **Hent**. Dette vil åbne en side, der viser **AppSource**- og **-apps til Power BI**.  

<!--    ![Choose apps from online services that you use.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)-->
4. Vælg **Apps** under fanen **Apps for Power BI**, vælg den **Microsoft Dynamics 365 Business Central**-app, du ønsker at bruge, og vælg derpå **Hent nu**.  
<!--    ![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packspowerbi-dynamics365-for-financials-get-it-now.png)/-->
5. Når du bliver bedt om det, skal du angive navnet på det miljø og den virksomhed i din [!INCLUDE[prodshort](includes/prodshort.md)]-app, som du vil oprette forbindelse til. Hvis du ikke har oprettet flere miljøer, skal du angive **Produktion**. Ved virksomhedsparameteren skal du sørge for at indtaste navnet og ikke visningsnavnet. Virksomhedsnavnet findes på siden **Virksomheder** i din [!INCLUDE[prodshort](includes/prodshort.md)]-forekomst.  

    > [!NOTE]
    > Hvis du opretter forbindelse til [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, skal du angive parameteren for *Webtjeneste-URL*. Find dette på siden **Webtjeneste** i [!INCLUDE [prodshort](includes/prodshort.md)]. Din [!INCLUDE [server](includes/server.md)]-forekomst skal være konfigureret til basisgodkendelse, og du skal angive en bruger og denne brugers web-adgangsnøgle som deres adgangskode. I følgende eksempel skal du erstatte *myserver:7048* med dit [!INCLUDE [server](includes/server.md)] navn og *CRONUS%20OS* med dit firmanavn.  
    > ```https://myserver:7048/BC140/ODataV4/Company('CRONUS%20US')/```

6. Når forbindelsen er oprettet, føjes der et dashboard og rapporter til dit Power BI-arbejdsområde. Når dette er fuldført, viser felterne data fra din [!INCLUDE[prodshort](includes/prodshort.md)]-virksomhed.

    ![Vælg Dynamics 365 Business Central, og vælg Hent nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

### <a name="what-now"></a>Hvad nu?

- Prøv [at stille et spørgsmål i feltet Spørgsmål og svar](/power-bi/service-q-and-a-tips) øverst i dashboardet.
- [Ændre felterne](/power-bi/service-dashboard-edit-tile) i dashboardet.  
- [Vælg et felt](/power-bi/service-dashboard-tiles) for at åbne den underliggende rapport.  
- Som standard er dit datasæt ikke planlagt til opdatering. Du kan ændre tidsplanen for opdatering eller prøve at opdatere det efter behov ved hjælp af **Opdater nu**. Du kan finde flere oplysninger i [Konfiguration af planlagt opdatering](/power-bi/refresh-scheduled-refresh).

## <a name="power-bi-in-include-prodshortincludesprodshortmd"></a>Power BI i [!INCLUDE [prodshort](includes/prodshort.md)]

Din startside i [!INCLUDE [prodshort](includes/prodshort.md)] kan indeholde et Power BI-kontrolelement, der kan konfigureres til at vise Power BI-rapporter på din startside.

> [!IMPORTANT]
> Du skal have en gyldig konto til [!INCLUDE [prodshort](includes/prodshort.md)] og til Power BI. Hvis du vil ændre rapporter, skal du også hente Power BI Desktop. Du kan finde flere oplysninger i [Bruge Business Central som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md).  

### <a name="on-first-login"></a>Ved første logon

Når du logger på [!INCLUDE [prodshort](includes/prodshort.md)]første gang, vil du bemærke et tomt Power BI-sted på startsiden. Hvis du vil have vist rapporterne, skal du først oprette forbindelse til Power BI ved at vælge linket til *Kom i gang med Power BI*.

[!INCLUDE [prodshort](includes/prodshort.md)] kommunikerer derefter med Power BI-tjenesten for at finde ud af, om du har en gyldig Power BI-konto. Når licensen er kontrolleret, vises standard-Power BI-rapporterne på startsiden.

### <a name="selecting-power-bi-reports"></a>Valg af Power BI rapporter

Power BI-kontrolelementet på startsiden kan vise alle Power BI-rapporter. Hvis du vil have vist en eksisterende rapport, skal du vælge handlingen **Vælg rapport** fra Power BI kommandorullelisten.  

På siden rapporter vises en liste over alle de Power BI-rapporter, du har adgang til. Denne liste hentes fra Power BI-arbejdsområdet. Aktivér hver enkelt rapport, der skal vises på startsiden, og vælg derefter OK. Du vender tilbage til din startside, og den sidste rapport, du har aktiveret, vises. Brug kommandoen forrige og næste til at navigere mellem rapporterne med kommandorullelisten.  

### <a name="get-reports"></a>Hent rapporter

Hvis der ikke vises nogen rapporter på siden Vælg rapporter, eller hvis du ikke kan se den ønskede rapport. Du kan vælge at hente rapporter fra *Min organisation* eller fra *Tjenester*.
Vælg *Min organisation* for at gå til de Power BI-tjenester, hvor du kan få vist de rapporter i organisationen, som du har rettigheder til at få vist, og føje til dit arbejdsområde. Vælg *Tjenester* for at gå til Microsoft AppSource, hvor du kan installere Power BI-apps.  

Du kan også vælge at oprette nye Power BI-rapporter. Når disse rapporter er publiceret til dit Power BI-arbejdsområde, vises de på denne side.  

### <a name="managing-reports"></a>Administration af rapporter

I afsnittet Power BI på startsiden kan du vælge handlingen **Administrer rapporter** på kommandorullelisten, så du kan ændre den rapport, der var i fokus i rollecenteret.  

Du kan foretage ændringer af rapporten og gemme den.  Alle ændringer, der foretages i rapporten, ændres for alle brugere, som denne rapport er delt med, eftersom du ændrer den rapport, der er gemt i Power BI-tjenesten.  

Når du har udført ændringerne, skal du vælge Gem. Hvis det er en delt rapport, ønsker du måske at vælge Gem som for at undgå at foretage denne ændring for alle brugere.
Gå tilbage til rollecenteret, hvorefter den opdaterede rapport vises. Hvis du brugte kommandoen Gem som, skal du åbne siden Vælg rapport og aktivere den nye rapport.

### <a name="uploading-reports"></a>Overførsel af rapporter

Du kan overføre nye Power BI rapporter og dele dem med alle brugere af [!INCLUDE [prodshort](includes/prodshort.md)]. Rapporterne deles inden for hver virksomhed i [!INCLUDE [prodshort](includes/prodshort.md)].  

For at overføre en rapport skal du vælge handlingen **Overfør rapport** fra kommandorullelisten. Du kan derefter overføre en. pbix-fil, der definerer de rapporter, du vil dele. Du kan ændre filens standardnavn.  

Når rapporten er blevet overført til dit Power BI-arbejdsområde, overføres den automatisk til Power BI-arbejdsområderne for alle andre brugere i virksomheden, næste gang de logger på [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="system-requirements"></a>Systemkrav

Hvis du vil importere dine [!INCLUDE[prodshort](includes/prodshort.md)]-data i Power BI, skal du have rettigheder til de webtjenester, der bruges til at hente data. De webtjenester, der er nødvendige for hver Power BI-app, omfatter:

### <a name="microsoft-dynamics-365-business-central--crm"></a>Microsoft Dynamics 365 Business Central – CRM

- Salgsmuligheder
- Vis virksomhedsoplysninger i Excel-skabelon
- Power BI-rapportetiketter

### <a name="microsoft-dynamics-365-business-central--finance"></a>Microsoft Dynamics 365 Business Central – Finance

- PowerBIFinance
- Vis virksomhedsoplysninger i Excel-skabelon
- Power BI-rapportetiketter

### <a name="microsoft-dynamics-365-business-central---sales"></a>Microsoft Dynamics 365 Business Central - Sales

- Varestatistik efter kunde
- Salgsdashboard
- Vis virksomhed i Excel-skabelon
- Power BI-rapportetiketter

> [!NOTE]
> [!INCLUDE [prodshort](includes/prodshort.md)] On-Premises bruger samme webtjeneste-slutpunkter som [!INCLUDE [prodshort](includes/prodshort.md)] online.

## <a name="web-services"></a>Webtjeneste

En nem måde at finde webtjenesterne på er at søge efter *webtjenester* i [!INCLUDE[prodshort](includes/prodshort.md)]. På siden **Webtjenester** skal du sørge for, at feltet **Udgiv** er markeret for de webtjenester, der er angivet ovenfor.

## <a name="troubleshooting"></a>Fejlfinding

Power BI-dashboardet er baseret på de publicerede webtjenester, der er anført ovenfor, og viser data fra demoregnskabet eller dit eget regnskab, hvis du indlæser data fra dit aktuelle økonomisystem. Men hvis noget går galt indeholder dette afsnit en løsning til de mest almindelige problemer.  

### <a name="you-do-not-have-a-power-bi-account"></a>Du har ikke en Power BI-konto

Der er ikke blevet oprettet en Power BI-konto. Fo at have en gyldig Power BI-konto skal du have en licens, og du skal tidligere have været logget på Power BI, for at Power BI-arbejdsområdet er blevet oprettet.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Meddelelse: Der er ingen aktiverede rapporter. Vælg Vælg rapport for at få vist en oversigt over de rapporter, du kan få vist.

Denne meddelelse vises, hvis standardrapporten ikke er blevet implementeret i Power BI-arbejdsområdet, eller hvis rapporten blev installeret, men ikke er blevet opdateret. Hvis dette sker, skal du gå til rapporten i dit Power BI-arbejdsområde, vælge **Datasæt**, **Indstillinger** og derefter manuelt opdatere legitimationsoplysningerne. Når datasættet er opdateret, skal du gå tilbage til Business Central og vælge rapporten manuelt på siden **Vælg rapporter**. 

### <a name="you-need-a-power-bi-pro-license-to-install-the-include-prodshortincludesprodshortmd-app-in-power-bi"></a>Du skal have Power BI-en Pro-licens for at kunne installere [!INCLUDE [prodshort](includes/prodshort.md)]-appen i Power BI

Power BI-apps kan kun installeres af brugere, der har en Power BI-Pro-licens. Når Power BI-appen er installeret, kan du dele den med brugere, der ikke har en Power BI-Pro-licens.  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>"Parametervalideringen mislykkedes, kontrollér, at alle parametre er gyldige"

Denne fejl angiver, at en eller flere af parametrene er ugyldige.

- Den angivne miljøparameter passer ikke til noget eksisterende [!INCLUDE [prodshort](includes/prodshort.md)]-produktions- eller sandkassemiljø. 
- Den angivne virksomhedsparameter passer ikke til nogen eksisterende [!INCLUDE [prodshort](includes/prodshort.md)]-virksomheder Kontrollér virksomhedsnavnet på siden **Virksomheder** i [!INCLUDE [prodshort](includes/prodshort.md)]
- Hvis der oprettes forbindelse til [!INCLUDE [prodshort](includes/prodshort.md)] on-premises. du har angivet en ugyldig URL-adresse. Du kan kontrollere URL-adressen på siden **Webtjeneste** i [!INCLUDE [prodshort](includes/prodshort.md)]  
- En port er ikke åben, så anmodningen kan passere gennem firewall'en.

### <a name="login-failed"></a>Logon mislykkedes

Hvis fejlmeddelelsen "Logon mislykkedes" vises, efter at du har brugt dine legitimationsoplysninger til [!INCLUDE [prodshort](includes/prodshort.md)] til at logge på, kan det skyldes en af følgende situationer:

- Den konto, du bruger, har ikke rettigheder til at hente [!INCLUDE [prodshort](includes/prodshort.md)]-data fra din konto. Kontrollér, at du har tilladelse til de nødvendige data i [!INCLUDE [prodshort](includes/prodshort.md)], og prøv igen.
- Du har valgt en anden godkendelsestype end basis, hvis der oprettes forbindelse til [!INCLUDE [prodshort](includes/prodshort.md)] on-premises.
- Du har ikke angivet et gyldigt brugernavn eller en gyldig adgangskode.

### <a name="incorrect-company-name"></a>Forkert virksomhedsnavn

Det er en normal fejl at angive fælles virksomhedens visningsnavn i stedet for navnet på virksomheden. Du kan finde navnet på virksomheden ved at søge efter **virksomheder**. Brug derefter feltet **Navn**, når du angiver navnet på virksomheden.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Nøglen svarer ikke til nogen rækker i tabellen

Hvis du angiver et ikke gyldigt firmanavn under oprettelsen af forbindelsen, kan du få vist meddelelsen "Nøglen svarer ikke nogen rækker i tabellen". Angiv det korrekte firmanavn, og forsøg igen.

### <a name="historical-data-appears-to-be-missing"></a>Der mangler tilsyneladende historiske data

Når Power BI-appen er installeret, og dine data vises i Power BI, bemærker du måske, at du ikke kan se alle dine data. Datasættene er filtrerede til kun at returnere de tidligere 365 dages data. Denne standard er på plads for at gøre det hurtigere at lave rapporterne.  

### <a name="i-only-see-data-for-a-single-company"></a>Jeg kan kun se data for en enkelt virksomhed

Power BI-appen viser kun data fra den [!INCLUDE [prodshort](includes/prodshort.md)]-virksomhed, der blev defineret, da Power BI-appen blev installeret. Du kan føje data fra yderligere virksomheder til rapporterne ved at tilføje nye forespørgsler, der bruger forskellige virksomheder som datakilde.  

## <a name="see-also"></a>Se også

[Power BI for forbrugere](/power-bi/consumer/end-user-consumer)  
[Power BI-tjenestens nye udseende](/power-bi/service-new-look)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentation](/power-bi/)  
[Business Intelligence](bi.md)  
[Introduktion](product-get-started.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Brug [!INCLUDE[d365fin](includes/d365fin_md.md)] som en Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
