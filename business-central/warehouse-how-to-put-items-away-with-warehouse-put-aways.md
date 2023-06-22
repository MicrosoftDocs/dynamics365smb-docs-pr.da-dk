---
title: Sådan lægges varer på lager med Læg-på-lager (lager)
description: Lære mere om de forskellige måder at bruge læg-på-lager-aktiviteter til at lægge modtagne varer på lager på.
author: bholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/24/2023
ms.custom: bap-template
ms.search.forms: '7352, 7333'
---
# <a name="put-items-away-with-warehouse-put-aways" />Lægge varer på lager med Læg-på-lager (logistik)

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du modtage varer og indsætte dem på en af fire måder som beskrevet i følgende tabel.

|Metode|Indgående proces|Kræv modtagelse|Kræv læg-på-lager|Sværhedsgrad (få mere at vide på [Warehouse Management-oversigt](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bogfør lagermodtagelse og læg-på-lager fra ordrelinjen|||Ingen dedikeret lageraktivitet.|  
|B|Bogfør lagermodtagelse og læg-på-lager fra et læg-på-lager-dokument||Aktiveret|Basis: Ordre for ordre.|  
|U|Bogfør lagermodtagelse og læg-på-lager fra et lagermodtagelsesdokument|Aktiveret||Basis: Konsolideret modtagelse/levering for flere ordrer.|  
|D|Bogfør modtagelse fra et lagermodtagelsesdokument, og bogfør læg-på-lager fra lagerets læg-på-lager-dokument|Aktiveret|Aktiveret|Avanceret|  

Få mere at vide i [Udgående lagerstedsflow](design-details-inbound-warehouse-flow.md).

Denne artikel henviser til metode D i tabellen og forudsætter, at der allerede er sket modtagelse. Flere oplysninger i [Montage varer](warehouse-how-receive-items.md).

Hvis lokationen kræver læg-på-lager (logistik) og lagermodtagelse, skal du bruge funktionen læg-på-lager-dokumenterne til at styre, hvordan varer lægges på lager. Når du bogfører en lagermodtagelse, opdateres kildedokumenter som f. eks. købs-, indgående overflytnings-eller salgsreturvareordrer. Det modtagne antal bogføres på varekladden, og linjerne for de modtagne varer sendes til læg-på-lager-funktionen på lagerstedet.

Afhængigt af værdien i feltet **Brug læg-på-lager-kladde** på **lokationskortet** er linjerne enten tilgængelige for læg-på-lager-kladden eller brugt til at generere læg-på-lager-dokumenter med det samme. Flere oplysninger i [Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md).  

Foruden de almindelige måder at oprette lagerets læg-på-lager, der er beskrevet i denne artikel, kan du oprette læg-på-lager fra den relaterede bogførte lagermodtagelse. Dette er nyttigt, hvis du har slettet læg-på-lager-linjer, eller hvis du bruger styret læg-på-lager og pluk og har besluttet dig til ikke at bruge læg-på-lager-kladden, fordi du kan oprette eller genoprette læg-på-lager-vejledninger fra de bogførte købsleverancelinjer.

## <a name="zone-and-bin-codes" />Zone-og placeringskoder

På lokationer, der er konfigureret til at bruge styret læg-på-lager og pluk, er følgende indstillinger forudsætninger for ovenstående fremgangsmåde:  

* Der oprettes en læg-på-lager-skabelon. Du kan finde flere oplysninger i [Konfigurere læg på lager-skabeloner](warehouse-how-to-set-up-put-away-templates.md).  
* Varens eller lagervarens vægt, rummål og andre særlige forudsætninger defineres.
* Placeringernes kapacitet, type og niveau defineres for placeringerne.  

Der tages hensyn til placeringsniveau, når mere end én placering opfylder kriterierne for læg-på-lager-skabelonen. Hvis kriterierne i læg-på-lager-skabelonen og placeringsniveauet er ens for mere end én placering, vælges placeringen med det højeste nummer.

## <a name="to-create-put-away-documents-in-bulk-with-the-put-away-worksheet" />Sådan oprettes plukdokumenter samlet med plukkladden

Du kan oprette læg-på-lager-dokumenter for flere modtagelser på én gang på siden **læg-på-lager-kladde**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Læg-på-lager-kladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Hent lagerdokumenter**. Siden **Læg-på-lager-valg** åbnes.  

    Listen indeholder alle bogførte modtagelser, der er klar til at blive lagt på lager, herunder dem, der allerede er oprettet læg-på-lager-instruktioner for. Dokumenter med læg-på-lager-linjer, der fuldt ud er blevet lagt på plads og er blevet registreret, vises ikke i oversigten.  
3. Vælg de dokumenter, du vil arbejde på. Du kan arbejde med linjer fra flere dokumenter samtidigt.  

    > [!NOTE]  
    >  Hvis du prøver at vælge et modtagelses- eller intern læg-på-lager-dokument, som der allerede er oprettet instruktioner for til samtlige linjer, får du besked fra [!INCLUDE[prod_short](includes/prod_short.md)]], hvis der ingenting er at håndtere.  

4. Udfyld feltet **Sorteringsmetode** for at sortere linjerne efter behov.  

    > [!NOTE]  
    >  Den måde, som linjerne sorteres på i kladden, overføres ikke automatisk til læg på lager-instruktionen. De samme muligheder for sortering og placeringsrangering findes dog. Du kan derfor nemt genskabe samme linjerækkefølge, når du opretter læg-på-lager-instruktionerne eller ved efterfølgende at sortere dem.

5. Udfyld feltet **Håndteringsantal**. Vælg handlingen **Autofyld håndteringsantal**, eller udfyld felterne manuelt.  
6. Du kan redigere linjerne efter behov. Du kan også slette linjer, f.eks. hvis der er varer, der skal lægges på en placering, der ligger langt fra de andre placeringer.  

    > [!NOTE]  
    > Hvis du sletter linjer, bliver de kun slettet fra kladden. De slettes ikke fra læg på lager-listen.  

7. Vælg handlingen **Opret læg-på-lager**. Siden **Opret dokument** åbnes, og her kan du tilføje flere oplysninger om den læg-på-lager-aktivitet, du opretter:  

    * Du kan tildele læg-på-lager-aktiviteten til en bestemt medarbejder.  
    * Du kan sortere læg-på-lager-instruktionslinjerne på samme måde som i kladden eller efter placeringsniveau. Når du sorterer efter placeringsniveau, vises *Hent*-linjerne først, fordi de fleste modtagelses placeringer har et placeringsniveau på 0. Der står sidst på *Placer*-linjerne, som starter med placeringerne med det laveste placeringsniveau. Hvis lagerstedet er struktureret, så placeringer med omtrent samme placeringsniveau står ved siden af hinanden, vil en sådan sorteringsmetode spare tid for lagermedarbejderne.  
    * Du kan vælge ikke at få vist de midlertidige linjer, som [!INCLUDE[prod_short](includes/prod_short.md)]] opretter, når programmet opdeler en stor måleenhed i mindre enheder ved at markere feltet **Angiv nedbrydningsfilter**. Du kan finde flere oplysninger i [Aktivere automatisk nedbrydning med styret læg-på-lager og pluk](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    * Du kan vælge, at feltet **Håndteringsantal** ikke skal udfyldes automatisk på læg-på-lager-instruktionerne.  
    * Du kan vælge at få udskrevet dokumentet med det samme.  

8. Vælg handlingen **OK** for at oprette læg-på-lager.  

## <a name="to-create-a-put-away-from-a-posted-receipt" />Sådan oprettes en læg-på-lager-aktivitet fra en bogført modtagelse

Hvis din lokation bruger både læg-på-lager-behandling og modtagelsesbehandling, og du har slettet læg-på-lager-linjer, eller hvis du bruger styret læg-på-lager og pluk og har besluttet dig til ikke at bruge læg-på-lager-kladden, kan du oprette eller genoprette læg-på-lager-vejledninger til bogførte købsleverancelinjer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte kvitteringer**, og vælg derefter det relaterede link.  
2. Vælg bogført modtagelse til læg-på-lager.  
3. Vælg handlingen **Kort**.  

    Hvis feltet **Bilagsstatus** er tomt, er modtagelsen ikke lagt på lager overhovedet. Ellers står der i feltet, at modtagelsen er delvist eller fuldt lagt på lager.  

4. Vælg handlingen **Opret læg-på-lager**, hvis modtagelsen er lagt delvist på lager eller slet ikke er lagt på lager.  
5. Udfyld felterne efter behov, og vælg derefter knappen **OK**.  

## <a name="to-put-items-away" />Sætte varer på plads

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Læg-på-lager**, og vælg derefter det relaterede link.

2. Åbn den læg-på-lager-aktivitet, der er klar til håndtering.  
3. Indtast eventuelt dit bruger-ID, når du begynder at arbejde på en læg-på-lager-aktivitet.  

    Du kan sortere på læg-på-lager-linjerne ud fra forskellige kriterier, f.eks. efter vare, placeringsnummer eller forfaldsdato. Sortering kan hjælpe med at optimere læg-på-lager-processen, f. eks.:

    * Hvis Hent- og Placer-linjerne til hver modtagelseslinje ikke står umiddelbart efter hinanden, og du gerne vil have det sådan, kan du sortere linjerne ved at vælge **Vare** i feltet **Sorteringsmetode**.  
    * Hvis placeringsniveauerne afspejler det fysiske lager for lagerstedet, skal du bruge sorteringsmetoden **Placeringsniveau** til at organisere omgåelsen af placeringerne.

4. Udføre handlingerne.

    Hvis der skal angives en placeringskode for lokationerne, bliver hver modtagelseslinje mindst to linjer i læg-på-lager-aktiviteten.  

    * Den første linje med **handlingstypen** **Hent** angiver, hvor varerne er placeret i modtagelsesområdet. Du kan ikke ændre felterne for zone og placering på denne linje.  
    * Den næste linje med **Placer** i feltet **Handlingstype** viser, hvor du skal placere varerne på lageret. Hvis du modtager et stort antal varer på en modtagelseslinje, skal de evt. lægges på lager på flere forskellige placeringer, så der er en Placer-linje for hver placering. 

    > [!NOTE]
    > Hvis det er nødvendigt at placere varerne for en enkelt linje på mere end én placering, f.eks. fordi den angivne placering er fuld, skal du bruge funktionen **Opdel linje** i oversigtspanelet **Linjer**. Handlingen opretter en linje for det resterende antal til ekspedition.

5. Vælg handlingen **Registrer læg-på-lager**, når du har placeret alle varer på de korrekte placeringer.  

## <a name="see-related-microsoft-trainingtrainingmodulesreceive-put-away-items" />Se relateret [Microsoft-træning](/training/modules/receive-put-away-items/)

## <a name="see-also" />Se også

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
