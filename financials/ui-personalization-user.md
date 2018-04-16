---
title: Tilpasse sider i Financials | Microsoft Docs
description: "Få at vide, hvordan du kan tilpasse brugergrænsefladen, så den passer til din måde at arbejde på."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: daf2a1349cc3e12e634324082d4e6507c5b312be
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="personalizing-your-workspace"></a>Tilpasse dit arbejdsområde
<!--NAV in the Web client-->
Du kan *tilpasse*, dit arbejdsområde, så det passer til dit arbejde og dine præferencer ved at ændre sidernes layout, så de kun viser de oplysninger, du har brug for, hvor du har brug for det. De tilpasningsændringer, du foretager, påvirker kun det, du ser, ikke hvad andre brugere ser.

Afhængigt af typen af side og dens indehold, kan du:

-   Tilføje, flytte og fjerne felter.
-   Tilføje, flytte og fjerne kolonner på en liste.
-   Ændre den fastlåste rude af kolonner på en liste. Den låste rude låser en eller flere kolonner til venstre side af en liste, så de altid er til stede, selv når du ruller vandret.
-   Flytte og fjerne køindikatorer (felter).
-   Flytte og fjerne dele. Dele er underinddelinger eller områder på en side, der indeholder elementer, f.eks. flere felter, en anden side, et diagram eller felter.  

## <a name="to-personalize-a-page"></a>Sådan tilpasses en side

1. I øverste højre hjørne skal du vælge ikonet ![Indstillinger](media/ui-experience/settings_icon_small.png "ikonet Indstillinger til rollecenter") og derefter **Tilpas**.

    Banneret **Tilpasning** vises øverst for at angive, at du kan begynde at foretage ændringer.

    ![Tilpasningstilstand](media/ui_personalize_mode_small.png "Tilpasningstilstand")

2. Gå til en side, du vil tilpasse.

   Hvis der vises et låseikon på banneret, skal du se [Derfor er siden låst](ui-personalization-locked.md) for at få yderligere oplysninger.

3. Peg på et område, som du vil tilpasse, f.eks. et felt eller kolonneoverskriften på en liste. Alt, du kan tilpasse, fremhæves straks med en pil eller ramme.
   <!--
   -  If a component can be personalized, an arrow head (![Personalization indicator arrow left](media/ui_personalize_arrow_left.png "Personalization indicator arrow left") or ![Personalization indicator arrow down](media/ui_personalize_arrow_down.png "Personalization indicator arrow down")) appears.
   -   If the component is a part, the extent of the part is indicated by a border.
   -   The freeze pane in a list is indicated by a vertical line along the entire right-side of the last column of the freeze pane.
   -->

4. Brug tabellen som en hjælp til at foretage ændringer:     <table>
       <tr><th>Hvad vil du foretage dig?</td><th>Hvordan du gør det</th></tr>
       <tr><td>Flytte noget, f.eks. et felt, en kolonne i listen, et felt eller en del</td><td> Peg et vilkårligt sted i det, du vil flytte, og træk det til den nye placering. Placeringen angives med enten en fed vandret eller lodret linje.</td></tr>
       <tr><td>Fjerne noget</td><td>Vælg pilespidsen, og vælg <b>Fjern</b>. </td></tr>
       <tr><td>Tilføje et felt eller en kolonne</td><td>I banneret <b>Tilpas</b> skal du vælge <b>Flere</b>, og derefter vælge <b>Felt</b>.<br /></br>Ruden <b>Tilføj felt til side</b> vises til højre. Den viser de felter, du kan føje til siden. Felter, der er markeret som <b>Placeret</b>, findes allerede på siden. Felter, der er markeret som <b>Klar</b>, findes i øjeblikke ikke på siden.<br /></br>Hvis du vil tilføje et felt, skal du trække det fra ruden til den ønskede placering. Placeringen angives med enten en fed vandret eller lodret linje.</td></tr>
       <tr><td>Flytte den fastlåste rude i en liste til en anden kolonne</td><td>Vælg pilespidsen for den kolonne, som du vil bruge som den sidste kolonne i den fastlåste rude, og vælg derefter <b>Angiv låst rude</b>.<br /><br/>Hvis du vil flytte den fastlåste rude tilbage til den oprindelige tiltænkte placering, skal du vælge pilespidsen for den aktuelle kolonne i den låste rude og vælge <b>Ryd låst rude</b>. Bemærk: Du kan ikke fjerne denne låste rude.</td></tr>
     </table>

   > [!IMPORTANT]  
   >   Du kan ikke ændre en liste, hvis listen vises side om side. Du skal først skifte siden til listevisningen ved at vælge ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Pil til venstre Vis som liste").

5. Du kan fortsætte med at foretage ændringer på samme side eller flytte til en anden side. Ændringerne gemmes automatisk, når du foretager dem. Når du er færdig, skal du i banneret **Tilpasning** vælge **Færdig**.

## <a name="clear-personalization-to-change-a-page-back-to-its-original-layout"></a>Ryd tilpasning for at skifte en side tilbage til det oprindelige layout
På et tidspunkt ønsker du måske at fjerne alle de tilpasningsændringer, du har foretaget på en side i tidens løb, så siden får sit oprindelige udseende. Hvis du vil gøre dette, skal du i banneret **Tilpasning** vælge **Flere**, og derefter **Fjern tilpasning**.

## <a name="personalization-in-detail"></a>Tilpasning i detaljer
Her er nogle forslag, der kan hjælpe dig med at opnå en bedre forståelse.  
-   Når du ændrer en kortside, som du åbner fra en liste, træder ændringerne træde i kraft på alle poster, der åbnes fra denne liste. Lad os antage, at du åbner en bestemt kunde fra listen Debitorer og derefter tilpasser siden ved at tilføje et felt. Når du åbner andre debitorer på listen, vises det felt, du har tilføjet, også.
-   Ændringer, du foretager, træder i kraft på alle dine rollecentre. Hvis du f.eks. foretager en ændring på listen Debitorer, når rollecenteret er angivet til virksomhedsleder, vises også ændringen i også i listen Debitorer, når rollecenter er angivet til salgsordrebehandler.
-   Ændringer af en side i en rude træder i kraft på siden, overalt hvor den vises.  
-   Du kan kun tilføje felter og kolonner fra en foruddefineret liste, der er baseret på siden. Du kan ikke oprette nye felter og kolonner.

## <a name="see-also"></a>Se også
[Administration af tilpasning](ui-personalization-manage.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
[Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md)  

