---
title: Revisoroplevelse i Dynamics 365 | Microsoft Docs
description: "Få mere at vide om Accountant Hub til Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 05/09/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 8901216a843440e922ae4df9d7508b543a6c1322
ms.contentlocale: da-dk
ms.lasthandoff: 05/15/2018

---
# <a name="get-started-with-include-d365acclongincludesd365acclongmdmd"></a>Kom i gang med [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Enhver virksomhed skal føre regnskab og godkende det. Nogle virksomheder benytter en ekstern revisor, mens andre har kvalificerede regnskabsmedarbejdere. Hvis du er revisor og har mange kunder, kan du bruge [!INCLUDE [d365acc](includes/d365acc_md.md)] som dit dashboard, hvor du kan få et bedre overblik over dine kunder.  

Du kan få adgang til [!INCLUDE [d365acc](includes/d365acc_md.md)] ved at tilmelde dig fra [Dynamics 365 – Accountant Hub på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants).  

> [!TIP]
>  Når du tilmelder dig [!INCLUDE [d365acc](includes/d365acc_md.md)], skal du angive din mailadresse til arbejde, f.eks. <em>me@accountant.com</em>. Det anbefales at bruge den samme mailadresse, når du arbejder i dine kunders [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)], så du let kan skifte mellem kunder. Mailadressen skal være en arbejdsadresse, der er baseret på Active Directory.

## <a name="working-with-individual-clients"></a>Arbejde med individuelle kunder
Dashboardet viser de vigtigste oplysninger om hver enkelt kunde.  
![Accountant Hub](./media/accountant-get-started/accountant-dashboard-tasks.png)

Kolonnen **Navn på kunde** viser navnene på dine kunder og kolonnen **Navn på virksomhed** viser alle virksomheder, hvis kunden har mere end én virksomhed i [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]. Desuden er der felter, som viser dig opgaver, der er tildelt til dig i kundens virksomhed, herunder overskredne opgaver.  

Du kan tilpasse dashboardet for at få vist de datapunkter, som du vil se, ved at tilføje eller fjerne kolonner. Du kan f.eks. få vist skatter, der er forfaldne til betaling, hvor mange åbne salgsdokumenter, kunden har, eller antallet af købsfakturaer, der forfalder næste uge. Du kan konfigurere visningen efter behov. Hvis du har mange kunder, kan du bruge filtre til at sortere visningen.  

Ud for kundens navn angiver ellipserne (...) en kort menu:

- Opdatere det aktuelle regnskab og få nye oplysninger om kunden  
- Gå til kundens [!INCLUDE [d365fin](includes/d365fin_md.md)]  
- Vælge flere kunder  

På samme måde kan du bruge rullemenuen **Oversigt over kunder** til f.eks. at opdatere alle virksomheder.  

> [!TIP]
>  For at få adgang til en kundes [!INCLUDE [d365fin](includes/d365fin_md.md)] skal du vælge menupunktet **Gå til kunde** - du er logget på automatisk.

## <a name="company-details"></a>Virksomhedsoplysninger
Du kan se flere oplysninger om dine kunders data ved at vælge navnet på den virksomhed, som du vil vide mere om. Dermed åbnes ruden **Virksomhedsoplysninger**, hvor du kan se yderligere oplysninger, f.eks. følgende:  

* Saldo for kassekonto  
* Pengestrømsprognose  
* Forfaldne købsfakturaer  
* Forfaldne salgsfakturaer  

![Oplysninger om kundens virksomhed i revisorens dashboard](./media/accountant-get-started/accountant-company-details.png)

Teknisk set har du nu logget på din kundes [!INCLUDE [d365fin](includes/d365fin_md.md)], og de data, du kan se, er dynamiske data. Hvis du vil se nærmere på dataene, f.eks. en forfalden købsfaktura, skal du vælge linket, så kommer du til kundens virksomhed.  

> [!TIP]
>  Du kan starte foruddefinerede Excel-projektmapper fra fanen **Rapporter** på båndet. Disse Excel-projektmapper er designet som vigtige regnskabsopgørelser og rapporter, der er klar til udskrivning, men du kan også ændre dem efter behov. Du kan finde flere oplysninger i [Analysere regnskabsopgørelser i Microsoft Excel](/dynamics365/business-central/finance-analyze-excel?toc=/dynamics365/accountants/toc.json) i hjælpen til [!INCLUDE [d365fin](includes/d365fin_md.md)].  

Ellers skal du lukke detaljeruden og fortsætte til den næste kunde.  

## <a name="assigned-tasks"></a>Tildelte opgaver
I kundens [!INCLUDE [d365fin](includes/d365fin_md.md)] kan du tildele opgaver til dig selv og andre, og andre kan tildele opgaver til dig. Dashboardet i [!INCLUDE [d365acc](includes/d365acc_md.md)] giver dig en oversigt over tildelte opgaver for hver kunde, og du kan også få vist en oversigt over alle tildelte opgaver ved at vælge **Mine brugeropgaver** i den venstre navigationsrude.  

I kundens virksomhed har du også køer, der fremhæver opgaver, der er tildelt til dig i denne bestemte kunde.

![Opgaver, der er tildelt til revisoren i kundens virksomhed](./media/accountant-get-started/accountant-company-details-tasks.png)

### <a name="my-user-tasks"></a>Mine brugeropgaver
Listen **Mine brugeropgaver** i [!INCLUDE [d365acc](includes/d365acc_md.md)] hjælper dig med at prioritere din dag ved at vise yderligere oplysninger om opgaver, der er tildelt til dig på tværs af alle dine kunder.  

![Liste over opgaver, der er tildelt til mig som ekstern revisor](./media/accountant-get-started/accountant-tasklist.png)

Du kan f.eks. sortere efter forfaldsdato eller andre typer data, der hjælper dig med at prioritere din dag. Listen viser som standard alle opgaver, der er tildelt til dig, men du kan oprette filtre, så der f.eks. kun vises opgaver, der er markeret som høj prioritet.

For at hente en opgave skal du blot vælge den på listen over ventende brugeropgaver. På båndet åbner linket **Gå til opgaveelementet** det vindue, hvor du kan udføre arbejdet.  

Når du har udført en opgave, skal du blot markeres som fuldført.  

## <a name="see-also"></a>Se også
[Tilføje kunder til dit dashboard i [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)  
[Velkommen til [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](index.md)  
[Analysere regnskabsopgørelser i Microsoft Excel](/dynamics365/business-central/finance-analyze-excel?toc=/dynamics365/accountants/toc.json)   
[Revisoroplevelser i [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json)  
[Dynamics 365 – Accountant Hub på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

