---
title: Salgsrapporter og analyser
description: Se, hvilke salgsrapporter og analyser der er tilgængelige i standardversionen af Business Central, så du kan holde styr på virksomheden.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 76f93a75f9f7fd52b2495d75bffe648d53f9c844
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543243"
---
# <a name="sales-reports-and-analytics-in-business-central"></a>Salgsrapporter og analyser i Business Central

Salgsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] gør det muligt for salgs- og erhvervs medarbejdere at få indsigt i og statistikker om aktuelle og tidligere salgsaktiviteter.  

## <a name="reports"></a>Rapporter

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
|**Salgsstatistik**|112|[!INCLUDE [reports-sales-statistics](includes/reports-sales-statistics.md)] |
|**Disp. salgsreservation**|209|Viser, hvilke varer der er disponible til levering på salgsdokumentet. Du angiver, om rapporten skal vise status på hvert dokument eller på hver salgslinje. Når du udskriver rapporten, kan du automatisk få indsat det antal, der kan leveres, i feltet **Afsend (antal)** på salgslinjerne. Herefter kan rapporten bruges til at afgøre, hvilke dokumenter der skal bogføres.<br>Der er også en egenskab, som du kan bruge til at angive det antal varer, der skal leveres. **Bemærk**: Denne funktionalitet er ikke tilgængelig for avancerede lagerfunktioner.|
|**Lagerleverancestatus**|7313|Rapporten kan bruges til alle lokationer, hvor **Påkrævede forsendelser** er aktiveret. **Lagerleverancestatus**-rapporten viser alle ikke-bogførte lagerleverancedokumenter, herunder lokationer, placeringskoder, dokument status, antal osv. Denne rapport er perfekt til at få overblik.|
|**Plukliste (lager)**|813|Viser en oversigt over de salgsordrer, en vare indgår i. Der vises følgende oplysninger om hver vare: salgsordrelinje med debitors navn, variantkode, lokationskode, placeringskode, afsendelsesdato, antal til levering og enhed. Antallet lægges sammen for hver vare. Rapporten kan f.eks. bruges, når der skal hentes varer fra lageret.<br>**Bemærk**: Denne funktionalitet er ikke tilgængelig for avancerede lagerfunktioner.|
|**Vare - restordrer til kunder**|718|Viser en oversigt med de ordrelinjer, hvor afsendelsesdatoen er overskredet. Der vises følgende oplysninger for de enkelte ordrer på hver vare: nummer, debitornavn, debitorens telefonnummer, afsendelsesdato, ordrestørrelse og antal i restordre. Rapporten viser også, om kunden har andre varer i restordre.|



## <a name="tasks"></a>Opgaver

I følgende artikler beskrives nogle af de vigtigste opgaver i forbindelse med analyse af virksomhedens tilstand:

* [Oprette analyserapporter](bi-how-create-analysis-views-reports.md)  
* [Vise varedisponering](inventory-how-availability-overview.md)


## <a name="see-also"></a>Se også

[Konfigurere salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Reservere varer](inventory-how-to-reserve-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
