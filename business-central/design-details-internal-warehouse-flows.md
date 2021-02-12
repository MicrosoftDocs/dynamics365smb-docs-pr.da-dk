---
title: Designoplysninger – Internt lagerflow | Microsoft Docs
description: Gennemstrømningen af varer mellem placeringer i virksomheden vedrører pluk af komponenter og at lægge færdigvarer på lager til produktions- eller montageordrer og ad hoc-bevægelser, f.eks. placeringsgenopfyldninger, uden relation til kildedokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d6b59df9677216cfcc3fd7e60ec92b1a17890763
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035727"
---
# <a name="design-details-internal-warehouse-flows"></a>Designoplysninger: Internt lagerflow
Gennemstrømningen af varer mellem placeringer i virksomheden vedrører pluk af komponenter og at lægge færdigvarer på lager til produktions- eller montageordrer og ad hoc-bevægelser, f.eks. placeringsgenopfyldninger, uden relation til kildedokumenter. Omfanget og arten af de involverede aktiviteter varierer mellem grundlæggende og avancerede logistikfunktioner.  

 Nogle interne strømme overlapper med indgående eller udgående strømme. Noget af denne overlapning vises som trin 4 og 5 i de grafiske diagrammer for avancerede indgående og udgående strømme. Du kan finde flere oplysninger i [Designoplysninger: Indgående lagerflow](design-details-outbound-warehouse-flow.md)  

## <a name="internal-flows-in-basic-warehousing"></a>Interne strømme i basislogistik  
 I grundlæggende lageropsætning centrerer gennemstrømningen af varer mellem placeringer i virksomheden på pluk af komponenter og at lægge færdigvarer på lager til produktion eller montageordrer og ad hoc-bevægelser, f.eks. placeringsgenopfyldninger, uden relation til kildedokumenter.  

### <a name="flows-to-and-from-production"></a>Flows til og fra Produktion  
 Den vigtigste integration mellem produktionsordrer og grundlæggende lageraktiviteter er repræsenteret af muligheden for at plukke produktionskomponenter med siden **Pluk (lager)** eller siden **Flytning (lager)**.  

> [!NOTE]  
>  På siden **Pluk (lager)** er komponentforbrug bogført sammen med bogføringen af pluk. Ved hjælp af siden **Flytning (lager)** registreres kun placeringsreguleringer, der bogføres ingen vareposter.  

 Udover håndtering af komponenter er integrationen repræsenteret af muligheden for at lægge producerede varer på lager med siden **Læg-på-lager**.  

 Felterne **Til-produktionsplaceringskode**, **Fra-produktionsplaceringskode** og **Åben prod.placeringskode** på lokationskortet eller produktionsressource/arbejdscenterkortene definerer standardflow til og fra produktionsområder.  

 Hvis du ønsker yderligere oplysninger om, hvordan komponentforbrug tømmes fra produktionsplaceringen eller den åbne produktionsplacering, kan du se afsnittet "Træk af produktionskomponenter i lageret" i dette emne.  

### <a name="flows-to-and-from-assembly"></a>Flows til og fra Montage  
 Den vigtigste integration mellem montageordrer og grundlæggende lageraktiviteter repræsenteres af muligheden for at flytte montagekomponenter til montageområdet.  

 Da der ikke findes nogen specifikke lagerfunktioner til at lægge montageelementer på lager, kan placeringskoden på montageordrehovedet indstilles til en læg-på-lager-standardplacering. Bogføring af montageordren fungerer derefter som bogføring af læg-på-lager. Lageraktiviteten til at flytte montageelementer til lageret kan administreres på siden **Intern flytning** uden relation til montageordren.  

 Der findes følgende montagestrømme.  

|Workflow|Beskrivelse|  
|----------|---------------------------------------|  
|Montage til lager|Komponenterne skal bruges på en montageordre, hvor outputtet gemmes i lageret.<br /><br /> Dette lagerflow administreres på siden **Flytning (lager)**. En tag-linje angiver, hvor komponenterne skal tages. En placeringslinje angiver, hvor komponenterne skal placeres.|  
|Montage til ordre|Komponenterne, der skal bruges på en montageordre, der er knyttet til en salgsordre, der leveres, når den solgte vare er monteret.|  

