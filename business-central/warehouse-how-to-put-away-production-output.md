---
title: Lægge produktionsoutput på lager
description: 'Denne artikel beskriver, hvordan du lægger produktionsafgangen på lager.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# <a name="put-away-production-or-assembly-output"></a>Lægge produktions- eller montageoutput på lager

Den måde, du lægger afgang på lager fra produktion, afhænger af, hvordan lagerstedet er sat op som en lokation. Flere oplysninger i [Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md).  

I en grundlæggende lagerkonfiguration for det indgående flow (læg-på-lager) skal du aktivere følgende indstillinger på **siden Lokation kort**  lokationen for lokationen:

* Til produktion i **produktionsproduktionslageret. skal** du vælge **Læg-på-lager (lager)**.
* Læg-på-lager understøttes ikke for montageprocesser. Du bogfører en montageordre for at registrere afgang. Hvis du bruger placeringer, kan du flytte varer mellem placeringer senere. Du kan finde flere oplysninger i [Flytte varer ad hoc i grundlæggende lageropsætninger](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  
* For projekter er læg-på-lager ikke relevant.

I avancerede lageropsætninger, hvor en lokation kræver læg-på-lager, kan du oprette et internt læg-på-lager-dokument eller et bevægelsesdokument for at lægge afgangen på lager.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Sådan lægges produktionsafgang på lager med en læg-på-lager-aktivitet

Det første trin til at lægge afgange på lager er at oprette den indgående lageranmodning. Denne anmodning oplyser lagerstedet om, at produktions- eller montageordreafgangen er klar til at blive lagt på lager.

### <a name="to-create-the-inbound-warehouse-request"></a>Sådan opretttes den indgående lageranmodning

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Frigivet produktionsordre**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Opret indgående lageranmodning** på den produktionsordre, der er klar til at blive lagt på lager.  

> [!NOTE]  
> Du kan også oprette en indgående lageranmodning ved at vælge feltet **Opret indgående anmodning**, når du opdaterer produktionsordren. Flere oplysninger i [Omplanlægge eller forny produktionsordrer direkte](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-away-output-with-an-inventory-put-away"></a>Sådan lægges afgang på lager med en læg-på-lager-aktivitet

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Læg-på-lager (lager)**, og vælg derefter det relaterede link.  
2. Opret en ny læg-på-lager-aktivitet. Flere oplysninger i [Lægge varer på lager med Læg-på-lager (lager)](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Du kan få adgang til produktionsordreafgangen ved at vælge handlingen **Hent kildedokumenter** og derefter vælge den frigivne produktionsordre.  
4. Udfyld læg-på-lager-linjerne efter behov.
5. Når linjerne er klar til at blive bogført, skal du vælge handlingen **Bogfør**. Når bogføringen opretter lagerposterne, bogfører afgangen af varerne.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

Du kan også oprette et **Læg-på-lager (lager)** direkte fra den frigivne produktionsordre. Flere oplysninger i [Lægge varer på lager med Læg-på-lager (lager)](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Når du bogfører en læg-på-lager-aktivitet [!INCLUDE [prod_short](includes/prod_short.md)] , antages det, at alle operationer bogføres i overensstemmelse med standardruten. Dvs. Afgangsantallet bogføres i overensstemmelse med den seneste operation. Du kan bruge afgangskladde til at bogføre afvigelser i afgangsantal og opstillings- og operationstid. Hvis du skal bogføre delvist, efter du har oprettet læg-på-lager, kan du gøre dette under opstillingstid og antal for alle operationer undtagen den sidste. Læg-på-lager-aktiviteten styrer den sidste operation.  

Hvis du kun har brug for at bogføre opstillings- eller operationstiden for den sidste operation, skal du angive afgangsantallet for den sidste operation til 0. Du kan vælge overhovedet ikke at bogføre den sidste linje ved at slette den.

## <a name="to-put-away-assembly-and-production-output-in-advanced-warehouse-configurations"></a>Sådan lægges montage og produktionsafgang på lager i avancerede lageropsætninger

Når du bogfører produktions- eller montageordreafgang på et lagersted, der bruger styret læg-på-lager og pluk, flyttes afgangen til den placering, der er defineret i produktions- eller montageordren. Du kan få mere at vide om forskellige måder at flytte varer på lagerstedet med avancerede konfigurationer ved at gå til [Flyt varer i avancerede lagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Du kan ikke angive kildedokumentnummeret, f.eks. prod.ordrenr., i dokumenterne intern læg-på-lager, læg-på-lager eller bevægelse i disse to procedurer.  

## <a name="see-also"></a>Se også

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
