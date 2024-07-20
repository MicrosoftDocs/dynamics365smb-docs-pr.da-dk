---
title: Opbevar transaktionsdata i fem år i Danmark
description: 'Denne artikel beskriver, hvordan du automatisk opbevarer data baseret på den danske bogføringslov.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 03/29/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="keep-transactional-data-for-five-years-in-denmark"></a>Opbevar transaktionsdata i fem år i Danmark

Med udgangspunkt i bogføringsloven skal Dynamics 365 Business Central, som digitalt standard bogføringssystem, understøtte opbevaring af virksomhedens registrerede transaktioner og kvitteringer, der er omfattet af §3, i fem år fra regnskabsårets udløb. Sammen med digitale bilag skal de bogførte transaktioner bevares, så de ikke kan ændres, tilbagedateres eller slettes af virksomheden eller en bruger. En softwareudbyder skal opbevare dem i et struktureret og maskinlæsbart format i den periode, uanset eventuelle ophør af kundeforhold til virksomheden, eller virksomhedens konkurs eller tvangsopløsning.

For at opfylde disse krav eksporterer Microsoft alle nødvendige transaktionsdata og de relaterede digitale bilag dagligt i den kontobeskyttede Azure Blob Storage. Efter at dataene og bilagene er bogført, kan de ikke ændres, tilbagedateres eller slettes af virksomheden. Disse data kan kun stilles til rådighed for danske myndigheder som svar på en officiel anmodning baseret på loven. Selv da er adgangen til disse data skrivebeskyttet.

Da systemet gemmer data dagligt, kan data, der ikke er lovpligtige (dvs. data, der er ældre end fem år fra udgangen af ​​det regnskabsår, som materialet vedrører) automatisk lokaliseres og fjernes, baseret på kravet om ikke opbevarer data længere end loven kræver. Microsoft vil ikke opbevare data i dette lager, før loven kræver det (det vil sige fra år 2024).

## <a name="mandatory-use-of-the-cvr-number"></a>Obligatorisk brug af CVR-nummer

Det Centrale Virksomhedsregister (CVR)-nummer skal udfyldes, før brugere bogfører til hovedbogen. Benyt følgende fremgangsmåde for at udfylde:

1. Vælg søgeknappen ![Forstørrelsesglas-knappen, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomhedsoplysninger**, og vælg derefter det relaterede link.
2. I feltet **Registreringsnr.** skal du indtaste CVR-nummeret for din virksomhed.
3. Luk siden.

> [!IMPORTANT]
> Når du har indtastet CVR-nummeret i **Registreringsnr.**-feltet på **Virksomhedsoplysninger**-siden, og Nemhandel API'er validerer nummer, du kan ikke ændre eller slette det.   

Du kan finde flere oplysninger i [Danmark Landespecifikke funktioner](denmark-local-functionality.md).

## <a name="see-also"></a>Se også

[Økonomistyring](../../finance.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
