---
title: Attract でジョブ求人の作成、承認、および転記
description: このトピックでは、Attract でのジョブ求人の要素について説明します。 ジョブ求人を作成する方法についても説明します。
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1e76572c1a843fe7abd515333d5b7cb03b91eb11
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518448"
---
# <a name="create-approve-and-post-jobs-in-attract"></a>Attract でジョブ求人の作成、承認、および転記

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Talent: Attract でのジョブ求人の要素について説明します。 ジョブ求人を作成する方法についても説明します。

## <a name="job-creation"></a>職務の作成

管理者、採用担当者、および採用マネージャーがジョブ求人を作成できます。 ジョブ求人を作成するときに、プロセスでのロールを選択するよう求められます: 採用マネージャーまたは採用担当者。 ロールを選択した後、プロセス テンプレートを選択するよう求められます。 **スキップ**を選択すると、既定のテンプレートが使用されます。 プロセス テンプレートの詳細については、[Attract でプロセス テンプレートの作成](./process-templates-attract.md) を参照してください。

Attract でのジョブ求人には、職務の詳細、採用チーム、採用プロセス、人材募集、および分析が含まれます。

## <a name="job-details"></a>職務の詳細

**職務の詳細**タブには、職務の職責と属性に関する詳細が含まれています。 職位、職務明細書、および勤務地のフィールドが必須です。 他のフィールドはオプションです。

既定では、**求人数**フィールドが **1** に設定されています。 ただし、その値は変更できます。 ジョブのオファーが準備された場合、**空いている求人数**フィールドは減少します。

職位管理が管理センターで有効になった場合、**職位の更新**ルックアップが使用できます。 このルックアップは Common Data Service の JobPosition エンティティを読み込み、職務に対して選択可能な職位の一覧を返します。 選択する求人数が職位の求人数を超える場合、警告が表示されます。 職位が複数の職務に使用される場合にも、警告が表示されます。

> [!NOTE]
> 職位管理は、 包括採用アドオンで使用できます。

採用プロセスのオファー アクティビティでの設定に応じて、職位数は 1 つのオファーに対して 2 回使用できます。 詳細については、[採用プロセス](./activities-attract.md) を参照してください。

Attract には、既定の一連の**スキル**が含まれます。 これらのスキルは、入力する際の提案として表示されます。 フィールドに新しいスキル テキストを入力し、Enter キーを押して、スキルをさらに追加できます。

Attract には、既定の一連の**職務権限**が含まれます。 フィールドに新しい職務権限を入力し、Enter キーを押して、3 つまでさらに職務権限を追加できます。

Attract には、既定の一連の**会社の業種**が含まれます。 フィールドに新しい会社の業種を入力し、Enter キーを押して、3 つまでさらに会社の業種を追加できます。

## <a name="hiring-team"></a>採用チーム

**採用チーム**タブには、ジョブ求人に関与する個人の一覧が含まれます。 ユーザーが採用チームに追加される場合、採用チームでのロールが割り当てられる必要があります。 ロールは、ユーザーのアクセス先および受信する通知のデータを決定します。 選択できるロールは、**採用担当者**、**採用マネージャー**、**代理人**、および**面接者**です。 ロール権限の詳細については、"ロール管理" ドキュメントを参照してください。 採用担当者および採用マネージャーは、代わりに 1 名以上の複数の代理人を指名できます。 代理人の詳細については、[Attract でのセキュリティおよびロールの管理](./security-attract.md) を参照してください。

ジョブ求人が有効になった後、採用チームを更新できます。

## <a name="process"></a>プロセス

採用プロセスに関する既定の情報は、ジョブ求人が作成されたときに選択されたプロセス テンプレートに基づきます。 その時点で特定のテンプレートが選択されなかった場合には、既定のテンプレートが使用されます。 採用プロセスを定義する場合、候補者、応募、およびオファー ステージ以外のさまざまなステージを追加または削除できます。 候補者のステージを削除できませんが、無効にはできます。 各ステージ内では、1 つまたは複数の事前に定義された活動を追加または削除できます。

採用プロセスに追加できる活動に関する詳細については、[Attract での採用プロセス活動](./activities-attract.md) を参照してください。

> [!NOTE]
> ジョブ求人が有効になった後は、採用のプロセスを更新できません。

## <a name="postings"></a>転記

