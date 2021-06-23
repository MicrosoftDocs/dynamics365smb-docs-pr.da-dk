---
title: Arbejde med timesedler for sager | Microsoft Docs
description: Beskriver, hvordan du opretter en timeseddel for en sag, kopierer planlægningslinjer til den, angive arbejdstyper, udfylde timesedlen og sender den til godkendelse.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheets
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 279eb576e60f324d04e3c2dd58ba57e4e7ca68b8
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184345"
---
# <a name="use-time-sheets-for-jobs"></a>Bruge timesedler for sager

Du bruger kørslen **Opret timesedler** til at oprette timesedler for et angivet antal tidsperioder eller uger. Du skal have tilladelser for at kunne oprette timesedler.

Du kan kopiere og bruge dine sagsplanlægningslinjer i en timeseddel. På denne måde må du kun indtaste oplysninger på ét sted, og linjeoplysningerne vil altid være korrekte.

Når du har godkendt timeseddelposter for en sag, kan du bogføre dem i den relevante sagskladde eller ressourcekladde.

Før du kan bruge timesedler, skal du angive generelle oplysninger og angive en administrator og en eller flere godkendere af timesedler. Der er flere oplysninger i [Konfigurere timesedler](projects-how-setup-time-sheets.md).

## <a name="to-create-a-time-sheet"></a>Sådan opretter du en timeseddel

Du kan bruge kørslen **Opret timesedler** til at oprette timesedler for et angivet antal tidsperioder eller uger. Derefter kan timesedlens ejer åbne den og registrere tid, der har været brugt på en opgave.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Timesedler**, og vælg derefter det relaterede link.
2. På siden **Timeseddeloversigt** skal du vælge handlingen **Opret timesedler**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Felterne **Brug timeseddel** og **Bruger-id for timeseddelejer** skal udfyldes på kortet for ressourcen for timesedlen.
4. Vælg knappen **OK**.  

Du kan se de timesedler, du har oprettet, på siden **Timeseddeloversigt**.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Sådan kopieres sagsplanlægningslinjer til en timeseddel
Følgende procedure beskriver, hvordan du hurtigt føjer sagsplanlægningslinjer til en timeseddel.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Timesedler**, og vælg derefter det relaterede link.  
2. På siden **Timeseddeloversigt** skal du vælge en timeseddel for den relevante periode og derefter klikke på handlingen **Rediger timeseddel**.  
3. Vælg handlingen **Opret linjer fra sagsplanlægning**. Alle sagsplanlægningslinjer i timeseddeltidsperioden kopieres til timesedlen for personen eller maskinen i feltet **Ressourcenr.** på timesedlen.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Sådan definerer du arbejdstyper og tilføjer en til en timeseddel
Du kan definere arbejdstypen for alle timeseddellinjer for sager. På denne måde kan du tilføje oplysninger, du behøver for at fakturere debitoren for forskellige typer arbejde.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Timesedler**, og vælg derefter det relaterede link.   
2. Åbn den relevante timeseddel.
3. Vælg feltet **Beskrivelse**.  
4. På siden **Sagsdetaljer for timeseddellinje** skal du vælge feltet **Arbejdstypekode** og vælge en arbejdstype på listen, f.eks **Miles**.  
5. Hvis der ikke findes nogen arbejdstyper, skal du vælge handlingen **Ny**.
6. På siden **Arbejdstyper** skal du udfylde felterne efter behov.
7. Gentag trin 4 for at tildele den nye arbejdstype til timesedlen.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Sådan genbruges timeseddellinjer i andre timesedler
Hvis dine timeseddeloplysninger forbliver de samme fra tidsperiode til tidsperiode, kan du spare tid ved at kopiere linjerne fra den forrige tidsperiode. Derefter skal du kun angive tidsforbruget for den nye periode.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Timesedler**, og vælg derefter det relaterede link.  
2. Åbn timesedlen for en period efter perioden for en eksisterende timeseddel med linjer.  
3. Vælg handlingen **Kopier linjer fra en tidligere timeseddel**.

