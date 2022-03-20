---
title: Bruge Microsoft Word-skabeloner til massekommunikation | Microsoft Docs
description: Word-skabeloner kan gøre det nemmere at masseoprette dokumenter, der er tilpasset bestemte objekter.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: fe9717f871fdc1db782ceeda4cbad267abddca90
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2022
ms.locfileid: "8383423"
---
# <a name="using-word-templates-for-bulk-communication"></a>Bruge Word-skabeloner til massekommunikation
Microsoft Word-skabeloner kan gøre det nemmere at massekommunikere på skrift eller i e-mails med objekter som f.eks. kontakter, debitorer og kreditorer. Du kan f.eks. oprette brochurer, som giver debitorer besked om en salgskampagne, breve til kreditorer om en ny indkøbspolitik eller invitationer, der skal tiltrække kontakter til et kommende arrangement.

> [!NOTE]
> Du kan kun bruge Word-skabeloner på enheder med Microsoft Word 2019 og Windows-operativsystemet installeret.

Du kan bruge objekter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakilde for skabelonen og til at tilføje fletfelter for at tilpasse dokumenter til de enkelte objekter. Fletfelterne hentes fra objektet i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du anvender en Word-skabelon til et objekt, indsættes data fra fletfelterne i dokumentet.

På siden **Word-skabeloner** kan du bruge en vejledning om assisteret opsætning for at hente en zip-fil, der indeholder filen DataSource.xlsx og en Word-skabelonfil til et objekt. Datakildefilen indeholder de felter, som du kan bruge i skabelonen. Undlad at redigere datakildefilen. Du kan kun bruge den Word-skabelon og de datakildefiler, som du henter fra [!INCLUDE[prod_short](includes/prod_short.md)], og du skal gemme filerne på den samme placering.

Når du har oprettet skabelonen og tilføjet fletfelter, bruger du den samme vejledning til at overføre skabelonen.

## <a name="setting-up-the-template-in-word"></a>Opsætning af skabelon i Word
Når du opretter skabelonen i Word, kan du tilføje fletfelter på fanen **Forsendelser** ved at vælge **Indsæt fletfelt**. De tilgængelige fletfelter stammer fra den datakildefil, du har hentet for objektet. De fungerer som pladsholdere, der fortæller Word, at der skal indsættes oplysninger om objektet i dokumentet. 

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Tilføje fletfelter i Microsoft Word":::

## <a name="adding-related-entities"></a>Tilføje relaterede objekter
Ud over at tilføje data til kildeobjektet, dvs. det objekt, du opretter skabelonen til, kan du også flette data fra objekter, der er knyttet til den. Hvis kilden f. eks. er kunde-objektet, kan du også flette data fra felter på kunde/indkøberen, fordi begge enheder har et felt fælles.

Relaterede enheder deler et felt, som ofte er et id, f. eks. et navn, en kode eller et ID, med kildeenheden. Når du opretter en skabelon, er der simple og avancerede indstillinger for valg af relaterede objekter:

* Enkel-Tilføj kendte relationer, som [!INCLUDE[prod_short](includes/prod_short.md)] gør tilgængelige som standard.
* Avanceret-Tilføj ikke-standardforbindelser, f. eks. dem, der er tilføjet af filtypenavne eller tilpasninger. Dette kræver, at du kender de felter, som objekterne er fælles om.

Når du tilføjer et relateret objekt, skal du angive et præfiks til feltnavnet. Når du føjer felter til skabelonen, kan præfikset gøre det nemmere at skelne mellem felter fra kildeenheden og felter fra relaterede objekter.

## <a name="to-create-a-word-template-in-business-central"></a>Sådan oprettes en Word-skabelon i Business central
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Word-skabeloner**, og vælg derefter det relaterede link.
2. Vælg **Ny**, **Opret en skabelon**, og følg derefter trinene i installationsvejledningen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Du kan også oprette en skabelon direkte fra siden for et objekt ved at vælge handlingen **Anvend Word**-skabelon for at åbne den assisterende installationsvejledning og derefter vælge **Ny skabelon**. Når du gør det, vælges datakilden for dig baseret på objekttypen.

## <a name="applying-a-template"></a>Anvende en skabelon
Når du har klargjort din Word-skabelon, kan du vælge **Anvend** for at oprette dokumenterne på siden **Word-skabeloner**. Når du anvender en Word-skabelon til et objekt, indsættes data fra fletfelterne i dokumentet. Du kan enten oprette ét dokument, der indeholder sektioner for hvert objekt, eller **opdele** handlingen for at oprette et nyt dokument for hvert objekt.

Du kan anvende skabeloner til en eller flere af de samme typer enheder, f. eks. en kontaktperson, direkte i denne sides kontekst, eller fra siden med Word-skabeloner for at anvende skabelonen på alle de enheder, der har denne type.

## <a name="using-word-templates-with-email"></a>Bruge Word-skabeloner med E-mail
Du kan bruge Word-skabeloner til at føje indhold til e-mail-meddelelser. Når du opretter en e-mail, kan du vælge at bruge handlingen **brug Word-skabelon** til at anvende indholdet af en skabelon på e-mailen. Dette kræver, at du har oprettet en eller flere skabeloner for enheden. Du kan bruge én skabelon ad gangen, og når du skifter mellem skabeloner, ændres den, så den afspejler indholdet af den valgte skabelon.

Derudover kan du bruge handlingen **Tilføj fil fra Word-skabelon** til at vedhæfte indholdet af skabelonen til mailen som en fil. Filen vil blive brugt det format, du angav til skabelon outputtet.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Indstillinger for brug af indhold fra en Word-skabelon i en e-mail":::

## <a name="see-also"></a>Se også
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
