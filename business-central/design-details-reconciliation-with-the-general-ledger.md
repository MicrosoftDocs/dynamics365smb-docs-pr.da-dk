---
title: Designoplysninger – Afstemning med Finans | Microsoft Docs
description: 'Dette emne beskriver afstemning med Finans, når du bogfører lagertransaktioner, f.eks. salgsleverancer, produktionsoutput eller nedreguleringer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, reconciliation, general ledger, inventory'
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-reconciliation-with-the-general-ledger"></a>Designoplysninger: Afstemning med Finans
Når du bogfører lagertransaktioner, f.eks. salgsleverancer, produktionsafgang eller nedreguleringer, registreres ændringen i antal og værdi for lageret i vareposterne og værdiposterne. Det næste trin i processen er at bogføre lagerværdierne på lagerkontiene i finansregnskabet.  

Der er to måder, hvorpå du kan afstemme lageret med finans:  

* Manuelt ved at køre kørslen **Bogfør lagerregulering**.  
* Automatisk, hver gang du bogfører en lagertransaktion.  

## <a name="post-inventory-cost-to-gl-batch-job"></a>Kørslen Bogfør lagerregulering
Når du udfører kørslen **Bogfør lagerregulering**, oprettes der finansposter på basis af værdiposter. Du har mulighed for at opsummere finansposterne for hver værdipost eller oprette finansposter for hver kombination af bogføringsdato, lokationskode, varebogføringsgruppe, virksomhedsbogføringsgruppe og produktbogføringsgruppe.  

Bogføringsdatoerne i Finans er indstillet til bogføringsdatoen for den tilsvarende værdipost, bortset fra når værdiposten ligger i en lukket regnskabsperiode. I så fald bliver værdiposten sprunget over, og du skal ændre enten finansopsætningen eller brugeropsætningen for at aktivere bogføring i datointervallet.  

Når du udfører kørslen **Bogfør lagerregulering**, kan der opstå fejl som følge af manglende opsætning eller inkompatibel opsætning af dimensioner. Hvis kørslen finder fejl i opsætningen af dimensioner, bliver disse fejl tilsidesat, og kørslen bruger dimensionerne for værdiposten. For andre typer fejl bogfører kørslen ikke værdiposterne, og der vises en oversigt over disse i slutningen af rapporten under overskriften **Poster, der er sprunget over**. Du skal rette fejlene, inden du kan bogføre disse poster. Hvis du vil se en liste over fejl før kørslen af bogføringen, kan du køre rapporten **Bogfør lagerregulering** – kontrol. Denne rapport viser alle de fejl, der er stødt på under en bogføringstest. Du kan rette fejlene og derefter udføre kørslen til bogføring af lagerreguleringer uden at springe nogen poster over.  

## <a name="automatic-cost-posting"></a>Aut. lagerværdibogføring
Hvis du vil opsætte kostbogføring i Finans til at køre automatisk, når du bogfører en lagertransaktion, skal du markere afkrydsningsfeltet **Aut. lagerværdibogføring** på siden **Opsætning af Lager**. Bogføringsdatoen for Finans er den samme som bogføringsdatoen for vareposten.  

## <a name="account-types"></a>Kontotyper
Under afstemningen bogføres lagerværdier til lagerkontoen i balancen. Det samme beløb, men med omvendt fortegn, bogføres på den relevante modkonto. Modkonto er som regel en konto til resultatopgørelse. Når du bogfører direkte omkostninger, der er relateret til forbrug eller afgang,er modkontoen dog en balancekonto. Typen af vareposten og værdiposten bestemmer, hvilken finanskonto der skal bogføres til.  

Posttypen angiver, hvilken finanskonto der bogføres til. Dette bestemmes enten af antalstegnet på vareposten eller af det værdiansatte antal på værdiposten, da antallene altid har de samme tegn. En salgspost med et positivt antal beskriver f.eks. en lagerreducering, der er forårsaget af et salg, og en salgspost med et negativt antal beskriver en lagerforøgelse, der er forårsaget af en salgsreturvare.  

### <a name="example"></a>Eksempel
Følgende eksempel viser en cykelkæde, der er fremstillet af købte links. Dette eksempel viser, hvordan de forskellige finanskontotyper bruges i et typisk scenarie.  

Afkrydsningsfeltet **Bogf. af forventet kostpris** på siden **Opsætning af lager** er markeret, og følgende opsætning er defineret.  

Følgende tabel viser, hvordan linket er angivet på varekortet.  

|Angive indstillinger for felt|Værdi|  
|-----------------|-----------|  
|**Kostmetode**|Standard|  
|**Kostpris (standard)**|RV 1,00|  
|**IPO-bidrag**|RV 0,02|  

