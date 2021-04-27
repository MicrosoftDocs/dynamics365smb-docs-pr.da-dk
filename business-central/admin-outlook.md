---
title: Bruge Business Central sammen med Outlook | Microsoft Docs
description: Denne tjeneste er tæt integreret med Microsoft 365, så du kan administrere alle dine forretningsaktiviteter og sende og modtage mail til og fra kunder og leverandører direkte i Outlook.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ee9587b323fe1b104a85319eba03bfdcfce8c13e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777437"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Bruge Business Central som din virksomheds Indbakke i Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] introducerer muligheden for at administrere forretningsinteraktioner med kunder og leverandører direkte i Microsoft Outlook. Med Outlook-tilføjelsesprogrammerne i [!INCLUDE[prod_short](includes/prod_short.md)] kan du se finansielle data, der er relateret til debitorer og kreditorer samt oprette og sende finansielle dokumenter, f.eks tilbud og fakturaer.  

## <a name="getting-the-add-in"></a>Få tilføjelsesprogrammet
Det er nemt at komme i gang med [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammet til Outlook. I den assisterende opsætningsvejledning **Konfigurer din virksomhedsindbakke i Outlook** kan du oprette forbindelsen til dig selv eller til din virksomhed, hvis virksomheden bruger Microsoft 365. Du skal blot angive dit Microsoft 365-brugernavn og din adgangskode, hvis du bliver bedt om det, og fortælle os, om du vil modtage et eksempel på en mailmeddelelse. [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammerne føjes derefter automatisk til Outlook. Du kan finde flere oplysninger i [Minimumkrav til Outlook](product-requirements.md#outlook).  

Når du derpå åbner Outlook, vises en mailmeddelelse fra *Dynamics 365 Business Central Administration*. De nye tilføjelsesprogrammer føjes til Outlook-båndet, og i browseren kan du se [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammerne lige over eller under brødteksten i mailen. Tilføjelsesprogrammerne opdateres med jævne mellemrum, og du får besked, når en ny version er klar i Outlook.  

> [!TIP]
> Hvis du bruger den nye Outlook online, kan [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammerne være skjult under **Flere handlinger**. Hvis du ofte bruger tilføjelsesprogrammet, kan du fastgøre det, så det altid er synligt med det samme. Du kan finde flere oplysninger i [Sådan bruger du tilføjelsesprogrammer i Outlook online](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

Hvis du arbejder med mere end ét [!INCLUDE[prod_short](includes/prod_short.md)]-regnskab, kan du nemt skifte mellem firmaer i Outlook. På tilføjelsesprogrammets handlingslinje skal du vælge **Flere handlinger**, hvorefter du kan se indstillingen for at skifte mellem virksomheder.  

<!--TEMP-->
> [!NOTE]
> Skift mellem virksomheder kræver frigivelsesbølge 2 i 2019 [!INCLUDE[prod_short](includes/prod_short.md)] eller nyere, som annonceret i [frigivelsesplanen](/dynamics365-release-plan/2019wave2/dynamics365-business-central/switch-between-companies-business-inbox-outlook).

Nogle virksomheder, der bruger Microsoft 365, begrænser brugernes adgang til at implementere tilføjelser. Derfor skal du kontrollere, at du har et Microsoft 365-abonnement, der omfatter e-mail, hvor du kan implementere tilføjelser. Hvis du vil prøve tilføjelsesprogrammet alligevel, kan du [prøve Microsoft 365 gratis](https://www.microsoft.com/microsoft-365/try).  

## <a name="using-the-contact-insights-add-in"></a>Bruge tilføjelsesprogrammet Kontaktoplysninger
Antag, at du får en e-mail fra en kunde, som ønsker et tilbud på nogle varer. I Outlook kan du åbne [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammet direkte. Programmet genkender afsenderen som debitor og åbner debitorkortet for virksomheden. Fra dette dashboard kan du få vist oversigtsoplysninger om kunden samt gå i dybden for at få yderligere oplysninger om bestemte dokumenter. Du kan også se nærmere på salgsoversigten for debitoren. Hvis det er en ny kontakt, kan du oprette vedkommende som en ny kunde i [!INCLUDE[prod_short](includes/prod_short.md)] uden at forlade Outlook.  

I tilføjelsesprogrammet kan du oprette et salgstilbud og sende det tilbage til kunden uden at forlade Outlook. Alle oplysninger, du behøver for at sende salgstilbuddet, er tilgængelige i din virksomheds Indbakke i Outlook.  
Når du har indtastet dataene, kan du bogføre tilbuddet. Du kan derefter sende det via mail. [!INCLUDE[prod_short](includes/prod_short.md)] genererer en .PDF-fil med salgstilbuddet og vedhæfter den i den mailmeddelelse, du laver udkast til i tilføjelsesprogrammet.  

På samme måde, hvis du modtager en e-mail fra en leverandør, kan du bruge tilføjelsesprogrammet til at arbejde med kreditorer og købsfakturaer.  

I nogle tilfælde kan det være praktisk at kunne se flere felter, end du kan i tilføjelsesprogrammet, f.eks når du skal udfylde linjerne i en faktura. For at få lidt mere plads til at arbejde på kan du åbne tilføjelsesprogrammet på en separat side. Det er stadig en del af Outlook, men du har mere plads. Når du angiver data for dokumentet gemmes ændringerne automatisk i det vindue, du har åbnet. Når du er færdig med at indtaste data til dokumentet, kan du vælge knappen **OK**. Når du vælger tilføjelsesprogramruden i Outlook, opdateres dokumentet automatisk med de ændringer, du foretog i det udvidede vindue.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Oprettelse af fakturaer fra dine mødeaftaler
Nogle virksomheder registrerer alle fakturerbare aftaler i Outlook-kalenderen. Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du oprette fakturaen til kunden direkte fra emnet i kalenderen: Åbn aftalen, og derefter kan du åbne [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammet, søge efter eksisterende oplysninger eller oprette en faktura eller et andet salgsdokument dér.  

## <a name="doing-quick-document-lookup"></a>Foretage hurtigt dokumentopslag
[!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammet Dokumentlinks giver dig hurtig adgang til dokumenter, der nævnes i mails. Tilføjelsesprogrammet kan bruges i en mail, hvis der findes et gyldigt bilagsnummer i selve meddelelsen. Når tilføjelsesprogrammet åbnes, giver det hurtig adgang til dokumentet.  

F.eks. hvis du modtager en mail, hvor der i teksten står *S-QUO100*, identificerer [!INCLUDE[prod_short](includes/prod_short.md)] det som et salgstilbud, og så kan du åbne dette dokument i Outlook. I Outlook skal du vælge knappen **Dokumentlinks** umiddelbart oven over brødteksten i mailen. I Outlook-webappen skal du vælge teksten *S-QUO1001* i brødteksten i mailen.  

I tilføjelsesprogrammet Dokumentlinks kan du redigere og foretage handlinger i dokumentet, ligesom du kan i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="adding-the-add-ins-manually"></a>Manuel tilføjelse af tilføjelsesprogrammerne
I nogle tilfælde bliver tilføjelsesprogrammerne ikke føjet automatisk til Outlook. Selvom du eller en kollega har kørt den assisterede opsætningsvejledning på vegne af virksomheden, bliver [!INCLUDE[prod_short](includes/prod_short.md)] muligvis ikke vist i Outlook. Hvis du oplever dette problem, kan du tilføje [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammer manuelt.  

Først skal du kontrollere, at du har adgang til tilføjelsesprogrammerne på din Microsoft 365-konto. Åbn ganske enkelt Outlook i en browser, åbn en meddelelse, vælg **Flere handlinger** (...) øverst i meddelelsen, og vælg derefter **Hent tilføjelsesprogrammer** nederst på listen. Derved åbnes siden **Tilføjelsesprogrammer til Outlook**, hvor du kan aktivere [!INCLUDE[prod_short](includes/prod_short.md)] for Outlook. Derefter, når du går tilbage til Outlook, skulle [!INCLUDE[prod_short](includes/prod_short.md)] være tilgængeligt.  

På samme måde kan du i Outlook-skrivebordsklienten kontrollere, at [!INCLUDE[prod_short](includes/prod_short.md)] er angivet på siden **Hent tilføjelsesprogrammer**.  

I begge tilfælde, hvis [!INCLUDE[prod_short](includes/prod_short.md)] stadig ikke er tilgængelig, skal du hente manifest for tilføjelsesprogram-filerne. Du kan få flere oplysninger ved at kontakt Microsoft 365-administratoren.

## <a name="using-other-email-accounts"></a>Bruge andre mailkonti

Tilføjelsesprogrammerne er designet til at blive brugt sammen med Microsoft 365. Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, vil administratoren vide, om du kan bruge [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammerne i Outlook. Du kan finde flere oplysninger i [Hvilken mailadresse kan jeg bruge med [!INCLUDE[prod_short](includes/prod_short.md)]?](across-faq.md#email), og de artiklen [Funktioner, der kræver særlige omstændigheder](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances?toc=/dynamics365/business-central/toc.json) og [Hvorfor virker Outlook-tilføjelsesprogrammet ikke for mine brugere?](/dynamics365/business-central/dev-itpro/faq#why-doesnt-the-outlook-add-in-work-for-my-users?toc=/dynamics365/business-central/toc.json) i afsnittet med generelle ofte stillede spørgsmål i administrationsindholdet.  

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