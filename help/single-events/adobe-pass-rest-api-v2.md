---
title: Adobe Pass — 新REST API v2
description: 本次研討會著重介紹Adobe的全新REST API v2，並引導使用者完成其移轉程式。
role: Developer
level: Beginner, Intermediate, Experienced
doc-type: Technical Video
duration: 3230
last-substantial-update: 2025-04-07T00:00:00Z
jira: KT-17685
hidefromtoc: true
source-git-commit: 1082d67d49901e151115255b585799a5f57bda4a
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---


# Adobe Pass — 新REST API v2

本次研討會著重介紹Adobe的全新REST API v2，並引導使用者完成其移轉程式。

>[!VIDEO](https://video.tv.adobe.com/v/3457461/?learn=on&enablevpops)

## 重要焦點

* **總覽與優點**

   * REST API v2專為現代、彈性及可擴充的驗證而設計，適合高需求事件和多裝置情況。
   * 金鑰改良功能包括增強式加密、工作階段一致性、跨裝置SSO，以及可加快偵錯速度的延伸錯誤資訊。

* **移轉步驟**

   * 使用者必須以REST API v2範圍建立新的已註冊應用程式。
   * 可重複使用現有設定，例如裝置識別和MVPD對應。
   * 移轉涉及註冊、設定、驗證、預先授權和授權等階段。

* **功能增強功能**

   * 統一的RESTful API取代了存取芳鄰SDK，簡化各平台的實作。
   * 支援相同工作階段中的多個驗證設定檔，並可順暢地跨裝置轉換。
   * 預先授權和授權流程對於內容存取仍然是強制性的。

* **時間表**

   * REST API v1將在2025年12月前停止接收更新，並在2026年底前完全淘汰。
   * 建議使用者在這些期限之前完成移轉。

* **資源與支援**

   * Adobe Experience League提供檔案、逐步指南和常見問答。
   * Adobe提供沙箱環境、Zendesk票務和移轉會議等支援。

* **問答重點**

   * REST API v2需要重新驗證，因為它無法向下相容於v1。
   * 預先授權是用於UI用途，而媒體權杖需要授權。
   * 透過新的Adobe服務權杖支援SSO。

