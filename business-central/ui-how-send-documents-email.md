---
title: Sende dokumenter og e-mails
description: 'Du kan definere indhold, der skal indsættes i brødteksten i en mail, f.eks. et PayPal-link. Du kan også knytte dokumenter til mails.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'SMTP, mail, Microsoft 365, cover, body, PayPal, layout'
ms.search.form: '41,'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Sende dokumenter og e-mails

Du kan nemt dele oplysninger og dokumenter, f.eks. salgs- og købsordrer og fakturaer, via mail direkte fra [!INCLUDE[prod_short](includes/prod_short.md)] uden at skulle åbne en mailapp.  

Du kan sende næsten alle typer dokumenter som vedhæftede PDF-filer. Du kan også oprette et rapportlayout, der indeholder oplysninger fra dokumentet i e-mail-teksten, sammen med tekst, som gør e-mailen mere brugervenlig, f.eks. en standardhilsen. Du kan finde flere oplysninger i [Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md).

Når du sender fakturaer, kan du gøre det nemmere for kunderne at foretage betalinger via en betalingstjeneste, som f.eks. PayPal, ved automatisk at tilføje oplysninger og en kæde til tjenesten i e-mailen. Du kan finde flere oplysninger i [Aktivere debitorbetalinger via betalingstjenester](sales-how-enable-payment-service-extensions.md).

For at aktivere mails fra [!INCLUDE[prod_short](includes/prod_short.md)] skal du starte den assisterede opsætningsvejledning **Konfigurer mail** i rollecenteret. Du kan finde flere oplysninger i [Konfigurer mail](admin-how-setup-email.md).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] understøtter kun udgående mailkommunikation. Du kan heller ikke modtage svar fra appen.

## Sådan sendes dokumenter som mail

Denne fremgangsmåde beskriver, hvordan du vedhæfter en bogført-salgsfaktura til en e-mail som PDF-fil og med dokumentspecifik e-mail-tekst. Fremgangsmåden er den samme for de andre dokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgsfakturaer**, og vælg derefter det relaterede link.
2. Vælg den relevante bogførte salgsfaktura, vælg **Udskriv/Send**, og vælg derefter handlingen **Send med e-mail**.
3. I feltet **Mail** skal du vælge **Ja (Bed om indstillinger)**. Du kan finde flere oplysninger i [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).

    Hvis feltet **Mail** på siden **Send bilag til** indstilles til **Ja (Bed om indstillinger)**, åbnes siden **Send mail** forhåndsudfyldt med kontaktpersonen i feltet **Til:** og dokumentet vedhæftet som PDF-fil. I feltet **Tekst** kan du enten indtaste tekst manuelt, eller du kan få udfyldt feltet med dokumentspecifikke brødtekst i mail, som du har oprettet.

4. Vælg knappen **OK**.
5. I feltet **Til:** skal du angive en gyldig mailadresse. Standardværdien er kundens mailadresse.
6. Brug feltet **Emne** til at indtaste en sigende emnetekst. Standardværdien er debitornavnet og fakturanummeret.
7. I feltet **Vedhæftet fil** er den genererede faktura som standard vedhæftet som en PDF-fil.
8. Brug feltet **Tekst** til at indtaste en kort meddelelse til modtageren.

    Hvis en dokumentspecifik tekst i mail er angivet på siden **Rapportvalg - salg**, udfyldes **Brødtekst** automatisk. Du kan finde flere oplysninger i [angive genanvendelige e-mail-tekst og layout](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).
9. Vælg knappen **OK** for at sende mailen.

> [!NOTE]  
> Hvis du ikke vil angive mailindstillinger, hver gang du sender en mail med et dokument, kan du vælge indstillingen **Ja (Brug standardindstillinger)** i feltet **Mail** på siden **Send bilag til**. I så fald åbnes siden **Send mail** ikke. Se trin 4. Du kan finde flere oplysninger i [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).  

## Sådan skrives og sendes en e-mail

Du kan hurtigt oprette e-mails til kontakter, debitorer, kreditorer, sælgere/indkøbere og bankkonti direkte fra siderne til de pågældende enheder. Vælg **proces**, og send derefter **e-mails** for at åbne e-mail-editoren. I forbindelse med bankkonti er handlingen **Send E-mail** under **Handlinger**.

> [!TIP]
> Hvis du ofte sender e-mailmeddelelser, der ligner hinanden, eller du vil sende en masse kommunikation, f. eks. for at annoncere en salgskampagne, kan du bruge Word-skabeloner med e-mail til at gøre processen hurtigere. Du kan oprette en skabelon for en eller flere enheder, f. eks. kunder, leverandører og kontakter, som vil generere indholdet af en e-mail for dig, og endda tilpasse indholdet for modtageren baseret på data i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Bruge Word-skabeloner til masse kommunikation](ui-mail-merge.md).  

### Vedhæfte dokument til en e-mail

Du kan vedhæfte dokumenter til e-mails på flere måder.

Hvis du er tildelt et e-mailscenarie med relation til det objekt, du sender e-mailen til, eller hvis det dokument, du sender, bliver du muligvis automatisk føjet til din meddelelse. Det skyldes, at der er tildelt en standard vedhæftning til e-mail-scenariet. Du kan slette den vedhæftede fil, hvis du ikke vil sende den med din meddelelse. Du kan finde flere oplysninger i [Tildele e-mailscenarier til e-mailkonti](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts). 

Hvis du selv vil vedhæfte en fil, skal du bruge følgende handlinger i e-mail-editoren:

* Vælg **Tilføj fil** for at vælge en fil.
* Vælg **Tilføj filer fra standardmarkeringen**, hvis du vil tilføje en fil, der er knyttet til e-mail-scenariet manuelt.
* Vælg **Tilføj fil fra kildedokumentet** for at vælge en fil, der er vedhæftet det dokument, du arbejder med. Filerne er enten vedhæftet selve dokumentet eller på en eller flere af dens linjer.

## Dokumenter, der er markeret som udskrevne, når de sendes

Nogle dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)] har et felt, der angiver, hvor mange gange dokumentet er blevet udskrevet. Tallet i feltet <!--"that field?" need a name...--> opdateres også, hvis du sender dokumentet med e-mail, fordi der er genereret en PDF-fil til den. Nummeret opdateres, selvom du ikke sender e-mailen. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## Sendte mails og din mail-udbakke

[!INCLUDE[prod_short](includes/prod_short.md)] gemmer de mails, som du sender, på siden **Sendt post**. På den måde kan du sende mails igen eller sende dem videre til en anden. Hvis du ikke kan finde en mail i dine sendt post, skal du lede efter den på siden **Mailudbakke**. 

> [!NOTE]
> Afhængigt af det filtypenavn, din virksomhed bruger til e-mail, kan administratorer få vist en liste over meddelelser, som alle har sendt, men ikke indholdet af meddelelserne

**E-mailudbakke** er det sted, hvor du kan finde de e-mails, du har gemt som kladder, og e-mails, der ikke kunne sendes, f.eks. hvis e-mailadressen er ugyldig. I forbindelse med meddelelser, som ikke kunne sendes, kan du vælge **Vis fejl** eller **Undersøg fejl** for at løse problemet.  

## Se relateret [Microsoft-træning](/training/modules/set-up-email/)

## Se også

[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Konfigurere mail](admin-how-setup-email.md)  
[Fakturere salg](sales-how-invoice-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
