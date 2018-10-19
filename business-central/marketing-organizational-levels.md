---
title: Konfigurere kompetenceniveauer for kontaktpersoner | Microsoft Docs
description: Du kan definere et kompetenceniveau og tildele det til din kontakt for at angive vedkommendes stilling i hans eller hendes virksomhed, f.eks. ledelse.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6680a5dedcbedc3ed7e430c4290871d5fbaaf9ad
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-organizational-levels-for-contact-persons"></a>Oprette kompetenceniveauer for kontaktpersoner
Du kan bruge kompetenceniveauer til kontakter, så de selv kan angive den stilling, som de har i virksomheden, f.eks. ledelse. Du kan bruge disse oplysninger, når du angiver oplysninger om dine kontakter.

Brug af kompetenceniveauer til kontakter er en totrinsproces. Først skal du definere koden for kompetenceniveauet. Du behøver kun at udføre dette trin én gang for hvert kompetenceniveau. Når du har et kompetenceniveau, kan du begynde at tildele koden til kontakter.

## <a name="to-define-an-organizational-level-code"></a>Sådan defineres en kompetenceniveaukode
Kompetenceniveaukoden definerer kompetenceniveautypen eller -kategorien, f.eks. ADMINDIR eller ØKODIR. Du kan have flere kompetenceniveaukoder. Du definerer kompetenceniveauet fra vinduet **Kompetenceniveauer**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kompetenceniveauer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

## <a name="to-assign-organizational-levels-to-a-contact-person"></a>Sådan tildeles kompetenceniveauer til en kontaktperson
Du kan kun tilknytte organisationsniveau til kontaktpersoner, ikke kontaktvirksomheder. Du kan kun tildele ét kompetenceniveau pr. kontakt.

1. Åbn kontakten.
2. I feltet **Kompetenceniveauer** skal du vælge den kode, du vil tildele.

Når du har tildelt kompetenceniveauer til dine kontakter, kan du bruge oplysningerne til at oprette målgrupper.

Når du har tildelt ansvarsområder til kontaktpersoner, kan du bruge oplysningerne til at udvælge kontakter til målgrupper. Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Oprette kontaktvirksomheder](marketing-create-contact-companies.md)  
[Oprette kontaktpersoner](marketing-create-contact-persons.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

