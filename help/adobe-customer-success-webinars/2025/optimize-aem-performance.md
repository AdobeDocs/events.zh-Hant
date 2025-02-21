---
title: 最佳化AEM效能 — 快取策略和技術
description: 會議內容包括快取策略和技術、快取機制和階層、動態內容處理、偵錯快取問題，以及在Dispatcher和CDN之間同步化快取失效。
topic: Performance
role: Admin, Developer, Leader, User
level: Intermediate
doc-type: Event
duration: 3764
last-substantial-update: 2025-02-21T00:00:00Z
jira: KT-17373
source-git-commit: e7bf8b79ad4920b303fc3afbdfb4adee60614c88
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# 最佳化AEM效能：快取策略和技術

在此會議中，我們會探索各種快取機制（例如頁面、資產和Dispatcher快取），以及如何在CDN層級實作快取，以最佳化內容傳送並減少載入時間。 此討論內容涵蓋每個快取階層的最佳實務、疑難排解常見問題，以及如何善用CDN功能來發揮最高效率。

## 主要討論點

* 快取簡介
* 快取型別、快取最佳實務、快取失效和重新整理
* 偵錯技巧

>[!VIDEO](https://video.tv.adobe.com/v/3444452/?learn=on&enablevpops)

## 重要技巧

* **快取策略與技術**&#x200B;此工作階段著重於各種快取策略與技術來最佳化效能，包括不同層級的快取，例如瀏覽器、CDN和Dispatcher。

* **快取機制和階層**&#x200B;討論內容涵蓋不同的快取機制和階層，包括瀏覽器快取、CDN快取和Dispatcher快取，以及如何設定和管理這些機制和階層。

* **動態內容處理**&#x200B;處理頁面上動態內容的技巧已經過討論，包括使用Sling Dynamic Include (SDI)和Edge Side Include (ESI)，以確保在靜態內容快取時不會快取動態內容。

* **偵錯快取問題**&#x200B;已說明在不同層級（瀏覽器、CDN、Dispatcher）偵錯快取問題的各種技術，包括使用標頭、記錄和特定設定來識別和解決快取問題。

* **快取失效的同步處理**&#x200B;工作階段解決了在Dispatcher和CDN之間同步處理快取失效的問題，建議使用較短的max-age值和CDN清除API，以確保在頁面啟動時兩個快取同時失效。