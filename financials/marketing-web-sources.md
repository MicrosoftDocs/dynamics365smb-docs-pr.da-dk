---
title: Konfigurere webkilder for kontaktvirksomheder | Microsoft Docs
description: "Du kan definere internet- eller webkilder og tildele dem til en kontaktvirksomhed for at identificere, hvordan du vil søge efter oplysninger om dine kontakter."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6e78a86ba3d29948b07777d0a346c1ef58d088e6
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-web-sources-for-contact-companies"></a>Fremgangsmåde: Angive webkilder for kontaktvirksomheder
Du kan bruge webkilder til dine kontaktvirksomheder for at identificere f.eks. søgemaskiner og websteder på internettet, som du vil bruge til at søge efter oplysninger om kontakterne. Når du tildeler websteder skal du angive den søgemaskine og det søgeord, som skal bruges til at finde de ønskede oplysninger.

Brug af webkilder for kontakter er totrinsproces. Først skal du angive webkildekoden. Du behøver kun at udføre dette trin én gang for hver webkilde. Når du har en webkildekode, kan du begynde at tildele koden til kontakter.

## <a name="to-define-a-web-source-code"></a>for at definere en webkildekode
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Webkilder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne **Kode**, **Beskrivelse** og **URL**.

    Indtast %1 i feltet **URL** for at indsætte en pladsholder for et søgeord i URL-adressen. Når du starter webkilden fra en kontakt, erstattes %1 med det søgeord, du har indtastet i vinduet **Webkilder for kontakter**, f.eks. navnet på virksomheden.

Gentag disse trin for hver webkilde, du vil oprette.

## <a name="to-assign-web-sources-to-a-contact-company"></a>for at tildele webkilder til en kontaktvirksomhed
Når du tildeler websteder skal du angive den søgemaskine og det søgeord, som skal bruges til at finde de ønskede oplysninger.

1. Åbn kontakten.
2. Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Webkilder**. Vinduet **Webkilder for kontakt** åbnes.
3. I feltet **Webkildekode** skal du vælge den webkilde , du vil tildele.
4. Brug feltet **Søgeord** til at indtaste det søgeord, som du vil bruge til at finde oplysningerne.

Gentag disse trin for hver webkilde, du vil tildele.

Du kan også tildele webkilder fra vinduet **Kontaktoversigt** ved at udføre samme procedure.

## <a name="see-also"></a>Se også
[Oprette kontaktvirksomheder](marketing-create-contact-companies.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

