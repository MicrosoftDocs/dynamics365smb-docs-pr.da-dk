---
title: Forberede overførsel af debitordata | Microsoft Docs
description: Når du har indløst og anvendt opsætningsdataene i den nye database, kan du starte overflytningen af debitorens eksisterende masterdata, som varer og debitornumre og -navne. Hvis du vil sikre, at disse data oprettes hurtigt og præcist i det nye virksomhed, skal du bruge skabeloner til at strukturere dataene.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 165eddfa28f2a48597d64c4480288e9280124fe7
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "912433"
---
# <a name="prepare-to-migrate-customer-data"></a>Forberede overflytning af debitordata
Når du har indløst og anvendt opsætningsdataene i den nye database, kan du starte overflytningen af debitorens eksisterende masterdata, som varer og debitornumre og -navne. Hvis du vil sikre, at disse data oprettes hurtigt og præcist i det nye virksomhed, skal du bruge skabeloner til at strukturere dataene.  

Du opretter typisk dataskabeloner til følgende masterdatatabeller:  

-   **Kontakt**  
-   **Debitor**  
-   **Vare**  
-   **Kreditor**  

Men du kan oprette en skabelonstruktur til og anvende den på alle tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>  Du kan også bruge dataskabeloner til daglige operationer til at oprette nye poster, der er baseret på skabeloner. Disse dataskabeloner fungerer kun til de understøttede masterdatatabeller. Du kan f.eks. finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).  

Når du importerer debitordata, f.eks. for varer, fra en fil, indsamles de obligatoriske feltdata, som du har angivet, fra den tilknyttede dataskabelon. Når du opretter en ny vare, kan du kun angive generelle oplysninger som varenavn, -beskrivelse og -pris, derefter skal du indsamle resten af de obligatoriske feltdata fra en valgt dataskabelon.  

Når du opretter en ny masterdatapost, f.eks. et debitorkort, er nogle felter obligatoriske og skal udfyldes. Du kan gruppere de fleste obligatoriske felter, f.eks. bogføringsgrupper og betalingsbetingelser, for at sikre, at oprette masterdata registreres lettere og mere stabilt. Du kan f.eks. gruppere obligatoriske felter til tabel 18, **Kunde**, som typerne **indenlandsk**, **udenlandsk** eller **eksport**.

## <a name="to-select-a-data-template"></a>Sådan vælges en dataskabelon
Når du vælger en eksisterende dataskabelon, skal du vurdere, om skabelonerne, der blev oprettet til den nye virksomhed, er tilstrækkelige til kunden. Gennemgå de angivne felter og værdier for at bestemme, hvilke skabeloner, der passer til en ny virksomhed.  

> [!TIP]  
>  Du kan også bruge dataskabeloner til hurtigt at oprette nye poster. Brug dem til hurtigere og mere nøjagtig dataoprettelse. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationsskabeloner**, og vælg derefter det relaterede link.  
2. På siden **Konfigurationsskabeloner** skal du vælge en dataskabelon på listen og derefter vælge handlingen **Rediger**.  

Hvis standardskabelonerne ikke opfylder dine behov, kan du oprette nye skabeloner, eller du kan føje felter til en eksisterende skabelon. Hvis standardskabelonerne er tilstrækkelige, kan du bruge dem til at oprette poster, der er baseret på masterdataskabeloner.

## <a name="to-create-a-new-data-template"></a>Sådan opretter du en ny dataskabelon
Du kan oprette en ny dataskabelon, hvis standardskabelonerne ikke opfylder din nye virksomheds behov. Hvis du vil oprette mere end én, kan du med fordel vedtage en navngivningskonvention for feltet **Kode**.

Hver skabelon består af et hoved og linjer. Når du opretter en skabelon, kan du angive, hvilke felter der altid skal anvendes til data af en bestemt type. Opret f.eks. forskellige debitorskabeloner for at anvende forskellige debitortyper. Når du opretter debitoren ved hjælp af en skabelon, kan du bruge skabelondata til på forhånd at udfylde visse felter.

