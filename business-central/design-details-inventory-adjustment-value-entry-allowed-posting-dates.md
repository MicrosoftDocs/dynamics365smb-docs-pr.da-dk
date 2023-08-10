---
title: Fejlmeddelelse "Bogføringsdatoen er ikke inden for intervallet af tilladte bogføringsdatoer"
description: 'Ret fejlen bag meddelelsen "bogføringsdatoen ligger ikke inden for den tilladte bogføringsdato", når kørslen Reguler kostværdi-vareposter køres.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---

# <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Fejlmeddelelse: "Bogføringsdatoen er ikke inden for intervallet af tilladte bogføringsdatoer..."

Når du bruger kørslen **Reguler kostværdi - vareposter**, kan du starte med følgende fejlmeddelelse:

**Bogføringsdato er ikke inden for den tilladte bogføringsperiode**

Denne fejlmeddelelse angiver, at brugeren ikke har tilladelse til at bogføre poster for den pågældende dato, og at det kan afhjælpes ved at ændre brugeropsætningen.

## <a name="change-the-user-setup"></a>Ændre Brugeropsætning

|Bruger-id  |Bogf. tilladt fra  | Bogf. tilladt til  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

Brugeren har i dette tilfælde et tilladt bogføringsdatointerval fra 11. september til 30. september og må derfor ikke bogføre reguleringsværdiposten med bogføringsdatoen 10. september.  

### <a name="overview-of-involved-posting-date-setup"></a>Oversigt over opsætning af den involverede bogføringsdato

#### <a name="inventory-periods"></a>Lagerperioder

|Afslutningsdato  |Name  |Lukket  |
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

|Bruger-id  |Bogf. tilladt fra  | Bogf. tilladt til  |
|---------|---------|--------|
|BRUGERNAVN |  2020-09-10      |2020-09-30      |

Hvis der tilknyttet et større tilladt bogføringsdatointerval som i lagerperiode eller Finans, bliver det muligt at undgå den konflikt, der forårsager fejlmeddelelsen. Reguleringen af værdiposten med bogføringsdatoen 10. september bogføres automatisk med denne opsætning.
  
## <a name="see-also"></a>Se også

[Designoplysninger: Bogføringsdato på post med reguleringsværdi](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  
[Designoplysninger: Vareudligning](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
