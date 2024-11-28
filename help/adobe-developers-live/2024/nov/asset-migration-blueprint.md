---
title: Assets移轉藍圖
description: 瞭解如何透過Achim Koch的深入分析將舊版DAM移轉至Adobe Experience Manager Assets，其中涵蓋利害關係人分析、資源規劃、資料轉換和最佳實務，例如使用CSV檔案進行資料處理。
feature: Migration
topic: Migration
solution: Experience Manager, Experience Manager Assets
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 1690
last-substantial-update: 2024-11-26T00:00:00Z
jira: KT-16576
exl-id: f588055b-05c7-44df-be67-799a0e3ee1ed
source-git-commit: 946d7cd484e8c5d4358d4099b3518705cab8d4a3
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Assets移轉藍圖

加入Adobe首席技術架構師Achim Koch，瞭解如何將舊版DAM移轉至Adobe Experience Manager Assets。 深入瞭解利害關係人分析、資源規劃、資料轉換和最佳實務，例如使用CSV檔案進行資料處理。 為您自己的Adobe Experience Manager移轉專案建置藍圖。

>[!VIDEO](https://video.tv.adobe.com/v/3440403/?learn=on&enablevpops)

## 社群討論

在Adobe Developers Live社群[討論區](https://adobe.ly/4hKHpnF)中繼續交談。

## 重要技巧

* **沒有立即可用的移轉工具**&#x200B;由於產品和自訂解決方案的多樣性，沒有單一工具可以從各種舊式系統移轉至Adobe Experience Manager (AEM)。

* **五個移轉階段**

   * 專案計畫
   * 實作規劃
   * AEM實作
   * 移轉指令碼實施
   * 移轉執行

* **利害關係人的參與**&#x200B;識別並吸收利害關係人（例如贊助者、業務使用者、IT系統管理員和舊版系統支援）是至關重要的。

* **資源與時間表規劃**&#x200B;確保資源可用，並針對假日、尖峰營業時間及超限時段進行規劃。

* **技術規劃**&#x200B;這包括需求分析、資料轉換和基礎建設規劃。

* **反複程式**&#x200B;移轉涉及指令碼執行、分析、回饋和適應的多次反複處理。

* **最好使用CSV檔案** CSV檔案，以便在移轉過程中容易使用且可讀性。

* 建議使用&#x200B;**指令碼語言** Node.js，因為其支援CSV、AWS和HTTP，而且是學習JavaScript的好機會。

* **品質和可重複性**&#x200B;確保高品質的資料移轉、保留原始資料和CSV檔案以供參考，並使程式可重複執行。

* **內容凍結**&#x200B;在移轉期間宣告內容凍結，以防止在拍攝快照後新增資料。

* **工具與秘訣**&#x200B;使用VS Code等工具搭配Rainbow CSV副檔名，並考慮UTF-8文字檔的位元組順序標籤(BOM)。

* **商務核准**&#x200B;預留測試與取得移轉後正式商務核准的時間，以解除內容凍結。
