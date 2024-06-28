---
title: Installera och konfigurera datorprogrammet v1.10
description: Installera och konfigurera [!DNL Experience Manager] datorprogram version 1.10 att arbeta med [!DNL Assets] servrar och mappa resurser som ska monteras som en enhet på skrivbordet.
exl-id: 7f3bdfb1-d345-4e48-b020-6e06531f46f2
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# Installera och konfigurera [!DNL Experience Manager] datorprogram v1.10 {#install-and-configure-aem-desktop-app}

Använda [!DNL Experience Manager] datorprogrammet, resurserna i [!DNL Experience Manager] är lättillgängliga på din lokala dator och kan användas i alla skrivbordsprogram. Assets kan visas i Mac Finder eller Utforskaren i Windows, redigeras i skrivbordsappar och ändringarna sparas i [!DNL Experience Manager], skapar en ny version vid överföring.

Integreringen gör det möjligt för olika roller att hantera resurser centralt inom organisationen i Assets, få tillgång till dem i Creative Cloud och andra program samt enkelt följa olika standarder, inklusive branding.

Använd [!DNL Experience Manager] datorprogram,

* Se till att [!DNL Experience Manager] serverversionen är kompatibel med [!DNL Experience Manager] datorprogram. Se [kompatibilitetsmatris](release-notes-of-v1.md#compatibilitymatrix).

* Hämta och installera programmet.

* Testa anslutningen med några resurser. Se [Få åtkomst till och öppna resurser på datorn](use-app-v1.md#openondesktop).

## Systemkrav, krav och nedladdningslänkar {#system-requirements-prerequisites-and-download-links}

Mer information finns i [[!DNL Experience Manager] versionsinformation för skrivbordsapp](release-notes-of-v1.md).

## Installera och anslut appen till [!DNL Experience Manager] server {#install-and-connect-aem-desktop-app-to-aem-server}

Mer information finns i [Installera och ansluta [!DNL Experience Manager] datorprogram till [!DNL Experience Manager] server](use-app-v1.md#installandconnect).

>[!NOTE]
>
>Endast en instans av [!DNL Experience Manager] datorprogrammet kan installeras och vara aktivt i taget.

## Filhantering {#file-handling}

När du ändrar en fil från en nätverksresursplats som monterats av skrivbordsprogrammet, sparas filerna på den platsen i två faser. I den första fasen sparas en fil lokalt. Användaren kan spara filen och fortsätta arbeta med den utan att vänta på att överföringen ska slutföras.

Under den andra fasen överför skrivbordsappen den uppdaterade filen till [!DNL Experience Manager] efter en fördefinierad fördröjning (t.ex. 30s). Den här åtgärden utförs i bakgrunden. Använd alternativet Visa resursstatus för att visa överföringsåtgärdens status.

1. Överför en mediefil till Assets.

1. Klicka på [!DNL Experience Manager] ikon för datorprogram från verktygsfältet.

1. Välj alternativet Visa resursstatus på menyn.

1. Granska överföringsåtgärdens status i dialogrutan.

>[!NOTE]
>
>[!DNL Experience Manager] datorprogrammet kan hantera resurser som är upp till 40 GB stora.

## Ansluta till en [!DNL Experience Manager] instans bakom en Dispatcher {#connect-to-an-aem-instance-behind-a-dispatcher}

Metoderna copy och move i Assets API kräver att följande rubriker skickas till [!DNL Experience Manager]:

* X-Destination
* X-djup
* X-Overwrite

[!DNL Experience Manager] skrivbordet ansluts till [!DNL Experience Manager] med en URL som innehåller standardporten. Därför är `virtualhosts` inställningen i Dispatcher-konfigurationen ska inkludera standardportnumret. Mer information om `virtualhosts` konfiguration, se [identifiera virtuella värdar](https://experienceleague.adobe.com/en/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#identifying-virtual-hosts-virtualhosts).

Mer information om hur du konfigurerar Dispatcher att skicka genom dessa ytterligare rubriker finns i [Ange HTTP-huvuden](https://experienceleague.adobe.com/en/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#specifying-the-http-headers-to-pass-through-clientheaders).

### Stöd för proxy {#proxy-support}

The [!DNL Experience Manager] datorprogrammet använder systemets fördefinierade proxy för att ansluta till Internet via HTTPS. Appen kan bara ansluta med en nätverksproxy som inte kräver extra autentisering.

Om du konfigurerar eller ändrar proxyserverinställningarna för Windows (Internetalternativ > LAN-inställningar) startar du om [!DNL Experience Manager] för att ändringarna ska börja gälla.

>[!NOTE]
>
>Proxykonfigurationen används bara när du startar skrivbordsprogrammet. Stäng och starta om programmet för att ändringarna ska börja gälla.

Om din proxy kräver autentisering kan IT-teamet tillåta att Experience Manager Assets URL:en i proxyserverinställningarna tillåter att programtrafiken passerar igenom.

## Anpassa dialogrutan Resursinformation {#customize-the-asset-info-dialog}

Du kan anpassa dialogrutan Resursinformation genom att täcka över en eller båda av dessa komponenter:

* Gränssnittssidan för Granite finns på `/libs/dam/gui/content/assets/moreinfo`.

* HTML `/css/javascript` komponent vid `/libs/dam/gui/components/admin/moreinfo`.

Vilken komponent som överlappas beror på typen av anpassning. Om du vill ändra vilka komponenter som visas som en del av dialogrutan Resursinformation ska du täcka över användargränssnittssidan för Granite. Om du vill ändra HTML, CSS eller JavaScript-innehåll i dialogrutan ska du täcka över HTML-komponenten.

## Hantera cache {#manage-cache}

I Windows finns cacheminnet på `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`, där är en kodad version av [!DNL Experience Manager] värddator konfigurerad i datorprogrammet. Till exempel: `http://localhost:4502` visas som `http%3A%2F%2Flocalhost%3A4502%2F`.

På macOS X finns en liknande katalog på `~/Library/Group Containers/group.com.adobe.aem.desktop/cache`.

### Alternativ i appen för att hantera cache {#in-app-option-to-manage-cache}

Du kan styra hur mycket diskutrymme som finns tillgängligt för lokal cachelagring. Artefakterna från Assets-servern cachas lokalt för en smidigare upplevelse. Du kan ändra standardinställningarna så att de passar dina behov. Du kan även rensa cacheminnet för att hämta alla resurser på nytt. Om du vill ange önskade alternativ klickar du på programikonen och klickar på **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**. ****

>[!NOTE]
>
>När du rensar cachen bevaras ändringarna som inte sparats. Alla resurser som inte har checkats in i [!DNL Experience Manager] servern behålls och tas inte bort.

### Ändra platsen för cachen i Windows {#change-location-of-cache-on-windows}

Standardplatsen för cacheminnet för [!DNL Experience Manager] är följande:

* I Windows `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`.

* I MAC `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`.

The `EncodedAEMEndpoint` är programmets konfigurerade [!DNL Experience Manager] URL för slutpunkt. Värdet är en kodad version av mål-URL:en för [!DNL Experience Manager] server. Om programmet till exempel har som mål `http://localhost:4502`, är katalognamnet `http%3A%2F%2Flocalhost%3A4502`. Windows-sökvägen till cachekatalogen i detta exempel är `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502`.

Om du vill peka programmet mot en annan mapp eller enhet redigerar du programmets konfigurationsfil.

1. Navigera till programmets installationskatalog. Standardplatsen i Windows är `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.

1. Redigera `Adobe Experience Manager Desktop.exe.config` med en textredigerare.

   Administratörsbehörighet krävs för att spara ändringar i den här filen.

1. Sök efter strängen ProxyCacheRoot. Du ser att dess värde är inställt på cacheplatsen `%LocalAppData%\Adobe\AssetsCompanion\Cache`. Ändra bara det här värdet till en giltig sökväg.

   >[!NOTE]
   >
   >Appen skapar automatiskt en *&lt;encoded aem=&quot;&quot; endpoint=&quot;&quot;>* underkatalog. Detta beteende kan inte konfigureras.

>[!MORELIKETHIS]
>
* Titta på en [Introduktion till [!DNL Experience Manager] datorprogram](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app) (5 minuter, 43 sekunder).
* [Använd [!DNL Experience Manager] datorprogram](use-app-v1.md).
* [Felsökning [!DNL Experience Manager] datorprogram](troubleshoot-app-v1.md).
