---
title: Bruge Business Central sammen med Outlook | Microsoft Docs
description: Denne tjeneste er tæt integreret med Office 365, så du kan administrere alle dine forretningsaktiviteter og sende og modtage mail til og fra kunder og leverandører direkte i Outlook.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 08/14/2019
ms.author: edupont
ms.openlocfilehash: 70299f86a1ebc3251780eb05f8b68afeff23fa5e
ms.sourcegitcommit: 81b6062194bf04d8052a3cd394cc0b41e3f53e6d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/20/2019
ms.locfileid: "1887687"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Bruge Business Central som din virksomheds Indbakke i Outlook
[!INCLUDE[d365fin](includes/d365fin_md.md)] introducerer muligheden for at administrere forretningsinteraktioner med kunder og leverandører direkte i Microsoft Outlook. Med Outlook-tilføjelsesprogrammerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du se finansielle data, der er relateret til debitorer og kreditorer samt oprette og sende finansielle dokumenter, f.eks tilbud og fakturaer.  

## <a name="getting-the-add-in"></a>Få tilføjelsesprogrammet
Det er nemt at komme i gang med [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilføjelsesprogrammet til Outlook. I den assisterende opsætningsvejledning **Konfigurer din virksomhedsindbakke i Outlook** kan du oprette forbindelsen til dig selv eller til din virksomhed, hvis virksomheden bruger Office 365. Du skal blot angive dit Office 365 brugernavn og din adgangskode, hvis du bliver bedt om det, og fortælle os, om du vil modtage et eksempel på en mailmeddelelse. [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilføjelsesprogrammerne føjes derefter automatisk til Outlook. Du kan finde flere oplysninger i [Minimumkrav til Outlook](product-requirements.md#outlook).  

Når du derpå åbner Outlook, vises en mailmeddelelse fra *Dynamics 365 Business Central Administration*. De nye tilføjelsesprogrammer føjes til Outlook-båndet, og i browseren kan du se [!INCLUDE[prodshort](includes/prodshort.md)]-tilføjelsesprogrammerne lige over eller under brødteksten i mailen. Tilføjelsesprogrammerne opdateres med jævne mellemrum, og du får besked, når en ny version er klar i Outlook.  

> [!TIP]
> Hvis du bruger den nye Outlook i en browser, kan [!INCLUDE [prodshort](includes/prodshort.md)]-tilføjelsesprogrammerne være skjult under **Flere handlinger**.

Nogle virksomheder, der bruger Office 365, begrænser brugernes adgang til at implementere tilføjelser. Derfor skal du kontrollere, at du har et Office 365-abonnement, der omfatter mail, hvor du kan implementere tilføjelser. Hvis du vil prøve tilføjelsesprogrammet alligevel, kan du [prøve Office 365 gratis](https://products.office.com/try).  

## <a name="using-the-contact-insights-add-in"></a>Bruge tilføjelsesprogrammet Kontaktoplysninger
Antag, at du får en e-mail fra en kunde, som ønsker et tilbud på nogle varer. I Outlook kan du åbne [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilføjelsesprogrammet direkte. Programmet genkender afsenderen som debitor og åbner debitorkortet for hans firma. Fra dette dashboard kan du få vist oversigtsoplysninger om kunden samt gå i dybden for at få yderligere oplysninger om bestemte dokumenter. Du kan også se nærmere på salgsoversigten for debitoren. Hvis det er en ny kontakt, kan du oprette vedkommende som en ny kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)] uden at forlade Outlook.  

I tilføjelsesprogrammet kan du oprette et salgstilbud og sende det tilbage til kunden uden at forlade Outlook. Alle oplysninger, du behøver for at sende salgstilbuddet, er tilgængelige i din virksomheds Indbakke i Outlook.  
Når du har indtastet dataene, kan du bogføre tilbuddet. Du kan derefter sende det via mail. [!INCLUDE[d365fin](includes/d365fin_md.md)] genererer en .PDF-fil med salgstilbuddet og vedhæfter den i den mailmeddelelse, du laver udkast til i tilføjelsesprogrammet.  

På samme måde, hvis du modtager en e-mail fra en leverandør, kan du bruge tilføjelsesprogrammet til at arbejde med kreditorer og købsfakturaer.  

I nogle tilfælde kan det være praktisk at kunne se flere felter, end du kan i tilføjelsesprogrammet, f.eks når du skal udfylde linjerne i en faktura. For at få lidt mere plads til at arbejde på kan du åbne tilføjelsesprogrammet på en separat side. Det er stadig en del af Outlook, men du har mere plads. Når du angiver data for dokumentet gemmes ændringerne automatisk i det vindue, du har åbnet. Når du er færdig med at indtaste data til dokumentet, kan du vælge knappen **OK**. Når du vælger tilføjelsesprogramruden i Outlook, opdateres dokumentet automatisk med de ændringer, du foretog i det udvidede vindue.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Oprettelse af fakturaer fra dine mødeaftaler
Nogle virksomheder registrerer alle fakturerbare aftaler i Outlook-kalenderen. Med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du oprette fakturaen til kunden direkte fra emnet i kalenderen: Åbn aftalen, og derefter kan du åbne [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilføjelsesprogrammet, søge efter eksisterende oplysninger eller oprette en faktura eller et andet salgsdokument dér.  

## <a name="doing-quick-document-lookup"></a>Foretage hurtigt dokumentopslag
[!INCLUDE[d365fin](includes/d365fin_md.md)]-tilføjelsesprogrammet Dokumentlinks giver dig hurtig adgang til dokumenter, der nævnes i mails. Tilføjelsesprogrammet kan bruges i en mail, hvis der findes et gyldigt bilagsnummer i selve meddelelsen. Når tilføjelsesprogrammet åbnes, giver det hurtig adgang til dokumentet.  

F.eks. hvis du modtager en mail, hvor der i teksten står *S-QUO100*, identificerer [!INCLUDE[d365fin](includes/d365fin_md.md)] det som et salgstilbud, og så kan du åbne dette dokument i Outlook. I Outlook skal du vælge knappen **Dokumentlinks** umiddelbart oven over brødteksten i mailen. I Outlook-webappen skal du vælge teksten *S-QUO1001* i brødteksten i mailen.  

I tilføjelsesprogrammet Dokumentlinks kan du redigere og foretage handlinger i dokumentet, ligesom du kan i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="adding-the-add-ins-manually"></a>Manuel tilføjelse af tilføjelsesprogrammerne
I nogle tilfælde bliver tilføjelsesprogrammerne ikke føjet automatisk til Outlook. Selvom du eller en kollega har kørt den assisterede opsætningsvejledning på vegne af virksomheden, bliver [!INCLUDE[d365fin](includes/d365fin_md.md)] muligvis ikke vist i Outlook. Hvis du oplever dette problem, kan du tilføje [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilføjelsesprogrammer manuelt.  

Først skal du kontrollere, at du har adgang til tilføjelsesprogrammerne på din Office 365-konto. Åbn ganske enkelt Outlook i en browser, åbn en meddelelse, vælg **Flere handlinger** (...) øverst i meddelelsen, og vælg derefter **Hent tilføjelsesprogrammer** nederst på listen. Derved åbnes siden **Tilføjelsesprogrammer til Outlook**, hvor du kan aktivere [!INCLUDE[prodshort](includes/prodshort.md)] for Outlook. Derefter, når du går tilbage til Outlook, skulle [!INCLUDE[prodshort](includes/prodshort.md)] være tilgængeligt.  

På samme måde kan du i Outlook-skrivebordsklienten kontrollere, at [!INCLUDE[d365fin](includes/d365fin_md.md)] er angivet på siden **Hent tilføjelsesprogrammer**.  

I begge tilfælde, hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] stadig ikke er tilgængelig, skal du hente manifest for tilføjelsesprogram-filerne. Du kan få flere oplysninger ved at kontakte Office 365-administratoren.

## <a name="using-other-email-accounts"></a>Bruge andre mailkonti

Tilføjelsesprogrammerne er designet til at blive brugt sammen med Office 365. Hvis du bruger [!INCLUDE [prodshort](includes/prodshort.md)] lokalt, vil administratoren vide, om du kan bruge [!INCLUDE [prodshort](includes/prodshort.md)]-tilføjelsesprogrammerne i Outlook. Du kan finde flere oplysninger i [Hvilken mailadresse kan jeg bruge sammen med [!INCLUDE[prodshort](includes/prodshort.md)]?](across-faq.md#what-email-address-can-i-use-with-) og [Funktioner, der kræver særlige omstændigheder](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances).  

## <a name="see-also"></a>Se også

[Introduktion](product-get-started.md)  
[Få Business Central på min mobilenhed](install-mobile-app.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Minimumkrav til Outlook](product-requirements.md#outlook)  
[Bruge tilføjelsesprogrammer i Outlook på internettet](https://support.office.com/en-us/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  
