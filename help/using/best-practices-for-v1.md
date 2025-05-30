---
title: Bästa praxis för datorprogram v1.10
description: Viktiga funktioner och rekommenderad användning av  [!DNL Adobe Experience Manager] datorprogrammet version 1.10.
exl-id: 5de06b33-c05c-47eb-b884-408b6f9afc94
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '1651'
ht-degree: 0%

---

# AEM praxis för datorprogram v1.10 {#aem-desktop-app-best-practices}

## Ökning {#overview}

Skrivbordsappen [!DNL Adobe Experience Manager] länkar din DAM-lösning (Digital Asset Management) till skrivbordet så att du kan öppna de filer som är tillgängliga i AEM webbgränssnitt direkt på skrivbordet. Om du har sparat en resurs från skrivbordet överförs den till AEM på lämplig plats.

AEM program eliminerar riskerna för att du uppdaterar felaktiga lokala kopior eller uppdaterar fel resurs i AEM. Skrivbordsappens lättanvända arbetsflöde aktiveras med hjälp av nätverksdelningsteknik från operativsystemen på datorn.

Datorprogrammet monterar AEM Assets-databasen som en nätverksresurs på skrivbordet. Därför ser mapparna och filerna ut som om de var lokala. Vi rekommenderar dock inte att du utför digitala resurshanteringsåtgärder direkt från skrivbordet i den monterade nätverksresursen i Finder eller Utforskaren. I stället rekommenderar Adobe att du använder AEM Assets webbgränssnitt för att utföra åtgärder, som att kopiera eller flytta ett stort antal resurser.

>[!NOTE]
>
>Innan du läser det här dokumentet kan du gå igenom den övergripande [AEM och Creative Cloud ](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/administer/aem-cc-integration-best-practices) -integreringen för att få en översikt över ämnet på en högre nivå.

## AEM datorprogramarkitektur {#aem-desktop-app-architecture}

AEM använder nätverksresurser för WebDAV (Windows) eller SMB (Mac) för att montera nätverksresurser. Den monterade nätverksresursen är endast lokal. AEM datorprogrammet fångar upp anropen (öppna, läsa, skriva) och erbjuder ytterligare lokal cachelagring. Det översätter fjärranrop till AEM Assets-servern för att optimera AEM HTTP-begäranden. I följande diagram visas arkitekturen för AEM datorprogram.

![AEM datorprogramarkitektur](assets/arch_v1.png)

*Bild: skrivbordsappens arkitektur*

När en fil sparas säkerställer den extra cachningen vid skrivning att den lagras lokalt först, så att användaren slipper vänta på nätverksöverföringen. Efter en fördefinierad fördröjning (30 sekunder) överförs filen till AEM i bakgrunden och resursen överförs sedan till AEM. AEM datorprogram har ett gränssnitt för övervakning av status för filöverföringar i bakgrunden.

## Rekommenderad användning av AEM {#recommended-use-of-aem-desktop-app}

De viktigaste funktionerna i AEM program:

* **Öppnar filer från AEM Assets webbgränssnitt på skrivbordet**. I webbgränssnittet kan du visa resurser på skrivbordet (i Finder, Utforskaren) eller öppna en resurs med ett skrivbordsprogram.

* **Checka ut och checka in**. Assets kan checkas ut för redigering och markeras som låst för användaren i AEM Assets. Efter redigeringen kan resursen checkas in för att låsa upp den.

* **Spara ändringar i filer**. Alla ändringar som du sparar i filen i nätverksresursen överförs automatiskt till AEM och en ny version skapas.

* **Montera länkade resurser i andra dokument**. I program som Creative Cloud ([!DNL Adobe Photoshop], [!DNL Adobe InDesign] och [!DNL Adobe Illustrator]) kan du montera en extern fil som en länk. Du kan till exempel montera en InDesign i ett bilddokument. I det här fallet kan du med hjälp av nätverksresursen bläddra bland och välja resurser från AEM för placering. Det går även att placera länkade filer i vissa program som inte är Adobe, till exempel MS® Office.

* **Referensupplösning i AEM**. Om både de monterade filerna och huvudfilerna med länken lagras i AEM kan det automatiskt tillhandahålla serversidesinformation om resursreferenserna.

