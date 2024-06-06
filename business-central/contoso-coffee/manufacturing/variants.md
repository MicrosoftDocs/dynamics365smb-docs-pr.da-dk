---
title: Varianter
description: 'Gennemgang for at lære, hvordan efterspørgselsprognoser opdateres for hver variant af et produkt i Business central.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-variants"></a>Gennemgang: varianter

I denne artikel kommer vi igennem de trin, du skal benytte, når du skal bruge Contoso Coffee-demodata for at lære om varianter.

## <a name="scenario"></a>Scenarie

Du er produktionsplanlægger hos Contoso Coffee. Du skal opdatere behovs budgettet for hver variant af vare SP-SCM1006, AutoDripLite. Da de har forskellige farver, skal du sørge for, at den rigtige stykliste bruges til hver variant. Køre planlægningskladden for at beregne levering.  

## <a name="steps"></a>Trin

1. Opsætte enheder for lagervarer for vare SP-SCM1006, AutoDripLite. Knytte en stykliste til SKU med varianterne rød og hvid.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv *varer*, og vælg derefter det relaterede link.  

    2. Åbn varen **SP-SCM1006, AutoDripLite**.

    3. Vælg handlingen **Opret lagervare**.  

    4. Angiv feltet **Opret pr.** til *Lokation og variant*.

    5. Angiv et filter for lokationen til *MAIN*, og klik derefter på knappen **OK**.

    6. Vælg handlingen **Lagervarer**.  

    7. Opdater produktionsstyklisterne for følgende lagervarer:

        1. RØD på MAIN, set SP-SCM1006-RØD  

        2. HVID på MAIN, set SP-SCM1006-HVID  

        3. Bevar produktionsstyklistenr. for SORT på MAIN  

2. Opdater Produktionsopsætning, og respekter behovsprognose på lokationer og varianter.  

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv *produktionsopsætning*, og vælg derefter det relaterede link.  

    2. Gå til feltet **Brug prognose på lokation**.

    3. Gå til feltet **Brug prognose på variant**.

    4. Luk vinduet **Produktionsopsætning**.

3. Opret en ny månedlig efterspørgselsprognose, *AUTODRIP*. Det skal filtreres efter varen SP-SCM1006 og lokation MAIN. Angiv behov for maj for hver variant. 

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv *Behovsprognose*, og vælg derefter det relaterede link.

    2. Opret et ny prognose med navnet *AUTODRIP*.

    3. Vælg handlingen **Rediger efterspørgselsprognose**.

    4. I feltet **Vis efter**-feltet vælges *Måned*.

    5. Vælg **SP-SCM1006** i feltet *Varefilter*

    6. Gå til feltet **Brug prognose på lokation**.

    7. Vælg **MAIN** i feltet *lokationsfilter*.

    8. Gå til feltet **Brug prognose på variant**.

    9. For hver linje opdaterede værdier i kolonnen maj

        1. RØD på MAIN, sæt 100

        2. HVID på MAIN, set 200

        3. SORT på MAIN, set 300

    10. Lukke efterspørgselsprognosevinduer

4. Kør MPS-plan i maj for oprettede efterspørgselsprognoser. Gennemgå komponenter for at se, at den pågældende vare maler sammenlignes med variant.

    1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv *planlægningskladde*, og vælg derefter det relaterede link.

    2. Vælg handlingen **Beregn totalplan**.

    3. Skift til feltet **MPS**.

    4. Skift væk fra feltet **MPS**.

    5. Marker **1. maj** i feltet *Startdato*

    6. Marker **31. maj** i feltet *Slutdato*

    7. I feltet **Brug prognose** skal du vælge *AUTODRIP*

    8. Vælg handlingen **OK**.

    9. For hver oprettet linje skal du vælge handlingen **Komponenter** og se, hvilken maling der anvendes.  

## <a name="see-also"></a>Se også

[Introduktion til demonstrationsdata for Contoso Coffee](../contoso-coffee-intro.md)  
