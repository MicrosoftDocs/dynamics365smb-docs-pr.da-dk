---
title: "Opsætning af kompetenceniveauer for kontaktpersoner | Microsoft Docs"
description: Beskriver kompetenceniveauer for kontakter i Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bde26a2d5fcb7ec10dcd70fdd30c74893bcb34d5
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-organizational-levels-for-contact-persons"></a>Opsætning af kompetenceniveauer for kontaktpersoner
Du kan bruge kompetenceniveauer til kontakter, så de selv kan angive den stilling, som de har i virksomheden, f.eks. ledelse. Du kan bruge disse oplysninger, når du angiver oplysninger om dine kontakter.

Brug af kompetenceniveauer til kontakter er en totrinsproces. Først skal du definere koden for kompetenceniveauet. Du behøver kun at udføre dette trin én gang for hvert kompetenceniveau. Når du har et kompetenceniveau, kan du begynde at tildele koden til kontakter.

## <a name="to-define-an-organizational-level-code"></a>for at definere en kompetenceniveaukode
Kompetenceniveaukoden definerer kompetenceniveautypen eller -kategorien, f.eks. ADMINDIR eller ØKODIR. Du kan have flere kompetenceniveaukoder. Du definerer kompetenceniveauet fra vinduet **Kompetenceniveauer**.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Kompetenceniveauer** og derefter vælge det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

## <a name="to-assign-organizational-levels-to-a-contact-person"></a>for at tildele kompetenceniveauer til en kontaktperson
Du kan kun tilknytte organisationsniveau til kontaktpersoner, ikke kontaktvirksomheder. Du kan kun tildele ét kompetenceniveau pr. kontakt.

1. Åbn kontakten.
2. I feltet **Kompetenceniveauer** skal du vælge den kode, du vil tildele.

Når du har tildelt kompetenceniveauer til dine kontakter, kan du bruge oplysningerne til at oprette målgrupper.

Når du har tildelt ansvarsområder til kontaktpersoner, kan du bruge oplysningerne til at udvælge kontakter til målgrupper. Du kan finde flere oplysninger i [Fremgangsmåde: Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Oprette kontaktvirksomheder](marketing-create-contact-companies.md)  
[Oprette kontaktpersoner](marketing-create-contact-persons.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

