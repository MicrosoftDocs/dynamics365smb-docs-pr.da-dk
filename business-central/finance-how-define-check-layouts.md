---
title: Angive layoutet for en check
description: Du kan designe og udskrive checks i forskellige formater i overensstemmelse med de standarder, der er angivet af de lokale myndigheder.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.search.form: 374, 404
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: ed0cf9383ed635e3f7b940ef4f28943ffb6bc1a0
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518099"
---
# <a name="select-a-check-layout"></a>Vælge et checklayout

Du kan udforme dine checks i overensstemmelse med de lokale myndigheders standarder. Checkbilleder kan udskrives på engelsk, fransk eller spansk.

Checks er designet til udskrivning i amerikanske og canadiske checkbilledformater i et checkfølgebrevformat eller et følgebrev-følgebrevcheckformat.

## <a name="to-select-a-check-layout"></a>Sådan vælges et checklayout

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rapportvalg - Bankkonto**, og vælg derefter det relaterede link.
2. På siden **Rapportvalg - bankkonto** skal du vælge feltet **Check** i feltet **Forbrug**.
3. Vælg et af følgende rapport-id'er.

| Rapport-id | Rapportnavn | Beskrivelse |
| --- | --- | --- |
| 1401 |Check |Dette er standardrapporten. |
| 10411 |Check (følgebrev/følgebrev/check) |Denne rapport er designet til at udskrive check i et følgebrev/følgebrev/check-format. |
| 10412 |Check (følgebrev/check/følgebrev) |Denne rapport er designet til at udskrive check i et følgebrev/check/følgebrev-format. |
| 10413 |Tre checks pr. side |Denne rapport er udviklet til at udskrive tre checks på hver side. |

Når du har oprettet checklayout, kan du udskrive check på siden **Udbetalingskladde**. Du kan finde flere oplysninger i [Arbejde med checks](payables-how-work-checks.md).

Hvis du vil ændre et af disse standardchecklayout, skal du bruge enten Word eller RDLC-integration til at gøre det. Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md).

## <a name="use-micr-and-security-fonts"></a>Bruge MICR og sikkerhedsskrifttyper
Onlineversionen af [!INCLUDE[prod_short](includes/prod_short.md)] indeholder forudinstallerede skrifttyper på de servere, der kan bruges, når checklayout defineres. Følgende dispositioner viser, hvilke skrifttyper der er tilgængelige og indeholder hyperlinks til detaljerede oplysninger fra tredjepartsleverandører af skrifttyperne.

> [!Important]
> MICR og sikkerhedsskrifttyper til checks i Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] licenseres i en skrifttypepakke fra IDAutomation.com, Inc. Disse produkter må kun anvendes som led i og i forbindelse med Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)].

I opdatering 15.3 og nyere er der installeret MICR-skrifttyper (Magnetic Ink Character Recognition), som kan bruges. Både E-13B- og CMC-7-standarder understøttes. Ud over MICR-skrifttyper er særlige sikkerhedsskrifttyper tilgængelige, så du kan oprette tekst, navne, beløb og valutasymbolerne dollar, euro, pund og yen, som er svære at ændre, når en check først er udskrevet.

> [!NOTE]
> Af hensyn til sikkerheden og af juridiske årsager kan du ikke overføre brugerdefinerede skrifttyper til [!INCLUDE[prod_short](includes/prod_short.md)]-miljøet.

### <a name="micr-e-13b-specifications"></a>MICR E-13B-specifikationer

Følgende opsummerer specifikationer for de MICR E-13B-skrifttyper, som kan være nyttige, når du kalibrerer skrifttyper til at kunne bruges i checklayout på specifikke MICR-printere.

![MICR E-13B-specifikationer.](media/font_MICR_E-13B_Specifications.png "MICR E-13B-specifikationer")

### <a name="delimiter-characters"></a>Afgrænsningstegn

![Afgrænsningstegn.](media/font-micr-letters.png "Afgrænsningstegn")

Den komplette specifikation af MICR E-13B-skrifttyper findes i leverandørens dokumentation her: (https://www.idautomation.com/micr-fonts/e13b/).

### <a name="micr-cmc-7-specifications"></a>MICR CMC-7-specifikationer

Følgende CMC-7-skrifttyper er tilgængelige i [!INCLUDE[prod_short](includes/prod_short.md)] online:

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
- IDAutomationCMC7n40

Følgende opsummerer specifikationer for de MICR CMC-7-skrifttyper, som kan være nyttige, når du kalibrerer skrifttyper til at kunne bruges i checklayout på specifikke MICR-printere.

![MICR CMC-7-specifikationer.](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7-specifikationer")

### <a name="delimiter-characters"></a>Afgrænsningstegn

![Afgrænsningstegn for CMC-7.](media/font-cmc7-letters.png "Afgrænsningstegn for CMC-7")

Den komplette specifikation af MICR CMC-7-skrifttyper findes i leverandørens dokumentation her: (http://www.idautomation.com/micr-fonts/cmc7/).

### <a name="secure-font-specifications"></a>Specifikationer for sikre skrifttyper

Følgende opsummerer specifikationer for sikkerhedsskrifttyper til checks, som kan være nyttige, når du kalibrerer skrifttyper til at kunne bruges i checklayout på specifikke MICR-printere.

![Specifikationer for sikkerhedsskrifttyper til checks.](media/font_check-security-font_Specifications.png "Specifikationer for sikkerhedsskrifttyper til checks")

Den komplette specifikation af sikkerhedsskrifttyper til checks findes i leverandørens dokumentation her: (https://www.idautomation.com/security-fonts/).

Skrifttyper til andre formål er også tilgængelige i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Tilgængelige skrifttyper](ui-fonts.md)

## <a name="see-also"></a>Se også

[Sådan opretter og ændrer du Brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md)  
[Skrifttyper i Business Central](ui-fonts.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Bankkontoafstemning](bank-manage-bank-accounts.md)   
[Fuldførelse af periodeafslutningsprocesser](year-how-complete-period-end-processes.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]