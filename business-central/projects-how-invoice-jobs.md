---
title: Oprette en projektsalgsfaktura for at fakturere for et projekt
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
# <a name="invoice-projects"></a>Fakturere projekter

I løbet af projektet kan der akkumuleres projektomkostninger fra ressourceforbrug, materialer og projektrelaterede indkøb. Efterhånden som status for projektet ændrer sig, bogføres disse transaktioner i projektkladden. Det er vigtigt, at alle omkostninger er registreret i projektkladden, før du fakturerer kunden.

> [!NOTE]
> Du kan også købe eksterne ressourcer uden relation til et projekt, f.eks. for at fakturere en kreditor for udført arbejde. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md).

Du kan fakturere hele projektet fra siden **Projektopgavelinjer** eller kun fakturere de valgte fakturerbare linjer fra siden **Projektplanlægningslinjer**. Faktureringen kan foretages, når projektet er afsluttet, eller med bestemte intervaller, efterhånden som status for projektet ændres, baseret på en faktureringsplan.

> [!NOTE]  
> Hvis du vælger **Fakturerbar** i feltet **Linjetype for projekt** på købsdokumenter for projektrelaterede indkøb, oprettes der projektplanlægningslinjer, som er klar til blive faktureret til kunden. Du kan finde flere oplysninger i [Administrere projektforsyninger](projects-how-manage-project-supplies.md).

Du kan også fakturere en virksomhed, der ikke er slut debitor. Nogle gange adskiller den part, der er til projektet, sig fra den part, der betaler fakturaen. På siden **Projekter** kan du angive den kunde, der skal have fordel af projektet i felterne **Sælg til**, og den part, der skal faktureres, i felterne **Faktureres til**.

## <a name="to-create-multiple-project-sales-invoices"></a>Sådan opretter du flere salgsfakturaer for projekter

Du kan oprette en faktura for et projekt eller for en eller flere projektopgaver for en debitor, når det arbejde, der skal faktureres, er udført, eller når den fakturadato, som er angivet i et fakturaskema, er nået.

Følgende procedure viser, hvordan du kan bruge en kørsel til at fakturere flere projekter.  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Opret salgsfaktura for projekt**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Du kan angive filtre, hvis du vil begrænse de projekter, som kørslen skal behandle.
4. Vælg **OK** for at starte oprette fakturaen.  

Du kan gennemse og bogføre oprettede fakturaer i vinduet **Salgsfakturaer**.

> [!NOTE]
> Du kan også fakturere en kunde ved at markere projektet og derefter vælge handlingen **Opret salgsfaktura for projekt**. 

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

## <a name="see-also"></a>Se også

[Administrere projekter](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
