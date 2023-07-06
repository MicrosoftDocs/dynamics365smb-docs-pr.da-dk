---
title: Tilføje Business Central-fane i Microsoft Teams
description: 'Få mere at vide om, hvordan du tilføjer faner i Teams, der viser Business Central-sider.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/04/2022
ms.custom: bap-template
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records, tab'
---

# <a name="add-business-central-tab-in-microsoft-teams"></a><a name="add-business-central-tab-in-microsoft-teams"></a><a name="add-business-central-tab-in-microsoft-teams"></a>Tilføje Business Central-fane i Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

I Teams vises faner i toppen af kanaler og chats, så deltagerne har hurtig adgang til relevante oplysninger. I denne artikel forklares forskellige måder at tilføje en fane på, der viser [!INCLUDE [prod_short](includes/prod_short.md)]-data.

![Faner i Teams](media/teams-tabs-border.png)

## <a name="about-business-central-tabs"></a><a name="about-business-central-tabs"></a><a name="about-business-central-tabs"></a>Om Business Central-faner

En [!INCLUDE [prod_short](includes/prod_short.md)]-fane giver en fokuseret visning af [!INCLUDE [prod_short](includes/prod_short.md)]-liste og kortsider. På fanen vises ikke hele [!INCLUDE [prod_short](includes/prod_short.md)]-webklienten. Der er ingen kant fra browseren, [!INCLUDE [prod_short](includes/prod_short.md)]-banner (f. eks. med Fortæl, søgning, hjælp) eller navigationsmenu - kun sidens indhold og handlinger. Indholdet er interaktivt, hvilket betyder, at du kan vælge handlinger og links, ændre data m.m. Du er begrænset til det, du ser, og hvad du kan udføre med de samme tilladelser, der er tildelt din konto i [!INCLUDE [prod_short](includes/prod_short.md)].

