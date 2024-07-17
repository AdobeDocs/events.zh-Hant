---
title: 將您的Adobe Analytics資料和分析帶入Customer Journey Analytics
description: 瞭解新的自動化流程如何協助您將分析和資料從Adobe Analytics移至Adobe Customer Journey Analytics。
jira: KT-14746
solution: Analytics,Customer Journey Analytics
feature: Experience Cloud Integration
event-cta-url-live: https://www.youtube.com/watch?v=BkAjaMPgpgE
event-cta-url-reg: https://engage.adobe.com/ExpLeagueLive-240117.html
event-start-time: 2024-01-17 10:00-7
event-guests: Doug Moore,Eric Matisoff,Bryan Skelton
exl-id: 2c2136a9-0b40-4a0a-907d-5af181568073
duration: 3655
source-git-commit: 0b2f63198af8767f24783dbafd244c9398c24f33
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# 將您的Adobe Analytics資料和分析帶入Customer Journey Analytics

與Bryan、Eric和Doug一起討論如何快速開始使用Customer Journey Analytics (CJA)。 您將瞭解如何使用自動化程式將資料和分析從Adobe Analytics移至CJA，以及在此過程中要考慮的任何問題。 當然，他們在此過程中還會有一些有趣的秘訣和技巧。

>[!VIDEO](https://video.tv.adobe.com/v/3426778/?quality=12&learn=on)

>[!BEGINSHADEBOX 「有問題嗎？」]

繼續在[Experience League社群論壇討論](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/experience-league-live-post-session-discussion-bringing-your/m-p/646093#M3582)上的討論。

>[!ENDSHADEBOX]

## 重要技巧

* 您可透過兩種方式，從Adobe Analytics將資料匯入Customer Journey Analytics：Analytics Data Connector (ADC)和Web SDK。
* ADC可將報表套裝中的資料複製到Adobe Experience Platform進行分析，而Web SDK會將資料直接傳送到Adobe Experience Platform。
* Customer Journey Analytics中的資料檢視提供一種自訂和分析匯入平台之資料的方式。
* 資料檢視提供強大的功能，例如追溯變更、自訂的衍生欄位，以及在精細層次篩選和分析資料的能力。
* Customer Journey Analytics中的連線可合併不同的資料集，以便在一個位置分析多個資料來源。
* 應策略且謹慎地使用資料檢視和連線，以確保對資料存取和分析進行適當的治理和控制。
* 有一個名為「元件移轉」的新工具，可讓Adobe Analytics管理員將專案移轉到CGA。
* 移轉專案時，表格中的所有元件，以及套用的任何區段或計算量度都會移至CGA。
* 有一個對應程式，可使用catch-all或衍生欄位來對CGA中不存在的元件。
* 建議您針對CGA中不存在的元素建立全包專案，然後在目標專案中進行編輯。
* 以前遷移至CGA時，系統認為必須重新建立計算量度和區段，但現在您可以選擇移轉它們。
* 若要確保移轉中包含計算量度和區段，這些量度和區段必須套用至Adobe Analytics中的表格或視覺效果。

