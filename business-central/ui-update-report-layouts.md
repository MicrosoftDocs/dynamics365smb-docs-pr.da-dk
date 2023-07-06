---
title: Opdater brugerdefinerede rapportlayouts
description: 'Få mere at vide om, hvordan du opdaterer et brugerdefineret rapportlayout, der er brugt i en rapport, når der f. eks. er ændringer i rapportens datasæt.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9652, 9650'
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="legacy-update-custom-report-layouts"></a><a name="legacy-update-custom-report-layouts"></a><a name="legacy-update-custom-report-layouts"></a>(Ældre) Opdater brugerdefinerede rapportlayouts

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Nogle gange skal du opdatere et brugerdefineret rapportlayout, der bruges i en rapport. Dette er påkrævet, når der er sket en designændring af rapportens datasæt, eksempelvis et felt, der bruges i layoutet, er blevet fjernet fra datasættet i rapporten. Hvis et rapportlayout kræver opdatering, får du en fejlmeddelelse, når du forsøger at se, udskrive eller gemme rapporten.  

Du kan automatisk opdatere et rapportlayout fra den fejlmeddelelse, der vises, når du kører rapporten, ved at vælge knappen **Ja** på fejlmeddelelsen. Eller før du kører rapporter, kan du opdatere specifikke rapportlayout eller alle tilpassede rapportlayout, der kunne blive påvirket af datasætændringer.  

Du har også mulighed for at kontrollere opdateringer uden at anvende de nødvendige ændringer på brugerdefinerede rapportlayout. Dette gør det muligt for dig at se, hvilke ændringer der anvendes på rapportlayoutet og identificere mulige problemer i processen. Fra resultaterne, kan du åbne de brugerdefinerede rapportlayout direkte til redigering for at løse problemer. Det anbefales at kontrollere kontrolrapportopdateringen, før du anvender opdateringerne.  

Ikke alle ændringer af rapportdatasæt kan opdateres automatisk i rapportlayout. Nogle ændringer kræver, at du manuelt redigere rapportlayout. Du kan finde flere oplysninger i [Begrænsninger for den brugerdefinerede rapport layoutopdatering](ui-update-report-layouts.md#UpdateLimitations).  

## <a name="to-update-one-or-more-custom-report-layouts"></a><a name="to-update-one-or-more-custom-report-layouts"></a><a name="to-update-one-or-more-custom-report-layouts"></a>Sådan opdaterer du ét eller flere brugerdefinerede rapportlayout

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Valg af rapportlayout**, og vælg derefter det relaterede link.  

2.  Hvis du vil opdatere en bestemt rapport, skal du på siden **Rapportlayoutvalg** vælge layoutet på listen og derefter vælge handlingen **Opdater layout**. Eller hvis du vil opdatere alle brugerdefinerede rapportlayout for virksomheden, skal du vælge handlingen **Opdater alle layout**.  

Hvis der ikke opstår fejl, anvendes opdateringerne på rapportlayout. Hvis der opstår fejl, vises en meddelelse, der indeholder de fejl, der er. Derefter skal du manuelt redigere brugerdefinerede rapportlayout for at rette fejlen. Du kan finde flere oplysninger i [Rettelse af fejl](ui-update-report-layouts.md#FixErrors).  

## <a name="to-test-custom-report-layout-updates"></a><a name="to-test-custom-report-layout-updates"></a><a name="to-test-custom-report-layout-updates"></a>Sådan kontrollerer du opdateringer til brugerdefinerede rapportlayout

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Valg af rapportlayout**, og vælg derefter det relaterede link.  

2.  På siden **Valg af rapportlayout** skal du vælge handlingen **Opdateringer af testlayout**.  

 Ændringer til de viste rapportlayout testes, men anvendes ikke på de faktiske rapportlayout. En **Log over rapportlayoutopdatering**-side åbnes og viser status for de mulig opdateringer til hver rapportlayout. Hvis der er fejl i et rapportlayout, kan du åbne rapportlayout direkte til redigering fra meddelelsen for at løse problemer. Du kan finde flere oplysninger i [Rettelse af fejl](ui-update-report-layouts.md#FixErrors).  

## <a name="limitations-of-the-custom-report-layout-update"></a><a name="limitations-of-the-custom-report-layout-update"></a><a name="limitations-of-the-custom-report-layout-update"></a><a name="UpdateLimitations"></a> Begrænsninger for den brugerdefinerede rapport layoutopdatering
 Der er flere typer ændringer, som den automatisk opdatering kan anvende på brugerdefinerede rapportlayout, f.eks. er et felt, der bruges i layoutet, fjernet fra rapportens datasæt. Men den automatisk opdatering kan ikke håndtere følgende ændringer af et rapportdatasæt.  

1.  Slettede felter, etiketter eller dataelementer.  

2.  Navn på dubletfelter i rapportlayout, når et felt er omdøbt i datasættet. Det skal behandles som en designfejl.  

3.  Opgraderingssituationer, hvor der er flere gentagelser af rapportlayout, som bevirker flere omdøbningshandlinger i de samme felter, etiketter eller dataelementer.  

 Hvis der registreres et af disse problemer under opdateringen, kan opdateringen ikke anvendes. Du er nødt til at løse problemerne manuelt, f.eks. ved at redigere rapportlayoutet i Word, eller gennem programmering ved at bruge opgraderingskodeenheder.  

## <a name="fixing-errors"></a><a name="fixing-errors"></a><a name="fixing-errors"></a><a name="FixErrors"></a> Rettelse af fejl
 Hvis du får en fejlmeddelelse, når du opdaterer eller kontrollerer layoutopdateringer, skal du sandsynligvis ændre rapportens layout for at løse problemet. Læs fejlmeddelelsen for at finde årsagen til problemet.  

 Det mest almindelige problem opstår, når et felt, der bruges i layoutet, er blevet fjernet fra rapportens datasæt. I dette tilfælde vil du se en linje i den fejlmeddelelse, der angiver, at en vare er blevet fjernet. Du kan løse dette problem ved at ændre layoutet og fjerne det pågældende felt.  

 Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayout](ui-how-create-custom-report-layout.md#ModifyCustomLayout).  

Når du ændrer layoutet, kan du prøve at opdatere layoutet igen.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også
 [Administration af rapportlayout](ui-manage-report-layouts.md)  
 [Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
