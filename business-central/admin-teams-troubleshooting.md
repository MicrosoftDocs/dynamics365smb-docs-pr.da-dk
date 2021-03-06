---
title: Fejlfinding af Microsoft Teams-integration
description: Få mere at vide om, hvad du kan gøre for en administrator at styre Microsoft Teams-integrationen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 10612a3e5e257969b2daf0839ea0826316a956ee
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046528"
---
# <a name="troubleshooting-microsoft-teams-integration-with-prod_short"></a>Fejlfinding af Microsoft Teams-integration med [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Denne artikel indeholder oplysninger om, hvordan du identificerer og løser problemer, der kan opstå, når du bruger Microsoft Teams med [!INCLUDE [prod_short](includes/prod_short.md)], som typisk bruger eller administrator.

## <a name="none-of-my-links-expand-into-a-card"></a>Ingen af mine links udvides til et kort 

Hvis du oplever dette problem, kan du prøve at:

1. Kontroller først, at [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Teams er installeret.

    Kontroller ved åbne Teams stationære pc-app eller Teams i browseren. Vælg derefter på venstre side **Apps**, og søg efter **[!INCLUDE [prod_short](includes/prod_short.md)]**. Når du finder **[!INCLUDE [prod_short](includes/prod_short.md)]**-appen, skal du vælge den for at åbne siden App-oplysninger. Hvis knappen **Tilføj til mig** vises, er appen [!INCLUDE [prod_short](includes/prod_short.md)] ikke installeret. Du kan finde flere oplysninger om, hvordan du installerer appen, i [Installation af [!INCLUDE [prod_short](includes/prod_short.md)]-app til Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Gæstebrugere kan ikke straks installere apps. Du kan finde flere oplysninger om gæstebrugere på vores ofte stillede spørgsmål om samarbejde med gæster. 

2. Kontroller derefter, at du har logget ind med den korrekte identitet.

    I Teams skal du gå til en vilkårlig chat og under meddelelsesboksen skal du vælge ikonet [!INCLUDE [prod_short](includes/prod_short.md)]. Når vinduet vises, skal du kontrollere, om brugeren har forbindelse, så det passer til det, du bruger til at oprette forbindelse til [!INCLUDE [prod_short](includes/prod_short.md)].

3. Kontroller at kodeenhed 2718 **Page Summary Provider** udgives som en webtjeneste.

    Teams opretter forbindelse til [!INCLUDE [prod_short](includes/prod_short.md)]ved hjælp af et slutpunkt til denne kodeenhed på [!INCLUDE [prod_short](includes/prod_short.md)]-tjenesten. Du kan finde flere oplysninger om udgivelse af webtjenester under [Udgive en webtjeneste](across-how-publish-web-service.md).

4. Din organisation kan også begrænse, at du indsætter hyperlinks i kort. Kontakt administratoren for at få kendskab til de team politikker, der gælder for dig.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Mine hyperlinks udvides nogle gange ikke til et kort 

Et link kan ikke udvides til et kort i følgende situationer:

- Hyperlinket er mål for en side af en type, der ikke repræsenterer en post. Det kan f. eks. være et link til [!INCLUDE [prod_short](includes/prod_short.md)] Rollecenter. Du kan kontrollere sidetypen ved hjælp af side inspektions ruden i webklienten i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger om side inspektion under [inspicere sider ](across-inspect-page.md).
- Hyperlinket er rettet mod en side, som (på et teknisk niveau) ikke er knyttet til en kildetabel i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan kontrollere om en side har en kildetabel ved hjælp af sideinspektionsruden i webklienten i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger om side inspektion under [inspicere sider ](across-inspect-page.md). 
- Teams understøtter ikke linkeksempler i alle funktioner. Når du opretter en chat, at du f. eks. har et møde, eller du er gæst hos en anden organisation.
- Teams afbryder uovervåget forsøg på at vise kortet efter 15 sekunder, f. eks. pga. netværksproblemer.
- Teams kan ikke udvide hyperlinket, hvis du allerede har indsat et hyperlink i den samme meddelelsesboks og har slettet kortet.

Linket skal også indeholde alle de oplysninger, der er nødvendige for at finde posten og få vist det tilsvarende kort. Disse oplysninger omfatter:

- Miljønavnet, ved at medtage det i URL-stien. Hvis du ikke angiver et miljønavn, antager Teams, at du forsøger at få adgang til miljøet med navnet "Produktion".
- Firmanavn ved hjælp af parameteren *Virksomhed=*
- Side-id ved hjælp af parameteren *side=*
- Bogmærket til posten ved hjælp af parameteren *Bookmark=*

Eksempler:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Du kan finde tekniske oplysninger om [!INCLUDE [prod_short](includes/prod_short.md)]-URL-adresser i [webklientens URL-adresse ](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) i [!INCLUDE [prod_short](includes/prod_short.md)]-hjælp til udviklere og it-fagfolk.

## <a name="the-card-is-displayed-in-the-message-compose-box-but-selecting-the-details-button-does-nothing"></a>Kortet vises i meddelelsesboksen, men hvis du vælger knappen detaljer, sker der ingenting. 

Når et hyperlink er udvidet til et kort i boksen meddelelses meddelelse, skal du sende meddelelsen til chatten, før du kan bruge knappen **Detaljer**.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a>Vinduet detaljer åbnes, men der vises en fejlmeddelelse, inden detaljer vises

Dette problem kan skyldes et par ting: manglende tilladelser i [!INCLUDE [prod_short](includes/prod_short.md)] eller webbrowserindstillinger (når der bruges Teams i browseren).

1. Kontroller tilladelserne i [!INCLUDE [prod_short](includes/prod_short.md)].

    Hvis du vil have vist detaljer om et kort [!INCLUDE [prod_short](includes/prod_short.md)], skal du kontrollere licensen og tilladelserne for at få vist den pågældende post og side i det specifikke regnskab og miljø. Hvis du ikke har tilladelse til noget af disse ting, vises standardfejlmeddelelsen [!INCLUDE [prod_short](includes/prod_short.md)] om tilladelserne i vinduet detaljer. 

    Du kan finde flere oplysninger om rettigheder i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md)

2. Kontroller browserindstillingerne, hvis du bruger teams i browseren.

    - Blokeringen af pop op-vinduer i browseren skal enten være deaktiveret eller indstillet til at tillade pop op-vinduer fra domænerne *businesscentral.dynamics.com* eller *bc.dynamics.com*. Du kan finde flere oplysninger om, hvordan du tillader pop op-vinduer i [!INCLUDE [prod_short](includes/prod_short.md)], skal du se [Opsætning af browseren](across-browser-settings.md#popup).
    - Browseren skal have adgang til lokal browser storage for cookies og præferencer, mens du arbejder.
    - Undgå at bruge gæst eller privat browsing, medmindre det er nødvendigt, fordi de sletter eller blokerer noget indhold i nogle browsere.

    Du kan finde flere oplysninger om minimumskrav til browseren i [Minimumskrav til brug af [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams"></a>Jeg har problemer med kameraet eller stedet i grupper 

Når du bruger [!INCLUDE [prod_short](includes/prod_short.md)]-funktioner i vinduet detaljer, som kræver adgang til din placering eller dit enheds kamera, skal du først give dit samtykke til, at teams kan få adgang til disse enhedsfunktioner.  

- For Teams i browseren skal du kontrollere, at browserindstillingerne giver adgang til kamera og placering for https://teams.microsoft.com. 

- For Teams i iOS eller Android skal du kontrollere, at enhedsindstillingerne giver adgang til kamera og placering for Teams-mobilapp. 

Hvis du vil have hjælp til at ændre disse indstillinger, skal du se [Mit kamera virker ikke i Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) i Microsoft Support.

[!INCLUDE [prod_short](includes/prod_short.md)]-appen understøtter ikke placering i Teams-desktopappen. Du kan finde flere oplysninger om placering i [Ofte stillede spørgsmål om Teams](teams-faq.md#location).

Nogle browsere, f. eks. den nye Microsoft Edge, giver dig mulighed for at vælge, hvilket enheds kamera der skal bruges, når enheden understøtter flere kameraer. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>Teams viser blandede sprog for mine kort og kort detaljer 

Hvis kort og kort skal vises ensartet på samme sprog i grupper, skal sproget for team klienten og det sprog, du bruger i [!INCLUDE [prod_short](includes/prod_short.md)]-webklienten, være ens.

- Hvis du vil vide mere om ændring af sproget i grupper, skal du se [Ændre indstillinger i Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) i Microsoft Support. 

- Hvis du vil vide mere om ændring af sproget i [!INCLUDE [prod_short](includes/prod_short.md)], se [Ændre grundlæggende indstillinger – sprog](ui-change-basic-settings.md#language).

Du kan finde flere oplysninger om, hvordan sprog fungerer mellem grupper og [!INCLUDE [prod_short](includes/prod_short.md)], i [Ofte stillede spørgsmål om Teams](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Jeg har redigeret et felt i detalje vinduet, men ændringen blev ikke gemt

De ændringer, du foretager i et felt i detalje vinduerne, gemmes automatisk, når du forlader feltet. Før du lukker vinduet, efter at du har ændret et felt, skal du trykke på tab eller klikke uden for feltet.

## <a name="see-also"></a>Se også

[[!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams Oversigt over integration](across-teams-overview.md)  
[Installér appen [!INCLUDE [prod_short](includes/prod_short.md)] til Microsoft Teams](across-install-app-for-teams.md)  
[Teams, ofte stillede spørgsmål](teams-faq.md)  
[Udvikling af Teams-integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]