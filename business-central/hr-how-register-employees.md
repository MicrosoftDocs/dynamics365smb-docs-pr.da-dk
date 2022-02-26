---
title: Konfigurere medarbejdere og redigere oplysninger
description: Beskriver, hvordan du bruger funktionen personale til at registrere nye medarbejdere eller redigere medarbejderoplysninger for eksisterende medarbejdere.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personnel, people, employee, staff, HR
ms.search.form: 5200, 5201
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: c3e8215f80d2d035643166832b866c569e1d2d1a
ms.sourcegitcommit: f4b32ba1f926a2a712400c36305616f320757723
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/08/2022
ms.locfileid: "8101103"
---
# <a name="register-employees"></a>Registrere medarbejdere
Hvis du vil bruge personale funktionen, skal du først tilføje medarbejderen ved at udfylde felterne på siden **medarbejderkort**.

## <a name="adding-new-customers"></a>Tilføje nye debitorer
Du kan tilføje nye medarbejdere manuelt ved at udfylde felterne på siden **medarbejderkort**, eller du kan bruge skabeloner, der indeholder foruddefinerede oplysninger. Du kan f. eks. oprette skabeloner til forskellige typer medarbejderprofiler. Du kan spare tid ved at bruge skabeloner, når du tilføjer nye medarbejdere, så oplysningerne bliver korrekte hver gang. Hvis du opretter skabeloner til mere end én type medarbejder, kan du vælge den skabelon, du vil bruge, når du tilføjer en medarbejder. Hvis du kun opretter én skabelon, vil den blive brugt til alle nye medarbejdere. Når du har oprettet en skabelon, kan du bruge handlingen **Anvend skabelon** for at anvende den på en eller flere valgte medarbejdere. Hvis du vil oprette en skabelon, skal du angive de oplysninger, du vil genbruge, på siden medarbejderkort og derefter gemme den som en skabelon.

> [!TIP]
> Det kan være nyttigt at tilpasse siden **medarbejderskabeloner**, når du opretter en skabelon. Du kan f. eks. tilføje et felt, der ikke allerede vises på siden. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Du kan til enhver tid redigere en medarbejders oplysninger. Det er lettere at udføre personaleopgaver, hvis medarbejderoplysningerne er opdateret. Hvis f.eks. en medarbejderadresse ændres, kan du registrere dette på medarbejderens kort.

> [!NOTE]  
> Du kan refundere medarbejdere for deres udgifter under forretningsaktiviteter. Til dette formål skal du udfylde felterne i oversigtspanelet **Betalinger** på siden **Medarbejderkort**. Du kan finde flere oplysninger i [Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md).

## <a name="to-set-up-an-employee"></a>Sådan oprettes en medarbejder
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Medarbejdere**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. På siden **Medarbejderkort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-insert-a-picture-of-an-employee"></a>Sådan indsætte et billede af en medarbejder
Hvis du har et billede af en medarbejder, kan du indsætte det på medarbejderkortet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Medarbejdere**, og vælg derefter det relaterede link.
2. Åbn kortet for den relevante medarbejder.
3. I faktaboksen **Medarbejderbillede** skal du klikke på rullelisten og derefter vælge **Indlæs**.
4. På siden **Vælg et billede til overførsel** skal du vælge knappen **Vælg**.
5. Vælg filen, og vælg derefter **Åbn**.

Billedet indsættes i faktaboksen **Medarbejderbillede**.

## <a name="to-register-various-information-about-an-employee"></a>Sådan registreres forskellige oplysninger om en medarbejder
På medarbejderkortet kan du angive oplysninger, som f.eks. medlemskab af fagforening, familiemedlemmer og kontrakter for medarbejderen. Følgende beskriver, hvordan du opretter en alternativ adresse. Trinene er de samme for alle andre oplysninger, du har angivet på et medarbejderkort.

Du kan bruge alternative adresser til at holde styr på medarbejdernes opholdssteder, f.eks. hvis medarbejderen er udstationeret i udlandet, er på en lang forretningsrejse eller bor på sin sommeradresse.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Medarbejdere**, og vælg derefter det relaterede link.
2. Åbn kortet for den relevante medarbejder.
3. Vælg handlingen **Alternative adresser**.
4. **På siden Alternativ adresseliste** skal du udfylde felterne efter behov.
5. Gentag trin 4 for hver alternative adresse.

## <a name="see-also"></a>Se også
[Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]