---
title: Håndtere bankkonti | Microsoft Docs
description: Du skal afstemme bankposter regelmæssigt med de relaterede banktransaktioner i dine bankkonti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 01/10/2020
ms.author: sgroespe
ms.openlocfilehash: 0d1a38468f5d07a1170027bc728ba16996f2b782
ms.sourcegitcommit: 2f741f442226b8be74586e355f283f365e43220f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947233"
---
# <a name="reconciling-bank-accounts"></a>Bankkontoafstemning
En bankafstemning skal udføres med jævne mellemrum for alle dine bankkonti for at sikre, at firmaets kontantposter er korrekte. Det gør du ved at sammenligne og afstemme poster på dine interne bankkonti med banktransaktioner i din bank og derefter bogføre saldi på dine interne bankkonti for at gøre totaler tilgængelige for økonomichefer. Bankafstemning er også en praktisk måde at opdage og løse manglende betalinger og bogføringsfejl på.

Du kan udføre opgaven adskilt på siden **Bankkontoafstemning**, hvor du sammenholder (afstemmer) bankkontoudtogslinjer i venstre rude med dine interne bankkontoposter i højre rude. Du kan også udføre denne opgave på siden **Betalingsudligningskladde** som en del af behandling af betalinger, der er repræsenteret på et bankkontoudtog. På begge sider kan du angive oplysninger for bankkontoudtog ved at importere en fil eller et feed, og du kan bruge automatiske sammenholdningsforslag.

> [!NOTE]  
> I nordamerikanske versioner kan du også udføre bankafstemning på siden **Bankafstemningskladde**, der er mere velegnet til checks og indskud, men ikke kan bruges til import af bankkontoudtogsfiler. Hvis du vil bruge denne side i stedet for siden **Bankkontoafstemning**, skal du fjerne markeringen i feltet **Bankafstemning med automatisk match** på siden **Regnskabsopsætning**. Du kan finde flere oplysninger i afsnittet "Afstemme bankkonti" under Lokal funktionalitet for USA.

Før du kan administrere dine bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du konfigurere hver bankkonto som et bankkontokort. Desuden skal du oprette elektroniske tjenester, som du kan bruge til import af bankens kontoudtog og eksport af betalingsfilen. Du kan finde flere oplysninger i [Oprette bankkonti](bank-setup-banking.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Skal du se |
| --- | --- |
| Afstemme bankkonti som en separat opgave på siden **Bankkontoafstemning**. |[Afstemme bankkonti](bank-how-reconcile-bank-accounts-separately.md) |
| Afstem bankkonti i forbindelse med betalingsbehandling på siden **Betalingudligningskladde**. |[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

## <a name="see-related-training-at-microsoft-learnlearnpathsreconcile-bank-accounts-dynamics-365-business-central"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)

## <a name="see-also"></a>Se også
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Overføre bankbeløb](bank-how-transfer-bank-funds.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Administrere skyldige beløb](payables-manage-payables.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)
