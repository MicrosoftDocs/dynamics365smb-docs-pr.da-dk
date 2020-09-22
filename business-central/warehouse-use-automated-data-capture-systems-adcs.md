---
title: Bruge ADCS (Automated Data Capture System) | Microsoft Docs
description: Du kan bruge ADCS-systemet (Automatic Data Capture System) til at registrere varebevægelser på lagerstedet og registrere bestemte kladdeaktiviteter, bl.a. regulering af vareantal på lagerkladden og lageropgørelser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: barcode
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 3360dff32fab445a5dafe825a48f5745ad6479f3
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786267"
---
# <a name="use-automated-data-capture-systems-adcs"></a>Brug ADCS (Automated Data Capture Systems)

> [!NOTE]
> ADCS-løsningen (Automated Data Capture System) gør det muligt for [!INCLUDE[d365fin](includes/d365fin_md.md)] at kommunikere med håndholdte enheder via webtjenester. Du skal arbejde med en Microsoft-partner, som kan sørge for forbindelsen mellem webtjenesten og den håndholdte enhed. 

Du kan bruge ADCS-systemet (Automatic Data Capture System) til at registrere varebevægelser på lagerstedet og registrere bestemte kladdeaktiviteter, bl.a. regulering af vareantal på lagerkladden og lageropgørelser. ADCS omfatter typisk scanning af en stregkode.

Hvis du vil bruge ADCS, skal du give hver enkelt vare, der er gemt i lageret, et vare-id. Du skal også konfigurere miniformularer, funktioner til håndholdt, dataudvekslinger og angive indstillinger for felter, der styrer ADCS. Du angiver, om du vil bruge ADCS på lokationskortet for et lagersted.

Ved opsætningen af miniformularer skal du definere, hvilke oplysninger der skal vises ud fra lagerstedets specifikke behov. Følgende er eksempler på oplysninger, som du kan få vist:  

- Data fra tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks en liste over plukdokumenter, som brugeren kan vælge.  
- Tekstoplysninger.  
- Meddelelser til at vise bekræftelser eller fejl om aktiviteter, der er udført og registreret af brugeren af den håndholdte enhed.

## <a name="to-enable-web-services-for-adcs"></a>Sådan aktiveres webtjenester til ADCS
Hvis du vil bruge Automated Data Capture System, skal du aktivere ADCS-webtjenesten.  

## <a name="to-enable-and-publish-the-adcs-web-service"></a>Sådan aktiveres og publiceres ADCS-webtjenesten  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Webtjenester**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.  
3. Indtast følgende oplysninger på en ny linje på siden **Webtjenester**:  

    |Felt|Værdi|  
    |---------------------------------|-----------|  
    |**Objekttype**|Codeunit|  
    |**Objekt-id**|7714|  
    |**Tjenestenavn**|**Vigtigt** i forbindelse med ADCS: Det er nødvendigt at navngive tjenesten **ADCS**.|  

5. Marker afkrydsningsfeltet **Publiceret**.  
6. Vælg knappen **OK**.  

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Sådan opsætter du et lager til brug af ADCS  
Hvis du vil bruge ADCS, skal du angive, hvilke lokationer på lagerstedet der bruger teknologien.  

> [!NOTE]  
>  Vi anbefaler, at du ikke konfigurerer et lager til at bruge ADCS, hvis lageret også har en placeringskapacitetsmetode.

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lokationer**, og vælg derefter det relaterede link.
2.  Vælg et lagersted på listen, som du vil aktivere ADCS for, og vælg derefter handlingen **Rediger**.
3. På siden **Lokationskort** skal du markere afkrydsningsfeltet **Brug ADCS**.  

## <a name="to-specify-an-item-to-use-adcs"></a>Angive en vare for at bruge ADCS  
Hver vare på lager, du vil bruge sammen med ADCS, skal tildeles en id-kode, som sammenkæder den med dens varenummer. Du kan for eksempel bruge varens stregkode som id-kode. En vare kan også have flere id-koder. Du kan finde dette nyttigt i tilfælde, hvor en vare findes i forskellige enhedskoder såsom stykker og paller. I dette tilfælde skal du tildele en id-kode til hver.    

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Vælg en vare på listen, som indgår i ADCS-løsningen, og vælg derefter handlingen **Rediger**.
3. På siden **Varekort** skal du vælge handlingen **Tegn**.
4. På siden **Vare-id'er** skal du vælge handlingen **Ny**.
5. Angiv identifikationsnummeret for varen i feltet **Kode**. Du kan for eksempel bruge varens stregkode som tegn.  

    Du kan også angive en **Variantkode** og en kode for **Enhed**.  

