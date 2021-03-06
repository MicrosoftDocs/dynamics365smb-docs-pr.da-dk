---
title: Vise og redigere grundlæggende indstillinger | Microsoft Docs
description: Lær, hvordan du kan ændre nogle af de grundlæggende indstillinger i , f.eks. rollecenteret, virksomheden eller arbejdsdatoen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: df3807f3d5d2baa7f50df4091a0d1f2622d09ff8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757638"
---
# <a name="change-basic-settings"></a>Ændre grundlæggende indstillinger

På siden **Mine indstillinger** kan du se og ændre grundlæggende indstillinger for [!INCLUDE[prod_short](includes/prod_short.md)]. De ændringer, du foretager, påvirker kun dit arbejdsområde, ikke arbejdsområder for andre brugere.  

## <a name="role-center"></a><a name="role-center"></a> Rollecenter
Rollecenteret repræsenterer startsiden, et startskærmbillede, der er beregnet til en bestemt rolles behov i en organisation. Afhængigt af din rolle giver Rollecenter dig et overblik over arbejde, din afdeling eller personlige opgaver. Du kan også navigere til de daglige opgaver, og find arbejde, der er tildelt til dig.

-   Øverst i navigationen kan du skifte mellem debitorer, kreditorer, varer og andre vigtige lister med oplysninger. Her kan du også starte opgaver, f.eks. oprette en ny salgsfaktura direkte fra Rollecenter.

-   I midten finder du området **Aktiviteter**, som viser aktuelle data, og som du kan klikke på eller trykke på for at få vist mere detaljerede oplysninger. Nøgletal (KPI'er) kan konfigureres til at vise et valgt diagram for en grafisk visning af f.eks. pengestrøm eller indtægter og udgifter. Du kan også oprette en række favoritdebitorer i rollecenteret for forretningskunder, som du handler med ofte, eller du skal have særlig opmærksomhed på.

### <a name="to-change-the-role"></a>Sådan ændres rollen
Standardrollen er **Virksomhedsleder**, men du kan vælge en anden rolle for at bruge et rollecenter, der passer bedre til dine behov.
1. I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") og derefter vælge handlingen **Mine indstillinger**.
2. På siden **Mine indstillinger** skal du i feltet **Rolle** vælge den rolle, du vil bruge som standard. Vælg f.eks **Regnskabsmedarbejder**.
3. Vælg knappen **OK**.

## <a name="company"></a><a name="company"></a>Virksomhed
En virksomhed fungerer som en beholder for data i [!INCLUDE[prod_short](includes/prod_short.md)]. Der kan være flere virksomheder i en database, men du kan vælge kun ét ad gangen.

Standardfirmaet kaldes CRONUS og indeholder kun demonstrationsdata. Du kan oprette en ny virksomhed med brugerdefinerede data. Du kan finde flere oplysninger under [Oprettelse af nye virksomheder](about-new-company.md).

## <a name="to-change-the-company-name"></a>Sådan ændres virksomhedsnavnet
Virksomhedsnavnet vises altid i øverste venstre hjørne og fungerer som en handling, som du kan vælge for at gå tilbage til rollecenteret. Du kan ændre dette navn på siden **Virksomhedsoplysninger**.

1. Vælg ![Tandhjulsikonet for at åbne menuen Indstillinger](media/ui-experience/settings_icon_small.png) og derefter vælge handlingen **Virksomhedsoplysninger**.
2. I feltet **Navn** skal du angive det nye virksomhedsnavn.
3. Forlad siden. Systemet genstarter og viser den nye virksomhed i øverste venstre hjørne.

## <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a>Sådan får du vist en virksomheds kort, så du hurtigt kan få adgang til virksomhedsoplysninger  
Du kan tilføje et tilpasset kort i øverste højre hjørne, som du kan vælge for hurtigt at få vist virksomhedsnavnet og oplysninger om lejer i et pop op-felt.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomhedsoplysninger**, og vælg derefter det relaterede link.
2. I oversigtspanelet **Virksomhedskort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Hvis der er defineret et virksomhedskort, kan du ikke ændre virksomhedsnavnet som beskrevet i [Sådan ændres virksomhedsnavnet](ui-change-basic-settings.md#to-change-the-company-name)

## <a name="work-date"></a><a name="work-date"></a>Arbejdsdato
Den mest almindeligt anvendte arbejdsdato er dags dato. Du skal muligvis midlertidigt ændre arbejdsdatoen for at kunne udføre opgaver, f.eks. udføre transaktioner for en dato, der ikke er dags dato.

> [!TIP]  
> I alle datofelter kan du skrive **d** for hurtigt at angive dags dato, og **a** for hurtigt at angive arbejdsdatoen, som er værdien i feltet **Arbejdsdato** på siden **Mine indstillinger**.

> [!IMPORTANT]  
>  Når du har ændret arbejdsdatoen, og hvis du logger af eller skifter til et andet regnskab, tilbageføres arbejdsdata til standardarbejdsdatoen. Så næste gang du logger på eller skifter tilbage til det oprindelige regnskab, kan det være nødvendigt at angive arbejdsdatoen igen.

### <a name="work-date-indication"></a>Angivelse af arbejdsdato
Når arbejdsdatoen ikke er indstillet til dags dato, vises der to typer indikatorer på sider, der kan redigeres, og hvor arbejdsdatoen derfor er kritisk:

* Der vises en rykker øverst på siden, som angiver, hvad arbejdsdatoen er indstillet til. Rykkeren viser en direkte tilknytning til arbejdsdatoindstillingen på siden **Mine indstillinger**, så du kan ændre datoen efter behov. I rykkeren kan du også vælge at afvise rykkeren for resten af din session. Medmindre du ændrer arbejdsdatoen til "dags dato", vises rykkeren, næste gang du logger på.

* Hvis du afviser rykkeren, vises arbejdsdatoen i sidetitlen.  

Hvis arbejdsdatoen ikke er sat til den aktuelle dag (i dag), vises den aktuelle arbejdsdato i øverste venstre hjørne af siden, på alle de sider, hvor du kan redigere data.

## <a name="region"></a><a name="region"></a> Område

Indstillingen **Område** bestemmer, hvordan datoer, klokkeslæt, tal og valutaer vises og formateres.

## <a name="language"></a><a name="language"></a> Sprog
Ændrer det viste sprog. Dette felt vises kun, hvis der er mere end ét sprog, du kan vælge mellem.

Det første sprog afhænger enten af administratoren eller af browserindstillingerne, når du logger på [!INCLUDE[prod_short](includes/prod_short.md)]. Det sprog, du har angivet, vil blive brugt på alle enheder, som du logger på fra, f.eks. en telefon eller tablet.

Du kan installere flere sprog til [!INCLUDE[prod_short](includes/prod_short.md)] ved at hente dem fra AppSource. Alle understøttede grænsefladesprog vises på listen, men administratoren skal installere det relevante sprogprogram til lejeren, før brugerne kan vælge det nye sprog i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="changing-when-i-receive-notifications"></a>Ændre, hvornår jeg modtager notifikationer
Vælg dette link for at få vist eller ændre de notifikationer, du får om bestemte hændelser eller ændringer af status, når du er ved at fakturere en kunde, der har et forfaldent beløb, eller den disponible lagerbeholdning er lavere end det antal, du er ved at sælge. Du kan finde flere oplysninger under [Administration af meddelelser](ui-smart-notifications.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Oprettelse af nye virksomheder](about-new-company.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]