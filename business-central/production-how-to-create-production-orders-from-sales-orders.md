---
title: Oprette produktionsordrer fra salgsordrer
description: Flere oplysninger om at oprette produktionsordrer på forskellige måder til producerede varer direkte fra salgsordrer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '99000883, 99000884,'
---
# <a name="create-production-orders-from-sales-orders" />Oprette produktionsordrer fra salgsordrer

Du kan oprette produktionsordrer til producerede varer direkte fra salgsordrer.  

## <a name="to-create-a-production-order-from-a-sales-order" />Sådan oprettes en produktionsordre fra en salgsordre

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Vælg den salgsordre, du vil oprette en produktionsordre for.  
3. Vælg handlingen **Planlægning**. På siden **Salgsordreplanlægning** kan du få vist disponeringen for en salgsordrevare.  
4. Vælg handlingen **Opret prod.ordre**.  
5. Vælg status og ordretype.  
6. Klik på knappen **Ja** for at oprette en eller flere produktionsordrer til de linjer, der har **produktionsordre** i feltet **Genbestillingssystem**.

    > [!NOTE]  
    > Linjer i den oprettede projektproduktionsordre, der har behov for **Prod.ordre** i feltet **Genbestillingssystem**, repræsenterer underliggende produktionsordrer. Når du har oprettet disse produktionsordrer, skal du huske at identificere eventuelle ikke-opfyldte komponentbehov for dem. Brug siden **Ordreplanlægning** eller handlingen **Omplanlæg** til at identificere ikke-opfyldte behov.
    >
    > Når du opretter produktionsordrer for salgsordrer med siden Salgsordreplanlægning, anvendes der ordre-til-ordre-links mellem behov og levering. Når der findes ordre-til-ordre-links, medtager planlægningssystemet ikke tilknyttet forsyning eller lagerbeholdning i udligningsproceduren. Hvis du vil vide mere om afstemning, skal du gå til [ordre-til-ordre-links](design-details-central-concepts-of-the-planning-system.md#order-to-order-links).

## <a name="order-type" />Ordretype

I følgende tabel beskrives to måder, du kan oprette produktionsordrer på.

|Indstilling|Beskrivlse|
|------|-----------|
|Vareordre|En produktionsordre oprettes for hver enkelt behov produktionsordre, der repræsenteres af a linje i vinduet **Salgsordreplanlægning**.|
|Projektordre|En produktionsordre oprettes for hver enkelt behov produktionsordre, der repræsenteres af a linje i vinduet **Salgsordreplanlægning**. Når du bruger projekt ordrer, viser feltet **Kildetype** i produktionsordren **Salgshoved**. Ordren indeholder én linje for hver salgslinjevare, der skal produceres.|

## <a name="see-also" />Se også

[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)  
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
