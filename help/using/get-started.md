---
title: Kom igång [!DNL Experience Manager] med datorprogrammet
description: Läs om hur  [!DNL Experience Manager] datorprogrammet förbättrar framtagning och publicering av innehåll med smidiga arbetsflöden och produktivitetsfunktioner.
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 0%

---


# Kom igång med [!DNL Adobe Experience Manager]-datorprogrammet {#getting-started-desktop-app}

Använd skrivbordsappen [!DNL Adobe Experience Manager] för att komma åt digitala resurser som lagras i en [!DNL Adobe Experience Manager] DAM-databas på din lokala dator. Du kan sedan använda dessa resurser i alla skrivbordsprogram. Du kan öppna och redigera resurserna lokalt i skrivbordsprogram. När du har gjort ändringar kan du överföra dem tillbaka till [!DNL Experience Manager] med versionskontroll för att dela uppdateringar med andra användare. Du kan också överföra nya filer och mapphierarkier till [!DNL Experience Manager], skapa mappar och ta bort resurser och mappar från [!DNL Experience Manager] DAM.

Integreringen gör att olika roller i organisationen kan hantera resurser centralt i [!DNL Experience Manager Assets] och få åtkomst till resurserna på det lokala skrivbordet i de ursprungliga programmen i Windows eller macOS.

När du öppnar programmet efter utloggning eller för första gången anger du URL-adressen till [!DNL Experience Manager]-servern i formatet `https://[aem-server-url]:[port]/`. Välj sedan alternativet [!UICONTROL Connect]. Ange autentiseringsuppgifter för att ansluta programmet till servern.

De huvuduppgifter du utför med skrivbordsappen [!DNL Adobe Experience Manager] är:

![Arbetsflöden och uppgifter som du kan utföra med [!DNL Experience Manager] skrivbordsappen ](assets/aem_desktop_app_usecases_v2.png)

## Så här fungerar skrivbordsappen {#how-app-works2}

