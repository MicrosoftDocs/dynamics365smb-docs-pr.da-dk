---
title: "Bruge OCR til at ændre PDF-filer til e-fakturaer | Microsoft Docs"
description: "Beskriver, hvordan du kan bruge en OCR-tjeneste til at omdanne indgående PDF- eller billedfiler til elektroniske dokumenter i Financials."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 91071855697c9235ba8734b40d77ed0b48c24923
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter
Fra PDF-filer eller billedfiler, som du modtager fra dine handelspartnere, kan du få en ekstern OCR-tjeneste (Optical Character Recognition) til at oprette elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. F.eks. når du modtager en faktura i PDF-format fra en leverandør, kan du sende den til tjenesten OCR fra vinduet **Indgående bilag**. Dette beskrives i den første fremgangsmåde.

I stedet for at sende filen fra vinduet **Indgående bilag** kan du sende den til OCR-tjenesten via mail. Når du får det elektroniske dokument retur, oprettes der automatisk en relateret indgående dokumentpost. Dette beskrives i den anden fremgangsmåde.

Efter nogle sekunder får du filen tilbage fra OCR-tjenesten som en elektronisk faktura, der kan konverteres til en købsfaktura til kreditoren. Dette beskrives i den tredje fremgangsmåde.

Da OCR er baseret på optiske registrering, er det sandsynligt, at OCR-tjenesten fortolker tegn i PDF- eller billedfilerne forkert, første gang programmet f.eks. behandler en bestemt kreditors dokumenter. Det fortolker muligvis virksomhedens logo som leverandørens navn eller fejlfortolker det samlede beløb på en kvittering på grund af layoutet. Hvis du vil undgå disse fejl fremover, kan du rette fejl i en separat version af vinduet **Indkommende dokument**. Derefter sender du rettelserne til OCR-tjenesten for at lære den at fortolke de bestemte tegn korrekt, næste gang den behandler et PDF- eller billleddokument for samme kreditor. Du kan finde flere oplysninger i afsnittet "Sådan lærer du OCR-tjenesten at undgå fejl".

Filtrafikken til og fra OCR-tjenesten afvikles af en dedikeret opgavekøpost, der oprettes automatisk, når du aktiverer den relaterede tjenesteforbindelse. Du kan finde flere oplysninger under [Konfigurere indgående dokumenter](across-how-setup-income-documents.md).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-window"></a>Sådan sendes en PDF- eller billedfil til OCR-tjenesten fra vinduet **Indgående bilag**
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.
2. Opret en ny indgående dokumentpost, og vedhæft filen. Du kan finde flere oplysninger under [Oprette indgående dokumentposter](across-how-create-income-document-records.md).  
3. I vinduet **Indgående bilag** skal du vælge en eller flere linjer, og derefter skal du vælge handlingen **Send til opgavekø**.

    Værdien i feltet **OCR-status** ændres til **Klar**. Den vedhæftede PDF- eller billedfil bliver sendt til OCR-tjenesten af opgavekøen i henhold til planen, forudsat at der ikke er nogen fejl.
4. Alternativt skal du i vinduet **Indgående bilag** vælge en eller flere linjer, og derefter skal du vælge handlingen **Send til OCR-tjeneste**.

Værdien i feltet **OCR-status** ændres til **Sendt**, forudsat at der ikke er nogen fejl.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>Sådan sendes en PDF- eller billedfil til OCR-tjenesten via mail
Brug dit mailprogram til at sende en mail til OCR-tjenesteudbyderen med PDF- eller billedfilen vedhæftet. Du kan finde oplysninger om, hvilken mailadresse du skal sende til, på OCR-tjenesteudbyderens websted.

Da der ikke findes nogen indgående dokumentposter for filen, oprettes der automatisk en ny post i vinduet **Indgående bilag**, når du modtager det elektronisk oprettede dokument fra OCR-tjenesten. Du kan finde flere oplysninger under [Oprette indgående dokumentposter](across-how-create-income-document-records.md).

> [!NOTE]  
>   Hvis du arbejder på en tablet eller telefon, kan du sende filen til OCR-tjenesten, så snart du har taget et billede af dokumentet, eller du kan oprette et indgående dokument direkte. Du kan finde flere oplysninger i afsnittet "Sådan opretter du indgående bilagsrecords ved at tage et billede" i afsnittet [Oprette indgående bilagsrecords](across-how-create-income-document-records.md).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>Sådan modtager du det resulterende elektroniske dokument fra OCR-tjenesten
Det elektroniske dokument, der oprettes af OCR-tjenesten fra PDF eller billedfilen, modtages automatisk i vinduet **Indgående bilag** ved den opgavekøpost, som er oprettet, når du aktiverer OCR-tjenesten.

Hvis du ikke bruger en opgavekø, eller du skal have et færdigt OCR-dokument hurtigere end opgavekøplanen angiver, kan du vælge knappen **Modtag fra OCR-tjeneste**. På denne måde vises alle dokumenter, der er udført af OCR-tjenesten.

