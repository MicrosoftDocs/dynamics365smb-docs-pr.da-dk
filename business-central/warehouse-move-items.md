---
title: Flytte varer | Microsoft Docs
description: Når varer ligger på lager, kan de være nødvendigt at flytte dem mellem placeringer for at understøtte de daglige lageraktiviteter, som holder varerne i cirkulation på lageret. Nogle bevægelser sker i direkte forhold til interne operationer, som f.eks. en produktionsordre, der skal have komponenter leveret eller slutvarer lagt på lager. Andre bevægelser sker som ren optimering af lagerplads eller som ad hoc-bevægelser til og fra handlinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 4d6cc3353380aed83dbb0963d7602a4660e05f4b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196015"
---
# <a name="moving-items"></a>Flytte varer
Lageraktiviteten flytning af varer på lagerstedet udføres på forskellige måder, afhængigt af hvordan lagerfunktionerne er konfigureret. Detaljeringsgraden kan variere fra ingen lagerfunktioner over grundlæggende lageropsætninger for ordre-for-ordre-håndtering i kun en eller flere aktiviteter til avancerede konfigurationer, hvor alle lageraktiviteter skal udføres i en styret arbejdsgang. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).

Når varer ligger på én lagerlokation, kan de være nødvendigt at flytte dem mellem placeringer for at understøtte de daglige lageraktiviteter, som holder varerne i cirkulation på lageret. Nogle bevægelser sker i direkte forhold til interne operationer, som f.eks. en produktionsordre, der skal have komponenter leveret eller slutvarer lagt på lager. Andre bevægelser sker som ren optimering af lagerplads eller som ad hoc-bevægelser til og fra handlinger.

Yderligere flytningsopgaver er periodisk opfyldning af plukplaceringer eller produktionsplaceringer og ændring af oplysninger om placeringers indhold.

Hvis varerne flyttes til andre lokationer, har det indflydelse på vareposterne, og overflytningen skal derfor udføres via en overflytningsordre. Du kan finde flere oplysninger i [Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md).  

Lagerrelaterede opgaver med optælling, regulering og ompostering af varer kan omfatte lagerstedsopgaver, der skal udføres på lagerposter, før de kan blive synkroniseret med de tilknyttede vareposter. Du kan finde flere oplysninger i [Tælle, justere og ompostere inventar](inventory-how-count-adjust-reclassify.md)  

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Flytte varer mellem placeringer i grundlæggende lageropsætninger til enhver tid og uden kildedokumenter.|[Flytte varer i grundlæggende lageropsætninger](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Du kan bruge lagerbevægelseskladden til at flytte elementer i avancerede lageropsætninger, både for kildedokumenter og ad hoc.|[Flytte varer i avancerede lageropsætninger](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Sæt komponentvarer til interne operationer i grundlæggende lageropsætninger, som der anmodes om i kildedokumenter for operationerne.|[Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Planlægge, hvilke placeringer der skal opfyldes eller tømmes for at fastholde et effektivt flow, f.eks. tømme et bulkområde før en større tilgang.|[Planlægge lagerbevægelser i kladder](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Opdatere, hvor ofte placeringer, som f.eks. plukplaceringer, skal genopfyldes på grund af behovsændringer.|[Beregn genopfyldning](warehouse-how-to-calculate-bin-replenishment.md)|
|Omstrukturere lagerstedet med nye placeringskoder og nye karakteristika for placeringer og evt. flytte rundt på dem.|[Omstrukturere lagre](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
