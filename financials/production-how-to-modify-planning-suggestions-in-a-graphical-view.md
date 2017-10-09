---
title: "Sådan ændres planlægningsforslag i en grafisk visning | Microsoft Docs"
description: "En typisk planlægningsaktivitet er at ændre eller tilføje planlægningskladdelinjer for at ændre de foreslåede forsyningsordrer, før du registrerer dem ved at køre funktionen **Udfør aktionsmeddelelse**. Et alternativ til at gøre dette i planlægningskladden er at bruge en grafisk visning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6cdd86fb96e89e99ea2378221d2991bd640f887e
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-modify-planning-suggestions-in-a-graphical-view"></a>Fremgangsmåde: Ændre planlægningsforslag i en grafisk visning
En typisk planlægningsaktivitet er at ændre eller tilføje planlægningskladdelinjer for at ændre de foreslåede forsyningsordrer, før du registrerer dem ved at køre funktionen **Udfør aktionsmeddelelse**. Et alternativ til at gøre dette i planlægningskladden er at bruge en grafisk visning.

I vinduet **Varedisponering pr. tidslinje** kan du ændre visse forsyningsordrer og forslag ved at trække elementer på x-aksen for at ændre antallet eller trække elementer på y-aksen for at ændre forfaldsdato.  

 I vinduerne **Varedisponering pr. tidslinje** og **Planlægningskladde** kan du foretage følgende ændringer:  

-   Redigere en foreslået forsyningsordre, der kun findes som en planlægningslinje.  
-   Redigere en eksisterende forsyningsordre, som planlægningssystemet foreslår ændret.  
-   Oprette en ny foreslået forsyningsordre og redigere den.  

Du kan finde flere oplysninger om de planlægningslinjetyper, der vises, i feltet Beskrivelse på oversigtspanelet **Begivenhedsændringer**.  

Når du vælger **Gem ændringer** i vinduet **Varedisponering pr. tidslinje** kopieres de ændringer, du har foretaget, til planlægnings- eller indkøbskladden. Du kan nu implementere dem ved hjælp af funktionen **Udfør aktionsmedl. - plan.**.  

Følgende procedure viser, hvordan du ændrer forsyningsforslag ved at trække og slippe. Som et alternativ kan du ændre feltet **Forfaldsdato** og feltet **Antal** i oversigtspanelet **Begivenhedsændringer** og straks se ændringerne grafisk i oversigtspanelet **Tidslinje** i vinduet **Planlægningskladde**.  

## <a name="to-modify-suggested-supply-orders-in-the-graphical-view"></a>Sådan ændres foreslåede forsyningsordrer i den grafiske visning  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varedisponering pr. tidslinje**, og vælg derefter det relaterede link.  

    Vinduet **Varedisponering pr. tidslinje** åbnes med varenummer, lokation og variant af varen på den valgte planlægningslinje, udfyldt på forhånd i oversigtspanelet **Indstillinger**. Oversigtspanelet **Tidslinje** viser en grafisk repræsentation af varens planlagte beholdning, herunder planlægningsforslag.  

