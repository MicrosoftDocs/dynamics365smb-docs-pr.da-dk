---
title: "Sådan angives flere rentesatser"
description: "Du kan beregne renter med flere rentesatser for en bestemt periode. Renteberegningen sker på samme måde for alle finansielle udgifter , der er kun ændring i rentesatsen for en bestemt periode."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0af01fe46f6b7df1149825c35a9fc0cc19482403
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-multiple-interest-rates"></a>Angive flere rentesatser
Flere rentesatser bruges til forskellige perioder for forsinkede betalinger i handelstransaktioner. F.eks. angiver det offentlige den maksimale rente, der kan opkræves for en bruger. Denne rentesats kan ændres to gange om året på 1. januar og 1. juli. Rentesatsen mellem virksomheder (B2B) aftales af parterne, og der er ingen grænser for denne kundegruppe. Den annoncerece rente er som regel fire procent højere end den normale bankrente.

Når du opretter rentebetingelser og rykkerbetingelser for forsinket betaling, kan du angive flere rentesatser, så strafgebyret beregnes ud fra forskellige rentesatser i forskellige perioder. Du kan finde flere oplysninger under [Indhente udestående beløb](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Sådan angives flere rentesatser  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Rentebetingelser**, og vælg derefter det relaterede link.  
2.  I vinduet **Rentebetingelser** skal du vælge de krævede økonomiske betingelser og derefter vælge handlingen **Rentesatser**.  
3.  Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Vælg knappen **OK**.  
5.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Rykkerbetingelser**, og vælg derefter det relaterede link.  
6.  I vinduet **Rentebetingelser** skal du vælge de krævede rykkerbetingelser og derefter vælge handlingen **Niveauer**.  
7.  I vinduet **Rykkerniveauer** skal du markere feltet **Beregn rente**.  

Når du udsteder en rentenota, viser notaen renterne med flere rentesatser for en bestemt tidsperiode. Rentenotaen indeholder også kontaktoplysningerne for kunden, virksomheden, der udsteder rentenotaen, et ekstra beløb og det samlede beløb. Åbningsposten på rentenotaen vises med fed skrift. Renteberegningen beregnes ved brug af flere rentesatser for en bestemt tidsperiode og udskrives efter åbningsposten på rentenotaen.  

## <a name="see-also"></a>Se også  
[Indhente udestående beløb](receivables-collect-outstanding-balances.md)  
[Konfigurere Finans](finance-setup-finance.md)

