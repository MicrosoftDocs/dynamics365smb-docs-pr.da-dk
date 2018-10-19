---
title: Konfigurere brancher for kontaktvirksomheder | Microsoft Docs
description: Beskriver, hvordan du definerer en branche og knytter den til en kontaktvirksomhed, for eksempel detailbranchen eller automobilbranchen.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f1927938bc7e882902d8f609242c529e0ba29cd1
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-industry-groups-for-contact-companies"></a>Angive brancher for kontaktvirksomheder
Du bruger brancher til at angive, hvilken branchetype dine kontakter tilhører, f.eks. detailbranchen eller automobilbranchen.

Brug af brancher i kontakter er en totrinsproces. Først skal du definere branchekoden. Du behøver kun at udføre dette trin én gang for hver branche. Når du har en branchekode, kan du begynde at tildele koden til kontaktvirksomheder.

> [!NOTE]  
>   Hvis du har planer om at synkronisere kontakter med kreditorer, debitorer eller bankkonti i andre dele af programmet, kan det være en god idé at definere forretningsrelationer for dem.

## <a name="to-define-an-industry-group-code"></a>Sådan defineres en branchekode
Koden for branchen definerer type eller kategori for gruppen, f.eks REKLAME for reklame, eller PRESSE for tv og radio. Du kan have flere branchekoder. Du definerer brancherne fra vinduet **Brancher**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brancher**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

## <a name="AssignIndustryGroupContact"></a> Sådan tildeles brancher til en kontakt
Du kan ikke tildele brancher til en kontaktperson – kun til virksomheder.

1. Åbn kontakten.
2. Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Brancher**. Vinduet **Branchegrupper** åbnes.
3. I feltet **Branchekode** skal du vælge den branche, du vil tildele.

Gentag disse trin for hver branche, du vil tildele. Du kan også tildele brancher fra kontaktoversigten ved at udføre samme procedure.

Det antal brancher, du har tildelt til kontakten, vises i feltet **Antal brancher** i sektionen **Segmentering** i vinduet **Kontakt**.

Når du har tildelt brancher til kontakter, kan du bruge oplysningerne til at udvælge kontakter til målgrupper. Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Oprette kontaktvirksomheder](marketing-create-contact-companies.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