Følgende tabel viser, hvordan kæden er angivet på varekortet.  

|Angive indstillinger for felt|Værdi|  
|-----------------|-----------|  
|**Kostmetode**|Standard|  
|**Kostpris (standard)**|RV 150,00|  
|**IPO-bidrag**|RV 25,00|  

Følgende tabel viser, hvordan arbejdscenteret er angivet på arbejdscenterkortet.  

|Angive indstillinger for felt|Værdi|  
|-----------------|-----------|  
|**Købspris**|RV 2,00|  
|**Indirekte omkostningsprocent**|10|  

##### <a name="scenario"></a>Scenarie
1. Brugeren køber 150 led og bogfører indkøbsordren som modtaget. (Køb)  
2. Brugeren bogfører indkøbsordren som faktureret. Dette opretter et indirekte kostbeløb på RV 3,00, der skal allokeres, og et afvigelsesbeløb på RV 18,00. (Køb)  

    1. Mellemregningskonti ryddes. (Køb)  
    2. Den direkte omkostning bogføres. (Køb)  
    3. De indirekte omkostninger beregnes og bogføres. (Køb)  
    4. Købsafvigelsen beregnes og bogføres (kun for varer med standardkostpriser). (Køb)  
3. Brugeren sælger en kæde og bogfører salgsordren som leveret. (Salg)  
4. Brugeren bogfører salgsordren som faktureret. (Salg)  

    1. Mellemregningskonti ryddes. (Salg)  
    2. Kostpris for solgte varer bogføres. (Salg)  

        ![Resultaterne af bogføring af salg på finanskonti.](media/design_details_inventory_costing_3_gl_posting_sales.png "Resultaterne af bogføring af salg på finanskonti")  
5. Brugeren bogfører forbruget af 150 led, som er antallet led, der bruges til at fremstille en kæde. (Forbrug, materiale)  

    ![Resultaterne af bogføring af materialer på finanskonti.](media/design_details_inventory_costing_3_gl_posting_material.png "Resultaterne af bogføring af materialer på finanskonti")  
6. Arbejdscentret brugte 60 minutter på at fremstille kæden. Brugeren bogfører konverteringsomkostningerne. (Forbrug, kapacitet)  

    1. De direkte omkostninger bogføres. (Forbrug, kapacitet)  
    2. De indirekte omkostninger beregnes og bogføres. (Forbrug, kapacitet)  

        ![Resultaterne af bogføring af kapacitet på finanskonti.](media/design_details_inventory_costing_3_gl_posting_capacity.png "Resultaterne af bogføring af kapacitet på finanskonti")  
7. Brugeren bogfører de forventede omkostninger for en kæde. (Afgang)  
8. Brugeren afslutter produktionsordren og udfører kørslen **Juster kostpris – vareposter**. (Afgang)  

    1. Mellemregningskonti ryddes. (Afgang)  
    2. Den direkte omkostning overføres fra den igangværende arbejdskonto til lagerkontoen. (Afgang)  
    3. Den indirekte omkostning overføres fra den indirekte omkostningskonto til lagerkontoen. (Afgang)  
    4. Dette medfører en prisafvigelse på RV 157,00. Afvigelser beregnes kun for varer med standardkostpriser. (Afgang)  

        ![Resultaterne af bogføring af afgang på finanskonti.](media/design_details_inventory_costing_3_gl_posting_output.png "Resultaterne af bogføring af afgang på finanskonti")  

        > [!NOTE]  
        >  Af hensyn til overskueligheden vises kun én afvigelseskonto. I virkeligheden findes fem forskellige konti:  
        >   
        >  * Materialeomkostningsafvigelse  
        >  * Kapacitetsomkostningsafvigelse  
        >  * Afvigelse i indirekte kapacitetsomkostning  
        >  * Underlev.kostafvigelse  
        >  * Afvigelse i indirekte produktionskostpriser  

9. Brugeren regulerer kæden fra RV 150,00 til 140,00. (Regulering/værdiregulering/afrunding/overførsel)  

    ![Resultaterne af bogføring af justeringer på finanskonti.](media/design_details_inventory_costing_3_gl_posting_adjustment.png "Resultaterne af bogføring af justeringer på finanskonti")  

Du kan finde flere oplysninger om forholdet mellem kontotyperne og de forskellige typer værdiposter i [Designoplysninger: Konti i Finans](design-details-accounts-in-the-general-ledger.md).  

## <a name="see-also"></a>Se også
[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)   
[Designoplysninger: Bogføring af forventet kostpris](design-details-expected-cost-posting.md)   
[Designoplysninger: Omkostningsregulering](design-details-cost-adjustment.md)
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
