---
title: 請咨詢專家 — 標籤（啟動）中的有用擴展，以幫助對Web SDK進行超級充電
description: 您是否考慮將實施遷移到新的AdobeWeb SDK?  我們將在「Adobe標籤」庫中運行我們最喜愛的一些擴展，這些擴展將幫助您將資料收集帶到下一個級別。
solution: Data Collection,Experience Platform
kt: 10528
thumbnail: 346610.jpeg
event-start-time: 2022-08-23 09:00-7
event-cta-url: null
event-guests: Rudi Shumpert,Jeff Chasin,Eric Matisoff
exl-id: 5ef987f4-37f5-473f-b9f2-1598b7e655ba
source-git-commit: 17070f55bae19ef0751a2c7c536af7758e31affc
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# 問問專家：標籤（啟動）中的有用擴展，有助於對Web SDK進行超級充電

您是否考慮將實施遷移到新的AdobeWeb SDK?  我們將在「Adobe標籤」庫中運行我們最喜愛的一些擴展，這些擴展將幫助您將資料收集帶到下一個級別。

>[!VIDEO](https://video.tv.adobe.com/v/346610/?quality=12&learn=on)

## 節目中的問題和評論

### 演化學中資料元素輔助擴展

<br> 
**問：** 從資料安全的角度來看，Evolytics是否安全使用，因為這是第三方擴展？

**答案：** 是的。 如果願意，您可以查看擴展代碼，而且它不保存任何日期，它只是進行轉換。

<br>

**問：** 此捕獲Adobe是否也是ECID?

**答案：** AdobeECID未在該擴展內捕獲。 此擴展用於建立附加的匿名標識符（除其他外）。

**答案：** AdobeECID可以通過其他方式捕獲。 我們將通過ExL筆記和Twitter來分享，因為我們無法在此處共用聊天連結。

<br>

**問：** 哈希功能是否提供了各種哈希技術，如SHA-256，並提供了公共和私有密鑰？

**答案：** 好！ SHA-256是預設

<br>

### 一般性問題和評論：

<br>

**問：** 按一下什麼可下載擴展的源檔案？ 是在&quot;三點菜單&quot;里嗎？

**答案：** 是的！ 三個點，然後是「下載源」（從目錄視圖）

<br>

**注釋：** 我真正喜歡的是延長的一個方面是節省時間。 他們中的很多人 *能* 使用某些自定義代碼，但副檔名不需要編寫該代碼。

**答復：** 就這樣。 而且它是可重複的，不需要每次都重新創造車輪。

<br>

**問：** 如何支援分析插件或用Web SDK實現替換分析插件？

**答案：** 由於Workspace和Adobe標籤的靈活性增加，許多分析插件現在實際上是不必要的。 但是，未遷移的正在被主動遷移以供Web SDK使用。

<br>

**問：** 是否使用Web SDK對活動圖跟蹤進行了任何開發？

**答案：** 我很高興地報告，Activity Map也在積極努力，以獲得Web SDK中的支援

<br>

**問：** 我們是否能夠訪問Adobe Edge網路以在將事件傳輸到最終目標之前管理這些事件？ 我知道我們也可以在Launch中完成，但將來是否也可以在伺服器上完成？

**答案：** 是的！ 這可以通過我們的事件轉發功能實現，客戶可以通過我們的任何Real-Time CDP產品(Real-Time CDP連接、最優或最終)購買該功能。

**答案：** RTCDP連接（事件轉發）提供了在將其發送到非Adobe目標之前擁有更多控制權的能力。

**答案：** 查看我們的其他ExL Live視頻以瞭解更多有關此內容的資訊(例如 [這個](exl-live-episode-06-23-22.md))。

<br>

**注釋：** 快速呼叫我最喜歡的擴展之一：有一個映射表副檔名，在該副檔名中可以讀取資料元素的表，該資料元素「如果此值為此，則將其設定為此值」。

**答復：** 它們提供的靈活性令人印象深刻。 另外，如果公司願意，也可以建立自己的私人擴展。

<br>

**問：** 你展示了CRM中的個人資料，比如城市和天氣，那麼我們在哪裡儲存個人反應？

**答案：** 響應儲存在每個觸發「事件轉發」屬性中規則的唯一事件中，並僅用於該特定事件。

<br>

繼續在 [Experience League社區討論](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-platform/experience-league-live-post-session-discussion-useful-extensions/m-p/542620#M240)。
<br> 

## 此資料收集系列中的其他Experience LeagueLIVE會話

* [詢問專家 — Web SDK的基本資訊](exl-live-episode-05-26-22.md)
* [詢問專家 — RTCDP連接](exl-live-episode-06-23-22.md)
* [詢問專家 — 資料流和資料準備](exl-live-episode-07-21-22.md)
