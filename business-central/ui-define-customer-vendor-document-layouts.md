---
title: Tildele dokumentlayouts til debitorer eller kreditorer
description: 'Brug dokumentlayout til at kontrollere udseende og format på dokumenter, f. eks. fakturaer og ordrer, som du sender til debitorer og kreditorer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '21, 9650'
ms.date: 07/05/2024
ms.service: dynamics-365-business-central
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Angive dokumentlayouts for debitorer og kreditorer

Dokumentlayout bruger rapportlayout til at definere udseende og funktionalitet for dokumenter, som du sender til kunder og leverandører. Business central indeholder standardlayout, men du kan også skræddersy tilpassede layout til de enkelte samarbejdspartnere. Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md). Du kan vælge standard-og brugerdefinerede dokumentlayout fra debitor-og kreditorkort ved at vælge handlingen **Dokumentlayout**. Værdien i feltet **Forbrug** definerer den proces, som dokumentlayoutet anvendes til. Du kan f. eks. bruge typerne **Rykker**, **Levering** og **Bekræftelse** til dokumentlayout.

Du kan også bruge dokumentlayout til at spare tid, når du sender dokumenter til debitor-eller kreditorkontakt personer pr. e-mail. Du kan angive en eller flere kontakt-e-mailadresser for hvert layout, som du tildeler debitoren eller kontaktpersonen. Du kan f. eks. sende en faktura til kundens købs-og lager kontakter. Det er nemt at tilføje e-mail-adresser.  **På siden** Dokumentlayout **giver handlingen Vælg e-mail fra kontakter** dig mulighed for at vælge fra en liste over de kontaktmailadresser, du har registreret for kunden eller kreditoren. Du kan også tilføje e-mailadresser manuelt. Hvis du angiver flere adresser, skal du adskille dem med et semikolon og ikke tilføje mellemrum mellem adresserne.

Før du kan definere, hvilket dokumentlayout, der skal bruges til hvilke processer, og hvilken kontaktperson, du vil sende dokumentet til, skal du indlæse alle de tilgængelige rapporter (dokumenter) fra siden **Rapportvalg**. Du kan hurtigt indlæse dokumenterne ved hjælp af handlingen **Kopier fra Rapportvalg** på siden **Dokumentlayout**.

I det følgende beskrives det, hvordan du definerer layouts for salgsdokumenter fra et **debitorkort**. Fremgangsmåden er den samme for layouts for købsdokumenter fra et **leverandørkort**.

## <a name="to-load-the-standard-document-layouts-for-sales-documents-for-a-customer"></a>Sådan indlæses standarddokument layout for salgsdokumenter for en debitor

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Åbn siden **Debitorkort** for debitoren, og vælg derefter handlingen **Dokumentlayout**.
3. På siden **Dokumentlayouts** skal du vælge handlingen **Kopier fra rapportvalg**.

På siden **Dokumentlayout** vises alle de tilgængelige layout for salgsdokumenter. 

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Sådan vælges et brugerdefineret rapportlayout, der skal bruges til layoutet for salgsdokumentet

I følgende trin antages det, at du allerede har et brugerdefineret rapportlayout til dokumenttypen. Hvis du ikke allerede har et tilpasset rapportlayout, skal du først oprette et. Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Åbn siden **Debitorkort** for debitoren, og vælg derefter handlingen **Dokumentlayout**.
3. På siden **Dokumentlayouts** skal du på linjen for det rapportlayout, som du ønsker, skal bruge et brugerdefineret layout, vælge feltet **Beskrivelse af brugerdefineret layout**.

   > [!TIP]
   > Feltet Beskrivelse af brugerdefineret layout er som standard skjult. Hvis feltet ikke er tilgængeligt, kan du tilpasse siden for at tilføje det. Hvis du vil tilpasse siden, skal du vælge :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="ikonet Indstillinger."::: , og vælg **derefter Tilpas**. Du kan få mere at vide om tilpasning af sider ved at gå til [Tilpasse dit arbejdsområde](ui-personalization-user.md).

1. På siden **Brugerdefinerede rapportlayouts** skal du vælge det specielle dokumentlayout, som du vil bruge til den pågældende salgsdokumenttype. Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md).

## <a name="to-specify-which-contact-receives-which-document-layout-for-a-customer"></a>Sådan angives det, hvilken kontakt der skal have hvilket dokumentlayout for en kunde

Hvis du vil spare tid, når du sender dokumenter til kunde-og leverandør kontaktpersoner via e-mail, skal du angive deres e-mail-adresser på dokumentlayout. F.eks. kan du altid sende et kontoudtog til revisionskontakter og salgsordrer til din kundes indkøbere og købsordrer til leverandørernes sælgere.

1. På siden **Dokumentlayouts** skal du på linjen for et rapportlayout, som du vil sende til en bestemt kontaktperson, vælge handlingen **Vælg e-mail fra kontaktpersoner**.
2. Vælg en eller flere kontakter på siden **kontaktpersoner**, og vælg derefter **OK**.

## <a name="see-also"></a>Se også

[Opdater brugerdefinerede rapportlayouts](ui-update-report-layouts.md)  
[Sådan opretter og ændrer du Brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md)  
[Importere og eksportere et brugerdefineret rapport- eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
