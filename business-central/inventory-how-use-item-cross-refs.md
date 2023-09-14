---
title: Anvend varereferencer
description: 'Oprette referencer mellem beskrivelser, måleenheder og varianter, som du og din leverandør eller kunde bruger for en vare.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/27/2021
ms.author: bholtorf
---
# Anvend varereferencer

Hvis du køber eller sælger varer, som du og leverandøren eller debitoren bruger forskellige betingelser for, kan du oprette en reference mellem betingelserne for varerne og de betingelser, som kunden eller leverandøren af den pågældende vare bruger. På den måde indsættes leverandørens eller kundens varebeskrivelse, enhed eller variantkode automatisk i de relevante dokumenter, når du udfylder feltet **Varereferencenr.** .  

> [!NOTE]
> [!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]
>
> Ikke alle virksomheder bruger varereferencer. Vi har minimeret rod på sider ved at skjule de relaterede felter og handlinger som standard. Hvis du beslutter dig for at bruge dem, kan du vælge feltet **Brug varereferencer** på siden **Lageropsætning**. Når du har aktiveret varereferencer, er felterne og handlingerne tilgængelige på siderne Varekort, Kreditorkort og Debitorkort samt fra salgs- og købsdokumenter.
>
> I tidligere versioner før 2021-udgivelsesbølge 2 kan administratoren aktivere funktionen *Skriv længere varereferencer* på siden [Funktionsstyring](https://businesscentral.dynamics.com/?page=2610) (linket kræver, at du har en [!INCLUDE [prod_short](includes/prod_short.md)]-lejer). Hvordan du bruger referencer, ændres ikke, men navnene på ting som f.eks. sider og knapper ændres. F.eks. bliver siden **Varens krydshenvisningsposter** til **Varereferenceposter**.

## Sådan begyndes du at bruge elementreferencer

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

1. Vælg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, skriv **Opsætning af Lager**, og vælg derefter det relaterede link.
2. Marker feltet **Brug varereferencer**.

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

## Se også

[Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]