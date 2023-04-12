---
title: Tilføje marketingtekst til varer
description: Skrive marketingtekst for varer i Business central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# Tilføje marketingtekst til varer

Du kan skrive *marketingtekst* om varen for alle de varer, der er registreret i Business central. Selvom marketingtekst er en slags beskrivelse, er den forskellig fra varens **beskrivelsesfelt**. Feltet **Beskrivelse** bruges typisk som et kort vist navn til at identificere produktet hurtigt. Marketingteksten er derimod en mere omfattende og beskrivende tekst. Formålet er at tilføje marketing- og reklameindhold, også kendt som *kopi*. Denne tekst kan derefter udgives sammen med varen, hvis den vises i en webshop, som f.eks. Shopify.

Der er to måder at oprette en marketingtekst på. Den nemmeste måde at komme i gang på er ved at bruge Copilot, som foreslår AI-genereret tekst for dig. Den anden måde er at starte fra bunden. 

## <a name=copilot></a>Opret AI-styret marketingtekst (forhåndsversion) med Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Med Copilot kan du hurtigt få et tekstforslag, der bliver genereret automatisk til dig. Den AI-genererede tekst er skræddersyet til elementet og er et godt udgangspunkt. Teksten er baseret på en del af følgende oplysninger:

- Definerede attributter for varen, f. eks. beskrivelse, farve, dimensioner, materialer osv.
- Indstillinger, der kan vælges som samtalens tone, format og længde.

Copilot er designet til at spare dig tid og hjælpe dig med at skrive kreativ og engagerende tekst, der afspejler dit varemærke og stemmer overens med produktlinjen. Start med at generere et forslag, og ret derefter den foreslåede tekst efter behov.

> [!NOTE]
> I forhåndsversionen af Business Central er den AI-genererede tekst kun på engelsk.

### Forudsætninger

