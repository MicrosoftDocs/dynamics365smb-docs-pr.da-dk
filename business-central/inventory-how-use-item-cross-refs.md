---
title: Anvend varereferencer
description: 'Oprette referencer mellem beskrivelser, måleenheder og varianter, som du og din leverandør eller kunde bruger for en vare.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/02/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Anvend varereferencer

Hvis du køber eller sælger varer, som du og leverandøren eller debitoren bruger forskellige betingelser for, kan du oprette en reference mellem betingelserne for varerne og de betingelser, som kunden eller leverandøren af den pågældende vare bruger. På den måde indsættes leverandørens eller kundens varebeskrivelse, enhed eller variantkode automatisk i de relevante dokumenter, når du udfylder feltet **Varereferencenr.** .  

## Sådan oprettes en varereference

1. Vælg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for en vare, som du vil oprette reference for.
3. Vælg handlingen **Varereferencer**.

     Hvis du ikke kan finde handlingen **Varereferencer**, skal du vælge at få vist flere indstillinger og derefter finde den under **Relateret** > **Vare**.
  
4. På en ny linje på siden **Varereferenceposter** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Følgende procedurer beskriver, hvordan du kan angive varereference på en købsordre. Lignende trin gælder for salgsdokumenter og andre købsdokumenter.  

## Sådan angiver du en kreditors varebeskrivelse på et dokument

1. Vælg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, skriv **Købsordrer**, og vælg derefter det relaterede link.
2. Opret en købsordre for den leverandør, som du angav en varereference for ovenfor.
3. Opret en købslinje for den vare, som du angav en varereference for ovenfor.
4. I feltet **Varereferencenr.** skal du vælge den relevante varereference og derefter vælge knappen **OK**.

Feltet **Beskrivelse** på linjen overskrives med kreditorens varebeskrivelse, som blev oprettet i varereferenceposten. Hvis varereferencen indeholder en variantkode eller en enhed, kopieres disse værdier også til dokumentet.  

## Scan stregkoder med Business Central-mobilapp

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Følgende tabel viser de sider, der understøtter stregkodescanning af varereferencer fra mobilappen [!INCLUDE [prod_short](includes/prod_short.md)].

|Side  |Feltværdi, du kan scanne  |
|---------|---------|
|Varereference     | Referencenr.        |
|Varekladdelinje     | Varereferencenr.        |
|Lageropgørelsesordrelinje     |Varereferencenr.         |
|Købslinje     |   Varereferencenr.      |
|Salgslinje     | Varereferencenr.        |

## Se også

[Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