* **Åtkomst till resursen från skrivbordet**. I den monterade nätverksresursen finns en sammanhangsbaserad meny med en [!UICONTROL More Info]-dialogruta (större förhandsgranskning, nyckelmetadata) och möjlighet att öppna en resurs i AEM.

* **Överför stora, hierarkiska mappar i bulk**. Om du använder alternativet **Skapa** > **Mappöverföring** i AEM gränssnitt för att överföra resurser, överför det AEM skrivbordsprogrammet den valda mapphierarkin till AEM i bakgrunden. Överföringsförloppet övervakas med ett dedikerat användargränssnitt i skrivbordsappen.

## Felaktig användning AEM datorprogrammet {#inappropriate-use-of-aem-desktop-app}

* Använd inte det AEM datorprogrammet för att hantera resurser från skrivbordet. AEM skrivbordsapp skapades inte som ersättning för nätverksenheter. Använd följande funktioner i stället:

   * AEM Assets webbgränssnitt för hantering av digitala resurser (söka efter eller dela resurser, metadata samt kopiera eller flytta).

   * AEM datorprogrammet [!UICONTROL Folder Upload] för att överföra stora, hierarkiska mappar.

* Behandla inte AEM datorprogram som en&quot;datorsynkroniseringsklient&quot; för AEM Assets. Den största fördelen med AEM datorprogram här är att det ger&quot;virtuell&quot; åtkomst till hela databasen, och program för datorsynkronisering synkroniserar vanligtvis bara resurser som tillhör en användare. AEM datorprogram erbjuder viss nivå av cachelagring och bakgrundsuppladdning, men fungerar ändå mycket annorlunda än vanliga Sync-program, som Adobe Creative Cloud datorprogram eller Microsoft OneDrive.

* Använd inte nätverksenheter AEM skrivbordsappen för att spara resurser ofta. Alla sparåtgärder överförs till AEM Assets. Därför är det opraktiskt att utföra intensiva redigeringsåtgärder direkt i den monterade AEM Assets-databasen. När du redigerar en resurs direkt i den monterade databasen krymper resursens tidslinje med irrelevanta versioner och lägger till ytterligare omkostnader på servern.