- Du bruger en [forhåndsversion](ai-preview-getstarted.md) af Business central, som er aktiveret til Copilot. Aktivering af Copilot udføres af en administrator. Du kan finde flere oplysninger i [Konfigurere marketingtekst for AI-styret vare med Copilot](enable-ai.md).
- Det sprog, du bruger i Business central, skal være engelsk. Alle de tilgængelige engelske landestandarder fungerer, som f. eks. engelsk (amerikansk), engelsk (Storbritannien) eller engelsk (Sydafrika).

   Hvis du vil skifte sprog, skal du i øverste højre hjørne vælge ikonet **Indstillinger** ![Indstillinger.](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") > **Mine indstillinger** > **Sprog**. Du kan finde flere oplysninger i [Ændre grundlæggende indstillinger](ui-change-basic-settings.md#language).
- Gennemse [Copilot ofte stillede spørgsmål](ai-faq.md) for at få mere at vide om AI-genererede tekstforslag fra Copilot, og hvordan du skal bruge dem.

### Oprette første kladde med Copilot

1. Åbn den side, du vil tilpasse, i Business central. Benyt følgende fremgangsmåde for at åbne en vare:

   1. I øverste højre hjørne skal du vælge den ![Lightbulb, der åbner funktionen Fortæl mig 22.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Varer**, og vælg derefter det relaterede link for at vise en liste over tilgængelige varer.
   2. Hvis du vil åbne varen, skal du dobbeltklikke på den eller vælge dens værdi i feltet **Nummer** kolonne.

   Du kan finde flere oplysninger om, hvordan du opretter en vare, i [Registrere nye varer](inventory-how-register-new-items.md).

   [![Viser varekort med marketing tekstrude](media/create-with-copilot.png)](media/create-with-copilot.png#lightbox)

2. På varekortet kan du komme i gang med at skrive marketingtekst med Copilot:

   - Du kan også bruge **Marketing tekst**-ruden i faktaboksen til højre for siden. Følg disse trin:

      1. Vælg **Opret med Copilot** i ruden **Marketing tekst**.

         Den foreslåede tekst vises i ruden.
      2. Hvis du vil have et andet forslag, skal du vælge **Opret med Copilot** igen. Hvis du ikke er tilfreds med et forslag, skal du vælge **Afvis** for at rydde ruden.

         Du kan udføre dette trin igen og igen, indtil du får et forslag, som du tror, du mener, det er et godt sted. Men vær opmærksom på, at det aktuelle forslag overskrives, og du ikke nødvendigvis vil komme tilbage igen. Gå til næste trin, hvis du kan lide det aktuelle forslag. Du har stadig mulighed for at få flere forslag, men du kan også forbedre forslagene, hvis du vil senere.
      3. Vælg **Gennemse, og gem forslaget**, eller **Rediger** for at gennemgå, redigere og gemme teksten.

         I dette trin kommer du til siden **Opret med Copilot**. Gå til næste sektion.

         > [!NOTE]
         > Teksten gemmes først, når du har gennemført dette trin.

   - Du kan også vælge handlingen **Marketingtekst** øverst på siden med varekortet, så du kan gå direkte til siden **Opret med Copilot** .

     Vælg **Opret med Copilot** på siden **Opret med Copilot** for at hente det første forslag. Du kan derefter få flere forslag, forsøge at forbedre de forslag, du får, redigere tekst m.m. Gå til [Gennemsyn, Rediger og Gem](#review-edit-and-save-text) for at få flere oplysninger.

   > [!TIP]
   > [Hvor kommer forslagene fra?](ai-faq.md#how-does-copilot-work-where-does-the-suggested-text-come-from)

### Gennemse, rediger og gem tekst

Når du har den første kladde, skal du gennemse den og foretage ændringer i teksten for at gøre den klar til udgivelse. Dette arbejde udføres fra siden **Opret med Copilot**. Den aktuelle tekst vises i feltet **Marketingtekst**. På siden kan du få flere forslag, ændre præferencerne, så de har indflydelse på forslagene, og manuelt foretage ændringer og typografi i teksten.

[![Viser vinduerne Opret med Copilot](media/create-with-copilot-window.png)](media/create-with-copilot-window.png#lightbox)

> [!IMPORTANT]
> Den AI-genererede tekst fra Copilot er kun et forslag, og der kan opstå fejl. Det kræver humant overblik og gennemgang for at sikre, at det er nøjagtigt og hensigtsmæssigt. Gennemse eventuel foreslået tekst, og rediger efter behov, inden du gemmer og udgiver den til offentlig forbrug.

Følg nedenstående retningslinjer for at afslutte og gemme marketingteksten.

1. Foretage ændringer i teksten direkte i feltet **Marketingtekst**. Brug værktøjslinjen nederst i boksen til at formatere og tilpasse tekst, tilføje links og meget mere.
2. Vælg **Opret kladde**, hvis du vil have et nyt forslag.
3. Hvis du ikke er tilfreds med forslag, kan du forbedre tekstforslag, der er baseret på dine behov.

   Vælg **Flere indstillinger**, rediger de indstillinger, der vises under **Vælg, hvordan Copilot opretter forslag**, og vælg derefter **Opret kladde** for at få et nyt forslag.

   Du kan få retningslinjer for at forbedre forslag ved at gå til [Forbedre og tilpasse tekstforslag](#improve-and-tailor-text-suggestions).

4. Hvis du vil gå tilbage til det forrige forslag, skal du vælge **Fortryd**.
5. Gennemgå teksten nøjagtigt og korrekt, og vælg derefter **OK** for at gemme den.

### Forbedre og skræddersy tekstforslag

Der er nogle trin, du kan udføre for at forbedre tekstforslagene og ændre dem, så de passer til dine personlige indstillinger.

1. Brug indstillingerne øverst på siden **Opret med Copilot** til at påvirke resultatet af den AI-genererede tekst: 

   |Indstilling|Beskrivlse|
   |-|-|
   |Attributter, der skal medtages|Brug denne indstilling til at basere forslagene på de attributter, der er knyttet til varen. Vælg de attributter, der bedst justeres efter de egenskaber, du vil fremhæve. De mere relevante attributter, som du kan medtage, jo større bliver resultatet. Hvis du synes, du mangler nogle nøgleattributter, kan du tilføje flere. Du kan finde flere oplysninger om attributter i [Arbejde med vareattributter](inventory-how-work-item-attributes.md) |
   |Fremhæv en kvalitet|Brug denne indstilling til at vælge fra en liste over foruddefinerede kvaliteter, som du vil fremhæve i teksten. Vælg en kvalitet, der bedst svarer til den type vare, du skriver om varen. Kvaliteter svarer ikke direkte til varens attributter, beskrivelse eller kategori. F.eks. kan **Kvalitet** kunne være et godt valg til både en cykel eller et skrivebord, mens **Hastighed** ville passe til cyklen, men ikke et skrivebord.|
   |Samtalens tone|Brug denne indstilling, hvis du vil have indflydelse på, hvilken type ord, sætninger og tegnsætning der bruges til at betjene målgruppen. Du kan vælge mellem flere foruddefinerede samtaletoner, lige fra **Formel** (hvilket resulterer i en største forretnings tone af valgmulighederne) til **Kreativt** (hvilket giver en mest uformel samtaletone). |
   |Format og længde|Brug denne indstilling til at styre tekstens generelle struktur, som består af tre dele, der er dækket af fire forskellige muligheder: <ul><li>**Slogan** - Et catch-udtryk eller en kort sætning, der identificerer varen eller varemærket.</li><li>**Afsnit** - Et enkelt punkt med flydende og udførlig tekst, der består af flere komplette sætninger.</li><li>**Slogan + afsnit** – Et slogan efterfulgt af et afsnit</li><li>**Kort** - En introduktions sætning, som svarer til et slogan, efterfulgt af en punktopstilling med vigtige hovedpunkter.</li></ul> |

2. Du kan forbedre feltet **Beskrivelse** på varekortet.

   Teksten i feltet **Beskrivelse** bruges, som den er, i den foreslåede tekst, så det er vigtigt, at beskrivelsen bedst portrays, hvordan du vil referere til varen i marketingteksten. 

3. Kontroller, at feltet **Varekategorikode** på varekortet er indstillet til en korrekt kategori.

   Copilot finder ord og udtryk, der er relateret til kategorien, og kan arbejde i den foreslåede tekst.

## Oprette marketingtekst fra bunden

1. Åbn den vare, du vil tilpasse, i Business central, som følgende:

    1. I øverste højre hjørne skal du vælge den ![Lightbulb, der åbner funktionen Fortæl mig 22.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Varer**, og vælg derefter det relaterede link for at vise en liste over tilgængelige varer.
    2. Hvis du vil åbne varen, skal du dobbeltklikke på den eller vælge dens nummer i **Nummer** .

2. Gør ét af følgende:

   - Vælg **Rediger** i ruden **Marketingtekst** i faktaboksen i højre side.
   - Vælg handlingen **Marketingtekst**.
3. Foretage ændringer i teksten direkte i feltet **Marketingtekst**. Brug værktøjslinjen nederst i boksen til at formatere og tilpasse tekst, tilføje links og meget mere.
4. Vælg derefter **OK** for at gemme den nye tekst.

## Se også

[Oversigt over AI-styret varemarketingtekst med Copilot](ai-overview.md)  
[Konfigurere marketingtekst med Copilot til AI-styret vare](enable-ai.md)  
[AI-drevet varemarketingtekst med Copilot, ofte stillede spørgsmål](ai-faq.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  