Innan du börjar använda programmet bör du förstå [hur appen fungerar](release-notes.md#how-app-works). Bekanta dig också med följande termer:

* **[!UICONTROL Desktop Actions]**: Från Assets webbgränssnitt, från en webbläsare, kan du utforska resursplatserna eller checka ut och öppna resursen för redigering i ditt datorprogram. De här åtgärderna är tillgängliga från webbgränssnittet och använder skrivbordsappsfunktioner.

* Filstatusen är **[!UICONTROL Cloud Only]**: Sådana resurser hämtas inte på den lokala datorn och är endast tillgängliga på [!DNL Experience Manager]-servern.

* Filstatusen är **[!UICONTROL Available locally]**: Resurserna hämtas och är tillgängliga på den lokala datorn som de är. Resurserna ändras inte.

* Filstatusen är **[!UICONTROL Edited locally]**: Sådana resurser ändras lokalt och ändringarna finns kvar på den överförda servern [!DNL Experience Manager]. När du har överfört filen ändras statusen till [!UICONTROL Available locally]. Se [redigera resurser](upload-assets.md#edit-assets-upload-updated-assets).

* Filstatus är **[!UICONTROL Editing conflict]**: Om du och andra redigerar en resurs samtidigt anger programmet att en redigeringskonflikt har inträffat. Programmet innehåller även alternativ för att behålla eller ignorera ändringarna. Se [hur du undviker redigeringskonflikter](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts).

* Filstatus är **[!UICONTROL Modified remotely]**: Programmet anger om en resurs som du har hämtat ändras på servern [!DNL Experience Manager]. Programmet har också möjlighet att hämta den senaste versionen och uppdatera din lokala kopia. Se [hur du undviker redigeringskonflikter](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts).

* **[!UICONTROL Check-out]**: Om du redigerar en fil eller har för avsikt att redigera en fil, kan du växla status för att checka ut. Den lägger till en låsikon på resursen i appen och [!DNL Experience Manager]-webbgränssnittet. Låsikonen anger för andra användare att de inte behöver redigera samma resurs samtidigt eftersom den leder till en redigeringskonflikt.

* **[!UICONTROL Check-in]**: Markera resursen som säker så att andra användare kan redigera den utan att orsaka en redigeringskonflikt. När du överför dina ändringar tas låsikonen automatiskt bort. När du växlar incheckningsstatus tas även låsikonen bort, men Adobe rekommenderar att du undviker att checka in manuellt utan att överföra ändringarna. Om du ångrar ändringarna växlar du incheckningen manuellt.

* **[!UICONTROL Open]**-åtgärd: Öppna resursen och förhandsgranska den i det ursprungliga programmet. Adobe rekommenderar att du undviker att redigera resursen genom att använda den här åtgärden. Orsaken är att den inte checkar ut tillgången. Samtidigt kan andra användare göra redigeringar som leder till redigeringskonflikter.

* **[!UICONTROL Edit]**-åtgärd: Använd åtgärden för att ändra bilden. Om du klickar på [!UICONTROL Edit] checkas resursen ut och en låsikon läggs till på resursen. Om du inte vill redigera resursen klickar du på [!UICONTROL Toggle check-in] när du har klickat på Redigera. Om du vill ta bort, byta namn på eller flytta resurser i DAM-mapphierarkin [!DNL Experience Manager] använder du [!DNL Experience Manager]-webbgränssnittsåtgärderna och inte redigeringsåtgärden.

* **[!UICONTROL Download]**-åtgärd: Hämta resursen till din lokala dator. Du kan hämta resurserna nu och redigera dem senare. Arbeta offline och ladda upp ändringarna senare. Assets laddas ned i en cachemapp i filsystemet.

* **[!UICONTROL Reveal File]**- eller **[!UICONTROL Reveal Folder]**-åtgärd: När resurserna hämtas till en lokal cachemapp härmar programmet en lokal nätverksenhet. Den ger en lokal sökväg för varje resurs. Om du vill veta sökvägen använder du lämpligt visningsalternativ i appen. Funktionen Visa krävs för att placera resurser i Creative Cloud-programmet. Se [placera resurser](search.md#place-assets-in-native-documents).

* **[!UICONTROL Open In Web]**-åtgärd: Om du vill visa resursen i webbgränssnittet för [!DNL Experience Manager] öppnar du den på webben. Du kan initiera fler arbetsflöden från gränssnittet [!DNL Experience Manager], som att uppdatera metadata eller resursidentifiering.

* **[!UICONTROL Delete]**-åtgärd: Ta bort resursen från DAM-databasen [!DNL Experience Manager]. Åtgärden tar bort originalkopian av resursen på Experience Manager-servern. Om du bara vill ignorera ändringar i den lokala resursen läser du [Ignorera ändringar](upload-assets.md#edit-assets-upload-updated-assets).

* **[!UICONTROL Upload Changes]**: Skrivbordsappen överför bara den uppdaterade resursen när du uttryckligen överför den till servern [!DNL Experience Manager]. När du sparar redigeringarna sparas ändringarna bara på den lokala datorn. När du överför filen checkas resursen in automatiskt och låsikonen tas bort. Se [redigera resurser](upload-assets.md#edit-assets-upload-updated-assets).

## Aktivera skrivbordsåtgärder i webbgränssnittet [!DNL Experience Manager] {#desktopactions-v2}

I [!DNL Assets]-användargränssnittet i en webbläsare kan du utforska resursplatserna eller checka ut och öppna resursen för redigering i skrivbordsprogrammet. Dessa alternativ kallas [!UICONTROL Desktop Actions] och är inte aktiverade som standard. Följ de här stegen för att aktivera den.

1. Klicka på ikonen [!DNL Assets] i verktygsfältet i **[!UICONTROL User]**-konsolen.
1. Klicka på **[!UICONTROL My Preferences]** för att visa dialogrutan **[!UICONTROL Preferences]**.

1. I dialogrutan [!UICONTROL User Preferences] väljer du **[!UICONTROL Show Desktop Actions For Assets]** och klickar sedan på **[!UICONTROL Accept]**.

   ![Markera Visa skrivbordsåtgärder för Assets om du vill aktivera skrivbordsåtgärder](assets/enable_desktop_actions1.png)

## Starta från webbgränssnittet [!DNL Assets] {#adv-workflow-start-from-aem-ui}

Starta vid behov arbetsflödet från Assets webbgränssnitt. Skrivbordsappen integreras med [!DNL Experience Manager] för att ta över när det efterfrågas med skrivbordsåtgärder.

Ett särskilt exempel på hur du startar ett arbetsflöde från webbgränssnittet är resursidentifiering. Omnissearch bar i Assets användargränssnitt ger en omfattande och avancerad sökfunktion. Du kanske först vill hitta en önskad resurs på webben och sedan starta arbetsflödet i appen med hjälp av [!UICONTROL Desktop Actions]. I vissa exempelfall kan du filtrera sökresultat med hjälp av ansikten, hitta en specifik resurs som licensierats från Adobe Stock eller anpassa den som implementerats av din organisation så att du kan identifiera den bättre i webbgränssnittet.

Funktionen för skrivbordsprogram används när du försöker utföra följande åtgärder i Assets webbgränssnitt:

* [!UICONTROL Desktop Actions] som tillåter [!UICONTROL Open], [!UICONTROL Edit] och [!UICONTROL Reveal]
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] eller [!UICONTROL check-in]

De åtgärder på webbgränssnittet som är tillgängliga för en resurs som är utcheckad i appen är till exempel [!UICONTROL Open], [!UICONTROL Reveal] och [!UICONTROL Check in].

![Skrivbordsåtgärder i [!DNL Experience Manager] webbgränssnittet](assets/assets_web_actions_da2.png "Skrivbordsåtgärder i Experience Manager webbgränssnitt")

>[!NOTE]
>
>Webbläsaren kan uppmana dig att tillåta att skrivbordet [!DNL Adobe Experience Manager] startas. Om du vill att appen ska kunna överföras utan avbrott från webbläsaren till appen varje gång markerar du kryssrutan så att appen kan ta över.

Du kan inte hitta följande information eller arbetsflöde med webbgränssnittet. Använd skrivbordsappen eftersom webbgränssnittet inte kan spåra lokala ändringar och inte känner till följande:

* Filerna redigeras lokalt.
* Filer som har en redigeringskonflikt och ett sätt att lösa den.
* Överför lokala ändringar till [!DNL Experience Manager].
* Olika statusvärden för de lokalt tillgängliga filerna.

Du kan tvärtom öppna resursen i webbgränssnittet från skrivbordsappen med åtgärden **[!UICONTROL Open In Web]**.

## Nästa steg {#next-steps}

* [Titta på en video för att komma igång med Adobe Experience Manager-datorprogrammet](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* Ge feedback om dokumentationen med [!UICONTROL Edit this page] ![redigera sidan](assets/do-not-localize/edit-page.png) eller [!UICONTROL Log an issue] ![skapa ett GitHub-problem](assets/do-not-localize/github-issue.png) som är tillgängligt på den högra sidopanelen

* Kontakta [kundtjänst](https://experienceleague.adobe.com/?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [Förstå användargränssnittet](/help/using/user-interface.md)
>* [Versionsinformation och kända fel](/help/using/release-notes.md)
>* [Installera eller uppgradera datorprogrammet](/help/using/install-upgrade.md)
