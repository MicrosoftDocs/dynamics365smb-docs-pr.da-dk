---
title: Designoplysninger – Tilgængelighed i lageret | Microsoft Docs
description: Systemet skal holde en konstant kontrol over varedisponering på lageret, så udgående ordrer kan flyde effektivt og levere optimale leverancer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 670fbfc0f7e576f92ef26e31418d0d44f6262eec
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132077"
---
# <a name="design-details-availability-in-the-warehouse"></a>Designoplysninger: Tilgængelighed i lageret
Systemet skal holde en konstant kontrol over varedisponering på lageret, så udgående ordrer kan flyde effektivt og levere optimale leverancer.  

Tilgængeligheden varierer afhængigt af allokeringer på placeringsniveauet, når lageraktiviteter som pluk og bevægelser forekommer, og når lagerreservationssystemet pålægger begrænsninger, der skal overholdes. En meget kompleks algoritme kontrollerer, at alle betingelser er opfyldt, før der tildeles antal til pluk for udgående forløb.

Hvis en eller flere af betingelserne ikke er opfyldt, kan der vises forskellige fejlmeddelelser, herunder "Der er intet at håndtere" . Meddelelsen "Der er intet at håndtere" kan blive vist af mange forskellige årsager, både i udgående og indgående strømme, hvor en direkte eller indirekte anvendt bilagslinje indeholder feltet **Håndteringsantal**.

> [!NOTE]
> Der bliver snart publiceret oplysninger her om mulige årsager og løsninger til "Der er intet at håndtere". .

## <a name="bin-content-and-reservations"></a>Placeringsindhold og reservationer  
 I en installation af logistik findes vareantal både som lagerposter, i logistikmodulet, og som vareposter i modulet Lagerbeholdning. Disse to typer indeholder forskellige oplysninger om, hvor varer findes, og om de er tilgængelige. Lagerposter definerer en vares tilgængelighed efter placering og placeringstype, samlet kaldet placeringsindhold. Vareposter definerer en varedisponering ved sin reservation til udgående dokumenter.  

 Der findes specielle funktioner i pluk-algoritme til beregning af den mængde, der er disponibel til pluk, når placeringsindholdet er kombineret med reservationer.  

## <a name="quantity-available-to-pick"></a>Mængde, der kan plukkes  
 Hvis for eksempel algoritmen for pluk ikke tager højde for vareantal, der er reserveret til en ventende salgsordreforsendelse, kan disse varer plukkes til en anden salgsordre, der er sendt tidligere, hvilket forhindrer, at det første salg er opfyldt. Hvis du vil undgå denne situation, fratrækker plukalgoritmen antal, der er reserveret til andre udgående dokumenter, antal på eksisterende plukdokumenter og antal, der er plukket, men endnu ikke leveret eller forbrugt.  

 Resultatet vises i feltet **Disp. antal til pluk** på siden **Plukkladde**, hvor feltet beregnes dynamisk. Værdien beregnes også, når brugere opretter lagerpluk direkte for udgående dokumenter. Disse udgående dokumenter kan være salgsordrer, produktionsforbrug eller udgående overflytninger, hvor resultatet er afspejlet i de relaterede antalsfelter, f.eks. **Mgd. at håndtere**.  

> [!NOTE]  
>  Med hensyn til prioriteten af reservationer fratrækkes antallet, der skal reserveres, fra antallet, der er disponibelt til pluk. Hvis det tilgængelige antal i plukplaceringer f.eks. er 5 enheder, men der er 100 enheder på læg-på-lager-placeringer, vises der en fejlmeddelelse, når du prøver at reservere mere end 5 enheder til en anden ordre, fordi det ekstra antal skal være tilgængeligt på plukplaceringer.  

### <a name="calculating-the-quantity-available-to-pick"></a>Beregning af det antal, der er disponibelt til pluk  
 Det antal, der kan plukkes, beregnes sådan:  

 mængde, der kan plukkes = antal i plukplaceringer - antal på pluk og bevægelser – (reserveret antal i plukplaceringer + reserveret antal på pluk og bevægelser)  

 Følgende diagram viser de forskellige elementer i beregningen.  

 ![Disponibel til pluk med reservationsoverlap.](media/design_details_warehouse_management_availability_2.png "Disponibel til pluk med reservationsoverlap")  

## <a name="quantity-available-to-reserve"></a>Antal disponible til reservation  
 Da begreberne om placeringsindhold og reservation eksisterer side om side, skal antallet af varer, der kan reserveres, justeres med fordelinger på udgående lagerdokumenter.  

 Det bør være muligt at reservere alle varer på lager, bortset fra dem, der har startet udgående behandling. Derfor defineres det antal, der kan reserveres, som antallet på alle dokumenter og alle placeringstyper, undtagen følgende udgående mængder:  

-   Antal på uregistrerede plukdokumenter  
-   Antal på forsendelsesplaceringer  
-   Antal til produktionsplaceringer  
-   Antal åbne produktionsplaceringer  
-   Antal til montageplaceringer  
-   Antal på reguleringsplaceringer  

 Resultatet vises i feltet **Beholdning i alt** på siden **Reservation**.  

 På en reservationslinje vises det antal, der ikke kan reserveres, fordi det er fordelt i lageret, i feltet **Allokeret antal på lager** på siden **Reservation**.  

### <a name="calculating-the-quantity-available-to-reserve"></a>Beregning af det antal, der er disponibelt til reservation  
 Det antal, der kan reserveres, beregnes sådan:  

 mængde, der kan reserveres = samlet antal på lager - antal på pluk og bevægelser for kildedokumenter - reserveret antal - antal i udgående placeringer  

 Følgende diagram viser de forskellige elementer i beregningen.  

 ![Disponibel for reservation pr. lagertildeling.](media/design_details_warehouse_management_availability_3.png "Disponibel for reservation pr. lagertildeling")  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
 [Vise varedisponering](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]