ジョブ求人が有効になった後に、転記できます。 採用担当者と管理者だけが、ジョブ求人を転記できます。 ジョブ求人は、Talent Careers (Microsoft Dynamics 365 for Talent キャリア サイト) または LinkedIn のいずれかに転記できます。 Attract チームは、継続的にジョブ ボード アグリゲーターと提携していきます。 このリストは時間の経過に伴い展開されます。 ジョブが内部のみに転記される場合、候補者はジョブを表示および申請するための AAD アカウントが必要です。 ジョブが一般公開される場合、候補者はすべての認証オプションを使い、ジョブを表示および申請が可能です。 

ジョブ求人の転記の詳細については、[Attractでキャリア サイト機能](career-site.md) を参照してください。

> [!NOTE]
> ジョブ求人の転記機能は、Attract の包括採用アドオンでのみ使用できます。

### <a name="posting-jobs-to-linkedin"></a>LinkedIn へのジョブ求人の転記 

Attract から LinkedIn にジョブを転記する前に、管理者は**管理者設定**に LinkedIn Company ID および LinkedIn Company 名を追加する必要があります。 LinkedIn Company ID は、Attract からのジョブ求人が正しい会社ページにマップされていることを確認するために必要です。

LinkedIn Company ID は、LinkedIn 内で会社を固有に識別する文字列です。 LinkedIn company ID を確認する方法の詳細については、[LinkedIn のサイト](https://aka.ms/findID) を参照してください。

LinkedIn の会社を更新するには、 **設定** メニュー (ギア記号) で **管理センター** を選択してから、 **LinkedIn の統合** タブを選択します。 **LinkedIn に接続**セクションで、LinkedIn 会社名 および 会社 ID を入力してから設定を保存します。

> [!NOTE]
> LinkedIn へのジョブ求人転記プロセスについての重要な注意事項が 4 つあります。
> 1. LinkedIn に転記されたジョブ求人は、「制限付きリスト」ジョブ求人として投稿されます。 制限付きリストのジョブ求人を LinkedIn のサイト全体で宣伝することはできません。 Attract から LinkedIn へ転記された制限付きリストのジョブ求人を宣伝したい場合は、LinkedIn と連携して「求人ラッピング」を有効にする必要があります。 詳細については、次のリンクを参照して LinkedIn サポートにご連絡ください。
>
>    [制限付きリストと Job Wrapping のプレミアム求人枠](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping)
>
>    [求人ラッピングよくある質問](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions)
>
> 1. LinkedIn にジョブ求人を転記する際、Attractは、ジョブ求人に対して Microsoft 365 組織名を渡します。 LinkedIn は、渡された組織名に基づいてジョブ求人を LinkedIn 側の会社にリンクします。 仕事が LinkedIn で間違った会社に対してリストされている場合は、Microsoft 365 の組織名が LinkedIn の会社名と一致することを確認してください。  
>
>    [住所や連絡先などの変更](https://docs.microsoft.com/en-us/office365/admin/manage/change-address-contact-and-more)
>
>    この手順の後に問題がある場合は、LinkedIn サポートにお問い合わせください。 
> 
> 1. LinkedIn に転記されたジョブは、ライブ LinkedIn サイトに表示されます。 LinkedIn にジョブを転記するためのテスト環境ではありません。 
>
> 1. 現在の LinkedIn バッチ ジョブ求人転記プロセスのため、LinkedIn に転記されたジョブ求人が LinkedIn 内から求職者に表示されるまでには、最大 24 時間かかることがあります。


## <a name="activate"></a>有効化する

ジョブ求人が有効になった後、転記でき、候補者および申請者を追加できます。 ジョブ求人に候補者を追加するオプションは、採用プロセスの候補者活動で設定されます。

> [!NOTE]
> ジョブ求人が有効になった後は、採用のプロセスを更新できません。

## <a name="prospects-and-applicants"></a>候補者および申請者

ジョブ求人に候補者を追加するオプションは、採用プロセスの [候補者活動](./activities-attract.md#prospect-activity) で設定されます。 ジョブ求人を有効にする前に、このオプションを設定する必要があります。 ジョブ求人が有効になった後、候補者および申請者を追加できます。

## <a name="approvals"></a>承認

Attract のジョブ求人は、承認用に申請できます。 すべてのジョブ求人に、承認が必要ではありません。 要件は、テンプレート レベルで設定されます。 既定では、テンプレートで承認が無効になっています。 承認を設定するには、プロセス テンプレートに移動し、**承認**フィールドを既定値に設定します。 それから、ジョブ求人を作成するときにそのテンプレートを選択します。

ジョブ求人を保存した後、承認用に申請できます。 次の表では、承認を使用するドキュメントのステータスが一覧表示されます。

| ステータス   | 行政単位 (区画)                                                               |
|----------|---------------------------------------------------------------------|
| ドラフト    | ジョブ求人が保存されたが、まだワークフローに送信されていません。 |
| 保留中  | ジョブ求人を承認者に送信しました。                            |
| 承認済 | ジョブ求人が承認されたが、まだ有効になっていません。            |
| 拒否済 | ジョブ求人が拒否されると、有効化はできません。               |
| 使用可能   | ジョブ求人が承認され、有効化されました。                            |

ジョブ求人の一覧で、ジョブ ステータスでフィルター処理できます。

承認は、会社内の任意の Microsoft Azure Active Directory(Azure AD) ユーザーに送信できます。 承認は、承認者として一覧表示されているすべての人に同時に送信されます。 すべての承認者は、移行可能になる前に、ジョブを許可する必要があります。 1 人の承認者がジョブを拒否すれば、ジョブは**否認済**ステータスに表示されます。 ジョブ求人が承認された後に、有効になります。

承認されたがまだ有効になっていない状態でユーザーがジョブを編集する場合、ジョブ ステータスは**ドラフト**にリセットされ、承認のためにジョブを再送信する必要があります。 承認済ジョブが有効となった後は、編集することができません。

承認者として一覧表示されている人は、Attract で承認する項目があるという通知を電子メールで受け取ります。  電子メールで、承認者はリンクをクリックしてジョブを開き、詳細を確認し、承認または却下することができます。 ジョブ ステータスが**承認済**または**否認済**に設定された後、申請者は Attract で通知され、電子メールを受け取ります。 また、承認者であっても、24 時間内に承認要求に応答しない場合、通知の電子メールが送信されます。

> [!NOTE]
> 承認電子メールのカスタム電子メール テンプレートを作成することができます。 詳細については、[電子メールのテンプレートを作成および管理](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/email-templates) を参照してください。

## <a name="create-a-job"></a>職務の作成

職務を作成するには、これらの手順に従います。

1. **職務**に移動します。
2. **新規** を選択します。
3. **職位**フィールドに、職位を入力します。 **ロール**フィールドに、ロールを入力します。
4. **テンプレート** フィールドで、テンプレートを選択します。 または、**スキップ**を選択します。 **スキップ**を選択した場合、既定のテンプレートとしてマークされているテンプレートが使用されます。

    ドキュメントが承認プロセスを経由する必要がある場合、**承認プロセス**フィールドを**既定値**に設定しているテンプレートを選択します。

5. **詳細**タブで、職務の詳細を入力します。 **肩書き**、**職務明細書**、および**勤務地**フィールドが必須です。
6. **保存** を選択します。
7. **採用チーム**タブで、採用マネージャー、採用担当者、または面接者を追加します。
8. **保存** を選択します。
9. **プロセス**タブで、必要なステージを追加または削除します。

    - ステージを追加するには、**+ 新規ステージ**を選択します。
    - ステージを削除するには、ポインターをステージに移動して削除し、表示されるごみ箱ボタンを選択します。

        > [!NOTE]
        > 候補者、申請、およびオファー ステージを削除することはできません。

10. 必要に応じて、活動を追加または削除します。

    - 活動を追加するには、右の一覧から適切なステージにドラッグします。 または、活動をダブルクリックし、それを追加するステージを選択します。
    - 活動を削除するには、活動を展開し、活動ヘッダーのごみ箱ボタンを選択します。

11. **保存** を選択します。
12. 承認プロセスを使用する選択をした場合は、次の手順に従います。

    1. **+ 承認者の追加**を選択し、Azure AD アカウントを持つユーザーを入力します。 複数の承認者を追加できます。
    2. **承認者に送信**を選択します。

    職務の**ジョブ ステータス**フィールドを**保留中**に設定します。 **ジョブ ステータス**フィールドの値が**承認済**に変更した後、ジョブ求人を有効化できます。

13. ジョブ求人を有効にするには、**有効化**を選択します。
14. ジョブ求人を転記するには、**転記**に移動し、Talent Careers サイトまたは LinkedIn で**今すぐ転記**を選択します。
