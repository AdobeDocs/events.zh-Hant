---
title: 詢問專家 — 瞭解混合與容量
description: 瞭解如何測量企業內的混合和容量。 此網路研討會錄製於2019年10月2日。
activity: use
doc-type: feature video
team: Technical Marketing
kt: 9913
exl-id: 5993c6c3-0583-4d1c-94aa-2e64a699e7f1
source-git-commit: ca06e5a8b1602a7bcfb83a43f529680a5a96bacf
workflow-type: tm+mt
source-wordcount: '2224'
ht-degree: 1%

---

# 詢問專家 — 瞭解混合與容量

瞭解如何測量企業內的混合和容量。 此網路研討會錄製於2019年10月2日。

>[!VIDEO](https://video.tv.adobe.com/v/341119/?quality=12)

## Q&amp;A

**問題**

如何將%s放在直條圖上？

**回答**

「混合報表」中列出的%值之所以存在，是因為我們在圖表索引標籤中選擇「群組欄」和「棧疊至100%」。 如果我們選擇「棧疊」，則會顯示計畫時數總計而非百分比。

**問題**

如果您的部門/組織工作負載是專案/任務和問題/請求的混合，您建議如何獲得WPI的高層級審查(在Workfront報告中)。

**回答**

專案、任務和問題各自需要有自己的報告及其自訂表單。 但是，他們每個人都可以使用相同的工作型別欄位。 您可能想要將三個報表顯示在一個儀表板中。

**問題**

我們是否必須大量編輯任務才能使其運作或策略化？

**回答**

我們建議的技術是建立一份報告，讓您取得可操作的任務清單。 一旦您能夠選取所有任務一次，批次編輯它們，然後附加自訂表單與工作型別，並將所有任務的工作型別一次設定為作業。 您可以依照相同的程式，收集策略任務的清單、大量編輯任務並新增自訂表單等。

網路研討會中會提到一些自訂提示的想法，這些提示可能有助於您獲得清單，例如檢查任務名稱、專案所有者、專案組合或指派的使用者中的特定字詞。 這些只是想法。 您應設計最適合您情況的報表。

**問題**

如果我的組合中有4個類別，我可以為每個類別建立目標，然後報告預測與計畫與實際之間的差異嗎？ （4個類別：促銷活動、業務單位、網頁和產品）。 我們在自訂表單/欄位中有專案層級的類別。 目標將是建立季度預測（預算/預測），然後追蹤計畫時數以達成該目標，最終達至實際。

**回答**

如果您將所有類別都在一個自訂欄位中（現在我們將其稱為「工作型別」），只需先在「計畫時數」上建立專案報告群組，然後在按「工作型別」建立專案報告群組即可。 篩選您的專案報告，以便在Planning中顯示所需日期範圍內的專案。 如果您想要檢視百分比，請使用具有已分組欄或棧疊至100%的橫條的圖表。 這可以是您的Forecast報表。

您可以複製報告並編輯它，以根據目前專案建立報告，仍然根據計畫時數顯示混合。

您可以再次複製報表、將報表變更為按實際時數分組（而非計畫時數），並僅顯示所需日期範圍內的已完成專案。 這會根據實際時數顯示百分比混合。

**問題**

如果您在專案或任務上有多個類別ID，此功能是否有效？

**回答**

可以，如果您有多個ID，則需要以索引標籤分隔，如下所示：

```
EXISTS:1:$$EXISTSMOD=NOTEXISTS
EXISTS:1:$$OBJCODE=OBJCAT
EXISTS:1:categoryID=5d76d82600e7926bb51eeb1e0886810e 5d54288d01034619f2eb2c74f6472f18
EXISTS:1:objID=FIELD:ID
```

以定位字元分隔它們的最佳方式是先在產生器中建立類別清單。 放入多個自訂表單名稱，當您切換到文字模式時，您會看到它們是以定位字元分隔的ID。

系統會將多個ID視為OR，因此若其中有任何一個ID附加至任務，該ID就不會顯示在報表中。

**問題**

報表提示是「AND」還是「OR」？

**回答**

個別自訂提示為「AND」。 因此，如果您指定Pam為專案擁有者，而指定Bill為指派給作業，則您只會看到Pam為專案擁有者的專案中指派給Bill的作業。

**問題**

為何只能依特定欄排序？ 即您無法依指派排序。

**回答**

「指派」是一個清單，您不能排序或分組在專案清單上。 您只能對個別專案進行排序或分組。

為了說明這一點，請設想一個任務中的指派清單，如下所示：

```
Jane
Bill
Dan
```

其他任務中的類似指派清單：

```
Bill
Jane
Helen
```

排序中應該先顯示哪個任務？ 您可以說「依清單中的名字排序」，但這並不一定有用，因為您無法控制順序。 Workfront完全不允許您依清單排序，因此可避免此問題。

依清單分組怎麼樣？ 如果我們可以依名稱清單分組，您會發現指派給Jane、Bill、Dan的所有任務已分組在一起，而指派給Jane、Dan、Bill的所有任務（相同的清單，但順序不同）位於不同的分組中。 同樣地，Workfront不允許依清單分組來避免此問題。

**問題**

計畫時數是否用於策略任務以及實際作業時數？

**回答**

不可以。 在我們的範例中，我們使用「計畫時數」來顯示策略和作業任務的計畫投入程度。 這可讓我們輕鬆比較這些變數，無論是過去、現在或未來。 您也可以使用實際時數來比較策略與營運任務，但僅適用於過去的任務，因為實際時數是人員報告為實際執行任務所花的時間。

**問題**

在資源規劃工具中，我們如何說明過去已規劃但未完成的任務？ 計畫時數似乎未前轉，因此，在未來幾週內不會顯示為需要資源的任務/時數。

**回答**

未完成的工作沒有「自動」前轉。 發生此情況時，您需要重新計畫專案。 也許您最初指派給特定任務的資源在新的時間範圍內無法使用，因此專案經理必須檢視並決定重新計畫的最佳方式。 這可能意味著讓利害關係人參與並獲得計畫變更的核准。

**問題**

您建議不要每天輸入2小時來檢查電子郵件、中斷，而是調整其FTE嗎？

**回答**

可以，如果您將FTE設為。75，則會在「資源規劃工具」中顯示使用者為每天6小時的可用時間。 這將是他們每天的可用性。 如果您想要根據日期將之顯示為不適用於不同期間，例如每個季的最後一天無法使用，則間接費用專案就是執行此作業的方法。

有些人偏好管理專案，因為他們可以自行建立專案，並在需要時進行變更，但可能無權編輯自己的FTE。

**問題**

無論您共用報告的人員擁有何種工作許可權，都可以使用團隊容量儀表板的資料嗎？

**回答**

如果使用者沒有檢視物件的許可權，該物件將不會顯示在報表/控制面板中。 不過，如果您希望每個人都能看到相同的結果，您可以前往「報表動作>編輯>報表設定」，並在欄位中輸入您的名稱「使用此報表的存取權執行此報表」。 這可讓在此報告上共用的使用者檢視您看到的確切結果。 它不會授予他們存取結果本身的額外許可權，因此有些結果不一定可點按。

**問題**

如何建立可顯示整體指派至專案（而非任務層級）之所有員工的報告？

**回答**

您可以在「專案報告」中建立欄，顯示列為「人員配備」標籤（專案團隊）一部分的所有使用者。 您會想要使用下列文字模式：

```
displayname=Project Team
listdelimiter=<p>
listmethod=nested(projectUsers).lists
textmode=true
type=iterate
valuefield=user:name
valueformat=HTML
```

**問題**

我想要有包含我的團隊運作方式的報告/儀表板。 尤其是以下情境： — 我擁有的專案/為我建立的專案/我指派給其他人的任務/指派給我的任務

**回答**

我擁有的專案

有一個名為「目前專案」的內建報告，其中將顯示所有目前專案。 您可以編輯此專案並新增篩選規則：專案>擁有者ID >等於> $$USER.IDT儲存並重新命名報告至「我擁有的專案」時。

為我建立的專案

有一個名為「我的專案」的內建報告，其中將顯示您目前在專案團隊中的所有專案（表示您是所有者、贊助者或受指派任務）。 不確定這是否為您的要求，但除了讓您成為專案所有者、贊助者或指派您至任務，沒有其他方法可知道是否有人為您建立專案。

我指派給其他人的任務

使用您想要的任何篩選器建立任務報告，然後前往「篩選器」索引標籤，按一下「切換到文字模式」。 將此程式碼新增至已有的任何專案：

```
EXISTS:1:$$OBJCODE=ASSGN
EXISTS:1:taskID=FIELD:ID
EXISTS:1:assignedByID=$$USER.ID
```

這會顯示登入使用者至少指派一個目前受指派人的所有任務。 如果受指派人是由多個人員指派，則只有指派人員的第一個人員的姓名會在任務登陸頁面上顯示為「請求者」。 如果您想要檢視所有指派的人員以及指派每個人員的對象，您可以將欄新增至檢視、切換至文字模式，然後以下列取代任何內容：

```
displayname=All Assignees and Requesters
listdelimiter=<p>
listmethod=nested(assignments).lists
textmode=true
type=iterate
valueexpression=CONCAT("Assigned To: ",{assignedTo}.{name},"; Requested By: ",{assignedBy}.{name})
valueformat=HTML
```

指派給我的任務

有一個名為「我的任務」的內建報告，將顯示您作為任務擁有者的目前專案中的所有未完成任務。 我建議您變更篩選條件，以顯示您是可能指派許多使用者之一的所有任務，而不僅僅是任務擁有者。 若要這麼做，請移除篩選規則

```
Task > Assigned To ID > Equal > $$USER.ID 
```

並將其取代為

```
Assignment Users > ID > Equal > $$USER.ID
```

**問題**

是否有自訂圖表標籤的方法？ 我發現當我建立圖表來反映專案狀態時，主群組的名稱最終會包含在標籤中。

**回答**

圖表上的標籤會使用您要分組的欄位名稱。 因此，變更標籤的唯一方式是使用具有任何所需名稱的計算自訂欄位。 在欄位的計算區段中，放置您想作為分組依據的原生欄位的欄位名稱。

**問題**

請您如何為Chuck團隊指派的報告列加上顏色編碼？ 例如琥珀色代表後方，紅色代表延遲，綠色代表準時？ 您也可以將順序變更為更符合邏輯（即紅色/琥珀色/綠色）還是反面？

**回答**

若要變更報告中進度狀態選項的顏色，請編輯報告並按一下「圖表」標籤。 尋找「自訂顏色>」下拉式清單。 視您是否選擇群組欄或橫條而定，它會顯示在「左(Y)軸」方塊或「群組資料依據」方塊旁邊。 在該下拉式清單中，您可以選取顏色。 如果您按一下顏色選項右下方的數字，您就可以從較大的調色盤中選取顏色。

很遺憾，您無法變更這些專案的順序。

**問題**

您可以建立圖表，指向工作者獲指派任務的專案計數嗎？

**回答**

是，方法如下：

* 建立專案報告
* 如果有問題的使用者是登入的使用者，則篩選器應包含此行：

```
   Project Users > ID > Equal >$$USER.ID 
```

* 如果沒有，請將使用者名稱取代 [!DNL $$USER.ID]. 這會顯示此人受指派任務或所有者或贊助者的所有專案。 如果您只想檢視其獲指派任務的專案，您應新增以下兩個額外的篩選規則：

```
   Project > Owner ID > Not Equal > $$USERID
   Project > Sponsor ID > Not Equal > $$USERID
```

* 建立至少一個群組，以便建立圖表。 依任何專案分組，例如公司。 然後按一下「圖表」標籤，並選擇圖表。 一個軸的預設值為「記錄計數」。 這將是使用者指派的專案數。

當使用者在專案中被指派任務（指派給任務或專案所有者或專案贊助者）時，該人員會新增到專案團隊，並且可以在「人員」子標籤下的「人員配備」標籤中看到。 如果從專案所有者、贊助者或任何任務指派中移除使用者，其名稱仍會保留在專案團隊中。 如果您想要移除它，則必須手動移除。 請記住，這可能會影響報告結果的準確性。 若要從專案團隊中移除某人，請前往「人員配備>人員」，選取一或多個人員，然後按一下出現在清單上方的「移除」按鈕。

**問題**

如何變更文字模式（在分組中）中欄的遞減順序？

**回答**

建立報表時，您可以選擇對「欄（檢視）」標籤中的大多數欄進行排序。 如果您沒有群組，這會排序您的整個清單報告。 如果您有群組，其會根據每個群組內的選擇排序。

**問題**

如何建立可識別指派至核准階段的團隊成員的欄？

**回答**

如果您正在執行任務或問題/請求報告，Report Builder中有一個名為「核准者和狀態」的欄可提取此資訊。
