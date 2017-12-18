---
title: Oprette og administrere katalogvarer | Microsoft Docs
description: "Beskriver, hvordan du handler med ikke-lagervarer eller varer, der ikke indgår i lagerbeholdningen."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b9256944295880d6ec9dad916eb9632b9d5f7c20
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# Fremgangsmåde: Arbejde med katalogvarer
Du kan tilbyde bestemte varer til dine kunder, som du ikke vil lagerføre, før du begynder at sælge dem. Når du vil begynde at lagerføre sådanne varer, kan du konvertere dem til normale varekort på to måder.

* Opret en ny varekort ud fra en skabelon for et katalogvarekort.
* Vælg en katalogvare fra en salgsordrelinje af typen **Vare** med et tomt **Nummer*-felt. Der oprettes automatisk et varekort for katalogvaren.

> [!NOTE]  
>   Du kan ikke vælge en katalogvare fra vinduet **Salgsfaktura**. Du kan vælge en katalogvare fra vinduet **Salgstilbud**, men katalogvaren konverteres ikke til en almindelig vare, når du bruger funktionen **Lav ordre**.

En katalogvare har typisk varenummeret fra den leverandør, som leverer den. Hvis du vil aktivere konvertering af et katalogvarekort til et normalt varekort, skal du først angive, hvordan leverandørens varenumre skal konverteres til dine egne varenumre.   

## Sådan oprettes en katalogvare
Katalogvarekort indeholder meget færre oplysninger end normale varekort, da du kun bruger til at give tilbud og andre formål. Derfor skal de konverteres til normale varekort, før du kan bogføre salgstransaktioner for dem.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Katalogvarer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Sådan angiver du, hvordan katalogvare konverteres til din egen nummerering
Hvis du vil aktivere konvertering af et katalogvarekort til et normalt varekort, skal du først angive, hvordan leverandørens varenummerering skal konverteres til dit eget varenummerformat.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Katalogvareopsætning**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.

## Sådan konverteres en katalogvare til en almindelig vare
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Katalogvarer**, og vælg derefter det relaterede link.
2. Åbn kortet for en katalogvare, som du vil konvertere til en almindelig vare.
3. I vinduet **Katalogvarekort** skal du vælge handlingen **Opret vare**.

Der oprettes et nyt varekort, der er udfyldt på forhånd med oplysninger fra katalogvaren og en relevant vareskabelon. Du kan derefter udfylde eller redigere felterne på det nye varekort efter behov. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md).

## Sådan sælges en katalogvare og konverteres den til en almindelig vare
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**. Udfyld felterne i oversigtspanelet **Generelt** for enhver salgsordre. Du kan finde flere oplysninger i [Fremgangsmåde: Sælge produkter](sales-how-sell-products.md).
3. På en ny salgslinje skal du vælge **Vare** i feltet **Type**, men lade feltet **Nummer** være tomt.
4. Vælg handlingen **Linje**, og vælg derefter handlingen **Vælg katalogvarer**.

    Katalogvaren konverteres til en almindelig vare. Der oprettes et nyt varekort, der er udfyldt på forhånd med oplysninger fra katalogvaren og en relevant vareskabelon.
5. I vinduet **Katalogvarer** skal du vælge den katalogvare, som du vil sælge, og derefter vælge knappen **OK**.
6. Når salgsordren er fuldført, skal du vælge handlingen **Bogfør**.

Du kan derefter udfylde eller redigere felterne på det nye varekort efter behov. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md).

> [!NOTE]  
>   Der oprettes automatisk en varereferencepost for kreditoren til varen mellem leverandørens varenummer og dit nye varenummer.

## Se også
[Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md)  
[Sådan oprettes specialordrer](sales-how-to-create-special-orders.md)|  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

