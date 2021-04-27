---
title: Ændre grundlæggende indstillinger for den aktuelle bruger
description: Lær, hvordan du kan ændre nogle af de grundlæggende indstillinger, f.eks. rollecenteret, virksomheden eller arbejdsdatoen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a0a504aa7c06c08d2e9f4251128e4203f0f90dee
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787448"
---
# <a name="change-basic-settings"></a>Ændre grundlæggende indstillinger

På siden **Mine indstillinger** kan du se og ændre grundlæggende indstillinger for [!INCLUDE[prod_short](includes/prod_short.md)]. De ændringer, du foretager, påvirker kun dit arbejdsområde, ikke arbejdsområder for andre brugere.  

## <a name="role"></a><a name="role-center"></a>Rolle

Rollen bestemmer startsiden, et startskærmbillede, der er designet til behovene for en bestemt rolle i organisationen. Afhængigt af din rolle, startside eller dit rollecenter får du et overblik over virksomheden, din afdeling eller dine personlige opgaver. Du kan også navigere til de daglige opgaver, og find arbejde, der er tildelt til dig.

* Øverst i navigationen kan du skifte mellem debitorer, kreditorer, varer og andre vigtige lister med oplysninger. Her kan du også starte opgaver, f.eks. oprette en ny salgsfaktura direkte fra startsiden.

