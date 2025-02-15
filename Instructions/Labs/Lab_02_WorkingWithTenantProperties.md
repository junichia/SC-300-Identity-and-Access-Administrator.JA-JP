---
lab:
  title: 02 - テナントのプロパティを操作する
  learning path: "01"
  module: Module 01 - Implement an Identity Management Solution
ms.openlocfilehash: f43e996adefddcf01f7feb5e01056582faab35eb
ms.sourcegitcommit: bc5c47a39782e94c249ec4bce01ba0da9249ec61
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "146822631"
---
# <a name="lab-02-working-with-tenant-properties"></a>ラボ 02: テナントのプロパティを操作する

## <a name="lab-scenario"></a>ラボのシナリオ

テナントに関連付けられているさまざまなプロパティを特定し、更新する必要があります。

#### <a name="estimated-time-15-minutes"></a>推定時間:15 分

### <a name="exercise-1---create-a-custom-subdomains"></a>演習 1 - カスタム サブドメインを作成する 

#### <a name="task-1---create-a-custom-subdomain-name"></a>タスク 1 - カスタム サブドメイン名を作成する

1. ディレクトリのグローバル管理者アカウントを使用して、[https://portal.azure.com](https://portal.azure.com) にアクセスし、サインインします。

1. **[ポータル メニューの表示]** ハンバーガー アイコンを選択し、**[Azure Active Directory]** を選択します。

    ![[Azure Active Directory] が選択された Azure portal メニュー](./media/azure-portal-menu-aad.png)

1. **Azure AD** の **[管理]** セクションで、 **[カスタム ドメイン名]** を選択します。

1. **[カスタム ドメインの追加]** を選択します。

1. "**カスタム ドメイン名**" フィールドで、**onmicrosoft.com** ドメイン名の前に **sales** を付けて、ラボ テナントのカスタム サブドメインを作成します。  形式は次のようになります。

    ```
    sales.labtenant.onmicrosoft.com
    ```

1. **[ドメインの追加]** を選択して、サブドメインを追加します。


### <a name="exercise-2---changing-the-tenant-display-name"></a>演習 2 - テナントの表示名を変更する

#### <a name="task-1---set-the-tenant-name-and-technical-contact"></a>タスク 1 - テナント名と技術部連絡先を設定する

1. Azure Active Directory 内から、左側のナビゲーションの **[管理]** セクションで **[プロパティ]** を選択します。

1. ダイアログで **[名前]** と **[技術部連絡先]** のテナント プロパティを変更します。

    | **設定** | **Value** |
    | :--- | :--- |
    | 名前 | Contoso マーケティング |
    | 技術部連絡先 | `your Global admin account` |

1. **[保存]** を選択してテナント プロパティを更新します。

   **保存が完了するとすぐに名前が変更されます。**

#### <a name="task-2---review-the-country-or-region-and-other-values-associated-with-your-tenant"></a>タスク 2 - テナントに関連付けられている国または地域およびその他の値を確認する

1. **[Azure Active Directory]** ページの [管理] セクションで、 **[プロパティ]** を選択します。

2. **[テナントのプロパティ]** で、**[国または地域]** を見つけて、情報を確認します。

    **重要** - テナントが作成されると、その時点で国または地域が指定されます。 この設定は後で変更できます。

3. **[プロパティ]** ページの **[テナントのプロパティ]** で、 **[場所]** を見つけて情報を確認します。

    ![[国または地域] と [場所] の設定が強調表示されている Azure Active Directory の [プロパティ] ページを表示する画面イメージ](./media/azure-active-directory-properties-country-location.png)

#### <a name="task-3---finding-the-tenant-id"></a>タスク3 - テナント ID を見つける

Azure サブスクリプションには、Azure Active Directory (Azure AD) との信頼関係があります。 サブスクリプションでは、ユーザー、サービス、デバイスを認証するために Azure AD が信頼されます。 各サブスクリプションには、それに関連付けられているテナント ID があり、いくつかの方法で、お使いのサブスクリプションのテナント ID を見つけることができます。

1. **[Azure Active Directory]** ページの [管理] セクションで、 **[プロパティ]** を選択します。

2. **[テナントのプロパティ]** で、**[テナント ID]** を見つけます。 これは一意のテナント識別子です。

    ![[テナント ID] ボックスが強調表示されている [テナントのプロパティ] ページを表示する画面イメージ](./media/portal-tenant-id.png)

### <a name="exercise-3---setting-your-privacy-information"></a>演習 3 - プライバシー情報を設定する

#### <a name="task-1---adding-your-privacy-info-on-azure-ad-including-global-privacy-contact-and-privacy-statement-url"></a>タスク 1 - グローバル プライバシー連絡先、プライバシーに関する声明の URL など、Azure AD にプライバシー情報を追加する

Microsoft では、社内の従業員と外部のゲストがポリシーを確認できるように、グローバル プライバシー連絡先と組織のプライバシーに関する声明の両方を追加することを強くお勧めします。 プライバシーに関する声明はそれぞれの会社に合わせて独自に作成､変更されるため､弁護士に相談することを強くお勧めします｡

   **注** - 個人データの表示または削除については、[https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure) を参照してください。 GDPR の詳細については、[https://servicetrust.microsoft.com/ViewPage/GDPRGetStarted](https://servicetrust.microsoft.com/ViewPage/GDPRGetStarted) を参照してください。

組織のプライバシー情報は、Azure AD の **[Properties]** エリアで追加します。 [Properties] エリアにアクセスしてプライバシー情報を追加するには:

1. **[Azure Active Directory]** ページの [管理] セクションで、 **[プロパティ]** を選択します。

    ![[技術部連絡先]、[グローバル プライバシー連絡先]、[プライバシーに関する声明] の各ボックスが強調表示されている、テナントのプロパティを表示する画面イメージ](./media/properties-area.png)

2. 従業員のプライバシー情報を追加します｡

- **グローバル プライバシー連絡先** - `AllanD@` **Azure ラボ ドメイン**
     - Allan Deyoung は、IT 管理者として働く Azure ラボ テナントの組み込みユーザーです。彼をプライバシー連絡先として使用します。
     - この連絡先は､データに関する違反があった場合に Microsoft が問い合わせを行う連絡先でもあります｡ 問い合わせの記載がない場合､Microsoft はグローバル管理者に問い合わせます｡

- **プライバシーに関する声明の URL** -  <https://github.com/MicrosoftLearning/SC-300-Identity-and-Access-Administrator/blob/master/Allfiles/Labs/Lab2/SC-300-Lab_ContosoPrivacySample.pdf>

     - サンプルのプライバシー PDF は、ラボのディレクトリにあります。
     - 組織が社内と外部のゲストの両方のデータのプライバシーをどのように処理するかを説明している組織のドキュメントへのリンクを入力します。

    **重要** - プライバシーに関する独自の声明とプライバシー連絡先のどちらも含めていない場合は、外部のゲストの [アクセス許可の確認] ボックスに、 **<組織名\>** は、ユーザーが確認する使用条件へのリンクを提供していませんというテキストが表示されます。 たとえば､このメッセージは､B2B コラボレーションでゲスト ユーザーが組織にアクセスするための招待を受けたときに表示されます｡

    ![B2B Collaboration Review Permissions ボックスとメッセージ](./media/active-directory-no-privacy-statement-or-contact.png)

3. **[保存]** を選択します。

#### <a name="task-2---check-your-privacy-statement"></a>タスク 2 - プライバシーに関する声明を確認する

1. Azure ホーム画面 - ダッシュボードに戻ります。
2. UI の右上隅で、ご利用のユーザー名を選択します。
3. ドロップダウン メニューから **[アカウントの表示]** を選択します。

     **新しいブラウザー タブが自動的に開きます。**

4. 左側のメニューで **[設定とプライバシー]**  を選びます。
5. **[プライバシー]** を選択します。
6. **[組織の通知]** で、Contoso マーケティング組織のプライバシーに関する声明の横にある **[表示]** 項目を選びます。

     **リンクしたプライバシー PDF ファイルが表示された新しいブラウザー タブが開きます。**

7. サンプルのプライバシーに関する声明を確認します。
8. PDF が含まれているブラウザー タブを閉じます。
9. **マイ アカウント**　アイテムを表示しているブラウザー タブを閉じます。
