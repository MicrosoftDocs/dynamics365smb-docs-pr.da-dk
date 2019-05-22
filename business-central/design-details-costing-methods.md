---
title: Designoplysninger – Kostmetoder | Microsoft Docs
description: Kostmetoden afgør, om en faktisk eller en budgetteret værdi føres som aktiv og bruges i beregningen af kostprisen. Sammen med bogføringsdatoen og rækkefølgen har kostmetoden også indflydelse på, hvordan kostprisforløbet registreres.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1175a7fe058de5f8e7876014d8a71227b7cc46d8
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243936"
---
# <a name="design-details-costing-methods"></a>Designoplysninger: Kostmetoder
Kostmetoden afgør, om en faktisk eller en budgetteret værdi føres som aktiv og bruges i beregningen af kostprisen. Sammen med bogføringsdatoen og rækkefølgen har kostmetoden også indflydelse på, hvordan kostprisforløbet registreres. Følgende metoder understøttes i [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

|Kostmetode|Beskrivelse|Hvornår skal den bruges|  
|--------------------|---------------------------------------|-----------------|  
|FIFO|En vares kostpris er den faktiske værdi af alle modtagelser af varen, som vælges af FIFO-reglen.<br /><br /> I lagerværdien forudsættes det, at de første varer, der lægges på lager, bliver solgt først.|I virksomhedsmiljøer, hvor produktomkostninger er stabile.<br /><br /> (Når priser stiger, viser balancen højere værdi. Dette betyder, at skatteforpligtelserne øges, men kreditvurderinger og muligheden for at låne penge forbedres.)<br /><br /> For varer med en begrænset hyldelevetid, fordi de ældste varer skal sælges, inden de overskrider deres sidste salgsdato.|  
|LIFO|En vares kostpris er den faktiske værdi af alle modtagelser af varen, som vælges af LIFO-reglen.<br /><br /> I lagerværdien forudsættes det, at de sidste varer, der lægges på lager, bliver solgt først.|Forbudt i mange lande/områder, da det kan bruges til at holde avancen nede.<br /><br /> (Når priser stiger, falder værdien på resultatopgørelsen. Dette betyder, at skatteforpligtelserne reduceres, men muligheden for at låne penge forringes.)|  
|Gennemsnit|En vares kostpris beregnes som den gennemsnitlige kostpris på hvert enkelt tidspunkt efter et køb.<br /><br /> For værdiansættelse af lageret antages det, at alle lagerbeholdninger sælges samtidig.|I virksomhedsmiljøer, hvor produktomkostninger er ustabile.<br /><br /> Når lagre stables eller blandes sammen, og der ikke kan skelnes mellem dem, f.eks. kemikalier.|  
|Bestemt|En vares kostpris er den præcise kostpris, som den aktuelle enhed er modtaget til.|I produktion eller handel med varer, der nemt kan identificeres, med forholdsvis høje kostpriser.<br /><br /> For varer, der er omfattet af regulering.<br /><br /> For varer med serienumre.|  
|Standard|En vares kostpris forudindstilles baseret på forventninger.<br /><br /> Når det faktiske kostbeløb realiseres senere, skal standardkostprisen reguleres til de faktiske omkostninger gennem variansværdier.|Hvor omkostningsstyring er afgørende.<br /><br /> I serieproduktion til at evaluere kostpriserne for direkte materialeomkostninger, arbejdsomkostninger og produktionsomkostninger.<br /><br /> Hvor der er disciplin og personale til at vedligeholde standarderne.|  

 Følgende billede viser, hvordan omkostningerne passerer gennem lageret for hver kostmetode.  

 ![Kostmetoder](media/design_details_inventory_costing_7_costing_methods.png "Kostmetoder")  

 Kostmetoder varierer i den måde, hvorpå de værdiansætter lagerreduceringer, og om de bruger faktiske omkostninger eller standardomkostninger som værdigrundlag. Den følgende tabel beskriver de forskellige karakteristika. (LIFO-metoden er udelukket, da den minder meget om FIFO-metoden).  

||FIFO|Gennemsnit|Standard|Bestemt|  
|-|----------|-------------|--------------|--------------|  
|Generelle egenskaber|Let at forstå|Baseret på periodeindstillinger: **dag**/**uge**/**måned**/**kvartal**/**regnskabsperiode**.<br /><br /> Kan beregnes pr. vare eller pr. vare/lokation/variant.|Let at bruge, men kræver kvalificeret vedligeholdelse.|Kræver varesporing på både indgående og udgående transaktion.<br /><br /> Bruges typisk til serienummererede varer.|  
|Udligning/justering|Udligning holder styr på **det resterende antal**.<br /><br /> Justering overfører omkostninger i henhold til antalsudligning.|Udligning holder styr på **det resterende antal**.<br /><br /> Omkostninger beregnes og overføres pr. **værdiansættelsesdato**.|Udligning holder styr på **det resterende antal**.<br /><br /> Udligning er baseret på FIFO.|Alle udligninger er faste.|  
|Regulering|Værdiregulerer kun fakturerede antal.<br /><br /> Kan foretages pr. vare eller pr. varepost.<br /><br /> Kan foretages bagudrettet.|Værdiregulerer kun fakturerede antal.<br /><br /> Kan kun foretages pr. vare.<br /><br /> Kan foretages bagudrettet.|Værdiregulerer fakturerede og ikke-fakturerede antal.<br /><br /> Kan foretages pr. vare eller pr. varepost.<br /><br /> Kan foretages bagudrettet.|Værdiregulerer kun fakturerede antal.<br /><br /> Kan foretages pr. vare eller pr. varepost.<br /><br /> Kan foretages bagudrettet.|  
|Diverse|Hvis du baguddaterer en lagerreducering, bliver eksisterende poster IKKE genanvendt for at sikre et korrekt FIFO-omkostningsforløb.|Hvis du baguddaterer en lagerforøgelse eller -reducering, genberegnes den gennemsnitlige kostpris, og alle berørte poster justeres.<br /><br /> Hvis du ændrer perioden eller beregningstypen, skal alle berørte poster reguleres.|Brug siden **Standardkladde** til regelmæssigt at opdatere og akkumulere standardomkostninger.<br /><br /> Understøttes ikke pr. lagervare.<br /><br /> Der findes ingen historiske poster for standardomkostninger.|Du kan bruge specifik varesporing uden at bruge den specifikke kostmetode. Derefter følger prisen IKKE lotnummeret, men omkostningsforventningen for den valgte kostmetode.|  

## <a name="example"></a>Eksempel  
 Dette afsnit indeholder eksempler på, hvordan forskellige kostmetoder påvirker lagerværdien.  

 Følgende tabel viser lagerforøgelser og -reduceringer, som eksemplerne er baseret på.  

|Bogføringsdato|Antal|Løbenr.|  
|------------------|--------------|---------------|  
|01-01-20|1|1|  
|01-01-20|1|2|  
|01-01-20|1|3|  
|02-01-20|-1|4|  
|03-01-20|-1|5|  
|04-01-20|-1|6|  

> [!NOTE]  
>  Det resulterende antal i lageret er nul. Derfor skal lagerværdien også være nul, uanset hvilken kostmetode der anvendes.  

### <a name="effect-of-costing-methods-on-valuing-inventory-increases"></a>Kostmetoders indflydelse på værdiansættelse af lagerforøgelser  
 **FIFO**/**LIFO**/**Gennemsnit**/**Specifik**  

 For varer med kostmetoder, der bruger de faktiske omkostninger som grundlag for værdiansættelsen (**FIFO**, **LIFO**, **Gennemsnit**, eller **Specifik**), værdiansættes lagerforøgelser til varens anskaffelsesomkostninger.  

 Følgende tabel viser, hvordan lagerforøgelser værdisættes i alle kostmetoder, undtagen **Standard**.  

|Bogføringsdato|Antal|Kostbeløb (faktisk)|Løbenr.|  
|------------------|--------------|----------------------------|---------------|  
|01-01-20|1|10,00|1|  
|01-01-20|1|20,00|2|  
|01-01-20|1|30,00|3|  

 **Standard**  

 For varer, der bruger kostmetoden **Standard** værdiansættes lagerforøgelser til varens aktuelle standardkostpris.  

 Følgende tabel viser, hvordan lagerforøgelser værdisættes i **Standard**-kostmetoden.  

|Bogføringsdato|Antal|Kostbeløb (faktisk)|Løbenr.|  
|------------------|--------------|----------------------------|---------------|  
|01-01-20|1|15.00|1|  
|01-01-20|1|15.00|2|  
|01-01-20|1|15.00|3|  

### <a name="effect-of-costing-methods-on-valuing-inventory-decreases"></a>Kostmetoders indflydelse på værdiansættelse af lagerreduktioner  
 **FIFO**  

 For varer, der benytter kostmetoden **FIFO**, sælges varer, der er købt først, altid først (løbenumre 3, 2 og 1 i dette eksempel). Ligeledes værdiansættes lagerreducering ved at tage værdien af den første lagerforøgelse.  

 VAREFORBRUG beregnes ud fra værdien af de første lageranskaffelser.  

 Følgende tabel viser, hvordan lagerreduktioner værdisættes til **FIFO**-kostmetoden.  

|Bogføringsdato|Antal|Kostbeløb (faktisk)|Løbenr.|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-10,00|4|  
|03-01-20|-1|-20,00|5|  
|04-01-20|-1|-30,00|6|  

 **LIFO**  

 For varer, der benytter kostmetoden **LIFO**, sælges varer, der er købt senest, altid først (løbenumre 3, 2 og 1 i dette eksempel). Ligeledes værdiansættes lagerreduceringer ved at tage værdien af den seneste lagerforøgelse.  

 VAREFORBRUG beregnes ud fra værdien af de seneste lageranskaffelser.  

 Følgende tabel viser, hvordan lagerreduktioner værdisættes til **LIFO**-kostmetoden.  

|Bogføringsdato|Antal|Kostbeløb (faktisk)|Løbenr.|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-30,00|4|  
|03-01-20|-1|-20,00|5|  
|04-01-20|-1|-10,00|6|  

 **Gennemsnit**  

 For varer, der bruger kostmetoden **Gennemsnit**, værdiansættes lagerreduktioner ved at beregne et vægtet gennemsnit af det resterende lager på den sidste dag i den gennemsnitlige omkostningsperiode, hvor lagerreduktionen blev bogført. Du kan finde flere oplysninger i [Designoplysninger: Gennemsnitlig kostpris](design-details-average-cost.md).  

 Følgende tabel viser, hvordan lagerreduktioner værdisættes i **Gennemsnit**-kostmetoden.  

|Bogføringsdato|Antal|Kostbeløb (faktisk)|Løbenr.|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-20,00|4|  
|03-01-20|-1|-20,00|5|  
|04-01-20|-1|-20,00|6|  

 **Standard**  

 For varer, der benytter kostmetoden **Standard**, værdiansættes lagerreduceringer svarende til kostmetoden **FIFO**, bortset fra at værdiansættelse er baseret på standardomkostninger, ikke på de faktiske omkostninger.  

 Følgende tabel viser, hvordan lagerreduktioner værdisættes i **Standard**-kostmetoden.  

|Bogføringsdato|Antal|Kostbeløb (faktisk)|Løbenr.|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-15,00|4|  
|03-01-20|-1|-15,00|5|  
|04-01-20|-1|-15,00|6|  

 **Bestemt**  

 I kostmetoder arbejdes der ud fra en antagelse om, hvordan kostprisen flyder fra en lagerforøgelse til en lagerreduktion. Hvis der findes mere nøjagtige oplysninger om kostprisforløbet, kan du dog tilsidesætte denne antagelse ved at oprette en fast udligning mellem poster. En fast udligning opretter et link mellem en lagerreducering og en bestemt lagerforøgelse og angiver kostprisforløbet i overensstemmelse hermed.  

 For varer, der benytter kostmetoden **Specifik**, værdiansættes lagerreduceringer i henhold til den lagerforøgelse, der er tilknyttet med den faste udligning.  

 Følgende tabel viser, hvordan lagerreduktioner værdisættes i **Specifik**-kostmetoden.  

|Bogføringsdato|Antal|Kostbeløb (faktisk)|Udlign.postløbenr.|Løbenr.|  
|------------------|--------------|----------------------------|-----------------------|---------------|  
|02-01-20|-1|-20,00|**2**|4|  
|03-01-20|-1|-10,00|**1**|5|  
|04-01-20|-1|-30,00|**3**|6|  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)   
 [Designoplysninger: Afvigelse](design-details-variance.md)   
 [Designoplysninger: Gennemsnitlig kostpris](design-details-average-cost.md)   
 [Designoplysninger: Vareudligning](design-details-item-application.md) [Administrere lageromkostninger](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
