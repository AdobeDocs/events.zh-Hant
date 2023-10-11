---
title: 詢問專家 — 評估品質和參與度
description: 瞭解如何建立可回答品質和參與問題的報表。 此網路研討會錄製於2019年11月13日。
activity: use
doc-type: feature video
team: Technical Marketing
kt: 9914
exl-id: 76a8e418-71c7-414a-9938-e64e4e73c184
source-git-commit: 1792dc318643aec2c12613f621361d72a7a918b1
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 1%

---

# 詢問專家 — 評估品質和參與度

瞭解如何建立可回答品質和參與問題的報表。 此網路研討會錄製於2019年11月13日。

>[!VIDEO](https://video.tv.adobe.com/v/341120/?quality=12)

## Q&amp;A

**問題**

有些欄位可供篩選依據，但在您嘗試按這些欄位進行群組時無法使用。 您是否致力於使其成為一致的選項？

**回答**

報告工具不允許您依動態欄位或可一次選取多個核取方塊的欄位來分組，如核取方塊欄位。 您只能將具有單一值的欄位分組，即使它們可能有許多選擇。

您可以依核取方塊篩選和檢視，但無法將其分組。

**問題**

在工作 — 角色範例的疊代中，我可以顯示主要的一個粗體嗎？

**回答**

在反複專案中，我們可以識別主要工作角色。 我們需要在valueexpression中執行此動作，但在valueexpression中無法辨識HTML程式碼。 因此，我們需要想出另一種方法，將這個角色識別為主要角色。 在此程式碼中，我會在主要角色名稱前後放置「**」。 嘗試一下，看看您喜歡的程度：

```
displayname=All Job Roles 
listdelimiter=<p> 
listmethod=nested(userRoles).lists 
textmode=true
type=iterate 
valueexpression=IF({user}.{roleID}={role}.{ID},CONCAT("**",{role}.{name},"**"),{role}. {name})
valueformat=HTML
```

這會為您提供如下的清單：

```
Support Engineer 
QA Engineer 
**Designer**
```

其中Designer是此使用者的主要角色。

**問題**

嗨！ 我正在為我們的編輯團隊整理一個工作流程，以追蹤文章在其生命週期中的哪個階段（初始撰寫 — >部門稽核 — >最終編輯 — >發佈）。 他們想要輕鬆檢視目前所在的「里程碑」或「任務」。 我收到的意見反應是標準的「里程碑」檢視（使用紅色或綠色陰影）太「忙碌且複雜」。 是否有方式可在表格或格線中只顯示「專案名稱」和「目前的里程碑」？

**回答**

可以。您可以建立任務報告，顯示目前執行中的里程碑任務及其關聯的任務。 您可以在表格或清單報表中執行此操作。

**問題**

報告中可以有與專案資訊合併的校訂資訊嗎？

**回答**

如果您已建立校訂核准報告，則可以使用文字模式將專案資訊提取到欄中。 例如，如果您想在欄中參照專案名稱，您可以使用以下專案：

```
displayname=Project Name
textmode=true 
valuefield=documentVersion:document:project:name 
valueformat=HTML
```

**問題**

我想要更瞭解與專案相關的校訂資料的報告。 例如，包含校訂決定和評論的專案報告。

**回答**

為了在單一報告中參考專案資訊和校訂資訊，您將會想要建立校訂核准報告。 目前，無法將校訂的評論提取到此報告中，但是，每個校訂核准者決定都可以在核准者決定欄下的行專案上找到。

**問題**

我經常使用Sharecol來建立單頁狀態（許多欄）。 不過，我發現如果我建立報表後，想要在頁面頂端新增欄，非常費時地返回並修改。 您對於此類變更是否有任何秘訣或訣竅？

**回答**

如果您打算將某個欄位置於文字模式欄位清單頂端，您只需要手動將欄位重新編號即可。

但是，如果您已建立報告，第一欄是一些共用欄，並且您想將另一個共用欄放在清單頂端，這會比較容易。

在報告編輯器中，只須新增幾個欄，並將它們拖曳到「欄」 （檢視）畫面的最左側。 這樣做之後，您會發現原來是左欄的內容，而且您會注意到文字模式的欄位編號全都遞增。 請視需要拖曳儘可能多的空白欄。 儲存前，請務必在這些空白欄中放入一些內容，否則它們將會被刪除。

**問題**

嗨 — 關於最終錯誤報告 — 如何為多個專案完成報告 — 如果錯誤來自多個專案??

**回答**

您可以根據組織工作的方式，依投資組合或專案進行篩選。

您也可以依請求佇列進行篩選。 您可能會想要為每個專案設定請求佇列，您可以將客戶使用者建立為檢閱者，檢閱者可以直接登入並將票證提交至您與他們共用的請求佇列。

**問題**

第一份報告是根據專案/專案名稱，這可以在任務上同時完成，如果是這樣，分組它們的最佳方式為何，因為任務名稱可能經常不相同……謝謝！

**回答**

所有這些報告都可做為任務、問題或專案報告來完成，端視您決定追蹤事情的方式而定。

分組任務的常見方法是先按其專案名稱分組任務，然後按每個專案中的任務名稱分組任務。 這樣一來，如果您有兩個名稱相同的任務，就很容易看到他們在哪個專案中。

**問題**

我想瞭解哪些校訂尚未完成、其所繫結的任務和專案、路由的時間、到期時間，以及誰是版主和核准者。

**回答**

在校訂核准報告中，透過等待決定>等於> True可以篩選未完成的校訂。 核准者欄會告訴您尚未做出決定的人員。

您可以使用文字模式來參考校訂繫結的任務或專案（請參閱以下範例）。

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

至於路由日期、到期日和版主，這些欄位目前無法提取至任何Workfront的報告，因此您需要直接按一下校樣以檢視該資訊。

**問題**

您可以設定自訂表單，在要求完成時自動傳送給要求者嗎？ 是否為「客戶滿意度」問卷調查？

**回答**

以下是您可以做的一件事，可能會符合您的需求。 您可以將「提醒通知」附加至問題，該問題會在輸入實際完成日期後傳送電子郵件至「輸入者」。 輸入者是建立問題的人員。

您可以建立提醒通知，就像我們在「提醒填寫動作後稽核(AAR)」網路研討會中所做的那樣，只是這會是問題提醒。 您可能想要為其建立電子郵件範本，並提供問卷的連結。 您必須手動將提醒通知套用至每個問題（或使用大量編輯）。

整合的效果較佳，因為它可自動化手動步驟，但提醒通知可立即完成。

**問題**

我建立了一個報告，顯示按範本型別的專案。 我可以列出專案所有者，但無法列出指派給專案的人員。

**回答**

如果您要將「專案團隊」（「人員配備」標籤）拉入專案報告中的欄，則需要透過文字模式建立此欄。 文字模式如下：

```
displayname=Staffing 
listdelimiter=<p> 
listmethod=nested(projectUsers).lists 
textmode=true
type=iterate 
valuefield=user:name 
valueformat=HTML
```

## AAR Engagement報表的文字模式代碼

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
