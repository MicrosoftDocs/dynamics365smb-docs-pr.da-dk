---
title: "Oprette dokumentspecifikt indhold og vedhæftede filer til mailmeddelelser | Microsoft Docs"
description: "Du kan definere indhold, der skal indsættes i brødteksten i en mail, f.eks. et PayPal-link. Du kan også knytte dokumenter til mails."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, cover, body, PayPal, layout
ms.date: 03/30/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a31558764cf8c2bccde7598119216096803eb1ca
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="send-documents-by-email"></a>Sende dokumenter som mail
For at give oplysningerne i forretningsdokumenter hurtigt til samarbejdspartnere, f.eks betalingsoplysningerne i salgsdokumenter til debitorer, kan du bruge funktionen Rapportlayout til at definere dokumentspecifik tekst, der bliver automatisk indsat i brødteksten i mails. Du kan finde flere oplysninger under [Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md).

For at aktivere mails fra [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du starte den assisterede opsætning **Konfigurer mail** i rollecenteret.

Du kan sende praktisk talt alle dokumenttyper vedhæftet i mails direkte fra vinduet, der viser dokumentet. Ud over den vedhæftede fil kan du oprette dokumentspecifik brødtekst i mails med grundlæggende oplysninger fra dokumentet og med en foranstående standardtekst, der indeholder en hilsen til modtageren og introducerer dokumentet. Hvis du vil tilbyde kunderne at betale for salg elektronisk ved hjælp af en betalingstjeneste, f.eks PayPal, kan du automatisk få PayPal oplysninger og hyperlink indsat i selve mailen.

Fra alle understøttede dokumenter starter du mailen ved at vælge handlingen **Send** i bogførte dokumenter eller **Bogfør og send** i ikke-bogførte dokumenter.

Hvis feltet **Mail** i vinduet **Send bilag til** indstilles til **Ja (Bed om indstillinger)**, åbnes **Send mail** forhåndsudfyldt med kontaktpersonen i feltet **Til:** og dokumentet vedhæftet som PDF-fil. I feltet **Tekst** kan du enten indtaste tekst manuelt, eller du kan få udfyldt feltet med dokumentspecifikke brødtekst i mail, som du har oprettet.

Følgende procedure beskriver, hvordan du konfigurerer rapporten **Salg - faktura**, så den kan bruges til dokumentspecifik brødtekst i mail, når du sender mails med bogførte salgsfakturaer.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Sådan oprettes dokumentspecifik brødtekst i mail til salgsfakturaer
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Rapportvalg - Salg**, og vælg derefter det relaterede link.
2. I vinduet **Rapportvalg - salg** skal du vælge **faktura** i feltet **Forbrug**.
3. På en ny linje i feltet **Rapport-ID** skal du vælge f.eks. standardrapport 1306.
4. Markér afkrydsningsfeltet **Brug til brødtekst i mail**.
5. Vælg feltet **Layoutkode for brødtekst i mail**, og vælg derefter et layoutformat på rullelisten.

    Rapportlayout angiver formatet og indholdet af brødteksten i mailen, herunder standardtekst, som går forud for de centrale dokumentoplysninger i selve mailens brødtekst. Du kan se alle tilgængelige rapportlayout, hvis du vælger knappen **Vælg fra komplet liste** på listen.
6. For at få vist eller redigere layoutet, som brødteksten i mailen er baseret på, skal du vælge layoutet i vinduet **Rediger Layout** og derefter vælge handlingen **Tilpassede rapportlayouts**.
7. Hvis du vil tilbyde kunderne at betale for salg elektronisk, kan du konfigurere den relaterede betalingstjeneste, f.eks PayPal, og derefter kan du også automatisk få PayPal oplysninger og hyperlink indsat i selve mailen. Du kan finde flere oplysninger i [Aktivere debitorbetalinger via PayPal](sales-how-enable-payment-service-extensions.md).
8. Vælg knappen **OK**.

Nu, når du vælger, f.eks. **Send**-handlingen i vinduet **Bogført salgsfaktura**, indeholder brødtekst i mail dokumentoplysningerne i rapporten 1306 med foranstående standardtekst, hvor typografierne er i overensstemmelse med det rapportlayout, som du valgte under trin 5.

Følgende fremgangsmåde beskriver, hvordan du sender en bogført salgsfaktura som mailmeddelelse med dokumentet vedhæftet som en PDF-fil og med dokumentspecifik brødtekst i mail.

## <a name="to-send-documents-by-email"></a>Sådan sendes dokumenter som mail
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogf. salgsfakturaer**, og vælg derefter det relaterede link.
2. Vælg den relevante bogførte salgsfaktura, og vælg derefter handlingen **Send**. Vinduet **Send bilag til** åbnes.
3. I feltet **Mail** skal du vælge **Ja (Bed om indstillinger)**. Du kan finde flere oplysninger under [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).
4. Vælg knappen **OK**. Vinduet **Send mail** åbnes.
5. I feltet **Til:** skal du angive en gyldig mailadresse. Standardværdien er kundens mailadresse.
6. Brug feltet **Emne** til at indtaste en sigende emnetekst. Standardværdien er debitornavnet og fakturanummeret.
7. I feltet **Vedhæftet fil** er den genererede faktura som standard vedhæftet som en PDF-fil. Vælg opslagsknappen for at åbne filen eller tilknytte en anden.
8. Brug feltet **Tekst** til at indtaste en kort meddelelse til modtageren.

    Hvis en dokumentspecifik brødtekst i mail er angivet i vinduet **Rapportvalg - salg**, udfyldes **Brødtekst** automatisk. Du kan finde flere oplysninger i afsnittet "Sådan oprettes dokumentspecifik brødtekst i mail til salgsfakturaer" i dette emne.
9. Vælg knappen **OK** for at sende mailen.

> [!NOTE]  
>   Hvis du ikke vil angive mailindstillinger, hver gang du sender en mail med et dokument, kan du vælge indstillingen **Ja (Brug standardindstillinger)** i feltet **Mail** i vinduet **Send bilag til**. I så fald åbnes vinduet **Send mail** ikke. Se trin 4. Du kan finde flere oplysninger under [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).

## <a name="see-also"></a>Se også
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Konfigurere mail](madeira-how-setup-email.md)  
[Fakturere salg](sales-how-invoice-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

