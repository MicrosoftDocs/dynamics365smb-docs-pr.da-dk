---
title: Definere forretningsrelationskode for kontakter | Microsoft Docs
description: "Brug forretningsrelationer i Business Central til at hjælpe med marketing og til at angive det forretningsforhold, som findes mellem din virksomhed og dine kundeemner og kunder, f.eks. en bank eller serviceleverandør."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8a950b87b7e7947de1602db76805a0b1f41d8274
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a>Opsætning af forretningsrelationer i kontaktvirksomheder
Du kan bruge forretningsrelationer til at angive det forretningsforhold, som findes mellem din virksomhed og dine kontakter, f.eks. et kundeemne, bank, konsulent, serviceleverandør osv.

Brug af forretningsrelationer i kontakter er en totrinsproces. Først skal du definere koden for forretningsrelationen. Du behøver kun at udføre dette trin én gang for hver forretningsrelation. Når du har en forretningsrelationskode, kan du begynde at tildele koden til kontaktvirksomheder.

> [!NOTE]  
>   Hvis du har planer om at synkronisere kontakter med kreditorer, debitorer eller bankkonti i andre dele af programmet, kan det være en god idé at definere forretningsrelationer for dem.

## <a name="to-define-a-business-relation-code"></a>Sådan defineres en forretningsrelationskode
Forretningsrelationskoden definerer en kategori eller type af forretningsrelation, f.eks BANK eller Law. Du kan have flere forretningsrelationskoder. Du kan definere forretningsrelationen fra vinduet **Forretningsrelationer**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forretningsrelationer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

## <a name="AssignBusRelContact"></a> Sådan tildeles forretningsrelationer til en kontakt
Du kan ikke tildele forretningsrelationer til en kontaktperson – kun til virksomheder.

1. Åbn kontakten.
2. Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Forretningsrelationer**.

    Vinduet **Kontakt til forretningsrelation** åbnes.
3. I feltet **Forretningsrelationskode** skal du vælge den forretningsrelation, du vil tildele.

Gentag disse trin for hver forretningsrelation, du vil tildele. Du kan også tildele forretningsrelationer fra kontaktoversigten ved at udføre samme procedure.

Det antal relationer, du har tildelt kontakten, vises i feltet **Antal forretningsrelationer** i sektionen **Segmentering** i vinduet **Kontakt**.

Når du har tildelt forretningsrelationer til kontakter, kan du bruge oplysningerne til at udvælge kontakter til dine målgrupper. Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Oprette kontaktvirksomheder](marketing-create-contact-companies.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

