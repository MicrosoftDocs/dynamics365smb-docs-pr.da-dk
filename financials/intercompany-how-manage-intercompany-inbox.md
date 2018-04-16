---
title: "Behandle indgående og udgående IC-transaktioner | Microsoft Docs"
description: IC-transaktioner, som du modtager fra koncerninterne partnere, vises i IC-indbakken, hvor du behandle dem manuelt eller automatisk.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: abeb3ee24434ca3549e7ed88ecfae54cc395002d
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Administrere IC-indbakken og -udbakken
Alle IC-transaktioner, som du modtager elektronisk fra koncerninterne partnere, vises i den koncerninterne indbakke.  

## <a name="organizing-the-inbox"></a>Organisere indbakken  
 Du kan bruge filterfelterne øverst i indbakken til at bestemme, hvilke transaktioner der skal vises i vinduet. Hvis du f.eks. kun vil have vist transaktioner oprettet af en bestemt partner, kan du angive det i filtrene **Transaktionskilde** og **Koncernintern partnerkode**.  

### <a name="transaction-source"></a>Transaktionskilde  
Hvad du kan foretage dig med en transaktion, afhænger af om den er:  

- Oprettet af din koncerninterne partner  
- Afvist af din koncerninterne partner og returneret til dig  

Du kan bruge feltet **Vis transaktionskilde** til at filtrere vinduet **Koncerninterne indbakketransaktioner**, så der kun vises én af disse typer transaktioner. Du kan også filtrere efter koncernintern partner eller efter oplysningerne i feltet **Linjehandling**.  

#### <a name="created-by-intercompany-partner"></a>Oprettet af koncernintern partner  
 Når du modtager en ny transaktion, der er oprettet af en partner, kan du vælge enten at:

- Acceptere transaktionen  
- Afvise transaktionen (returnere den til partneren)  
- Annullere transaktionen (slette transaktionen uden at returnere den til partneren)  

#### <a name="returned-from-intercompany-partner"></a>Returneret fra koncernintern partner  
 Hvis transaktionen blev afvist af din koncerninterne partner, har du kun mulighed for at annullere transaktionen i indbakken. Derefter skal du oprette rettelseslinjer eller tilbageføre kladden eller dokumentet i regnskabet.  

## <a name="re-creating-inbox-entries"></a>Gendanne indbakkeposter  
 Hvis du har accepteret en transaktion i indbakken, men efterfølgende har slettet dokumentet eller kladden i stedet for at bogføre den/det, kan du gendanne indbakkeposten og acceptere dokumentet eller kladden igen.  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a>Få vist en oversigt over IC-transaktioner i en periode  
 Du kan få vist en oversigt over alle de IC-transaktioner, som du har sendt og modtaget i en periode. Brug rapporten **Koncerninterne transaktioner** til at se alle IC-finansposter, -debitorposter og -kreditorposter.

 > [!NOTE]  
 > Hvis de koncerninterne partnere findes i samme database, overføres transaktioner uden brug af fil eller e-mail. Få vist feltet **Overførselstype** i vinduet **Koncernintern partner**. <br /><br />
I så fald kan du indstille systemet til at spring indbakke og udbakke over ved at markere henholdsvis afkrydsningsfeltet **Automatisk accept af transaktioner** i vinduet **Koncernintern partner** og afkrydsningsfeltet **Automatisk afsendelse af transaktioner** i vinduet **Koncernintern opsætning**.

## <a name="to-import-intercompany-transactions-from-a-file"></a>Sådan indlæses IC-transaktioner fra en fil  
Hvis du har en IC-partner, der ikke er med i den samme database som dit regnskab, kan du modtage IC-transaktioner fra partneren i en .xml-fil. Derefter kan du indlæse transaktionerne til din indbakke.  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Virksomhedsoplysninger**, og vælg derefter det relaterede link.
2. Gem filen på den placering, som du har angivet i feltet **Koncerninterne indbakkeoplysninger** i vinduet **Virksomhedsoplysninger**.  
3. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncerninterne indbakketransaktioner**, og vælg derefter det relaterede link.
4. I vinduet **Koncerninterne indbakketransaktioner** skal du vælge handlingen **Indlæs transaktionsfil**.  
5. Marker den .xml-fil, der indeholder transaktionerne i det vindue, som vises, og vælg derefter knappen **Åbn**.  

Transaktioner indlæses nu til indbakken, hvor du kan arbejde med dem.

## <a name="to-process-incoming-intercompany-transactions"></a>Sådan behandles indgående IC-transaktioner  
Når dine partnere sender dig IC-transaktioner, ender transaktionerne i IC-indbakken. Du skal tage stilling til hver transaktion i indbakken og følge op på den.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncerninterne indbakketransaktioner**, og vælg derefter det relaterede link.  
2. I vinduet **Koncerninterne indbakketransaktioner** skal du vælge en linje og derefter vælge en handling, f.eks. **Accepter**, til behandling af linjen.
3. I vinduet **Fuldfør IC-indbakkehandling** skal du udfylde felterne efter behov. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg knappen **OK**.  

For linjer, som du har behandlet med handlingen **Accepter** oprettes dokument- eller kladdelinjer i regnskabet. Åbn hvert dokument eller hver kladde, foretag alle eventuelle ændringer, og bogfør dem derefter.  

Linjer, som du har behandlet med handlingen **Returner til partner**, bliver flyttet til udbakken, hvorfra du derefter kan sende dem til partneren.

For linjer, som du har behandlet med handlingen **Returneret af partner**, skal du nu bogføre en rettelse af den oprindelige transaktion, som du har bogført i regnskabet.

## <a name="to-process-outgoing-intercompany-transactions"></a>Sådan håndteres udgående IC-transaktioner  
Når du bogfører en IC-kladde eller et IC-dokument eller sender en IC-ordrebekræftelse, sendes transaktionerne til din IC-udbakke. Du skal åbne udbakken og behandle transaktionerne, før de kan sendes til dine partnere.  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncerninterne udbakketransaktioner**, og vælg derefter det relaterede link.  
2. I vinduet **Koncerninterne udbakketransaktioner** skal du vælge en linje og derefter vælge en handling, f.eks. **Returner til indbakke**, til behandling af linjen.

Linjer, som du har behandlet med handlingen **Send til koncernintern partner**, sendes til den relevante partners indbakke.

Linjer, som du har behandlet med handlingen **Returner til Indbakke**, flyttes til indbakken, hvor du derefter kan acceptere dem for at oprette dokumenter eller kladdelinjer i regnskabet.  

For linjer, som du har behandlet med handlingen **Annuller**, skal du nu bogføre en rettelse af den oprindelige transaktion, som du har bogført i regnskabet.  

## <a name="to-recreate-intercompany-inbox-transactions"></a>Sådan gendannes transaktioner i ICindbakken  
Af og til vil du måske gendanne en transaktion i indbakken eller udbakken. Hvis du f.eks. har accepteret en transaktion i indbakken, men efterfølgende har slettet dokumentet eller kladden i stedet for at bogføre den/det, kan du gendanne indbakkeposten og acceptere dokumentet eller kladden igen.  

Følgende procedure beskriver, hvordan du gendanner transaktioner i indbakken, men proceduren er den samme for udbakken.

  1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncerninterne indbakketransaktioner**, og vælg derefter det relaterede link.  

  2.  I vinduet **Håndterede IC-indbakketransaktioner**, skal du markere linjen med den transaktion, som du vil gendanne i indbakken, og derefter vælge handlingen **Genopret indbakketransaktion**.  

## <a name="see-also"></a>Se også
[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

