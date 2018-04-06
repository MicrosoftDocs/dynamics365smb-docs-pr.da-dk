---
title: Bruge ADCS (Automated Data Capture System) | Microsoft Docs
description: "Du kan bruge ADCS-systemet (Automatic Data Capture System) til at registrere varebevægelser på lagerstedet og registrere bestemte kladdeaktiviteter, bl.a. regulering af vareantal på lagerkladden og lageropgørelser."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3249ed4b8bc50f7cbc577d5dc01b03029b4c06c3
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="enable-automated-data-capture-systems-adcs"></a>Aktivere ADCS (Automated Data Capture Systems)
Du kan bruge ADCS-systemet (Automatic Data Capture System) til at registrere varebevægelser på lagerstedet og registrere bestemte kladdeaktiviteter, bl.a. regulering af vareantal på lagerkladden og lageropgørelser.  

Hvis du vil bruge ADCS, skal du give hver enkelt vare, der er gemt i lageret, et vare-id. Du skal også konfigurere miniformularer, funktioner til håndholdt, dataudvekslinger og angive indstillinger for felter, der styrer ADCS. Du angiver, om du vil bruge ADCS på lokationskortet for et lagersted.

Ved opsætningen af miniformularer skal du definere, hvilke oplysninger der skal vises ud fra lagerstedets specifikke behov. Følgende er eksempler på oplysninger, som du kan få vist:  

- Data fra tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks en liste over plukdokumenter, som brugeren kan vælge.  
- Tekstoplysninger.  
- Meddelelser til at vise bekræftelser eller fejl om aktiviteter, der er udført og registreret af brugeren af den håndholdte enhed.

Du kan finde flere oplysninger i [Konfiguration af Automated Data Capture System](/dynamics-nav/Configuring-Automated-Data-Capture-System) i hjælpen til udviklere og it-eksperter.

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Sådan opsætter du et lager til brug af ADCS  
Hvis du vil bruge ADCS, skal du angive, hvilke lokationer på lagerstedet der bruger teknologien.  

> [!NOTE]  
>  Vi anbefaler, at du ikke konfigurerer et lager til at bruge ADCS, hvis lageret også har en placeringskapacitetsmetode.

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg det relaterede link.
2.  Vælg et lagersted på listen, som du vil aktivere ADCS for, og vælg derefter handlingen **Rediger**.
3. I vinduet **Lokationskort** skal du markere afkrydsningsfeltet **Brug ADCS**.  

## <a name="to-specify-an-item-to-use-adcs"></a>Angive en vare for at bruge ADCS  
Hver vare på lager, du vil bruge sammen med ADCS, skal tildeles en id-kode, som sammenkæder den med dens varenummer. Du kan for eksempel bruge varens stregkode som id-kode. En vare kan også have flere id-koder. Du kan finde dette nyttigt i tilfælde, hvor en vare findes i forskellige enhedskoder såsom stykker og paller. I dette tilfælde skal du tildele en id-kode til hver.    

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Vælg en vare på listen, som indgår i ADCS-løsningen, og vælg derefter handlingen **Rediger**.
3. I vinduet **Varekort** skal du vælge handlingen **Tegn**.
4. I vinduet **Vare-id'er** skal du vælge handlingen **Ny**.
5. Angiv identifikationsnummeret for varen i feltet **Kode**. Du kan for eksempel bruge varens stregkode som tegn.  

    Du kan også angive en **Variantkode** og en kode for **Enhed**.  

6. Hvis det er nødvendigt, skal du angive flere koder for hver vare.
7. Vælg knappen **OK**.  
8.  For at få vist oplysningerne skal du vælge feltet **Id-kode** for at åbne vinduet **Vare-id'er**.

