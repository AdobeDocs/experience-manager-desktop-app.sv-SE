---
title: Använd [!DNL Experience Manager] datorprogrammet
description: Använd [!DNL Adobe Experience Manager] datorprogrammet för att arbeta med [!DNL Adobe Experience Manager] DAM-resurser direkt från Win- eller Mac-datorn och använda i andra program.
feature: Desktop App,Asset Management
source-git-commit: c5aeee9ab636ba7bedff4225172140d59cfe627d
workflow-type: tm+mt
source-wordcount: '1416'
ht-degree: 0%

---


# Assets-hanteringsuppgifter i [!DNL AEM Desktop App] {#assets-management-tasks}

Resurshantering innebär att organisera, underhålla och optimera digitala resurser för att effektivisera arbetsflödena. Det innehåller uppgifter som att duplicera och byta namn på filer, fästa eller ta bort mappar för snabb åtkomst samt visa resurser i olika layouter. Detta förbättrar effektiviteten, förenklar resursspårningen och gör det enkelt att hämta och organisera digitala resurser på olika plattformar.

## Visa resurser {#view-assets}

Med AEM Desktop App kan du visa resurser i fyra olika vyer:

* **[!UICONTROL Show Assets]:** Gör att du kan visa alla resurser.
* **[!UICONTROL Show Collections]:** Gör att du kan se alla samlingar som har skapats i det ursprungliga AEM-programmet. Visa fler [samlingar](#collections-desktop-app).
* **[!UICONTROL Edited Locally]:** Gör att du kan visa alla lokalt ändrade resurser. I den här vyn kan du lägga till och överföra flera resurser.
* **[!UICONTROL Asset transfers]:** Gör att du kan visa alla resurser som har överförts från det ursprungliga programmet till det lokala programmet eller vice versa.
* **[!UICONTROL Pinned items]:** Gör att du kan visa alla fästa objekt.

Så här väljer du bland olika vyer av resurser i AEM-datorprogrammet:

1. Öppna AEM-datorprogrammet.

1. Gå till listrutan för visning överst till höger. Välj en av de tillgängliga vyerna.

   ![fäst eller ta bort mapp](assets/view-pinned-assets.png)

## Visa nyligen tillagda mappar och filer {#view-newly-added-files-folders}

Du kan överföra nyskapade resurser från din lokala dator till AEM, där den centrala databasen lagras. Om du vill visa de nya resurserna lokalt går du till listrutan **[!UICONTROL View]** och väljer **[!UICONTROL Show Assets]** för att visa alla uppdateringar med deras tidslinje och titlar, eller väljer **[!UICONTROL Edited Locally]**. Båda alternativen visar explicit de lokalt redigerade resurserna.

## Duplicera filer {#duplicate-files}

När du vill bevara en originalfil och göra ändringar i en liknande fil kan du duplicera filer på olika platser (lokala och molnbaserade) samtidigt. Det kan åstadkommas genom att duplicera filer används för flera resurser.

Så här duplicerar du filer i AEM-datorprogrammet:

1. Bläddra till en mapp och markera den resurs som du vill duplicera.

   ![Fler alternativ](assets/more-options1.png)

1. Klicka på **[!UICONTROL More actions]** ![ikonen Fler åtgärder](assets/do-not-localize/more2_da2.png) och välj åtgärden ![Duplicera ikon](assets/do-not-localize/duplicate.svg) **[!UICONTROL Duplicate File]** .

1. Den duplicerade filen skapas med samma filnamn och innehåll.

## Ändra namn på en resurs eller mapp {#rename-asset-title}

Så här byter du namn på en resurs eller mapp:

1. Bläddra bland resursen som du vill byta namn på. Vid namngivning av en mapp tillåts inte specialtecken som `\ / : * ?  | < > [ ] %`;. Om de inkluderas ersätts de automatiskt med ett bindestreck `-`.

1. Klicka på **[!UICONTROL More actions]** ![ikonen Fler åtgärder](assets/do-not-localize/more2_da2.png) och välj **[!UICONTROL Rename]** för att lägga till den önskade titeln för en resurs.


## Fäst eller ta bort mapp {#pin-unpin-folder}

Fastnålade mappar synkroniseras automatiskt för att återspegla ändringar som gjorts i programmet. För snabb åtkomst kan du fästa eller ta bort en mapp genom att utföra stegen nedan:

1. Bläddra efter den resurs som du vill fästa eller ta bort.

1. Klicka på **[!UICONTROL More actions]** ![ikonen Fler åtgärder](assets/do-not-localize/more2_da2.png) och välj [!UICONTROL pin] för att fästa resursen eller mappen. Du kan också klicka på [!UICONTROL unpin] för att ta bort den.

   ![fäst eller ta bort mapp](assets/pin-unpin.png)

## Uppdatera automatiskt {#auto-refresh}

Funktionen för automatisk uppdatering uppdaterar automatiskt innehållet i realtid så att du alltid ser den senaste informationen utan att behöva läsa in sidan manuellt. Utför stegen nedan om du vill uppdatera resurser automatiskt för att få en lista över uppdaterade resurser:

1. Öppna AEM-datorprogrammet.

1. Klicka på ![uppdateringsikonen](assets/do-not-localize/refresh.png) på menyraden för att hämta uppdateringarna.

## Samlingar {#collections-desktop-app}

Med AEM skrivbordsapp kan du [visa](#view-collections-desktop-app), [hämta](#download-collections-desktop-app) och bläddra bland samlingar som har skapats i [!DNL Adobe Experience Manager Assets]-programmet.

### Visa samlingar {#view-collections-desktop-app}

Utför följande steg för att visa samlingar i skrivbordsappen:

1. Öppna AEM-datorprogrammet och gå till [visa resurser](#view-assets).

1. Välj **[!UICONTROL Show Collections]**. De samlingar som är tillgängliga i det ursprungliga programmet visas.

   ![Datorappen Collections](assets/collections-desktop-app.png)

### Hämta samlingar {#download-collections-desktop-app}

Utför följande steg för att hämta samlingar i skrivbordsappen:

1. Följ steg 1 och 2 så som visas i [visa samlingar](#view-collections-desktop-app).

1. Gå till fler åtgärder ![Ikonen Fler åtgärder](assets/do-not-localize/more2_da2.png) i samlingen som du vill hämta.

1. Klicka på **[!UICONTROL Download]** om du vill hämta den aktuella samlingen.

## Skapa mapp med metadataschema {#create-folder-with-metadata-schema}

Med AEM Desktop App kan du tilldela metadata när du skapar en ny mapp. Gör så här:

1. Gå till ikonen Skapa katalog ![ikonen Lägg till mapp](assets/do-not-localize/add-folder.svg). **[!UICONTROL Create Directory]**-skärmen visas.

1. Lägg till följande information:
   * **[!UICONTROL Name]** av mappen.
   * **[!UICONTROL Folder Metadata Schema]** om du vill välja en metadatahierarki för mappen eller **[!UICONTROL none]** om du inte vill relatera några metadata till den.

1. Klicka på **[!UICONTROL OK]** om du vill fortsätta.

## Lista över överförda tillgångar {#list-of-transferred-assets}

Mer information om hur du visar en lista över resurser som överförts under en viss session finns i [Överför resurser till [!DNL Experience Manager]](#upload-and-add-new-assets-to-aem).

## Avancerat arbetsflöde: samarbeta med samma filer och undvik redigeringskonflikter {#adv-workflow-collaborate-avoid-conflicts}

I samarbetsmiljöer kan flera användare arbeta med samma uppsättning resurser, vilket kan leda till versionskonflikter. Följ dessa metodtips för att förhindra konflikter:

* Redigera inga resurser genom att klicka på [!UICONTROL Open]. Redigera inte lokalt hämtade resurser genom att öppna dem från filsystemmappen. Andra användare vet inte om resursen redigeras.
* Om du vill redigera en resurs klickar du alltid på [!UICONTROL Edit]. Resursen öppnas i det ursprungliga programmet och en låsikon läggs till på resursen, så att de andra användarna vet att resursen redigeras.
* Klicka på [!UICONTROL Toggle Check-in] om du av misstag påbörjar redigering utan att klicka på [!UICONTROL Edit]. Den här funktionen lägger till en låsikon till resursen. Även om du planerar att redigera en resurs senare men vill undvika att andra redigerar den, klickar du på [!UICONTROL Toggle Check-in] för att låsa resursen.
* Innan du redigerar en resurs måste du se till att andra användare inte redigerar den. Leta efter låsikonen på resursen.
* När du är klar med redigeringarna överför du alla ändringar och checkar sedan in resursen.

![Status för redigeringskonflikter](assets/edits_conflicts_status_da2.png "Status för redigeringskonflikter")

Om en lokalt hämtad resurs uppdateras på servern [!DNL Experience Manager] visas programmets **[!UICONTROL Modified remotely]**-status. Du kan antingen ta bort din lokala kopia eller uppdatera den lokala kopian genom att klicka på [!UICONTROL Remove] respektive [!UICONTROL Update]. Med länkarna i dialogrutan kan du visa båda versionerna av resursen.

![Alternativ för att lösa konflikten när resursen ändras på fjärrbasis](assets/modified_remotely_dialog_da2.png "Alternativ för att lösa konflikten när resursen ändras på fjärrbasis")

Om en resurs som du redigerar lokalt även uppdateras på servern utan din vetskap, visas statusen **[!UICONTROL Editing Conflict]** i appen. Du kan behålla en uppsättning av ändringarna - antingen behålla dina uppdateringar (klicka på **[!UICONTROL Keep Mine]**) och ta bort den andra användarens redigering eller ta hänsyn till den andra användarens uppdateringar och ta bort din (**[!UICONTROL Overwrite Mine]**).

![Alternativ för att lösa en redigeringskonflikt](assets/editing_conflict_dialog_da2.png "Alternativ för att lösa en redigeringskonflikt")

## Avancerat arbetsflöde: placera och länka resurser i InDesign-filer {#adv-workflow-place-assets-indesign}

När du använder datorprogrammet [!DNL Experience Manager] för att öppna filer med länkade resurser hämtas resurserna i förväg och visas i de ursprungliga programmen. För att det här arbetsflödet ska fungera måste ditt inbyggda program ha stöd för att placera länkar till lokala resurser och [!DNL Experience Manager] måste ha stöd för att kunna matcha länkarna i de binära filerna med referenser på serversidan.

Skrivbordsappen [!DNL Experience Manager] har stöd för det här arbetsflödet med några utvalda Adobe Creative Cloud-program och -filformat - Adobe InDesign, Adobe Illustrator och Adobe Photoshop. Med arbetsflödet kan du arbeta effektivt med de Creative Cloud-filer som stöds. Om användare A lägger till resurser i en InDesign-fil och checkar in dem i [!DNL Experience Manager] kan användare B se resurserna i filen även om de inte är en del av den. Resurserna hämtas lokalt till dator med användare B.

>[!NOTE]
>
>Skrivbordsappen kan mappas till valfri enhet i Windows. För mjuka åtgärder ska du dock inte ändra standardenhetsbokstaven. Om användare i samma organisation använder olika enhetsbokstäver kan de inte se resurser som placerats av andra. De placerade resurserna hämtas inte när sökvägen ändras. De placerade resurserna fortsätter att vara placerade i den binära filen (till exempel INDD) och tas inte bort.

Mer information om begränsningarna i det här arbetsflödet finns i [systemkraven och versionerna som stöds](release-notes.md).

Så här provar du arbetsflödet med en bildresurs och InDesign:

1. Använd en INDD-fil med placerade resurser i [!DNL Experience Manager]. Mer information om hur du skapar en sådan INDD-fil finns i [Placera grafik](https://helpx.adobe.com/indesign/using/placing-graphics.html).
1. I skrivbordsappen **[!UICONTROL Edit]** den INDD-fil som innehåller placerade resurser i [!DNL Experience Manager].
1. Programmet hämtar InDesign-filen och de länkade resurserna. När InDesign öppnar dokumentet är länkarna lösta, resurserna hämtas och resurserna visas i InDesign-dokumentet.
1. Om du vill montera en ny bild i InDesign-filen använder du åtgärden **[!UICONTROL Reveal File]** för resursen. Åtgärden hämtar resursen lokalt och öppnar den lokala nätverksresursplatsen i Utforskaren eller Mac Finder.
1. Placera den visade resursen i InDesign-dokumentet. Då skapas en länk i dokumentet.
1. När du är klar med redigeringarna i InDesign-dokumentet sparar du det och överför det till [!DNL Experience Manager] med datorprogrammet.

## Nästa steg {#next-steps}

* [Titta på en video för att komma igång med Adobe Experience Manager-datorprogrammet](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* Ge feedback om dokumentationen med [!UICONTROL Edit this page] ![redigera sidan](assets/do-not-localize/edit-page.png) eller [!UICONTROL Log an issue] ![skapa ett GitHub-problem](assets/do-not-localize/github-issue.png) som är tillgängligt på den högra sidopanelen

* Kontakta [kundtjänst](https://experienceleague.adobe.com/?support-solution=General#support)

<!--* Provide product feedback using the [!UICONTROL Feedback] option available on the AEM Desktop App user interface>-->

>[!MORELIKETHIS]
>
>* [Förstå användargränssnittet](/help/using/user-interface.md).
>* [Guiden Kom igång](/help/using/get-started.md).
