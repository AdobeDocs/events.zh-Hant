---
title: 最佳化內容傳送 — 釋放Edge服務的強大功能
description: 關於Edge Delivery Services (EDS)的座談會涵蓋其架構、與檔案式和AEM式撰寫的整合、快速網站建立、自訂選項，以及維持高效能的最佳實務。
solution: Experience Manager, Experience Manager as a Cloud Service
feature: Edge Delivery Services
role: Admin, Developer, Leader, User
level: Intermediate
doc-type: Event
duration: 3589
last-substantial-update: 2024-12-06T00:00:00Z
jira: KT-16631
exl-id: 2057e491-9ec3-4bfe-b85a-6b74d70822bf
source-git-commit: 32060a6a0d2cc24b8dc09c8f5e9f9d9c679e6d3e
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# 最佳化內容傳送：釋放Edge服務的強大功能

在這場會議中，我們將概述Edge Delivery Services (EDS)及其架構。 我們將透過Universal Editor深入探討EDS如何與檔案式撰寫和AEM式撰寫整合。 即時示範會展示EDS的實際運作概況，並提供資源以供進一步探索及問答環節使用。

>[!VIDEO](https://video.tv.adobe.com/v/3440938/?learn=on&enablevpops)

## 重要技巧

### EDS簡介

* EDS是一組可撰寫的服務，旨在增強ATM的功能&#x200B;。
* 其目標是提供卓越的體驗，透過快速的開發週期和100%的燈塔分數來推動參與和轉換。&#x200B;URL

### 製作選項

* **檔案式撰寫**&#x200B;使用熟悉的工具(如Microsoft Word或Google Docs)來建立內容，無需經過大量訓練即可快速建立內容。&#x200B;URL
* **通用編輯器**&#x200B;提供與傳統ATM網站類似的WYSIWYG介面，允許建立更詳細且更視覺化的內容。&#x200B;URL

### 架構

* EDS整合至Amazon Cloud Service架構。&#x200B;URL
* 它支援無伺服器實作，且不需要傳統作者或發佈者執行個體即可運作。&#x200B;URL
* 可以實作兩個快取層級：在客戶基礎架構層級和EDS層級。&#x200B;URL

### 內容管理

* 檔案式製作需要GitHub帳戶、Google Drive或Microsoft SharePoint、Sidekick外掛程式和程式碼同步工具。&#x200B;URL
* 使用IAM編寫的EDS需要GitHub帳戶、IAM as a Cloud Service授權和程式碼同步工具。

### 開發和部署

* 使用EDS建立網站的程式很快，通常只需要不到一天的時間。&#x200B;URL
* 本機開發可使用aem up命令來建立網站的本機版本。
* 變更可以提交至功能分支，以供在合併至主要分支之前進行測試。&#x200B;URL

### 自訂性與擴充性

* 您可以使用簡單的CSS和JavaScript來建立自訂元件。&#x200B;URL
* 此架構可提供協力廠商整合和自訂編寫來源。

### 最佳實務

* 建議您使用vanilla JavaScript和CSS來維持高的Lighthouse分數。
* 匯入React等程式庫時，應經過審慎考量及測試，避免效能降低。

### 支援和檔案

* 提供完整的檔案，以引導使用者完成設定和自訂程式。&#x200B;URL
* 如有任何未解決的問題，建議使用者聯絡Adobe支援。&#x200B;URL
