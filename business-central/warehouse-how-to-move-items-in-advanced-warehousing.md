---
title: 'Flytte varer i lagre, hvor der bruges styret læg-på-lager og pluk'
description: 'I denne artikel forklares det, hvordan du kan flytte varer på lokationer, der bruger styret læg-på-lager og pluk.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/23/2024
ms.custom: bap-template
ms.search.form: '7351,'
ms.service: dynamics-365-business-central
---

# <a name="move-items-in-advanced-warehouse-configurations-that-use-directed-put-away-and-pick"></a>Flytte varer i avancerede konfigurationer af lagersteder med styret læg-på-lager

Du kan flytte varer mellem placeringer uden et behov fra et kildedokument. Du kan f. eks. få brug for at gøre det som en del af følgende aktiviteter:

* Reorganiser lagerstedet.
* Flytte varer til et kontrolområde.
* Fjern varer midlertidigt fra lagerplaceringer, f.eks. fordi de skal fungere som demonstrationsvarer ved en salgspræsentation.
* Flytte ekstra varer til produktionsområder for komponenter, der er konfigureret med nogle trækmetoder.
* Flytte producerede eller monterede varer fra produktions-eller montageområdet til lagerstedet.
* Flytte varer fra masselager til placeringer, der skal plukkes.

Hvordan du flytter varer afhænger af den måde, som lagerstedet er sat op på som en lokation. Flere oplysninger i [Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md).

I lageropsætninger, hvor indstillingen til til/fra placering obligatorisk-opsætning er aktiveret, men ikke **styret pluk og læg-på-lager**, kan du registrere ikke-planlagte bevægelser på følgende sider:  

* Bevægelseskladde
* Internt lagerstedspluk
* Intern læg-på-lager
* Lageromposteringskladde

Siderne **Bevægelseskladden** , **Internt lagerpluk** og **Internt lager læg-på-lager** fungerer på samme måde. Brug siderne til at forberede lageraktiviteter for lagermedarbejdere. Differencen er i den avancerede funktionalitet, der er knyttet til hver side, og de forskellige typer lageraktiviteter, der sandsynligvis udføres af forskellige medarbejdere:

* Bevægelseskladder giver dig mulighed for at udfylde plukplaceringer med varer fra andre placeringer
* Læg-på-lager bruger læg-på-lager-skabeloner
* Ved pluk anvendes placeringsniveau og disponering

## <a name="warehouse-movement-worksheet"></a>Lagerbevægelseskladde

### <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Sådan flyttes varer med lagerbevægelseskladden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bevægelseskladde**, og vælg derefter det relaterede link.  
2. Udfyld felterne på kladdelinjerne manuelt, eller brug en af følgende fremgangsmåder for at udfylde linjerne automatisk:

    * **Hent placeringsindh.** udfylder kladdelinjerne med hele placeringsindholdet af den eller de placeringer, du angiver.
    * **Beregn genopfyldning** bruger placeringsniveauerne til at foreslå genopfyldning til placeringer med et højt niveau fra placeringer med et lavt niveau.

    > [!NOTE]  
    > Hvis varen opfylder kriterierne på listen nedenfor, vil felterne **Fra zone** og **Fra placering** være tomme. [!INCLUDE [prod_short](includes/prod_short.md)] beregner, hvorfra varerne kun kan flyttes, når du bruger handlingen **Opret bevægelse** .  
    >  
    > * Varen har en udløbsdato.  
    > * Afkrydsningsfeltet **Vælg i overensstemmelse med FEFO** på lokationskortet er markeret.  
    > * Du bruger funktionen **Beregn genopfyldning**.  

3. Vælg handlingen **Opret bevægelse** for at oprette bevægelsen. Når flytningen er færdig, kan du registrere den.  

