# Sora iOS SDK を利用する

`shiguredo/sora-ios-sdk: WebRTC SFU Sora iOS SDK <https://github.com/shiguredo/sora-ios-sdk>`\_

Sora iOS SDK のクイックスタートまたはサンプル集を利用して Sora Labo に接続できます。

- [WebRTC SFU Sora iOS SDK クイックスタート](https://github.com/shiguredo/sora-ios-sdk-quickstart)
- [WebRTC SFU Sora iOS SDK サンプル集](https://github.com/shiguredo/sora-ios-sdk-samples)

## 1. Environment.swift の作成

クイックスタートまたはサンプル集の `Environment.example.swift` を元に `Environment.swift` を作成します。

### Environment.swift の作成

```bash
$ cp Environment.example.swift Environment.swift
```

## 2. 接続情報の設定

`Environment.swift` に Sora Labo への接続情報を設定します。

- `signaling_endpoint` に Sora Labo の Sora シグナリング URLs を全て指定してください
- `channel_id` に `<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>` を指定してください
  - ここでは GitHub Username を `shiguredo` としています
  - ここでは GitHub ID を `0` としています
- `signalingConnectMetadata` に自分のアクセストークンを指定してください
  - ここではアクセストークンを `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is` としています

### Environment.swift への設定例

```swift
// 接続するサーバーのシグナリング URL
static let urls = [URL(string: "wss://0001.canary.sora-labo.shiguredo.app/signaling")!,
                   URL(string: "wss://0002.canary.sora-labo.shiguredo.app/signaling")!,
                   URL(string: "wss://0003.canary.sora-labo.shiguredo.app/signaling")!]

// チャネル ID
static let channelId = "shiguredo_0_sora"

// metadata
static let signalingConnectMetadata = ["access_token" : "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is"]
```
