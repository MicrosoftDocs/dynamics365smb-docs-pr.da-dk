---
title: Modtagelse og placering på lager i avanceret logistik | Microsoft Docs
description: I Business Central kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2020
ms.author: edupont
ms.openlocfilehash: 9a54bcb1131e2b5df0fd98ece66701c9f601ce41
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786742"
---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a>Gennemgang: Modtagelse og placering på lager i avancerede lageropsætninger

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.  

|Metode|Indgående proces|Placering|Modtagelser|Læg-på-lager-aktiviteter|Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|T|Bogfør lagermodtagelse og læg-på-lager fra ordrelinjen|X|||2|  
|B|Bogfør lagermodtagelse og læg-på-lager fra et læg-på-lager-dokument|||X|3|  
|L|Bogfør lagermodtagelse og læg-på-lager fra et lagermodtagelsesdokument||X||5-4-6|  
|D|Bogfør modtagelse fra et lagermodtagelsesdokument, og bogfør læg-på-lager fra lagerets læg-på-lager-dokument||X|X|5-4-6|  

Du kan finde flere oplysninger i [Designoplysninger: Indgående lagerflow](design-details-inbound-warehouse-flow.md)  

Den følgende gennemgang viser metode D i forrige tabel.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
I avancerede lageropsætninger, hvor din lokation er opsat til at kræve modtagende behandling udover læg-på-lager-behandling, skal du bruge siden **Lagermodtagelse** til at registrere og bogføre modtagelsen af varer på flere indgående ordrer. Når lagermodtagelsen bogføres, oprettes der et eller flere læg-på-lager-dokumenter for at instruere lagermedarbejderne om at tage de modtagne varer og placere dem på de tildelte steder i henhold til placeringskonfiguration eller på andre placeringer. Den specifikke placering af varer registreres, når læg-på-lager-aktiviteten er registreret. Det indgående kildedokument kan være en købsordre, en salgsreturvareordre, en indgående overflytningsordre eller en montage- eller produktionsordre med afgang, der er klar til at blive lagt på lager. Hvis leverancen oprettes fra en indgående ordre, kan mere end ét indgående kildedokument være hentet til leverancen. Ved hjælp af denne metode kan du registrere mange varer, der ankommer fra forskellige indgående ordrer med én leverance.  

Denne gennemgang viser følgende opgaver.  

-   Oprettelse af lokationen HVID til modtagelse og læg-på-lager.  
-   Oprettelse og frigivelse af to købsordrer til komplet lagerekspedition.  
-   Oprettelse og bogføring af et lagermodtagelsesdokument for flere købsordrelinjer fra bestemte kreditorer.  
-   Registrering af en læg-på-lager-aktivitet for de modtagne varer.  

## <a name="roles"></a>Roller  
Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:  

-   Lagerchef  
-   Indkøbsagent  
-   Modtagermedarbejdere  
-   Lagermedarbejder  

## <a name="prerequisites"></a>Forudsætninger  
For at gennemføre denne gennemgang skal du:  

-   CRONUS Danmark A/S være installeret.  
-   Sådan opretter du dig selv som en lagermedarbejder på lokationen HVID ved at følge disse trin:  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
2.  Vælg feltet **Bruger-id**, og vælg din egen brugerkonto på siden **Brugere**.  
3.  Angiv HVID i feltet **Lokationskode**.  
4.  Markér feltet **Standard**.  

## <a name="story"></a>Historie  
Ellen, som er indkøbschef hos CRONUS Danmark A/S, opretter to købsordrer for tilbehørsvarer fra kreditorerne 10000 og 20000, som skal leveres til lagerstedet HVID. Når leveringerne ankommer til lagerstedet, bruger Sammy, der er ansvarlig for modtagelse af varer fra kreditorerne 10000 og 20000, et filter til at oprette modtagelseslinjer til købsordrer, der ankommer fra de to kreditorer. Sammy bogfører varerne som modtaget på lageret i en lagermodtagelse, og varerne bliver tilgængelige til salg eller andre behov. John, lagermedarbejder, tager varerne fra den modtagende placering og lægger dem på lager. Han lægger alle enheder på deres standardplaceringer, undtagen 40 ud af 100 modtagne hængsler, som han lægger på lager i montageafdelingen ved at opdele læg-på-lager-linjen. Når John registrerer læg-på-lager, opdateres placeringsindholdet, varerne er gøres tilgængelige til pluk fra lagerstedet.  

## <a name="reviewing-the-white-location-setup"></a>Gennemse lokationsopsætningen for HVID  
Opsætningen af siden **Lokationskort** definerer flows i virksomheden.  

### <a name="to-review-the-location-setup"></a>Sådan gennemgås lokationsopsætningen  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lokationer**, og vælg dernæst det relaterede link.  
2.  Åbn lokationskortet HVID.  
3.  Bemærk, at i oversigtspanelet **Lagersted** er afkrydsningsfeltet **Styret læg-på-lager og pluk** markeret.  

    Dette betyder, at lokationen er konfigureret for det højeste kompleksitetsniveau, og afspejles af det faktum, at alle afkrydsningsfelter i forbindelse med lagerekspedition på oversigtspanelet er markeret.  

4.  Bemærk, at i oversigtspanelet under **Placeringer** er placeringer angivet i felterne **Modt.placeringskode** og **Lev.placeringskode**.  

Dette betyder, at når du opretter en lagermodtagelse, kopieres denne placeringskode automatisk til sidehovedet på lagermodtagelsesdokumentet og til linjerne på de resulterende læg-på-lager-dokumenter.  

