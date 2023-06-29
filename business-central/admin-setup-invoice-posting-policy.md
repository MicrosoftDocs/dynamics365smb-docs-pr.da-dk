---
title: Definere en faktura bogføringsmetode for brugere
description: 'Brug fakturabogføringspolitikkerne til at styre, om en bruger kan bogføre salgs- og købsfakturaer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.forms: '119, 9807,'
---

# <a name="define-an-invoice-posting-policy-for-users"></a><a name="define-an-invoice-posting-policy-for-users"></a>Definere en fakturabogføringsmetode for brugere

Virksomheder har ofte forskellige processer til bogføring af salgs- og købsfakturaer og leverancer. Processer kan f. eks. variere fra én person, der bogfører alt på en købsordre, til flere medarbejdere. Du kan begrænse brugere i at bogføre fakturaer eller kræve, at fakturaerne bogføres sammen med leverancer eller modtagelser.

## <a name="to-specify-a-posting-policy"></a><a name="to-specify-a-posting-policy"></a>Sådan angives bogføringspolitik

På siden **Brugeropsætning** i felterne **Bogføringsmetode til salgsfaktura** og **Politik til bogføring af købsfaktura** skal du vælge en af følgende indstillinger:

* **Tilladt** (standard) – Bevar den aktuelle funktionsmåde, hvor en bruger kan vælge den bogføringsindstilling, der skal bruges, f.eks. **Lever**, **Fakturer** og **Lever og Fakturer**. 
* **Forbudt** -forhindrer, at brugeren bogfører fakturaer. Business central viser en bekræftelsesdialogboks, der kun viser **Lever**- eller **Modtag**-indstillingerne.
* **Obligatorisk** - Tillad, at brugeren bogfører fakturaer sammen med modtagelser eller leverancer. Business central viser en bekræftelsesdialogboks, der kun viser **Lever og Fakturer** eller **Modtag og Fakturer**-indstillingerne.

## <a name="effect-on-documents"></a><a name="effect-on-documents"></a>Indvirkning på dokumenter

Følgende tabel beskriver, hvordan fakturabogføringspolitikker påvirker dokumenter.

|Bilag | Mulighed 1: Tillade <br>Viser en række muligheder| Mulighed 2: Forbudt <br>Bekræftelsesdialogboks | Mulighed 3: Tvungen <br>Bekræftelsesdialogboks|
|--|--|--|--|
|Salgsordre |- Lever <br>- Fakturer <br>- Lever og fakturer |Vil du bogføre leveringen? |Skal forsendelsen bogføres og faktureres?|
|Salgsreturordre |- Modtag <br>- Fakturer <br>- Modtag og fakturer |Skal modtagelsen bogføres? |Vil du bogføre kvitteringen og fakturaen?|
|Pluk |- Lever <br>- Lever og fakturer |Vil du bogføre leveringen? |Skal forsendelsen bogføres og faktureres?|
|Købsordre |- Modtag <br>- Fakturer <br>- Modtag og fakturer |Skal modtagelsen bogføres? |Vil du bogføre kvitteringen og fakturaen?|
|Købsreturvareordre |- Lever <br>- Fakturer <br>- Lever og fakturer |Vil du bogføre leveringen? |Skal forsendelsen bogføres og faktureres?|
|Læg-på-lager |- Modtag <br>- Modtag og fakturer |Skal modtagelsen bogføres? |Vil du bogføre kvitteringen og fakturaen?|
|Lagerleverance |- Lever <br>- Lever og fakturer | Vil du bogføre leveringen? |Skal forsendelsen bogføres og faktureres?|

   > [!Note]
   > Indstillingen påvirker ikke bogføring af finanskladdelinjer, hvor du kan vælge **faktura** i feltet **Bilagstype**.

## <a name="see-also"></a><a name="see-also"></a>Se også

[Fakturere salg](sales-how-invoice-sales.md)  
[Registrere køb med købsfakturaer og ordrer](purchasing-how-record-purchases.md)  
[Købe varer til et salg ved at oprette købsfakturaer](purchasing-how-purchase-products-sale.md)
[klargøre virksomheden](ui-get-ready-business.md)  
