---
title: Anskaffe anlægsaktiver
description: 'Du kan oprette et anlægsaktiv, tildele en afskrivningsprofil og registrere anlægsaktivets anskaffelsespris.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Anskaffe anlægsaktiver

Brug siden **Anlægskort** til at angive oplysninger om et anlægsaktiv. Du kan angive bygninger eller produktionsudstyr som et hovedanlæg med en komponentliste, og du kan gruppere dem på forskellige måder, f.eks efter art, afdeling eller lokation. Du skal oprette og tilknytte en afskrivningsprofil til hvert enkelt anlægsaktiv, før du kan erhverve det.

Når du har oprettet et anlægsaktiv og tilknyttet en afskrivningsprofil, skal du anskaffe anlægget. For at få et anlægsaktiv skal du registrere dens anskaffelsespris i den relevante finanskonto, bankkonto eller leverandør ved at bogføre en anskaffelsestransaktion fra siden **Anlægskassekladde**. Du kan bruge siden **Bistået anskaffelse af anlægsaktiv** til at oprette og bogføre de nødvendige finanskladdelinjer automatisk.

Indeksering bruges til at justere for ændringer af det generelle prisniveau.  **Bruge kørslen Indekser anlæg** til at beregne anskaffelser og udskiftningsomkostninger.

## Føje et anlægsaktiv til listen over anlægsaktiver

Før du kan anskaffe et anlægsaktiv, skal du føje det til oversigten over anlægsaktiver. Du kan føje anlægsaktiver til listen på flere måder:

* Angiv oplysninger om anlægsaktiverne **på siden Anlægskort** .
* Brug handlingen **Rediger i Excel** til at hente listen over aktiver til et regneark, føje nye aktiver til listen og derefter publicere opdateringen til [!INCLUDE [prod_short](includes/prod_short.md)].
* Bruge en købsordre til at tilføje aktiver.
* Brug handlingen **Kopiér anlæg** .

