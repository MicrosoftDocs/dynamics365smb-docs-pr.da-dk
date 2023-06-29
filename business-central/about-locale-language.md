---
title: Flere sprog og oversættelse
description: 'Få mere at vide om, hvordan sprog og geografisk område påvirker din oplevelse i Business Central. Skift sproget i brugergrænsefladen ved at gå til siden Indstillinger.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'language, locale, localization, culture, region, regional settings'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="changing-language-and-region"></a><a name="changing-language-and-region"></a>Ændre sprog og geografisk område

[!INCLUDE[prod_short](includes/prod_short.md)] fås på mange markeder og sprog i hele verden. På de markeder, hvor [!INCLUDE[prod_short](includes/prod_short.md)] er tilgængelig, er der lovmæssige funktioner, som kan hjælpe virksomheder med lovmæssige forpligtelser. [!INCLUDE[prod_short](includes/prod_short.md)] kan vises på forskellige sprog. Du kan endda ændre det sprog, der bruges til at vise tekst. Ændringen sker med det samme, når du du automatisk er blevet logget af og på igen. Indstillingen gælder for dig og ikke for alle andre i virksomheden.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Du bruger f. eks. den canadiske version af [!INCLUDE[prod_short](includes/prod_short.md)]. Det betyder, at du kan se brugergrænsefladen på engelsk, tysk, fransk eller et andet sprog, men det er stadig den canadiske version af [!INCLUDE[prod_short](includes/prod_short.md)]. Det er ikke det samme som f.eks [!INCLUDE[prod_short](includes/prod_short.md)] i Tyskland, hvor funktionaliteten er tilpasset dette markeds krav.  

Du kan ændre sproget i brugergrænsefladen ved at gå til siden **Indstillinger**. Du kan finde flere oplysninger i [Ændre grundlæggende indstillinger](ui-change-basic-settings.md#language). 

> [!NOTE]  
> Valget af sprog nulstilles til indstillingen på din Microsoft 365-profil, hvis administratoren synkroniserer brugere fra Microsoft 365 til [!INCLUDE[prod_short](includes/prod_short.md)].

Du kan ikke ændre de tekster, der er gemt som programdata. Eksempler på sådanne tekster er navnene på varer på lager eller bemærkningerne om en kunde. Disse teksttyper oversættes altså ikke.  

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] understøtter kun et enkelt tegnsæt for data. Derfor kan der være nogle tegn, der ikke understøttes i dit miljø, og du kan opleve problemer ved hentning af data, der er angivet ved hjælp af et andet tegnsæt. Dit miljø understøtter f.eks. muligvis kun engelske og russiske tegn. Hvis du angiver data i et andet sprog, gemmes de derfor muligvis ikke korrekt. Du bør kontakte systemadministratoren for at sikre dig, at du ved, hvilke sprog der understøttes i din [!INCLUDE[prod_short](includes/prod_short.md)]-installation.  

## <a name="changing-your-region-setting"></a><a name="changing-your-region-setting"></a>Ændre områdeopsætning

Det geografiske område adskiller sig fra både sprog og lovgivningsmæssige krav på lokale markeder. Området bestemmer, hvordan dataene vises med hensyn til f.eks. kommaseparator, og hvordan teksten justeres til venstre eller højre. Området bestemmer også nogle af systemelementerne i browseren, f.eks. handlingen til at oprette en ny vare på en liste.  

Du kan ændre området under den browserfane, du bruger til at arbejde i [!INCLUDE[prod_short](includes/prod_short.md)]. Ændringen gælder kun for dig og ikke for andre brugere i virksomheden.  Valget af område nulstilles til indstillingen på din Microsoft 365-profil, hvis administratoren synkroniserer brugere fra Microsoft 365 til [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]  
> Når du ændrer området, vises der en lang række sprog og områder. Sproget påvirkes dog ikke af det område, du vælger.  

Du kan ændre området ved at gå til siden **Mine indstillinger**. Du kan finde flere oplysninger i [Ændre grundlæggende indstillinger](ui-change-basic-settings.md).  

## <a name="changing-the-region-setting-for-customers-contacts-and-vendors"></a><a name="changing-the-region-setting-for-customers-contacts-and-vendors"></a>Ændre områdeindstillinger for debitorer, kontakter og leverandører

I nogle virksomheder bruges der en ekstern tjeneste, som validerer adresseoplysninger i deres land eller område. Når du har brug for at opdatere adresseoplysninger, er den strukturerede fremgangsmåde dog ikke altid lige noget for scenarierne. Business Central tilbyder en mere fleksibel måde at indtaste adresseoplysninger på.

Hvis du på siden **Finansopsætning** aktiverer indstillingen **Kræv lande-/områdekode i adresse** til/fra vil ændringer i feltet **Lande-/områdekode** på adresser for debitorer, kontakter eller leverandører automatisk nulstille værdierne i andre adressefelter.

## <a name="application-version"></a><a name="application-version"></a>Programversion

Du kan kontrollere, hvilken version af [!INCLUDE[prod_short](includes/prod_short.md)] din virksomhed er baseret på, på siden **Hjælp og support**. Hvis du vil basere en virksomhed på en anden version, kan administratoren oprette et nyt produktionsmiljø. Du kan finde flere oplysninger i [Oprette et nyt produktionsmiljø](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) i Indhold til udviklere og it-eksperter.  

## <a name="languages-of-the--help"></a><a name="languages-of-the--help"></a>Sprog i [!INCLUDE[prod_short](includes/prod_short.md)] Hjælp

Hjælp-indholdet til standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] udgives til Microsoft Learn. Indholdet er tilgængeligt på forskellige sprog. Hvis du åbner dokumentationen fra [!INCLUDE[prod_short](includes/prod_short.md)], vises indholdet på dit eget sprog. Hvis en bestemt side som standard endnu ikke er tilgængelig på dit eget sprog, vises den på engelsk.

### <a name="how-do-i-change-the-language-of-the-microsoft-learn-site"></a><a name="how-do-i-change-the-language-of-the-microsoft-learn-site"></a>Hvordan kan jeg ændre sproget for Microsoft Learn-webstedet?

Det er nemt – rul til bunden af webbrowsersiden, og vælg globussymbolet i nederste venstre hjørne.

> [!NOTE]  
> Listen viser alle sprog, der understøttes af webstedet Microsoft Learn. [!INCLUDE[prod_short](includes/prod_short.md)] fås i et begrænset antal lande/områder, og indholdet i [!INCLUDE [prod_short](includes/prod_short.md)]-hjælpen er ikke tilgængelig på alle de sprog, som Microsoft Learn-webstedet understøtter.

## <a name="see-also"></a><a name="see-also"></a>Se også

[Ressourcer til hjælp og support](product-help-and-support.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Blive køreklar](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
