---
title: AEM GEM — 開始使用Adobe Managed CDN
description: 瞭解如何在AEM Cloud Service中設定Adobe Managed CDN，以透過新的CDN設定功能增強效能和安全性。
role: Developer, User
level: Intermediate
doc-type: Event
duration: 3438
last-substantial-update: 2025-01-30T00:00:00Z
jira: KT-17227
source-git-commit: 1cfa9cdb0e973e6d088b1faeaa63539b0a7fba36
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---


# AEM GEM — 開始使用Adobe Managed CDN

瞭解AEM Cloud Service中的Adobe Managed CDN以及如何進行設定。 加入我們，探索可用來增強AEM as a Cloud Service應用程式效能和安全的新CDN設定功能。 在此工作階段中，您將探索

* 什麼是AdobeCDN
* AEMaaCS和Edge Delivery Services的相關拓撲
* 可透過CDN規則實施的典型使用案例
* 如何使用RDE快速測試和部署CDN設定

>[!VIDEO](https://video.tv.adobe.com/v/3443168/?learn=on&enablevpops)

*錄製於2025年1月22日*

有疑問嗎，可以發表意見嗎？  加入[Experience League社群](https://adobe.ly/4haufPK)中的討論！

## 重要技巧

### Adobe Managed CDN的主要功能

* **自訂網域和憑證**&#x200B;託管自訂網域和憑證以建立安全連線所必需的。
* **快取**&#x200B;從快取傳送HTTP回應比從來源擷取（數百毫秒）快很多（不到10毫秒）。
* **現成可用和自訂CDN** Adobe提供現成可用的Managed CDN，但使用者也可以自備CDN。

### 設定選項

* **要求轉換**&#x200B;修改標頭、重寫路徑、封鎖流量及重新導向要求。
* **流量篩選器**&#x200B;根據特定規則封鎖或允許流量。
* **驗證**&#x200B;支援邊緣金鑰、打孔金鑰和基本驗證。
* 根據定義的規則，**來源選取器** Proxy要求不同來源。
* **回應轉換**&#x200B;修改回應標題和狀態。

### 部署和自訂

* **設定管道**&#x200B;部署YAML檔案以設定CDN規則。
* **流量保護**&#x200B;使用流量篩選規則來根據模式封鎖、記錄及警示流量。
* **限制** Protect對每個IP的請求數量進行限制，以防止DDoS攻擊。

### 工具與分析

* **ElasticsearchKibana棧疊**&#x200B;使用提供的儀表板分析使用情況和流量。
* **記錄檔轉送**&#x200B;將記錄檔轉送至Splunk執行個體以供分析。

### 示範重點專案

* **部署組態**&#x200B;示範部署流量篩選規則與重新導向。
* **驗證和來源選擇**&#x200B;顯示如何設定基本驗證和Proxy流量到不同來源。

### 最佳實務

* **快速回應**&#x200B;確保來自來源的快速回應，以避免漏洞。
* **良好的快取**&#x200B;利用快取來有效處理流量。
* **使用儀表板**&#x200B;分析流量和使用情況以設定適當的速率限制。
* **結合策略**&#x200B;使用不同的速率限制策略以獲得更好的保護。
* **設定警示**&#x200B;當網站受到攻擊時收到通知。
* **測試規則**&#x200B;在封鎖之前先開始記錄動作，以確保規則如預期般運作。

### 聯絡與意見回饋

* **意見與使用案例**&#x200B;請聯絡團隊以取得進階使用案例與意見回饋。
* **未來的工作階段**&#x200B;參與投票，為未來的工作階段建議主題。