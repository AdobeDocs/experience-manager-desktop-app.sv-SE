---
title: "[!DNL Adobe Experience Manager] versionsinformation för skrivbordsappen"
description: Versionsinformation, förbättringar, nya funktioner, kompatibilitet och hämtningslänkar för  [!DNL Adobe Experience Manager] skrivbordsappen.
mini-toc-levels: 1
feature: Desktop App,Release Information
exl-id: e058e7a2-fcc8-4ad1-899e-20695db6bc72
source-git-commit: 19f059875a7519cf28628fd801662da7243b077b
workflow-type: tm+mt
source-wordcount: '1955'
ht-degree: 0%

---

# Versionsinformation för [!DNL Adobe Experience Manager]-datorprogrammet {#release-notes-v2}

Versionsinformationen för den senaste versionen av datorprogrammet, version 2.3.1, visas nedan. Lanseringsdatumet är 25 juli 2024.

Den senaste versionen av skrivbordsappen innehåller följande felkorrigeringar och förbättringar:

* Det nya installationsprogrammet för Enterprise Windows installerar programmet under Program Files.
* Stöd för **grundläggande autentisering** under AEM- och SSO-inloggningar.
* Konfigurerbart antal resurser som tillåts under överföring.

**De [!DNL Experience Manager] versioner** som stöds är:

* [!DNL Experience Manager] som [!DNL Cloud Service]. Se [versionsinformation](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/home).
* [!DNL Experience Manager] 6.5.0 eller senare, på Adobe Managed Services (AMS) eller On-Premise. Se [versionsinformation för Service Pack](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/release-notes/release-notes).

Datorprogrammet [!DNL Adobe Experience Manager] är tillgängligt för följande **operativsystem**:

* macOS X 10.14 eller senare, med de senaste felkorrigeringarna.
* Windows 10 med de senaste servicepaketen och felkorrigeringarna.

Två versioner av Windows-installationsprogrammet finns för AEM version 2.3.1 och senare av skrivbordsappen. Det grundläggande installationsprogrammet installerar det AEM datorprogrammet under användarens lokala App Data-katalog. Adobe rekommenderar att de flesta användare installerar programmet. Det finns också ett installationsprogram för Enterprise Windows, som installerar AEM skrivbordsapp i katalogen med delade programfiler. Dessa två installationsprogram installerar samma version av AEM skrivbordsapp, utan några skillnader i funktionalitet.

**URL:erna för hämtning** för operativsystem som stöds är:

| Operativsystem | [!DNL Experience Manager] som en [!DNL Cloud Service] | [!DNL Experience Manager] 6.x |
|---|---|---|
| macOS (v2.3.1) | [Hämta länk](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-osx-x64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081954149%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=mwSX5ilZL0he2raIx8t5ecQ%2FWuizky4MpcCXX3mEN38%3D&amp;reserved=0) | [Hämta länk](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-osx-x64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081981239%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=LJH3OCFq7yRykN4wU8HN9%2FBXC%2BjfXLJH4QizeFZfRHE%3D&amp;reserved=0) |
| macOS Apple Silicon (M1) (v2.3.1) | [Hämta länk](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-osx-arm64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081965822%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=2YENn0tDduiucogClt6aBZHDOE6dbzBdigq8VQawIO0%3D&amp;reserved=0) | [Hämta länk](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-osx-arm64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081986151%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=jCepldg4dMej0%2BrK2mUonXwqsWL8ksE8%2BLMSgsH9qTA%3D&amp;reserved=0) |
| Windows 64-bitars (v2.3.1) | [Hämta länk](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.exe&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081970892%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=sRn2UWW%2Bi7SMEvSO74ZGGvJ40vHh1KhLc7zAfKc37Es%3D&amp;reserved=0) | [Hämta länk](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.exe&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081991004%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=aQWZtEK%2F3cWX8n8Au%2FwZ5Zd9xPVo5phvk%2FuF%2Be0HRrE%3D&amp;reserved=0) |
| Windows 64-bitars Enterprise (v2.3.1) | [Hämta länk](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.msi&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081976350%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=v9C0sLDSkuL%2FMIyae2WkbitJPVgSlAw2BqcaH5Im0uw%3D&amp;reserved=0) | [Hämta länk](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.msi&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081995827%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=2btCh0aIrUBiyeG37K9YorvzTeIJOggbq%2FRauUMn4LY%3D&amp;reserved=0) |
| macOS (v2.3.0) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) |
| macOS Apple Silicon (M1) (v2.3.0) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) |
| Windows 64-bitars (v2.3.0) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) |
| macOS (v2.2.2) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) |
| macOS Apple Silicon (M1) (v2.2.2) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) |
| Windows 64-bitars (v2.2.2) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) |
| macOS (v2.2.1) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) |
| macOS Apple Silicon (M1) (v2.2.1) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) |
| Windows 64-bitars (v2.2.1) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) |
| macOS (v2.2.0) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) |
| macOS Apple Silicon (M1) (v2.2.0) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) |
| Windows 64-bitars (v2.2.0) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) |
| macOS (v2.1.5.0) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) |
| Windows 64-bitars (v2.1.5.0) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) |
| Windows 32-bitars (v2.1.5.0) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) |
| macOS (v2.1.4.0) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) |
| Windows 64-bitars (v2.1.4.0) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) |
| Windows 32-bitars (v2.1.4.0) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) |
| macOS (v2.1.3.4) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) |
| Windows 64-bitars (v2.1.3.4) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) |
| Windows 32-bitars (v2.1.3.1) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) | [Hämta länk](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) |

