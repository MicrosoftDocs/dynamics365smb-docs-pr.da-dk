---
title: Vise og redigere grundlæggende indstillinger | Microsoft Docs
description: Lær, hvordan du kan ændre nogle af de grundlæggende indstillinger i , f.eks. rollecenteret, virksomheden eller arbejdsdatoen.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: d95d2f609129e4bdba35deda726323dbed2ba67a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250959"
---
# <a name="changing-basic-settings"></a>Ændring af grundlæggende indstillinger
På siden [**Mine indstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med dine brugerindstillinger i Business Central"), kan du få vist og ændre grundlæggende indstillinger for [!INCLUDE[d365fin](includes/d365fin_md.md)]. De ændringer, du foretager, påvirker kun dit arbejdsområde, ikke arbejdsområder for andre brugere.  

## <a name="role-center"></a> Rollecenter
Rollecenteret repræsenterer startsiden, et startskærmbillede, der er beregnet til en bestemt rolles behov i en organisation. Afhængigt af din rolle giver Rollecenter dig et overblik over arbejde, din afdeling eller personlige opgaver. Du kan også navigere til de daglige opgaver, og find arbejde, der er tildelt til dig.

-   Øverst i navigationen kan du skifte mellem debitorer, kreditorer, varer og andre vigtige lister med oplysninger. Her kan du også starte opgaver, f.eks. oprette en ny salgsfaktura direkte fra Rollecenter.

-   I centeret kan du finde **Aktiviteter**. Aktiviteter viser aktuelle data, og du kan klikke eller trykke på dem for at få vist mere detaljerede oplysninger. Nøgletal kan konfigureres til at vise et valgt diagram for en grafisk visning af f.eks. pengestrøm eller indtægter og udgifter. Du kan også oprette en række favoritdebitorer på startsiden for konti, som du handler med ofte eller skal have særlig opmærksomhed på.

### <a name="to-change-role-center"></a>Sådan ændres et rollecenter
Standardrollecenteret er **Virksomhedsleder**, men du kan vælge et andet rollecenter, der passer bedre til dine behov.
1. I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger](media/ui-experience/settings_icon_small.png "ikonet Indstillinger for rollecenter") og derefter vælge **Indstillinger**.
2. På siden **Mine indstillinger** skal du i feltet **Rollecenter** vælge det rollecenter, du vil angive som standard. Vælg f.eks **Regnskabsmedarbejder**.
3. Vælg knappen **OK**.

## <a name="company"></a>Virksomhed
En virksomhed fungerer som en beholder for data i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Der kan være flere virksomheder i en database, men du kan vælge kun ét ad gangen.

Standardfirmaet kaldes CRONUS og indeholder kun demonstrationsdata.

> [!TIP]  
>   Hvis du vil vise et andet navn til din virksomhed i programmet (f.eks. i Rollecenter), skal du indstille feltet **Navn** på siden **Virksomhedsoplysninger** eller feltet **Visningsnavn** på siden **Virksomheder**.  

## <a name="work-date"></a>Arbejdsdato
Standardarbejdsdatoen er normalt dags dato. Du skal muligvis midlertidigt ændre arbejdsdatoen for at kunne udføre opgaver, f.eks. udføre transaktioner for en dato, der ikke er dags dato.

> [!TIP]  
>   Hvis du hurtigt vil indtaste arbejdsdatoen i et datofelt, skal du skrive **a**. Hvis du hurtigt vil indtaste dags dato i datofeltet, skal du skrive **d**.

> [!IMPORTANT]  
>   Når du har ændret arbejdsdatoen, og hvis du logger af eller skifter til et andet regnskab, tilbageføres arbejdsdata til standardarbejdsdatoen. Så næste gang du logger på eller skifter tilbage til det oprindelige regnskab, kan det være nødvendigt at angive arbejdsdatoen igen. 

### <a name="work-date-indication"></a>Angivelse af arbejdsdato
<!--
Whenever the work date is not set to the current day (today), there are two indicators on pages that you open for editing:

- A reminder appears at the top of the page that tells you what the work date is set to. The reminder provides a direct link to the work date setting on the **My Settings** page so you change the date if you want. From the reminder, you can also choose to dismiss the reminder for the rest of your session. Unless you change the work date to "today", the reminder will appear the next time you sign in. 

- If you dismiss the reminder, the work date will appear in the title of the page.  
-->
Hvis arbejdsdatoen ikke er sat til den aktuelle dag (i dag), vises den aktuelle arbejdsdato i øverste venstre hjørne af siden, på alle de sider, hvor du kan redigere data.
  
## <a name="region"></a> Område

Indstillingen **Område** bestemmer, hvordan datoer, klokkeslæt, tal og valutaer vises og formateres.


## <a name="language"></a> Sprog
Ændrer det viste sprog. Dette felt vises kun, hvis der er mere end ét sprog, du kan vælge mellem. 

Det første sprog afhænger enten af administratoren eller af browserindstillingerne, når du logger på [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det sprog, du har angivet, vil blive brugt på alle enheder, som du logger på fra, f.eks. en telefon eller tablet.

## <a name="changing-when-i-receive-notifications"></a>Ændre, hvornår jeg modtager notifikationer
Vælg dette link for at få vist eller ændre de notifikationer, du får om bestemte hændelser eller ændringer af status, når du er ved at fakturere en kunde, der har et forfaldent beløb, eller den disponible lagerbeholdning er lavere end det antal, du er ved at sælge. Du kan finde flere oplysninger under [Smarte notifikationer](ui-smart-notifications.md).

## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
