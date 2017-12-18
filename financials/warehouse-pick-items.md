---
title: Plukke varer | Microsoft Docs
description: "Lageraktiviteten plukning af varer, før de afsendes eller forbruges kan udføres på forskellige måder, afhængigt af hvordan lagerfunktionerne er konfigureret. [Opsætningens](../configure-warehouse-processes.md) detaljeringsgrad kan variere fra ingen lagerfunktioner over grundlæggende lageropsætninger for ordre-for-ordre-håndtering i kun en eller flere aktiviteter til avancerede opsætninger, hvor alle lageraktiviteter skal udføres i en styret arbejdsgang."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 13db47dcfcc7eb6d30230490baa5ac961fc825a8
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="pick-items"></a>Plukke varer
Lageraktiviteten plukning af varer, før de afsendes eller forbruges kan udføres på forskellige måder, afhængigt af hvordan lagerfunktionerne er konfigureret. Detaljeringsgraden kan variere fra ingen lagerfunktioner over grundlæggende lageropsætninger for ordre-for-ordre-håndtering i kun en eller flere aktiviteter til avancerede konfigurationer, hvor alle lageraktiviteter skal udføres i en styret arbejdsgang. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).

Hvis du beslutter dig for at organisere og registrere plukaktiviteten med lagerdokumenter, skal du markere feltet **Kræv pluk** på lokationskortet. Dette angiver, at når du har varer, der skal plukkes i forbindelse med et udgående kildedokument, skal plukket af de pågældende varer styres af systemet. Et udgående kildedokument kan være en salgsordre, en købsreturvareordre, en udgående overflytning, en serviceordre eller en produktionsordre, hvor komponenterne er klar til at blive plukket.

> [!NOTE]
> Selv om indstillingen kaldes **Kræv pluk**, kan du bogføre leverancer direkte fra kildeforretningsdokumentet på den lokation, hvor du markerer dette afkrydsningsfelt.

Hvis lokationen er indstillet til at kræve pluk-, men ikke leverancebehandling, kan du bruge vinduet **Pluk (lager)** til at organisere plukoplysningerne, udskrive oplysningerne, skrive resultatet af plukningen og bogføre plukoplysningerne, hvilket medfører, at leverancen af varerne også bogføres. Hvis du plukker komponenter til en produktionsordre, bogføres forbruget også, hvis du bogfører plukket.

Hvis lokationen er indstillet til at kræve både pluk og leverance, dvs. at du har markeret både feltet **Kræv pluk** og feltet **Kræv leverance** på lokationskortet, kan du bruge vinduet **Pluk (logistik)** til at håndtere plukningen. Pluk i forbindelse med logistik fungerer på samme måde som pluk fra lager, bortset fra at du registrerer plukket i stedet for at bogføre plukoplysningerne. Registreringen medfører ikke, at leverancen bogføres, men blot, at varerne bliver tilgængelige til levering. Som lagerchef kan du bruge en plukkladde til at organisere plukoplysningerne, før du opretter de enkelte plukinstruktioner (logistik).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|
|------------|-------------|  
|Bogføre afsendelsen af varer direkte i det udgående ordredokument, fordi der ikke findes nogen lagerfunktioner. (Fungerer på samme måde for salgsordrer, udgående overflytningsordrer og returvareleverancer).|[Fremgangsmåde: Sende varer](warehouse-how-ship-items.md)|  
|Plukke varer en ordre ad gangen og bogføre afsendelsen i samme aktivitet i en grundlæggende lageropsætning.|[Sådan plukkes varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md)|
|Plukke varer for flere ordrer i en avanceret lageropsætning.|[Sådan plukkes varer med Pluk (logistik)](warehouse-how-to-pick-items-for-warehouse-shipment.md)|  
|Plukke komponenter til produktion eller montage i en grundlæggende eller avanceret lageropsætning.|[Fremgangsmåde: Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md)|  
|Planlægge optimerede plukinstruktioner for et antal forsendelser i stedet for at lade lagermedarbejderne håndtere bogførte forsendelser direkte.|[Sådan planlægges pluk i kladder](warehouse-how-to-plan-picks-in-worksheets.md)|  
|Plukke varer teknisk til et særligt formål, f.eks. til en produktionsenhed, der skal bruge ekstra komponenter, på en sådan måde, at varerne ikke teknisk forlader lagerstedet.|[Fremgangsmåde: Plukke og lægge på lager uden et kildedokument](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Forstå, hvordan du kan plukke varer ud fra deres udløbsdato, for eksempel letfordærvelige varer, automatisk.|[Plukke efter FEFO](warehouse-picking-by-fefo.md)|
|Opdel en pluklinje i flere linjer, f.eks. fordi der ikke er nok varer at tage af i den anviste placering.|[Fremgangsmåde: Opdele lageraktivitetslinjer](warehouse-how-to-split-warehouse-activity-lines.md)|
|Få umiddelbar adgang til pluk, der er tildelt til dig som lagermedarbejder.|[Fremgangsmåde: Finde lageropgaver](warehouse-how-to-find-your-warehouse-assignments.md)|  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

