---
title: Hämta resurser med  [!DNL Experience Manager] datorprogrammet
description: Hämta resurser med  [!DNL Adobe Experience Manager] datorprogrammet.
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---


# Hämta resurser lokalt {#download-assets-locally}

Appen hämtar ofta resurser från servern [!DNL Experience Manager] till det lokala filsystemet. Nedladdningarna förbrukar bandbredd och diskutrymme. Genom att känna till scenarierna kan du optimera väntetiden för nedladdningen. Du kan hämta resurserna på det lokala filsystemet. Appen hämtar resurserna från servern [!DNL Experience Manager] och sparar samma kopia i det lokala filsystemet.

Klicka på **[!UICONTROL More actions]** ![Ikonen Fler alternativ](assets/do-not-localize/more2_da2.png) för alternativ och klicka på ![ikonen Hämta](assets/do-not-localize/download_cloud_da2.png) för att hämta.

![Hämtningsalternativ för en resurs](assets/download_option_da2.png "Hämtningsalternativ för en resurs")

>[!NOTE]
>
>När du hämtar eller överför en stor fil eller många filer, inaktiveras åtgärderna för resurser och mappar. Åtgärderna är tillgängliga när hämtningen eller överföringen är klar.

När du använder åtgärden [!UICONTROL Open] för att öppna en resurs i ett systemspecifikt skrivbordsprogram hämtas resursen lokalt, om den inte redan är tillgänglig lokalt. Se [Öppna resurser](#openondesktop-v2).

När du visar platsen för en resurs eller en mapp inifrån programmet hämtas resursen eller mappen först lokalt och öppnas sedan på datorn i den lokala nätverksresursen. Se [Öppna resurser](#openondesktop-v2).

När du använder åtgärden [!UICONTROL Edit] för att redigera en resurs i ett systemspecifikt skrivbordsprogram hämtas resursen lokalt, om den inte redan är tillgänglig lokalt. Se [Redigera resurser och överföra uppdaterade resurser till [!DNL Experience Manager]](#edit-assets-upload-updated-assets).

Om programmet är installerat och tillåts att göra det, slutförs åtgärderna när du använder [!UICONTROL Desktop Actions] från [!DNL Experience Manager]-webbgränssnittet. Programmet hämtar resursen först och slutför sedan åtgärden.

## Hämta flera resurser {#download-multiple-assets}

Hämtning av flera resurser kan leda till sämre prestanda om köstorleken är stor eller om du har problem med nätverket. Du kan också ovetande köa många resurser för hämtning när du hämtar en mapp. För att undvika långa väntetider begränsar appen antalet resurser som hämtas på en gång. Mer information om hur du konfigurerar den finns i [Ange inställningar](install-upgrade.md#set-preferences). Även under denna gräns kan programmet ibland behöva be om en bekräftelse innan en till synes stor mapp laddas ned.

![Appen bekräftar hämtning av relativt stort antal resurser](assets/download_confirmation_da2.png "Appen bekräftar hämtning av relativt stort antal resurser")

Om mappar markeras och hämtas hämtar programmet bara resurser som lagras direkt i mapparna i [!DNL Experience Manager]. Det hämtar inte resurser från undermappar automatiskt.

## Nästa steg {#next-steps}

* [Titta på en video för att komma igång med Adobe Experience Manager-datorprogrammet](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* Ge feedback om dokumentationen med [!UICONTROL Edit this page] ![redigera sidan](assets/do-not-localize/edit-page.png) eller [!UICONTROL Log an issue] ![skapa ett GitHub-problem](assets/do-not-localize/github-issue.png) som är tillgängligt på den högra sidopanelen

* Kontakta [kundtjänst](https://experienceleague.adobe.com/?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [Överför resurser](/help/using/upload-assets.md)
>* [Förstå användargränssnittet](/help/using/user-interface.md)
>* [Sökning](/help/using/search.md)

