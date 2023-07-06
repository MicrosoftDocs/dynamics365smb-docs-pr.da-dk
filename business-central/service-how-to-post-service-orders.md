---
title: 'Fremgangsmåde: Bogføre serviceordrer'
description: 'Når du har oprettet en serviceordre, angivet alle de nødvendige oplysninger og foretaget eventuelle ændringer, kan du bogføre serviceordren.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="post-service-orders-and-credit-memos"></a><a name="post-service-orders-and-credit-memos"></a><a name="post-service-orders-and-credit-memos"></a>Bogføre serviceordrer og kreditnotaer
Når du har oprettet en serviceordre, angivet alle de nødvendige oplysninger og foretaget eventuelle ændringer, kan du bogføre serviceordren. Ordren skal indeholde mindst én serviceartikellinje og én servicelinje, inden du kan bogføre den. Hvis ordren indeholder mere end én ordrelinje, bogføres alle linjerne på én gang.  

Hvis du har et stort antal serviceordrer, kan du spare tid ved at bruge en kørsel til at bogføre dem på samme tid. Du kan udføre kørslen fra en serviceordre.

> [!Tip]
> Før du bogfører et servicedokument, er det en god ide at bruge handlingen **Testrapport** til at kontrollere, om der er eventuelle fejl eller manglende oplysninger. Hvis der er fejl, skal du løse problemet. Du kan udskrive en ny testrapport for at kontrollere rettelsen og derefter bogføre dokumentet.

## <a name="to-post-a-service-order"></a><a name="to-post-a-service-order"></a><a name="to-post-a-service-order"></a>Sådan bogføres serviceordrer
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link.  
2. Åbn den relevante serviceordre.  
3. På siden **Serviceordre** skal du vælge en af følgende handlinger.  

    |**Handling**|**Resultat**|  
    |------------------|----------------|  
    |**Kontroller** | Kontrollerer alle dele af dokumentet, og viser resultatet i en rapport. Hvis der i rapporten angives nogen fejl eller manglende oplysninger, skal du afhjælpe problemet. Derefter kan du udskrive en ny kontrolrapport.|  
    |**Bogfør** | Bogfører ordren uden at udskrive en levering eller en faktura.|  
    |**Bogfør og udskriv** | Bogfører ordren og udskriver en levering, hvis du leverer ordren uden at fakturere den, eller en faktura, hvis du fakturerer ordren.|  
    |**Massebogfør** | Bogfører flere serviceordrer på én gang.|  

4. Når du bogfører ordren, skal du angive en af følgende indstillinger for, hvordan du vil bogføre ordren.  

    |**Bogføringsvalg**|**Resultat**|  
    |------------------------|----------------|  
    |**Lever** | Bogfører leveringen af varerne.|  
    |**Faktura** | Fakturerer varer, der allerede er leveret.|  
    |**Lever og fakturer** | Leverer og fakturerer varerne.|  
    |**Send og forbrug** | Bogfører leverance og forbrug af ordren. De relevante antal på servicelinjerne i ordren og i det serviceleverancedokument, der tidligere er bogført, opdateres.|  

Du kan kun bogføre forbrug, hvis linjen indeholder et antal, der er leveret, men ikke faktureret eller forbrugt.  

Når ordren bogføres, oprettes de tilsvarende poster og bogførte dokumenter i programmet. De relevante felter opdateres i serviceordredokumentet.  

## <a name="to-batch-post-service-orders"></a><a name="to-batch-post-service-orders"></a><a name="to-batch-post-service-orders"></a>Massebogføre serviceordrer
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link.  
2. Vælg handlingen **Massebogfør**.  
3.  Du kan angive et filter for at vælge bestemte serviceordrenumre eller et interval af ordrenumre, som kørslen skal behandle.  
4.  Vælg **OK** for at starte kørslen.  

