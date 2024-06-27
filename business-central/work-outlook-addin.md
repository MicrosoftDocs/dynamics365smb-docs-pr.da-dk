---
title: Bruge Outlook sammen med Business Central
description: 'Denne tjeneste er tæt integreret med Microsoft 365, så du kan administrere alle dine forretningsaktiviteter og sende og modtage mail til og fra kunder og leverandører direkte i Outlook.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'SMTP, mail, Microsoft 365'
ms.date: 06/14/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="use-business-central-as-your-business-inbox-in-outlook"></a>Brug Business Central som din virksomheds Indbakke i Outlook

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

    Start med at logge på Outlook og åbne en e-mailmeddelelse. Hvis du bruger Outlook-appen, skal du så gå til båndet og se efter **[!INCLUDE[prod_short](includes/prod_short.md)]**.  Hvis du bruger Outlook på internettet, skal du øverst i mailen vælge **Apps** ![Viser knappen apps button i Outlook.](media/apps-icon.png) > **Business Central** ![Ikon for Business Central-tilføjelsesprogram i Outlook.](media/outlook-business-central-icon.png) eller vise flere handlinger ![Vise flere handlinger for en mail i Outlook.](media/outlook-more-actions-button.png) knap.

    ![Aktivér Business Central-tilføjelsesprogram i Outlook.](media/outlook-business-central-addin.png)

   Hvis du har installeret tilføjelsesprogrammet på egen hånd og har valgt at få et e-mail-eksempel på en e-mail, skal du kontrollere din indbakke for velkomstmailen. Denne e-mail indeholder oplysninger, der kan hjælpe dig i gang.

Første gang du bruger tilføjelsesprogrammet [!INCLUDE[prod_short](includes/prod_short.md)], kan du blive bedt om at logge på i ruden med tilføjelsesprogrammet. Hvis det er tilfældet, skal du vælge **Log på nu** og følge instruktionerne på skærmen for at logge på Business central ved hjælp af din konto.

> [!TIP]
> Hvis du bruger den nye Outlook på World Wide Web, kan du fastgøre **[!INCLUDE[prod_short](includes/prod_short.md)]**, så det altid er umiddelbart synlig, i stedet for at gå til knappen flere handlinger, hvilket gør det praktisk at få vist kontaktoplysninger, mens du gennemser forskellige mails.

