---
title: 詢問專家 — Tags (Launch)中有用的擴充功能，可協助Web SDK額外收費
description: 您考慮將實作移轉至新的Adobe Web SDK嗎？  我們將在Adobe標籤庫中執行一些我們最喜歡的擴充功能，可幫助您將資料收集提升到新的境界。
solution: Data Collection,Experience Platform
kt: 10528
thumbnail: https://video.tv.adobe.com/v/346610?format=jpeg
event-start-time: 2022-08-23 09:00-7
event-cta-url: null
event-guests: Rudi Shumpert,Jeff Chasin,Eric Matisoff
exl-id: 5ef987f4-37f5-473f-b9f2-1598b7e655ba
source-git-commit: 3d2289642f4164bf82dc1c8a42c5798e9183188b
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# 詢問專家：Tags (Launch)中有用的擴充功能，可協助Web SDK額外收費

您考慮將實作移轉至新的Adobe Web SDK嗎？  我們將在Adobe標籤庫中執行一些我們最喜歡的擴充功能，可幫助您將資料收集提升到新的境界。

>[!VIDEO](https://video.tv.adobe.com/v/346610/?quality=12&learn=on)

## 節目中的問題和評論

### 來自Evolytics的資料元素助理員擴充功能

<br> 
**問題：** 從資料安全性的角度來看，使用Evolytics是否安全，因為這是協力廠商擴充功能？

**回答：** 是。 您可以視需要檢閱擴充功能程式碼，它不會儲存任何日期，只會進行轉換。

<br>

**問題：** 這也會擷取AdobeECID嗎？

**回答：** 該擴充功能中未擷取AdobeECID。 此擴充功能的用途是建立其他匿名識別碼（及其他專案）。

**回答：** 不過，您仍可透過其他方式擷取AdobeECID。 我們將透過ExL附註和Twitter分享這些內容，因為我們無法在此聊天中分享連結。

<br>

**問題：** 雜湊功能是否提供各種雜湊技術（例如SHA-256）以及公開和私密金鑰？

**回答：** 對！ SHA-256為預設值

<br>

### 一般問題和意見：

<br>

**問題：** 按一下如何下載副檔名的來源檔案？ 這是否在「3點選單」中？

**回答：** 是！ 這3個點，然後「下載來源」（從目錄檢視）

<br>

**註解：** 我對擴充功能的其中一個真正瞭解就是其省時的方面。 他們中的許多人會做您該做的事 *可以* 請處理一些自訂程式碼，但使用擴充功能時，您不需要編寫該程式碼。

**回覆：** 右上。 而且可重複使用，不需要每次都重新建立方向盤。

<br>

**問題：** Web SDK實作將如何支援或取代Analytics外掛程式？

**回答：** 由於Workspace和Adobe標籤新增了彈性，現在實際上不需要許多Analytics增效模組。 不過，尚未移轉的使用者正積極移轉，以供Web SDK使用。

<br>

**問題：** 使用Web SDK進行Activity Map追蹤的相關開發工作嗎？

**回答：** 我在此很高興回報，我們也在積極籌劃Activity Map以獲得Web SDK的支援

<br>

**問題：** 我們是否能夠存取Adobe Edge網路來管理事件，然後再將事件傳輸至終端目的地？ 我瞭解我們也可以在Launch中執行此作業，但未來是否也能在伺服器上執行此作業？

**回答：** 是！ 這是可以透過我們的事件轉送功能實現的，客戶可以透過我們的任何Real-Time CDP產品(Real-Time CDP Connections、Prime或Ultimate)購買。

**回答：** RTCDP連線（事件轉送）可讓您在將連線傳送至非Adobe目的地之前，擁有更多控制權。

**回答：** 檢視我們的一些其他ExL Live影片，以進一步瞭解此功能(例如 [這個](exl-live-episode-06-23-22.md))。

<br>

**註解：** 快速呼叫我最愛的擴充功能之一：有一個對應表格擴充功能，您可以在其中讀取「如果此值是這個，則將其設定為」的資料元素表格。

**回覆：** 它們提供的彈性令人印象深刻。 另請注意，公司也可以選擇建立自己的私人擴充功能。

<br>

**問題：** 您顯示了CRM的個別資料，例如城市和天氣，那麼我們要將個別回應儲存在何處？

**回答：** 回應會儲存在「事件轉送」屬性內觸發規則的每個唯一事件中，且僅用於該特定事件。

<br>

請繼續此主題的討論，於 [Experience League社群討論](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-platform/experience-league-live-post-session-discussion-useful-extensions/m-p/542620#M240).
<br> 

## 此資料收集系列的其他Experience League即時工作階段

* [詢問專家 — Web SDK基本知識](exl-live-episode-05-26-22.md)
* [詢問專家 — RTCDP連線](exl-live-episode-06-23-22.md)
* [詢問專家 — 資料串流和資料準備](exl-live-episode-07-21-22.md)
