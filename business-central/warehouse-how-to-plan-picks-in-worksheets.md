---
title: "Sådan planlægges pluk i kladder | Microsoft Docs"
description: "Hvis dit lagersted er sat op til at kræve både pluk- og leveringsbehandling, kan lagerstedet vælge at køre, så linjerne på forsendelsesdokumenterne ikke automatisk overføres til plukinstruktioner, men i stedet bliver tilgængelige i et arbejdsark."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 46c19e9fc255c34cfce6e547173f14f548785a0b
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="plan-picks-in-worksheets"></a>Planlægge pluk i kladder
Hvis dit lagersted er sat op til at kræve både pluk- og leveringsbehandling, kan lagerstedet vælge at køre, så linjerne på forsendelsesdokumenterne ikke automatisk overføres til plukinstruktioner, men i stedet bliver tilgængelige i et arbejdsark.  

> [!NOTE]  
>  Hvis plukinstruktionerne for lagerstedet allerede er oprettet, og du vil kombinere dem til én effektiv plukinstruktion, skal du slette de enkelte pluklister for lagerstedet. De linjer, der skal plukkes, kan nu anføres i plukkladden.  

I plukkladden kan du sætte pluklister op for medarbejderne, der reducerer den tid, de har til at flytte varerne på lagerpluklisten. Der er felter, der indeholder oplysninger om, hvor mange varer der er tilgængelige i de direkte afsendelsesplaceringer. Dette er nyttigt i forbindelse med planlægning af direkte afsendelsesplaceringer, fordi programmet altid foreslår et pluk fra en direkte afsendelsesplacering før en anden placering uden at tage højde for måleenheden. Linjerne i plukkladden kan komme fra forskellige kildedokumenter og kan sorteres efter vare, hyldenr. kildedokument, forfaldsdato eller leveringsadresse.  

Hvis du sorterer efter forfaldsdato, kan du vælge at slette alle linjer fra regnearket undtagen dem, der kræver øjeblikkelig behandling. De mindre hastende linjer slettes ikke som sådan, men sendes blot tilbage til **Plukkladden**. Når du opretter pluklisten, er linjerne allerede sorteret efter forfaldsdato, og du kan vælge at tildele pluklisten til en bestemt medarbejder.  

> [!NOTE]  
>  Pluk til lagerleverance af varer, der monteres til salgsordren, der leveres, følger de samme trin som for normale lagerpluk til leverance, som det er beskrevet i dette emne. Antallet af pluklinjer pr. antal til levering kan være mange til en, da du plukker komponenterne og ikke montageelementet.  
>   
>  Lagerpluklinjerne oprettes for værdien i feltet **Restantal** på linjerne for den montageordre, der er knyttes til salgsordren, der leveres. Dette sikrer, at alle komponenter plukkes i én handling.  
>   
>  Du kan finde flere oplysninger i afsnittet "Håndtere montageordrevarer i lagerleverancer" i Lagerleverance.  
>   
>  Se [Plukke til montage eller produktion i avancerede lageropsætninger](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md) for at få oplysninger om pluk af komponenter til montageordrer generelt, herunder situationer, hvor montageelementet ikke er forfaldent på en salgsleverance.  

## <a name="to-plan-picks-in-the-worksheet"></a>Sådan planlægges pluk i plukkladden  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Plukkladde**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Hent lagerdokumenter**.  
3.  Vælg de leverancer, som du vil forberede en plukliste til. Du kan nu sortere linjerne til en vis grad, men den sortering, du foretager her, videreføres ikke til plukinstruktionerne. Du kan også slette nogle af linjerne og derved oprette en mere effektiv plukliste. Hvis der f.eks. er en række linjer med varer i direkte afsendelsesplaceringer, kan du vælge at oprette pluklister til alle de linjer, der er relateret til disse linjer. Varerne i de direkte afsendelsesplaceringer forsendes sammen med de andre varer i forsendelsen, og de direkte afsendelsesplaceringer har plads til flere indkommende varer.  
4.  Vælg handlingen **Opret pluk**, og udfyld anmodningsvinduet **Opret pluk**. Den sortering, du anmoder om her, sorterer de pluklinjer, du opretter. Du kan f.eks. oprette en linje for hver zone og sortere linjerne efter placeringsorden inden for hvert pluk.  
5.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Pluk**, og vælg derefter det relaterede link. Vinduet **Pluk** åbnes.  
6.  Du kan nu se de pluktildelinger, du har oprettet, ved at vælge det pluk, der har det højeste nummer.  
7.  Hvis det er nødvendigt, kan du stadig ændre det tildelte bruger-id i plukket og den måde, som linjerne sorteres på..  
8.  Hvis du vil udskrive plukvejledningen, skal du vælge handlingen **Udskriv**.  
9. Når du har plukket varerne, skal du vælge handlingen **Registrer**.  

Hvis placeringerne er nummereret på en måde, der afspejler det fysiske lager, lader de linjer, der er sorteret efter placering, brugeren plukke et antal leverancer i én runde på lagerstedet. Medarbejderen tager det nødvendige antal varer for hver leverancelinje og anbringer dem sammen med de andre varer i leverancen. Der kan spares meget tid ved at plukke varer til flere leverancer på samme tid.  

En anden sorteringsmulighed er placeringsniveau, hvis det fysiske lager er indrettet efter niveau i stedet for efter kode.  

I plukkladden kan du også sortere efter leveringsadresse og derved samle og levere ordrer til kunder, der har adresse langt fra lageret, først.  

## <a name="see-also"></a>Se også
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

