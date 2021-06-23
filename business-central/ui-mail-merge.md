---
title: Bruge Microsoft Word-skabeloner til massekommunikation | Microsoft Docs
description: Word-skabeloner kan gøre det nemmere at masseoprette dokumenter, der er tilpasset bestemte objekter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d29e29eca7dfc24ded51aed994ac7003fb4d30ab
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110950"
---
# <a name="using-word-templates-for-bulk-communication"></a>Bruge Word-skabeloner til massekommunikation
Microsoft Word-skabeloner kan gøre det nemmere at massekommunikere med objekter som f.eks. debitorer og kreditorer. Du kan f.eks. oprette brochurer, som giver debitorer besked om en salgskampagne, breve til kreditorer om en ny indkøbspolitik eller invitationer, der skal tiltrække kontakter til et kommende arrangement.

> [!NOTE]
> Du kan kun bruge Word-skabeloner på enheder med Microsoft Word 2019 og Windows-operativsystemet installeret.

Du kan bruge objekter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakilde for skabelonen og til at tilføje fletfelter for at tilpasse dokumenter til de enkelte objekter. Fletfelterne hentes fra objektet i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du anvender en Word-skabelon til et objekt, indsættes data fra fletfelterne i dokumentet.

På siden **Word-skabeloner** kan du bruge en vejledning om assisteret opsætning for at hente en zip-fil, der indeholder filen DataSource.txt og en Word-skabelonfil til et objekt. Når du har oprettet skabelonen og tilføjet fletfelter, bruger du den samme vejledning til at overføre skabelonen. Du kan kun bruge den Word-skabelon og de datakildefiler, som du henter fra [!INCLUDE[prod_short](includes/prod_short.md)], og du skal gemme filerne på den samme placering.

> [!NOTE]
> Når du vælger et objekt, som du vil oprette en skabelon for, viser listen alle objekter i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan dog ikke oprette skabeloner for alle objekter. Hvis navnet på et objekt indeholder specialtegn som f.eks **/**, **.**, **_** eller **-**, kan du ikke oprette en skabelon for det. Navnet på objektet vises i kolonnen **Objekttitel**.

Når du opretter skabelonen i Word, kan du tilføje fletfelter på fanen **Forsendelser** ved at vælge **Indsæt fletfelt**.

> [!NOTE]
> Du kan ikke bruge fletfelter, hvis navnet på feltet indeholder 40 tegn eller mere. Du kan f.eks. ikke bruge feltet Toldregistreringsdato i virksomhedsoplysninger, da det indeholder 40 tegn. 

Når du har klargjort din Word-skabelon, kan du vælge **Anvend** for at oprette dokumenterne på siden **Word-skabeloner**. Du kan enten oprette ét dokument, der indeholder sektioner for hvert objekt, eller opdele handlingen for at oprette et nyt dokument for hvert objekt.

## <a name="to-create-a-word-template"></a>Sådan oprettes en Word-skabelon
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Word-skabeloner**, og vælg derefter det tilknyttede link.
2. Følg trinnene i guiden til assisteret opsætning. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se også
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
