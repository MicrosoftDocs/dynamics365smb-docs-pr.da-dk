---
title: Arbejde med Power BI-rapporter i Business Central| Microsoft Docs
description: Du kan nemt få indsigt, business intelligence og nøgletal i dine Business Central-data med Business Central-apps for Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 28e332137346aae320b73c326bb3a41d3b7e7097
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927193"
---
# <a name="working-with-power-bi-reports-in-prodshort"></a>Arbejde med Power BI-rapporter i [!INCLUDE [prodshort](includes/prodshort.md)]

I denne artikel får du nogle grundlæggende oplysninger om visning af Power BI-rapporter i [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="overview"></a>Oversigt

Power BI-rapporter giver dig indblik i din [!INCLUDE[prodshort](includes/prodshort.md)]. Forskellige sider i [!INCLUDE [prodshort](includes/prodshort.md)] omfatter en Power BI-del af en rapport, der kan vise Power BI-rapporter. Rollecenteret er en typisk side, hvor du kan se en Power BI-del af rapporten. Nogle listesider som **Elementer** indeholder også en Power BI-del.

[!INCLUDE [prodshort](includes/prodshort.md)] arbejder sammen med Power BI-tjenesten. Rapporter til visning i [!INCLUDE [prodshort](includes/prodshort.md)] gemmes i en Power BI-tjeneste. I [!INCLUDE [prodshort](includes/prodshort.md)] kan du udskifte den rapport, der vises i Power BI-delen, til enhver Power BI-rapport, der er tilgængelig i Power BI-servicen. Første gang, du logger på [!INCLUDE [prodshort](includes/prodshort.md)], og indtil du opretter forbindelse til en Power BI-tjeneste, vil dele være tomme, som vist her:

![Power BI-del i Business Central](./media/power-bi-part.png)

## <a name="prerequisites"></a>Forudsætninger

Hvis du bruger [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, skal det aktiveres til Power BI-integration. Denne opgave udføres typisk af en administrator. Du kan finde flere oplysninger i [Konfigurere [!INCLUDE[prodshort](includes/prodshort.md)] on-premises til Power BI-integration](admin-powerbi-setup.md#setup).

> [!NOTE]
> [!INCLUDE[prodshort](includes/prodshort.md)] online er allerede konfigureret til at blive integreret med Power BI.

## <a name="get-ready"></a>Gør dig klar

Tilmeld dig Power BI-tjenesten. Hvis du ikke allerede har tilmeldt dig, skal du gå til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Når du tilmelder dig, skal du bruge din mailadresse og adgangskode.

## <a name="connect-to-power-bi---one-time-only"></a>Kun oprette forbindelse til Power BI én gang

Når du første gang logger på [!INCLUDE [prodshort](includes/prodshort.md)], kan du få vist en tom Power BI-del på en side, som vist i det forrige billede. Det første, du skal gøre, er at oprette forbindelse til din Power BI-konto. Når du har oprettet forbindelse, kan du se rapporter. Du behøver kun at udføre dette trin én gang.

Hvis du vil oprette forbindelse til Power BI, skal du vælge linket **Kom i gang med Power BI** i **Power BI-rapporter**-delen.

Under tilslutningsprocessen kommunikerer [!INCLUDE [prodshort](includes/prodshort.md)] med Power BI-tjenesten for at afgøre, om du har en gyldig Power BI-konto og -licens. Når licensen er kontrolleret, vises Power BI-standardrapporten på siden. Hvis der ikke vises en rapport, kan du vælge en rapport fra delen.

> [!TIP]
> Med [!INCLUDE [prodshort](includes/prodshort.md)] online overfører dette trin automatisk Power BI-standardrapporter, der er anvendt i [!INCLUDE [prodshort](includes/prodshort.md)], til dit Power BI-arbejdsområde.

##### <a name="from-prodshort-on-premises"></a>Fra [!INCLUDE [prodshort](includes/prodshort.md)] on-premises

Oprettelse af forbindelse til Power BI fra [!INCLUDE [prodshort](includes/prodshort.md)] ligner online. Du vil dog på siden **AZURE ACTIVE DIRECTORY-TJENESTETILLADELSER** blive bedt om at give adgang til Power BI-tjenester. Hvis du vil tildele adgang, skal du vælge **Godkend Azure-tjenester** og derefter **Acceptér**.

Når forbindelsen er oprettet, kan du vælge en rapport fra Power BI-delen på siderne.

## <a name="show-power-bi-reports-on-list-pages"></a>Vise Power BI-rapporter på listesider

[!INCLUDE[prodlong](includes/prodlong.md)] indeholder en Power BI-faktaboks på flere nøglelistesider. Denne faktaboks giver yderligere indblik i dataene på listen. Når du flytter mellem rækkerne på listen, opdateres rapporten og filtreres for den valgte post. Hvis du ikke kan se denne del, skal du på handlingslinjen vælge **Handlinger** > **Vis** > **Vis/skjul Power BI-rapporter**. Du kan finde flere oplysninger under [Oprette Power BI-rapporter til visning af listedata i [!INCLUDE[prodshort](includes/prodshort.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="select-power-bi-reports"></a>Vælge Power BI-rapporter

En Power BI-del på en side kan vise alle de Power BI-rapporter, der er tilgængelige for dig. Hvis du vil skifte til at få vist en anden rapport, skal du vælge handlingen **Vælg rapport** på rullelisten over kommandoer øverst i delen.  

På siden **Power BI-rapportvalg** vises en liste over alle de Power BI-rapporter, du har adgang til. Denne liste hentes fra Power BI-arbejdsområdet. Vælg **Aktivér** for hver enkelt rapport, der skal vises på startsiden, og vælg derefter **OK**. Du vender tilbage til siden, og den sidste rapport, du har aktiveret, vises. Brug kommandoen **Forrige** og **Næste** til at navigere mellem rapporterne på kommandorullelisten.  

## <a name="get-reports"></a>Hent rapporter

Hvis der ikke vises nogen rapporter på siden **Power BI-rapportvalg**, eller hvis du ikke kan se den ønskede rapport, skal du vælge **Hent rapporter**. Du kan bruge denne handling til at søge efter rapporter fra to placeringer: *Min organisation* eller fra *Tjenester*.

- Vælg **Min organisation** for at gå til Power BI-tjenesterne. Herfra kan du få vist de rapporter i organisationen, som du har fået tildelt rettigheder til at se. Derefter kan du føje dem til dit arbejdsområde.
- Vælg **Tjenester** for at gå til Microsoft AppSource, hvor du kan installere Power BI-apps.  

> [!TIP]
> Hvis du har Power BI Desktop, kan du også oprette nye Power BI-rapporter. Når disse rapporter er publiceret til dit Power BI-arbejdsområde, vises de på siden **Power BI-rapportvalg**.  

## <a name="manage-and-modify-reports"></a>Administrere og redigere rapporter

Du kan foretage ændringer af en rapport i Power BI-delen. De ændringer, du foretager, publiceres derefter til Power BI-tjenesten. Hvis rapporten deles med andre brugere, kan de også se ændringerne, medmindre du gemmer ændringerne i en ny rapport.

Hvis du vil redigere en rapport, skal du vælge handlingen **Administrer rapport** fra kommandorullelisten i Power BI-delen. Begynd at foretage ændringer. Når du er færdig med at foretage ændringer, skal du vælge **Fil** > **Gem**. Hvis det er en delt rapport, og du ikke vil foretage ændringen for alle brugere, skal du vælge **Gem som** for at undgå at skulle foretage denne ændring for alle brugere.

Når du går tilbage til rollecenteret, vises den opdaterede rapport. Hvis du har brugt **Gem som**, skal du vælge **Vælg rapport** og derefter aktivere den nye rapport for at se den.

> [!NOTE]
> Denne funktion er ikke tilgængelig for [!INCLUDE [prodshort](includes/prodshort.md)] on-premises.

## <a name="upload-reports"></a><a name="upload"></a>Overføre rapporter

Power BI-rapporter kan distribueres blandt brugere som .pbix-filer. Hvis du har nogen .pbix-filer, kan du overføre og dele dem med alle brugere af [!INCLUDE [prodshort](includes/prodshort.md)]. Rapporterne deles inden for hver virksomhed i [!INCLUDE [prodshort](includes/prodshort.md)].  

For at overføre en rapport skal du vælge handlingen **Overfør rapport** fra kommandorullelisten i delen **Power BI-rapporter**. Find derefter den .pbix-fil, der definerer de rapporter, du vil dele. Du kan ændre filens standardnavn.  

Når rapporten overføres til Power BI-arbejdsområdet, overføres den automatisk til andre brugeres Power BI-arbejdsområder.

> [!NOTE]
> Hvis du overfører en rapport, kræver det, at du har SUPER-brugerrettigheder i [!INCLUDE[prodshort](includes/prodshort.md)]. Du kan heller ikke overføre rapporter med [!INCLUDE [prodshort](includes/prodshort.md)] on-premises. Med on-premises kan du overføre rapporter direkte til dit Power BI-arbejdsområde. Du kan finde flere oplysninger i [Arbejde med [!INCLUDE [prodshort](includes/prodshort.md)]-data i Power BI](across-working-with-business-central-in-powerbi.md).

## <a name="fixing-problems"></a>Løse problemer

Men hvis noget går galt indeholder dette afsnit en løsning til de mest almindelige problemer.  

### <a name="you-dont-have-a-power-bi-account"></a>Du har ikke en Power BI-konto

Der er ikke blevet oprettet en Power BI-konto. Fo at få en gyldig Power BI-konto skal du have en licens, og du skal tidligere have været logget på Power BI for at kunne oprette et Power BI-arbejdsområde.   

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Meddelelse: Der er ingen aktiverede rapporter. Vælg Vælg rapport for at få vist en oversigt over de rapporter, du kan få vist.

Denne meddelelse vises, hvis standardrapporten ikke blev implementeret i Power BI-arbejdsområdet. Eller den blev installeret, men blev ikke opdateret korrekt. Gå til rapporten i dit Power BI-arbejdsområde, vælg **Datasæt**, **Indstillinger**, og opdater derefter legitimationsoplysningerne manuelt. Når datasættet er opdateret, skal du gå tilbage til [!INCLUDE[prodshort](includes/prodshort.md)] og vælge rapporten manuelt på siden **Vælg rapporter**.


## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Business Central og Power BI](admin-powerbi.md)  
[Oprette Power BI-rapporter, der viser [!INCLUDE [prodlong](includes/prodlong.md)]-data](across-how-use-financials-data-source-powerbi.md)  
[Oversigt over Power BI-integrationskomponent og -arkitektur for [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
[Arbejde med [!INCLUDE [prodshort](includes/prodshort.md)]-data i Power BI](across-working-with-business-central-in-powerbi.md)  
[Power BI for forbrugere](/power-bi/consumer/end-user-consumer)  
[Power BI-tjenestens nye udseende](/power-bi/service-new-look)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentation](/power-bi/)  
[Business Intelligence](bi.md)  
[Introduktion](product-get-started.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
