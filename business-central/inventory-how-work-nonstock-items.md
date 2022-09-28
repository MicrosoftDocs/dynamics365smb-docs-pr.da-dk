---
title: Oprette og håndtere katalogvarer
description: Beskriver, hvordan du sælger de varer, du ikke beholder, på listen over varer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.search.forms: 5725, 5726, 5732
ms.date: 06/20/2022
ms.author: bholtorf
ms.openlocfilehash: deeca03327afa4b231cb9b4ce23088334fa50153
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532102"
---
# <a name="work-with-catalog-items"></a>Arbejde med katalogvarer

Katalogvarer er varer, som du ikke administrerer i [!INCLUDE[prod_short](includes/prod_short.md)], før du sælger dem. Når du bruger funktionen **Vælg katalogelement** til at føje en katalogvare til en linje i en salgsordre eller et tilbud, konverteres katalogvaren til en almindelig vare.

> [!NOTE]  
> Du kan ikke vælge en katalogvare på siden **Salgsfaktura**.

En katalogvare har typisk varenummeret fra den leverandør, som leverer den. Inden du kan konvertere en katalogvare til en normal vare, skal du angive, hvordan leverandørens varenumre skal konverteres til vare nummereringen. Du kan finde flere oplysninger i [Sådan angiver du, hvordan katalogvarenumre konverteres til din egen nummerering](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Katalogvarer må ikke forveksles med ikke-lagervarer, som er almindelige varer, som har typen **Ikke-lager** for at holde dem ude af tilgængeligheds- og omkostningsberegninger, f.eks. fordi de kun anvendes internt af programmet og har lave omkostninger. Du kan finde flere oplysninger i [Om varetyper](inventory-about-item-types.md).

## <a name="create-a-catalog-item"></a>Oprette en katalogvare

Katalogvarekort indeholder meget færre oplysninger end normale varekort, da du kun bruger til at give tilbud og andre formål. Derfor skal de konverteres til normale varekort, før du kan bogføre salgstransaktioner for dem.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **katalogvarer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Angive, hvordan katalogvarenumre konverteres til din egen nummerering

Inden du kan konvertere en katalogvare til en normal vare, skal du angive, hvordan leverandørens varenumre skal konverteres til vare nummereringen.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af katalogvare**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.

## <a name="convert-a-catalog-item-to-a-normal-item"></a>Konvertere en katalogvare til en almindelig vare

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **katalogvarer**, og vælg derefter det relaterede link.
2. Åbn kortet for en katalogvare, som du vil konvertere til en almindelig vare.
3. På siden **Katalogvarekort** skal du vælge handlingen **Opret vare**.

Der oprettes et nyt varekort, der er udfyldt på forhånd med oplysninger fra katalogvaren og en relevant vareskabelon. Du kan derefter udfylde eller redigere felterne på det nye varekort efter behov. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Sådan sælges en katalogvare og konverteres til en almindelig vare

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**. Udfyld felterne i oversigtspanelet **Generelt** for enhver salgsordre. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).
3. På en ny salgslinje skal du vælge **Vare** i feltet **Type**, men lade feltet **Nummer** være tomt.
4. Vælg handlingen **Linje**, og vælg derefter handlingen **Vælg katalogvarer**.

    Katalogvaren konverteres til en almindelig vare. Der oprettes et nyt varekort, der er udfyldt på forhånd med oplysninger fra katalogvaren og en relevant vareskabelon.
5. På siden **Katalogvarer** skal du vælge den katalogvare, som du vil sælge, og derefter vælge knappen **OK**.
6. Når salgsordren er fuldført, skal du vælge handlingen **Bogfør**.

Du kan derefter udfylde eller redigere felterne på det nye varekort efter behov. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).

> [!NOTE]  
> Der oprettes automatisk en varereference for kreditoren til varen mellem leverandørens varenummer og dit nye varenummer. Du kan finde flere oplysninger i [Bruge varereferencer](inventory-how-use-item-cross-refs.md).

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Registrere nye varer](inventory-how-register-new-items.md)  
[Oprette specialordrer](sales-how-to-create-special-orders.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
