---
title: Bruge Business Central sammen med Outlook | Microsoft Docs
description: Denne tjeneste er tæt integreret med Microsoft 365, så du kan administrere alle dine forretningsaktiviteter og sende og modtage mail til og fra kunder og leverandører direkte i Outlook.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 08/13/2021
ms.author: jswymer
ms.openlocfilehash: c281ce94e518f8ef099bb3e48177b90732a65c45
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145128"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Bruge Business Central som din virksomheds Indbakke i Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] giver mulighed for en tilføjelse, der sætter dig i stand til at administrere forretningsinteraktioner med dine kunder og leverandører direkte i Microsoft Outlook. Med Outlook-tilføjelsesprogrammerne i [!INCLUDE[prod_short](includes/prod_short.md)] kan du se finansielle data, der er relateret til debitorer og kreditorer samt oprette og sende finansielle dokumenter, f.eks tilbud og fakturaer.

[!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammet består af to separate tilføjelsesprogrammer, der giver følgende muligheder:

- Kontaktoplysninger

   Dette tilføjelsesprogram giver dig adgang til [!INCLUDE[prod_short](includes/prod_short.md)]-oplysninger om kunde eller leverandør i Outlook-mails og-aftaler. Du kan også oprette og sende [!INCLUDE[prod_short](includes/prod_short.md)]-forretningsdokumenter, f. eks. salgstilbud eller fakturaer til en kontakt.

- Dokumentvisning

   Når et forretningsdokument sendes i en e-mail, indeholder tilføjelsesprogrammet et direkte link fra e-mailen til det aktuelle forretningsdokument i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="get-started"></a>Kom i gang

1. Det første, du skal gøre, er at få [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammet installeret i Outlook. Administratoren har muligvis allerede installeret tilføjelsesprogrammet. Hvis du ikke er sikker, skal du kontakte administratoren eller se næste trin for at kontrollere, om det er installeret.

    Hvis tilføjelsesprogrammet ikke er installeret for dig, skal du se [installere tilføjelsesprogrammet til eget brug](admin-outlook.md#install). 

2. Hvis tilføjelsesprogrammet er installeret, kan du få adgang til **[!INCLUDE[prod_short](includes/prod_short.md)]**-tilføjelsesprogrammet fra en hvilken som helst ny eller eksisterende e-mail eller kalenderaftale i Outlook.

    Start med at logge på Outlook og åbne en e-mailmeddelelse. Hvis du bruger Outlook-appen, skal du så gå til båndet og se efter **[!INCLUDE[prod_short](includes/prod_short.md)]**.  Hvis du bruger Outlook på World Wide Web, skal du i Outlook øverst eller nederst på e-mailen Se ![ikonet for Business Central-tilføjelse i Outlook.](media/outlook-business-central-icon.png) eller vise flere handlinger ![Vise flere handlinger for en mail i Outlook.](media/outlook-more-actions-button.png) knap.

    ![Aktivér Business Central-tilføjelsesprogram i Outlook.](media/outlook-business-central-addin.png)

   Hvis du har installeret tilføjelsesprogrammet på egen hånd og har valgt at få et e-mail-eksempel på en e-mail, skal du kontrollere din indbakke for velkomstmailen. Denne e-mail indeholder oplysninger, der kan hjælpe dig i gang.

Første gang du bruger tilføjelsesprogrammet [!INCLUDE[prod_short](includes/prod_short.md)], kan du blive bedt om at logge på i ruden med tilføjelsesprogrammet. Hvis det er tilfældet, skal du vælge **Log på nu** og følge instruktionerne på skærmen for at logge på Business central ved hjælp af din konto.

> [!TIP]
> Hvis du bruger den nye Outlook på World Wide Web, kan du fastgøre **[!INCLUDE[prod_short](includes/prod_short.md)]**, så det altid er umiddelbart synlig, i stedet for at gå til knappen flere handlinger, hvilket gør det praktisk at få vist kontaktoplysninger, mens du gennemser forskellige mails.

Du kan finde flere oplysninger i [Sådan bruger du tilføjelsesprogrammer i Outlook online](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

## <a name="work-with-contacts-and-documents-using-the-contact-insights-add-in"></a>Arbejde med kontaktpersoner og dokumenter ved hjælp af tilføjelsesprogrammet Kontaktoplysninger

Antag, at du får en e-mail fra en kunde, som ønsker et tilbud på nogle varer. I Outlook kan du åbne [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammet direkte. Programmet genkender afsenderen som debitor og åbner debitorkortet for virksomheden. Fra dette dashboard kan du få vist oversigtsoplysninger om kunden samt gå i dybden for at få yderligere oplysninger om bestemte dokumenter. Du kan også se nærmere på salgsoversigten for debitoren. Hvis det er en ny kontakt, kan du oprette vedkommende som en ny kunde i [!INCLUDE[prod_short](includes/prod_short.md)] uden at forlade Outlook.  

I tilføjelsesprogrammet kan du oprette et salgstilbud og sende det tilbage til kunden uden at forlade Outlook. Alle oplysninger, du behøver for at sende salgstilbuddet, er tilgængelige i din virksomheds Indbakke i Outlook. Når du har indtastet dataene, kan du bogføre tilbuddet og sende det via e-mail. [!INCLUDE[prod_short](includes/prod_short.md)] genererer en .PDF-fil med salgstilbuddet og vedhæfter den i den mailmeddelelse, du laver udkast til i tilføjelsesprogrammet.  

På samme måde, hvis du modtager en e-mail fra en leverandør, kan du bruge tilføjelsesprogrammet til at arbejde med kreditorer og købsfakturaer.  

I nogle tilfælde kan det være praktisk at kunne se flere felter, end du kan i tilføjelsesprogrammet, f.eks når du skal udfylde linjerne i en faktura. For at få lidt mere plads til at arbejde på kan du åbne tilføjelsesprogrammet på en separat side. Det er stadig en del af Outlook, men du har mere plads. Når du angiver data for dokumentet gemmes ændringerne automatisk i det vindue, du har åbnet. I de følgende afsnit gennemgås nogle grundlæggende opgaver, så du får en generel forståelse af, hvordan du bruger den.

> [!TIP]
> Opgaverne forklarer, hvordan du bruger tilføjelsesprogrammet fra en e-mail-meddelelse. Men du kan gøre det samme fra en kalenderaftale i Outlook.

### <a name="look-up-a-business-contact-when-composing-an-email"></a>Slå en forretningskontaktperson op ved oprettelse af en e-mail

1. Opret en ny e-mail.
2. På båndet skal du gå til **[!INCLUDE[prod_short](includes/prod_short.md)]** og vælge **Kontaktoplysninger**. Hvis du bruger Outlook på World Wide Web, skal du i Outlook nederst på e-mailen og vælge ![ikonet for Business Central-tilføjelse i Outlook.](media/outlook-business-central-icon.png) > **Kontaktoplysninger**.
3. I **[!INCLUDE[prod_short](includes/prod_short.md)]**-tilføjelsesruden, der åbnes, skal du søge og vælge den ønskede kontakt.

    Der vises en oversigt over kontakten i ruden, og kontaktpersonen tilføjes på linjen **Til** i e-mailen.

### <a name="view-and-change-the-contact-details-or-switch-company"></a>Få vist og Rediger kontaktoplysninger eller Skift regnskab

Handlingslinjen øverst i [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammet indeholder flere handlinger, der gør din grave længere tid i detaljer om kontakten og ændringer.

![Aktivér handlingslinjen i Business Central-tilføjelsesprogram i Outlook.](media/outlook-addin-action-bar.png)

Du kan f. eks. åbne alle kontaktoplysninger, som du får vist dem i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du arbejder med mere end ét [!INCLUDE[prod_short](includes/prod_short.md)]-regnskab, kan du nemt skifte mellem firmaer.

### <a name="track-incoming-documents"></a>Registrér indgående dokumenter 

Du skal måske bruge listen over **Indgående bilag** i [!INCLUDE[prod_short](includes/prod_short.md)] til at spore dokumenter til behandling, som kreditorerne sender til dig, f. eks. en købsfaktura, der skal betales. Hvis du gør det, kan du nemt oprette indkommende dokumenter fra Outlook-tilføjelsesprogrammet og medtage vedhæftede filer i e-mail.

1. Når du modtager en e-mail fra en leverandør, der har en vedhæftet fil, skal du vælge ![ikonet Business central-tilføjelsesprogrammet i Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Kontaktoplysninger**. 

2. På handlingslinjen i tilføjelsesprogrammet skal du vælge **Vis flere handlinger** og derefter vælge **Send til indgående dokumenter...**. 

### <a name="create-and-send-new-document-to-a-contact"></a>Oprette og sende et nyt dokument til en kontaktperson

1. Vælg på båndet eller nederst i e-mailen ![ikonet Business central-tilføjelsesprogram i Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Ny**, og vælg derefter den dokumenttype, du vil oprette, f.eks. **Salgstilbud**.
2. Foretag ændringer af dokumentet i ruden med **[!INCLUDE[prod_short](includes/prod_short.md)]**-tilføjelsesprogrammet.
3. Når dokumentet er klar til at blive sendt til kontakten, skal du på handlingslinjen vælge **Vis flere handlinger** og derefter vælge handlingen **Send via e-mail**.

## <a name="view-a-document-from-an-email-using-the-document-view-add-in"></a>Vise et dokument fra en e-mail ved hjælp af tilføjelsesprogrammet dokumentvisning

Uanset om det er en mail, du har sendt eller modtaget, kan du overflade alle [!INCLUDE[prod_short](includes/prod_short.md)]-dokumenter, f. eks. salgstilbuddet, direkte i Outlook. Derfra kan du foretage ændringer og navigere til relaterede oplysninger på samme måde som i [!INCLUDE[prod_short](includes/prod_short.md)].

Hvis du bruger Outlook-appen, skal du blot vælge **Dokumentlink** øverst i e-mailen. Til Outlook på World Wide Web skal du se efter hyperlinket dokumentreference i e-mailen. Reference linkteksten vil indeholde bilagsnummeret, som er baseret på den nummerserie, der bruges i [!INCLUDE[prod_short](includes/prod_short.md)]. F. eks. vil linket til et salgstilbud være noget som **Salgstilbud S-QUO1000**.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Blive køreklar](ui-get-ready-business.md)  
[Få Business Central på min mobilenhed](install-mobile-app.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Minimumkrav til Outlook](product-requirements.md#outlook)  
[Bruge tilføjelsesprogrammer i Outlook på internettet](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]