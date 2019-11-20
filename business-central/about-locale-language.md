---
title: Flere sprog og oversættelse | Microsoft Docs
description: Få mere at vide, hvordan sprog og landestandard påvirker din oplevelse i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture
ms.date: 10/22/2019
ms.author: edupont
ms.openlocfilehash: 81377dfe391415c6922cf0dcf00a8c8567ee4c80
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692700"
---
# <a name="changing-language-and-locale"></a>Ændre sprog og landestandard

[!INCLUDE[d365fin](includes/d365fin_md.md)] understøttes på flere forskellige markeder og findes på de sprog, som disse markeder kræver. Dette er et resultat af understøttelse af flere sprog på kørselstidspunktet sammen med understøttelse af lovgivningsmæssige krav i de understøttede markeder. Det betyder, at [!INCLUDE[d365fin](includes/d365fin_md.md)] kan vises på forskellige sprog. Du kan ændre det sprog, der bruges til at få vist tekst, og ændringen sker med det samme, når du er blevet automatisk logget ud og ind igen. Indstillingen gælder for dig og ikke for alle andre i virksomheden.  

Hvis du f.eks. bruger den canadiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du se brugergrænsefladen på engelsk og fransk, men det er stadig den canadiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)] i alle andre aspekter. Det er ikke det samme, som f.eks. [!INCLUDE[d365fin](includes/d365fin_md.md)] i Storbritannien.  

Du kan ændre sproget i brugergrænsefladen ved at gå til siden **Indstillinger**. Du kan finde flere oplysninger under [Ændre grundlæggende indstillinger](ui-change-basic-settings.md#language).  

Ændring af de tekster, der er arkiveret som programdata, er ikke en del af flersprogsfunktionen. Det er et spørgsmål om programdesign. Eksempler på sådanne tekster er navnene på varer på lager eller bemærkningerne om en kunde. Disse teksttyper oversættes altså ikke.  

> [!NOTE]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter kun et enkelt tegnsæt for data. Derfor kan der være nogle tegn, der ikke understøttes i din lejer, og du kan opleve problemer ved hentning af data, der er angivet ved hjælp af et andet tegnsæt. Din lejer understøtter f.eks. muligvis kun engelske og russiske tegn, og hvis du angiver data på et andet sprog, gemmes de muligvis ikke korrekt. Du bør kontakte systemadministratoren for at sikre dig, at du ved, hvilke sprog der understøttes i din [!INCLUDE[d365fin](includes/d365fin_md.md)]-installation.  

## <a name="changing-the-locale"></a>Ændring af landestandarden
Landestandarden adskiller sig fra både sprog og lovgivningsmæssige krav på lokale markeder. Landestandarden bestemmer, hvordan dataene vises med hensyn til kommaseparator, venstre- eller højrejustering og visse andre indstillinger. Landestandarden bestemmer også nogle af systemelementerne i browseren, f.eks. handlingen til at oprette en ny vare på en liste.  

Du kan ændre landestandarden under den browserfane, du bruger til at arbejde i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ændringen gælder kun for dig og ikke for andre brugere i virksomheden.  

> [!IMPORTANT]  
>  Når du ændrer landestandarden, vises der en lang række sprog og landestandarder. Men indstillingen for landestandard bruges i den aktuelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Du kan ændre landestandarden ved at gå til siden **Mine indstillinger**. Du kan finde flere oplysninger under [Ændre grundlæggende indstillinger](ui-change-basic-settings.md).  

## <a name="application-version"></a>Programversion

Du kan kontrollere, hvilken version af [!INCLUDE [prodshort](includes/prodshort.md)] din virksomhed er baseret på, på siden **Hjælp og support**. Hvis du vil basere en virksomhed på en anden version, kan administratoren oprette et nyt produktionsmiljø. Du kan finde flere oplysninger i [Oprette et nyt produktionsmiljø](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) i Indhold til udviklere og it-eksperter.  

## <a name="languages-of-the-included365finincludesd365fin_mdmd-help"></a>Sprog i [!INCLUDE[d365fin](includes/d365fin_md.md)] Hjælp
Indholdet af Hjælp til den grundlæggende funktionalitet i [!INCLUDE[d365fin](includes/d365fin_md.md)] udgives til webstedet Microsoft Docs og findes på en række forskellige sprog. Hvis du åbner dokumenter fra [!INCLUDE[d365fin](includes/d365fin_md.md)], vises indholdet på dit eget sprog. Hvis en bestemt side ikke endnu er tilgængelig på dit eget sprog, vises den på engelsk.

### <a name="how-do-i-change-the-language"></a>Hvordan kan jeg ændre sproget?
Det er nemt – rul til bunden af webbrowsersiden, og vælg globussymbolet i nederste venstre hjørne.

> [!NOTE]  
> Listen viser alle sprog, der understøttes af webstedet Microsoft Docs. [!INCLUDE[d365fin](includes/d365fin_md.md)] findes i et begrænset antal lande/områder, men indholdet af Hjælp gøres tilgængeligt på flere sprog. Indholdet af Hjælp er ikke tilgængeligt på alle sprog, der understøtter webstedet for Microsoft Docs.

## <a name="see-also"></a>Se også

[Ressourcer til hjælp og support](product-help-and-support.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Introduktion](product-get-started.md)  
