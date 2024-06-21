---
title: Designoplysninger - Ikke-fradragsberettiget moms
description: 'Denne artikel indeholder oplysninger om moms uden fradragsberettiget moms, der skal betales af en indkøber, men som ikke er fradragsberettiget for køberens eget momsansvar.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/04/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="design-details-non-deductible-vat"></a>Designoplysninger: Ikke-fradragsberettiget moms

Moms uden fradragsberettiget moms er den moms, der skal betales af en indkøber, men som ikke er fradragsberettiget for køberens eget momsansvar. Da det kan være svært at vide, hvor og hvordan en vare anvendes, skal du kontakte de lokale skattemyndigheder i dit land eller område for at finde ud af, om en bestemt procent af momsen fradrages i forhold til historiske data. Selv når du ved, at en bestemt procentdel af momsen ikke er fradragsberettiget, er der forskellige modeller til håndtering af ikke-fradragsberettigede beløb, da de er relateret til **varer** og **anlægsaktiver**.

## <a name="prerequisites-for-using-non-deductible-vat"></a>Forudsætninger for brug af ikke-fradragsberettiget moms

Benyt følgende fremgangsmåde, hvis du vil bruge og bogføre ikke-fradragsberettiget moms.

1. Vælg **Aktiver ikke-fradragsberettiget moms** på siden **Momsopsætning** for at aktivere funktionen.
2. På siden **Momsbogføringsopsætning** skal du vælge, hvilke momsbogføringsgrupper der kan bruge ikke-fradragsberettiget moms.

## <a name="examples"></a>Eksempler

For følgende eksempler er ikke-fradragsberettiget moms aktiveret, og følgende opsætning er fuldført:

- Feltet **Momsproduktbogføringsgruppe** er angivet til **NDVAT**.
- På siden **Momsbogf.opsætning**:

    - **NDVAT** er angivet som momsproduktbogføringsgruppe, og **INDLAND** er angivet som momsvirksomhedsbogføringsgruppe.
    - Værdien i feltet **Moms-id** skal være entydig.
    - Feltet **Moms %** er sat til **25**.
    - Feltet **Tillad ikke-fradragsberettiget moms** er angivet til **Tillad**.
    - Feltet **Ikke-fradragsberettiget moms %** er angivet til **100**.
    - Feltet **Momsberegningstype** er angivet til **Normal moms**.
    - Kun salgsmomskontoen og købsmomskontoen er konfigureret.

I alle eksempler bruges der varer og anlægsaktiver, hvor momsproduktbogføringsgruppen er **NDVAT**.

### <a name="items"></a>Varer

En ny vare har **NDVAT** angivet som momsproduktbogføringsgruppe. På købsdokumentet, **Antal** = **1** og **Købspris Ekskl. moms** = **1.000,00**

Uanset hvilken indstilling der bruges, er resultatet af **momsposten** ens.

| Dokumenttype | Enhedstype | Basis | Beløb | Ikke-fradragsberettiget momsgrundlag | Ikke-fradragsberettiget momsbeløb |
|---|---|---|---|---|---|
| Fakturer | Køb | 0.00 | 0.00 | 1,000.00 | 250.00 |

Detaljerne vises i **værdiposterne**.

> [!NOTE]
> Du kan aktivere feltet **Brug til varekostpris** på siden **Momsopsætning**.

#### <a name="use-for-item-cost-isnt-enabled"></a>Brug til vare omkostning er ikke aktiveret

| Vareposttype | Postens type | Kostbeløb (faktisk) | Varepostmængde |
|---|---|---|---|
| Køb | Købspris | 1,000.00 | 1 |

#### <a name="use-for-item-cost-is-enabled"></a>Brug til vare omkostning er aktiveret

| Vareposttype | Postens type | Kostbeløb (faktisk) | Varepostmængde |
|---|---|---|---|
| Køb | Købspris | 1,250.00 | 1 |

### <a name="fixed-assets"></a>Anlægsaktiver

Et nyt anlægsaktiv har den anskaffelses konto, der er indstillet til at bruge **NDVAT** som momsproduktbogføringsgruppe. På købsdokumentet, **Antal** = **1** og **Købspris Ekskl. moms** = **1.000,00**

Uanset hvilken indstilling der bruges, er resultatet af **momsposten** ens.

| Dokumenttype | Enhedstype | Basis | Beløb | Ikke-fradragsberettiget momsgrundlag | Ikke-fradragsberettiget momsbeløb |
|---|---|---|---|---|---|
| Fakturer | Køb | 0.00 | 0.00 | 1,000.00 | 250.00 |

Detaljerne vises i **anlægsposterne**.

> [!NOTE]
> Du kan aktivere feltet **Brug til anlægsaktivomkostning** på siden **Momsopsætning**.

#### <a name="use-for-fixed-asset-cost-isnt-enabled"></a>Bruges til anlægsaktiv omkostninger er ikke aktiveret

| Dokumenttype | Anlægsbogføringstype | Beløb | Momsbeløb |
|---|---|---|---|
| Fakturer | Omkostning ved anskaffelse | 1,000.00 | 250.00 |

#### <a name="use-for-fixed-asset-cost-is-enabled"></a>Bruges til anlægsaktiv omkostninger er aktiveret

| Dokumenttype | Anlægsbogføringstype | Beløb | Momsbeløb |
|---|---|---|---|
| Fakturer | Omkostning ved anskaffelse | 1,000.00 | 250.00 |
| Fakturer | Omkostning ved anskaffelse | 250.00 | 0.00 |

## <a name="see-also"></a>Se også

[Opsætte ikke-fradragsberettiget moms](finance-setup-nondeductible-vat.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
