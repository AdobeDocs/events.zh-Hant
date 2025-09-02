---
title: 解決電子郵件以外的Adobe歷程
description: 瞭解如何使用Adobe Journey Optimizer設計和測試多頻道歷程，使用測試設定檔、事件資料和現實世界情境來達到最佳參與。
solution: Journey Optimizer
feature: Email, Direct Mail, Journeys
role: User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 0
last-substantial-update: 2025-08-28T00:00:00Z
jira: KT-18850
exl-id: e611a377-0e3c-4ccd-ac9c-280638b6ea36
source-git-commit: 91120ff6bfd81c7b3c9218fbbb6dbff9397b37e6
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# 解決電子郵件以外的Adobe歷程

本會議透過實際範例，探索Adobe Journey Optimizer中解決現實世界的挑戰。 它重點說明跨電子郵件、語音和直接郵件建立多接觸點歷程的策略，以建立有凝聚力的客戶體驗。 與會者將從產品所有者的角度獲得可操作的深入分析和方法，以最佳化歷程。

## 重點提要

* 使用特定的跨管道歷程對應來劃分現實世界中的問題。
* 每個問題都有多種有效的解決方案 — 靈活性是關鍵。

>[!VIDEO](https://video.tv.adobe.com/v/3471331/?learn=on&enablevpops)

## 套用真實世界的歷程案例

* **週期性付款拒絕**&#x200B;當捐贈者的每月付款失敗時，觸發多管道回應以解決問題並維持關係。
* **頻道選擇**&#x200B;先使用電子郵件，如果電子郵件退回或未採取行動，則使用直接郵件或通話。
* **Personalization**&#x200B;根據捐贈者資料（例如兒童贊助細節）調整訊息，使通訊相關。
* **可擴充性**&#x200B;設計歷程，將團隊的參與降至最低，並使未來的更新更容易。

## 逐步設計多管道歷程

* **識別定期信用卡拒絕，以識別事件**&#x200B;開始。 這會觸發歷程。
* **將資料傳送至AEP**&#x200B;將拒絕事件批次化至Adobe Experience Platform中的自訂資料集。
* **劃分歷程**&#x200B;建立三個微歷程 — 電子郵件通知、直接郵件和對外通話。 每個都使用不同的資料和時間。
* **個人化通訊**&#x200B;使用電子郵件事件資料、列印和通話的設定檔資料。 提前規劃，讓每個管道都能使用正確的資料。
* **監視回應**&#x200B;根據客戶動作（例如電子郵件開啟、點按或付款解析）調整歷程，以決定後續步驟。
