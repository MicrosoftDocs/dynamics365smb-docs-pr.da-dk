---
title: Bruge Word-skabeloner til massekommunikation
description: 'Word-skabeloner kan gøre det nemmere at masseoprette dokumenter, der er tilpasset bestemte objekter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/01/2023
ms.custom: bap-template
ms.search.forms: '9989, 13,'
ms.service: dynamics-365-business-central
---

# <a name="use-word-templates-for-bulk-communication"></a>Bruge Word-skabeloner til massekommunikation

Microsoft Word-skabeloner kan gøre det nemmere at massekommunikere på skrift eller i e-mails med objekter som f.eks. kontakter, debitorer og kreditorer. Du kan f.eks. oprette:

* Brochurer for at advare debitorer om en salgskampagne
* Breve, der oplyser leverandører om en ny indkøbspolitik
* Invitationer til at tiltrække kontaktpersoner til et kommende arrangement

> [!NOTE]
> Når du konfigurerer Word-skabeloner, skal du bruge en enhed med Microsoft Word 2019 eller nyere og Windows-operativsystemet installeret.

## <a name="set-up-the-source-of-data"></a>Konfigurer datakilden

Bruge objekter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakilde for skabelonen og til at tilføje fletfelter for at tilpasse dokumenter til de enkelte objekter. Fletfelterne hentes fra objektet i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du anvender en Word-skabelon til et objekt, indsættes data fra fletfelterne i dokumentet.

Når du på siden **Word-skabeloner** opretter en ny skabelon, vil en assisteret installationsvejledning hjælpe dig gennem følgende trin:

