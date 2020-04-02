---
title: Bästa tillvägagångssätt för och felsökning av Adobe Experience Manager-datorprogrammet
description: Följ bästa praxis och felsök för att lösa tillfälliga problem som rör installation, uppgradering, konfiguration och så vidare.
uuid: ce98a3e7-5454-41be-aaaa-4252b3e0f8dd
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f5eb222a-6cdf-4ae3-9cf2-755c873f397c
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ac4be2cb69a112f393ec76d5d95987634d0c9c46

---


# Felsöka Adobe Experience Manager-datorprogrammet {#troubleshoot-v2}

Adobe Experience Manager-datorprogrammet (AEM) ansluter till en fjärransluten Experience Manager-distributionsdatabas för digital resurshantering (DAM). The app fetches repository information and search results on your machine, downloads and uploads files and folders, and includes capabilities to manage conflicts with AEM Assets user interface.

Read on to troubleshoot the app, learn the best practices, and find out the limitations.

## Best practices {#best-practices-to-prevent-troubles}

Adhere to the following best practices to prevent some common issues and troubleshooting.

* **Understand how the desktop app works**: Before starting to use the application, spend a few minutes knowing how the app works. Know about linking between Web UI and desktop, repository mapping, asset caching, saving locally and uploading in background. Se [hur det fungerar](release-notes.md#how-app-works).

* **Undvik tecken som inte stöds i mappnamn**: Använd inte blanksteg och ogiltiga tecken när du skapar eller överför mappar. Se en lista med tecken på [Skapa mappar i Experience Manager Assets](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html#Creatingfolders). Vissa användningsfall i Adobe Experience Manager kan påverkas av tecken i mappnamnet som inte stöds.

* **Bästa tillvägagångssätt för att undvika konflikter**: Information om hur du undviker potentiella konflikter när du samarbetar med flera resurser finns i [Undvik redigeringskonflikter](using.md#adv-workflow-collaborate-avoid-conflicts).

* **Använd mappöverföring för stora, hierarkiska mappar**: Använd Experience Manager-skrivbordsappen för att överföra stora mappar i stället för att använda Assets-webbgränssnittet eller andra metoder. Programmet överför resurserna i bakgrunden med loggning och övervakning. Se [Massöverföring av resurser](using.md#bulk-upload-assets).

* **Använd den senaste versionen**: Använd den senaste programversionen och kontrollera alltid om den är kompatibel innan du installerar en ny programversion eller innan du uppgraderar till en nyare version av Adobe Experience Manager. Se [versionsinformation](release-notes.md).

* **Använd samma enhetsbeteckning**: Använd samma enhetsbeteckning i hela organisationen för att mappa till Adobe Experience Manager DAM. Om du vill visa resurser som placerats av andra användare måste sökvägarna vara desamma. Om du använder samma enhetsbeteckning säkerställs en konstant sökväg till DAM-resurser. Resurserna förblir placerade och tas inte bort även om olika enhetsbeteckningar används av olika användare.

* **Lägg märke till nätverket**: Nätverksprestanda är avgörande för prestandan i datorprogrammet Experience Manager. Om du får ett långsammare svar på filöverföringar eller större åtgärder inaktiverar du de funktioner eller program som kan orsaka mycket nätverkstrafik.

* **Användningsexempel som inte stöds för datorprogrammet**: Använd inte appen för Assets&#39; migrering (den kräver planering och andra verktyg). för krävande DAM-åtgärder (som att flytta stora mappar, stora överföringar, hitta filer med avancerade metadatasökningar), och som en synkroniseringsklient (designprinciper och användningsmönster skiljer sig från synkroniserade klienter som Microsoft OneDrive eller Adobe Creative Cloud-synkronisering).

* **Timeout**: För närvarande har skrivbordsappen inte ett konfigurerbart timeout-värde som kopplar från anslutningen mellan Experience Manager-servern och skrivbordsappen efter ett fast tidsintervall. När du överför stora resurser, och anslutningen får timeout efter en stund, försöker programmet överföra resursen några gånger genom att öka tidsgränsen för överföring. Det finns inget rekommenderat sätt att ändra standardinställningarna för timeout.

## Felsöka {#troubleshooting-prep}

Om du vill felsöka problem med skrivbordsprogram bör du känna till följande information. Där kan du också bättre förmedla problemen till Adobes kundtjänst om du väljer att söka support.

### Aktivera felsökningsläge {#enable-debug-mode}

Om du vill felsöka kan du aktivera felsökningsläget och få mer information i loggarna. Om du vill köra programmet i felsökningsläge använder du följande kommandoradsalternativ i en terminal eller i kommandotolken.

* I Windows: `SET AEM_DESKTOP_LOG_LEVEL=DEBUG & "C:\Program Files\Adobe\Adobe Experience Manager Desktop\Adobe Experience Manager Desktop.exe"`

* Mac: `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`

### Plats för loggfiler {#check-log-files-v2}

Du hittar loggfilerna för AEM-skrivbordsappen på följande platser. När du överför många resurser och vissa filer inte kan överföras kan du se filen på `backend.log` ovanstående plats för att identifiera misslyckade överföringar.

* I Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

* Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

>[!NOTE]
>
>När du arbetar med Adobes kundtjänst på en supportförfrågan/anmälan kan du bli ombedd att dela loggfilerna för att hjälpa supportteamet att förstå problemet. Arkivera hela `Logs` mappen och dela den med kundtjänst.

### Rensa cache {#clear-cache-v2}

Att rensa cacheminnet för AEM-skrivbordsappen är en preliminär felsökningsuppgift som kan lösa flera problem. Rensa cacheminnet från appinställningarna. Se [Ange inställningar](install-upgrade.md#set-preferences). Standardplatsen för cachemappen är:

* I Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\`

* Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/`

However, the location can change depending on AEM desktop&#39;s configured AEM endpoint. Värdet är en kodad version av mål-URL:en. For example, if the application is targeting `http://localhost:4502`, the directory name is `http%3A%2F%2Flocalhost%3A4502%2F`. To clear the cache, delete the appropriate folder. Another reason to clear cache is to free disk space when you are running low on disk space.

>[!CAUTION]
>
>If you clear AEM desktop cache, local asset modifications that are not synced to AEM server, are irrevocably lost.

### Know the AEM desktop app version {#know-app-version-v2}

Click ![App menu](assets/do-not-localize/more_options_da2.png) to open the app&#39;s menu and click **[!UICONTROL Help]** > **[!UICONTROL About]**.

## Kan inte se placerade resurser {#placed-assets-missing}

Om du inte kan se de resurser som du eller andra kreatörer har placerat i supportfilerna (till exempel INDD-filer) ska du kontrollera följande:

* Anslutning till servern. Smidig nätverksanslutning kan stoppa hämtningar av resurser.
* Filstorlek. Stora resurser tar längre tid att hämta och visa.
* Enhetliga brev. Om du eller någon annan medarbetare placerade resurserna när du mappade AEM DAM till en annan enhetsbeteckning visas inte de placerade resurserna.
* Behörigheter. Kontakta AEM-administratören om du har behörighet att hämta de placerade resurserna.

## Problem vid uppgradering på macOS {#issues-when-upgrading-on-macos}

Ibland kan problem uppstå när du uppgraderar AEM-datorprogrammet på macOS. Detta orsakas av att det inte går att läsa in nya versioner av AEM-skrivbordsappen korrekt i en äldre systemmapp för AEM-skrivbordsappen. Följande mappar och filer kan tas bort manuellt för att åtgärda problemet.

Innan du utför följande steg drar du programmet `Adobe Experience Manager Desktop` från mappen macOS-program till papperskorgen. Öppna sedan terminalen, kör följande kommando och ange ditt lösenord när du uppmanas till det.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## Kan inte överföra filer {#upload-fails}

Om du använder datorprogrammet med AEM 6.5.1 eller senare uppgraderar du S3- eller Azure-anslutningen till version 1.10.4 eller senare. It resolves file upload failure issue related to [OAK-8599](https://issues.apache.org/jira/browse/OAK-8599). Se [installationsanvisningar](install-upgrade.md#install-v2).

## SSL-konfigurationsproblem {#ssl-config-v2}

De bibliotek som används av AEM-datorprogrammet för HTTP-kommunikation använder strikt SSL-kontroll. Ibland kan en anslutning fungera med en webbläsare, men misslyckas med att använda AEM-skrivbordsappen. Installera det saknade mellanliggande certifikatet i Apache om du vill konfigurera SSL korrekt. Se [Så här installerar du ett mellanliggande CA-certifikat i Apache](https://access.redhat.com/solutions/43575).

## Appen svarar inte {#unresponsive}

I vissa fall kan programmet inte svara, bara visa en vit skärm eller visa ett fel längst ned i gränssnittet utan några alternativ i gränssnittet. Prova följande i den ordning du vill:

1. Högerklicka på programgränssnittet och klicka **[!UICONTROL Refresh]**.
1. Avsluta programmet och starta om det.

I båda metoderna startar programmet i rotmappen DAM.

>[!MORELIKETHIS]
>
>* [Kända fel](release-notes.md#known-issues-v2)
>* [Undvik redigeringskonflikter](using.md#adv-workflow-collaborate-avoid-conflicts)