---
lab:
  title: 25 - 内部および外部ユーザーのアクセス レビューの作成
  learning path: "04"
  module: Module 04 - Plan and Implement and Identity Governance Strategy
ms.openlocfilehash: c5207f3a8886c28390b38d3e1387168ca1d65021
ms.sourcegitcommit: b5fc07c53b5663eaa1883cf38b70c57cd88470ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "146741693"
---
# <a name="lab-25---creating-access-reviews-for-internal-and-external-users"></a>ラボ 25 - 内部および外部ユーザーのアクセス レビューの作成  

## <a name="lab-scenario"></a>ラボのシナリオ

特権ユーザー アクセスは、同様の方法で定期的に確認する必要があります。  これらは昇格されたアクセスの割り当てであるため、これらのレビューは、会社によって識別された一貫した基準で行う必要があります。  未使用の不要な特権の割り当てを削除する必要があります。  また、会社に所属しなくなったユーザーや社内の部門が変更されたユーザーについても、自動削除を構成する必要があります。

#### <a name="estimated-time-5-minutes"></a>推定時間:5 分

### <a name="exercise-1---create-an-internal-access-review"></a>演習 1 - 内部アクセス レビューを作成する

#### <a name="task---create-a-new-access-review"></a>タスク - 新しいアクセス レビューを作成する

1. グローバル管理者として [https://portal.azure.com](https://portal.azure.com) にサインインします。

2. アクセス レビューでは、アクセス ライフサイクルを管理できます。  **Azure Active Directory** 内で、 **[管理]** メニューの **[Identity Governance]** を見つけます。  **[Identity Governance]** で、 **[アクセス レビュー]** を選択します。

3. アクセス レビューに名前を付け、開始日と頻度を設定します。 期間とは、アクセス レビューが実行される時間の長さで、これを過ぎると期限切れになります。  終了は特定の日付に設定することも、何回実行された後、とすることもできます。  次に、アクセス レビューのユーザー スコープを選択します。

4. このスコープの一部となるロールのスコープを選択します。  すべてのロールを追加することも、特定のレビューに対してのみ特定のロールを選択することもできます。 

5. 次の手順では、レビュー担当者を特定します。  これらのレビュー担当者は、自己レビューを行うメンバー自身にすることもできますが、部門全体のアクセスをレビューする場合はスーパーバイザーに割り当てることもできます。 レビュー担当者が応答しない場合に、その特権アクセスをメンバーから自動的に削除するようにアクションを設定することもできます。

6. 詳細設定を使用すると、レビューの一部としてメッセージを配置できます。  [開始] を選択してアクセス レビューを開始します。

7. アクセス レビューが作成されると、アクセス レビュー リストにレビューのロールと所有者が設定されます。

8. レビュー中のメンバーは、レビューが開始されるときに電子メールを受け取ります。

9. いずれかのロールのアクセス レビューを選択すると、これらのアクセス レビューの状態が表示されます。

