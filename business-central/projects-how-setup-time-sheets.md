---
title: Konfigurere timesedler og deres godkendelse
description: 'Få mere at vide om, hvordan du bruger timesedler til at spore tid til projekter og ressourcer.'
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
mw.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77, 462'
ms.date: 07/27/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-time-sheets"></a>Opsætte timesedler

Timesedler i [!INCLUDE[prod_short](includes/prod_short.md)] håndterer tidsregistrering i ugentlige intervaller på syv dage. Du kan bruge dem til at registrere den tid, der er brugt på projekter, og du kan bruge dem til at registrere simpel ressourcetidsregistrering. Før du bruger timesedler, skal du angive, hvilke brugere der skal sende timesedler, og hvordan du vil konfigurere timesedler.  

> [!TIP]
> De personer, der bruger timesedler lig med *ressourcer*. Det giver f.eks. mulighed for at bruge timesedler til at spore ikke medarbejderes arbejde. Hvis du vil spore arbejdet for dine medarbejdere eller bruge timesedler til at spore medarbejderfravær, skal du knytte ressourcer til medarbejdere. Der er en assisteret opsætningsvejledning, der kan hjælpe dig med at gøre det. Du kan få mere at vide om vejledningen ved at gå til [Konfigurere timesedler med den assisterede opsætningsvejledning](#set-up-time-sheets-with-the-assisted-setup-guide).  

Du kan også angive, om og hvordan timesedler skal godkendes. Afhængigt af organisationens behov kan du angive:

* En eller flere brugere som timeseddeladministrator og godkendere for alle timesedler.
* En timeseddelgodkender for hver ressource.

Når du har oprettet timesedler, kan du oprette timesedler for ressourcer, og ressourcerne kan bogføre timeseddellinjer. Du kan også knytte timesedler til projektplanlægningslinjer. Hvis du vil vide mere, skal du gå til [Bruge timesedler](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Oprette timesedler med assisterende opsætningsvejledning

Assisteret opsætningsvejledning kan hjælpe med oprette timesedler.  

> [!TIP]
> Hvis du har en versioner, der er tidligere end 2023 udgivelsesbølge 1 (v22) skal du aktivere **Funktionsopdatering: ny funktion til visning af timesedler** på siden [Funktionsstyring](https://businesscentral.dynamics.com/?page=2610) for at bruge denne funktion.
>
> Denne indstilling giver dig også mulighed for at bruge timesedler på mobilenheder.

Åbn **Konfigurere timesedler**-assisteret konfigurationsvejledning fra siden [Assisteret opsætning](https://businesscentral.dynamics.com/?page=1801).

Den assisterede opsætningsvejledning fører dig gennem følgende trin:

1. Konfigurer deltagerne i timeseddelprocessen.

    Den første side i guiden viser antallet af brugere i din [!INCLUDE [prod_short](includes/prod_short.md)]. Den indeholder også andre obligatoriske og valgfrie oplysninger.  
2. Angive den første dag i en arbejdsuge i denne organisation.

    Den første dag i arbejdsugen vil være standard første dag for alle timesedler.
3. Angiv den person, der administrerer timesedler.

    Denne person kan redigere og slette alle timesedler. Du kan også tilføje den samme rolle som andre på siden **Brugeropsætning**.
4. Oprette ressourcer, der skal bruge timesedler, og de personer, der skal godkende timesedler.

I slutningen af installationsvejledningen kan du vælge at lade [!INCLUDE [prod_short](includes/prod_short.md)] oprette timesedler baseret på din konfiguration. Se de nye timesedler på siden **Timesedler**, som du kan åbne [her](https://businesscentral.dynamics.com/?page=951). Du kan også køre installationsvejledningen igen eller fuldføre opsætningen manuelt.

> [!IMPORTANT]
> Hvis du bruger udgivelsesbølge 1 i 2023 (v22) eller senere, skal du manuelt aktivere indstillingen **Brug ny timeseddeloplevelse** til opsætningen af timesedler for at sikre, at du kan administrere timesedler på mobilenheder, som beskrevet i næste procedure.

## <a name="set-up-time-sheets-manually"></a>Konfigurere timesedler manuelt

I følgende afsnit beskrives det, hvordan du konfigurerer timesedler, hvis du ikke bruger vejledningen til assisteret opsætning **Konfigurere timesedler**.  

### <a name="set-up-general-information-for-time-sheets-manually"></a>Konfigurer generelle oplysninger for timesedler manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourceopsætning**, og vælg derefter det relaterede link.  
1. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!IMPORTANT]
   > Hvis du bruger udgivelsesbølge 1 i 2023 (v22) eller nyere, skal du aktivere indstillingen **Brug ny timeseddeloplevelse** for at sikre, at du kan administrere timesedler på mobilenheder.
1. For feltet **Timeseddel efter sagsgodkendelse** skal du vælge en af følgende indstillinger.

| Indstilling | Beskrivelse |
| --- | --- |
| **Aldrig** |Brugeren i feltet **Bruger-id for timeseddelgodkender** på ressourcekortet godkender timesedlen. |
| **Altid** |Brugeren i feltet **Ansvarlig person** på projektkortet godkender timesedlen. |
| **Kun maskine** |Hvis maskintimesedlen er knyttet til en sag, godkendes timesedlen af brugeren i feltet **Ansvarlig person** på projektkortet. Hvis maskintimesedlen er knyttet til en ressource, godkendes timesedlen af brugeren i feltet **Bruger-id for timeseddelgodkender** på ressourcekortet. |

### <a name="assign-a-time-sheet-administrator-manually"></a>Tildel en timeseddeladministrator manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugeropsætning**, og vælg derefter det relaterede link.  
2. Vælg den bruger, der skal være timeseddeladministrator, og marker derefter afkrydsningsfeltet **Timeseddeladm.**.  

> [!TIP]  
> Det anbefales, at du kun udpeger én bruger til timeseddeladministrator for en virksomhed. I følgende procedure opretter du en timeseddelejer og -godkender, hvor timeseddelgodkenderen tildeles for hver ressource.  

### <a name="assign-a-time-sheets-owner-and-approver-manually"></a>Tildel en timeseddelejer og -godkender manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourcer**, og vælg derefter det relaterede link.
2. Vælg den ressource, du vil konfigurere til at kunne bruge timesedler, og vælg derefter afkrydsningsfeltet **Brug timeseddel**.  
3. I feltet **Bruger-id for timeseddelejer** skal du angive id'et for ejeren af timesedlen. Ejeren kan angive tidsforbrug på en timeseddel og sende den til godkendelse. Når ressourcen er en person, er denne person typisk også ejeren.  
4. I feltet **Bruger-id for timeseddelgodkender** skal du angive id'et for godkenderen af timesedlen. Godkenderen kan godkende, afvise eller åbne en timeseddel igen.  

> [!NOTE]  
> Du kan ikke ændre id'et på godkenderen af timesedler, hvis der er timesedler, der endnu ikke er behandlet, og som har statussen **Sendt** eller **Åben**.

## <a name="see-also"></a>Se også

[Bruge timesedler for projekter](projects-how-use-time-sheets.md)  
[Sådan oprettes timesedler](projects-how-use-time-sheets.md#create-time-sheets)  
[Registrere forbrug eller anvendelse af projekter](projects-how-record-job-usage.md)  
[Konfigurere projektstyring](projects-setup-projects.md)  
[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
