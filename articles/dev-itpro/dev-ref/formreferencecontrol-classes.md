---
title: F クラス (FormReferenceControl から FormStringControl)
description: FormReferenceControl から FormStringControl までのクラスの API 参照。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 63733
ms.assetid: d163623b-8ae3-4f18-b804-fe890b5d2fe0
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2f12c33a8ea66d56066a5856ed6100ce44b09b0
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833696"
---
# <a name="f-classes-formreferencecontrol-to-formstringcontrol"></a>F クラス (FormReferenceControl から FormStringControl)

[!include [banner](../includes/banner.md)]

FormReferenceControl から FormStringControl までのクラスの API 参照。

## <a name="class-formreferencecontrol"></a>クラス FormReferenceControl


    class FormReferenceControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                           | 説明                                                                                                                                                             |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                   | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public boolean allowEdit(\[boolean value\])                                      | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])         | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public str countryRegionCodes(\[str value\])                                     | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                      |                                                                                                                                                                         |
| public int dataField()                                                           |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                       | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                         | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                       |
| public int displayTarget(\[int value\])                                          | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                               | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public boolean enabled(\[boolean value\])                                        | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                 |                                                                                                                                                                         |
| public FilterValue filterValue(FieldBinding fieldBinding)                        |                                                                                                                                                                         |
| public int height(int value, \[int mode\])                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                             | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                            | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpText(\[str value\])                                               | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                        | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public boolean isResolvingReference()                                            |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                         | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMode(\[int value\])                                               | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                              | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public Common lookupReference()                                                  |                                                                                                                                                                         |
| public boolean mandatory(\[boolean value\])                                      |                                                                                                                                                                         |
| public str name(\[str value\])                                                   | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                       |                                                                                                                                                                         |
| public FormObjectSet referenceDataSource()                                       |                                                                                                                                                                         |
| public FieldId referenceField(\[FieldId value\])                                 |                                                                                                                                                                         |
| public str replacementFieldGroup(\[str value\])                                  |                                                                                                                                                                         |
| public Common resolveReference()                                                 |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                        | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public boolean skip(\[boolean value\])                                           | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int top(int value, \[int mode\])                                          | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMode(\[int value\])                                                | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                               | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                   |                                                                                                                                                                         |
| public int userData(\[int value\])                                               | コントロールのユーザー データを取得または設定します。                                                                                                                             |
| public int userDataItem(\[int value\])                                           | コントロールのユーザー データ品目を取得または設定します。                                                                                                                        |
| public int userDataItems(\[int value\])                                          | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                             |
| public Int64 value(\[Int64 value\])                                              |                                                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                     | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                           | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                   | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public boolean visible(\[boolean value\])                                        | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                              | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                             | コントロールの幅を取得または設定します。                                                                                                                                  |
| ::public static boolean CanUserAdd(FormDataSource formDataSource, str fieldName) |                                                                                                                                                                         |
| public void resolveChanges()                                                     |                                                                                                                                                                         |
| public void performFormLookup(xFormRun form)                                     |                                                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する国/地域コードを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの国/地域コードのコンマ区切りのリスト。

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafield"></a>メソッド dataField

    public int dataField()

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  
ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。

#### <a name="remarks"></a>備考

このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。 参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-displaytarget"></a>メソッド displayTarget

Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

Finance and Operations、クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-filtervalue"></a>メソッド filterValue

    public FilterValue filterValue(FieldBinding fieldBinding)

#### <a name="parameters"></a>パラメーター

fieldBinding  

#### <a name="return-value"></a>戻り値

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します。

| モード            | 高さの計算                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| -1 正確        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します。

| モード          | 高さの計算                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| 正確         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの HierarchyParent プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールの HierarchyParent プロパティ値。

### <a name="method-isresolvingreference"></a>メソッド isResolvingReference

    public boolean isResolvingReference()

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

フォームのコントロールの水平位置を取得または設定します。

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-leftmode"></a>メソッド leftMode

フォームのコントロールの水平配置モードを設定します。

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの水平配置モード。

### <a name="method-leftvalue"></a>メソッド leftValue

フォームのコントロールの水平位置を取得または設定します。

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-lookupreference"></a>メソッド lookupReference

    public Common lookupReference()

#### <a name="return-value"></a>戻り値

### <a name="method-mandatory"></a>メソッド mandatory

    public boolean mandatory([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-referencedatasource"></a>メソッド referenceDataSource

    public FormObjectSet referenceDataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-referencefield"></a>メソッド referenceField

    public FieldId referenceField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-replacementfieldgroup"></a>メソッド replacementFieldGroup

    public str replacementFieldGroup([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-resolvereference"></a>メソッド resolveReference

    public Common resolveReference()

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるセキュリティ キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。

### <a name="method-top"></a>メソッド top

フォームのコントロールの垂直位置を取得または設定します。

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-topmode"></a>メソッド topMode

フォームのコントロールの垂直配置モードを設定します。

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直配置モード。

### <a name="method-topvalue"></a>メソッド topValue

フォームのコントロールの垂直位置を取得または設定します。

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

コントロールのユーザー データを取得または設定します。

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ。

### <a name="method-userdataitem"></a>メソッド userDataItem

コントロールのユーザー データ品目を取得または設定します。

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ アイテム。

### <a name="method-userdataitems"></a>メソッド userDataItems

コントロールのユーザー データ項目の数を取得または設定します。

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目の数を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ項目の数。

### <a name="method-value"></a>メソッド value

    public Int64 value([Int64 value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの AutoMode を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォームのコントロールの垂直スペーシング モードを設定します。

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング モード。

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの上下の間隔を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの可視化設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します。

| モード           | 幅計算                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| -1 正確       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します。

| モード         | 幅計算                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-canuseradd"></a>メソッド CanUserAdd

    public static boolean CanUserAdd(FormDataSource formDataSource, str fieldName)

#### <a name="parameters"></a>パラメーター

formDataSource  

<!-- -->

fieldName  

#### <a name="return-value"></a>戻り値

### <a name="method-resolvechanges"></a>メソッド resolveChanges

    public void resolveChanges()

### <a name="method-performformlookup"></a>メソッド performFormLookup

    public void performFormLookup(xFormRun form)

#### <a name="parameters"></a>パラメーター

フォーム  

## <a name="class-formreferencegroupcontrol"></a>クラス FormReferenceGroupControl
    class FormReferenceGroupControl extends FormReferenceControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                              | 説明                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])            |                                                                                                                                                                         |
| public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])                     |                                                                                                                                                                         |
| public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\]) |                                                                                                                                                                         |
| public boolean alignControl(\[boolean value\])                                                                      | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                         | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                                      | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                                   | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int backgroundColor(\[int value\])                                                                           | コントロールの背景色を取得または設定します。                                                                                                                       |
| public Image backgroundImage(\[Image image\], \[int drawMode\])                                                     |                                                                                                                                                                         |
| public int backStyle(\[int value\])                                                                                 | コントロールの背景色を透明にできるかどうかを決定します。                                                                                                          |
| public int beginDrag(int x, int y)                                                                                  | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public int bold(\[int value\])                                                                                      | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                                                     |
| public int border(\[int value\])                                                                                    | コントロールの境界線のスタイルを取得または設定します。                                                                                                                |
| public container calcControlSize(int chars, int lines)                                                              | コントロールのサイズを取得します。                                                                                                                                      |
| public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])                               |                                                                                                                                                                         |
| public boolean canContain(FormControl control)                                                                      |                                                                                                                                                                         |
| public int characterSet(\[int value\])                                                                              | フォントの文字セットを取得または設定します。                                                                                                                             |
| public int colorScheme(\[int value\])                                                                               | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                            | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                                    | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public boolean contains(FormControl control)                                                                        |                                                                                                                                                                         |
| public int controlCount()                                                                                           |                                                                                                                                                                         |
| public FormControl controlNum(int controlNo)                                                                        |                                                                                                                                                                         |
| public str countryRegionCodes(\[str value\])                                                                        | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                         |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                          | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                            | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                       |
| public int displayTarget(\[int value\])                                                                             | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                                  | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                               | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enableChilds(\[boolean enable\])                                                                     |                                                                                                                                                                         |
| public boolean enabled(\[boolean value\])                                                                           | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public boolean expand(\[boolean expand\])                                                                           |                                                                                                                                                                         |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                                    |                                                                                                                                                                         |
| public str font(\[str value\])                                                                                      | 使用するコントロールのフォントの名前を取得または設定します。                                                                                                               |
| public int fontSize(\[int value\])                                                                                  | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                                               |
| public int foregroundColor(\[int value\])                                                                           | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public boolean hasChanged(\[boolean val\])                                                                          | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                                     | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                          | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                                | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                               | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                              | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                                  | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public boolean hideIfEmpty(\[boolean value\])                                                                       |                                                                                                                                                                         |
| public str hierarchyParent(\[str value\])                                                                           | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                                   | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public boolean isContainer()                                                                                        |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                        | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                                       | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                            | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。                                                                     |
| public boolean isValid()                                                                                            |                                                                                                                                                                         |
| public boolean italic(\[boolean value\])                                                                            |                                                                                                                                                                         |
| public str label(\[str value\])                                                                                     | コントロールのラベルを取得または設定します。                                                                                                                                   |
| public int labelAlignment(\[int value\])                                                                            |                                                                                                                                                                         |
| public int labelBold(\[int value\])                                                                                 |                                                                                                                                                                         |
| public int labelCharacterSet(\[int value\])                                                                         |                                                                                                                                                                         |
| public str labelFont(\[str value\])                                                                                 |                                                                                                                                                                         |
| public int labelFontSize(\[int value\])                                                                             |                                                                                                                                                                         |
| public int labelForegroundColor(\[int value\])                                                                      |                                                                                                                                                                         |
| public int labelGuide(\[int value\])                                                                                |                                                                                                                                                                         |
| public int labelHeight(int value, \[int mode\])                                                                     |                                                                                                                                                                         |
| public int labelHeightMode(\[int value\])                                                                           |                                                                                                                                                                         |
| public int labelHeightValue(\[int value\])                                                                          |                                                                                                                                                                         |
| public boolean labelItalic(\[boolean value\])                                                                       |                                                                                                                                                                         |
| public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                                |                                                                                                                                                                         |
| public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                    |                                                                                                                                                                         |
| public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                      |                                                                                                                                                                         |
| public int labelPosition(\[int value\])                                                                             |                                                                                                                                                                         |
| public boolean labelUnderline(\[boolean value\])                                                                    |                                                                                                                                                                         |
| public int labelWidth(int value, \[int mode\])                                                                      |                                                                                                                                                                         |
| public int labelWidthMode(\[int value\])                                                                            |                                                                                                                                                                         |
| public int labelWidthValue(\[int value\])                                                                           |                                                                                                                                                                         |
| public boolean leave()                                                                                              |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                            | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMode(\[int value\])                                                                                  | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                                 | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public boolean mandatory(\[boolean value\])                                                                         |                                                                                                                                                                         |
| public boolean markAsUserAdd(\[boolean value\])                                                                     | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public boolean modified()                                                                                           |                                                                                                                                                                         |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                                     | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                         | ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。                                                                                                       |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                         | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                           | ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。                                                                                                |
| public int moveControl(int controlId, \[int insertAfterId\])                                                        |                                                                                                                                                                         |
| public str name(\[str value\])                                                                                      | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                          |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                             |                                                                                                                                                                         |
| public FormControl parentControl()                                                                                  | コントロールの親コントロールを取得します。                                                                                                                           |
| public str previewPartRef(\[str value\])                                                                            |                                                                                                                                                                         |
| public int promptrect(\[int value\])                                                                                |                                                                                                                                                                         |
| public FieldId referenceField(\[FieldId value\])                                                                    |                                                                                                                                                                         |
| public str replacementFieldGroup(\[str value\])                                                                     |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                           | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int showContextMenu(int menuHandle)                                                                          | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showLabel(\[boolean value\])                                                                         |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                              | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[SortOrder sortDirection\])                                                                        |                                                                                                                                                                         |
| public int style(\[int value\])                                                                                     |                                                                                                                                                                         |
| public str toolTip()                                                                                                | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                             | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMode(\[int value\])                                                                                   | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                                  | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                                      |                                                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                         |                                                                                                                                                                         |
| public boolean SysObsoleteAttribute(container data)                                                                 |                                                                                                                                                                         |
| public int userData(\[int value\])                                                                                  | コントロールのユーザー データを取得または設定します。                                                                                                                             |
| public int userDataItem(\[int value\])                                                                              | コントロールのユーザー データ品目を取得または設定します。                                                                                                                        |
| public int userDataItems(\[int value\])                                                                             | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                             |
| public int userDisable(\[int value\])                                                                               | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                                     |
| public int userHeight(\[int value\])                                                                                | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                                                    |
| public int userHide(\[int value\])                                                                                  | コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。                                                                                      |
| public int userOrgContainer(\[int value\])                                                                          | コントロールの組織コンテナを取得または設定します。                                                                                                                |
| public int userOrgSibling(\[int value\])                                                                            | コントロールの組織兄弟を取得または設定します。                                                                                                                  |
| public str userPromptText(\[str value\])                                                                            | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                                       |
| public int userSecurityLevel(\[int value\])                                                                         | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                   |
| public int userSkip(\[int value\])                                                                                  | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。                    |
| public int userWidth(\[int value\])                                                                                 | ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。                                                                                           |
| public boolean useUserLayout(\[boolean value\])                                                                     |                                                                                                                                                                         |
| public boolean validate()                                                                                           |                                                                                                                                                                         |
| public Int64 value(\[Int64 value\])                                                                                 |                                                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                        | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                              | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                                      | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public int viewEditMode(\[int value\])                                                                              |                                                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                           | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                           | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                                 | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                                | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void lostFocus()                                                                                             | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void displayControl()                                                                                        | コントロールを表示します。                                                                                                                                                   |
| private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])                                         |                                                                                                                                                                         |
| public void jumpRef()                                                                                               |                                                                                                                                                                         |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])         |                                                                                                                                                                         |
| public void cut()                                                                                                   | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                                       | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                            |                                                                                                                                                                         |
| public void dragLeave()                                                                                             | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void filter(\[str filterStr\])                                                                               |                                                                                                                                                                         |
| public void arrange()                                                                                               |                                                                                                                                                                         |
| public void enter()                                                                                                 |                                                                                                                                                                         |
| public void paste()                                                                                                 | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])                                       |                                                                                                                                                                         |
| public void setFocus()                                                                                              | コントロールにフォーカスを設定します。                                                                                                                                          |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                         |                                                                                                                                                                         |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                          |                                                                                                                                                                         |
| public void inputSearch(str searchStr)                                                                              | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                           | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void mouseLeave()                                                                                            | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void prefColumnSize(int width, int height)                                                                   | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void undo()                                                                                                  |                                                                                                                                                                         |
| public void gotFocus()                                                                                              | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                        |                                                                                                                                                                         |
| public void lookup()                                                                                                |                                                                                                                                                                         |
| public void resetUserSetting()                                                                                      | コントロールのユーザー設定をリセットします。                                                                                                                               |
| private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])                                           |                                                                                                                                                                         |
| private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])                                        |                                                                                                                                                                         |
| public void copy()                                                                                                  | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                               | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void context()                                                                                               | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void endDrag()                                                                                               | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |

