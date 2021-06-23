---
title: Lager- og lagerstedrapporter og -analyse
description: Se, hvilke samling rapporter og analyser der er tilgængelige i standardversionen af Business Central, så du kan holde styr på virksomheden.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 8a4418699f28acd3ede80616ba69c56f50781e43
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216334"
---
# <a name="inventory-and-warehouse-reports-and-analytics-in-business-central"></a>Lager- og lagerstedrapporter og -analyse i Business Central

Lagerbeholdning og lagerstedsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] gør det muligt for lagerbeholdning og ansatte at få indsigt i og hente statistikker om aktuelle og tidligere lagerbeholdning og lagerstedsaktiviteter.  

## <a name="reports"></a>Rapporter

I følgende tabel beskrives nogle af nøglerapporterne i lagerbeholdning og lagerstedsrapportering.

|Report |Objekt-id|Beskrivelse  |
|---------|---------|---------|
|**Lagerbeholdning - tilgængelighedsplan**|707|Hvis du vil have en oversigt over specifikke varer/lagervarer og deres tilgængelighed. Denne rapport viser akkumulerede værdier som f. eks. bruttobehov, planlagte tilgange, lager osv. |
|**Lagerværdi**|1001|Viser lagerværdien for udvalgte varer på dit lager. Rapporten viser også oplysninger om værdien af forøgelse og reduktion af lageret over en given periode.|
|**Vareudløb - antal**|5809|Viser en oversigt over det antal udvalgte varer på lageret, hvor udløbsdatoen falder inden for en bestemt periode. Listen viser antallet af enheder for den udvalgte vare, der udløber inden for en angivet tidsperiode. Det udskrevne dokument viser antallet af enheder, der udløber inden for hver af tre perioder med samme varighed og det samlede lagerantal for hver af de varer, du har angivet under opsætning af rapporten.<br>Du kan bruge filtre til at angive, hvad der skal medtages i rapporten. Hvis du ikke angiver nogen filtre, medtages alle posterne i rapporten. Antallet i rapporten viser kun det antal af varen, hvor der er angivet en udløbsdato.|
|**Mængde - sammensætning af varens alder** eller **Værdi - sammensætning af varens alder**|5807 eller 5808|Viser en oversigt over den aktuelle alderssammensætning på bestemte varer i lagerbeholdningen. Oversigten viser, hvor mange enheder eller værdien af en bestemt vare der er tilføjet eller fjernet fra lageret, og hvornår det er gjort. Når der tilføjes eller fjernes varer fra lageret, skyldes det for eksempel køb, salg eller op- og nedreguleringer.|
|**Lagerbeholdsudgift og prisliste**|716|Viser en oversigt over prisoplysninger om de valgte varer eller lagervarer: købspris, sidste købspris, salgspris, avanceprocent og avance. |
|**Lagerplaceringsoversigt**|7319|Viser en oversigt over lagerplaceringer, deres opsætning og antallet af varer på placeringerne. Rapporten kan bruges til alle lokationer, hvor feltet er obligatorisk som obligatorisk. |
|**Lagerleverancestatus**|7313|Viser en oversigt pr. lokation over åbne kildedokumenter med varer, der er leveret eller som skal leveres. Rapporten kan bruges til alle lokationer, var **Påkrævede forsendelser** aktiveret. **Lagerleverance status** viser lokationer, placeringskoder, bilagsstatus, antal.|
|**Plukliste (lager)**|813|Viser en oversigt over de salgsordrer, en vare indgår i. Der vises følgende oplysninger om hver vare: salgsordrelinje med debitors navn, variantkode, lokationskode, placeringskode, afsendelsesdato, antal til levering og enhed. Antallet lægges sammen for hver vare. Rapporten kan f.eks. bruges, når der skal hentes varer fra lageret.<br>Bemærk! denne funktionalitet er ikke tilgængelig for avancerede lagerfunktioner.|
|**Regul.placering (logistik)**|7320|Denne specialrapport er kun beregnet til et forudindstillet lagersted og viser de Restantal, der stadig er gemt på selve reguleringsplaceringen. Normalt skal denne bestemte placering være tom. Den eneste årsag, hvor denne placering skal udfyldes, er som resultat af den fysiske optællings proces, eller om antallet af varer er fjernet eller føjet til lagerstedet|


## <a name="tasks"></a>Opgaver

I følgende artikler beskrives nogle af de vigtigste opgaver i forbindelse med analyse af virksomhedens tilstand:

* [Oprette analyserapporter](bi-how-create-analysis-views-reports.md)  
* [Vise varedisponering](inventory-how-availability-overview.md)


## <a name="see-also"></a>Se også

[Opsætning af lagerbeholdning](inventory-setup-inventory.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Logistik](warehouse-manage-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
