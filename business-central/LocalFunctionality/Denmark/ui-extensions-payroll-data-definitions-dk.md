---
title: Definitioner af løndata [DK]
description: I dette emne forklares det, hvordan du kan bruge udvidelser til at udveksle data med løntjenesteudbydere i Danmark.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: bholtorf
ms.openlocfilehash: d023e3420f9115d5342d8d8b5f66a6df8a8cb750
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8131109"
---
# <a name="the-payroll-data-definitions-dk-extension"></a>Udvidelsen Definitioner af løndata (DK)
Hvis dit firma bruger løntjenesteudbyderne Danløn, Dataløn, Lønservice, Multiløn eller Proløn i Danmark, kan udvidelsen Definitioner af løndata(DK) hjælpe dig med hurtigt og nøjagtigt at registrere løntransaktioner fra disse udbydere. Udvidelsen indeholder dataudvekslingsdefinitioner, der gør det muligt at importere løntransaktioner i filer, som udbyderne sender til dig. Du kan finde flere oplysninger om dataudvekslingsdefinitioner under [Konfigurere dataudvekslingsdefinitioner](../../across-how-to-set-up-data-exchange-definitions.md).  

## <a name="getting-started"></a>Introduktion
Det første trin er at tilknytte de forskellige typer af løntransaktioner til de finanskonti, de skal bogføres på i Business Central. Du kan f.eks. bogføre pensionsbidrag til en konto med navnet Pension, og afgifter, der er betalt som bidrag, til en konto med navnet Pensionsafgift. Dette sker uden for Business Central, f.eks. kan du bruge et Excel-regneark til at visualisere tilknytningen. Samarbejd med løntjenesteudbyderen for at sikre, at den fil, de eksporterer, indeholder tilknytningen. Normalt kan du finde oplysninger om, hvordan du konfigurerer eksportfiler på udbyderens websted.

Når du har installeret udvidelsen, er det næste trin at angive formatet for løndatafilen fra løntjenesteudbyderen. Det gør du ved at gå til siden **Opsætning af Finans** og vælge udbyderen i feltet **Format til import af løntransaktion**.

## <a name="to-import-a-payroll-file"></a>Sådan importereres en lønningslistefil
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Finanskladder**, og vælg derefter det relaterede link.  
2.  Vælg den kladde, du skal bruge, og brug derefter handlingen **Importér lønfil** for at indlæse datafilen fra løntjenesteudbyderen.

## <a name="see-also"></a>Se også
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]