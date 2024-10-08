---
title: Behandle delleverancer
description: Leverancer af salgsordrer kan behandles i Business Central med delleverancer vha. felterne Afsendelsesadvis og Lever (antal).
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'shipping advice, partial shipments, partial deliveries, trade, customer sales order'
ms.date: 02/14/2024
ms.author: bholtorf
ms.reviewer: bholtorf
---
# <a name="process-partial-shipments"></a>Behandle delleverancer

I en delvis leverance bliver en ordre ikke leveret på én gang. Af en ordre på 100 enheder kan du f.eks. sende 40 med det samme og 60 senere. Der kan foretages et ubegrænset antal leverancer i en ordre.

Men før du kan bruge delleverancer i [!INCLUDE [prod_short](includes/prod_short.md)], skal du angive, at debitoren accepterer delleverancer, når du angiver feltet **Afsendelsesadvis** på **debitorkortet**. Hvis kunden kun accepterer komplette leverancer, men anmoder om eller aftaler med en delvis leverance for en bestemt salgsordre, kan du ændre feltet **Afsendelsesadvis** inden bogføringen.

Som standard angives [!INCLUDE [prod_short](includes/prod_short.md)] feltet på **debitorkort**-siden som **delvis**, hvilket tillader delvis leverance. Men hvis feltet er indstillet til at angive **Fuldført**, vises feltet **Lever (antal)** blokeret i salgsordrer for den pågældende kunde.

[!INCLUDE [order-ship-invoice_md](includes/order-ship-invoice.md)]

## <a name="see-also"></a>Se også

[Sælge produkter med en debitorsalgsordre](sales-how-sell-products.md)  
[Afsende varer](warehouse-how-ship-items.md)  
[Foretage direkte leveringer](sales-how-drop-shipment.md)  
[Salg](sales-manage-sales.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Opsætning](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
