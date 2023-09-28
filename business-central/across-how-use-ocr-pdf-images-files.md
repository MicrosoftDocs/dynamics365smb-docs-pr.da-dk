---
title: Bruge OCR til at ændre PDF-filer til e-fakturaer
description: 'Beskriver, hvordan du kan bruge en OCR-tjeneste til at omdanne indgående PDF- eller billedfiler til elektroniske dokumenter.'
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
---
# Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter

Fra PDF-filer eller billedfiler, som du modtager fra dine handelspartnere, kan du få en ekstern OCR-tjeneste (Optical Character Recognition) til at oprette elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)]. F.eks. når du modtager en faktura i PDF-format fra en leverandør, kan du [sende den til tjenesten OCR fra siden **Indgående bilag**](#to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page).

I stedet for at sende filen fra siden **Indgående bilag** kan OCR-tjenesten tilbyde funktionen til at [behandle de filer, der videresendes til de dedikeret e-mailadresse](#to-send-a-pdf-or-image-file-to-the-ocr-service-by-email). Når du får det elektroniske dokument retur, oprettes der automatisk en relateret indgående bilagspost i [!INCLUDE[prod_short](includes/prod_short.md)].

Efter nogle sekunder sender OCR-tjenesten den behandlede fil til siden med **Indgående bilag** som en elektronisk dokument post, der kan [konverteres til en købsfaktura for kreditoren](#to-receive-the-resulting-electronic-document-from-the-ocr-service), en salgsfaktura, kreditnota eller en journaloptegnelse.

Da OCR er baseret på optiske registrering, er det sandsynligt, at OCR-tjenesten fortolker tegn i PDF- eller billedfilerne forkert, første gang programmet f.eks. behandler en bestemt kreditors dokumenter. Det fortolker muligvis virksomhedens logo som leverandørens navn eller fejlfortolker det samlede beløb på en kvittering på grund af layoutet. Hvis du vil undgå disse fejl fremover, kan du rette fejl i en separat version af siden **Indgående bilag**. Derefter sender du rettelserne til OCR-tjenesten for at lære den at fortolke de bestemte tegn og felter korrekt, næste gang den behandler et PDF- eller billeddokument for samme kreditor. Du kan finde flere oplysninger i [Træning af OCR-tjenesten til at undgå fejl](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Trafikken i filer til og fra OCR-tjenesten behandles af en dedikeret opgavekøpost. Denne opgavekø oprettes automatisk, når du aktiverer den eksterne OCR-tjenesteforbindelse. Du kan finde flere oplysninger i [Konfigurere indgående bilag](across-how-setup-income-documents.md).

> [!NOTE]
> OCR-funktionen leveres af eksterne udbydere. Vælg en servicepakke, der passer til din organisation og/eller dit land/område. Find tjenester, der er kompatible med [!INCLUDE[prod_short](includes/prod_short.md)], og oplysninger om tilgængelige funktioner på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## Sådan sendes en PDF- eller billedfil til OCR-tjenesten fra siden Indgående bilag

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Indgående bilag** og derefter vælge det relaterede link.
2. Opret en ny indgående bilagspost, og vedhæft filen. Du kan finde flere oplysninger i [Oprette indgående bilagsposter](across-how-create-income-document-records.md).  
3. På siden **Indgående bilag** skal du vælge en eller flere linjer, og derefter skal du vælge handlingen **Send til opgavekø**.

   Værdien i feltet **OCR-status** ændres til **Klar**. Den vedhæftede PDF- eller billedfil bliver sendt til OCR-tjenesten af opgavekøen i henhold til planen, forudsat at der ikke er nogen fejl.
4. Alternativt skal du på siden **Indgående bilag** vælge en eller flere linjer, og derefter skal du vælge handlingen **Send til OCR-tjeneste** for øjeblikkeligt at sende filer til behandling.

   Værdien i feltet **OCR-status** ændres til **Sendt**, forudsat at der ikke er nogen fejl.

## Sådan sendes en PDF- eller billedfil til OCR-tjenesten via mail

Brug dit mailprogram til at videresende en mail til OCR-tjenesteudbyderen med PDF- eller billedfilen vedhæftet. Du kan finde oplysninger om, hvilken mailadresse du skal sende til, på OCR-tjenesteudbyderens websted.

Da der ikke findes nogen indgående bilagsposter for filen, oprettes der automatisk en ny post på siden **Indgående bilag**, når OCR-tjenesten sender det elektronisk oprettede dokument fra OCR-tjenesten. Du kan finde flere oplysninger i [Oprette indgående bilagsposter](across-how-create-income-document-records.md).

> [!NOTE]  
> Hvis du arbejder på en tablet eller telefon, kan du sende filen til OCR-tjenesten, så snart du har taget et billede af bilaget, eller du kan oprette et indgående bilag direkte. Du kan finde flere oplysninger i [Oprette en indgående bilagspost ved at tage et billede](across-how-create-income-document-records.md#create-an-incoming-document-record-by-taking-a-photo).

## Sådan modtager du det resulterende elektroniske dokument fra OCR-tjenesten

Det elektroniske dokument, der oprettes af OCR-tjenesten fra PDF eller billedfilen, modtages automatisk på siden **Indgående bilag** ved den opgavekøpost, som er oprettet, når du aktiverer OCR-tjenesten.

Hvis du ikke bruger en opgavekø, eller du skal have et færdigt OCR-dokument hurtigere end opgavekøplanen angiver, kan du vælge handlingen **Modtag fra OCR-tjeneste**. Denne funktion kan vise alle dokumenter, der er udført af OCR-tjenesten.

> [!NOTE]  
> Hvis OCR-tjenesten er indstillet til at kræve manuel verifikation af behandlede dokumenter, indeholder feltet **OCR-status** **Afventer bekræftelse**. I så fald skal du gøre følgende for at logge på OCR-tjenestens websted for at verificere OCR-dokumentet manuelt.

1. I feltet **OCR-status** skal du vælge hyperlinket **Afventer bekræftelse**.
2. Log på med legitimationsoplysningerne for din OCR-tjenestekonto på webstedet for OCR-tjenesten. Du kan finde flere oplysninger i [Konfigurere en OCR-tjeneste](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

   Oplysninger om OCR-dokumentet vises med både kildeindholdet fra PDF- eller billedfilen og de resulterende OCR-feltværdier.
3. Gennemgå feltværdierne, og rediger eller angiv værdier manuelt i de felter, som OCR-tjenesten har kodet som usikre.
4. Vælg knappen **OK**. OCR-processen fuldføres, og det resulterende elektroniske dokument sendes til siden **Indgående bilag** i [!INCLUDE[prod_short](includes/prod_short.md)] i overensstemmelse med opgavekøplanen.
5. Gentag trin 2 til 4 for andre OCR-dokumenter der skal bekræftes.

Nu kan du fortsætte med at oprette dokumentposter for de modtagne elektroniske dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)] manuelt eller automatisk. Der er flere oplysninger i næste procedure. Du kan også [forbinde den nye indgående bilagspost med eksisterende bogførte eller ikke-bogførte bilag](across-how-connect-disconnect-income-document-records.md), så kildefilen er nem at få adgang til fra [!INCLUDE[prod_short](includes/prod_short.md)].

## Sådan oprettes en købsfaktura fra et elektronisk dokument, der er modtaget fra OCR-tjenesten

Følgende fremgangsmåde beskriver, hvordan du opretter en købsfakturapost fra en kreditorfaktura, der er modtaget som et elektronisk dokument fra OCR-tjenesten. Fremgangsmåden er den samme som, når du f.eks. opretter en finanskladdelinje fra en udgiftskvittering eller en salgsreturvareordre fra en kunde.

> [!NOTE]  
> Felterne **Beskrivelse** og **Nummer** på de oprettede bilagslinjer udfyldes kun, hvis du først har tilknyttet tekst, der findes i OCR-dokumentet, til de to felter i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan udføre denne tilknytning som varereferencer for dokumentlinjer af typen vare. Du kan finde flere oplysninger i [Bruge varereferencer](inventory-how-use-item-cross-refs.md). Du kan også bruge funktionen **Tilknytning af tekst til konto**. Du kan finde yderligere oplysninger i [Tilknytte tekst på et indgående bilag til en bestemt leverandør, finanskonto eller bankkonto](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Vælg linjen for det indgående bilag, og vælg derefter handlingen **Opret dokument**.

Der oprettes en købsfaktura i [!INCLUDE[prod_short](includes/prod_short.md)] baseret på oplysningerne i det elektroniske kreditordokument, du har modtaget fra OCR-tjenesten. Oplysningerne indsættes i feltet ny købsfaktura, der er baseret på den tilknytning, du har defineret som en reference eller som en tilknytning mellem tekst og konto.

Enhver valideringsfejl, der typisk vedrører forkerte eller manglende data i [!INCLUDE[prod_short](includes/prod_short.md)], vises i oversigtspanelet **Fejl og advarsler**. Du kan finde flere oplysninger i [Håndtere fejl ved modtagelse af elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### Sådan knyttes tekst på et indgående bilag til en bestemt kreditorkonto

For indgående bilag kan du normalt bruge handlingen **Knyt tekst til konto** for at definere, at en bestemt tekst på en kreditorfaktura, som er modtaget fra OCR-tjenesten, er knyttet til en bestemt kreditorkonto. Fremover skal en del af den indgående bilags beskrivelse, der findes som en tilknytnings tekst, betyder, at feltet **Leverandørnr.** på dokument-eller kladdelinjer af typen *Finanskonto* udfyldes med den pågældende kreditor.

Ud over tilknytning til en kreditorkonto eller finanskonti kan du også knytte tekst til en bankkonto. Dette funktion er nyttig, f.eks. ved elektroniske dokumenter for udgifter, der allerede er betalt, hvor du vil oprette en finanskladdelinje, der er klar til at blive bogført på en bankkonto.

1. Vælg den relevante indgående bilagslinje, og vælg derefter handlingen **Knyt tekst til konto**. Siden **Tekst til kontotilknytning** åbnes.
2. I feltet **Koblingstekst** skal du angive enhver tekst, der opstår for kreditorfakturaer, som du ønsker at oprette købsdokumenter eller kladdelinjer for. Du kan angive op til 50 tegn.
3. I feltet **Kreditornummer** skal du angive den kreditor, som købsdokumentet eller kladden skal oprettes for.
4. I feltet **Debetkontonr.**, skal du angive den finanskonto af debettypen, der skal indsættes i det oprettede dokument eller den oprettede kladdelinje af typen Finanskonto.
5. I feltet **Kreditkontonr.**, skal du angive den finanskonto af kredittypen, der skal indsættes i det oprettede dokument eller den oprettede kladdelinje af typen Finanskonto.

   > [!NOTE]
   > Brug ikke felterne **Modkontokildetype** og **Modkontokildenr.** i forbindelse med indgående bilag. De bruges kun til afstemning af automatisk betaling. Du kan finde flere oplysninger i [Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
6. Gentag trin 2 til 5 for al tekst på indgående bilag, du automatisk vil oprette bilag til.

## Sådan håndteres fejl ved modtagelse af elektroniske dokumenter

1. På siden **Indgående bilag** skal du vælge linjen for et elektronisk dokument, der er modtaget fra OCR-tjenesten med fejl, der angives ved værdien *Fejl* i feltet **OCR Status**.
2. Vælg handlingen **Rediger** for at åbne siden **Indgående bilag**.
3. På oversigtspanelet **Fejl og advarsler** skal du vælge meddelelsen og derefter vælge handlingen **Åbn relateret record**.
4. Siden med forkerte eller manglende data, såsom et kreditorkort med en manglende feltværdi, åbnes.
5. Ret fejlen eller fejlene, som beskrevet i hver fejlmeddelelse.
6. Fortsæt med at behandle det indgående elektroniske dokument ved vælge handlingen **Opret manuelt** igen.
7. Gentag trin 5 og 6 for de resterende fejl, indtil det elektroniske dokument kan modtages uden fejl.

## Sådan lærer du OCR-tjenesten at undgå fejl

Da OCR er baseret på optiske registrering, kan OCR-tjenesten fortolke tegn forkert i PDF- eller billedfilerne forkert, første gang programmet f.eks. behandler dokumenter fra en bestemt kreditor. Det fortolker muligvis virksomhedens logo som leverandørens navn eller fejlfortolker det samlede beløb på en kvittering på grund af layoutet. Hvis du vil undgå disse fejl fremover, skal du rette data modtaget af tjenesten OCR og derefter sende feedback til tjenesten.

Siden **Korrektion af OCR-data**, som du kan åbne fra siden **Indgående bilag**, indeholder felterne fra oversigtspanelet **Finansielle oplysninger** i to kolonner, én med OCR dataene, som kan redigeres, og én med OCR dataene skrivebeskyttet. Når du vælger knappen **Send OCR-feedback**, sendes indholdet af siden **Korrektion af OCR-data** til OCR tjenesten. Næste gang tjenesten behandler PDF eller billedfiler, der indeholder de pågældende data, inkorporeres dine rettelser for at forbedre dokumentgenkendelsen.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Indgående bilag** og derefter vælge det relaterede link.
2. Åbn en indgående bilagspost, der indeholder data, som er modtaget fra OCR-tjenesten, og som du vil rette.
3. På siden **Indgående bilag** skal du vælge handlingen **Korrigér OCR-data**.
4. På siden **Korrektion af OCR-data** skal du overskrive dataene i kolonnen, der kan redigeres, for hvert felt, der har en forkert værdi.
5. Du kan fortryde rettelser, du har foretaget, siden du åbnede siden **Korrektion af OCR-data**, ved at vælge handlingen **Nulstil OCR-data**.
6. For at sende rettelserne OCR-tjenesten skal du vælge handlingen **Send OCR-feedback**.
7. Hvis du vil gemme ændringerne, skal du lukke **Korrektion af OCR-data**-siden.

Felterne i oversigtspanelet **Finansielle oplysninger** på siden **Indgående bilag** opdateres med de nye værdier, du angav i trin 4.

## Se også

[Oprette indgående bilagsposter](across-how-create-income-document-records.md)
[Oprette indgående bilagsposter direkte fra dokumenter og poster](across-how-connect-disconnect-income-document-records.md)
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
