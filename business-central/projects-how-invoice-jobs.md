---
title: Oprette en projektsalgsfaktura for at fakturere et projekt
description: 'Beskriver, hvordan du fakturerer debitorer for diverse projektudgifter, efterhånden som et projekt skrider frem og omkostningerne stiger.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: project invoice
ms.search.form: '1002, 1007,'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
---
# <a name="invoice-projects"></a>Faktura projekter

I løbet af projektet kan der akkumuleres projektomkostninger fra ressourceforbrug, materialer og projektrelaterede indkøb. Efterhånden som status for projektet ændrer sig, bogføres disse transaktioner i projektkladden. Det er vigtigt, at alle omkostninger er registreret i projektkladden, før du fakturerer kunden.
Faktureringen kan foretages, når projektet er afsluttet, eller med bestemte intervaller, efterhånden som status for projektet ændres, baseret på en faktureringsplan.

Du kan fakturere:

* Flere projekter, der bruger en **Project Create Sales Invoice-opgave** .
* Hele projekter, nogle projekter inden for projekt eller individuelle projektplanlægningslinjer, der bruger den relevante handling på projektsiderne.
* Kombinere flere projektplanlægningslinjer fra forskellige projekter til en enkelt salgsfaktura ved hjælp af **handlingen Hent projektplanlægningslinjer** på **siden Salgsfaktura** .

## <a name="to-create-multiple-project-sales-invoices"></a>Sådan opretter du flere salgsfakturaer for projekter

Du kan oprette en faktura for et projekt eller for en eller flere projektopgaver for en debitor, når det arbejde, der skal faktureres, er udført, eller når den fakturadato, som er angivet i et fakturaskema, er nået.

Følgende procedure viser, hvordan du kan bruge en kørsel til at fakturere flere projekter.  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Opret salgsfaktura for projekt**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Du kan angive filtre, hvis du vil begrænse de projekter, som kørslen skal behandle.
4. Vælg **OK** for at starte oprette fakturaen.  

Du kan gennemse og bogføre oprettede fakturaer på siden **Salgsfakturaer** .

> [!NOTE]
> Du kan også fakturere en kunde ved at vælge projektet og derefter vælge handlingen **Opret projektsalgsfaktura** eller bruge **handlingen Opret salgsfaktura** i projektopgaverne.

## <a name="to-create-and-post-project-sales-invoice-from-project-planning-lines"></a>Sådan opretter og bogfører du salgsfakturaer for projekter fra projektplanlægningslinjer

Du kan oprette en faktura ud fra en projektplanlægningslinje og på det tidspunkt angive antallet af varen, ressourcen eller finanskontoen, som du vil fakturere.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.
2. Åbn et relevant projekt.
3. Vælg en projektopgave, hvor feltet **Projektopgavetype** indeholder **Bogføring**, og vælg derefter handlingen **Projektplanlægningslinjer**.  
4. Angiv antallet af varen, ressourcen og finanskontotype, som du vil fakturere, i feltet **Antal til overførsel til faktura** i en projektplanlægningslinje.  
5. Vælg handlingen **Opret salgsfaktura**.
6. På siden **Projektoverførsel til salgsfaktura** skal du angive bogføringsdatoen, og om du vil oprette en ny faktura eller føje denne faktura til en eksisterende.
7. Vælg knappen **OK**.  
8. På siden **Projektplanlægningslinjer** skal du vælge **Salgsfakturaer/kreditnotaer**.

    Siden **Salgsfaktura** åbnes og viser det antal, du har overført til fakturaen.
9. Foretag yderligere ændringer, og vælg derefter handlingen **Bogfør**.

> [!NOTE]  
> Ovenstående fremgangsmåde er ens for at oprette, gennemse og bogføre en projektrelateret salgskreditnota.

## <a name="invoice-one-customer-for-multiple-project-tasks"></a>Fakturere én debitor for flere projektopgaver

Du kan forenkle faktureringsprocessen ved at sende én faktura til en debitor for flere projekter. Føj projektplanlægningslinjer fra flere projekter til en salgsfaktura på én gang. Denne proces svarer til at oprette en salgsfaktura fra en projektplanlægningslinje og angive en værdi i feltet **Føj til salgsfakturanr.**

Her er en oversigt over processen.

1. Opret en ny salgsordre, og udfyld feltet **Kundenummer** . Hvis det er nødvendigt, kan du også udfylde felterne **Faktureres til kundenr.** og **Valutakode**.
2. I oversigtspanelet **Linjer** skal du vælge handlingen **Hent projektplanlægningslinjer**. Siden **Hent projektplanlægningslinjer** viser fakturerbare projektplanlægningslinjer fra projekter for kunden, debitoren og faktureringsvalutaen, hvor det antal, der skal faktureres, er større end nul. 
3. Vælg de linjer, du vil føje til fakturaen, og vælg derefter **OK**.

Gentag disse trin, hvis du vil tilføje endnu et sæt projektplanlægningslinjer. Du kan også slette fakturaen eller dens linjer og starte forfra.

> [!NOTE]
> Der er et par begrænsninger:
>
> * Handlingen **Hent projektplanlægningslinjer** er ikke tilgængelig på salgsordrer eller salgstilbud.
> * Du kan ikke filtrere på felterne **Leveringsadressekode** eller **Kontaktnummer** .


## <a name="see-also"></a>Se også

[Administrere projekter](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
