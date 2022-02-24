---
title: Tildel det specielle dokumentlayout til debitorer eller leverandører | Microsoft Docs
description: Når der er defineret brugerdefinerede rapportlayout, kan du vælge dem fra debitor- og leverandørkortene for at angive, at det valgte layout skal bruges til de dokumenter, som du har oprettet for den pågældende debitor eller leverandør.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 11/15/2019
ms.author: sgroespe
ms.openlocfilehash: 23c4573c3121a660b8263c3bc9bb2c6ac8b1d331
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/15/2019
ms.locfileid: "2809395"
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Angiv dokumentlayout for debitorer og leverandører
Når der er defineret brugerdefinerede rapportlayout, kan du vælge dem fra debitor- og leverandørkortene for at angive, hvilke layout der skal bruges til de forskellige typer dokumenter, som du har oprettet for den pågældende debitor eller leverandør. Værdien i feltet **Forbrug** angiver, hvilken proces, dokumentlayoutet skal bruges til, f.eks. **Rykker**, **Forsendelse** og **Bekræftelse**.

Ud over at konfigurere, hvilket layout der skal bruges til hvilket dokument, kan du spare tid, når du sender dokumenter til forskellige debitor- eller leverandørkontakter, ved at konfigurere, hvilket specifikke kontaktpersoners e-mail-adresser, der skal bruges i forbindelse med bestemte dokumenter. F.eks. vil der blive sendt kontoudtog til revisionskontakter, salgsordrer til din kundes indkøbere og købsordrer til leverandørernes sælgere eller account managers.

Når du opretter et dokumentlayout for en debitor eller leverandør, kan du også angive e-mail-adressen på den kontaktperson, der skal modtage dokumentet. Du kan hurtigt gøre dette med funktionen **Vælg e-mail fra kontaktperson**, hvilket automatisk angiver et filter for de kontakt-e-mail-adresser, der er registreret for den pågældende kunde eller leverandør.

Før du kan definere, hvilket dokumentlayout, der skal bruges til hvilke processer, og hvilken kontaktperson, du vil sende dokumentet til, skal du indlæse alle de tilgængelige rapporter (dokumenter) fra siden **Rapportvalg**. Du kan hurtigt gøre dette med funktionen **Kopier fra Rapportvalg**.

I det følgende beskrives det, hvordan du definerer layouts for salgsdokumenter fra et debitorkort. Fremgangsmåden er den samme for layouts for købsdokumenter fra et leverandørkort.

## <a name="to-enable-all-available-sales-documents-for-a-customer"></a>Sådan aktiveres alle tilgængelige salgsdokumenter for en debitor
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn kortet for den debitor, som du vil definere dokumentlayout for pr. forretningsproces.
3. På siden **Debitorkort** skal du vælge siden **Dokumentlayouts**.
4. På siden **Dokumentlayouts** skal du vælge handlingen **Kopier fra rapportvalg**.

Siden **Dokumentlayouts** for den pågældende debitor er udfyldt med alle rapportlayouts for salg, der findes i systemet. Du kan finde flere oplysninger om, hvordan de blev oprettet, se [Opret og ændr brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md).

Du kan nu fortsætte med at tilpasse listen med brugerdefinerede rapportlayouts eller e-mail-adresser på de kontaktpersoner, som dokumenterne skal sendes til.

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Sådan vælges et brugerdefineret rapportlayout, der skal bruges til layoutet for salgsdokumentet
Hvis et eller flere af de rapportlayouts, der er defineret på siden **Dokumentlayouts** for debitoren, ikke har et brugerdefineret rapportlayout defineret, kan du hurtigt gøre det.

1. På siden **Dokumentlayouts** skal du på linjen for det rapportlayout, som du ønsker, skal bruge et brugerdefineret layout, vælge feltet **Beskrivelse af brugerdefineret layout**. Feltet er enten udfyldt, hvis der allerede er valgt debitorlayout, eller tomt.
2. På siden **Brugerdefinerede rapportlayouts** skal du vælge det specielle dokumentlayout, som du vil bruge til den pågældende salgsdokumenttype. Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md).

## <a name="to-set-up-which-contact-receives-which-document-layout-for-a-customer"></a>Sådan angives det, hvilken kontaktperson, der modtager et givent dokumentlayout for en debitor
Du kan spare tid, når du sender dokumenter til forskellige debitorer eller leverandørkontaktpersoner ved at angive e-mail-adresserne på de forskellige linjer på siden **Dokumentlayouts**. F.eks. kan der blive sendt et kontoudtog til revisionskontakter, salgsordrer til din kundes indkøbere og købsordrer til leverandørernes sælgere eller account managers.

1. På siden **Dokumentlayouts** skal du på linjen for et rapportlayout, som du vil sende til en bestemt kontaktperson, vælge handlingen **Vælg e-mail fra kontaktpersoner**.
2. På siden **Kontaktpersoner** skal du vælge linjen for den relevante kontaktperson og dernæst vælge knappen **OK**.

Kontaktpersonens e-mail-adresse indsættes nu på dokumentlayoutlinjen, så det pågældende salgsdokument såsom rykkere altid sendes til den pågældende kontaktperson i debitorens virksomhed.

## <a name="see-also"></a>Se også  
[Opdater brugerdefinerede rapportlayouts](ui-update-report-layouts.md)  
[Sådan opretter og ændrer du Brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md)  
[Importere og eksportere et brugerdefineret rapport- eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md)  
[Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md)  
