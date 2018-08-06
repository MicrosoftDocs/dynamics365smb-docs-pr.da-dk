---
title: "Definitioner af løndata (DK) | Microsoft Docs"
description: "Denne udvidelse gør det nemt at udveksle data med løntjenesteudbydere i Danmark."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 04/23/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba50e74b51148e42dd25752ade5a37d0e3285509
ms.openlocfilehash: 34065229f3833f8e957dcdc4c7c4796bcc4b1be5
ms.contentlocale: da-dk
ms.lasthandoff: 04/26/2018

---

# <a name="the-payroll-data-definitions-dk-extension"></a>Udvidelsen Definitioner af løndata (DK)
Hvis dit firma bruger løntjenesteudbyderne Danløn, Dataløn, Lønservice, Multiløn eller Proløn i Danmark, kan udvidelsen Definitioner af løndata(DK) hjælpe dig med hurtigt og nøjagtigt at registrere løntransaktioner fra disse udbydere. Udvidelsen indeholder dataudvekslingsdefinitioner, der gør det muligt at importere løntransaktioner i filer, som udbyderne sender til dig. Du kan finde flere oplysninger om dataudvekslingsdefinitioner under [Konfigurere dataudvekslingsdefinitioner](../../across-how-to-set-up-data-exchange-definitions.md).  

## <a name="getting-started"></a>Introduktion
Det første trin er at tilknytte de forskellige typer af løntransaktioner til de finanskonti, de skal bogføres på i Business Central. Du kan f.eks. bogføre pensionsbidrag til en konto med navnet Pension, og afgifter, der er betalt som bidrag, til en konto med navnet Pensionsafgift. Dette sker uden for Business Central, f.eks. kan du bruge et Excel-regneark til at visualisere tilknytningen. Samarbejd med løntjenesteudbyderen for at sikre, at den fil, de eksporterer, indeholder tilknytningen. Normalt kan du finde oplysninger om, hvordan du konfigurerer eksportfiler på udbyderens websted.

Når du har installeret udvidelsen, er det næste trin at angive formatet for løndatafilen fra løntjenesteudbyderen. Det gør du ved at gå til siden **Opsætning af Finans** og vælge udbyderen i feltet **Format til import af løntransaktion**. 

## <a name="how-to-import-a-payroll-file"></a>Fremgangsmåde: Importere en lønfil
1.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladder**, og vælg derefter det relaterede link.  
2.  Vælg den kladde, du skal bruge, og brug derefter handlingen **Importér lønfil** for at indlæse datafilen fra løntjenesteudbyderen. 

## <a name="see-also"></a>Se også
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  