---
title: Modtage varer
description: Denne artikel er en oversigt over de forskellige måder at modtage varer på et lagersted, f. eks. varer med en købsordre eller varer med en lagermodtagelse.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: 6cca8d8f9b0ec28b149532581f9bc458022c3cd5
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529510"
---
# <a name="receive-items"></a>Modtage varer

Når varer ankommer til et lagersted, der ikke er konfigureret til behandling af lagermodtagelser, skal du blot registrere modtagelsen på det relaterede forretningsbilag f.eks. en købsordre, en salgsreturvareordre eller en indgående overflytningsordre.

Når der ankommer varer til et lagersted, der er sat op til lagermodtagelse, henter du de linjer i kildedokumentet, som har udløst modtagelsen. Hvis du benytter placeringer, kan du enten acceptere den standardplacering, der udfyldes, eller du kan udfylde den placering, hvor varen skal lægges på lager, hvis varen aldrig er brugt før på lagerstedet. Du skal derefter udfylde det antal af varen, du har modtaget, og bogføre modtagelsen.  

## <a name="receive-items-with-a-purchase-order"></a>Modtage varer med en købsordre

Nedenfor kan du se, hvordan du modtager varer med en købsordre. Trinnene er tilsvarende dem for salgsreturvareordrer og overflytningsordrer.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsordrer**, og vælg derefter det relaterede link.
2. Åbn en eksisterende købsordre eller opret en ny. Flere oplysninger i [Registrere Køb](purchasing-how-record-purchases.md).
3. Angiv det modtagne antal i feltet **Modtag (antal)**.

   > [!NOTE]
   > Hvis det modtagne antal er større end det, der er bestilt på købsordren ifølge feltet **Antal**, og kreditoren må tillade overmodtagelser, skal du bruge feltet **Overmodtagelse** til at håndtere mere end det maksimale antal. Flere oplysninger i afsnittet [Sådan modtager du flere varer end det bestilte antal](warehouse-how-receive-items.md#receive-more-items-than-ordered).
4. Vælg handlingen **Bogfør**.

  Værdien i feltet **Modtaget antal** opdateres. Hvis det er en delvis modtagelse, er værdien lavere end værdien i feltet **Antal**.

> [!NOTE]
> Hvis du bruger et lagerdokument til at bogføre modtagelsen, kan du ikke bruge handlingen **Bogfør** i købsordren. I stedet har en lagermedarbejder allerede bogført antallet på købsordren som modtaget. Flere oplysninger i [Sådan modtages varer med en lagermodtagelse](warehouse-how-receive-items.md#receive-items-with-a-warehouse-receipt).

## <a name="receive-items-with-a-warehouse-receipt"></a>Modtage varer med en lagermodtagelse

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermodtagelse**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  

    Udfyld felterne i oversigtspanelet **Generelt**. Når du henter kildedokumentlinjer, kopieres nogle af oplysningerne fra hovedet til hver linje.  

    I forbindelse med lageropsætning med styret læg-på-lager og pluk: Hvis der på lokationen er en standardzone og -placering til modtagelser, udfyldes felterne **Zonekode** og **Placeringskode** automatisk, men du kan ændre dem efter behov.  

    > [!NOTE]  
    > Hvis du vil modtage varer med en anden lagerklassekode end placeringens klassekode i feltet **Placeringskode** i dokumenthovedet, skal du slette indholdet i feltet **Placeringskode** i hovedet, inden du henter kildedokumentlinjerne for varerne.  
3. Vælg handlingen **Hent kildedokumenter**. Siden **Kildedokumenter** åbnes.

    Fra en ny eller en åben lagermodtagelse kan du bruge siden **Filtre til at hente kildedok.** til at hente de frigivne kildedokumentlinjer, der definerer, hvilke varer der skal modtages eller leveres.

    1. Vælg handlingen **Brug filtre til at hente kildedok.**.  
    2. Hvis du vil oprette et nyt filter, skal du indtaste en beskrivende kode i feltet **Kode** og derefter vælge handlingen **Ret**.  
    3. Definer den type kildedokumentlinjer, som du ønsker at hente, ved at udfylde de relevante filterfelter.  
    4. Vælg **Kør**.  

    Alle frigivne kildedokumentlinjer, som opfylder filterkriterierne, indsættes nu på siden **Lagermodtagelse**, hvorfra du har aktiveret filterfunktionen. 

    De filterkombinationer, du definerer, gemmes på siden **Filtre til at hente kildedok.**, indtil næste gang du skal bruge dem. Du kan oprette et ubegrænset antal filterkombinationer. Du kan til enhver tid ændre kriterierne ved at vælge handlingen **Ret**.

4. Vælg de kildedokumenter, som du vil modtage varer fra, og vælg derefter knappen **OK**.  

    Linjerne fra kildedokumentet vises på siden **Lagermodtagelse**. Feltet **Modtag (antal)** er på forhånd udfyldt med det udestående antal varer for hver linje, men du kan ændre antallet efter behov. Hvis du slettede indholdet i feltet **Placeringskode** i oversigtspanelet **Generelt**, inden du hentede linjerne, skal du udfylde alle modtagelseslinjer med den rette placeringskode.  

    > [!NOTE]  
    >  Hvis du vil udfylde feltet **Modtag (antal)** på alle linjer med nul, skal du vælge handlingen **Slet Modtag antal**. Hvis du vil udfylde det igen med det udestående antal, skal du vælge handlingen **Autoudfyld Modtag antal**.  
    >
    >  Du kan ikke modtage flere varer end antallet i feltet **Antal udestående** på kildedokumentlinjen. Hvis du vil modtage flere varer, skal du hente et andet kildedokument, der indeholder en linje for varen ved hjælp af filterfunktionen.  

5. Bogfør lagermodtagelsen. Mængdefelterne opdateres på kildedokumenterne, og varerne registreres som en del af virksomhedens varebeholdning.  

Hvis du bruger læg-på-lager, sendes modtagelseslinjerne til læg-på-lager-funktionen. Selvom varerne er modtaget, kan de ikke plukkes, før de er lagt på lager. De modtagede varer betragtes først som disponible, når der er registreret en læg-på-lager.  

Hvis du ikke bruger læg-på-lager, men placeringer, registreres varernes læg-på-lager på den placering, der er angivet på kildedokumentlinjen.  

> [!NOTE]  
> Hvis du bruger funktionen **Bogfør og udskriv**, bogfører du både modtagelsen og udskriver en læg-på-lager-instruktion, der viser, hvor du vil lægge varerne på plads i lageret.  
>
> Hvis din lokation bruger styret læg-på-lager og pluk, anvendes læg-på-lager-skabelonen til at beregne den bedste placering for varerne. Dette udskrives på læg-på-lager-instruktionen.

## <a name="receive-more-items-than-ordered"></a>Modtage flere varer end det bestilte antal

Når du modtager flere varer, end du har bestilt, kan det være en god idé at modtage dem i stedet for at annullere modtagelsen. Det kan f.eks. være billigere at lade de overskydende varer indgå i lagerbeholdningen frem for at returnere dem, eller også kan leverandøren måske tilbyde en rabat mod, at du beholder dem.

### <a name="set-up-over-receipts"></a>Konfigurere overmodtagelser

Du skal angive en procentdel,, som gør det muligt at overskride det bestilte antal ved modtagelse. Du kan definere dette med en overmodtagelseskode, som indeholder procentdelen i feltet **Tolerance-% for overmodtagelse**. Derefter tildeler du koden til kortene for de relevante varer og/eller kreditorer.  

Følgende afsnit handler om, hvordan du opretter og tildeler en overmodtagelseskode til en vare. Trinnene er de samme for leverandør- og kontaktkort.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for en vare, som du har mistanke om kan blive leveret med et højere antal end det bestilte.
3. Klik på **Søg** i feltet **Overmodtagelseskode**.
4. Vælg handlingen **Ny**.
5. På siden **Overmodtagelseskoder** kan du oprette en eller flere nye linjer, der definerer forskellige politikker for overmodtagelse. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
6. Marker en linje, og vælg derefter **OK**.

Overmodtagelseskoden knyttes til varen. En købsordre eller lagermodtagelse for varen giver nu mulighed for at modtage mere end det bestilte antal i henhold til den angivne toleranceprocent for overlevering.

> [!NOTE]
> Du kan oprette en godkendelsesproces for at kræve, at overmodtagelser skal godkendes, før de kan behandles. Hvis det er tilfældet, skal du markere afkrydsningsfeltet **Godkendelse kræves** på siden **Overmodtagelseskoder**. Flere oplysninger i [Oprette workflows](across-how-to-create-workflows.md).

### <a name="perform-an-over-receipt"></a>Udføre en overmodtagelse

På købslinjer og lagermodtagelseslinjer bruges feltet **Overmodtagelsesantal** til at registrere overmodtagne mængder, dvs. mængder, der overstiger værdien i feltet **Antal**, det bestilte antal.

Når du håndterer en overmodtagelse, kan du enten øge værdien i feltet **Modtag (antal)** til det faktisk modtagne antal. Feltet **Overmodtagelsesantal** opdateres derefter, så det overskydende antal vises. Du kan også angive det overskydende antal i feltet **Overmodtagelsesantal**. Feltet **Modtag (antal)** opdateres derefter, så det bestilte antal plus det overskydende antal vises. Følgende fremgangsmåde beskriver, hvordan du udfylder feltet **Modtag (antal)**.  

1. På en købsordre eller et lagermodtagelsesdokument, hvor det modtagne antal er højere end det bestilte, skal du angive det faktisk modtagne antal i feltet **Modtag (antal)**.

    Hvis stigningen ligger inden for den tolerance, der er angivet i overmodtagelseskoden, opdateres feltet **Overmodtagelsesantal**, så det viser det antal, der angiver, hvilken værdi i feltet **Antal**, der overskrides.

    Hvis forøgelsen er større end den angivne tolerance, er overmodtagelse ikke tilladt. Hvis det er tilfældet, kan du undersøge, om der findes en anden overmodtagelseskode, der tillader det. Ellers er det kun det bestilte antal, der kan modtages, og overskydende antal skal håndteres på en anden måde, f.eks. ved at returnere den til leverandøren.

2. Bogfør modtagelsen ligesom enhver anden modtagelse.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] indeholder ikke funktioner til automatisk start af den økonomiske administration af overmodtagelser. Du skal håndtere dette manuelt efter aftale med leverandøren, f.eks. ved at leverandøren videresender en ny eller opdateret faktura.

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Se også

[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
