---
title: Skifte til et andet firma eller miljø
description: 'Hvis du arbejder for flere organisationer, kan du hurtigt skifte mellem miljøerne og virksomhederne.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'environments, companies, tenants, organization'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 04/24/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="switching-to-another-company-or-environment"></a>Skifte til et andet firma eller miljø

[!INCLUDE [prod_short](includes/prod_short.md)] er tilgængelig i mange forskellige lande/områder og understøtter mange forskellige organisationstyper. Organisationen kan vælge at organisere arbejde i [!INCLUDE [prod_short](includes/prod_short.md)] i flere *firmaer* og *miljøer*. Denne artikel hjælper dig med at forstå de vigtigste forskelle og arbejde på tværs af dem.

## <a name="about-companies-and-environments"></a>Om virksomheder og miljøer

[!INCLUDE [company_environment](includes/company_environment.md)]

> [!TIP]
> Hvis du ofte skifter mellem firmaer eller arbejder med [!INCLUDE[prod_short](includes/prod_short.md)] fra en anden app Microsoft Teams, kan det være nemt at miste numre på det sted, hvor du er. For at hjælpe dig med at holde styr på det kan du tilføje et kort, der viser navnet på virksomheden, så du hurtigt kan se, at du er på det rigtige sted. Du kan finde flere oplysninger i [Vise et virksomhedskort](admin-company-information.md#badge).
> 
> Afhængigt af browseren kan du også fastgøre de forskellige regnskaber til din Foretrukne-linje.  

<!--
[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]-->

## <a name="features-for-switching-company-or-environment"></a>Funktioner til at skifte firma eller miljø

Der er nogle få funktioner, som du kan bruge til at skifte firma eller miljø, mens du arbejder. I følgende tabel sammenlignes funktionerne i funktionen, som forklares mere detaljeret i de efterfølgende afsnit.

|Funktion|Skift firma|Skift miljø|Skift til en ny fane i browseren| Tilgængelige i det lokale miljø|
|-------|--------------|------------------|-------------------------|----------------------|
|[Firmaskifter](#use-the-company-switcher)|![markering](media/check.png "check")|![markering](media/check.png "check")|![markering](media/check.png "check")|![markering](media/check.png "check")|
|[App-starter](#use-the-app-launcher)||![markering](media/check.png "check")|![markering](media/check.png "check")||
|[Mine indstillinger](#use-my-settings)|![markering](media/check.png "check")|||![markering](media/check.png "check")|
|[Virksomhedshub](#use-company-hub)|![markering](media/check.png "check")|![markering](media/check.png "check")|![markering](media/check.png "check")||

## <a name="use-the-company-switcher"></a>Brug firmaskifter

Det er sandsynligvis den hurtigste og mest alsidige måde at skifte virksomhed på. Virksomhedsskifteren er en rude, som er nem at finde på alle sider. I ruden kan du få et overblik over alle regnskaber i alle de miljøer, du har adgang til, og du kan skifte direkte til en hvilken som helst af dem - enten i den samme webbrowser fane eller på en ny. Det er især nyttigt, når du arbejder i mange virksomheder på tværs af forskellige miljøer.

1. I øverste højre hjørne vil du i nærheden af søgeikonet Se enten ikonet standardregnskab, f.eks. ![firma ikonet Startside.](media/ui-experience/company-icon.png "Viser ikonet for virksomhedsskifteren, der bruges, når der er et enkelt miljø") og ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Viser ikonet for virksomhedsskifteren, der bruges, når der er flere miljøer") eller et [brugerdefineret badge](admin-company-information.md#badge) for den virksomhed, som du aktuelt arbejder med. Vælg ikonet for at åbne ruden regnskabsskifter.

   :::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Viser ikonet for virksomhedsskifteren i overskriften for Business Central-klienten.":::  

   > [!TIP]
   > Du kan også bruge genvejstasten <kbd>Crtl</kbd>+<kbd>O</kbd> til at åbne ruden.
2. Marker det firma, du vil skifte til, i ruden **Tilgængelige firmaer**, vælg pilen **skift**, og vælg derefter en af følgende indstillinger:

   |Indstilling|Beskrivelse|
   |------|-----------|
   |Skift|Åbner rollecenteret for den valgte virksomhed i den samme fane i browseren, som du arbejder i. Virksomheden bliver standardregnskabet, der åbnes i Business central, indtil du skifter igen eller ændrer virksomheden vha. **Mine indstillinger**. |
   |Åbn på ny fane|Åbner rollecenteret for den valgte virksomhed i en ny browserfane, så den oprindelige virksomhed er åben i den anden fane.|
   |Åbn under ny fane, og gå til samme side|Denne indstilling er kun aktiv på listesider, f.eks. debitorer, salgsordrer eller varer. Den åbner samme liste, men for det valgte firma under fanen ny. |

> [!TIP]
> Vælg <kbd>F5</kbd> for at opdatere listen over miljøer og regnskaber.

## <a name="use-the-app-launcher"></a>Bruge appstarter

Når du er logget på [!INCLUDE[prod_short](includes/prod_short.md)], er de miljøer, du har adgang til, tilgængelige på Microsoft 365.  

1. Vælg ikonet **App-starter** til ![App-starter.](media/app-launcher-icon.png "Appstarteren giver adgang til flere funktioner").
2. I den rude, der vises, skal du søge efter og vælge [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du ikke kan se [!INCLUDE[prod_short](includes/prod_short.md)], skal du vælge **Alle apps** og derefter angive **Business Central** i feltet **Søg**.

   :::image type="content" source="media/app-launcher-bc-tile.png" alt-text="Microsoft 365-appstarteren viser feltet Business Central.":::  

3. Hvis der er mere end ét miljø, bliver du bedt om at vælge, hvilket miljø du vil have adgang til.

> [!NOTE]
> Appstarter er ikke tilgængelig, hvis du er logget på Business Central som gæst.

<!--
The following image shows tiles for accessing production and sandbox environments on the Dynamics 365 Home page.

:::image type="content" source="media/app-picker-environments.png" alt-text="The Dynamics 365 Home page showing production and sandbox environments.":::
-->
## <a name="use-my-settings"></a>Bruge Mine indstillinger

Når du er logget på [!INCLUDE[prod_short](includes/prod_short.md)], kan du hurtigt skifte til en anden virksomhed i samme miljø. Når du har foretaget skiftet, bliver den virksomhed, du vælger, din standardvirksomhed, som åbnes, næste gang du logger på.

1. I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter"), og derefter vælge handlingen **Mine indstillinger**.

    > [!TIP]
    > Du kan også bruge tastaturgenvejen <kbd>Alt</kbd>+<kbd>T</kbd> til hurtigt at åbne siden Mine indstillinger.

2. På siden **Mine indstillinger** skal du vælge virksomheden i feltet **Virksomhed**.  
3. Vælg knappen **OK**.

> [!TIP]
> En god metode til at gå direkte til din standardvirksomhed, når du logger på, og undgå at skulle angive et miljø, er at føje URL-adressen til listen over foretrukne, når du er logget på.

## <a name="use-company-hub"></a>Bruge firmahub

*Firmahub* er et særdeles specialiseret rollecenter, der giver en økonomisk oversigt over virksomheder og miljøer. Tilgængelig som en [udvidelse](ui-extensions-company-hub.md) indeholder firmahubben et dashboard med oversigtsdata for hvert firma, du har adgang til. Startsiden viser de økonomiske nøgletal og en direkte forbindelse til de enkelte miljøer og firmaer. Du kan finde flere oplysninger i [Administrer arbejde på tværs af flere firmaer i virksomhedens hub](company-hub.md).

[![Viser siden med virksomhedshub, der viser alle virksomheder.](media/company-hub.png)](media/company-hub.png#lightbox)  

## <a name="see-also"></a>Se også

[Oprettelse af nye virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Miljøer og virksomheder (kun engelsk version)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  
[Virksomhedsoplysninger](admin-company-information.md)  
[Business Central Administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