### <a name="to-copy-an-existing-data-template"></a>Sådan kopierer du en eksisterende dataskabelon
Du kan hurtigt oprette en ny dataskabelon ved at kopiere oplysninger fra en eksisterende dataskabelon, som du derefter redigerer.

1. Åbn siden **Konfigurationsskabeloner**.
2. Vælg handlingen **Ny**.
3. Udfyld feltet **Kode**.
4. Vælg handlingen **Kopiér konfigurationsskabelon**.
5. På siden **Konfigurationsskabelon** skal du vælge en eksisterende skabelon, du vil kopiere, og derefter vælge knappen **OK**.

Tabel-ID, tabelnavn og linjerne i den eksisterende dataskabelon indsættes i den nye skabelon.

### <a name="to-create-a-data-template-header-manually"></a>Sådan oprettes et dataskabelonhoved manuelt
1. Åbn siden **Konfigurationsskabeloner**.
2. Vælg handlingen **Ny**.
3. Udfyld feltet **Kode**.
3. Angiv den tabel, skabelonen gælder for, i feltet **Tabel-id**. Feltet **Tabelnavn** udfyldes automatisk, når feltet **Tabel-id** angives.

### <a name="to-create-a-data-template-line-manually"></a>Sådan oprettes en dataskabelonlinje manuelt
1. Vælg på den første linje feltet **Feltnavn**. Siden **Feltoversigt** viser listen over felter i tabellen.
2. Vælg et felt, og vælg derefter knappen **OK**. Feltet **Felttitel** udfyldes med feltnavnet.
3. Angiv en passende værdi i feltet **Standardværdi**. I nogle tilfælde vil du måske bruge en værdi, der ikke er en værdi, der er tilgængelig i databasen. Hvis det er tilfældet, kan du markere afkrydsningsfeltet **Spring relationskontrol over** for at gøre det muligt at anvende data uden fejl.

    > [!TIP]  
    > Da feltet **Standardværdi** ikke har opslag til de tilsvarende [!INCLUDE[d365fin](includes/d365fin_md.md)]-feltindstillinger, skal du kopiere den ønskede værdi fra den relaterede side og indsætte den i skabelonen.

4. Marker afkrydsningsfeltet **Obligatorisk**, hvis brugerne skal udfylde det pågældende felt.

    > [!NOTE]
    > Afkrydsningsfeltet er kun til orientering. Ingen forretningslogik træder i kraft. Brugerne kan f.eks. ikke bogføre en faktura, hvis du ikke har konfigureret bogføringsgrupper. Du kan markere afkrydsningsfeltet **Obligatorisk** ud for felterne, så brugeren skal udfylde dem og dermed undgå en bogføringsfejl senere.
5. Angiv nødvendige oplysninger om feltet i feltet **Reference**.
6. Vælg knappen **OK**.

