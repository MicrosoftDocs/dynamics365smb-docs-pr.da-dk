---
title: Afhænde eller lade anlæg udgå
description: 'Når du sælger eller på anden måde afhænder et anlægsaktiv, skal salgsværdien bogføres for at beregne og registrere tab eller vinding.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.search.form: '5628, 5610, 5611, 5629, 5633'
ms.date: 06/15/2021
ms.author: bholtorf
---
# <a name="dispose-of-or-retire-fixed-assets"></a>Afhænde eller lade anlægsaktiver udgå

Når du sælger eller på anden måde afhænder et anlægsaktiv, skal salgsværdien bogføres for at beregne og registrere tab eller vinding. En salgspost skal være den sidste post, der bogføres for et anlæg. I forbindelse med delvist solgte anlægsaktiver, kan du bogføre mere end én salgspost. Det samlede antal bogførte salgsbeløb skal være et kreditbeløb.  

> [!NOTE]  
> Hvis du bruger et anlæg som delvis betaling for et andet, skal du registrere både salget af det gamle anlæg og købet (anskaffelsen) af det nye. Du kan finde flere oplysninger i [Anskaffe anlægsaktiver](fa-how-acquire.md).  

I følgende trin antages det, at du allerede har oprettet de relevante bogføringsgrupper på siden **Anlægsbogføringsgrupper**. Du kan finde flere oplysninger i [Sådan oprettes anlægsbogføringsgrupper](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Sådan bogføres et salg fra anlægskassekladden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskasseklader**, og vælg derefter det relaterede link.  
2. Opret en første kladdelinje, og udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. I feltet **Anlægsbogføringstype** skal du vælge **Salg**.  
4. Vælg handlingen **Indsæt anlægsmodkonto**. Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af salg.  

    > [!NOTE]  
    >  Trin 4 fungerer kun, hvis du har angivet følgende: På siden **Anlægsbogføringsgruppekort** for bogføringsgruppen for anlægsaktivet indeholder feltet **Salgskonto** finansdebetkontoen, og feltet **Salgsmodkonto** indeholder den finanskonto, hvor du vil bogføre modposter til opskrivning. Du kan finde flere oplysninger i [Sådan oprettes anlægsbogføringsgrupper](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Vælg handlingen **Bogfør**.  

Hvis du sælger eller afhænder en del af et anlæg, skal du opdele anlægget, inden du kan registrere salgstransaktionen. Du kan finde flere oplysninger i [Overføre, opdele eller kombinere anlægsaktiver](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Sådan får du vist salgsposter

Når du sælger eller på anden måde afhænder et anlægsaktiv, skal salgsværdien bogføres i finansregnskabet, når du kan se resultatet.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.  
2. Vælg det anlægsaktiv, du vil have vist poster for, og vælg derefter handlingen **Afskrivningsprofiler**.  
3. Vælg den afskrivningsprofil, du vil have vist poster for, og vælg derefter handlingen **Poster**.  
4. Vælg en linje med **Salg** i feltet **Anlægsbogføringskategori**, og vælg derefter handlingen **Find poster**.  
5. På siden **Find poster** skal du vælge finanspostlinjen og derefter vælge handlingen **Vis relaterede poster**.  

Siden **Finansposter** åbnes, og du kan se de poster, som bogføringen af salget har resulteret i.  

## <a name="see-also"></a>Se også

[Anlægsaktiver](fa-manage.md)  
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Sådan oprettes anlægsbogføringsgrupper](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Finans](finance.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Find poster](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
