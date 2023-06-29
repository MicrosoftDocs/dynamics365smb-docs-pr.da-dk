---
title: Sådan konfigureres en dokumentudvekslingstjeneste | Microsoft Docs
description: Du kan bruge en ekstern tjenesteudbyder til at udveksle elektroniske dokumenter med dine handelspartnere.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: edupont
---
# <a name="set-up-a-document-exchange-service"></a><a name="set-up-a-document-exchange-service"></a>Konfigurere en dokumentudvekslingstjeneste

Som en del af data Exchange-programmet kan du udveksle salgs-og købsdokumenter med samhandelspartnere uden ekstra trin, f. eks. vedhæfte dokumenter til e-mailmeddelelser som PDF-filer. Når du er klar til at fakturere en kunde, kan du f. eks. bogføre fakturaen og sende den til betaling som en fil, som kunden kan modtage i virksomhedens forretnings styringsprogram. Du kan finde flere oplysninger i [Udveksle data elektronisk](across-data-exchange.md).

> [!NOTE]
> Oprettelse af en dokumentudvekslingsservice for Business Central-lokalt kræver nogle yderligere trin til godkendelse. Du kan finde flere oplysninger i [Indstillinger til Business Central lokalt](#settings-for-business-central-on-premises).

## <a name="connecting-with-trading-partners"></a><a name="connecting-with-trading-partners"></a>Oprette forbindelse til handelspartnere

At udveksle elektroniske dokumenter kræver en forbindelse til samhandelspartnere. Hvis du vil gøre det nemmere at oprette en sikker forbindelse, er [!INCLUDE[prod_short](includes/prod_short.md)]-online konfigureret til at bruge appen Business central integration. Appen er tilgængelig på Tradeshift-app-lageret, og alle dig og dine forretningspartnere skal gøre sig for at oprette en Tradeshift-konto og derefter aktivere appen. Business central integration-appen leveres i produktions-og sandkasseversioner. Hvis du f. eks. bruger sandkasseversionen er god til at teste dokumentudvekslingen. Du kan skifte mellem produktions-og sandkasse versioner ved at slå **sandkasse** til/fra på siden **Opsætning af dok.udv.tjen.**. Når du gør det, opdateres oplysningerne i oversigtspanelet **Tjeneste** for dig.

Hvis du vil bruge en anden tjeneste, skal du angive oplysninger for at oprette forbindelsen. Du kan finde flere oplysninger i [Tilslutte til en dokumentudvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md#to-connect-to-a-document-exchange-service).

## <a name="to-connect-to-the-business-central-integration-app-on-tradeshift"></a><a name="to-connect-to-the-business-central-integration-app-on-tradeshift"></a>Sådan oprettes der forbindelse til appen Business central integration på Tradeshift

Du kan hurtigt oprette en Tradeshift-konto og komme i gang med appen Business central integration fra siden **Opsætning af dok.udv.tjen.**. Vælg enten linket **Aktiver app** i meddelelses- eller **app-URL-adresse** for at gå til appen i Tradeshift-app-lageret. På siden logon til Tradeshift skal du enten logge på eller logge på.

> [!NOTE]
> Når du har logget på din Tradeshift konto, kommer webstedet muligvis ikke til den side, hvor du aktiverede app'en. Hvis du vil gøre det, skal du klikke på linket på siden **Opsætning af dok.udv.tjen.** i Business central igen for at gå direkte til appen.

Hvis du ikke længere vil bruge appen Business central integration, skal du deaktivere den i Tradeshift app store. 

## <a name="to-connect-to-a-document-exchange-service"></a><a name="to-connect-to-a-document-exchange-service"></a>Tilslutte til en dokumentudvekslingstjeneste

Hvis du foretrækker at bruge en anden dokumentudvekslingstjeneste, skal du angive nogle oplysninger for at oprette forbindelse til tjenesten.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af Dokumentudvekslingstjeneste**, og vælg derefter det relaterede link.  
2. Udfyld felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivlse|  
    |---------------------------------|---------------------------------------|  
    |**Brugeragent**|Skriv en tekst, der kan bruges til at identificere din virksomhed i dokumentudvekslingsprocesser.|  
    |**Aktiveret**|Angiv, om forbindelsen til servicen er aktiveret.<br><br> **Bemærk:**  Når du har aktiveret tjenesten, oprettes der mindst to opgavekøposter til at sende og modtage elektroniske dokumenter. Når du deaktiverer tjenesten, slettes posterne i opgavekøen.|  
    |**Sandkasse**|Angiv, om du opretter forbindelse til en sandkasse version af dokumentudvekslingstjeneste.|
    |**URL-adresse til tilmelding**|Angiv den webside, hvor du tilmelder dig dokumentudvekslingstjenesten.|  
    |**App-URL**|Vælg dette link for at åbne app store, og slå appen Business Central-integration til og fra.|
    |**URL-adresse for tjeneste**|Angiv adressen på den dokumentudvekslingstjeneste, som bliver kaldt, når du sender og modtager elektroniske dokumenter.|  
    |**Log på URL**|Angiv URL for den webside, hvor du tilmelder dig dokumentudvekslingstjenesten. Det er denne side, hvor du angiver virksomhedens brugernavn og adgangskode.|  
    
    > [!NOTE]  
    > Logonoplysningerne krypteres automatisk. Du kan ikke deaktivere denne kryptering.

    > [!NOTE]
    > Hvis du ikke kan oprette forbindelse til dokument bytte tjenesten pga. et godkendelses problem, kan det skyldes, at [!INCLUDE[prod_short](includes/prod_short.md)] ikke automatisk kan forny adgangs-token. Dette kan f. eks. forekomme, hvis du ikke har brugt tjenesten i nogen tid. Du kan forny tokenet manuelt vha. handlingen **Forny token**.

## <a name="settings-for-business-central-on-premises"></a><a name="settings-for-business-central-on-premises"></a>Indstillinger for Business Central lokalt

Hvis du vil forbinde Business Central lokalt, skal du oprette en app på Tradeshift-app-lageret. Når du gør det, skal du bruge URL-adressen til omdirigering fra feltet **URL-adresse til omdirigering** på siden **Opsætning af Dokumentudvekslingstjeneste**. Når du har registreret din app, vil Tradeshift levere et klient-ID og en klienthemmelighed. I [!INCLUDE[prod_short](includes/prod_short.md)] skal du angive værdierne i oversigtspanelet **godkendelse** på siden **Opsætning af Dokumentudvekslingstjeneste**.

Hvis du foretrækker at gemme app-id'et og hemmeligheden et andet sted, kan du lade felterne Klient-id og Klienthemmelighed være tomme og skrive en udvidelse for at hente id'et og hemmeligheden fra placeringen. Du kan levere hemmeligheden på kørselstidspunktet ved at abonnere på hændelserne OnGetClientId og OnGetClientSecret i codeunit 1410 "Doc. Exch. Service Mgt."

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/electronic-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Konfigurere dataudveksling](across-set-up-data-exchange.md)  
[Udveksle data elektronisk](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
