---
author: brentholtorf
ms.topic: include
ms.date: 10/05/2022
ms.author: bholtorf
---
Når du har indsat alle varer på linjerne, kan du beregne fakturarabatten for det samlede salgsdokument ved at vælge Handlinger og derefter vælge **Beregn fakturarabat**.

Rabatten beregnes ud fra alle linjer i salgsdokumentet, hvor afkrydsningsfeltet **Tillad fakturarabat** er markeret. Som standard er fakturarabatter tilladt. Men linjer med varegebyrer er f.eks. ikke medtaget i beregningen af fakturarabatten. Hvis du vil anvende en rabat på disse linjer, skal du angive værdien i feltet **Linjerabat i %** på linjerne.  

> [!NOTE]
> Felterne **Tillad fakturarabat** og **Linjerabatbeløb** er som standard skjult på linjerne. Hvis felterne ikke er tilgængelige, kan du tilføje dem ved at tilpasse siden. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](../ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

> [!TIP]
> Hvis feltet **Beregn fakturarabat** er markeret på siden **Salgsopsætning**, beregnes fakturarabatten automatisk. Når beregningen sker anderledes, afhængigt af den type salgsdokument, du bruger.
>
> Hvis du bruger en salgsordre, beregnes rabatten, når du tilføjer en linje. For alle andre salgsdokumenter, f. eks. salgsfakturaer, beregnes rabatten, når du udfører en af følgende handlinger:
>
> * Vis statistik
> * Vis a kontrolrapport
> * Udskriv
> * Post

Du kan definere fakturarabatbetingelser for en debitor på siden **Deb./fakturarabat**. Desuden anvendes valutakoden på salgsdokumentet til at fastsætte fakturarabatbetingelserne i den tilsvarende valuta.

Hvis du ikke har angivet fakturarabatter for udenlandske valutaer, bruges rabatbetingelserne på siden **Debitorrabat** til at beregne rabatten. Beregningen bruger den lokale valuta og den valutakurs, der var gældende på bogføringsdatoen for dokumentet.
