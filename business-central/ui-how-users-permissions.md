---
title: Tildele eller redigere brugertilladelser | Microsoft Docs
description: Beskriver, hvordan du kan føje Office 365-brugere til Business Central og derefter tildele tilladelser, adgangsrettigheder og sikkerhedsindstillinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: e60b7d875ebd0a598908f37a59a49953c61479f1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792902"
---
# <a name="managing-users-and-permissions"></a>Administrere brugere og deres rettigheder
Når du vil tilføje brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal din virksomheds Office 365-administrator først oprette brugerne i Office 365 Administration. Du kan finde flere oplysninger under [Føje brugere til Office 365 til virksomheder](https://aka.ms/CreateOffice365Users).

Når brugerne er oprettet i Office 365, kan de importeres til siden **Brugere** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Brugere tildeles rettighedssæt afhængigt af den plan, der er tildelt til brugeren i Office 365. Du kan finde detaljerede oplysninger om licenser i [Licensvejledning til Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

Du kan derefter fortsætte med at tildele rettighedssæt til brugerne for at definere, hvilke databaseobjekter, og dermed hvilke elementer i brugergrænsefladen, de skal have adgang til, og i hvilke virksomheder. Du kan føje brugere til brugergrupper. Det gør det nemmere at tildele de samme rettighedssæt til flere brugere.

Et rettighedssæt er en samling tilladelser til bestemte objekter i databasen. Alle brugere skal være tildelt et eller flere rettighedssæt, før de kan få adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)].