### <a name="method-addcontrol"></a>メソッド addControl

    public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])

#### <a name="parameters"></a>パラメーター

controlType  

<!-- -->

controlName  

<!-- -->

insertAfter  

#### <a name="return-value"></a>戻り値

### <a name="method-addcontrolex"></a>メソッド addControlEx

    public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])

#### <a name="parameters"></a>パラメーター

controlClass  

<!-- -->

controlName  

<!-- -->

insertAfter  

#### <a name="return-value"></a>戻り値

### <a name="method-adddatafield"></a>メソッド addDataField

    public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSourceId  

<!-- -->

fieldId  

<!-- -->

insertAfter  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  
プロパティの新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  
allowEdit プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

    public boolean allowSysSetup()

#### <a name="return-value"></a>戻り値

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  
プロパティの新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backgroundimage"></a>メソッド backgroundImage

    public Image backgroundImage([Image image], [int drawMode])

#### <a name="parameters"></a>パラメーター

image  

<!-- -->

drawMode  

#### <a name="return-value"></a>戻り値

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。

    public int beginDrag(int x, int y)

#### <a name="parameters"></a>パラメーター

x  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

<!-- -->

y  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 先頭値 | 説明 |
|-------|-------------|
| 0     | 自動        |
| 1     | 3D          |
| 2     | 単一明細行 |
| 3     | 均一        |
| 4     | None        |

### <a name="method-calccontrolsize"></a>メソッド calcControlSize

コントロールのサイズを取得します。

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a>パラメーター

chars  
高さを決定するために使用する行数。

<!-- -->

明細行  
高さを決定するために使用する行数。

#### <a name="return-value"></a>戻り値

幅と高さを保持するコンテナー。

### <a name="method-canadddatafield"></a>メソッド canAddDataField

    public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSourceId  

<!-- -->

fieldId  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-cancontain"></a>メソッド canContain

    public boolean canContain(FormControl control)

#### <a name="parameters"></a>パラメーター

control  

#### <a name="return-value"></a>戻り値

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 先頭値 | 説明          |
|-------|----------------------|
| 0     | ANSI\_CHARSET        |
| 1     | DEFAULT\_CHARSET     |
| 2     | SYMBOL\_CHARSET      |
| 77    | MAC\_CHARSET         |
| 128   | SHIFTJIS\_CHARSET    |
| 129   | HANGUL\_CHARSET      |
| 134   | GB2312\_CHARSET      |
| 136   | CHINESEBIG5\_CHARSET |
| 161   | GREEK\_CHARSET       |
| 162   | TURKISH\_CHARSET     |
| 163   | VIETNAMESE\_CHARSET  |
| 186   | BALTIC\_CHARSET      |
| 204   | RUSSIAN\_CHARSET     |
| 238   | EASTEUROPE\_CHARSET  |
| 255   | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 金額 | 説明    |
|-------|----------------|
| 130   | JOHAB\_CHARSET |

次のテーブルの値は、中東言語語版 Windows の値です。

| 先頭値 | 説明     |
|-------|-----------------|
| 177   | HEBREW\_CHARSET |
| 178   | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Windows の値です。

| 先頭値 | 説明   |
|-------|---------------|
| 222   | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 先頭値 | スタイル                 |
|-------|-----------------------|
| 0     | 既定               |
| 1     | Windows パレット   |
| 2     | 真の配色 |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるコンフィギュレーション キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。

#### <a name="remarks"></a>備考

返されるリストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。

### <a name="method-contains"></a>メソッド contains

    public boolean contains(FormControl control)

#### <a name="parameters"></a>パラメーター

control  

#### <a name="return-value"></a>戻り値

### <a name="method-controlcount"></a>メソッド controlCount

    public int controlCount()

#### <a name="return-value"></a>戻り値

### <a name="method-controlnum"></a>メソッド controlNum

    public FormControl controlNum(int controlNo)

#### <a name="parameters"></a>パラメーター

controlNo  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する国/地域コードを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの国/地域コードのコンマ区切りのリスト。

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  
ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。

#### <a name="remarks"></a>備考

このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。 参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-displaytarget"></a>メソッド displayTarget

Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

Finance and Operations、クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  
ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

#### <a name="remarks"></a>備考

dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。

### <a name="method-dragover"></a>メソッド dragOver

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragoverex"></a>メソッド dragOverEx

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragtext"></a>メソッド dragText

フォーム コントロールをドラッグしたときに表示されるテキストを取得します。

    public str dragText()

#### <a name="return-value"></a>戻り値

コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。

### <a name="method-enablechilds"></a>メソッド enableChilds

    public boolean enableChilds([boolean enable])

#### <a name="parameters"></a>パラメーター

enable  

#### <a name="return-value"></a>戻り値

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが有効かどうかを指定するブール値; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-expand"></a>メソッド expand

    public boolean expand([boolean expand])

#### <a name="parameters"></a>パラメーター

expand  

#### <a name="return-value"></a>戻り値

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-haschanged"></a>メソッド hasChanged

コントロールの内容が変更されたかどうかを示す値を設定するか返します。

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  
コントロールの hasChanged 値として割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの内容が変更された場合は true。それ以外の場合は、false。

### <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

    public boolean hasUserSetting()

#### <a name="return-value"></a>戻り値

コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
高さの計算方法を示す整数。オプション。

<!-- -->

モード  
高さの計算方法を示す整数。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します。

| モード            | 高さの計算                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| -1 正確        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの高さの計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します。

| モード          | 高さの計算                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| 正確         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  
高さをピクセル単位で指定する整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを取得します。

    public str helpField()

#### <a name="return-value"></a>戻り値

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

