---
title: "Opsætning af forretningsrelationer for kontakter | Microsoft Docs"
description: Beskriver forretningsrelationer for kontakter i Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f6719ac45f298d6c952427c871eaf818cb7480c3
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-business-relations-on-contact-companies"></a>Opsætning af forretningsrelationer i kontaktvirksomheder
Du kan bruge forretningsrelationer til at angive det forretningsforhold, som findes mellem din virksomhed og dine kontakter, f.eks. et kundeemne, bank, konsulent, serviceleverandør osv.

Brug af forretningsrelationer i kontakter er en totrinsproces. Først skal du definere koden for forretningsrelationen. Du behøver kun at udføre dette trin én gang for hver forretningsrelation. Når du har en forretningsrelationskode, kan du begynde at tildele koden til kontaktvirksomheder.

**Bemærk**: Hvis du har planer om at synkronisere kontakter med kreditorer, debitorer eller bankkonti i andre dele af programmet, kan det være en god idé at definere forretningsrelationer for dem.

## <a name="to-define-a-business-relation-code"></a>Sådan defineres en forretningsrelationskode
Forretningsrelationskoden definerer en kategori eller type af forretningsrelation, f.eks BANK eller Law. Du kan have flere forretningsrelationskoder. Du kan definere forretningsrelationen fra vinduet **Forretningsrelationer**.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Forretningsrelationer** og derefter vælge det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

## <a name="AssignBusRelContact"></a> Sådan tildeles forretningsrelationer til en kontakt
Du kan ikke tildele forretningsrelationer til en kontaktperson – kun til virksomheder.

1. Åbn kontakten.
2. Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Forretningsrelationer**.

    Vinduet **Kontakt til forretningsrelation** åbnes.
3. I feltet **Forretningsrelationskode** skal du vælge den forretningsrelation, du vil tildele.

Gentag disse trin for hver forretningsrelation, du vil tildele. Du kan også tildele forretningsrelationer fra kontaktoversigten ved at udføre samme procedure.

Det antal relationer, du har tildelt kontakten, vises i feltet **Antal forretningsrelationer** i sektionen **Segmentering** i vinduet **Kontakt**.

Når du har tildelt forretningsrelationer til kontakter, kan du bruge oplysningerne til at udvælge kontakter til dine målgrupper. Du kan finde flere oplysninger i [Fremgangsmåde: Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Oprette kontaktvirksomheder](marketing-create-contact-companies.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

