---
title: Arbejde med Power BI-rapporter i Business Central| Microsoft Docs
description: 'Få indsigt, business intelligence og KPI''er fra Business Central-data med Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/24/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Arbejde med Power BI-rapporter i [!INCLUDE [prod_short](includes/prod_short.md)]

I denne artikel får du nogle grundlæggende oplysninger om arbejde med rapporter. Dette omfatter visning af Power BI-rapporter i [!INCLUDE [prod_short](includes/prod_short.md)] (herunder scorecards og dashboards) og redigering af Power BI-rapporter, der bruger [!INCLUDE [prod_short](includes/prod_short.md)] som datakilde. I artiklen diskuteres nogle aspekter, som kan hjælpe dig med at komme i gang som [!INCLUDE[prod_short](includes/prod_short.md)]-bruger. Du kan finde generelle retningslinjer og instruktioner i brugen af Power BI i [Power BI-dokumentationen til forbrugerne](/power-bi/consumer).

## Oversigt

Power BI-rapporter giver dig indblik i din [!INCLUDE[prod_short](includes/prod_short.md)]. Forskellige sider i [!INCLUDE [prod_short](includes/prod_short.md)] omfatter en Power BI-del af en rapport, der kan vise Power BI-rapporter. Rollecenteret er en typisk side, hvor du kan se en Power BI-del af rapporten. Nogle listesider som **Elementer** indeholder også en Power BI-del.

[!INCLUDE [prod_short](includes/prod_short.md)] arbejder sammen med Power BI-tjenesten. Rapporter til visning i [!INCLUDE [prod_short](includes/prod_short.md)] gemmes i en Power BI-tjeneste. I [!INCLUDE [prod_short](includes/prod_short.md)] kan du udskifte den rapport, der vises i Power BI-delen, til enhver Power BI-rapport, der er tilgængelig i Power BI-servicen. Første gang, du logger på [!INCLUDE [prod_short](includes/prod_short.md)], og indtil du opretter forbindelse til en Power BI-tjeneste, vil dele være tomme, som vist her:

![Power BI-del i Business Central.](./media/power-bi-part.png)

## Kom i gang

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] online er allerede konfigureret til at blive integreret med Power BI.

### Oprette dig som bruger af Power BI

Før du kan bruge Power BI sammen med [!INCLUDE[prod_short](includes/prod_short.md)], skal du registrere dig som bruger af Power BI-tjenesten. Hvis du ikke allerede har tilmeldt dig, skal du gå til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Når du tilmelder dig, skal du bruge din mailadresse og adgangskode.

