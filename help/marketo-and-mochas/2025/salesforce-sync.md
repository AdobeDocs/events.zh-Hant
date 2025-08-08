---
title: Marketo與Mochas - Salesforce同步
description: 使用許可權、欄位可見度、管理員共同作業和最佳實務方面的專家指引，掌握Marketo-Salesforce同步功能，以確保順暢、最佳化的整合。
feature: Salesforce Integration
topic: Integrations
role: Admin, Developer, Leader, User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 3547
last-substantial-update: 2025-08-07T00:00:00Z
jira: KT-18706
source-git-commit: bc5752512fb1bc50cefe0180c308574e821888a2
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 0%

---


# Marketo與Mochas：Salesforce同步

Marketo只有很少的原生整合，但Salesforce是其中最強大的。 由於約90%的Marketo客戶也使用Salesforce，Adobe致力於為客戶提供建議，協助他們理化、診斷並最佳化兩者之間的同步作業。 Marketo與SFDC的同步主要是以SFDC中授與Marketo同步使用者的ID許可權為基礎。 由於多個管理員或不同團隊圍繞系統中的更新建立溝通獨立單位，因此客戶可能很難做到這一點。

此網路研討會會說明與Marketo &lt;-> SFDC同步相關的以下內容：

·以鳥瞰圖解方式說明同步作業
·在SFDC中向Marketo同步使用者隱藏欄位和物件
·如何與SFDC管理員通訊
·如何與Marketo支援有效合作
·將Marketo同步至SFDC時應避免的事項

>[!VIDEO](https://video.tv.adobe.com/v/3470624/?learn=on&enablevpops)

## 使用Salesforce Sync的最佳做法

若要將Salesforce與Marketo有效同步，請遵循以下最佳實務，並以簡單的術語逐步說明：

1. **瞭解同步程式**

   同步會連線Marketo和Salesforce，讓資料可在兩個系統之間流動。 您可以將「Marketo Sync使用者」視為兩個平台之間的橋樑。 此使用者擁有讀取和寫入特定資料的許可權：

   * **寫入存取權**&#x200B;銷售機會和聯絡人(Marketo可以在Salesforce中更新這些專案)。
   * **讀取存取權**&#x200B;帳戶、商機、自訂物件和活動(Marketo可以檢視這些專案，但不能變更它們)。

   當Salesforce或Marketo中的資料變更時，同步會每五分鐘更新另一個系統。 不過，您可以使用如「同步至SFDC」的流程步驟，優先處理緊急更新。

1. **清除欄位**

   僅同步目前使用的欄位。 例如：

   * 如果您有類似「COVID-19附註」等不再相關的舊欄位，請從同步處理中將其移除。 這能減少雜亂，並加快流程。
   * 避免同步公式欄位（例如「天數內的潛在客戶年齡」），因為它們不會更新時間戳記，這可能會造成問題。

1. **防止積壓**

   當過多資料等待同步時，就會發生待處理專案。 若要避免此情況：

   * 限制不必要的更新：例如，如果帳戶分數稍微變更（例如，從60變更為61），則可能會觸發所有相關連絡人的更新。 相反地，請將分數分組到範圍（例如，0-25、26-50）中以減少更新。
   * 批次行銷活動：使用批次行銷活動而非觸發行銷活動，以更有效率地處理資料。

1. **管理錯誤**

   當Marketo嘗試更新Salesforce中的欄位但沒有許可權時，可能會發生錯誤。 若要進行疑難排解：

   * 以Marketo同步使用者身分登入Salesforce，並嘗試執行相同的動作。 這有助於識別許可權問題或無效的資料。
   * 在Marketo中設定週期性行銷活動，以修正常見錯誤，例如將國家/州值標準化（例如「CA」到「加州」）。

1. **使用自訂同步篩選器**

   自訂篩選器可協助您控制哪些記錄在Salesforce和Marketo之間同步。 例如，建立名為「不要同步至Marketo」的欄位。 若此欄位針對記錄標示為「true」，則不會同步至Marketo。 這對於排除無效的電子郵件地址或過時的連絡人非常有用。

1. **限制任務建立**

   elm Salesforce。 將焦點放在有意義的活動上，例如「填寫的表單」或「電子郵件中的點選連結」。

1. **與您的Salesforce管理員共同作業**

   由於同步涉及兩個系統，請與Salesforce管理員密切合作，以：

   * 管理Marketo Sync使用者的許可權。
   * 清除Salesforce中不必要的欄位。
   * 一起疑難排解同步問題。

1. **監視器同步處理效能**

   請定期檢視Marketo管理員區段中的同步狀態：

   尋找「同步待處理專案趨勢」或「同步處理輸送量」儀表板中的尖峰。 這些表示延遲或過度更新。
如果您發現問題，請調查哪些欄位或記錄導致了問題。

1. **明智地使用自訂物件**

   自訂物件是特殊的資料結構，可儲存其他資訊（例如產品詳細資訊）。 僅同步行銷活動所需的自訂物件，以避免資料庫膨脹。

1. **規劃擴充性**

   設定同步時，請考慮長遠因素：

   * 維護資料字典，以追蹤已同步哪些欄位及原因。
   * 請避免同步不必要的欄位或記錄，以維持系統效率。

依照這些步驟操作，您可以確保Marketo與Salesforce之間流暢且有效的整合，將錯誤減至最少，並讓您的資料發揮最大價值。
