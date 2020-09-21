---
title: Bruge OCR til at ændre PDF-filer til e-fakturaer | Microsoft Docs
description: Beskriver, hvordan du kan bruge en OCR-tjeneste til at omdanne indgående PDF- eller billedfiler til elektroniske dokumenter.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 9517f2bc0639959d06ce1baeaf7cf7489e3b5e63
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3777853"
---
# <a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter
Fra PDF-filer eller billedfiler, som du modtager fra dine handelspartnere, kan du få en ekstern OCR-tjeneste (Optical Character Recognition) til at oprette elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. F.eks. når du modtager en faktura i PDF-format fra en leverandør, kan du sende den til tjenesten OCR fra siden **Indgående bilag**. Dette beskrives i den første fremgangsmåde.

I stedet for at sende filen fra siden **Indgående bilag** kan du sende den til OCR-tjenesten via mail. Når du får det elektroniske dokument retur, oprettes der automatisk en relateret indgående bilagspost. Dette beskrives i den anden fremgangsmåde.

Efter nogle sekunder får du filen tilbage fra OCR-tjenesten som en elektronisk faktura, der kan konverteres til en købsfaktura til kreditoren. Dette beskrives i den tredje fremgangsmåde.

Da OCR er baseret på optiske registrering, er det sandsynligt, at OCR-tjenesten fortolker tegn i PDF- eller billedfilerne forkert, første gang programmet f.eks. behandler en bestemt kreditors dokumenter. Det fortolker muligvis virksomhedens logo som leverandørens navn eller fejlfortolker det samlede beløb på en kvittering på grund af layoutet. Hvis du vil undgå disse fejl fremover, kan du rette fejl i en separat version af siden **Indgående bilag**. Derefter sender du rettelserne til OCR-tjenesten for at lære den at fortolke de bestemte tegn korrekt, næste gang den behandler et PDF- eller billleddokument for samme kreditor. Du kan finde flere oplysninger i [Sådan lærer du OCR-tjenesten at undgå fejl](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Filtrafikken til og fra OCR-tjenesten afvikles af en dedikeret opgavekøpost, der oprettes automatisk, når du aktiverer den relaterede tjenesteforbindelse. Du kan finde flere oplysninger under [Konfigurere indgående bilag](across-how-setup-income-documents.md).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a>Sådan sendes en PDF- eller billedfil til OCR-tjenesten fra siden **Indgående bilag**
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Indgående bilag**, og vælg derefter det relaterede link.
2. Opret en ny indgående bilagspost, og vedhæft filen. Du kan finde flere oplysninger under [Oprette indgående bilagsposter](across-how-create-income-document-records.md).  
3. På siden **Indgående bilag** skal du vælge en eller flere linjer, og derefter skal du vælge handlingen **Send til opgavekø**.

    Værdien i feltet **OCR-status** ændres til **Klar**. Den vedhæftede PDF- eller billedfil bliver sendt til OCR-tjenesten af opgavekøen i henhold til planen, forudsat at der ikke er nogen fejl.
4. Alternativt skal du på siden **Indgående bilag** vælge en eller flere linjer, og derefter skal du vælge handlingen **Send til OCR-tjeneste**.

Værdien i feltet **OCR-status** ændres til **Sendt**, forudsat at der ikke er nogen fejl.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>Sådan sendes en PDF- eller billedfil til OCR-tjenesten via mail
Brug dit mailprogram til at sende en mail til OCR-tjenesteudbyderen med PDF- eller billedfilen vedhæftet. Du kan finde oplysninger om, hvilken mailadresse du skal sende til, på OCR-tjenesteudbyderens websted.

Da der ikke findes nogen indgående bilagsposter for filen, oprettes der automatisk en ny post på siden **Indgående bilag**, når du modtager det elektronisk oprettede dokument fra OCR-tjenesten. Du kan finde flere oplysninger under [Oprette indgående bilagsposter](across-how-create-income-document-records.md).

> [!NOTE]  
>   Hvis du arbejder på en tablet eller telefon, kan du sende filen til OCR-tjenesten, så snart du har taget et billede af bilaget, eller du kan oprette et indgående bilag direkte. Du kan finde flere oplysninger under [Sådan opretter du en indgående bilagspost ved at tage et billede](across-how-create-income-document-records.md#to-create-an-incoming-document-record-by-taking-a-photo).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>Sådan modtager du det resulterende elektroniske dokument fra OCR-tjenesten
Det elektroniske dokument, der oprettes af OCR-tjenesten fra PDF eller billedfilen, modtages automatisk på siden **Indgående bilag** ved den opgavekøpost, som er oprettet, når du aktiverer OCR-tjenesten.

Hvis du ikke bruger en opgavekø, eller du skal have et færdigt OCR-dokument hurtigere end opgavekøplanen angiver, kan du vælge knappen **Modtag fra OCR-tjeneste**. På denne måde vises alle dokumenter, der er udført af OCR-tjenesten.

> [!NOTE]  
>   Hvis OCR-tjenesten er indstillet til at kræve manuel verifikation af behandlede dokumenter, indeholder feltet **OCR-status** **Afventer bekræftelse**. I så fald skal du gøre følgende for at logge på OCR-tjenestens websted for at verificere OCR-dokumentet manuelt.

1. I feltet **OCR-status** skal du vælge hyperlinket **Afventer bekræftelse**.
2. Log på med legitimationsoplysningerne for din OCR-tjenestekonto på webstedet for OCR-tjenesten. Dette er de legitimationsoplysninger, du brugte, da du konfigurerede tjenesten. Du kan finde flere oplysninger i [Sådan konfigureres en OCR-tjeneste](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

    Oplysninger om OCR-dokumentet vises med både kildeindholdet fra PDF- eller billedfilen og de resulterende OCR-feltværdier.
3. Gennemgå forskellige feltværdierne, og rediger eller angiv værdier manuelt i de felter, som OCR-tjenesten har kodet som usikre.
4. Vælg knappen **OK**. OCR-processen fuldføres, og det resulterende elektroniske dokument sendes til siden **Indgående bilag** i [!INCLUDE[d365fin](includes/d365fin_md.md)] i overensstemmelse med opgavekøplanen.
5. Gentag trin 4 for andre OCR-dokumenter der skal bekræftes.

Nu kan du fortsætte med at oprette dokumentposter for de modtagne elektroniske dokumenter i [!INCLUDE[d365fin](includes/d365fin_md.md)] manuelt eller automatisk. Der er flere oplysninger i næste procedure. Du kan også forbinde den nye indgående bilagspost med eksisterende bogførte eller ikke-bogførte bilag, så kildefilen er nem at få adgang til fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Fremgangsmåde: Behandle indgående bilag](across-process-income-documents.md).

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Sådan oprettes en købsfaktura fra et elektronisk dokument, der er modtaget fra OCR-tjenesten
Følgende fremgangsmåde beskriver, hvordan du opretter en købsfakturapost fra en kreditorfaktura, der er modtaget som et elektronisk dokument fra OCR-tjenesten. Fremgangsmåden er den samme som, når du f.eks. opretter en finanskladdelinje fra en udgiftskvittering eller en salgsreturvareordre fra en kunde.

> [!NOTE]  
>   Felterne **Beskrivelse** og **Nummer** på de oprettede bilagslinjer udfyldes kun, hvis du først har tilknyttet tekst, der findes i OCR-dokumentet, til de to felter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan udføre denne tilknytning som varekrydsreferencer for dokumentlinjer af typen vare. Du kan finde flere oplysninger i [Bruge varereferencer](inventory-how-use-item-cross-refs.md). Du kan også bruge funktionen Tilknytning af tekst til konto. Du kan finde yderligere oplysninger i [Sådan tilknyttes tekst på et indgående bilag til en bestemt leverandør, finanskonto eller bankkonto](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Vælg linjen for det indgående bilag, og vælg derefter handlingen **Opret dokument**.

Der oprettes en købsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)] baseret på oplysningerne i det elektroniske kreditordokument, du har modtaget fra OCR-tjenesten. Oplysningerne indsættes i feltet ny købsfaktura, der er baseret på den tilknytning, du har defineret som en krydsreference eller som en tilknytning mellem tekst og konto.

Enhver valideringsfejl, der typisk vedrører forkerte eller manglende stamdata i [!INCLUDE[d365fin](includes/d365fin_md.md)], vises i oversigtspanelet **Fejl og advarsler**. Du kan finde flere oplysninger i [Sådan håndteres fejl ved modtagelse af elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### <a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a>Sådan knyttes tekst på et indgående bilag til en bestemt kreditorkonto
For indgående bilag kan du normalt bruge handlingen **Knyt tekst til konto** for at definere, at en bestemt tekst på en kreditorfaktura, som er modtaget fra OCR-tjenesten, er knyttet til en bestemt kreditorkonto. Fremover betyder enhver del af beskrivelsen af et indgående bilag, der findes som en tilknytningstekst, at feltet **Nr.** på resulterende bilags- eller kladdelinjer af typen Finanskonto udfyldes med den pågældende kreditor.

Ud over tilknytning til en kreditorkonto eller finanskonti kan du også knytte til en bankkonto. Dette er nyttigt, f.eks. ved elektroniske dokumenter for udgifter, der allerede er betalt, hvor du vil oprette en finanskladdelinje, der er klar til at blive bogført på en bankkonto.

1. Vælg den relevante indgående bilagslinje, og vælg derefter handlingen **Knyt tekst til konto**. Siden **Tekst til kontotilknytning** åbnes.
3. I feltet **Koblingstekst** skal du angive enhver tekst, der opstår for kreditorfakturaer, som du ønsker at oprette købsdokumenter eller kladdelinjer for. Du kan angive op til 50 tegn.
4. I feltet **Kreditornummer** skal du angive den kreditor, som købsdokumentet eller kladden skal oprettes for.
5. I feltet **Debetkontonr.**, skal du angive den finanskonto af debettypen, der skal indsættes i det oprettede dokument eller den oprettede kladdelinje af typen Finanskonto.
6. I feltet **Kreditkontonr.**, skal du angive den finanskonto af kredittypen, der skal indsættes i det oprettede dokument eller den oprettede kladdelinje af typen Finanskonto.

    > [!NOTE]
    > Brug ikke felterne **Modkontokildetype** og **Modkontokildenr.** i forbindelse med indgående bilag. De bruges kun til afstemning af automatisk betaling. Du kan finde flere oplysninger under [Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

7. Gentag trin 2 til 5 for al tekst på indgående bilag, du automatisk vil oprette bilag til.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a>Sådan håndteres fejl ved modtagelse af elektroniske dokumenter
1. På siden **Indgående bilag** skal du vælge linjen for et elektronisk dokument, der er modtaget fra OCR-tjenesten med fejl. Det er angivet med værdien Fejl i feltet **OCR-status**.
2. Vælg handlingen **Rediger** for at åbne siden **Indgående bilag**.
3. På oversigtspanelet **Fejl og advarsler** skal du vælge meddelelsen og derefter vælge handlingen **Åbn relateret record**.
4. Siden med forkerte eller manglende data, såsom et kreditorkort med en manglende feltværdi, åbnes.
5. Ret fejlen eller fejlene, som beskrevet i hver fejlmeddelelse.
6. Fortsæt med at behandle det indgående elektroniske dokument ved vælge handlingen **Opret manuelt** igen.
7. Gentag trin 5 og 6 for de resterende fejl, indtil det elektroniske dokument kan modtages uden fejl.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a>Sådan lærer du OCR-tjenesten at undgå fejl
Da OCR er baseret på optiske registrering, er det sandsynligt, at OCR-tjenesten fortolker tegn i PDF- eller billedfilerne forkert, første gang programmet f.eks. behandler dokumenter fra en bestemt kreditor. Det fortolker muligvis virksomhedens logo som leverandørens navn eller fejlfortolker det samlede beløb på en kvittering på grund af layoutet. Hvis du vil undgå disse fejl fremover, skal du rette data modtaget af tjenesten OCR og derefter sende feedback til tjenesten.

Siden **Korrektion af OCR-data**, som du kan åbne fra siden **Indgående bilag**, indeholder felterne fra oversigtspanelet **Finansielle oplysninger** i to kolonner, én med OCR dataene, som kan redigeres, og én med OCR dataene skrivebeskyttet. Når du vælger knappen **Send OCR-feedback**, sendes indholdet af siden **Korrektion af OCR-data** til OCR tjenesten. Næste gang tjenesten behandler PDF eller billedfiler, der indeholder de pågældende data, inkorporeres dine rettelser for at undgå samme fejl.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Indgående bilag**, og vælg derefter det relaterede link.
2. Åbn en indgående bilagspost, der indeholder data, som er modtaget fra OCR-tjenesten, og som du vil rette.
3. På siden **Indgående bilag** skal du vælge handlingen **Korrigér OCR-data**.
4. På siden **Korrektion af OCR-data** skal du overskrive dataene i kolonnen, der kan redigeres, for hvert felt, der har en forkert værdi.
5. Du kan fortryde rettelser, du har foretaget, siden du åbnede siden **Korrektion af OCR-data**, ved at vælge handlingen **Nulstil OCR-data**.
6. For at sende rettelserne OCR-tjenesten skal du vælge handlingen **Send OCR-feedback**.
7. Hvis du vil gemme ændringerne, skal du lukke **Korrektion af OCR-data**-siden.

Felterne i oversigtspanelet **Finansielle oplysninger** på siden **Indgående bilag** opdateres med de nye værdier, du angav i trin 4.

## <a name="see-also"></a>Se også
[Behandle indgående bilag](across-process-income-documents.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