> [!NOTE]  
>  Hvis varer samles til ordre, udløser lagerpluk af den tilknyttede salgsordre en flytning (lager) for alle de involverede montagekomponenter, ikke blot for den solgte vare som ved levering af lagervarer.  

 Felterne **Placeringskode til til-montage**, **Placeringskode til fra-montage** og **Pla.kode til ordremontagelev.** på lokationskortet definerer standardflow til og fra montageområder.  

> [!NOTE]  
>  Feltet **Pla.kode til ordremontagelev.** fungerer som fra-montageplaceringen i montage til ordre-scenarier.  

### <a name="ad-hoc-movements"></a>Ad hoc-flytninger  
 I grundlæggende lagerfunktioner styres flytning af varer fra placering til placering uden relation til kildedokumenter på siden **Intern flytning**, der fungerer sammen med siden **Flytning (lager)**.  

 En anden måde, hvorpå varer kan flyttes ad hoc mellem placeringer, er ved at bogføre positive poster i feltet **Ny placeringskode** på siden **Vareomposteringskladde**.  

## <a name="internal-flows-in-advanced-warehousing"></a>Interne strømme i avanceret logistik  
 I avancerede lageropsætninger centrerer gennemstrømningen af varer mellem placeringer i virksomheden omkring pluk af komponenter og at lægge varer til produktionsordrer på lager og plukke komponenter til montageordrer. Desuden opstår interne strømme som ad hoc-bevægelser, såsom placeringsgenopfyldninger, uden relation til kildedokumenter.  

### <a name="flows-to-and-from-production"></a>Flows til og fra Produktion  
 Den vigtigste integration mellem produktionsordrer og avancerede lageraktiviteter er repræsenteret af muligheden for at plukke produktionskomponenter, på siden **Pluk (logistik)** og **Plukkladde**, og muligheden for at lægge producerede varer på lager med siden **Intern læg-på-lager-aktivitet**.  

 Et andet integrationspunkt i produktionen er angivet på siden **Bevægelse (logistik)** sammen med siden Bevægelseskladde, som gør det muligt at placere komponenter og tage producerede varer for frigivne produktionsordrer.  

 Felterne **Til-produktionsplaceringskode**, **Fra-produktionsplaceringskode** og **Åben prod.placeringskode** på lokationskortet eller produktionsressource/arbejdscenterkortene definerer standardflow til og fra produktionsområder.  

 Hvis du ønsker yderligere oplysninger om, hvordan komponentforbrug tømmes fra produktionsplaceringen eller den åbne produktionsplacering, kan du se afsnittet "Træk af produktionskomponenter i lageret" i dette emne.  

### <a name="flows-to-and-from-assembly"></a>Flows til og fra Montage  
 Den vigtigste integration mellem montageordrer og avancerede lageraktiviteter er repræsenteret af muligheden for at plukke montagekomponenter, begge med siderne **Pluk (logistik)** og **Plukkladde**. Denne funktion fungerer ligesom ved pluk af komponenter til produktionsordrer.  

 Da der ikke findes nogen specifikke lagerfunktioner til at lægge montageelementer på lager, kan placeringskoden på montageordrehovedet indstilles til en læg-på-lager-standardplacering. Bogføring af montageordren fungerer derefter som bogføring af læg-på-lager. Lageraktiviteten til at flytte montageelementer til lageret kan administreres på siden **Bevægelseskladde** eller på siden **Intern læg-på-lager-aktivitet** med uden relation til montageordren.  

> [!NOTE]  
>  Hvis varer samles til ordre, udløser lagerleveringen af den tilknyttede salgsordre et lagerpluk for alle de involverede montagekomponenter, ikke blot for den solgte vare som ved levering af lagervarer.  

 Felterne **Placeringskode til til-montage** og **Placeringskode til fra-montage** på lokationskortet definerer standardflow til og fra montageområder.  

