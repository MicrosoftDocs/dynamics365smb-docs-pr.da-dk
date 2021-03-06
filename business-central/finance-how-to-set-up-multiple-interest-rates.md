---
title: Sådan angives flere rentesatser
description: Du kan beregne renter med flere rentesatser for en bestemt periode. Renteberegningen sker på samme måde for alle finansielle udgifter , der er kun ændring i rentesatsen for en bestemt periode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 484174bf02377081d9220f9dd4f0b47fdc547c34
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915531"
---
# <a name="set-up-multiple-interest-rates"></a>Angive flere rentesatser
Flere rentesatser bruges til forskellige perioder for forsinkede betalinger i handelstransaktioner. F.eks. angiver det offentlige den maksimale rente, der kan opkræves for en bruger. Denne rentesats kan ændres to gange om året på 1. januar og 1. juli. Rentesatsen mellem virksomheder (B2B) aftales af parterne, og der er ingen grænser for denne kundegruppe. Den annoncerece rente er som regel fire procent højere end den normale bankrente.

Når du opretter rentebetingelser og rykkerbetingelser for forsinket betaling, kan du angive flere rentesatser, så strafgebyret beregnes ud fra forskellige rentesatser i forskellige perioder. Du kan finde flere oplysninger under [Indhente udestående beløb](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Sådan angives flere rentesatser  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rentebetingelser**, og vælg derefter det relaterede link.  
2.  På siden **Rentebetingelser** skal du vælge de krævede økonomiske betingelser og derefter vælge handlingen **Rentesatser**.  
3.  Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Vælg knappen **OK**.  
5.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rykkerbetingelser**, og vælg derefter det relaterede link.  
6.  På siden **Rentebetingelser** skal du vælge de krævede rykkerbetingelser og derefter vælge handlingen **Niveauer**.  
7.  På siden **Rykkerniveauer** skal du markere feltet **Beregn rente**.  

Når du udsteder en rentenota, viser notaen renterne med flere rentesatser for en bestemt tidsperiode. Rentenotaen indeholder også kontaktoplysningerne for kunden, virksomheden, der udsteder rentenotaen, et ekstra beløb og det samlede beløb. Åbningsposten på rentenotaen vises med fed skrift. Renteberegningen beregnes ved brug af flere rentesatser for en bestemt tidsperiode og udskrives efter åbningsposten på rentenotaen.  

## <a name="see-also"></a>Se også  
[Indhente udestående beløb](receivables-collect-outstanding-balances.md)  
[Konfigurere Finans](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]