* Använd inte AEM datorprogram för att migrera stora mängder data från en AEM till en annan. Se [Migreringshandboken](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/administer/assets-migration-guide) för att planera och köra resursmigreringar. Datorprogrammet [stöder däremot massöverföring](use-app-v1.md#bulkupload) av många resurser för första gången i [!DNL Adobe Experience Manager].

## Recommendations för utvalda användningsområden {#recommendations-for-selected-use-cases}

### Tillgång till material för kreativa användare {#access-to-assets-for-creative-users}

AEM datorprogram ger virtuell åtkomst till hela DAM-databasen - och det kan vara komplicerat för de kreativa användarna på skrivbordet att hitta och komma åt rätt resurser på skrivbordet. Använd de här bästa sätten för att förenkla för dem.

* Använd samarbetsfunktionerna i AEM Assets webbgränssnitt för att ge mer direkt åtkomst till rätt material för den kreativa användaren. Några av dem är att dela mappar eller samlingar, tillhandahålla smarta samlingar (sparade sökningar) eller skicka meddelanden med pekare till rätt resurser. Den kreativa användaren kan sedan använda skrivbordsåtgärder i webbgränssnittet för snabb åtkomst till dessa resurser på sin dator.

* Tänk på rätt behörigheter för materialet (åtkomstkontroll) för att förenkla visningen av DAM-databasen för de kreativa användarna, och begränsa i princip åtkomsten till endast de resurser de behöver eller är intresserade av:

   * Vissa områden som inte är relevanta för de kreativa användarna kan nekas användargrupperna att ta bort dem från sina vyer, även på skrivbordet.

   * De flesta resurser i DAM är slutgiltiga och är inte avsedda att ändras - sådana resurser bör vara skrivskyddade för de kreativa användarna.

   * Endast resurser som kräver ändringar eller retuschering ska vara skrivaktiverade för de kreativa användarna. Vissa organisationer använder AEM projekt och de mappar de skapar för att lagra resurser som fortfarande kan ändras.

### Söka efter resurser {#searching-assets}

Så här söker du efter en fil som du vill öppna på skrivbordet:

* Använd AEM Assets webbgränssnitt för att hitta resursen. Det är inte bara sökning i AEM Assets kraftfulla funktioner (sökfaktorer, sparade sökningar), utan även andra funktioner för att hitta rätt resurs. Detta inkluderar ytterligare filter, som möjligheten att söka efter resurser baserat på status (godkännande, förfallodatum), samlingar, uppgifter, meddelanden och att dela mappar/samlingar med andra användare/grupper.

* När du har hittat resursen använder du skrivbordsåtgärder i AEM för att komma åt resursen på skrivbordet.

### Uppdatera resurser som har öppnats med AEM datorprogram {#updating-assets-opened-using-aem-desktop-app}

Om du redigerar en resurs direkt på den plats som mappats från AEM Assets till en lokal nätverksresurs, överförs resursen till AEM varje gång du sparar den på skrivbordet. Dessutom skapar AEM en version och skapar återgivningar.

Om en resurs som lagras i AEM behöver uppdateras:

* För **mindre uppdateringar**, till exempel mindre retuscheringsbegäranden i godkännandeprocessen:

   * Checka ut filen och öppna den på skrivbordet.

   * Uppdatera filen.

   * Spara den uppdaterade versionen. Resursen uppdateras och tidslinjen visar den ursprungliga versionen för jämförelse.

* För **större uppdateringar**, till exempel en ändringsbegäran som kräver en liten kreativ PIA-cykel:

   * Använd alternativet Visa för att öppna lämplig mapp på skrivbordet.

   * Kopiera filen till en WIP-mapp utanför den mappade AEM Assets-resursen (kopiera till exempel filen till en mapp som synkroniseras med Adobe Creative Cloud-datorprogrammet).

   * Arbeta med filen och spara den regelbundet. Ändringarna sparas inte i AEM Assets.

   * När redigeringarna är klara flyttar, kopierar eller sparar du filen som mappats från AEM för att överföra den som en ny version.

## Nätverksprestanda {#network-performance}

En bra användarupplevelse med AEM datorprogram kräver stabil nätverksanslutning och en välanpassad server, särskilt för att överföra och uppdatera resurser. Rekommendationerna är till för nätverks-/IT-team i organisationer.

### Nätverkshändelser {#network-considerations}

Om du vill ha mer information om de bästa sätten att använda AEM Assets nätverkskonfiguration går du till dokumentet [Så här gör du för att migrera resurser i grupp](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/administer/assets-migration-guide). Några av de viktiga aspekter som hjälper användarna att optimera upplevelsen av AEM program är:

* **Använd en korrekt konfigurerad Dispatcher**. Använd AEM Dispatcher för ytterligare säkerhet och se till att den är konfigurerad för [AEM anslutning till skrivbordsappen AEM bakom en Dispatcher](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher)

* **Spara bandbredd**. Överväg att stänga av ikonförhandsvisningen i Finder i Mac när du bläddrar i den monterade databasen med Finder. Finder begär att varje fil ska generera en förhandsgranskning och gör att skrivbordsappen hämtar och cachelagrar resursen lokalt. När du sparar bandbredd minskas även användarupplevelsen för användarna på skrivbordet, så du bör göra det när du arbetar i databaser med stora resurser eller begränsad bandbredd.

>[!NOTE]
>
>Om du vill inaktivera förhandsvisningar av ikoner går du till [!UICONTROL View], väljer [!UICONTROL View Options] och avmarkerar sedan alternativet [!UICONTROL Show icon preview] i Finder. Detta fungerar bara för den aktuella mappen. Om du vill göra den till standard klickar du på alternativet [!UICONTROL Use as default] i samma dialogruta.

### Optimera serverprestanda {#optimizing-server-performance}

Om du vill veta hur AEM Assets-servern ska optimeras för prestanda går du till [AEM Assets Performance Tuning Guide](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/administer/performance-tuning-guidelines). Några av de viktiga aspekterna av serverprestanda för AEM datorprogram är att optimera arbetsflödeskonfigurationen så att den fungerar bra för överföringar av resurser:

* **Mer prestandaöverföring av resurser**. Konfigurera arbetsflödesmodellen [AEM Resursuppdatering så att den blir tillfällig](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/administer/performance-tuning-guidelines).

* **Begränsa serverns CPU för överföringar**. Se till att parametern för maximala parallella arbetsflödesjobb är korrekt inställd så att överföringar inte tar bort hela processorn.
