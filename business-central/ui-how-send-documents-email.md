---
title: Oprette dokumentspecifikt mailindhold | Microsoft Docs
description: Du kan definere indhold, der skal indsættes i brødteksten i en mail, f.eks. et PayPal-link. Du kan også knytte dokumenter til mails.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, cover, body, PayPal, layout
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f318825b87b0c9aa51ef8493ba89a74a02384b73
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756863"
---
# <a name="send-documents-and-emails"></a>Sende dokumenter og e-mails
Du kan nemt dele oplysninger og dokumenter, f. eks. salgs-og købsordrer og fakturaer, via e-mail direkte fra [!INCLUDE[prod_short](includes/prod_short.md)] ] uden at skulle åbne en e-mailapp. 

Du kan sende næsten alle typer dokumenter som vedhæftede PDF-filer. Du kan også oprette et rapportlayout, der indeholder oplysninger fra dokumentet i e-mail-teksten, sammen med tekst, som gør e-mailen mere brugervenlig, f. eks. en standardhilsen. Du kan finde flere oplysninger under [Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md). <!--this topic does not mention how to set up a layout for email. Need to investigate.-->

Når du sender fakturaer, kan du gøre det nemmere for kunderne at foretage betalinger via en betalingstjeneste, som f. eks. PayPal, ved automatisk at tilføje oplysninger og en kæde til tjenesten i e-mailen. Du kan finde flere oplysninger i [Aktivere debitorbetalinger via betalingstjenester](sales-how-enable-payment-service-extensions.md).

For at aktivere mails fra [!INCLUDE[prod_short](includes/prod_short.md)] skal du starte den assisterede opsætningsvejledning **Konfigurer mail** i rollecenteret. Du kan finde flere oplysninger i [Konfigurer mail](admin-how-setup-email.md).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]] understøtter kun udgående mailkommunikation. Du kan heller ikke modtage svar fra appen.

## <a name="to-send-documents-by-email"></a>Sådan sendes dokumenter som mail
Denne fremgangsmåde beskriver, hvordan du vedhæfter en bogført-salgsfaktura til en e-mail som PDF-fil og med dokumentspecifik e-mail-tekst. <!--update this-->

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte salgsfakturaer**, og vælg derefter det relaterede link.
2. Vælg den relevante bogførte salgsfaktura, og vælg derefter handlingen **Udskriv/Send**.
3. I feltet **Mail** skal du vælge **Ja (Bed om indstillinger)**. Du kan finde flere oplysninger under [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).
    
    Hvis feltet **Mail** på siden **Send bilag til** indstilles til **Ja (Bed om indstillinger)**, åbnes siden **Send mail** forhåndsudfyldt med kontaktpersonen i feltet **Til:** og dokumentet vedhæftet som PDF-fil. I feltet **Tekst** kan du enten indtaste tekst manuelt, eller du kan få udfyldt feltet med dokumentspecifikke brødtekst i mail, som du har oprettet.

4. Vælg knappen **OK**.
5. I feltet **Til:** skal du angive en gyldig mailadresse. Standardværdien er kundens mailadresse.
6. Brug feltet **Emne** til at indtaste en sigende emnetekst. Standardværdien er debitornavnet og fakturanummeret.
7. I feltet **Vedhæftet fil** er den genererede faktura som standard vedhæftet som en PDF-fil.
8. Brug feltet **Tekst** til at indtaste en kort meddelelse til modtageren.

    Hvis en dokumentspecifik tekst i mail er angivet på siden **Rapportvalg - salg**, udfyldes **Brødtekst** automatisk. Der er flere oplysninger i [Angiv genanvendelig e-mailtekst og layout til salgs-og købsdokumenter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents).
9. Vælg knappen **OK** for at sende mailen.

> [!NOTE]  
> Hvis du ikke vil angive mailindstillinger, hver gang du sender en mail med et dokument, kan du vælge indstillingen **Ja (Brug standardindstillinger)** i feltet **Mail** på siden **Send bilag til**. I så fald åbnes siden **Send mail** ikke. Se trin 4. Du kan finde flere oplysninger under [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).  

## <a name="to-compose-and-send-an-email"></a>Sådan skrives og sendes en e-mail
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **E-mailkonti**, og vælg derefter det relaterede link.
2. Vælg den konto, e-mailen skal sendes fra, og vælg derefter handlingen **Sammensæt e-mail**.

## <a name="documents-marked-as-printed-when-they-are-sent"></a>Dokumenter, der er markeret som udskrevne, når de sendes
Nogle dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)] har et felt, der angiver, hvor mange gange dokumentet er blevet udskrevet. Tallet i feltet <!--"that field?" need a name...--> opdateres også, hvis du sender dokumentet med e-mail, fordi der er genereret en PDF-fil til den. Nummeret opdateres, selvom du ikke sender e-mailen. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## <a name="sent-emails-and-your-email-outbox"></a>Sendte mails og din mail Udbakke
[!INCLUDE[prod_short](includes/prod_short.md)]] gemmer de mails, som du sender, på siden **Sendt post**. På den måde kan du sende mails igen eller sende dem videre til en anden. Hvis du ikke kan finde en mail i dine sendt post, skal du lede efter den på siden **Mailudbakke**. 

> [!NOTE]
> Afhængigt af det filtypenavn, din virksomhed bruger til e-mail, kan administratorer få vist en liste over meddelelser, som alle har sendt, men ikke indholdet af meddelelserne

**E-mailudbakke** er det sted, hvor du kan finde de e-mails, du har gemt som kladder, og e-mails, der ikke kunne sendes, f. eks. hvis e-mailadressen er ugyldig. I forbindelse med meddelelser, som ikke kunne sendes, kan du vælge **Vis fejl** eller **Undersøg fejl** for at løse problemet.

## <a name="see-also"></a>Se også
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Konfigurere mail](admin-how-setup-email.md)  
[Fakturere salg](sales-how-invoice-sales.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]