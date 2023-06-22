---
title: Brug fakturering og Business Central
description: 'Løsning, der giver adgang til Microsoft Invoicing, når du har fået Dynamics 365 Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Invoicing, Microsoft 365'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="use-the-same-microsoft--account-in-includeprodshortincludesprodlongmd-and-microsoft-invoicing" />Bruge den samme Microsoft 365-konto i [!INCLUDE[prod_short](includes/prod_long.md)] og Microsoft Invoicing
Når du tilmelder dig en prøveversion af [!INCLUDE[prod_short](includes/prod_short.md)], kan du gå til en 30-dages evalueringsfase, påbegynde et abonnement eller afslutte din brug af [!INCLUDE[prod_short](includes/prod_short.md)]. I alle tilfælde har du måske på et tidspunkt set noget, der hedder **Microsoft Invoicing** og klikket på det. Dette var en app, som var en del af det, der nu hedder Microsoft 365 Business Standard. Dette hed tidligere et Microsoft 365 Business Premium-abonnement. Derfor er det ikke alle, der har set feltet i Microsoft 365.  

Microsoft Invoicing er ikke længere tilgængelig, men hvis du skal logge på Invoicing for at hente dine data, vil du muligvis se en besked om, at du ikke kan få adgang til Microsoft Invoicing, fordi din konto bruges i [!INCLUDE[prod_short](includes/prod_short.md)].  

En lignende meddelelse vises, hvis du installerer mobilappen til Invoicing.  

## <a name="workaround" />Løsning
Invoicing og [!INCLUDE[prod_short](includes/prod_short.md)] har en fælles platform. Det betyder, at du genkendes som en eksisterende bruger af [!INCLUDE[prod_short](includes/prod_short.md)], når du klikker på Invoicing i Microsoft 365 Administration. Det skyldes, at Invoicing ikke kan bruge den samme virksomhed som [!INCLUDE[prod_short](includes/prod_short.md)].  

Så du skal logge på [!INCLUDE[prod_short](includes/prod_short.md)] og omdøbe din eksisterende virksomhed og derefter oprette en ny virksomhed, som du kan bruge i Invoicing. Ingen data flyttes eller overskrives under denne løsningsprocedure.

### <a name="to-rename-your-company" />Sådan omdøber du din virksomhed
1. Log på [!INCLUDE[prod_short](includes/prod_short.md)].
2. I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") og vælge **Mine indstillinger**.
3. I feltet **Virksomhed**, skal du vælge en anden leverandør.
4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **firmaer**, og vælg derefter det relaterede link.  
5. På siden **Virksomheder** skal du vælge **Rediger liste**.  
6. Giv posten *Min virksomhed* et andet navn.  

    Vent nogle minutter. Vi foretager en række ændringer i den underliggende database, og det tager et stykke tid.
7.  Når systemet er klar igen, skal du vælge knappen **Opret ny virksomhed**.  
8.  I den dialogboks, der vises, skal du angive navnet som *Min virksomhed* og vælge indstillingen **Produktion – Kun konfigurationsdata**.  

Der går igen nogle minutter. Når processen er fuldført, kan du få adgang til Invoicing som en del af din Microsoft 365 Business Standard-oplevelse. men kun for at eksportere data, da Invoicing-programmet er udfaset.  

### <a name="what-about-my-data" />Hvad med mine data?
Når du omdøber det oprindelige Min virksomhed, omdøbes de tabeller i databasen, der indeholder din eksisterende [!INCLUDE[prod_short](includes/prod_short.md)]-data, men selve dataene ændres ikke.  

Hvis du bruger både Invoicing og [!INCLUDE[prod_short](includes/prod_short.md)], gemmes dataene i to forskellige beholdere (de to virksomheder). Intet deles, så du skal administrere kunder og varer i begge virksomheder.  

## <a name="see-also" />Se også
[Ofte stillede spørgsmål](across-faq.yml)  
[Opsætning](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