Linjerne kopieres, herunder oplysninger som type og beskrivelse. Hvis linjen f.eks. er knyttet til en sag, kopieres **Sagsnr.**. Alle kopierede linjer har statussen **Åben**. Du kan nu redigere linjerne efter behov.

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a>Sådan udfyldes en timeseddels linjer og sendes til godkendelse
Registrering af timesedler spores i timer, standardbasisenheden for ressourcer. En timeseddel har som standard almindelige arbejdsdage fra mandag til fredag.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Timesedler**, og vælg derefter det relaterede link.  
2. Vælg en timeseddel for den relevante periode, og vælg derefter handlingen **Rediger timeseddel**.  
3. Udfyld felterne på en linje efter behov. Angiv det antal timer, der bruges af ressourcen på hver ugedag.

    > [!TIP]  
    >   Du kan se summen af timeseddeltimer, du har angivet i faktaboksen **Faktisk/budgetteret oversigt**.  
4. Gentag trin 3 for andre arbejdstyper, der udføres af ressourcen.
5. Vælg handlingen **Send**, og vælg derefter handlingen **Alle åbne linjer** for at sende alle linjer eller handlingen **Kun valgte linjer** for kun at sende de linjer, der er valgt på siden **Timeseddel**.  

    > [!NOTE]  
    >   Du kan dog kun sende timeseddellinjer, som du har angivet tidspunkter for.  
6. Hvis du vil ændre oplysningerne på en linje, der er indstillet til **Sendt**, skal du markere linjen og derefter vælge handlingen **Åbn igen**.

    > [!NOTE]  
    >   En leder kan afvise en timeseddellinje, der er sendt til godkendelse. Hvis en linje har statussen **Afvist**, kan du foretage ændringer i linjen og derefter vælge **Send** igen.  
7. Vælg knappen **OK**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Sådan godkendes eller afvises en timeseddel
En timeseddel skal sendes til godkendelse, før den kan bruges. Du kan godkende og afvise individuelle linjer på en timeseddel eller sende dem tilbage til afsenderen til yderligere behandling. En timeseddel kan godkendes på to måder:

