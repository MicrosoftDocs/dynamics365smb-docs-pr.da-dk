---
title: Overvåge status og ydeevne af projekt
description: 'Beskriver, hvordan du kan oprette en VIA-metode (work in progress) og beregne VIA for at estimere den økonomiske værdi af projekter, mens de er i gang.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 07/31/2024
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
ms.service: dynamics-365-business-central
---

# Overvåge status og ydeevne af projekt

Med igangværende arbejde (WIP)-funktionen kan du estimere den økonomiske værdi af igangværende projekter i finansregnskabet.

Efterhånden som status for et projekt ændrer sig, forbruges der materialer og ressourcer, der skal bogføres i projektet. Du kan i mange tilfælde bogføre udgifterne for et projekt, før projektet faktureres. Hvis der kun er bogført udgifter, vil din regnskabsopgørelse ikke være helt korrekt. Hvis du vil spore den faktiske værdi af projektet, skal du beregne igangværende arbejde og bogføre det i finansregnskabet. Få mere at vide på [Forstå igangværende arbejde-metoder](projects-understanding-wip.md).

Du kan beregne VIA baseret på følgende:

* Kostværdi
* Salgsværdi
* Realiserede omkostninger
* Færdiggørelsesgrad
* Afsluttet kontrakt

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## Oprette en projektmetode for igangværende arbejde

Opret et projekt med igangværende arbejde-metode, der afspejler behovet i organisationen og angiver det som standard.  

> [!NOTE]
> Når du har brugt en ny metode til at oprette poster for igangværende arbejde, kan du ikke ændre eller slette metoden.  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Projekt VIA-metoder**, og vælg derefter den relaterede sammenkæde.  
2. Vælg handlingen **Ny**, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Luk siden.   
4. Hvis du vil gøre den nye metode til standardmetoden, skal du vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Projektopsætning**, og vælg derefter den relaterede sammenkæde.  
5. I feltet **Standard-VIA-metode** skal du vælge metoden fra listen.

## Definere en metode for igangværende arbejde for et projekt

Når du opretter et nyt projekt, skal du angive, hvilken metode for igangværende arbejde der gælder. I nogle tilfælde er den igangværende arbejde-metode for projekter, du bruger, allerede angivet som standard.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Projekter**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**. Flere oplysninger i [Oprette projekter](projects-how-create-jobs.md).  
3.  **Vælg en VIA-metode på listen i feltet**  **VIA-metode** i oversigtspanelet Bogføring på siden Projekt **kort** . Hvis der er defineret en standardmetode, kan du vælge en anden indstilling, hvis det er nødvendigt.  

### Definere en metode for igangværende arbejde for en projektopgave

Du kan definere en igangværende arbejde-metode for en projektopgave, udelukke nogle projektopgaver fra igangværende arbejde-beregningen eller gruppere opgaver som beregnet. 

Hvis du vil beregne igangværende arbejde for hver projektopgave individuelt, har bogføringen af igangværende arbejde defineret dimensioner for de enkelte opgaver.

**Igangværende arbejde-total** angiver de projektopgaver, du vil gruppere ved beregning af Igangværende arbejde og registrering. I en gruppe af opgaver skal der være én opgave, som opfylder to betingelser:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Har et **samlet Igangværende arbejde** angivet til *I alt*. (Hvis der ikke er nogen projektopgaver med **Samlet Igangværende arbejde** angivet til *I alt*, indstilles *I alt* automatisk på den sidste projektopgavelinje, når Igangværende arbejde beregnes første gang).

* Har et **Projektopgavenummer**, der er det sidste i gruppen eller intervallet af projektopgaver.

Følgende tabel beskriver tre indstillinger:

| Felt | Beskrivelse |
|--|--|
| **\<blank\>** | Lad stå tomt, hvis projektopgaven er del af en gruppe opgaver. |
| **I alt** | Definerer det område eller den gruppe af opgaver, der er medtaget i beregningen af Igangværende arbejde og registrering. Inden for gruppen vil alle projektopgaver med **Projektopgavetype** indstillet til **Bogføring** blive inkluderet i igangværende arbejde i alt, medmindre feltet **Igangværende arbejde i alt** er indstillet til **Ekskluderet**. |
| **Ikke medtaget** | Gælder kun for en opgave, hvor **Projektopgavetype** er **Postering**, i hvilket tilfælde opgaven ikke medtages ved beregning af igangværende arbejde og registrering. |

