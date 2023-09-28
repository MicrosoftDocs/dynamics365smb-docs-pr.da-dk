---
title: Konfigurere bedste fremgangsmåder - Genbestillingsmetoder | Microsoft Docs
description: 'Feltet Genbestillingsmetode på varekortene tilbyder fire forskellige planlægningsmetoder, der bestemmer, hvordan individuelle planlægningsparametre skal arbejde sammen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# Oprette bedste fremgangsmåder: Genbestillingspolitikker

Feltet **Genbestillingsmetode** på varekortene tilbyder fire forskellige planlægningsmetoder, der bestemmer, hvordan individuelle planlægningsparametre skal arbejde sammen.  

Ét grundlag for bedste fremgangsmåde til valg af en genbestillingsmetode er varens ABC-klassificering. Når du bruger ABC-klassificering til lagerstyring og forsyningsplanlægning, administreres varer i henhold til tre forskellige klasser, alt efter deres værdi og volumen i forhold til den samlede beholdning. I følgende tabel vises værdimængdefordelingen af de tre klasser.

|Klasse|Procent af total lagermængde|Procent af total lagerværdi|
|-----|-----------------------------|----------------------------|
|A|10-20|50-70|
|B|20|20|
|L|60-70|10-30|

ABC-klassificeringen angiver, at der kan spares besvær og penge ved at anvende løsere kontrol på varer med lav værdivolumen i forhold til varer med høj værdivolumen. Følgende illustration viser, hvilken genbestillingsmetode i [!INCLUDE[prod_short](includes/prod_short.md)], der er bedst egnet til henholdsvis A-, B- og C-elementer.

![ABC-klassificering.](media/abc_classification.png "ABC-klassificering")

Følgende tabel indeholder de bedste fremgangsmåder til at vælge mellem de fire politikker.  

|Opsætningsindstilling|Bedste fremgangsmåde|Bemærkning|  
|------------------|-------------------|-------------|  
|**Ordre**|Brug af A-varer.<br /><br /> Bruges til fremstil-til-ordre-varer.<br /><br /> Bruges i produktion til varer på øverste niveau og dyre komponenter og halvfabrikata.<br /><br /> Bruges til varer, der købes som direkte leveringer og særlige ordrer.<br /><br /> Brug ikke, hvis du ikke accepterer automatisk reservation.|A-varer, f.eks. lædersofaer i en møbelbutik, er varer af høj værdi med lav og uregelmæssig velocity, hvor lager er uacceptabelt eller de påkrævede attributter varierer. Den bedste genbestillingsmetode er derfor at planlægge specifikt til hvert behov.|  
|**Lot-for-Lot**|Brug af B-varer.<br /><br /> Bruges i produktion til komponenter, der forekommer i flere styklister. Dette sikrer, at købsordrer kombineres til samme leverandør, så der kan forhandles bedre priser.<br /><br /> Brug denne indstilling, hvis du er i tvivl om, hvilken genbestillingsmetode der skal vælges.|B-varer, f.eks. spisestuestole, har en regelmæssig og forholdsvis stor ordre velocity, men også høje lagerbindingsomkostninger. Den bedste genbestillingsmetode for B-varer er derfor en, der er økonomisk ved at samle behovet i bundter i genbestillingscyklussen.<br /><br /> 80 procent af varerne kan bruge denne metode.<br /><br /> Kan anvendes korrekt uden planlægningsparametre.|  
|**Fast genbestil.antal**|Brug af C-varer.<br /><br /> Kombinere med parametre for genbestillingspunkt.<br /><br /> Bruges i produktion til komponenter på laveste niveau.<br /><br /> Brug ikke, hvis varen ofte er reserveret.|C-varer, f.eks. tekopper, er varer af lav værdi med høj og regelmæssig ordre velocity. Den bedste genbestillingsmetode for C-varer er derfor en, der garanterer konstant tilgængelighed ved altid at være over et genbestillingspunkt.<br /><br /> Hvis brugeren reserverer en mængde til nogle fremtidige behov, forstyrres grundlaget for planlægningen. Selvom det planlagte beholdningsniveau er acceptabelt med hensyn til genbestillingspunkt, er mængderne muligvis ikke tilgængelige på grund af reservationen.|  
|**Maks. antal**|Bruges til C-varer med høje lagerbindingsomkostninger eller lagringsbegrænsninger.<br /><br /> Kombineres med en eller flere ordrefaktorer (Minimum/maksimum antal eller oprundingsfaktor).|C-varer, f.eks. tekopper, er varer af lav værdi med høj og regelmæssig ordre velocity. Den bedste genbestillingsmetode for C-varer er derfor en, der garanterer konstant tilgængelighed ved altid at være over et genbestillingspunkt, men under et maksimalt lagerantal.<br /><br /> Hvis du vil ændre den foreslåede ordre, vil du måske formindske ordrestørrelsen til en angiven maksimal ordrestørrelse, øge til en angiven minimumordrestørrelse eller runde op for at opfylde en angiven oprundingsfaktor. **Bemærk:** Hvis den anvendes med et genbestillingspunkt, forbliver lageret mellem genbestillingspunktet og det maksimale antal.|  

## Se også

 [Konfigurere bedste praksis: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
 [Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)  
 [Opret komplekse moduler ved hjælp af bedste praksis](set-up-complex-application-areas-using-best-practices.md)  
 [Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