## <a name="to-add-an-adcs-user"></a>Sådan tilføjes en ADCS-bruger  
Du kan tilføje enhver bruger som ADCS-bruger (Automated Data Capture System). Når du gør dette, skal brugeren også angive en adgangskode. Du kan eventuelt også angive en forbindelse, der identificerer ADCS-brugeren som lagermedarbejder. ADCS-brugeradgangskoden kan være forskellig fra Windows-logonadgangskoden for brugeren. Du kan finde flere oplysninger i [Administrere brugere og rettigheder](ui-how-users-permissions.md).

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **ADCS-brugere**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3.  Indtast et navn til brugeren i feltet **Navn**. Navnet må ikke indeholde mere end 20 tegn, inklusive mellemrum.  
4.  Indtast en adgangskode i feltet **Adgangskode**. Adgangskoden er skjult.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Sådan angiver du, at en lagermedarbejder er ADCS-bruger  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
2.  Hvis det er nødvendigt, kan du tilføje en ny lagermedarbejder. Du kan finde flere oplysninger i [Definere lagermedarbejdere](warehouse-how-to-set-up-warehouse-employees.md).  
3.  Vælg handlingen **Rediger liste**.  
4.  Vælg en lagermedarbejder på listen. I feltet **ADCS-bruger** skal du vælge rullepilen og derefter vælge navnet på en ADCS-bruger på listen.  

> [!NOTE]  
>  Standardlagerstedet for medarbejderen skal være ét, der anvender ADCS.

## <a name="to-create-and-customize-miniforms"></a>Sådan oprettes og tilpasses miniformularer
Du kan bruge miniformularer til at beskrive de oplysninger, som du vil vise på en håndholdt enhed. Du kan f.eks. oprette miniformularer, der understøtter lageraktiviteten at plukke varer. Når du opretter en miniformular, kan du føje funktioner til den for almindelige handlinger, en bruger udfører med håndholdte enheder, f.eks flytte en linje op eller ned.  

Hvis du vil implementere eller ændre funktionaliteten af en miniformular-funktion, skal du oprette en ny codeunit eller redigere en eksisterende, så den krævede handling eller det krævede svar udføres. Du kan lære mere om ADCS-funktionaliteten ved at undersøge codeunits såsom 7705, som er codeunit til håndtering af logonfunktionalitet. Codeunit 7705 viser, hvordan en miniformular af korttypen fungerer.  

### <a name="to-create-a-miniform-for-adcs"></a>Sådan oprettes en miniformular til ADCS  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Miniformularer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3.  Angiv en kode for miniformularen i feltet **Kode**. Angiv eventuelt værdier i alle andre felter.  

    Markér afkrydsningsfeltet **Start miniformular** for at angive, at miniformularen er den første formular, som brugeren ser ved logon.  

4.  I oversigtspanelet **Linjer** definerer du de felter, der vises i miniformularen. Den rækkefølge, du angiver linjerne i, er den rækkefølge, som linjerne vises i på den håndholdte enhed.  

Når du har oprettet en miniformular, er næste trin at oprette funktioner og knytte funktioner til forskellige tastaturinput.  

### <a name="to-add-support-for-a-function-key"></a>Sådan tilføjes understøttelse af en funktionstast  
1.  Tilføj kode i lighed med følgende eksempel til .xsl-filen for den pågældende plug-in. Dette opretter en funktion for tasten **F6**. Oplysninger om tasterækkefølgen kan fås fra producenten af enheden.  
    ```  
    <xsl:template match="Function[.='F6']">  
      <Function Key1="27" Key2="91" Key3="49" Key4="55" Key5="126" Key6="0"><xsl:value-of select="."/></Function>  
    </xsl:template>  

    ```  
2.  I udviklingsmiljøet i [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du åbne tabellen 7702 og tilføje en kode, der repræsenterer den nye tast. I dette eksempel skal du oprette en tast, der hedder **F6**.  
3.  Tilføj en C/AL-kode til den relevante funktion af den miniformular-specifikke codeunit til håndtering af funktionstasten.  

### <a name="to-customize-miniform-functions"></a>Sådan tilpasses miniformularfunktioner  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Miniformularer**, og vælg derefter det relaterede link.  
2.  Vælg en miniformular på listen, og vælg derefter handlingen **Rediger**.  
3.  Vælg handlingen **Funktioner**.  
4.  På rullelisten **Funktionskode** skal du vælge en kode til at repræsentere den funktion, du vil knytte til miniformularen. For eksempel kan du vælge ESC, som tilknytter funktionalitet, når der trykkes på ESC-tasten.  

I udviklingsmiljøet i [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du redigere koden for feltet **Håndtering af Codeunit** for at oprette eller redigere kode, som kan udføre den krævede handling eller det krævede svar.

Du kan finde flere oplysninger i [Konfiguration af Automated Data Capture System](/dynamics-nav/Configuring-Automated-Data-Capture-System) i hjælpen til udviklere og it-eksperter.

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