## <a name="to-export-to-a-template-in-excel"></a>Sådan udlæses til en skabelon i Excel
Du kan hurtigt oprette en Excel-projektmappe, der skal fungere som en skabelon, der er baseret på strukturen i en eksisterende databasetabel. Derefter kan du bruge skabelonen til at indsamle debitordata i et ensartet format til senere import i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationskladde**, og vælg derefter det relaterede link.
2. Tilføj en tabel på listen, eller vælg en eksisterende tabel. Du kan finde flere oplysninger i [Administrere virksomhedskonfigurationen i et regneark](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Definer felterne fra den tabel, du vil medtage i skabelonen.
4. Vælg handlingen **Udlæs til skabelon**.
5. Navngiv og gem Excel-filen. Excel-projektmappen åbnes automatisk.

Du kan nu angive debitordata i Excel-regnearket. Hvis du har eksporteret flere tabeller, placeres hver tabel i et separat regneark. Gem projektmappen, før du fortsætter med den næste procedure.

> [!NOTE]  
> Følgende fejl kan opstå, når du kører en engelsk version af Excel, men har internationale indstillinger konfigureret for et ikke-engelsk sprog: "Gammelt format eller ugyldig bibliotekstype". Hvis du vil afhjælpe denne fejl, skal du sikre dig, at sprogpakken for det ikke-engelske sprog er installeret.

## <a name="to-import-from-a-template-in-excel"></a>Sådan importeres fra en skabelon i Excel
1. På siden **Konfigurationskladde** skal du vælge handlingen **Indlæs fra skabelon**.
3. Gå til det skabelonregneark, du har oprettet, og vælg derefter handlingen **Åbn**.
4. Hvis du vil føje de indsamlede debitordata til databasen, skal du vælge handlingen **Anvend Data**.

Når du anvender data fra en skabelon i Excel til en tabel, der også har en konfigurationsskabelon tilknyttet i konfigurationspakken, anvendes standardfeltværdierne fra konfigurationsskabelonen også.

Enhver post, hvis data anvendes på denne måde, er fuldført, da den består af data, der er angivet af brugeren i Excel, plus de standardværdier, der er angivet af konfigurationsskabelonen.

## <a name="to-create-a-record-from-a-configuration-template"></a>Sådan opretter du en post fra en konfigurationsskabelon
Du kan bruge strukturen i de data, der er indeholdt i dataskabelonerne til at konvertere dine oplysninger til poster i databasen, én efter én. Hvis du vil gøre dette, skal du bruge funktionen **Opret forekomst**. Dette er en miniatureudgave af processen for dataoverflytning, og den kan være nyttig som prototype eller til at behandle mindre opgaver til oprettelse af data.  

Følgende trin illustrerer, hvordan du opretter et varekort fra en varedataskabelon. Du kan oprette en post fra alle dataskabeloner ved hjælp af samme fremgangsmåde.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationsskabeloner**, og vælg derefter det relaterede link.  
2. Markér skabelonen **Vare**, og vælg derefter handlingen **Rediger**. Yderligere oplysninger finder du under [Sådan oprettes en dataskabelon](admin-use-templates-to-prepare-customer-data-for-migration.md#to-create-a-new-data-template).
3. Vælg handlingen **Opret forekomst**. Der oprettes et varekort.  
4. Vælg knappen **OK**.  
5. For at få vist det nye varekort skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Varer** og derefter vælge det relaterede link.  
6. Åbn det nye varekort.  
7. Udvid de forskellige oversigtspaneler, og kontrollér, at oplysningerne er oprettet korrekt på dem.  

## <a name="to-use-a-configuration-template-on-a-record"></a>Bruge en konfigurationsskabelon på en post
Du kan anvende en dataskabelon på enhver post, der er i [!INCLUDE[d365fin](includes/d365fin_md.md)], og bruge denne teknik til at ændre eller redigere en post. Men når du gør dette, overskriver du eksisterende værdier i posten med dem fra skabelonen. Derfor skal du være omhyggelig, når du anvender en skabelon til en eksisterende poster.

> [!WARNING]  
>  Funktionen **Anvend skabelonen** overskriver eksisterende data i en post. Hvis denne funktion bruges ved overflytning af masterdata, overskrives de importerede data, når du opretter poster.

Følgende procedure er baseret på et nyt debitorkort.  

1. Oprette en debitor Du kan finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).
2. På siden **Debitorkort** skal du vælge handlingen **Anvend skabelon**.  
3. På siden **Debitorskabeloner** skal du vælge én af skabelonerne, og derefter vælge knappen **OK**.  

Standardværdierne fra den valgte debitorskabelon indsættes i debitorkortet.

## <a name="see-also"></a>Se også  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)  
[Registrere nye debitorer](sales-how-register-new-customers.md)
