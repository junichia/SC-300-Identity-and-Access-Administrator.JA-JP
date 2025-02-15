---
lab:
  title: 24 - Azure AD Identity Governance の設定で外部ユーザーのライフサイクルを管理する
  learning path: "04"
  module: Module 04 - Plan and Implement and Identity Governance Strategy
ms.openlocfilehash: a159b0548b2755c34ad9e4412e8f70ea14be1d5f
ms.sourcegitcommit: b5fc07c53b5663eaa1883cf38b70c57cd88470ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "146741695"
---
# <a name="lab-24-manage-the-lifecycle-of-external-users-in-azure-ad-identity-governance-settings"></a>ラボ 24:Azure AD Identity Governance の設定で外部ユーザーのライフサイクルを管理する  

## <a name="lab-scenario"></a>ラボのシナリオ

アクセス パッケージ要求が承認されることでディレクトリに招待された外部ユーザーが、アクセス パッケージの割り当てを失ったときに行われる処理を選択できます。 これは、ユーザーがアクセス パッケージの割り当てをすべて放棄した場合、または最後のアクセス パッケージの割り当てが期限切れになった場合に、行われる可能性があります。 既定では、アクセス パッケージの割り当てをすべて失った外部ユーザーは、ディレクトリへのサインインをブロックされます。 30 日後に、ゲスト ユーザー アカウントがディレクトリから削除されます。

#### <a name="estimated-time-5-minutes"></a>推定時間:5 分

### <a name="exercise-1---azure-ad-identity-governance-settings"></a>演習 1 - Azure AD Identity Governance の設定

#### <a name="task-1---manage-the-lifecycle-of-external-users-in-azure-ad-identity-governance-settings"></a>タスク 1 - Azure AD Identity Governance の設定で外部ユーザーのライフサイクルを管理する

1. グローバル管理者として [https://portal.azure.com](https://portal.azure.com) にサインインします。

2. これらのタスクを行うには、グローバル管理者またはユーザー管理者のアカウントが必要です。

3. [Azure Active Directory] を開き、**[Identity Governance]** を選択します。

4. 左側のナビゲーション メニューの **[エンタイトルメント管理]** で、**[設定]** を選択します。

5. 上部のメニューで、**[編集]** を選択します。

    ![[manage the lifecycle of external users]\(外部ユーザーのライフサイクルを管理する\) が強調された Identity Governance の [設定] ページが表示されている画面イメージ。](./media/lp4-mod1-manage-lifcycle-of-ext-users.png)

6. **[Manage the lifecycle of external users]\(外部ユーザーのライフサイクルを管理する\)** セクションで、外部ユーザーに対するさまざまな設定を確認します。

7. 外部ユーザーがアクセス パッケージへの最後の割り当てを失ったときに、そのユーザーによるこのディレクトリへのサインインをブロックする場合は、**[Block external user from signing in to this directory]\(外部ユーザーによるこのディレクトリへのサインインをブロックする\)** を **[はい]** に設定します。

8. ディレクトリへのサインインをブロックされたユーザーは、アクセス パッケージを再要求したり、このディレクトリで追加のアクセス権を要求したりすることができません。 その後、これらのユーザーが他のアクセス パッケージへのアクセスを要求する必要がある場合は、サインインをブロックするように構成しないでください。

9. 外部ユーザーがアクセス パッケージへの最後の割り当てを失ったときに、このディレクトリ内のゲスト ユーザー アカウントを削除する場合は、 **[Remove external user]\(外部ユーザーを削除\)** を **[はい]** に設定します。

    **注** - エンタイトルメント管理を使用すると、エンタイトルメント管理によって招待されたアカウントのみが削除されます。 また、ユーザーがこのディレクトリ内のアクセス パッケージの割り当てではないリソースに追加されていた場合でも、そのユーザーはサインインをブロックされ、このディレクトリから削除されることに注意してください。 アクセス パッケージの割り当てを受け取る前に、ゲストがこのディレクトリ内に存在していた場合は、そのまま残ります。 ただし、ゲストがアクセス パッケージの割り当てによって招待され、招待された後で OneDrive for Business または SharePoint Online サイトにも割り当てられた場合でも、そのゲストは削除されます。

10. このディレクトリ内のゲスト ユーザー アカウントを削除する場合は、削除するまでの日数を設定できます。 アクセス パッケージへの最後の割り当てが失われた直後にゲスト ユーザー アカウントを削除する場合は、 **[Number of days before removing external user from this directory]\(このディレクトリから外部ユーザーを削除するまでの日数\)** を **0** に設定します。

11. 変更を行った場合は、**[保存]** を選択します。
