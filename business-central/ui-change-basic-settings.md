---
title: Ændre grundlæggende indstillinger for den aktuelle bruger
description: 'Få mere at vide om, hvordan du ændrer nogle grundlæggende indstillinger i Business Central, f. eks. dit rolle og rollecenter, firma, arbejdsdato og tidszone.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'change Role Center, notification, change company, change work date, decimal separator'
ms.search.form: '9022, 9019, 9027, 9020, 9026, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/31/2022
ms.author: jswymer
---
# Ændre grundlæggende indstillinger

På siden **Mine indstillinger** kan du se og ændre grundlæggende indstillinger for [!INCLUDE[prod_short](includes/prod_short.md)]. De ændringer, du foretager, påvirker kun dit arbejdsområde, ikke arbejdsområder for andre brugere.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="role-center"></a>Rolle

Rollen bestemmer startsiden, et startskærmbillede, der er designet til behovene for en bestemt rolle i organisationen. Afhængigt af din rolle, startside eller dit rollecenter får du et overblik over virksomheden, din afdeling eller dine personlige opgaver. Du kan også navigere til de daglige opgaver, og find arbejde, der er tildelt til dig.

* Øverst i navigationen kan du skifte mellem debitorer, kreditorer, varer og andre vigtige lister med oplysninger. Her kan du også starte opgaver, f.eks. oprette en ny salgsfaktura direkte fra startsiden.

