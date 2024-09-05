---
title: Oprette en projekt kort for et projekt og angive opgaver
description: 'Du kan oprette et projektkort, der viser projektopgaver og planlægningslinjer, så det er nemmere at administrere status og budgetter for et nyt projekt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-projects"></a>Oprette projekter

Når du starter et nyt projekt, skal du oprette et projektkort med integrerede projektopgaver og projektplanlægningslinjer, opdelt i to niveauer.  

Det første niveau består af projektopgaver. Da al bogføring henviser til en projektopgave, skal du oprette mindst én projektopgave pr. projekt. Når projektet indeholder mindst én projektopgave, kan du oprette projektplanlægningslinjer og bogføre forbruget i projektet.

Det andet lag består af projektplanlægningslinjer, der angiver den detaljerede brug af ressourcer, varer og diverse regnskabsmæssige udgifter.

Den lagdelte struktur giver dig mulighed for at opdele projektet i mindre opgaver og dermed angive mere detaljerede oplysninger i budgetter, rekvisitioner og registreringer. Desuden får du indsigt i, hvordan et projekt skrider frem. Du kan f.eks. spore, om du opfylder udpegede milepæl, eller om du overholder tidsplanen for opfyldelse af forventninger til budgettet.

> [!TIP]
> Vælg handlingen **Nyt projekt** i rollecenteret **Projektleder** for at starte en assisteret opsætningsvejledning, som fører dig gennem trinnene til oprettelse af et projekt med integrerede opgaver og planlægningslinjer. Følgende fremgangsmåde beskriver, hvordan trinnene udføres manuelt. <!-- For an example of how to create a project manually, go to [Video: How to create a project in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).-->

## <a name="to-create-a-project-card"></a>Sådan oprettes et projektkort

Du kan oprette et projektkort og derefter oprette projektopgavelinjer og projektplanlægningslinjer for det.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil basere projektet på oplysninger fra et andet projekt, skal du vælge handlingen **Kopier projekt**, udfylde felterne efter behov og derefter vælge knappen **OK**.

> [!NOTE]  
> Hvis du bruger timesedler med dit projekt, skal du også udpege en ansvarlig person. Denne person kan godkende timesedler for medarbejderopgaver, der er knyttet til projektet. Der er flere oplysninger i [Konfigurere timesedler](projects-how-setup-time-sheets.md).

> [!NOTE]  
> Til **/fra-knappen Anvend forbrug sammenkæde**  angiver, om projektposter er kædet sammen med projektplanlægningslinjer. Til **/fra-knappen Anvend forbrug sammenkæde**  aktiverer også lagerhåndtering, planlægning, montage efter ordre, varesporing og reservationsfunktioner for et projekt.

Du kan også vælge at markere handlinger på projekt som blokeret vha. feltet **spærret**. I følgende tabel beskrives effekten af indstillingerne for dette felt.

|Indstilling  |Beskrivelse  |
|---------|---------|
|Tom |Alle handlingerne er tilladt.|
|Bogfører    |Du kan arbejde med planlægningslinjer, men projektet kan ikke bogføres. Du kan ikke bogføre forbrug eller salg for projektet.|
|Alle  |Alle handlingerne er blokeret.|

## <a name="to-create-tasks-for-a-project"></a>Sådan oprettes opgaver for et projekt

Når du opretter et projekt, skal du også angive de forskellige opgaver, som projektet indeholder. Du angiver opgaver ved at oprette en linje per opgave i oversigtspanelet **Opgaver** på siden **Projektkort**. Hvert projekt skal have mindst én opgave.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.
2. Åbn projektkortet for det relevante projekt.
3. På oversigtspanelet **Opgaver** skal du udfylde felterne efter behov på en ny linje.
4. For at indrykke opgaver og oprette et hierarki, skal du vælge handlingen **Opgaver** og derefter vælge handlingen **Indryk projektopgaver**.
5. Gentag trin 3 og 4 for alle de opgaver, du skal bruge for projektet.
6. For at angive projektopgaverne med oplysninger om andre projektopgaver skal du vælge handlingen **Kopier projektopgaver fra**, udfylde felterne efter behov og derefter vælge knappen **OK**.

## <a name="invoice-one-or-more-customers-for-project-tasks"></a>Fakturere en eller flere debitorer for projektopgaver

Nogle gange adskiller den part, der modtager en service, sig fra den part, der betaler fakturaen. Nogle gange kan det også være nødvendigt at fakturere flere debitorer for opgaver i projektet. På siden **Projektkort** skal du bruge feltet **Faktureringsmetode for opgave** til at angive, om du fakturerer én eller flere debitorer.