### <a name="to-register-the-warehouse-movement"></a>Sådan registreres lagerbevægelsen

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bevægelser**, og vælg derefter det relaterede link.  
2. Åbne flytningsdokumentet, der skal registreres.  
3. På linjer af handlingstypen **Placer** skal du angive, hvor, hvilken og hvornår den pågældende vare skal flyttes ved at redigere feltet **Zonekode**, **Placeringskode**, **Håndteringsantal** eller **Forfaldsdato**.  
4. På linjer af handlingstypen **Hent** skal du i feltet **Håndteringsantal** angive en delmængde af det placeringsindhold, du vil flytte. Du kan kun redigere dette felt på linjerne **Hent**. 

    > [!NOTE]
    > Hvis det er nødvendigt at placere varerne for en enkelt linje på mere end én placering, f.eks. fordi den angivne placering er fuld, skal du bruge funktionen **Opdel linje** i oversigtspanelet **Linjer**. Handlingen opretter en linje for det resterende antal til ekspedition.
 
5. Hvis du vil flytte alle foreslåede mængder som anført i feltet **Antal**, skal du vælge handlingen **Autofyld håndteringsantal**.  
6. Vælg handlingen **Registrer**.  

> [!NOTE]  
> For lokationer, der bruger styret læg-på-lager og pluk, kan du ikke manuelt flytte varer på placeringer af typen **Modtag**, fordi de endnu ikke betragtes som disponibel lagerbeholdning. Du skal lægge varerne på plads på placeringerne, før de kan bruges til bevægelser.

## <a name="internal-pick"></a>Internt pluk

