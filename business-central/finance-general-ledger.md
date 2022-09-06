---
title: Om Finans og kontoplanen
description: Beskriver finans, kontoplan og kontokategorier. Brug siden Opsætning af Finans til at angive, hvordan du vil behandle bestemte regnskabsopgaver i virksomheden.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.search.form: 18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158
ms.date: 08/23/2022
ms.author: edupont
ms.openlocfilehash: 29f66fae0413bb0f8a757cfceedce8e0504e8686
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/29/2022
ms.locfileid: "9362271"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Forstå Finans og Kontoplan

Finansbogholderiet gemmer dine finansielle oplysninger. Kontoplanen viser de konti, hvor finansposter bogføres. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en standardkontoplan, der er klar til at understøtte din virksomhed.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Finansopsætning og bogføringsopsætning

Opsætningen af finansmodulet er kernen i økonomiprocesser, fordi den definerer, hvordan du bogfører data. To sider spiller en vigtig del ved at konfigurere økonomi processerne:  

* Åbn siden **Finansopsætning**

  På siden **Opsætning af Finans** angiver du, hvordan du vil behandle bestemte regnskabsopgaver i virksomheden, f.eks.:  

  * Detaljer om fakturaafrunding  
  * Adresseformater  
  * Økonomirapportering  

  > [!TIP]
  > Siden **Regnskabsopsætning** indeholder generiske felter og felter, der er specifikke for dit land eller område. Hvis du ikke er sikker på, hvad et felt betyder, anbefaler vi, at du spørger din bogholder, om det er relevant for din virksomhed. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    Åbn siden [her](https://businesscentral.dynamics.com/?page=118)
* Siden **Finansopsætning**

    Desuden kan du på siden **Bogføringsopsætning** angive, hvordan du vil oprette kombinationer af virksomheds- og produktbogføringsgrupper. Bogføringsgrupper knytter enheder som debitorer, kreditorer, varer, ressourcer og salgs- og købsdokumenter til finanskonti. Udfyld en linje for hver kombination af virksomheds- og produktbogføringsgrupper. Men du kan også åbne hver linje på sit eget bogføringsopsætningskort. Du kan finde flere oplysninger i [Opsætning af bogføringsgrupper](finance-posting-groups.md).  

    > [!TIP]
    > Hvis du ikke kan se de ønskede felter på siden **Bogføringsopsætning**, skal du bruge det vandrette rullepanel nederst på siden til at rulle til højre.  

    Åbn siden [her](https://businesscentral.dynamics.com/?page=314)

## <a name="the-chart-of-accounts"></a>Kontoplanen

Kontoplanen viser alle finanskonti. Fra kontoplanen kan du gøre ting som at:  

* Vise rapporter med finansposter og saldi.  
* Lukke din resultatopgørelse.  
* Åbne finanskontokortet for at tilføje eller ændre indstillinger.  
* Se en oversigt over bogføringsgrupper, som bogføres til kontoen.
* Vise separate debet- og kreditsaldi for en enkelt konto  

Du kan tilføje, ændre eller slette finanskonti. Men for at forhindre afvigelser kan du ikke slette en finanskonto, hvis dens data bruges i kontoplanen. Hvis du vil undgå fejltagelser i følsomme perioder, kan du også blokere for sletning af konti. Du kan finde flere oplysninger i [Slette bankkonti](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="account-categories"></a>Kontokategorier

Du kan tilpasse strukturen i regnskabsopgørelser ved at knytte finanskonti til kontokategorier.  

Siden **Finanskontokategorier** viser dine kategorier og underkategorier, og de finanskonti, der er knyttet til dem. Du kan oprette nye underkategorier og tildele disse kategorier til eksisterende konti.  

Du kan oprette en kategorigruppe ved at indrykke andre underkategorier under en linje på siden **Finanskontokategorier**. Med kategorigrupper kan du nemt få vist en oversigt, da hver grupperingen viser den samlede saldo. Du kan f.eks. oprette underkategorier for forskellige typer anlægsaktiver og derefter oprette kategorigrupper for anlægsaktiver i forhold til omsætningsaktiver.  

Du kan angive, om kontiene i hver underkategori skal medtages i bestemte typer rapporter. Kontokategorier hjælper med at definere layoutet af regnskabet.  

### <a name="example"></a>Eksempel

F.eks. har standardsaldoopgørelsen en underkategori for *Kassebeholdning* under *Omsætningsaktiver*. Hvis du vil have, at kontantbeholdning og checks skal indgå i saldoopgørelsen, kan du gør følgende:  

1. Tilføje to nye underkategorier:

    * En til kontantbeholdning  
    * En til din checkkonto  
2. Angive en anden rapportdefinition **Saldo for kassekonti** for disse underkategorier.  
3. Indrykke dem under underkategorien **Kassebeholdning**.  

Næste gang du genererer kontoskemaer, vil saldoopgørelsen vise følgende linjer:

* Total balance for kontanter.
* Linjer med saldi for kontantbeholdning og checkkontoen.  

> [!NOTE]
> Hvis du opretter en finanskonto uden at tilknytte en kontokategori, tildeles kontoarten automatisk fra finanskontoen, når du knytter kontoen til en bogføringsgruppe [!INCLUDE[prod_short](includes/prod_short.md)], lige over kontoen i din kontoplan. Hvis du vil medtage den nye konto i dine regnskabsrapporter, skal du imidlertid vælge handlingen **Generér finansielle rapporter** på siden **finanskontokategorier**. Du kan også åbne Finanskortsiden, angive kontoarten og derefter generere din finansrapport igen.

## <a name="get-a-quick-overview"></a>Få et hurtigt overblik

**Kontoplan** viser kontiene på en hierarkisk liste, der giver hurtig adgang til nøgleoplysninger for hver konto. Listen er imidlertid statisk. Hvis du har mange konti, skal du muligvis rulle for at få vist forskellige konti. Hvis du blot vil have et hurtigt overblik over det grundlæggende, f. eks. bevægelser og saldi, er siden **Oversigt over kontoplaner** et nyttigt alternativ. Kolonnelayoutet på siden er nu den samme, som du finder på siden **kontoplan** (men med færre kolonner), så du ikke behøver at vende tilbage til dig selv. Du kan udvide eller skjule de hierarkiske niveauer for at gøre visningen smallere. Hvis du vil gøre det nemt at skifte mellem siderne, er siden **Oversigt over kontoplan** tilgængelig på siden **kontoplan**.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Adgang til at oprette og redigere konti og kontokategorier

I en mindre organisation, f. eks. CRONUS-demonstrationsregnskabet, kan de fleste brugere redigere kontoplanen. Undtagen brugere med en licens til TEAM-medlemmer. I større organisationer bruges roller og tilladelser typisk til at begrænse adgang til redigering af kontoplanen. Hvis du er administrator, eller du har rollen **Forretningschef** eller **Bogholder**, kan du kontrollere tilladelserne for alle brugere for at sikre, at de rette personer har adgang til de relevante tabeller. Du kan finde flere oplysninger i [Sådan får du vist en oversigt over en brugers rettigheder](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/business-central-configure-general-ledger-setup/)

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Konfigurere eller ændre kontoplanen](finance-setup-chart-accounts.md)  
[Business Intelligence](bi.md)  
[Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
