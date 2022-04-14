---
title: Administrere IC-indbakken og -udbakken
description: IC-transaktioner, som du modtager fra koncerninterne partnere, vises i IC-indbakken, hvor du behandle dem manuelt eller automatisk.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.search.form: 600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611
ms.date: 03/09/2022
ms.author: edupont
ms.openlocfilehash: 868f07b2b56ccaefb4c56e26be72c27b941d950c
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522114"
---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Administrere IC-indbakken og -udbakken
Alle IC-transaktioner, som du modtager elektronisk fra koncerninterne partnere, vises i den koncerninterne indbakke.  

Men afhængigt af, hvor intercompany er oprettet for virksomheden, replikeres nogle af transaktionerne automatisk til de relevante IC-partnere. Med start i 2022 udgivelsesbølge 1 kan du også angive, at regnskabet automatisk skal oprette IC-transaktioner, der er modtaget fra IC-partnere, og som bogføres via IC-finanskladden. Du kan finde flere oplysninger i [Udfylde og bogføre IC-kladde](intercompany-how-work-documents-journals.md#to-fill-in-and-post-an-intercompany-journal).  

## <a name="organizing-the-inbox"></a>Organisere indbakken  
 Du kan bruge filterfelterne øverst i indbakken til at bestemme, hvilke transaktioner der skal vises på siden. Hvis du f.eks. kun vil have vist transaktioner oprettet af en bestemt partner, kan du angive det i filtrene **Transaktionskilde** og **Koncernintern partnerkode**.  

### <a name="transaction-source"></a>Transaktionskilde  
Hvad du kan foretage dig med en transaktion, afhænger af om den er:  

- Oprettet af din koncerninterne partner  
- Afvist af din koncerninterne partner og returneret til dig  

Du kan bruge feltet **Vis transaktionskilde** til at filtrere siden **Koncerninterne indbakketransaktioner**, så der kun vises én af disse typer transaktioner. Du kan også filtrere efter koncernintern partner eller efter oplysningerne i feltet **Linjehandling**.  

#### <a name="created-by-intercompany-partner"></a>Oprettet af koncernintern partner  
 Når du modtager en ny transaktion, der er oprettet af en partner, kan du vælge enten at:

- Acceptere transaktionen  
- Afvise transaktionen (returnere den til partneren)  
- Annullere transaktionen (slette transaktionen uden at returnere den til partneren)  

#### <a name="returned-from-intercompany-partner"></a>Returneret fra koncernintern partner  
 Hvis transaktionen blev afvist af din koncerninterne partner, har du kun mulighed for at annullere transaktionen i indbakken. Derefter skal du oprette rettelseslinjer eller tilbageføre kladden eller dokumentet i regnskabet.  

## <a name="recreating-inbox-entries"></a>Gendanne indbakkeposter  
 Hvis du har accepteret en transaktion i indbakken, men efterfølgende har slettet dokumentet eller kladden i stedet for at bogføre den/det, kan du gendanne indbakkeposten og acceptere dokumentet eller kladden igen.  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a>Få vist en oversigt over IC-transaktioner i en periode  
 Du kan få vist en oversigt over alle de IC-transaktioner, som du har sendt og modtaget i en periode. Brug rapporten **Koncerninterne transaktioner** til at se alle IC-finansposter, -debitorposter og -kreditorposter.

 > [!NOTE]  
 > Hvis de koncerninterne partnere findes i samme database, overføres transaktioner uden brug af fil eller e-mail. Få vist feltet **Overførselstype** på siden **Koncernintern partner**. <br /><br />
I så fald kan du indstille systemet til at spring indbakke og udbakke over ved at markere henholdsvis afkrydsningsfeltet **Automatisk accept af transaktioner** på siden **Koncernintern partner** og afkrydsningsfeltet **Automatisk afsendelse af transaktioner** på siden **Koncernintern opsætning**. Indgående interne transaktioner kan kun accepteres automatisk, hvis Opgavestyring er aktiveret. Du kan finde flere oplysninger i [Konfigurere Business Central Server - Indstillinger for Opgavestyring](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Task).

## <a name="to-import-intercompany-transactions-from-a-file"></a>Sådan indlæses IC-transaktioner fra en fil

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Hvis du har en IC-partner, der ikke er med i den samme database som dit regnskab, kan du modtage IC-transaktioner fra partneren i en .xml-fil. Derefter kan du indlæse transaktionerne til din indbakke.  

1. Gem filen på den placering, som du har angivet i feltet **Koncerninterne indbakkeoplysninger**, når du konfigurerer virksomhedsoplysninger.  
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncerninterne indbakketransaktioner**, og vælg derefter det relaterede link.
3. På siden **Koncerninterne indbakketransaktioner** skal du vælge handlingen **Indlæs transaktionsfil**.  
4. Marker den .xml-fil, der indeholder transaktionerne på den side, som vises, og vælg derefter knappen **Åbn**.  

Transaktioner indlæses nu til indbakken, hvor du kan arbejde med dem.

## <a name="to-process-incoming-intercompany-transactions"></a>Sådan behandles indgående IC-transaktioner  
Når dine partnere sender dig IC-transaktioner, ender transaktionerne i IC-indbakken. Du skal tage stilling til hver transaktion i indbakken og følge op på den.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncerninterne indbakketransaktioner**, og vælg derefter det relaterede link.  
2. På siden **Koncerninterne indbakketransaktioner** skal du vælge en linje og derefter vælge en handling, f.eks. **Accepter**, til behandling af linjen.
3. På siden **Fuldfør IC-indbakkehandling** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg knappen **OK**.  

For linjer, som du har behandlet med handlingen **Accepter** oprettes dokument- eller kladdelinjer i regnskabet. Åbn hvert dokument eller hver kladde, foretag alle eventuelle ændringer, og bogfør dem derefter.  

Linjer, som du har behandlet med handlingen **Returner til partner**, bliver flyttet til udbakken, hvorfra du derefter kan sende dem til partneren.

For linjer, som du har behandlet med handlingen **Returneret af partner**, skal du nu bogføre en rettelse af den oprindelige transaktion, som du har bogført i regnskabet.

## <a name="to-process-outgoing-intercompany-transactions"></a>Sådan håndteres udgående IC-transaktioner  
Når du bogfører en IC-kladde eller et IC-dokument eller sender en IC-ordrebekræftelse, sendes transaktionerne til din IC-udbakke. Du skal åbne udbakken og behandle transaktionerne, før de kan sendes til dine partnere.  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncerninterne udbakketransaktioner**, og vælg derefter det relaterede link.  
2. På siden **Koncerninterne udbakketransaktioner** skal du vælge en linje og derefter vælge en handling, f.eks. **Returner til indbakke**, til behandling af linjen.

Linjer, som du har behandlet med handlingen **Send til koncernintern partner**, sendes til den relevante partners indbakke.

Linjer, som du har behandlet med handlingen **Returner til Indbakke**, flyttes til indbakken, hvor du derefter kan acceptere dem for at oprette dokumenter eller kladdelinjer i regnskabet.  

For linjer, som du har behandlet med handlingen **Annuller**, skal du nu bogføre en rettelse af den oprindelige transaktion, som du har bogført i regnskabet.  

## <a name="to-recreate-intercompany-inbox-transactions"></a>Sådan gendannes transaktioner i ICindbakken  
Af og til vil du måske gendanne en transaktion i indbakken eller udbakken. Hvis du f.eks. har accepteret en transaktion i indbakken, men efterfølgende har slettet dokumentet eller kladden i stedet for at bogføre den/det, kan du gendanne indbakkeposten og acceptere dokumentet eller kladden igen.  

Følgende procedure beskriver, hvordan du gendanner transaktioner i indbakken, men proceduren er den samme for udbakken.

  1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Håndterede IC-indbakketransaktioner**, og vælg derefter det relaterede link.  

  2.  På siden **Håndterede IC-indbakketransaktioner**, skal du markere linjen med den transaktion, som du vil gendanne i indbakken, og derefter vælge handlingen **Genopret indbakketransaktion**.  

## <a name="see-also"></a>Se også
[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