* I midten finder du området **Aktiviteter**, som viser aktuelle data, og som du kan klikke på eller trykke på for at få vist mere detaljerede oplysninger. Nøgletal (KPI'er) kan konfigureres til at vise et valgt diagram for en grafisk visning af f.eks. pengestrøm eller indtægter og udgifter. Du kan også oprette en liste over favoritdebitorer på startsiden for virksomhedskonti, som du ofte handler med eller skal være særligt opmærksom på.

### <a name="to-change-the-role"></a>Sådan ændres rollen

Standardrollen er **Virksomhedsleder**, men du kan vælge en anden rolle for at bruge et rollecenter, der passer bedre til dine behov.  

1. I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") og derefter vælge handlingen **Mine indstillinger**.
2. På siden **Mine indstillinger** skal du i feltet **Rolle** vælge den rolle, du vil bruge som standard. Vælg f.eks **Regnskabsmedarbejder**.
3. Vælg knappen **OK**.

## <a name="company"></a><a name="company"></a>Virksomhed

En virksomhed fungerer som en beholder for data i [!INCLUDE[prod_short](includes/prod_short.md)]. Der kan være flere virksomheder i en database, men du kan vælge kun ét ad gangen.

Standardfirmaet kaldes CRONUS og indeholder kun demonstrationsdata. Du kan oprette en ny virksomhed med brugerdefinerede data. Du kan finde flere oplysninger i [Oprettelse af nye virksomheder](about-new-company.md).

### <a name="to-change-the-company-name"></a>Sådan ændres virksomhedsnavnet

Virksomhedsnavnet vises altid i øverste venstre hjørne og fungerer som en handling, som du kan vælge for at gå tilbage til rollecenteret. Du kan ændre dette navn på siden **Virksomhedsoplysninger**.

1. Vælg ![Tandhjulsikonet for at åbne menuen Indstillinger](media/ui-experience/settings_icon_small.png) og derefter vælge handlingen **Virksomhedsoplysninger**.
2. I feltet **Navn** skal du angive det nye virksomhedsnavn.
3. Forlad siden. Systemet genstarter og viser den nye virksomhed i øverste venstre hjørne.

### <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>Sådan får du vist en virksomheds kort, så du hurtigt kan få adgang til virksomhedsoplysninger

Du kan tilføje et tilpasset kort i øverste højre hjørne, som du kan vælge for hurtigt at få vist virksomhedsnavnet og oplysninger om lejer i et pop op-felt. Virksomheds badgen er også nyttig, når [!INCLUDE[prod_short](includes/prod_short.md)] integreres i et andet program, f.eks, Microsoft Teams eller i et andet webprogram. Da der i disse tilfælde, hvor [!INCLUDE[web_client](includes/web_client.md)] viser mindre omkringliggende kontekstoplysninger, fungerer virksomhedens kort som den eneste måde at bestemme, hvilket firma eller hvilket miljø en post tilhører.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomhedsoplysninger**, og vælg derefter det relaterede link.
2. I oversigtspanelet **Virksomhedskort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Hvis der er defineret et virksomhedskort, kan du ikke ændre virksomhedsnavnet som beskrevet i [Sådan ændres virksomhedsnavnet](ui-change-basic-settings.md#to-change-the-company-name)

## <a name="work-date"></a><a name="work-date"></a>Arbejdsdato
Den mest almindeligt anvendte arbejdsdato er dags dato. Du skal muligvis midlertidigt ændre arbejdsdatoen for at kunne udføre opgaver, f.eks. udføre transaktioner for en dato, der ikke er dags dato.

> [!TIP]  
> I alle datofelter kan du skrive **d** for hurtigt at angive dags dato, og **a** for hurtigt at angive arbejdsdatoen, som er værdien i feltet **Arbejdsdato** på siden **Mine indstillinger**.

> [!IMPORTANT]  
> Når du har ændret arbejdsdatoen, og hvis du logger af eller skifter til et andet regnskab, tilbageføres arbejdsdata til standardarbejdsdatoen. Så næste gang du logger på eller skifter tilbage til det oprindelige regnskab, kan det være nødvendigt at angive arbejdsdatoen igen.

### <a name="work-date-indication"></a>Angive arbejdsdato

Arbejdsdatoen er afgørende for sider, der kan redigeres. Når arbejdsdatoen ikke er angivet til dags dato på en redigerbar side, vises der to typer indikatorer på siden:

* Der vises en rykker øverst på siden, som angiver, hvad arbejdsdatoen er indstillet til. Rykkeren viser en direkte tilknytning til arbejdsdatoindstillingen på siden **Mine indstillinger**, så du kan ændre datoen efter behov. I rykkeren kan du også vælge at afvise rykkeren for resten af din session. Medmindre du ændrer arbejdsdatoen til "dags dato", vises rykkeren, næste gang du logger på.

* Hvis du afviser rykkeren, vises arbejdsdatoen i sidetitlen.  

Hvis arbejdsdatoen ikke er sat til den aktuelle dag (i dag), vises den aktuelle arbejdsdato i øverste venstre hjørne af siden, på alle de sider, hvor du kan redigere data.

## <a name="region"></a><a name="region"></a> Område

Indstillingen **Område** bestemmer, hvordan datoer, klokkeslæt, tal og valutaer vises og formateres.

## <a name="language"></a><a name="language"></a> Sprog

Ændrer det viste sprog. Dette felt vises kun, hvis der er mere end ét sprog, du kan vælge mellem.

Det første sprog afhænger enten af administratoren eller af browserindstillingerne, når du logger på [!INCLUDE[prod_short](includes/prod_short.md)]. Det sprog, du har angivet, vil blive brugt på alle enheder, som du logger på fra, f.eks. en telefon eller tablet.

Du kan installere flere sprog til [!INCLUDE[prod_short](includes/prod_short.md)] ved at hente dem fra AppSource. Alle understøttede grænsefladesprog vises på listen, men administratoren skal installere det relevante sprogprogram til lejeren, før brugerne kan skifte til det nye sprog i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="time-zone"></a>Tidszone

Definerer den tidszone, hvor du er placeret. Når du logger på [!INCLUDE [prod_short](includes/prod_short.md)] første gang, angives tidszonen ud fra virksomhedens adresse. Du kan ændre den, hvis den ikke passer til din fysiske lokation.  

## <a name="notifications"></a>Notifikationer

Vælg linket *Rediger, når jeg modtager notifikationer* for at få vist eller ændre de notifikationer, du får om bestemte hændelser eller ændringer af status, f.eks. når du skal fakturere en kunde, der har et forfaldent beløb, eller den disponible lagerbeholdning er lavere end det antal, du er ved at sælge. Du kan finde flere oplysninger i [Administration af meddelelser](ui-smart-notifications.md).

## <a name="teaching-tips"></a>Undervisningstip

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Oprettelse af nye virksomheder](about-new-company.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
