---
title: Behandle salgsmuligheder i salgsprocesser | Microsoft Docs
description: "Du kan få vist, lukke eller slette leads, og du kan også oprette tilbud og salgsordrer for leads og flytte et lead gennem faserne i en salgsproces."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 78f9235e0115b75c3c479f789c76710b97a216c3
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-process-sales-opportunities"></a>Fremgangsmåde: Behandle salgsleads
Når du opretter et lead, er der flere funktioner til administration af et lead og til at flytte det til afslutning.

## <a name="to-view-opportunities"></a>Sådan vises salgsmuligheder
De eksisterende salgsleads er tilgængelige i vinduet **Leadoversigt**. Der er forskellige måder at få adgang til vinduet for at behandle salgsleads:

| For at få vist salgsleads for | Så |
| --- | --- |
| Alle sælgere og kontakter |Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Leadoversigt**, og vælg derefter det relaterede link. |
| En bestemt sælger |Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sælgere**, og vælg derefter det relaterede link. Vælg sælgeren, vælg handlingen **Leads**, og vælg derefter handlingen **Oversigt**. |
| En bestemt kontakt |Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontakter**, og vælg derefter det relaterede link. Vælg kontakten på listen, og vælg derefter handlingen **Leads**. |

Hver af disse opgaver åbnes i vinduet **Leadoversigt**.

## <a name="to-close-opportunities"></a>Sådan lukkes leads
Når forhandlingerne er afsluttet, kan du lukke leads. Når du lukker et lead, kan du samtidig angive, om det blev vundet eller tabt, og hvorfor det lukkes. For at angive en årsag, skal du have defineret lukkekoder for leads.

1. I vinduet **Leadoversigt** skal du vælge leadet og derefter vælge handlingen **Luk**. Vinduet **Luk lead** åbnes.
2. Udfyld de relevante felter, og vælg derefter knappen **OK**.

   Felterne **Leadlukkekode** og **Lukket den** er obligatoriske og skal udfyldes, før du kan vælge knappen **OK**.

   I feltet **Leadlukkekode** kan du vælge en af de eksisterende leadlukkekoder eller tilføje en ny kode. Du kan tilføje en ny kode ved at vælge **Vælg fra komplet liste** på listen og derefter vælge **ny**. På den nye tomme linje skal du udfylde felterne **Kode**, **Type** og **Beskrivelse** og derefter vælge knappen **OK**.

## <a name="to-create-quotes-for-opportunities"></a>Sådan oprettes tilbud til leads
Du kan oprette salgstilbud for kontakter, der ikke er registreret som debitorer.

1. I vinduet **Leadoversigt** skal du vælge leadet og derefter vælge handlingen **Tildel salgstilbud**. Vinduet **Salgstilbud** åbnes.
2. Udfyld de relevante felter.

## <a name="to-create-sales-orders-for-opportunities"></a>Sådan oprettes salgsordrer til leads
Du kan oprette salgsordrer ud fra de tilbud, som du har oprettet til leads. Før du kan oprette salgsordrer til dine kontaktpersoner, skal du oprette kontaktpersonen som debitor. Du kan finde flere oplysninger under [Oprette en debitor, kreditor eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

1. I vinduet **Leadoversigt** skal du finde det lead, du har oprettet et salgstilbud til.
2. Vælg handlingen **Tildel salgstilbud**. Vinduet **Salgstilbud**, der indeholder det salgstilbud, som du har knyttet til leadet, åbnes.
3. Udfyld de øvrige felter, og vælg derefter handlingen **Lav ordre**.

Når du arbejder med leads, kan det være nødvendigt at afgive tilbud til den kontakt, som leadet vedrører.

## <a name="to-delete-opportunities"></a>Sådan slettes leads
Du kan slette lead, hvis du f.eks. har afsluttet en handel. Men du kan kun slette lukkede leads. Der er to måder at slette lukkede leads. Du kan slette individuelle lukkede leads fra vinduet **Leadoversigt**, eller du kan starte kørslen **Slet lukkede leads** for at slette flere leads baseret på et angivet kriterium.

Når du vil slette lukkede leads fra vinduet **Leadoversigt**, skal du vælge leadet og derefter vælge handlingen **Slet**.

Du sletter lukkede leads med kørslen **Slet lukkede leads** ved at følge disse trin:

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Slet salgsmuligheder**, og vælg derefter det relaterede link.
2. I afsnittet **Lead** skal angive filtre, der angiver de lukkede leads, der skal slettes.
3. Vælg knappen **OK**.

Når du har slettet et lead, fjernes det automatisk fra vinduet **Leadoversigt**.

## <a name="to-move-an-opportunity-through-sales-cycle-stages"></a>Sådan flyttes et lead via salgsprocesfaser
Hvis et lead følger en salgsproces, kan du flytte det frem eller tilbage i de forskellige faser, f.eks flytte til den næste eller forrige fase og også springe en fase over.

1. Vælg handlingen **Opdater** i vinduet **Leadoversigt**. **Opdater lead** åbnes.
2. Brug feltet **Handlingstype** til at flytte leadet gennem salgsprocesfaserne:
   * **Næste** flytter et lead én fase frem.
   * **Spring over** flytter et lead en eller flere faser frem i salgsprocessen, som du angiver i feltet **Præsentation**. Du kan kun springe faser over, der er indstillet til at tillade overspringning.
   * **Forrige** flytter et lead én fase tilbage.
   * **Gå til** flytter et lead en eller flere faser tilbage i salgsprocessen, som du angiver i feltet **Præsentation**.
   * Med **Opdater** kan du ændre oplysninger (f.eks. for at ændre vurderingen af succespotentialet eller de anslåede værdier) uden at flytte til en anden fase.
3. Udfyld de øvrige felter efter behov, og vælg derefter knappen **OK**.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Oprette og administrere kontakter](marketing-contacts.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

