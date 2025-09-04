---
title: 分析的架構 — 如何接近您的Customer Journey Analytics資料模型
description: 瞭解如何使用事件階層、歸因和KPI來建構CJA資料模型，以解鎖更深入的客戶歷程深入分析。
feature: Attribution
role: User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 0
last-substantial-update: 2025-09-04T00:00:00Z
jira: KT-18813
source-git-commit: 124b52203b98a80dd9202dab1b0dbe575475a52b
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# 分析的架構：如何處理Customer Journey Analytics資料模型

建立CJA資料模型的一個重要面向是瞭解不同接觸點與互動之間的階層式關係。 這為進行有意義的分析和深入分析奠定了基礎。

主要考量事項包括

* 識別並對應所有管道的客戶互動點
* 建立明確的事件階層與關係
* 定義一致的歸因模型
* 建立標準化量度和KPI

透過正確建構這些元素，組織可以更好地追蹤和分析完整的客戶歷程，以獲得更可行的深入分析和改善決策能力。

>[!VIDEO](https://video.tv.adobe.com/v/3471111/?learn=on&enablevpops)

## 為強大的Analytics解鎖資料模型

探索Adobe Experience Platform (AEP)和Customer Journey Analytics (CJA)中的有效資料架構如何推動可操作的深入分析和報告。

* **結構描述設計很重要**&#x200B;平面結構描述、陣列和物件陣列之間的選擇，會直接影響分析功能和報表彈性。
* **轉換程式**&#x200B;擷取到AEP的資料必須經過周密的結構化，才能確保CJA中的轉換順暢且易於使用。
* **容器階層**&#x200B;瞭解事件、工作階段和人員層級，對多層級分析和準確報告至關重要。
* **實用策略**&#x200B;預先規劃、結構描述控管和運用平台功能，是擴充性、未來可行的實施的關鍵。

熟悉這些概念可讓團隊最佳化其分析工作流程，並解鎖更深入的業務深入分析。

## 結構描述型別及其使用案例

* **一般結構描述**&#x200B;最適合直接的、一對一的資料關係。 適用於基本事件追蹤和簡單量度/維度。
* **陣列**&#x200B;適用於相關專案清單（例如產品類別、內容標籤）。 每個陣列元素都會變成要分析的個別維度。
* **物件陣列**&#x200B;專為複雜使用案例（例如產品購買）所設計，每個物件會維護自己的屬性和關係。 啟用詳細的物件層級分析。
* **明智選擇**&#x200B;選取最簡單的結構描述，以符合您的需求，但針對需要保留關係的進階情境，請使用陣列和物件。