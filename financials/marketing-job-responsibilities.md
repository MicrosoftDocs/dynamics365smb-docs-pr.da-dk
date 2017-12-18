---
title: "Opsætning af ansvarsområder for kontakter | Microsoft Docs"
description: "Du kan definere en ansvarsområdekode og knytte den til en kontakt for at angive de opgaver, som kontaktpersonen er ansvarlig for i virksomheden, f.eks. IT eller produktion."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fd949573e7bfd1b6ce1fc849625a1a3474013f96
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-job-responsibilities-for-contact-persons"></a>Fremgangsmåde: Definere dine kontaktpersoners ansvarsområder
Du kan tilføje oplysninger om ansvarsområder for kontaktpersoner for at angive, hvad kontaktpersonen er ansvarlig for i virksomheden, f.eks. IT, administration eller produktion. Du kan bruge disse oplysninger, når du angiver oplysninger om dine kontakter.

Brug af ansvarsområder for kontakter er en totrinsproces. Først skal du definere koden for ansvarsområdet. Du behøver kun at udføre dette trin én gang for hvert ansvarsområde. Når du har et ansvarsområde, kan du begynde at tildele koden til kontakter.

## <a name="to-define-a-job-responsibility-code"></a>for at definere en ansvarsområdekode
Ansvarsområdekoden definerer jobtypen eller -kategorien, f.eks. MARKETING eller INDKØB. Du kan have flere ansvarsområdekoder. Du definerer ansvarsområdet fra vinduet **Ansvarsområder**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ansvarsområder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a>for at tildele ansvarsområder til en kontaktperson
Du kan ikke tildele ansvarsområder til kontaktvirksomheder.

1. Åbn kontaktpersonen.
2. Vælg handlingen **Person**, og vælg derefter handlingen **Ansvarsområder**. Vinduet **Kontakts ansvarsområder** åbnes.
3. I feltet **Ansvarsområdekode** skal du vælge det ansvarsområde, du vil tildele.

Gentag disse trin for hver ansvarsområde, du vil tildele. Du kan også tildele ansvarsområder fra kontaktoversigten ved at udføre samme procedure.

Det antal ansvarsområder, du har tildelt til kontakten, vises i feltet **Antal ansvarsområder** i sektionen **Segmentering** i vinduet **Kontakt**.

Når du har tildelt ansvarsområder til kontaktpersoner, kan du bruge oplysningerne til at udvælge kontakter til målgrupper. Du kan finde flere oplysninger i [Fremgangsmåde: Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Oprette kontaktpersoner](marketing-create-contact-persons.md)  
[Oprette kontaktvirksomheder](marketing-create-contact-companies.md)  
[Arbejde med Financials](ui-work-product.md)

