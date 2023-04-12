---
title: Overvåge jobstatus og -udførelse
description: 'Beskriver, hvordan du kan oprette en metode for igangværende arbejde og beregne igangværende arbejde for at estimere den økonomiske værdi af sager, der er igangværende.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
---
# Overvåge jobstatus og -udførelse

Med igangværende arbejde (WIP)-funktionen kan du estimere den økonomiske værdi af igangværende sager i finansregnskabet.

Efterhånden som status for en sag ændrer sig, forbruges der materialer og ressourcer, der skal bogføres i sagen. Du kan i mange tilfælde bogføre udgifterne for en sag, før sagen faktureres. Hvis der kun er bogført udgifter, vil din regnskabsopgørelse ikke være helt korrekt. Hvis du vil spore den faktiske værdi af sagen, skal du beregne igangværende arbejde og bogføre det i finansregnskabet. Få mere at vide på [Forstå igangværende arbejde-metoder](projects-understanding-wip.md).

Du kan beregne VIA baseret på følgende:

* Kostværdi
* Salgsværdi
* Realiserede omkostninger
* Færdiggørelsesgrad
* Afsluttet kontrakt

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## Opret et job med igangværende arbejde-metoden

Opret et job med igangværende arbejde-metode, der afspejler behovet i organisationen og angiver det som standard.  

> [!NOTE]
> Når du har brugt en ny metode til at oprette poster for igangværende arbejde, kan du ikke ændre eller slette metoden.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **job med igangværende arbejde-metoder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Luk siden.   
4. Hvis du vil gøre den nye metode til standardmetoden, skal du vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **jobopsætning**, og vælg derefter det relaterede link.  
5. I feltet **Standard-VIA-metode** skal du vælge metoden fra listen.

## Definere en metode for igangværende arbejde for en sag

Når du opretter en ny sag, skal du angive, hvilken metode for igangværende arbejde der gælder. I nogle tilfælde er den igangværende arbejde-metode for sager, du bruger, allerede angivet som standard.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Jobs**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**. Få mere at vide på [Oprettelse af job](projects-how-create-jobs.md).  
3. På siden **Sagskort** i feltet **Metode for igangværende arbejde** skal du vælge en metode for igangværende arbejde. Hvis der er defineret en standardmetode, kan du vælge en anden indstilling, hvis det er nødvendigt.  

### Definere en metode for igangværende arbejde for en sagsopgave

Du kan definere en igangværende arbejde-metode for en sagsopgave, udelukke nogle sagsopgaver fra igangværende arbejde-beregningen eller gruppere opgaver som beregnet. 

Hvis du vil beregne igangværende arbejde for hver sagsopgave individuelt, har via-bogføringen defineret dimensioner for de enkelte opgaver.

**Igangværende arbejde-total** angiver de sagsopgaver, du vil gruppere ved beregning af Igangværende arbejde og registrering. I en gruppe af opgaver skal der være én opgave, som opfylder to betingelser:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Har et **samlet Igangværende arbejde** angivet til *I alt*. (Hvis der ikke er nogen sagsopgaver med **Samlet Igangværende arbejde** angivet til *I alt*, indstilles *I alt* automatisk på den sidste sagsopgavelinje, når Igangværende arbejde beregnes første gang.)

* Har et **Job-opgavenummer** -nummer, der er det sidste i gruppen eller intervallet af sagsopgaver.

Følgende tabel beskriver tre indstillinger:

| Felt | Beskrivelse |
|--|--|
| **\<blank\>** | Lad stå tomt, hvis sagsopgaven er del af en gruppe opgaver. |
| **Total** | Definerer det område eller den gruppe af opgaver, der er medtaget i beregningen af Igangværende arbejde og registrering. Inden for gruppen vil alle sagsopgaver med **Sagsopgavetype** indstillet til **Bogføring** blive inkluderet i VIA i alt, medmindre feltet **VIA i alt** er indstillet til **Ekskluderet**. |
| **Udelukket** | Gælder kun for en opgave med **bogføringstypen** **Postering**, i hvilket tilfælde opgaven ikke medtages ved beregning af VIA og registrering. |

I følgende eksempel er sagsopgaver inddelt i to grupper for VIA, som viser, hvordan feltet **VIA-sum** fungerer:

