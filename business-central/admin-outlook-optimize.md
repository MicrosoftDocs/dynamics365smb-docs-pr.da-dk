---
title: Optimere Outlook til Business Central-indbakke
description: 'Få mere at vide om, hvad du kan gøre for at forbedre oplevelsen med Business-indbakken i Microsoft Outlook.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in'
ms.date: 12/06/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Optimere Outlook til Business Central-indbakke 

Denne artikel beskriver, hvad du kan gøre for at få den bedst mulige oplevelse med Business-indbakken i Microsoft Outlook. 

## Opdatere Outlook

Opdater til Outlook version 2012 eller nyere.

> [!NOTE]
> Hvis du ikke kan opdatere Outlook til version 2012 eller nyere, skal du kontrollere, at du mindst opdaterer til version 1905. Dette forhindrer Outlook-tilføjelsesprogrammet i at køre med ældre Internet Explorer-komponenter

### Sådan kontrolleres din version af Outlook

Uanset om du bruger Office 2019 eller Microsoft 365, skal du følge denne Microsoft Support vejledning for at kontrollere, hvilken version af Outlook du har:  

[Om Office: Hvilken version af Office, bruger jeg?](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### Sådan opdateres Outlook

Hvis du vil opdatere Outlook til den seneste version, skal du følge denne Microsoft Support vejledning eller kontakte administratoren:

[Installere Office-opdateringer](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## Installer Microsoft Edge WebView2

Kontroller, at Microsoft Edge WebView2 er installeret på din enhed.

### Sådan kontrollerer du, om Microsoft Edge WebView2 er installeret 

Hvis du vil kontrollere, om du har Microsoft Edge WebView2 installeret på en computer, skal du benytte følgende fremgangsmåde:

Fra menuen Start:

1. Vælg **Start** ![Windows Start.](media/windows-start-icon.png "Ikonet Windows Start") > **Indstillinger** ![Windows-indstillinger](media/windows-settings-icon.png "Windows-ikonet indstillinger") > **Apps og funktioner**.
2. Skriv **WebView2** i søgefeltet. Hvis Microsoft Edge WebView2 er installeret, kan du se en post med navnet **Microsoft Edge WebView2 Runtime**.

Fra kontrolpanel:

1. I søgefeltet ved siden af **Start** ![Windows Start](media/windows-start-icon.png "Ikonet Windows Start"), skal du skrive **Kontrolpanel** og vælg derefter resultatet.
2. Vælg **Programmer** > **Programmer og funktioner**.
3. Skriv **WebView2** i søgefeltet. Hvis Microsoft Edge WebView2 er installeret, kan du se en post med navnet **Microsoft Edge WebView2 Runtime**.

### Sådan installeres Microsoft Edge WebView2 

1. Brug browseren til at gå til [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).
2. Vælg **Hent**.
3. Indstil den **Valgte arkitektur**, så den passer til systemet.
4. Vælg **Hent**.

> [!NOTE]
> Organisationen kan have begrænsninger for, hvilke komponenter der kan installeres på din enhed. Kontakt din administrator for at få hjælp.

## Brug en understøttet browser

Overvej at bruge Outlook til World Wide Web i en af de browsere, der understøttes af Business central. Du kan finde en liste over understøttede browsere under [Minimum krav til brug af Business Central](product-requirements.md#browsers).

## Se også

[Blive køreklar til at foretage handler](ui-get-ready-business.md)  
[Få Business Central på min mobilenhed](install-mobile-app.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Minimumkrav til Outlook](product-requirements.md#outlook)  
[Brug tilføjelsesprogrammer i Outlook på internettet](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]