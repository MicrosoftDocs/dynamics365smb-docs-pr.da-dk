---
title: Bruge fakturering og Business Central | Microsoft Docs
description: "Løsning, der giver adgang til Microsoft Invoicing, når du har fået Dynamics 365 Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 3e2357766d514f30e42869a4f10ede1e66a6fec1
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a>Bruge den samme Office 365-konto i [!INCLUDE[d365fin](includes/d365fin_long_md.md)] og Microsoft Invoicing
Når du tilmelder dig en prøveversion af [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du gå til en 30-dages evalueringsfase, påbegynde et abonnement eller afslutte din brug af [!INCLUDE[d365fin](includes/d365fin_md.md)]. I alle tilfælde kan du, hvis du logger på Office-portalen, se et felt med navnet **Business-center**, som du skal klikke på. Dette er en del af Office 365 Business Premium-abonnementet, så ikke alle ser dette felt i Office-portalen.  

Hvis du får adgang til Business-centeret, kan du se afsnittet **Invoicing**. Hvis du åbner dette afsnit, vises en meddelelse om, at du ikke kan få adgang til Microsoft Invoicing, fordi kontoen bruges i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

En lignende meddelelse vises, hvis du installerer mobilappen til Invoicing.  

## <a name="workaround"></a>Løsning
Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)] har en fælles platform. Det betyder, at du genkendes som en eksisterende bruger af [!INCLUDE[d365fin](includes/d365fin_md.md)], når du klikker på Invoicing i Business center. Det skyldes, at Invoicing ikke kan bruge den samme virksomhed som [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Så du skal logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] og omdøbe din eksisterende virksomhed og derefter oprette en ny virksomhed, som du kan bruge i Invoicing. Ingen data flyttes eller overskrives under denne løsningsprocedure.

### <a name="to-rename-your-company"></a>Sådan omdøber du din virksomhed
1.  Log på dit [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomheder**, og vælg derefter det relaterede link.  
3.  På siden **Virksomheder** skal du vælge knappen **Rediger liste**.  
4.  Giv posten *Min virksomhed* et andet navn.  

    Vent nogle minutter. Vi foretager en række ændringer i den underliggende database, og det tager et stykke tid.
5.  Når systemet er klar igen, skal du vælge knappen **Opret ny virksomhed**.  
6.  I den dialogboks, der vises, skal du angive navnet som *Min virksomhed* og vælge indstillingen **Produktion – Kun konfigurationsdata**.  

Der går igen nogle minutter. Når processen er fuldført, kan du få adgang til Invoicing som en del af din Office 365 Business Premium-oplevelse.  

### <a name="what-about-my-data"></a>Hvad med mine data?
Når du omdøber det oprindelige Min virksomhed, omdøbes de tabeller i databasen, der indeholder din eksisterende [!INCLUDE[d365fin](includes/d365fin_md.md)]-data, men selve dataene ændres ikke.  

Hvis du bruger både Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)], gemmes dataene i to forskellige beholdere (de to virksomheder). Intet deles, så du skal administrere kunder og varer i begge virksomheder.  

## <a name="see-also"></a>Se også
[Ofte stillede spørgsmål](across-faq.md)  
[Opsætning](admin-setup-and-administration.md)  

