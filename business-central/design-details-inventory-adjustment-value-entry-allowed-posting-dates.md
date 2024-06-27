---
title: Fejlmeddelelse "Bogføringsdatoen er ikke inden for intervallet af tilladte bogføringsdatoer"
description: 'Ret fejlen bag meddelelsen "bogføringsdatoen ligger ikke inden for den tilladte bogføringsdato", når kørslen Reguler kostværdi-vareposter køres.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---

# <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Fejlmeddelelse: "Bogføringsdatoen er ikke inden for intervallet af tilladte bogføringsdatoer..."

Når du bruger kørslen **Reguler kostværdi - vareposter**, kan du starte med følgende fejlmeddelelse:

**Bogføringsdato er ikke inden for den tilladte bogføringsperiode**

Denne meddelelse angiver, at du ikke har tilladelse til at bogføre poster for den dato, du indtastede. Du kan omgå dette problem ved at ændre din brugeropsætning.

## <a name="change-the-user-setup"></a>Ændre Brugeropsætning

|Bruger-id  |Bogføring tilladt fra  | Bogføring tilladt til  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

I dette tilfælde har du tilladelse til at bogføre i datointervallet fra 11. sept. til 30. sept. Du kan dog ikke bogføre posten med en bogføringsdato d. 10. sept.  

### <a name="overview-of-the-posting-date-setup"></a>Oversigt over opsætning af bogføringsdatoen

#### <a name="inventory-periods"></a>Lagerperioder

|Afslutningsdato  |Navn  |Lukket  |
|---------|---------|---------|
|2020-01-31     |2020. januar      |  Ja    |
|2020-02-28     |Februar 2020     |  Ja    |
|2020-03-31     |Marts 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Maj 2020        |  Ja    |
|2020-06-30     |Juni 2020       |  Ja    |
|2020-07-31     |Juli 2020        |   Ja   |
|2020-08-31     |August 2020     |   Ja   |
|2020-09-30     |September 2020  |         |
|2020-10-31     |Oktober 2020    |         |
|2020-11-30     |November 2020   |         |
|2020-12-31     |December 2020   |         |  

#### <a name="general-ledger-setup"></a>Opsætning af Finans

|Felt|Værdi|
|---------|---------|
|Bogf. tilladt fra:  |  2020-09-10      |
|Bogf. tilladt til:    |  2020-09-30      |
|Registrer tid:       |         |
|Lokalt adresseformat:|   Postnr.      |  

#### <a name="user-setup"></a>Brugeropsætning

|Bruger-id  |Bogf. tilladt fra  | Bogføring tilladt til  |
|---------|---------|--------|
|BRUGERNAVN |  2020-09-10      |2020-09-30      |

Hvis der tilknyttet et større område, hvor du tillader bogføring på siderne **Lagerperiode** eller **Opsætning af Finans** kan du undgå den konflikt, der forårsager fejlmeddelelsen. Det bredere interval giver dig f.eks. mulighed for at bogføre posten med reguleringsværdien med bogføringsdatoen d. 10. sept.
  
## <a name="see-also"></a>Se også

[Designoplysninger: Bogføringsdato på post med reguleringsværdi](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  
[Designoplysninger: Vareudligning](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