> [!NOTE]  
>   Hvis OCR-tjenesten er indstillet til at kræve manuel verifikation af behandlede dokumenter, indeholder feltet **OCR-status** **Afventer bekræftelse**. I så fald skal du gøre følgende for at logge på OCR-tjenestens websted for at verificere OCR-dokumentet manuelt.

1. I feltet **OCR-status** skal du vælge hyperlinket **Afventer bekræftelse**. Du kan også vælge feltet **Afventer bekræftelse** på hjemmesiden.
2. Log på med legitimationsoplysningerne for din OCR-tjenestekonto på webstedet for OCR-tjenesten. Dette er de legitimationsoplysninger, du brugte, da du konfigurerede tjenesten. Du kan finde flere oplysninger i afsnittet "Sådan konfigureres en OCR-tjeneste" i [Konfigurere indgående bilag](across-how-setup-income-documents.md).

    Hvis du åbner webstedet fra feltet **OCR-status**, vises det pågældende dokument umiddelbart efter logon. Hvis du åbner webstedet ved at vælge feltet på startsiden på den første side i OCR-tjenesten, der åbnes, skal du vælge knappen **Start** på fanen **Bekræft** eller dobbeltklikke på det dokument, du vil verificere.

    Oplysninger om OCR-dokumentet vises med både kildeindholdet fra PDF- eller billedfilen og de resulterende OCR-feltværdier.
3. Gennemgå forskellige feltværdierne, og rediger eller angiv værdier manuelt i de felter, som OCR-tjenesten har kodet som usikre.
4. Vælg knappen **OK**. OCR-processen fuldføres, og det resulterende elektroniske dokument sendes til vinduet **Indgående bilag** i [!INCLUDE[d365fin](includes/d365fin_md.md)] i overensstemmelse med opgavekøplanen.

    Hvis du har adgang til webstedet ved at vælge feltet på startsiden, vises alle andre OCR-dokumenter, der skal bekræftes automatisk, på webstedet.
5. Gentag trin 4 for andre OCR-dokumenter der skal bekræftes.

Nu kan du fortsætte med at oprette dokumentposter for de modtagne elektroniske dokumenter i [!INCLUDE[d365fin](includes/d365fin_md.md)] manuelt eller automatisk. Der er flere oplysninger i næste procedure. Du kan også forbinde den nye indgående dokumentpost med eksisterende bogførte eller ikke-bogførte dokumenter, så kildefilen er nem at få adgang til fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Fremgangsmåde: Behandle indgående bilag](across-process-income-documents.md).

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Sådan oprettes en købsfaktura fra et elektronisk dokument, der er modtaget fra OCR-tjenesten
Følgende fremgangsmåde beskriver, hvordan du opretter en købsfakturapost fra en kreditorfaktura, der er modtaget som et elektronisk dokument fra OCR-tjenesten. Fremgangsmåden er den samme som, når du f.eks. opretter en finanskladdelinje fra en udgiftskvittering eller en salgsreturvareordre fra en kunde.

> [!NOTE]  
>   Felterne **Beskrivelse** og **Nummer** på de oprettede bilagslinjer udfyldes kun, hvis du først har tilknyttet tekst, der findes i OCR-dokumentet, til de to felter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan udføre denne tilknytning som varekrydsreferencer for dokumentlinjer af typen vare. Du kan også bruge funktionen Tilknytning af tekst til konto. Du kan finde yderligere oplysninger i afsnittet "Sådan tilknyttes tekst på et indgående dokument til en bestemt leverandør, finanskonto eller bankkonto".

Hvis du vil knytte varenumrene på bilaget til dine beskrivelser kreditorens varer, skal du åbne kortet for hver vare og derefter vælge handlingen **Varereferencer** for at oprette krydsreferencer mellem dine varebeskrivelser og kreditorens varer. Kan finde flere oplysninger i værktøjstippet til handlingen **Krydsreferencer** på varekort.

1. Vælg linjen for det indgående dokument, og vælg derefter handlingen **Opret dokument**.

Der oprettes en købsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)] baseret på oplysningerne i det elektroniske kreditordokument, du har modtaget fra OCR-tjenesten. Oplysningerne indsættes i feltet ny købsfaktura, der er baseret på den tilknytning, du har defineret som en krydsreference eller som en tilknytning mellem tekst og konto.

Enhver valideringsfejl, der typisk vedrører forkerte eller manglende stamdata i [!INCLUDE[d365fin](includes/d365fin_md.md)], vises i oversigtspanelet **Fejl og advarsler**. Du kan finde flere oplysninger i afsnittet "Sådan håndteres fejl ved modtagelse af elektroniske dokumenter".

### <a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a>Sådan knyttes tekst på et indgående dokument til en bestemt kreditorkonto
For indgående bilag kan du normalt bruge handlingen **Knyt tekst til konto** for at definere, at en bestemt tekst på en kreditorfaktura, som er modtaget fra OCR-tjenesten, er knyttet til en bestemt kreditorkonto. Fremover betyder enhver del af beskrivelsen af et indgående dokument, der findes som en tilknytningstekst, at feltet **Nr.** på resulterende bilags- eller kladdelinjer af typen Finanskonto udfyldes med den pågældende kreditor.

