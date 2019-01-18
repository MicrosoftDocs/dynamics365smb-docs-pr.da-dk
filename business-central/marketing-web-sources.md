---
title: Konfigurere webkilder for kontaktvirksomheder | Microsoft Docs
description: "Du kan definere internet- eller webkilder og tildele dem til en kontaktvirksomhed for at identificere, hvordan du vil søge efter oplysninger om dine kontakter."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: d7a02a85e65a663bc304becd8392e949d485f13a
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a>Angive webkilder for kontaktvirksomheder
Du kan bruge webkilder til dine kontaktvirksomheder for at identificere f.eks. søgemaskiner og websteder på internettet, som du vil bruge til at søge efter oplysninger om kontakterne. Når du tildeler websteder skal du angive den søgemaskine og det søgeord, som skal bruges til at finde de ønskede oplysninger.

Brug af webkilder for kontakter er totrinsproces. Først skal du angive webkildekoden. Du behøver kun at udføre dette trin én gang for hver webkilde. Når du har en webkildekode, kan du begynde at tildele koden til kontakter.

## <a name="to-define-a-web-source-code"></a>Sådan defineres en webkildekode
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Webkilder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne **Kode**, **Beskrivelse** og **URL**.

    Indtast %1 i feltet **URL** for at indsætte en pladsholder for et søgeord i URL-adressen. Når du starter webkilden fra en kontakt, erstattes %1 med det søgeord, du har indtastet på siden **Webkilder for kontakter**, f.eks. navnet på virksomheden.

Gentag disse trin for hver webkilde, du vil oprette.

## <a name="to-assign-web-sources-to-a-contact-company"></a>Sådan tildeles webkilder til en kontaktvirksomhed
Når du tildeler websteder skal du angive den søgemaskine og det søgeord, som skal bruges til at finde de ønskede oplysninger.

1. Åbn kontakten.
2. Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Webkilder**. Siden **Webkilder for kontakt** åbnes.
3. I feltet **Webkildekode** skal du vælge den webkilde , du vil tildele.
4. Brug feltet **Søgeord** til at indtaste det søgeord, som du vil bruge til at finde oplysningerne.

Gentag disse trin for hver webkilde, du vil tildele.

Du kan også tildele webkilder fra siden **Kontaktoversigt** ved at udføre samme procedure.

## <a name="see-also"></a>Se også
[Oprette kontaktvirksomheder](marketing-create-contact-companies.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

