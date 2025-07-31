---
title: Överför resurser med  [!DNL Experience Manager] datorprogrammet
description: Överför resurser med  [!DNL Adobe Experience Manager] datorprogrammet.
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---


# Överför resurser {#upload-assets}

## Redigera resurser och överföra uppdaterade resurser till [!DNL Experience Manager] {#edit-assets-upload-updated-assets}

Öppna resurser för redigering när du vill göra ändringar och överföra de uppdaterade resurserna till servern [!DNL Experience Manager]. Om du vill undvika konflikter med redigeringar av andra användare använder du programmet för att starta en redigeringssession. Innan du börjar redigera bör du kontrollera att resursen inte har en låsikon som anger att en annan användare redigerar resursen.

Om du vill redigera en resurs söker du efter resursen eller bläddrar till resursens plats. Klicka på ikonen ![Mer](assets/do-not-localize/more2_da2.png) och sedan på **[!UICONTROL Edit]**.

Använd **[!UICONTROL Toggle Check-out]** för att låsa resursen för att förhindra konflikter med redigeringar av andra användare i båda följande situationer:

* Du har börjat redigera en resurs utan att först checka ut den (till exempel genom att öppna den).
* Du har för avsikt att börja redigera en resurs inom kort och vill inte att andra ska kunna redigera den.

När du är klar med redigeringarna visas statusen **[!UICONTROL Edited Locally]** för de ändrade resurserna. Alla ändringar som har sparats i resurserna är bara lokala tills du överför ändringarna till [!DNL Experience Manager]. Om du vill överföra en enskild resurs eller ett fåtal resurser klickar du på **[!UICONTROL Upload Changes]** bland alternativen för en resurs. Den skapar en version av resursen i [!DNL Experience Manager]. Med webbgränssnittet för [!DNL Assets] kan du se resurshistorik i [tidslinjevyn](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/using/activity-stream).

![Alternativet Överför ändringar i appen](assets/upload_changes_single1_da2.png "alternativet Överför ändringar i appen")

![Alternativet Överför ändringar när du visar en stor förhandsvisning av en resurs](assets/upload_changes_single2_da2.png "Alternativet Överför ändringar när du visar en stor förhandsvisning av en resurs")

Mer information om samarbetsbaserad redigering finns i [Avancerat arbetsflöde: Samarbeta med samma filer och undvik redigeringskonflikter](#adv-workflow-collaborate-avoid-conflicts).

I följande fall kanske du vill ignorera dina ändringar och redigeringar av den lokala resursen. Klicka på **[!UICONTROL Discard Changes]**.

* Om du inte vill spara ändringarna lokalt i [!DNL Experience Manager].
* Börja göra ändringar i den ursprungliga resursen när du har sparat några ändringar.
* Sluta redigera resursen eftersom den inte längre behövs.

Om det behövs kan du växla utcheckning. Den uppdaterade resursen tas bort från den lokala cachemappen och hämtas igen när du redigerar eller öppnar den.

## Överför och lägg till nya resurser till [!DNL Experience Manager] {#upload-and-add-new-assets-to-aem}

Användare kan lägga till nya resurser i DAM-databasen. Du kan till exempel vara fotograf eller entreprenör på en byrå som vill lägga till ett stort antal foton från en fotografering i [!DNL Experience Manager]-databasen. Om du vill lägga till nytt innehåll i [!DNL Experience Manager] väljer du ![alternativet ](assets/do-not-localize/upload_to_cloud_da2.png) för överföring till molnet i appens övre fält. Bläddra till resursfilerna i det lokala filsystemet och klicka på **[!UICONTROL Select]**. Du kan också överföra resurser genom att dra filerna eller mapparna i programgränssnittet. I Windows överförs resurserna till mappen om du drar resurser till en mapp i appen. Om det tar längre tid att överföra visas en förloppsindikator.

<!-- ![Download progress bar for large-sized assets](assets/upload_status_da2.png "Download progress bar for large-sized assets")
-->

Du kan överföra mappar eller enskilda filer från det lokala filsystemet. En mapps hierarki bevaras när den överförs. Se [Massöverföring](#bulk-upload-assets) innan du överför resurser i grupp.

Klicka **[!UICONTROL View]** > **[!UICONTROL Assets transfers]** om du vill visa listan över resurser som överförts i en given session. I listan kan du visa och snabbt verifiera filöverföringar för den aktuella sessionen.

![Lista över överförda resurser i en viss session](assets/assets_transfered_da2.png "Lista över överförda resurser i en viss session")

Du kan styra samtidighet för överföring (acceleration) i inställningen **[!UICONTROL Preferences]** > **[!UICONTROL Upload acceleration]**. Mer samtidighet ger vanligtvis snabbare överföringar, men kan vara resurskrävande och förbrukar mer processorkraft på den lokala datorn. Om du upplever ett långsamt system försöker du överföra igen med ett lägre värde av samtidighet.

>[!NOTE]
>
>Överföringslistan är inte beständig och är inte tillgänglig om du avslutar programmet och öppnar det igen.

## Överför resurser gruppvis {#bulk-upload-assets}

Användare eller organisationer, som fotografer och byråer, kan skapa olika resurser på plats under aktiviteter som fotografering, retuschering eller urval från en större uppsättning. Dessa åtgärder utförs ofta utanför [!DNL Experience Manager]. De kan överföra dessa stora lokala mappar till [!DNL Assets] direkt från skrivbordsappen. Mapphierarkierna bevaras och alla kapslade undermappar och inkluderade resurser överförs. De överförda resurserna är omedelbart tillgängliga för andra användare på samma server för användning. Assets överförs i bakgrunden, så åtgärden är inte kopplad till en webbläsarsession.

![Ladda upp flera lokala mappar från skrivbordet i [!DNL Experience Manager]](assets/upload_local_folders_da2.png "Ladda upp flera lokala mappar från skrivbordet till Experience Manager i grupp")

Om de förväntade ändringarna inte visas i appen klickar du på uppdateringsikonen ![Uppdatera ](assets/do-not-localize/refresh.png) när du har överfört filen.

>[!NOTE]
>
>Använd inte överföringsfunktionalitet för att migrera resurser över två [!DNL Experience Manager]-distributioner. Se i stället [migreringsguiden](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-migration-guide).

## Nästa steg {#next-steps}

* [Titta på en video för att komma igång med Adobe Experience Manager-datorprogrammet](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* Ge feedback om dokumentationen med [!UICONTROL Edit this page] ![redigera sidan](assets/do-not-localize/edit-page.png) eller [!UICONTROL Log an issue] ![skapa ett GitHub-problem](assets/do-not-localize/github-issue.png) som är tillgängligt på den högra sidopanelen

* Kontakta [kundtjänst](https://experienceleague.adobe.com/?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [Hämta resurser](/help/using/download-assets.md)
>* [Förstå användargränssnittet](/help/using/user-interface.md)
>* [Sökning](/help/using/search.md)
