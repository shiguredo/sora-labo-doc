# Sora Labo ドキュメント

これは時雨堂が提供している [Sora Labo](https://sora-labo.shiguredo.app/) のドキュメントです。
ご利用前にかならずご確認いただきますよう、お願いいたします。

## ステータスページ

<https://shiguredo.onlineornot.com>

## おしらせ

### 本ドキュメントおよび利用規約を改定しました

**日時**: 2025-06-16

- アカデミックの利用を **可** としました
- 個人事業主の利用を **不可** としました
- その他、ご利用時の制限事項や禁止事項などを変更しました

 [新しい利用規約](https://github.com/shiguredo/sora-labo-doc/blob/master/TERMS.md) についてはこちらからご確認ください

### WHIP/WHEP の TURN 利用を必須としました

**日時**: 2024-12-20

- OBS を利用する場合は OBS 30.2 以降を利用してください

### Sora クラスターのノード数を 20 に増やしました

**日時**: 2024-11-21

- レギュラーノード: 5
- テンポラリーノード: 15

### JWT プライベートクレームを追加し、検証用の metadata 項目を廃止しました

**日時**: 2024-10-28

- JWT のプライベートクレームを追加しました
  - `turn_tcp_only` を追加しました
  - `turn_tls_only` を追加しました
  - `cluster_affinity` を追加しました
- 検証用の metadata 項目を廃止しました
  - `turn_tcp_only` を廃止しました
  - `turn_tls_only` を廃止しました
  - `cluster_affinity` を廃止しました

今後は `metadata` に指定するのではなく、JWT のプライベートクレームに指定して利用してください。

### Sora クラスターの構成を変更しました

**日時**: 2024-08-30

- シグナリング URL を一本化しました
  - `wss://sora.sora-labo.shiguredo.app/signaling`
- レギュラーノード: 5 / テンポラリーノード: 5 の 10 台構成に変更しました
- ノード間通信を VPC から VLAN に変更しました

### Sora の構成を一新しました

**日時**: 2024-05-29

Sora Labo で提供する Sora の構成を一新しました。

#### Sora クラスター

- Akamai Connected Cloud に変更しました
- リージョンは大阪です
- シグナリング URL を一本化しました
  - `wss://sora.sora-labo.shiguredo.app/signaling`
- レギュラーノード: 5 / テンポラリーノード: 2 の 7 台構成に変更しました
- リレーあり / アフィニティなし
- ノード間通信は VPC です

#### Sora マルチリージョンクラスター

- 大阪 / チェンナイ / ストックホルム / マイアミ / シアトルの 5 リージョンでクラスターを組んでいます
- レギュラーノード: 5 の 5 台構成です
- リレーあり / アフィニティなし
- ノード間通信はパブリックかつ [Tailscale](https://tailscale.com/) です

#### Sora IPv6 オンリー

- Akamai Connected Cloud に変更しました
- リージョンは大阪です
- シグナリング URL を変更しました
  - `wss://sora-ipv6.sora-labo.shiguredo.app/signaling`
- シングルノードです

## 古いお知らせ

[OLD_NEWS.md](OLD_NEWS.md) をご覧ください。

## FAQ

**Sora Labo は WebRTC SFU Sora または Sora Cloud の導入を前提とした検証、および WebRTC の技術そのものに関心のある個人の方の技術的な理解を目的として無償で提供しています。それ以外の目的で本サービスを利用することはできません**

- Sora Labo は無料で利用できますか？
  - 無料で利用できます
- Sora Labo は商用サービスや商用製品で利用できますか？
  - 商用サービスや商用製品では利用できません
  - 商用サービスや商用製品で利用する場合は Sora の本番環境用ライセンス、または Sora Cloud を契約してください
- Sora Labo を商用サービスや商用製品の開発のために利用できますか？
  - 商用サービスや商用製品の開発のためには利用できません
  - 商用サービスや商用製品の開発のために利用する場合は Sora の開発環境用ライセンス、または Sora Cloud を契約してください
- Sora Labo は不特定多数の人が利用する無料のサービスや製品、展示会などで利用できますか？
  - 無料・有料を問わず、不特定多数の人が利用するサービスや製品、展示会などでは利用できません
  - 不特定多数の人が利用するサービスや製品、展示会で利用する場合は Sora の本番環境用ライセンス、または Sora Cloud を契約してください
- Sora Labo は法人や団体で利用できますか？
  - 法人や団体でも利用できますが、Sora および Sora Cloud の導入を前提とした検証目的でのみご利用いただけます
- Sora Labo はアカデミックで利用できますか？
  - **利用できます**
  - 以前は利用不可でしたが、アカデミックでも Sora および Sora Cloud の導入を前提とした検証目的であればご利用いただけます
- Sora Labo は個人事業主で利用できますか？
  - **利用できません**
  - 以前は利用可能でしたが、Sora および Sora Cloud は個人事業主の方に提供していないことから、Sora Labo の提供を中止しました
  - ~~利用可能ですが、Sora の検証目的でのみご利用いただけます~~
- Sora Labo は日本以外からも利用できますか？
  - 利用できません
  - 何か問題が起きたときに海外の場合は対応ができないため、日本国内からの利用に限定しています
- Sora Labo サービス全体での転送量制限はありますか？
  - ありません
  - ただし極端に転送量の多い配信をされると他の利用者に影響しますので、ご配慮をお願いします
- Sora Labo サービス全体での帯域制限はありますか？
  - サービス全体ではなく Sora ノードごとに帯域制限があります
  - In 40 Gbps / Out 1 Gbps です
- Sora Labo は同時接続数の制限がありますか？
  - 1 チャネルあたりの最大同時接続数は 10 です
- Sora Labo は映像ビットレートの制限はありますか？
  - 最大 15 Mbps です
- Sora Labo の合計接続時間制限はありますか？
  - あります
  - **月 2000 分まで**です
  - 30 日経過すると復活します
  - 1 月 1 日 に 300 分利用すると、 1 月 31 日に 300 分追加されます
- Sora Labo の連続接続時間制限はありますか？
  - あります
  - 60 分です。60 分経過すると接続は切断されます
- Sora Labo の DataChannel メッセージング機能に制限はありますか？
  - ありません
  - 極端に転送量の多い配信をされると他の利用者に影響しますので、ご配慮をお願いします
- Sora Labo は TURN-TCP や TURN-TLS を提供していますか？
  - 提供しています
  - TURN-TCP は 443 ポートです
  - TURN-TLS は 443 ポートです
- Sora Labo は IPv6 に対応していますか？
  - 対応しています
- Sora Labo の SLA はいくつですか？
  - SLA はありません
- Sora Labo はウェブフック機能を提供しますか？
  - 提供はしていません。Sora の評価版または Sora Cloud をご検討ください
- Sora Labo は Sora の HTTP API を提供しますか？
  - 提供はしていません。Sora の評価版または Sora Cloud をご検討ください
- Sora Labo はサポートを提供していますか？
  - 提供していません
- Sora SDK のサポートは提供していますか？
  - 提供していません
- 変更などの通知は行いますか？
  - すべて時雨堂 Discord の `#sora-labo` にて通知します
- メンテナンス告知は行いますか？
  - 原則として行いません
  - 長時間にわたるメンテナンスの場合のみ、時雨堂 Discord の `#sora-labo` にて通知します
- Sora Labo の Sora のバージョンはいくつですか？
  - 今後リリースを予定している最新の Sora の開発版で、製品版とは異なります
- 認証エラー理由に `PLEASE-CONTACT-US` が出ました
  - いずれかの制限または禁止項目に当てはまっている可能性があります。Discord にてご連絡ください
- 認証エラー理由に `CONNECTION-LIMIT` が出ました
  - 直近 30 日間の利用が 2000 分を超えると利用できなくなるので、少し時間をおいてから再度試してみてください

## Discord

アナウンスなどの情報共有は全て Discord を利用しています。

- サポート
  - しません
- アドバイス
  - します
- フィードバック
  - 歓迎します

<https://discord.gg/shiguredo>

`#sora-labo` へどうぞ

## 制限

- 最大合計接続時間は 2000 分です
- 1 接続の連続接続時間は 60 分です
- Sora の **HTTP API は提供していません**
- Sora の **ウェブフック機能は提供していません**
- Sora の **録画機能は提供していません**
- Sora Labo は Sora SDK と Momo 以外での利用を想定していません
- サービス全体での最大同時接続数は 1000 です
- 1 チャネルに接続できる最大の数は 10 です
- 1 接続のビットレートの最大値は 15 Mbps です

## 禁止

- ~~アカデミックでの利用~~
- 商用サービス・製品での利用
- 商用サービス・製品開発目的での利用
- 不特定多数の人に向けたサービスでの利用
- 個人事業主の利用
- 同業他社の社員（その代理人、委託先を含む）の利用
- 負荷試験ツールの利用
- すでに登録済みのアカウントとは別にアカウントを作成しての利用
- Sora Labo のベンチマーク結果を第三者へ公開すること

## 商用利用について

Sora Labo は商用利用は許可していませんので、以下のいずれかをご検討ください。

- [Sora Cloud](https://sora-cloud.shiguredo.jp/) を契約をする
  - 運用を全部任せたい
- [WebRTC SFU Sora](https://sora.shiguredo.jp/) を契約をする
  - 自分たちで運用したい

## 利用可能な SDK やクライアント、ライブラリ

- [WebRTC SFU Sora JavaScript SDK](https://github.com/shiguredo/sora-js-sdk)
  - [Sora JavaScript SDK ドキュメント](https://sora-js-sdk.shiguredo.jp/)
- [WebRTC SFU Sora iOS SDK](https://github.com/shiguredo/sora-ios-sdk)
  - [Sora iOS SDK ドキュメント](https://sora-ios-sdk.shiguredo.jp/)
  - [WebRTC SFU Sora iOS SDK クイックスタート](https://github.com/shiguredo/sora-ios-sdk-quickstart)
  - [WebRTC SFU Sora iOS SDK サンプル集](https://github.com/shiguredo/sora-ios-sdk-samples)
- [WebRTC SFU Sora Android SDK](https://github.com/shiguredo/sora-android-sdk)
  - [Sora Android SDK ドキュメント](https://sora-android-sdk.shiguredo.jp/)
  - [WebRTC SFU Sora Android SDK クイックスタート](https://github.com/shiguredo/sora-android-sdk-quickstart)
  - [WebRTC SFU Sora Android SDK サンプル集](https://github.com/shiguredo/sora-android-sdk-samples)
- [WebRTC SFU Sora Unity SDK](https://github.com/shiguredo/sora-unity-sdk)
  - [WebRTC SFU Sora Unity SDK サンプル集](https://github.com/shiguredo/sora-unity-sdk-samples)
- [WebRTC SFU Sora C++ SDK](https://github.com/shiguredo/sora-cpp-sdk)
- [WebRTC SFU Sora Python SDK](https://github.com/shiguredo/sora-python-sdk)
  - [WebRTC SFU Sora Python SDK サンプル集](https://github.com/shiguredo/sora-python-sdk-examples)
- [WebRTC SFU Sora C SDK](https://github.com/shiguredo/sora-c-sdk)
- [WebRTC Native Client Momo](https://github.com/shiguredo/momo)

## 比較表

Sora Labo は検証目的以外での利用はできません。それ以外は [Sora Cloud](https://sora-cloud.shiguredo.jp)_または [Sora](https://sora.shiguredo.jp) をご検討ください。

| 機能       | Sora Labo          | Sora Cloud         | Sora           |
|:------------:| :------------------: | :-------------------:|:----------------:|
| タイプ     | SaaS               | SaaS               | パッケージ     |
| 商用利用   | 不可、検証目的のみ | 可                 | 可             |
| 同時接続   | 1 チャネル 10 程度 | 制限なし          | ライセンスに依存 |
| 帯域       | 制限あり           | 制限なし       | 自由           |
| 認証       | アクセストークン   | アクセストークン   | 自由           |
| ウェブフック | 不可             | 可                 | 可             |
| API        | 不可               | 一部を除いて可     | 可             |
| 録画       | 不可               | 可                 | 可             |
| 運用       | 不要               | 不要               | 必要           |
| 構築       | 不要               | 不要               | 必要           |
| サポート   | 無し               | 有り(チケット)     | 有り(メール)   |

## 利用方法

### アクセストークンを生成する

- シークレットキーを利用して JWT (HS256) で生成してください
- exp はオプションです
- nbf はオプションです
- channel_id はオプションです
  - channel_id クレームを指定するとチャネル ID が一致していないと認証に失敗します
- turn_tcp_only はオプションです
- turn_tls_only はオプションです
- cluster_affinity はオプションです

アクセストークンは Sora Labo のダッシュボードで作成可能です。

![Image](https://i.gyazo.com/2da238f201c08ffef50d01c791d80e34.png)

### シークレットキーをアクセストークンとして利用する

アクセストークンを生成せずに、シークレットキーをそのままアクセストークンとしても利用可能です。

### Sora DevTools を利用する

[Sora DevTools](https://github.com/shiguredo/sora-devtools) という開発者ツールを <https://sora-devtools.shiguredo.jp/> にデプロイして公開しています。

ダッシュボードページに Sora DevTools をSora Labo 経由で利用できるように、
チャネル ID とアクセストークンとシグナリング URL 埋め込んである URL を用意してあります。

![Image](https://i.gyazo.com/8c7863443bd8c86130f428f13470191e.png)

## Sora JavaScript SDK を利用する

以下をご確認ください。

[Sora Labo](https://sora-js-sdk.shiguredo.jp/sora_labo)


## Sora Android SDK を利用する

[shiguredo/sora-android-sdk: WebRTC SFU Sora Android SDK](https://github.com/shiguredo/sora-android-sdk)

Sora Android SDK のクイックスタートまたはサンプル集を利用して Sora Labo に接続できます。

- [WebRTC SFU Sora Android SDK クイックスタート](https://github.com/shiguredo/sora-android-sdk-quickstart)
- [WebRTC SFU Sora Android SDK サンプル集](https://github.com/shiguredo/sora-android-sdk-samples)

### gradle.properties の作成

クイックスタートまたはサンプル集のディレクトリトップの `gradle.properties.example` を元に `gradle.properties` を作成します。

gradle.properties の作成:

```bash
cp gradle.properties.example gradle.properties
```

### 接続情報の設定

`gradle.properties` に Sora Labo への接続情報を設定します。

- `signaling_endpoint` に Sora Labo の Sora シグナリング URLs を設定してください。カンマ区切りですべてのシグナリング URL を指定してください。
- `channel_id` に `<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>` を指定してください
  - ここでは GitHub Username を `shiguredo` としています
  - ここでは GitHub ID を `0` としています
- `signaling_metadata` に自分のアクセストークンを指定してください
  - ここではアクセストークンを `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is` としています

gradle.properties への設定例:

```properties
# Setting Sora's signaling endpoint and channel_id
signaling_endpoint = wss://sora.sora-labo.shiguredo.app/signaling
channel_id         = shiguredo_0_sora

# Setting Signaling Metadata.
# Quotes must be double escaped.
# e.g.) signaling_metadata = {\\"spam\\":\\"egg\\"}
# This setting is required. If you do not want to use it, set it to blank.
signaling_metadata = {\\"access_token\\":\\"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is\\"}
```

## Sora iOS SDK を利用する

[shiguredo/sora-ios-sdk: WebRTC SFU Sora iOS SDK](https://github.com/shiguredo/sora-ios-sdk)

Sora iOS SDK のクイックスタートまたはサンプル集を利用して Sora Labo に接続できます。

- [WebRTC SFU Sora iOS SDK クイックスタート](https://github.com/shiguredo/sora-ios-sdk-quickstart)
- [WebRTC SFU Sora iOS SDK サンプル集](https://github.com/shiguredo/sora-ios-sdk-samples)

### Environment.swift の作成

クイックスタートまたはサンプル集の `Environment.example.swift` を元に `Environment.swift` を作成します。

Environment.swift の作成:

```bash
cp Environment.example.swift Environment.swift
```

### 接続情報の設定

`Environment.swift` に Sora Labo への接続情報を設定します。

- `signaling_endpoint` に Sora Labo の Sora シグナリング URLs を全て指定してください
- `channel_id` に `<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>` を指定してください
  - ここでは GitHub Username を `shiguredo` としています
  - ここでは GitHub ID を `0` としています
- `signalingConnectMetadata` に自分のアクセストークンを指定してください
  - ここではアクセストークンを `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is` としています

Environment.swift への設定例:

```swift
// 接続するサーバーのシグナリング URL
static let urls = [URL(string: "wss://sora.sora-labo.shiguredo.app/signaling")!]

// チャネル ID
static let channelId = "shiguredo_0_sora"

// metadata
static let signalingConnectMetadata = ["access_token" : "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is"]
```

## WebRTC Native Client Momo で Sora を利用する

[shiguredo/momo: WebRTC Native Client Momo](https://github.com/shiguredo/momo)

Momo で Sora が利用できます。

- `channel_id` に `<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>` を指定してください
  - ここでは GitHub Username を `shiguredo` としています
  - ここでは GitHub ID を `0` としています
- 自分のアクセストークンを --metadata で指定してください
  - ここではアクセストークンを `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is` としています
- Sora Labo は Sora クラスターを採用しているため提供されているシグナリング URL をすべて指定してください

GitHub Username が shiguredo で、 チャネル ID が sora-devtools の場合:

```bash
./momo --resolution VGA --no-audio-device sora --auto \
    --signaling-url wss://sora.sora-labo.shiguredo.app/signaling \
    --channel-id shiguredo_0_sora \
    --role sendonly --multistream true --video-codec-type VP8 --video-bit-rate 2500 \
    --metadata '{"access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is"}'
```

Sora DevTools のマルチストリーム受信を開いて接続してみてください。

![Image](https://i.gyazo.com/05f695c875b5d95c6a74c5150e7bd11a.png)

### AV1 を利用する

- Chrome 最新版
- Edge 最新版
- Safari Technology Preview 最新版

上記ブラウザや Momo を利用する事で、 AV1 が利用可能です。

### H.265 を利用する

Safari Technology Preview 最新版で H.265 を試すことが可能です。

## OBS (WebRTC/WHIP) で配信する

### 手順

1. OBS をダウンロードする
1. OBS に WHIP エンドポイント URL を指定する
1. OBS の `Bearer Token` にアクセストークンを指定する

### OBS のダウンロード

OBS の WebRTC/WHIP は 30.0.0 から対応していますが、Sora Labo は WebRTC/WHIP の TURN 利用を必須とする設定を行なっています。
TURN の利用に対応した OBS 30.2.0 以降をご利用ください。

<https://obsproject.com/ja/download>

### OBS (WebRTC/WHIP) の設定

1. サービスで WHIP を選ぶ
1. サーバーに WHIP エンドポイントを指定する
    - `https://sora.sora-labo.shiguredo.app/whip/{channel_id}`
    - `channel_id` は `{github-username}_{github-id}_{channel_name}` です
1. `Bearer Token` にアクセストークンを指定する

### OBS (WebRTC/WHIP) の設定例

以下は macOS の H.264 HWA を利用して 1080p 60fps で配信する際の設定例です。

![Image](https://i.gyazo.com/2343be3113f6ee62bbd5854832095d7b.png)

![Image](https://i.gyazo.com/bde10b937928dd43b588c205ee8e0435.png)

![Image](https://i.gyazo.com/988535745d0b273d9615d562dcf7330d.png)

## 認証方法

### チャネル ID を決める

アクセストークンを利用してチャネルに認証をかけてみます。

チャネル ID は GitHub アカウントのユーザ名を先頭に指定する必要があります。

`<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>` と指定する必要があります。

以下はチャネル名 sora-devtools 、Github ユーザ名 shiguredo 、GitHub ID 0 を指定した例です。

#### チャネル ID 例

`shiguredo_0_sora-devtools`

### metadata に access_token を指定する

Sora の SDK は metadata をシグナリング時に指定できます。metadata に `access_token` を指定して下さい。
これで利用可能になります。

アクセストークンが `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is` の場合

```json
{"access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is"}
```

## 検証向け機能

`metadata` の `access_token` に JWT を指定する際、JWT のプライベートクレームに検証用のクレームを指定できます。

### TURN-TCP 利用強制機能

指定した接続が TURN-TCP を強制的に利用する機能です。

JWT のプライベートクレームに `turn_tcp_only` を boolean 型で指定してください。

### TURN-TLS 利用強制機能

指定した接続が TURN-TLS を強制的に利用する機能です。

JWT のプライベートクレームに `turn_tls_only` を boolean 型で指定してください。

### クラスターアフィニティ有効化機能

同一セッションの接続を同一ノードに集約する機能です。

JWT のプライベートクレームに `cluster_affinity` を boolean 型で指定してください。

## Sora Labo のアカウントを削除する

**アカウントは削除しますが、ログは削除しないためアカウントを削除したとしても利用時間はリセットされません**

もし今後、 Sora Labo を利用しないのであればアカウントを削除できます。

ダッシュボードの一番下にアカウントの削除があります。
