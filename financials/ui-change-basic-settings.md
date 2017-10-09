---
title: "Vise og redigere grundlæggende indstillinger i Financials | Microsoft Docs"
description: "Lær, hvordan du kan ændre nogle af de grundlæggende indstillinger i Financials, f.eks. rollecenteret, virksomheden eller arbejdsdatoen."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b486061fbb497019a56eda803df0b320565ea7bf
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="changing-basic-settings"></a>Ændring af grundlæggende indstillinger
I vinduet **Mine indstillinger** kan du se og ændre grundlæggende indstillinger for [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="role-center"></a>Rollecenter
Rollecenteret repræsenterer startsiden, der er beregnet til rollens behov. På startsiden kan du få et overblik over virksomheden. Til venstre vises en navigationslinje, som giver dig nem adgang til debitorer, kreditorer, varer osv.

Du finder ruden Aktiviteter i midten. Aktiviteter viser aktuelle data, og du kan klikke eller trykke på dem for hurtigt at få adgang til det valgte dokument. Nøgletal kan konfigureres til at vise et valgt diagram for en grafisk visning af f.eks. pengestrøm eller indtægter og udgifter.

Du kan også oprette en række Favoritdebitorer på startsiden for konti, som du handler med ofte eller skal have særlig opmærksomhed på. Brug pilene til at skjule en del af siden og få mere plads til at se specifikke oplysninger. Øverst på startsiden finder du alle de handlinger, der kan anvendes på det aktuelle indhold. Dette kan også skjules, og du behøver kun at klikke på eller trykke i det skjulte område for at få det vist igen.

Standardrollecenteret er **Virksomhedsleder**, men du kan vælge et andet rollecenter, der passer bedre til dine behov. Du kan finde flere oplysninger i [Fremgangsmåde: Ændre rollecentret](change-role.md).

## <a name="company"></a>Virksomhed
En virksomhed fungerer som en beholder for data i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Der kan være flere virksomheder i en database, men du kan vælge kun ét ad gangen.

Standardfirmaet kaldes CRONUS og indeholder kun demonstrationsdata.

> [!TIP]  
>   Hvis du vil vise et andet navn til din virksomhed i programmet (f.eks. på startsiden), skal du indstille feltet **Navn** på siden **Virksomhedsoplysninger** eller i feltet **Visningsnavn** på siden **Virksomheder**.  

## <a name="work-date"></a>Arbejdsdato
Standardarbejdsdatoen er normalt dags dato. Du skal muligvis midlertidigt ændre arbejdsdatoen for at kunne udføre opgaver, f.eks. udføre transaktioner for en dato, der ikke er dags dato.

> [!TIP]  
>   Hvis du hurtigt vil indtaste arbejdsdatoen i et datofelt, skal du skrive **w**. Hvis du hurtigt vil indtaste dags dato i datofeltet, skal du skrive **t**.

> [!IMPORTANT]  
>   Arbejdsdatoen ændres kun, indtil du lukker virksomheden, eller indtil datoen skifter. Hvis du vælger et andet regnskab eller åbner det samme regnskab næste dag og stadig har brug for at angive en anden arbejdsdato, skal du angive arbejdsdatoen igen.

## <a name="region"></a>Land/område
Indstillingen **Område** bestemmer, hvordan datoer, klokkeslæt, tal og valutaer vises og formateres.   

## <a name="change-when-i-receive-notifications"></a>Ændre, hvornår jeg modtager notifikationer
Vælg dette link for at få vist eller ændre de notifikationer, du får om bestemte hændelser eller ændringer af status, når du er ved at fakturere en kunde, der har et forfaldent beløb, eller den disponible lagerbeholdning er lavere end det antal, du er ved at sælge. Du kan finde flere oplysninger under [Smarte notifikationer](ui-smart-notifications.md).

## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Fremgangsmåde: Ændre rollecentret](change-role.md)  
[Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md)  

