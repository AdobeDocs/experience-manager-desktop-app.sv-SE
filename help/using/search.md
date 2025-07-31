---
title: Bläddra bland, söka efter och förhandsgranska resurser i [!DNL Experience Manager]-datorprogrammet
description: Bläddra bland, söka efter och förhandsgranska resurser i  [!DNL Adobe Experience Manager] datorprogrammet.
feature: Desktop App
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---


# Bläddra bland, söka efter och förhandsgranska resurser {#browse-search-preview-assets}

Du kan bläddra till, söka efter och förhandsvisa de resurser som finns i [!DNL Experience Manager]-databasen, allt från skrivbordsprogrammet. Prova följande i appen:

1. Bläddra till en mapp och se grundläggande information om resurserna som finns i mappen, tillsammans med små miniatyrbilder av alla resurser.

   ![Bläddra bland filer och mappar i DAM](assets/browse_folder_da2.png "Bläddra bland filer och mappar i DAM")

1. Om du vill visa mer information och en större miniatyrbild av en enskild resurs klickar du på filnamnet.

   ![Se en större förhandsvisning av en resurs och åtgärder](assets/large_preview_actions_da2.png "Se en större förhandsvisning av en resurs och åtgärder")

1. Klicka på **[!UICONTROL Open]** eller **[!UICONTROL Edit]** om du vill hämta filen lokalt och bara visa eller redigera den i det ursprungliga programmet.
1. Sök med nyckelord för att hitta en relaterad resurs i databasen [!DNL Experience Manager]. Använd `?` och `*` som jokertecken. Dessa jokertecken ersätter ett enda tecken eller flera tecken. Filtrera och sortera resultatet efter behov.

   ![Exempelsökning med asterisk som jokertecken](assets/search_wildcard_da2.png "Exempelsökning med asterisk som jokertecken")

   ![En annan exempelsökning med asterisk-jokertecken](assets/search_wildcard2_da2.png "En annan exempelsökning med en annan placering av asterisk-jokertecken")

>[!NOTE]
>
>Resurserna visas i programmet genom att sökvillkoren matchas i flera metadatafält, inte bara resursens namn eller filnamn.

## Öppna resurser på datorn {#openondesktop-v2}

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

Klicka på **[!UICONTROL Reveal File]** eller **[!UICONTROL Reveal Folder]** i en mapp för att öppna Utforskaren eller Mac Finder med filen eller mappen förmarkerad på den lokala datorn. Alternativet är till exempel användbart om du vill montera [!DNL Experience Manager]-filerna i de ursprungliga programmen som har stöd för montering eller länkning av lokala filer. Mer information om hur du monterar filer i Adobe InDesign finns i [Montera bilder](https://helpx.adobe.com/indesign/using/placing-graphics.html).

Åtgärden **[!UICONTROL Reveal File]** öppnar en lokal nätverksresurs. Endast de resurser som är tillgängliga lokalt visas. Det innebär att resurser som har visats, hämtats eller öppnats/redigerats med appen visas. Den lokala nätverksresursen överför inga ändringar till [!DNL Experience Manager]. Använd **[!UICONTROL Upload Changes]**- eller **[!UICONTROL Upload]**-åtgärderna i appen explicit för att överföra ändringarna.

>[!NOTE]
>
>För bakåtkompatibilitet med [!DNL Experience Manager]-datorprogrammet v1.x hanteras de filer som visas från en lokal nätverksresurs, endast lokalt tillgängliga filer visas. Skrivbordssökvägarna för de visade filerna är samma som sökvägarna som skapas i programmet v1.x.

>[!CAUTION]
>
>Använd inte alternativet **[!UICONTROL Reveal File]** för att redigera resurser i inbyggda program. Använd i stället **[!UICONTROL Edit]**-åtgärderna. Mer information finns i [Avancerat arbetsflöde: samarbeta med samma filer och undvika redigeringskonflikter](#adv-workflow-collaborate-avoid-conflicts).

### Hantera specialtecken i resursnamn {#special-characters-in-filename}

I det äldre programmet bevarade de nodnamn som skapades i databasen utrymmet och skiftläget för mappnamnen som användaren angett. Aktivera [!UICONTROL Use legacy conventions when creating nodes for assets and folders] i [!UICONTROL Preferences] om du vill att det aktuella programmet ska emulera reglerna för nodnamngivning i v1.10-appen. Se [appinställningar](/help/using/install-upgrade.md#set-preferences). Den här äldre inställningen är inaktiverad som standard.

>[!NOTE]
>
>Programmet ändrar bara nodnamnen i databasen med följande namnkonventioner. Appen behåller resursens `Title` som den är.

| Characters ‡ | Äldre inställning i appen | Vid förekomst i filnamn | Vid förekomst i mappnamn | Exempel |
|---|---|---|---|---|
| `. / : [ ] \| *` | Aktiverad eller inaktiverad | Ersatt med `-` (bindestreck). En `.` (punkt) i filnamnstillägget behålls som den är. | Ersatt med `-` (bindestreck). | `myimage.jpg` förblir oförändrad och `my.image.jpg` ändras till `my-image.jpg`. |
| `% ; # , + ? ^ { } "` och blanksteg | ![avmarkera ikon](assets/do-not-localize/deselect-icon.png) inaktiverad | Blanksteg behålls | Ersatt med `-` (bindestreck). | `My Folder.` ändras till `my-folder-`. |
| `# % { } ? & .` | ![avmarkera ikon](assets/do-not-localize/deselect-icon.png) inaktiverad | Ersatt med `-` (bindestreck). | NA. | `#My New File.` ändras till `-My New File-`. |
| Versaler | ![avmarkera ikon](assets/do-not-localize/deselect-icon.png) inaktiverad | Läsningen behålls som den är. | Ändrad till gemener. | `My New Folder` ändras till `my-new-folder`. |
| Versaler | ![markeringskontrollerad ikon](assets/do-not-localize/selection-checked-icon.png) aktiverad | Läsningen behålls som den är. | Läsningen behålls som den är. | NA. |

‡ Teckenlistan är en blankstegsavgränsad lista.

## Söka efter alla redigerade bilder {#find-all-edited-images}

Programmet tillhandahåller en vy med namnet **[!UICONTROL Edited locally]** som ger dig snabb åtkomst till alla filer som du har hämtat lokalt (via [!UICONTROL Open] eller [!UICONTROL Edit] åtgärder) och sedan ändrat. Med appen kan du välja alla lokalt redigerade resurser och överföra ändringarna med några klick. I den här vyn visas även lokalt redigerade resurser som har en redigeringskonflikt.

![Filtrera för att se alla lokalt redigerade resurser](assets/edited_locally_filter_da2.png "Du kan till exempel filtrera för att se alla lokalt redigerade resurser för en massöverföring av redigeringar")

## Nästa steg {#next-steps}

* [Titta på en video för att komma igång med Adobe Experience Manager-datorprogrammet](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* Ge feedback om dokumentationen med [!UICONTROL Edit this page] ![redigera sidan](assets/do-not-localize/edit-page.png) eller [!UICONTROL Log an issue] ![skapa ett GitHub-problem](assets/do-not-localize/github-issue.png) som är tillgängligt på den högra sidopanelen

* Kontakta [kundtjänst](https://experienceleague.adobe.com/?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [Förstå användargränssnittet](/help/using/user-interface.md)
>* [Använder skrivbordsapp](/help/using/using-desktop-app.md)
>* [Hantera Assets i skrivbordsapp](/help/using/assets-management-tasks.md)
