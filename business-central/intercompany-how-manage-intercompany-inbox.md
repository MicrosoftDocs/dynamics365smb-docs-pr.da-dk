---
title: Administrere IC-indbakken og -udbakken
description: 'IC-transaktioner, som du modtager fra koncerninterne partnere, vises i IC-indbakken, hvor du behandle dem manuelt eller automatisk.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
---
# <a name="manage-the-intercompany-inbox-and-outbox" />Administrere IC-indbakken og -udbakken

Alle IC-transaktioner, som du modtager elektronisk fra koncerninterne partnere, vises i den **koncerninterne indbakke**. Du kan lære mere om at behandle indgående IC-transaktioner ved at gå til [Behandle indgående IC-transaktioner](#process-incoming-intercompany-transactions). Alle IC-transaktioner, som du sender til partnere, vises i den **koncerninterne udbakke**. Du kan lære mere om at behandle udgående IC-transaktioner ved at gå til [Behandle udgående IC-transaktioner](#to-process-outgoing-intercompany-transactions).

Men afhængigt af virksomhedens interne opsætning, håndteres der automatisk visse transaktioner. Du kan indstille kilde regnskabet og partnervirksomheder til automatisk at oprette dokumenter og kladder, der svarer til transaktioner, som partnere bogfører via IC-finanskladden. Hvis du vil vide mere om brug af IC-kladder, skal du gå til [Udfylde og bogføre en IC-kladde](intercompany-how-work-documents-journals.md#fill-in-and-post-an-intercompany-journal).  

## <a name="organizing-the-inbox" />Organisere indbakken

Du kan bruge filterfelterne øverst i indbakken til at bestemme, hvilke transaktioner der skal vises på siden. Hvis du f.eks. kun vil udforske transaktioner oprettet af en bestemt partner, kan du angive det i filtrene **Transaktionskilde** og **Koncernintern partnerkode**.  

### <a name="transaction-source" />Transaktionskilde

Hvad du kan foretage dig med en transaktion, afhænger af om den er:  

* Oprettet af din koncerninterne partner  
* Afvist af din koncerninterne partner og returneret til dig  

Du kan bruge feltet **Vis transaktionskilde** til at filtrere siden **Koncerninterne indbakketransaktioner**, så der kun vises én af disse typer transaktioner. Du kan også filtrere efter koncernintern partner eller efter oplysningerne i feltet **Linjehandling**.  

#### <a name="created-by-intercompany-partner" />Oprettet af koncernintern partner

 Når du modtager en ny transaktion, der er oprettet af en partner, kan du vælge enten at:

* Acceptere transaktionen  
* Afvise transaktionen (returnere den til partneren)  
* Annullere transaktionen (slette transaktionen uden at returnere den til partneren)  

#### <a name="returned-from-intercompany-partner" />Returneret fra koncernintern partner

Hvis din koncerninterne partner afviser en transaktion, kan du annullere transaktionen i indbakken og derefter oprette rettelseslinjer eller tilbageføre kladden eller dokumentet i regnskabet.  

## <a name="recreating-inbox-entries" />Gendanne indbakkeposter

Hvis du har accepteret en transaktion i indbakken, men efterfølgende har slettet dokumentet eller kladden i stedet for at bogføre den/det, kan du gendanne indbakkeposten og acceptere dokumentet eller kladden igen.  

## <a name="get-an-overview-of-intercompany-transactions-for-a-period" />Få vist en oversigt over IC-transaktioner i en periode

Du kan få vist en oversigt over alle de IC-transaktioner, som du har sendt og modtaget i en periode. Brug rapporten **Koncerninterne transaktioner** til at se alle IC-finansposter, -debitorposter og -kreditorposter.

> [!NOTE]  
> Hvis IC-partnerne er i samme database, kan partnerne automatisk acceptere transaktioner. Gå direkte til de **Håndterede transaktioner i IC-indbakken** og **Håndterede IC-udbakketransaktioner** . Hvis du vil vide mere om automatisk accept af transaktioner, skal du gå til [Automatisk accept af transaktioner fra IC-partnere](intercompany-how-setup.md#auto-accept-transactions-from-intercompany-partners).  
>
> * For synkroniseringspartneren skal du aktivere **Auto-send transaktioner** til siden **Koncernintern konfiguration**.
> * For partnervirksomheder skal du aktivere **Auto-send transaktioner** til siden **Koncernintern konfiguration** .  

## <a name="import-intercompany-transactions-from-a-file" />Importere IC-transaktioner fra en fil

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Hvis du har en IC-partner, der ikke er med i den samme database som dit regnskab, kan du modtage IC-transaktioner fra partneren i en .xml-fil. Derefter kan du indlæse transaktionerne til din indbakke.  

1. Gem filen på den placering, som du har angivet i feltet **Koncerninterne indbakkeoplysninger**, når du konfigurerer virksomhedsoplysninger.  
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncerninterne indbakketransaktioner**, og vælg derefter det relaterede link.
3. På siden **Koncerninterne indbakketransaktioner** skal du vælge handlingen **Indlæs transaktionsfil**.  
4. Marker den .xml-fil, der indeholder transaktionerne på den side, som vises, og vælg derefter knappen **Åbn**.  

Transaktioner indlæses nu til indbakken, hvor du kan arbejde med dem.

## <a name="process-incoming-intercompany-transactions" />Sådan behandles indgående IC-transaktioner

Når dine partnere sender dig IC-transaktioner, ender transaktionerne i IC-indbakken. Du skal tage stilling til hver transaktion i indbakken og følge op på den.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncerninterne indbakketransaktioner**, og vælg derefter det relaterede link.  
2. På siden **Koncerninterne indbakketransaktioner** skal du vælge en linje og derefter vælge en handling, f.eks. **Accepter**, til behandling af linjen.
3. På siden **Fuldfør IC-indbakkehandling** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg knappen **OK**.  

For linjer, som du accepterer, dokumenterer eller kladdelinjer, oprettes i virksomheden. Åbn hvert dokument eller hver kladde, foretag alle eventuelle ændringer, og bogfør dem derefter.  

Linjer, som du afviser og vender tilbage til din partner, flyttes til din intercompany-udbakke, hvor du kan sende dem til partneren.

For linjer, som en partner afviste og returnerede, skal du nu bogføre en rettelse af den oprindelige transaktion, som du har bogført i regnskabet.

## <a name="to-process-outgoing-intercompany-transactions" />Sådan håndteres udgående IC-transaktioner

Når du bogfører en IC-kladde eller et IC-dokument eller sender en IC-ordrebekræftelse, skal du gå til transaktionerne til din IC-udbakke. Du skal åbne udbakken og behandle transaktionerne, før de kan sendes til dine partnere.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncerninterne udbakketransaktioner**, og vælg derefter det relaterede link.  
2. På siden **Koncerninterne udbakketransaktioner** skal du vælge en linje og derefter vælge en handling, f.eks. **Returner til indbakke**, til behandling af linjen.

Brug handlingen **Send til koncernintern partner** for at sende linjer til den relevante partners indbakke.

Brug handlingen **Returner til Indbakke** for at flytte til indbakken, hvor du derefter kan acceptere dem for at oprette dokumenter eller kladdelinjer i regnskabet.  

Hvis du bruger handlingen **Annuller**, skal du nu bogføre en rettelse af den oprindelige transaktion, som du har bogført i regnskabet.  

## <a name="recreate-intercompany-inbox-transactions" />Gendanne transaktionerne i den koncerninterne indbakke

Du kan måske gendanne en transaktion i indbakken eller udbakken. Hvis du f.eks. har accepteret en transaktion i indbakken, men efterfølgende har slettet dokumentet eller kladden i stedet for at bogføre den/det, kan du gendanne indbakkeposten og acceptere dokumentet eller kladden igen.  

Følgende procedure beskriver, hvordan du gendanner transaktioner i indbakken, men proceduren er den samme for udbakken.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Håndterede IC-indbakketransaktioner**, og vælg derefter det relaterede link.  
2. På siden **Håndterede IC-indbakketransaktioner**, skal du markere linjen med den transaktion, som du vil gendanne i indbakken, og derefter vælge handlingen **Genopret indbakketransaktion**.  

## <a name="see-also" />Se også

[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