Fra siden **Brugerkort** kan du åbne siden **Gældende rettigheder** for at se, hvilke rettigheder brugeren har, og hvilke rettighedssæt de er tildelt gennem. Her kan du også ændre rettighedsdetaljer for rettighedssæt af typen **Brugerdefineret**. Du kan finde flere oplysninger i [Sådan får du vist en oversigt over en brugers rettigheder](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

Administratorer kan bruge siden **Brugeropsætning** til at definere perioder, hvor angivne brugere kan bogføre, og de kan også angive, om systemet skal registrere, hvor lang tid brugerne er logget på.

En anden metode, der definerer, hvad brugerne har adgang til, er indstillingen Oplevelse. Du kan finde flere oplysninger i [Ændre, hvilke funktioner der vises](ui-experiences.md).

## <a name="to-add-a-user-in-business-central"></a>Sådan tilføjes en bruger i Business Central
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Vælg handlingen **Hent brugere fra Office 365**.

Nye brugere, der er oprettet for dit Office 365-abonnement, tilføjes på siden **Brugere**.

## <a name="to-group-users-in-user-groups"></a>Sådan grupperes brugere i brugergrupper
Du kan oprette brugergrupper, så du bedre kan administrere rettighedssæt for grupper af brugere i virksomheden.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugergrupper**, og vælg derefter det relaterede link.
2. Du kan også vælge handlingen **Brugergrupper** på siden **Brugere**.
3. Du kan også vælge handlingen **Medlemmer af brugergruppe** på siden **Brugergruppe**.
4. Du kan også vælge handlingen **Medlemmer af brugergruppe** på siden **Tilføj brugere**.

Når du opretter brugere eller brugergrupper, skal du tildele rettighedssæt til hver af dem for at definere, hvilket objekt en bruger har adgang til. Først skal du organisere de relevante rettigheder i rettighedssæt. Du kan finde flere oplysninger i [Sådan får du vist en oversigt over en brugers rettigheder](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Sådan kopierer du en brugergruppe og alle dens rettighedssæt
Hvis du hurtigt vil definere en ny brugergruppe, kan du kopiere alle rettighedssæt fra en eksisterende brugergruppe til den nye brugergruppe.

Brugergruppemedlemmerne kopieres ikke til den nye brugergruppe. Du skal tilføje dem bagefter.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugergrupper**, og vælg derefter det relaterede link.
2. Vælg de brugergrupper, som du vil kopiere, og vælg derefter handlingen **Kopiér brugergruppe**.
3. I feltet **Ny brugergruppekode** skal du angive et navn til gruppen og derefter vælge knappen **OK**.

Den nye gruppe tilføjes på siden **Brugergrupper**. Fortsæt for at tilføje brugere. Yderligere oplysninger finder du i [Sådan grupperes brugere i brugergrupper](ui-how-users-permissions.md#to-group-users-in-a-user-group).  

## <a name="to-set-up-user-time-constraints"></a>Sådan opsættes tidsbegrænsninger for brugere
Administratorer kan definere perioder, hvor angivne brugere kan bogføre, og de kan også angive, om systemet skal registrere, hvor lang tid brugerne er logget på. Administratorer kan også knytte ansvarscentre til brugere. Du kan finde flere oplysninger i [Arbejde med ansvarscentre](inventory-responsibility-centers.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugeropsætning**, og vælg derefter det relaterede link.
2. Når siden **Brugeropsætning** åbnes, skal du vælge handlingen **Ny**.
3. I feltet **Bruger-ID** skal du angive ID'et for en bruger, eller vælge feltet for at få vist alle aktuelle Windows-brugere i systemet.
4. Udfyld felterne efter behov.

## <a name="to-create-or-modify-a-permission-set"></a>Sådan oprettes eller redigeres et rettighedssæt
Rettighedssæt fungerer som objektbeholdere for rettigheder, så du let kan håndtere flere rettigheder i én post. Når du har oprettet et rettighedssæt, skal du tilføje de faktiske rettigheder. Du kan finde flere oplysninger i [Sådan oprettes eller redigeres rettigheder](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).

> [!NOTE]  
> En [!INCLUDE[d365fin](includes/d365fin_md.md)]-løsning indeholder typisk et antal foruddefinerede rettighedssæt, der er tilføjet af Microsoft eller din softwareleverandør. Disse rettighedssæt er af typen **System** eller **Udvidelse**. Du kan ikke oprette eller redigere disse typer rettighedssæt eller rettighederne i dem. Du kan dog kopiere dem for at definere dine egne rettighedssæt og rettigheder. <br /><br />
Rettighedssæt, som brugerne opretter fra grunden eller som kopier, er af typen **Brugerdefineret** og kan redigeres.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rettighedssæt**, og vælg derefter det relaterede link.
2. For at oprette et nyt rettighedssæt skal du vælge handlingen **Ny**.
3. Udfyld felterne på den nye linje efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-copy-a-permission-set"></a>Sådan kopieres et rettighedssæt
Når du opretter nye rettighedssæt, kan du bruge en kopieringsfunktion til hurtigt at overføre alle rettigheder fra et andet rettighedssæt til et nyt rettighedssæt.

> [!NOTE]  
> Hvis et System-rettighedssættet, som du har kopieret, ændres, får du besked (afhængigt af dit valg), så du kan overveje, om ændringerne skal kopieres eller skrives til dit brugerdefinerede rettighedssæt.

1. På siden **Rettighedssæt** skal du vælge linjen for et bestemt rettighedssæt, som du vil kopiere, og vælg derefter handlingen **Kopiér rettighedssæt**.
2. På siden **Kopiér rettighedssæt** skal du angive navnet på det nye rettighedssæt og derefter vælge knappen **OK**.
3. Marker afkrydsningsfeltet **Informer i tilfælde af ændret rettighedssæt**, hvis du vil bevare en forbindelse mellem de oprindelige og de kopierede rettighedssæt. Forbindelsen bruges derefter til at give dig besked, hvis navnet eller indholdet af det oprindelige rettighedssæt ændres i en fremtidig version, som løsningen opgraderes til senere.

Det nye rettighedssæt, der indeholder alle rettigheder for det kopierede rettighedssæt, tilføjes som en ny linje på siden **Rettighedssæt**. Bemærk, at linjerne sorteres alfabetisk inden for hver type.

## <a name="to-create-or-modify-permissions-manually"></a>Sådan oprettes eller redigeres rettigheder manuelt
Denne fremgangsmåde beskriver, hvordan du kan tilføje eller redigere rettigheder manuelt. Du kan også få et rettighedssæt oprettet automatisk på grundlag af dine handlinger i brugergrænsefladen. Du kan finde flere oplysninger i [Sådan opretter eller redigerer du rettigheder ved at registrere dine handlinger](ui-how-users-permissions.md#to-create-or-modify-permission-sets-by-recording-your-actions).

1. På siden **Rettighedssæt** skal du vælge linjen for et bestemt rettighedssæt og derefter vælge handlingen **Rettigheder**.
2. På siden **Rettigheder** kan du oprette en ny linje eller redigere felterne på en eksisterende linje.

I hvert af felterne for de fem adgangstyper **Læserettighed**, **Indsætterettighed**, **Redigeringsrettighed**, **Sletterettighed** og **Udførelsesrettighed** kan du vælge en af følgende tre rettighedsindstillinger:

|Indstilling|Beskrivelse|Placeringsniveau|
|------|-----------|
|**Ja**|Brugeren kan udføre handlingen på det pågældende objekt.|Højeste|
|**Indirekte**|Brugeren kan udføre handlingen på det pågældende objekt, men kun via et relateret objekt, som brugeren har fuld adgang til.|Næsthøjeste|
|**Tomt**|Brugeren kan ikke udføre handlingen på det pågældende objekt.|Laveste|

### <a name="example---indirect-permission"></a>Eksempel - indirekte rettighed
Du kan tildele en indirekte rettighed for kun at bruge et objekt gennem et andet objekt.
En bruger kan f.eks. have tilladelse til at køre codeunit 80, salg-post Codeunit Salgs-post udfører mange opgaver, herunder ændring af tabel 37, Salgslinje. Når brugeren bogfører et salgsdokument, codeunit Salgs-post, kontrollerer [!INCLUDE[d365fin](includes/d365fin_md.md)], om brugeren har rettighed til at ændre tabellen Salgslinje. Hvis ikke, kan codeunit'en ikke udføre sine opgaver, og brugeren får en fejlmeddelelse. I så fald kører codeunit'en korrekt.

Men brugeren behøver ikke at have fuld adgang til tabellen Salgslinje for at køre codeunit'en. Hvis brugeren har indirekte rettighed til tabellen Salgslinje, kører codeunit'en Salgs-post korrekt. Når en bruger har indirekte rettighed, kan brugeren kun redigere tabellen Salgslinje ved at køre codeunit'en salgs-post eller et andet objekt, der har rettighed til at ændre tabellen Salgslinje. Brugeren kan kun redigere tabellen Salgslinje, når det sker fra understøttede funktionalitetsområder. Brugeren kan ikke køre funktionen ved et uheld eller skadeligt ved andre metoder.

### <a name="to-limit-a-users-access-to-specific-records-in-a-table"></a>Sådan begrænses en brugers adgang til bestemte poster i en tabel
Når det drejer sig om postbaseret sikkerhed i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du bruge filtrene til at begrænse en brugers adgang til data i en tabel. Du kan oprette sikkerhedsfiltre for tabeldata. Et sikkerhedsfilter beskriver et sæt af poster i en tabel, som en bruger har adgang til. For eksempel kan du angive, at en bruger kun skal kunne læse poster, der indeholder oplysninger om en bestemt kunde. Det betyder, at brugeren ikke kan få adgang til de poster, der indeholder oplysninger om andre kunder. Du kan finde flere oplysninger under [Bruge sikkerhedsfiltre](/dynamics365/business-central/dev-itpro/security/security-filters) i hjælpen til udviklere og it-eksperter.


## <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Sådan opretter eller redigerer du rettigheder ved at registrere dine handlinger
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rettighedssæt**, og vælg derefter det relaterede link.
2.  Du kan også vælge handlingen **Rettighedssæt** på siden **Brugere**.
3.  Vælg handlingen **Ny** på siden **Rettighedssæt**.
4.  Udfyld felterne på en ny linje efter behov.
5.  Vælg handlingen **Rettigheder**.
6.  På siden **Rettigheder** skal du vælge handlingen **Registrer rettigheder** og derefter vælge handlingen **Start**.

    Der startes en registreringsproces, som registrerer alle dine handlinger i brugergrænsefladen.
7.  Gå til de forskellige sider og aktiviteter i [!INCLUDE[d365fin](includes/d365fin_md.md)], som du vil give brugerne med dette rettighedssæt adgang til. Du skal udføre de opgaver, som du vil registrere rettigheder for.
8.  Når du vil afslutte registreringen, skal du vende tilbage til siden **Rettigheder** og derefter vælge handlingen **Stop**.
9.  Vælg knappen **Ja** for at føje de registrerede rettigheder til det nye rettighedssæt.
10. Angiv, om brugerne skal kunne indsætte, redigere eller slette poster i de registrerede tabeller for hvert objekt på listen over registrerede elementer.

> [!NOTE]  
> Når du redigerer en rettighed og dermed relaterede rettighedssæt, gælder ændringerne også for andre brugere, som rettighedssættet er tildelt til.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Sådan tildeles rettighedssæt til brugere eller brugergrupper
Du kan tildele rettigheder til brugere på to måder:
- Definer rettighedssæt på en brugers brugerkort.
- Marker afkrydsningsfeltet for en bruger, i en kolonne, for et relateret rettighedssæt, i en række, på siden **Rettighedssæt efter bruger**.
    Du kan også tildele rettighedssæt til brugergrupper med denne metode.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Sådan tildeles et rettighedssæt på et brugerkort
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Vælg den bruger, du vil tildele rettigheden til.
Ethvert rettighedssæt, der allerede er tildelt brugeren, vises i faktaboksen **Rettighedssæt**.
3. Vælg handlingen **Rediger** for at åbne siden **Brugerkort**.
4. I oversigtspanelet **Brugerrettighedssæt** skal du udfylde felterne efter behov på en ny linje. Du kan finde flere oplysninger i [Sådan oprettes eller redigeres et rettighedssæt](ui-how-users-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Sådan tildeles et rettighedssæt på siden **Rettighedssæt efter bruger**  
Følgende procedure beskriver, hvordan du tildeler rettighedssæt til en bruger på siden **Rettighedssæt efter bruger**. Trinene er de samme på siden **Rettighedssæt efter brugergruppe**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
2. På siden **Brugere** skal du vælge den relevante bruger og derefter vælge handlingen **Rettighedssæt efter bruger**.
3. På siden **Rettighedssæt efter bruger** skal du markere afkrydsningsfeltet **[brugernavn]** på en linje for det relevante rettighedssæt for at tildele sættet til brugeren.
4. Marker afkrydsningsfeltet **Alle brugere** for at tildele rettighedssættet til alle brugere.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Sådan får du vist en oversigt over en brugers rettigheder
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
2. Åbn den relevante brugers kort.
3. Vælg handlingen **Gældende rettigheder**.

    Delen **Rettigheder** viser alle elementer i databasen, som brugeren har adgang til. Du kan ikke redigere denne sektion.

    Delen **Efter rettighedssæt** viser de tildelte rettighedssæt, som rettighederne tildeles via til brugeren, kilden og type af rettighedssæt, og i hvilket omfang de forskellige adgangstyper har rettigheder.

    For hver række, du vælger i sektionen **Rettigheder**, viser sektionen **Efter rettighedssæt**, hvilket rettighedssæt eller sæt rettigheden tildeles gennem. I denne sektion kan du redigere værdien i hvert af felterne for de fem adgangstyper **Læserettighed**, **Indsætterettighed**, **Redigeringsrettighed**, **Sletterettighed** og **Udførelsesrettighed**.   

    > [!NOTE]  
    > Kun rettighedssæt af typen **Brugerdefineret** kan redigeres.<br /><br />
    > Rækker med kilden Rettighed stammer fra abonnementsplanen. Rettighedsværdierne for rettigheden tilsidesætter værdier i andre rettighedssæt, hvis de ligger på et højere placeringsniveau. En værdi i et ikke-rettighedssæt, der har et højere placeringsniveau end den relaterede værdi i rettighedsfeltet, sættes i parentes for at angive, at det ikke er gældende, fordi det er tilsidesat af rettigheden. Du kan finde en forklaring på placeringsniveauer i [Sådan oprettes eller redigeres rettigheder manuelt](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

4. For at redigere et rettighedssæt skal du i delen **Efter rettighedssæt** på linjen for en relevant rettighed angive typen **Brugerdefineret**, vælge et af de fem adgangstypefelter og vælge en anden værdi.

5. For at redigere individuelle rettigheder i rettighedssættet skal du vælge værdien i feltet **Rettighedssæt** for at åbne siden **Rettigheder**. Følg de trin, der er beskrevet i [Sådan oprettes eller redigeres rettighedssæt](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Når du redigerer et rettighedssæt, gælder ændringerne også for andre brugere, som rettighedssættet er tildelt til.

## <a name="see-also"></a>Se også
[Sikkerhed og beskyttelse i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Forstå brugere, profiler og rollecentre](admin-users-profiles-roles.md)  
[Blive klar til at handle](ui-get-ready-business.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Opsætning](admin-setup-and-administration.md)  
[Føje brugere til Office 365 til virksomheder](https://aka.ms/CreateOffice365Users)  
[Licensvejledning til Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing)
