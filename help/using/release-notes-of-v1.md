---
title: Versionsinformation om datorprogrammet v1.10
description: Versionsinformation, förbättringar, nya funktioner, kompatibilitet och nedladdningslänkar för AEM program version 1.10.
exl-id: 886864e0-016a-4a17-b3ba-4b18a514214a
source-git-commit: 23719d2f5d92f6031687df18036acdbc04722402
workflow-type: tm+mt
source-wordcount: '3989'
ht-degree: 0%

---

# Versionsinformation om [!DNL Adobe Experience Manager]-datorprogrammet v1.10 {#aem-desktop-app-release-notes}

För datorprogram v1.x är följande hämtningslänkar och AEM kompatibilitetsinformation.

| Produkter | Datorprogrammet [!DNL Adobe Experience Manager] |
|--- |--- |
| Version | 1.10 (1.10.0.6 i Mac och 1.10.0.3 i Windows) |
| Typ | Mindre release |
| Datum | 1.10.0.6 (Mac): 15 april 2020; 1.10.0.3 (Win): 31 augusti 2018 |
| Hämta URL:er | [macOS X 64 bitar](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-1.10.0.6.dmg); [Windows 32 bitar](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-1.10.0.3.exe); [Windows 64 bitar](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-1.10.0.3.exe) |
| Kompatibilitet | AEM 6.5.x; AEM 6.4.x; AEM 6.3 SP2; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |

>[!NOTE]
>
>Storleksgränsen för cachen används inte. När skrivbordsappen startas beräknas cachestorleken en gång och ett meddelande visas om storleken ligger nära den fördefinierade gränsen.

## Systemkrav och krav {#system-requirements-and-prerequisites}

Datorprogrammet [!DNL Adobe Experience Manager] är kompatibelt med följande operativsystem:

* macOS X 10.10 eller senare, med de senaste felkorrigeringarna.

* Windows 10 med de senaste servicepaketen och felkorrigeringarna.

Adobe rekommenderar att du använder den senaste versionen av AEM för att vara säker på att du använder den senaste funktionen, de senaste felkorrigeringarna och bästa möjliga prestanda.

Den version av AEM program du tänker installera på den lokala datorn kräver en specifik AEM
version/ytterligare komponenter på serversidan (Service Pack, hot fixes eller feature packs). Kontrollera att AEM är korrekt konfigurerad innan du ansluter till den för första gången. Kontakta AEM om du behöver hjälp.

