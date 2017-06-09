---
title: "Fremgangsmåde: Administrere brugere og rettigheder | Microsoft Docs"
description: "Administrer rettighedssæt for brugere, når du har oprettet brugere i Office 365."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d1a973b864a654e2047c5a89271519da04f55c08
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-users-and-permissions"></a>Fremgangsmåde: Administrere brugere og rettigheder
Når du vil tilføje brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal din virksomheds Office 365-administrator først oprette brugerne i Office 365 Administration. Du kan finde flere oplysninger under [Føje brugere til Office 365 til virksomheder](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Når brugerne er oprettet i Office 365, kan de importeres i vinduet **Brugere** ved hjælp af handlingen **Hent brugere fra Office 365**. Brugere tildeles rettighedssæt afhængigt af den plan, der er tildelt til Brugere i Office 365.

Du kan derefter fortsætte med at tildele rettighedssæt til brugerne for at definere, hvilke databaseobjekter, og dermed hvilke elementer i brugergrænsefladen, de skal have adgang til, og i hvilke virksomheder.

**Vigtigt!** Hvis databasen indeholder flere regnskaber, skal mindst én bruger være medlem af superbrugergruppen i alle regnskaber.

Et rettighedssæt er en samling tilladelser til bestemte objekter i databasen. Alle brugere skal være tildelt et eller flere rettighedssæt, før de kan få adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Der findes som standard et antal foruddefinerede rettighedssæt. Du kan bruge disse tilladelsessæt, som allerede er defineret, ændre standardtilladelsessættene eller oprette flere tilladelsessæt.

Du kan føje brugere til brugergrupper. Det gør det nemmere at tildele de samme rettighedssæt til flere brugere.

**Bemærk!** Denne funktion kræver, at oplevelsen er indstillet til Pakke. Du kan finde flere oplysninger i [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Sådan tildeles rettigheder til en bruger
1. I øverste højre hjørne skal du vælge ikonet Søg efter side eller rapport, angive **Brugere** og derefter vælge det relaterede link.
2. Vælg den bruger, du vil tildele rettigheden til.
Ethvert rettighedssæt, der allerede er tildelt brugeren, vises i faktaboksen **Rettighedssæt**.
3. Vælg handlingen **Rediger** for at åbne vinduet **Brugerkort**.
4. I oversigtspanelet **Brugerrettighedssæt** skal du udfylde felterne efter behov på en ny linje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Sådan grupperes brugere i brugergrupper
Du kan oprette brugergrupper, så du bedre kan administrere rettighedssæt for grupper af brugere i virksomheden. Du kan bruge en funktion til at kopiere alle rettighedssæt fra en eksisterende brugergruppe til den nye brugergruppe. Brugergruppemedlemmerne kopieres ikke.

1. I øverste højre hjørne skal du vælge ikonet Søg efter side eller rapport, angive **Brugergrupper** og derefter vælge det relaterede link.
2. Du kan også vælge handlingen **Brugergrupper** i vinduet **Brugere**.
3. I vinduet **Brugergrupper** skal du vælge en eksisterende gruppe, du vil kopiere, og derefter vælge handlingen **Kopiér brugergruppe**.
4. I feltet **Ny brugergruppekode** skal du angive navnet på den nye gruppe og derefter vælge knappen **OK**.

    I stedet for at kopiere kan du også vælge handlingen Ny for at oprette en ny linje til en tom brugergruppe, som du derefter udfylder manuelt.
5. Hvis du vil tilføje nye eller flere brugere, skal du vælge handlingen **Medlemmer af brugergruppe** i vinduet **Brugergruppe**.
6. I vinduet **Medlemmer af brugergruppe** skal du på en ny linje udfylde felterne efter behov ved at vælge mellem eksisterende brugere.
7. Hvis du vil tilføje nye eller flere rettighedssæt, skal du vælge handlingen **Rettighedssæt for brugergruppe** i vinduet **Brugergruppe**.
8. I vinduet **Rettighedssæt for brugergruppe** skal du på en ny linje udfylde felterne efter behov ved at vælge mellem eksisterende rettighedssæt.

## <a name="to-create-or-modify-permission-sets"></a>Sådan oprettes eller redigeres rettighedssæt
Hvis de standardrettighedssæt, der leveres sammen med [!INCLUDE[d365fin](includes/d365fin_md.md)], ikke er tilstrækkelige eller ikke passer til din organisation, kan du oprette nye rettighedssæt. Og hvis de enkelte objekttilladelser, der definerer et rettighedssæt, ikke er tilstrækkelige, kan du ændre et rettighedssæt. Du kan oprette et rettighedssæt manuelt, eller du kan bruge en registreringsfunktion, der registrerer dine handlinger, når du navigerer gennem et scenarie, og derefter opretter de nødvendige rettighedssæt.

### <a name="to-create-or-modify-permission-sets-manually"></a>Sådan oprettes eller redigeres rettighedssæt manuelt
1. I øverste højre hjørne skal du vælge ikonet Søg efter side eller rapport, angive **Brugere** og derefter vælge det relaterede link.
2. Vælg handlingen **Rettighedssæt** i vinduet **Brugere**.
3. Vælg handlingen **Ny** i vinduet **Rettighedssæt**.
4. Udfyld felterne på en ny linje efter behov.
5. Vælg handlingen **Rettigheder**.
6. I vinduet **Rettigheder** skal du udfylde felterne i hovedet efter behov.
7. Udfyld de fem felter for de forskellige rettigheder som beskrevet i følgende tabel på en ny linje.

    |Indstilling|Beskrivelse|
    |------|-----------|
    |Tom|Angiver, at rettighedstypen ikke er tildelt til objektet.|
    |**Ja**|Angiver, at rettighedstypen er tildelt med direkte adgang til objektet.|
    |**Indirekte**|Angiver, at rettighedstypen er tildelt med indirekte adgang til objektet.|

    Indirekte rettighed til en tabel betyder, at du ikke kan åbne tabellen og læse fra den, men du kan få vist dataene i tabellen ved hjælp af et andet objekt, f.eks. en side, som du har direkte adgangsrettigheder til. Du kan finde flere oplysninger i afsnittet "Eksempel - indirekte rettighed" i dette afsnit.

8. I feltet **Sikkerhedsfilter** skal du angive et filter, der skal anvendes på rettigheder, ved at markere det felt, hvor du vil begrænse brugeradgangen.

    F.eks. hvis du vil oprette et sikkerhedsfilter, så en bruger kan få vist kun salg med en specifik sælgerkode, skal du vælge feltnummeret for feltet **Sælgerkode**. I feltet **Feltfilter** skal du angive værdien af det, du vil bruge til at begrænse adgangen. Hvis du f.eks. vil begrænse en brugers adgang til kun Anne Grethe Hansens salg, skal du angive AGH.
9. Gentag trin 7 og 8 for at føje rettigheder til flere objekter til rettighedssættet.

### <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Sådan opretter eller redigerer du rettigheder ved at registrere dine handlinger
1. I øverste højre hjørne skal du vælge ikonet Søg efter side eller rapport, angive **Brugere** og derefter vælge det relaterede link.
2. Vælg handlingen **Rettighedssæt** i vinduet **Brugere**.
3. Vælg handlingen **Ny** i vinduet **Rettighedssæt**.
4. Udfyld felterne på en ny linje efter behov.
5. Vælg handlingen **Rettigheder**.
6. Vælg handlingen **Start** i vinduet **Rettigheder**.

    En registreringsproces begynder at registrere alle dine handlinger i brugergrænsefladen.
7. Gå til de forskellige vinduer og aktiviteter i [!INCLUDE[d365fin](includes/d365fin_md.md)], som du vil give brugerne med dette rettighedssæt adgang til. Du skal udføre de opgaver, som du vil registrere rettigheder for.
8. Når du vil afslutte registreringen, skal du vende tilbage til vinduet **Rettigheder** og derefter vælge handlingen **Stop**.
9. Vælg knappen **Ja** for at føje de registrerede rettigheder til det nye rettighedssæt.
10. Angiv, om brugerne skal kunne indsætte, redigere eller slette poster i de registrerede tabeller for hvert objekt på listen over registrerede elementer. Se trin 7 i afsnittet "Sådan oprettes eller redigeres rettighedssæt manuelt".

### <a name="example---indirect-permission"></a>Eksempel - indirekte rettighed
Du kan tildele en indirekte rettighed for kun at bruge et objekt gennem et andet objekt.
En bruger kan f.eks. have rettighed til at køre codeunit 80, **Salgs-post** Codeunit **Salgs-post** udfører mange opgaver, herunder ændring af tabel 37, **Salgslinje**. Når brugeren bogfører et salgsdokument, codeunit **Salgs-post**, kontrollerer [!INCLUDE[d365fin](includes/d365fin_md.md)], om brugeren har rettighed til at ændre tabellen **Salgslinje**. Hvis ikke, kan codeunit'en ikke udføre sine opgaver, og brugeren får en fejlmeddelelse. I så fald kører codeunit'en korrekt.

Men brugeren behøver ikke at have fuld adgang til tabellen **Salgslinje** for at køre codeunit'en. Hvis brugeren har indirekte rettighed til tabellen **Salgslinje**, kører codeunit'en **Salgs-post** korrekt. Når en bruger har indirekte rettighed, kan brugeren kun redigere tabellen **Salgslinje** ved at køre codeunit'en **salgs-post** eller et andet objekt, der har rettighed til at ændre tabellen **Salgslinje**. Brugeren kan kun redigere tabellen **Salgslinje**, når det sker fra understøttede funktionalitetsområder. Brugeren kan ikke køre funktionen ved et uheld eller skadeligt ved andre metoder.

## <a name="see-also"></a>Se også
[Blive klar til at handle](ui-get-ready-business.md)  
[Velkommen til [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

