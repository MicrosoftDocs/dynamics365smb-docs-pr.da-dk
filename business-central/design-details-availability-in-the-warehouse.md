---
title: Designoplysninger - Tilgængelighed i lageret
description: 'Lære mere om de forskellige faktorer, der påvirker Varedisponering på lagerstedet.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="design-details-availability-in-the-warehouse"></a>Designoplysninger: Tilgængelighed i lageret

Hold styr på varedisponeringen for at sikre, at udgående ordrer flyder effektivt, og at leveringstiderne er optimale.  

Tilgængelighed kan variere afhængigt af flere faktorer. Eksempler:

* Fordelinger på placeringsniveau, når der sker lageraktiviteter, f. eks. pluk og bevægelser.
* Når der i lager reservations system opkræves restriktioner for at overholde betingelserne.

[!INCLUDE [prod_short](includes/prod_short.md)] kontrollerer, at alle betingelser er opfyldt, før der tildeles antal til pluk for udgående forløb.

Når betingelserne ikke er opfyldt, vises fejlmeddelelser. Én typisk meddelelse er standardindstillingen "intet at håndtere". . Meddelelsen kan blive vist af mange forskellige årsager, både i udgående og indgående strømme, hvor en direkte eller indirekte anvendt bilagslinje indeholder feltet **Håndteringsantal**.

## <a name="bin-content-and-reservations"></a>Placeringsindhold og reservationer

Vareantal findes både som lagerposter og som vareposter på lager. Disse to typer indeholder forskellige oplysninger om, hvor varer findes, og om de er tilgængelige. Lagerposter definerer en vares tilgængelighed efter placering og placeringstype, samlet kaldet placeringsindhold. Vareposter definerer en varedisponering ved sin reservation til udgående dokumenter.  

[!INCLUDE [prod_short](includes/prod_short.md)] beregner det antal, der er disponibelt til plukning, når placeringsindhold skal kobles fra reservationer.  

## <a name="quantity-available-to-pick"></a>Mængde, der kan plukkes

[!INCLUDE [prod_short](includes/prod_short.md)] reserverer varer til ventende salgsordreforsendelser, så de ikke plukkes til andre salgsordrer, der leveres tidligere. [!INCLUDE [prod_short](includes/prod_short.md)] trækker antal af varer, der allerede behandles, som følger:

* Antal, der er reserveret til andre udgående dokumenter.
* Antal i eksisterende plukdokumenter.
* Antal plukket, men endnu ikke leveret eller forbrugt.  

Resultatet vises i feltet **Disp. antal til pluk** på siden **Plukkladde**, hvor feltet beregnes dynamisk. Værdien beregnes også, når brugere opretter lagerpluk direkte for udgående dokumenter. Der findes følgende udgående kildedokumenter:

* Salgsordrer
* Produktionsforbrug
* Udgående overflytninger

Resultatet er tilgængeligt i disse dokumenter i antalsfelterne, f. eks. feltet **Håndteringsantal** .  

> [!NOTE]  
> Med hensyn til prioriteten af reservationer fratrækkes antallet, der skal reserveres, fra antallet, der er disponibelt til pluk. Hvis det tilgængelige antal i plukplaceringer f.eks. er 5 enheder, men der er 100 enheder på læg-på-lager-placeringer, vises der en fejlmeddelelse, når du prøver at reservere mere end 5 enheder til en anden ordre, fordi det ekstra antal skal være tilgængeligt på plukplaceringer.  

### <a name="calculating-the-quantity-available-to-pick"></a>Beregning af det antal, der er disponibelt til pluk

[!INCLUDE [prod_short](includes/prod_short.md)] beregner det antal, der kan plukkes, sådan:  

mængde, der kan plukkes = antal i plukplaceringer - antal på pluk og bevægelser – (reserveret antal i plukplaceringer + reserveret antal på pluk og bevægelser)  

Følgende diagram viser de forskellige elementer i beregningen.  

![Disponibel til pluk med reservationsoverlap.](media/design_details_warehouse_management_availability_2.png "Disponibel til pluk med reservationsoverlap")  

## <a name="quantity-available-to-reserve"></a>Antal disponible til reservation

Da begreberne om placeringsindhold og reservation eksisterer side om side, skal antallet af varer, der kan reserveres, justeres med fordelinger på udgående lagerdokumenter.  

Du kan reservere alle lagervarer, undtagen varer, som den udgående behandling er startet for. Den mængde, der kan reserveres, defineres som antallet på alle dokumenter og alle placeringstyper. Følgende udgående antal er undtagelser:  

* Antal på uregistrerede plukdokumenter  
* Antal på forsendelsesplaceringer  
* Antal til produktionsplaceringer  
* Antal åbne produktionsplaceringer  
* Antal til montageplaceringer  
* Antal på reguleringsplaceringer  

Resultatet vises i feltet **Beholdning i alt** på siden **Reservation**.  

På en reservationslinje vises det antal, der ikke kan reserveres, fordi det er fordelt i lageret, i feltet **Allokeret antal på lager** på siden **Reservation**.  

## <a name="check-whether-items-are-available-for-picking"></a>Kontrollere, om varer er tilgængelige til pluk

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

### <a name="calculating-the-quantity-available-to-reserve"></a>Beregning af det antal, der er disponibelt til reservation

[!INCLUDE [prod_short](includes/prod_short.md)] beregner det antal, der kan reserveres, sådan:  

mængde, der kan reserveres = samlet antal på lager - antal på pluk og bevægelser for kildedokumenter - reserveret antal - antal i udgående placeringer  

Følgende diagram viser de forskellige elementer i beregningen.  

![Disponibel for reservation pr. lagertildeling.](media/design_details_warehouse_management_availability_3.png "Disponibel for reservation pr. lagertildeling")  

## <a name="see-also"></a>Se også

[Oversigt over Warehouse Management](design-details-warehouse-management.md)
[Vise varer, der er disponible](inventory-how-availability-overview.md)
[Plukke til produktion, samling eller jobs i avancerede lageropsætninger](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
