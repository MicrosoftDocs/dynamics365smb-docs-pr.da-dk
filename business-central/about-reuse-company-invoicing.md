---
title: Bruge fakturering og Business Central | Microsoft Docs
description: Løsning, der giver adgang til Microsoft Invoicing, når du har fået Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: b04da7a7fa6d831646c6af9f0606afa90dc00bd6
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188848"
---
# <a name="using-the-same-office-365-account-in-d365fin-and-microsoft-invoicing"></a>Bruge den samme Office 365-konto i [!INCLUDE[d365fin](includes/d365fin_long_md.md)] og Microsoft Invoicing
Når du tilmelder dig en prøveversion af [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du gå til en 30-dages evalueringsfase, påbegynde et abonnement eller afslutte din brug af [!INCLUDE[d365fin](includes/d365fin_md.md)]. I alle tilfælde kan du, hvis du logger på Office-portalen, se et felt med navnet **Microsoft Invoicing**, som du skal klikke på. Dette er en del af Office 365 Business Premium-abonnementet, så ikke alle ser dette felt i Office-portalen.  

Hvis du åbner Microsoft Invoicing, vises en meddelelse om, at du ikke kan få adgang til Microsoft Invoicing, fordi kontoen bruges i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

En lignende meddelelse vises, hvis du installerer mobilappen til Invoicing.  

## <a name="workaround"></a>Løsning
Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)] har en fælles platform. Det betyder, at du genkendes som en eksisterende bruger af [!INCLUDE[d365fin](includes/d365fin_md.md)], når du klikker på Invoicing i Office-portalen. Det skyldes, at Invoicing ikke kan bruge den samme virksomhed som [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Så du skal logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] og omdøbe din eksisterende virksomhed og derefter oprette en ny virksomhed, som du kan bruge i Invoicing. Ingen data flyttes eller overskrives under denne løsningsprocedure.

### <a name="to-rename-your-company"></a>Sådan omdøber du din virksomhed
1. Log på [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") og vælge **Mine indstillinger**.
3. I feltet **Virksomhed**, skal du vælge en anden leverandør.
4. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomheder**, og vælg derefter det relaterede link.  
5. På siden **Virksomheder** skal du vælge **Rediger liste**.  
6. Giv posten *Min virksomhed* et andet navn.  

    Vent nogle minutter. Vi foretager en række ændringer i den underliggende database, og det tager et stykke tid.
7.  Når systemet er klar igen, skal du vælge knappen **Opret ny virksomhed**.  
8.  I den dialogboks, der vises, skal du angive navnet som *Min virksomhed* og vælge indstillingen **Produktion – Kun konfigurationsdata**.  

Der går igen nogle minutter. Når processen er fuldført, kan du få adgang til Invoicing som en del af din Office 365 Business Premium-oplevelse.  

### <a name="what-about-my-data"></a>Hvad med mine data?
Når du omdøber det oprindelige Min virksomhed, omdøbes de tabeller i databasen, der indeholder din eksisterende [!INCLUDE[d365fin](includes/d365fin_md.md)]-data, men selve dataene ændres ikke.  

Hvis du bruger både Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)], gemmes dataene i to forskellige beholdere (de to virksomheder). Intet deles, så du skal administrere kunder og varer i begge virksomheder.  

## <a name="see-also"></a>Se også
[Ofte stillede spørgsmål](across-faq.md)  
[Opsætning](admin-setup-and-administration.md)  
