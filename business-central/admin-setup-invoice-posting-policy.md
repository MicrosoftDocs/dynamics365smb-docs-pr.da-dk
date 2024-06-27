---
title: Definere politik til bogføring af faktura for brugere
description: 'Brug fakturabogføringspolitikkerne til at styre, om en bruger kan bogføre salgs- og købsfakturaer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/12/2024
ms.custom: bap-template
ms.search.forms: '119, 9807,'
ms.service: dynamics-365-business-central
---

# <a name="define-an-invoice-posting-policy-for-users"></a>Definere en fakturabogføringsmetode for brugere

Virksomheder har ofte forskellige processer til bogføring af salgs- og købsfakturaer og leverancer. Processer kan f. eks. variere fra én person, der bogfører alt på en købsordre, til flere medarbejdere. Du kan begrænse brugere i at bogføre fakturaer eller kræve, at fakturaerne bogføres sammen med leverancer eller modtagelser.

## <a name="to-specify-a-posting-policy"></a>Sådan angives bogføringspolitik

På siden **Brugeropsætning** i felterne **Bogføringsmetode til salgsfaktura** og **Politik til bogføring af købsfaktura** skal du vælge en af følgende indstillinger:

* **Tilladt** (standard) – Bevar den aktuelle funktionsmåde, hvor en bruger kan vælge den bogføringsindstilling, der skal bruges, f.eks. **Lever**, **Fakturer** og **Lever og Fakturer**. 
* **Forbudt** -forhindrer, at brugeren bogfører fakturaer. [!INCLUDE [prod_short](includes/prod_short.md)] viser en bekræftelsesdialogboks, der kun indeholder indstillingen **Lever** og **Modtag**.
* **Obligatorisk** - Tillad, at brugeren bogfører fakturaer sammen med modtagelser eller leverancer. [!INCLUDE [prod_short](includes/prod_short.md)] viser en bekræftelsesdialogboks, der kun viser indstillingerne **Lever og Fakturer** eller **Modtag og Fakturer**.

## <a name="effect-on-documents"></a>Indvirkning på dokumenter

Følgende tabel beskriver, hvordan fakturabogføringspolitikker påvirker dokumenter.

> [!NOTE]
> Når du bogfører salgs- og købsfakturaer og kreditnotaer, har du ingen bogføringsmuligheder. Dokumenterne bogfører altid de fysiske og økonomiske transaktioner samlet. Du kan ikke bogføre fakturaer og kreditnotaer delvist.

|Dokument | Mulighed 1: Tillade <br>Viser en række muligheder| Mulighed 2: Forbudt <br>Bekræftelsesdialogboks | Mulighed 3: Tvungen <br>Bekræftelsesdialogboks|
|--|--|--|--|
|Salgsordre |- Lever <br>- Fakturer <br>- Lever og fakturer |Vil du bogføre leveringen? |Skal forsendelsen bogføres og faktureres?|
|Salgsfaktura|Ingen indstillinger| Bogføring er forbudt pr. brugeropsætning|Vil du bogføre fakturaen?|
|Salgskreditnota|Ingen indstillinger|Bogføring er forbudt pr. brugeropsætning|Vil du bogføre kreditnotaen?|
|Salgsreturvareordre |- Modtag <br>- Fakturer <br>- Modtag og fakturer |Skal modtagelsen bogføres? |Vil du bogføre kvitteringen og fakturaen?|
|Lagerpluk |- Lever <br>- Lever og fakturer |Vil du bogføre leveringen? |Skal forsendelsen bogføres og faktureres?|
|Købsordre |- Modtag <br>- Fakturer <br>- Modtag og fakturer |Skal modtagelsen bogføres? |Vil du bogføre kvitteringen og fakturaen?|
|Købsfaktura|Ingen indstillinger|Bogføring er forbudt pr. brugeropsætning|Vil du bogføre fakturaen?|
|Købskreditnota|Ingen indstillinger|Bogføring er forbudt pr. brugeropsætning|Vil du bogføre kreditnotaen?|
|Købsreturordre |- Lever <br>- Fakturer <br>- Lever og fakturer |Vil du bogføre leveringen? |Skal forsendelsen bogføres og faktureres?|
|Læg-på-lager |- Modtag <br>- Modtag og fakturer |Skal modtagelsen bogføres? |Vil du bogføre kvitteringen og fakturaen?|
|Lagerleverance |- Lever <br>- Lever og fakturer | Vil du bogføre leveringen? |Skal forsendelsen bogføres og faktureres?|

   > [!Note]
   > Indstillingen påvirker ikke bogføring af finanskladdelinjer, hvor du kan vælge **faktura** i feltet **Bilagstype**.

## <a name="see-also"></a>Se også

[Fakturere salg](sales-how-invoice-sales.md)  
[Registrere køb med købsfakturaer og ordrer](purchasing-how-record-purchases.md)  
[Købe varer til et salg ved at oprette købsfakturaer](purchasing-how-purchase-products-sale.md)
[klargøre virksomheden](ui-get-ready-business.md)  
