# Sora Android SDK を利用する

[shiguredo/sora-android-sdk: WebRTC SFU Sora Android SDK](https://github.com/shiguredo/sora-android-sdk)

Sora Android SDK のクイックスタートまたはサンプル集を利用して Sora Labo に接続できます。

- [WebRTC SFU Sora Android SDK クイックスタート](https://github.com/shiguredo/sora-android-sdk-quickstart)
- [WebRTC SFU Sora Android SDK サンプル集](https://github.com/shiguredo/sora-android-sdk-samples)

## 1. gradle.properties の作成

クイックスタートまたはサンプル集のディレクトリトップの `gradle.properties.example` を元に `gradle.properties` を作成します。

### gradle.properties の作成

```bash
$ cp gradle.properties.example gradle.properties
```

## 2. 接続情報の設定

`gradle.properties` に Sora Labo への接続情報を設定します。

- `signaling_endpoint` に Sora Labo の Sora シグナリング URLs を設定してください。カンマ区切りですべてのシグナリング URL を指定をしてください。
- `channel_id` に `<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>` を指定してください
  - ここでは GitHub Username を `shiguredo` としています
  - ここでは GitHub ID を `0` としています
- `signaling_metadata` に自分のアクセストークンを指定してください
  - ここではアクセストークンを `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is` としています

### gradle.properties への設定例

```
# Setting Sora's signaling endpoint and channel_id
signaling_endpoint = wss://0001.canary.sora-labo.shiguredo.app/signaling, wss://0002.canary.sora-labo.shiguredo.app/signaling, wss://0003.canary.sora-labo.shiguredo.app/signaling
channel_id         = shiguredo_0_sora

# Setting Signaling Metadata.
# Quotes must be double escaped.
# e.g.) signaling_metadata = {\\"spam\\":\\"egg\\"}
# This setting is required. If you do not want to use it, set it to blank.
signaling_metadata = {\\"access_token\\":\\"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is\\"}
```
