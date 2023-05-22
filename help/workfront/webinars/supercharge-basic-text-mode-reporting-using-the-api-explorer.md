---
title: 使用API瀏覽器詢問專家 — Supercharge基本文本模式報告
description: 瞭解API瀏覽器、如何使用它以及如何利用基本文本模式增強報告。 本網路研討會於2020年1月22日錄制。
activity: use
doc-type: feature video
team: Technical Marketing
kt: 9918
source-git-commit: edd0bdb28a9b3d065a64a95af6a216b747577c77
workflow-type: tm+mt
source-wordcount: '1658'
ht-degree: 2%

---

# 使用API瀏覽器詢問專家 — Supercharge基本文本模式報告

瞭解API瀏覽器、如何使用它以及如何利用基本文本模式增強報告。 本網路研討會於2020年1月22日錄制。

>[!VIDEO](https://video.tv.adobe.com/v/341124/?quality=12)

## 其他資源

![顯示文本模式代碼規則示例的圖表](assets/text-mode-chart.png)


**最終「所有作業角色」列**

```
description="Primary =" indicates the user's primary job role
displayname=All Job Roles
listdelimiter=<p>
listmethod=nested(userRoles).lists
textmode=true
type=iterate
valueexpression=IF({user}.{roleID}={role}.{ID},CONCAT("Primary = ",{role}.{name}),{role}.{name})
valueformat=HTML
```

**「所有團隊」列的文本模式**

```
displayname=All Teams
listdelimiter=<p>
listmethod=nested(teams).lists
textmode=true
type=iterate
valueexpression={name}
valueformat=HTML
```

**「所有組」列的文本模式**

```
displayname=All Groups
listdelimiter=<p>
listmethod=nested(userGroups).lists
textmode=true
type=iterate
valuefield=group:name
valueformat=HTML
```

**「直接報告」列的文本模式**

```
displayname=Direct Reports
listdelimiter=<p>
listmethod=nested(directReports).lists
textmode=true
type=iterate
valueexpression={name}
valueformat=HTML
```

## 問答

**問題**

是否可以使用文本模式在報表中使用任何集合？

**回答**

是，可以使用集合區域中的任何對象。 您將希望瀏覽並查看您有權訪問的內容。 並非所有元件都具有訪問用戶對象和作業角色對象的權限，就像我們在API資源管理器中看到的用戶角色對象一樣。

**問題**

您能否討論「在同一列中使用不同集合的條件（項目更新與任務更新）」

**回答**

在小版本區域中，看到值欄位或值表達式時，該表達式會訪問集合清單中的一個項。 使用valuefield ，我們可以獲取該作業角色的名稱，例如，或清單中該項中的任何內容。 如果您在任務中，則任務對象可以引用它所在的項目。

**問題**

是否可以討論「任務更新集合僅能在任務報告中進行？」

**回答**

在建立問題報告時，如果針對任務報告了問題，則可以查看任務資訊，並且還可以從集合中查看該資訊。 除了這些情況外，您需要在任務報告中才能查看任務收集資料。

**問題**

是否共用文本格式([!DNL CSS])示例？

**回答**

Workfront不支援 [!DNL CSS] 的子菜單。

**問題**

查找自定義欄位名稱的最佳或最快的方法是什麼？ 我在瀏覽器或中使用了HTML編輯選項，方法是在報表中添加一個欄位，然後切換到文本模式來獲取它……好奇別人是怎麼做到的

**回答**

我發現在UI中選擇欄位最快，然後切換到文本模式並複製欄位名稱。 這可確保我獲得該欄位的正確拼寫。

**問題**

如何使用文本模式來標識報表中團隊的成員？ 我們當前在任務審批工作流中使用團隊分配，希望將當前審批階段的團隊成員列在與「批准者和狀態」(Approvers and Status)欄位的工作方式類似的列中。

**回答**

為了引用與當前審批階段關聯的團隊成員，您需要引用引用的集合的集合，而當前無法通過Workfront的文本模式功能來引用該集合。 您的組織當前使用的列顯示與批准關聯的團隊是您的最佳選項。

**問題**

欄位和對象名稱是否必須為Por Case(例如 角色與角色)?

**回答**

在文本模式下引用對象時，您將希望完全按照API資源管理器的右欄顯示的方式來寫入對象。 例如，如果要從任務報表中引用項目名稱，則值欄位將如下所示：

```
valuefield=project:name
```

但是，在「問題」的情況下，在API瀏覽器中將這些任務稱為opTask。 因此，如果要運行「小時」報告，並要為「問題名稱」添加列，則值欄位將如下所示：

```
valuefield=opTask:name
```

**問題**

我希望構建一個報告，顯示每個項目當前正在處理的活動任務。 我最好怎麼做？ 我想，還會添加項目資訊列的任務報告嗎？

**回答**

沒錯。 任務報告最適合這一點。 您需要定義「活動任務」。 如果使用前置任務，則這將是「就緒」任務。 因此，您可以按「就緒」=「真」進行篩選。 這將引入任何「準備啟動」任務。 然後，我建議您按項目名稱分組，這樣您的任務就都分組在一起，您一眼就可以看到哪些任務屬於哪個項目。

**問題**

是否有一種方法來建立計算資料的報告 — 例如，滿足特定條件的項目百分比？

**回答**

建立報告以呈現或計算資料（例如%）的最佳方法是將分組應用於報告，然後應用圖表。 如果要向報表添加餅圖，則可以選擇餅圖切片的值或百分比。

**問題**

是否可以使用文本模式來標識分配給當前任務審批階段的團隊成員，類似於「批准者和狀態」列？

**回答**

您需要在「任務」報告中添加文本模式下的收集列，其中包括以下內容：

```
displayname=Current Approval Stage Approvers 
listdelimiter=<p> 
listmethod=nested(currentApprovalStep.stepApprovers).lists 
textmode=true
type=iterate 
valuefield=user:name 
valueformat=HTML
```

**問題**

是否可以篩選所有組包含特定組的位置？

**回答**

如果要篩選報告中的項，則應在報告的篩選器頁籤下進行篩選。 因此，如果您只想看到其組中的一個是Accounting的用戶，您會添加一個過濾規則，該規則說：

```
Other Groups>ID>Equal>Accounting
```

**問題**

是否有一種方法來建立確定任務組合的實際持續時間的報告？

**回答**

您需要篩選報告，以便只包括所需任務的組合。 然後，您需要在視圖中放置一個「實際持續時間」列，並在「列設定」中按「總」進行匯總，最後，您需要以某種方式對報告進行分組。 運行報表時，分組欄將顯示分組行中包含的實際持續時間的總和。

**問題**

是否有方法減去父項下的任務以確定父項下其餘任務的持續時間？

**回答**

通過從父任務下最近結束任務的結束日期中減去最早開始任務的起始日期，計算父任務的持續時間。 在報告中，您只知道是否顯示正在考慮的每個任務。 報表引擎無法保留某個任務中的資訊，並在查看另一個任務時使用它。 因此，要完成您所要求的任務，唯一的方法是刪除某個任務在項目任務清單中位於某個父項之下，並觀察父項任務的持續時間如何重新計算。

**問題**

對於條件分組，自定義格式（請考慮「西方國家」、「中央國家」、「東部國家」）來解碼各個組是一種常見技術，在此說明上，您建議何時使用計算分組而不是計算參數？

**回答**

計算分組（又稱分組中的值表達式）是獲取在分組欄中顯示結果的便捷方法。 也可以使用計算的自定義欄位來完成此操作。 每種方法都有利和弊，它們是：

* 每次刷新瀏覽器頁面時，都會計算值表達式。 這可能比計算的自定義欄位更好，這些自定義欄位在編輯其附加到的對象時重新計算，或在批量編輯中重新計算計算欄位時重新計算，或在編輯自定義表單並選擇「更新以前的計算」選項時重新計算。
* 但是，不能在圖表、條件格式或篩選器中使用值表達式。 您需要為這些欄位使用計算的自定義欄位。

**問題**

是否無法將分組顯示名稱從「無值」更改為我們選擇為報告目的而調用它的任何其他名稱？ 換句話說，它永遠是&quot;無價值&quot;?

**回答**

有一種方法用不同的東西來取代&quot;無價值&quot;。 假設您有按Portfolio名稱分組的項目報告。 所有未分配給項目組合的項目將最終以標題分組：

```
Portfolio: Name: No Value
```

要更改此設定，請以文本模式編輯分組並替換此行：

```
group.0.valuefield=portfolio:name
```

使用此行：

```
group.0.valueexpression=IF(ISBLANK({portfolio}.{name}),"Not in any Portfolio",{portfolio}.{name})
```

分組現在將具有以下標題：

```
Portfolio: Name: Not in any Portfolio
```

**問題**

是否有一個參數來跟蹤未完成的分配，例如：

1. 沒有為其分配個人的單個分配的任務或
1. 具有多個分配的任務，這些分配至少為請求的角色具有一個未分配的個人

**回答**

這可以通過使用「分配報告」和篩選

```
Assigned To ID > Is Blank and Role ID > Is Not Blank
```

這將納入已分配給角色的所有任務或問題，但不一定是特定用戶。 您需要為「任務」和「問題」名稱添加列，以查看分配屬於哪個對象，如果按項目名稱分組，則有助於保持分配的有序性。

**問題**

恰克，我忘了，但是你是否記得，在懸停時，以文本模式呈現的屬性會作為工具提示呈現？

**回答**

description=允許在懸停在列標題上時顯示工具提示。

**問題**

是否可以報告允許多個選擇但僅將第一個選擇納入報告的複選框欄位？

**回答**

可以。複選框欄位中的選定選項全部在一個字串中，每個選項用逗號分隔。 您將使用SEARCH表達式在複選框欄位中查找第一個逗號的位置，然後將該索引與LEFT表達式一起使用，從清單的開頭顯示這麼多字元。 代碼如下：

```
valueexpression=IF(SEARCH(",",{DE:Checkbox Field},0)>0,LEFT({DE:Checkbox Field},SEARCH(",",{DE:Checkbox Field},0)),{DE:Checkbox Field})
```

如果在複選框欄位中的選擇名稱中使用逗號，則只會將該選擇的部分顯示到第一個逗號。
