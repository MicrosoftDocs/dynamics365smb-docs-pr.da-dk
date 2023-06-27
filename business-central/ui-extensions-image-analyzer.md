---
title: Billedanalyseudvidelsen
description: 'Med denne udvidelse kan du analysere billeder af kontaktpersoner og varer for at finde attributter, så du hurtigt kan tildele dem i Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition'
ms.search.form: '2026, 2027, 2029,'
ms.date: 05/19/2021
ms.author: bholtorf
---

# <a name="the-image-analyzer-extension"></a>Billedanalyseudvidelsen

Billedanalyseudvidelsen bruger effektiv billedanalyse fra Computer Vision API'en til Azure Cognitive Services til at registrere attributter i de billeder, du importerer til varer og kontaktpersoner, så du let kan gennemse og tildele dem. For varer kan attributterne dreje sig om, hvorvidt varen er et bord eller en bil, og om den er rød eller blå. For kontaktpersoner kan attributterne vedrøre køn eller alder.

Billedanalysefunktionen foreslår attributter baseret på koder, der bliver fundet af Computer Vision API og et tillidsniveau. Som standard foreslås attributter kun, hvis der er mindst 80 % sikkerhed for, at attributten er korrekt. Du kan angive et andet tillidsniveau, hvis det er nødvendigt. Du kan finde flere oplysninger om, hvordan koder og tillidsniveauer fastlægges i [Computer Vision-API](https://go.microsoft.com/fwlink/?linkid=851476).  

Billedanalyseudvidelsen er gratis i [!INCLUDE[prod_short](includes/prod_short.md)], men der er en grænse for, hvor mange varer du kan analysere i en bestemt periode. Som standard kan du analysere 100 billeder pr. måned.

Når du har aktiveret udvidelsen, kører billedanalysefunktionen, hver gang du importerer et billede til en vare eller kontaktperson. Du får vist attributter, tillidsniveau og oplysninger med det samme og kan beslutte, hvad der skal gøres med hver attribut. Hvis du har importeret billeder, før du aktiverede billedanalyseudvidelsen, skal du gå til varen eller kontakten og vælge handlingen **Analysér billede**.  

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Denne udvidelse bruger Computer Vision-API'en fra Azure Cognitive Services, som kan have forskellige niveauer af overensstemmelsesforpligtelser i forhold til [!INCLUDE[prod_short](includes/prod_short.md)]. Når du aktiverer udvidelsen Image Analyzer filtypen, sendes debitordata, f.eks. et billede af en kontaktperson, til Computer Vision-API'en. Ved at installere denne udvidelse, accepterer du, at dette begrænsede sæt af data sendes til Computer Vision-API'en. Bemærk, at du til enhver tid kan deaktivere og fjerne udvidelsen Image Analyzer for at afbryde brugen af denne funktion. Du kan finde flere oplysninger i [Microsofts sikkerhedscenter](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Krav

Der er nogle krav til billederne:

* Billedformater: JPEG, PNG, GIF, BMP  
* Maksimal filstørrelse: mindre end 4 MB  
* Billeddimensioner: større end 50 x 50 pixel  

## <a name="switch-on-the-image-analyzer-extension"></a>Aktiver billedanalyseudvidelsen

Billedanalyseudvidelsen er indbygget i [!INCLUDE[prod_short](includes/prod_short.md)]. Du skal blot aktivere den.

> [!NOTE]  
> Du skal være administrator for at aktivere billedanalyseudvidelsen. Kontroller, at du har fået tildelt brugerrettighedssættet **SUPER**. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).

Gør ét af følgende for at aktivere billedanalyseudvidelsen:

* Åbn et vare- eller kontaktkort. Vælg **Analysér billede** på meddelelseslinjen, og følg derefter trinnene i den assisterende opsætningsvejledning.  
* Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Serviceforbindelser**, og vælg derefter **Opsætning af billedanalyse**. Marker afkrydsningsfeltet **Aktivér billedanalyse**, og fuldfør derefter trinnene i den assisterende opsætningsvejledning.  

    > [!TIP]  
    > På siden **Opsætning af billedanalyse** kan du også ændre graden af tillid for attributforslag. Hvis du f.eks. ønsker en større grad af tillid, kan du angive en højere procentsats.

## <a name="analyze-an-item-image"></a>Analysere et billede af en vare

