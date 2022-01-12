---
title: Om Finans og kontoplanen
description: Beskriver finans, kontoplanen og kontokategorier. Brug siden Opsætning af Finans til at angive, hvordan du vil behandle bestemte regnskabsopgaver i virksomheden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 12/03/2021
ms.author: edupont
ms.openlocfilehash: 2af34c84c7b359d2cae64d19a9aec151e0d9a3bb
ms.sourcegitcommit: 088bb19634f60891a12736c034ab3e86bdb91891
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2021
ms.locfileid: "7928805"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Forstå Finans og Kontoplan

Finansregnskabet gemmer de finansielle data, og kontoplanen viser de konti, som alle finansposter bogføres til. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en standardkontoplan, der er klar til at understøtte din virksomhed.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Finansopsætning og bogføringsopsætning

Opsætningen af finansmodulet er kernen i økonomiprocesser, fordi den definerer, hvordan du bogfører data.  

På siden **Opsætning af Finans** angiver du, hvordan du vil behandle bestemte regnskabsopgaver i virksomheden, f.eks.:  

* Detaljer om fakturaafrunding  
* Adresseformater  
* Økonomirapportering  

> [!TIP]
> Siden **Regnskabsopsætning** indeholder generiske felter og felter, der er specifikke for dit land eller område. Hvis du ikke er sikker på, hvad et felt betyder, anbefaler vi, at du spørger din bogholder, om det er relevant for din virksomhed.  

Desuden kan du på siden **Bogføringsopsætning** angive, hvordan du vil oprette kombinationer af virksomheds- og produktbogføringsgrupper. Bogføringsgrupper knytter enheder som debitorer, kreditorer, varer, ressourcer og salgs- og købsdokumenter til finanskonti. Udfyld en linje for hver kombination af virksomheds- og produktbogføringsgrupper. Men du kan også åbne hver linje på sit eget bogføringsopsætningskort. Du kan finde flere oplysninger i [Opsætning af bogføringsgrupper](finance-posting-groups.md).  

> [!TIP]
> Hvis du ikke kan se de ønskede felter på siden **Bogføringsopsætning**, skal du bruge det vandrette rullepanel nederst på siden til at rulle til højre.  

## <a name="the-chart-of-accounts"></a>Kontoplan

Kontoplanen viser alle finanskonti. Fra kontoplanen kan du gøre ting som at:  

* Vise rapporter med finansposter og saldi.  
* Lukke din resultatopgørelse.  
* Åbne finanskontokortet for at tilføje eller ændre indstillinger.  
* Se en oversigt over bogføringsgrupper, som bogføres til kontoen.
* Vise separate debet- og kreditsaldi for en enkelt konto  

Du kan tilføje, ændre eller slette finanskonti. Men for at forhindre afvigelser kan du ikke slette en finanskonto, hvis dens data bruges i kontoplanen.  

## <a name="account-categories"></a>Kontokategorier

Du kan tilpasse strukturen i regnskabsopgørelser ved at knytte finanskonti til kontokategorier.  

Siden **Finanskontokategorier** viser dine kategorier og underkategorier, og de finanskonti, der er knyttet til dem. Du kan oprette nye underkategorier og tildele disse kategorier til eksisterende konti.  

Du kan oprette en kategorigruppe ved at indrykke andre underkategorier under en linje på siden **Finanskontokategorier**. Dermed kan du nemt få vist en oversigt, da hver grupperingen viser den samlede saldo. Du kan f.eks. oprette underkategorier for forskellige typer anlægsaktiver og derefter oprette kategorigrupper for anlægsaktiver i forhold til omsætningsaktiver.  

Du kan angive, om kontiene i hver underkategori skal medtages i bestemte typer rapporter. Kontokategorier hjælper med at definere layoutet af regnskabet.  

### <a name="example"></a>Eksempel

F.eks. har standardsaldoopgørelsen en underkategori for *Kassebeholdning* under *Omsætningsaktiver*. Hvis du vil have, at kontantbeholdning og checks skal indgå i saldoopgørelsen, kan du gør følgende:  

1. Tilføje to nye underkategorier:

    * En til kontantbeholdning  
    * En til din checkkonto  
2. Angive den ekstra rapportdefinition **Saldo for kassekonti** for disse underkategorier.  
3. Indrykke dem under underkategorien **Kassebeholdning**.  

Næste gang du genererer kontoskemaer viser din kontoopgørelse den samlede saldo for kontant og to linjer med saldi for kontantbeholdning og checkkontoen.  

## <a name="getting-a-quick-overview"></a>Få et hurtigt overblik
Kontoplan siden viser kontiene på en hierarkisk liste, der giver hurtig adgang til nøgleoplysninger for hver konto. Listen er imidlertid statisk, og hvis du har mange konti, skal du muligvis foretage en smule rulning for at få vist oplysninger om forskellige konti. Hvis du blot vil have et hurtigt overblik over det grundlæggende, f. eks. bevægelser og saldi, er siden **Oversigt over kontoplaner** et nyttigt alternativ. Kolonnelayoutet på siden er nu det samme som på siden kontoplan (der er bare færre af dem), så du ikke behøver at vende tilbage til dig selv, og du kan udvide eller skjule de hierarkiske niveauer for at gøre visningen mere aktuel. Hvis du vil gøre det nemt at skifte mellem siderne, er siden **Oversigt over kontoplan** tilgængelig på siden kontoplan.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Adgang til at oprette og redigere konti og kontokategorier

I en mindre organisation, f. eks. CRONUS-demonstrationsregnskabet, kan de fleste brugere redigere kontoplanen, undtagen brugere med en licens til teammedlemmer. I større organisationer er adgangen til at redigere kontoplanen imidlertid begrænset af roller og tilladelser. Hvis du er administrator, eller du har rollen *forretningschef* eller *bogholder*, kan du kontrollere tilladelserne for alle brugere for at sikre, at de rette personer har adgang til de relevante tabeller. Du kan finde flere oplysninger i [Sådan får du vist en oversigt over en brugers rettigheder](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Konfigurere eller ændre kontoplanen](finance-setup-chart-accounts.md)  
[Business Intelligence](bi.md)  
[Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
