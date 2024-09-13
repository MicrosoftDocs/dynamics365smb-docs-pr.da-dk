---
title: Bæredygtighed finansiel rapportering
description: 'Beskriver, hvordan du bruger finansielle rapporter til at oprette forskellige visninger og rapporter til analyse af bæredygtighedsdata.'
author: altotovi
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: '104, 108, 490'
ms.date: 08/22/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Analyse af bæredygtighedsposter med finansielle rapporter 

Funktionen *Finansielle rapporter* giver dig indsigt i de finansielle data, der vises i din kontoplan. Du kan konfigurere finansrapporter til at analysere tal i finanskonti og sammenligner finansposter med budgetposter. Men du kan også analysere statistiske data og bæredygtighedsdata med den samme funktion og endda kombinere alle tre typer data.  

## Forudsætninger for regnskabsaflæggelse  

Oprettelse af finansielle rapporter kræver en forståelse af strukturen af de data, du vil analysere. Der er nogle nøglebegreber, som du sandsynligvis skal være opmærksom på, før du designer dine finansielle rapporter: 

1. Relateret til kontoplanen: 
   1. Knyt finansbogføringskonti til finanskontokategorier. 
   2. Design, hvordan du bruger dimensioner.
   3. Konfigurere finansbudgetter.  
2. Relateret til bæredygtighed:   
   1. Opret dine bæredygtighedskonti. 
   2. Opsæt dine kulstofgebyrer og CO2e i **emissionsgebyrerne**.
   3. Design, hvordan du bruger dimensioner.  
3. Relateret til statistikregnskabet: 
   1. Oprette statistiske konti. 
   2. Design, hvordan du bruger dimensioner.  

> [!NOTE]
> Finansielle rapporter fungerer ikke direkte med CO2-, CH4- eller N2O-emissioner. I stedet bruger den CO2-ækvivalentmodellen, og det betyder, at du først skal konfigurere **CO2e**  (kuldioxidækvivalent) på **siden Emissionsgebyrer** .  

> [!NOTE]
> Du kan finde flere oplysninger om brug af finansielle rapporter med finansielle data og kontoplan her [Oprette finansielle rapporter ved hjælp af finansielle data og kontokategorier](bi-how-work-account-schedule.md).   

## Oprette en ny finansiel rapport  

Du kan starte med at kopiere en eksisterende finansiel rapport for hurtigt at oprette dine egne rapporter som beskrevet i trin 3 nedenfor. 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansielle rapporter**, og vælg derefter det relaterede link.  
2. På siden **Finansielle rapporter** skal du vælge **Ny** for at oprette et nyt navn til den finansielle rapport.  
3. Udfyld rapportens korte navn i **feltet Navn**  (du kan ikke ændre navnet senere), og angiv **Beskrivelse**.  
4. Vælg en rækkedefinition og en kolonnedefinition.   
5. Vælg handlingen **Rediger rapportdefinition**  for at få adgang til flere ejendomme i den økonomiske rapport.  
6. I oversigtspanelet **Indstillinger** kan du redigere rapportbeskrivelsen, ændre række- og kolonnedefinitionerne og definere, hvordan datoer skal vises. Datoer kan være et dag/uge/måned/kvartal/år-hierarki eller kan vises med regnskabsperioder. Du kan lære mere i [Sammenligne regnskabsperioder ved hjælp af periodeformler](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas). 
7. I oversigtspanelet **Dimensioner** kan du angive dimensionsfiltre for rapporten.  
8. Du kan få vist et eksempel på rapporten i området under oversigtspanelet **Dimensioner**.   

Hvis du vil analysere dine bæredygtigheds- eller statistiske data, kan du opnå dette ved at oprette **rækkedefinition**.  

Følg trinnene for at oprette eller redigere en rækkedefinition:

1. På siden **Finansielle rapporter** skal du vælge den relevante finansielle rapport og vælge **Rediger kolonnedefinition**. 
2. Oprette rækker som i følgende trin.  

> [!NOTE]
> **Rækkenummer** feltet viser de første 10 tegn i et id, f.eks. et kontonummer. Hvis du tilføjer elementer med id'er, der starter med de samme 10 tegn, vil du have dubletter i feltet **Rækkenr.** . Hvis det er nødvendigt, kan du redigere id'er manuelt, efter at du har indsat elementerne. De fulde id'er vises i feltet **Sammentælling**.

> [!NOTE]
> Du kan kombinere alle **sammentællingstyper**, dvs. bogføringskonti, Sust. Regnskab, statistisk konto.

> [!NOTE]
> Rækkedefinitioner versioneres ikke. Når du ændrer en rækkedefinition, erstattes den gamle version, og dine ændringer gemmes i databasen. 

### Analyse af bæredygtighedsdata  

1. Angiv rækkenummeret **.** For at identificere din rå og tilføje **Beskrivelse** som en tekst, der vises på finansrapportlinjen. 
2. I kolonnen Sammentællingstype skal du vælge Sust **. Mulighed for konti** .   
3. I feltet Sammentælling skal du vælge en eller flere bæredygtighedskonti ved hjælp af alle relevante filtre. 
4. Vælg en af følgende muligheder i **Beløbstype** :   
   1. **CO2e**, hvis du vil rapportere CO2-ækvivalentværdi fra feltet **CO2e-emission** i **bæredygtighedsposterne**. 
   2. **CO2-gebyr** hvis du vil rapportere økonomisk ækvivalent (CO2-gebyr) fra feltet **CO2-gebyr** i **bæredygtighedsposterne**. 
5. Hvis du vælger **Formel** som **Sammentællingstype**, kan du bruge matematiske formler i **kolonnen Sammentælling.**   

### Analyse af statistiske data

1. Angiv rækkenummeret **.** For at identificere din række og tilføje **Beskrivelse** som en tekst, der vises på linjen i den finansielle rapport. 
2.  **I kolonnen Sammentællingstype** skal du vælge **indstillingen Statistikkonti** .   
3.  **I feltet Sammentælling** skal du vælge en eller flere bæredygtighedskonti ved hjælp af alle relevante filtre. 
4. Hvis du vælger **Formel** som **Sammentællingstype**, kan du bruge matematiske formler i **kolonnen Sammentælling.**   

## Se også

[Oversigt over bæredygtighedsstyring](finance-manage-sustainability.md)    
[Bæredygtighedsrapporter og -analyser i Business Central](sustainability-reports.md)   
[Bæredygtigheds-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Forbered finansiel rapportering](bi-how-work-account-schedule.md)    
[rækkedefinition i finansiel rapportering](bi-row-definitions.md)    
[kolonnedefinition i finansiel rapportering](bi-column-definitions.md)    
[Finance](finance.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
