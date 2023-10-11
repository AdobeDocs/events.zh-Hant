---
title: 詢問專家 — 使用API Explorer製作超額基本文字模式報表
description: 瞭解API Explorer、其使用方式，以及如何運用基本文字模式來增強報表。 此網路研討會錄製於2020年1月22日。
activity: use
doc-type: feature video
team: Technical Marketing
kt: 9918
exl-id: f859c4eb-8b3c-4d91-9765-9957dc4678f5
source-git-commit: 1792dc318643aec2c12613f621361d72a7a918b1
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 2%

---

# 詢問專家 — 使用API Explorer製作超額基本文字模式報表

瞭解 [[!UICONTROL API總管]](https://developer.adobe.com/workfront/api-explorer/)，如何使用它，以及如何運用基本文字模式來增強報表。 此網路研討會錄製於2020年1月22日。

>[!VIDEO](https://video.tv.adobe.com/v/341124/?quality=12)

## 其他資源

![顯示文字模式程式碼規則範例的圖表](assets/text-mode-chart.png)


**最後「所有職位角色」欄**

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

**「所有團隊」欄的文字模式**

```
displayname=All Teams
listdelimiter=<p>
listmethod=nested(teams).lists
textmode=true
type=iterate
valueexpression={name}
valueformat=HTML
```

**「所有群組」欄的文字模式**

```
displayname=All Groups
listdelimiter=<p>
listmethod=nested(userGroups).lists
textmode=true
type=iterate
valuefield=group:name
valueformat=HTML
```

**「直接下屬」欄的文字模式**

```
displayname=Direct Reports
listdelimiter=<p>
listmethod=nested(directReports).lists
textmode=true
type=iterate
valueexpression={name}
valueformat=HTML
```

## Q&amp;A

**問題**

是否可以使用文字模式，在報表中使用任何集合？

**回答**

可以，您可以使用收藏集中的任何物件。 您想要探索並檢視您有權存取的內容。 並非所有專案都能存取使用者物件和工作角色物件，就像我們在API總管中看到的「使用者角色」物件一樣。

**問題**

您可以討論「相同欄中不同集合的條件使用（專案更新與任務更新）」嗎

**回答**

當您在反複專案區域中，並且看到那裡的valuefield或valueexpression時，表示正在存取您的集合清單中的其中一個專案。 例如，使用值欄位，我們可獲得該工作角色的名稱，或清單中該專案中的任何內容。 如果您在任務中，任務物件可以參照它所在的專案。

**問題**

您可以討論「任務更新集合是否只能在任務報告中進行？」

**回答**

當您建立問題報告時，如果問題是根據任務報告的，則可以檢視任務資訊，並且您也可以在集合中檢視該資訊。 除了這些情況，您需要在任務報告中才能檢視任務收集資料。

**問題**

您可以共用文字格式嗎([!DNL CSS])範例？

**回答**

Workfront不支援 [!DNL CSS] 在文字模式中。

**問題**

尋找自訂欄位名稱的最佳或快速方式為何 — 適用於文字模式報表？ 我已在瀏覽器中使用HTML編輯選項，或在報表中新增欄位並切換到文字模式以抓取它，但……奇怪其他人如何執行此動作

**回答**

我發現在UI中選取欄位然後切換到文字模式並複製欄位名稱是最快的。 這樣可確保我獲得正確的欄位拼字。

**問題**

如何使用文字模式在報告中識別團隊成員？ 我們目前在任務核准工作流程中使用團隊指派，並希望在類似「核准者」和「狀態」欄位運作方式的欄中，列出目前核准階段中的團隊成員。

**回答**

若要參照與目前核准階段相關聯的專案團隊成員，您需要參照參照集合的集合，目前透過Workfront的文字模式功能無法做到這點。 您的組織目前正在使用的欄會顯示與核准相關聯的團隊，這是您的最佳選項。

**問題**

欄位和物件名稱是否必須為正確的大小寫(例如， 角色vs角色)？

**回答**

當您以文字模式參考物件時，您會想要將它寫成與API Explorer右欄顯示的完全一樣。 例如，如果您想從「任務」報告參考「專案」名稱，您的值欄位將如下所示：

```
valuefield=project:name
```

但是，如果發生問題，這些任務在API Explorer中稱為opTasks。 因此，如果您要執行時數報告並想要為問題名稱新增欄，則值欄位將如下所示：

```
valuefield=opTask:name
```

**問題**

我想要建置一份報告，顯示每個專案目前執行中的任務。 我應該怎麼做？ 我想它會是一個任務報告，其中也會新增專案資訊欄？

**回答**

沒錯。 最好使用任務報告。 您需要定義「作用中任務」。 如果您使用前置任務，這將會是已準備就緒的任務。 因此您可以依「就緒= True」來篩選。 這會帶入任何已準備好開始的任務。 接著，我建議您依「專案名稱」分組，如此一來，您的任務就會全部分組在一起，而您可以一目瞭然地看到哪些任務屬於哪一個專案。

**問題**

是否有方法可以建立報表來計算資料，例如，符合特定條件的專案百分比？

**回答**

建立報表以顯示或計算資料（例如%）的最佳方式是將分組套用至報表，然後套用圖表。 如果要將圓形圖新增到報表中，您可以選擇圓形圖切片使用值或百分比。

**問題**

您能否使用文字模式來識別指派給類似「核准者」和「狀態」欄目前任務核准階段的團隊成員？

**回答**

您需要以文字模式將集合欄新增至「任務」報表，其中包含以下專案：

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

您是否能篩選出所有群組都包含特定群組的位置？

**回答**

如果要篩選報告中的專案，可在報告的篩選標籤下進行。 因此，如果您只想檢視其中一個群組為Accounting的使用者，您可新增篩選規則，指出：

```
Other Groups>ID>Equal>Accounting
```

**問題**

是否有方法可以建立報告，以決定任務組合的實際持續時間？

**回答**

您需要篩選報告以僅包含您想要的任務組合。 然後，您需要在檢視中放入「實際持續時間」欄，並在「欄設定」中依「總和」摘要該欄，最後，您需要以某種方式將報表分組。 當您執行報表時，分組列將顯示分組列中包含的實際期間總數。

**問題**

是否有方法可以減去屬於父系的任務，以判斷屬於父系下其餘任務的持續時間？

**回答**

計算父系任務的期間的方法是從該父系下最近結束任務的結束日期減去最早開始任務的開始日期。 在報表中，您只知道考量是否要顯示的每個個別任務。 報表引擎無法保留一項任務的資訊，並在檢視另一項任務時使用這些資訊。 因此，要完成您所要求的任務，唯一的方法是移除在專案任務清單中的任務，並觀察父系任務的持續時間如何重新計算。

**問題**

對於條件分組，解碼個別群組的自訂表單（想一下「西部國家」、「中部國家」、「東部國家」）是適用於該附註的常見技巧，何時建議使用計算分組與計算引數？

**回答**

計算分組（亦即分組中的值運算式）是取得結果以顯示於分組列的便利方式。 您也可以使用計算自訂欄位來完成此操作。 每種方法都有優缺點，包括：

* 每次重新整理瀏覽器頁面時，都會計算值運算式。 這可能優於已計算自訂欄位，當編輯其附加的物件時、或在大量編輯中重新計算已計算欄位時、或在編輯自訂表單並選取「更新先前的計算」選項時，重新計算自訂欄位。
* 不過，值運算式無法用於圖表、條件式格式或篩選。 您需要針對這些使用計算自訂欄位。

**問題**

無法將群組顯示名稱從「沒有值」變更為任何我們選擇用於報表用途的其他名稱嗎？ 換句話說，永遠是「沒有值」？

**回答**

有方法可將「沒有值」取代為其他值。 假設您有一個依Portfolio名稱分組的專案報告。 所有未指派給投資組合的專案最終將歸入具有標題的群組中：

```
Portfolio: Name: No Value
```

若要變更此專案，請在文字模式中編輯群組並取代此行：

```
group.0.valuefield=portfolio:name
```

行：

```
group.0.valueexpression=IF(ISBLANK({portfolio}.{name}),"Not in any Portfolio",{portfolio}.{name})
```

群組現在將具有此標題：

```
Portfolio: Name: Not in any Portfolio
```

**問題**

是否有引數可追蹤未完成的指派，例如：

1. 具有單一工作分派，但未指派個人給它的任務，或
1. 具有多個指派的任務，這些指派至少有一個未指派個人負責請求的角色

**回答**

您可以透過使用指派報告並篩選來完成

```
Assigned To ID > Is Blank and Role ID > Is Not Blank
```

這會提取已指派給角色但未一定指派給特定使用者的所有任務或問題。 您需要為任務和問題名稱新增欄，以檢視指派屬於哪個物件，如果按專案名稱分組，則應有助於保持其井然有序。

**問題**

Chuck，我忘了，但您記得文字模式中的屬性嗎？停留在游標上時，該屬性隨後會呈現為工具提示。

**回答**

description=可讓您在欄標題上暫留時顯示工具提示。

**問題**

我可以在允許多重選取，但只將第一個選取提取到報表中的核取方塊欄位上製作報表嗎？

**回答**

可以。核取方塊欄位中選取的選擇全部為一個字串，每個選擇以逗號分隔。 您將使用SEARCH運算式來尋找Checkbox欄位中第一個逗號的位置，然後將該索引與LEFT運算式一起使用，以顯示清單開頭的字元數。 程式碼如下：

```
valueexpression=IF(SEARCH(",",{DE:Checkbox Field},0)>0,LEFT({DE:Checkbox Field},SEARCH(",",{DE:Checkbox Field},0)),{DE:Checkbox Field})
```

如果您在核取方塊欄位的選取名稱中使用逗號，則只會顯示該選取專案的部分，直到第一個逗號為止。
