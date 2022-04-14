---
title: Konfigurere kontoplan (indeholder video)
description: Kontoplanen viser de finanskonti, hvor dine finansielle data er gemt. Du kan ændre standardkontiene i COA, og du kan tilføje nye konti.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.search.form: 16, 17, 18, 118, 386, 391
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: f2ef4432d91d9f647a4bea58febbdfd5513a4350
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520278"
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Konfigurere eller ændre kontoplanen

Kontoplanen viser de finanskonti, hvor dine finansielle data er gemt. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en standardkontoplan, der er klar til at understøtte din virksomhed.
Men du kan ændre standardkontiene, og du kan tilføje nye konti.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Tilføje eller ændre konti

Fra kontoplanen kan du åbne hver finanskonto og tilføje eller ændre indstillinger for hver konto. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Hvis det er nødvendigt, kan du bruge mere end én linje til et navn på en finanskonto. På **finanskontokortet** i **Konto**-gruppen skal du vælge **udvidede tekster** og derefter udfylde en eller flere linjer med den tekst, der skal kopieres, og kontonavnet.  

For kontoer af typen **I alt** skal du udfylde feltet **Sammentælling**. For kontoer af typen **Til-sum** udfyldes feltet automatisk af funktionen Indryk. Når du har oprettet kontiene, skal du vælge **proces**-handlinger og derefter vælge **Indryk kontoplan**.  

> [!IMPORTANT]
> Hvis du har angivet definitioner i felterne **I alt** for konti med **Til-sum**, før du anvender indrykningsfunktionen, skal du angive dem igen bagefter, fordi funktionen overskriver værdierne i alle felter med **Til-sum**.

## <a name="delete-accounts"></a>Slet konti

Du kan slette en finanskonto. Men før du sletter den, skal følgende være opfyldt:  

* Saldoen på kontoen skal være nul.  
* Feltet **Tillad sletning af finanskonti før** skal være indstillet på siden **Opsætning af Finans**, og der må ikke bogføres poster på kontoen på eller efter den pågældende dato.  
* Hvis feltet **Kontroller brug af finanskonto** på siden **Opsætning af Finans** er markeret, må kontoen ikke bruges i nogen bogføringsgrupper eller bogføringsopsætning.  

[!INCLUDE[prod_short](includes/prod_short.md)] forhindrer, at du kan slette en finanskonto, der indeholder data, der skal bruges i kontoplanen.  

## <a name="block-deletion-of-gl-accounts"></a>Bloker sletning af finanskonti

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

2022 udgivelsesbølge 2 introducerer en ekstra beskyttelse mod utilsigtet sletning af finanskonti i de situationer, hvor kriterierne er opfyldt.  

Et nyt felt, **bloker sletning af finanskonti**, føjes til **Finansopsætning**-siden. Feltet fungerer som en ekstra validering, når en bruger forsøger at slette en konto, hvor der er poster efter den dato, der er angivet i feltet **Kontroller finanskontosletning efter**.

Når feltet **Bloker sletning af finanskonti** er angivet til *Ja*, kan du ikke slette finanskonti, der er sagsposter efter den dato i feltet **Kontrollér sletning af finanskonto efter**. Hvis du vil slette en sådan konto, skal en bruger med adgang til siden **Finansopsætning** først angive feltet til *Nej*. Kontoen kan derefter slettes.  

Det anbefales, at du angiver feltet **Bloker sletning af finanskonti** til *Ja*. Det anbefales også, at du altid har en dato i feltet **Kontrollér sletning af finanskonto efter**, f. eks. det tidspunkt, hvor du skal gemme dine økonomi data.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Finans- og kontoplanen](finance-general-ledger.md)  
[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Importere data fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Arbejde med kontoskemaer](bi-how-work-account-schedule.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Nulstil konti til resultatopgørelse i den franske version](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Udskriv resultatopgørelser i den australske version](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Udskriv resultatopgørelser i den new zealandske version](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Oprette og lukke saldi for resultatopgørelse i den spanske version](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Indrykke kontoplanen og validere den i den spanske version](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]