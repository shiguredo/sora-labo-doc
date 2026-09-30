# Sora MoQ について

Sora Labo では Sora の Media over QUIC 機能である Sora MoQ を検証することができます。

2026 年 10 月現時点では Sora MoQ は以下のライブラリとの接続検証を行っています

まずは [MOQT DevTools](https://moqt-devtools.shiguredo.app/) でお試しください。

## 注意

Media over QUIC は主な仕様は全て RFC ドラフトです。 Sora MoQ では最新版の RFC ドラフトへの追従を積極的に行います。そのため破壊的変更が前提となります。

またブラウザ毎に WebTransport や WebCodecs 対応状況も異なります。Sora MoQ では Chrome と Safari の二つのブラウザをメインターゲットとしています。 Edge と Firefox やそれ以外のブラウザに対しては優先度を一つ落としています。

## 対応 RFC ドラフト

### Media over QUIC

- [draft\-ietf\-moq\-transport\-21](https://datatracker.ietf.org/doc/html/draft-ietf-moq-transport-21)
- [draft\-ietf\-moq\-loc\-04](https://datatracker.ietf.org/doc/html/draft-ietf-moq-loc-04)
- [draft\-ietf\-moq\-msf\-01](https://datatracker.ietf.org/doc/html/draft-ietf-moq-msf-01)
- [draft\-ietf\-moq\-c4m\-01](https://datatracker.ietf.org/doc/html/draft-ietf-moq-c4m-01)

### WebTransport

- [draft\-ietf\-webtrans\-overview\-13](https://datatracker.ietf.org/doc/html/draft-ietf-webtrans-overview-13)
- [draft\-ietf\-webtrans\-http3\-16](https://datatracker.ietf.org/doc/html/draft-ietf-webtrans-http3-16)
- [draft\-ietf\-webtrans\-http2\-15](https://datatracker.ietf.org/doc/html/draft-ietf-webtrans-http2-15)

## Namespace

MoQ では Sora の ChannelId のような仕組みを Namepsace という仕組みを利用します。 Namespace はバイナリの配列です。 Sora Labo の Sora MoQ ではユニークな ID である GitHub-ID を採用しています。

`["<GitHub-ID>", <好きな文字列(128 文字)>]`

## 認証方式

Sora Labo の Sora MoQ では認証方式に C4M (CAT 4 MOQT) を採用しています。

利用できるクレーム内容は 2026 年 10 月現時点では時点では固定しています。

- SETUP
- PUBLISH/SUBSCRIBE: catalog
- PUBLISH/SUBSCRIBE: audio
- PUBLISH/SUBSCRIBE/FETCH/REQUEST_UPDATE: video
- PUBLISH/SUBSCRIBE: events

trackname も固定しています。

## 時雨堂の MOQT ライブラリ

### [shiguredo/moqt-js](https://github.com/shiguredo/moqt-js)

WebTransport API や WebCodecs API を利用する高レベル API と MOQT を直接利用する低レベル (Sans I/O) API を提供しているライブラリです。

### [shiguredo/moqt-rs](https://github.com/shiguredo/moqt-rs)

MOQT の Sans I/O ライブラリです。サンプルに moq-pub / moq-sub を用意しています。

### [shiguredo/moqt-py](https://github.com/shiguredo/moqt-py)

webtransport-py (nghttp2 / nghtcp2/ nghttp3) をトランスポートに採用しています。
その上に moqt-rs を PyO3 経由で利用しているライブラリです。そのため MOQT の挙動は moqt-rs と同じです。

## Sora MoQ SDK

現在提供準備中です。

JavaScript / Rust / Python / Swfit / Kotlin を提供予定です。

- Swift / Kotlin は QUIC のみ利用できます
  - Swift と kotlin は moqt-rs を採用し、QUIC には AWS の s2n-quic を採用しています
- JavaScript は WebTransport のみ利用できます
- Rust / Python は QUIC と WebTransport が利用できます
