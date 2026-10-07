# Sora MoQ について

Sora Labo では Sora の Media over QUIC 機能である Sora MoQ を検証することができます。

2026 年 10 月現時点では Sora MoQ は以下のライブラリとの接続検証を行っています。

まずは [MOQT DevTools](https://moqt-devtools.shiguredo.app/) でお試しください。

## 注意

Media over QUIC は主な仕様は全て Internet-Draft (I-D) のため、仕様が固まっていません。Sora MoQ では最新版の RFC ドラフトへの追従を積極的に行うため、破壊的変更が前提となりますのでご注意ください。

WebTransport や WebCodecs の対応状況はブラウザによって異なります。Sora MoQ は Chrome と Safari の二つのブラウザをメインターゲットとしています。Edge、Firefox などその他のブラウザは優先度を下げています。

## 対応 Internet-Draft

### Media over QUIC Transport (MOQT)

- [draft-ietf-moq-transport-22](https://datatracker.ietf.org/doc/html/draft-ietf-moq-transport-22)
- [draft-ietf-moq-loc-04](https://datatracker.ietf.org/doc/html/draft-ietf-moq-loc-04)
- [draft-ietf-moq-msf-01](https://datatracker.ietf.org/doc/html/draft-ietf-moq-msf-01)
- [draft-ietf-moq-c4m-01](https://datatracker.ietf.org/doc/html/draft-ietf-moq-c4m-01)

### WebTransport

- [draft-ietf-webtrans-overview-13](https://datatracker.ietf.org/doc/html/draft-ietf-webtrans-overview-13)
- [draft-ietf-webtrans-http3-16](https://datatracker.ietf.org/doc/html/draft-ietf-webtrans-http3-16)
- [draft-ietf-webtrans-http2-15](https://datatracker.ietf.org/doc/html/draft-ietf-webtrans-http2-15)

## Namespace

MOQT では Sora のチャネル ID のような仕組みを `Namespace` と呼びます。Namespace はバイト列の並び (タプル) です。 Sora Labo の Sora MoQ ではユニークな ID である GitHub-ID をプレフィックスとして採用しています。

`["<GitHub ID>", "<チャネル名 (128 文字)>"]`

## 認可方式

Sora Labo の Sora MoQ では認可方式に C4M (CAT for MOQT) を採用しています。

利用できる アクション内容は 2026 年 10 月現時点では固定しています。

- SETUP
- PUBLISH / SUBSCRIBE: catalog
- PUBLISH / SUBSCRIBE: audio
- PUBLISH / SUBSCRIBE / FETCH / REQUEST_UPDATE: video
- PUBLISH / SUBSCRIBE: events

Track Name も音声は audio で映像は video と固定しています。events は MOQT-DevTools に合わせています。

C4M を利用する場合は、 MSF の URI フラグメントを利用します。

`moqt://sora-moq.sora-labo.shiguredo.app/#msf:<namespace>--catalog&c4m=<token>`

MOQT DevTools を利用する場合は、これを MOQT URI に指定してください。

## Sora Labo で Sora MoQ に接続する

### Sora MoQ のトークン署名鍵を生成する

Sora MoQ へ接続するためのトークン署名用の秘密鍵を生成します。

「sora-moq のトークン署名鍵」で「生成」ボタンをクリックすると、秘密鍵の生成とダウンロードが行えます。

ダウンロードした秘密鍵は自分でトークンを発行する場合に使用します。
この手順では Sora Labo 側で秘密鍵で署名したトークンを発行するため、ダウンロードした秘密鍵は使用しません。

[![Image from Gyazo](https://i.gyazo.com/f96f0e433f2c5a9d1ebb0fe9d3e075dd.png)](https://gyazo.com/f96f0e433f2c5a9d1ebb0fe9d3e075dd)

### トークンと MOQT URI を発行する

任意のチャネル名を入力して、Sora MoQ に接続するためのトークンと MOQT URI を発行します。

[![Image from Gyazo](https://i.gyazo.com/028f42bd433f1f772887d37ca9b3d62f.png)](https://gyazo.com/028f42bd433f1f772887d37ca9b3d62f)

MOQT-DevTools の URL をコピーしてブラウザで開きます。MOQT URI を設定済みの MOQT-DevTools が表示されます。

[![Image from Gyazo](https://i.gyazo.com/028f42bd433f1f772887d37ca9b3d62f.png)](https://gyazo.com/028f42bd433f1f772887d37ca9b3d62f)

### MOQT-DevTools から Sora MoQ に接続する

MOQT Devtools では設定された MOQT URI やトークンの内容が確認できます。

[![Image from Gyazo](https://i.gyazo.com/01404fb31ccfb1dd3ffe8e82547eadc2.png)](https://gyazo.com/01404fb31ccfb1dd3ffe8e82547eadc2)

Sora MoQ に接続して映像の配信と視聴が行えます。

[![Image from Gyazo](https://i.gyazo.com/be355d58e03f7ae7aed7e010e0554e6e.png)](https://gyazo.com/be355d58e03f7ae7aed7e010e0554e6e)


## 時雨堂の MOQT ライブラリ

### shiguredo/moqt-js

[shiguredo/moqt-js](https://github.com/shiguredo/moqt-js)

WebTransport API や WebCodecs API を利用する高レベル API と MOQT を直接利用する低レベル API を提供しているライブラリです。

### shiguredo/moqt-rs

[shiguredo/moqt-rs](https://github.com/shiguredo/moqt-rs)

MOQT の Sans I/O ライブラリです。サンプルに `moq-pub` / `moq-sub` を用意しています。

### shiguredo/moqt-py

[shiguredo/moqt-py](https://github.com/shiguredo/moqt-py)

`webtransport-py` (nghttp2 / nghtcp2 / nghttp3) をトランスポートに採用しています。

その上に moqt-rs を PyO3 経由で利用しているライブラリです。そのため MOQT の挙動は moqt-rs と同じです。

## Sora MoQ SDK

現在提供準備中です。

JavaScript / Rust / Python / Swift / Kotlin を提供予定です。

- Swift / Kotlin は QUIC のみ利用できます
  - Swift と Kotlin は moqt-rs を採用し、QUIC には AWS の s2n-quic を採用しています
- JavaScript は WebTransport のみ利用できます
- Rust / Python は QUIC と WebTransport が利用できます
