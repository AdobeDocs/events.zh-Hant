---
title: 使用網頁元件捲動您自己的HTML
description: 透過Raymond Camden， Sr.學習Web元件基本知識。Adobe的開發人員宣傳專員，包括自訂元素、陰影DOM和HTML範本，並提供內嵌PDF和建立可排序表格等實務範例，以增強您的應用程式。
topic: Development
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 2580
last-substantial-update: 2024-11-26T00:00:00Z
jira: KT-16579
source-git-commit: 8770c8172ee90524079efc65aec7e129f1d1d031
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---


# 使用網頁元件捲動您自己的HTML

與Adobe的資深開發人員宣傳專員Raymond Camden一起瞭解Web元件基本知識，包括自訂元素、陰影DOM和HTML範本。 探索內嵌PDF和建立可排序表格等真實世界的範例，以透過可重複使用的現代解決方案增強您的應用程式。

>[!VIDEO](https://video.tv.adobe.com/v/3440406/?learn=on&enablevpops)

## 社群討論

在Adobe Developers Live社群[討論區](https://adobe.ly/48PRE63)中繼續交談。

## 重點提要

* **網頁元件簡介**&#x200B;網頁元件可讓開發人員建立自訂HTML元素，使其具有使用JavaScript定義的外觀和互動性。
* **核心技術** Web元件是使用三種核心技術建置：自訂元素**陰影DOM和HTML範本。
* **自訂元素**&#x200B;自訂元素可建立新的HTML標籤。 它們必須使用串音大小寫並包含破折號。 JavaScript類別是用來定義其行為。
* **陰影DOM**&#x200B;陰影DOM為元件的DOM樹狀結構提供封裝，避免CSS洩漏並允許更受控制的樣式。
* **HTML範本** HTML範本允許HTML的定義和可複製並附加至DOM的CSS。 不過，簡報者偏好使用插槽，而非範本，以提升發佈與彈性。
* **屬性和事件**&#x200B;自訂元素可以有屬性和事件處理常式（例如connectedCallback和disconnectedCallback），以便管理從DOM新增或移除時的行為。
* **位置**&#x200B;位置允許將內容插入至Web元件，同時支援預設和具名位置，以便更靈活的內容管理。
* **真實世界的範例**&#x200B;範例包括PDF內嵌檢視器、影像預留位置及表格排序器，以示範Web元件的實際應用程式。
* 如果JavaScript無法載入，**漸進式增強功能** Web元件可以增強現有HTML而不會中斷功能。
* **後續步驟和資源**&#x200B;簡報建議探索表單參與率、宣告式陰影DOM、自訂HTML屬性以及伺服器端轉譯。 資源包括MDN、webcomponents.org以及Ben Farrell的《Web Components in Action》一書。