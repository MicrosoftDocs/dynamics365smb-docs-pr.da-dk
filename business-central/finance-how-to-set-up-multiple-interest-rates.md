---
title: Sådan angives flere rentesatser
description: Dette emne angiver, hvordan du kan beregne renter med flere rentesatser for en bestemt periode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 1a4a47ef587a4d49c92e63f746a3b973f3f40ad9
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435955"
---
# <a name="set-up-multiple-interest-rates"></a>Angive flere rentesatser
Flere rentesatser bruges til forskellige perioder for forsinkede betalinger i handelstransaktioner. F.eks. angiver det offentlige den maksimale rente, der kan opkræves for en bruger. Denne rentesats kan ændres to gange om året på 1. januar og 1. juli. Rentesatsen mellem virksomheder (B2B) aftales af parterne, og der er ingen grænser for denne kundegruppe. Den annoncerece rente er som regel fire procent højere end den normale bankrente.

Når du opretter rentebetingelser og rykkerbetingelser for forsinket betaling, kan du angive flere rentesatser, så strafgebyret beregnes ud fra forskellige rentesatser i forskellige perioder. Du kan finde flere oplysninger i [Indhente udestående beløb](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Sådan angives flere rentesatser  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rentebetingelser**, og vælg derefter det relaterede link.  
2.  På siden **Rentebetingelser** skal du vælge de krævede økonomiske betingelser og derefter vælge handlingen **Rentesatser**.  
3.  Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Vælg knappen **OK**.  
5.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rykkerbetingelser**, og vælg derefter det relaterede link.  
6.  På siden **Rentebetingelser** skal du vælge de krævede rykkerbetingelser og derefter vælge handlingen **Niveauer**.  
7.  På siden **Rykkerniveauer** skal du markere feltet **Beregn rente**.  

Når du udsteder en rentenota, viser notaen renterne med flere rentesatser for en bestemt tidsperiode. Rentenotaen indeholder også kontaktoplysningerne for kunden, virksomheden, der udsteder rentenotaen, et ekstra beløb og det samlede beløb. Åbningsposten på rentenotaen vises med fed skrift. Renteberegningen beregnes ved brug af flere rentesatser for en bestemt tidsperiode og udskrives efter åbningsposten på rentenotaen.  

## <a name="see-also"></a>Se også  
[Indhente udestående beløb](receivables-collect-outstanding-balances.md)  
[Konfigurere Finans](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]