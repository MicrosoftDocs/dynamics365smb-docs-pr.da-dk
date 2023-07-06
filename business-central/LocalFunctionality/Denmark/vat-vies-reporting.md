---
title: 'Momsindberetning [DK]'
description: Du kan oprette de nødvendige momsopgørelser for vare- eller tjenestefiler i en dansk version ved hjælp af rapporten Oversigt over EU-salg.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: null
ms.date: 05/09/2022
ms.author: edupont
---
# <a name="vat-vies-reporting-in-the-danish-version"></a><a name="vat-vies-reporting-in-the-danish-version"></a><a name="vat-vies-reporting-in-the-danish-version"></a>Momslisterapportering i den danske version

Danske virksomheder skal angive moms af handel med varer eller tjenesteydelser med andre EU-lande/områder. Du kan oprette den ønskede fil ved hjælp af kørslen rapporten **Oversigt over EU-salg**.  

## <a name="set-up-vat-registration-numbers"></a><a name="set-up-vat-registration-numbers"></a><a name="set-up-vat-registration-numbers"></a>Konfigurere Momsregistreringsnumre

Hvis du vil rapportere momsangivelser korrekt, skal du angive et almindeligt momsregistreringsnummer i feltet **Momsregistreringsnummer** på kortene **Debitor** og **Kreditor**. Det betyder, at du ikke kan tilføje landekoder eller andre genveje, da momsregistreringsrapporten kræver almindeligt momsnummer for klienter. Den er forskelligt for Intrastat, så du kan konfigurere præcis, hvordan momsregistreringsnumre skal oprettes til Intrastat på siden **Intrastat, Opsætning**. Du kan finde flere oplysninger i [Konfigurere momsregistreringsnummer for Intrastat](vat-registration-no-intrastat.md).  

## <a name="reporting-eu-sales"></a><a name="reporting-eu-sales"></a><a name="reporting-eu-sales"></a>Rapportering af salg til EU

Hvis du vil registrere moms af handel med varer eller tjenesteydelser mellem EU-lande/områder, skal du indberette oplysninger om denne handel til det danske listesystem. Rapporten **Oversigt over EU-salg** opretter en fil, som du derefter kan overføre til Told og skat på [www.skat.dk](https://go.microsoft.com/fwlink/?LinkId=212340)-websiden. Inden du opretter filen, kan du kontrollere dine kunders CVR-nummer online. SKAT anbefaler også, at du ikke sender store filer til onlineportalen. Hvis din indberetning består af mere end 1.000 linjer, anbefales det, at du sender flere mindre filer i stedet. Du kan finde flere oplysninger på SKATs [websted](https://www.skat.dk).  

[!INCLUDE [finance-ecsaleslist](../../includes/finance-ecsaleslist.md)]

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Om rapporten Oversigt over EU-salg](../../finance-how-report-vat.md#ecsaleslist)  
[Rapportere moms til skattemyndighederne](../../finance-how-report-vat.md)  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Udskrive rapporter til afstemning af moms](how-to-print-vat-reconciliation-reports.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
