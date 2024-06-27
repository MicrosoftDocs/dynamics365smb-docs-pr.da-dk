---
title: Foretage direkte forsendelser
description: 'Beskriver, hvordan du opretter en salgsordre, der er knyttet til en købsordre for at muliggøre levering direkte fra leverandøren til kunden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: direct shipment
ms.date: 05/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="make-drop-shipments"></a>Foretage direkte forsendelser

En direkte levering er en levering af varer fra en af dine leverandører direkte til din kunde.

Når en salgsordre er markeret til direkte levering, og du opretter en købsordre, der angiver kunden i feltet **Leveres til**, **Debitoradresse**, kan du sammenkæde de to dokumenter for at give kreditoren besked om at levere direkte til debitoren.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Sådan oprettes en salgsordre til direkte levering

Hvis du vil forberede en direkte levering, skal du oprette en salgsordre for en vare og angive på salgslinjen, at salget kræver direkte levering.

1. Opret en salgsordre for en vare. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).
2. Markér afkrydsningsfeltet **Direkte levering** på salgsordrelinjen for den direkte levering. I feltet **Indkøbskode** kan du alternativt vælge en indkøbskode, hvor der er en markering i feltet **Direkte levering**.

> [!TIP]
> Som standard er afkrydsningsfeltet Direkte levering og Indkøbskodefeltet ikke tilgængeligt på linjerne. Hvis det ikke er tilfældet, kan du tilføje dem ved at tilpasse den sektionen af siden, der indeholder linjerne. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Sådan oprettes købsordren til direkte levering

Hvis du vil forberede en direkte levering, skal du angive på købsordren, at den skal sendes til kunden og ikke til dig selv.

1. Opret en indkøbsordre. Udfyld ikke felter på linjerne. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md).
2. Vælg **Debitoradresse** i feltet **Leveres til**.
3. Vælg den kunde, du sælger til, i feltet **Debitor**.
4. Vælg handlingen **Direkte leveringer**, og vælg derefter handlingen **Hent salgsordre**.
5. På siden **Salgsoversigt** skal du vælge den salgsordre, du forberedt i [Sådan oprettes en salgsordre til direkte levering](#to-create-a-sales-order-for-drop-shipment).
6. Vælg knappen **OK**.

Linjeoplysningerne på salgsordren indsættes på købsordrelinjen(erne).

Du kan nu fortælle din leverandør, at varerne leveres direkte til kunden. Du kan f. eks. sende dem som e-mail.

Hvis kreditoren angiver yderligere oplysninger, som f.eks. et sporingsnummer eller lignende oplysninger, kan du tilføje disse oplysninger på en købsordrelinje af typen bemærkning. Hvis du vil føje en bemærkning til en linje, skal du vælge **Bemærkning** i feltet **Type** og derefter angive oplysningerne i feltet **Beskrivelse** .  

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Sådan oprettes flere købsordrer til direkte leveringer

Du kan også bruge indkøbskladden til at oprette købsordren. Fordelen ved at bruge indkøbskladden er, at den kan oprette købsordrer til alle udestående direkte leveringer, så du ikke behøver at oprette dem en ad gangen. Det betyder, at du ikke behøver at oprette hver ordre for sig.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Indkøbskladder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Direkte leveringer**, og vælg derefter handlingen **Hent salgsordre**.
3. Hvis det er nødvendigt, kan du angive filterkriterier for de ordrer, du vil modtage, og derefter vælge knappen **OK** .
4. Gennemgå købsordrelinjerne, og vælg den leverandør, der leverer varerne, i feltet **Leverandørnr.**.
5. Vælg handlingen **Udfør aktionsmeddelelse** for at konvertere linjerne til en købsordre.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Sådan får du vist den tilknyttede købsordre fra salgsordren

Markér salgsordrelinjen til direkte levering, vælg handlingen **Ordre**, vælg handlingen **Direkte levering**, og vælg derefter handlingen **Købsordre**.

## <a name="to-post-a-drop-shipment"></a>Sådan bogfører du en direkte levering

Når kreditoren har leveret varerne, kan du bogføre salgsordren som leveret. Du kan også bogføre købsordren, men kun med indstillingen **Modtag**, indtil salgsordren er faktureret.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.
2. Åbn den salgsordre, du oprettede i [Sådan oprettes en salgsordre til direkte levering](#to-create-a-sales-order-for-drop-shipment)(sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
3. I feltet **Levér (antal)** skal du angive, hvor mange varer af ordreantallet der skal leveres, hele eller en del af ordreantallet.
4. Vælg handlingen **Bogfør** eller **Bogfør og send**.
5. Vælg enten indstillingen **Levér** for at fakturere senere, eller vælg indstillingen **Levér og fakturer** for at fakturere med det samme.

> [!TIP]
> Husk, at du skal bogføre købsordrefakturaen.

## <a name="see-also"></a>Se også

[Oprette specialordrer](sales-how-to-create-special-orders.md)  
[Købe varer til et salg](purchasing-how-purchase-products-sale.md)  
[Sælge produkter](sales-how-sell-products.md)  
[Registrere køb](purchasing-how-record-purchases.md)  
[Salg](sales-manage-sales.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
