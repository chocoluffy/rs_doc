# ReboSharp APIドキュメント

サポートされている C# の機能：

- 制御構造： 'if'、'else'、'while'、'for'、'do'、'foreach'、'switch'、'return'、'break'、'continue'、および条件ツール（条件？trueOutcome：falseOutcome）を組み込みます。
- 条件操作のバイパス（たとえば、true || ValidateCondition() は ValidateCondition() をトリガーしません）。
- 'typeof' での型取得。
- 'out' または 'ref' 属性を使用した外部関数（例：Physics.Detect() のいくつかのバージョン）。
- ユーザー定義関数：入力値と出力値を持つもの、拡張機能と柔軟なパラメータを使用するものを含みます。
- ユーザー定義の属性。
- RebornScript の機能を採用し、仮想関数を含む。
- パラメータを取るイベントレスポンダーを通じて Unity/RS と対話。
- 文字列内に変数値を埋め込む。
- 属性の初期設定。
- 自己参照関数呼び出しが可能。
- 直接および間接的なデータ型の変換。
- 配列構造とその要素のアクセサ。
- すべての組み込み数学関数。

ご質問がある場合は、[Discordサーバー](https://discord.gg/kFs7h7vtJJ)にご参加いただき、#SDKチャンネルでご質問ください。ドキュメントやAPIの使用方法のいかなる部分についても、説明させていただく準備ができております。

[Unity SDKをこちらでダウンロード](https://reborn-dev.oss-cn-zhangjiakou.aliyuncs.com/4T2M2QiR/RebornSDK_1_6_8.unitypackage), Unityのバージョン要件は2022.3.8以上で、新しいURPプロジェクトを作成してください。

## SDKインストールプロセス
1. パッケージをプロジェクトにドラッグしてインストールをクリックします。インストーラーが表示されます。インストーラーで、Reborn SDKをインストールをクリックします。
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/aab7f8b4de8713792f214e19fa1a8f3d9b845202/images/demo1.png" alt="画像1" style="height: 350px;" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo2.png" alt="画像2" style="height: 350px;" /></div>
</div>

2. SDKツールでログインし、RebornScriptセクションでRebornScriptsをインストールをクリックします。画像3に示すように、インストールが完了します。
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo3.png" alt="画像1" style="height: 350px;" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo4.png" alt="画像2" style="height: 350px;" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo5.png" alt="画像3" style="height: 350px;" /></div>
</div>

3.RebornScript例シーン
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo6.png" alt="画像1" style="height: 150px;" /></div>
</div>


# ReboSharp カスタマイズコンポーネント

## RSNetwork

- `IsNetworkSettled` - このクライアントから見たネットワークが安定しているか確認します。

- `IsMaster` - このメソッドを呼び出したクライアントがマスタークライアントか確認します。

- `IsClogged` - このクライアントから見たネットワークの混雑状況を確認します。

- `LocalPlayer` - このメソッドを呼び出したクライアントのローカルプレイヤーインスタンスを取得します。

- `MasterPlayer` - このメソッドを呼び出したクライアントから見たマスタークライアントのプレイヤーインスタンスを取得します。

- `IsOwner(RSPlayerプレイヤー, GameObjectオブジェクト)` - プレイヤーがこのGameObjectの所有者か確認します。
  - `player`: 所有権を確認するRSPlayer。
  - `obj`: プレイヤーが所有しているか確認するGameObject。

- `GetOwner(GameObjectオブジェクト)` - このGameObjectの所有者を取得します。
  - `obj`: 所有者を取得するGameObject。

- `SetOwner(RSPlayerプレイヤー, GameObjectオブジェクト)` - GameObjectの所有権を指定したプレイヤーに設定します。
  - `player`: 所有者として設定するRSPlayer。
  - `obj`: 所有権を設定するGameObject。 

- `IsObjectReady(GameObjectオブジェクト)` - ネットワーク化されたGameObjectが準備完了/生成済みか確認します。
  - `obj`: 準備完了状態を確認するGameObject。

- `Destroy(GameObjectオブジェクト)` - 指定したネットワーク化されたGameObjectを破棄します。
  - `obj`: 破棄するGameObject。

- `GetUniqueName(GameObjectオブジェクト)` - GameObjectの一意の識別名を取得します。
  - `obj`: 一意の名前を取得するGameObject。

- `GetServerTimeInSeconds` - サーバー時刻を秒単位で取得します。

- `GetServerTimeInMilliseconds` - サーバー時刻をミリ秒単位で取得します。

- `CalculateServerDeltaTime(double時刻を秒で, double前の時刻を秒で)` - 2つのサーバー時刻スタンプの間のデルタ時間を計算します。
  - `timeInSeconds`: 現在のサーバー時刻(秒)。
  - `previousTimeInSeconds`: 前のサーバー時刻(秒)。

- `CreateNetAudioAsset(long id, Vector3座標, Quaternion回転)` - ネットワーク化されたオーディオソースを生成します。
  - `id`: オーディオソースの一意のID。
  - `pos`: オーディオソースの座標。
  - `rot`: オーディオソースの回転。

- `SetNetMapCustomMessage(stringメッセージ)` - ネットマップ上にカスタムステータステキストを設定します。
  - `message`: カスタムステータスメッセージの文字列。

## RSProp

- `grabbable` - Propを直接掴めるかを示すブール値。

- `wearable` - Propが装着可能かを示すブール値。

- `scalable` - 把持時にスケールを調整できるかを示すブール値。

- `grabState` - 現在のGrabState列挙値。

- `grabType` - GrabType列挙値。 

- `specialMessage` - 特殊ステータステキスト用の文字列。

- `currentPlayer` - 現在掴んでいるRSPlayerを取得。

- `currentHand` - 現在掴んでいる手(GrabHand列挙)を取得。

- `Drop()` - 現在の所有者に自身を落とすように指示します。

- `GenerateHapticEvent(float継続時間, float振幅, float周波数)` - 掴んでいる手で触覚イベントを生成します。
  - `duration`: 触覚の継続時間(秒)。
  - `amplitude`: 触覚の振幅 0-1。
  - `frequency`: 触覚の周波数(Hz)。

- `OnDestroy()` - 破棄時に呼び出されます。RSInternalPropの破棄ロジックを呼び出します。

- `PlayHaptics()` - デフォルトの触覚イベントを発生させるヘルパー。

- `GrabHand` - 左右の手を表す列挙型。

- `GrabState` - すべての掴み状態を表す列挙型。

- `GrabType` - 掴みメカニズムを記述する列挙型。

## RSGraphics

- `Blit(Textureソース, RenderTextureデスティネーション)`
  - `source`: コピー元のソーステクスチャ。
  - `dest`: コピー先のレンダーテクスチャ。

- `Blit(Textureソース, RenderTextureデスティネーション, Materialマテリアル)`
  - `source`: コピーするテクスチャ。
  - `dest`: コピー先のレンダーテクスチャ。
  - `mat`: コピーに使用するマテリアル。

- `Blit(Textureソース, RenderTextureデスティネーション, Vector2スケール, Vector2オフセット)`
  - `source`: ソーステクスチャ。
  - `dest`: デスティネーションレンダーテクスチャ。
  - `scale`: コピー時に適用するスケール係数。
  - `offset`: コピー時に適用するオフセット。
  
- `DrawMeshInstanced(Meshメッシュ, Materialマテリアル, Matrix4x4[]行列リスト)`
  - `mesh`: 描画するメッシュ。
  - `mat`: 使用するマテリアル。
  - `matrices`: 各インスタンスに適用する行列のリスト。

- `DrawMeshInstanced(Meshメッシュ, Materialマテリアル, Matrix4x4[]行列リスト, intインスタンス数)`
  - `mesh`: 描画するメッシュ。
  - `mat`: 使用するマテリアル。
  - `matrices`: 適用する行列のリスト。
  - `count`: 描画するインスタンス数。

## RSPlayer  

- `gameObject` - プレイヤーのGameObjectを取得。

- `isMaster` - プレイヤーがマスタークライアントか確認。

- `isMine` - プレイヤーがローカルクライアントか確認。

- `nickName` - プレイヤーのニックネーム文字列を取得。

- `profilePicture` - プレイヤーのプロフィールピクチャテクスチャを取得。 

- `userId` - プレイヤーの一意の識別子を取得。

- `GetAllPlayers()` - すべてのRSPlayerインスタンスを取得。

- `GetPlayerCount()` - プレイヤー数を取得。

- `GetPlayerId(RSPlayerプレイヤー)` - プレイヤーのIDを取得。
  - `player`: IDを取得するプレイヤー。

- `GetPlayerByGameObject(GameObjectオブジェクト)` - GameObjectからプレイヤーを取得。
  - `go`: プレイヤーのGameObject。

- `GetPlayerById(int id)` - IDからプレイヤーを取得。
  - `id`: 検索するID。

- `GetBoneTransform(HumanBodyBonesボーン)` - ボーンの変換を取得。
  - `bone`: 変換を取得するボーン。

- `GetBonePosition(HumanBodyBonesボーン)` - ボーンの位置を取得。
  - `bone`: 位置を取得するボーン。

- `GetBoneRotation(HumanBodyBonesボーン)` - ボーンの回転を取得。
  - `bone`: 回転を取得するボーン。 

- `GetCameraPosition()` - カメラの位置を取得。

- `GetCameraRotation()` - カメラの回転を取得。

- `GetPropInHand(GrabHand手)` - 手に持っているPropを取得。
  - `hand`: Propを持っている手。

- `PlayHapticEventInHand(GrabHand手, float継続時間, float振幅, float周波数)` - 手で触覚を再生。
  - `hand`: 再生する手。
  - `duration`: 触覚の継続時間(秒)。
  - `amplitude`: 触覚の振幅 0-1。
  - `frequency`: 触覚の周波数(Hz)。

- `Teleport(Vector3座標, Quaternion回転)` - プレイヤーをテレポート。
  - `position`: テレポート先の座標。
  - `rotation`: テレポート先の回転。

- `Respawn()` - プレイヤーを復活。

- `EnableGrab(bool有効)` - 掴みを有効/無効。
  - `enable`: trueで有効、falseで無効。

- `IsUserInVR()` - プレイヤーがVR中か確認。

- `GetPosition()` - プレイヤーの座標を取得。

- `GetRotation()` - プレイヤーの回転を取得。

## RSShader

- `PropertyToID(string名前)` - プロパティ名をシェーダーIDに変換。
  - `name`: シェーダープロパティの名前。

- `SetGlobalInteger(int名前ID, int値)` - グローバル整数シェーダープロパティを設定。
  - `nameID`: プロパティのID。
  - `value`: 設定する整数値。

- `SetGlobalFloat(int名前ID, float値)` - グローバル浮動小数点数プロパティを設定。
  - `nameID`: プロパティのID。
  - `value`: 設定する浮動小数点数値。

- `SetGlobalTexture(int名前ID, Texture値)` - グローバルテクスチャプロパティを設定。
  - `nameID`: プロパティのID。
  - `value`: 設定するテクスチャ値。

- `SetGlobalColor(int名前ID, Color値)` - グローバルカラープロパティを設定。
  - `nameID`: プロパティのID。
  - `value`: 設定するカラー値。

- `SetGlobalVector(int名前ID, Vector4値)` - グローバルベクトルプロパティを設定。
  - `nameID`: プロパティのID。
  - `value`: 設定するVector4値。

- `SetGlobalMatrix(int名前ID, Matrix4x4値)` - グローバル行列プロパティを設定。
  - `nameID`: プロパティのID。
  - `value`: 設定するMatrix4x4値。

- `ValidateAgainstPropertyIDWhitelist(int名前ID)` - プロパティIDがホワイトリストにあることを検証。
  - `nameID`: プロパティのID。

- `ClearGlobalVariableWhitelist()` - 許可IDのホワイトリストをクリア。

- `ShaderVariableType` - 異なるシェーダー変数型の列挙。

## RSRenderTexture

- `GetTemporary(int幅, int高さ, intデプスバッファ, RenderTextureFormatフォーマット 等)` - 一時レンダーテクスチャを取得。
  - `width`: テクスチャの幅(ピクセル)。
  - `height`: テクスチャの高さ(ピクセル)。
  - `depthBuffer`: 使用するデプスバッファのサイズ。 
  - `format`: レンダーテクスチャのフォーマット。

- `GetTemporary(RenderTextureDescriptor説明)` - 一時レンダーテクスチャを取得。
  - `desc`: 設定を定義したRenderTextureDescriptor。

- `ReleaseTemporary(RenderTextureテクスチャ)` - 一時テクスチャを解放。
  - `texture`: 解放する一時RenderTexture。

## RSMesh 

- `Slice(GameObjectオブジェクト, Vector3点, Vector3方向, Materialマテリアル, GameObject部分1, GameObject部分2)` - ゲームオブジェクトを2つに切り分ける。
  - `go`: 切り分けるGameObject。
  - `point`: スライスを実行するワールド空間での点。
  - `direct`: スライスの方向。
  - `partMat`: スライス面に適用するマテリアル。
  - `part1`: 最初のスライス部分のGameObject。
  - `part2`: 2番目のスライス部分のGameObject。

## RSMath

- `FFT(float[]時間領域)` - 時間領域のオーディオデータに高速フーリエ変換を適用し、周波数領域に変換する。周波数領域データを返す。
  - `timeDomain`: 時間領域のオーディオサンプルデータ。

- `CalculateDifferenceTotal(float[]配列1, float[]配列2, bool負を無視)` - 2つの配列の差分の合計を計算する。
  - `array1`: 比較する最初の浮動小数点数配列。
  - `array2`: 比較する2番目の浮動小数点数配列。
  - `ignoreNegative`: 負値を無視するか。

## RebornScriptBehaviour

- `SendCustomEvent(stringイベント名)` - このビヘイビアでカスタムイベントメソッドを呼び出す。
  - `eventName`: 呼び出す0パラメはい、続けます。

- `SendCustomNetworkEvent(NetworkEventTarget対象, stringイベント名)` - カスタムネットワークイベントを送信。
  - `target`: 所有者か全員に送信するか。
  - `eventName`: 呼び出すメソッド名。

- `SendNetMessage(NetworkEventTarget対象, string内容)` - ネットワークメッセージを送信。
  - `target`: メッセージの送信対象。
  - `content`: メッセージの内容文字列。

- `OnReceiveNetMessage(string内容)` - 受信したメッセージを処理。
  - `content`: 受信したメッセージの内容。

- `UpdateNetMapCustomMessage()` - ネットマップテキストの更新を指示。

- `OnUpdateNetMapCustomMessageComplete()` - ネットマップテキストの更新完了時のコールバック。

- `Interact()` - プレイヤーがこのゲームオブジェクトをクリックした時に呼び出し。

- `OnDrop()` - このオブジェクトがドロップされた時に呼び出し。

- `OnOwnershipTransferred(RSPlayerプレイヤー)` - オーナーシップが変更された時に呼び出し。
  - `player`: 新しいオーナープレイヤー。

- `OnGrab()` - このオブジェクトが掴まれた時に呼び出し。

- `OnPickupUseDown()` - ピックアップの使用が開始された時に呼び出し。

- `OnPickupUseUp()` - ピックアップの使用が終了した時に呼び出し。

- `OnHoverEnter()` - プレイヤーの手がこのオブジェクトの上にホバーした時に呼び出し。

- `OnHoverExit()` - ホバーが終了した時に呼び出し。

- `OnLeftTriggerDown()` - オブジェクトを持っている間に左トリガーを押した時に呼び出し。

- `OnLeftTriggerUp()` - 左トリガーが離された時に呼び出し。

- `OnRightTriggerDown()` - オブジェクトを持っている間に右トリガーを押した時に呼び出し。

- `OnRightTriggerUp()` - 右トリガーが離された時に呼び出し。

- `OnPlayerJoined(RSPlayerプレイヤー)` - プレイヤーが参加した時に呼び出し。
  - `player`: 参加したプレイヤー。

- `OnPlayerLeft(RSPlayerプレイヤー)` - プレイヤーが退室した時に呼び出し。
  - `player`: 退室したプレイヤー。

- `OnPlayerTriggerEnter(RSPlayerプレイヤー)` - プレイヤーがトリガーに入った時に呼び出し。
  - `player`: トリガーに入ったプレイヤー。

- `OnPlayerTriggerExit(RSPlayerプレイヤー)` - プレイヤーがトリガーから出た時に呼び出し。
  - `player`: トリガーから出たプレイヤー。  

- `OnPlayerTriggerStay(RSPlayerプレイヤー)` - プレイヤーがトリガー内にいる間、毎フレーム呼び出し。
  - `player`: トリガー内に留まっているプレイヤー。

- `OnReceiveNetMessage(string内容)` - このオブジェクトがネットワークメッセージを受信した時に呼び出し。
  - `content`: 受信したメッセージの内容文字列。

- `OnUpdateNetMapCustomMessageComplete(string内容)` - ネットマップテキストの更新完了時に呼び出し。
  - `content`: 更新されたステータステキスト。