2.  Kontrollér, at feltet **Medtag planlægningsforslag** er markeret.  
3.  Find den foreslåede forsyningsordre, du vil ændre. Du kan identificere de redigerbare elementer ved den grønne cirkel og diskikonet. Du kan finde flere oplysninger om de forskellige symboler i afsnittet "Symboler og ikoner på oversigtspanelet Tidslinje".  
4.  Placer markøren over den grønne cirkel, indtil den forstørres, og markøren ændres til Flyt figur (fire pile).  
5.  Tryk og hold museknappen nede, mens du trækker markøren op eller ned for at ændre mængden. Tryk og hold museknappen nede, mens du trækker markøren mod venstre eller højre for at ændre forfaldsdatoen.  
6.  Ud over at flytte elementer med træk og slip, kan du ændre planlægningsforslag ved hjælp af et antal rullemenufunktioner. Få adgang til rullemenuen i den grønne cirkel for et foreslået forsyningselement, og vælg én af følgende funktioner  

    |Funktion|Description|  
    |--------------|---------------------------------------|  
    |**Opret ny forsyning**|Opretter et nyt element på det punkt, hvor du går ind i rullemenuen. Punktet repræsenterer en ny foreslået forsyningsordre. Det bliver til en ny linje i planlægningskladden, når du vælger **Gem ændringer**.<br /><br /> **BEMÆRK:** Hvis felterne **Lokationsfilter** eller **Variantfilter** i oversigtspanelet **Indstillinger** er tomme eller har mere end én filterværdi, oprettes den nye forsyning og gemmes senere til planlægnings- eller indkøbskladden med følgende koder:<br /><br /> * Hvis filterfeltet er tomt, oprettes den nye levering uden en lokation eller variantkode.<br /><br /> * Hvis der er defineret mere end én filterværdi, oprettes den nye levering for den første filterværdi i henhold til sorteringsmetoden.<br /><br /> Hvis du ønsker en anden variant eller lokationskode, skal du manuelt ændre den på den nye planlægningslinje.|  
    |**Juster forsyning automatisk**|Optimerer en ny forsyning, du har oprettet i diagrammet, ved at sørge for, at den resulterer i nul lager inden næste forsyning.|  
    |**Slet forsyning**|Sletter elementet i oversigtspanelet **Tidslinje** og sletter planlægningslinjen, når du vælger **Gem ændringer**. Ikonet ændres til en disk med et rødt kryds, når forsyningen er blevet slettet.<br /><br /> **BEMÆRK:** Du kan kun slette en forsyning af aktionsmeddelelsestypen **Ny**. Når du vælger **Gem ændringer**, skal du manuelt slette den pågældende planlægningslinje i planlægnings- eller indkøbskladden.|  

7.  Vælg handlingen **Genindlæs**, hvis du vil nulstille alle ændringer, du har foretaget, efter at du sidst åbnede vinduet **Varedisponering pr. tidslinje** eller valgte **Genindlæs**.  
8. Når elementerne er placeret der, hvor du ønsker dem i diagrammet, skal du vælge **Gem ændringer** for at kopiere ændrede mængder og datoændringer til de planlægnings- eller rekvisitionslinjer, der repræsenterer de grafiske elementer.  

Hvis du vil implementere ændringerne af forsyningsplanen, skal du følge de aktionsmeddelelser, der er resultatet, fra planlægnings- eller indkøbskladde. Du kan finde flere oplysninger i Udfør aktionsmedl. - plan.

## <a name="symbols-and-icons-on-the-timeline-fasttab"></a>Symboler og ikoner på en oversigtspanelet Tidslinje
 |Symbol-ikon|Description|  
 |------------------|---------------------------------------|  
 |Sort kryds|Ordrer (både udbud og efterspørgsel).<br /><br /> -   Kan ikke ændres.<br />-   Synlig, når feltet **Vis planlagt beholdning** er markeret (orange graf).|  
 |Rød cirkel|Eksisterende forsyningsordrer, der ikke er i planlægningsforslag.<br /><br /> -   Kan ikke ændres.<br />-   Synlig, når feltet **Vis planlagt beholdning** er markeret (orange graf).|  
 |Gul stjerne|Forecastbehov.<br /><br /> -   Kan ikke ændres.<br />-   Synlig, når feltet **Forecastnavn** har en værdi.<br /><br /> Når både feltet **Vis projekterede lagerbeholdning** og feltet **Medtag planlægningsforslag** er markeret, har hver gul stjerne et sammenkædet modstykke i den modsatte graf. Illustrerer, hvordan en foreslået forsyning opfylder den prognosticeret efterspørgsel.|  
 |Grøn cirkel med et ikon formet som en disk med et rødt kryds|Foreslået forsyningsordre med aktionsmeddelelsen *Annuller*.<br /><br /> -   Kan ikke ændres.<br />-   Synlig, når feltet **Medtag planlægningsforslag** er markeret (grøn graf).|  
 |Grøn cirkel med et ikon formet som en disk med en stjerne|Foreslåede forsyningsordrer med aktionsmeddelelsen *Ny*.<br /><br /> -   Kan ændres.<br />-   Synlig, når feltet **Medtag planlægningsforslag** er markeret (grøn graf).|  
 |Grøn cirkel med et ikon formet som en disk med en eller to pile|Forslåede forsyningsordrer med aktionsmeddelelsen *Omplanlæg*, *Ret antal* eller *Omplanlæg og ret antal*<br /><br /> -   Kan ændres.<br />-   Synlig, når feltet **Medtag planlægningsforslag** er markeret (grøn graf).<br /><br /> Pilene afspejler retningen af planlægningsforslaget. For eksempel afspejler en venstre pil sammen med en opadgående pil en *Omplanlæg og ret antal*-aktionsmeddelelse, der består af en bagudrettet omplanlægning og et antalsforøgelse.|  
 ||  

