---
title: "Sådan konfigureres nye virksomheder | Microsoft Docs"
description: "Du kan konfigurere og tilpasse en ny virksomhed, som du har oprettet. Hvis du vil finjustere din implementering, skal du fortsætte i tre faser for at fuldføre konfigurationen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 22c79e4a878f474b29831d86b613a80184395d99
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="configure-new-companies"></a>Konfigurere nye virksomheder
Hvis du vil konfigurere en ny virksomhed i løsningsimplementeringen, følger du typisk tre faser. I den første fase indlæser du konfigurationspakken, der er en .rapidstart-fil med konfigurationsoplysningerne. I anden fase skal du ændre konfigurationsoplysningerne og derefter anvende dem på din nye virksomhed. I den endelige fase skal du finde og rette eventuelle fejl.  

Følgende procedurer forudsætter, at du har oprettet og gemt en konfigurationspakke. Du kan finde flere oplysninger i [Forberede en konfigurationspakke](admin-how-to-prepare-a-configuration-package.md).  

I nedenstående procedurer forudsættes det, at du har initialiseret og åbnet din nye virksomhed, og at du bruger rollecentret RapidStart Services-implementering

## <a name="to-import-a-configuration-package"></a>Importere en konfigurationspakke  
1. Åbn den nye virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen.  
2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationspakker**, og vælg derefter det relaterede link.  
3. Vælg handlingen **Indlæs pakke**.  
4. Gå til det sted, hvor du har gemt .rapidstart-filen med konfigurationspakken, og vælg derefter knappen **Åbn**.  
5. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomhedsoplysninger**, og vælg derefter det relaterede link. Angiv oplysninger om virksomheden på virksomhedsoplysningskortet. Medtag oplysninger som f.eks. bankdetaljer. Du kan også angive et logo for virksomheden.  

Alle de tabeller, du har angivet til medtagelse i den nye virksomhed, importeres. På dette tidspunkt kan du anvende pakkedata på databasen eller justere og ændre tabeldata for at opfylde dine kundespecifikationer.  

## <a name="to-apply-package-data"></a>Overføre pakkedata  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationskladde**, og vælg derefter det relaterede link.  
2. Vælg en tabel, du vil ændre data for, og vælg derefter handlingen **Anvend data**. Vælg knappen **Ja** for at bekræfte anvendelsen.
3. Hvis du vil bekræfte, at dataene nu er i databasen, og at anvendelsen er lykkedes, skal du vende tilbage til vinduet **Konfig.kladde** og vælge handlingen **Databasedata**.  

> [!NOTE]  
>  Når du har anvendt data, kan du kun se dem i databasen. De er ikke længere i pakken.  

## <a name="to-modify-and-apply-package-data"></a>Ændre og anvende pakkedata  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationskladde**, og vælg derefter det relaterede link.  
2. Vælg en tabel, du vil ændre data for, og vælg derefter handlingen **Pakkedata**.  
3. Foretag de ønskede ændringer i vinduet **Konfigurationspakkeposter**. Du kan f.eks. slette de indstillinger, du ikke kan anvende.  
4. Vælg handlingen **Anvend data**, og vælg derefter knappen **OK**.  
5. Hvis du vil bekræfte, at dataene nu er i databasen, og at anvendelsen er lykkedes, skal du vende tilbage til vinduet **Konfig.kladde** og vælge handlingen **Databasedata**.  

## <a name="to-locate-and-identify-a-configuration-error"></a>Du kan finde og identificere en konfigurationsfejl  
Der er visse typer fejl, der kan opstå, når du anvender data på en database. Den mest almindelige fejl er, at påkrævede relaterede tabeller ikke blev medtaget. Du kan rette disse fejl i konfigurationsregnearket.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationspakker**, og vælg derefter det relaterede link.  
2. Marker den pakke, som du vil gennemgå, og vælg derefter handlingen **Rediger**.  

    Alle tabeller, der har fejl, er fremhævet. Antallet af pakkefejl vises i feltet **Antal pakkefejl**.  

3. Vælg feltet **Antal pakkefejl** for at åbne vinduet **Konfigurationspakkeposter**, der viser en liste over poster med fejl.  

### <a name="to-fix-an-error"></a>Rette en fejl  
1. Åbn den virksomhed, som er baseret på konfigurationspakken.  
2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationskladde**, og vælg derefter det relaterede link.  
3. Ret fejl, f.eks. manglende relaterede tabeller til regnearket.  
4. Føj tabellerne til den eksisterende konfigurationspakke, eller opret en ny pakke, der kun indeholder de nye tabeller. Du kan finde flere oplysninger i [Forberede en konfigurationspakke](admin-how-to-prepare-a-configuration-package.md).  
5. Åbn den nye virksomhed, som du implementerer konfigurationen for, igen.  
6. Importér konfigurationspakken.  

    > [!NOTE]  
    >  Hvis du importerer den samme pakke igen, overskriver du alle dataændringer, som du allerede har foretaget. Derfor vil du muligvis føje nye tabeller til en ny pakke og importere den i stedet.  

7. Anvend dataene i databasen, som beskrevet i afsnittet "Ændre og anvende pakkedata".

## <a name="see-also"></a>Se også  
[Anvende konfigurationer på nye virksomheder](admin-apply-configuration-to-new-companies.md)  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)

