---
title: "Servicebogføring | Microsoft Docs"
description: "Servicebogføringsfunktionen gør det muligt at behandle dokumenter effektivt og hele tiden bevare en gennemført kundeservicepolitik. Du kan oprette og opdatere bogførte dokumenter og oprette poster både inden for serviceområdet og i andre moduler for at sikre korrekt opdatering."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d82961b41266f645f87b79555171891cd2ce828f
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="service-posting"></a>Bogføring af tjenesten
Servicebogføringsfunktionen gør det muligt at behandle dokumenter effektivt og hele tiden bevare en gennemført kundeservicepolitik. Du kan oprette og opdatere bogførte dokumenter og oprette poster både inden for serviceområdet og i andre moduler for at sikre korrekt opdatering.  

> [!NOTE]  
>  Nedenfor beskrives servicepostering, uanset hvordan varerne fysisk håndteres på lageret.  
>   
>  På en placering, der ikke er konfigureret til at kræve lagerekspedition, skal du udføre bogføringsprocesserne direkte fra vinduet **Servicelinjer**. På lokationer, der involverer lagerekspedition, udføres de beskrevne bogføringsprocesser, undtagen Send og forbrug, indirekte via forskellige lagerleverancefunktioner afhængigt af konfuguration. Du kan finde flere oplysninger i [Sådan plukkes varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).  

## <a name="ship"></a>Lever  
Med leveringsindstillingen kan du registrere relevante varer og den tid, der er angivet på linjerne i en serviceordre, når du har afsluttet servicen. Der oprettes en bogført leverance, og modulet Lagerbeholdning og andre moduler i [!INCLUDE[d365fin](includes/d365fin_md.md)] opdateres, så det afspejles, at varerne er taget ud af lageret og sendt til kunden. Der oprettes specielt vareposter, værdiposter, serviceposter og garantiposter.  

Hvis lokationen er angivet til at kræve lagerekspedition, sker forsendelse og flytning af servicelinjevarefunktioner på samme måde som for andre kildedokumenter. Den eneste forskel er, at servicelinjevarer kan forbruges eksternt eller internt, hvilket kræver de to forskellige frigivelsesfunktioner.

## <a name="invoice"></a>Faktura  
Du skal bruge faktureringsindstillingen til at udstede en faktura til den kunde, der skal betale for servicen. Det er som regel forskellen mellem det leverede antal, der er registreret vha. funktionen **Bogfør lev.**, og det forbrugte antal, der er registreret vha. funktionen til **bogføring af forbrug**, som er forbundet med faktureringen. Du kan ikke fakturere noget, der ikke er leveret. Når du kører funktionen **Bogfør fakturaer**, opretter du en bogført servicefaktura og opdaterer de dokumenter, der er bogført før, så de er i overensstemmelse med det antal, der er angivet i den udstedte faktura. Som det er tilfældet med andre bogføringsprocedurer, oprettes de relevante poster, inklusive finansposter.  

## <a name="ship-and-invoice"></a>Lever og fakturer  
Med indstillingen Send og fakturer kan du udstede en serviceleverance og en faktura på samme tid.  

## <a name="ship-and-consume"></a>Send og forbrug  
Med indstillingen Send og forbrug, kan du registrere og bogføre varer, omkostninger eller timer, der er anvendt til servicen, men som ikke kan medtages på fakturaen til kunden. Der udstedes ikke en faktura i programmet, men du har mulighed for at udstede både serviceleverance og serviceforbrug samtidig for at afspejle den kendsgerning, at kunden får nogle varer eller timer gratis. De tilsvarende poster oprettes også, så forbruget registreres.  

> [!NOTE]  
>  Proceduren til servicepostering sætter dig i stand til at foretage delvis bogføring. Du kan oprette en delleverance eller en delfaktura ved at udfylde felterne **Lever (antal)** og **Fakturer (antal)** på de enkelte servicelinjer i serviceordrerne, før du bogfører. Bemærk, at du ikke kan oprette en faktura for noget, der ikke er leveret. Dvs., før du kan fakturere, skal der være registreret en leverance, eller du skal vælge at sende og fakturere på samme tid.  

Når bogføringen er færdig, kan du se de bogførte servicedokumenter i de tilsvarende vinduer **Bogført serviceleverance** og **Bogført servicefaktura**. De bogførte poster, der er oprettet, kan ses i de forskellige vinduer med bogførte poster **Finansposter**, **Vareposter**, **Lagerposter**, **Serviceposter**, **Sagsposter** og **Garantiposter**.  

## <a name="to-view-information-about-a-posted-service-document"></a>Sådan får du vist oplysninger om et bogført servicedokument  
Når du bogfører en servicefaktura, en serviceleverance eller en servicekreditnota, overføres oplysningerne i dokumentet til et af vinduerne **Bogført servicefaktura**, **Bogført serviceleverance** eller **Bogført servicekreditnota**. Du kan ikke skrive, ændre eller slette noget i disse vinduer. Du kan udskrive en leverance, faktura eller kreditnota fra disse vinduer.  

I følgende procedure bruges en bogført servicefaktura som eksempel, men der kan anvendes samme fremgangsmåde på bogførte serviceleverancer og bogførte kreditnotaer.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogført servicefaktura**, og vælg derefter det relaterede link.  
2. Åbn den bogførte servicefaktura, som du vil se.  
3. For at få et overblik over den bogførte faktura skal du vælge handlingen **Statistik**.  

    Vinduet **Serviceordrestatistik** åbnes. I vinduet vises der oplysninger som antal, beløb, moms, omkostninger, avance og kundekreditmaksimum for det bogførte dokument.

## <a name="see-also"></a>Se også  
[Sådan gør du: Bogføre serviceordrer](service-how-to-post-service-orders.md)   
[Fremgangsmåde: Oprette serviceordrer](service-how-to-create-service-orders.md)

