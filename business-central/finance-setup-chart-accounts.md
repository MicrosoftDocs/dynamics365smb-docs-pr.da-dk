---
title: Konfigurere eller ændre kontoplan (indeholder video)
description: 'Få mere at vide om konfiguration af kontoplanen med de finanskonti, hvor dine finansielle data er gemt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 04/23/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Konfigurere eller ændre kontoplanen

Kontoplanen viser de finanskonti, hvor dine finansielle data er gemt. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en standardkontoplan, der er klar til at understøtte din virksomhed. Men du kan ændre standardkontiene, og du kan tilføje nye konti.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Tilføje eller ændre konti

Fra kontoplanen kan du åbne hver finanskonto og tilføje eller ændre indstillinger for hver konto. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Hvis det er nødvendigt, kan du bruge mere end én linje til et navn på en finanskonto. På **finanskontokortet** i **Konto**-gruppen skal du vælge **udvidede tekster** og derefter udfylde en eller flere linjer med kontonavnet og den kopierede tekst.  

For kontoer af typen **I alt** skal du udfylde feltet **Sammentælling**. For kontoer af typen **Til-sum** udfyldes feltet automatisk af funktionen Indryk. Når du har oprettet kontiene, skal du vælge **Proces**-handlinger og derefter vælge **Indryk kontoplan**.  

> [!IMPORTANT]
> Hvis du har angivet definitioner i felterne **I alt** for konti med **Til-sum**, før du anvender indrykningsfunktionen, skal du angive dem igen bagefter, fordi funktionen overskriver værdierne i alle felter med **Til-sum**.

## <a name="delete-accounts"></a>Slet konti

Du kan slette en finanskonto. Men før du sletter den, skal følgende betingelser være opfyldt:  

* Saldoen på kontoen skal være nul.  
* Feltet **Tillad sletning af finanskonti før** skal være indstillet på siden **Opsætning af Finans**, og der må ikke bogføres poster på kontoen på eller efter den pågældende dato.  
* Hvis feltet **Kontroller brug af finanskonto** på siden **Opsætning af Finans** er markeret, må kontoen ikke bruges i nogen bogføringsgrupper eller bogføringsopsætning.  

[!INCLUDE[prod_short](includes/prod_short.md)] forhindrer, at du kan slette en finanskonto, der indeholder data, der skal bruges i kontoplanen.  

Du kan også angive, hvornår folk skal have lov til at slette konti. På **Hovedbogsopsætning**-siden, fungerer **Bloker sletning af artskonti** sammen med datoen i **Tjek G/L Acc. Sletning efter**-feltet til at fungere som en ekstra validering. Hvis du aktiverer **Bloker sletning af finanskonti**, kan du ikke slette finanskonti, der er sagsposter efter den dato i feltet **Kontrollér sletning af finanskonto efter**. For at slette en sådan konto skal en person med adgang til **Hovedbogsopsætning**-siden skal **Bloker sletning af artskonti** slås fra.  

Hvis du aktiverer **Blokér sletning af feltet finanskonto**, er det ofte den bedste fremgangsmåde at indstille datoen i feltet **Kontroller, om finanskonto slettes efter**-feltet til den dato, hvor du skal gemme dine finansdata.  

### <a name="video-guidance"></a>Videovejledning

Denne video viser, hvordan man angiver, om og hvornår folk kan slette artskonti.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1g3oY]

## <a name="learning-path-set-up-the-chart-of-accounts-in-dynamics-365-business-central"></a>Læringssti: Konfigurere IC-kontoplanen i Dynamics 365 Business Central

Vil du lære, hvordan du kan konfigurere kontoplanen i [!INCLUDE [prod_short](includes/prod_short.md)]? Start derefter på følgende læringsforløb [Konfigurer kontoplanen i Dynamics 365 Business Central](/training/modules/chart-accounts-dynamics-365-business-central).

## <a name="see-also"></a>Se også

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
