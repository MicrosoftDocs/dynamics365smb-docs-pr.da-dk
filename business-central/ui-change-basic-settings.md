---
title: "Vise og redigere grundlæggende indstillinger i Financials | Microsoft Docs"
description: "Lær, hvordan du kan ændre nogle af de grundlæggende indstillinger i Financials, f.eks. rollecenteret, virksomheden eller arbejdsdatoen."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 03/02/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: c7f07bd3cee8d52cccf171dfd229265d65e99cba
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="changing-basic-settings"></a>Ændring af grundlæggende indstillinger
I vinduet **Mine indstillinger** kan du se og ændre grundlæggende indstillinger for [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="role-center"></a>Rollecenter
Rollecenteret repræsenterer startsiden, der er beregnet til rollens behov. Rollecenteret giver et overblik over virksomheden, som afspejler oplysningerne, opgaverne og prioriteringen i din rolle.

Øverst i rollecenteret kan du se en navigationslinje, som giver dig nem adgang til typiske enheder for rollen, f.eks. debitorer, kreditorer, varer osv.

Hvad der vises i området med hovedindholdet afhænger af det specifikke rollecenter. I de fleste rollecentre kan du f.eks. finde aktivitetsfelter, der viser aktuelle data, og der kan klikkes på dem for at få nem adgang til det valgte dokument. Nøgletal kan konfigureres til at vise et valgt diagram for en grafisk visning af f.eks. pengestrøm eller indtægter og udgifter. Nogle rollecentre giver dig mulighed at oprette en liste over foretrukne enheder, f.eks. debitorer og kreditorer, eller få vist Rapportindbakken.

### <a name="to-change-role-center"></a>Sådan ændres et rollecenter
Standardrollecenteret er **Virksomhedsleder**, men du kan vælge et andet rollecenter, der passer bedre til dine behov.
1. I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger](media/ui-experience/settings_icon_small.png "ikonet Indstillinger for rollecenter") og derefter vælge **Indstillinger**.
2. I vinduet **Mine indstillinger** skal du i feltet **Rollecenter** vælge det rollecenter, du vil angive som standard. Vælg f.eks **Regnskabsmedarbejder**.
3. Vælg knappen **OK**.

## <a name="company"></a>Virksomhed
En virksomhed fungerer som en beholder for data i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Der kan være flere virksomheder i en database, men du kan vælge kun ét ad gangen.

Standardfirmaet kaldes CRONUS og indeholder kun demonstrationsdata.

> [!TIP]  
>   Hvis du vil vise et andet navn til din virksomhed i programmet (f.eks. i Rollecenter), skal du indstille feltet **Navn** på siden **Virksomhedsoplysninger** eller feltet **Visningsnavn** på siden **Virksomheder**.  

## <a name="work-date"></a>Arbejdsdato
Standardarbejdsdatoen er normalt dags dato. Du skal muligvis midlertidigt ændre arbejdsdatoen for at kunne udføre opgaver, f.eks. udføre transaktioner for en dato, der ikke er dags dato.

> [!TIP]  
>   Hvis du hurtigt vil indtaste arbejdsdatoen i et datofelt, skal du skrive **w**. Hvis du hurtigt vil indtaste dags dato i datofeltet, skal du skrive **t**.

> [!IMPORTANT]  
>   Arbejdsdatoen ændres kun, indtil du lukker virksomheden, eller indtil datoen skifter. Hvis du vælger et andet regnskab eller åbner det samme regnskab næste dag og stadig har brug for at angive en anden arbejdsdato, skal du angive arbejdsdatoen igen.

## <a name="region"></a>Land/område
Indstillingen **Område** bestemmer, hvordan datoer, klokkeslæt, tal og valutaer vises og formateres.   

## <a name="changing-when-i-receive-notifications"></a>Ændre, hvornår jeg modtager notifikationer
Vælg dette link for at få vist eller ændre de notifikationer, du får om bestemte hændelser eller ændringer af status, når du er ved at fakturere en kunde, der har et forfaldent beløb, eller den disponible lagerbeholdning er lavere end det antal, du er ved at sælge. Du kan finde flere oplysninger under [Smarte notifikationer](ui-smart-notifications.md).

## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md)  

