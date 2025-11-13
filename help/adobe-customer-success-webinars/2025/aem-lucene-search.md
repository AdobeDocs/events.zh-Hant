---
title: AEM Lucene搜尋的重要提示和最佳實務
description: 使用進階AEM搜尋工具，例如篩選器、多面向、自動建議、NGram和拼字檢查，大幅提升數位參與度。 從真實世界的示範中學習。
solution: Experience Manager
feature: Search
role: Admin, Developer
level: Intermediate, Experienced
doc-type: Event
duration: 3630
last-substantial-update: 2025-11-13T00:00:00Z
jira: KT-19550
source-git-commit: 84c9a126769fa94b0197d12ca594137e13edc510
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---


# AEM Lucene搜尋的重要提示和最佳實務

瞭解如何使用尖端搜尋功能（包括篩選器、多面向、自動建議、NGram和拼字檢查）增強您的數位顯示並改善客戶參與度。 從真實世界的示範中學習，並深入瞭解如何使用AEM和Lucene最佳化您的搜尋功能。 此網路研討會可讓您提升搜尋體驗，並在數位環境中保持領先地位。

>[!VIDEO](https://video.tv.adobe.com/v/3476410/?learn=on&enablevpops)

## 解鎖Adobe Experience Manager中的強大搜尋

Adobe Experience Manager (AEM)運用Lucene搜尋，跨內容、資產和中繼資料提供快速的相關結果。 此會議探索Lucene索引如何運作、如何設定索引，以及最大化搜尋效能的最佳實務。

* **Lucene搜尋無處不在**&#x200B;支援AEM作者、發佈者和入口網站的搜尋，可處理自動建議、篩選器、Facet和分頁。
* **索引定義磁碟機效能**&#x200B;自訂Oak索引定義對於有效率、目標性的搜尋至關重要。
* **最佳實務事項**&#x200B;複製現有的索引定義、限制索引屬性，並使用正確的旗標進行全文檢索和屬性搜尋。
* **進階功能增強UX** Facet、自動建議、拼字檢查、提升和字乾可針對更豐富的搜尋體驗啟用。

瞭解這些原則有助於確保AEM中穩定且高價值的搜尋功能，同時支援技術和業務目標。

## Lucene索引建置區塊

AEM Lucene索引定義是搜尋效能和正確性的基礎。 主要元件包括：

* **型別**&#x200B;指定索引種類（Lucene、屬性等）。
* **節點型別限制**&#x200B;目標為特定內容型別（例如dam:Asset、cq:Page）。
* **路徑限制**&#x200B;為了效率，將索引限製為定義的存放庫路徑。
* **彙總規則**&#x200B;控制索引內容的深度和範圍，確保相關屬性可搜尋。
* **索引規則**&#x200B;核心組態；設定nodeScopeIndex之類的旗標（廣泛全文檢索搜尋）並加以分析（標籤化/標準化）。

仔細設定這些元素可確保搜尋查詢快速、相關且節省資源。

## 最佳化搜尋效能

AEM Lucene中的有效搜尋最佳化涉及策略設定和遵循最佳實務：

* **從現有的索引開始**&#x200B;永遠複製和修改現成的定義，永遠不要從頭開始建置。
* **限制索引屬性**&#x200B;僅包含保持索引精簡和效能的必要屬性。
* **明智地使用旗標：
   * **nodeScopeIndex** true適用於廣泛全文檢索搜尋
   * **已分析**&#x200B;屬性層級代碼化為true
   * 路徑型查詢的&#x200B;**evaluatePathRestriction** true
* **屬性索引**&#x200B;偏好屬性限制搜尋最佳效能；只有在需要時才使用全文。
* **排序與Facet**&#x200B;啟用propertyIndex與排序順序；設定Facet**true以計數篩選。

套用這些策略可加快查詢速度、減少資源使用量，並產生更具相關性的結果。

