---
title: Använder [!DNL Experience Manager] skrivbordsappen
description: Använder  [!DNL Adobe Experience Manager] datorprogrammet.
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---


# Öppna resurser på datorn {#openondesktop-v2}

Du kan öppna fjärrresurserna för visning i det ursprungliga programmet. Resurserna hämtas till en lokal mapp. Sedan startas de i det program som är associerat med filformatet. Du kan ändra det inbyggda programmet så att det öppnar specifika filtyper (tillägg) i Mac eller Windows.

Klicka på **[!UICONTROL Open]** på resursmenyn. Resursen hämtas lokalt och öppnas i det ursprungliga programmet. Kontrollera hämtningsförloppet och överföringshastigheten för stora resurser i statusfältet.

<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")
-->

>[!NOTE]
>
>Om de förväntade ändringarna inte visas i appen klickar du på ikonen Uppdatera ![ikonen Uppdatera](assets/do-not-localize/refresh.png) eller högerklickar i appgränssnittet och klickar på **[!UICONTROL Refresh]**. Åtgärderna är inte tillgängliga medan större hämtningar eller överföringar pågår.

Om du vill öppna den lokala hämtningsmappen för en resurs klickar du på ikonen ![Fler åtgärder](assets/do-not-localize/more2_da2.png) och sedan på åtgärden ![Visa ikon](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** .

## Använd eller placera resurser i ursprungsdokument {#place-assets-in-native-documents}

I vissa fall, till exempel när du monterar en resurs i ett internt dokument, kan du få åtkomst till en fil i Utforskaren i Windows eller Mac Finder. Använd alternativet ![Visa ikon](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** om du vill gå till filsystemplatsen för den lokalt hämtade filen.

![Åtgärden Visa fil för en resurs](assets/revealfile_action_da2.png "Åtgärden Visa fil för en resurs")

Klicka på **[!UICONTROL Reveal File]** eller **[!UICONTROL Reveal Folder]** i en mapp för att öppna Utforskaren eller Mac Finder med filen eller mappen förmarkerad på den lokala datorn. Alternativet är till exempel användbart om du vill montera [!DNL Experience Manager]-filerna i de ursprungliga programmen som har stöd för montering eller länkning av lokala filer. Mer information om hur du monterar filer i Adobe InDesign finns i [Montera bilder](https://helpx.adobe.com/se/indesign/using/placing-graphics.html).

Åtgärden **[!UICONTROL Reveal File]** öppnar en lokal nätverksresurs. Endast de resurser som är tillgängliga lokalt visas. Det innebär att resurser som har visats, hämtats eller öppnats/redigerats med appen visas. Den lokala nätverksresursen överför inga ändringar till [!DNL Experience Manager]. Använd **[!UICONTROL Upload Changes]**- eller **[!UICONTROL Upload]**-åtgärderna i appen explicit för att överföra ändringarna.

>[!NOTE]
>
>För bakåtkompatibilitet med [!DNL Experience Manager]-datorprogrammet v1.x hanteras de filer som visas från en lokal nätverksresurs, endast lokalt tillgängliga filer visas. Skrivbordssökvägarna för de visade filerna är samma som sökvägarna som skapas i programmet v1.x.

>[!CAUTION]
>
>Använd inte alternativet **[!UICONTROL Reveal File]** för att redigera resurser i inbyggda program. Använd i stället **[!UICONTROL Edit]**-åtgärderna. Mer information finns i [Avancerat arbetsflöde: samarbeta med samma filer och undvika redigeringskonflikter](#adv-workflow-collaborate-avoid-conflicts).

## Nästa steg {#next-steps}

* [Titta på en video för att komma igång med Adobe Experience Manager-datorprogrammet](https://experienceleague.adobe.com/sv/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* Ge feedback om dokumentationen med [!UICONTROL Edit this page] ![redigera sidan](assets/do-not-localize/edit-page.png) eller [!UICONTROL Log an issue] ![skapa ett GitHub-problem](assets/do-not-localize/github-issue.png) som är tillgängligt på den högra sidopanelen

* Kontakta [kundtjänst](https://experienceleague.adobe.com/sv?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [Förstå användargränssnittet](/help/using/user-interface.md)
>* [Hantera Assets i skrivbordsapp](/help/using/assets-management-tasks.md)
>* [Sökning](/help/using/search.md)
