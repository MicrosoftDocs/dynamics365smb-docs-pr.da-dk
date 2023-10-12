---
title: 'Grundlæggende rapporter og dokumenter output, hurtig start'
description: 'Business Central tilbyder indbyggede skabeloner til rapporter og dokumenter, hvor det er nødvendigt med mange muligheder for at tilpasse dem til virksomhedens behov.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: null
ms.date: 08/15/2022
ms.author: bholtorf
---

# Grundlæggende rapporter og dokumenter output, hurtig start

Til at tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] til dine virksomhedsbehov, angive og anvende rapporter og tilpassede dokumenter, som passer til virksomhedens processer og visuelle identitet.

## Tilføj firmalogo til dokumenter

[!INCLUDE[prod_short](includes/prod_short.md)] har skabeloner indstillet til at bruge dit firmalogo til at spare dig tid på at tilpasse dokumenter, f. eks. fakturaer, ordrer og kontoudtog.

1. Vælg ![ikonet Tandhjul for at åbne menuen Indstillinger.](media/ui-experience/settings_icon_small.png) menuen, og vælg derefter **Virksomhedsoplysninger**.
2. Vælg handlingen **Billede**, og vælg derefter **Vælg**.
3. Vælg billedfilen på enheden.

Du kan se ovenstående instruktioner i [denne YouTube-video](https://www.youtube.com/watch?v=AatXbKF1NGg). Når billedet vises i feltet **billede**, kan du lukke siden **firmaoplysninger**.

## Køre rapporter

Rapporter organisering af oplysninger fra forskellige kilder i [!INCLUDE[prod_short](includes/prod_short.md)] og vis dem på en læsbar måde, der nemt kan udskrives eller deles digitalt. Rapporter kan findes på de sider, som er tilknyttet en kontekst. F. eks. viser siden **varer** rapporter vedrørende lagerniveauer, køb, salg m.m.

1. Åbn den side, der er knyttet til den ønskede rapport, f.eks. siden **varer**.
2. Vælg rapporten **Lager - top 10 liste** i menuen **rapporter**.
3. På rapport anmodningssiden skal du indstille filtre for at begrænse datoområdet eller ændre den anvendte referenceenhed i rapporten.
4. Vælg handlingen **Udskriv**, og følg enhedens udskrivningstrin.
    1. Du kan også vælge **Forhåndsversion** for at få vist rapporten på skærmen.

Få mere at vide om filtrering af data, planlægning af rapporter og meget mere, på [Kør og udskriv rapporter](ui-work-report.md).

## Gem rapporter som PDF, Excel eller Word-dokumenter

Hvis du hurtigt vil dele rapporter, kan du gemme [!INCLUDE[prod_short](includes/prod_short.md)]-rapporter direkte til PDF, Microsoft Excel eller Microsoft Word-dokumenter.

1. Gentag trin 1 til 3 fra afsnittet [Kør rapporter](#run-reports) ovenfor.
2. Vælg handlingen **Send til**.
3. Vælg filen, og vælg derefter **OK**.
r Den genererede skabelonfil gemmes automatisk i webbrowserens overførselsmappe.

### Ændre rapport- og dokumentlayout

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder mange indbyggede layouts til rapporter og andre genererede dokumenter, f. eks. salgsfakturaer. Du kan bruge programmer som Microsoft Word eller Excel til at redigere layoutskabeloner til dokumenter og rapporter som beskrevet i følgende eksempel:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Rapportlayout**, og vælg derefter det relaterede link.
2. På siden **rapportlayout** skal du vælge knappen **Søg** for at vælge layoutet *StandardSalesInvoice.docx* og derefter vælge handlingen **Eksporter layout** for at hente layoutskabelonfilen.

    Et Word-dokument gemmes på din enhed med det samme filnavn vist på siden **Rapportlayout**.
3. Åbn layoutfilen i Microsoft Word, og rediger dokumentet, f. eks. ved at flytte feltet dato ( *DocumentDate*) eller dit logo eller ved at ændre skriftstørrelsen, og derefter gemme filen.
4. Tilbage til **Rapportlayouts** vælge handlingen **Nyt layout**.
5. Angiv et navn og en beskrivelse til felterne **layoutnavn** og **Beskrivelse** på siden **Tilføj nyt layout** for at gøre det nemt at finde layoutet.
6. Vælg indstillingen **Word** i feltet **formatindstillinger**, og klik derefter på **OK**.
7. På siden **Vælg Word-layout** skal du vælge **Vælg** for at åbne filen med de redigerede layout på enheden.
8. Test det nye layout ved at vælge **Kør rapport**-handlingen.

Få mere at vide om, hvordan du tilpasser rapporter og dokumenter til dine forretningsbehov i [rapport-og dokumentlayout](ui-manage-report-layouts.md).

## Se også

[Bruge rapporter i dagligt arbejde](reports-use-reports.md)  
[Tilgængelige rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Valg af Dokumentrapport](across-report-selections.md)  
[Hurtig start af Business Central](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