### <a name="to-create-an-internal-pick"></a>Sådan oprettes et internt pluk

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Internt lagerpluk**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.
3. Udfyld feltet **Nummer**. feltet **Lokationskode** og feltet **Til placeringskode** i oversigtspanelet **Generelt**. Feltet **Til placeringskode** angiver den placering, hvor de plukkede varer skal hentes. I forbindelse med produktion er denne placering placeringen for indgående produktion eller åben produktion. I andre forbindelser skal du vælge en placeringskode med en placeringstype, som ikke bruges til pluk, sandsynligvis en leveranceplacering eller specialplacering.  
4. Vælg en vare i feltet **Varenr.** , og indtast de antal, der skal plukkes.  
5. Vælg handlingen **Opret pluk**. Der er nu en lagerplukinstruktion klar til en lagermedarbejder. Alternativt kan du vælge handlingen **Frigiv** og oprette pluk (logistik) ved hjælp af **Plukkladde**. Du kan lære mere om plukkladder ved at gå til [Opret plukdokumenter samlet i plukkladden](warehouse-how-to-pick-items-for-warehouse-shipment.md#to-create-pick-documents-in-bulk-with-the-pick-worksheet).
6. Når plukningen er færdig, kan du registrere den.  

### <a name="to-register-the-warehouse-pick"></a>Sådan registreres lagerplukningen

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk**, og vælg derefter det relaterede link.  

    Hvis du skal arbejde med et bestemt pluk, skal du vælge plukket på listen eller filtrere oversigten for at finde de pluk, der er blevet tildelt specielt til dig.  
2. Hvis feltet **Tildelt bruger-ID** er tomt, skal du skrive dit id for at identificere dig selv, hvis det er nødvendigt.  
3. Plukke varer.  

    Da lagerstedet er sat op til at bruge styret læg-på-lager og pluk, bestemmer placeringsniveau de placeringer, der skal plukkes fra. Placeringerne foreslås på pluklinjerne. Instruktionerne indeholder mindst to separate linjer, mindst én for hver type handling, Hent og Placer.  

4. Når du har foretaget plukket og har placeret varerne på rette sted, skal du vælge handlingen **Registrer pluk**.  

## <a name="internal-put-away"></a>Intern læg-på-lager

### <a name="to-create-an-internal-put-away"></a>Sådan oprettes en intern læg-på-lager-aktivitet

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Intern læg-på-lager-aktivitet**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.
3. Udfyld feltet **Nummer**. og felterne **Lokationskode**.
4. Udfyld en linje for hver vare, der skal flyttes til lagerstedet. Felterne **Varenr.** og **Antal** skal udfyldes.

    > [!NOTE]  
    > Når du vælger feltet **Varenr.**, åbnes vinduet **Placeringsindholdsoversigt** i stedet for **Vareoversigt**. Det er fordi, du lægger en vare på plads, der skal opbevares på en særlig placering - *Placeringsindhold* - ikke bare en vare, og du ved allerede, hvilken placering varen skal tages fra. Hvis du har udfyldt feltet **Fra placeringskode**, bliver placeringsindholdet filtreret efter den værdi.

5. For at udfylde kladdelinjerne med hele placeringsindholdet eller det filtrerede placeringsindhold for placeringer på lokationen skal du vælge handlingen **Hent placeringsindhold**.  
6. Vælg handlingen **Opret læg-på-lager**. Der er nu en læg-på-lager-instruktion klar til en lagermedarbejder. Alternativt kan du vælge handlingen **Frigiv** og oprette pluk (logistik) ved hjælp af **Plukkladde**. Du kan lære mere om plukkladder ved at gå til [Opret plukdokumenter samlet i plukkladden](warehouse-how-to-put-items-away-with-warehouse-put-aways.md#to-create-put-away-documents-in-bulk-with-the-put-away-worksheet).
6. Når læg-på-lager er færdig, kan du registrere den.  

### <a name="to-register-the-warehouse-put-away"></a>Fortsæt med at registrere læg-på-lager

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **læg-på-lager**, og vælg derefter det relaterede link.
2. Åbn den læg-på-lager-aktivitet, der er klar til håndtering.  
3. Indtast eventuelt dit bruger-ID, når du begynder at arbejde på en læg-på-lager-aktivitet.  

    Hvis du vil optimere læg-på-lager-processen, kan du sortere læg-på-lager-linjerne efter forskellige kriterier. F.eks. efter vare, hyldenummer eller forfaldsdato.
   
    * Hvis Hent- og Placer-linjerne til hver modtagelseslinje ikke står umiddelbart efter hinanden, og du gerne vil have det sådan, kan du sortere linjerne ved at vælge **Vare** i feltet **Sorteringsmetode**.  
    * Hvis placeringsniveauerne afspejler det fysiske lager for lagerstedet, skal du bruge sorteringsmetoden **Placeringsniveau** til at organisere omgåelsen af placeringerne.

  > [!NOTE]  
  > Linjer sorteres i stigende rækkefølge efter valgte kriterier. Hvis du sorterer efter dokument, foretages sorteringen først efter dokumenttype baseret på optællingen af **Lageraktivitetskildedokument**. Hvis du sorterer efter levering, foretages sorteringen efter destinationstype baseret på feltet **Lagerdestinationstype**.

4. Udføre læg-på-lager-aktiviteten.

    Bemærk, at hver modtagelseslinje mindst er blevet til to linjer i instruktionen.  

    * Den første linje med **handlingstypen** **Hent** angiver, hvor varerne er placeret i modtagelsesområdet. Du kan ikke ændre felterne for zone og placering på denne linje.  
    * Den næste linje med **Placer** i feltet **Handlingstype** viser, hvor du skal placere varerne på lageret. Hvis du modtager et stort antal varer på en modtagelseslinje, skal de evt. lægges på lager på flere forskellige placeringer, så der er en Placer-linje for hver placering.  

5. Vælg handlingen **Registrer læg-på-lager**, når du har placeret alle varer på de korrekte placeringer.  

## <a name="to-register-a-movement-that-has-already-happened"></a>Sådan registreres en bevægelse, der allerede er sket

Hvis du skal registrere, at varerne allerede er blevet flyttet til andre placeringer uden læg-på-lager, pluk eller bevægelse, kan du bruge siden **Lager-Bogf. Omposteringskladde** for at registrere bevægelsen.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lageromposteringskladde**, og vælg derefter det relaterede link.  
2. Udfyld felterne **Varenr.**, **Fra zonekode**, **Fra placeringskode**, **Til zonekode** og **Til placeringskode**.  
3. Vælg handlingen **Registrer**.  

## <a name="see-also"></a>Se også

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
