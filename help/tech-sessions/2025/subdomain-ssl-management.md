---
title: 技術研討會 — 「控制面板」中的Adobe Campaign子網域和SSL管理
description: 瞭解如何在Adobe Campaign的「控制面板」中委派和設定子網域、設定SSL憑證及監控設定，以確保安全的電子郵件傳遞能力。
solution: Campaign
feature: Subdomains and Certificates
role: Admin, Developer, Leader, User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 3409
last-substantial-update: 2025-09-05T00:00:00Z
jira: KT-18866
source-git-commit: 18ce421793d97372198151afc92b24f3bed053a8
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# 技術研討會：控制面板中的Adobe Campaign子網域和SSL管理

在這場會議中，我們會探索Adobe Campaign中子網域委派和設定的概念，包括安裝SSL憑證來保護子網域。

瞭解子網域是什麼、其用途，以及可讓Adobe有效使用它的委派方法。 此課程也涵蓋透過SSL憑證保護子網域安全的原則，以及維護安全環境的最佳實務。

我們提供使用自助控制面板設定子網域的逐步指引，強調潛在障礙及解決方法。 參與者可獲得實用的知識，以確保順利設定並安全地管理其子網域。

無論您是管理員、開發人員或平台擁有者，本課程都能讓您具備在Adobe Campaign中自信設定及保護子網域安全的技能。

>[!VIDEO](https://video.tv.adobe.com/v/3471391/?learn=on&enablevpops)

## 在Adobe Campaign中掌握子網域管理

解鎖Adobe Campaign電子郵件通訊的子網域委派、設定和安全性要點：

* **子網域委派**&#x200B;選擇完整委派或CNAME委派，以控制Adobe管理您的DNS和電子郵件傳遞的方式。
* **DNS與SSL設定** MX、SPF、DKIM、DMARC和SSL憑證的正確設定，對於安全、可靠的電子郵件傳送至關重要。
* **控制面板**&#x200B;使用Adobe的自助服務工具來簡化子網域設定、監控記錄及管理SSL憑證。
* **常見陷阱**&#x200B;瞭解稽核時間表、記錄需求和疑難排解步驟，以避免延遲和錯誤。

掌握這些流程可確保您的行銷活動安全無虞、可傳遞成果，並維護您品牌的聲譽。

## 委派方法**完整與CNAME

* **完全委派** Adobe會管理子網域的所有DNS記錄，確保最佳傳遞能力與安全性。 建議大部分使用者使用。
* **CNAME委派**&#x200B;客戶和Adobe共用DNS責任。 客戶建立指向Adobe管理資源的CNAME記錄。
* **主要差異：
* **完整** Adobe擁有完整許可權；減少客戶維護工作。
* **CNAME**&#x200B;分擔責任；更多手動步驟可供客戶使用。
* **秘訣**&#x200B;永遠不要委派您的根網域（僅限子網域），以免失去對主網域的控制。
