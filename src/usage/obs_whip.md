# OBS (WebRTC/WHIP) で配信する

## 手順

1. OBS をダウンロードする
1. OBS に WHIP エンドポイント URL を指定する
1. OBS の `Bearer Token` にアクセストークンを指定する

## OBS のダウンロード

OBS の WebRTC/WHIP は 30.0.0 から対応しています。

OBS は以下からダウンロード可能です。
https://obsproject.com/download

## OBS (WebRTC/WHIP) の設定

1. サービスで WHIP を選ぶ
1. サーバーに WHIP エンドポイントを指定する

- `https://canary.sora-labo.shiguredo.app/whip/{channel_id}`
- `channel_id` は `{github-username}_{github-id}_{channel_name}` です
  1. `Bearer Token` を指定する

[![Image from Gyazo](https://i.gyazo.com/40b0143574fcdc8f27e28102d3040608.png)](https://gyazo.com/40b0143574fcdc8f27e28102d3040608)

## OBS (WebRTC/WHIP) の設定例

以下は macOS の H.264 HWA を利用して 1080p 60fps で配信する際の設定例です。

[![Image from Gyazo](https://i.gyazo.com/2343be3113f6ee62bbd5854832095d7b.png)](https://gyazo.com/2343be3113f6ee62bbd5854832095d7b)

[![Image from Gyazo](https://i.gyazo.com/bde10b937928dd43b588c205ee8e0435.png)](https://gyazo.com/bde10b937928dd43b588c205ee8e0435)
