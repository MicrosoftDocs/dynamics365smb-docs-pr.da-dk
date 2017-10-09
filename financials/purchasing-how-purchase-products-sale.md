---
title: "Oprette en købsfaktura fra en salgsfaktura for at købe varer til et salg | Microsoft Docs"
description: "Du kan oprette en købsfaktura for en kreditor eller en leverandør fra en salgsfaktura for at købe produkter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 05/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2d7eb238395a0b1060668996fbbc3e13d9dd8a94
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-purchase-items-for-a-sale"></a>Fremgangsmåde: Købe varer til et salg
Fra salgsordrer og salgsfakturaer kan du bruge funktioner til hurtig oprettelse af indkøbsdokumenter for manglende vareantal, der kræves til salget. Du kan bruge to forskellige funktioner afhængigt af dokumenttypen.
|Funktion|Description|
|--------|-----------|
|**Opret købsordrer**|Fra en salgsordre kan du bruge denne funktion til at oprette en købsordre for hver leverandør af varer på salgsordren. Før du opretter købsordrerne, kan du redigere købsantallet. Der foreslås kun ikke-tilgængelige salgsantal.
|**Opret købsfaktura**|Fra en salgsordre og en salgsfaktura opretter denne funktion en købsfaktura for en valgt kreditor for alle linjer eller valgte linjer i salgsdokumentet. Det fulde salgsantal foreslås.|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a>Sådan oprettes en eller flere købsordrer fra en salgsordre
Hvis du vil oprette en købsordre for hvert vareantal, der ikke er tilgængeligt på salgsordren, skal du bruge funktionen **Opret købsordrer**. 

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Suite**. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

1. På startsiden skal du vælge feltet **Igangværende salgsordrer**.
2. Åbn en salgsordre, som du vil købe varer til.
3. Vælg handlingen **Opret købsordrer**.

    Vinduet **Opret købsordrer** åbnes og viser en linje for hver vare på salgsordren. Linjer for både fuldt tilgængeligt salgsantal og ikke-tilgængelige salgsantal (nedtonet) vises som standard. Du kan vælge handlingen **Vis utilgængelige** for kun at få vist linjer for salgsantal, der er ikke tilgængelig.

    Feltet **Købsantal** viser det antal, der ikke er tilgængeligt, som standard.
4. For at købe et andet antal end det antal, der ikke er tilgængeligt, skal du redigere værdien i feltet **Købsantal**.

    > [!NOTE]  
>   Du kan også ændre feltet **Købsantal** på nedtonede linjer, selv om de repræsenterer fuldt tilgængelige salgsantal.
5. Vælg knappen **OK**. 
    
    Der oprettes en indkøbsordre for hver vareleverandør på salgsordren, herunder eventuelle ændringer af antal, du har foretaget i vinduet **Opret købsordrer**.
7. Fortsæt med at behandle købsordrer eller ordrer, for eksempel ved at redigere eller tilføje købsordrelinjer. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md).


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a>Sådan oprettes en købsfaktura fra en salgsordre eller salgsfaktura
Når du vil oprette en enkelt købsfaktura for en eller flere linjer i et salgsdokument, skal du først at vælge, hvilken leverandør du vil købe fra ved at bruge funktionen **Opret købsfaktura**. 

> [!NOTE]  
>   Denne funktion opretter en købsfaktura for det nøjagtige vareantal i det valgte salgsdokument. Hvis du vil ændre købsantallet, skal du redigere købsfakturaen, når den er oprettet.  

1. På startsiden skal du vælge feltet **Igangværende salgsfakturaer**.
2. Åbn en salgsfaktura, som du vil købe varer til.
3. Marker en eller flere fakturalinjer, som du vil bruge på købsfakturaen. Hvis du vil bruge alle salgsfakturalinjer, skal du enten vælge dem alle eller ikke vælge nogen linjer.
4. Vælg handlingen **Opret købsfaktura**.
5. Vælg enten **Alle linjer** eller **Valgte linjer**, og vælg derefter knappen **OK**.  
6. På listen over kreditorer, der vises, skal du vælge den kreditor, du vil købe alle varerne fra, og derefter vælge knappen **OK**.

    Der oprettes en købsfaktura, der indeholder en, flere eller alle linjer på salgsfakturaen.
7. Fortsæt med at behandle købsfakturaen, for eksempel ved at redigere eller tilføje købsfakturalinjer. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md)  
[Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md)  
[Fremgangsmåde: Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

