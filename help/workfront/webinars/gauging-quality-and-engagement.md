---
title: 詢問專家 — 評估質量和參與
description: 學習構建可回答質量和接洽問題的報告。 本網路研討會於2019年11月13日錄制。
activity: use
doc-type: feature video
team: Technical Marketing
kt: 9914
source-git-commit: edd0bdb28a9b3d065a64a95af6a216b747577c77
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 1%

---

# 詢問專家 — 評估質量和參與

學習構建可回答質量和接洽問題的報告。 本網路研討會於2019年11月13日錄制。

>[!VIDEO](https://video.tv.adobe.com/v/341120/?quality=12)

## 問答

**問題**

有些欄位可用於篩選，但在嘗試按它們分組時不可用。 你是否在努力讓他們選擇一致？

**回答**

報告工具將不允許您按動態欄位或可同時選擇多個子欄位（如複選框欄位）進行分組。 您只能對具有單個值的欄位進行分組，即使它們可能有許多選擇。

您可以按複選框進行篩選並查看它們，但是不能對它們進行分組。

**問題**

在job-roles的小版本示例中，是否可以顯示主要的粗體？

**回答**

在迭代中，我們可以確定主作業角色。 我們需要在valueexpression中執行此操作，但在valueexpression中不會識別HTML代碼。 因此，我們需要找到另一種方法來確定角色是主角色。 我在此代碼中的主角色名稱前後放置「**」。 試試看你喜歡什麼：

```
displayname=All Job Roles 
listdelimiter=<p> 
listmethod=nested(userRoles).lists 
textmode=true
type=iterate 
valueexpression=IF({user}.{roleID}={role}.{ID},CONCAT("**",{role}.{name},"**"),{role}. {name})
valueformat=HTML
```

這樣，您就可以得到一個清單：

```
Support Engineer 
QA Engineer 
**Designer**
```

其中，設計器是此用戶的主要角色。

**問題**

嗨！ 我正在為我們的編輯團隊構建一個工作流，用於跟蹤文章在其生命週期中的位置（初始寫作 — >部門評論 — >最終編輯 — >發佈）。 他們希望輕鬆查看當前所在的里程碑或任務。 我得到的反饋是標準的里程碑視圖（帶有紅色或綠色底紋）太「忙碌而複雜」。 是否有方法在表或網格中僅顯示「項目名稱」和「當前里程碑」？

**回答**

可以。您可以建立一個任務報告，該報告將顯示當前正在處理的里程碑任務及其關聯的任務。 您可以在表或清單報告中執行此操作。

**問題**

我們能否在報告中將證據資訊與項目資訊結合起來？

**回答**

如果已建立「證明批准」報告，則可以使用文本模式將項目資訊拖入列中。 例如，如果要引用列中的項目名稱，可以使用以下方法：

```
displayname=Project Name
textmode=true 
valuefield=documentVersion:document:project:name 
valueformat=HTML
```

**問題**

我還希望瞭解有關與項目相關的證據資料的更多資訊。 例如，包含證明決策和注釋的項目報告。

**回答**

為了在單個報告中引用項目資訊和證明資訊，您需要建立證明批准報告。 目前，無法將證明中的注釋拉入此報表，但是，每個證明批准者決定都可以在其自己的行項目的「批准者決定」列下找到。

**問題**

我經常使用共用列來建立單頁狀態（許多列）。 但是，我發現，如果在建立報告後，我想在頁面頂部添加一個列，則返回並修改會非常耗時。 您是否有進行此類更改的提示或技巧？

**回答**

如果要將列置於文本模式清單的頂部，則只需手動對列重新編號。

但是，如果您已經建立了報告，其中第一列是一些共用列，並且希望將另一個共用列放在清單的頂部，則這會更容易。

在「報告」編輯器中，只需添加幾個新列，然後將它們拖到「列（視圖）」螢幕的最左側。 完成此操作後，請查看以前是左欄的內容，您會注意到文本模式列號全部遞增。 根據需要將任意多個空白列拖到那裡。 在保存之前，請務必在這些空白欄中放些東西，否則它們將被去除。

**問題**

您好 — 關於最終的Bug報告 — 如果多個項目出現Bug，如何為多個項目完成報告？

**回答**

您可以根據您對工作的組織方式按項目組合或項目進行篩選。

您還可以對請求隊列進行篩選。 您可能希望為每個項目設定請求隊列，在該隊列中，您可以將客戶用戶建立為「審閱者」，以直接登錄票證並將票證提交到您與他們共用的請求隊列。

**問題**

第一份報告基於項目/項目名稱，是否也可以對任務進行分組，如果是，最好的分組方式是什麼，因為任務名稱可能經常不同……謝謝！

**回答**

所有這些報告都可以作為任務、問題或項目報告完成，具體取決於您決定如何跟蹤事項。

對任務進行分組的一種常見方法是，首先按其項目名稱對任務進行分組，然後按每個項目中的任務名稱對其進行分組。 這樣，如果您有兩個同名任務，則很容易看到其中的哪個項目。

**問題**

我想知道哪些證據未結、它們與哪些任務和項目關聯、路由時間、到期時間以及誰是審閱人和批准人。

**回答**

在「證明批准」報表中，可以通過「等待決定」>「等於」>「真」篩選未清證明。 「批准者」有一列，它將告訴您誰尚未做出決定。

您可以引用任務或項目證明與使用文本模式相關聯（請參閱下面的示例）。

```
displayname=Task Name
textmode=true 
valuefield=documentVersion:document:task:name 
valueformat=HTML
```

```
displayname=Project Name
textmode=true 
valuefield=documentVersion:document:project:name
valueformat=HTML
```

至於工藝路線日期、到期日期和版主，這些欄位當前不能被拉入任何Workfront的報表，因此您需要直接按一下校樣以查看該資訊。

**問題**

您是否可以設定一個自定義表單，以便在請求者的請求完成後自動將其發送給請求者？ 比如「客戶滿意度」調查？

**回答**

有一件事你可以做以滿足你的需要。 您可以將提醒通知附加到在輸入實際完成日期後將電子郵件發送到「輸入者」的問題。 「輸入者」是建立問題的人。

您會像我們在網路研討會中一樣建立提醒通知，以「提醒填寫後操作審閱(AAR)」，但這將是問題提醒。 您可能希望為其建立電子郵件模板，並提供指向調查的連結。 您必須手動將提醒通知應用於每個問題（或使用批量編輯）。

整合會更好，因為它可以自動執行手動步驟，但提醒通知可以立即完成。

**問題**

我建立了一個按模板類型顯示項目的報告。 我可以列出項目所有者，但不能列出分配給項目的人員。

**回答**

如果要將「項目團隊」（「人員配備」頁籤）納入項目報告中的列，則需要通過文本模式建立此列。 文本模式如下：

```
displayname=Staffing 
listdelimiter=<p> 
listmethod=nested(projectUsers).lists 
textmode=true
type=iterate 
valuefield=user:name 
valueformat=HTML
```

## AAR項目報表的文本模式代碼

```
column.0.displayname=Task Details
column.0.value=<b>Project Name:</b>&nbsp;
column.0.valueformat=HTML
column.0.sharecol=true
column.1.valuefield=project:name
column.1.valueformat=HTML
column.1.sharecol=true
column.2.value=<br>
column.2.valueformat=HTML
column.2.sharecol=true
column.3.value=<b>Task Name:</b>&nbsp;
column.3.valueformat=HTML
column.3.sharecol=true
column.4.valuefield=name
column.4.valueformat=HTML
column.4.sharecol=true
column.5.value=<br>
column.5.valueformat=HTML
column.5.sharecol=true
column.6.value=<b>Task Owner:</b>&nbsp;
column.6.valueformat=HTML
column.6.sharecol=true
column.7.valuefield=assignedTo:name
column.7.valueformat=HTML
column.7.sharecol=true
column.8.value=<br>
column.8.valueformat=HTML
column.8.sharecol=true
column.9.value=<b>Actual Completion Date:</b>&nbsp;
column.9.valueformat=HTML
column.9.sharecol=true
column.10.valuefield=actualCompletionDate
column.10.valueformat=HTML
column.11.displayname=Name of Reviewer
column.11.linkedname=Name of Reviewer
column.11.namekey=view.relatedcolumn
column.11.namekeyargkey.0=Name of Reviewer
column.11.namekeyargkey.1=name
column.11.querysort=DE:Name of Reviewer:name
column.11.valuefield=Name of Reviewer:name
column.11.valueformat=customReferenceObjectAsString
column.12.displayname=AAR 1
column.12.description=In your view, does the work match stakeholders’ expectations? Did we achieve the intended results?
column.12.value=<b>AAR 1 Score:</b>&nbsp;
column.12.valueformat=HTML
column.12.sharecol=true
column.13.valuefield=AAR 1 - In your view, does the work match stakeholders’ expectations? Did we achieve the intended results?
column.13.valueformat=customDataLabelsAsString
column.13.sharecol=true
column.14.value=<br>
column.14.valueformat=HTML
column.14.sharecol=true
column.15.value=<br><b>AAR 1 User Comment:</b>&nbsp;
column.15.valueformat=HTML
column.15.sharecol=true
column.16.valuefield=AAR 1 User Comment
column.16.valueformat=customDataLabelsAsString
column.17.linkedname=direct
column.17.namekey=AAR 1 Reviewer Comment
column.17.querysort=DE:AAR 1 Reviewer Comment
column.17.valuefield=AAR 1 Reviewer Comment
column.17.valueformat=customDataLabelsAsString
column.18.linkedname=direct
column.18.displayname=AAR 1 Needs Attn
column.18.querysort=DE:AAR 1 Needs Attention
column.18.valuefield=AAR 1 Needs Attention
column.18.valueformat=customDataLabelsAsString
column.19.linkedname=direct
column.19.displayname=AAR 1 Needs Attn Notes
column.19.querysort=DE:AAR 1 Needs Attention Notes
column.19.valuefield=AAR 1 Needs Attention Notes
column.19.valueformat=customDataLabelsAsString
column.20.displayname=AAR 2
column.20.description=Do You Believe This Work Will Make an Impact?
column.20.value=<b>AAR 2 Score:</b>&nbsp;
column.20.valueformat=HTML
column.20.sharecol=true
column.21.valuefield=AAR 2 - Do You Believe This Work Will Make an Impact?
column.21.valueformat=customDataLabelsAsString
column.21.sharecol=true
column.22.value=<br>
column.22.valueformat=HTML
column.22.sharecol=true
column.23.value=<br><b>AAR 2 User Comment:</b>&nbsp;
column.23.valueformat=HTML
column.23.sharecol=true
column.24.valuefield=AAR 2 User Comment
column.24.valueformat=customDataLabelsAsString
column.25.linkedname=direct
column.25.namekey=AAR 2 Reviewer Comment
column.25.querysort=DE:AAR 2 Reviewer Comment
column.25.valuefield=AAR 2 Reviewer Comment
column.25.valueformat=customDataLabelsAsString
column.26.linkedname=direct
column.26.displayname=AAR 2 Needs Attn
column.26.querysort=DE:AAR 2 Needs Attention
column.26.valuefield=AAR 2 Needs Attention
column.26.valueformat=customDataLabelsAsString
column.27.linkedname=direct
column.27.displayname=AAR 2 Needs Attn Notes
column.27.querysort=DE:AAR 2 Needs Attention Notes
column.27.valuefield=AAR 2 Needs Attention Notes
column.27.valueformat=customDataLabelsAsString
column.28.displayname=AAR 3
column.28.description=Are you proud of the work you did on this?
column.28.value=<b>AAR 3 Score:</b>&nbsp;
column.28.valueformat=HTML
column.28.sharecol=true
column.29.valuefield=AAR 3 - Are you proud of the work you did on this?
column.29.valueformat=customDataLabelsAsString
column.29.sharecol=true
column.30.value=<br>
column.30.valueformat=HTML
column.30.sharecol=true
column.31.value=<br><b>AAR 3 User Comment:</b>&nbsp;
column.31.valueformat=HTML
column.31.sharecol=true
column.32.valuefield=AAR 3 User Comment
column.32.valueformat=customDataLabelsAsString
column.33.linkedname=direct
column.33.namekey=AAR 3 Reviewer Comment
column.33.querysort=DE:AAR 3 Reviewer Comment
column.33.valuefield=AAR 3 Reviewer Comment
column.33.valueformat=customDataLabelsAsString
column.34.linkedname=direct
column.34.displayname=AAR 3 Needs Attn
column.34.querysort=DE:AAR 3 Needs Attention
column.34.valuefield=AAR 3 Needs Attention
column.34.valueformat=customDataLabelsAsString
column.35.linkedname=direct
column.35.displayname=AAR 3 Needs Attn Notes
column.35.querysort=DE:AAR 3 Needs Attention Notes
column.35.valuefield=AAR 3 Needs Attention Notes
column.35.valueformat=customDataLabelsAsString
column.36.displayname=Done
column.36.valuefield=Review Complete
column.36.valueformat=customDataLabelsAsString
```
