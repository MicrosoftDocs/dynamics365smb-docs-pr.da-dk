---
title: Tilføje marketingtekst til varer
description: Skrive marketingtekst for varer i Business central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 12/13/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# <a name="add-marketing-text-to-items"></a>Tilføje marketingtekst til varer

Du kan skrive *marketingtekst* om varen for alle de varer, der er registreret i Business central. Selvom marketingtekst er en slags beskrivelse, er den forskellig fra en vares **Beskrivelsesfelt**. Feltet **Beskrivelse** bruges typisk som et kort vist navn til at identificere produktet hurtigt. Marketingteksten er derimod en mere omfattende og beskrivende tekst. Formålet er at tilføje marketing- og reklameindhold, også kendt som *kopi*. Denne tekst kan derefter publiceres med varen, hvis den er publiceret på en webshop, f.eks. Shopify, eller indsat i e-mails eller anden kommunikation med dine kunder.

Der er to måder at oprette en marketingtekst på. Den nemmeste måde at komme i gang på er ved at bruge Copilot, som foreslår AI-genereret tekst for dig. Den anden måde er at starte fra bunden. 

## <a name="get-marketing-text-suggestions-with-copilot"></a><a name=copilot></a>Hent marketingtekstforslag med Copilot

Med Copilot kan du hurtigt få et tekstforslag, der bliver genereret automatisk til dig. Den AI-genererede tekst er skræddersyet til elementet og er et godt udgangspunkt. Teksten er baseret på en del af følgende oplysninger:

- Definerede attributter for varen - f.eks. beskrivelse, farve, dimensioner, materialer osv. [Flere oplysninger i vareattributter](inventory-how-work-item-attributes.md).
- Varens **beskrivelse**-felt.
- Varekategori. [Flere oplysninger om at kategorisere varer](inventory-how-categorize-items.md).
- Indstillinger, der kan vælges som samtalens tone, format og længde.

Copilot er designet til at spare dig tid og hjælpe dig med at skrive kreativ og engagerende tekst, der afspejler dit varemærke og stemmer overens med produktlinjen. Start med at generere et forslag, og ret derefter den foreslåede tekst efter behov.

### <a name="prerequisites"></a>Forudsætninger

