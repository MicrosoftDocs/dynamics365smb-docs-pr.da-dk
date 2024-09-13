---
title: Arbejde med kulstofkreditter
description: 'Få mere at vide om, hvordan du konfigurerer og køber kulstofkredit.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, carbon, credit, CO2'
ms.search.form: null
ms.date: 08/20/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: solsen
---

# Arbejde med kulstofkredit  

Når virksomheder ikke kan reducere deres emissioner af forskellige årsager, kan de købe kulstofkreditter for at kompensere for deres emissioner. Ved at købe kulstofkreditter kan en virksomhed stadig udlede den tilsvarende mængde gasser, mens den forbliver kulstofneutral. Disse kreditter købes fra specialiserede udbydere, hvilket tilskynder til emissionsreduktioner.  

Generelt er kulstofkreditter tilladelser, der giver ejeren mulighed for at udlede en vis mængde kuldioxid (CO₂) eller andre drivhusgasser (GHG'er). En kulstofkredit repræsenterer typisk retten til at udlede et ton CO₂ eller en tilsvarende mængde af en anden drivhusgas, så det er vigtigt at aktivere denne mulighed for nogle organisationer.  

## Konfigurer kulstofkreditten  

Kulstofkredit i [!INCLUDE[prod_short](includes/prod_short.md)] kan indstilles som **Vare**. Hvis du vil konfigurere **varen** som en kulstofkredit, skal du følge trinnene:
  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link. 
2. [Opret en ny vare som forklaret](inventory-how-register-new-items.md).   
3. Når varen er oprettet, skal du vælge **feltet Drivhusgaskredit** i **oversigtspanelet Bæredygtighed** og tilføje værdien af kulstofkredit ved hjælp af **feltet Kulstofkredit pr. UOM** .

> [!NOTE]
> **CO₂-kredit pr. måleenhed** repræsenterer mængden af CO₂ i den måleenhed, **der er konfigureret i emissionsenhedskoden** i **bæredygtighedsopsætningen**. Så dette betyder den samlede værdi af kulstofkredit som mængden af krediteret CO₂ pr **. Basisenhed** for brugt vare.  

> [!NOTE]
> Du kan konfigurere enhver type vare, uanset om det er lager, service eller ikke-lager, som en kulstofkredit.  

## At købe kulstofkredit 

### Købsdokumenter 

Hvis du vil arbejde med købsrelaterede dokumenter, skal du følge trinnene:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Ikon og:  
   1. Angiv **Købsfakturaer, hvis du vil have faktura som** bilagstype **·**, og vælg derefter de relaterede sammenkæde.  
   2. Angiv **Købsordrer**, hvis du vil have ordre som **bilagstype**, og vælg derefter de relaterede sammenkæde.   
2. Udfyld dokumenthovedet baseret på følgende vejledning [i, hvordan du arbejder med købsfakturaer og -ordrer](purchasing-how-record-purchases.md). 
3. Vælg elementet konfigurer som en kulstofkredit i feltet **Nr.** På købsdokumentlinjerne, og tilføj den relevante **Antal** og **Købspris**. 
4. Tilføj bæredygtighedskontonummeret **.** du ville bruge til at reducere din kuldioxid (CO₂) værdi. Systemet udfylder automatisk værdien i **feltet Emission CO2** baseret på den værdi, du har konfigureret i **feltet Kulstofkredit pr. UOM** på **Vare**  kort.
5. Bogfør dokumentet.

> [!NOTE]
> Selvom kulstofkredit reducerer værdien af poster, vil du se en positiv mængde værdi i udledningen af **CO2**. Men når du bogfører dokumentet, kan du se en værdi med en negativ log i bæredygtighedsposten med drivhusgaskreditten **som** bilagstype **.**  **·**  

### Bæredygtighedskladder 

Følg trinene for at arbejde med **Sustainability Journal** :  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bæredygtighedskladde**, og vælg derefter det relaterede link. 
2. På siden Bæredygtighedskladde **skal** du indtaste så mange linjer, som du vil bogføre i samme batch.  
3. Vælg GHG-kreditten **i** feltet **Bilagstype** .    
4. I feltet **Kontonr.** kan du kun vælge ikke-blokerede bæredygtighedskonti med feltet **Direkte bogføring** markeret, og hvor feltet **Bogføringstype** er angivet til **Bogfører**. Konti skal også være konfigureret med en kategori og en underkategori. Vælg den relevante konto for at bogføre kulstofkreditter.
5. Vælg **Manuel indtastning**, og indtast den værdi, du vil bogføre som en kulstofkreditering i **feltet Emission CO2** .  
6. Bogfør journalen.   

## Se også

[Finance](finance.md)    
[Registrer bæredygtighedsposter](finance-sustainability-journal.md)    
[Oversigt over styring af bæredygtighed](finance-manage-sustainability.md)    
[Opsætning af bæredygtighed](finance-sustainability-setup.md)   
[Diagram over bæredygtighedskonti og finans](finance-sustainability-accounts-ledger.md)  
[Ad hoc-analyse af bæredygtighedsdata](ad-hoc-analysis-sustainability.md)    
[Bæredygtighedsrapporter og analyser i [!INCLUDE[prod_short](includes/prod_short.md)]](sustainability-reports.md)   
[Bæredygtigheds-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