Du kan finde flere oplysninger i [B ruge tilføjelsesprogrammer i Outlook online](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

## <a name="work-with-contacts-and-documents-using-the-contact-insights-add-in"></a>Arbejde med kontaktpersoner og dokumenter ved hjælp af tilføjelsesprogrammet Kontaktoplysninger

Antag, at du får en e-mail fra en kunde, som ønsker et tilbud på nogle varer. I Outlook kan du åbne [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammet direkte. Programmet genkender afsenderen som debitor og åbner debitorkortet for virksomheden. Fra dette dashboard kan du få vist oversigtsoplysninger om kunden samt gå i dybden for at få yderligere oplysninger om bestemte dokumenter. Du kan også se nærmere på salgsoversigten for debitoren. Hvis det er en ny kontakt, kan du oprette vedkommende som en ny kunde i [!INCLUDE[prod_short](includes/prod_short.md)] uden at forlade Outlook.  

I tilføjelsesprogrammet kan du oprette et salgstilbud og sende det tilbage til kunden uden at forlade Outlook. Alle oplysninger, du behøver for at sende salgstilbuddet, er tilgængelige i din virksomheds Indbakke i Outlook. Når du har indtastet dataene, kan du bogføre tilbuddet og sende det via e-mail. [!INCLUDE[prod_short](includes/prod_short.md)] genererer en .PDF-fil med salgstilbuddet og vedhæfter den i den mailmeddelelse, du laver udkast til i tilføjelsesprogrammet.  

På samme måde, hvis du modtager en e-mail fra en leverandør, kan du bruge tilføjelsesprogrammet til at arbejde med kreditorer og købsfakturaer.  

I nogle tilfælde kan det være praktisk at kunne se flere felter, end du kan i tilføjelsesprogrammet, f.eks når du skal udfylde linjerne i en faktura. For at få lidt mere plads til at arbejde på kan du åbne tilføjelsesprogrammet på en separat side. Det er stadig en del af Outlook, men du har mere plads. Når du angiver data for dokumentet gemmes ændringerne automatisk i det vindue, du har åbnet. I de følgende afsnit gennemgås nogle grundlæggende opgaver, så du får en generel forståelse af, hvordan du bruger den.

> [!TIP]
> Opgaverne forklarer, hvordan du bruger tilføjelsesprogrammet fra en e-mail-meddelelse. Men du kan gøre det samme fra en kalenderaftale i Outlook.

### <a name="look-up-a-business-contact-when-composing-an-email"></a>Slå en forretningskontaktperson op ved oprettelse af en e-mail

1. Opret en ny e-mail.
2. På båndet skal du gå til **[!INCLUDE[prod_short](includes/prod_short.md)]** og vælge **Kontaktoplysninger**. Hvis du bruger Outlook på internettet, skal du øverst i meddelelsen vælge **Apps** ![Viser knappen apps button i Outlook.](media/apps-icon.png) > **Business Central** ![Ikon for Business Central-tilføjelsesprogram i Outlook.](media/outlook-business-central-icon.png) > **Kontaktoplysninger**.
3. I **[!INCLUDE[prod_short](includes/prod_short.md)]**-tilføjelsesruden, der åbnes, skal du søge og vælge den ønskede kontakt.

    Der vises en oversigt over kontakten i ruden, og kontaktpersonen tilføjes på linjen **Til** i e-mailen.

### <a name="view-and-change-the-contact-details-or-switch-company"></a>Få vist og Rediger kontaktoplysninger eller Skift regnskab

Handlingslinjen øverst i [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammet indeholder flere handlinger, der gør din grave længere tid i detaljer om kontakten og ændringer.

![Aktivér handlingslinjen i Business Central-tilføjelsesprogram i Outlook.](media/outlook-addin-action-bar.png)

Du kan f. eks. åbne alle kontaktoplysninger, som du får vist dem i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du arbejder med mere end ét [!INCLUDE[prod_short](includes/prod_short.md)]-regnskab, kan du nemt skifte mellem firmaer.

### <a name="track-incoming-documents"></a>Registrér indgående dokumenter

Du skal måske bruge listen over **Indgående bilag** i [!INCLUDE[prod_short](includes/prod_short.md)] til at spore dokumenter til behandling, som kreditorerne sender til dig, f. eks. en købsfaktura, der skal betales. Hvis du gør det, kan du nemt oprette indkommende dokumenter fra Outlook-tilføjelsesprogrammet og medtage vedhæftede filer i e-mail.

1. Når du modtager en e-mail fra en leverandør, der har en vedhæftet fil, skal du vælge ![ikonet Business central-tilføjelsesprogrammet i Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Kontaktoplysninger**.  

2. På handlingslinjen i tilføjelsesprogrammet skal du vælge **Vis flere handlinger** og derefter vælge **Send til indgående dokumenter...** .  

### <a name="create-and-send-new-document-to-a-contact"></a>Oprette og sende et nyt dokument til en kontaktperson

1. Vælg på båndet eller nederst i e-mailen ![ikonet Business central-tilføjelsesprogram i Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Ny**, og vælg derefter den dokumenttype, du vil oprette, f.eks. **Salgstilbud**.
2. Foretag ændringer af dokumentet i ruden med **[!INCLUDE[prod_short](includes/prod_short.md)]**-tilføjelsesprogrammet.
3. Når dokumentet er klar til at blive sendt til kontakten, skal du på handlingslinjen vælge **Vis flere handlinger** og derefter vælge handlingen **Send via e-mail**.

### <a name="attach-files-to-records"></a>Vedhæfte filer til poster

Din e-mail-indbakke fungerer ofte som en kilde til indgående filer, der initierer eller fjerner blokering af arbejdsgange. Filer kan omfatte ting som f. eks. PDF-betalinger, fotografier af varer eller krav i et Word-dokument. Når du arbejder i Outlook med Business Central-poster som f. eks. leverandører, debitorer, købsfakturaer eller salgsordrer, kan du vedhæfte filerne til posterne.

Du kan vedhæfte filer på flere måder. Den ene måde er at overføre filer fra enheden. Den anden måde er at overføre filer, der er knyttet til en e-mail. Antag f. eks., at du får en e-mail med filer fra en kontaktperson. Tilføjelsesprogrammet viser automatisk den kontaktpost, der svarer til e-mail-afsenderen. Derfra kan du navigere til et dokument for kontakten, f. eks. den seneste salgsordre. Når du har identificeret den rækkefølge, e-mailen er relateret til, kan du hurtigt overføre filerne fra mailen til denne ordre.

![Viser, hvordan du føjer vedhæftede filer fra en e-mail til poster i Business central.](media/outlook-attach-files.png)

Når du har vedhæftet en fil, kan medarbejderne straks hente og få vist filen fra faktaboksen **Vedhæftede filer** i en hvilken som helst af deres Business Central-klienter. De kan også åbne filen i OneDrive for at dele og samarbejde med deres afdeling.

#### <a name="how-to-attach-a-file"></a>Sådan vedhæftes en fil

1. Åbn e-mailen, Vælg ![ikonet for tilføjelsesprogrammet Business Central i Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Kontaktoplysninger**.
2. Vælg **Vis flere handlinger** > **Vedhæftede filer** på handlingslinjen i tilføjelsesprogrammet.

    Siden **Vedhæftede dokumenter** åbner for at få vist en oversigt over de dokumenter, der allerede er knyttet til posten.
3. Vælg **Vedhæftede filer...**, og vælg derefter en af følgende indstillinger:

   - Vælg **Vedhæft fra mail** for at overføre alle eller udvalgte filer, som er knyttet til e-mailen.
   - Vælg **Overfør fra fil** for at sende en eller flere filer fra enheden.

> [!NOTE]
> Du kan ikke vedhæfte filer til alle poster. Funktionen er tilgængelig for poster, hvor der bruges faktaboksen **Vedhæftede filer**, f. eks. kreditor, debitor, købsfaktura eller salgsordre.

## <a name="view-a-document-from-an-email-using-the-document-view-add-in"></a>Vise et dokument fra en e-mail ved hjælp af tilføjelsesprogrammet dokumentvisning

Uanset om det er en mail, du har sendt eller modtaget, kan du overflade alle [!INCLUDE[prod_short](includes/prod_short.md)]-dokumenter, f. eks. salgstilbuddet, direkte i Outlook. Derfra kan du foretage ændringer og navigere til relaterede oplysninger på samme måde som i [!INCLUDE[prod_short](includes/prod_short.md)].

Hvis du bruger Outlook-appen, skal du blot vælge **Dokumentlink** øverst i e-mailen. Til Outlook på World Wide Web skal du se efter hyperlinket dokumentreference i e-mailen. Reference linkteksten vil indeholde bilagsnummeret, som er baseret på den nummerserie, der bruges i [!INCLUDE[prod_short](includes/prod_short.md)]. F. eks. vil linket til et salgstilbud være noget som **Salgstilbud S-QUO1000**.  

> [!TIP]
> Starter i 2022 udgivelsesbølge 1 ved at åbne et nyt browservindue i et nyt browservindue med alle de egenskaber, du kender fra [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan navigere fra et dokument til en liste og tilbage igen, åbne lister i Excel, sende dokumenter til udskrivning og køre eller få vist relaterede rapporter. Du har også alle de velkendte tastaturgenveje, når du åbner dokumenter fra Outlook.  

## <a name="see-also"></a>Se også

[Blive køreklar](ui-get-ready-business.md)  
[Få Business Central på min mobilenhed](install-mobile-app.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Minimumkrav til Outlook](product-requirements.md#outlook)  
[Brug tilføjelsesprogrammer i Outlook på internettet](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
