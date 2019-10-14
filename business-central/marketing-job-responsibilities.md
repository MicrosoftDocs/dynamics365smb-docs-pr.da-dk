---
title: Opsætning af ansvarsområder for kontakter | Microsoft Docs
description: Du kan definere en ansvarsområdekode og knytte den til en kontakt for at angive de opgaver, som kontaktpersonen er ansvarlig for i virksomheden, f.eks. IT eller produktion.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 10/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 937a913a5e05670e4e4fa00138a3b8ce365ecaa7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308904"
---
# <a name="set-up-job-responsibilities-for-contact-persons"></a>Definere dine kontaktpersoners ansvarsområder
Du kan tilføje oplysninger om ansvarsområder for kontaktpersoner for at angive, hvad kontaktpersonen er ansvarlig for i virksomheden, f.eks. IT, administration eller produktion. Du kan bruge disse oplysninger, når du angiver oplysninger om dine kontakter.

Brug af ansvarsområder for kontakter er en totrinsproces. Først skal du definere koden for ansvarsområdet. Du behøver kun at udføre dette trin én gang for hvert ansvarsområde. Når du har et ansvarsområde, kan du begynde at tildele koden til kontakter.

## <a name="to-define-a-job-responsibility-code"></a>Sådan defineres en ansvarsområdekode
Ansvarsområdekoden definerer jobtypen eller -kategorien, f.eks. MARKETING eller INDKØB. Du kan have flere ansvarsområdekoder. Du definerer ansvarsområdet fra siden **Ansvarsområder**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ansvarsområder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Sådan tildeles ansvarsområder til en kontaktperson
Du kan ikke tildele ansvarsområder til kontaktvirksomheder.

1. Åbn kontaktpersonen.
2. Vælg handlingen **Person**, og vælg derefter handlingen **Ansvarsområder**. Siden **Kontakts ansvarsområder** åbnes.
3. I feltet **Ansvarsområdekode** skal du vælge det ansvarsområde, du vil tildele.

Gentag disse trin for hver ansvarsområde, du vil tildele. Du kan også tildele ansvarsområder fra kontaktoversigten ved at udføre samme procedure.

Det antal ansvarsområder, du har tildelt til kontakten, vises i feltet **Antal ansvarsområder** i sektionen **Segmentering** på siden **Kontakt**.

Når du har tildelt ansvarsområder til kontaktpersoner, kan du bruge oplysningerne til at udvælge kontakter til målgrupper. Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Oprettelse af kontakter](marketing-create-contact-companies.md)  
[Arbejde med Business Central](ui-work-product.md)
