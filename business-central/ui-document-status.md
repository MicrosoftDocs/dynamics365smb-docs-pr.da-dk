---
title: Statusfelt i dokumenter
description: 'Få mere at vide om status "åben" og "frigivet" for tilbuds-, ordre-eller kreditnotadokumenter.'
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,'
ms.search.form: null
ms.date: 09/19/2022
ms.author: bholtorf
---
# <a name="status-field-on-documents"></a><a name="status-field-on-documents"></a><a name="status-field-on-documents"></a>Statusfelt i dokumenter

Når du opretter et tilbud, en ordre eller en kreditnota, indeholder feltet **Status** i dokumenthovedet som standard statusangivelsen **Åben**.

Når du har udfyldt dokumentet, kan du frigive det, hvorefter [!INCLUDE[prod_short](includes/prod_short.md)] ændrer værdien i feltet **Status** til **Frigivet**. Denne status angiver, at ordren er klar til næste trin i behandlingsprocessen, før den skal bogføres.

| Status | Beskrivelse |
| ------ | ----------- |
| Åben   | At du kan ændre i dokumentet. |
| Frigivet | At dokumentet er frigivet til næste fase i behandlingen, og at du ikke kan ændre linjer af typen *Vare* og *Anlæg*.<br /><br />Du kan åbne et frigivet dokument igen, hvis du vil ændre dets indhold. Du skal frigive dokumentet igen for at flytte de ændrede dokumenter til næste fase i behandlingen. |
| Afventer godkendelse   | At dokumentet venter på at blive godkendt. |
| Afventer forudbetaling | Der er bogført en forudbetalingsfaktura for dokumentet. |

## <a name="release-process"></a><a name="release-process"></a><a name="release-process"></a>Frigivelsesproces

Du kan bruge frigivelsesproceduren til at lette forskellige normale arbejdsprocesser, f.eks. til at følge virksomhedens godkendelsesprocedurer eller starte lageraktiviteter.

### <a name="approval-procedures"></a><a name="approval-procedures"></a><a name="approval-procedures"></a>Godkendelsesprocedurer

Virksomheden kan bruge frigivelsesproceduren til at angive, at en anden bruger har godkendt dokumentet, eller at en ekstern kontaktperson kan opfylde specifikationerne i dokumentet, som vist i følgende eksempler:

* Du kan kun frigive en købsordre, hvis leverandøren har erklæret sig indforstået med at eksekvere ordren.
* Du skal oprette en ordre, og en anden bruger skal af sikkerhedsmæssige årsager godkende den, før du må frigive den.
* Den leder, der er ansvarlig for at godkende alle tilbagebetalinger, skal frigive en kreditnota, du har oprettet.

Få mere at vide om godkendelsesarbejdsgange ved hjælp af [arbejdsprocesser](across-use-workflows.md).

### <a name="warehouse-activities"></a><a name="warehouse-activities"></a><a name="warehouse-activities"></a>Lageraktiviteter

Hvis ordrestatus er **Åben**, vil lagerstedet hverken begynde at forberede leveringen eller forvente at modtage varerne på en købsordre. Når du frigiver ordren, angiver du, at ordren er færdiggjort, og at lagerstedet kan medtage den i sine aktiviteter.

## <a name="reopen-a-released-order"></a><a name="reopen-a-released-order"></a><a name="reopen-a-released-order"></a>Genåbne en frigivet ordre

Du kan foretage ændringer i en frigivet ordre ved at åbne den igen. Du kan imidlertid kun øge antallet på de linjer, der allerede er behandlet af lagerstedet.

Når du har foretaget ændringerne og igen frigiver ordren, genberegner [!INCLUDE [prod_short](includes/prod_short.md)] moms og rabatter på det fakturerede beløb.

Hvis du ændrer en frigivet ordre, skal du give lagerstedet besked om ændringerne.

> [!NOTE]
> Hvis du vil bogføre en enkelt åben ordre eller en kreditnota uden at frigive den først, udgiver [!INCLUDE [prod_short](includes/prod_short.md)] automatisk dokumentet, når du bogfører det. Hvis du bogfører ordrer eller kreditnotaer vha. funktionen **Massebogfør**, kan du vælge kun at bogføre de ordrer eller kreditnotaer, du har frigivet.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Sælge produkter med en debitorsalgsordre](sales-how-sell-products.md)  
[Registrere køb med købsfakturaer](purchasing-how-record-purchases.md)  
[Afsende varer](warehouse-how-ship-items.md)  
[Modtage varer](warehouse-how-receive-items.md)  
[Bruge godkendelsesworkflows](across-how-use-approval-workflows.md)  
[Sortering af, søgning i og filtrering af lister](ui-enter-criteria-filters.md)  
[Arkivere dokumenter](across-how-to-archive-documents.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
