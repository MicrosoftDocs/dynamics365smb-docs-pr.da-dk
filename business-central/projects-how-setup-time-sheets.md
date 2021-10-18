---
title: Konfigurere timesedler og deres godkendelse
description: Du kan konfigurere timesedler for at registrere den tid, der bruges på sager og på anvendelse af ressourcer, der hjælper dig med projektstyring, personale og kapacitet
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheet
ms.date: 10/01/2021
ms.author: edupont
ms.openlocfilehash: 72618aaeddae0a72a0c699f19a04a388ced0b9c1
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589203"
---
# <a name="set-up-time-sheets"></a>Konfigurere timesedler

Timesedler i [!INCLUDE[prod_short](includes/prod_short.md)] håndterer tidsregistrering i ugentlige intervaller på syv dage. Du kan bruge til at registrere den tid, der er brugt på sager, og du kan bruge dem til at registrere simpel ressourcetidsregistrering. Før du kan bruge timesedler, skal du angive, hvordan du vil have dem oprettet og konfigureret.

Når du har konfigureret, hvordan organisationen skal bruge timesedler, kan du angive, om og hvordan timesedler godkendes. Afhængigt af organisationens behov kan du angive:

* En eller flere brugere som timeseddeladministrator og godkendere for alle timesedler.
* En timeseddelgodkender for hver ressource.

Når du har oprettet timesedler, kan du oprette timesedler for ressourcer, tildele dem til planlægningslinjer og bogføre timeseddellinjer. Du kan finde flere oplysninger i [Bruge timesedler](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Oprette timesedler med assisterende opsætningsvejledning

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

Fra 2021 udgivelsesbølge 2 kan du bruge en assisteret installationsvejledning som hjælp til at oprette timesedler.  

> [!TIP]
> Du skal aktivere **Funktionsopdatering: ny funktion til visning af timesedler** på siden [Funktionsstyring](https://businesscentral.dynamics.com/?page=2610) for at bruge denne funktion.
>
> Den samme funktion gør det også nemmere at administrere timesedler på en mobil enhed.

Den assisterede opsætningsvejledning fører dig gennem følgende trin:

1. Konfigurer deltagerne i timeseddelprocessen
2. Angive den første dag i en arbejdsuge i denne organisation

    Den første dag i arbejdsugen vil være standard første dag for alle timesedler.
3. Angiv den person, der administrerer timesedler

    Denne person kan redigere og slette alle timesedler. Du kan også tilføje den samme rolle som andre på siden **Brugeropsætning**.
4. Oprette ressourcer, der skal bruge timesedler, og de personer, der skal godkende timesedler

    > [!NOTE]
    > I forbindelse med projekter og sager er brugerne af timesedler *ressourcer*, ikke medarbejdere. Hvis du vil kunne spore arbejdet for medarbejderne, skal du knytte ressourcer til medarbejdere i installationsvejledningen.

I slutningen af installationsvejledningen kan du vælge at lade [!INCLUDE [prod_short](includes/prod_short.md)] oprette timesedler baseret på din konfiguration. Du kan også køre installationsvejledningen igen eller fuldføre opsætningen manuelt.  

## <a name="set-up-time-sheets-manually"></a>Konfigurere timesedler manuelt

I følgende afsnit beskrives det, hvordan du konfigurerer timesedler, hvis du ikke bruger vejledningen **opsætningsvejledning til oprettelse af timesedler**.  

### <a name="to-set-up-general-information-for-time-sheets-manually"></a>Sådan angives generelle oplysninger for timesedler manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourceopsætning**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. For feltet **Timeseddel efter sagsgodkendelse** skal du vælge en af følgende indstillinger.

| Indstilling | Beskrivelse |
| --- | --- |
| **Aldrig** |Brugeren i feltet **Bruger-id for timeseddelgodkender** på ressourcekortet godkender timesedlen. |
| **Altid** |Brugeren i feltet **Ansvarlig person** på sagskortet godkender timesedlen. |
| **Kun maskine** |Hvis maskintimesedlen er knyttet til en sag, godkendes timesedlen af brugeren i feltet **Ansvarlig person** på sagskortet. Hvis maskintimesedlen er knyttet til en ressource, godkendes timesedlen af brugeren i feltet **Bruger-id for timeseddelgodkender** på ressourcekortet. |

### <a name="to-assign-a-time-sheet-administrator-manually"></a>Sådan tildeles en timeseddeladministrator manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugeropsætning**, og vælg derefter det relaterede link.  
2. Tilføj en ny bruger, hvis brugerlisten ikke omfatter den person, som du ønsker, skal være timeseddeladministrator. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).
3. Vælg en bruger, der skal være timeseddeladministrator, og marker derefter afkrydsningsfeltet **Timeseddeladm.**.  

> [!TIP]  
> Det anbefales, at du kun udpeger én bruger til timeseddeladministrator for en virksomhed. I følgende procedure opretter du en timeseddelejer og -godkender, hvor timeseddelgodkenderen tildeles for hver ressource.  

### <a name="to-assign-a-time-sheets-owner-and-approver-manually"></a>Sådan tildeles en timeseddelejer og -godkender manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourcer**, og vælg derefter det relaterede link.
2. Vælg den ressource, du vil konfigurere til at kunne bruge timesedler, og vælg derefter afkrydsningsfeltet **Brug timeseddel**.  
3. I feltet **Bruger-id for timeseddelejer** skal du angive id'et for ejeren af timesedlen. Ejeren kan angive tidsforbrug på en timeseddel og sende den til godkendelse. Når ressourcen er en person, er denne person generelt også ejeren.  
4. I feltet **Bruger-id for timeseddelgodkender** skal du angive id'et for godkenderen af timesedlen. Godkenderen kan godkende, afvise eller åbne en timeseddel igen.  

> [!NOTE]  
> Du kan ikke ændre id'et på godkenderen af timesedler, hvis der er timesedler, der endnu ikke er behandlet, og som har statussen **Sendt** eller **Åben**.

## <a name="see-also"></a>Se også

[Bruge timesedler for sager](projects-how-use-time-sheets.md)  
[Sådan opretter du timesedler](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Registrere forbrug eller forbrug til sager](projects-how-record-job-usage.md)  
[Konfigurere projektstyring](projects-setup-projects.md)  
[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]