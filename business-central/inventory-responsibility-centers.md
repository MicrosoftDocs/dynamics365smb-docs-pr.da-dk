---
title: Sådan arbejder du med ansvarscentre | Microsoft Docs
description: Ansvarscentre gør det muligt at håndtere administrative centre. Et ansvarscenter kan være et kostcenter, et overskudscenter eller et investeringscenter eller et andet administrativt center, der er defineret i firmaet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: edupont
ms.openlocfilehash: 97904add0f97be5a93bec5e53b45179fadfddffb
ms.sourcegitcommit: 0fb6952376d853a878ed33257e73aadc03b95572
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968329"
---
# <a name="work-with-responsibility-centers"></a>Arbejde med ansvarscentre

Ansvarscentre gør det muligt at håndtere administrative centre. Et ansvarscenter kan være et kostcenter, et resultatcenter eller et investeringscenter eller et andet administrativt center, der er defineret i firmaet. Eksempler på ansvarscentre er et salgskontor, en indkøbsafdeling for flere lokationer og et kontor for anlægsplanlægning. Ved hjælp af disse funktioner kan firmaer f.eks. oprette brugerspecifikke visninger af salgs- og købsdokumenter, der udelukkende er relateret til et bestemt ansvarscenter.  

Det kan være svært at holde styr på alle aktiviteter i en virksomhed, men driften kan styres både fleksibelt og optimalt med funktionerne til flere lokationer og ansvarscentre.

Flere lokationer betyder, at en virksomhed kan nøjes med at bruge en enkelt database til styring af lagerbeholdning på flere lokationer. I denne sammenhæng er hhv. lokationer og lagervarer de to vigtigste begreber. En lokation defineres som et sted, der varetager den rent fysiske håndtering og placering af varer. Dette begreb er bredt nok til også at omfatte lokationer som fabriks- eller produktionsanlæg samt distributionscentre, lagerbygninger, udstillingslokaler og servicevogne. En lagervare defineres som en vare på en bestemt lokation og/eller som en variant. Når en virksomhed med flere lokationer bruger lagervarer, kan der tilføjes oplysninger om genbestilling, adresser og visse økonomiske bogføringsrelaterede oplysninger på lokationsniveau. Dermed bliver det muligt at genbestille varianter af den samme vare til hver enkelt lokation og at bestille varer til de forskellige lokationer på basis af genbestillingsoplysninger, der er specifikke for den enkelte lokation.  

## <a name="to-set-up-a-responsibility-center"></a>Sådan oprettes et ansvarscenter

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ansvarscentre**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Hvis du bruger ansvarscentre til at administrere din virksomhed, kan være nyttigt at have et standardansvarscenter for din virksomhed.
4. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomhedsoplysninger**, og vælg derefter det relaterede link.
5. I feltet **Ansvarscenter** skal du angive en ansvarscenterkode.

Denne ansvarskode vil blive brugt på alle købs-, salgs- eller servicedokumenter, hvis bruger, debitor eller kreditor ikke har noget standardansvarscenter. På salgs-, købs- eller servicedokumenter kan du altid angive et andet ansvarscenter end standardcenteret.

> [!NOTE]  
> Når du angiver en ansvarscenterkode i et dokument, får den indflydelse på adresse, dimensioner og priser i dokumentet.  

## <a name="to-assign-responsibility-centers-to-users"></a>Sådan knyttes ansvarscentre til brugere

Du kan opsætte brugere, så programmet i deres daglige rutine kun henter de dokumenter, der er relevante for deres specielle arbejdsområde. Brugere er normalt knyttet til et ansvarscenter og arbejder kun med dokumenter med relation til bestemte moduler i det pågældende center.  

Du kan angive dette ved at knytte ansvarscentre til brugere i tre funktionsmoduler: Køb, Salg og Service.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugeropsætning**, og vælg derefter det relaterede link.  
2. Vælg den bruger, du vil knytte et ansvarscenter til, på siden **Brugeropsætning**. Hvis brugeren ikke er i oversigten, skal du angive en bruger-id i feltet **Bruger-id**.  
3. Angiv det ansvarscenter, hvor brugeren har opgaver i relation til salg, i feltet **Filter til salgsansvarscenter**.  
4. Angiv det ansvarscenter, hvor brugeren har opgaver i relation til indkøb, i feltet **Filter til købsansvarscenter**.  
5. Angiv det ansvarscenter, hvor brugeren har opgaver i relation til servicestyring, i feltet **Filter til serviceansvarscenter**.  

> [!NOTE]  
> Brugere vil stadig være i stand til at få vist alle bogførte dokumenter og poster og altså ikke kun dem, der har relation til deres ansvarscenter.

## <a name="see-also"></a>Se også

[Opsætning af lagerbeholdning](inventory-setup-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)
[Lager](inventory-manage-inventory.md)[Logistik](warehouse-manage-warehouse.md)  
[Logistik](warehouse-manage-warehouse.md)  
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
