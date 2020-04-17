---
title: Konfigurere mail i Business Central | Microsoft Docs
description: Beskriver, hvordan du bruger virksomhedens SMTP-server til at sende og modtage mails i Business Central eller alternativt kan bruge de mailserverindstillinger, der blev oprettet med Office 365-abonnementet.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 9ece89b1d797d31a99c92f1bb292280b7f54ab7b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187264"
---
# <a name="set-up-email"></a>Konfigurer mail
Når du vil sende og modtage mails fra [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du udfylde felterne på siden **SMTP-mailopsætning**.

I stedet for at angive detaljer om SMTP-serveren manuelt kan du bruge funktionen **Apply Office 365 Server-indstillinger**, der bruger oplysninger fra dit abonnement på Office 365.

Du kan enten oprette mail manuelt, som beskrevet nedenfor, eller du kan få hjælp af den assisterede opsætningsvejledning **Mailopsætning**. Du kan finde flere oplysninger under [Blive klar til at handle](ui-get-ready-business.md).  

## <a name="to-set-up-email"></a>Sådan konfigurer du mail
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **SMTP-mailopsætning**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Hvis du bruger en konto, der kræver tofaktorgodkendelse, skal den adgangskode, du angiver i feltet **Adgangskode**, være den samme, som du bruger til dit abonnement på Office 365, og det skal være af typen **Appadgangskode**. Du kan finde flere oplysninger under [Administration af appadgangskoder til totrinsbekræftelse](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Du kan også vælge handlingen **Anvend Office 365 Server-indstillinger** for at indsætte de oplysninger, der er allerede defineret til Office 365-abonnementet.
4. Når alle felter er udfyldt korrekt, kan du vælge handlingen **Test mailopsætning**.
5. Når testen er gennemført, skal du lukke siden.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Bruge en erstatningsafsenderadresse på udgående mailmeddelelser
Alle udgående mailmeddelelser fra [!INCLUDE[d365fin](includes/d365fin_md.md)] vil bruge standardadressen for den konto, som du har angivet på siden SMTP-mailopsætning, som beskrevet ovenfor. Du kan imidlertid bruge funktionerne **Send som** eller **Send på vegne af** på Exchange-serveren for at ændre afsenderadressen i udgående meddelelser. [!INCLUDE[d365fin](includes/d365fin_md.md)] bruger standardkontoen til at godkende til Exchange, men den vil enten erstatte afsenderadressen med den, du angiver, eller ændre den med "på vegne af."

Følgende er eksempler på, hvordan Send som og Send på vegne af bruges i [!INCLUDE[d365fin](includes/d365fin_md.md)].:

 * Når du sender dokumenter, f.eks. købs-eller salgsordrer, til kreditorer og debitorer, kan det være en god ide at få dem vist til at komme fra en _noreply@yourcompanyname.com_-adresse.
 * Når arbejdsprocessen sender en anmodning om godkendelse pr. mail med anmoderens mailadresse.

> [!Note]
> Du kan kun bruge én konto til at erstatte afsenderadresser. Det vil sige, at du ikke kan have én erstatningsadresse til indkøbsprocesser og en anden til salgsprocesser.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Sådan opsættes erstatningsafsenderadressen for alle udgående mailmeddelelser
1. Find den postkasse, der skal bruges som erstatningsadresse, i **Exchange Administrationscenter** til din Office 365 konto, og kopiér eller notér adressen. Hvis du har brug for en ny adresse, skal du gå til Microsoft 365 administration for at oprette en ny bruger og oprette postkassen.
2. I [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **SMTP-mailopsætning** og dernæst vælge det relaterede link.
3. Angiv erstatningsadressen i feltet **Send som**.
4. Kopiér eller notér adressen i feltet **bruger-id**.
5. Find den postkasse, der skal bruges som erstatningsadresse, i **Exchange Administrationscenter**, og angiv derefter adressen fra feltet **bruger-id** i feltet **Send som**. Du kan finde flere oplysninger under [Brug af EAC til at tildele tilladelser til individuelle postkasser](/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Sådan bruges erstatningsadressen i godkendelsesarbejdsgange
1. I [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **SMTP-mailopsætning** og dernæst vælge det relaterede link.
2. Kopiér eller notér adressen i feltet **bruger-id**.
3. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugeropsætning af godkendelser**, og vælg derefter det relaterede link.
4. I **Exchange Administrationscenter** skal du finde postkasserne for hver bruger angivet på siden **Brugeropsætning af godkendelser** og i feltet **Send som** indtaste adressen fra feltet **bruger-id** på siden **SMTP-mailopsætning** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Administrere tilladelser for modtagere](/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. I [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **SMTP-mailopsætning** og dernæst vælge det relaterede link.
6. Hvis du vil aktivere erstatning, skal du aktivere funktionen til skift af **Tillad afsendererstatning**.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] bestemmer, hvilken adresse der skal vises i følgende rækkefølge: <br><br> 1. Den adresse, der er angivet i feltet **Mail** på siden **Brugeropsætning af godkendelser** for meddelelser i en arbejdsgang. <br> 2. Den adresse, der er angivet i feltet **Send som** på siden **SMTP-mailopsætning**. <br> 3. Den adresse, der er angivet i feltet **Bruger-id** på siden **SMTP-mailopsætning**.


## <a name="see-also"></a>Se også

[Delte postkasser i Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som din virksomheds Indbakke i Outlook](admin-outlook.md)  
[Få [!INCLUDE[d365fin](includes/d365fin_md.md)] på min mobilenhed](install-mobile-app.md)