## <a name="to-post-a-service-credit-memo"></a><a name="to-post-a-service-credit-memo"></a><a name="to-post-a-service-credit-memo"></a>Sådan bogføres servicekreditnotaer
Når du har oprettet en servicekreditnota og udfyldt den, kan du bogføre den. Hvis der konstateres fejl eller manglende oplysninger i kreditnotaen under bogføringen, afbrydes processen med en fejlmeddelelse.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Servicekreditnotaer**, og vælg derefter det relaterede link.  
2. Opret en ny servicekreditnota. Vælg handlingen **Ny**.  
3. Udfyld de påkrævede felter.  
4. Vælg handlingen **Bogfør**. Hvis du vil udskrive kreditnotaen samtidig med, at du bogfører den, skal du vælge handlingen **Bogfør og udskriv** i stedet for.  
5. Vælg **Kontroller** for at teste kreditnotaer, før du bogfører. Når du kører rapporten, kontrolleres de bogføringsdatoer, der er angivet i dokumentet.  
6. Hvis du vil bogføre flere kreditnotaer på samme tid. Kør kørslen **Massebogfør servicekreditnotaer**. Det kan være en fordel, hvis du har et stort antal kreditnotaer, der skal bogføres.  

> [!NOTE]  
>  Det er vigtigt at angive alle de nødvendige oplysninger i kreditnotaer, før der køres massebogføring. Ellers kan du risikere, at de ikke bliver bogført. Når kørslen er færdig med at bogføre, vises en meddelelse om, hvor mange servicekreditnotaer der blev bogført.  

## <a name="to-post-consumption-from-a-service-order"></a><a name="to-post-consumption-from-a-service-order"></a><a name="to-post-consumption-from-a-service-order"></a>Sådan bogføres forbrug fra en serviceordre
I følgende fremgangsmåde beskrives det, hvordan du bogfører varer, ressourcetimer og/eller omkostninger, der er brugt til en bestemt servicehandling, som kunden ikke skal opkræves for. Bemærk, at du kun kan bogføre forbrugte varer, timer eller omkostninger for en bogført leverance, der ikke har bogførte fakturaer eller forbrug.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link.  
2. Åbn serviceordren for at bogføre forbruget for den.  
3. Vælg serviceartiklen. Vælg handlingen **Servicelinjer**.  
4. Find de nødvendige poster, og angiv de antal, du vil bogføre forbrug for, i feltet **Antal til forbrug**. Antallet kan ikke være større end den mængde, der allerede er leveret, og den resterende mængde, der ikke er faktureret efter delvis fakturering af denne leverance.  

    > [!NOTE]  
    >  Hvis du vil registrere forbruget i forbindelse med en opgave, skal du udfylde felterne **Sagsnr.**, **Sagsopgavenr.** og **Linjetype for sag** på servicelinjen.  

5. Vælg de linjer, der skal bogføres, og vælg derefter handlingen **Bogfør**. Vælg **Send og forbrug** på den side, der åbnes.  

Servicen bogføres enten helt eller delvist som forbrugt, afhængigt af værdien i feltet **Antal til forbrug** og de relevante poster oprettes. Derudover opdateres de serviceleverancedokumenter, der tidligere er bogført, i kronologisk rækkefølge med de forbrugte antal. De relevante antal opdateres på servicelinjerne i ordren.  

## <a name="to-post-shipments-from-service-orders"></a><a name="to-post-shipments-from-service-orders"></a><a name="to-post-shipments-from-service-orders"></a>Bogføre leverancer fra serviceordrer
Når du har angivet detaljerne i en service, kan du regulere og bogføre antallet af varer, der er anvendt, den tid, der er forbrugt, og de omkostninger, der er påløbet. Som et resultat foretager [!INCLUDE[prod_short](includes/prod_short.md)] de nødvendige ændringer i programmet, så den nye lagerstatus og den aktuelle status for den angivne ordrebehandling afspejles.  

