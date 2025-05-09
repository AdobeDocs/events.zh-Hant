---
title: Adobe Experience Manager as a Cloud Service中的Dispatcher設定
description: 探索AEM Dispatcher的快取、安全性和效能最佳實務，以充份發揮AEM as a Cloud Service的擴充性和效率。
solution: Experience Manager as a Cloud Service
version: Experience Manager as a Cloud Service
feature: Dispatcher
role: Developer, Leader, User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 4200
last-substantial-update: 2025-05-07T00:00:00Z
jira: KT-17903
source-git-commit: cfc7b54ae4360779ca2c41f88fc08089bae99165
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---


# 技術研討會：Adobe Experience Manager as a Cloud Service中的Dispatcher設定

**Adobe Experience Manager (AEM) as a Cloud Service**&#x200B;為現代數位體驗平台提供擴充性、彈性和改善的效能。 此架構的核心是&#x200B;**AEM Dispatcher**，這是負責快取、安全性與請求管理的重要元件。 正確設定後，Dispatcher可加速內容傳送、保護後端系統，並提升網站整體效能。

此概覽重點說明重要的Dispatcher設定，包括快取策略、存取控制機制和請求篩選。 此外，也概述在雲端中維持安全且高效能AEM部署的最佳作法。 無論您是開發人員、架構師或業務決策者，對於Dispatcher設定的深入瞭解是充分發揮AEM as a Cloud Service潛力的關鍵。

>[!VIDEO](https://video.tv.adobe.com/v/3457891/?learn=on&enablevpops)

## 重點提要

* **用於驗證的Dispatcher SDK** AEM Dispatcher SDK是用於靜態分析設定的強大工具。 它可讓您快速驗證設定、檢查不變性並識別錯誤，與完整管道部署相比可節省大量時間。

* **快速開發環境(RDE)** RDE提供互動式執行階段環境，用於測試和偵錯靜態分析以外的組態。 如此可加快驗證和偵錯速度，減少部署和測試所需的時間。

* **具有Mod Proxy的進階網路**&#x200B;進階網路設定（例如VPN和專用輸出IP）可以使用Cloud Manager進行設定。 mod proxy模組可將交易從AEM解除安裝到外部服務，以最佳化效能並降低JVM的負載。

* **Dispatcher組態的最佳作法**&#x200B;重要建議包括使用相對路徑、唯一的x-vhost標頭、適當的使用者端標頭，以及運用快取控制標頭來有效管理快取。 這些做法有助於避免管道故障並提高偵錯效率。

* **部署的Web層管道** Web層管道是部署隔離的Dispatcher設定的公用程式。 它包含其他測試，例如快取失效，確保內容更新在生產環境中及時準確地反映。