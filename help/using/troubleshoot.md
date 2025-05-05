---
title: Best practices for and troubleshooting [!DNL Adobe Experience Manager] desktop app
description: Följ bästa praxis och felsök för att lösa tillfälliga problem som rör installation, uppgradering, konfiguration och så vidare.
exl-id: f388e4ac-907d-4093-ba6f-86ecdafeb015
source-git-commit: 5676e7ece8bb43f051dae72d17e15ab1c34caefc
workflow-type: tm+mt
source-wordcount: '2275'
ht-degree: 0%

---

# Felsök [!DNL Adobe Experience Manager]-datorprogrammet {#troubleshoot-v2}

Skrivbordsappen [!DNL Adobe Experience Manager] ansluter till DAM-databasen (Digital Asset Management) för en [!DNL Experience Manager]-distribution. Appen hämtar databasinformation och sökresultat på din dator, hämtar och överför filer och mappar samt innehåller funktioner för att hantera konflikter med Assets användargränssnitt.

Läs vidare för att felsöka appen, lära dig de bästa metoderna och ta reda på begränsningarna.

## God praxis {#best-practices-to-prevent-troubles}

Följ följande metodtips för att förebygga vissa vanliga problem och felsökning.

* **Förstå hur skrivbordsappen fungerar**: Innan du börjar använda programmet bör du ägna en stund åt att veta hur appen fungerar. Lär dig mer om att länka mellan webbgränssnittet [!DNL Experience Manager] och skrivbordet, databasmappning, resurscachning, spara lokalt och överföra i bakgrunden. Se [hur det fungerar](release-notes.md#how-app-works).

* **Undvik tecken som inte stöds i mappnamn**: Använd inte blanksteg och ogiltiga tecken när du skapar eller överför mappar. Visa en lista med tecken på [Skapa mappar i [!DNL Adobe Experience Manager Assets]](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/managing/manage-assets#creating-folders). Tecken som inte stöds i mappnamnet kan påverka vissa [!DNL Experience Manager]-användningsfall.

* **Bästa tillvägagångssätt för att undvika konflikter**: Om du vill undvika potentiella konflikter när du samarbetar med flera resurser går du till [Undvik redigeringskonflikter](using.md#adv-workflow-collaborate-avoid-conflicts).

* **Använd mappöverföring för stora, hierarkiska mappar**: Använd [!DNL Experience Manager]-datorprogrammet för att överföra stora mappar i stället för att använda Assets webbgränssnitt eller andra metoder. Programmet överför resurserna i bakgrunden med loggning och övervakning. Se [massöverföring av resurser](using.md#bulk-upload-assets).

* **Använd den senaste versionen**: Använd den senaste programversionen. Kontrollera alltid kompatibiliteten innan du installerar en ny programversion eller innan du uppgraderar till en nyare [!DNL Experience Manager]-version. Se [versionsinformation](release-notes.md).

* **Använd samma enhetsbeteckning**: Använd samma enhetsbeteckning i en organisation för att mappa till [!DNL Experience Manager] DAM. Om du vill visa resurser som placerats av andra användare måste sökvägarna vara desamma. Om du använder samma enhetsbeteckning säkerställs en konstant sökväg till DAM-resurser. Resurserna förblir placerade och tas inte bort även om olika enhetsbeteckningar används av olika användare.

* **Lägg märke till nätverket**: Nätverksprestanda är avgörande för prestandan för skrivbordsappen [!DNL Experience Manager]. Om du får ett långsammare svar på filöverföringar eller gruppåtgärder inaktiverar du de funktioner eller program som kan orsaka mycket nätverkstrafik.

* **Användningsexempel som inte stöds för skrivbordsappen**: Undvik att använda appen för resursmigrering eftersom den kräver planering och ytterligare verktyg. Den är inte heller lämplig för krävande DAM-åtgärder, som att flytta stora mappar, stora överföringar eller avancerade metadatasökningar. Använd den inte heller som synkroniseringsklient eftersom dess designprinciper och användningsmönster skiljer sig från synkroniseringsklienter som Microsoft OneDrive eller Adobe Creative Cloud desktop sync.

* **Timeout**: För närvarande har skrivbordsprogrammet inte ett konfigurerbart timeout-värde som kopplar från anslutningen mellan [!DNL Experience Manager]-servern och skrivbordsappen efter ett fast tidsintervall. När du överför stora resurser, och anslutningen får timeout efter en stund, försöker programmet överföra resursen några gånger genom att öka tidsgränsen för överföring. Det finns inget rekommenderat sätt att ändra standardinställningarna för timeout.

## Felsöka {#troubleshooting-prep}

Om du vill felsöka problem med skrivbordsprogram bör du känna till följande information. Där kan du också förmedla problemen bättre till Adobe kundsupport om du väljer att söka support.

### Plats för loggfiler {#check-log-files-v2}

Skrivbordsappen [!DNL Experience Manager] lagrar loggfilerna på följande platser beroende på operativsystemet:

I Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

På Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

När du överför många resurser och vissa filer inte kan överföras kan du läsa filen `backend.log` för att identifiera de misslyckade överföringarna.

>[!NOTE]
>
>När du arbetar med Adobe kundsupport på en supportförfrågan eller ett supportärende kan du bli ombedd att dela loggfilerna för att hjälpa kundsupport att förstå problemet. Arkivera hela mappen `Logs` och dela den med kundsupportkontakten.

### Ändra detaljnivå i loggfiler {#level-of-details-in-log}

Så här ändrar du detaljnivån i loggfiler:

1. Kontrollera att programmet inte körs.

1. I Windows:

   1. Öppna ett kommandofönster.

   1. Starta skrivbordsappen [!DNL Adobe Experience Manager] genom att köra kommandot:

   ```shell
   set AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe
   ```

   På Mac:

   1. Öppna ett terminalfönster.

   1. Starta skrivbordsappen [!DNL Adobe Experience Manager] genom att köra kommandot:

   ```shell
   AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app
   ```

Giltiga loggnivåer är DEBUG, INFO, WARN eller ERROR. Loggarnas utförlighet är högst i DEBUG och lägst i FEL.

### Aktivera felsökningsläge {#enable-debug-mode}

Om du vill felsöka kan du aktivera felsökningsläget och få mer information i loggarna.

>[!NOTE]
>
>Giltiga loggnivåer är DEBUG, INFO, WARN och ERROR. Loggarnas utförlighet är högst i DEBUG och lägst i FEL.

Så här använder du programmet i felsökningsläge på Mac:

1. Öppna ett terminalfönster eller en kommandotolk.

1. Starta skrivbordsappen [!DNL Experience Manager] genom att köra följande kommando:

   `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`.

Så här aktiverar du felsökningsläge i Windows:

1. Öppna ett kommandofönster.

1. Starta skrivbordsappen [!DNL Experience Manager] genom att köra följande kommando:

`AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe`.

### Lär känna versionen av [!DNL Adobe Experience Manager] för datorprogrammet {#know-app-version-v2}

Så här ser du versionsnumret:

1. Starta programmet.

1. Klicka på ellipserna i det övre högra hörnet, hovra över [!UICONTROL Help] och klicka sedan på [!UICONTROL About].

   Versionsnumret visas på den här skärmen.

### Rensa cache {#clear-cache-v2}

Utför följande steg:

1. Starta programmet och anslut till en instans av [!DNL Experience Manager].

1. Öppna programmets inställningar genom att klicka på ellipserna i det övre högra hörnet och välja [!UICONTROL Preferences].

1. Leta reda på posten som visar [!UICONTROL Current Cache Size]. Klicka på papperskorgsikonen bredvid elementet.

Så här rensar du cacheminnet manuellt:

>[!CAUTION]
>
>Dessa steg kan vara destruktiva. Om det finns lokala filändringar som inte har överförts till [!DNL Adobe Experience Manager], försvinner dessa ändringar.

Cacheminnet rensas genom att programmets cachekatalog, som finns i programmets inställningar, tas bort.

1. Starta programmet.

1. Öppna programmets inställningar genom att markera ellipserna i det övre högra hörnet och välja [!UICONTROL Preferences].

1. Observera värdet [!UICONTROL Cache Directory].

   I den här katalogen finns det underkataloger som heter efter de kodade [!DNL Adobe Experience Manager] slutpunkterna. Namnen är en kodad version av mål-URL:en [!DNL Adobe Experience Manager]. Om programmet till exempel har `localhost:4502` som mål är katalognamnet `localhost_4502`.

Om du vill rensa cachen tar du bort den kodade [!DNL Adobe Experience Manager]-slutpunktskatalogen. Om du tar bort hela katalogen som anges i inställningarna rensas cachen för alla instanser som har använts av programmet.

Att rensa [!DNL Adobe Experience Manager]-datorprogrammets cache är en preliminär felsökningsåtgärd som kan lösa flera problem. Rensa cacheminnet från appinställningarna. Se [ange inställningar](install-upgrade.md#set-preferences). Standardplatsen för cachemappen är:

## Kan inte se placerade resurser {#placed-assets-missing}

Om du inte kan se de resurser som du eller andra kreatörer har placerat i supportfilerna (till exempel INDD-filer) ska du kontrollera följande:

* Anslutning till servern. Smidig nätverksanslutning kan stoppa hämtningar av resurser.

* Filstorlek. Stora resurser tar längre tid att hämta och visa.

* Enhetliga brev. Om du eller någon annan medarbetare placerade resurserna när du mappade [!DNL Experience Manager] DAM till en annan enhetsbeteckning visas inte de placerade resurserna.

* Behörigheter. Kontakta [!DNL Experience Manager]-administratören om du har behörighet att hämta de placerade resurserna.

### Redigeringar av filer i skrivbordsappens användargränssnitt återspeglas inte direkt i [!DNL Adobe Experience Manager] {#changes-on-da-not-visible-on-aem}

Datorprogrammet [!DNL Adobe Experience Manager] låter användaren bestämma när alla redigeringar av en fil är slutförda. Beroende på storleken och komplexiteten hos en fil tar det lång tid att överföra den nya versionen av en fil tillbaka till [!DNL Adobe Experience Manager]. Programmet är utformat för att minimera antalet filöverföringar, i stället för att automatiskt överföra filer baserat på gissad redigering. Vi rekommenderar att användaren initierar överföringen av filen tillbaka till [!DNL Adobe Experience Manager] genom att välja att överföra en fils ändringar.

### Problem vid uppgradering till macOS {#issues-when-upgrading-on-macos}

Det kan ibland uppstå problem när du uppgraderar datorprogrammet [!DNL Experience Manager] på macOS. Äldre systemmappar för datorprogrammet [!DNL Experience Manager] orsakar dessa problem. Mapparna förhindrar att nya versioner av skrivbordsappen [!DNL Experience Manager] läses in korrekt. Följande mappar och filer kan tas bort manuellt för att åtgärda problemet.

Innan du utför följande steg drar du programmet `Adobe Experience Manager Desktop` från macOS-programmappen till papperskorgen. Öppna sedan terminalen, kör följande kommando och ange ditt lösenord när du uppmanas till det.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## Det går inte att överföra filer {#upload-fails}

Om du använder skrivbordsappen med [!DNL Experience Manager] 6.5.1 eller senare uppgraderar du S3- eller Azure-anslutningen till version 1.10.4 eller senare. Det löser problemet med filöverföringsfel som rör [OAK-8599](https://issues.apache.org/jira/browse/OAK-8599). Se [installationsanvisningar](install-upgrade.md#install-v2).

## [!DNL Experience Manager] anslutningsproblem för skrivbordsprogram {#connection-issues}

Om du har allmänna anslutningsproblem kan du få mer information om vad skrivbordsappen [!DNL Experience Manager] gör.

**Kontrollera begärandeloggen**

Skrivbordsappen [!DNL Experience Manager] loggar alla begäranden som skickas, tillsammans med varje begärans svarskod, i en dedikerad loggfil.

1. Öppna `request.log` i programmets loggkatalog för att se dessa begäranden.

1. Varje rad i loggen representerar antingen en begäran eller ett svar. Begäranden har ett `>`-tecken följt av den URL som begärdes. Svaren har ett `<`-tecken följt av svarskoden och URL:en som begärdes. Begäranden och svar kan matchas med varje rads GUID.

**Kontrollera förfrågningar som lästs in av programmets inbäddade webbläsare**

En majoritet av programmets begäranden finns i begärandeloggen. Men om det inte finns någon användbar information där kan det vara användbart att undersöka de förfrågningar som skickas av programmets inbäddade webbläsare.
Se [SAML-avsnittet](#da-connection-issue-with-saml-aem) för instruktioner om hur du visar dessa begäranden.

### SAML-inloggningsautentisering fungerar inte {#da-connection-issue-with-saml-aem}

Skrivbordsappen [!DNL Experience Manager] kan inte ansluta till din SSO-aktiverade (SAML) [!DNL Adobe Experience Manager]-distribution. Programmets design används för att anpassa variationerna och komplexiteten i SSO-anslutningar och processer. En installation kan dock kräva ytterligare felsökning.

Ibland dirigeras SAML-processen inte tillbaka till den ursprungligen begärda sökvägen. Eller så är den sista omdirigeringen till en annan värd än den som är konfigurerad i [!DNL Adobe Experience Manager]-datorprogrammet. Så här kontrollerar du att detta problem inte är fallet:

1. Öppna en webbläsare. Åtkomst till URL för `https://[aem_server]:[port]/content/dam.json`.

1. Logga in på distributionen [!DNL Adobe Experience Manager].

1. När inloggningen är klar tittar du på webbläsarens aktuella adress i adressfältet. Den ska exakt matcha den URL som ursprungligen angavs.

1. Verifiera också att allt före `/content/dam.json` matchar det [!DNL Adobe Experience Manager]-målvärde som konfigurerats i inställningarna för [!DNL Adobe Experience Manager] för skrivbordsappen.

**SAML-inloggningsprocessen fungerar korrekt enligt ovanstående steg, men användarna kan fortfarande inte logga in**

Fönstret i datorprogrammet [!DNL Adobe Experience Manager] som visar inloggningsprocessen är bara en webbläsare som visar [!DNL Adobe Experience Manager]-målinstansens webbanvändargränssnitt:

* Mac-versionen använder en [WebView](https://developer.apple.com/documentation/webkit/webview).

* I Windows-versionen används Chromium-baserad [CefSharp](https://cefsharp.github.io/).

Kontrollera att SAML-processen har stöd för dessa webbläsare.

Om du vill felsöka ytterligare kan du visa de exakta URL:er som webbläsaren försöker läsa in. Om du vill se den här informationen:

1. Följ instruktionerna för att starta programmet i [felsökningsläget](#enable-debug-mode).

1. Återskapa inloggningsförsöket.

1. Navigera till programmets [loggkatalog](#check-log-files-v2).

1. För Windows:

   1. Öppna&quot;aemcompanionlog.txt.&quot;

   1. Sök efter meddelanden som börjar med &quot;Inloggningsläsarens adress har ändrats till&quot;. Dessa poster innehåller även den URL som programmet har läst in.

   För Mac:

   1. I `com.adobe.aem.desktop-nnnnnnnn-nnnnnn.log` ersätter det nummer som finns i det senaste filnamnet **n**.

   1. Sök efter meddelanden som börjar med&quot;inläst bildruta&quot;. Dessa poster innehåller även den URL som programmet har läst in.

Om du tittar på den URL-sekvens som läses in kan det hjälpa till att felsöka i SAML:s slut för att avgöra vad som är fel.

### SSL-konfigurationsproblem {#ssl-config-v2}

De bibliotek som [!DNL Experience Manager]-datorprogrammet använder för HTTP-kommunikation använder strikta SSL-regler. Ibland kan en anslutning fungera med en webbläsare, men misslyckas när du använder datorprogrammet [!DNL Experience Manager]. Installera det saknade mellanliggande certifikatet i Apache om du vill konfigurera SSL korrekt. Se [Så här installerar du ett mellanliggande CA-certifikat i Apache](https://access.redhat.com/solutions/43575).

De bibliotek som [!DNL Experience Manager]-datorprogrammet använder för HTTP-kommunikation använder strikt SSL-kontroll. Det kan därför finnas instanser där SSL-anslutningar som lyckas via en webbläsare misslyckas med skrivbordsappen [!DNL Adobe Experience Manager]. Resultatet är bra eftersom det uppmuntrar till korrekt konfigurering av SSL och ökar säkerheten, men det kan vara frustrerande när programmet inte kan ansluta.

I det här fallet rekommenderar vi att du använder ett verktyg för att analysera serverns SSL-certifikat och identifiera problem så att de kan korrigeras. Det finns webbplatser som inspekterar serverns certifikat genom att ange dess URL.

Som en tillfällig åtgärd är det möjligt att inaktivera strikt SSL-tvång i datorprogrammet [!DNL Adobe Experience Manager]. Detta tillvägagångssätt är inte en rekommenderad långsiktig lösning, eftersom det minskar säkerheten genom att dölja grundorsaken till felaktigt konfigurerad SSL. Så här inaktiverar du strikt tvingande:

1. Använd valfri redigerare för att redigera programmets JavaScript-konfigurationsfil, som finns (som standard) på följande platser (beroende på operativsystem):

   På Mac: `/Applications/Adobe Experience Manager Desktop.app/Contents/Resources/javascript/lib-smb/config.json`

   I Windows: `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop\javascript\config.json`

1. Leta reda på följande avsnitt i filen:

   ```shell
   ...
   "assetRepository": {
       "options": {
   ...
   ```

1. Ändra avsnittet genom att lägga till `"strictSSL": false` enligt följande:

   ```shell
   ...
   "assetRepository": {
       "options": {
           "strictSSL": false,
   ...
   ```

1. Spara filen och starta om datorprogrammet [!DNL Adobe Experience Manager].

### Inloggningsproblem vid växling till en annan server {#cannot-login-cookies-issue}

När du har använt en [!DNL Experience Manager]-server och försöker ändra anslutningen till en annan server kan du råka ut för inloggningsproblem. Det beror på att gamla cookies stör den nya autentiseringen. Ett alternativ på huvudmenyn till [!UICONTROL Clear Cookies] hjälper. Logga ut från den aktuella sessionen i appen och välj [!UICONTROL Clear Cookies] innan du fortsätter med anslutningen.

![Rensa cookies när du byter server](assets/main_menu_logout_da2.png)

## Appen svarar inte {#unresponsive}

I vissa fall kan programmet inte svara, bara visa en vit skärm eller visa ett fel längst ned i gränssnittet utan några alternativ i gränssnittet. Prova följande i den ordning du vill:

* Högerklicka på programgränssnittet och klicka på **[!UICONTROL Refresh]**.
* Avsluta programmet och öppna det igen.

I båda metoderna startar programmet i rotmappen DAM.

## Dölj utgångna resurser {#hide-expired-assets}

När du bläddrar bland resurser i användargränssnittet [!DNL Experience Manager] visas inte de utgångna resurserna. Administratörer kan konfigurera inställningar för att förhindra visning, sökning och hämtning av utgångna resurser när de bläddrar från skrivbordsappen och Asset Link. Om du gör det kan du vara säker på att utgångna resurser inte är tillgängliga under dessa åtgärder. Konfigurationen fungerar för alla användare, oavsett administratörsbehörighet.

* [Konfiguration i Experience Manager 6.5 för att dölja utgångna resurser](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/managing/manage-assets#hide-expired-assets-via-acp-api).
* [Konfiguration i Experience Manager as a Cloud Service för att dölja utgångna resurser](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets#hide-expired-assets-via-acp-api).

<!--
### Need additional help with [!DNL Experience Manager] desktop app {#additional-help}

Create Jira ticket with the following information:

* Use `DAM - Companion App` as the [!UICONTROL Component].

* Detailed steps to reproduce the issue in [!UICONTROL Description].

* DEBUG level logs that were captured while reproducing the issue.

* Target Experience Manager version.

* Operating system version.

* [!DNL Adobe Experience Manager] desktop app version. To know your app version, see [finding the desktop app version](#know-app-version-v2).
-->

>[!MORELIKETHIS]
>
>* [Kända fel](release-notes.md#known-issues-v2)
>* [Undvik att redigera konflikter](using.md#adv-workflow-collaborate-avoid-conflicts)