1. Vælg en eller flere enheder, der skal bruges som datakilde. Hvis du f. eks. vil oprette en brochure til en salgskampagne, skal du sandsynligvis vælge kunde enhed som kilde.
2. Vælge andre enheder som ekstra datakilder. Få mere at vide i [Tilføj poster, der er relateret eller ikke relateret til kildeenheden](#add-entries-that-are-related-or-unrelated-to-the-source-entity).
3. Download en tom skabelon. Du kan oprette skabelonen i Word med det samme, eller du kan overføre den tomme skabelon og afslutte programguiden. Når skabelonen er klar, skal du bruge handlingen **Overfør** på siden **Word-skabeloner** for at erstatte den tomme skabelon med den færdige skabelon. Du kan finde flere oplysninger i [Konfigurere skabelonen i Word](#set-up-the-template-in-word).
4. Overfør den skabelon, du har forberedt.
5. Angiv en kode og et navn, der identificerer skabelonen.

Når du henter en skabelon, får du en. zip-fil, der indeholder to filer.

|Fil  |Beskrivlse  |
|---------|---------|
|DataSource.xlsx     | Datakildefilen indeholder de felter, som du kan bruge i skabelonen. Undlad at redigere datakildefilen. Du kan kun bruge den Word-skabelon og de datakildefiler, som du downloader, og du skal gemme filerne på den samme placering.     |
|Word-skabelon     | En .docx-fil, der skal bruges som skabelon.        |

Hvis du vil vide, hvordan du opretter en skabelon i Word, skal du vælge [Opsætning for skabelonen i Word](#set-up-the-template-in-word).

## <a name="add-entries-that-are-related-or-unrelated-to-the-source-entity"></a>Tilføj poster, der er relateret eller ikke relateret til kildeenheden

Du kan også flette data fra andre objekter. Hvis du vil tilføje andre objekter som datakilder, skal du bruge en af følgende handlinger på siden med **Word-skabeloner**, eller når du bruger den assisterende installationsguide:

|Handling  |Beskrivlse  |
|---------|---------|
|**Tilføj relateret enhed**  | Brug data fra enheder, der er relateret til kildeenheden. Du kan f. eks. bruge debitorobjektet til at flette data fra objektet Kontakt. Objekter er relateret, når et felt i et objekt henviser til et andet. Et felt i debitorobjektet henviser til et felt i objektet Kontakt, så den er relateret. Det delte felt er ofte et id, f. eks. et navn, en kode eller et ID.        |
|**Tilføj ikke-relateret enhed**| Brug data fra enheder, der ikke er relateret til kildeenheden. Du er f. eks. ved at oprette en skabelon til debitorobjektet. Du kan tilføje objektet virksomhedsoplysninger, så du kan medtage dine kontaktoplysninger. En vigtig fordel er, at hvis du ændrer kontaktoplysningerne, opdateres de automatisk i skabelonen. Når du har tilføjet en ikke-relateret enhed, kan du føje tilknyttede enheder.         |

Hvis du ikke har relaterede poster, skal du vælge en bestemt post. Da du kun kan tilføje en enhed én gang, skal du slette objektet og tilføje den igen med den nye post for at bruge en anden post.

Du kan oprette et hierarki af enheder, både relaterede og ikke-relaterede. Relationen vises som en træstruktur. Feltet **objektrelation** indeholder også oplysninger om relationen. For ikke-relaterede objekter viser feltet den post, der opretter relationen.

Når du tilføjer objekter, skal du bruge feltet **Præfiks** til at angive et præfiks for feltnavnene. Senere når du føjer felter til skabelonen, kan præfikset gøre det nemmere at skelne mellem felter fra kildeenheden og andre objekter.

### <a name="select-the-fields-to-include"></a>Vælg de felter, der skal medtages

Du kan angive de felter, der skal være tilgængelige for skabelonen for hver enkelt objekttype. Vælg tallet i kolonnen **Antal markerede felter** for at få adgang til en liste over felter, der er tilgængelige. På siden **Feltvalg** skal du bruge afkrydsningsfeltet **Medtag** til at angive felterne. I forbindelse med nogle objekter er de felter, som virksomheder typisk bruger, som standard medtaget. Du kan f. eks. redigere listen for at fjerne standardfelterne. Dine ændringer gælder kun for den skabelon, du arbejder på.

> [!NOTE]
> Det samlede antal felter, du kan tilføje fra alle enheder, er 250.

> [!NOTE]
> Du eller din Microsoft-partner kan føje brugerdefinerede felter til enheder. Når du gør det, indsætter vi navnene på felterne med **Beregn** og giver dem felttypen **Beregnet**. Felttypen beregnes for at angive, at feltet kan vise forskellige værdityper, f. eks. tekst, tal, datoer osv.

## <a name="to-create-a-word-template-in-business-central"></a>Sådan oprettes en Word-skabelon i Business central

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Word-skabeloner**, og vælg derefter det relaterede link.
2. Vælg **Ny**, **Opret en skabelon**, og følg derefter trinene i installationsvejledningen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Du kan også oprette en skabelon direkte fra siden for et objekt ved at vælge handlingen **Anvend Word**-skabelon for at åbne den assisterende installationsvejledning og derefter vælge **Ny skabelon**. Når du gør det, vælges datakilden for dig baseret på objekttypen.

## <a name="set-up-the-template-in-word"></a>Opsætning af skabelon i Word

Når du opretter skabelonen i Word, kan du tilføje fletfelter på fanen **Forsendelser** ved at vælge **Indsæt fletfelt**. De tilgængelige fletfelter stammer fra den datakildefil, du har hentet for objektet. De fungerer som pladsholdere, der fortæller Word, at der skal indsættes oplysninger om objektet i dokumentet.

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Tilføje fletfelter i Microsoft Word":::

## <a name="apply-a-template"></a>Anvend en skabelon

Når du har klargjort din Word-skabelon, kan du vælge **Anvend** for at oprette dokumenterne på siden **Word-skabeloner**. Når du anvender en Word-skabelon til et objekt, indsættes data fra fletfelterne i dokumentet. Du kan enten oprette ét dokument, der indeholder sektioner for hvert objekt, eller **opdele** handlingen for at oprette et nyt dokument for hvert objekt.

Du kan anvende handlingen **Anvend Word-skabeloner** til at anvende skabeloner til en eller flere af de samme typer enheder, f. eks. en debitor, direkte i denne sides kontekst til objektet. F.eks. siderne **Debitor** eller **Kreditor**.

## <a name="use-word-templates-with-email"></a>Bruge Word-skabeloner med e-mail

Du kan bruge Word-skabeloner til at føje indhold til e-mail-meddelelser. Når du opretter en e-mail, kan du vælge at bruge handlingen **brug Word-skabelon** til at anvende indholdet af en skabelon på e-mailen. Du skal have oprettet skabeloner til objektet. Du kan bruge én skabelon ad gangen, og når du skifter mellem skabeloner, ændres den, så den afspejler indholdet af den valgte skabelon.

Derudover kan du bruge handlingen **Tilføj fil fra Word-skabelon** til at vedhæfte indholdet af skabelonen til mailen som en fil. Filen vil blive brugt det format, du angav til skabelon outputtet.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Indstillinger for brug af indhold fra en Word-skabelon i en e-mail":::

## <a name="edit-a-word-template"></a>Redigere en Word-skabelon

Du kan foretage følgende ændringer af dine Word-skabeloner:

* Hvis du vil redigere den brødtekst eller de fletfelter, der er medtaget i skabelonen, skal du bruge handlingen **Download**, foretage ændringerne og derefter bruge **Upload**-handlingen
* Hvis du vil ændre datakilder, skal du bruge handlingen **Rediger relaterede objekter**
* Hvis du vil erstatte Word-skabelonen med en ny skabelon, skal du bruge handlingen **Upload**
* Slette skabelonen

## <a name="see-also"></a>Se også

[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Konfigurer mail](admin-how-setup-email.md)  
