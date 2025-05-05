---
title: Installera och konfigurera datorprogrammet v1.10
description: Installera och konfigurera  [!DNL Experience Manager] skrivbordsappversion 1.10 så att den fungerar med  [!DNL Assets] servrar och mappa resurserna som ska monteras som en enhet på skrivbordet.
exl-id: 7f3bdfb1-d345-4e48-b020-6e06531f46f2
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# Installera och konfigurera [!DNL Experience Manager]-datorprogrammet v1.10 {#install-and-configure-aem-desktop-app}

Med skrivbordsappen [!DNL Experience Manager] är resurserna i [!DNL Experience Manager] enkelt tillgängliga på ditt lokala skrivbord och kan användas i alla skrivbordsprogram. Assets kan visas i Mac Finder eller Utforskaren i Windows, redigeras i skrivbordsappar och ändringar sparas tillbaka i [!DNL Experience Manager], vilket skapar en ny version vid överföringen.

Integreringen gör det möjligt för olika roller att hantera resurser centralt inom organisationen i Assets, få tillgång till dem i Creative Cloud och andra program samt enkelt följa olika standarder, inklusive branding.

Om du vill använda datorprogrammet [!DNL Experience Manager]

* Kontrollera att serverversionen [!DNL Experience Manager] är kompatibel med skrivbordsappen [!DNL Experience Manager]. Se [kompatibilitetsmatrisen](release-notes-of-v1.md#compatibilitymatrix).

* Hämta och installera programmet.

* Testa anslutningen med några resurser. Se [Få åtkomst till och öppna resurser på skrivbordet](use-app-v1.md#openondesktop).

## Systemkrav, krav och nedladdningslänkar {#system-requirements-prerequisites-and-download-links}

Mer information finns i [[!DNL Experience Manager] versionsinformationen för skrivbordsappen](release-notes-of-v1.md).

## Installera och anslut appen till [!DNL Experience Manager]-servern {#install-and-connect-aem-desktop-app-to-aem-server}

Mer information finns i [Installera och ansluta [!DNL Experience Manager] datorprogrammet till [!DNL Experience Manager] server](use-app-v1.md#installandconnect).

>[!NOTE]
>
>Endast en instans av [!DNL Experience Manager]-datorprogrammet kan installeras och vara aktiv åt gången.

## Filhantering {#file-handling}

När du ändrar en fil från en nätverksresursplats som monterats av skrivbordsprogrammet, sparas filerna på den platsen i två faser. I den första fasen sparas en fil lokalt. Användaren kan spara filen och fortsätta arbeta med den utan att vänta på att överföringen ska slutföras.

I den andra fasen överför skrivbordsappen den uppdaterade filen till [!DNL Experience Manager]-servern efter en fördefinierad fördröjning (till exempel 30-tal). Den här åtgärden utförs i bakgrunden. Använd alternativet Visa resursstatus för att visa överföringsåtgärdens status.

1. Överför en mediefil till Assets.

1. Klicka på ikonen [!DNL Experience Manager] för skrivbordsappen i verktygsfältet.

1. Välj alternativet Visa resursstatus på menyn.

1. Granska överföringsåtgärdens status i dialogrutan.

>[!NOTE]
>
>Skrivbordsappen [!DNL Experience Manager] kan hantera resurser som är upp till 40 GB stora.

## Anslut till en [!DNL Experience Manager]-instans bakom en Dispatcher {#connect-to-an-aem-instance-behind-a-dispatcher}

Kopierings- och flyttningsmetoderna i Assets API kräver att följande ytterligare rubriker skickas till [!DNL Experience Manager]:

* X-Destination
* X-djup
* X-Overwrite

Skrivbordet [!DNL Experience Manager] ansluter till [!DNL Experience Manager] med en URL som innehåller standardporten. Inställningen `virtualhosts` i Dispatcher-konfigurationen bör därför innehålla standardportnumret. Mer information om konfigurationen av `virtualhosts` finns i [Identifiera virtuella värdar](https://experienceleague.adobe.com/en/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#identifying-virtual-hosts-virtualhosts).

Mer information om hur du konfigurerar Dispatcher att skicka genom dessa ytterligare rubriker finns i [Ange HTTP-rubriker](https://experienceleague.adobe.com/en/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#specifying-the-http-headers-to-pass-through-clientheaders).

### Stöd för proxy {#proxy-support}

Skrivbordsappen [!DNL Experience Manager] använder systemets fördefinierade proxy för att ansluta till Internet via HTTPS. Appen kan bara ansluta med en nätverksproxy som inte kräver extra autentisering.

Om du konfigurerar eller ändrar proxyserverinställningarna för Windows (Internetalternativ > LAN-inställningar) startar du om datorprogrammet [!DNL Experience Manager] så att ändringarna börjar gälla.

>[!NOTE]
>
>Proxykonfigurationen används bara när du startar skrivbordsprogrammet. Stäng och starta om programmet för att ändringarna ska börja gälla.

Om din proxy kräver autentisering kan IT-teamet tillåta att Experience Manager Assets URL:en i proxyserverinställningarna tillåter att programtrafiken passerar igenom.

## Anpassa dialogrutan Resursinformation {#customize-the-asset-info-dialog}

Du kan anpassa dialogrutan Resursinformation genom att täcka över en eller båda av dessa komponenter:

* Gränssnittssidan för Granite på `/libs/dam/gui/content/assets/moreinfo`.

* HTL `/css/javascript`-komponenten vid `/libs/dam/gui/components/admin/moreinfo`.

Vilken komponent som överlappas beror på typen av anpassning. Om du vill ändra vilka komponenter som visas som en del av dialogrutan Resursinformation ska du täcka över användargränssnittssidan för Granite. Om du vill ändra HTML, CSS eller JavaScript-innehåll i dialogrutan ska du täcka över HTML-komponenten.

## Hantera cache {#manage-cache}

I Windows finns cachen på `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`, där är en kodad version av värddatorn [!DNL Experience Manager] som konfigurerats i skrivbordsprogrammet. `http://localhost:4502` visas till exempel som `http%3A%2F%2Flocalhost%3A4502%2F`.

På macOS X finns en liknande katalog på `~/Library/Group Containers/group.com.adobe.aem.desktop/cache`.

### Alternativ i appen för att hantera cache {#in-app-option-to-manage-cache}

Du kan styra hur mycket diskutrymme som finns tillgängligt för lokal cachelagring. Artefakterna från Assets-servern cachas lokalt för en smidigare upplevelse. Du kan ändra standardinställningarna så att de passar dina behov. Du kan även rensa cacheminnet för att hämta alla resurser på nytt. Om du vill ange önskade alternativ klickar du på programikonen och sedan på **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**. **&#x200B;**

>[!NOTE]
>
>När du rensar cachen bevaras ändringarna som inte sparats. Alla resurser som inte har checkats in på servern [!DNL Experience Manager] behålls och tas inte bort.

### Ändra platsen för cachen i Windows {#change-location-of-cache-on-windows}

Standardplatsen för cacheminnet för datorprogrammet [!DNL Experience Manager] är följande:

* I Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`.

* `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint` i Mac.

`EncodedAEMEndpoint` är programmets konfigurerade [!DNL Experience Manager]-slutpunkts-URL. Värdet är en kodad version av mål-URL:en för servern [!DNL Experience Manager]. Om programmet till exempel har `http://localhost:4502` som mål är katalognamnet `http%3A%2F%2Flocalhost%3A4502`. Windows-sökvägen till cachekatalogen i detta exempel är `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502`.

Om du vill peka programmet mot en annan mapp eller enhet redigerar du programmets konfigurationsfil.

1. Navigera till programmets installationskatalog. Standardplatsen i Windows är `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.

1. Redigera filen `Adobe Experience Manager Desktop.exe.config` med en textredigerare.

   Administratörsbehörighet krävs för att spara ändringar i den här filen.

1. Sök efter strängen ProxyCacheRoot. Du ser att dess värde är inställt på cacheplatsen `%LocalAppData%\Adobe\AssetsCompanion\Cache`. Ändra bara det här värdet till en giltig sökväg.

   >[!NOTE]
   >
   >Programmet skapar automatiskt en *&lt;Encoded AEM Endpoint>*-underkatalog. Detta beteende kan inte konfigureras.

>[!MORELIKETHIS]
>
>* Titta på en [introduktion till [!DNL Experience Manager] skrivbordsappen](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app) (5 minuter, 43 sekunder).
>* [Använd [!DNL Experience Manager] datorprogrammet](use-app-v1.md).
>* [Felsökning [!DNL Experience Manager] datorprogrammet](troubleshoot-app-v1.md).
