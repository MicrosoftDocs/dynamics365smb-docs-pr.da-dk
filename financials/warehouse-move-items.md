---
title: Flytte varer | Microsoft Docs
description: "Når varer ligger på lager, kan de være nødvendigt at flytte dem mellem placeringer for at understøtte de daglige lageraktiviteter, som holder varerne i cirkulation på lageret. Nogle bevægelser sker i direkte forhold til interne operationer, som f.eks. en produktionsordre, der skal have komponenter leveret eller slutvarer lagt på lager. Andre bevægelser sker som ren optimering af lagerplads eller som ad hoc-bevægelser til og fra handlinger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5b8ddfc5e255dbaf20027c27c9c0210e4479a681
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="moving-items"></a>Flytte varer
Lageraktiviteten flytning af varer på lagerstedet udføres på forskellige måder, afhængigt af hvordan lagerfunktionerne er konfigureret. Detaljeringsgraden kan variere fra ingen lagerfunktioner over grundlæggende lageropsætninger for ordre-for-ordre-håndtering i kun en eller flere aktiviteter til avancerede konfigurationer, hvor alle lageraktiviteter skal udføres i en styret arbejdsgang. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).

Når varer ligger på én lagerlokation, kan de være nødvendigt at flytte dem mellem placeringer for at understøtte de daglige lageraktiviteter, som holder varerne i cirkulation på lageret. Nogle bevægelser sker i direkte forhold til interne operationer, som f.eks. en produktionsordre, der skal have komponenter leveret eller slutvarer lagt på lager. Andre bevægelser sker som ren optimering af lagerplads eller som ad hoc-bevægelser til og fra handlinger.

Hvis varerne flyttes til andre lokationer, har det indflydelse på vareposterne, og overflytningen skal derfor udføres via en overflytningsordre. Du kan finde flere oplysninger i [Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md).  

Yderligere flytningsopgaver er periodisk opfyldning af plukplaceringer eller produktionsplaceringer og ændring af oplysninger om placeringers indhold.  

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

