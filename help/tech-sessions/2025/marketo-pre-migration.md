---
title: Marketo移轉至Adobe Admin Console - （移轉前）
description: Adobe正在將Marketo Engage移轉至Admin Console，以提升使用者管理效能。 瞭解自動和自行移轉型別、先決條件、移轉後變更、最佳實務、常見陷阱和支援。 存取Adobe Experience League網站上的工作階段影片。
role: Admin, Developer, Leader, User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 2280
last-substantial-update: 2025-03-14T00:00:00Z
jira: KT-17483
exl-id: 9c3da83f-9e02-4a2e-9784-10213facf056
source-git-commit: 848fa8fee05b315361781059eabb3b19904c78c2
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Marketo移轉至Adobe Admin Console — 移轉前

加入我們，與Adobe專家一起順暢地移轉Marketo！

透過此資訊豐富的網路研討會，與Adobe的客戶體驗與身分團隊搶先體驗Marketo移轉。 我們將逐步解說重要步驟、最佳實務和常見挑戰，以確保順利轉換至Adobe Admin Console。

您將學到什麼，

* 移轉前程式的逐步藍圖
* 簡化轉換過程並避免陷阱的最佳實務
* 專家解答常見的移轉問題

無論您是剛開始移轉或準備最後步驟，本課程都能協助您掌握相關知識和工具，安心地完成整個過程。 不要錯過這個機會，以取得領先優勢，讓Marketo順利遷移！

>[!VIDEO](https://video.tv.adobe.com/v/3449712/?learn=on&enablevpops)

## 重要技巧

### 移轉的用途與概覽

Adobe正在將Marketo Engage移轉至Admin Console，以便將所有產品整合到一個中心，提供更優異的使用者管理和存取能力。  Admin Console將做為管理Adobe產品、使用者角色、許可權和支援存取的中央中樞。 存取Marketo Engage的URL將變更為Adobe的Experience Cloud平台。

### 移轉型別

* **自動移轉**&#x200B;針對使用者少於75名且沒有SSL設定的組織。 Adobe會處理移轉。
* **自助移轉**&#x200B;適用於具有SSL設定的組織。 管理員可使用移轉主控台管理移轉程式。

### 移轉的必要條件

* 系統管理員必須完成同意電子郵件。
* SSL必須在Admin Console (而非Marketo執行個體)中設定。

### 移轉後變更

* 使用者將使用Adobe ID或Federated ID (SSL)登入。
* 管理員角色和許可權將決定Admin Console中的存取層級。

### 最佳實務

* 在移轉之前，驗證使用者電子郵件並解決鎖定的帳戶。
* 確保指派適當的管理員角色。
* 停用廣告封鎖程式或使用無痕模式以避免登入問題。

### 常見陷阱

* 不正確的管理員許可權可能會限制存取權。
* 瀏覽器擴充功能和廣告封鎖程式可能會干擾存取。
* Admin Console尚未支援IP白名單，不過正在開發中。

### 對功能的影響

* 自動傳送的電子郵件、API使用者和Munchkin程式碼不受移轉的影響。
* 移轉主要影響使用者驗證和管理。

### 支援

* 遇到問題的使用者應向Adobe客戶服務提出支援案例。
* 在支援案例中加入IMS組織ID以更快解決問題。
