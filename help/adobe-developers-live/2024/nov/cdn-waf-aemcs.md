---
title: Adobe Experience Manager as a Cloud Service中的CDN與WAF設定
description: 透過Adobe專家共用的可自訂CDN規則、WAF保護和設定管道，提升Adobe Experience Manager as a Cloud Service應用程式的效能和安全性。
feature: Security
topic: Performance, Security
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 2211
last-substantial-update: 2024-11-26T00:00:00Z
jira: KT-16574
exl-id: a9f38e79-c707-443d-8b2f-e534ce4dd43d
source-git-commit: 946d7cd484e8c5d4358d4099b3518705cab8d4a3
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Adobe Experience Manager as a Cloud Service中的CDN與WAF設定

透過可自訂的CDN規則、WAF保護和設定管道，充分發揮Adobe Managed CDN的潛力。 Adobe的資深電腦科學家Marius Petria、Adobe的軟體開發工程師Quentin Vecchio和Adobe的軟體開發工程師Florian Froese分享策略以提升Adobe Experience Manager as a Cloud Service應用程式的效能和安全性。

>[!VIDEO](https://video.tv.adobe.com/v/3440613/?learn=on&enablevpops&captions=chi_hant)

## 社群討論

在Adobe Developers Live社群[討論區](https://adobe.ly/3O0TyYa)中繼續交談。

## 要點

* **新設定功能簡介**&#x200B;此簡報介紹雲端服務中CDN的新設定功能，著重於針對各種使用案例設定CDN的功能。
* **CDN設定選項**&#x200B;新選項可與HTTP要求和回應互動，例如新增/移除標頭、重新寫入要求路徑、封鎖流量、重新導向使用者端以及代理至不同的來源。
* **安全性增強功能**&#x200B;新功能包含流量篩選規則，以根據請求模式封鎖或記錄流量，並匯入M WAF以針對SQL插入和XSS等Web攻擊提供進階保護。
* **宣告式組態**&#x200B;組態是使用YAML檔案完成，並透過Cloud Manager中的組態管道進行部署，使其成為快速而直接的程式。
* **要求與回應轉換**&#x200B;新功能允許要求轉換以標準化URL並移除不必要的查詢引數，以及在傳送回應給使用者端之前設定標頭的回應轉換。
* **流量篩選器與速率限制**&#x200B;流量篩選器可以封鎖特定的IP或國家/地區，並實作速率限制以防止DDoS攻擊。 可根據各種條件設定速率限制，例如使用者端IP、使用者代理程式和請求路徑。
* **監控與分析工具** Adobe提供Elasticsearch/Kibana和Splunk儀表板等工具，可分析流量和使用情況，有助於識別和緩解潛在的安全威脅。
* **實用示範**&#x200B;此簡報包含示範，說明如何使用Cloud Manager部署CDN設定，以及如何使用AEM在本機處理錯誤和驗證設定。