Nedenfor beskrives det, hvordan du kan analysere et billede, der er blevet indlæst, før du har aktiveret billedanalyseudvidelsen.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2. Vælg vare, og vælg derefter handlingen **Analysér billede**.  
3. På siden **Billedanalyseattributter** vises de registrerede attributter, tillidsniveauet og andre oplysninger om attributten. Brug **Handlingen til at udføre**-indstillinger for at angive, hvad der skal ske med attributten, eller Vælg **Tilføj til varebeskrivelse** for at føje navnet på attributten til varebeskrivelsen. Denne handling er f.eks. velegnet til hurtigt at tilføje detaljer.

Feltet **Handling, der skal udføres** har følgende muligheder:

| Handling | Beskrivelse |
| ------ | ----------- |
| *Ignorer* | Der udføres ingen handlinger. |
| *Brug som attribut* | Værdien føjes til vareattributterne. Flere oplysninger i [Arbejde med vareattributter](inventory-how-work-item-attributes.md). |
| *Bruge som kategori* | Den markerede værdi tilføjes som en kategori. Flere oplysninger i [Kategorisere varer](inventory-how-categorize-items.md). |
| *Føj til blokliste* | Hvis analysen foreslår en attribut, som du ikke vil have vist, kan du blokere den. Men gå forsigtigt frem. Blokerede attributter foreslås heller ikke for andre varer. Hvis du fortryder blokeringen af en attribut, kan du vælge **Vis blokerede attributter** og derefter slette attributten fra listen. |

> [!NOTE]  
> Som standard viser **Vareattributter** attributter, hvor **Tillidsscore** er større end **Tærsklen for tillidsscore %** defineret i **Opsætning af billedanalyse**. Hvis du vil se alle fundne attributter, skal du vælge handlingen **Vis alle attributter**.

## <a name="analyze-a-contact-person-picture"></a>Analyse af billede af en kontaktperson

Nedenfor beskrives det, hvordan du kan analysere et billede, der er blevet indlæst, før du har aktiveret billedanalyseudvidelsen.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontakter**, og vælg derefter det relaterede link.  
2. Vælg kontaktpersonen, og vælg derefter handlingen **Analysér billede**.  
3. I oversigtspanelet **Profilspørgeskema** skal du gennemgå forslagene og foretage rettelser, hvis det er nødvendigt. Flere oplysninger [Bruge profilspørgeskemaer til at klassificere forretningskontakter](marketing-create-contact-profile-questionnaire.md).  

    > [!NOTE]  
    >
    > Computer vision API returnerer følgende attributter:
    >
    > * *alder*
    >
    >     En anslået "visuel alder" i år. Det er den måde, gamle en person ser ud i modsætning til den faktiske biologiske alder.
    > * *køn*
    >
    >    Mand eller kvinde.
    >
    > Computerens API returnerer ikke et tillidsniveau for alder og køn.
  
## <a name="use-your-own-computer-vision-api-account"></a>Brug af din egen konto til Computer Vision API

Du kan også bruge din egen konto til Computer Vision API'en, f.eks. hvis du vil analysere flere billeder, end standardintegrationen tillader.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af billedanalyse**, og vælg derefter det relaterede link.
2. Angiv **URI for API** og **API-nøgle**, du har modtaget Computer Vision API.  

    > [!NOTE]  
    > Du skal tilføje **/analysere** i slutningen af API-URI'en, hvis det ikke allerede står der. Eksempel: ```https://cronus.api.cognitive.microsoft.com/vision/v2.0/analyze```.

## <a name="see-how-many-analyses-you-have-left-in-the-current-period"></a>Se, hvor mange analyser du har udfyldt i den aktuelle periode

Du kan få vist antallet af analyser, du har udført, og hvor mange du stadig kan udføre, i den aktuelle periode.  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af billedanalyse**, og vælg derefter det relaterede link.
2. Felterne **Grænsetype**, **Grænseværdi** og **Udførte analyser** oplyser om forbruget.  

## <a name="stop-using-the-image-analyzer-extension"></a>Afslut brug af billedanalyseudvidelsen

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Serviceforbindelser**, og vælg derefter **Opsætning af billedanalyse**.  
2. Fjern markeringen i feltet **Aktiver billedanalyse**.  

Du kan også fjerne udvidelsen fuldstændigt. Du kan altid hente den igen fra AppSource. Du kan finde flere oplysninger i [Installation og fjernelse af udvidelser i Business Central](ui-extensions-install-uninstall.md#uninstall-an-app).  

## <a name="see-also"></a>Se også

[Arbejde med vareattributter](inventory-how-work-item-attributes.md)  
[Kategorisere varer](inventory-how-categorize-items.md)  
[Bruge profilspørgeskemaer til at klassificere forretningskontakter](marketing-create-contact-profile-questionnaire.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Blive køreklar](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
