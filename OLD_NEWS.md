# 古いおしらせ

## OBS (WebRTC/WHEP) 対応

**日時**: 2023-03-26

OBS (WebRTC/WHEP) のソースに対応しました。以下の URL で利用できます。
OBS の ``Bearer Token`` にはアクセストークンを指定してください。

`https://canary.sora-labo.shiguredo.app/whep/{channel-id}`

## クラスターリレー機能

**日時**: 2024-03-19

Sora Canary 版にてクラスターリレー機能を有効にしました。
どの Sora ノードに繫いでも同一チャネルに接続することができます。

## ロードバランサーで WebSocket が突然切断される問題への対応

**日時**: 2023-07-20

シグナリング URL の一本化に利用しているロードバランサー (以下 LB) を経由した場合、 WebSocket が突然切断される問題があることがわかりました。
この問題をすぐに解決することは難しいため、 Sora Labo の Canary 版 Sora のシグナリング URL は LB を利用することを停止しました。そのため Canary 版 Sora のシグナリング URL が変更になります。

```text
(変更前) wss://canary.sora-labo.shiguredo.app/signaling
  ↓
(変更後) wss://<node-id>.canary.sora-labo.shiguredo.app/signaling
```

`<node-id>` の箇所は "0001" などの文字列になります

OBS (WebRTC) は WebSocket を利用しないため、以前通り LB を指定する方式にしています。

## OBS (WebRTC/WHIP) 対応

**日時**: 2023-04-17

OBS (WebRTC/WHIP) での配信に対応しました。以下の URL で利用できます。
OBS の ``Bearer Token`` にはアクセストークンを指定してください。

`https://canary.sora-labo.shiguredo.app/whip/{channel-id}`

## チャネル ID の方式変更 (2023)

**日時**: 2023-04-17

チャネル ID の方式を変更しました。

いままでは `<好きな文字列>@<github-username>#<github-id>` でしたが、これを `<github-username>_<github-id>_<好きな文字列>` に変更します。

- OBS (WebRTC/WHIP) 機能に伴い URL にチャネル ID を指定する必要が出てきたため `#` と `@` を `_` に変更します
- 固有値を先頭に持ってくるため GitHub ユーザ名と ID を先頭に持ってきます
- _ は GitHub ユーザ名には利用できないため、採用しました
- GitHub ID とは GitHub アカウントに紐付けられている変更できないユニークな数値です
- GitHub Username とは GitHub アカウント名で、自由に変更が可能です

例えば GitHub ユーザ名が shiguredo で GitHub ID が 0 でチャネル名が sora の場合は `shiguredo_0_sora` となります。

## シグナリング URL 一本化

**日時**: 2023-04-10

Sora Labo の Canary 版 Sora のシグナリング URL を一本化しました。

`wss://canary.sora-labo.shiguredo.app/signaling`

## マルチクラウド化

**日時**: 2022-09-02

Sora Labo のバックエンドをマルチクラウド化しました。

## チャネル ID の方式変更 (2022)

**日時**: 2022-08-26

チャネル ID の方式を変更しました。

いままでは `<github-username>@<好きな文字列>` でしたが、これを `<好きな文字列>@<github-username>#<github-id>` に変更します。

- GitHub ID とは GitHub アカウントに紐付けられている変更できないユニークな数値です
- GitHub Username とは GitHub アカウント名で、自由に変更が可能です

例えばチャネル名が sora 、 GitHub ID が 0 、 GitHub Username が shiguredo の場合は `sora@shiguredo#0` となります。

## シグナリングキーの廃止とアクセストークンの開始

**日時**: 2022-08-25

シグナリングキーを廃止しました。今後はアクセストークンまたはシークレットキーを利用してください。

- アクセストークンは JWT HS256 でシークレットキーを利用して生成してください
- シークレットキーをアクセストークンとして利用可能です

今までは `metadata` の `signaling_key` にシグナリングキーを指定する必要がありましたが、
今後は `metadata` の `access_token` にアクセストークン、またはシークレットキーを指定する必要があります。

## canary 版のクラスターのノード追加

**日時**: 2022-08-22

5 ノードから 10 ノードへ変更しました。

## stable 版の単独ノードでの提供

**日時**: 2022-07-01

非クラスターを検証できるようにするため、
stable 版でのクラスター提供を廃止しました。

## stable 版 devtools へのリンクを追加

**日時**: 2022-04-08

canary 版 sora-devtools へのリンク以外に、stable 版 sora-devtools へのリンクを追加しました。

## multistream: false 無効化

**日時**: 2022-04-08

canary / stable で `multistream: false` を無効化しました。

マルチストリームへの一本化を検討するためのものとなります。

## multistream_auto_sharing_video_bit_rate = false に変更

**日時**: 2022-03-22

canary / stable 両方の Sora ノードの multistream_auto_sharing_video_bit_rate を false に変更しました。
そのため、マルチストリームを利用した場合、人数に応じて自動で配信ビットレートが制限されなくなります。利用の際は注意をお願いします。

[マルチストリームにおける映像ビットレート自動シェアリング機能](https://sora-doc.shiguredo.jp/MULTISTREAM#4fa79a)

## 利用時間拡大のお知らせ

**日時**: 2022-02-28

利用時間を直近 30 日 1000 分から直近 30 日 2000 分に拡大いたしました。

## アカデミック向けのご提供終了のお知らせ

**日時**: 2022-02-24

2022 年 2 月 28 日をもってアカデミック向けの提供を終了とさせていただきます。
アカデミックでのご利用をご検討されている方はライセンスの購入をご検討ください。

## 制限解除終了のお知らせ

**日時**: 2022-02-22

利用時間を直近 7 日 100 分から直近 30 日 1000 分に緩和したこともあり、制限解除申請を終了させていただきました。

現在ご利用いただいているお客様は制限期間までご利用可能です。

## Sora Labo ドメインの変更およびサービス全体での最大同時接続数の変更

**日時**: 2022-02-01

- Sora Labo のドメイン変更を行いました
  - Sora Labo に関するすべてのドメインが `sora-labo.shiguredo.jp` から `sora-labo.shiguredo.app` へ変更されました
  - シグナリング URL も変更となります。Sora Labo サイトをご確認のうえ変更をお願いします

- Canary 版 Sora クラスターの提供を開始しました
  - 開発中のスナップショット版の Sora です
  - 3 台でクラスターを構成しているため、クラスターの最大同時接続数は 300 となります

- Stable 版 Sora クラスターの提供を開始しました
  - 正式リリース版の Sora です
  - 2 台でクラスターを構成しているため、クラスターの最大同時接続数は 200 となります

- 利用可能時間を直近 7 日間 100 分から直近 30 日間 1000 分に変更しました
- 制限時の最大接続時間を 10 分から 60 分へ変更しました
- 制限解除時の最大接続時間を無制限へ変更しました