#### <a name="remarks"></a>備考

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのヘルプ テキストとして割り当てられる値。

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hideifempty"></a>メソッド hideIfEmpty

    public boolean hideIfEmpty([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの HierarchyParent プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールの HierarchyParent プロパティ値。

### <a name="method-hwnd"></a>メソッド hWnd

コントロールの Windows ハンドルを取得します。

    public int hWnd()

#### <a name="return-value"></a>戻り値

ハンドラーコントロールのハンドルです。

#### <a name="remarks"></a>備考

この処理は、Windows API で使用できます。

### <a name="method-iscontainer"></a>メソッド isContainer

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を取得します。

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

コントロールが表示される場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

### <a name="method-isrestricted"></a>メソッド isRestricted

コントロールが制限されるかどうかを示す値を取得します。

    public boolean isRestricted()

#### <a name="return-value"></a>戻り値

コントロールが制限される場合は true。それ以外の場合は false。

### <a name="method-isusersetupenabled"></a>メソッド isUserSetupEnabled

コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a>パラメーター

neededSetupRights  
コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。

#### <a name="return-value"></a>戻り値

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

### <a name="method-isvalid"></a>メソッド isValid

    public boolean isValid()

#### <a name="return-value"></a>戻り値

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-labelalignment"></a>メソッド labelAlignment

    public int labelAlignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelbold"></a>メソッド labelBold

    public int labelBold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

    public int labelCharacterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfont"></a>メソッド labelFont

    public str labelFont([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfontsize"></a>メソッド labelFontSize

    public int labelFontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelforegroundcolor"></a>メソッド labelForegroundColor

    public int labelForegroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelguide"></a>メソッド labelGuide

    public int labelGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheight"></a>メソッド labelHeight

    public int labelHeight(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightmode"></a>メソッド labelHeightMode

    public int labelHeightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightvalue"></a>メソッド labelHeightValue

    public int labelHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelitalic"></a>メソッド labelItalic

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmousedblclick"></a>メソッド labelMouseDblClick

    public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmousedown"></a>メソッド labelMouseDown

    public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmouseup"></a>メソッド labelMouseUp

    public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelposition"></a>メソッド labelPosition

    public int labelPosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelunderline"></a>メソッド labelUnderline

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidth"></a>メソッド labelWidth

    public int labelWidth(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthmode"></a>メソッド labelWidthMode

    public int labelWidthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthvalue"></a>メソッド labelWidthValue

    public int labelWidthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leave"></a>メソッド leave

    public boolean leave()

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

フォームのコントロールの水平位置を取得または設定します。

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-leftmode"></a>メソッド leftMode

フォームのコントロールの水平配置モードを設定します。

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの水平配置モード。

### <a name="method-leftvalue"></a>メソッド leftValue

フォームのコントロールの水平位置を取得または設定します。

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-mandatory"></a>メソッド mandatory

    public boolean mandatory([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-markasuseradd"></a>メソッド markAsUserAdd

ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。

### <a name="method-modified"></a>メソッド modified

    public boolean modified()

#### <a name="return-value"></a>戻り値

### <a name="method-mousedblclick"></a>メソッド mouseDblClick

コントロールがユーザーにダブルクリックされると呼び出されます。

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-mousemove"></a>メソッド mouseMove

ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-movecontrol"></a>メソッド moveControl

    public int moveControl(int controlId, [int insertAfterId])

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->

insertAfterId  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parentcontrol"></a>メソッド parentControl

コントロールの親コントロールを取得します。

    public FormControl parentControl()

#### <a name="return-value"></a>戻り値

コントロールの親コントロール。

### <a name="method-previewpartref"></a>メソッド previewPartRef

    public str previewPartRef([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-promptrect"></a>メソッド promptrect

    public int promptrect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-referencefield"></a>メソッド referenceField

    public FieldId referenceField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-replacementfieldgroup"></a>メソッド replacementFieldGroup

    public str replacementFieldGroup([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるセキュリティ キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。

### <a name="method-showcontextmenu"></a>メソッド showContextMenu

コントロールのショートカット メニューを表示します。

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a>パラメーター

menuHandle  
表示するメニューの ID。

#### <a name="return-value"></a>戻り値

通話が成功したかどうかを示す整数値。

### <a name="method-showlabel"></a>メソッド showLabel

    public boolean showLabel([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。

### <a name="method-sort"></a>メソッド sort

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a>パラメーター

sortDirection  

#### <a name="return-value"></a>戻り値

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tooltip"></a>メソッド toolTip

コントロールのツール ヒント テキストを取得します。

    public str toolTip()

#### <a name="return-value"></a>戻り値

コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。

#### <a name="remarks"></a>備考

メソッドを上書きして、toolTip メソッドに値を渡すことができます。

### <a name="method-top"></a>メソッド top

フォームのコントロールの垂直位置を取得または設定します。

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-topmode"></a>メソッド topMode

フォームのコントロールの垂直配置モードを設定します。

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直配置モード。

### <a name="method-topvalue"></a>メソッド topValue

フォームのコントロールの垂直位置を取得または設定します。

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

コントロールのユーザー データを取得または設定します。

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ。

### <a name="method-userdataitem"></a>メソッド userDataItem

コントロールのユーザー データ品目を取得または設定します。

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ アイテム。

### <a name="method-userdataitems"></a>メソッド userDataItems

コントロールのユーザー データ項目の数を取得または設定します。

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目の数を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ項目の数。

### <a name="method-userdisable"></a>メソッド userDisable

ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。

    public int userDisable([int value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。

### <a name="method-userheight"></a>メソッド userHeight

コントロールのカスタム ユーザーの高さを取得または設定します。

    public int userHeight([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザーの高さ (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのカスタム ユーザーの高さ。

### <a name="method-userhide"></a>メソッド userHide

コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。

    public int userHide([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

#### <a name="remarks"></a>備考

ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 このメソッドを使用すると、プログラムによって値を決定して設定できます。

### <a name="method-userorgcontainer"></a>メソッド userOrgContainer

コントロールの組織コンテナを取得または設定します。

    public int userOrgContainer([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織コンテナー (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織コンテナー。

### <a name="method-userorgsibling"></a>メソッド userOrgSibling

コントロールの組織兄弟を取得または設定します。

    public int userOrgSibling([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織の兄弟 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織の兄弟。

### <a name="method-userprompttext"></a>メソッド userPromptText

コントロールのユーザーラベル テキストを取得または設定します。

    public str userPromptText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー ラベルのテキスト (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザーラベル テキスト。

### <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

コントロールのユーザー セキュリティ レベルを取得または設定します。

    public int userSecurityLevel([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー セキュリティ レベル (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザー セキュリティ レベル。

### <a name="method-userskip"></a>メソッド userSkip

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。

    public int userSkip([int value])

#### <a name="parameters"></a>パラメーター

値  
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。

#### <a name="return-value"></a>戻り値

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

### <a name="method-userwidth"></a>メソッド userWidth

ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅として使用するピクセル数 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

### <a name="method-useuserlayout"></a>メソッド useUserLayout

    public boolean useUserLayout([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-validate"></a>メソッド validate

    public boolean validate()

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

    public Int64 value([Int64 value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの AutoMode 値を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode 値を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォームのコントロールの垂直スペーシング モードを設定します。

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング モード。

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの上下の間隔を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの可視化設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
幅の計算方法を示す整数です (オプション)。

<!-- -->

モード  
幅の計算方法を示す整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します。

| モード           | 幅計算                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| -1 正確       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロール幅の計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します。

| モード         | 幅計算                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  
幅をピクセル単位で指定する整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-onmodified"></a>メソッド OnModified

    private void OnModified([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-jumpref"></a>メソッド jumpRef

    public void jumpRef()

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

### <a name="method-arrange"></a>メソッド arrange

    public void arrange()

### <a name="method-enter"></a>メソッド enter

    public void enter()

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-onvalidating"></a>メソッド OnValidating

    private void OnValidating([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-drop"></a>メソッド drop

ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-undo"></a>メソッド undo

    public void undo()

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-lookup"></a>メソッド lookup

    public void lookup()

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-onlookup"></a>メソッド OnLookup

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-onvalidated"></a>メソッド OnValidated

    private void OnValidated([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-dropex"></a>メソッド dropEx

ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

## <a name="class-formreferenceobject"></a>クラス FormReferenceObject
    class FormReferenceObject extends FormDataObject

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                    | 説明                                                                                                                                                             |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public int allowAdd(\[int value\])                                        | フォーム データ オブジェクトの allowAdd プロパティの値を設定するか返します。                                                                                            |
| public boolean allowEdit(\[boolean value\])                               | ユーザーがコントロールの内容を変更できるかどうかを示します。                                                                                                      |
| public FieldId dataField(\[FieldId value\])                               |                                                                                                                                                                         |
| public boolean enabled(\[boolean value\])                                 | オブジェクトを有効または無効にするかどうかを示します。                                                                                                                      |
| public Common lookupReference(FormReferenceControl formReferenceControl)  |                                                                                                                                                                         |
| public boolean mandatory(\[boolean value\])                               | データ フィールドが必須であるかどうかを示す値を設定するか返します。                                                                                             |
| public Common resolveReference(FormReferenceControl formReferenceControl) |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                    | ユーザーが Tab キーを押して、データ ソースに関連付けられたコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。 |
| public boolean visible(\[boolean value\])                                 | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |

### <a name="method-allowadd"></a>メソッド allowAdd

フォーム データ オブジェクトの allowAdd プロパティの値を設定するか返します。

    public int allowAdd([int value])

#### <a name="parameters"></a>パラメーター

値  
allowEdit プロパティに割り当てられている値。

#### <a name="return-value"></a>戻り値

allowAdd プロパティが No、Restricted もしくは Yes に設定されているかどうかを示す FormAllowAdd 列挙値。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを示します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-datafield"></a>メソッド dataField

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを示します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-lookupreference"></a>メソッド lookupReference

    public Common lookupReference(FormReferenceControl formReferenceControl)

#### <a name="parameters"></a>パラメーター

formReferenceControl  

#### <a name="return-value"></a>戻り値

### <a name="method-mandatory"></a>メソッド mandatory

データ フィールドが必須であるかどうかを示す値を設定するか返します。

    public boolean mandatory([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フィールドの必須プロパティに割り当てられる値。

#### <a name="return-value"></a>戻り値

フィールドが必須項目である場合は true。それ以外の場合は、false。

### <a name="method-resolvereference"></a>メソッド resolveReference

    public Common resolveReference(FormReferenceControl formReferenceControl)

#### <a name="parameters"></a>パラメーター

formReferenceControl  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押して、データ ソースに関連付けられたコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに関連付けられているデータ ソースの skip プロパティに割り当てられている値 (オプション)。

#### <a name="return-value"></a>戻り値

データ ソースに関連付けられているコントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。 コントロールまたはデータ ソースのスキップ値が true の場合、コントロールはスキップされます。

### <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの表示設定に割り当てられている値。

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。 既定は true です。

#### <a name="remarks"></a>備考

データ ソース フィールドを参照するコントロールは、コントロールおよび基になるデータ ソース フィールドの両方で Visible プロパティが true に設定されている場合にのみ表示されます。 コントロールの代わりにデータ ソース フィールドのプロパティを設定することにより、フォーム全体で一貫してフィールドが処理されることを確認します。 これにより、アップグレードが容易になります。

## <a name="class-formrichtextcontrol"></a>クラス FormRichTextControl
    class FormRichTextControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                                                          |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                                                     |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                                                |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                                                         |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                                                             |
| public int charFromPos(int x, int y)                                                                        |                                                                                                                                                                         |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                                                         |
| public int dataFieldArrayIndex()                                                                            |                                                                                                                                                                         |
| public FieldName dataFieldName()                                                                            |                                                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                       |
| public int direction(\[int value\])                                                                         |                                                                                                                                                                         |
| public int displayHeight(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                                                         |
| public AutoMode displayHeightMode(\[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public int displayHeightValue(\[int value\])                                                                |                                                                                                                                                                         |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                                                         |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                                                         |
| public int fastTabSummary(\[int value\])                                                                    |                                                                                                                                                                         |
| public int find(\[str findStr\], \[int start\], \[int end\], \[int flags\])                                 |                                                                                                                                                                         |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public container getCursorPos()                                                                             |                                                                                                                                                                         |
| public int getFirstVisibleLine()                                                                            |                                                                                                                                                                         |
| public str getLine(int lineNo)                                                                              |                                                                                                                                                                         |
| public int getLineCount()                                                                                   |                                                                                                                                                                         |
| public container getSelection()                                                                             |                                                                                                                                                                         |
| public boolean hasChanged(\[boolean val\])                                                                  | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public int iMEMode(\[int value\])                                                                           |                                                                                                                                                                         |
| public boolean isContainer()                                                                                |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。                                                                   |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                                                         |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                                                   |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                                                         |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                                                         |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                                                         |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                                                         |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                                                         |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                                                         |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                                                         |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                                                         |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                                                         |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                                                         |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                                                         |
| public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                        |                                                                                                                                                                         |
| public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                            |                                                                                                                                                                         |
| public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                              |                                                                                                                                                                         |
| public int labelPosition(\[int value\])                                                                     |                                                                                                                                                                         |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                                                         |
| public int labelWidth(int value, \[int mode\])                                                              |                                                                                                                                                                         |
| public int labelWidthMode(\[int value\])                                                                    |                                                                                                                                                                         |
| public int labelWidthValue(\[int value\])                                                                   |                                                                                                                                                                         |
| public boolean leave()                                                                                      |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMode(\[int value\])                                                                          | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                         | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int limitText(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                                                         |
| public AutoMode limitTextMode(\[AutoMode mode\])                                                            |                                                                                                                                                                         |
| public int limitTextValue(\[int value\])                                                                    |                                                                                                                                                                         |
| public int lineFromChar(int charIndex)                                                                      |                                                                                                                                                                         |
| public int lineIndex(int lineNo)                                                                            |                                                                                                                                                                         |
| public int lineLength(int lineNo)                                                                           |                                                                                                                                                                         |
| public int lookupButton(\[int value\])                                                                      |                                                                                                                                                                         |
| public boolean mandatory(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean markAsUserAdd(\[boolean value\])                                                             | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public boolean modified()                                                                                   |                                                                                                                                                                         |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                             | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。                                                                                                       |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                   | ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。                                                                                                |
| public boolean multiLine(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                     |                                                                                                                                                                         |
| public FormControl parentControl()                                                                          | コントロールの親コントロールを取得します。                                                                                                                           |
| public container posFromChar(int charIndex)                                                                 |                                                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                                                         |
| public boolean replaceOnLookup(\[boolean value\])                                                           |                                                                                                                                                                         |
| public int replaceText(\[str findStr\], \[str replaceStr\], \[int start\], \[int end\], \[int flags\])      |                                                                                                                                                                         |
| public int searchAfterInput(\[int value\])                                                                  |                                                                                                                                                                         |
| public int searchMode(\[int value\])                                                                        |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[SortOrder sortDirection\])                                                                |                                                                                                                                                                         |
| public int style(\[int value\])                                                                             |                                                                                                                                                                         |
| public str text(\[str value\])                                                                              |                                                                                                                                                                         |
| public str toolTip()                                                                                        | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                     | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMode(\[int value\])                                                                           | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                          | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                              |                                                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean SysObsoleteAttribute(container data)                                                         |                                                                                                                                                                         |
| public int userData(\[int value\])                                                                          | コントロールのユーザー データを取得または設定します。                                                                                                                             |
| public int userDataItem(\[int value\])                                                                      | コントロールのユーザー データ品目を取得または設定します。                                                                                                                        |
| public int userDataItems(\[int value\])                                                                     | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                             |
| public int userDisable(\[int value\])                                                                       | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                                     |
| public int userFastTabSummary(\[int value\])                                                                |                                                                                                                                                                         |
| public int userHeight(\[int value\])                                                                        | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                                                    |
| public int userHide(\[int value\])                                                                          | コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。                                                                                      |
| public int userOrgContainer(\[int value\])                                                                  | コントロールの組織コンテナを取得または設定します。                                                                                                                |
| public int userOrgSibling(\[int value\])                                                                    | コントロールの組織兄弟を取得または設定します。                                                                                                                  |
| public str userPromptText(\[str value\])                                                                    | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                                       |
| public int userSecurityLevel(\[int value\])                                                                 | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                   |
| public int userSkip(\[int value\])                                                                          | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。                    |
| public int userWidth(\[int value\])                                                                         | ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。                                                                                           |
| public boolean validate()                                                                                   |                                                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void lookup()                                                                                        |                                                                                                                                                                         |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void performFormLookup(xFormRun form)                                                                |                                                                                                                                                                         |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])                                   |                                                                                                                                                                         |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void scrollCursor()                                                                                  |                                                                                                                                                                         |
| public void undo()                                                                                          |                                                                                                                                                                         |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void setSelection(int charIndexFrom, int charIndexTo)                                                |                                                                                                                                                                         |
| public void pasteText(str pasteStr, \[boolean InsertSel\])                                                  |                                                                                                                                                                         |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| public void filter(\[str filterStr\])                                                                       |                                                                                                                                                                         |
| public void enter()                                                                                         |                                                                                                                                                                         |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])         |                                                                                                                                                                         |
| private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])                               |                                                                                                                                                                         |
| public void setCursorPos(int x, int y)                                                                      |                                                                                                                                                                         |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void lineScroll(int dx, int dy)                                                                      |                                                                                                                                                                         |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])       |                                                                                                                                                                         |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void textChange()                                                                                    |                                                                                                                                                                         |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void jumpRef()                                                                                       |                                                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

    public boolean allowSysSetup()

#### <a name="return-value"></a>戻り値

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

### <a name="method-arrayindex"></a>メソッド arrayIndex

    public int arrayIndex([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。

    public int beginDrag(int x, int y)

#### <a name="parameters"></a>パラメーター

x  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

<!-- -->

y  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 先頭値 | 説明 |
|-------|-------------|
| 0     | 自動        |
| 1     | 3D          |
| 2     | 単一明細行 |
| 3     | 均一        |
| 4     | None        |

### <a name="method-cachedatamethod"></a>メソッド cacheDataMethod

    public int cacheDataMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-calccontrolsize"></a>メソッド calcControlSize

コントロールのサイズを取得します。

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a>パラメーター

chars  
高さを決定するために使用する行数。

<!-- -->

明細行  
高さを決定するために使用する行数。

#### <a name="return-value"></a>戻り値

幅と高さを保持するコンテナー。

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 先頭値 | 説明          |
|-------|----------------------|
| 0     | ANSI\_CHARSET        |
| 1     | DEFAULT\_CHARSET     |
| 2     | SYMBOL\_CHARSET      |
| 77    | MAC\_CHARSET         |
| 128   | SHIFTJIS\_CHARSET    |
| 129   | HANGUL\_CHARSET      |
| 134   | GB2312\_CHARSET      |
| 136   | CHINESEBIG5\_CHARSET |
| 161   | GREEK\_CHARSET       |
| 162   | TURKISH\_CHARSET     |
| 163   | VIETNAMESE\_CHARSET  |
| 186   | BALTIC\_CHARSET      |
| 204   | RUSSIAN\_CHARSET     |
| 238   | EASTEUROPE\_CHARSET  |
| 255   | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 金額 | 説明    |
|-------|----------------|
| 130   | JOHAB\_CHARSET |

次のテーブルの値は、中東言語語版 Windows の値です。

| 先頭値 | 説明     |
|-------|-----------------|
| 177   | HEBREW\_CHARSET |
| 178   | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Windows の値です。

| 先頭値 | 説明   |
|-------|---------------|
| 222   | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-charfrompos"></a>メソッド charFromPos

    public int charFromPos(int x, int y)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

#### <a name="return-value"></a>戻り値

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 先頭値 | スタイル                 |
|-------|-----------------------|
| 0     | 既定               |
| 1     | Windows パレット   |
| 2     | 真の配色 |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。

#### <a name="remarks"></a>備考

返されるリストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する国/地域コードを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの国/地域コードのコンマ区切りのリスト。

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafield"></a>メソッド dataField

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafieldarrayindex"></a>メソッド dataFieldArrayIndex

    public int dataFieldArrayIndex()

#### <a name="return-value"></a>戻り値

### <a name="method-datafieldname"></a>メソッド dataFieldName

    public FieldName dataFieldName()

#### <a name="return-value"></a>戻り値

### <a name="method-datamethod"></a>メソッド dataMethod

    public str dataMethod([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  
ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。

#### <a name="remarks"></a>備考

このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。 参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-direction"></a>メソッド direction

    public int direction([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheight"></a>メソッド displayHeight

    public int displayHeight([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightmode"></a>メソッド displayHeightMode

    public AutoMode displayHeightMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightvalue"></a>メソッド displayHeightValue

    public int displayHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylength"></a>メソッド displayLength

    public int displayLength([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthmode"></a>メソッド displayLengthMode

    public AutoMode displayLengthMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthvalue"></a>メソッド displayLengthValue

    public int displayLengthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

Finance and Operations、クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-dragover"></a>メソッド dragOver

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragoverex"></a>メソッド dragOverEx

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragtext"></a>メソッド dragText

フォーム コントロールをドラッグしたときに表示されるテキストを取得します。

    public str dragText()

#### <a name="return-value"></a>戻り値

コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-fasttabsummary"></a>メソッド fastTabSummary

    public int fastTabSummary([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-find"></a>メソッド find

    public int find([str findStr], [int start], [int end], [int flags])

#### <a name="parameters"></a>パラメーター

findStr  

<!-- -->

開始  

<!-- -->

終了  

<!-- -->

flags  

#### <a name="return-value"></a>戻り値

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-getcursorpos"></a>メソッド getCursorPos

    public container getCursorPos()

#### <a name="return-value"></a>戻り値

### <a name="method-getfirstvisibleline"></a>メソッド getFirstVisibleLine

    public int getFirstVisibleLine()

#### <a name="return-value"></a>戻り値

### <a name="method-getline"></a>メソッド getLine

    public str getLine(int lineNo)

#### <a name="parameters"></a>パラメーター

lineNo  

#### <a name="return-value"></a>戻り値

### <a name="method-getlinecount"></a>メソッド getLineCount

    public int getLineCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getselection"></a>メソッド getSelection

    public container getSelection()

#### <a name="return-value"></a>戻り値

### <a name="method-haschanged"></a>メソッド hasChanged

コントロールの内容が変更されたかどうかを示す値を設定するか返します。

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  
コントロールの hasChanged 値として割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの内容が変更された場合は true。それ以外の場合は、false。

### <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

    public boolean hasUserSetting()

#### <a name="return-value"></a>戻り値

コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します。

| モード            | 高さの計算                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| -1 正確        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。         | 高さの計算                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| 正確         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを取得します。

    public str helpField()

#### <a name="return-value"></a>戻り値

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

#### <a name="remarks"></a>備考

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの HierarchyParent プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールの HierarchyParent プロパティ値。

### <a name="method-hwnd"></a>メソッド hWnd

コントロールの Windows ハンドルを取得します。

    public int hWnd()

#### <a name="return-value"></a>戻り値

ハンドラーコントロールのハンドルです。

#### <a name="remarks"></a>備考

この処理は、Windows API で使用できます。

### <a name="method-imemode"></a>メソッド iMEMode

    public int iMEMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を取得します。

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

コントロールが表示される場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

### <a name="method-isrestricted"></a>メソッド isRestricted

コントロールが制限されるかどうかを示す値を取得します。

    public boolean isRestricted()

#### <a name="return-value"></a>戻り値

コントロールが制限される場合は true。それ以外の場合は false。

### <a name="method-isusersetupenabled"></a>メソッド isUserSetupEnabled

コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a>パラメーター

neededSetupRights  
コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。

#### <a name="return-value"></a>戻り値

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-labelalignment"></a>メソッド labelAlignment

    public int labelAlignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelbold"></a>メソッド labelBold

    public int labelBold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

    public int labelCharacterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfont"></a>メソッド labelFont

    public str labelFont([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfontsize"></a>メソッド labelFontSize

    public int labelFontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelforegroundcolor"></a>メソッド labelForegroundColor

    public int labelForegroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelguide"></a>メソッド labelGuide

    public int labelGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheight"></a>メソッド labelHeight

    public int labelHeight(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightmode"></a>メソッド labelHeightMode

    public int labelHeightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightvalue"></a>メソッド labelHeightValue

    public int labelHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelitalic"></a>メソッド labelItalic

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmousedblclick"></a>メソッド labelMouseDblClick

    public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmousedown"></a>メソッド labelMouseDown

    public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmouseup"></a>メソッド labelMouseUp

    public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelposition"></a>メソッド labelPosition

    public int labelPosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelunderline"></a>メソッド labelUnderline

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidth"></a>メソッド labelWidth

    public int labelWidth(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthmode"></a>メソッド labelWidthMode

    public int labelWidthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthvalue"></a>メソッド labelWidthValue

    public int labelWidthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leave"></a>メソッド leave

    public boolean leave()

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

フォームのコントロールの水平位置を取得または設定します。

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-leftmode"></a>メソッド leftMode

フォームのコントロールの水平配置モードを設定します。

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの水平配置モード。

### <a name="method-leftvalue"></a>メソッド leftValue

フォームのコントロールの水平位置を取得または設定します。

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-limittext"></a>メソッド limitText

    public int limitText([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextmode"></a>メソッド limitTextMode

    public AutoMode limitTextMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextvalue"></a>メソッド limitTextValue

    public int limitTextValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linefromchar"></a>メソッド lineFromChar

    public int lineFromChar(int charIndex)

#### <a name="parameters"></a>パラメーター

charIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-lineindex"></a>メソッド lineIndex

    public int lineIndex(int lineNo)

#### <a name="parameters"></a>パラメーター

lineNo  

#### <a name="return-value"></a>戻り値

### <a name="method-linelength"></a>メソッド lineLength

    public int lineLength(int lineNo)

#### <a name="parameters"></a>パラメーター

lineNo  

#### <a name="return-value"></a>戻り値

### <a name="method-lookupbutton"></a>メソッド lookupButton

    public int lookupButton([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-mandatory"></a>メソッド mandatory

    public boolean mandatory([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-markasuseradd"></a>メソッド markAsUserAdd

ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。

### <a name="method-modified"></a>メソッド modified

    public boolean modified()

#### <a name="return-value"></a>戻り値

### <a name="method-mousedblclick"></a>メソッド mouseDblClick

コントロールがユーザーにダブルクリックされると呼び出されます。

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-mousemove"></a>メソッド mouseMove

ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-multiline"></a>メソッド multiLine

    public boolean multiLine([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parentcontrol"></a>メソッド parentControl

コントロールの親コントロールを取得します。

    public FormControl parentControl()

#### <a name="return-value"></a>戻り値

コントロールの親コントロール。

### <a name="method-posfromchar"></a>メソッド posFromChar

    public container posFromChar(int charIndex)

#### <a name="parameters"></a>パラメーター

charIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-promptrect"></a>メソッド promptrect

    public int promptrect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-replaceonlookup"></a>メソッド replaceOnLookup

    public boolean replaceOnLookup([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-replacetext"></a>メソッド replaceText

    public int replaceText([str findStr], [str replaceStr], [int start], [int end], [int flags])

#### <a name="parameters"></a>パラメーター

findStr  

<!-- -->

replaceStr  

<!-- -->

開始  

<!-- -->

終了  

<!-- -->

flags  

#### <a name="return-value"></a>戻り値

### <a name="method-searchafterinput"></a>メソッド searchAfterInput

    public int searchAfterInput([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-searchmode"></a>メソッド searchMode

    public int searchMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるセキュリティ キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。

### <a name="method-showcontextmenu"></a>メソッド showContextMenu

コントロールのショートカット メニューを表示します。

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a>パラメーター

menuHandle  
表示するメニューの ID。

#### <a name="return-value"></a>戻り値

通話が成功したかどうかを示す整数値。

### <a name="method-showlabel"></a>メソッド showLabel

    public boolean showLabel([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。

### <a name="method-sort"></a>メソッド sort

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a>パラメーター

sortDirection  

#### <a name="return-value"></a>戻り値

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tooltip"></a>メソッド toolTip

コントロールのツール ヒント テキストを取得します。

    public str toolTip()

#### <a name="return-value"></a>戻り値

コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。

#### <a name="remarks"></a>備考

メソッドを上書きして、toolTip メソッドに値を渡すことができます。

### <a name="method-top"></a>メソッド top

フォームのコントロールの垂直位置を取得または設定します。

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-topmode"></a>メソッド topMode

フォームのコントロールの垂直配置モードを設定します。

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直配置モード。

### <a name="method-topvalue"></a>メソッド topValue

フォームのコントロールの垂直位置を取得または設定します。

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

コントロールのユーザー データを取得または設定します。

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ。

### <a name="method-userdataitem"></a>メソッド userDataItem

コントロールのユーザー データ品目を取得または設定します。

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ アイテム。

### <a name="method-userdataitems"></a>メソッド userDataItems

コントロールのユーザー データ項目の数を取得または設定します。

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目の数を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ項目の数。

### <a name="method-userdisable"></a>メソッド userDisable

ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。

    public int userDisable([int value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。

### <a name="method-userfasttabsummary"></a>メソッド userFastTabSummary

    public int userFastTabSummary([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userheight"></a>メソッド userHeight

コントロールのカスタム ユーザーの高さを取得または設定します。

    public int userHeight([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザーの高さ (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのカスタム ユーザーの高さ。

### <a name="method-userhide"></a>メソッド userHide

コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。

    public int userHide([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

#### <a name="remarks"></a>備考

ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 このメソッドを使用すると、プログラムによって値を決定して設定できます。

### <a name="method-userorgcontainer"></a>メソッド userOrgContainer

コントロールの組織コンテナを取得または設定します。

    public int userOrgContainer([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織コンテナー (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織コンテナー。

### <a name="method-userorgsibling"></a>メソッド userOrgSibling

コントロールの組織兄弟を取得または設定します。

    public int userOrgSibling([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織の兄弟 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織の兄弟。

### <a name="method-userprompttext"></a>メソッド userPromptText

コントロールのユーザーラベル テキストを取得または設定します。

    public str userPromptText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー ラベルのテキスト (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザーラベル テキスト。

### <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

コントロールのユーザー セキュリティ レベルを取得または設定します。

    public int userSecurityLevel([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー セキュリティ レベル (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザー セキュリティ レベル。

### <a name="method-userskip"></a>メソッド userSkip

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。

    public int userSkip([int value])

#### <a name="parameters"></a>パラメーター

値  
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。

#### <a name="return-value"></a>戻り値

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

### <a name="method-userwidth"></a>メソッド userWidth

ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅として使用するピクセル数 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

### <a name="method-validate"></a>メソッド validate

    public boolean validate()

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの AutoMode 値を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode 値を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォームのコントロールの垂直スペーシング モードを設定します。

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング モード。

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの上下の間隔を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの可視化設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します。

| モード           | 幅計算                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| -1 正確       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します。

| モード         | 幅計算                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-lookup"></a>メソッド lookup

    public void lookup()

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-performformlookup"></a>メソッド performFormLookup

    public void performFormLookup(xFormRun form)

#### <a name="parameters"></a>パラメーター

フォーム  

### <a name="method-drop"></a>メソッド drop

ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

### <a name="method-onlookup"></a>メソッド OnLookup

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-scrollcursor"></a>メソッド scrollCursor

    public void scrollCursor()

### <a name="method-undo"></a>メソッド undo

    public void undo()

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-onmodified"></a>メソッド OnModified

    private void OnModified([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-dropex"></a>メソッド dropEx

ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

### <a name="method-setselection"></a>メソッド setSelection

    public void setSelection(int charIndexFrom, int charIndexTo)

#### <a name="parameters"></a>パラメーター

charIndexFrom  

<!-- -->

charIndexTo  

### <a name="method-pastetext"></a>メソッド pasteText

    public void pasteText(str pasteStr, [boolean InsertSel])

#### <a name="parameters"></a>パラメーター

pasteStr  

<!-- -->

InsertSel  

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

### <a name="method-enter"></a>メソッド enter

    public void enter()

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-performtypelookup"></a>メソッド performTypeLookup

    public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])

#### <a name="parameters"></a>パラメーター

userType  

<!-- -->

arrayIndex  

<!-- -->

会社  

### <a name="method-onvalidating"></a>メソッド OnValidating

    private void OnValidating([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-setcursorpos"></a>メソッド setCursorPos

    public void setCursorPos(int x, int y)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-linescroll"></a>メソッド lineScroll

    public void lineScroll(int dx, int dy)

#### <a name="parameters"></a>パラメーター

dx  

<!-- -->

dy  

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-performdblookup"></a>メソッド performDBLookup

    public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])

#### <a name="parameters"></a>パラメーター

fieldId  

<!-- -->

tableId  

<!-- -->

会社  

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-textchange"></a>メソッド textChange

    public void textChange()

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-onvalidated"></a>メソッド OnValidated

    private void OnValidated([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-jumpref"></a>メソッド jumpRef

    public void jumpRef()

## <a name="class-formrowdisplayoption"></a>クラス FormRowDisplayOption
    class FormRowDisplayOption extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                            | 説明 |
|-------------------------------------------------------------------|-------------|
| public int backColor(\[int color\])                               |             |
| public boolean fontBold(\[boolean bold\])                         |             |
| public boolean fontItalic(\[boolean italic\])                     |             |
| public boolean fontStrikethrough(\[boolean strikethrough\])       |             |
| public boolean fontUnderline(\[boolean underline\])               |             |
| public int textColor(\[int color\])                               |             |
| public void clear()                                               |             |
| public void clearTextColor()                                      |             |
| public void affectedElementsByField(\[FieldId fieldId\], VarArg ) |             |
| public void affectedElementsByControl(\[int controlId\], VarArg ) |             |
| public void clearBackColor()                                      |             |

### <a name="method-backcolor"></a>メソッド backColor

    public int backColor([int color])

#### <a name="parameters"></a>パラメーター

色  

#### <a name="return-value"></a>戻り値

### <a name="method-fontbold"></a>メソッド fontBold

    public boolean fontBold([boolean bold])

#### <a name="parameters"></a>パラメーター

太字  

#### <a name="return-value"></a>戻り値

### <a name="method-fontitalic"></a>メソッド fontItalic

    public boolean fontItalic([boolean italic])

#### <a name="parameters"></a>パラメーター

斜体  

#### <a name="return-value"></a>戻り値

### <a name="method-fontstrikethrough"></a>メソッド fontStrikethrough

    public boolean fontStrikethrough([boolean strikethrough])

#### <a name="parameters"></a>パラメーター

取り消し線  

#### <a name="return-value"></a>戻り値

### <a name="method-fontunderline"></a>メソッド fontUnderline

    public boolean fontUnderline([boolean underline])

#### <a name="parameters"></a>パラメーター

下線  

#### <a name="return-value"></a>戻り値

### <a name="method-textcolor"></a>メソッド textColor

    public int textColor([int color])

#### <a name="parameters"></a>パラメーター

色  

#### <a name="return-value"></a>戻り値

### <a name="method-clear"></a>メソッド clear

    public void clear()

### <a name="method-cleartextcolor"></a>メソッド clearTextColor

    public void clearTextColor()

### <a name="method-affectedelementsbyfield"></a>メソッド affectedElementsByField

    public void affectedElementsByField([FieldId fieldId], VarArg )

#### <a name="parameters"></a>パラメーター

fieldId  

<!-- -->



### <a name="method-affectedelementsbycontrol"></a>メソッド affectedElementsByControl

    public void affectedElementsByControl([int controlId], VarArg )

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->



### <a name="method-clearbackcolor"></a>メソッド clearBackColor

    public void clearBackColor()

## <a name="class-formsegment"></a>クラス FormSegment
    class FormSegment extends Object

FormSegment クラスは、SegmentedEntry コントロールでセグメントを表すために使用されます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                          | 説明                            |
|-----------------------------------------------------------------|----------------------------------------|
| public str text()                                               | セグメントの現在のテキストを取得します。  |
| public boolean allowEdit(\[boolean value\])                     |                                        |
| public str description(\[str description\])                     |                                        |
| public boolean enabled(\[boolean value\])                       |                                        |
| public int getIndex()                                           |                                        |
| public str name()                                               |                                        |
| public SegmentedEntryState state(\[SegmentedEntryState state\]) |                                        |
| public str value(\[str value\])                                 | セグメントの現在の値を取得します。 |

### <a name="method-text"></a>メソッド text

セグメントの現在のテキストを取得します。

    public str text()

#### <a name="return-value"></a>戻り値

セグメントの現在のテキスト。

#### <a name="remarks"></a>備考

このメソッドは、変更中であっても、セグメントのテキストの持続値を常に返します。 セグメントの保存された最後の値を取得するには、value メソッドを使用します。

### <a name="method-allowedit"></a>メソッド allowEdit

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-description"></a>メソッドの説明

    public str description([str description])

#### <a name="parameters"></a>パラメーター

description  

#### <a name="return-value"></a>戻り値

### <a name="method-enabled"></a>メソッド enabled

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-getindex"></a>メソッド getIndex

    public int getIndex()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name()

#### <a name="return-value"></a>戻り値

### <a name="method-state"></a>メソッド state

    public SegmentedEntryState state([SegmentedEntryState state])

#### <a name="parameters"></a>パラメーター

状態  

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

セグメントの現在の値を取得します。

    public str value([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

セグメントの現在の値。

#### <a name="remarks"></a>備考

このメソッドは、変更中であっても、セグメントの現在の持続値を常に返します。 コントロールの現在のテキストを取得するには、text メソッドを使用します。

## <a name="class-formsegmentedentrycontrol"></a>クラス FormSegmentedEntryControl
    class FormSegmentedEntryControl extends FormReferenceControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                                                       
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                                                          |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                                                |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                |
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                                                         |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public boolean hasChanged(\[boolean val\])                                                                  | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public boolean isContainer()                                                                                |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。                                                                   |
| public boolean isValid()                                                                                    |                                                                                                                                                                         |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                                                   |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                                                         |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                                                         |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                                                         |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                                                         |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                                                         |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                                                         |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                                                         |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                                                         |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                                                         |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                                                         |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                                                         |
| public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                        |                                                                                                                                                                         |
| public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                            |                                                                                                                                                                         |
| public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                              |                                                                                                                                                                         |
| public int labelPosition(\[int value\])                                                                     |                                                                                                                                                                         |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                                                         |
| public int labelWidth(int value, \[int mode\])                                                              |                                                                                                                                                                         |
| public int labelWidthMode(\[int value\])                                                                    |                                                                                                                                                                         |
| public int labelWidthValue(\[int value\])                                                                   |                                                                                                                                                                         |
| public boolean leave()                                                                                      |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMode(\[int value\])                                                                          | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                         | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public boolean mandatory(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean markAsUserAdd(\[boolean value\])                                                             | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public boolean modified()                                                                                   |                                                                                                                                                                         |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                             | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。                                                                                                       |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                   | ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。                                                                                                |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                     |                                                                                                                                                                         |
| public FormControl parentControl()                                                                          | コントロールの親コントロールを取得します。                                                                                                                           |
| public str previewPartRef(\[str value\])                                                                    |                                                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                                                         |
| public FieldId referenceField(\[FieldId value\])                                                            |                                                                                                                                                                         |
| public str replacementFieldGroup(\[str value\])                                                             |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[SortOrder sortDirection\])                                                                |                                                                                                                                                                         |
| public str toolTip()                                                                                        | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                     | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMode(\[int value\])                                                                           | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                          | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                              |                                                                                                                                                                         |
| public boolean SysObsoleteAttribute(container data)                                                         |                                                                                                                                                                         |
| public int userData(\[int value\])                                                                          | コントロールのユーザー データを取得または設定します。                                                                                                                             |
| public int userDataItem(\[int value\])                                                                      | コントロールのユーザー データ品目を取得または設定します。                                                                                                                        |
| public int userDataItems(\[int value\])                                                                     | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                             |
| public int userDisable(\[int value\])                                                                       | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                                     |
| public int userHeight(\[int value\])                                                                        | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                                                    |
| public int userHide(\[int value\])                                                                          | コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。                                                                                      |
| public int userOrgContainer(\[int value\])                                                                  | コントロールの組織コンテナを取得または設定します。                                                                                                                |
| public int userOrgSibling(\[int value\])                                                                    | コントロールの組織兄弟を取得または設定します。                                                                                                                  |
| public str userPromptText(\[str value\])                                                                    | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                                       |
| public int userSecurityLevel(\[int value\])                                                                 | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                   |
| public int userSkip(\[int value\])                                                                          | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。                    |
| public int userWidth(\[int value\])                                                                         | ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。                                                                                           |
| public boolean validate()                                                                                   |                                                                                                                                                                         |
| public Int64 value(\[Int64 value\])                                                                         |                                                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void undo()                                                                                          |                                                                                                                                                                         |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void jumpRef()                                                                                       |                                                                                                                                                                         |
| public void enter()                                                                                         |                                                                                                                                                                         |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void lookup()                                                                                        |                                                                                                                                                                         |
| private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void filter(\[str filterStr\])                                                                       |                                                                                                                                                                         |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])                               |                                                                                                                                                                         |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])                                   |                                                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  
プロパティの新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  
allowEdit プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

    public boolean allowSysSetup()

#### <a name="return-value"></a>戻り値

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  
プロパティの新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。

    public int beginDrag(int x, int y)

#### <a name="parameters"></a>パラメーター

x  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

<!-- -->

y  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 先頭値 | 説明 |
|-------|-------------|
| 0     | 自動        |
| 1     | 3D          |
| 2     | 単一明細行 |
| 3     | 均一        |
| 4     | None        |

### <a name="method-calccontrolsize"></a>メソッド calcControlSize

コントロールのサイズを取得します。

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a>パラメーター

chars  
高さを決定するために使用する行数。

<!-- -->

明細行  
高さを決定するために使用する行数。

#### <a name="return-value"></a>戻り値

幅と高さを保持するコンテナー。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 金額 | スタイル                        |
|-------|------------------------------|
| 0     | 既定                      |
| 1     | Microsoft Windows パレット。 |
| 2     | 真の配色        |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。

#### <a name="remarks"></a>備考

返されるリストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する国/地域コードを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの国/地域コードのコンマ区切りのリスト。

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  
ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。

#### <a name="remarks"></a>備考

このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。 参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-displaytarget"></a>メソッド displayTarget

Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

Finance and Operations、クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  
ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

#### <a name="remarks"></a>備考

dragLeave メソッド、dragOver メソッド、および dragOverEx メソッドを使用して、ビヘイビアーを指定します。

### <a name="method-dragover"></a>メソッド dragOver

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragoverex"></a>メソッド dragOverEx

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragtext"></a>メソッド dragText

フォーム コントロールをドラッグしたときに表示されるテキストを取得します。

    public str dragText()

#### <a name="return-value"></a>戻り値

コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが有効かどうかを指定するブール値; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-haschanged"></a>メソッド hasChanged

コントロールの内容が変更されたかどうかを示す値を設定するか返します。

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  
コントロールの hasChanged 値として割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの内容が変更された場合は true。それ以外の場合は、false。

### <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

    public boolean hasUserSetting()

#### <a name="return-value"></a>戻り値

コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
高さの計算方法を示す整数値。オプション。

<!-- -->

モード  
高さの計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します。

| モード            | 高さの計算                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| -1 正確        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの高さの計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します。

| モード          | 高さの計算                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| 正確         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  
高さをピクセル単位で指定する整数。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを取得します。

    public str helpField()

#### <a name="return-value"></a>戻り値

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

#### <a name="remarks"></a>備考

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのヘルプ テキストとして割り当てる値。

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの HierarchyParent プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールの HierarchyParent プロパティ値。

### <a name="method-hwnd"></a>メソッド hWnd

コントロールの Windows ハンドルを取得します。

    public int hWnd()

#### <a name="return-value"></a>戻り値

ハンドラーコントロールのハンドルです。

#### <a name="remarks"></a>備考

この処理は、Windows API で使用できます。

### <a name="method-iscontainer"></a>メソッド isContainer

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を取得します。

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

コントロールが表示される場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

### <a name="method-isrestricted"></a>メソッド isRestricted

コントロールが制限されるかどうかを示す値を取得します。

    public boolean isRestricted()

#### <a name="return-value"></a>戻り値

コントロールが制限される場合は true。それ以外の場合は false。

### <a name="method-isusersetupenabled"></a>メソッド isUserSetupEnabled

コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a>パラメーター

neededSetupRights  
コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。

#### <a name="return-value"></a>戻り値

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

### <a name="method-isvalid"></a>メソッド isValid

    public boolean isValid()

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-labelalignment"></a>メソッド labelAlignment

    public int labelAlignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelbold"></a>メソッド labelBold

    public int labelBold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

    public int labelCharacterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfont"></a>メソッド labelFont

    public str labelFont([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfontsize"></a>メソッド labelFontSize

    public int labelFontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelforegroundcolor"></a>メソッド labelForegroundColor

    public int labelForegroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelguide"></a>メソッド labelGuide

    public int labelGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheight"></a>メソッド labelHeight

    public int labelHeight(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightmode"></a>メソッド labelHeightMode

    public int labelHeightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightvalue"></a>メソッド labelHeightValue

    public int labelHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelitalic"></a>メソッド labelItalic

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmousedblclick"></a>メソッド labelMouseDblClick

    public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmousedown"></a>メソッド labelMouseDown

    public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmouseup"></a>メソッド labelMouseUp

    public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelposition"></a>メソッド labelPosition

    public int labelPosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelunderline"></a>メソッド labelUnderline

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidth"></a>メソッド labelWidth

    public int labelWidth(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthmode"></a>メソッド labelWidthMode

    public int labelWidthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthvalue"></a>メソッド labelWidthValue

    public int labelWidthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leave"></a>メソッド leave

    public boolean leave()

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

フォームのコントロールの水平位置を取得または設定します。

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-leftmode"></a>メソッド leftMode

フォームのコントロールの水平配置モードを設定します。

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの水平配置モード。

### <a name="method-leftvalue"></a>メソッド leftValue

フォームのコントロールの水平位置を取得または設定します。

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-mandatory"></a>メソッド mandatory

    public boolean mandatory([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-markasuseradd"></a>メソッド markAsUserAdd

ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。

### <a name="method-modified"></a>メソッド modified

    public boolean modified()

#### <a name="return-value"></a>戻り値

### <a name="method-mousedblclick"></a>メソッド mouseDblClick

コントロールがユーザーにダブルクリックされると呼び出されます。

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-mousemove"></a>メソッド mouseMove

ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parentcontrol"></a>メソッド parentControl

コントロールの親コントロールを取得します。

    public FormControl parentControl()

#### <a name="return-value"></a>戻り値

コントロールの親コントロール。

### <a name="method-previewpartref"></a>メソッド previewPartRef

    public str previewPartRef([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-promptrect"></a>メソッド promptrect

    public int promptrect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-referencefield"></a>メソッド referenceField

    public FieldId referenceField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-replacementfieldgroup"></a>メソッド replacementFieldGroup

    public str replacementFieldGroup([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるセキュリティ キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。

### <a name="method-showcontextmenu"></a>メソッド showContextMenu

コントロールのショートカット メニューを表示します。

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a>パラメーター

menuHandle  
表示するメニューの ID。

#### <a name="return-value"></a>戻り値

通話が成功したかどうかを示す整数値。

### <a name="method-showlabel"></a>メソッド showLabel

    public boolean showLabel([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。

### <a name="method-sort"></a>メソッド sort

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a>パラメーター

sortDirection  

#### <a name="return-value"></a>戻り値

### <a name="method-tooltip"></a>メソッド toolTip

コントロールのツール ヒント テキストを取得します。

    public str toolTip()

#### <a name="return-value"></a>戻り値

コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。

#### <a name="remarks"></a>備考

メソッドを上書きして、toolTip メソッドに値を渡すことができます。

### <a name="method-top"></a>メソッド top

フォームのコントロールの垂直位置を取得または設定します。

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-topmode"></a>メソッド topMode

フォームのコントロールの垂直配置モードを設定します。

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直配置モード。

### <a name="method-topvalue"></a>メソッド topValue

フォームのコントロールの垂直位置を取得または設定します。

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

コントロールのユーザー データを取得または設定します。

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ。

### <a name="method-userdataitem"></a>メソッド userDataItem

コントロールのユーザー データ品目を取得または設定します。

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ アイテム。

### <a name="method-userdataitems"></a>メソッド userDataItems

コントロールのユーザー データ項目の数を取得または設定します。

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目の数を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ項目の数。

### <a name="method-userdisable"></a>メソッド userDisable

ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。

    public int userDisable([int value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。

### <a name="method-userheight"></a>メソッド userHeight

コントロールのカスタム ユーザーの高さを取得または設定します。

    public int userHeight([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザーの高さ (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのカスタム ユーザーの高さ。

### <a name="method-userhide"></a>メソッド userHide

コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。

    public int userHide([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

#### <a name="remarks"></a>備考

ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 このメソッドを使用すると、プログラムによって値を決定して設定できます。

### <a name="method-userorgcontainer"></a>メソッド userOrgContainer

コントロールの組織コンテナを取得または設定します。

    public int userOrgContainer([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織コンテナー (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織コンテナー。

### <a name="method-userorgsibling"></a>メソッド userOrgSibling

コントロールの組織兄弟を取得または設定します。

    public int userOrgSibling([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織の兄弟 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織の兄弟。

### <a name="method-userprompttext"></a>メソッド userPromptText

コントロールのユーザーラベル テキストを取得または設定します。

    public str userPromptText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー ラベルのテキスト (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザーラベル テキスト。

### <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

コントロールのユーザー セキュリティ レベルを取得または設定します。

    public int userSecurityLevel([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー セキュリティ レベル (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザー セキュリティ レベル。

### <a name="method-userskip"></a>メソッド userSkip

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。

    public int userSkip([int value])

#### <a name="parameters"></a>パラメーター

値  
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。

#### <a name="return-value"></a>戻り値

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

### <a name="method-userwidth"></a>メソッド userWidth

ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅として使用するピクセル数 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

### <a name="method-validate"></a>メソッド validate

    public boolean validate()

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

    public Int64 value([Int64 value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの AutoMode 値を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode 値を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォームのコントロールの垂直スペーシング モードを設定します。

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング モード。

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの上下の間隔を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの可視化設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
幅の計算方法を示す整数値。オプション。

<!-- -->

モード  
幅の計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します。

| モード           | 幅計算                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| -1 正確       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロール幅の計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します。

| モード         | 幅計算                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  
幅をピクセル単位で指定する整数。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-undo"></a>メソッド undo

    public void undo()

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-onvalidated"></a>メソッド OnValidated

    private void OnValidated([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-jumpref"></a>メソッド jumpRef

    public void jumpRef()

### <a name="method-enter"></a>メソッド enter

    public void enter()

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-drop"></a>メソッド drop

ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-lookup"></a>メソッド lookup

    public void lookup()

### <a name="method-onmodified"></a>メソッド OnModified

    private void OnModified([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-dropex"></a>メソッド dropEx

ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

### <a name="method-onvalidating"></a>メソッド OnValidating

    private void OnValidating([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-onlookup"></a>メソッド OnLookup

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

## <a name="class-formspreloadingmanager"></a>クラス FormsPreloadingManager
    class FormsPreloadingManager extends Object

FormsPreloadingManager クラスは、ワークスペースの関連付けとリソース負荷管理などのフォームのプリロードを管理します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>方法

| 方法                                              | 説明                                                                                  |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------|
| ::private static FormsPreloadingManager construct() |                                                                                              |
| public void workspaceActivated()                    | プリロード ワークスペース アフィニティを最後にアクティブ化されたワークスペースに設定します。                      |
| private void new()                                  | FormsPreloadingManager クラスの新しいインスタンスを初期化します。                              |
| public void updateState()                           | 読み込みのためにフォームを照会し、リソース使用率の負荷を処理し、その他の内部の状態を更新します。 |

### <a name="method-construct"></a>メソッド construct

    private static FormsPreloadingManager construct()

#### <a name="return-value"></a>戻り値

### <a name="method-workspaceactivated"></a>メソッド workspaceActivated

プリロード ワークスペース アフィニティを最後にアクティブ化されたワークスペースに設定します。

    public void workspaceActivated()

#### <a name="remarks"></a>備考

このメソッドは、通常、ワークスペースが有効にされた後にタイマーで呼び出されます。 ワークスペースを変更に対してすぐに親和させるには、このメソッドを直接呼び出します。

### <a name="method-new"></a>メソッド new

FormsPreloadingManager クラスの新しいインスタンスを初期化します。

    private void new()

### <a name="method-updatestate"></a>メソッド updateState

読み込みのためにフォームを照会し、リソース使用率の負荷を処理し、その他の内部の状態を更新します。

    public void updateState()

#### <a name="remarks"></a>備考

このメソッドは、通常アイドル状態のときタイマーで呼び出されます。 実行時間の長い X++ コードが実行されている場合など、非アイドル時に状態を強制的に更新するには、このメソッドを直接呼び出します。

## <a name="class-formstatictextcontrol"></a>クラス FormStaticTextControl
    class FormStaticTextControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public int alignment(\[int value\])                                                                         |                                                                                                                                                                         |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを示します。                                                                                                            |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                                             |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                                                         |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用するデータ ソースを取得または設定します。                                                                                                          |
| public int displayHeight(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                                                         |
| public AutoMode displayHeightMode(\[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public int displayHeightValue(\[int value\])                                                                |                                                                                                                                                                         |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                                                         |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。                                                                                        |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public boolean hasChanged(\[boolean val\])                                                                  | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public boolean isContainer()                                                                                |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。                                                                   |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMode(\[int value\])                                                                          | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                         | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public boolean markAsUserAdd(\[boolean value\])                                                             | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                             | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。                                                                                                       |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                   | ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。                                                                                                |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                     |                                                                                                                                                                         |
| public FormControl parentControl()                                                                          | コントロールの親コントロールを取得します。                                                                                                                           |
| public str previewPartRef(\[str value\])                                                                    |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[SortOrder sortDirection\])                                                                |                                                                                                                                                                         |
| public int style(\[int value\])                                                                             |                                                                                                                                                                         |
| public str text(\[str value\])                                                                              |                                                                                                                                                                         |
| public str toolTip()                                                                                        | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                     | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMode(\[int value\])                                                                           | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                          | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                              |                                                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean SysObsoleteAttribute(container data)                                                         |                                                                                                                                                                         |
| public int userData(\[int value\])                                                                          | コントロールのユーザー データを取得または設定します。                                                                                                                             |
| public int userDataItem(\[int value\])                                                                      | コントロールのユーザー データ品目を取得または設定します。                                                                                                                        |
| public int userDataItems(\[int value\])                                                                     | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                             |
| public int userDisable(\[int value\])                                                                       | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                                     |
| public int userHeight(\[int value\])                                                                        | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                                                    |
| public int userHide(\[int value\])                                                                          | コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。                                                                                      |
| public int userOrgContainer(\[int value\])                                                                  | コントロールの組織コンテナを取得または設定します。                                                                                                                |
| public int userOrgSibling(\[int value\])                                                                    | コントロールの組織兄弟を取得または設定します。                                                                                                                  |
| public str userPromptText(\[str value\])                                                                    | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                                       |
| public int userSecurityLevel(\[int value\])                                                                 | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                   |
| public int userSkip(\[int value\])                                                                          | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。                    |
| public int userWidth(\[int value\])                                                                         | ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。                                                                                           |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void filter(\[str filterStr\])                                                                       |                                                                                                                                                                         |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void jumpRef()                                                                                       |                                                                                                                                                                         |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-alignment"></a>メソッド alignment

    public int alignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

    public boolean allowSysSetup()

#### <a name="return-value"></a>戻り値

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを示します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。

    public int beginDrag(int x, int y)

#### <a name="parameters"></a>パラメーター

x  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

<!-- -->

y  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-cachedatamethod"></a>メソッド cacheDataMethod

    public int cacheDataMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-calccontrolsize"></a>メソッド calcControlSize

コントロールのサイズを取得します。

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a>パラメーター

chars  
高さを決定するために使用する行数。

<!-- -->

明細行  
高さを決定するために使用する行数。

#### <a name="return-value"></a>戻り値

幅と高さを保持するコンテナー。

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 先頭値 | 説明          |
|-------|----------------------|
| 0     | ANSI\_CHARSET        |
| 1     | DEFAULT\_CHARSET     |
| 2     | SYMBOL\_CHARSET      |
| 77    | MAC\_CHARSET         |
| 128   | SHIFTJIS\_CHARSET    |
| 129   | HANGUL\_CHARSET      |
| 134   | GB2312\_CHARSET      |
| 136   | CHINESEBIG5\_CHARSET |
| 161   | GREEK\_CHARSET       |
| 162   | TURKISH\_CHARSET     |
| 163   | VIETNAMESE\_CHARSET  |
| 186   | BALTIC\_CHARSET      |
| 204   | RUSSIAN\_CHARSET     |
| 238   | EASTEUROPE\_CHARSET  |
| 255   | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 金額 | 説明    |
|-------|----------------|
| 130   | JOHAB\_CHARSET |

次のテーブルの値は、中東言語語版 Windows の値です。

| 先頭値 | 説明     |
|-------|-----------------|
| 177   | HEBREW\_CHARSET |
| 178   | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Windows の値です。

| 先頭値 | 説明   |
|-------|---------------|
| 222   | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 先頭値 | スタイル                 |
|-------|-----------------------|
| 0     | 既定               |
| 1     | Windows パレット   |
| 2     | 真の配色 |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。

#### <a name="remarks"></a>備考

返されるリストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する国/地域コードを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの国/地域コードのコンマ区切りのリスト。

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafield"></a>メソッド dataField

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datamethod"></a>メソッド dataMethod

    public str dataMethod([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  
ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。

#### <a name="remarks"></a>備考

このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。 参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用するデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-displayheight"></a>メソッド displayHeight

    public int displayHeight([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightmode"></a>メソッド displayHeightMode

    public AutoMode displayHeightMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightvalue"></a>メソッド displayHeightValue

    public int displayHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylength"></a>メソッド displayLength

    public int displayLength([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthmode"></a>メソッド displayLengthMode

    public AutoMode displayLengthMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthvalue"></a>メソッド displayLengthValue

    public int displayLengthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

Finance and Operations、クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は true。それ以外の場合は、false。

### <a name="method-dragover"></a>メソッド dragOver

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragoverex"></a>メソッド dragOverEx

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragtext"></a>メソッド dragText

フォーム コントロールをドラッグしたときに表示されるテキストを取得します。

    public str dragText()

#### <a name="return-value"></a>戻り値

コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-haschanged"></a>メソッド hasChanged

コントロールの内容が変更されたかどうかを示す値を設定するか返します。

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  
コントロールの hasChanged 値として割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの内容が変更された場合は true。それ以外の場合は、false。

### <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

    public boolean hasUserSetting()

#### <a name="return-value"></a>戻り値

コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します。

| モード            | 高さの計算                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| -1 正確        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します。

| モード          | 高さの計算                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| 正確         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを取得します。

    public str helpField()

#### <a name="return-value"></a>戻り値

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

#### <a name="remarks"></a>備考

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの HierarchyParent プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールの HierarchyParent プロパティ値。

### <a name="method-hwnd"></a>メソッド hWnd

コントロールの Windows ハンドルを取得します。

    public int hWnd()

#### <a name="return-value"></a>戻り値

ハンドラーコントロールのハンドルです。

#### <a name="remarks"></a>備考

この処理は、Windows API で使用できます。

### <a name="method-iscontainer"></a>メソッド isContainer

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を取得します。

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

コントロールが表示される場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

### <a name="method-isrestricted"></a>メソッド isRestricted

コントロールが制限されるかどうかを示す値を取得します。

    public boolean isRestricted()

#### <a name="return-value"></a>戻り値

コントロールが制限される場合は true。それ以外の場合は false。

### <a name="method-isusersetupenabled"></a>メソッド isUserSetupEnabled

コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a>パラメーター

neededSetupRights  
コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。

#### <a name="return-value"></a>戻り値

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

フォームのコントロールの水平位置を取得または設定します。

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-leftmode"></a>メソッド leftMode

フォームのコントロールの水平配置モードを設定します。

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの水平配置モード。

### <a name="method-leftvalue"></a>メソッド leftValue

フォームのコントロールの水平位置を取得または設定します。

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-markasuseradd"></a>メソッド markAsUserAdd

ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。

### <a name="method-mousedblclick"></a>メソッド mouseDblClick

コントロールがユーザーにダブルクリックされると呼び出されます。

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-mousemove"></a>メソッド mouseMove

ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parentcontrol"></a>メソッド parentControl

コントロールの親コントロールを取得します。

    public FormControl parentControl()

#### <a name="return-value"></a>戻り値

コントロールの親コントロール。

### <a name="method-previewpartref"></a>メソッド previewPartRef

    public str previewPartRef([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるセキュリティ キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。

### <a name="method-showcontextmenu"></a>メソッド showContextMenu

コントロールのショートカット メニューを表示します。

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a>パラメーター

menuHandle  
表示するメニューの ID。

#### <a name="return-value"></a>戻り値

通話が成功したかどうかを示す整数値。

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。

### <a name="method-sort"></a>メソッド sort

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a>パラメーター

sortDirection  

#### <a name="return-value"></a>戻り値

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tooltip"></a>メソッド toolTip

コントロールのツール ヒント テキストを取得します。

    public str toolTip()

#### <a name="return-value"></a>戻り値

コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。

#### <a name="remarks"></a>備考

メソッドを上書きして、toolTip メソッドに値を渡すことができます。

### <a name="method-top"></a>メソッド top

フォームのコントロールの垂直位置を取得または設定します。

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-topmode"></a>メソッド topMode

フォームのコントロールの垂直配置モードを設定します。

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直配置モード。

### <a name="method-topvalue"></a>メソッド topValue

フォームのコントロールの垂直位置を取得または設定します。

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

コントロールのユーザー データを取得または設定します。

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ。

### <a name="method-userdataitem"></a>メソッド userDataItem

コントロールのユーザー データ品目を取得または設定します。

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ アイテム。

### <a name="method-userdataitems"></a>メソッド userDataItems

コントロールのユーザー データ項目の数を取得または設定します。

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目の数を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ項目の数。

### <a name="method-userdisable"></a>メソッド userDisable

ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。

    public int userDisable([int value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。

### <a name="method-userheight"></a>メソッド userHeight

コントロールのカスタム ユーザーの高さを取得または設定します。

    public int userHeight([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザーの高さ (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのカスタム ユーザーの高さ。

### <a name="method-userhide"></a>メソッド userHide

コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。

    public int userHide([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

#### <a name="remarks"></a>備考

ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 このメソッドを使用すると、プログラムによって値を決定して設定できます。

### <a name="method-userorgcontainer"></a>メソッド userOrgContainer

コントロールの組織コンテナを取得または設定します。

    public int userOrgContainer([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織コンテナー (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織コンテナー。

### <a name="method-userorgsibling"></a>メソッド userOrgSibling

コントロールの組織兄弟を取得または設定します。

    public int userOrgSibling([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織の兄弟 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織の兄弟。

### <a name="method-userprompttext"></a>メソッド userPromptText

コントロールのユーザーラベル テキストを取得または設定します。

    public str userPromptText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー ラベルのテキスト (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザーラベル テキスト。

### <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

コントロールのユーザー セキュリティ レベルを取得または設定します。

    public int userSecurityLevel([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー セキュリティ レベル (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザー セキュリティ レベル。

### <a name="method-userskip"></a>メソッド userSkip

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。

    public int userSkip([int value])

#### <a name="parameters"></a>パラメーター

値  
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。

#### <a name="return-value"></a>戻り値

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

### <a name="method-userwidth"></a>メソッド userWidth

ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅として使用するピクセル数 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの AutoMode 値を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode 値を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォームのコントロールの垂直スペーシング モードを設定します。

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング モード。

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの上下の間隔を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの可視化設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します。

| モード           | 幅計算                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| -1 正確       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します。

| モード         | 幅計算                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-jumpref"></a>メソッド jumpRef

    public void jumpRef()

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-dropex"></a>メソッド dropEx

ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-drop"></a>メソッド drop

ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

## <a name="class-formstringcontrol"></a>クラス FormStringControl
    class FormStringControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを示します。                                                                                                                                 |
| public int alignment(\[int value\])                                                                         |                                                                                                                                                                         |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを示します。                                                                                                      |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを示します。                                                                       |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを示します。                                                                                                            |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                                             |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                                                |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                                                         |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public int changeCase(\[int value\])                                                                        |                                                                                                                                                                         |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                                                             |
| public int charFromPos(int x, int y)                                                                        |                                                                                                                                                                         |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                                                         |
| public int dataFieldArrayIndex()                                                                            |                                                                                                                                                                         |
| public FieldName dataFieldName()                                                                            |                                                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                |
| public int direction(\[int value\])                                                                         |                                                                                                                                                                         |
| public int displayHeight(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                                                         |
| public AutoMode displayHeightMode(\[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public int displayHeightValue(\[int value\])                                                                |                                                                                                                                                                         |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                                                         |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。                                                                                        |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを示します。                                                                                                                      |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                                                         |
| public int fastTabSummary(\[int value\])                                                                    |                                                                                                                                                                         |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public container getCursorPos()                                                                             |                                                                                                                                                                         |
| public int getFirstVisibleLine()                                                                            |                                                                                                                                                                         |
| public str getLine(int lineNo)                                                                              |                                                                                                                                                                         |
| public int getLineCount()                                                                                   |                                                                                                                                                                         |
| public container getSelection()                                                                             |                                                                                                                                                                         |
| public boolean hasChanged(\[boolean val\])                                                                  | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public int iMEMode(\[int value\])                                                                           |                                                                                                                                                                         |
| public boolean isContainer()                                                                                |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。                                                                   |
| public boolean isValid()                                                                                    |                                                                                                                                                                         |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                                                         |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                                                   |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                                                         |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                                                         |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                                                         |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                                                         |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                                                         |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                                                         |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                                                         |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                                                         |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                                                         |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                                                         |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                                                         |
| public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                        |                                                                                                                                                                         |
| public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                            |                                                                                                                                                                         |
| public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                              |                                                                                                                                                                         |
| public int labelPosition(\[int value\])                                                                     |                                                                                                                                                                         |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                                                         |
| public int labelWidth(int value, \[int mode\])                                                              |                                                                                                                                                                         |
| public int labelWidthMode(\[int value\])                                                                    |                                                                                                                                                                         |
| public int labelWidthValue(\[int value\])                                                                   |                                                                                                                                                                         |
| public boolean leave()                                                                                      |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMode(\[int value\])                                                                          | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                         | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int limitText(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                                                         |
| public AutoMode limitTextMode(\[AutoMode mode\])                                                            |                                                                                                                                                                         |
| public int limitTextValue(\[int value\])                                                                    |                                                                                                                                                                         |
| public int lineFromChar(int charIndex)                                                                      |                                                                                                                                                                         |
| public int lineIndex(int lineNo)                                                                            |                                                                                                                                                                         |
| public int lineLength(int lineNo)                                                                           |                                                                                                                                                                         |
| public int lookupButton(\[int value\])                                                                      |                                                                                                                                                                         |
| public boolean lookupOnly(\[boolean value\])                                                                |                                                                                                                                                                         |
| public boolean mandatory(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean markAsUserAdd(\[boolean value\])                                                             | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public boolean modified()                                                                                   |                                                                                                                                                                         |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                             | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。                                                                                                       |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                   | ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。                                                                                                |
| public boolean multiLine(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                     |                                                                                                                                                                         |
| public FormControl parentControl()                                                                          | コントロールの親コントロールを取得します。                                                                                                                           |
| public boolean passwordStyle(\[boolean value\])                                                             |                                                                                                                                                                         |
| public container posFromChar(int charIndex)                                                                 |                                                                                                                                                                         |
| public FieldId presenceDataField(\[FieldId value\])                                                         |                                                                                                                                                                         |
| public int presenceDataSource(\[AnyType value\])                                                            |                                                                                                                                                                         |
| public int presenceIndicatorAllowed(\[int value\])                                                          |                                                                                                                                                                         |
| public str previewPartRef(\[str value\])                                                                    |                                                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                                                         |
| public boolean replaceOnLookup(\[boolean value\])                                                           |                                                                                                                                                                         |
| public str resolveAmbiguousReference()                                                                      |                                                                                                                                                                         |
| public FieldBinding disambiguationLookupTarget()                                                            |                                                                                                                                                                         |
| public str lookupDisambiguateReference(FieldBinding fieldBinding)                                           |                                                                                                                                                                         |
| public int searchAfterInput(\[int value\])                                                                  |                                                                                                                                                                         |
| public int searchMode(\[int value\])                                                                        |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[SortOrder sortDirection\])                                                                |                                                                                                                                                                         |
| public int style(\[int value\])                                                                             |                                                                                                                                                                         |
| public str text(\[str value\])                                                                              |                                                                                                                                                                         |
| public str toolTip()                                                                                        | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                     | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMode(\[int value\])                                                                           | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                          | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                              |                                                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean SysObsoleteAttribute(container data)                                                         |                                                                                                                                                                         |
| public int userData(\[int value\])                                                                          | コントロールのユーザー データを取得または設定します。                                                                                                                             |
| public int userDataItem(\[int value\])                                                                      | コントロールのユーザー データ品目を取得または設定します。                                                                                                                        |
| public int userDataItems(\[int value\])                                                                     | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                             |
| public int userDisable(\[int value\])                                                                       | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                                     |
| public int userFastTabSummary(\[int value\])                                                                |                                                                                                                                                                         |
| public int userHeight(\[int value\])                                                                        | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                                                    |
| public int userHide(\[int value\])                                                                          | コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。                                                                                      |
| public int userOrgContainer(\[int value\])                                                                  | コントロールの組織コンテナを取得または設定します。                                                                                                                |
| public int userOrgSibling(\[int value\])                                                                    | コントロールの組織兄弟を取得または設定します。                                                                                                                  |
| public str userPromptText(\[str value\])                                                                    | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                                       |
| public int userSecurityLevel(\[int value\])                                                                 | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                   |
| public int userSkip(\[int value\])                                                                          | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。                    |
| public int userWidth(\[int value\])                                                                         | ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。                                                                                           |
| public boolean validate()                                                                                   |                                                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void presenceRefresh()                                                                               |                                                                                                                                                                         |
| private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])                                   |                                                                                                                                                                         |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])         |                                                                                                                                                                         |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void undo()                                                                                          |                                                                                                                                                                         |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void setSelection(int charIndexFrom, int charIndexTo)                                                |                                                                                                                                                                         |
| public void scrollCursor()                                                                                  |                                                                                                                                                                         |
| public void enter()                                                                                         |                                                                                                                                                                         |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])       |                                                                                                                                                                         |
| public void filter(\[str filterStr\])                                                                       |                                                                                                                                                                         |
| private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])                               |                                                                                                                                                                         |
| public void setCursorPos(int x, int y)                                                                      |                                                                                                                                                                         |
| public void performFormLookup(xFormRun form)                                                                |                                                                                                                                                                         |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void lineScroll(int dx, int dy)                                                                      |                                                                                                                                                                         |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void textChange()                                                                                    |                                                                                                                                                                         |
| public void jumpRef()                                                                                       |                                                                                                                                                                         |
| public void lookup()                                                                                        |                                                                                                                                                                         |
| public void pasteText(str pasteStr, \[boolean InsertSel\])                                                  |                                                                                                                                                                         |
| private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを示します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-alignment"></a>メソッド alignment

    public int alignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを示します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

    public boolean allowSysSetup()

#### <a name="return-value"></a>戻り値

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

### <a name="method-arrayindex"></a>メソッド arrayIndex

    public int arrayIndex([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを示します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを示します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。

    public int beginDrag(int x, int y)

#### <a name="parameters"></a>パラメーター

x  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

<!-- -->

y  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 先頭値 | 説明 |
|-------|-------------|
| 0     | 自動        |
| 1     | 3D          |
| 2     | 単一明細行 |
| 3     | 均一        |
| 4     | None        |

### <a name="method-cachedatamethod"></a>メソッド cacheDataMethod

    public int cacheDataMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-calccontrolsize"></a>メソッド calcControlSize

コントロールのサイズを取得します。

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a>パラメーター

chars  
高さを決定するために使用する行数。

<!-- -->

明細行  
高さを決定するために使用する行数。

#### <a name="return-value"></a>戻り値

幅と高さを保持するコンテナー。

### <a name="method-changecase"></a>メソッド changeCase

    public int changeCase([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 先頭値 | 説明          |
|-------|----------------------|
| 0     | ANSI\_CHARSET        |
| 1     | DEFAULT\_CHARSET     |
| 2     | SYMBOL\_CHARSET      |
| 77    | MAC\_CHARSET         |
| 128   | SHIFTJIS\_CHARSET    |
| 129   | HANGUL\_CHARSET      |
| 134   | GB2312\_CHARSET      |
| 136   | CHINESEBIG5\_CHARSET |
| 161   | GREEK\_CHARSET       |
| 162   | TURKISH\_CHARSET     |
| 163   | VIETNAMESE\_CHARSET  |
| 186   | BALTIC\_CHARSET      |
| 204   | RUSSIAN\_CHARSET     |
| 238   | EASTEUROPE\_CHARSET  |
| 255   | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 金額 | 説明    |
|-------|----------------|
| 130   | JOHAB\_CHARSET |

次のテーブルの値は、中東言語語版 Windows の値です。

| 先頭値 | 説明     |
|-------|-----------------|
| 177   | HEBREW\_CHARSET |
| 178   | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Windows の値です。

| 先頭値 | 説明   |
|-------|---------------|
| 222   | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-charfrompos"></a>メソッド charFromPos

    public int charFromPos(int x, int y)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

#### <a name="return-value"></a>戻り値

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 先頭値 | スタイル                 |
|-------|-----------------------|
| 0     | 既定               |
| 1     | Windows パレット   |
| 2     | 真の配色 |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。

#### <a name="remarks"></a>備考

返されるリストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する国/地域コードを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの国/地域コードのコンマ区切りのリスト。

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafield"></a>メソッド dataField

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafieldarrayindex"></a>メソッド dataFieldArrayIndex

    public int dataFieldArrayIndex()

#### <a name="return-value"></a>戻り値

### <a name="method-datafieldname"></a>メソッド dataFieldName

    public FieldName dataFieldName()

#### <a name="return-value"></a>戻り値

### <a name="method-datamethod"></a>メソッド dataMethod

    public str dataMethod([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  
ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。

#### <a name="remarks"></a>備考

このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。 参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-direction"></a>メソッド direction

    public int direction([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheight"></a>メソッド displayHeight

    public int displayHeight([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightmode"></a>メソッド displayHeightMode

    public AutoMode displayHeightMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightvalue"></a>メソッド displayHeightValue

    public int displayHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylength"></a>メソッド displayLength

    public int displayLength([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthmode"></a>メソッド displayLengthMode

    public AutoMode displayLengthMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthvalue"></a>メソッド displayLengthValue

    public int displayLengthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

Finance and Operations、クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-dragover"></a>メソッド dragOver

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragoverex"></a>メソッド dragOverEx

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragtext"></a>メソッド dragText

フォーム コントロールをドラッグしたときに表示されるテキストを取得します。

    public str dragText()

#### <a name="return-value"></a>戻り値

コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを示します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-fasttabsummary"></a>メソッド fastTabSummary

    public int fastTabSummary([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-getcursorpos"></a>メソッド getCursorPos

    public container getCursorPos()

#### <a name="return-value"></a>戻り値

### <a name="method-getfirstvisibleline"></a>メソッド getFirstVisibleLine

    public int getFirstVisibleLine()

#### <a name="return-value"></a>戻り値

### <a name="method-getline"></a>メソッド getLine

    public str getLine(int lineNo)

#### <a name="parameters"></a>パラメーター

lineNo  

#### <a name="return-value"></a>戻り値

### <a name="method-getlinecount"></a>メソッド getLineCount

    public int getLineCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getselection"></a>メソッド getSelection

    public container getSelection()

#### <a name="return-value"></a>戻り値

### <a name="method-haschanged"></a>メソッド hasChanged

コントロールの内容が変更されたかどうかを示す値を設定するか返します。

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  
コントロールの hasChanged 値として割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの内容が変更された場合は true。それ以外の場合は、false。

### <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

    public boolean hasUserSetting()

#### <a name="return-value"></a>戻り値

コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します。

| モード            | 高さの計算                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| -1 正確        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します。

| モード          | 高さの計算                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| 正確         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを取得します。

    public str helpField()

#### <a name="return-value"></a>戻り値

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

#### <a name="remarks"></a>備考

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの HierarchyParent プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールの HierarchyParent プロパティ値。

### <a name="method-hwnd"></a>メソッド hWnd

コントロールの Windows ハンドルを取得します。

    public int hWnd()

#### <a name="return-value"></a>戻り値

ハンドラーコントロールのハンドルです。

#### <a name="remarks"></a>備考

この処理は、Windows API で使用できます。

### <a name="method-imemode"></a>メソッド iMEMode

    public int iMEMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を取得します。

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

コントロールが表示される場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

### <a name="method-isrestricted"></a>メソッド isRestricted

コントロールが制限されるかどうかを示す値を取得します。

    public boolean isRestricted()

#### <a name="return-value"></a>戻り値

コントロールが制限される場合は true。それ以外の場合は false。

### <a name="method-isusersetupenabled"></a>メソッド isUserSetupEnabled

コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a>パラメーター

neededSetupRights  
コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。

#### <a name="return-value"></a>戻り値

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

### <a name="method-isvalid"></a>メソッド isValid

    public boolean isValid()

#### <a name="return-value"></a>戻り値

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-labelalignment"></a>メソッド labelAlignment

    public int labelAlignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelbold"></a>メソッド labelBold

    public int labelBold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

    public int labelCharacterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfont"></a>メソッド labelFont

    public str labelFont([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfontsize"></a>メソッド labelFontSize

    public int labelFontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelforegroundcolor"></a>メソッド labelForegroundColor

    public int labelForegroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelguide"></a>メソッド labelGuide

    public int labelGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheight"></a>メソッド labelHeight

    public int labelHeight(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightmode"></a>メソッド labelHeightMode

    public int labelHeightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightvalue"></a>メソッド labelHeightValue

    public int labelHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelitalic"></a>メソッド labelItalic

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmousedblclick"></a>メソッド labelMouseDblClick

    public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmousedown"></a>メソッド labelMouseDown

    public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmouseup"></a>メソッド labelMouseUp

    public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelposition"></a>メソッド labelPosition

    public int labelPosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelunderline"></a>メソッド labelUnderline

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidth"></a>メソッド labelWidth

    public int labelWidth(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthmode"></a>メソッド labelWidthMode

    public int labelWidthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthvalue"></a>メソッド labelWidthValue

    public int labelWidthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leave"></a>メソッド leave

    public boolean leave()

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

フォームのコントロールの水平位置を取得または設定します。

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-leftmode"></a>メソッド leftMode

フォームのコントロールの水平配置モードを設定します。

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの水平配置モード。

### <a name="method-leftvalue"></a>メソッド leftValue

フォームのコントロールの水平位置を取得または設定します。

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-limittext"></a>メソッド limitText

    public int limitText([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextmode"></a>メソッド limitTextMode

    public AutoMode limitTextMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextvalue"></a>メソッド limitTextValue

    public int limitTextValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linefromchar"></a>メソッド lineFromChar

    public int lineFromChar(int charIndex)

#### <a name="parameters"></a>パラメーター

charIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-lineindex"></a>メソッド lineIndex

    public int lineIndex(int lineNo)

#### <a name="parameters"></a>パラメーター

lineNo  

#### <a name="return-value"></a>戻り値

### <a name="method-linelength"></a>メソッド lineLength

    public int lineLength(int lineNo)

#### <a name="parameters"></a>パラメーター

lineNo  

#### <a name="return-value"></a>戻り値

### <a name="method-lookupbutton"></a>メソッド lookupButton

    public int lookupButton([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-lookuponly"></a>メソッド lookupOnly

    public boolean lookupOnly([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-mandatory"></a>メソッド mandatory

    public boolean mandatory([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-markasuseradd"></a>メソッド markAsUserAdd

ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。

### <a name="method-modified"></a>メソッド modified

    public boolean modified()

#### <a name="return-value"></a>戻り値

### <a name="method-mousedblclick"></a>メソッド mouseDblClick

コントロールがユーザーにダブルクリックされると呼び出されます。

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-mousemove"></a>メソッド mouseMove

ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-multiline"></a>メソッド multiLine

    public boolean multiLine([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parentcontrol"></a>メソッド parentControl

コントロールの親コントロールを取得します。

    public FormControl parentControl()

#### <a name="return-value"></a>戻り値

コントロールの親コントロール。

### <a name="method-passwordstyle"></a>メソッド passwordStyle

    public boolean passwordStyle([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-posfromchar"></a>メソッド posFromChar

    public container posFromChar(int charIndex)

#### <a name="parameters"></a>パラメーター

charIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-presencedatafield"></a>メソッド presenceDataField

    public FieldId presenceDataField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-presencedatasource"></a>メソッド presenceDataSource

    public int presenceDataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-presenceindicatorallowed"></a>メソッド presenceIndicatorAllowed

    public int presenceIndicatorAllowed([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-previewpartref"></a>メソッド previewPartRef

    public str previewPartRef([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-promptrect"></a>メソッド promptrect

    public int promptrect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-replaceonlookup"></a>メソッド replaceOnLookup

    public boolean replaceOnLookup([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-resolveambiguousreference"></a>メソッド resolveAmbiguousReference

    public str resolveAmbiguousReference()

#### <a name="return-value"></a>戻り値

### <a name="method-disambiguationlookuptarget"></a>メソッド disambiguationLookupTarget

    public FieldBinding disambiguationLookupTarget()

#### <a name="return-value"></a>戻り値

### <a name="method-lookupdisambiguatereference"></a>メソッド lookupDisambiguateReference

    public str lookupDisambiguateReference(FieldBinding fieldBinding)

#### <a name="parameters"></a>パラメーター

fieldBinding  

#### <a name="return-value"></a>戻り値

### <a name="method-searchafterinput"></a>メソッド searchAfterInput

    public int searchAfterInput([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-searchmode"></a>メソッド searchMode

    public int searchMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるセキュリティ キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。

### <a name="method-showcontextmenu"></a>メソッド showContextMenu

コントロールのショートカット メニューを表示します。

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a>パラメーター

menuHandle  
表示するメニューの ID。

#### <a name="return-value"></a>戻り値

通話が成功したかどうかを示す整数値。

### <a name="method-showlabel"></a>メソッド showLabel

    public boolean showLabel([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。

### <a name="method-sort"></a>メソッド sort

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a>パラメーター

sortDirection  

#### <a name="return-value"></a>戻り値

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tooltip"></a>メソッド toolTip

コントロールのツール ヒント テキストを取得します。

    public str toolTip()

#### <a name="return-value"></a>戻り値

コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。

#### <a name="remarks"></a>備考

メソッドを上書きして、toolTip メソッドに値を渡すことができます。

### <a name="method-top"></a>メソッド top

フォームのコントロールの垂直位置を取得または設定します。

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-topmode"></a>メソッド topMode

フォームのコントロールの垂直配置モードを設定します。

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直配置モード。

### <a name="method-topvalue"></a>メソッド topValue

フォームのコントロールの垂直位置を取得または設定します。

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

コントロールのユーザー データを取得または設定します。

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ。

### <a name="method-userdataitem"></a>メソッド userDataItem

コントロールのユーザー データ品目を取得または設定します。

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ アイテム。

### <a name="method-userdataitems"></a>メソッド userDataItems

コントロールのユーザー データ項目の数を取得または設定します。

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目の数を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ項目の数。

### <a name="method-userdisable"></a>メソッド userDisable

ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。

    public int userDisable([int value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。

### <a name="method-userfasttabsummary"></a>メソッド userFastTabSummary

    public int userFastTabSummary([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userheight"></a>メソッド userHeight

コントロールのカスタム ユーザーの高さを取得または設定します。

    public int userHeight([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザーの高さ (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのカスタム ユーザーの高さ。

### <a name="method-userhide"></a>メソッド userHide

コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。

    public int userHide([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

#### <a name="remarks"></a>備考

ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 このメソッドを使用すると、プログラムによって値を決定して設定できます。

### <a name="method-userorgcontainer"></a>メソッド userOrgContainer

コントロールの組織コンテナを取得または設定します。

    public int userOrgContainer([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織コンテナー (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織コンテナー。

### <a name="method-userorgsibling"></a>メソッド userOrgSibling

コントロールの組織兄弟を取得または設定します。

    public int userOrgSibling([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織の兄弟 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織の兄弟。

### <a name="method-userprompttext"></a>メソッド userPromptText

コントロールのユーザーラベル テキストを取得または設定します。

    public str userPromptText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー ラベルのテキスト (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザーラベル テキスト。

### <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

コントロールのユーザー セキュリティ レベルを取得または設定します。

    public int userSecurityLevel([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー セキュリティ レベル (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザー セキュリティ レベル。

### <a name="method-userskip"></a>メソッド userSkip

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。

    public int userSkip([int value])

#### <a name="parameters"></a>パラメーター

値  
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。

#### <a name="return-value"></a>戻り値

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

### <a name="method-userwidth"></a>メソッド userWidth

ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅として使用するピクセル数 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

### <a name="method-validate"></a>メソッド validate

    public boolean validate()

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの AutoMode 値を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode 値を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォームのコントロールの垂直スペーシング モードを設定します。

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング モード。

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの上下の間隔を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの可視化設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します。

| モード           | 幅計算                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| -1 正確       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します。

| モード         | 幅計算                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-presencerefresh"></a>メソッド presenceRefresh

    public void presenceRefresh()

### <a name="method-onlookup"></a>メソッド OnLookup

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

### <a name="method-performtypelookup"></a>メソッド performTypeLookup

    public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])

#### <a name="parameters"></a>パラメーター

userType  

<!-- -->

arrayIndex  

<!-- -->

会社  

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-undo"></a>メソッド undo

    public void undo()

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-setselection"></a>メソッド setSelection

    public void setSelection(int charIndexFrom, int charIndexTo)

#### <a name="parameters"></a>パラメーター

charIndexFrom  

<!-- -->

charIndexTo  

### <a name="method-scrollcursor"></a>メソッド scrollCursor

    public void scrollCursor()

### <a name="method-enter"></a>メソッド enter

    public void enter()

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-performdblookup"></a>メソッド performDBLookup

    public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])

#### <a name="parameters"></a>パラメーター

fieldId  

<!-- -->

tableId  

<!-- -->

会社  

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

### <a name="method-onmodified"></a>メソッド OnModified

    private void OnModified([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-dropex"></a>メソッド dropEx

ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-onvalidating"></a>メソッド OnValidating

    private void OnValidating([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-setcursorpos"></a>メソッド setCursorPos

    public void setCursorPos(int x, int y)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

### <a name="method-performformlookup"></a>メソッド performFormLookup

    public void performFormLookup(xFormRun form)

#### <a name="parameters"></a>パラメーター

フォーム  

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-linescroll"></a>メソッド lineScroll

    public void lineScroll(int dx, int dy)

#### <a name="parameters"></a>パラメーター

dx  

<!-- -->

dy  

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-textchange"></a>メソッド textChange

    public void textChange()

### <a name="method-jumpref"></a>メソッド jumpRef

    public void jumpRef()

### <a name="method-lookup"></a>メソッド lookup

    public void lookup()

### <a name="method-pastetext"></a>メソッド pasteText

    public void pasteText(str pasteStr, [boolean InsertSel])

#### <a name="parameters"></a>パラメーター

pasteStr  

<!-- -->

InsertSel  

### <a name="method-onvalidated"></a>メソッド OnValidated

    private void OnValidated([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-drop"></a>メソッド drop

ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。



