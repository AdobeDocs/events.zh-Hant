---
title: 詢問專家 — Tags (Launch)中的實用擴充功能，可協助對Web SDK充電
description: 您考慮將實作移轉至新的Adobe Web SDK嗎？  我們將在Adobe標籤庫中執行一些我們最愛的擴充功能，協助您將資料收集提升到新的境界。
solution: Data Collection, Experience Platform
feature: Tags
kt: 10528
event-start-time: 2022-08-23 09:00-7
event-guests: Rudi Shumpert,Jeff Chasin,Eric Matisoff
exl-id: 5ef987f4-37f5-473f-b9f2-1598b7e655ba
duration: 3833
source-git-commit: 0b2f63198af8767f24783dbafd244c9398c24f33
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 0%

---

# 詢問專家：標籤(Launch)中有用的擴充功能，可協助對Web SDK額外收費

您考慮將實作移轉至新的Adobe Web SDK嗎？  我們將在Adobe標籤庫中執行一些我們最愛的擴充功能，協助您將資料收集提升到新的境界。

>[!VIDEO](https://video.tv.adobe.com/v/346610/?quality=12&learn=on)

## 節目中的問題和評論

### 來自Evolytics的資料元素助理員擴充功能

<br> 
**問題：**&#x200B;從資料安全性的觀點來看，Evolytics是否安全，因為這是協力廠商擴充功能？

**回答：**&#x200B;是。 您可以視需要檢閱擴充功能程式碼，它不會儲存任何日期，只會進行轉換。

<br>

**問題：**&#x200B;這個擷取Adobe是否也有ECID？

**回答：**&#x200B;未在該擴充功能中擷取AdobeECID。 此擴充功能用於建立額外的匿名識別碼（與其他功能搭配使用）。

**回答：**&#x200B;可透過其他方式擷取AdobeECID。 我們將透過ExL附註和Twitter分享這些內容，因為我們無法在此聊天中分享連結。

<br>

**問題：**&#x200B;雜湊功能是否提供各種雜湊技術，例如SHA-256，並提供公開和私密金鑰？

**回答：**&#x200B;是！ 預設值為SHA-256

<br>

### 一般問題和意見：

<br>

**問題：**&#x200B;我們按一下如何下載副檔名的來源檔案？ 這是否在「3點選單」中？

**回答：**&#x200B;是！ 這3個點，然後（從目錄檢視）下載Source

<br>

**註解：**&#x200B;擴充功能的省時特性是我真正感興趣的因素之一。 其中許多程式碼會執行您&#x200B;*可以*&#x200B;使用某些自訂程式碼執行的動作，但若使用擴充功能，您就不需要編寫該程式碼。

**回覆：**&#x200B;立即開啟。 而且可重複使用，每次都不需要重新建立方向盤。

<br>

**問題：**&#x200B;如何支援Analytics外掛程式，或以Web SDK實作取代？

**回答：**&#x200B;由於Workspace和Adobe標籤增加了彈性，現在實際上不需要許多Analytics外掛程式。 不過，尚未移轉的使用者正積極移轉，以供Web SDK使用。

<br>

**問題：**&#x200B;使用Web SDK的Activity Map追蹤有任何開發專案嗎？

**回答：**&#x200B;我很高興回報目前也正在處理Activity Map以獲得Web SDK的支援

<br>

**問題：**&#x200B;在將事件傳輸到終端目的地之前，我們是否能夠存取Adobe Edge網路來管理事件？ 我瞭解我們也可以在Launch中執行此作業，但未來也有可能在伺服器上執行此作業嗎？

**回答：**&#x200B;是！ 這可透過我們的事件轉送功能實現，客戶可透過我們的任何Real-Time CDP產品(Real-Time CDP Connections、Prime或Ultimate)購買。

**回答：** RTCDP連線（事件轉送）讓您在將連線傳送至非adobe目的地之前，能夠擁有更多控制權。

**回答：**&#x200B;檢視我們其他的ExL Live影片，以進一步瞭解此內容（例如[這個](exl-live-episode-06-23-22.md)）。

<br>

**註解：**&#x200B;快速呼叫我最愛的擴充功能之一：有一個對應資料表擴充功能，您可以在其中讀取「如果此值是這個，則將其設定為那個」資料元素的資料表。

**回覆：**&#x200B;它們所提供的彈性令人印象深刻。 也請注意，公司也可以選擇建立自己的私人擴充功能。

<br>

**問題：**&#x200B;您顯示了來自CRM的個別資料，例如城市和天氣，那麼我們要將個別回應儲存在何處？

**回答：**&#x200B;回應會儲存在Event Forwarding屬性內觸發規則的每個唯一事件中，而且僅用於該特定事件。

<br>

繼續在[Experience League社群討論](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-platform/experience-league-live-post-session-discussion-useful-extensions/m-p/542620#M240)中討論此主題。
<br> 

## 此資料收集系列的其他Experience League即時工作階段

* [詢問專家 — Web SDK基礎知識](exl-live-episode-05-26-22.md)
* [詢問專家 — RTCDP Connections](exl-live-episode-06-23-22.md)
* [詢問專家 — 資料串流和資料準備](exl-live-episode-07-21-22.md)