### <a name="ad-hoc-movements"></a>Ad hoc-flytninger  
 I avancerede lagerfunktioner styres flytning af varer fra placering til placering uden relation til kildedokumenter på siden **Bevægelseskladde** og registreres på siden Bevægelse (logistik).  

## <a name="flushing-production-components-in-the-warehouse"></a>Træk af produktionskomponenter i lageret  
 Hvis det er angivet på varekortet, bliver komponenter, der plukkes med lagerpluk, bogført som forbrugt af produktionsordren, når lagerpluk er registreret. Ved hjælp af metoden **Pluk + Forlæns** og trækmetoden **Pluk + Baglæns**, udløser plukregistreringen den relaterede forbrugsbogføring henholdsvis, når den første handling starter, eller når den sidste handling afsluttes.  

 Forestil dig følgende scenarie, der er baseret på [!INCLUDE[prod_short](includes/prod_short.md)]-demodatabasen.  

 Der findes en produktionsordre for 15 stk. af vare LS-100. Nogle af varerne på komponentlisten skal trækkes manuelt i en forbrugskladde, og andre varer på listen kan plukkes og trækkes automatisk ved hjælp af metoden **pluk + baglæns**.  

> [!NOTE]  
>  **Pluk + Forlæns** fungerer kun, hvis den anden rutelinje for produktion bruger en rutebindingskode. Frigivelse af en planlagt produktionsordre starter forlæns træk af komponenter, der er angivet til **Pluk + Forlæns**. Men træk kan ikke finde sted, før pluk af komponenter er registreret, som igen kun kan finde sted, når ordren er frigivet.  

 De følgende trin beskriver de handlinger, der er involveret for forskellige brugere, og de relaterede svar:  

1.  Den tilsynsførende frigiver produktionsordren. Elementer med **Fremad** som trækmetode og ingen rutebindingskode bliver fratrukket åben produktionsplacering.  
2.  Den tilsynsførende vælger knappen **Opret pluk (logistik)** på produktionsordren. Der oprettes et lagerplukdokument for varer med trækmetoderne **Manuel**, **Pluk + Baglæns** og **Pluk + Forlæns**. Disse varer placeres på produktionsplaceringen.  
3.  Lagerchefen tildeler pluk til en lagermedarbejder.  
4.  Lagermedarbejderen plukker varerne fra relevante placeringer og placerer dem på produktionsplaceringen eller på placeringen, der er angivet på lagerplukket, hvilket kan være et arbejdscenter- eller en produktionsressourceplacering.  
5.  Lagermedarbejderen registrerer plukket. Antallet trækkes fra plukplaceringerne og føjes til forbrugsplaceringen. Feltet **Plukket antal** på komponentlisten for alle de plukkede varer opdateres.  

    > [!NOTE]  
    >  Kun det antal, der er plukket, kan forbruges.  

6.  Maskinoperatøren oplyser produktionschefen om, at færdigvarerne er klar.  
7.  Den tilsynsførende bruger forbrugskladden eller produktionskladden til at bogføre forbruget af komponentvarer, som enten bruger en **manuel** trækmetode eller **Forlæns**- eller **Pluk + Forlæns**-trækmetoder sammen med rutebindingskoder.  
8.  Produktionschefen bogfører afgang for produktionsordren og ændrer status til **Udført**. Antallet af komponentvarer, der bruger **baglæns**-trækmetoden, trækkes fra den åbne produktionsplacering, og antallet af komponentvarer, der bruger **pluk + baglæns**-trækmetoden trækkes fra produktionsplaceringen.  

 Følgende illustration viser, når feltet **Placeringskode** på komponentlisten udfyldes i overensstemmelse med konfiguration af din lokation eller maskine/arbejdscenter.  

 ![Oversigt over, hvornår/hvordan feltet Placeringskode skal udfyldes](media/binflow.png "Oversigt over, hvornår/hvordan feltet Placeringskode skal udfyldes")  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Logistik](design-details-warehouse-management.md)