I følgende eksempel er projektopgaver inddelt i to grupper for igangværende arbejde, som viser, hvordan feltet **Igangværende arbejde i alt** fungerer:

|Projektopgavenr.|Beskrivelse|Projektopgavetype|**VIA-Total**-felt|  
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

* *1000* til *og med 1299*: VIA beregnes separat for denne gruppe projektopgaver. Bemærk dog, at to af opgaverne, 1010 og 1110 ikke er omfattet af beregningen af igangværende arbejde, fordi den pågældende projektfunktion er **Bogføring**.

* *1300* til *og med 1399*: VIA beregnes separat for denne gruppe projektopgaver.

## Beregn VIA

Du kan fastlægge det beløb for VIA, der skal bogføres til balancekonti ved periodeafslutningsrapporteringen. Brug batchprojektet **Beregn igangværende arbejde for projekt** til at gøre det.  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Beregn VIA** i projekt, og vælg derefter den relaterede sammenkæde.  
2. Vælg handlingen **Beregn igangværende arbejde**.
3. På siden **Beregn igangværende arbejde for projekt** skal du udfylde felterne efter behov.
4. Vælg knappen **OK**.  

> [!NOTE]  
> Batchprojektet beregner kun igangværende arbejde, men det bogføres ikke. Hvis du vil bogføre, skal du udføre kørslen **Bogfør projektets igangværende arbejde til finans**, når du har beregnet igangværende arbejde. Der er flere oplysninger i følgende procedure.

## Bogfør VIA

Når du har beregnet igangværende arbejde, kan du bogføre det til balancekontiene for periodeafslutningsrapporteringen. Det gør du ved at køre batchprojektet **Bogfør projektets igangværende arbejde til finans**.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Bogfør projektets igangværende arbejde til finans**, og vælg derefter det relaterede link.  
2. På siden **Bogfør projektets igangværende arbejde til finans** skal du udfylde felterne efter behov.  
3. Vælg knappen **OK**.

## Beregn og bogfør projektafslutningsposter

Når du har fuldført alle aktiviteter for et projekt, inklusive bogføring og fakturering af forbrug, skal du opdatere projektets status til **Afsluttet**. Derefter skal du tilbageføre alt igangværende arbejde, som er blevet bogført i finansregnskabet.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Projekter**, og vælg derefter det relaterede link.  
2. Vælg et åbent projekt, og vælg derefter handlingen **Rediger**.
3. Gå til **oversigtspanelet Bogføring** og feltet **Status**, og vælg **Afsluttet**.
4. Følg trinnene i hjælpen for at beregne og bogføre igangværende arbejde, eller følg trin 5 og 6 for at gøre det manuelt.  
5. Vælg handlingen **Beregn igangværende arbejde**.
6. På siden **Beregn igangværende arbejde for projekt** skal du udfylde felterne efter behov.  

     De VIA-poster for projektet, som oprettes ved at udføre kørslen, markeres afkrydsningsfeltet **Projekt fuldført** for at vise, at de er færdiggørelsesposter.  
7. Vælg handlingen **Bogfør igangværende arbejde til finans**.
8. På siden **Bogfør projektets igangværende arbejde til finans** skal du udfylde felterne efter behov.  

     For de VIA-finansposter for projektet, der oprettes ved kørsel af batchprojektet, markeres afkrydsningsfeltet **Projekt fuldført** for at vise, at de er færdiggørelsesposter.

## Få vist projektfinansposter

Alle projektrelaterede poster er registreret i projektjournaler med fortløbende nummerering, hvor der startes med 1. Fra projektjournalen kan du få et overblik over alle projektposter.    

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektregistre**, og vælg derefter det relaterede link.
2. Vælg en relevant journal, og vælg derefter handlingen **Projektposter**.

På siden **Projektposter** kan du gennemse de poster, der er tilknyttet et projekt.  

## Se også

[Gennemgang – beregning af igangværende arbejder for et projekt](walkthrough-calculating-work-in-process-for-a-job.md)    
[Administrere projekter](projects-manage-projects.md)    
[Administrere lageromkostninger](finance-manage-inventory-costs.md)    
[Finance](finance.md)    
[Køb](purchasing-manage-purchasing.md)    
[Salg](sales-manage-sales.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
