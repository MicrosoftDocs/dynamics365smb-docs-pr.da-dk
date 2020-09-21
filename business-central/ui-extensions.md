---
title: Installation af udvidelser til tilpasning af Business Central | Microsoft Docs
description: Få mere at vide om tilføjelse af funktioner og tilpasning af Business Central ved at installere udvidelser.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765917"
---
# <a name="customizing-business-central-using-extensions"></a>Tilpasse Business Central ved brug af udvidelser

Du kan ændre [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at installere udvidelser, der f.eks. tilføjer funktioner, ændrer funktionsmåder eller giver dig adgang til nye onlinetjenester.

> [!NOTE]
> Hvis du vil installere udvidelser fra AppSource eller tilføje udvidelser pr. lejer, skal du have de rigtige rettigheder. Du skal enten være medlem af brugergruppen D365 EXTENSION MGMT, eller du skal have rettighedssættet D365 EXTENSION MGMT. Hvis du er administrator, kan du tildele brugergrupper og rettigheder til andre brugere i virksomheden.<br /><br />
Hvis du vil bruge de funktioner, der findes i en udvidelse, f. eks. åbne sider, køre rapporter, vælge handlinger osv., skal du være tildelt de rettighedssæt, der er installeret som en del af udvidelsen.

> [!IMPORTANT]  
> Overførsel af udvidelser pr. lejer og installation af AppSource-udvidelser understøttes ikke via siden **Udvidelsesstyring** til lokale installationer.

Når du starter [!INCLUDE[d365fin](includes/d365fin_md.md)] første gang, er der allerede installeret nogle udvidelser for dig. Med tiden gøres flere udvidelser tilgængelige for dig, og du kan derefter vælge, om du vil bruge udvidelsen eller ej.

Microsoft leverer f.eks. en udvidelse, der giver integration med PayPal Payments Standard. Denne udvidelse er installeret som standard.
Men hvis en anden udvidelse, som tilbyder integration med en anden betalingstjeneste, stilles til rådighed, kan du installere nye udvidelse og derefter vælge, hvilken af to de tjenester du vil bruge.  

Du kan administrere udvidelserne på siden **Udvidelsesstyring**. Du kan åbne siden fra Start. Du kan også vælge ikonet **Søg efter side eller rapport** ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), skrive **Udvidelse** i øverste højre hjørne og derefter vælge det relaterede kæde. Du kan finde flere oplysninger under [Installere og fjerne udvidelser](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Hvis du mener, at du skal have adgang til en udvidelse, men ikke kan finde de relevante funktioner, skal du vælge siden **Udvidelsesstyring** – hvis filtypen ikke er angivet der, kan du installere den som beskrevet i følgende afsnit.  

> [!NOTE]  
> Der findes ingen nye udvidelser i AppSource umiddelbart efter, at vi har oplyst om en opdatering. Du kan holde øje med udvidelser på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="see-also"></a>Se også

[Udvidelse af Dynamics 365 Business Central](about-develop-extensions.md)  
[Business Central-udvidelser fra andre leverandører](ui-extensions-other.md)  
[Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Aktivere debitorbetaling via PayPal](sales-how-enable-payment-service-extensions.md)  
[Overførsel af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfiguration af den britiske GetAddress.io-postnummerudvidelse](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]-udvidelser fra andre leverandører](ui-extensions-other.md)  
[Introduktion](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
