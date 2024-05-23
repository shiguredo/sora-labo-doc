# お知らせ

## OBS (WebRTC/WHEP) 対応

- 日時: 2023-03-26

OBS (WebRTC/WHEP) のソースに対応しました。以下の URL で利用できます。
OBS の `Bearer Token` にはアクセストークンを指定してください。

`https://canary.sora-labo.shiguredo.app/whep/{channel-id}`

## クラスターリレー機能

- 日時: 2024-03-19

Sora Canary 版にてクラスターリレー機能を有効にしました。
どの Sora ノードに繫いでも同一チャネルに接続することができます。

## ロードバランサーで WebSocket が突然切断される問題への対応

- 日時: 2023-07-20

シグナリング URL の一本化に利用しているロードバランサー (以下 LB) を経由した場合、 WebSocket が突然切断される問題があることがわかりました。
この問題をすぐに解決することは難しいため、 Sora Labo の Canary 版 Sora のシグナリング URL は LB を利用することを停止しました。そのため Canary 版 Sora のシグナリング URL が変更になります。

```none
(変更前) wss://canary.sora-labo.shiguredo.app/signaling
↓
(変更後) wss://<node-id>.canary.sora-labo.shiguredo.app/signaling
```

- `<node-id>` の箇所は "0001" などの文字列になります

OBS (WebRTC) は WebSocket を利用しないため、以前通り LB を指定する方式にしています。

## OBS (WebRTC/WHIP) 対応

- 日時: 2023-04-17

OBS (WebRTC/WHIP) での配信に対応しました。以下の URL で利用できます。
OBS の `Bearer Token` にはアクセストークンを指定してください。

`https://canary.sora-labo.shiguredo.app/whip/{channel-id}`

## チャネル ID の方式変更

- 日時: 2023-04-17

チャネル ID の方式を変更しました。

いままでは `<好きな文字列>@<github-username>#<github-id>` でしたが、これを `<github-username>_<github-id>_<好きな文字列>` に変更します。

- OBS (WebRTC/WHIP) 機能に伴い URL にチャネル ID を指定する必要が出てきたため `#` と `@` を `_` に変更します
- 固有値を先頭に持ってくるため GitHub ユーザ名と ID を先頭に持ってきます
- \_ は GitHub ユーザ名には利用できないため、採用しました
- GitHub ID とは GitHub アカウントに紐付けられている変更できないユニークな数値です
- GitHub Username とは GitHub アカウント名で、自由に変更が可能です

例えば GitHub ユーザ名が shiguredo で GitHub ID が 0 でチャネル名が sora の場合は `shiguredo_0_sora` となります。

## シグナリング URL 一本化

- 日時: 2023-04-10

Sora Labo の Canary 版 Sora のシグナリング URL を一本化しました。

`wss://canary.sora-labo.shiguredo.app/signaling`

## 古いお知らせ

[古いお知らせ](./OLD_NEWS.md)
