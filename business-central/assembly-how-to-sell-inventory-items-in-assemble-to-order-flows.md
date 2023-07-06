---
title: Sælge lagervarer i montage til ordre-forløb
description: Montage efter ordre-varer samles til salgsordrer via en montageordre.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="selling-inventory-items-in-assemble-to-order-flows"></a><a name="selling-inventory-items-in-assemble-to-order-flows"></a><a name="selling-inventory-items-in-assemble-to-order-flows"></a>Sådan sælges lagervarer i montage efter ordre-forløb

Hvis feltet **Montagepolitik** på varekortet til et montageelement indeholder **Montage efter ordre**, vil standardsalgsordreprocessen forudsætte, at elementet ikke er på lageret, og at det skal monteres til denne specifikke salgsordre. Når du indtaster varen på en salgsordrelinje, opretter [!INCLUDE [prod_short](includes/prod_short.md)] automatisk en montageordre, hvorefter den knyttes til salgsordren. Du kan lære mere om montage efter ordre ved at gå til [Sælge varer, der er samlet til ordre](assembly-how-to-sell-items-assembled-to-order.md). Men hvis en del af salgsordremængden allerede er tilgængelig på lageret, kan du sænke montageordremængden ved at ændre feltet **Antal til montage efter ordre** på salgsordrelinjen.  

Det er relativt sjældent, at virksomheder sælger lagervarer som montage efter ordre-varer. Montage efter ordre-varer er typisk ikke standard. De er tilpasset til at imødekomme specifikke kundebehov. Du kan dog have mængder, der er montage efter ordre på lageret pga. returneringer eller ordreannulleringer. Disse mængder skal plukkes og sælges, før nye samles.  

> [!NOTE]  
> Hvis du vil kontrollere, om montageordrevarer allerede er tilgængelige for montageordrer, skal du bruge faktaboksen **salgslinjedetaljer** på salgsordren.  

Du kan gøre det, når du sælger montageelementer fra lageret, og nogle eller alle mængder er ikke disponible. Du kan angive det manglende antal via en montageordre. Du kan finde flere oplysninger om at sælge lager og montagevarer i [Sælge montage til ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
> Der gælder bestemte regler for feltet **Levér antal** på salgsordrelinjer, der indeholder en kombination af montage til ordre-antal og lagerantal. Hvis du vil vide mere om reglerne, skal du gå til [kombinationsscenarier](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

I denne procedure skal du erstatte montage efter ordre-mængder med lagerantal på en salgsordrelinje. Følgende trin giver en oversigt:

1. Bestemme tilgængelighed.
2. Reduktion af den pågældende mængde fra den tilknyttede montageordre.
3. Reservér lagerbeholdningen for at sikre, at det er plukket og leveret til ordren.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a><a name="to-sell-inventory-items-in-assemble-to-order-flows"></a><a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>Sådan sælges lagervarer i montage efter ordre-forløb

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Oprette en salgsordre. Flere oplysninger om brug af salgsordrer i [Sælge produkter](sales-how-sell-products.md).  
3. På en salgsordrelinje til et montage efter ordre-element i feltet **Antal** skal du angive det ønskede antal.  
4. I faktaboksen **Salgslinjedetaljer** skal du afgøre, om hele eller noget af den påkrævede mængde er tilgængelig.  
5. I feltet **Antal til montage efter ordre** skal du fratrække den disponible mængde, så kun den utilgængelige mængde er samlet til ordren. Feltet **Reserveret antal** faldt tilsvarende og afspejler, at ordre-til-ordre-linket eller -reservation kun gælder for den mængde, der skal samles.  
6. I oversigtspanelet **Linjer** skal du vælge **Funktioner** og derefter vælge handlingen **Reservér**.  
7. På siden **Reservation** skal du markere den eller de finanspostvarelinjer, der indeholder de tilgængelige mængder, vælge handlingen **Reservér fra aktuel linje** og derefter klikke på knappen **OK**.  

    På siden **Salgsordre** viser feltet **Reserveret antal** nu, at hele ordrelinjemængden er reserveret. Feltet **Antal til montage efter ordre** afspejler stadig de undermængder, der skal samles.  

8. Frigiv salgsordren for at gøre varerne tilgængelige til pluk af lagervarer og montage af utilgængelige elementer. Hvis du vil vide mere om montageelementer, skal du gå til [montagevarer](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Feltet **Placeringskode** på salgsordren kan være udfyldt på forhånd i henhold til feltet **Pla.kode til ordremontagelev.** eller feltet **Placeringskode til fra-montage** på lokationskortet. I så fald kan feltet **Placeringskode** på salgsordrelinjen være forkert i denne kombination af mængder til montage efter ordre og montage til lager. Det er en god idé at undersøge feltet **Placeringskode** og kontrollere, at placeringen fungerer for alle mængder. Du kan også angive de to forskellige mængder på separate salgsordrelinjer.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Montagestyring](assembly-assemble-items.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbejde med montagestyklister](assembly-how-work-assembly-boms.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