|Sagsopgavenr.|Beskrivelse|Sagsopgavetype|**VIA-Total**-felt|  
|------------------|----------------------|----------------------|----------------------|  
|1000|Forberedelse|Fra-sum|\<blank\>|
|1010|.    Rengøring|Bogfører|**Udelukket**|
|1099|Samlet forberedelse|Til-sum|\<blank\>|
|1100|Lægning af tæppe|Fra-sum|\<blank\>|
|1110|.    Limning af gulv|Bogfører|**Udelukket**|
|1120|.    Udlægning af tæppe|Bogfører|\<blank\>|
|1199|Samlet tæppelægning|Til-sum|\<blank\>|
|1200|Udfør|Fra-sum|\<blank\>|
|1210|.    Støvsugning af tæppe|Bogfører|\<blank\>|
|1299|Samlet afslutning|Til-sum|**Total**|
|1300|Rettelse af fejl|Fra-sum|\<blank\>|
|1310|.    Rettelse af fejl|Bogfører|\<blank\>|
|1399|Samlet rettelse af fejl|Til-sum|**Total**|

Du bemærker følgende:

* *1000* til *1299*: VIA beregnes separat for denne gruppe sagsopgaver. Bemærk dog, at to af opgaverne, 1010 og 1110 ikke er omfattet af VIA-beregningen, fordi den pågældende jobfunktion **bogføres**.

* *1300* til *1399*: VIA beregnes separat for denne gruppe sagsopgaver.

## Beregn VIA

Du kan fastlægge det beløb for VIA, der skal bogføres til balancekonti ved periodeafslutningsrapporteringen. Det gør du ved at udføre kørslen **Beregn VIA for sag**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Beregn VIA for sag**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Beregn igangværende arbejde**.
3. På siden **Beregn VIA for sag** skal du udfylde felterne efter behov.
4. Vælg knappen **OK**.  

> [!NOTE]  
>   Batchjobbet beregner kun VIA, men VIA bogføres ikke. Hvis du vil bogføre, skal du udføre kørslen **Bogfør igangværende arbejde - finansafstemning**, når du har beregnet igangværende arbejde. Der er flere oplysninger i følgende procedure.

## Bogfør VIA

Når du har beregnet igangværende arbejde, kan du bogføre det til balancekontiene for periodeafslutningsrapporteringen. Det gør du ved at udføre kørslen **Bogfør VIA for sag**.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogfør VIA for sag til finans**, og vælg derefter det relaterede link.  
2. På siden **Bogfør VIA - finansafstemning** skal du udfylde felterne efter behov.  
3. Vælg knappen **OK**.

## Beregn og bogfør sagsafslutningsposter

Når du har fuldført alle aktiviteter for en sag, inklusive bogføring og fakturering af forbrug, skal du opdatere sagen for at få **status** **Afsluttet**. Derefter skal du tilbageføre alt igangværende arbejde, som er blevet bogført i finansregnskabet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Jobs**, og vælg derefter det relaterede link.  
2. Vælg en åben sag, og vælg derefter handlingen **Rediger**.
3. I feltet **Status** skal du vælge **Fuldført**.
4. Følg hjælpetrinnene for at beregne og bogføre igangværende arbejde. Du kan også følge trin 5 og 6 for at gøre det manuelt.  
5. Vælg handlingen **Beregn igangværende arbejde**.
6. På siden **Beregn VIA for sag** skal du udfylde felterne efter behov.  

     Posterne for igangværende arbejde for sagen, som blev oprettet ved at udføre kørslen, vil nu være markeret i feltet **Sagen er fuldført** for at vise, at de er færdiggørelsesposter.  
7. Vælg handlingen **Bogfør VIA - finansafstemning**.
8. På siden **Bogfør VIA - finansafstemning** skal du udfylde felterne efter behov.  

     Sagens VIA-finansposter, som blev oprettet ved at udføre kørslen, vil nu være markeret i feltet **Sagen er fuldført** for at vise, at de er færdiggørelsesposter.

## Vise sagsposter

Alle sagsrelaterede poster er registreret i sagsjournaler med fortløbende nummerering, hvor der startes med 1. Fra sagsjournalen kan du få et overblik over alle sagsposter.    

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagsjournaler**, og vælg derefter det relaterede link.
2. Vælg en relevant journal, og vælg derefter handlingen **Sagsposter**.

På siden **Sagsposter** kan du gennemse de poster, der er tilknyttet en sag.  

## Se relateret [Microsoft-træning](/training/paths/calculate-post-job-wip/)

## Se også

[Gennemgang - Beregning af igangværende arbejder for en sag](walkthrough-calculating-work-in-process-for-a-job.md)
[Managing Projects](projects-manage-projects.md)  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
