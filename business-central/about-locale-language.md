---
title: "Flere sprog og oversættelse | Microsoft Docs"
description: "Få mere at vide, hvordan sprog og landestandard påvirker din oplevelse i Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 8ec773b74bf258d6bb09ad82c7afec6e93c98869
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="changing-language-and-locale"></a>Ændre sprog og landestandard
[!INCLUDE[d365fin](includes/d365fin_md.md)] understøttes på flere forskellige markeder og findes på de sprog, som disse markeder kræver. Dette er et resultat af understøttelse af flere sprog på kørselstidspunktet sammen med understøttelse af lovgivningsmæssige krav i de understøttede markeder. Det betyder, at [!INCLUDE[d365fin](includes/d365fin_md.md)] kan vises på forskellige sprog. Du kan ændre det sprog, der bruges til at få vist tekst, og ændringen sker med det samme, når du er blevet automatisk logget ud og ind igen. Indstillingen gælder for dig og ikke for alle andre i virksomheden.  

Hvis du f.eks. er canadier, kan du se brugergrænsefladen på engelsk og fransk, men det er stadig den canadiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)] i alle andre aspekter. Det er ikke det samme, som f.eks. [!INCLUDE[d365fin](includes/d365fin_md.md)] i Storbritannien.  

> [!NOTE]  
>  Ændring af sproget understøttes ikke i øjeblikket i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ændring af de tekster, der er arkiveret som programdata, er ikke en del af flersprogsfunktionen. Det er et spørgsmål om programdesign. Eksempler på sådanne tekster er navnene på varer på lager eller bemærkningerne om en kunde. Disse teksttyper oversættes altså ikke.  

> [!NOTE]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter kun et enkelt tegnsæt for data. Derfor kan der være nogle tegn, der ikke understøttes i din lejer, og du kan opleve problemer ved hentning af data, der er angivet ved hjælp af et andet tegnsæt. Din lejer understøtter f.eks. muligvis kun engelske og russiske tegn, og hvis du angiver data på et andet sprog, gemmes de muligvis ikke korrekt. Du bør kontakte systemadministratoren for at sikre dig, at du ved, hvilke sprog der understøttes i din [!INCLUDE[d365fin](includes/d365fin_md.md)]-installation.  

## <a name="changing-the-locale"></a>Ændring af landestandarden
Landestandarden adskiller sig fra både sprog og lovgivningsmæssige krav på lokale markeder. Landestandarden bestemmer, hvordan dataene vises med hensyn til kommaseparator, venstre- eller højrejustering og visse andre indstillinger. Landestandarden bestemmer også nogle af systemelementerne i browseren, f.eks. handlingen til at oprette en ny vare på en liste.  

Du kan ændre landestandarden under den browserfane, du bruger til at arbejde i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ændringen gælder kun for dig og ikke for andre brugere i virksomheden.  

> [!IMPORTANT]  
>  Når du ændrer landestandarden, vises der en lang række sprog og landestandarder. Men indstillingen for landestandard bruges i den aktuelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Du kan ændre landestandarden ved at gå til vinduet **Mine indstillinger**. Du kan finde flere oplysninger under [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).  

## <a name="languages-of-the-included365finincludesd365finmdmd-help"></a>Sprog i [!INCLUDE[d365fin](includes/d365fin_md.md)] Hjælp
Indholdet af Hjælp til den grundlæggende funktionalitet i [!INCLUDE[d365fin](includes/d365fin_md.md)] udgives til webstedet Microsoft Docs og findes på en række forskellige sprog. Hvis du åbner dokumenter fra [!INCLUDE[d365fin](includes/d365fin_md.md)], vises indholdet på dit eget sprog. Hvis en bestemt side ikke endnu er tilgængelig på dit eget sprog, vises den på engelsk.

### <a name="how-do-i-change-the-language"></a>Hvordan kan jeg ændre sproget?
Det er nemt – Rul til bunden af webbrowservinduet, og vælg globussymbolet i nederste venstre hjørne.

> [!NOTE]  
> Listen viser alle sprog, der understøttes af webstedet Microsoft Docs. [!INCLUDE[d365fin](includes/d365fin_md.md)] findes i et begrænset antal lande/områder, men indholdet af Hjælp gøres tilgængeligt på flere sprog. Indholdet af Hjælp er ikke tilgængeligt på alle sprog, der understøtter webstedet for Microsoft Docs.

## <a name="see-also"></a>Se også  
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
[Introduktion](product-get-started.md)  

