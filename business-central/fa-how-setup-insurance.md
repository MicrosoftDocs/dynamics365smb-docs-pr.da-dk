---
title: "Definere anlægsforsikring | Microsoft Docs"
description: "Når du vil administrere forsikringsdækning for anlægsaktiver, skal du konfigurere et forsikringskort og nogle generelle forsikringsoplysninger pr. police."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 16098723fed40fbe26b9ba238e7fe5bf339003f5
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-fixed-asset-insurance"></a>Definere anlægsforsikring
Hvis du vil administrere forsikringsdækning for anlægsaktiver, skal du først angive nogle generelle forsikringsoplysninger og forsikringskort pr. police.

## <a name="to-set-up-general-insurance-information"></a>Sådan angives generelle forsikringsoplysninger
Du skal angive nogle generelle forsikringsoplysninger for at bruge forsikringsfunktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægsaktiver - Opsætning**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Sådan defineres forsikringstyper
Du kan gruppere forsikringspolicer i kategorier, som f.eks. forsikring mod tyveri eller brand. Forsikringstyperne bruges på forsikringskortet.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forsikringstyper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## <a name="to-set-up-insurance-cards"></a>Sådan defineres forsikringskort
Du kan samle oplysninger om hver enkelt forsikringspolice på forsikringskortet.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forsikring**, og vælg derefter det relaterede link.  
2. I vinduet **Forsikring** skal du vælge handlingen **Ny** for at oprette et forsikringskort.  
3. Udfyld felterne efter behov.

## <a name="to-set-up-insurance-journal-templates"></a>Sådan defineres forsikringskladdetyper
Første gang du åbner vinduet **Forsikringskladde** i [!INCLUDE[d365fin](includes/d365fin_md.md)], oprettes der automatisk en forsikringskladdetype, men du kan oprette flere kladdetyper. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forsikringskladdetyper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## <a name="to-set-up-insurance-journal-batches"></a>Sådan defineres forsikringskladdenavne
Du kan definere navne i en forsikringskladdetype. Værdierne i kladdenavnet bruges som standardværdier, hvis felterne ikke er udfyldt på kladdelinjerne. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forsikringskladdetyper**, og vælg derefter det relaterede link.  
2. Markér en forsikringskladdetype, og vælg derefter handlingen **Navne**.
3. I vinduet **Forsikringskladdenavne** skal du udfylde felterne efter behov.

> [!NOTE]  
>   Tallene har en særlig funktion i kladdenavne. Hvis et kladdetypenavn eller et kladdenavn indeholder et tal, vil tallet automatisk forøges med 1, hver gang kladden bogføres. Hvis du f.eks. angiver HH1 i feltet **Navn**, ændres kladdenavnet til HH2, når kladden HH1 er blevet bogført.

## <a name="see-also"></a>Se også
[Opsætning af anlægsaktiver](fa-setup.md)  
[Anlægsaktiver](fa-manage.md)  
[Finans](finance.md)  
[Introduktion](product-get-started.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

