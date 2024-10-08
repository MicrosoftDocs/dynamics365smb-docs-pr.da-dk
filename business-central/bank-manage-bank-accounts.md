---
title: Håndtere bankkonti
description: Du skal afstemme bankposter regelmæssigt med de relaterede banktransaktioner i dine bankkonti.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: reconcile
ms.search.form: '377, 378, 165, 1284'
ms.date: 07/24/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="manage-and-reconcile-your-bank-accounts"></a>Administrere og afstemme dine bankkonti

En bankafstemning skal udføres med jævne mellemrum for alle dine bankkonti for at sikre, at firmaets kontantposter er korrekte. Det gør du ved at sammenligne og afstemme poster på dine interne bankkonti med banktransaktioner i din bank og derefter bogføre saldi på dine interne bankkonti for at gøre totaler tilgængelige for økonomichefer. Bankafstemning er også en praktisk måde at opdage og løse manglende betalinger og bogføringsfejl på.

Du kan udføre opgaven adskilt på siden **Bankkontoafstemning**, hvor du sammenholder (afstemmer) bankkontoudtogslinjer i venstre rude med dine interne bankkontoposter i højre rude. Du kan også udføre denne opgave på siden **Betalingsudligningskladde** som en del af behandling af betalinger, der er repræsenteret på et bankkontoudtog. På begge sider kan du angive oplysninger for bankkontoudtog ved at importere en fil eller et feed, og du kan bruge automatiske sammenholdningsforslag.

> [!NOTE]  
> I nordamerikanske versioner kan du også udføre bankafstemning på siden **Bankafstemningskladde**, der er mere velegnet til checks og indskud, men ikke kan bruges til import af bankkontoudtogsfiler. Hvis du vil bruge denne side i stedet for siden **Bankkontoafstemning**, skal du fjerne markeringen i feltet **Bankafstemning med automatisk match** på siden **Regnskabsopsætning**. Du kan finde flere oplysninger i afsnittet [Afstemme bankkonti](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under Lokal funktionalitet for USA.

Før du kan administrere dine bankkonti inden for, skal du konfigurere hver bankkonto som en bankkonto kort [!INCLUDE[prod_short](includes/prod_short.md)]. Desuden skal du oprette elektroniske tjenester, som du kan bruge til import af bankens kontoudtog og eksport af betalingsfilen. Der er flere oplysninger i [Konfigurere banktransaktioner](bank-setup-banking.md).

Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.

| Til | Se |
| --- | --- |
| Afstemme bankkonti som en separat opgave på siden **Bankkontoafstemning**. |[Afstemme bankkonti](bank-how-reconcile-bank-accounts-separately.md) |
| Afstem bankkonti i forbindelse med betalingsbehandling på siden **Betalingudligningskladde**. |[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> Brug bankafstemning til at kontrollere, at dine bøger er opdaterede og ikke bogfører afstemningen, før du er tilfreds med afstemningen.

## <a name="see-also"></a>Se også

[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Afstemme bankkonti](bank-how-reconcile-bank-accounts-separately.md)  
[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Overføre bankbeløb](bank-how-transfer-bank-funds.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
