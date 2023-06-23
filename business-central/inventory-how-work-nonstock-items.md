---
title: Oprette og håndtere katalogvarer
description: 'Lær, hvordan du sælger de varer, du ikke beholder, på listen over varer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.keywords: non-inventoriable
ms.search.forms: '5725, 5726, 5732'
---

# <a name="work-with-catalog-items" />Arbejde med katalogvarer

Katalogvarer er varer, som du ikke administrerer i [!INCLUDE[prod_short](includes/prod_short.md)], før du sælger dem. Når du bruger funktionen **Vælg katalogelement** til at føje en katalogvare til en linje i en salgsordre, et tilbud eller en rammesalgsordre, konverteres katalogvaren til en almindelig vare.

> [!NOTE]  
> Du kan ikke vælge en katalogvare på siden **Salgsfaktura**.

En katalogvare har typisk varenummeret fra den leverandør, som leverer den. Inden du kan konvertere en katalogvare til en normal vare, skal du angive, hvordan leverandørens varenumre skal konverteres til vare nummereringen. Du kan finde flere oplysninger om varenummerering i [Sådan angiver du, hvordan katalogvarenumre konverteres til din egen nummerering](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Katalogvarer må ikke forveksles med ikke-lagervarer, som er almindelige varer, som har typen **Ikke-lager** for at holde dem ude af tilgængeligheds- og omkostningsberegninger, f.eks. fordi de kun anvendes internt af programmet og har lave omkostninger. Du kan lære mere om varer, der ikke er lager, ved at gå til [Om varetyper](inventory-about-item-types.md).

## <a name="create-a-catalog-item" />Oprette en katalogvare

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **katalogvarer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering" />Angive, hvordan katalogvarenumre konverteres til din egen nummerering

Inden du kan konvertere en katalogvare til en normal vare, skal du angive, hvordan leverandørens varenumre skal konverteres til strukturen, du bruger til varenumre.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af katalogvare**, og vælg derefter det relaterede link.
2. I feltet **Nummer format** skal du vælge den ønskede indstilling.

## <a name="convert-a-catalog-item-to-a-normal-item" />Konvertere en katalogvare til en almindelig vare

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **katalogvarer**, og vælg derefter det relaterede link.
2. Åbn kortet for en katalogvare, som du vil konvertere til en almindelig vare.
3. På siden **Katalogvarekort** skal du vælge handlingen **Opret vare**.

Der oprettes et nyt varekort, der er udfyldt på forhånd med oplysninger fra katalogvaren og en vareskabelon. Du kan redigere oplysningerne om den nye vare, hvis det er nødvendigt. Hvis du vil vide mere om oprettelse af varer, skal du gå til [Registrere nye varer](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item" />Sådan sælges en katalogvare og konverteres til en almindelig vare

Følgende proces bruger en salgsordre, men fremgangsmåden er den samme for rammesalgsordrer og tilbud.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**. Udfyld felterne i oversigtspanelet **Generelt** for enhver salgsordre. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).
3. På en ny salgslinje skal du vælge **Vare** i feltet **Type**, men lade feltet **Nummer** være tomt.
4. Vælg handlingen **Linje**, og vælg derefter handlingen **Vælg katalogvarer**.
5. På siden **Katalogvarer** skal du vælge den katalogvare, som du vil sælge, og derefter vælge knappen **OK**.
6. Når salgsordren er fuldført, skal du vælge handlingen **Bogfør**.

> [!NOTE]  
> Der oprettes automatisk en varereference for kreditoren til varen mellem leverandørens varenummer og dit nye varenummer. Hvis du vil vide mere om varereferencer, skal du gå til [Brug af varereferencer](inventory-how-use-item-cross-refs.md).

## <a name="see-related-microsoft-trainingtrainingmodulescreate-sales-documents-dynamics-365-business-central" />Se relateret [Microsoft-træning](/training/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Registrere nye varer](inventory-how-register-new-items.md)  
[Oprette specialordrer](sales-how-to-create-special-orders.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