Ud over tilknytning til en kreditorkonto eller finanskonti kan du også knytte til en bankkonto. Dette er nyttigt, f.eks. ved elektroniske dokumenter for udgifter, der allerede er betalt, hvor du vil oprette en finanskladdelinje, der er klar til at blive bogført på en bankkonto.

1. Vælg den relevante indgående dokumentlinje, og vælg derefter handlingen **Knyt tekst til konto**. Vinduet **Tekst til kontotilknytning** åbnes.
3. I feltet **Koblingstekst** skal du angive enhver tekst, der opstår for kreditorfakturaer, som du ønsker at oprette købsdokumenter eller kladdelinjer for. Du kan angive op til 50 tegn.
4. I feltet **Kreditornummer** skal du angive den kreditor, som købsdokumentet eller kladden skal oprettes for.
5. I feltet **Debetkontonr.**, skal du angive den finanskonto af debettypen, der skal indsættes i det oprettede dokument eller den oprettede kladdelinje af typen Finanskonto.
6. I feltet **Kreditkontonr.**, skal du angive den finanskonto af kredittypen, der skal indsættes i det oprettede dokument eller den oprettede kladdelinje af typen Finanskonto.

    > [!NOTE]
    > Brug ikke felterne **Modkontokildetype** og **Modkontokildenr.** i forbindelse med indgående dokumenter. De bruges kun til afstemning af automatisk betaling. Du kan finde flere oplysninger under [Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

7. Gentag trin 2 til 5 for al tekst på indgående dokumenter, du automatisk vil oprette dokumenter til.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a>Sådan håndteres fejl ved modtagelse af elektroniske dokumenter
1. I vinduet **Indgående bilag** skal du vælge linjen for et elektronisk dokument, der er modtaget fra OCR-tjenesten med fejl. Det er angivet med værdien Fejl i feltet **OCR-status**.
2. Vælg handlingen **Rediger** for at åbne vinduet **Indgående bilag**.
3. På oversigtspanelet **Fejl og advarsler** skal du vælge meddelelsen og derefter vælge handlingen **Åbn relateret record**.
4. Vinduet med forkerte eller manglende data, såsom et kreditorkort med en manglende feltværdi, åbnes.
5. Ret fejlen eller fejlene, som beskrevet i hver fejlmeddelelse.
6. Fortsæt med at behandle det indgående elektroniske dokument ved vælge handlingen **Opret manuelt** igen.
7. Gentag trin 5 og 6 for de resterende fejl, indtil det elektroniske dokument kan modtages uden fejl.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a>Sådan lærer du OCR-tjenesten at undgå fejl
Da OCR er baseret på optiske registrering, er det sandsynligt, at OCR-tjenesten fortolker tegn i PDF- eller billedfilerne forkert, første gang programmet f.eks. behandler dokumenter fra en bestemt kreditor. Det fortolker muligvis virksomhedens logo som leverandørens navn eller fejlfortolker det samlede beløb på en kvittering på grund af layoutet. Hvis du vil undgå disse fejl fremover, skal du rette data modtaget af tjenesten OCR og derefter sende feedback til tjenesten.

Vinduet **Korrektion af OCR-data**, som du kan åbne fra vinduet **Indgående dokument**, indeholder felterne fra oversigtspanelet **Finansielle oplysninger** i to kolonner, én med OCR dataene, som kan redigeres, og én med OCR dataene skrivebeskyttet. Når du vælger knappen **Send OCR-feedback**, sendes indholdet af vinduet **Korrektion af OCR-data** til OCR tjenesten. Næste gang tjenesten behandler PDF eller billedfiler, der indeholder de pågældende data, inkorporeres dine rettelser for at undgå samme fejl.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.
2. Åbn en indgående dokumentpost, der indeholder data, som er modtaget fra OCR-tjenesten, og som du vil rette.
3. I vinduet **Indgående dokument** skal du vælge handlingen **Korrigér OCR-data**.
4. I feltet **Korrektion af OCR-data** skal du overskrive dataene i kolonnen, der kan redigeres, for hvert felt, der har en forkert værdi.
5. Du kan fortryde rettelser, du har foretaget, siden du åbnede vinduet **Korrektion af OCR-data**, ved at vælge handlingen **Nulstil OCR-data**.
6. For at sende rettelserne OCR-tjenesten skal du vælge handlingen **Send OCR-feedback**.
7. Hvis du vil gemme ændringerne, skal du lukke **Korrektion af OCR-data**-vinduet.

Felterne i oversigtspanelet **Finansielle oplysninger** i vinduet **Indgående dokument** opdateres med de nye værdier, du angav i trin 4.

## <a name="see-also"></a>Se også
[Behandle indgående bilag](across-process-income-documents.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

