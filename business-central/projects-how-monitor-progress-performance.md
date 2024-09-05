---
title: Overvåge status og ydeevne af projekt
description: 'Beskriver, hvordan du kan oprette en VIA-metode (work in progress) og beregne VIA for at estimere den økonomiske værdi af projekter, mens de er i gang.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/19/2024
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
ms.service: dynamics-365-business-central
---

# <a name="monitor-project-progress-and-performance"></a>Overvåge status og ydeevne af projekt

Med igangværende arbejde (WIP)-funktionen kan du estimere den økonomiske værdi af igangværende projekter i finansregnskabet.

Efterhånden som status for et projekt ændrer sig, forbruges der materialer og ressourcer, der skal bogføres i projektet. Du kan i mange tilfælde bogføre udgifterne for et projekt, før projektet faktureres. Men hvis du kun bogfører udgifter, er din regnskabsopgørelse unøjagtig. Hvis du vil spore den faktiske værdi af projektet, skal du beregne igangværende arbejde og bogføre det i finansregnskabet. Følgende VIA-metoder er tilgængelige som standard:

* Kostværdi
* Salgsværdi
* Realiserede omkostninger
* Færdiggørelsesgrad
* Afsluttet kontrakt

Du kan også oprette en VIA-metode, der opfylder organisationens behov, og angive den som standardmetode.  

Få mere at vide på [Forstå igangværende arbejde-metoder](projects-understanding-wip.md).

Hvis du vil have vist resultatet ved hjælp af en anden metode, skal du ændre metoden og beregne VIA igen. Der er ingen grænse for, hvor mange gange du kan beregne VIA. Værdien bogføres ikke automatisk i finansregnskabet. Når du har beregnet VIA ved hjælp af den metode, du foretrækker, kan du bogføre i finansregnskabet.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Projekt VIA-metoder**, og vælg derefter den relaterede sammenkæde.  
2. Vælg handlingen **Ny**, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Luk siden.   
4. Hvis du vil gøre den nye metode til standardmetoden, skal du vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Projektopsætning**, og vælg derefter den relaterede sammenkæde.  
5. I feltet **Standard-VIA-metode** skal du vælge metoden fra listen.

## <a name="define-a-wip-method-for-a-project"></a>Definere en metode for igangværende arbejde for et projekt

Når du opretter et nyt projekt, skal du angive, hvilken metode for igangværende arbejde der gælder. I nogle tilfælde er den igangværende arbejde-metode for projekter, du bruger, allerede angivet som standard.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Projekter**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**. Flere oplysninger i [Oprette projekter](projects-how-create-jobs.md).  
3.  **Vælg en VIA-metode på listen i feltet**  **VIA-metode** i oversigtspanelet Bogføring på siden Projekt **kort** . Hvis der er defineret en standardmetode, kan du vælge en anden indstilling, hvis det er nødvendigt.  

### <a name="define-a-wip-method-for-a-project-task"></a>Definere en metode for igangværende arbejde for en projektopgave

Du kan definere en VIA-metode for en projektopgave, udelukke projektopgaver fra VIA-beregningen eller gruppere opgaver, der skal beregnes sammen.

Hvis du vil beregne igangværende arbejde for hver projektopgave individuelt, har bogføringen af igangværende arbejde defineret dimensioner for de enkelte opgaver.

**Igangværende arbejde-total** angiver de projektopgaver, du vil gruppere ved beregning af Igangværende arbejde og registrering. I en gruppe af opgaver skal der være én opgave, som opfylder to betingelser:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* **VIA i alt** er angivet til **I alt**. Hvis der ikke er nogen projektopgaver **, hvor VIA i alt** er angivet til Total, angives Total automatisk på den sidste projektopgavelinje, når VIA beregnes første gang.
* Nummeret i projektopgavenummeret **.** - den sidste i gruppen eller rækken af projektopgaver.

I følgende tabel beskrives indstillingerne:

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

Du bemærker:

* For *projektopgaverne fra 1000* til *og med 1299* beregnes VIA separat for denne gruppe projektopgaver. Bemærk dog, at to af opgaverne, 1010 og 1110, udelades fra VIA-beregningen, fordi deres projektopgavetype er **Bogføring**.
* For *projektopgaverne fra 1300* til *og med 1399* beregnes VIA separat for denne gruppe projektopgaver.

## <a name="calculate-wip"></a>Beregn VIA