* En timeseddeladministrator kan godkende enhver timeseddel.
* Den person, der er angivet i feltet **Bruger-id for timeseddelgodkender** på et ressourcekort, kan godkende timesedler for den pågældende ressource. Der er flere oplysninger i [Konfigurere timesedler](projects-how-setup-time-sheets.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leders timesedler**, og vælg derefter det relaterede link.
2. Vælg en timeseddel på listen.  
3. På siden **Timeseddel** skal du vælge handlingen **Godkend** og derefter vælge handlingen **Alle sendte linjer** for at godkende alle linjer eller handlingen **Kun valgte linjer** for kun at godkende de linjer, der er valgt på siden **Timeseddel**.
4. Vælg knappen **OK**.  
5. Du kan også vælge handlingen **Afvis** og følge trin 4 til 5.  

> [!TIP]  
>   Brug faktaboksene **Timeseddelstatus** og **Faktisk/budgetteret oversigt** for at få et overblik over timeseddeloplysninger.

Når du har godkendt eller afvist en timeseddel, kan den ikke redigeres, medmindre den er blevet genåbnet. Følgende fremgangsmåde beskriver, hvordan du genåbner en godkendt eller afvist timeseddel.

## <a name="to-reopen-a-time-sheet"></a>Sådan genåbnes en timeseddel
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leders timesedler** eller **Timesedler**, og vælg derefter det relaterede link.
2. Åbn en timeseddel på listen.  

    > [!NOTE]  
    >   Du kan kun åbne linjer med statussen **Godkendt**. Du kan ikke genåbne linjer med statussen **Afvist**. Du kan ikke genåbne en timeseddel, hvis den er blevet bogført.  
3. På siden **Timeseddel** skal du vælge handlingen **Åbn igen** og derefter vælge handlingen **Alle sendte linjer** for at åbne alle linjer igen eller handlingen **Kun valgte linjer** for kun at åbne de linjer, der er valgt på siden **Timeseddel**, igen.
4. Vælg knappen **OK**. Status for timeseddellinjerne er ændringer for **Sendt**.  

## <a name="to-view-and-approve-time-sheets-by-job"></a>Sådan kan du se og godkende en timeseddel efter sag

Du kan for en sag angive en person, der er ansvarlig for sagen. Disse oplysninger er knyttet til timeseddellinjer og kan bruges til at angive en liste over timesedler, som en projektleder skal gennemse og godkende. Teamprojektlederen kan for eksempel være ansvarlig for bestemte sager i din virksomhed. I så fald bør lederen udpeges som **Ansvarlig person** på sagskortet. Du kan se sagsopgaver, der er knyttet til en sag, og antal timer brugt, i denne visning af timeseddeloplysninger.

> [!NOTE]
> Du skal godkende timesedler i vinduet **Leders timeseddel efter sag**, når du har valgt en indstilling for **Timeseddel efter sagsgodkendelse** på siden **Ressourceopsætning**. Der er flere oplysninger i [Konfigurere ressourcer](projects-how-setup-resources.md).

### <a name="to-approve-or-reject-a-time-sheet-by-job"></a>Sådan godkendes eller afvises en timeseddel efter sag

1. Indtast **Leders timeseddel efter sag** i feltet **Søg**, og vælg derefter det relaterede link. Microsoft Dynamics NAV viser en liste over timeseddellinjer, der er knyttet til de job, du har ansvaret for.
2. Vælg **Godkend** under fanen **Startside**. Vælg **Alle** for at godkende alle linjer. Vælg **Valgte** for kun at godkende markerede linjer.

    > [!NOTE]
    > Du kan kun godkende timesedler med status **Sendt**.

3. Markér en timeseddellinje, og vælg **Bemærkninger** under fanen **Naviger** for at give yderligere oplysninger om godkendelse eller afvisning. Indtast en dato i feltet **Dato**, og angiv en bemærkning i feltet **Bemærkning**.
4. Vælg knappen **OK**.

> [!NOTE]
> Når du har godkendt eller afvist en timeseddellinje efter sag, kan den ikke åbnes igen eller ændres i vinduet **Timeseddel**.

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Sådan bogfører du timeseddellinjer i en ressourcekladde
Når du har godkendt timeseddelposter for en ressource, kan du bogføre dem i den relevante ressourcekladde.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ressourcekladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Foreslå linjer fra timesedler**.  
3. Udfyld felterne efter behov.  
4. Vælg knappen **OK**. Der oprettes poster for forbrug i ressourcekladden, hvor du kan ændre oplysningerne efter behov.  
5. Vælg handlingen **Bogfør**.  
6. Vælg handlingen **Poster** for at bekræfte posteringen. Siden **Ressourceposter** åbnes og viser resultatet for bogføring af ressourcekladden.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Sådan bogfører du timeseddellinjer i en sagskladde
Når du har godkendt timeseddelposter for en sag, kan du bogføre dem i den relevante sagskladde.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sagskladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Foreslå linjer fra timesedler**.  
3. Udfyld felterne efter behov.  
4. Vælg knappen **OK**. Der oprettes poster for forbrug i sagskladden, hvor du kan ændre oplysningerne efter behov.  

    > [!NOTE]  
    >   Oplysninger om arbejdstype, og om arbejdet er fakturerbart, kopieres fra timeseddellinjen. Du kan om nødvendigt reducere antallet af timer og foretage en delvis bogføring. Hvis du reducerer antallet, sker der følgende: Næste gang, du vælger handlingen **Foreslå linjer fra timesedler**, vil den linje, der oprettes, indeholde den resterende mængde timer.  
5. Vælg handlingen **Bogfør**.  
6. Vælg handlingen **Poster** for at bekræfte posteringen. Siden **Sagsposter** åbnes og viser resultatet for bogføring af ressourcekladden.

## <a name="to-archive-time-sheets"></a>Sådan arkiveres timesedler
Når du har bogført timesedler, kan du arkivere dem til fremtidig reference. Alle linjer på timesedler skal bogføres, før en timeseddel kan arkiveres.

> [!NOTE]  
>   Når du arkiverer en timeseddel, fjernes den fra oversigterne på siden **Timesedler** og på siden **Leders timesedler**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Flyt timesedler til arkiv**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov, og vælg derefter knappen **OK**.  
3. Hvis du vil gennemgå arkiverede timesedler, skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Arkiver for timesedler** eller **Arkiver for leders timesedler** og derefter vælge det relaterede link.

## <a name="see-also"></a>Se også
[Projektstyring](projects-manage-projects.md)  
[Konfigurere projektstyring](projects-setup-projects.md)    
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)     
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]