Se den [detaljerade kompatibilitetsmatrisen](#compatibilitymatrix) i slutet av det här dokumentet för att utvärdera kraven för din konfiguration.

## Nyheter i datorprogrammet v1.10 {#what-s-new-in-aem-desktop-app}

AEM datorprogram 1.10 fokuserar på att förbättra användarupplevelsen kring stora överföringar, information om bakgrundsåtgärder och optimerad upplevelse när resurser öppnas med länkade filer (som InDesign).

>[!NOTE]
>
>Om du använder macOS 10.15.4 eller senare ska du använda minst version 1.10.0.6 av programmet. Den här korrigeringsversionen uppfyller kraven för [Apple-notation](https://developer.apple.com/news/?id=04102019a).

**Lokal redigering/utcheckning**: Automatisk överföring av ändringar som sparats i resurser kan inaktiveras i statusfönstret. På så sätt kan användaren fortsätta arbeta med filer och spara ändringar och sedan, när de är klara, bestämma sig för att överföra alla ändringar.

**Förenklad resursstatus**. Statusfönstret förenklades. Fliken [!UICONTROL Uploads] visar nu både enskilda resurser och mapp- eller bulköverföringar. Fliken för tidigare bulköverföringar har tagits bort.

**Programikon för att indikera massöverföring**. Programikonen indikerar att en massöverföring pågår genom att visa ett &quot;överföringsöverlägg&quot;.

**Meddelanden om uppdateringskonflikter**. När programmet upptäcker en konflikt under en resursuppdatering visas ett meddelande så att användaren kan granska den utan att övervaka statusfönstret. När programmet startas görs en sökning efter alla konflikter så att användaren kan lösa dem.

**Bättre hantering av anslutningsförluster**. Massöverföringar pausas om anslutningen bryts och användaren kan återuppta senare. Det finns ett [!UICONTROL Retry]-alternativ tillgängligt för att försöka överföra en enskild fil igen.

## Installationsanvisningar {#installation-instructions}

Detaljerade instruktioner finns i [Installera och konfigurera AEM datorprogram](install-configure-app-v1.md).

## Förbättringar i tidigare versioner {#enhancements-in-the-previous-versions}

Den här versionen utökar och ersätter de tidigare versionerna av skrivbordsappen [!DNL Experience Manager], som innehåller följande viktiga förbättringar:

* **Version 1.9/1.9.1**: Återtagbara överföringar, förbättrat statusfönster, programikoner som anger status för programmet/anslutningen, förhämtning av länkade resurser för InDesign-filer.

* **Version 1.8**: bättre kontroll över användarens cachestorlek, förbättrad inloggningsupplevelse för SAML/SSO i Windows, stöd för `.pac` nätverksproxy på Mac samt problem som rapporterats av kund.

* **Version 1.7**: förbättrad stabilitet och cachelagringslogik, bättre stöd för nätverksproxy och möjlighet att rensa interna filer efter avinstallation.

* **Version 1.6**: Förbättringar av inloggningsprocessen för olika AEM säkerhetskonfigurationer samt programmets stabilitet och prestanda.

* **Version 1.5**: Programstabilitet och motståndskraft mot olika nätverksproblem, bättre stödbarhet.

* **Version 1.4**: Möjlighet att överföra hierarkiska mappar i bakgrunden med förloppsövervakning.

* **Version 1.3**: prestandaförbättringar och stabilitet vid åtkomst av filer och när ändringar sparas i AEM, särskilt från skrivbordsprogram i Creative Cloud, som InDesign, Illustrator eller Photoshop. Det syftade till att ge användarna en mer lokal skrivbordsliknande upplevelse när de arbetade med filer, samtidigt som de hanterade nätverksdataöverföringsåtgärder i bakgrunden.

### Förbättringar har gjorts sedan AEM datorprogram 1.9 {#Enhancements-Available-Since-AEM-Desktop-App-19x}

[!DNL Adobe Experience Manager]-datorappversion 1.9.1 var en korrigeringsversion. Den har utformats för att åtgärda viktiga kundproblem med utcheckning av mediefiler. Och adressera kopiering av filer från en nätverksresurs till en lokal katalog.

* Assets utcheckad av en användare bör inte vara tillgängligt för ändring för andra användare (CQ-4246009)

* Supportkopia från en mappad mapp till en lokal mapp när användarmappen finns på en separat diskpartition (CQ-4243978)

AEM program 1.9 fokuserar på att förbättra användarupplevelsen kring stora överföringar, information om bakgrundsåtgärder och optimerad upplevelse när resurser öppnas med länkade filer (som InDesign).

**Återuppta överföringar**
För överföringar, särskilt runt stora filer, finns det ett alternativ för att pausa/återuppta dem i det nya fönstret Resursstatus.

**Förbättrat statusfönster för resurs**
Ett förbättrat fönster för Resursstatus innehåller följande information om resurser.

[!UICONTROL Changes]

* Visar ändringar som står i kö.

* Visar pågående överföringar med en förloppsindikator, överföringshastighet, total filstorlek och den mängd som överförts hittills.

* Slutförda överföringar visas med total överförd och slutlig kostnad.

* Misslyckade överföringar visas tillsammans med ett felmeddelande och överföringsinformation, om sådan finns.

* Överföringar som har misslyckats tre gånger visar ett felmeddelande.

* Filkonflikter visas med en ikon som användaren kan klicka på. Om du klickar på ikonen visas en dialogruta med en förklaring och två alternativ:

   * [!UICONTROL Keep Mine] överför filen omedelbart till servern.

   * [!UICONTROL Overwrite Mine] tar omedelbart bort den lokala filen och hämtar en ny kopia från servern.

[!UICONTROL Downloads]

* Visar pågående hämtningar, inklusive överföringshastighet och storlek som överförts hittills.

* Slutförda nedladdningar visas med totalt överfört värde, slutvärde och en ikon som öppnar filen när du klickar på den (endast tillgängligt för enstaka filer).

* Misslyckade hämtningar visas med ett felmeddelande och överföringsinformation, om sådan finns.

* Sidfoten visar det totala antalet filer som har laddats ned och den genomsnittliga överföringshastigheten.

* Om en användare väljer att öppna eller redigera flera filer från webbgränssnittet [!DNL Experience Manager Assets] grupperas de tillsammans. Exempel: myasset.jpeg och ytterligare fyra filer.

* När du hämtar InDesign-dokument med länkade resurser från AEM Assets hämtar skrivbordsappen först alla länkade resurser innan dokumentet öppnas och visar hämtningsstatus. Exempel: 5 av 24.

[!UICONTROL Bulk Uploads]

Om du överför stora mapphierarkier via [!UICONTROL Create] > [!UICONTROL Upload Folder] i det AEM webbgränssnittet öppnas den här dialogrutan. Samma sak händer när du kopierar och väljer Klistra in Assets i Finder eller Utforskaren på snabbmenyn för skrivbordsappen.

* Visar pågående överföringar, inklusive en förloppsindikator och namnet på filen som överförs för närvarande.

* Överföringar som pågår innehåller en ikon som avbryter överföringen när användaren klickar på den. Överföringen avbryts när den överförda filen har slutförts.

* Misslyckade överföringsprocesser visas med ett felmeddelande (endast om hela överföringen misslyckas).

* Om en enskild fil inte överförs visas den på fliken som ett fel. Annars visas inte enskilda filer på fliken * bara en post för hela överföringen.

**Ikoner som anger status för bakgrundsåtgärder**

Programikonen indikerar läget för bakgrundsåtgärderna för att ge användarna en bättre visuell referens. Om programmet till exempel inte är anslutet till AEM är ikonen nedtonad. När det finns en aktiv överföring visas en&quot;synkroniseringsövertäckning&quot; och så vidare.

**Förhämtning av länkade Assets**

För att förbättra användarupplevelsen av InDesign-dokument som innehåller länkade resurser som lagras i AEM hämtar skrivbordsappen dessa länkade filer i förväg till det lokala cacheminnet. Det här flödet inträffar innan InDesignen hämtas och öppnas. På så sätt är de länkade filerna tillgängliga lokalt och behöver inte vänta längre vid åtkomst av resurser i InDesignen (på länkpanelen).
Förhämtning fungerar bara om AEM känner igen länkarna på serversidan. En resurs med identifierade länkar har en lista med &quot;referenser&quot; som visas i egenskapsvyn för InDesignen.

### Förbättringar som är tillgängliga sedan AEM datorprogrammet 1.8.x {#enhancements-available-since-aem-desktop-app-18x}

AEM program 1.8.1 snabbspolning tillkom förbättringar när flera filer öppnas samtidigt från AEM till version 1.8 (CQ-4237747, CQ-4238780). Förbättringar i AEM program 1.8:

* Cachelagring: nytt användargränssnitt för hantering AEM datorprogramcache (CQ-4208690), inklusive

   * visa aktuell cachestorlek

   * ange den maximala cachestorleken innan ett meddelande skickas

   * Cachestorleken kontrolleras endast vid start av skrivbordsappen och ett meddelande visas om den når den konfigurerade gränsen

   * rensningsknappen för cache är nu tillgänglig i det nya användargränssnittet

* Logga in: (Win) Inloggningen till AEM instans som konfigurerats att använda SAML och SSL (CQ-4216353) har korrigerats

* Nätverk:

   * när en AEM förfaller meddelas användaren nu och kan klicka på meddelandet för att logga in igen (CQ-4202028).

   * (Mac) Lägg till stöd för anslutning till AEM genom att använda proxykonfigurationen `.pac` (CQ-4233430).

   * (Win) Åtgärda problem med dialogrutan Avancerat - inloggnings-URL (CQ-4236061).

* Felkorrigeringar:

   * Dialogrutan Mer resursinformation: ibland var åtgärdsfältet inte synligt (CQ-4208540).

   * (Win) Filen kan nu synkroniseras efter återställning till en tidigare version från AEM Assets UI (CQ-4216411).

### Förbättringar som är tillgängliga sedan AEM datorprogram 1.7 {#Enhancements-Available-Since-AEM-Desktop-App-17}

* Stabilitet:

   * Förbättrad stabilitet när AEM datorprogram ansluter till en överbelastad AEM (CQ-4224803).

   * Förbättrad stabilitet när många filer begärs (CQ-4224212).

   * Förbättrad uppdatering av resurser med ytterligare kontroll (CQ-4228291).

* Cachelagring:

   * Åtgärda diskfel och problem med att öppna filer i Photoshop, InDesign, Finder (CQ-4223993, CQ-4217603, CQ-4223717).

   * Förbättrad cachelagring för att undvika binärfiler i nollstorlek (CQ-4216599).

* Inloggning: Tillåt anslutning med strictSSL inaktiverat för specialkonfigurationer (som lokalt utfärdade certifikat) (CQ-4223949).

* Nätverk: Förbättrat stöd för anslutning via nätverksproxy (CQ-4223477, CQ-4221280, CQ-4206854).

* Installation och avinstallation:

   * (Win) Avinstallation av rengöringsmedel (CQ-4220906).

   * Installationsprogrammet för [Windows 32bit] kan inte installera Microsoft .NET Framework v. 4.5 (CQ-4218084).

   * (Mac) Manuellt skript för att ta bort skrivbordsappfiler helt (CQ-4216489).

>[!NOTE]
>
>Problem som påträffas AEM betaversioner av program 1.7 som inte fanns i version 1.6 utelämnas i versionsinformationen.

### Förbättringar som är tillgängliga sedan AEM datorprogram 1.6 {#Enhancements-Available-Since-AEM-Desktop-App-16}

* Dokumentation: Ny [metodtips för v1.x-appdokumentation](/help/using/best-practices-for-v1.md).

* Förbättrad inloggningsprocess för AEM:

   * Förbättra SAML-hanteringen * Slappna av i regler (CQ-4202781).

   * Lägg till funktioner för att konfigurera en separat inloggnings-URL i Inställningar (CQ-4214052, CQ-4214051).

* Användbarhet: Meddela användaren när en resurs fortfarande hämtas för större resurser (CQ-4216284).

* Nätverk:

   * DNS-cachning (CQ-4210176).

   * Stöd för anslutning via proxy i Windows (CQ-4206854).

* Cachelagring och åtkomst till nätverksresurs i Finder/Utforskaren:

   * Låsikonen visas nu för utcheckade resurser i Windows 10 (CQ-90957).

   * Mappinnehåll kan försvinna/visas igen i en nätverksresurs (CQ-4209160, CQ-4210180).

   * Fel vid filöverföring på grund av en konflikt som rapporterats i status för överföringskön (CQ-4215727).

   * När du öppnar flera filer från skrivbordsappen i PS kan trunkerade eller ofullständiga meddelanden visas (CQ-4216276).

* Stabilitets- och prestandakorrigeringar:

   * Förbättrade prestanda vid bläddring i mappar med många resurser (CQ-4214933).

   * Skrivbordsappen 1.5 kan göra en stationär dator långsammare med tiden (CQ-4209159).

   * Visa endast köstatusfunktionen för den användare som installerade programmet (CQ-4212199).

   * (Windows) Kontrollera att 32-bitars installationsprogrammet inte innehåller 64-bitarskod (CQ-4217406).

* Utvalda problem som hittats och korrigerats i 1.6 Beta:

   * Hög processoranvändning (CQ-4218070).

   * Dra och släpp-filer genererar fel vid överföring till AEM (CQ-4217006).

### Förbättringar som är tillgängliga sedan AEM datorprogram 1.5 {#Enhancements-Available-Since-AEM-Desktop-App-15}

**Version 1.5.1.5 för macOS X:** Versionen 1.5.1.5 ger följande fördelar:

* Nya funktioner och förbättringar: Lägg till funktionen Kopiera/Klistra in i Finder-integreringen för direkt överföring från skrivbordet till AEM (CQ-4208158).

* Felkorrigeringar:

   * Korrigerat fel 43 som uppstod ibland vid namnbyte av resurser (CQ-4207900).

   * När du återgår till en äldre version från tidslinjen i AEM uppdateras inte resursen i Finder (CQ-4205194).

   * skrivbordsappen kraschar vid bläddring i stora kapslade kataloger (CQ-4208539).

   * monteringspunkten för skrivbordsappen är nu /Volumes/DAM så den är konsekvent för alla användare (CQ-4208159).

   * När du placerar en fil i InDesign för första gången visas en uppdateringsvarning (CQ-4207454).

Kommentarer till länkvarningar: Creative Cloud-program (t.ex. InDesign) tar en ögonblicksbild av objektets senaste ändringsdatum när det placeras. Om det datumet ändras vid ett senare tillfälle rapporterar Adobe Creative Cloud-programmet att länkarna är inaktuella. Denna information rapporteras på några sätt:

* När Adobe Creative Cloud-programmet startas visas en dialogruta som informerar användaren om att de länkade resurserna är inaktuella och uppmanar användaren att vidta åtgärder.

* Om Adobe Creative Cloud-programmet redan körs visas en gul triangelvarningsikon på den länkade resursen.

Detta beteende är detsamma för resurser på den lokala hårddisken och resurser i en AEM skrivbordskatalog, med följande undantag:

* Om en annan användare redigerar en placerad resurs visas varningsikonen första gången som andra användare öppnar ett dokument som innehåller den placerade resursen. Den här varningen inträffar bara om den placerade resursen redan har cachelagrats lokalt.

* Om en användare ändrar en placerad resurs via AEM skrivbordskatalog och sedan rensar sin lokala cache, rapporteras den placerade resursen som inaktuell.

Båda dessa fall förväntas och är biverkningar av den&quot;fördröjda synkroniseringsarkitekturen&quot; i AEM dator.

**Version 1.5.0.x för macOS X och Windows:** Den här versionen av AEM ger följande fördelar:

* Bättre stabilitet och motståndskraft mot nätverksproblem.

   * Mer stabil mappning av AEM Assets-mappar (CQ-103276, CQ-4204669, CQ-4203957).

   * Bättre hantering av cachade filer (CQ-4204336, CQ-4206263).

   * Förbättrad hantering av hämtning/överföring av stora filer som är större än 2 GB (CQ-4206438).

   * Korrigerat &quot;Fel 36&quot; vid flytt eller namnbyte av ett större antal filer i Finder (CQ-4204640).

* Optimeringar i nätverkskommunikation med AEM server (CQ-4204974, CQ-100903).

* Förbättrad tillförlitlighet för att öppna, placera och spara resurser från AEM i Creative Cloud-appar (CQ-4203968, CQ-4205511, CQ-103543, CQ-4207141, CQ-90980).

* Förbättrad stödbarhet: möjlighet att rensa cacheminne (CQ-4202541), enkel åtkomst till loggar (CQ-4202340, CQ-4204673).

* Andra korrigeringar:
   * Bättre stöd för resurser och mappar med japanska tecken i språkinställningarna för namn/icke-engelska (CQ-4195433, CQ-4205793, CQ-4199446).

   * Bättre inloggningshantering med SSL (CQ-4200217).

   * Säkrare montering av aktier (CQ-4200793).

   * Olika stabilitetsförbättringar (CQ-4207539, CQ-4200378).

   * Bättre hantering av AEM Assets URL i Inställningar (CQ-97388).

### Förbättringar som är tillgängliga sedan AEM datorprogram 1.4 {#Enhancements-Available-Since-AEM-Desktop-App-14}

* Förenklad överföring av hierarkiska mappar med den nya åtgärden Skapa > Överför mapp i Touch-gränssnittet.
   * Den här åtgärden initierar en mappöverföring som utförs av skrivbordsprogrammet.
   * Skrivbordsappen går igenom mapphierarkin på skrivbordet i bakgrunden och överför filerna till AEM Assets.
   * Användaren kan övervaka förloppet i det nya fönstret Status för överföringskö för pågående åtgärder.
   * Status för överföringskö ger även bättre felsökningsinformation (till exempel ingen anslutning till servern).
* Ny redigeringsåtgärd i Touch-gränssnittet som kombinerar åtgärderna Checka ut och Öppna i ett.
* Optimerad gruppering av skrivbordsrelaterade åtgärder i Touch-gränssnittet (AEM 6.3).
* Förbättrad kompatibilitet med de senaste operativsystemsversionerna.
* Kundrapporterade korrigeringar.

### Förbättringar som är tillgängliga sedan AEM datorprogram 1.3 {#Enhancements-Available-Since-AEM-Desktop-App-13}

* Ökad effektivitet. Användarna slipper vänta på att nätverksoperationerna ska slutföras.
* Förbättrad integrering med Finder, som ger bättre stabilitet och åtkomst till funktioner som miniatyrbilder.
* Cachelagring och prestandaförbättringar.
* Bättre stöd för att spara direkt från skrivbordsappar (PS, ID, AI och så vidare).
* Förbättrad integrering med macOS (protokoll för lokal nätverksenhet har ändrats från WebDAV till stabilare SMB1).
* Skrivbordsappen ansluter till AEM server med AEM HTTP RESTful-protokoll.
* Filerna sparas först lokalt och överförs sedan tillbaka till AEM i bakgrunden efter en fördefinierad tidpunkt (30 sek). Det här arbetsflödet minskar tiden det tar att spara filer.
* Bättre hantering av skrivbordsprogram där mellanliggande filåtgärder används för att spara en fil (delvis sparade och tillfälliga filer), vilket gör att tidslinjen för AEM kan visa korrekt information om version och överföring av resurser.
* En dialogruta visas för att spåra status för bakgrundsuppladdningsuppgifter.

## Ändringslista {#list-of-changes}

### Monteringspunkt på Mac {#mount-point-on-mac}

Sedan macOS 10.12 (Sierra) har Apple ändrat behörigheterna för mappen /Volumes som används för att montera nätverksenheter och enheter till mer restriktiva. För att skapa en ny monteringspunkt på den platsen krävs administratörsbehörighet. Problemet har åtgärdats i macOS 10.12.5.

AEM monteringspunkt har ändrats i versionerna 1.4 och 1.5. I macOS har den ändrats till en DAM-undermapp i användarens lokala mapp med stöd för icke-adminanvändare (CQ-104183).

Eftersom mappen `/Volumes` inte längre kräver administratörsbehörighet har den här ändringen återställts i 1.5.1. Den här ändringen gör det också möjligt att dela InDesign-dokument som har placerat resurser från AEM mellan macOS-användare.

### Protokolländring (sedan v1.3) {#protocol-change-since}

* macOS X:
   * Det lokala nätverksenhetsprotokollet för OS X-skrivbordsintegrering har ändrats till SMB1 från WebDAV.
   * Den AEM databasen som är monterad med skrivbordsappen visas som en `smb`-nätverksenhet i Finder i stället för som en WebDAV-enhet.
* Windows:
   * Det lokala nätverksenhetsprotokollet för Windows-skrivbordsintegreringar behålls. AEM monteras som en WebDAV-resurs.
* För båda plattformarna (Windows och Mac):
   * Protokollet för åtkomst/hämtning av resurser och för överföring av ändringar i AEM har ändrats till det inbyggda AEM-protokollet, som är ett HTTP-baserat RESTful-protokoll. Den ger bättre kontroll över nätverksoperationer och är mer kompatibel med nätverksinfrastrukturen.

>[!NOTE]
>
>I macOS X resulterar ändringen av det lokala nätverksenhetsprotokollet från WebDAV till SMB1 i en annan lokal sökväg till samma resurs i databasen. Den här ändringen kan påverka länkar till filer som har placerats i Adobe Creative Cloud-program med hjälp av kommandot Montera. Mer information finns i [Använd AEM datorprogram](use-app-v1.md).

### Filhantering (sedan 1.3) {#file-handling-since}

* Mappar uppdateras automatiskt efter en fördefinierad fördröjning (för närvarande 30 sekunder).
* Filer som har checkats ut av andra användare är skrivskyddade.
* Filerna sparas på en nätverksenhet som monterats med skrivbordsappen i två faser.
* I den första fasen sparas en fil lokalt. På så sätt behöver användaren som sparar filen inte vänta tills filen har överförts helt till AEM och kan återuppta arbetet så fort filen har sparats.
* I den andra fasen överför skrivbordsprogrammet en uppdaterad fil till AEM efter en fördefinierad fördröjning (till exempel trettio sekunder). Den här åtgärden utförs i bakgrunden. Använd alternativet **Visa status för filsynkronisering i bakgrunden** för att visa status för överföringen.

## Viktiga meddelanden {#important-notices}

**Mappöverföring.** Adobe rekommenderar att du använder den nya mappöverföringsfunktionen för att överföra större, hierarkiska mappar till AEM. Det här arbetssättet rekommenderas i stället för att använda en kopia/dra och släpp i en monterad AEM från Finder-/Utforskarnivå. När du använder funktionen för mappöverföring kommunicerar skrivbordsappen direkt med AEM och har därför bättre kontroll över hela processen.

**Håll AEM session tillgänglig.** Det AEM skrivbordsprogrammet är beroende av en session som är öppen för AEM Assets-servern för att garantera att åtgärden fungerar som den ska. Dagliga användare bör avmontera AEM Assets vid dagens slut för att logga ut och fjärransluta på morgonen för att säkerställa funktioner för inloggning och nätverksdelning.

**Inaktivera&quot;Förhandsvisning av ikon&quot; i Finder.** Kontrollera att både Icon och Icon Preview är inaktiverade för att du ska kunna bläddra i stora mappar med Finder, särskilt om nätverksanslutningen är dålig. Annars börjar Finder hämta varje resurs i en mapp för att generera en liten förhandsvisning, vilket kan leda till sämre prestanda och hög bandbreddsanvändning (CQ-4219779)

* Gå till AEM Assets delade nätverksmapp i Finder
* Högerklicka på DAM-monteringspunkten
* Välj Visa visningsalternativ
* Avmarkera Visa ikonförhandsvisning
* Klicka på Använd som standard

**Rensa cachen vid anslutning till en ny AEM.** Om skrivbordsappen ansluter till en annan AEM med samma URL rensas inte cachen automatiskt. Rensa cacheminnet manuellt för att säkerställa korrekta åtgärder. Observera att detta vanligtvis sker vid testning, när AEM installationer kan ersättas när de körs på samma URL (CQ-4216982)

**Använd certifikatsignerade SSL-certifikat.** Skrivbordsappen AEM stöder inte självsignerade SSL-certifikat vid anslutning till AEM via en säker HTTPS-anslutning. Ett CA-signerat certifikat krävs på servern för sådana anslutningar. (CQ-87941)

## Kända fel {#known-issues}

* Allmänt:
   * Server-URL:er krävs för att peka mot servern utan sökväg (till exempel `http://server`, `https://server`, `http://server:port` eller `https://server:port`). Kontextsökvägar och andra undermappar än /content/dam stöds inte (CQ-89343, CQ-87272)
* Filnamn/lokalisering:
   * Fil- och mappnamn med reserverade tecken hanteras inte korrekt. Se till att du använder fil- och mappnamn som passar AEM. (CQ-93361, CQ-93308, CQ-89276, CQ-4217183)
   * I vissa program, som Adobe Illustrator, kan filer med namn som inte stöds i AEM skapas. Du kan till exempel lägga till `Converted` efter konvertering av en fil, vilket gör att den inte kan överföras. (CQ-4216985)
   * Assets med internationella namn kan dyka upp och försvinna några sekunder.
* Checka in och Checka ut:
   * En resurs som har checkats ut av en användare kan inte öppnas för en annan användare, antingen genom åtgärden Öppna från Touch-gränssnittet eller direkt på skrivbordet. I vissa program kan det rapporteras som låst, men det kan också vara skadat eller till och med låst när programmet öppnas. (CQ-4199234)
   * Om flera användare ändrar filer samtidigt kan vissa ändringar gå förlorade. Du kan lösa problemet genom att använda funktionerna för in- och utcheckning för att förhindra att flera användare ändrar samma fil. CQ-97035
   * I vissa program stöds inte den skrivskyddade flaggan korrekt, vilket gör att en användare kan spara en fil som en annan användare har checkat ut. Den ändrade filen överförs inte förrän den andra användaren checkar in filen. Båda ändringarna är tillgängliga i AEM som olika versioner av tillgången. (CQ-89551, CQ-87572, CQ-89615)
   * De utcheckade och skrivskyddade statusvärdena rapporteras separat i Finder. Det här sättet ger två låsikoner när en användare checkar ut en resurs. (CQ-89507)
* Integrering med Finder:
   * När du drar och släpper stora filer kan det hända att programmet får en timeout när filerna överförs i bakgrunden. Fördröjningen resulterar i en `Error - 36`. Du kan lösa problemet genom att dra och släppa eller öppna resursen igen. (CQ-4219628)
   * Manuell mappinläsning fungerar inte alltid. Tillfällig lösning: vänta trettio sekunder på att mappen uppdateras automatiskt. (CQ-97389)
   * Mer resursinformation ... begränsas till enstaka filval. (CQ-89542, CQ-87656)
   * Öppna i AEM Assets.. begränsas till att markera en fil och en mapp. (CQ-83382)
   * Ett fel uppstod vid namnändring av resurser som inte har något tillägg. (CQ-4218971)
* Funktionen Kopiera/Klistra in: Klistra in är tillgänglig när ingen resurs har kopierats till Urklipp.
* Windows:
   * Filer med ADS (Alternate Data Streams) stöds endast fullt ut på NTFS. När du kopierar filer till WebDAV-resursen via skrivbordsappen visas ett varningsmeddelande om att vissa filegenskaper inte kan överföras till den nya platsen. Den här varningen är vanligtvis bra eftersom egenskaperna bara är relevanta för ett visst program på användarens skrivbord och inte har något att göra med det faktiska filinnehållet. (CQ-103770) (Win)
   * Användaren som använder datorprogrammet i Windows måste vara den som installerar det. (CQ-4216389) (Win)
   * Appen kan krascha när du väljer alternativet [!UICONTROL Retry] för en misslyckad överföring. Denna krasch kan inträffa under vissa omständigheter efter att batchöverföringen återupptagits när anslutningen bryts. (CQ-4251884) (Win)

## Användbara resurser {#helpful-resources}

* [AEM dokumentation](https://experienceleague.adobe.com/en/docs)
* [Använd AEM v1.x](use-app-v1.md)
* [AEM praxis för datorprogram v1.x](best-practices-for-v1.md)

## Kompatibilitetsmatris och krav {#compatibilitymatrix}

AEM kan användas med olika versioner av AEM. Se kompatibilitetsmatrisen för de versioner som stöds.

| Version | Revision | Releasedatum | Kompatibilitet |
|--- |--- |--- |--- |
| 1,10 | 1.10.0.3 (Mac och Win) | 31 augusti 2018 | AEM 6.5; AEM 6.4 SP1; AEM 6.3 SP2; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
| 1,9 | 1.9.1.1 (Mac och Win) | 21 juni 2018 | AEM 6.4; AEM 6.3 SP1; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
| 1,8 | 1.8.1.0 (Mac och Win) | 28 mars 2018 | AEM 6.4; AEM 6.3 SP1; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
| 1,7 | 1.7.0.3 (Mac och Win) | 10 januari 2018 | AEM 6.3 SP1; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
