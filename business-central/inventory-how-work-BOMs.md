---
title: Arbejde med styklister
description: 'Du opretter en montagestykliste eller produktionsstykliste for at angive de komponenter eller ressourcer, der kræves for at sammensætte den vare, som styklisten repræsenterer.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bills of material, assembly BOM, production BOM,'
ms.search.form: null
ms.date: 09/26/2022
ms.author: a-reishima
---
# <a name="work-with-bills-of-material" />Arbejde med styklister

Du kan bruge styklister til at strukturere overordnede varer, der skal samles fra andre varer eller fremstilles af ressourcer eller produktionsressourcer fra komponenter.

## <a name="assembly-boms-or-production-boms" />Montagestykliste eller produktionsstyklister

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter to forskellige typer styklister:

| Styklistetype | Generelle kategori | Eksempel |
| -------- | ---------------- | ------- |
| [Montagestyklister](assembly-how-work-assembly-boms.md) | Lagersted/montage | Elementer, der består af andre varer, monteret med grundlæggende eller ingen ressourcer. |
| [Produktionsstyklister](production-how-to-create-production-boms.md) | Produktion | Varer, der består af forskellige komponenter og halvfabrikata, som er produceret i et arbejdscenter eller en produktionsressource. |

Du kan bruge montageordrer til at oprette slutvarer fra komponenter i en enkel proces, der kan udføres af en eller flere grundlæggende ressourcer, som ikke er produktions- eller arbejdscentre, eller uden nogen ressourcer. En montageproces kunne f.eks. være at plukke to vinflasker og én kaffesæk og pakke dem som en gave.  

En montagestykliste er masterdata, der definerer, hvilke komponentvarer der indgår i en monteret færdigvare, og hvilke ressourcer der bruges til at montere montageelementet. Når du angiver et montageelement og et antal i hovedet på en ny montageordre, udfyldes montageordrelinjerne automatisk i henhold til montagestyklisten med én montageordrelinje pr. komponent eller ressource. Flere oplysninger i [Montagestyring](assembly-assemble-items.md).

Du kan bruge produktionsordrer til at oprette slutvarer fra komponenter i en kompleks proces, der kræver en produktionsrute og arbejdscentre eller produktionsressourcer, som repræsenterer produktionskapacitet. F.eks. kunne en produktionsproces være at klippe stålplader i én handling, svejse dem i den næste operation og male færdigvaren i den sidste operation. Flere oplysninger i [Produktion](production-manage-manufacturing.md).

En produktionsstykliste er masterdata, der definerer en produktionsvare og de komponenter, der går ind i den. Ved montageelementer skal produktionsstyklisten certificeres og tildeles til produktionsvaren, før elementet kan bruges i en produktionsordre. Når du angiver produktionsvaren på en produktionsordrelinje, enten manuelt eller ved at opdatere ordren, bliver produktionsstyklisteindholdet komponenterne i produktionsordren. Flere oplysninger i [Oprette produktionsstyklister](production-how-to-create-production-boms.md).

Begrebet ressourcer i produktionen er langt mere avanceret end i montagestyring. Arbejdscentre og produktionsressourcer fungerer som ressourcer, og produktionstrin repræsenteres af operationer, der er tildelt til ressourcer i produktionsruter. Få mere at vide i artiklen [Oprette ruter](production-how-to-create-routings.md).

Både montageordrer og produktionsordrer kan knyttes direkte til salgsordrer. Du kan dog kun bruge montageordrer til at tilpasse færdigvaren direkte til en debitoranmodning med salgsordren.

## <a name="see-also" />Se også

[Arbejde med montagestyklister](assembly-how-work-assembly-boms.md)  
[Oprette produktionsstyklister](production-how-to-create-production-boms.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Administrere produktvarianter](inventory-item-variants.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Produktion](production-manage-manufacturing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