- Funktionen Forslag til marketingtekst er aktiveret og aktiveret i dit miljø. Denne opgave er udføres typisk af en administrator. Du kan finde flere oplysninger i [Konfigurere Copilot og AI-funktioner](enable-ai.md).
- Du bruger et af de sprog, der aktuelt understøttes af forslagene til marketingtekster.

  [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

  Hvis du vil skifte sprog, skal du i øverste højre hjørne vælge ikonet **Indstillinger** ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") > **Mine indstillinger** > **Sprog**. Du kan finde flere oplysninger i [Ændre grundlæggende indstillinger](ui-change-basic-settings.md#language).
- Gennemgå [Ofte stillede spørgsmål for markedsføringstekstforslag](faqs-marketing-text.md) for at lære, hvordan AI anvendes.

### <a name="create-first-draft-with-copilot"></a>Oprette første kladde med Copilot

Udfør følgende trin for at føje marketingtekst til en eksisterende vare. Du kan finde flere oplysninger om, hvordan du opretter en ny vare, i [Registrere nye varer](inventory-how-register-new-items.md).

1. Åbn den vare, du vil tilpasse, i Business Central, ved at fuldføre følgende trin:

   - I øverste højre hjørne skal du vælge den ![Lightbulb, der åbner funktionen Fortæl mig 22.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Varer**, og vælg derefter det relaterede link for at vise en liste over tilgængelige varer.

   - Dobbeltklik på varen, eller vælg dets værdi i **Nummer** kolonne .

   [![Viser et varekort med marketing tekstrude](media/create-with-copilot.svg)](media/create-with-copilot.svg#lightbox)

2. På varekortet kan du komme i gang med at skrive marketingtekst med Copilot. Gør ét af følgende:

   - Vælg **Udarbejd forslag med Copilot** i højre side af ruden **Marketingtekst**. 
   
     Copilot begynder at udarbejde marketingteksten. 

   - Vælg handlingen **Marketingtekst** øverst på siden, og vælg derefter **Kladde med Copilot** i vinduet **Rediger marketingtekst**.  Vinduerne **Kladde til marketingtekst med Copilot** vises med alle tilgængelige attributter for varen.
   
     ![Viser vinduet med redigering af marketingtekst](media/marketing-text-copilot-attributes.svg)

     Vælg de attributter, du vil have Copilot-basisforslag på, og vælg derefter **Generer**. Du kan ændre de valgte attributter og andre indstillinger senere. Copilot begynder at udarbejde marketingteksten. 
     
3. Når Copilot færdiggør kladden, vises teksten i Copilot-editorvinduet til gennemgang og redigering. 

   [![Viser vinduerne Opret med Copilot](media/create-with-copilot-window.svg)](media/create-with-copilot-window.svg#lightbox)

   Du kan nu få flere forslag, forsøge at forbedre de forslag, du får, redigere tekst m.m. Gå til [Gennemsyn, Rediger og Gem](#review-edit-and-save-text) for at få flere oplysninger.


### <a name="review-edit-and-save-text"></a>Gennemse, rediger og gem tekst

Når du har den første kladde, skal du gennemse den og foretage ændringer i teksten for at gøre den klar til udgivelse. Dette arbejde udføres fra Copilot-redigeringssiden, hvor du kan få flere forslag, ændre præferencerne, så de har indflydelse på forslagene, og manuelt foretage ændringer og typografi i teksten.

> [!IMPORTANT]
> Den AI-genererede tekst fra Copilot er kun et forslag, og der kan opstå fejl. Det kræver humant overblik og gennemgang for at sikre, at det er nøjagtigt og hensigtsmæssigt. Gennemse eventuel foreslået tekst, og rediger efter behov, inden du gemmer og udgiver den til offentlig forbrug.

Følg nedenstående retningslinjer for at afslutte og gemme marketingteksten.

1. Foretage ændringer i teksten direkte i tekstfeltet. Brug værktøjslinjen nederst i boksen til at formatere og tilpasse tekst, tilføje links og meget mere.
2. Vælg **Gendan**, hvis du vil have et nyt forslag.
3. Hvis du ikke er tilfreds med forslagene, kan du forbedre tekstforslagene ved hjælp af indstillingerne **Tone**, **Format** og **Fremhævelse** .

   <!--Select **More Settings**, change the options that are shown under **Choose how Copilot creates suggestions**, then select **Create draft** to get a new suggestion.-->

   Du kan få retningslinjer for at forbedre forslag ved at gå til [Forbedre og tilpasse tekstforslag](#improve-and-tailor-text-suggestions).

4. For at gå frem og tilbage gennem forslag skal du bruge de forrige og næste links øverst på siden (*x* **af** *y*). <!-- or select the **...** (More formatting options) along the bottom of the window, then select **Undo**. Select **Redo** to go back.-->
5. Gennemgå teksten for at sikre, at den er nøjagtigt og korrekt:

   - Hvis du vil gemme teksten, skal du vælge **Behold den**. 
   - Hvis du ikke vil gemme, skal du vælge knappen Kassér (papirkurv) ![Viser papirkurvsikonet til sletning af alle Copilot-forslag til bankkontoafstemning](media/copilot-delete-trash-can.png).

### <a name="improve-and-tailor-text-suggestions"></a>Forbedre og skræddersy tekstforslag

Der er nogle trin, du kan udføre for at forbedre tekstforslagene og ændre dem, så de passer til dine personlige eller professionelle indstillinger.

1. Ændre de vareattributter, der bruges af Copilot.

   Copilot-forslag er delvist baseret på de attributter, der er knyttet til varen. Hvis du vil se de tilgængelige attributter og aktuelle indstillinger, skal du vælge redigeringsikonet ![Viser redigeringsikonet i Copilot-vinduet til ændring af attributter](media/edit-pencil.png) i øverste venstre hjørne. På siden **Vareattributter** skal du vælge de attributter, der bedst justeres efter de egenskaber, du vil fremhæve. De mere relevante attributter, som du kan medtage, jo større bliver resultatet. Hvis du synes, du mangler nogle nøgleattributter, kan du tilføje flere. Du kan finde flere oplysninger om attributter i [Arbejde med vareattributter](inventory-how-work-item-attributes.md)
1. Rediger dine præferenceindstillinger for **Tone**, **Format** og **Fremhævelse**.

   |Indstilling|Beskrivelse|
   |-|-|
   |Tone |Brug denne indstilling, hvis du vil have indflydelse på, hvilken type ord, sætninger og tegnsætning der bruges til at betjene målgruppen. Du kan vælge mellem flere foruddefinerede samtaletoner, lige fra **Formel** (hvilket resulterer i en største forretnings tone af valgmulighederne) til **Kreativt** (hvilket giver en mest uformel samtaletone). |
   |Format og længde|Brug denne indstilling til at styre tekstens generelle struktur, som består af tre dele, der er dækket af fire forskellige muligheder: <ul><li>**Slogan** - Et catch-udtryk eller en kort sætning, der identificerer varen eller varemærket.</li><li>**Afsnit** - Et enkelt punkt med flydende og udførlig tekst, der består af flere komplette sætninger.</li><li>**Slogan + afsnit** – Et slogan efterfulgt af et afsnit</li><li>**Kort** - En introduktions sætning, som svarer til et slogan, efterfulgt af en punktopstilling med vigtige hovedpunkter.</li></ul> |
   |Fremhævning|Brug denne indstilling til at vælge fra en liste over foruddefinerede kvaliteter, som du vil fremhæve i teksten. Vælg en kvalitet, der bedst svarer til den type vare, du skriver om varen. Kvaliteter svarer ikke direkte til varens attributter, beskrivelse eller kategori. F.eks. kan **Kvalitet** kunne være et godt valg til både en cykel eller et skrivebord, mens **Hastighed** ville passe til cyklen, men ikke et skrivebord.|

1. Du kan forbedre feltet **Beskrivelse** på varekortet.

   Teksten i feltet **Beskrivelse** bruges, som den er mange steder i den foreslåede tekst, så det er vigtigt, at beskrivelsen bedst beskriver, hvordan du vil referere til varen i marketingteksten. 

1. Kontroller, at feltet **Varekategorikode** på varekortet er indstillet til en korrekt kategori.

   Copilot finder ord og udtryk, der er relateret til kategorien, og kan arbejde i den foreslåede tekst.

### <a name="working-with-multiple-languages"></a>Arbejde med flere sprog

Tekst genereres altid på det sprog, der er defineret af dine bruger [indstillinger](ui-change-basic-settings.md#language). Hvis din organisation opererer og indtaster data i Business Central på et andet sprog, eller hvis Business Central er forbundet til din onlinebutik, f.eks. med Shopify, kan det resultere i udgivelse af indhold, der ikke matcher lignende marketingindhold.

## <a name="create-text-from-scratch"></a>Oprette tekst fra bunden

1. Åbn den vare, du vil tilpasse, i Business central, som følgende:

    1. I øverste højre hjørne skal du vælge den ![Lightbulb, der åbner funktionen Fortæl mig 22.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Varer**, og vælg derefter det relaterede link for at vise en liste over tilgængelige varer.
    2. Hvis du vil åbne varen, skal du dobbeltklikke på den eller vælge dens nummer i feltet **Nummer** .

2. Gør ét af følgende:

   - Vælg **Rediger** i ruden **Marketingtekst** i faktaboksen i højre side.
   - Vælg handlingen **Marketingtekst**.
3. Foretage ændringer i teksten direkte i feltet **Marketingtekst**. Brug værktøjslinjen nederst i boksen til at formatere og tilpasse tekst, tilføje links og meget mere.
4. Vælg derefter **OK** for at gemme den nye tekst.

## <a name="see-also"></a>Se også

[Oversigt over forslag til marketingtekst](ai-overview.md)  
[Fejlfinde Copilot- og AI-funktioner](ai-copilot-troubleshooting.md)  
[Ofte stillede spørgsmål til forslag til marketingtekst](faqs-marketing-text.md)  
[Konfigurere Copilot- og AI-funktioner](enable-ai.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
