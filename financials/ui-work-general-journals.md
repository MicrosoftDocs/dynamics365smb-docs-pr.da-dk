---
title: Arbejde med finanskladder | Microsoft Docs
description: "Få at vide, hvordan finanskladder fungerer."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/03/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 13257a5d82d742d92fb22da9da7ff7f773d7d2f8
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="working-with-general-journals"></a>Arbejde med finanskladder
Du bruger finanskladder til at bogføre økonomisk transaktioner på finanskonti og andre konti, f.eks. bank-, debitor- og kreditorkonti. Når du bogfører via en finanskonto, oprettes der altid poster i finanskonti. Det gælder også, når du bogfører f.eks. en kladdelinje på en debitorkonto, fordi der bogføres en post på en finanskonto for tilgodehavende via en bogføringsgruppe.

[!INCLUDE[d365fin](includes/d365fin_md.md)] har ikke-finanskladder som f.eks. varekladde og lageropgørelseskladde, men disse kladder vises ikke i brugergrænsefladen.

De oplysninger, du angiver i en kladde, er midlertidige og kan ændres, mens de er i kladden. Når du bogfører kladden, overføres oplysningerne til poster på individuelle konti, hvor de ikke kan ændres. Du kan imidlertid annullere udligningen af bogførte poster, og du kan bogføre tilbageførsels- eller rettelsesposter.

## <a name="journal-templates-and-batches"></a>Kladdetyper og -navne
Der er forskellige finanskladdetyper. Hver kladdetype er repræsenteret af et dedikeret vindue med bestemte funktioner og de felter, der kræves for at understøtte disse funktioner, f.eks. vinduet **Betalingsudligningskladde** til behandling af bankbetalinger og vinduet **Udbetalingskladde** til betaling af kreditorer.

**Bemærk!** Hvis du eksporterer betalingsfiler til banken fra betalingskladden, skal du markere afkrydsningsfeltet **Tillad eksport af betaling** ud for den pågældende kladde i vinduet **Finanskladdenavne**. Du kan finde flere oplysninger i [Fremgangsmåde: Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).

For hver kladdetype kan du angive din egen private kladde som kladdenavn. F.eks. kan du angive din egen kladdetype som udbetalingskladden med dit personlige layout og dine indstillinger.

Et eksempel på en personlig indstilling, som du kan definere i dit finanskladdenavn, er at få systemet til at hjælpe med at udfylde beløbsfelter. Hvis du markerer afkrydsningsfeltet **Foreslå modkontobeløb** på linjen for dit kladdenavn i vinduet **Finanskladdenavne**, udfyldes feltet **Beløb** på f.eks. finanskladdelinjer for samme bilagsnummer automatisk med den værdi, der er nødvendig for at afstemme dokumentet. Du kan finde flere oplysninger under [Lade [!INCLUDE[d365fin](includes/d365fin_md.md)] foreslå værdier](ui-let-system-suggest-values.md).

## <a name="main-accounts-and-balancing-accounts"></a>Hovedkonti og modkonti
Hvis du har oprettet modkonti for kladdenavnene, udfyldes modkontoen automatisk, når du udfylder **Kontonr.** . Hvis ikke, skal du udfylde både feltet **Kontonr.** og feltet **Modkonto** manuelt. Et positivt beløb i feltet **Beløb** debiteres på hovedkontoen og krediteres på modkontoen. Et negativt beløb krediteres på hovedkontoen og debiteres på modkontoen.

**Bemærk**: Moms beregnes separat for hovedkontoen og modkontoen, så der kan bruges forskellige momsprocentsatser.

## <a name="recurring-journals"></a>Gentagelseskladder
En gentagelseskladde er en finanskladde med særlige felter til administration af transaktioner, som bogføres ofte med få eller ingen ændringer. Med disse felter til gentagelsestransaktioner kan du bogføre både faste og variable beløb. Du kan også angive automatiske tilbageførselsposter for dagen efter bogføringsdatoen og bruge allokeringsnøgler sammen med gentagelsesposterne.

## <a name="see-also"></a>Se også
[Fremgangsmåde: Bruge fordelingsnøgler i finanskladder](ui-how-use-allocation-keys-general-journals.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

