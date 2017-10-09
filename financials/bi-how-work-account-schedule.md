---
title: Arbejde med kontoskemaer | Microsoft Docs
description: Beskriver, hvordan du kan bruge kontoskemaer til at oprette forskellige visninger og rapporter til analyse af data for finansiel ydeevne.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 192efcf377f6f6d665c775b24aa715aadd50922f
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-account-schedules"></a>Fremgangsmåde: Arbejde med kontoskemaer
Du kan bruge kontoskemaer til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan. Kontoskemaer analyserer tal i finanskonti og sammenligner finansposter med finansbudgetposter. Resultaterne vises i diagrammer på din startside, f.eks. pengestrømsdiagrammet.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder et par eksempelkontoskemaer, som du kan bruge det samme, eller du kan konfigurere dine egen rækker og kolonner for at angive de tal, du vil sammenligne. Du kan f.eks. oprette kontoskemaer for at beregne avancer på dimensioner som afdelinger eller debitorgrupper. Du kan oprette så mange tilpassede kontoudtog, som du har behov for.  

Oprettelse af kontoskemaer kræver en forståelse af de finansielle data i kontoplanen. Du kan f.eks. få vist finansposter som procenter af budgetposterne. Dette kræver, at der er oprettet budgetter. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette budgetter](finance-how-create-budgets.md).

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Suite**. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="account-categories-and-account-schedules"></a>Kontokategorier og kontoskemaer
Du kan bruge kontokategorier til at ændre layoutet af regnskabet. Når du har oprettet kontokategorierne i vinduet **Finanskontokategorier**, og du vælger handlingen **Opret kontoskemaer** opdateres de underliggende kontoskemaer for de grundlæggende regnskabsrapporter. Næste gang du kører en af disse rapporter, f.eks. saldoopgørelsen, tilføjes nye totaler og underordnede linjer, baseret på dine ændringer. Du kan finde flere oplysninger i [Finans- og kontoplanen](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Sådan oprettes nye kontoskemaer  
 Du bruger kontoskemaer til at analysere tal i finanskonti eller til at sammenligne finansposter med finansbudgetposter. Du kan f.eks. få vist finansposter som procenter af budgetposter.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.  
2. I vinduet **Kontoskemanavne** i skal du vælge handlingen **Ny** for at oprette et nyt kontoskemanavn.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg handlingen **Rediger kontoskema**.
5. Udfyld felterne efter behov i vinduet **Kontoskema**.  

    Når du har oprettet et nyt kontoskema og oprettet rækkerne, skal du angive kolonner. Du kan oprette dem manuelt eller tilknytte et foruddefineret kolonneformat til kontoskemaet.
6. Vælg handlingen **Rediger opsætning af kolonneformat**.
7. Udfyld felterne efter behov i vinduet **Kolonnelayout**.

> [!NOTE]  
>   Hvis du ikke har tildelt et standard kolonneformat til kontoskemaet, skal du definere kolonnerne manuelt.   

### <a name="to-create-a-column-that-calculates-percentages"></a>Sådan oprettes en kolonne, hvor procenten beregnes  
Du vil muligvis gerne medtage en kolonne i et kontoskema for at beregne procenter af et totalbeløb. Hvis du f.eks. har et antal rækker, som specificerer salg efter dimension, kan du have en kolonne, som angiver procenten af det samlede salg, som hver række repræsenterer.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.
2. Vælg et kontoskema i vinduet **Kontoskemanavne**.  
3. Vælg handlingen **Rediger kontoskema** for at konfigurere en kontoskemarække til beregning af den total, som procentdelene baseres på.  
4. Indsæt en linje lige over den første række, som du vil vise en procent for.  
5. Udfyld felterne på linjen på følgende måde: I feltet **Sammentællingstype** skal du angive **Angiv grundlag for procent**. I feltet **Sammentælling** skal du indtaste en formel for den total, som procentdelen skal baseres på. Hvis række 11 f.eks. indeholder det samlede salg, indtastes **11**.  
6. Vælg handlingen **Rediger opsætning af kolonneformat** for at oprette en kolonne.  
7. Udfyld felterne på linjen på følgende måde: I feltet **Kolonnetype** skal du vælge **Formel**. I feltet **Formel** skal du indtaste en formel for det beløb, som du vil beregne en procentdel for, efterfulgt af %. Hvis kolonnenummer N f.eks. indeholder bevægelsen, indtastes **N %**.  
8. Gentag trin 4 til 7 for alle de grupper af rækker, du vil specificere efter procent.

## <a name="to-set-up-account-schedules-with-overviews"></a>Sådan oprettes kontoskemaer med oversigter  
Du kan bruge et kontoskema til at oprette en opgørelse, hvor tallene i finansposter sammenlignes med tallene i finansbudgettet.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.
2. Vælg et kontoskema i vinduet **Kontoskemanavne**.  
3. Vælg handlingen **Rediger kontoskema**  
4. I vinduet **Kontoskema** skal du vælge standardkontoskemanavnet i feltet **Navn**.
5. Vælg handlingen **Indsæt konti**.  
6. Marker de konti, som du ønsker at medtage i opgørelsen, og vælg derefter knappen **OK**.

    Kontiene indsættes i kontoskemaet. Hvis du vil, kan du også ændre kolonneformatet.  
7. Vælg handlingen **Oversigt**.  
8. Klik på oversigtspanelet **Dimensionsfiltre**, og sæt budgetfilteret til det ønskede filternavn.  
9. Vælg knappen **OK**.  

Du kan nu kopiere og indsætte budgetoversigten i et regneark..

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

