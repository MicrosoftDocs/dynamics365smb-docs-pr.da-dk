---
title: Konfigurere timesedler og godkendelse af dem | Microsoft Docs
description: Du kan konfigurere timesedler for at registrere den tid, der bruges på sager og på anvendelse af ressourcer, der hjælper dig med projektstyring, personale og kapacitet
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 25db2730cebefe224494561e6f5179cc3bfed56e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758663"
---
# <a name="set-up-time-sheets"></a>Konfigurere timesedler
Timesedler i [!INCLUDE[prod_short](includes/prod_short.md)] håndterer tidsregistrering i ugentlige intervaller på syv dage. Du kan bruge til at registrere den tid, der er brugt på sager, og du kan bruge dem til at registrere simpel ressourcetidsregistrering. Før du kan bruge timesedler, skal du angive, hvordan du vil have dem oprettet og konfigureret.

Når du har konfigureret, hvordan organisationen skal bruge timesedler, kan du angive, om og hvordan timesedler godkendes. Afhængigt af organisationens behov kan du angive:

* En eller flere brugere som timeseddeladministrator og godkendere for alle timesedler.
* En timeseddelgodkender for hver ressource.

Når du har oprettet timesedler, kan du oprette timesedler for ressourcer, tildele dem til planlægningslinjer og bogføre timeseddellinjer. Du kan finde flere oplysninger i [Bruge timesedler](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Sådan angives generelle oplysninger for timesedler
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ressourceopsætning**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. For feltet **Timeseddel efter sagsgodkendelse** skal du vælge en af følgende indstillinger.

| Indstilling | Beskrivelse |
| --- | --- |
| **Aldrig** |Brugeren i feltet **Bruger-id for timeseddelgodkender** på ressourcekortet godkender timesedlen. |
| **Altid** |Brugeren i feltet **Ansvarlig person** på sagskortet godkender timesedlen. |
| **Kun maskine** |Hvis maskintimesedlen er knyttet til en sag, godkendes timesedlen af brugeren i feltet **Ansvarlig person** på sagskortet. Hvis maskintimesedlen er knyttet til en ressource, godkendes timesedlen af brugeren i feltet **Bruger-id for timeseddelgodkender** på ressourcekortet. |

## <a name="to-assign-a-time-sheet-administrator"></a>Sådan tildeles en timeseddeladministrator
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugeropsætning**, og vælg derefter det relaterede link.  
2. Tilføj en ny bruger, hvis brugerlisten ikke omfatter den person, som du ønsker, skal være timeseddeladministrator. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).
3. Vælg en bruger, der skal være timeseddeladministrator, og marker derefter afkrydsningsfeltet **Timeseddeladm.**.  

> [!TIP]  
>   Det anbefales, at du kun udpeger én bruger til timeseddeladministrator for en virksomhed. I følgende procedure opretter du en timeseddelejer og -godkender, hvor timeseddelgodkenderen tildeles for hver ressource.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Sådan tildeles en timeseddelejer og -godkender
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ressourcer**, og vælg derefter det relaterede link.
2. Vælg den ressource, du vil konfigurere til at kunne bruge timesedler, og vælg derefter afkrydsningsfeltet **Brug timeseddel**.  
3. I feltet **Bruger-id for timeseddelejer** skal du angive id'et for ejeren af timesedlen. Ejeren kan angive tidsforbrug på en timeseddel og sende den til godkendelse. Når ressourcen er en person, er denne person generelt også ejeren.  
4. I feltet **Bruger-id for timeseddelgodkender** skal du angive id'et for godkenderen af timesedlen. Godkenderen kan godkende, afvise eller åbne en timeseddel igen.  

> [!NOTE]  
>   Du kan ikke ændre id'et på godkenderen af timesedler, hvis der er timesedler, der endnu ikke er behandlet, og som har statussen **Sendt** eller **Åben**.

## <a name="see-also"></a>Se også
[Konfigurere projektstyring](projects-setup-projects.md)  
[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]