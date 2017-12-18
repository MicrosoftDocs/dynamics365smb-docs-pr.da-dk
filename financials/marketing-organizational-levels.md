---
title: Konfigurere kompetenceniveauer for kontaktpersoner | Microsoft Docs
description: Du kan definere et kompetenceniveau og tildele det til din kontakt for at angive vedkommendes stilling i hans eller hendes virksomhed, f.eks. ledelse.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d101076c8a51b1c7a79606d207f79a826c89bf29
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-organizational-levels-for-contact-persons"></a>Fremgangsmåde: Oprette kompetenceniveauer for kontaktpersoner
Du kan bruge kompetenceniveauer til kontakter, så de selv kan angive den stilling, som de har i virksomheden, f.eks. ledelse. Du kan bruge disse oplysninger, når du angiver oplysninger om dine kontakter.

Brug af kompetenceniveauer til kontakter er en totrinsproces. Først skal du definere koden for kompetenceniveauet. Du behøver kun at udføre dette trin én gang for hvert kompetenceniveau. Når du har et kompetenceniveau, kan du begynde at tildele koden til kontakter.

## <a name="to-define-an-organizational-level-code"></a>Sådan defineres en kompetenceniveaukode
Kompetenceniveaukoden definerer kompetenceniveautypen eller -kategorien, f.eks. ADMINDIR eller ØKODIR. Du kan have flere kompetenceniveaukoder. Du definerer kompetenceniveauet fra vinduet **Kompetenceniveauer**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kompetenceniveauer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

## <a name="to-assign-organizational-levels-to-a-contact-person"></a>Sådan tildeles kompetenceniveauer til en kontaktperson
Du kan kun tilknytte organisationsniveau til kontaktpersoner, ikke kontaktvirksomheder. Du kan kun tildele ét kompetenceniveau pr. kontakt.

1. Åbn kontakten.
2. I feltet **Kompetenceniveauer** skal du vælge den kode, du vil tildele.

Når du har tildelt kompetenceniveauer til dine kontakter, kan du bruge oplysningerne til at oprette målgrupper.

Når du har tildelt ansvarsområder til kontaktpersoner, kan du bruge oplysningerne til at udvælge kontakter til målgrupper. Du kan finde flere oplysninger i [Fremgangsmåde: Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Oprette kontaktvirksomheder](marketing-create-contact-companies.md)  
[Oprette kontaktpersoner](marketing-create-contact-persons.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

