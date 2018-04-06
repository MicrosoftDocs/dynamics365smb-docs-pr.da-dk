---
title: "Opsætning af mailgrupper for kontakter | Microsoft Docs"
description: "Du kan bruge mailgrupper til at identificere grupper af kontakter, som skal modtage de samme oplysninger, f.eks. til en marketingkampagne eller et fremstød."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7402899cb7fe369503eee1b451dc652180e96264
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a>Oprette mailgrupper til kontakter
Du kan bruge mailgrupper til at angive grupper af kontakter, som skal modtage de samme oplysninger. F.eks. kan du oprette en mailgruppe til de kontakter, du vil sende en meddelelse til om at skifte kontor, og en anden gruppe om at sende gaver til andre kontakter.

Brug af mailgrupper til kontakter er en totrinsproces. Først skal du definere mailgruppekoden. Du behøver kun at udføre dette trin én gang for hver mailgruppe. Når du har en mailgruppekode, kan du begynde at tildele koden til kontaktvirksomheder.

## <a name="to-define-mailing-group-codes"></a>Sådan defineres mailgruppekoder
Feltet Mailgruppekode definerer type eller kategori af gruppen, f.eks SKIFT i forbindelse med skift af kontor eller GAVE i forbindelse med barsel. Du kan have flere branchekoder. Du definerer brancherne fra vinduet **Mailgrupper**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Mailgrupper**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

## <a name="AssignMailGroupContact"></a> Sådan tildeles mailgrupper til en kontakt
1. Åbn kontakten.
2. Vælg handlingen **Mailgrupper**. Vinduet **Mailgrupper for kontakt** åbnes.
3. I feltet **Mailgruppekode** skal du vælge den mailgruppe, du vil tildele.

Gentag disse trin for hver mailgruppe, du vil tildele. Du kan også tildele mailgrupper fra kontaktoversigten ved at udføre samme procedure.

Det antal mailgrupper, du har tildelt kontakten, vises i feltet **Antal mailgrupper** i sektionen **Segmentering** i vinduet **Kontakt**.

Når du har tildelt mailgrupper til kontakter, kan du bruge oplysningerne til at udvælge kontakter til målgrupper. Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Oprette kontaktvirksomheder](marketing-create-contact-companies.md)  
[Oprette kontaktpersoner](marketing-create-contact-persons.md)  
[Arbejde med Financials](ui-work-product.md)

