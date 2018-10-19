---
title: "Afhænde eller lade anlæg udgå | Microsoft Docs"
description: "Når du kasserer, sælger eller lader et anlægsaktiv udgå, skal du bogføre en salgsværdi."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 550ae80bb03fb053547713fc71a8708fae100e5f
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="dispose-of-or-retire-fixed-assets"></a>Afhænde eller lade anlægsaktiver udgå
Når du sælger eller på anden måde afhænder et anlægsaktiv, skal salgsværdien bogføres for at beregne og registrere tab eller vinding. En salgspost skal være den sidste post, der bogføres for et anlæg. I forbindelse med delvist solgte anlægsaktiver, kan du bogføre mere end én salgspost. Det samlede antal bogførte salgsbeløb skal være et kreditbeløb.  

> [!NOTE]  
>   Hvis du bruger et anlæg som delvis betaling for et andet, skal du registrere både salget af det gamle anlæg og købet (anskaffelsen) af det nye. Du kan finde flere oplysninger i [Anskaffe anlægsaktiver](fa-how-acquire.md).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Sådan bogføres et salg fra anlægskassekladden
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægsfinanskladder**, og vælg derefter det relaterede link.  
2. Opret en første kladdelinje, og udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. I feltet **Anlægsbogføringstype** skal du vælge **Salg**.  
4. Vælg handlingen **Indsæt anlægsmodkonto**. Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af salg.  

    > [!NOTE]  
    >   Trin 4 fungerer kun, hvis du har angivet følgende: I vinduet **Anlægsbogføringsgruppekort** for bogføringsgruppen for anlægsaktivet indeholder feltet **Salgskonto** finansdebetkontoen, og feltet **Salgsmodkonto** indeholder den finanskonto, hvor du vil bogføre modposter til opskrivning. Du kan finde flere oplysninger i afsnittet "Sådan oprettes anlægsbogføringsgrupper" i [Angive generelle oplysninger om anlægsaktiver](fa-how-setup-general.md).  
5. Vælg handlingen **Bogfør**.  

Hvis du sælger eller afhænder en del af et anlæg, skal du opdele anlægget, inden du kan registrere salgstransaktionen. Du kan finde flere oplysninger i [Overføre, opdele eller kombinere anlægsaktiver](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Sådan får du vist salgsposter
Når du sælger eller på anden måde afhænder et anlægsaktiv, skal salgsværdien bogføres i finansregnskabet, når du kan se resultatet.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.  
2. Vælg det anlægsaktiv, du vil have vist poster for, og vælg derefter handlingen **Afskrivningsprofiler**.  
3. Vælg den afskrivningsprofil, du vil have vist poster for, og vælg derefter handlingen **Poster**.  
4. Vælg en linje med **Salg** i feltet **Anlægsbogføringskategori**, og vælg derefter handlingen **Naviger**.  
5. I vinduet **Naviger** skal du vælge finanspostlinjen og derefter vælge handlingen **Vis**.  

Vinduet **Finansposter** åbnes, og du kan se de poster, som bogføringen af salget har resulteret i.  

## <a name="see-also"></a>Se også
[Anlægsaktiver](fa-manage.md)  
[Opsætning af anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Introduktion](product-get-started.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