Når du har føjet anlægsaktiver til listen, er næste trin at anskaffe dem, så du kan bruge dem i transaktioner. Få mere at vide under [Erhverve et anlægsaktiv](#acquire-fixed-assets).

### Tilføje et anlægsaktiv på siden Anlægskort

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** handling, og udfyld felterne på oversigtspanelet **Generelt** efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I oversigtspanelet **Afskrivningsprofil** skal du udfylde felterne efter behov. I dette trin tildeles en afskrivningsprofil til anlægsaktivet.  
4. Hvis du vil tildele mere end én afskrivningsprofil til anlægsaktivet, skal du vælge handlingen **Tilføj flere afskrivningsprofiler**. Du kan få mere at vide ved at gå til [Sådan knyttes en afskrivningsprofil til et anlægsaktiv](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Når du har udfyldt de obligatoriske felter, vises ikonet **Du er klar til at anskaffe anlægsaktivet.** Meddelelsen vises øverst på siden. Hvis du er klar til at erhverve aktivet nu, skal du vælge handlingen **Ansk** . Følg trinnene på **siden Assisteret anskaffelse af anlægsaktiver** for at fuldføre anskaffelsen. Hvis du ikke er klar, kan du altid erhverve aktivet senere.

### Brug Rediger i Excel til at tilføje aktiver

Hvis du vil tilføje adskillige anlægsaktiver, er Rediger i Excel et fantastisk værktøj at bruge. Værktøjet henter den aktuelle liste over aktiver i en kladde, der indeholder de fleste af de felter, der er tilgængelige på siden Anlægskort. Du kan udfylde nogle eller alle felterne på en række for hvert aktiv og publicere dine ændringer, så du kan føje dem til din liste [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du ikke kan udfylde alle obligatoriske felter, er det ok. Du kan opdatere dem [!INCLUDE [prod_short](includes/prod_short.md)] , når du er klar.

> [!NOTE]
> Hvis du vil bruge handlingen Rediger i Excel, skal Office-tilføjelsesprogrammet være Microsoft Dynamics installeret. Tilføjelsesprogrammet opretter forbindelsen mellem Excel og [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan få mere at vide ved at gå til [Hent Business Central-tilføjelsesprogrammet til Excel](admin-deploy-excel-addin.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg ikonet :::image type="content" source="media/share-icon.png" alt-text="Del denne side med andre brugere eller apps."::: , og vælg **derefter Rediger i Excel**.
3. Åbn den hentede fil, og skriv oplysninger om de nye anlægsaktiver.

   > [!TIP]
   > Du behøver ikke at angive et id i feltet **Nej.** . Når du udgiver opdateringen, tildeles der et id baseret på den nummerserie, [!INCLUDE [prod_short](includes/prod_short.md)]  du bruger til anlægsaktiver.

4. Hvis du vil opdatere [!INCLUDE [prod_short](includes/prod_short.md)], skal du vælge **Microsoft Dynamics** Udgiv **i ruden**.

### Tilføje et anlægsaktiv fra en købsordre eller faktura

I følgende procedure beskrives, hvordan du tilføjer et anlægsaktiv fra en købsordre. Fremgangsmåden er den samme for en købsfaktura.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.
2. Vælg **Ny** for at oprette en ny købsordre.
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]
4.  **I oversigtspanelet Linjer** i feltet **Type** skal du vælge **Anlæg**.
5. I feltet **Nummer** Vælge et eksisterende anlægsaktiv for at tilføje en udgift eller vælge **Ny** for at tilføje et nyt aktiv.
6. Når du har angivet oplysningerne for det nye aktiv og købsordren, skal du vælge **Bogfør**.

## Anskaffe et anlægsaktiv ved hjælp af en anlægskassekladde

Følgende fremgangsmåde beskriver, hvordan du anskaffer ved at oprette og bogføre de nødvendige anlægskassekladdelinjer. Du kan også oprette og bogføre linjerne manuelt. Du kan få mere at vide ved at gå til [Anskaffe et anlægsaktiv ved hjælp af en anlægskassekladde](#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
1. Vælg det aktiv, du vil anskaffe, og vælg derefter handlingen **Ansk** .
1. Følg trinnene på **siden Assisteret anskaffelse af anlægsaktiver** for at fuldføre anskaffelsen.

> [!NOTE]  
> Du kan også bogføre anskaffelsespriser som kreditposter. I så fald skal du huske, at værdien i feltet **Anskaffelsespris inkl. moms** skal have et minustegn for at angive en kredit.

Når du vælger **Udfør**, udfyldes feltet **Bogført værdi** på **siden Anlægskort**, hvilket angiver, at anlægsaktivet er anskaffet til den angivne anskaffelsespris.  

## Sådan bogføres en anskaffelse manuelt med en anlægskassekladde

Følgende fremgangsmåde bruges til at anskaffe et anlægsaktiv manuelt ved at oprette og bogføre linjerne på siden **Anlægsfinanskladde**. Du kan også erhverve et anlægsaktiv automatisk på siden **Anlægskort** ved at vælge handlingen Anskaf **anlæg** . Du kan få mere at vide ved at gå til [Erhverve et anlægsaktiv](#acquire-fixed-assets).

> [!NOTE]  
> Du kan også bogføre anskaffelsespriser som kreditposter. I så fald skal du huske, at værdien i feltet **Beløb** skal have et minustegn for at angive en kredit.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskasseklader**, og vælg derefter det relaterede link.
2. På siden **Anlægskassekladde** i feltet **Anlægsbogføringstype** skal du vælge **Anskaffelsespris**.
3. Udfyld de resterende felter efter behov.
4. Vælg handlingen **Bogfør**.  

> [!TIP]  
> Hvis du udfylder feltet **Forsikringsnr.**  [!INCLUDE[prod_short](includes/prod_short.md)] Desuden bogføres anskaffelsesprisen for anlægsaktivet på forsikringsposterne. Du kan få mere at vide ved at gå til [Forsikre](fa-how-insure.md) anlæg.

## Sådan konfigureres en komponentliste for et hovedanlæg

Du kan gruppere anlægsaktiverne i hovedanlæg og de tilhørende komponenter. Du kan f.eks. have en produktionsmaskine, der består af flere dele, som du vil gruppere på denne måde.  

Du skal oprette hovedanlægget og alle dets komponenter som individuelle anlægsaktiver. Når du har oprettet en komponentliste, [!INCLUDE[prod_short](includes/prod_short.md)]  udfyldes felterne **Hovedanlæg/Del**  **og Del af hovedanlæg** på anlægsaktiverne automatisk.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, der er hovedanlægget, og vælg derefter handlingen **Hovedanlæg**.
3. På siden **Hovedanlæg** skal du vælge feltet **Anlægsnr**. og derefter vælge de anlægsaktiver, der skal tilføjes som en komponent i hovedanlægget.
4. Luk siden.
5. Gentag trin 3 til 4 for hver underdel til anlægget, du vil tilføje.
6. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsopsætning**, og vælg derefter det relaterede link.
7. Aktivér til/fra-knappen **Tillad bogføring af hovedanlæg** .

## Sådan annulleres bogføringen af en anskaffelsespris for et anlægsaktiv

Hvis du laver en fejl under bogføring af en anskaffelsespris, kan du fjerne posten vha. kørslen **Annuller anlægsposter** og derefter bogføre den korrekte anskaffelsespost. De forkerte poster overføres til siden **Anlægsfejlposter**.

Hvis du f.eks, bogfører en anskaffelse med den forkerte dato, skal du rette den snarest muligt, fordi bogføringsdatoen for anlægsaktivet bruges i mange vigtige beregninger.

> [!IMPORTANT]  
> Du kan ikke bruge handlingen **Tilbagefør transaktion** til anlægsposter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Anlægsfinansposter**, og vælg derefter det relaterede link.  
2. Vælg den eller de poster, du vil annullere, på siden **Anlægsfinansposter**.  
3. Vælg menuen **Handlinger**, og vælg derefter handlingen **Annuller poster**.
4. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Vælg **OK** for at eksekvere kørslen.
6. Når den eller de forkerte poster annulleres, kan du fortsætte med at bogføre den korrekte anskaffelsespris.

## Sådan bogføres skrapværdien sammen med anskaffelsesprisen

Skrapværdien er restværdien af et anlæg, der ikke længere kan bruges. Du kan bogføre skrapværdien samtidigt med, at du bogfører anskaffelsesprisen. Du kan få mere at vide ved at gå til [Afskriv eller afskriv på anlæg](fa-how-depreciate-amortize.md).

Du kan bogføre skrapværdien sammen med anskaffelsesprisen fra en anlægskladde.

> [!NOTE]
> Denne proces kan kræve, at du tilpasser siden Anlægsaktivkladder ved at tilføje feltet Skrapværdi. Feltet vises ikke som standard på siden. Du kan få mere at vide ved at gå til [Tilpas dit arbejdsområde](ui-personalization-user.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskassekladder**, og vælg derefter det relaterede link.
2. Opret anskaffelseslinjen på siden **Anlægskladde**. Du kan få mere at vide ved at gå til [Sådan bogføres en anskaffelse manuelt med en anlægskassekladde](#to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal).
3. Angiv beløbet for skrapværdien som en kreditpost (med et minustegn, f.eks. **-** 100) i feltet **Skrapværdi** på kladdelinjen.
4. Vælg handlingen **Bogfør**.

> [!NOTE]
> Hvis der findes en skrapværdi for et anlægsaktiv, bruges denne værdi i afskrivningsbogføringen i stedet for værdien i feltet **Slutbogført værdi** på siden **Anlægsafskrivningsprofiler** . Du kan få mere at vide ved at gå til [Sådan administreres den slutbogførte værdi](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## Se også

[Anlægsaktiver](fa-manage.md)  
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Designdetaljer om ikke-fradragsberettiget momspåvirkning på anlægsaktiver](design-details-nondeductible-vat.md)  
[Finans](finance.md)  
[Blive køreklar til at foretage handler](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
