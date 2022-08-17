---
title: Oprette et jobkort for en sag og angive opgaver
description: Du kan oprette et sagskort, der viser sagsopgaver og planlægningslinjer, så det er nemmere at administrere status og budgetter for et nyt projekt.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management, task
ms.search.form: 88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020
ms.date: 08/03/2022
ms.author: edupont
ms.openlocfilehash: 8d70c11aa3d467ada4f7aae3a1cf3efa1603bbe4
ms.sourcegitcommit: bb9b2b4e693fa326a13d94e5e83f60e6c7ac5b68
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227468"
---
# <a name="create-jobs"></a>Oprette sager

Når du starter et nyt projekt, skal du oprette et sagskort med integrerede sagsopgaver og sagsplanlægningslinjer, opdelt i to niveauer.  

Det første niveau består af sagsopgaver. Da al bogføring henviser til en sagsopgave, skal du oprette mindst én sagsopgave pr. sag. Når sagen indeholder mindst én sagsopgave, kan du oprette sagsplanlægningslinjer og bogføre forbruget i sagen.

Det andet lag består af sagsplanlægningslinjer, der angiver den detaljerede brug af ressourcer, varer og diverse regnskabsmæssige udgifter.

Den lagdelte struktur giver dig mulighed for at opdele sagen i mindre opgaver og dermed angive mere detaljerede oplysninger i budgetter, rekvisitioner og registreringer. Desuden får du indsigt i, hvordan en sag skrider frem. Du kan f.eks. spore, om du opfylder udpegede milepæl, eller om du overholder tidsplanen for opfyldelse af forventninger til budgettet.

> [!TIP]
> Vælg handlingen **Ny sag** i rollecenteret **Projektleder** for at starte en assisteret opsætningsvejledning, som fører dig gennem trinnene til oprettelse af en sag med integrerede opgaver og planlægningslinjer. Følgende fremgangsmåde beskriver, hvordan trinnene udføres manuelt. Du kan se et eksempel på, hvordan du opretter en sag manuelt i [Video: Sådan oprettes en sag i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

Nogle gange adskiller den part, der modtager en service, sig fra den part, der betaler fakturaen. På siden **sager** kan du angive den kunde, der skal have fordel af projektet i felterne **kunde**, og den part, der skal faktureres, i felterne **faktureres**. Du kan også angive følgende oplysninger. 

* Hvor arbejdet skal foretages ved at vælge fra en liste over leveringsadresser for debitoren.
* Tilføj oplysninger om eksterne referencer for at forenkle kommunikationen om projektet.
* Overskriv projektets standardbetingelser.

## <a name="to-create-a-job-card"></a>Sådan oprettes et sagskort

Du kan oprette et sagskort og derefter oprette sagsopgavelinjer og sagsplanlægningslinjer for det.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. For at angive sagen med oplysninger om andre sager skal du vælge handlingen **Kopier sag**, udfylde felterne efter behov, og derefter vælge knappen **OK**.

> [!NOTE]  
> Hvis du bruger timesedler i din sag, skal du også tildele en ansvarlig person. Denne person kan godkende timesedler for medarbejderopgaver, der er knyttet til sagen. Der er flere oplysninger i [Konfigurere timesedler](projects-how-setup-time-sheets.md).

Du kan også vælge at markere handlinger på projekt som blokeret vha. feltet **spærret**. følgende tabel beskrives effekten af indstillingerne for dette felt.

|Indstilling  |Beskrivelse  |
|---------|---------|
|Tom |Alle handlingerne er tilladt.|
|Bogfører    |Du kan arbejde med planlægningslinjer, men sagen kan ikke bogføres. Hvis du vælger denne indstilling, kan du ikke bogføre forbrug eller salg for sagen.|
|Alle  |Alle handlingerne er blokeret.|

## <a name="to-create-tasks-for-a-job"></a>Sådan oprettes opgaver for en sag

Når du opretter en sag, skal du også angive de forskellige opgaver, som sagen indeholder. Du angiver opgaver ved at oprette en linje per opgave i oversigtspanelet **Opgaver** på siden **Jobkort**. Hver sag skal have mindst én opgave.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.
2. Åbn sagskortet for den relevante sag.
3. På oversigtspanelet **Opgaver** skal du udfylde felterne efter behov på en ny linje.
4. For at indrykke opgaver og oprette et hierarki, skal du vælge handlingen **Opgaver** og derefter vælge handlingen **Indryk sagsopgaver**.
5. Gentag trin 3 og 4 for alle de opgaver, du skal bruge for sagen.
6. For at angive sagsopgaverne med oplysninger om andre sagsopgaver skal du vælge handlingen **Kopier sagsopgaver fra**, udfylde felterne efter behov, og derefter vælge knappen **OK**.

## <a name="to-create-planning-lines-for-a-job"></a>Sådan oprettes planlægningslinjer for en sag

Du kan begrænse dine nye sagsopgaver på sagsplanlægningslinjer. En planlægningslinje kan registrere de oplysninger, du vil spore for en sag. Du kan f. eks. spore, hvilke ressourcer opgaven kræver, eller om de varer, der er nødvendige. Du kan f. eks. udføre en opgave for at få en kunde til at godkende et job. Du kan knytte den pågældende opgave til planlægningslinjer for varer, f.eks. et møde med kunden og tildele en ressource.  

En sagsplanlægningslinje han være en af følgende typer.  

| Enhedstype | Beskrivelse |
| --- | --- |
| **Budget** |Viser forventet forbrug og omkostninger i forbindelse med sagen, typisk i et projekt af typen tidspunkt og materialer. Planlægningslinjer af denne type kan ikke faktureres. |
| **Fakturerbar** |Viser forventet fakturering til kunden, typisk i et fast pris-projekt. |
| **Både budget og fakturerbar** |Viser budgetteret forbrug, der er lig med, hvad du vil fakturere. |

> [!NOTE]
> Mens du angiver oplysninger på sagsplanlægningslinjer, udfyldes omkostningsoplysninger automatisk. Omkostning, pris og rabat for ressourcer og varer er f.eks. først baseret på de oplysninger, der er defineret på ressource- og varekort. 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.
2. Åbn et relevant sagskort.
3. Vælg en sagsopgave, hvor feltet **Sagsopgavetype** indeholder **Bogføring**, og vælg derefter handlingen **Sagsplanlægningslinjer**.  
4. På siden **Sagsplanlægningslinjer** skal du udfylde felterne på en ny linje efter behov.
5. Gentag trin 3 og 4 for alle planlægninglinjer, du skal bruge for sagsopgaven.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/create-new-job/)

## <a name="see-also"></a>Se også

[Projektstyring](projects-manage-projects.md)  
[Video: Sådan oprettes en sag i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
