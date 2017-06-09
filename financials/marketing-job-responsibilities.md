---
title: "Opsætning af ansvarsområder for kontakter | Microsoft Docs"
description: "Beskriver ansvarsområder for kontakter i Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 610ae314502e60b959f0e2ff705a48b936d79d68
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-job-responsibilities-for-contact-persons"></a>Definere dine kontaktpersoners ansvarsområder
Du kan tilføje oplysninger om ansvarsområder for kontaktpersoner for at angive, hvad kontaktpersonen er ansvarlig for i virksomheden, f.eks. IT, administration eller produktion. Du kan bruge disse oplysninger, når du angiver oplysninger om dine kontakter.

Brug af ansvarsområder for kontakter er en totrinsproces. Først skal du definere koden for ansvarsområdet. Du behøver kun at udføre dette trin én gang for hvert ansvarsområde. Når du har et ansvarsområde, kan du begynde at tildele koden til kontakter.

## <a name="tp-define-a-job-responsibility-code"></a>for at definere en ansvarsområdekode
Ansvarsområdekoden definerer jobtypen eller -kategorien, f.eks. MARKETING eller INDKØB. Du kan have flere ansvarsområdekoder. Du definerer ansvarsområdet fra vinduet **Ansvarsområder**.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Ansvarsområder** og derefter vælge det relaterede link.
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

