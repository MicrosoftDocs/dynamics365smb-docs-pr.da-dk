---
title: "Angive farvede symboler for at tilpasse visuelle signaler om en køindikators aktivitet til virksomheden eller individuelle brugere | Microsoft Docs"
description: "Som administrator kan du oprette køindikatorer, der vises i rollecentre for brugere, for at medtage en indikator, der skifter farve ud fra dataværdierne i køerne."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f68bd92456ccab6d4bade8f5545d5c715a0c35bd
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-a-colored-indicator-on-cues-for-the-company-or-individual-users"></a>Oprette en farvet indikator på køindikatorer for firmaet eller individuelle brugere
Som administrator kan du oprette køindikatorer, der vises i rollecentre for brugere, for at medtage en indikator, der skifter farve ud fra dataværdierne i køerne.  
  
Indikatoren vises som en farvet streg langs den øverste kant af feltet Køindikator. Det indeholder et visuelt signal af status for køindikatorens aktivitet, som kan indikere favorable eller ikke-favorable betingelser for at bede brugeren om at handle. Hvis en køindikator f.eks. viser løbende salgsfakturaer, kan du oprette indikatoren som grøn (favorabel), når det samlede antal løbende salgsfakturaer er under 10, og rød (ikke-favorabel), når det samlede antal er større end 20.  
  
Fra vinduet **Opsætning af køindikator** kan du konfigurere indikatorer for alle køindikatorer, der findes i regnskabsdatabasen. Du kan angive indikatorerne, der skal gælde for alle brugere i virksomheden eller en individuel bruger. Indikatorindstillingerne i vinduet **Opsætning af køindikator** fungerer som standardindikatorindstillingerne. Hvis vinduet **Opsætning af køindikator for slutbruger** er gjort tilgængelig for brugere, kan de tilpasse indstillingerne for indikatorer, som du definerer i vinduet **Opsætning af køindikator**.  
  
Hvis du vil konfigurere indikatoren, kan du angive op til to tærskelværdier, der definerer tre områder af dataværdier (lav, mellem og høj), hvor du kan anvende en anden farve (eller type).  
  
### <a name="to-set-up-colored-indicators-on-cues"></a>Sådan opretter farveindikatorer på køindikatorer  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af køindikator**, og vælg derefter det relaterede link.  
  
     Vinduet **Opsætning af køindikator** vises. Vinduet viser de indikatorer, der aktuelt er konfigureret på køindikatorer. Indikatorer, der gælder for alle brugere i virksomheden, har et tomt **Brugernavn**-felt. Indikatorer, der gælder for en bestemt bruger, omfatter brugerens navn i feltet **Brugernavn**.  
  
    > [!NOTE]  
    >  Hvis du konfigurerer en indikator for hele firmaet, og en bruger ændrer indikatoren senere, vises en separat post til indikatoren på listen for den pågældende bruger.  
  
2. Vælg handlingen **Rediger liste**.  
3. Hvis du vil oprette en indikator for en køindikator, der ikke vises i vinduet, skal du vælge handlingen **Ny** og derefter udfylde felterne som beskrevet nedenstående. Hvis du vil redigere en eksisterende indikator, skal du gå til næste trin.  
  
    |  Felt  |  Beskrivelse  |    
    |---------|---------------|  
    |**Brugernavn**|Hvis du vil konfigurere indikatoren for alle brugere, skal du lade feltet være tomt.<br /><br /> Hvis du vil konfigurere indikatoren for en bestemt bruger, skal du indstille feltet til brugernavnet.|  
    |**Tabelnr.**|Angiver id for det tabelobjekt, der indeholder køindikatoren. Brug rullelisten til at finde tabellen. Rullelisten indeholder alle køindikatortabeller i firmadatabasen.<br /><br /> Feltet **Tabelnavn** udfyldes automatisk på baggrund af dine valg.|  
    |**Feltnr.**|Angiver id'et for den køindikator, hvor du vil oprette en indikator. Brug rullelisten til at finde den ønskede køindikator. **Bemærk:** Køindikator-id'et svarer til det feltnummer, der er tildelt køindikatoren i tabellen. <br /><br /> Feltet **Feltnavn** udfyldes automatisk på baggrund af dit valg|  
  
4. Hvis du vil konfigurere indikatoren for en køindikator, skal du angive felterne som beskrevet i følgende tabel.  
  
    |  Felt  |  Beskrivelse  |    
    |---------|---------------|  
    |**LowStyle**|Angiver farven på indikatoren, når køindikatorens værdi er mindre end værdien af feltet **Grænse 1**.|  
    |**LowThreshold**|Angiver den værdi, fra og med hvilken indikatoren ændres til den farve, der er angivet af feltet **Typen Mellem interval**.|  
    |**MiddleStyle**|Angiver farven på indikatoren, når køindikatorens værdi er større end eller lig med værdien af feltet **Grænse 1**, men mindre end eller lig med værdien af feltet **Grænse 2**.|  
    |**HighThreshold**|Angiver den værdi, over hvilken indikatoren ændres til den farve, der er angivet af feltet **Typen Højt interval**.|  
    |**HighStyle**|Angiver farven, der skal bruges, når køindikatorens værdi er over værdien af feltet **Grænse 2**.|  
  
     Følgende tabel viser de farver, der svarer til indstillingerne for felterne **LowStyle**, **MiddleStyle** og **HighStyle**.  
  
    |  Indstilling  |  Farve  |  
    |----------|---------|  
    |**Ingen**|Ingen farve (samme farve som feltet Køindikator)|  
    |**Favorabel**|Grøn|  
    |**Ikke-favorabel**|Rød|  
    |**Tvetydig**|Gul|  
    |**Underordnet**|Grå|  
  
## <a name="see-also"></a>Se også  
[Oprette en farvet indikator på køindikatorer i dit arbejdsområde](ui-how-setup-colored-indicator-cues.md)  
