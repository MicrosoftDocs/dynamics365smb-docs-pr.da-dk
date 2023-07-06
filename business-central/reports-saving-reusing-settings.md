---
title: Administrere gemte indstillinger for rapporter og kørsler
description: 'Beskriver, hvordan Administrator kan konfigurere foruddefinerede indstillinger og filtre for en rapport og dele disse indstillinger med en eller alle brugere.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customization, personalization'
ms.date: 12/21/2021
ms.author: edupont
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><a name="manage-saved-settings-for-reports-and-batch-jobs"></a><a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Administrere gemte indstillinger for rapporter og kørsler

Når brugerne kører rapporter, får de normalt vist en side, hvor de kan vælge indstillinger og angive filtre for at ændre, hvilke data der skal medtages i den genererede rapport. Denne side kaldes *anmodningssiden*. En rapport kan medtage én eller flere *gemte indstillinger*, som brugerne kan anvende til rapporten fra anmodningssiden. *Gemte indstillinger* er grundlæggende foruddefinerede indstillinger og filtre. Med gemte indstillinger kan du hurtigt og pålideligt generere ensartede rapporter, der indeholder de korrekte data. Du kan finde flere oplysninger i [Bruge gemte indstillinger](ui-work-report.md#SavedSettings).

> [!NOTE]
> I dette emne omtales *rapporter*, men lignende oplysninger gælder for *batchjob*.

Hvis du har de nødvendige tilladelser, kan du få vist, oprette og redigere de gemte indstillinger for alle rapporter for alle brugere i en virksomhed. Du kan tildele gemte indstillinger for en rapport til enkelte brugere eller til alle brugere i virksomheden.

## <a name="manage-saved-settings"></a><a name="manage-saved-settings"></a><a name="manage-saved-settings"></a>Administrere gemte indstillinger

Du administrerer gemte indstillinger på siden **Rapportindstillinger**. Du kan åbne siden på to måder:

- Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Rapportindstillinger**, og vælg derefter det relaterede link.
- På rapportens forespørgselsside skal du vælge opslaget i feltet **Brug standardværdier fra**, og vælg derefter handlingen **Vælg fra komplet liste**.

    Feltet er kun synligt, hvis du har kørt rapporten mindst én gang. Listen viser kun de indstillinger, der er tilgængelige for dig, enten fordi de er dine egne indstillinger, eller fordi indstillingerne deles med dig.

Siden **Rapportindstillinger** viser alle eksisterende poster for gemte indstillinger for alle brugere. Hvis der er et brugernavn i feltet **Tildelt til**, er det kun denne bruger, der kan bruge de gemte indstillinger for den tilknyttede rapport. Hvis der er en markering i feltet **Del med alle brugere**, kan alle brugere anvende de gemte indstillinger for rapporten.  

> [!TIP]
> Når en bruger har kørt en rapport, der understøtter delte indstillinger, gemmes deres indstillinger, som føjes til listen. I de fleste tilfælde kan administratoren redigere indstillingerne og vælge at dele indstillingerne med alle brugere.
>
> I nogle tilfælde kan indstillingerne imidlertid ikke deles, og administrator kan heller ikke ændre dem. De fleste batchjob understøtter ikke delte indstillinger.  

## <a name="create-or-modify-saved-settings-for-all-users"></a><a name="create-or-modify-saved-settings-for-all-users"></a><a name="create-or-modify-saved-settings-for-all-users"></a>Oprette eller redigere gemte indstillinger for alle brugere

Fra siden **Rapportindstillinger** kan du:

- Vælge handlingen **Ny** for at oprette en ny post for gemte indstillinger fra bunden.
- Vælg en post for gemte indstillinger på listen, og vælg handlingen **Kopiér** for at oprette en kopi.
- Vælg en post for gemte indstillinger på listen, og vælg handlingen **Rediger** for at ændre en post for gemte indstillinger.

> [!Important]
> Overvej, hvilket navn du giver en post for gemte indstillinger. Hvis du opretter en post for gemte indstillinger for alle brugere, og du giver den samme navn som en eksisterende post for gemte indstillinger, som er tildelt til en bestemt bruger, kan den pågældende bruger ikke anvende den post for gemte indstillinger, der er tildelt til alle.  I sektionen **Gemte indstillinger** på rapportanmodningssiden får brugeren vist to poster for gemte indstillinger med det samme navn. Men uanset hvilken indstilling brugeren vælger, anvendes den brugerspecifikke post for gemte indstillinger.

> [!NOTE]
> Muligheden for at gemme indstillinger er kun tilgængelig, når egenskaben [SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) for rapportens anmodningsside er indstillet til **Ja**. Egenskaben **SaveValues** indstilles af udvikleren.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
