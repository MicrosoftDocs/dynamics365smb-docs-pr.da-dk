---
title: Importér løntransaktioner
description: 'For at administrere løn skal du importere og bogføre finanstransaktioner fra din lønningslisteudbyder i finansregnskabet ved hjælp af lønudvidelsen, f.eks. Ceridian.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Ceridian, Quickbooks, salary'
ms.search.form: '1660, 1661, 36601'
ms.date: 06/16/2021
ms.author: bholtorf
---
# importere løntransaktioner

For at tage højde for lønbetalinger og relaterede transaktioner, skal du importere og bogføre finansielle transaktioner, der er foretaget af din lønningssystemudbyder i finansbogholderiet. For at gøre dette skal du først importere en fil, som du modtager fra lønningsystemudbyderen, på siden **Finanskladde**. Derefter knytter du de eksterne konti i lønningslistefilen til de relevante finanskonti. Til sidst skal du bogføre lønningstransaktionerne i overensstemmelse med kontotilknytningen.

> [!NOTE]  
> Hvis du vil bruge denne funktion, skal en udvidelse til import af løn være installeret og aktiveret. Importudvidelserne Ceridian løn og Quickbooks-lønfil er forudinstalleret i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md).

## Sådan importereres en lønningslistefil

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Finanskladder**, og vælg derefter det relaterede link.
2. I den relevante finanskladdekørsel skal du vælge handlingen **Importér løntransaktioner**. En assisteret opsætningsvejledning åbnes.
3. Udfør trinnene på siden **Importér løntransaktioner**.

    > [!TIP]  
    >   I trinnet for tilknytning af de eksterne lønposter til dine finanskonti vil de tilknytninger, du foretager, blive husket, næste gang de samme poster importeres. Derved sparer du tid, da du ikke behøver at udfylde feltet **Kontonr.** manuelt i finanskladden, hver gang du har indlæst gentagne løntransaktioner.   

    Når du vælger knappen **OK** i den assisterede opsætningsvejledning, udfyldes siden **Finanskladde** med linjer, der repræsenterer de transaktioner, som lønningslistefilen indeholder, og de relevante konti udfyldt på forhånd i **Finanskonto**-felterne i overensstemmelse med de tilknytninger, du har foretaget i vejledningen.
4. Rediger eller bogfør kladdelinjerne som for alle andre finanstransaktioner. Du kan finde flere oplysninger i [Bogføre transaktioner direkte i finansregnskabet](finance-how-post-transactions-directly.md).   

## Se også

[Finans](finance.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]