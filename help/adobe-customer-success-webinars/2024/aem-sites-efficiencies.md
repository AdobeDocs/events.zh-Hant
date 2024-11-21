---
title: AEM Sites效率 — 效能最佳化、設定和疑難排解
description: 本課程涵蓋Adobe Experience Manager (AEM) Sites的基本疑難排解技能，專注於針對效能問題、複雜設定和使用者許可權的實際動手解決方案。
solution: Experience Manager
version: Cloud Service
role: Admin, Developer, Leader, User
level: Intermediate
doc-type: Event
duration: 3452
last-substantial-update: 2024-10-30T00:00:00Z
jira: KT-16353
exl-id: 55f7c1d8-7c2c-4392-894a-2aa9b3cc0e4a
source-git-commit: ef652eb09c33f11d69ec66f70013cd3e53537a95
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# AEM Sites效率：效能最佳化、設定和疑難排解

在本網路研討會中，我們將深入探討Adobe Experience Manager (AEM) Sites疑難排解的要點。 無論您是面臨效能問題或處理複雜的設定，本課程都能提供維護及最佳化AEM環境的實用技能。 我們將優先安排即時示範而非投影片，提供親身體驗來應對現實世界的挑戰&#x200B;。

>[!VIDEO](https://video.tv.adobe.com/v/3435114/?learn=on)

## 要點

此網路研討會著重於AMP網站效率，包括效能最佳化、設定和疑難排解。

### Dispatcher設定

* Dispatcher在傳送高效能網站中的重要性。
* Dispatcher設定的主要方面：虛擬主機設定、具有快取結構的網域對應，以及定期報告和重新導向。

### Rights Management

* 最佳實務：將權利套用至群組、避免拒絕陳述並避免過度工程。
* 使用Netcentric ACL工具，透過Yaml檔案管理許可權，確保部署簡單且可追蹤。

### 效能問題

* 在同步操作中識別增量以避免完整快取排清的重要性。
* 避免在工作時間進行大型頁面操作。
* 將工作流程簡化為必要步驟。
* 在製作系統上使用協力廠商系統程式時，請務必小心，尤其是使用ImageMagick等工具時。
* 避免向無法處理負載的協力廠商系統發出同步請求。
* 管理繁重的自訂元件，避免效能降低。
* 監視長時間執行的工作階段，以防止找不到區段例外狀況。
