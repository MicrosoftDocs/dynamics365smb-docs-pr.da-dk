---
title: Bruge billedanalyseudvidelsen | Microsoft Docs
description: "Med denne udvidelse kan du analysere billeder af kontaktpersoner og varer for at finde attributter, så du hurtigt kan tildele dem i Finans."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 06/19/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c981c5528c7a622f9d78ed6a77c27e2ceeba44e3
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---

# <a name="the-image-analyzer-extension-for-microsoft-dynamics-365-for-financials"></a>Billedanalyseudvidelsen til Microsoft Dynamics 365 for Financials
Billedanalyseudvidelsen bruger effektiv billedanalyse fra Computer Vision API'en til Computer Vision API til at registrere attributter i de billeder, du importerer til varer og kontaktpersoner, så du let kan gennemse og tildele dem. For varer kan attributterne dreje sig om, hvorvidt varen er et bord eller en bil, og om den er rød eller blå. For kontaktpersoner kan attributterne vedrøre køn eller alder.

Billedanalysefunktionen foreslår attributter baseret på koder, der bliver fundet af Computer Vision API og et tillidsniveau. Som standard foreslås attributter kun, hvis der er mindst 80 % sikkerhed for, at attributten er korrekt. Du kan angive et andet tillidsniveau, hvis det er nødvendigt. Du kan finde flere oplysninger om, hvordan koder og tillidsniveauer fastlægges i [Computer Vision-API](https://go.microsoft.com/fwlink/?linkid=851476).  

Billedanalyseudvidelsen er gratis i [!INCLUDE[d365fin](includes/d365fin_md.md)], men der er en grænse for, hvor mange varer du kan analysere i en bestemt periode. Som standard kan du analysere 100 billeder pr. måned.

Når du har aktiveret udvidelsen, kører billedanalysefunktionen, hver gang du importerer et billede til en vare eller kontaktperson. Du får vist attributter, tillidsniveau og oplysninger med det samme og kan beslutte, hvad der skal gøres med hver attribut. Hvis du har importeret billeder, før du aktiverede billedanalyseudvidelsen, skal du gå til varen eller kontakten og vælge handlingen **Analysér billede**.  

>   [!NOTE]  
>   Hvis du aktiverer denne udvidelse, accepterer du, at Microsoft kan gemme dine data og bruge dem til at forbedre Microsoft-tjenester, f.eks. forbedre Computer Vision API'en. For at beskytte dine personlige oplysninger sørger vi for at gøre dine data anonyme og beskytte dem. Vi publicerer ikke dine data og lader ikke andre bruge dem. Du kan fjerne billedet fra varen i [!INCLUDE[d365fin](includes/d365fin_md.md)], men billedet findes stadig i Computer Vision API'en i dets ikke-identificerbare form. Du kan finde flere oplysninger i [Microsofts sikkerhedscenter](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Krav
Der er nogle krav til billederne:

* Billedformater: JPEG, PNG, GIF, BMP  
* Maksimal filstørrelse: mindre end 4 MB  
* Billeddimensioner: større end 50 x 50 pixel  

## <a name="blacklisting-suggested-attributes"></a>Sortlistning af foreslåede attributter
Hvis analysen foreslår en attribut, som du ikke vil have vist, kan du sortliste attributten. Men gå forsigtigt frem. Sortlistede attributter foreslås heller ikke for andre varer eller kontaktpersoner. Hvis du fortryder sortlistningen af en attribut, kan du vælge **Sortlistede attributter** og derefter slette attributten fra listen.

## <a name="to-enable-image-analyzer"></a>Sådan aktiveres billedanalysefunktionen
Billedanalyseudvidelsen er indbygget i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du skal blot aktivere den.

> [!NOTE]  
> Du skal være administrator for at aktivere billedanalyseudvidelsen. Kontroller, at du har fået tildelt brugerrettighedssættet **SUPER**.

1. Gør ét af følgende for at aktivere billedanalyseudvidelsen:
  
* Åbn et vare- eller kontaktkort. Vælg **Analysér billeder** på meddelelseslinjen, og følg derefter trinnene i den assisterende opsætningsvejledning.  
* Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceforbindelser**, og vælg derefter **Opsætning af billedanalyse**. Marker afkrydsningsfeltet **Aktivér billedanalyse**, og fuldfør derefter trinnene i den assisterende opsætningsvejledning.  

>   [!TIP]  
>   På siden **Opsætning af billedanalyse** kan du også ændre graden af tillid for attributforslag. Hvis du f.eks. ønsker en større grad af tillid, kan du angive en højere procentsats. 

## <a name="to-analyze-an-image-of-an-item"></a>Sådan analyseres et billede af en vare
Nedenfor beskrives det, hvordan du analyserer et billede, der er blevet indlæst, før du har aktiveret billedanalyseudvidelsen.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.  
2. Vælg vare, og vælg derefter handlingen **Analysér billede**.  
3. På siden **Billedanalyseattributter** vises de registrerede attributter, tillidsniveauet og andre oplysninger om attributten. Brug indstillingerne **Handling, der skal udføres** for at angive, hvad der skal gøres med attributten.  

>   [!TIP]  
>   Du kan føje navnet på attributten til varebeskrivelsen ved at vælge **Føj til varebeskrivelse**. Det er f.eks. velegnet til hurtigt at tilføje detaljer.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Sådan analyseres et billede af en kontaktperson
Nedenfor beskrives det, hvordan du analyserer et billede, der er blevet indlæst, før du har aktiveret billedanalyseudvidelsen.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontakter**, og vælg derefter det relaterede link.  
2. Vælg kontaktpersonen, og vælg derefter handlingen **Analysér billede**.  
3. I oversigtspanelet **Profilspørgeskema** skal du gennemgå forslagene og foretage rettelser, hvis det er nødvendigt.  

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Sådan bruger du din egen konto til Computer Vision API'en
Du kan også bruge din egen konto til Computer Vision API'en, f.eks. hvis du vil analysere flere billeder, end vi tillader.  
  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af billedanalyse**, og vælg derefter det relaterede link.  
2. Angiv **URI for API** og **API-nøgle**, du har modtaget Computer Vision API.  
  
>   [!NOTE]  
>   Du skal tilføje **/analysere** i slutningen af API-URI'en, hvis det ikke allerede står der. Eksempel: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Sådan ser du, hvor mange analyser du har udfyldt i den aktuelle periode
Du kan få vist antallet af analyser, du har udført, og hvor mange du stadig kan udføre, i den aktuelle periode.  
  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af billedanalyse**, og vælg derefter det relaterede link.  
2. **Grænsetype**, **Grænseværdi** og **Udførte analyser** oplyser om forbruget.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Sådan afslutter du brugen af billedanalyseudvidelsen
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceforbindelser**, og vælg derefter **Opsætning af billedanalyse**.  
2. Fjern markeringen i afkrydsningsfeltet **Aktiver billedanalyse**.  

## <a name="see-also"></a>Se også
[Fremgangsmåde: Arbejde med vareattributter](inventory-how-work-item-attributes.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Velkommen til [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  


