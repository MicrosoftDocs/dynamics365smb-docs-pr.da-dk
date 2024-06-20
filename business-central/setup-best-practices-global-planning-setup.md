---
title: Bedste fremgangsmåder for opsætning af global planlægning | Microsoft Docs
description: 'Oversigtpanelet Planlægning på siden Produktionsopsætning indeholder flere felter, der definerer globale regler for forsyningsplanlægning.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Konfigurere bedste fremgangsmåder: Global planlægningsopsætning
Oversigtpanelet **Planlægning** på siden **Produktionsopsætning** indeholder flere felter, der definerer globale regler for forsyningsplanlægning.  

 Følgende tabel viser de bedste fremgangsmåder til konfiguration af udvalgte globale felter med planlægningsparametre. Du kan få yderligere oplysninger om et felt ved at vælge linket i kolonnen **Opsætningsfelt**.  

|Angive indstillinger for felt|Bedste fremgangsmåde|Bemærkning|  
|-----------------|-------------------|-------------|  
|Forecast på lokationer|Vælg denne indstilling, hvis du har prognoser for bestemte lokationer.||  
|Komponenter på lokation|Hvis varerne ikke er defineret som lagervarer, skal du vælge lokationskoden til hovedlageret.|Dette gælder også, hvis du kun bruger indkøbskladden.|  
|Tomt overløbsniveau|Vælg **Tillad standardberegning** Hvis du overfører fra Microsoft Dynamics NAV 5.0 eller tidligere.|Skal kun bruges, hvis du vil tillade alle eller nogle af varerne at løbe over genbestillingspunktet.|  
|Standardbufferperiode|Indstillingen skal ligge mellem 1D og 5D.<br /><br /> Hvis du er nybegynder i planlægning i [!INCLUDE[prod_short](includes/prod_short.md)], skal du angive en længere periode.|Når brugerne er mere fortrolige med de forskellige årsager til aktionsmeddelelser, kan du afkorte bufferperioden for at tillade flere ændringsforslag.|  
|Standardbufferantal %|Indstilles til mellem 5 og 20 % af varens lotstørrelse.||  

## Se også  
 [Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)   
 [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
 [Opret komplekse moduler ved hjælp af bedste praksis](set-up-complex-application-areas-using-best-practices.md)  
 [Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]