## Stöd för olika resurser och filtyper {#support-for-file-types}

Programmet stöder resurser som lagras i [!DNL Experience Manager] och som representerar binära filer för dess grundläggande åtgärder. När du öppnar filer i det inbyggda datorprogrammet måste operativsystemet koppla filtyperna PNG eller JPG till specifika program som Mac Preview eller Adobe Photoshop.

Några filtyper har stöd för att placera länkade resurser i binärfilen. Programmet hämtar de länkade resurserna i förväg om resursen finns i [!DNL Experience Manager]-databasen när sådana binära filer öppnas med skrivbordsappen. Filtyper som stöds för närvarande är:

* [!DNL Adobe InDesign] filer (INDD-format)
* [!DNL Adobe Illustrator] filer (AI-format)
* [!DNL Adobe Photoshop] filer (PS-format)

Funktionen stöds i versionerna [!DNL Adobe Creative Cloud] 2018 och [!DNL Adobe Creative Cloud] 2019 av ovanstående program. Appen använder en heuristisk, bäst matchande metod för att mappa de lokala skrivbordssökvägarna för länkade resurser till URL:er på servern [!DNL Experience Manager]. Den bygger på några antaganden:

* Sökvägar till monterade filer i det ursprungliga programmet använder en global skrivbordssökväg (placerad från den lokala nätverksresursen som visas med alternativet [!UICONTROL Reveal]).

* Sökvägar lagras i filens XMP av det inbyggda programmet.

* [!DNL Experience Manager] har extraherat XMP med sökvägarna till resursens metadatapost.

* Sökvägarna kan matchas mot resurser i [!DNL Experience Manager], vilket innebär att de monterade filerna också finns i [!DNL Experience Manager] under en matchande sökväg.

## Nya funktioner, förbättringar och felkorrigeringar {#what-is-new}

