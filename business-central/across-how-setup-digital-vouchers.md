---
title: Opsætte digitale bilag
description: 'Denne artikel forklarer, hvordan du opsætter og bruger tvungne digitale værdikuponer i Microsoft Dynamics 365 Business Central.'
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'digital voucher, voucher, attachment, setup'
ms.search.form: '5579, 5582, 5587'
ms.date: 11/17/2023
ms.custom: bap-template
---

# <a name="set-up-digital-vouchers"></a>Opsætte digitale bilag

Administratorer kan bruge digital voucher-funktionalitet til at kræve, at dokumenter er knyttet til specifikke transaktioner, når de bogføres. Derfor giver denne funktionalitet mulighed for en kildedrevet tilgang og giver et bedre revisionsspor. Forskellige former for håndhævelse kan konfigureres til dette formål, afhængigt af dokumenter eller journaltyper.

Udtrykket *digitalt bilag* henviser til en digital eller elektronisk form for et traditionelt bilag i regnskabet. En voucher er et dokument, der bruges til at understøtte og godkende finansielle transaktioner. I regnskabet tjener et bilag typisk som bevis for en udgift eller en modtagelse af midler. Kuponen kan indeholde detaljer såsom datoen for transaktionen, en beskrivelse, beløbet og eventuelle autorisationssignaturer.

> [!IMPORTANT]
> I nogle lande og områder kan du være begrænset fra at konfigurere nogle indstillinger, fordi specifikke opsætninger kan være påbudt af juridiske krav. Hvis du støder på disse begrænsninger, skal du se efter en detaljeret forklaring på dokumentationssiden for dit land eller område.

## <a name="enable-digital-vouchers"></a>Aktivere digitale bilag

Følg disse trin for at aktivere digital voucher-funktionalitet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfiguration af digital voucher**, og vælg derefter det relaterede link.
2. Marker afkrydsningsfeltet **Aktiveret**.

## <a name="set-up-digital-vouchers-1"></a>Opsætte digitale bilag

Du kan bruge forskellige opsætninger til følgende dokumenter og journaler.

| Posttype | Beskrivelse |
|------------|-------------|
| Salgsdokument | Angiver posteringer, der udfyldes fra salgsbilag. |
| Købsdokument | Angiver posteringer, der udfyldes fra købsdokumenter. |
| Finanskladde | Angiver posteringer, der udfyldes fra den generelle kladde for alle kontotyper undtagen dem, der er relateret til debitor og kreditor. Hvis du vælger en af ​​disse kontotyper, ændrer du kontrol over bogføringsprocessen. Hvis du vælger **Kunde** som kontotype, tjekker systemet din opsætning, der er relateret til salgskladden. Hvis du vælger **Kreditor** som kontotype, tjekker systemet din opsætning, der er relateret til købskladden. |
| Salgskladde | Angiver de posteringer, der udfyldes fra salgskladden og den generelle kladde hvor **Kunde** er valgt som kontotype. |
| Købskladde | Angiver de posteringer, der udfyldes fra købskladden og den generelle kladde hvor **Kreditor** er valgt som kontotype. |

Følg disse trin for at definere, hvordan din organisation bruger tvungne digitale værdikuponer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfiguration af digital voucherpost**, og vælg derefter det relaterede link. Alternativt på siden **Digital voucher opsætning**, vælg **Postopsætning**.
2. I kolonnen **Posttype** skal du vælge en mulighed.
3. I kolonnen **Kontrollér type** skal du vælge en gennemtvingelsesmulighed. Hvis du vælger **Ingen**, kan du bogføre den valgte type post uden en digital voucher. Hvis du vælger **Vedhæftet fil**, skal posten indeholde en vedhæftet fil. Hvis du vælger **Vedhæftet fil eller note**, kan du inkludere en vedhæftet fil eller en note til posten. 
4. Vælg **Generer automatisk**-afkrydsningsfeltet for at generere den digitale voucher automatisk. For eksempel, hvis du ikke manuelt vil tilføje en salgsfaktura til din transaktion, skal du markere dette afkrydsningsfelt. Så skal du bare sende dokumentet. Systemet opretter automatisk dokumentet, baseret på dit rapportlayout, og vedhæfter det til transaktionen.
5. Vælg **Spring over hvis tilføjet manuelt**-afkrydsningsfeltet, hvis du ikke ønsker at tilføje en automatisk genereret digital voucher, hvis brugeren allerede har tilføjet en manuel vedhæftning.

### <a name="use-source-codes-for-setup"></a>Brug kildekoder til opsætning

For at bruge håndhævelse for kladder, men ikke for alle transaktionstyper, skal du forbinde den specifikke kildekode for at identificere posteringstypen den generelle kladde, salgskladde eller indkøbskladde.

Følg denne vejledning for at konfigurere specifikke kildekoder til digitale vouchers.

1. På siden **Digital voucher postopsætning**, vælg **Kildekoder**.
2. På siden **Kildekoder for voucher-indtastning** skal du vælge de kildekoder, du vil konfigurere.
3. Luk siden.

## <a name="use-the-functionality"></a>Bruge funktionaliteten

Åbn et købs- eller salgsdokument, og indtast oplysninger i de påkrævede felter. Før du bogfører dokumentet, skal du følge disse trin for at vedhæfte en digital voucher.

1. I faktaboksen **Indgående dokumentfiler** skal du vælge **Vedhæft fil**.
2. Træk en fil direkte til siden **Indsæt fil**, eller browse til filen fra denne side.

Dokumentet vedhæftes faktaboksen **Indgående bilagspost**. For hver linje kan du finde dokumentets navn og type.

Hvis du ved et uheld vedhæfter den forkerte voucher, skal du følge disse trin for at slette den, før du bogfører dokumentet.

1. I faktaboksen **Indgående dokumentfiler** fra dokumentlinjen skal du vælge **Indgående dokument**.
2. På siden **Indgående dokument** skal du vælge **Slet**.

> [!NOTE]
> Hvis vedhæftning af et digitalt bilag er konfigureret som obligatorisk, og du forsøger at bogføre dokumenter eller kladder uden at vedhæfte et bilag, forhindrer systemet dig i at bogføre. Du får følgende fejlmeddelelse: "Ikke muligt at bogføre uden at vedhæfte den digitale voucher."

### <a name="find-attached-vouchers-in-transactions"></a>Find vedhæftede værdibeviser i transaktioner

Du kan finde den vedhæftede bilag fra det bogførte dokument eller fra siden **General Bogføring** ved at se i faktaboksen **Indgående dokumentfiler**.

Du kan ikke slette et vedhæftet dokument, efter at bogføringen er afsluttet. Du kan dog tilføje flere vedhæftede filer, efter at indlægget er afsluttet.

## <a name="see-also"></a>Se også

[Økonomistyring](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
