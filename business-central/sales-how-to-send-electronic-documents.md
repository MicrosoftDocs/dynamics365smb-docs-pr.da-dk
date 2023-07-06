---
title: Sende elektroniske dokumenter
description: 'Få mere at vide om, hvordan du bruger Business central til at sende elektroniske fakturaer og kreditnotaer i PEPPOL.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="send-electronic-documents"></a><a name="send-electronic-documents"></a><a name="send-electronic-documents"></a>Sende elektroniske dokumenter

Den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter afsendelse af elektroniske fakturaer og kreditnotaer i PEPPOL-formatet, som understøttes af de største udbydere af dokumentudvekslingstjenester. En udbyder af dokumentudvekslingstjenester sender elektroniske dokumenter mellem handelspartnere. For at understøtte andre elektroniske dokumentformater kan du bruge dataudvekslingsstrukturen.  

 I den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)] er en dokumentudvekslingstjeneste forudkonfigureret og klar til at blive konfigureret til din virksomhed. Du kan finde flere oplysninger i [Konfigurere en dokumentudvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md). Du skal imidlertid installere en app i nogle tilfælde. Du kan finde flere oplysninger i [Ofte stillede spørgsmål til Oversigt over elektronisk fakturering](faq-electronic-invoicing.yml).  

 Når du vil sende en salgsfaktura som et elektronisk PEPPOL dokument, skal du vælge indstillingen **Elektronisk dokument** i dialogboksen **Bogfør og send**. Herfra kan du også angive debitorens standardprofil for afsendelse af dokumenter. Først skal du konfigurere forskellige stamdata, såsom firmaoplysninger, debitorer, varer og enheder. Disse bruges til at identificere forretningspartnere og varer ved konvertering af data i felterne i [Konfigurere afsendelse og modtagelse af elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a><a name="to-send-an-electronic-sales-invoice"></a><a name="to-send-an-electronic-sales-invoice"></a>Sådan sendes en elektronisk salgsfaktura

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.  

2. Opret en ny salgsfaktura.  

3. Når salgsfakturaerne er klar til at blive faktureret, skal du vælge handlingen **Bogfør og send**.  

     Hvis debitorens standardprofil til afsendelse er **Elektronisk dokument**, vises det i dialogboksen **Bekræftelse af bogfør og send**. På den måde behøver du kun at vælge knappen **Ja** for at bogføre og sende fakturaen elektronisk i det valgte format.  

4. I dialogboksen **Bekræftelse af bogfør og send** skal du vælge knappen AssistEdit til højre for feltet **Send bilag til**.  

5. I **Send dokument til** dialogboksen og i feltet **Elektronisk dokument** skal du vælge **Via dokumentudvekslingstjeneste**.  

6. I feltet **Format** skal du vælge **PEPPOL**.  

7. Vælg knappen **OK**. Dialogboksen **Bekræftelse af bogfør og send** vises. **Elektronisk dokument (PEPPOL)** føjes til feltet **Send dokument til**.  

8. Vælg knappen **Ja**.  

     Salgsfakturaen bogføres og sendes til kunden som et elektronisk dokument i PEPPOL-format.  

    > [!NOTE]  
    >  Du kan også sende en bogført salgsfaktura som et elektronisk dokument. Fremgangsmåden er den samme som beskrevet i dette emne for ikke-bogførte salgsdokumenter. På siden **Bogført salgsfaktura** skal du vælge handlingen **Aktivitetslog** for at få vist statussen for det elektroniske dokument.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Fakturere salg](sales-how-invoice-sales.md)  
[Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md)  
[Konfigurere afsendelse og modtagelse af elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Konfigurere en dokumentudvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md)  
[Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)  
[Udveksle data elektronisk](across-data-exchange.md)  
[Ofte stillede spørgsmål om elektronisk fakturering](faq-electronic-invoicing.yml)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