Følgende procedure viser, hvordan du bogfører leverancen af servicelinje på steder, hvor der ikke er indstillet til at kræve lagerekspedition.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link. 2. Vælg **Handlinger**, **Ordre**, **Servicelinjer** på siden med den serviceordre, du har valgt.  
3. Find de nødvendige poster på siden **Servicelinjer**, og angiv det antal, der skal bogføres, i feltet **Lever (antal)**.  

   > [!NOTE]  
   >  Angivelse af det antal, der skal leveres, afhænger af om du vil foretage fuld eller delvis levering. Vælger du at foretage fuld levering, skal værdien i feltet **Lever (antal)** være den samme som værdien i feltet **Antal**. Når du foretager delvis levering, skal du angive det antal, du først vil levere. Hvis du allerede har leveret en del af servicen i ordren, skal du notere værdien i feltet **Leveret (antal)**. Det maksimale antal, du kan angive i feltet **Lever (antal)**, er det antal enheder, der endnu ikke er leveret.  

4. Vælg handlingen **Bogfør**. Vælg knappen **Lever** på den side, der vises.

[!INCLUDE[prod_short](includes/prod_short.md)] opretter posterne (i garantipost, varepost, servicepost eller finanspost) og det bogførte serviceleverancedokument, og de relevante felter på servicelinjerne i serviceordren opdateres.  

Hvis lokationen er angivet til at kræve lagerekspedition, sker forsendelse og flytning af servicelinjevarefunktion på samme måde som for andre kildedokumenter. Den eneste forskel er, at servicelinjevarer kan forbruges eksternt eller internt, og derfor kræver de to forskellige frigivelsesfunktioner.  

Hvis du vil vide mere om varer til en forsendelses servicelinje i avancerede logistik konfigurationer, skal du gå til pluk varer til lagerleverance](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

## <a name="to-undo-posted-consumption"></a><a name="to-undo-posted-consumption"></a><a name="to-undo-posted-consumption"></a>Sådan fortrydes bogført forbrug
Du kan annullere forbruget i serviceordrerne. F.eks. fordi det er bogført ved en fejltagelse.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte serviceforsendelser**, og vælg derefter det relaterede link.  
2. Åbn den bogførte serviceleverance, som det fejlagtige forbrug er bogført for.  
3. Vælg handlingen **Serviceleverancelinjer**.  
4. Vælg de linjer, der indeholder det forkerte forbrug, og vælg derefter handlingen **Fortryd forbrug**.  

 Der indsættes en modpostering til serviceleverancelinjen med negative værdier i antalsfelterne til de valgte linjer.  
  
> [!NOTE]  
>  Du kan ikke fortryde serviceforbruget, hvis:  

>    * Serviceordren er blevet lukket.  
>    * Den er blevet bogført i området sager, så der er sagsposter knyttet til den.  

## <a name="to-post-service-lines"></a><a name="to-post-service-lines"></a><a name="to-post-service-lines"></a>Sådan bogføres servicelinjer
Hvis du er nødt til at arbejde i længere tid med en serviceordre uden at bogføre den, kan du bogføre nogle af de servicelinjer, der er knyttet til den, f.eks. for at holde lageret opdateret. Du kan bogføre ved at angive de relevante antal på de linjer, der skal bogføres. Du kan vælge at bogføre linjerne én for én eller ved at vælge flere linjer ad gangen.  

Følgende procedure beskriver leverancebogføring direkte fra en serviceordre på lokationer uden lagerekspedition konfigureret. Hvis lokationen er konfigureret til at kræve lagerekspedition, sker leverancebogføringen i et andet lagerdokument, afhængigt af lokationsopsætningen.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link.  
2. Åbn serviceordren, og vælg derefter handlingen **Servicelinjer**.  
4. På de linjer, der skal bogføres, skal du udfylde felterne **Lever (antal)**, **Fakturer (antal)** og/eller **Antal til forbrug** afhængigt af, hvordan du vil bogføre linjerne.  
5. Vælg handlingen **Bogfør**.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også
[Bogføring i Service](service-service-posting.md)  
[Oprette en serviceordre](service-how-to-create-service-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
