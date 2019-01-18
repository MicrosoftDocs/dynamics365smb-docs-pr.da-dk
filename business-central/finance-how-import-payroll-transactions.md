---
title: "Importere løntransaktioner | Microsoft Docs"
description: "For at administrere løn skal du importere og bogføre finanstransaktioner fra din lønningslisteudbyder i finansregnskabet ved hjælp af lønudvidelsen, f.eks. Ceridian eller Quickbooks."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 642c35fa993b9177ec51deccaef7beb3615ab336
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="import-payroll-transactions"></a>Importér løntransaktioner
For at tage højde for lønbetalinger og relaterede transaktioner, skal du importere og bogføre finansielle transaktioner, der er foretaget af din lønningssystemudbyder i finansbogholderiet. For at gøre dette skal du først importere en fil, som du modtager fra lønningsystemudbyderen, på siden **Finanskladde**. Derefter knytter du de eksterne konti i lønningslistefilen til de relevante finanskonti. Til sidst skal du bogføre lønningstransaktionerne i overensstemmelse med kontotilknytningen.

> [!NOTE]  
>   Hvis du vil bruge denne funktion, skal en udvidelse til import af løn være installeret og aktiveret. Importudvidelserne Ceridian løn og Quickbooks-lønfil er forudinstalleret i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Sådan importereres en lønningslistefil
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladder**, og vælg derefter det relaterede link.
2. I den relevante finanskladdekørsel skal du vælge handlingen **Importér løntransaktioner**. En assisteret opsætningsvejledning åbnes.
3. Udfør trinnene på siden **Importér løntransaktioner**.

    > [!TIP]  
    >   I trinnet for tilknytning af de eksterne lønposter til dine finanskonti vil de tilknytninger, du foretager, blive husket, næste gang de samme poster importeres. Derved sparer du tid, da du ikke behøver at udfylde feltet **Kontonr.** manuelt i finanskladden, hver gang du har indlæst gentagne løntransaktioner.   

    Når du vælger knappen **OK** i den assisterede opsætningsvejledning, udfyldes siden **Finanskladde** med linjer, der repræsenterer de transaktioner, som lønningslistefilen indeholder, og de relevante konti udfyldt på forhånd i **Finanskonto**-felterne i overensstemmelse med de tilknytninger, du har foretaget i vejledningen.
4. Rediger eller bogfør kladdelinjerne som for alle andre finanstransaktioner. Du kan finde flere oplysninger i [Bogføre transaktioner direkte i finansregnskabet](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  

