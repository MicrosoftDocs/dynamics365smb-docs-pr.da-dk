---
title: Arbejde med finansielle oversigter i Excel
description: 'Få mere at vide om, hvordan du kan åbne regnskabsopgørelser i Microsoft Excel fra Business Central for bedre analyse.'
author: edupont04
ms.topic: overview
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: 9027
ms.date: 08/23/2022
ms.author: edupont
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a><a name="analyzing-financial-statements-in-microsoft-excel"></a>Analysere regnskaber i Microsoft Excel

[!INCLUDE [prod_short](includes/prod_short.md)] indeholder KPI'er og modtager oversigter over din virksomheds økonomi. Her følger nogle eksempler på, hvordan du kan analysere KPI'er og oversigter i Excel:

* Åbn lister i Excel, og analyser dataene. 
* Eksporter tunge regnskabsopgørelser, f.eks. din balance eller resultatopgørelse, til Excel, analyser dataene, og udskriv rapporterne.  

> [!TIP]
> De rapporter, du kan få vist i Excel, er som standard udformet, så de er nemmere at analysere nuværende år. Resultatopgørelsesrapporten er dog en undtagelse. Med denne rapport kan du filtrere dataene, så de medtages i tidligere år i analyser.

## <a name="getting-the-overview-and-the-details-in-excel"></a><a name="getting-the-overview-and-the-details-in-excel"></a>Få oversigten og detaljerne i Excel

Du kan få adgang til disse to rapporter i Excel med handlingen **Rapporter** i rollecentrene Virksomhedsleder og Bogholder. Når du vælger et kontoudtog, åbnes det i Excel eller Excel Online. Et tilføjelsesprogram forbinder dataene til [!INCLUDE [prod_short](includes/prod_short.md)]. Du skal dog logge på med den samme konto, der bruges i forbindelse med [!INCLUDE [prod_short](includes/prod_short.md)]. Følgende tabel viser rapporterne, og hvor de er tilgængelige.  


|Rapport  |Rollecenter  |
|---------|---------|
|Statusopgørelse                 | Virksomhedsleder, Revisor |
|Resultatopgørelse              | Virksomhedsleder, Revisor |
|Opgørelser over pengestrøm       | Virksomhedsleder, Revisor |
|Opgørelse af overført resultat| Virksomhedsleder, Revisor |
|Opkrævet moms         | Virksomhedsleder, Revisor |
|Debitorkontoudtog           | Virksomhedsleder, Revisor |
|Aldersfordelt gæld         | Revisor |
|Aldersfordelt tilgodehavende      | Revisor |

Lad os antage, at du vil lære mere om din pengestrøm. Du kan åbne rapporten **Opgørelser over pengestrøm** i Excel, men det, der egentlig sker, er, at vi eksporterer de relevante data for dig og opretter en Excel-projektmappe, der er baseret på en foruddefineret skabelon fra Business Manager eller rollecenteret Regnskabsmedarbejder. Afhængigt af din webbrowser kan du blive bedt om at åbne eller gemme projektmappen.  

I Excel kan se du en fane, hvor dataene er opstillet for dig i det første regneark. De data, der blev eksporteret, findes også i andre regneark i de tilfælde, der er behov for. Du kan udskrive rapporten med det samme, eller du kan ændre den, indtil du har den oversigt og de oplysninger, du skal bruge. Brug tilføjelsesprogrammet [!INCLUDE [prod_short](includes/prod_short.md)] Excel til at filtrere og analysere data.  

### <a name="understanding-the-excel-templates"></a><a name="understanding-the-excel-templates"></a>Om Excel-skabeloner

De foruddefinerede Excel-rapporter er baseret på dataene i det aktuelle regnskab. Demoregnskabet har f.eks. oprettet kontoplanen, så du kan få vist tre kontantkonti under de *Aktuelle aktiver*: 10100 **Checkkonto**, 10200 **Opsparingskonto** og 10300 **Kontantbeholdning**. Felterne **Konto underkategori** er angivet til *Kontant*, og det samlede beløb, der vises som *Kontant* i Excel-rapporten **Balance**.  

Andre ark i Excel-projektmappen viser dataene bag rapporten. Hvis du vil se, hvad der er bag grupperne i Excel-rapporterne, skal du muligvis filtrere listerne i [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="the--excel-add-in"></a><a name="the--excel-add-in"></a>Tilføjelsesprogrammet [!INCLUDE [prod_short](includes/prod_short.md)]-Excel

Din [!INCLUDE [prod_short](includes/prod_short.md)]-oplevelse indeholder et tilføjelsesprogram til Excel. Afhængigt af dit abonnement er du logget på automatisk, eller du skal angive de samme login-oplysninger til [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Vise og redigere i Excel fra Business Central](across-work-with-excel.md).  

Med tilføjelsesprogrammet kan du få nye data fra [!INCLUDE [prod_short](includes/prod_short.md)], og du kan overføre ændringerne tilbage i [!INCLUDE [prod_short](includes/prod_short.md)]. Men muligheden for at sende data tilbage til databasen er ikke tilgængelig for de regnskabsrapporter, du kan se i Excel.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Visning og redigering i Excel fra Business Central](across-work-with-excel.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
