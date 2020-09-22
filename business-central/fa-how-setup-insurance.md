---
title: Definere anlægsforsikring | Microsoft Docs
description: Når du vil administrere forsikringsdækning for anlægsaktiver, skal du konfigurere et forsikringskort og nogle generelle forsikringsoplysninger pr. police.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 8f0711159c2a78b81932d429b6e8ff5c915fafaa
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788592"
---
# <a name="set-up-fixed-asset-insurance"></a>Definere anlægsforsikring
Hvis du vil administrere forsikringsdækning for anlægsaktiver, skal du først angive nogle generelle forsikringsoplysninger og forsikringskort pr. police.

## <a name="to-set-up-general-insurance-information"></a>Sådan angives generelle forsikringsoplysninger
Du skal angive nogle generelle forsikringsoplysninger for at bruge forsikringsfunktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Sådan defineres forsikringstyper
Du kan gruppere forsikringspolicer i kategorier, som f.eks. forsikring mod tyveri eller brand. Forsikringstyperne bruges på forsikringskortet.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forsikringstyper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## <a name="to-set-up-insurance-cards"></a>Sådan defineres forsikringskort
Du kan samle oplysninger om hver enkelt forsikringspolice på forsikringskortet.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forsikring**, og vælg derefter det relaterede link.  
2. På siden **Forsikring** skal du vælge handlingen **Ny** for at oprette et forsikringskort.  
3. Udfyld felterne efter behov.

## <a name="to-set-up-insurance-journal-templates"></a>Sådan defineres forsikringskladdetyper
Første gang du åbner siden **Forsikringskladde** i [!INCLUDE[d365fin](includes/d365fin_md.md)], oprettes der automatisk en forsikringskladdetype, men du kan oprette flere kladdetyper. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forsikringskladdetyper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## <a name="to-set-up-insurance-journal-batches"></a>Sådan defineres forsikringskladdenavne
Du kan definere navne i en forsikringskladdetype. Værdierne i kladdenavnet bruges som standardværdier, hvis felterne ikke er udfyldt på kladdelinjerne. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forsikringskladdetyper**, og vælg derefter det relaterede link.  
2. Markér en forsikringskladdetype, og vælg derefter handlingen **Navne**.
3. På siden **Forsikringskladdenavne** skal du udfylde felterne efter behov.

> [!NOTE]  
>   Tallene har en særlig funktion i kladdenavne. Hvis et kladdetypenavn eller et kladdenavn indeholder et tal, vil tallet automatisk forøges med 1, hver gang kladden bogføres. Hvis du f.eks. angiver HH1 i feltet **Navn**, ændres kladdenavnet til HH2, når kladden HH1 er blevet bogført.

## <a name="see-also"></a>Se også
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Anlægsaktiver](fa-manage.md)  
[Finans](finance.md)  
[Introduktion](product-get-started.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
