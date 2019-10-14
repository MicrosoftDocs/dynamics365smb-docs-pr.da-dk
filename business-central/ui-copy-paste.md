---
title: Kopiere og indsætte data
description: Kopier felter og rækker fra Business Central-sider, og indsæt dem et andet sted.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a77c5bcadb15cd1180fc102a1f15881d0cc5db5a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315656"
---
# <a name="copy-and-paste-faq"></a>Ofte stillede spørgsmål om kopiering og indsætning
Du kan kopiere en eller flere rækker (poster) fra en liste eller et enkelt felt på en side og derefter indsætte det, du har kopieret på den samme side, en anden side eller et eksternt dokument (som Microsoft Excel og e-mails i Outlook). Kort sagt, når du vil kopiere, skal du trykke på CTRL + C (cmd + C i macOS) på tastaturet. Når du vil indsætte, skal du trykke på CTRL + V (cmd + V i macOS).

Der er mange andre tastaturgenveje til kopiering og indsætning, som hjælper dig med spare tid, når du indtaster data. Du kan finde flere oplysninger om dem i [Tastaturgenveje](keyboard-shortcuts.md#CopyRows).

Denne artikel indeholder svar på almindelige spørgsmål om kopiering og indsætning.  

## <a name="what-can-i-copy-and-paste"></a>Hvad kan jeg kopiere og indsætte?
- Kopier en eller flere rækker i [!INCLUDE[d365fin](includes/d365fin_md.md)] på samme liste eller til en liste med identiske kolonner.
- Kopier en eller flere rækker i [!INCLUDE[d365fin](includes/d365fin_md.md)] og indsæt dem i Excel eller andre programmer.
- Kopier en eller flere rækker i Excel, og indsæt dem på en [!INCLUDE[d365fin](includes/d365fin_md.md)]-liste.
- Kopiér værdien af et enkelt felt i [!INCLUDE[d365fin](includes/d365fin_md.md)] og indsæt den hvor som helst.

## <a name="does-copy-and-paste-work-with-tiles"></a>Kan kopier og indsæt bruges i felter?
Ja, men kun for et enkelt markeret felt.

## <a name="how-do-i-copy-a-row"></a>Hvordan kopierer jeg en række?
Du kan kopiere en enkelt række ved at markere den og derefter trykke på Ctrl + C.

Hvis du vil kopiere flere rækker, kan du:
- Tryk på Ctrl + klik på en anden række, eller tryk på Skift + klik for at markere rækken og alle rækker indimellem. Se [Tastaturgenveje](keyboard-shortcuts.md#CopyRows) for flere mus- og tastaturkombinationer til markering af rækker.
- Vælg ![Vis flere indstillinger](media/show-more-options-icon.png "Ikonet Vis flere indstillinger") i den første kolonne for at vælge **Vælg flere**, marker afkrydsningsfeltet ud for hver række, du vil kopiere, og tryk på Ctrl + C.

## <a name="how-do-i-paste-rows"></a>Hvordan indsætter jeg rækker?
Marker en tom række, med fokus i en celle, og tryk derefter på Ctrl + V.

Hvis du vil erstatte eksisterende rækker, skal du markere rækkerne og derefter trykke på Ctrl + V. I dette tilfælde kan du kun indsætte det samme antal rækker, som du har markeret.

> [!NOTE]
> Den liste, du indsætter, skal kunne redigeres.

<!-- Rows are pasted directly where your cursor is located. If you paste into an empty line, any existing subsequent lines will be moved after the pasted lines. If you paste into an existing line or lines, this will be overwritten.-->

## <a name="can-i-paste-rows-into-an-outlook-email"></a>Kan jeg indsætte rækker i en Outlook-e-mail?
Ja. Dette indsættes som en flot formateret tabel, som bevarer indrykning, numerisk justering og farve, som de vises i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="in-which-lists-can-i-copy-and-paste-rows"></a>I hvilke lister kan jeg kopiere og indsætte rækker?
Du kan kopiere rækker i enhver liste, herunder regneark, faktabokse eller lister, der er integrerede på en side (som linjer i en salgsordre). Men hvis du vil indsætte rækker, skal listen kunne redigeres.

På nogle sider kan programdesignet forhindre, at du kan indsætte rækker. Kontakt systemadministratoren eller programudvikleren for at ændre [egenskaben Redigerbar](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) på siden eller [egenskaben PasteIsValid](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-pasteisvalid-property) i kildetabellen.

## <a name="on-which-clients-is-copy-and-paste-available"></a>I hvilke klienter findes kopiere og indsætte?
Kopier og indsæt findes i browseren eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-appen til Windows 10.

## <a name="what-is-the-maximum-number-of-rows-that-can-be-copied"></a>Hvor mange rækker kan kopieres som maksimum?
Du kan kopiere så mange rækker, som du har rullet ind i visningen. F.eks. for at kopiere alle 1000 rækker på en side skal du først rulle til bunden af siden og vente, indtil rækkerne vises, før du kopierer. Det maksimale antal rækker, du kan kopiere, begrænses kun af hukommelsen på enheden.

## <a name="must-i-have-the-exact-same-number-of-columns-when-pasting-rows"></a>Skal jeg have nøjagtig samme antal kolonner, når jeg indsætter rækker?
Ja. Uanset om du kopierer fra [!INCLUDE[d365fin](includes/d365fin_md.md)], fra Excel eller fra en anden tabelkilde, skal de rækker, du indsætter i [!INCLUDE[d365fin](includes/d365fin_md.md)], have nøjagtigt tilsvarende antal kolonner - ikke flere ikke færre.

## <a name="why-do-i-get-errors-when-pasting-rows"></a>Hvorfor vises der fejlmeddelelser, når jeg indsætter rækker?
Når du indsætter i [!INCLUDE[d365fin](includes/d365fin_md.md)], kontrolleres hver række for at sikre, at værdierne i hver kolonne er gyldige. Hvis en kolonne indeholder en værdi, der ikke er gyldig, standes indsætningen, og der vises en fejlmeddelelse. For at undgå dette, skal du kontrollere, at kolonnerne har gyldige værdier, før du indsætter dem.


## <a name="see-also"></a>Se også
[Hjælpefunktioner](ui-accessibility.md)  
[Introduktion](product-get-started.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ofte stillede spørgsmål](across-faq.md)  
