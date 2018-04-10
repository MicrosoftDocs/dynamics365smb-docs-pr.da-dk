---
title: Administrere, slette eller komprimere dokumenter | Microsoft Docs
description: Beholde dine historiske data eller slette dem.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 696100bfbcc987b1d684e7987e7fd43979813282
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="manage-documents"></a>Administrere dokumenter
En central rolle, f.eks. som programadministrator, skal regelmæssigt håndtere store mængder akkumulerede oversigtsdokumenter, der skal slettes eller komprimeres.  

## <a name="delete-documents"></a>Slet dokumenter
Du kan i visse situationer have behov for at slette fakturaer. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer, om de slettede købsordrer er fuldt faktureret. Du kan kun slette ordrer, hvis de er blevet fuldt faktureret og modtaget.  

Returvareordrer slettes normalt, når de er faktureret. Når en faktura bogføres, overføres den til vinduet **Bogført købskreditnota**. Hvis afkrydsningsfeltet **Returvarekvit. på kreditnota** er markeret i vinduet **Købsopsætning**, overføres fakturaen til vinduet **Bogført returvareleverance**. Du kan slette dokumenter ved hjælp af kørslen **Slet fakt. købsreturvareordrer**. Før du sletter, kontrollerer kørslen, om købsreturvareordreordrer er fuldt leveret og faktureret.  

Rammekøbsordrer slettes ikke, når du har behandlet og faktureret alle relaterede købsordrer. Du kan slette rammeordrer med kørslen **Slet fak. rammekøbsordrer**.  

Fakturerede serviceordrer slettes som regel automatisk, når de er faktureret fuldt ud. Når en faktura bogføres, oprettes der en tilsvarende post i vinduet **Bogførte servicefakturaer**. Det bogførte dokument kan ses i vinduet **Bogført servicefaktura**.  

Serviceordrer slettes ikke automatisk i programmet, men hvis det samlede antal i ordren er bogført, ikke fra selve serviceordren, men fra vinduet **Servicefaktura**. Det kan i så fald være nødvendigt at slette fakturerede ordrer, der ikke er slettet. Det kan du gøre ved at aktivere kørslen **Slet fakturerede serviceordrer**.  

## <a name="see-also"></a>Se også  
[Opsætning](admin-setup-and-administration.md)  