Når du har en Power BI-konto, kan du logge på [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

Power BI-tjenesten er vært for alle de rapporter, der er tilgængelige. Hvis du vil se en rapport i dit personlige arbejdsområde, skal du vælge **Mit arbejdsområde** > **Rapporter**. Derefter skal du blot vælge den rapport, du vil have vist. Hvis du har adgang til et eller flere delte Power BI-arbejdsområder, kan du også se rapporter i disse arbejdsområder.

Med [!INCLUDE[prod_short](includes/prod_short.md)] online får du automatisk et sæt standardrapporter i arbejdsområdet. Hvis du vil oprette dine egne rapporter, kan du bruge Power BI Desktop til at oprette rapporter og derefter udgive dem i arbejdsområdet. Du kan finde flere oplysninger i [Introduktion til oprettelse af rapporter i Power BI Desktop for at få vist [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="connect"></a>Tilknyt til Power BI - èn gang

Når du logger på [!INCLUDE [prod_short](includes/prod_short.md)] første gang, får du sandsynligvis vist en tom Power BI-del (som vist i den forrige figur) på forskellige sider. Det første, du skal gøre, er at oprette forbindelse til din Power BI-konto. Når du har oprettet forbindelse, kan du se rapporter. Du behøver kun at udføre dette trin én gang.

1. Vælg linket **Kom i gang med Power BI** i delen **Power BI-rapporter**.
2. Den assisterede opsætning **Opsæt Power BI-rapporter i Business Central** starter. Vælg **Næste** for at fortsætte.
3. På siden **Tjek din Power BI-licens**. Gør ét af følgende:

    - Hvis du ikke har registreret dig som bruger af Power BI endnu, skal du vælge [Gå til Power BI-startside](https://powerbi.microsoft.com). Registrer dig som bruger af konto, gå tilbage til [!INCLUDE[prod_short](includes/prod_short.md)], og fuldfør opsætningen.

    - Hvis du allerede har en licens, skal du vælge **Næste**.
4. På næste side overfører [!INCLUDE[prod_short](includes/prod_short.md)] nu en demo-rapport til Power BI. Dette trin kan tage nogle få minutter, så det gøres i baggrunden. Vælg **Næste** og derefter **Udfør** for at fuldføre opsætningen.

Forbindelsesprocessen starter. Under processen kommunikerer [!INCLUDE [prod_short](includes/prod_short.md)] med Power BI-tjenesten for at afgøre, om du har en gyldig Power BI-konto og -licens. Når licensen er kontrolleret, vises Power BI-standardrapporten på siden. Hvis der ikke vises en rapport, kan du vælge en rapport fra delen.

> [!TIP]
> Med [!INCLUDE [prod_short](includes/prod_short.md)] online overfører dette trin automatisk Power BI-standardrapporter, der er anvendt i [!INCLUDE [prod_short](includes/prod_short.md)], til dit Power BI-arbejdsområde.

<!--#### From [!INCLUDE [prod_short](includes/prod_short.md)] on-premises

Connecting to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] is similar to online. However, you might be prompted on the **MICROSOFT ENTRA SERVICE PERMISSIONS** page to grant access to Power BI Services. To grant access, select **Authorize Azure Services**, and then **Accept**.

Once connected, you can select a report from the Power BI part on pages.-->

## Arbejde med Power BI-rapporter

### Hente de seneste data

Hver Power BI-rapport er baseret på et datasæt, som henter data fra [!INCLUDE[prod_short](includes/prod_short.md)]-kilderne. Du skal være sikker på, at dataene i dine Power BI-rapporter er opdaterede med dataene i [!INCLUDE[prod_short](includes/prod_short.md)]. Dette begreb omtales som *opdatering*.  Afhængigt af, hvordan din organisation har oprettet Power BI, sker opdateringen muligvis ikke automatisk. Du kan opdatere data på to måder: manuelt eller ved at planlægge en opdatering. Manuel opdatering udføres efter behov. Planlagt opdatering giver dig automatisk opdatering med bestemte tidsintervaller.

#### Opdatere manuelt

Fra Power BI online i navigationsruden under **Datasæt** skal du vælge **Flere indstillinger (...)** ud for datasættet, og vælg derefter **Opdater nu**.

#### Planlægge en opdatering

Vælg Flere indstillinger (...) ud for datasættet i navigationsruden fra Power BI online under Datasæt, og vælg derefter **Planlæg opdatering**. Udfyld oplysningerne under **Planlæg opdatering**, og vælg **Anvend**.

Du kan finde flere oplysninger i [Konfigurere planlagt opdatering](/power-bi/connect-data/refresh-scheduled-refresh)

### Vise rapporter på listesider

[!INCLUDE[prod_long](includes/prod_long.md)] indeholder en Power BI-faktaboks på flere nøglelistesider. Denne faktaboks giver ekstra indblik i dataene på listen. Når du flytter mellem rækkerne på listen, opdateres rapporten og filtreres for den valgte post.

Hvis du vil lære, hvordan du opretter rapporter for listesider, skal du se [Oprettelse af Power BI-rapporter til visning af listedata i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

> [!TIP]
> Hvis du ikke kan se Power BI-faktaboksen, kan den være skjult i arbejdsområdet med personlig tilpasning. Vælg ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") Vælg derefter handlingen **Tilpas**. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).
>
> Hvis du har en ældre version af Business central, skal du gå til handlingslinjen, vælge **Handlinger** > **Vis** > **Vis/Skjul Power BI-rapporter**.

### Skifte rapporter

En Power BI-del på en side kan vise alle de Power BI-rapporter, der er tilgængelige for dig. Hvis du vil skifte til at få vist en anden rapport, skal du vælge handlingen **Vælg rapport** på rullelisten over kommandoer øverst i delen.  

På siden **Power BI-rapportvalg** vises en liste over alle de Power BI-rapporter, du har adgang til. Denne liste hentes fra dine arbejdsområder eller arbejdsområder, som du har delt med dig i Power BI.tjenesten. Vælg **Aktivér** for hver enkelt rapport, der skal vises på startsiden, og vælg derefter **OK**. Du vender tilbage til siden, og den sidste rapport, du har aktiveret, vises. Brug kommandoen **Forrige** og **Næste** til at navigere mellem rapporterne på kommandorullelisten.  

### Hente flere rapporter

Hvis der ikke vises nogen rapporter på siden **Power BI-rapportvalg**, eller hvis du ikke kan se den ønskede rapport, skal du vælge **Hent rapporter**. Du kan bruge denne handling til at søge efter rapporter fra to placeringer: *Min organisation* eller fra *Tjenester*.

- Vælg **Min organisation** for at gå til Power BI-tjenesterne. Herfra kan du få vist de rapporter i organisationen, som du har fået tildelt rettigheder til at se. Derefter kan du føje dem til dit arbejdsområde.
- Vælg **Tjenester** for at gå til Microsoft AppSource, hvor du kan installere Power BI-apps.  

> [!TIP]
> Hvis du har Power BI Desktop, kan du også oprette nye Power BI-rapporter. Når disse rapporter er publiceret til dit Power BI-arbejdsområde, vises de på siden **Power BI-rapportvalg**.  

### Administrere og redigere rapporter

Du kan foretage ændringer af en rapport i Power BI-delen. De ændringer, du foretager, publiceres derefter til Power BI-tjenesten. Hvis rapporten deles med andre brugere, kan de også se ændringerne, medmindre du gemmer ændringerne i en ny rapport.

Hvis du vil redigere en rapport, skal du vælge handlingen **Administrer rapport** fra kommandorullelisten i Power BI-delen. Begynd at foretage ændringer. Når du er færdig med at foretage ændringer, skal du vælge **Fil** > **Gem**. Hvis det er en delt rapport, og du ikke vil foretage ændringen for alle brugere, skal du vælge **Gem som** for at undgå at skulle foretage denne ændring for alle brugere.

Når du går tilbage til rollecenteret, vises den opdaterede rapport. Hvis du har brugt **Gem som**, skal du vælge **Vælg rapport** og derefter aktivere den nye rapport for at se den.

> [!NOTE]
> Denne funktion er ikke tilgængelig for [!INCLUDE [prod_short](includes/prod_short.md)] on-premises.

### <a name="upload"></a>Overføre rapporter

Power BI-rapporter kan distribueres blandt brugere som .pbix-filer. Hvis du har nogen .pbix-filer, kan du overføre og dele dem med alle brugere af [!INCLUDE [prod_short](includes/prod_short.md)]. Rapporterne deles inden for hver virksomhed i [!INCLUDE [prod_short](includes/prod_short.md)].  

For at overføre en rapport skal du vælge handlingen **Overfør rapport** fra kommandorullelisten i delen **Power BI-rapporter**. Find derefter den .pbix-fil, der definerer de rapporter, du vil dele. Du kan ændre filens standardnavn.  

Når rapporten overføres til Power BI-arbejdsområdet, overføres den automatisk til andre brugeres Power BI-arbejdsområder.

> [!NOTE]
> Hvis du overfører en rapport via [!INCLUDE[prod_short](includes/prod_short.md)], kræver det, at du har SUPER-brugerrettigheder i [!INCLUDE[prod_short](includes/prod_short.md)]. Du behøver ikke nogen særlig tilladelse for at overføre rapporter til dit arbejdsområde via Power BI-tjenesten.

## <a name="upload"></a>Overføre rapporter fra filer

Power BI-rapporter kan distribueres blandt brugere som .pbix-filer. Hvis du har en .pbix-fil, kan du overføre filen til et arbejdsområde. Benyt følgende fremgangsmåde for at overføre en rapport:

1. Vælg **Hent data** i det nye arbejdsområde .

2. I feltet Filer skal du vælge **Hent**.

3. Vælg **Lokal fil**, gå til det sted, hvor du har gemt filen, og vælg **Åbn**.

Du kan finde flere oplysninger i [Overføre rapporten til tjenesten](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). -->

> [!TIP]
> Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] online, kan du også overføre en rapport inde fra [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Arbejde med Power BI-rapporter i [!INCLUDE [prod_short](includes/prod_short.md)] - Overføre rapporter](across-working-with-powerbi.md#upload).

## <a name="share"></a>Dele rapporter med andre

Når en rapport findes i dit arbejdsområde, kan du dele den med andre i din organisation.

Hvis du vil dele en rapport i en listerapport eller i en åben rapport, skal du vælge **Del**. I ruden **Del rapport** skal du indtaste de fulde mailadresser for de enkeltpersoner eller distributionsgrupper, du vil dele med. Følg instruktionerne på skærmen for at fuldføre delingen. Du kan finde flere oplysninger i [Dele et dashboard eller en rapport](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> Det kræves, at både du og de personer, du deler rapporten med, har [Power BI Pro-licens](/power-bi/service-features-license-type). Ellers skal indholdet skal være i et [Premium-kapacitet](/power-bi/service-premium-what-is). Du kan få flere oplysninger i [Sådan deler du dit arbejde i Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

## Løsning af problemer

Men hvis noget går galt indeholder dette afsnit en løsning til de mest almindelige problemer.  

### Du har ikke en Power BI-konto

Der er ikke blevet oprettet en Power BI-konto. Fo at få en gyldig Power BI-konto skal du have en licens, og du skal tidligere have været logget på Power BI for at kunne oprette et Power BI-arbejdsområde.

### Meddelelse: Der er ingen aktiverede rapporter. Vælg Vælg rapport for at få vist en oversigt over de rapporter, du kan få vist.

Denne meddelelse vises, hvis standardrapporten ikke blev implementeret i Power BI-arbejdsområdet. Eller den blev installeret, men blev ikke opdateret korrekt. Gå til rapporten i dit Power BI-arbejdsområde, vælg **Datasæt**, **Indstillinger**, og opdater derefter legitimationsoplysningerne manuelt. Når datasættet er opdateret, skal du gå tilbage til [!INCLUDE[prod_short](includes/prod_short.md)] og vælge rapporten manuelt på siden **Vælg rapporter**.

#### Du kan ikke se en rapport på siden Vælg rapport på en listeside

Det skyldes sandsynligvis, at rapportens navn ikke indeholder navnet på listesiden. Ryd filteret for at se en komplet liste over tilgængelige Power BI-rapporter.

## Se også

[Business Central og Power BI](admin-powerbi.md)    
[Oprette Power BI-rapporter, der viser [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md)    
Oversigt over [Power BI-integrationskomponent og -arkitektur for [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)    
[Opret forbindelse til Power BI fra [!INCLUDE [prod_short](includes/prod_short.md)] i det lokale miljø](across-working-with-business-central-in-powerbi.md)    
[Power BI til forbrugere](/power-bi/consumer/end-user-consumer)     
[Det 'nye udseende' for Power BI-tjenesten](/power-bi/service-new-look)    
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)    
[Power BI-dokumentation](/power-bi/)    
[Business Intelligence](bi.md)    
[Bliv klar til at handle](ui-get-ready-business.md)    
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)    
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)    
[Brug [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerapps.md)    
[Brug af [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)    
[Brug [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
