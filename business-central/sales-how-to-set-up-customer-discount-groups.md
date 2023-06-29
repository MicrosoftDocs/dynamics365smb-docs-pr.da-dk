---
title: Oprette debitorrabatgrupper
description: 'Se, hvordan du opretter debitorrabatgrupper og opretter salgslinjerabatter for disse grupper.'
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 06/08/2022
ms.author: a-reishima
---
# <a name="set-up-customer-discount-groups"></a><a name="set-up-customer-discount-groups"></a>Oprette debitorrabatgrupper

Du kan definere Salgslinjerabatter for en gruppe debitorer i stedet for at udligne dem individuelt.

**Debitorrabatgrupper** fungerer på samme måde som [Debitorprisgrupper](sales-how-to-set-up-customer-price-groups.md), men kan kombineres med varerabatgrupper for hurtigt at angive linjerabatter til mange varer for udvalgte debitorer.

## <a name="create-sales-line-discounts-for-a-customer-group"></a><a name="create-sales-line-discounts-for-a-customer-group"></a>Sådan oprettes salgslinjerabatter for en kundegruppe

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Debitorrabatgrupper**, og vælg derefter det relaterede link.
2. Vælg **Ny** på siden **debitorrabatgrupper** for at oprette en ny rabatgruppe, og angive et navn under kolonnen **Kode** og tilføje en beskrivelse.
3. Vælg handlingen **Naviger**, og vælg **Salgslinjerabatter**.
4. Udfyld **Salgskode** med den rabatgruppe, du har oprettet på forrige side.
5. Udfyld felterne på linjerne med **Type** (vare- eller varerabatgruppe), **Kode**, **Enhedskode** og **Linjerabat %**.
6. Hvis debitorgruppen skal købe et minimumsantal for at opnå rabatten, skal du udfylde feltet **Min. antal**.
7. Angiv evt. **Startdato** og **Slutdato** for rabatgruppen.
8. Hvis det er relevant, kan du også angive **Valutakode** eller **variantkode**, når du [tilpasser kolonnerne](ui-personalization-user.md).

Gentag trin 4-8 for hver vare eller varerabatgruppe, du vil oprette Salgslinjerabat for.

## <a name="assign-a-customer-to-a-discount-group"></a><a name="assign-a-customer-to-a-discount-group"></a>Knytte en kunde til en rabatgruppe

Når du har oprettet kunderabatgrupper, kan du angive kunderabatgruppekoder på kundekortene.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Åbn det relevante **Kundekort** for en kunde, der skal være en del af en kunderabatgruppe.
3. I oversigtspanelet **fakturering** skal du i feltet **Debitorrabatgruppe** vælge gruppekoden.

## <a name="see-also"></a><a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Registrere specialsalgspriser og -rabatter](sales-how-record-sales-price-discount-payment-agreements.md)  
[Konfigurere debitorprisgrupper](sales-how-to-set-up-customer-price-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