Hvis den debitor, der modtager servicen, også skal betale regningen, skal du i felterne **Faktureres til** og **Leveres til** vælge **Standard (debitor)** og **Standard (kundeadresse)**.

Hvis du fakturerer flere debitorer, kan du angive den debitor, der skal modtage servicen, og den debitor, der skal faktureres for hver opgave i projektet. Du kan også angive følgende oplysninger.

* Vælg leveringsadressen på den kunde, hvor arbejdet skal udføres.
* Tilføj oplysninger om eksterne referencer for at forenkle kommunikationen om projektet.
* Overskriv projektets standardbetingelser.

## <a name="specify-a-default-location-for-project-items"></a>Angive en standardplacering for projektelementer

Du kan spare tid på dataindtastning ved at angive en standardlokation og -placering for projekter på siden **Projektkort**. Når du opretter projektopgaver, projektplanlægningslinjer og projektkladdelinjer for projektet, tildeles standardlokationen og -placeringen automatisk. Du kan dog ændre lokationskoden og placeringen på opgaver og linjer, hvis det er nødvendigt.

Hvis du definerer en **Til-projektplaceringskode** på lokationen, udfyldes placeringskoden, når du vælger lokationskoden. Hvis lagerstedsprocessen kræver lagerpluk, kan du også definere andre placeringer, som varerne skal forbruges fra.

Disse felter er standardværdier, når du opretter projektopgaver. Eksisterende projektopgaver ændres ikke.

Der er et par ting, du skal vide om brug af standardplaceringer:

* Hvis du for projektopgaver definerer en **Til-projektplaceringskode** på lokationen, tildeles placeringskoden, når du vælger lokationskoden. Hvis lagerstedsprocessen kræver lagerpluk, kan du også definere andre placeringer, som varerne skal forbruges fra.
* For projektplanlægningslinjer er **lokationskoden** baseret på den værdi, der er valgt på projektplanlægningslinjen, når du vælger en vare. Hvis der ikke er defineret en placeringskode for projektopgaven, vælges placeringen fra indholdet på standardplaceringen. Du kan ændre begge værdier manuelt.
* For projektkladdelinjer er **lokationskoden** baseret på den værdi, der er valgt på projektkladdelinjen, når du vælger en vare. Hvis der ikke er defineret en placeringskode for projektopgaven, vælges placeringen fra indholdet på standardplaceringen. Du kan ændre begge værdier manuelt.

## <a name="to-create-planning-lines-for-a-project"></a>Sådan oprettes planlægningslinjer for et projekt

Du kan begrænse dine nye projektopgaver på projektplanlægningslinjer. En planlægningslinje kan registrere de oplysninger, du vil spore for et projekt. Du kan f.eks. spore, hvilke ressourcer projektet kræver, eller de varer, der er nødvendige. Du kan f.eks. udføre en opgave for at få en kunde til at godkende et projekt. Du kan knytte den pågældende opgave til planlægningslinjer for varer, f.eks. et møde med kunden og tildele en ressource.  

En projektplanlægningslinje kan være en af følgende typer.  

| Enhedstype | Beskrivelse |
| --- | --- |
| **Budget** |Viser forventet forbrug og omkostninger i forbindelse med projektet, typisk i et projekt af typen tidspunkt og materialer. Du kan ikke fakturere planlægningslinjer af denne type. |
| **Fakturerbar** |Viser forventet fakturering til kunden, typisk i et fast pris-projekt. |
| **Både budget og fakturerbar** |Viser budgetteret forbrug, der er lig med, hvad du vil fakturere. |

> [!NOTE]
> Mens du angiver oplysninger på projektplanlægningslinjer, udfyldes omkostningsoplysninger automatisk. Omkostning, pris og rabat for ressourcer og varer er f.eks. først baseret på de oplysninger, der er defineret på ressource- og varekort.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.
2. Åbn et relevant projektkort.
3. Vælg en projektopgave, hvor feltet **Projektopgavetype** indeholder **Bogføring**, og vælg derefter handlingen **Projektplanlægningslinjer**.  
4. På siden **Projektplanlægningslinjer** skal du udfylde felterne på en ny linje efter behov.
5. Gentag trin 3 og 4 for alle planlægningslinjer, du skal bruge for projektopgaven.

## <a name="see-also"></a>Se også

[Projektstyring](projects-manage-projects.md)  
[Video: Sådan oprettes et projekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
