---
title: "Fremgangsmåde: Kontrollere SE/CVR-numre | Microsoft Docs"
description: "Du kan bruge en EU-webtjeneste til at kontrollere, om de momsregistreringsnumre, du angiver på debitor-, kreditor- eller kontaktkort, er gyldige."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a>Fremgangsmåde: Kontrollere SE/CVR-numre
Du kan bruge en EU-webtjeneste til at kontrollere, om de momsregistreringsnumre, du angiver på debitor-, kreditor- eller kontaktkort, er gyldige.  

 Når du ændrer værdien i feltet **SE/CVR-nr.** på et kort, hvor værdien i feltet **Lande-områdekode** er et EU-landområde, bliver det nye momsregistreringsnummer og dit bruger-id logført i vinduet **Log over SE/CVR-nr.**. Du kan kontrollere et CVR-nummer ved at vælge knappen **Bekræft SE/CVR-nr.** i vinduet **Log over SE/CVR-nr.**. Der oprettes en ny linje, hver gang du bruger kontrolfunktionen. Hvis nummeret kunne bekræftes, indeholder feltet **Status** værdien **Gyldig**. Hvis nummeret ikke kunne bekræftes, vil feltet **Status** indeholde **Ugyldig**, og du skal derefter ændre tallet i feltet **SE/CVR-nr.** på kortet og starte kontrolfunktionen igen.  

 URL-adressen for standard-webtjenesten er angivet i feltet **URL-adresse til validering af SE/CVR-nr.** i vinduet **Regnskabsopsætning**.  

 I tabellen **SE/CVR-nr.format** kan du for hvert land/område ændre de forskellige formater af CVR-nummer, som brugere har tilladelse til at skrive i feltet **SE/CVR-nr.**.  

> [!WARNING]  
>  Denne webtjeneste bruger HTTP-protokollen, hvilket betyder, at data, der overføres via tjenesten, ikke er krypteret.  

> [!NOTE]  
>  Du kan opleve nedetid for denne tjeneste, som Microsoft ikke er ansvarlig for, da tjenesten er en del af et bredt EU-netværk af nationale momsregistre.  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a>Sådan bekræftes et CVR-nummer fra et debitorkort  
Benyt følgende fremgangsmåde til at kontrollere momsregistreringsnummeret for en debitor. Trinene er de samme for en leverandør og en kontaktperson.   
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorer**, og vælg derefter det relaterede link.  

2.  Åbn et debitorkort, hvor du vil kontrollere momsregistreringsnummeret.  

    > [!NOTE]  
    >  Feltet **Lande/områdekode** på debitorkortet skal indeholde et EU-land/område.  
3.  Brug oversigtspanelet **Fakturering** til at vælge Specificer-knappen ud for feltet **SE/CVR-nr.**.  

    Vinduet **Log over SE/CVR-nr.** åbnes og viser én linje, hvor feltet **Status** indeholder **Ikke bekræftet**.  
4.  Vælg handlingen **Bekræft SE/CVR-nr.**.  

     Der oprettes en ny linje, hvor feltet **Status** indeholder enten **Gyldig** eller **Ugyldig**.  
5.  Hvis feltet **Status** indeholder **Ugyldig**, skal du ændre nummeret i feltet **SE/CVR-nr.** på kortet og derefter gentage trin 3 og 4.  

## <a name="see-also"></a>Se også  
[Finans](finance.md)  
[Fremgangsmåde: Registrere nye debitorer](sales-how-register-new-customers.md)  
[Fremgangsmåde: Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

