---
title: "Sådan modtager du varer | Microsoft Docs"
description: "Når der ankommer varer til et lagersted, der er sat op til lagermodtagelse, henter du de linjer i kildedokumentet, som har udløst modtagelsen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3e6ab403945df0f3c98ab1d47eefa0633f0172e3
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="receive-items"></a>Modtage varer
Når varer ankommer til et lagersted, der ikke er konfigureret til behandling af lagermodtagelser, skal du blot registrere modtagelsen på det relaterede forretningsbilag f.eks. en købsordre, en salgsreturvareordre eller en indgående overflytningsordre.

Når der ankommer varer til et lagersted, der er sat op til lagermodtagelse, henter du de linjer i kildedokumentet, som har udløst modtagelsen. Hvis du benytter placeringer, kan du enten acceptere den standardplacering, der udfyldes, eller du kan udfylde den placering, hvor varen skal lægges på lager, hvis varen aldrig er brugt før på lagerstedet. Du skal derefter udfylde det antal af varen, du har modtaget, og bogføre modtagelsen.  

## <a name="to-receive-items-with-a-purchase-order"></a>Sådan modtages varer med en købsordre
Nedenfor kan du se, hvordan du modtager varer med en købsordre. Der er en tilsvarende fremgangsmåde for salgsreturvareordrer og overflytningsordrer.  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsordrer**, og vælg derefter det relaterede link.
2. Åbn en eksisterende købsordre eller opret en ny. Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).
3. Angiv det modtagne antal i feltet **Modtag (antal)**.

    Værdien i feltet **Modtaget antal** opdateres. Hvis det er en delvis modtagelse, er værdien lavere end værdien i feltet **Antal**.
4. Vælg handlingen **Bogfør**.

## <a name="to-receive-items-with-a-warehouse-receipt"></a>Sådan modtages varer med en lagermodtagelse
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagermodtagelser**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  

    Udfyld felterne i oversigtspanelet **Generelt**. Når du henter kildedokumentlinjer, kopieres nogle af oplysningerne fra hovedet til hver linje.  

    I forbindelse med lageropsætning med styret læg-på-lager og pluk: Hvis der på lokationen er en standardzone og -placering til modtagelser, udfyldes felterne **Zonekode** og **Placeringskode** automatisk, men du kan ændre dem efter behov.  

    > [!NOTE]  
    >  Hvis du vil modtage varer med en anden lagerklassekode end placeringens klassekode i feltet **Placeringskode** i dokumenthovedet, skal du slette indholdet i feltet **Placeringskode** i hovedet, inden du henter kildedokumentlinjerne for varerne.  
3.  Vælg handlingen **Hent kildedokumenter**. Vinduet **Kildedokumenter** åbnes.

    Fra en ny eller en åben lagermodtagelse kan du bruge vinduet **Filtre til at hente kildedok.** til at hente de frigivne kildedokumentlinjer, der definerer, hvilke varer der skal modtages eller leveres.

    1. Vælg handlingen **Brug filtre til at hente kildedok.**.  
    2. Hvis du vil oprette et nyt filter, skal du indtaste en beskrivende kode i feltet **Kode** og derefter vælge handlingen **Ret**.  
    3. Definer den type kildedokumentlinjer, som du ønsker at hente, ved at udfylde de relevante filterfelter.  
    4. Vælg handlingen **Kør**.  

    Alle frigivne kildedokumentlinjer, som opfylder filterkriterierne, indsættes nu i vinduet **Lagermodtagelse**, hvorfra du har aktiveret filterfunktionen.  

    De filterkombinationer, du definerer, gemmes i vinduet **Filtre til at hente kildedok.**, indtil næste gang du skal bruge dem. Du kan oprette et ubegrænset antal filterkombinationer. Du kan til enhver tid ændre kriterierne ved at vælge handlingen **Ret**.

4.  Vælg de kildedokumenter, som du vil modtage varer fra, og vælg derefter knappen **OK**.  

    Linjerne fra kildedokumentet vises i vinduet **Lagermodtagelse**. Feltet **Modtag (antal)** er på forhånd udfyldt med det udestående antal varer for hver linje, men du kan ændre antallet efter behov. Hvis du slettede indholdet i feltet **Placeringskode** i oversigtspanelet **Generelt**, inden du hentede linjerne, skal du udfylde alle modtagelseslinjer med den rette placeringskode.  

    > [!NOTE]  
    >  Hvis du vil udfylde feltet **Modtag (antal)** på alle linjer med nul, skal du vælge handlingen **Slet Modtag antal**. Hvis du vil udfylde det igen med det udestående antal, skal du vælge handlingen **Autoudfyld Modtag antal**.  

    > [!NOTE]  
    >  Du kan ikke modtage flere varer end antallet i feltet **Antal udestående** på kildedokumentlinjen. Hvis du vil modtage flere varer, skal du hente et andet kildedokument, der indeholder en linje for varen. Du kan bruge filterfunktionen til at hente kildedokumenter på varen.  

5.  Bogfør lagermodtagelsen. Mængdefelterne opdateres på kildedokumenterne, og varerne registreres som en del af virksomhedens varebeholdning.  

Hvis du bruger læg-på-lager, sendes modtagelseslinjerne til læg-på-lager-funktionen. Selvom varerne er modtaget, kan de ikke plukkes, før de er lagt på lager. De modtagede varer betragtes først som disponible, når der er registreret en læg-på-lager.  

Hvis du ikke bruger læg-på-lager, men placeringer, registreres varernes læg-på-lager på den placering, der er angivet på kildedokumentlinjen.  

> [!NOTE]  
>  Hvis du bruger funktionen **Bogfør og udskriv**, bogfører du både modtagelsen og udskriver en læg-på-lager-instruktion, der viser, hvor du vil lægge varerne på plads i lageret.  
>   
>  Hvis din lokation bruger styret læg-på-lager og pluk, anvendes læg-på-lager-skabelonen til at beregne den bedste placering for varerne. Dette udskrives på læg-på-lager-instruktionen.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

