---
title: 效能傳遞的最佳實務
description: 運用最適化串流、自訂視訊設定檔、SEO最佳實務、影像最佳化、大量內容管理、檢視器預設集、快取失效和智慧型影像處理，使用Dynamic Media最佳化媒體傳送和效能。
feature: Dynamic Media, Video, SEO Optimization, Smart Imaging, Viewer Presets, Best Practices
topic: Content Management
solution: Experience Manager, Experience Manager Assets
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 1596
last-substantial-update: 2024-11-26T00:00:00Z
jira: KT-16572
exl-id: a1920020-b9ce-43be-8f9e-e52aac68da7b
source-git-commit: 946d7cd484e8c5d4358d4099b3518705cab8d4a3
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# 效能傳遞的最佳實務

加入Adobe資深產品經理Riya Midha，探索設定Adobe Experience Manager Assets Dynamic Media的最佳實務。 瞭解如何最佳化資產傳送、增強視訊串流、設定檢視器以及衡量和改善效能。

>[!VIDEO](https://video.tv.adobe.com/v/3440428/?learn=on&enablevpops&captions=chi_hant)

## 社群討論

在Adobe Developers Live社群[討論區](https://adobe.ly/3YGedpb)中繼續交談。

## 重要技巧

* **Dynamic Media功能** Dynamic Media可跨裝置快速且彈性地傳送高品質、個人化的媒體，每年可處理超過9萬億次的媒體傳送，每日最高可達690億個資產。
* **自我調整資料流**&#x200B;使用自我調整資料流進行視訊傳送可大幅減少緩衝。 測試顯示，在頻寬限製為5 Mbps的60秒視訊上，緩衝器計數從50減少到5。
* **視訊設定檔**&#x200B;建立具有不同品質編碼的自訂視訊設定檔，可確保在不同網路狀況下提供最佳視訊效能。
* **SEO最佳作法**
   * 使用規則集建立描述性URL以獲得更佳的SEO。
   * 新增替代文字和標題屬性至影像。
   * 利用智慧型影像和最新的影像格式（如WebP）提升搜尋排名。
* **影像最佳化**
   * 使用縮放引數，根據熒幕大小調整影像解析度。
   * 避免使用100%的影像品質；改用80-90%的範圍來縮減檔案大小，而不會造成明顯的品質損失。
   * 套用銳利化引數以增強影像中的文字清晰度。
* **大量內容管理**
   * 將動態媒體傳送的內容與其他內容分開。
   * 使用選擇性同步來最佳化處理時間並縮短上市時間。
* **檢視器預設集**&#x200B;使用檢視器預設集自訂檢視器外觀和行為，而不變更程式碼。 例如，編輯播放/暫停按鈕、啟用自動播放和回圈，以及新增影像覆蓋。
* **快取失效**&#x200B;使用快取失效來立即反映對已發佈資產所做的變更，略過預設的10小時TTL。
* **監視和偵錯**&#x200B;使用AEM案頭應用程式和查詢偵錯工具頁面之類的工具來追蹤處理工作並識別未處理的資產。
* **智慧型影像**&#x200B;預設會在所有網域上啟用智慧型影像，減少影像檔案大小並改善載入時間。