## <a name="creating-the-purchase-orders"></a>Oprettelse af købsordrer  
Købsordrer er den mest almindelige type indgående kildedokument.  

### <a name="to-create-the-purchase-orders"></a>Sådan oprettes købsordrerne  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsordre**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Opret en købsordre for kreditor 10000 på arbejdsdatoen (23. januar) med følgende købsordrelinjer.  

    |Vare|Lokationskode|Antal|  
    |----------|-------------------|--------------|  
    |70200|HVID|100 STK.|  
    |70201|HVID|50 STK.|  

    Fortsæt ved at meddele lageret, at købsordren er klar til lagerekspedition, når leverancen ankommer.  

4.  Vælg handlingen **Frigivelse**.  

    Fortsæt med at oprette den næste købsordre.  

5.  Vælg handlingen **Ny**.  
6.  Opret en købsordre for kreditor 20000 på arbejdsdatoen med følgende købsordrelinjer.  

    |Vare|Lokationskode|Antal|  
    |----------|-------------------|--------------|  
    |70100|HVID|10 DÅSER|  
    |70101|HVID|12 DÅSER|  

    Vælg handlingen **Frigivelse**.  

    Leveringerne af varer fra kreditor 10000 og 20000 er ankommet på lagerstedet HVID, og Sammy begynder at behandle købsleverancerne.  

## <a name="receiving-the-items"></a>Modtagelse af varerne  
På siden **Lagermodtagelse** kan du administrere flere indgående ordrer til kildedokumenter, f.eks. en købsordre.  

### <a name="to-receive-the-items"></a>Sådan modtages varerne  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagermodtagelse**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Angiv HVID i feltet **Lokationskode**.  
4.  Vælg handlingen **Brug filtre til at hente kildedok.**.  
5.  Skriv **Tilbehør** i feltet **Kode**.  
6.  I feltet **Beskrivelse** skal du indtaste **Kreditorer 10000 og 20000**.  
7.  Vælg handlingen **Ret**.  
8.  I oversigtspanelet **Køb** i skal du i feltet **Leverandørnummerfilter** angive **10000&#124;20000**.  
9. Vælg handlingen **Kør**. Lagermodtagelsen udfyldes med fire linjer, der repræsenterer købsordrelinjer for de angivne kreditorer. Feltet **Modtag (antal)** udfyldes, fordi du ikke markerede afkrydsningsfeltet **Undlad at udfylde håndteringsantal** på siden **Filtre til at hente kildedok.**.  
10. Hvis du vil bruge et filter, som beskrevet tidligere i dette afsnit, skal du vælge handlingen **Hent kildedokument** og derefter vælge købsordrer fra de pågældende kreditorer.  
11. Vælg handlingen **Bogfør modtagelse**, og vælg derefter knappen **Ja**.  

    Positive vareposter oprettes, som afspejler de bogførte købsleverancer for tilbehør fra kreditorerne 10000 og 20000, og varerne er klar til at blive lagt på lager fra den modtagende placering.  

## <a name="putting-the-items-away"></a>Lægge varerne på lager  
På siden **Læg-på-lager (logistik)** kan du administrere læg-på-lager-aktiviteter for et bestemt lagermodtagelsesdokument, der dækker flere kildedokumenter. Ligesom alle lageraktivitetsdokumenter, er hver vare på læg-på-lager repræsenteret af en Hent-linje og en Placer-linje. I følgende procedure er placeringskoden på Hent-linjerne standardmodtagelsesplaceringen for lokationen HVID, W-08-0001.  

### <a name="to-put-the-items-away"></a>Sådan lægges varerne på lager  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Læg-på-lager-aktiviteter**, og vælg derefter det relaterede link.  
2.  Vælg det eneste læg-på-lager-dokument i oversigten, og vælg derefter handlingen **Rediger**.  

    Lagerets læg-på-lager-dokument åbnes med i alt otte Hent eller Placer-linjer til de fire købsordrelinjer.

    Lagermedarbejderen får at vide, at der skal bruges 40 hængsler i montageafdelingen, og han fortsætter med at opdele den enkelte Placer-linje for at angive en anden linje for placering W-02-0001 i montageafdelingen, hvor han placerer den del af de modtagne hængsler.  

3.  Vælg den anden linje på siden **Læg-på-lager (logistik)**, Placer-linjen for vare 70200.  
4.  I feltet **Håndteringsantal** skal du rette værdien fra 100 til 60.  
5.  På oversigtspanelet **Linjer** skal du vælge **Funktioner** og derefter **Opdel linje**. En ny linje indsættes for emne 70200 med 40 i feltet **Håndteringsantal**.  
6.  Skriv W-02-0001 i feltet **Placeringskode**. Feltet **Zonekode** udfyldes automatisk.  

    Fortsæt med at registrere læg-på-lager.  

7.  Vælg handlingen **Registrer læg-på-lager**, og vælg derefter knappen **Ja**.  

    Det modtagne tilbehør lægges nu væk på varernes standardplaceringer, og der placeres 40 hængsler i montageafdelingen. De modtagne varer er nu tilgængelige til pluk til interne behov, f.eks. montageordrer, eller til eksterne behov, f.eks. salgsleverancer.  

## <a name="see-also"></a>Se også  
 [Lægge varer på lager med Læg-på-lager (logistik)](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Flytte varer i avancerede lageropsætninger](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Designoplysninger: Indgående lagerflow](design-details-inbound-warehouse-flow.md)   
 [Gennemgang: Modtagelse og placering på lager i grundlæggende lageropsætninger](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)   
 [Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)
