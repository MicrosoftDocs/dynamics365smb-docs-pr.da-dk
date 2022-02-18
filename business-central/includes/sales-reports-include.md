---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f25e82f8276715d8d5e945bd5d6a309e12502f8e
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104064"
---
I følgende tabel beskrives nogle af nøglerapporterne i salgsapporter.

|Report |Objekt-id|Beskrivlse  |
|---------|---------|---------|
|**Debitor - ordreoversigt**|107| Viser ordrebeholdningen med ikke-leveret antal pr. debitor i tre perioder á 30 dage med udgangspunkt i en valgt dato. Der vises desuden kolonner med ordrer, der skal leveres før og efter de tre perioder, og en kolonne med ordrebeholdningen pr. debitor i alt. Rapporten kan f.eks. bruges til at analysere virksomhedens forventede omsætning. |
|**Debitor - top 10-liste**|111| Viser oplysninger om debitorers køb og saldo inden for en valgt periode. Du kan angive antallet af debitorer, der skal med i rapporten. Kun de debitorer, der har køb i løbet af perioden eller saldo ved periodens afslutning, vil blive vist i rapporten.<br>Debitorerne sorteres efter beløbsstørrelsen, og du kan vælge, om de skal sorteres efter salg eller saldo. Rapporten giver et hurtigt overblik over, hvilke kunder der køber mest eller skylder mest.|
|**Kunde/varestatistik**|113|Viser en oversigt over salg i den valgte periode for hver debitor. Rapporten viser oplysninger om antal, salgsbeløb, avance og eventuel rabat. Du kan f.eks. bruge rapporten til at analysere kundegrupper.|
|**Lagerbeholdning - kundesalg**|713|En oversigt fra lagerstedets synspunkt. Dette er en anden visning, der sammenlignes med rapporten **Debitor/varesalg** og viser varen først og derefter den kunde, der har købt produktet.|
|**Debitor - salgsliste**|119|Viser debitorsalg for en periode. Rapporten bruges til Told Skat. Du kan vælge kun at medtage debitorer med et samlet salg, der overstiger et bestemt beløb. Du kan også angive, om rapporten skal vise adresseoplysningerne for hver enkelt debitor.<br>Rapporten er baseret på det rapporterede salg (RV) fra debitorposter. Nederst i rapporten vises det samlede rapporterede salg i RV. Det samlede beløb er baseret på de debitorer, der er medtaget i rapporten, dvs. de debitorer, der er filtreret på i oversigtspanelet Debitor, og som har et samlet salg, der er større end det beløb, der er angivet i feltet **Beløb (RV) større end** i oversigtspanelet **Indstillinger**.|
|**Debitor - saldo til dato**|121|Viser detaljerede saldooplysninger for udvalgte debitorer. Brug f.eks. rapporten ved afslutningen af en regnskabsperiode eller ved årsafslutningen.|
|**Debitor - balance**|129|Viser detaljerede saldooplysninger for udvalgte debitorer. Du kan bruge rapporten til at bekræfte, at saldoen for en debitorbogføringsgruppe svarer til saldoen på den tilsvarende finanskonto på en bestemt dato. Brug f.eks. rapporten ved afslutningen af en regnskabsperiode eller ved årsafslutningen. Hvis du har brug for en mere detaljeret version af denne type rapport, skal du bruge rapporten **Debitor - Detaljeret råbalance** (104).|
|**Salgsstatistik**|112|[!INCLUDE [reports-sales-statistics](reports-sales-statistics.md)] |
|**Disp. salgsreservation**|209|Viser, hvilke varer der er disponible til levering på salgsdokumentet. Du angiver, om rapporten skal vise status på hvert dokument eller på hver salgslinje. Når du udskriver rapporten, kan du automatisk få indsat det antal, der kan leveres, i feltet **Afsend (antal)** på salgslinjerne. Herefter kan rapporten bruges til at afgøre, hvilke dokumenter der skal bogføres.<br>Der er også en egenskab, som du kan bruge til at angive det antal varer, der skal leveres. **Bemærk**: Denne funktionalitet er ikke tilgængelig for avancerede lagerfunktioner.|
|**Lagerleverancestatus**|7313|Rapporten kan bruges til alle lokationer, hvor **Påkrævede forsendelser** er aktiveret. **Lagerleverancestatus**-rapporten viser alle ikke-bogførte lagerleverancedokumenter, herunder lokationer, placeringskoder, dokument status, antal osv. Denne rapport er perfekt til at få overblik.|
|**Plukliste (lager)**|813|Viser en oversigt over de salgsordrer, en vare indgår i. Der vises følgende oplysninger om hver vare: salgsordrelinje med debitors navn, variantkode, lokationskode, placeringskode, afsendelsesdato, antal til levering og enhed. Antallet lægges sammen for hver vare. Rapporten kan f.eks. bruges, når der skal hentes varer fra lageret.<br>**Bemærk**: Denne funktionalitet er ikke tilgængelig for avancerede lagerfunktioner.|
|**Vare - restordrer til kunder**|718|Viser en oversigt med de ordrelinjer, hvor afsendelsesdatoen er overskredet. Der vises følgende oplysninger for de enkelte ordrer på hver vare: nummer, debitornavn, debitorens telefonnummer, afsendelsesdato, ordrestørrelse og antal i restordre. Rapporten viser også, om kunden har andre varer i restordre.|
|**Varer i salgsordrer**|708|Viser en liste over, hvilke ordrer der endnu ikke er leveret, og hvilke varer der indgår i ordren. Den viser ordrenummer, debitors navn, afsendelsesdato, ordrestørrelse, forsinket mængde, restordreantal, pris samt eventuel rabatprocent og beløb. Ikke leveret antal, restordreantal og beløb lægges sammen for hver vare. Brug rapporten til at vise, om der er aktuelle eller kommende leveringsproblemer.|