* I midten finder du området **Aktiviteter**, som viser aktuelle data, og som du kan vælge for at få vist mere detaljerede oplysninger. Nøgletal (KPI'er) kan konfigureres til at vise et valgt diagram for en grafisk visning af f.eks. pengestrøm eller indtægter og udgifter. Du kan også oprette en liste over favoritdebitorer på startsiden for virksomhedskonti, som du ofte handler med eller skal være særligt opmærksom på.

### Ændre rollen

Standardrollen er **Virksomhedsleder**, men du kan vælge en anden rolle for at bruge et rollecenter, der passer bedre til dine behov.  

1. I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") og derefter vælge handlingen **Mine indstillinger**.
2. På siden **Mine indstillinger** skal du i feltet **Rolle** vælge den rolle, du vil bruge som standard. Vælg f.eks **Regnskabsmedarbejder**.
3. Vælg **OK**.

## <a name="company"></a>Virksomhed

En virksomhed fungerer som en beholder for data i [!INCLUDE[prod_short](includes/prod_short.md)]. Der kan være flere virksomheder i en database, men du kan vælge kun ét ad gangen. Standardfirmaet kaldes CRONUS og indeholder kun demonstrationsdata.

Feltet **Firma** viser den virksomhed, som du aktuelt arbejder i, og du kan bruge det til at skifte til et andet regnskab. Virksomhedsnavnet vises altid i øverste venstre hjørne og fungerer som en handling, som du kan vælge for at gå tilbage til rollecenteret.

> [!TIP]
> Du kan også ændre virksomheden vha. virksomhedsskifter (CRTL + O). Du kan finde flere oplysninger om denne funktion og andre måder at ændre regnskab eller miljø på i [skifte til et andet firma eller miljø](ui-organization-switch.md).

Standardfirmaet kaldes CRONUS og indeholder kun demonstrationsdata. Du kan oprette en ny virksomhed med brugerdefinerede data. Du kan finde flere oplysninger i [Oprettelse af nye virksomheder](about-new-company.md).

<!--
### To change the company name

The company name is always displayed at the top left corner and works as an action that you can choose to go back to the Role Center. You can change this name on the **Company Information** page.

1. Choose the ![Sprocket icon to open the Settings menu.](media/ui-experience/settings_icon_small.png) icon, and then choose the **Company Information** action.
2. In the **Name** field, enter the new company name.
3. Leave the page. The system restarts and displays the new company in the top-left corner.

### <a name="badge"></a>To display a company badge for quick access to company information

You can add a customized badge in the top-right corner, which you can choose to quickly view company name and tenant information in a pop-up box. The company badge is also useful when [!INCLUDE[prod_short](includes/prod_short.md)] is embedded in another application, like Microsoft Teams or in some other web application. In these cases, because the [!INCLUDE[web_client](includes/web_client.md)] displays less surrounding contextual information, the company badge serves as the only way to determine which company or environment a record belongs to.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.
2. On the **Company Badge** FastTab, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> If a company badge is defined, then you cannot change the company name as described in [To change the company name](ui-change-basic-settings.md#to-change-the-company-name)-->

## <a name="work-date"></a>Arbejdsdato

Den mest almindeligt anvendte arbejdsdato er dags dato. Du skal muligvis midlertidigt ændre arbejdsdatoen for at kunne udføre opgaver, f.eks. udføre transaktioner for en dato, der ikke er i dag.

> [!TIP]  
> I alle datofelter kan du skrive **d** for hurtigt at angive dags dato, og **a** for hurtigt at angive arbejdsdatoen, som er værdien i feltet **Arbejdsdato** på siden **Mine indstillinger**.

> [!IMPORTANT]  
> Når du har ændret arbejdsdatoen, og hvis du logger af eller skifter til et andet regnskab, tilbageføres arbejdsdata til standardarbejdsdatoen. Så næste gang du logger på eller skifter tilbage til det oprindelige regnskab, kan det være nødvendigt at angive arbejdsdatoen igen.

### Angive arbejdsdato

Arbejdsdatoen er afgørende for sider, der kan redigeres. Når arbejdsdatoen ikke er angivet til dags dato på en redigerbar side, vises der to typer indikatorer på siden:

* Der vises en rykker øverst på siden, som angiver, hvad arbejdsdatoen er indstillet til. Rykkeren viser en direkte tilknytning til arbejdsdatoindstillingen på siden **Mine indstillinger**, så du kan ændre datoen efter behov. I rykkeren kan du også vælge at afvise rykkeren for resten af din session. Medmindre du ændrer arbejdsdatoen til "dags dato", vises rykkeren, næste gang du logger på.

* Hvis du afviser rykkeren, vises arbejdsdatoen i sidetitlen.  

Hvis arbejdsdatoen ikke er sat til den aktuelle dag (i dag), vises den aktuelle arbejdsdato i øverste venstre hjørne af siden, på alle de sider, hvor du kan redigere data.

## <a name="region"></a> Område

Indstillingen **Område** bestemmer, hvordan datoer, klokkeslæt, tal og valutaer vises og formateres. Det bestemmer også, hvilket tegn der bruges som decimalseparator, når du bruger et numerisk tastatur til at indtaste data. Flere oplysninger i [Indtastning af data](ui-enter-data.md#decimal).

## <a name="language"></a> Sprog

Ændrer det viste sprog. Dette felt vises kun, hvis der er mere end ét sprog, du kan vælge mellem.

Det første sprog afhænger enten af administratoren eller af browserindstillingerne, når du logger på [!INCLUDE[prod_short](includes/prod_short.md)]. Det sprog, du har angivet, vil blive brugt på alle enheder, som du logger på fra, f.eks. en telefon eller tablet.

Du kan installere flere sprog til [!INCLUDE[prod_short](includes/prod_short.md)] ved at hente dem fra AppSource. Alle understøttede grænsefladesprog vises på listen, men administratoren skal installere det relevante sprogprogram til lejeren, før brugerne kan skifte til det nye sprog i [!INCLUDE[prod_short](includes/prod_short.md)].  

## Tidszone

Definerer den tidszone, hvor du er placeret. Når du logger på [!INCLUDE [prod_short](includes/prod_short.md)] første gang, angives tidszonen ud fra virksomhedens adresse. Du kan ændre den, hvis den ikke passer til din fysiske lokation.  

## Notifikationer

Vælg linket *Rediger, når jeg modtager notifikationer* for at få vist eller ændre de notifikationer, du får om bestemte hændelser eller statusændringer, f.eks. når du skal fakturere en kunde, der har et forfaldent beløb, eller den disponible lagerbeholdning er lavere end det antal, du er ved at sælge. Få mere at vide på [Administration af meddelelser](ui-smart-notifications.md).

## Undervisningstip

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## Se relateret [Microsoft-træning](/training/modules/personalize-ui-dynamics-365-business-central/index)

## Se også

[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Oprettelse af nye virksomheder](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
