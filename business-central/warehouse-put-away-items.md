---
title: Lægge varer på lager | Microsoft Docs
description: Den lageraktivitet, der omfatter at lægge varer på lager, efter at de er modtaget eller udlagret, udføres på forskellige måder, afhængigt af hvordan logistikfunktionerne er konfigureret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d19486956fbaa0addb58a71c13849b0bb32c958a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771570"
---
# <a name="putting-items-away"></a>Lægge varer på lager
Den lageraktivitet, der omfatter at lægge varer på lager, efter at de er modtaget eller udlagret, udføres på forskellige måder, afhængigt af hvordan logistikfunktionerne er konfigureret. Detaljeringsgraden kan variere fra ingen lagerfunktioner over grundlæggende lageropsætninger for ordre-for-ordre-håndtering i kun en eller flere aktiviteter til avancerede konfigurationer, hvor alle lageraktiviteter skal udføres i en styret arbejdsgang. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).

Hvis du beslutter dig for at organisere og registrere læg-på-lager-oplysninger med lagerdokumenter, skal du markere feltet **Kræv læg-på-lager** på lokationskortet. Dette angiver, at når du har varer, der ankommer til lagerlokationen via et indgående kildedokument, skal læg-på-lager styres af systemet. Et indgående kildedokument kan være en købsordre, en salgsreturvareordre, en indgående overflytningsordre eller en produktionsordre, hvis afgang er klar til at blive lagt på lager.  

Hvis lokationen bruger læg-på-lager, men ikke modtagelse, kan du bruge siden **Læg-på-lager (lager)** til at organisere læg-på-lager-oplysningerne, udskrive dem, skrive resultatet af den faktiske læg-på-lager-aktivitet og bogføre læg-på-lager-oplysningerne, hvilket medfører, at modtagelsesoplysningerne for kildedokumentet også bogføres. Hvis der er tale om en produktionsordre, bogføres ordreafgangen, og produktionsordren afsluttes.

Hvis lokation kræver både modtagelse og læg-på-lager, dvs. hvis du har markeret både feltet **Kræv modtagelse** og feltet **Kræv læg-på-lager** på lokationskortet, er processen for at lægge varer på lager anderledes. I dette tilfælde skal du bruge siden **Læg-på-lager (logistik)** til at håndtere læg-på-lager-aktiviteten. Læg-på-lager i forbindelse med logistik fungerer på samme måde som læg-på-lager i forbindelse med lager, bortset fra at du registrerer læg-på-lager-aktiviteten i stedet for at bogføre oplysningerne. Bemærk, at registrering af læg-på-lager-aktiviteten ikke bogfører modtagelsen af varerne. Det opdaterer blot placeringsindholdet. Som lagerchef kan du bruge en læg-på-lager-kladde til at organisere læg-på-lager-oplysningerne, før du opretter de enkelte læg-på-lager-instruktioner (logistik).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Bogføre tilgangen af varer direkte fra det indgående ordredokument og dermed registrere læg-på-lager, fordi der ikke findes nogen lageropsætning.|[Modtage varer](warehouse-how-receive-items.md)|  
|Lægge varer på lager en ordre ad gangen og bogføre tilgangen i samme aktivitet i en grundlæggende lageropsætning.|[Lægge varer på lager med Læg-på-lager (lager)](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Lægge varer på lager for flere ordrer i en avanceret lageropsætning.|[Lægge varer på lager med Læg-på-lager (logistik)](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  
|Lægge producerede varer eller montagevarer på lager i en grundlæggende eller avanceret lageropsætning.|[Lægge produktions- eller montageafgange på lager](warehouse-how-to-put-away-production-output.md)|
|Planlægge optimerede instruktioner for læg-på-lager for et antal bogførte lagertilgange i stedet for at lade lagermedarbejdere håndtere tilgangene direkte.|[Planlægge læg-på-lager-aktiviteter i kladder](warehouse-how-to-plan-put-aways-in-worksheets.md)|  
|Lægge varer, der er plukket teknisk med et internt pluk, tilbage, f.eks. for en produktionsordre, der ikke forbrugte det forventede antal.|[Plukke og lægge på lager uden et kildedokument](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Opdele en læg-på-lager-linje for at placere en del af læg-på-lager-antallet på tilgængelige placeringer, fordi den anviste placering er fyldt op.|[Opdele lageraktivitetslinjer](warehouse-how-to-split-warehouse-activity-lines.md)|
|Få omgående adgang til læg-på-lager-varer, der er knyttet til dig som lagermedarbejder.|[Finde dine lageropgaver](warehouse-how-to-find-your-warehouse-assignments.md)|    

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]