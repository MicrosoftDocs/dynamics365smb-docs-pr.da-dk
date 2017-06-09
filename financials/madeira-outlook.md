---
title: Bruge Dynamics 365 for Financials som din virksomheds Indbakke i Outlook | Microsoft Docs
description: Bruge Dynamics 365 for Financials som din virksomheds Indbakke i Outlook
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 03/28/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a872c8817c412953a64cb1adb8f8234f2801e8fa
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-as-your-business-inbox-in-outlook"></a>Bruge Dynamics 365 for Financials som din virksomheds Indbakke i Outlook
[!INCLUDE[d365fin](includes/d365fin_md.md)] introducerer muligheden for at administrere forretningsinteraktioner med kunder og leverandører direkte i Microsoft Outlook. Med Outlook-tilføjelsesprogrammerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du se finansielle data, der er relateret til debitorer og kreditorer samt oprette og sende finansielle dokumenter, f.eks tilbud og fakturaer.  

## <a name="get-the-add-in"></a>Hent tilføjelsesprogrammet
I [!INCLUDE[d365fin](includes/d365fin_md.md)] er et af trinnene i den assisterede opsætningsvejledning Introduktion vinduet **Kør din virksomhed fra Office 365**. I dette vindue skal du angive Office 365 brugernavn og adgangskode, når du klikker på knappen **Opsæt i Outlook**. [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilføjelsesprogrammerne føjes derefter automatisk til Outlook.  

Når du åbner Outlook, vises en e-mail fra Financials-administratoren. Det nye tilføjelsesprogram føjes til Outlook-båndet og i Outlook Web Access kan du se det i tilføjelsesprogrambåndet lige over brødteksten i mailen. Selve tilføjelsesprogrammet opdateres med jævne mellemrum, og du får besked, når en ny version er klar i Outlook.  

Nogle virksomheder, der bruger Office 365, begrænser brugertilladelser til at implementere programmer. Så skal du sørge for at have et Office 365 abonnement, der omfatter mail, og hvor du kan implementere tilføjelsesprogrammer. Hvis du vil prøve tilføjelsesprogrammet alligevel, kan du [prøve Office 365 gratis](https://products.office.com/try).  

## <a name="using-the-contact-insights-add-in"></a>Bruge tilføjelsesprogrammet Kontaktoplysninger
Antag, at du får en e-mail fra en kunde, som ønsker et tilbud på nogle varer. I Outlook kan du åbne Financials-tilføjelsesprogrammet direkte. Programmet genkender afsenderen som debitor og åbner debitorkortet for hans firma. Fra dette dashboard kan du få vist oversigtsoplysninger om kunden samt gå i dybden for at få yderligere oplysninger om bestemte dokumenter. Du kan også se nærmere på salgsoversigten for debitoren. Hvis det er en ny kunde, kan du oprette vedkommende som en ny kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)] uden at forlade Outlook.  

I tilføjelsesprogrammet kan du oprette et salgstilbud og sende det tilbage til kunden uden at forlade Outlook. Alle oplysninger, du behøver for at sende salgstilbuddet, er tilgængelige i din virksomheds Indbakke i Outlook.  
Når du har indtastet dataene, kan du bogføre tilbuddet. Du kan derefter sende det via mail. [!INCLUDE[d365fin](includes/d365fin_md.md)] genererer en .PDF-fil med salgstilbuddet og vedhæfter den i den mailmeddelelse, du laver udkast til i tilføjelsesprogrammet.  

På samme måde, hvis du modtager en e-mail fra en leverandør, kan du bruge tilføjelsesprogrammet til at arbejde med kreditorer og købsfakturaer.  

I nogle tilfælde kan det være praktisk at kunne se flere felter, end du kan i tilføjelsesprogrammet, f.eks når du skal udfylde linjerne i en faktura. For at få lidt mere plads til at arbejde på kan du åbne tilføjelsesprogrammet i et separat vindue. Det er stadig en del af Outlook, men du har mere plads. Når du angiver data for dokumentet gemmes ændringerne automatisk i det vindue, du har åbnet. Når du er færdig med at indtaste data til dokumentet, kan du vælge knappen **OK**. Når du vælger tilføjelsesprogramruden i Outlook, opdateres dokumentet automatisk med de ændringer, du foretog i det udvidede vindue.  

## <a name="create-invoices-from-your-meeting-appointments"></a>Oprette fakturaer fra dine mødeaftaler
Nogle virksomheder registrerer alle fakturerbare aftaler i Outlook-kalenderen. Med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du oprette fakturaen til kunden direkte fra emnet i kalenderen: Åbn aftalen, og derefter kan du åbne [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilføjelsesprogrammet, søge efter eksisterende oplysninger eller oprette en faktura eller et andet salgsdokument dér.  

## <a name="quick-document-lookup"></a>Hurtigt dokumentopslag
[!INCLUDE[d365fin](includes/d365fin_md.md)]-tilføjelsesprogrammet Document Links giver dig hurtig adgang til dokumenter, der nævnes i mails. Tilføjelsesprogrammet kan bruges i en mail, hvis der findes et gyldigt bilagsnummer i selve meddelelsen. Når tilføjelsesprogrammet åbnes, giver det hurtig adgang til dokumentet.  

F.eks. hvis du modtager en mail, hvor der i teksten står *S-QUO100*, identificerer [!INCLUDE[d365fin](includes/d365fin_md.md)] det som et salgstilbud, og så kan du åbne dette dokument i Outlook. I Outlook skal du vælge knappen **Document Links** umiddelbart oven over brødteksten i mailen. I Outlook-webappen skal du vælge teksten *S-QUO1001* i brødteksten i mailen.  

I tilføjelsesprogrammet Document Links kan du redigere og foretage handlinger i dokumentet, ligesom du kan i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="adding-the-add-ins-manually"></a>Tilføje tilføjelsesprogrammerne manuelt
I nogle tilfælde bliver tilføjelsesprogrammerne ikke føjet automatisk til Outlook. Selvom du eller en kollega har kørt den assisterede opsætningsvejledning på vegne af virksomheden, bliver [!INCLUDE[d365fin](includes/d365fin_md.md)] muligvis ikke vist i Outlook. Hvis du oplever dette problem, kan du tilføje [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilføjelsesprogrammer manuelt.  

Først skal du kontrollere, at du har adgang til tilføjelsesprogrammerne på din Office 365-konto. Åbn Outlook Web Access i en webbrowser, og føj derefter `/owa/#path=/options/manageapps` til URL-adresse på adresselinjen. Dermed åbnes siden **Administrere tilføjelsesprogrammer**, hvor du kan aktivere Financials til din Outlook. Derefter, når du går tilbage til Outlook, skulle [!INCLUDE[d365fin](includes/d365fin_md.md)] være tilgængeligt.  

På samme måde kan du i Outlook-skrivebordsklienten kontrollere, at [!INCLUDE[d365fin](includes/d365fin_md.md)] er angivet i vinduet **Administrer tilføjelsesprogrammer**.  

I begge tilfælde, hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] stadig ikke er tilgængelig, skal du hente manifest for tilføjelsesprogram-filerne. Du kan få flere oplysninger ved at kontakt Office 365-administratoren.

## <a name="see-also"></a>Se også
[Velkommen til [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  

