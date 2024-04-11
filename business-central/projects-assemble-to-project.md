---
title: Montage til projekt
description: 'Få mere at vide om, hvordan du bruger montage til ordre til projekter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/03/2022
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Montage til projekt

Montage til projekt hjælper dig med at forbedre lagerstyringen ved kun at udføre montage til ordre, når det er nødvendigt.

Når du vælger en montage til ordre-vare på en projektplanlægningslinje, opretter [!INCLUDE [prod_short](includes/prod_short.md)] en montageordre. Montageordren er baseret på projektplanlægningslinjen, og de tilhørende linjer er baseret på varens montagestykliste. Hvis du vil vide mere om montagestyklister, skal du gå til [Arbejde med montagestyklister](assembly-how-work-assembly-boms.md). Antallet af komponenter på montagestyklisten ganges med ordreantallet. Siden **montage til ordre-linjer** viser detaljer om tilknyttede montageordrelinjer. Du kan bruge oplysningerne til at tilpasse montageelementet. Som ved salg kan du ikke bogføre sammenkædede montageordrer direkte. Du kan lære mere om montageordrer ved at gå til [Sådan sælges lagervarer i montage efter ordre-forløb](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).

Montageordrer er reserveret til projekter, og [!INCLUDE [prod_short](includes/prod_short.md)] synkroniserer varesporing mellem projektplanlægningslinjer og montageordre.

## Integrere med lagerstedsstyring

Montage til projekt integreres med lagerstyringsfunktioner for at gøre montage og forsendelse nemmere. Processen er også med til at sikre, at flowet fra projektmontage til levering forløber problemfrit i interne lagerstedsprocesser. Du kan få mere at vide om interne lagerflow for projekter ved at gå til [Flows til produktion, montage og sager](design-details-internal-warehouse-flows.md#flows-to-and-from-assembly-in-a-basic-warehouse-configuration).

I følgende tabel beskrives de lagerstedskonfigurationer, som montage til ordre understøtter.

|Konfiguration  |Beskrivelse  |
|---------|---------|
|**Ingen lagerstedshåndtering**|Brug en projektkladde til at bogføre helt eller delvist forbrug. Afgang og forbrug af komponenter bogføres automatisk for montageordren.         |
|**Lagerpluk**|Brug lagerpluk til at bogføre helt eller delvist forbrug. Afgang og forbrug af komponenter bogføres automatisk for montageordren.          |
|**Lagerpluk**|Opret og registrer lagerpluk for komponenter, og brug derefter en projektkladde til at bogføre forbrug. [!INCLUDE [prod_short](includes/prod_short.md)] kontrollerer, om de forbrugte montagekomponenter blev plukket. Afgang og forbrug af komponenter bogføres automatisk for montageordren.         |

## Kendte begrænsninger

I dette afsnit beskrives kendte begrænsninger for montage til projekt.

* Feltet **Antal til montage til ordre** er ikke tilgængeligt for projekter, der er lukket.
* I forbindelse med lagerplukscenarier kan **Antal til montage til ordre** enten være nul eller lig med antallet. Du kan ikke blande montage til ordre og montage til lager på en projektplanlægningslinje. Du skal oprette separate projektplanlægningslinjer.
* Montage til ordre påvirker ikke de fakturerbare dele af et projekt. En montage medtages på salgsfakturaer, men ikke på dens komponenter. Du kan ikke redigere feltet **Antal til montage til ordre** for fakturerbare linjer.
* Ordreplanlægning og planlægningskladden påvirkes ikke, fordi projektet er input til planlægningen. I planlægningsprogrammet betragtes montagen som efterspørgsel.
* Du kan ikke angive et negativt antal i feltet **Antal til montage til ordre**.
* Du kan ikke fortryde en montage.

## Se også

[Projektstyring](projects-manage-projects.md)  
[Montagestyring](assembly-assemble-items.md)  
[Oprette sager](projects-how-create-jobs.md)
