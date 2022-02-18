---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 02/09/2022
ms.author: edupont
ms.openlocfilehash: ff8d69a96fb34deb5a196067d553d72efb7f0813
ms.sourcegitcommit: 8a968e9176a913635e47e5170c66962e485e6689
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2022
ms.locfileid: "8105879"
---
Du kan bruge rykkere til at minde debitorer om forfaldne beløb. Du kan også bruge rykkere til at beregne renter eller gebyrer og inkludere dem på rykkeren.

Inden du kan oprette rykkere, skal du oprette betingelser og knytte dem til debitorerne. Du kan finde flere oplysninger i [Konfiguration af rykkerbetingelser og -niveauer](../finance-setup-reminders.md). [!INCLUDE [reminder-terms](reminder-terms.md)] Indholdet af siden **Rentebetingelser** er bestemmende for, om der beregnes rente på rykkeren.  

Du kan med mellemrum udføre kørslen **Opret rykkere** for at oprette rykkere til alle debitorer med forfaldne beløb, eller du kan oprette en rykker manuelt til en bestemt debitor og få linjerne beregnet og udfyldt automatisk.  

Du kan ændre rykkerne, når først du har oprettet dem. Den tekst, der vises i begyndelsen og slutningen af rykkeren, afhænger af betingelserne for rykkerniveauet og kan ses i kolonnen **Beskrivelse**. Hvis et beregnet beløb er blevet indsat automatisk i start- eller slutteksten, reguleres teksten ikke, hvis du sletter linjerne. Derefter skal du bruge funktionen **Opdater rykkertekst**.  

En debitorpost, hvor feltet **Afvent** er markeret, vil ikke udløse oprettelse af en rykker. Men hvis en rykker oprettes på basis af en anden post, vil en forfalden post, der er markeret som afventende, også blive inkluderet i rykkeren. Der beregnes ikke rente på linjer med disse poster.

Når du har oprettet rykkere og foretaget eventuelle nødvendige ændringer, kan du enten udskrive testrapporter eller udstede rykkere, typisk som mail.

### <a name="to-create-a-reminder-automatically"></a>Sådan oprettes en rykker automatisk

En rykker svarer til en faktura. Når du opretter en rykker, skal et rykkerhoved og en eller flere rykkerlinjer udfyldes. Du kan bruge en funktion til at oprette rykkere for alle kunder automatisk.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 0.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rykkere**, og vælg derefter det relaterede link.
2. Vælg handlingen **Opret rykkere** på siden **Rykkermeddelelse**.
3. På siden **Opret rykkere** skal du udfylde felterne for at angive, hvordan og hvem rykkerne oprettes til.
4. Vælg knappen **OK**.

### <a name="to-create-a-reminder-manually"></a>Sådan oprettes rykkere manuelt

På siden **Rykker** skal du udfylde oversigtspanelet **Generelt** manuelt og lade linjerne blive udfyldt automatisk.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig igen 2.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rykkere**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**.
4. Vælg handlingen **Foreslå rykkerlinjer**.
5. I kørslen **Foreslå rykkerlinjer** skal du udfylde felterne for at angive, hvordan og hvem rykkerne oprettes til.
6. Marker afkrydsningsfeltet **Medtag afventende poster**, hvis rykkere skal indeholde forfaldne åbne poster, som er i venteposition.
7. Marker afkrydsningsfeltet **Kun poster med forfaldne beløb**, hvis rykkere kun skal indeholde forfaldne åbne poster. Kun fakturaer og betalinger vises, da de er poster, hvor kundernes betalinger kan være forfaldne.

    > [!Important]
    > Afventende åbne poster indsættes, uanset hvilken indstilling der er markeret i afkrydsningsfeltet **Kun poster med forfaldne beløb**.

8. Vælg knappen **OK**.

### <a name="to-replace-reminder-texts"></a>Sådan erstattes rykkertekst

Du kan angive den tekst, der angives i rykkere, på flere måder. I nogle tilfælde kan du have brug for at erstatte start- og slutteksten, der er angivet for det aktuelle niveau, med tekst fra et andet niveau.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig endnu en gang 3.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rykkere**, og vælg derefter det relaterede link.
2. Åbn den relevante rykker, og vælg derefter handlingen **Opdater rykkertekst**.
3. Angiv det ønskede niveau i feltet **Rykkerniveau** på siden **Opdater rykkertekst**.
4. Klik på **OK** for at opdatere start- og slutteksten.

### <a name="to-issue-a-reminder"></a>Sådan udstedes en rykker

Når du har oprettet rykkere og foretaget eventuelle nødvendige ændringer, kan du enten udskrive testrapporter eller udstede rykkere.

Når du udsteder en rykker, overføres dataene til en separat side med udstedte rykkere. Samtidigt bogføres rykkerposter. Hvis der er beregnet rente eller ekstragebyr, bogføres posterne på debitorposten og finansposten.

Når man udsteder en rykker, bogføres posterne automatisk svarende til de betingelser, der er angivet på siden **Rykkerbetingelser**. Denne specifikation angiver, om renter og/eller gebyrer skal bogføres på debitorens konto og på finanskonti. Opsætningen på siden **Debitorbogføringsgrupper** angiver, hvilke konti der bogføres på.

Der er oprettet en post på siden **Rykker-/rentenotaposter** for hver debitorpost på rentenotaen.

Hvis afkrydsningsfelterne **Bogfør rente** eller **Bogfør opkrævningsgebyr** er markeret på siden **Rykkerbetingelser**, oprettes følgende poster også:

- Én post på siden **Debitorposter**
- Én betalingspost på den relevante finanskonto
- Én rente- og/eller en gebyrpost i den relevante finanskonto

Desuden kan udstedelse af en rykker medføre momsposteringer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig også her 4.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rykkere**, og vælg derefter det relaterede link.
2. Markér den relevante rykker, og vælg derefter handlingen **Udsted**.
3. På siden **Udsted rykkere** skal du udfylde felterne efter behov.
4. Vælg knappen **OK**.

Rykkeren udskrives enten eller sendes til en mail, der er angivet som en vedhæftet PDF-fil.

### <a name="to-cancel-an-issued-reminder"></a>Sådan annulleres en udstedt rykker

Hvis rykkere er blevet udstedt ved en fejl, kan du annullere dem, før de sendes. Det kan du gøre enten en for en eller som en kørsel.

1. På siden **Udstedte rykkere** skal du vælge en eller flere linjer for udstedte rykkere, som du vil annullere, og derefter vælge handlingen **Annuller**.
2. På siden **Annuller udstedte rykkere** skal du udfylde felterne efter behov, og derefter vælge knappen **OK**.