Mer information finns i [Nyheter i v2.0](introduction.md#whats-new-v2).

**Uppdateringar i app v2.3.0**

* Stöd för IMS-inloggning har lagts till. Med IMS-integrering kan skrivbordsappen utföra automatisk uppdatering av åtkomsttoken, vilket gör att användaren kan vara inloggad i upp till 14 dagar.

* Förbättrat stöd för företagsutkast och webbfiltrering.

**Uppdateringar i app v2.2.2**

* (Endast Windows) Skrivbordsappen visar en tom skärm efter installation av versionerna 2.2.0 och 2.2.1.

**Uppdateringar i app v2.2.1**

* Skrivbordsappen visar ett meddelande om timeout för session när du klickar på **[!UICONTROL Sign In]**.

* Problem vid åtkomst till datorprogrammet v2.2.0 på macOS.

* Skrivbordsappen visar ett felmeddelande när du sorterar resurser genom att klicka på **[!UICONTROL Edited Locally]**.

**Uppdateringar i app v2.2.0**

* Stöd för Apple Silicon (M1).

* Möjlighet att komma ihåg anslutningssträngen när du loggar in på datorprogrammet.

**Uppdateringar i app v2.1.5.0**

* Skrivbordsappen slutar svara när du överför filer i en mapp som innehåller kinesiska tecken (ASSETS-9237).

* datorprogrammet ersätter punkter med streck i filnamn (ASSETS-10955).

**Uppdateringar i app v2.1.4.0**

I den nya versionen av programmet finns felkorrigeringar.

**Uppdateringar i app v2.1.3.4**

Den nya versionen av programmet innehåller en felkorrigering.

**Uppdateringar i app v2.1.3.3**

Den nya versionen av programmet innehåller en felkorrigering.

**Uppdateringar i app v2.1.3.2**

I den här versionen av programmet finns en felkorrigering.

**Uppdateringar i app v2.1.3.1**

Felet som har åtgärdats i den här versionen är:

* Överförings- och nedladdningshastigheterna har förbättrats, även med stora resurser. Den här versionen åtgärdade ett problem där resursöverföringar med [!DNL desktop app] ibland misslyckades när mycket stora filer överfördes.

**Uppdatering i app v2.1.2.0**

* Ett nytt alternativ för [!UICONTROL Clear Cookies] läggs till på programmets huvudmeny. Det hjälper vid potentiella inloggningsproblem, t.ex. när en anslutning ändras från en server till en annan. Se [rensa cookies innan du ansluter](/help/using/troubleshoot.md#cannot-login-cookies-issue).

* Ett nytt alternativ har lagts till som, om det här alternativet har valts, tillåter programmet att överföra mappar och filer med nodnamn i [!DNL Adobe Experience Manager] som matchar de lokala fil- och mappnamnen. Den här processen säkerställer enhetlighet mellan lokala och överförda namn.

  Det här beteendet liknar standardbeteendet i version 1 av datorprogrammet. Om alternativet inte är aktiverat i den aktuella versionen ersätts blanksteg och tecknen `% ; # , + ? ^ { } "` i mappnamn med bindestreck i mappsökvägar. Versaler konverteras också till gemener i mappsökvägar. I filnamn ersätts dock tecknen `# % { } ? &` med bindestreck, men blanksteg och versaler behålls. Mer information finns i [appinställningar](/help/using/install-upgrade.md#set-preferences) och [Överför och lägg till nya resurser](/help/using/using.md#upload-and-add-new-assets-to-aem).

**Uppdatering i app v2.1.1.0**

* Med en avancerad inställning kan appen emulera beteendet v1.10 när mappar överförs. I v1.10 respekterar de nodnamn som skapas i databasen utrymmet och skiftläget för mappnamnen som anges av användaren. I version 2.1 är standardbeteendet oförändrat: flera mellanslag i mappnamn ersätts med bindestreck i databasens nodnamn, och nodnamn konverteras till gemener. Se [appinställningarna](/help/using/install-upgrade.md#set-preferences).

**Uppdatering i app v2.1.0.0**

* Om du vill överföra resurser kan användare nu dra filer eller mappar i programmets gränssnitt, direkt från Utforskaren i Windows eller Mac Finder. Den här processen fungerar utöver det överföringsalternativ som är tillgängligt i programmet. Se [Överför resurser](/help/using/using.md#upload-and-add-new-assets-to-aem) <!-- CQ-4309527 -->

**Uppdatering i app v2.0.3**

Felet som har åtgärdats i den här versionen är:

* Ett inloggningsproblem har korrigerats för appanvändare i Windows som försöker få åtkomst till DAM-databasen på [!DNL Adobe Experience Manager] 6.5.5.0.

**Uppdateringar i app v2.0.2**

Felkorrigeringarna och uppdateringarna är:

* Inställningen för uppladdningsacceleration är nu tillgänglig för att öka uppladdningsprestanda. När den här inställningen är aktiverad laddas programmet upp snabbare med fler lokala CPU-trådar och är mer resurskrävande.

* Resursuppladdning när filnamn eller sökvägar som innehåller vissa GB18030-tecken är fasta. <!-- CQ-4283494 -->

* Alternativet Sortera efter relevans är tillgängligt efter byte till en annan sorteringstyp i sökresultaten. <!-- CQ-4286874 -->

* Skrivbordsprogrammet visar nu undermappar utan att någon explicit uppdatering behövs. <!-- CQ-4285711 -->

* (Windows) Korrigerade ett sällsynt problem med oanvändbart appgränssnitt på vissa Windows-datorer. Användarna kan inte klicka på appgränssnittet eftersom det ser ut att vara förvrängt av klickområdet för gränssnittselementen &quot;shifts&quot;. <!-- CQ-4280785 -->

**Uppdateringar i app v2.0.1**

Felkorrigeringarna och uppdateringarna är:

* Tillåt alternativet att konfigurera katalogen `%Temp%` så att den matchar sökvägen `%APPDATA%`. <!-- CQ-4282665 -->

* Tillåt användare att logga in på [!DNL Experience Manager] Author via Okta SAML-autentisering. <!-- CQ-4278134 -->

## Installationsanvisningar {#installation-instructions-v2}

Mer information om hur du installerar och konfigurerar programmet finns i [Installera [!DNL Experience Manager] skrivbordsappen](install-upgrade.md).

Om du uppgraderar från ett tidigare [!DNL Experience Manager]-datorprogram måste du följa de bästa metoderna för övergångar som listas vid [uppgradering från den tidigare versionen](install-upgrade.md#upgrade-from-previous-version).

## Viktiga anteckningar om hur appen fungerar {#how-app-works}

Det är viktigt att du förstår följande om programmet och hur det fungerar.

* Programmet ger fullständig kontroll över åtgärder som kräver fullständig överföring av objektbinärfiler från och till [!DNL Experience Manager] (**Öppna**, **Redigera**, **Överför ändringar** och **Överför Assets**).

   * Om du vill arbeta med resursen på skrivbordet måste du uttryckligen öppna, redigera eller hämta till skrivbordet, antingen individuellt, i en mapp eller genom att markera flera.

   * Om du vill få lokala ändringar av resurser överförda till [!DNL Experience Manager] måste du välja [!UICONTROL Upload Changes], antingen individuellt eller via flerval.

   * Programmet är inte en synkroniseringsklient som synkroniserar resurser på skrivbordet och [!DNL Experience Manager].

   * Programmet tillhandahåller inte någon nätverksresurs som mappar databasen [!DNL Experience Manager] som en virtuell mappstruktur.

* Den lista över resurser som visas av programmet baseras på statusen för Assets-databasen. Filer som laddas ned lokalt och därefter byter namn i de lokala filerna eller cachemappen visas eller hanteras inte i programmet.

* Om programmet inte visar det förväntade resultatet klickar du på uppdateringsikonen i det övre fältet.

* Den lokala nätverksresursen, som visas när du använder åtgärden [!UICONTROL Reveal File], visar bara filer (och mappar) som är tillgängliga lokalt. [!UICONTROL Reveal File] och [!UICONTROL Reveal Folder] hämtar resurser i förväg för att det ska gå att visa rätt resurser i den lokala nätverksresursen.

* Den lokala nätverksresursen SMB (Mac)/WebDAV (Win) används när en Adobe Creative Cloud-app läser resursfilerna som är länkade/placerade i en systemspecifik fil i appen Creative Cloud.

I följande diagram visas flödet av resurser och filer från molnet till det lokala filsystemet och tvärtom, vilket initierats av användaråtgärder.

![Flöde av resurser från [!DNL Experience Manager]-servern till inbyggda datorprogram via skrivbordsappen](assets/da20_flow_diagram.png)

## Kända fel {#known-issues-v2}

**Problem med användargränssnittet:**

* Ibland blir gränssnittet i skrivbordsappen tomt. Högerklicka och klicka på [!UICONTROL Refresh] för att läsa in programmet igen. Efter en sådan uppdatering börjar du i DAM-databasens rot. Uppdateringar eller status för dina resurser behålls. <!-- CQ-4270267 -->

* Svårt att navigera i mappar/sökresultat utan styrplatta eller muspekare. Rullningslisten visas inte med hjullösa musenheter. <!-- CQ-4269947 -->

* I vissa fall visas inte förloppsindikatorn korrekt när den överförda resursen ändras.

* När du har tillämpat och tagit bort filtret för att hitta alla lokalt redigerade resurser tar programmet inte användarna till sökresultaten eller mappvyn som användarna började med. Appen visar rotmappen för DAM-databasen.

* När du ansluter till en URL som inte har någon [!DNL Experience Manager]-server aktiverad, svarar ibland inte anslutningsskärmen. Avsluta programmet och starta det igen.

**CRUD-problem (Skapa, Läs, Uppdatera och Ta bort):**

* När du överför ändringar till en resurs med kommentarer lagras kommentarerna med resursen i [!DNL Experience Manager], men de visas inte som versionskommentarer. Problemet har lösts i [!DNL Experience Manager] 6.4.5 och [!DNL Experience Manager] 6.5.1. Adobe rekommenderar att du installerar de senaste Service Pack-uppdateringarna. <!-- CQ-4268990 -->

* En användare kan inte avbryta överföringar av resurser. Om du utlöste en oavsiktlig stor överföring avslutar du programmet och startar det igen. <!-- CQ-4278940 -->

**Plattformsproblem:**

* I Windows kan en medias status ändras omedelbart till [!UICONTROL Edited Locally] efter att den har öppnats, även om du inte har redigerat den. Klicka på [!UICONTROL Refresh] för att uppdatera.

>[!MORELIKETHIS]
>
>* [[!DNL Experience Manager] som en [!DNL Cloud Service] dokumentation](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service)
>* [[!DNL Experience Manager] som en [!DNL Cloud Service] [!DNL Assets] dokumentation](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview)
>* [Så här använder du [!DNL Experience Manager] datorprogrammet](using.md)
>* [Installera och uppgradera datorprogrammet](install-upgrade.md)
>* [God praxis och felsökningstips](troubleshoot.md)
