---
title: 現代Adobe Experience Manager編寫的通用編輯器總覽
description: 探索AEM的Universal Editor — 使用案例、跨架構支援，以及簡化製作和提升內容傳送的關鍵考量事項。
solution: Experience Manager
feature: Authoring
role: Admin, Developer, User
level: Beginner, Intermediate
doc-type: Event
duration: 2891
last-substantial-update: 2025-08-19T00:00:00Z
jira: KT-18763
source-git-commit: 3b54c46988da18248024d115997704d9881f5e68
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# Universal Editor：現代AEM撰寫策略概觀

瞭解Adobe Experience Manager的Universal Editor如何跨不同架構將內容製作從Edge Delivery Services轉換為Headless實施。 此會議將提供Universal Editor實際使用案例和關鍵技術考量的全面概觀，以協助您判斷它是否適合您的專案。 瞭解如何在您的AEM環境中實施通用編輯器，並做出明智的決策。

## 主要討論點

* 通用編輯器的主要使用案例
* 適用於傳統AEM Sites內容的Universal Editor
* 各架構的常見技術考量
* 常見問題

>[!VIDEO](https://video.tv.adobe.com/v/3470850/?learn=on&enablevpops)

## 通用編輯器功能

* **核心功能**&#x200B;支援內嵌編輯、表單式編輯和模組化對話方塊。
* **整合**&#x200B;可順暢地與AEM工具搭配使用，例如工作流程、翻譯和多網站管理。
* 自訂資料專案型別、索引標籤和模組對話方塊的&#x200B;**自訂**&#x200B;延伸點。
* **彈性**&#x200B;與多個內容後端相容，包括AEM JCR、GraphQL和Edge傳遞服務。

這些功能讓Universal Editor成為滿足現代內容管理需求的通用工具。

## 比較AEM編輯器

| 功能 | AEM頁面編輯器 | 通用編輯器 |
|--------------------------|-------------------------------|-----------------------------|
| **已匯入** | 2014 （觸控式UI） | 2024 版 |
| **內容來源** | AEM JCR | AEM JCR、GraphQL、Edge |
| **UI架構** | Coral UI | React Spectrum |
| **使用案例** | 傳統AEM網站 | Headless、Edge Delivery |
| **自訂** | 可編輯的範本，樣式系統 | JSON邏輯結構描述 |