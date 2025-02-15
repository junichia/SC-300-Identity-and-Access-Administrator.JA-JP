---
lab:
  title: 11 - Privileged Identity Management で Azure リソース ロールを割り当てる
  learning path: "02"
  module: Module 02 - Implement an authentication and access management solution
ms.openlocfilehash: ca3725a8f81afffeb093fc997c2caf7917a35948
ms.sourcegitcommit: 80c5c0ef60c1d74fcc58c034fe6be67623013cc0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "146823191"
---
# <a name="lab-11---assign-azure-resource-roles-in-privileged-identity-management"></a>ラボ 11 - Privileged Identity Management で Azure リソース ロールを割り当てる

**注** - このラボでは Azure Pass が必要です。 手順については、ラボ 00 を参照してください。

## <a name="lab-scenario"></a>ラボのシナリオ

Azure Active Directory (Azure AD) Privileged Identity Management (PIM) では、組み込みの Azure リソース ロールと、以下を含むカスタム ロール (ただしこれらに限定されません) を管理できます。

- 所有者
- User Access Administrator
- Contributor
- セキュリティ管理者
- Security Manager

ユーザーを Azure リソース ロールの候補にする必要があります。


#### <a name="estimated-time-10-minutes"></a>推定時間:10 分

### <a name="exercise-1---pim-with-azure-resources"></a>演習 1 - Azure AD リソースを使用した PIM

#### <a name="task-1---assign-azure-resource-roles"></a>タスク 1 - Azure リソース ロールを割り当てる

1. 全体管理者アカウントを使用して、[https://portal.azure.com](https://portal.azure.com) にサインインします。

2. **[Azure AD Privileged Identity Management]** を検索してから選択します。

3. [Privileged Identity Management] ページの左側のナビゲーションで **[Azure リソース]** を選択します。

4. 上部のメニューで **[リソースを検出する]** を選択します。

5. [Azure リソース - 検出] ページでサブスクリプションを選択し、上部のメニューで **[リソースの管理]** を選択します。

   ![サブスクリプションとリソースの管理が強調表示されている [Azure リソース - 検出] ページを表示している画面イメージ](./media/lp4-mod3-pim-azure-resource-management.png)

6. **[管理用に選択したリソースのオンボード]** ダイアログ ボックスで情報を確認し、**[OK]** を選択します。

7. オンボードが完了したら、[Azure リソース - 検出] ページを閉じます。

8. [Azure リソース] ページで、サブスクリプションを選びます。

   ![最近追加された Azure リソースを表示している画面イメージ](./media/lp4-mod3-pim-az-resource-overview.png)

9. 左側のナビゲーション メニューで、**[管理]** の下にある **[ロール]** を選択して、Azure リソースのロールの一覧を表示します。

10. 上部のメニューで **[+ 割り当ての追加]** を選択します。

11. [割り当ての追加] ページで、 **[ロールの選択]** メニューを選択し、 **[API Management サービス共同作成者]** を選択します。

12. **[メンバーの選択]** で **[メンバーが選択されていません]** を選択します。

13. ロールを割り当てる組織から **[Miriam Graham]** を選択します。  次に、**[選択]** を選択します。

14. **[次へ]** を選択します。

15. **[設定]** タブの **[割り当ての種類]** で **[対象]** を選択します。

   - **[対象]** 割り当ての場合、このロールのメンバーは、ロールを使用するにはアクションを実行する必要があります。 要求されるアクションには、多要素認証 (MFA) チェックの実行、業務上の妥当性の指定、指定された承認者に対する承認要求などがあります。

   - **アクティブ** 割り当てでは、メンバーがロールを使用するためのアクションを実行する必要はありません。 アクティブとして割り当てられたメンバーには常に、そのロールに割り当てられた特権があります。

16. 開始日時と終了日時を変更して割り当て期間を指定します。

17. 完了したら、 **[割り当て]** を選択します。

18. 新しいロールの割り当てが作成されると、状態の通知が表示されます。

#### <a name="task-2---update-or-remove-an-existing-resource-role-assignment"></a>タスク 2 - 既存のリソースのロールの割り当てを更新または削除する

既存のロールの割り当てを更新または削除するには、次の手順を実行します。

1. **[Azure AD Privileged Identity Management]** を開きます。

2. **[Azure リソース]** を選択します。

3. 管理するサブスクリプションを選択して、その概要ページを開きます。

4. **[管理]** で、 **[割り当て]** を選択します。

5. **[対象ロール]** タブの [操作] 列で、使用可能なオプションを確認します。

6. **[削除]** を選択します。

7. **[削除]** ダイアログ ボックスで情報を確認し、**[はい]** を選択します。