Hvis du vil vide, hvordan du kan få vist indholdet af en [!INCLUDE [prod_short](includes/prod_short.md)]-fane, kan du se o [Hvem kan se indholdet af en fane?](/dynamics365/business-central/teams-faq?tabs=tabs#who-can-view).

> [!TIP]
> Er du udvikler? Du kan også tilføje faner programmeringsmæssigt ved hjælp af Microsoft Graph API. Du kan finde flere oplysninger i [Tilføje en Business Central-faner i Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams-tabs).  

## <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Forudsætninger

Hvis du vil tilføje en [!INCLUDE [prod_short](includes/prod_short.md)]-fane, skal følgende krav være opfyldt:

- Du har adgang til Microsoft Teams.
- Du har en [!INCLUDE [prod_short](includes/prod_short.md)]-licens.
- Du har installeret [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams. Du kan finde flere oplysninger i [Installere [!INCLUDE [prod_short](includes/prod_short.md)]-appen til Microsoft Teams](across-install-app-for-teams.md).

Hvis du vil have vist [!INCLUDE [prod_short](includes/prod_short.md)]-fanen, som er tilføjet af en anden deltager i kanalen eller chatten, skal følgende krav være opfyldt:

- Du har adgang til Microsoft Teams.
- Du har en [!INCLUDE [prod_short](includes/prod_short.md)]-licens eller begrænset adgang til Business Central med en Microsoft 365-licens. Du kan finde flere oplysninger i [Adgang til Business Central med Microsoft 365-licenser](admin-access-with-m365-license.md).
- Du har installeret [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams.

## <a name="add-tab-using-recommended-content"></a><a name="add-tab-using-recommended-content"></a><a name="add-tab-using-recommended-content"></a>Tilføje fane med anbefalet indhold

Du kan bruge disse trin til at tilføje en fane ved at vælge, hvad der skal vises fra en direkte tilgængelig liste over anbefalet indhold, der er baseret på rollecenteret - uden at forlade Teams. Hvis du vil vide mere om det indhold, du kan vælge mellem, kan du se [Hvor kommer det anbefalede indhold fra?](/dynamics365/business-central/teams-faq?tabs=tabs#where-does-the-recommended-content-come-from).

1. Marker **+ Tilføj en fane** øverst på en kanal eller chat i Teams.
2. Skriv **Business central** i feltet *Søg*, og vælg **[!INCLUDE [prod_short](includes/prod_short.md)]**-ikonet, og vent, til [!INCLUDE [prod_short](includes/prod_short.md)]-fanen med konfigurationsvinduet vises.

   ![Viser fanen Business Central med konfigurationsvinduet i Teams](media/teams-bc-tab-config-window.png)

3. Indstillingen **Vælg fra indhold, der anbefales til** indstilling, viser det firma i [!INCLUDE [prod_short](includes/prod_short.md)], som du arbejder med. Hvis du vil have vist indhold fra en anden virksomhed, skal du vælge den aktuelle virksomhed og derefter bruge indstillingerne for **Miljø** og **Virksomhed** til at angive den virksomhed, du vil arbejde med.
4. Vælg pil ned under fanen **Indhold**, og vælg det indhold, du vil have vist.

   <!-- The list shows all pages that are bookmarked on your role center in [!INCLUDE [prod_short](includes/prod_short.md)]. To learn more about the content that you can choose from, see [Where does the recommended content come from?](teams-faq.md#recommended-content).-->
5. Nogle sider kan indeholde forskellige visninger, som er variationer af den side, der er filtreret, til at vise bestemte data. Hvis du vil ændre visningen for indholdet, skal du vælge pil ned for den **foretrukne visning** og vælge visningen på listen.

   Du kan finde flere oplysninger om visninger i [Gemme og tilpasse listevisninger](ui-views.md).
6. Vælg **Send til kanalen om denne fane**, hvis du automatisk vil sende en meddelelse i en Teams-kanal eller via chat, så du kan se, at du har tilføjet denne fane.
7. Vælg **Gem**.

## <a name="add-tab-using-a-page-link"></a><a name="add-tab-using-a-page-link"></a><a name="add-tab-using-a-page-link"></a>Tilføj fane ved hjælp af et sidelink

Du kan også tilføje en fane med et link (URL) på den side, du vil vise. Denne måde er nyttig, når du vil have vist en bestemt [!INCLUDE [prod_short](includes/prod_short.md)]-post eller en listeside, der ikke er bogmærket i rollecenteret.

1. Marker **+ Tilføj en fane** øverst på en kanal eller chat i Teams.
2. Skriv **Business Central** i feltet *Søg*, og vælg derefter **[!INCLUDE [prod_short](includes/prod_short.md)]**-ikonet.
3. Vent, til [!INCLUDE [prod_short](includes/prod_short.md)]-fanen med konfigurationsvinduet vises, og vælg derefter indstillingen **Indsæt et [!INCLUDE [prod_short](includes/prod_short.md)]-link i stedet**.

   ![Viser fanen Business Central med konfigurationsvinduet i Teams og fremhæver linkindstillingen](media/teams-bc-tab-config-window-page-link.png)
4. Gå til [!INCLUDE [prod_short](includes/prod_short.md)], og Åbn den side, der skal vises på fanen.
5. Kopier linket til siden.

   Der er to måder at kopiere linket på. Den nemmeste og foretrukne måde er at vælge ikonet **Del** ![Del-ikon i Business Central](media/share-icon.png) > **Kopier link**. Du kan også kopiere hele URL-adressen direkte fra browserens adressefelt. Du kan få mere at vide om dette trin i [Deling af Business Central-poster og sidelinks](across-working-with-teams.md).

6. Gå tilbage til Teams, og indsæt linket i feltet **URL-adresse**.
7. Indtast et navn, der skal vises under fanen, i boksen **Fanenavn**.
8. Vælg **Send til kanalen om denne fane**, hvis du automatisk vil sende en meddelelse i en Teams-kanal eller via chat, så du kan se, at du har tilføjet denne fane.
9. Vælg **Gem**.

## <a name="add-tab-by-pinning-card-details"></a><a name="add-tab-by-pinning-card-details"></a><a name="add-tab-by-pinning-card-details"></a>Tilføj fane ved at fastgøre kortdetaljer

Benyt følgende trin for at føje en fane til en post, der er delt eller indsat i en Teams-kanal eller chat. Du kan finde flere oplysninger om deling af poster og sidelinks i Teams i [Dele poster og sidelinks i Teams](across-working-with-teams.md).

1. I Teams skal du vælge knappen **Detaljer** på kortet.
2. I øverste højre hjørne af kortdetaljerne skal du vælge **Fastgør til toppen af chat** ![Fastgør-ikon for at tilføje fanen Teams i Business Central](media/pin-teams.png)-ikonet.

## <a name="change-a-tab-and-its-content"></a><a name="change-a-tab-and-its-content"></a><a name="change-a-tab-and-its-content"></a>Ændre en fane og dens indhold

Når der er tilføjet en fane, kan du foretage visse ændringer af fanen. Du kan f. eks. omdøbe fanen, flytte den og fjerne den. Du finder disse handlinger under fanens indstillinger, der er tilgængelige, når du vælger den nedadgående pil på fanen.

![Viser fanen Business Central med konfigurationsvinduet i Teams og menuen med faneindstillinger](media/teams-bc-tab-config-window-options.png)

Som til indholdet af en fane kan du redigere dataene, hvis du har tilladelse. Hvis du ændrer dataene, kan andre brugere ikke se ændringerne, før de forlader den pågældende fane og vender tilbage. Det samme gælder, hvis en anden foretager ændringer til data. Du kan ikke ændre den side, der vises under fanen, så du skal bare fjerne fanen og tilføje en ny.

Du kan også ændre visningen af siden og dens data, f.eks. sortere og skifte layout mellem liste og feltvisning. Når du foretager denne slags ændringer, har de ingen indflydelse på, hvad andre ser. De kan se, hvad du oprindeligt bogførte, indtil de foretager lignende ændringer.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Oversigt over integrationen af Business Central og Microsoft Teams](across-teams-overview.md)  
[Installere appen [!INCLUDE [prod_short](includes/prod_short.md)] til Microsoft Teams](across-install-app-for-teams.md)  
[Dele Business Central-poster og Sidelinks i Microsoft Teams](across-working-with-teams.md).
[Teams, ofte stillede spørgsmål](teams-faq.md)  
[Søgning efter debitorer, kreditorer og andre kontakter fra Microsoft Teams](across-search-contacts-teams.md)  
[Ændring af virksomhed og andre indstillinger i Teams](across-teams-settings.md)  
[Fejlfinding i Teams](admin-teams-troubleshooting.md)  
[Udvikling af Teams-integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