Når du får adgang til rullemenuen for oversigtspanelet **Tidslinje**, vises følgende funktioner, afhængigt af dit valg  

 |Funktion|Description|  
 |--------------|---------------------------------------|  
 |**Opret ny forsyning**|Opretter et nyt element på det punkt, hvor du går ind i rullemenuen. Punktet repræsenterer en ny foreslået forsyningsordre. Det bliver til en ny linje i planlægningskladden, når du vælger **Gem ændringer** under fanen **Proces**.<br /><br /> Filterværdier, der er defineret i felterne **Lokationsfilter** eller **Variantfilter** i oversigtspanelet **Indstillinger** bliver anvendt på den nye forsyningsordre. **Bemærk**: Hvis filterfelterne er tomme eller har mere end én filterværdi, oprettes den nye forsyningsordre ved hjælp af følgende koder: <ul><li>Hvis filterfeltet er tomt, oprettes den nye levering uden en lokation eller variantkode.</li><li>Hvis der er defineret mere end én filterværdi, oprettes den nye forsyning vha. den første filterværdi i henhold til sorteringsrækkefølgen.</li></ul> Hvis du ønsker en anden variant eller lokationskode i den nye forsyningsordre, skal du manuelt ændre den på den nye planlægningslinje.|  
 |**Juster forsyning automatisk**|Optimerer en ny forsyning, du har oprettet i diagrammet, ved at sørge for, at den opretter nul lager inden næste forsyning.|  
 |**Slet forsyning**|Sletter elementet i oversigtspanelet **Tidslinje** og sletter planlægningslinjen, når du vælger **Gem ændringer** under fanen **Proces**. Ikonet ændres til en disk med et rødt kryds, når forsyningen er blevet slettet. **Bemærk:** Du kan kun slette en forsyning af aktionsmeddelelsestypen *Ny*. Når du har valgt **Gem ændringer** under fanen **Proces**, skal du manuelt slette den pågældende planlægningslinje i planlægnings- eller indkøbskladden.|  
 |**Vis bilag**|Åbner den ordre, planlægningslinje eller forecast, som elementet repræsenterer.|  
 |**Zoom ud (Ctrl ++)**|Gør skalaen på x-aksen større, så det bliver vist færre dage. **Bemærk!** Du kan også gøre dette ved at trykke på Ctrl + musens rullehjul.|  
 |**Zoom ind (Ctrl +-)**|Gør skalaen på x-aksen mindre, så det bliver vist flere dage. **Bemærk!** Du kan også gøre dette ved at trykke på Ctrl + musens rullehjul.|  
 |**Nulstil Zoom (Ctrl + 0)**|Gendanner skalaen på x-aksen til det, der blev brugt, før du zoomede.|  

Foruden de tastaturhandlinger, der blev nævnt tidligere, kan du også bruge følgende tastaturhandlinger i oversigtspanelet **Tidslinje**.  

 |Tastaturhandling|Description|  
 |---------------------|---------------------------------------|  
 |Ctrl + rul musens hjul|Ændrer skaleringen af x-aksen.|  
 |Vælg et element, og tryk derefter på Skift + pil|Flytter elementet i retning af pilestrøget.|  
 |Tab|Flytter til det næste element.|  
 |Shift+Tab|Flytter til det forrige element.|  
 |Tryk på Esc, mens du flytter et element.|Annullerer flytningen. **Bemærk:** Fungerer ikke, hvis du har sluppet museknappen.|

## <a name="see-also"></a>Se også  
[Planlægning](production-planning.md)   
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