6. Hvis det er nødvendigt, skal du angive flere koder for hver vare.
7. Vælg knappen **OK**.  
8.  For at få vist oplysningerne skal du vælge feltet **Id-kode** for at åbne siden **Vare-id'er**.

## <a name="to-add-an-adcs-user"></a>Sådan tilføjes en ADCS-bruger  
Du kan tilføje enhver bruger som ADCS-bruger (Automated Data Capture System). Når du gør dette, skal brugeren også angive en adgangskode. Du kan eventuelt også angive en forbindelse, der identificerer ADCS-brugeren som lagermedarbejder. ADCS-brugeradgangskoden kan være forskellig fra Windows-logonadgangskoden for brugeren. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **ADCS-brugere**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3.  Indtast et navn til brugeren i feltet **Navn**. Navnet må ikke indeholde mere end 20 tegn, inklusive mellemrum.  
4.  Indtast en adgangskode i feltet **Adgangskode**. Adgangskoden er skjult.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Sådan angiver du, at en lagermedarbejder er ADCS-bruger  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
2.  Hvis det er nødvendigt, kan du tilføje en ny lagermedarbejder. Du kan finde flere oplysninger i [Definere lagermedarbejdere](warehouse-how-to-set-up-warehouse-employees.md).  
3.  Vælg handlingen **Rediger liste**.  
4.  Vælg en lagermedarbejder på listen. I feltet **ADCS-bruger** skal du vælge rullepilen og derefter vælge navnet på en ADCS-bruger på listen.  

> [!NOTE]  
>  Standardlagerstedet for medarbejderen skal være ét, der anvender ADCS.

## <a name="to-create-and-customize-miniforms"></a>Sådan oprettes og tilpasses miniformularer
Du kan bruge miniformularer til at beskrive de oplysninger, som du vil vise på en håndholdt enhed. Du kan f.eks. oprette miniformularer, der understøtter lageraktiviteten at plukke varer. Når du opretter en miniformular, kan du føje funktioner til den for almindelige handlinger, en bruger udfører med håndholdte enheder, f.eks flytte en linje op eller ned.  

> [!NOTE] 
> Hvis du vil implementere eller ændre funktionaliteten af en miniformular-funktion, skal du oprette en ny codeunit til feltet **Håndtering af Codeunit**, så den krævede handling eller det krævede svar udføres. Du kan få mere at vide om ADCS-funktionaliteten ved at undersøge kodeenheder som 7705, 7706, 7712 og 7713.  

### <a name="to-create-a-miniform-for-adcs"></a>Sådan oprettes en miniformular til ADCS  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Miniformularer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3.  Angiv en kode for miniformularen i feltet **Kode**. Angiv eventuelt værdier i alle andre felter.  

    Markér afkrydsningsfeltet **Start miniformular** for at angive, at miniformularen er den første formular, som brugeren ser ved logon.  

4.  I oversigtspanelet **Linjer** definerer du de felter, der vises i miniformularen. Den rækkefølge, du angiver linjerne i, er den rækkefølge, som linjerne vises i på den håndholdte enhed.  

Når du har oprettet en miniformular, er næste trin at oprette funktioner og knytte funktioner til forskellige tastaturinput.  

### <a name="to-customize-miniform-functions"></a>Sådan tilpasses miniformularfunktioner  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Miniformularer**, og vælg derefter det relaterede link.  
2.  Vælg en miniformular på listen, og vælg derefter handlingen **Rediger**.  
3.  Vælg handlingen **Funktioner**.  
4.  På rullelisten **Funktionskode** skal du vælge en kode til at repræsentere den funktion, du vil knytte til miniformularen. For eksempel kan du vælge ESC, som tilknytter funktionalitet, når der trykkes på ESC-tasten.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
