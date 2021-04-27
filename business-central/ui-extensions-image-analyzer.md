---
title: Bruge billedanalyseudvidelsen | Microsoft Docs
description: Med denne udvidelse kan du analysere billeder af kontaktpersoner og varer for at finde attributter, så du hurtigt kan tildele dem i Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 841ad4ff4963d8cfc6a284859affb60336e805a5
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771308"
---
# <a name="the-image-analyzer-extension"></a>Billedanalyseudvidelsen

Billedanalyseudvidelsen bruger effektiv billedanalyse fra Computer Vision API'en til Computer Vision API til at registrere attributter i de billeder, du importerer til varer og kontaktpersoner, så du let kan gennemse og tildele dem. For varer kan attributterne dreje sig om, hvorvidt varen er et bord eller en bil, og om den er rød eller blå. For kontaktpersoner kan attributterne vedrøre køn eller alder.

Billedanalysefunktionen foreslår attributter baseret på koder, der bliver fundet af Computer Vision API og et tillidsniveau. Som standard foreslås attributter kun, hvis der er mindst 80 % sikkerhed for, at attributten er korrekt. Du kan angive et andet tillidsniveau, hvis det er nødvendigt. Du kan finde flere oplysninger om, hvordan koder og tillidsniveauer fastlægges i [Computer Vision-API](https://go.microsoft.com/fwlink/?linkid=851476).  

Billedanalyseudvidelsen er gratis i [!INCLUDE[prod_short](includes/prod_short.md)], men der er en grænse for, hvor mange varer du kan analysere i en bestemt periode. Som standard kan du analysere 100 billeder pr. måned.

Når du har aktiveret udvidelsen, kører billedanalysefunktionen, hver gang du importerer et billede til en vare eller kontaktperson. Du får vist attributter, tillidsniveau og oplysninger med det samme og kan beslutte, hvad der skal gøres med hver attribut. Hvis du har importeret billeder, før du aktiverede billedanalyseudvidelsen, skal du gå til varen eller kontakten og vælge handlingen **Analysér billede**.  

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Denne udvidelse bruger Computer Vision-API'en fra Microsoft Cognitive Services, som kan have forskellige niveauer af overensstemmelsesforpligtelser i forhold til [!INCLUDE[prod_short](includes/prod_short.md)]. Når du aktiverer udvidelsen Image Analyzer filtypen, sendes debitordata, f.eks. et billede af en kontaktperson, til Computer Vision-API'en. Ved at installere denne udvidelse, accepterer du, at dette begrænsede sæt af data sendes til Computer Vision-API'en. Bemærk, at du til enhver tid kan deaktivere og fjerne udvidelsen Image Analyzer for at afbryde brugen af denne funktion. Du kan finde flere oplysninger i [Microsofts sikkerhedscenter](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Krav

Der er nogle krav til billederne:

* Billedformater: JPEG, PNG, GIF, BMP  
* Maksimal filstørrelse: mindre end 4 MB  
* Billeddimensioner: større end 50 x 50 pixel  

## <a name="to-enable-image-analyzer"></a>Sådan aktiveres billedanalysefunktionen

Billedanalyseudvidelsen er indbygget i [!INCLUDE[prod_short](includes/prod_short.md)]. Du skal blot aktivere den.

> [!NOTE]  
> Du skal være administrator for at aktivere billedanalyseudvidelsen. Kontroller, at du har fået tildelt brugerrettighedssættet **SUPER**.

1. Gør ét af følgende for at aktivere billedanalyseudvidelsen:

* Åbn et vare- eller kontaktkort. Vælg **Analysér billeder** på meddelelseslinjen, og følg derefter trinnene i den assisterende opsætningsvejledning.  
* Vælg ikonet ![Elpære, der åbner funktionen Fortæl Mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceforbindelser**, og vælg **Opsætning af billedanalyse**. Marker afkrydsningsfeltet **Aktivér billedanalyse**, og fuldfør derefter trinnene i den assisterende opsætningsvejledning.  

    > [!TIP]  
    > På siden **Opsætning af billedanalyse** kan du også ændre graden af tillid for attributforslag. Hvis du f.eks. ønsker en større grad af tillid, kan du angive en højere procentsats.

## <a name="to-analyze-an-image-of-an-item"></a>Sådan analyseres et billede af en vare

Nedenfor beskrives det, hvordan du kan analysere et billede, der er blevet indlæst, før du har aktiveret billedanalyseudvidelsen.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.  
2. Vælg vare, og vælg derefter handlingen **Analysér billede**.  
3. På siden **Billedanalyseattributter** vises de registrerede attributter, tillidsniveauet og andre oplysninger om attributten. Brug indstillingerne **Handling, der skal udføres** for at angive, hvad der skal gøres med attributten.  

    > [!TIP]  
    > Du kan føje navnet på attributten til varebeskrivelsen ved at vælge **Føj til varebeskrivelse**. Det er f.eks. velegnet til hurtigt at tilføje detaljer.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Sådan analyseres et billede af en kontaktperson

Nedenfor beskrives det, hvordan du kan analysere et billede, der er blevet indlæst, før du har aktiveret billedanalyseudvidelsen.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontakter**, og vælg derefter det relaterede link.  
2. Vælg kontaktpersonen, og vælg derefter handlingen **Analysér billede**.  
3. I oversigtspanelet **Profilspørgeskema** skal du gennemgå forslagene og foretage rettelser, hvis det er nødvendigt.  

## <a name="block-suggested-attributes"></a>Blokere foreslåede attributter

Hvis analysen foreslår en attribut, som du ikke vil have vist, kan du blokere den. Men gå forsigtigt frem. Blokerede attributter foreslås heller ikke for andre varer eller kontaktpersoner. Hvis du fortryder blokeringen af en attribut, kan du vælge **Vis blacklistede attributter** og derefter slette attributten fra listen.

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Sådan bruger du din egen konto til Computer Vision API'en

Du kan også bruge din egen konto til Computer Vision API'en, f.eks. hvis du vil analysere flere billeder, end vi tillader.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af billedanalysatoren**, og vælg derefter det relaterede link.  
2. Angiv **URI for API** og **API-nøgle**, du har modtaget Computer Vision API.  

    > [!NOTE]  
    > Du skal tilføje **/analysere** i slutningen af API-URI'en, hvis det ikke allerede står der. Eksempel: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Sådan ser du, hvor mange analyser du har udfyldt i den aktuelle periode

Du kan få vist antallet af analyser, du har udført, og hvor mange du stadig kan udføre, i den aktuelle periode.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af billedanalysatoren**, og vælg derefter det relaterede link.  
2. **Grænsetype**, **Grænseværdi** og **Udførte analyser** oplyser om forbruget.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Sådan afslutter du brugen af billedanalyseudvidelsen

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl Mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceforbindelser**, og vælg **Opsætning af billedanalysatoren**.  
2. Fjern markeringen i afkrydsningsfeltet **Aktiver billedanalyse**.  

## <a name="see-also"></a>Se også

[Arbejde med vareattributter](inventory-how-work-item-attributes.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Blive køreklar](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]