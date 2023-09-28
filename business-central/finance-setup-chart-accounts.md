---
title: Konfigurere eller ændre kontoplan (indeholder video)
description: 'Kontoplanen viser de finanskonti, hvor dine finansielle data er gemt. Du kan ændre standardkontiene i COA, og du kan tilføje nye konti.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 01/21/2022
ms.author: bholtorf
---
# Konfigurere eller ændre kontoplanen

Kontoplanen viser de finanskonti, hvor dine finansielle data er gemt. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en standardkontoplan, der er klar til at understøtte din virksomhed. Men du kan ændre standardkontiene, og du kan tilføje nye konti.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## Tilføje eller ændre konti

Fra kontoplanen kan du åbne hver finanskonto og tilføje eller ændre indstillinger for hver konto. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Hvis det er nødvendigt, kan du bruge mere end én linje til et navn på en finanskonto. På **finanskontokortet** i **Konto**-gruppen skal du vælge **udvidede tekster** og derefter udfylde en eller flere linjer med kontonavnet og den kopierede tekst.  

For kontoer af typen **I alt** skal du udfylde feltet **Sammentælling**. For kontoer af typen **Til-sum** udfyldes feltet automatisk af funktionen Indryk. Når du har oprettet kontiene, skal du vælge **proces**-handlinger og derefter vælge **Indryk kontoplan**.  

> [!IMPORTANT]
> Hvis du har angivet definitioner i felterne **I alt** for konti med **Til-sum**, før du anvender indrykningsfunktionen, skal du angive dem igen bagefter, fordi funktionen overskriver værdierne i alle felter med **Til-sum**.

## Slet konti

Du kan slette en finanskonto. Men før du sletter den, skal følgende være opfyldt:  

* Saldoen på kontoen skal være nul.  
* Feltet **Tillad sletning af finanskonti før** skal være indstillet på siden **Opsætning af Finans**, og der må ikke bogføres poster på kontoen på eller efter den pågældende dato.  
* Hvis feltet **Kontroller brug af finanskonto** på siden **Opsætning af Finans** er markeret, må kontoen ikke bruges i nogen bogføringsgrupper eller bogføringsopsætning.  

[!INCLUDE[prod_short](includes/prod_short.md)] forhindrer, at du kan slette en finanskonto, der indeholder data, der skal bruges i kontoplanen.  

## Bloker sletning af finanskonti

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

2022 udgivelsesbølge 2 introducerer en ekstra beskyttelse mod utilsigtet sletning af finanskonti i de situationer, hvor kriterierne er opfyldt.  

Et nyt felt, **bloker sletning af finanskonti** er blevet føjet til **Finansopsætning**-siden. Når feltet er indstillet til *Ja*, fungerer feltet som en ekstra vurdering, der betyder, at du ikke kan slette finanskonti med poster efter den dato i feltet **Kontrollér sletning af finanskonto efter**. Hvis du vil slette en sådan konto, skal en bruger med adgang til siden **Finansopsætning** først angive feltet til *Nej*.  

Hvis du angiver en **Blokér sletning af feltet finanskonto** til *Ja*, kan det anses for at være en bedste fremgangsmåde, da datoen i feltet **Kontroller, om finanskonto slettes efter**-feltet f.eks. er den dato, hvor du skal gemme dine finansdata.  

## Se også

[Finans- og kontoplanen](finance-general-ledger.md)  
[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Importere data fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Arbejde med finansielle rapporter](bi-how-work-account-schedule.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Nulstil konti til resultatopgørelse i den franske version](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Udskriv resultatopgørelser i den australske version](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Udskriv resultatopgørelser i den new zealandske version](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Oprette og lukke saldi for resultatopgørelse i den spanske version](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Indrykke kontoplanen og validere den i den spanske version](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
