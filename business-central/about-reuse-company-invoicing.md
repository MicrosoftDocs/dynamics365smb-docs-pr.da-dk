---
title: Bruge fakturering og Business Central | Microsoft Docs
description: Løsning, der giver adgang til Microsoft Invoicing, når du har fået Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Microsoft 365
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 4267dfb550fb4e8ccf2181762b2b5edcbd0fc188
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753563"
---
# <a name="using-the-same-microsoft-365-account-in-prod_short-and-microsoft-invoicing"></a>Bruge den samme MIcrosoft 365-konto i [!INCLUDE[prod_short](includes/prod_long.md)] og Microsoft Invoicing
Når du tilmelder dig en prøveversion af [!INCLUDE[prod_short](includes/prod_short.md)], kan du gå til en 30-dages evalueringsfase, påbegynde et abonnement eller afslutte din brug af [!INCLUDE[prod_short](includes/prod_short.md)]. I alle tilfælde har du måske på et tidspunkt set noget, der hedder **Microsoft Invoicing** og klikket på det. Dette var en app, som var en del af det, der nu hedder Microsoft 365 Business Standard. Dette hed tidligere et Microsoft 365 Business Premium-abonnement. Derfor er det ikke alle, der har set feltet i Microsoft 365.  

Microsoft Invoicing er ikke længere tilgængelig, men hvis du skal logge på Invoicing for at hente dine data, vil du muligvis se en besked om, at du ikke kan få adgang til Microsoft Invoicing, fordi din konto bruges i [!INCLUDE[prod_short](includes/prod_short.md)].  

En lignende meddelelse vises, hvis du installerer mobilappen til Invoicing.  

## <a name="workaround"></a>Løsning
Invoicing og [!INCLUDE[prod_short](includes/prod_short.md)] har en fælles platform. Det betyder, at du genkendes som en eksisterende bruger af [!INCLUDE[prod_short](includes/prod_short.md)], når du klikker på Invoicing i Microsoft 365 Administration. Det skyldes, at Invoicing ikke kan bruge den samme virksomhed som [!INCLUDE[prod_short](includes/prod_short.md)].  

Så du skal logge på [!INCLUDE[prod_short](includes/prod_short.md)] og omdøbe din eksisterende virksomhed og derefter oprette en ny virksomhed, som du kan bruge i Invoicing. Ingen data flyttes eller overskrives under denne løsningsprocedure.

### <a name="to-rename-your-company"></a>Sådan omdøber du din virksomhed
1. Log på [!INCLUDE[prod_short](includes/prod_short.md)].
2. I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") og vælge **Mine indstillinger**.
3. I feltet **Virksomhed**, skal du vælge en anden leverandør.
4. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomheder**, og vælg derefter det relaterede link.  
5. På siden **Virksomheder** skal du vælge **Rediger liste**.  
6. Giv posten *Min virksomhed* et andet navn.  

    Vent nogle minutter. Vi foretager en række ændringer i den underliggende database, og det tager et stykke tid.
7.  Når systemet er klar igen, skal du vælge knappen **Opret ny virksomhed**.  
8.  I den dialogboks, der vises, skal du angive navnet som *Min virksomhed* og vælge indstillingen **Produktion – Kun konfigurationsdata**.  

Der går igen nogle minutter. Når processen er fuldført, kan du få adgang til Invoicing som en del af din Microsoft 365 Business Standard-oplevelse. men kun for at eksportere data, da Invoicing-programmet er udfaset.  

### <a name="what-about-my-data"></a>Hvad med mine data?
Når du omdøber det oprindelige Min virksomhed, omdøbes de tabeller i databasen, der indeholder din eksisterende [!INCLUDE[prod_short](includes/prod_short.md)]-data, men selve dataene ændres ikke.  

Hvis du bruger både Invoicing og [!INCLUDE[prod_short](includes/prod_short.md)], gemmes dataene i to forskellige beholdere (de to virksomheder). Intet deles, så du skal administrere kunder og varer i begge virksomheder.  

## <a name="see-also"></a>Se også
[Ofte stillede spørgsmål](across-faq.md)  
[Opsætning](admin-setup-and-administration.md)  