Du kan bestemme det VIA-beløb, der skal bogføres på balancekonti for periodeafslutningsrapporteringen ved hjælp af **kørslen Beregn VIA** i projekt.  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Beregn VIA** i projekt, og vælg derefter den relaterede sammenkæde.  
2. Vælg handlingen **Beregn igangværende arbejde**.
3. På siden **Beregn igangværende arbejde for projekt** skal du udfylde felterne efter behov.
4. Vælg knappen **OK**.  

> [!NOTE]  
> Kørslen beregner kun VIA, men bogfører den ikke i finansregnskabet. Hvis du vil bogføre VIA, skal du udføre **kørslen Bogfør VIA**, når du har beregnet VIA. Der er flere oplysninger i følgende procedure.

### <a name="review-warnings"></a>Gennemgå advarsler

Hvis VIA-beregningen *, der resulterer i, at VIA blev beregnet med en advarselsmeddelelse*, kan det være en god idé at gennemse advarslerne.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektcockpit til igangværende arbejde**, og vælg derefter det relaterede link.  
2. Vælg det projekt, du vil gennemse advarsler for. Til **/fra-knappen VIA-advarsler** er aktiveret for projekter, der har VIA-advarsler.
3. Vælg handlingen **Vis advarsel** .

### <a name="delete-wip-entries"></a>Slette VIA-poster

Hvis du vil prøve forskellige VIA-metoder, får du muligvis vist fejlen *Projektopgaven kan ikke ændres, fordi projektet har en fejl med tilknyttede VIA-poster* i projektet. Du kan kontrollere VIA-metoden ved at slette eksisterende VIA-poster.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektcockpit til igangværende arbejde**, og vælg derefter det relaterede link.  
2. Vælg det projekt, du vil slette VIA-poster for.
3. Vælg handlingen **Slet VIA-poster** .

## <a name="post-wip"></a>Bogfør VIA

Når du beregner VIA, kan du bogføre den på balancekonti for periodeafslutningsrapporteringen.  **Brug kørslen Bogfør VIA for projekter** .

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Project Post VIA til finans**, og vælg derefter den relaterede sammenkæde.  
2. På siden **Bogfør projektets igangværende arbejde til finans** skal du udfylde felterne efter behov.  
3. Vælg knappen **OK**.

## <a name="calculate-and-post-project-completion-entries"></a>Beregn og bogfør projektafslutningsposter

Når du har fuldført alle aktiviteter for et projekt, herunder bogføring af forbrug og fakturering, skal du opdatere projektets status til **Afsluttet**. Derefter skal du tilbageføre alle VIA, der blev bogført i finansregnskabet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Projekter**, og vælg derefter det relaterede link.  
2. Vælg et åbent projekt, og vælg derefter handlingen **Rediger**.
3. Gå til **oversigtspanelet Bogføring** og feltet **Status**, og vælg **Afsluttet**.
4. Følg trinnene i hjælpen for at beregne og bogføre igangværende arbejde, eller følg trin 5 og 6 for at gøre det manuelt.  
5. Vælg handlingen **Beregn igangværende arbejde**.
6. På siden **Beregn igangværende arbejde for projekt** skal du udfylde felterne efter behov.  

     I de VIA-poster for projektet, som oprettes ved at udføre kørslen, er afkrydsningsfeltet **Projekt fuldført** markeret for at vise, at de er færdiggørelsesposter.  
7. Vælg handlingen **Bogfør igangværende arbejde til finans**.
8. På siden **Bogfør projektets igangværende arbejde til finans** skal du udfylde felterne efter behov.  

     I de VIA-finansposter for projektet, som oprettes ved kørsel af batchprojektet, er afkrydsningsfeltet **Projekt fuldført** markeret for at vise, at de er færdiggørelsesposter.

## <a name="view-project-ledger-entries"></a>Få vist projektfinansposter

Alle projektrelaterede poster er registreret i projektjournaler med fortløbende nummerering, hvor der startes med 1. Fra projektjournalen kan du få et overblik over alle projektposter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektregistre**, og vælg derefter det relaterede link.
2. Vælg en relevant journal, og vælg derefter handlingen **Projektposter**.

På siden **Projektposter** kan du gennemse de poster, der er knyttet til et projekt.  

## <a name="see-also"></a>Se også

[Gennemgang – beregning af igangværende arbejder for et projekt](walkthrough-calculating-work-in-process-for-a-job.md)    
[Administrere projekter](projects-manage-projects.md)    
[Administrere lageromkostninger](finance-manage-inventory-costs.md)    
[Finance](finance.md)    
[Køb](purchasing-manage-purchasing.md)    
[Salg](sales-manage-sales.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
