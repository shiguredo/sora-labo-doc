# Sora MoQ について

Sora Labo では Sora の Media over QUIC 機能である Sora MoQ を検証することができます。

2026 年 10 月現時点では Sora MoQ は以下のライブラリとの接続検証を行っています

まずは [MOQT DevTools](https://moqt-devtools.shiguredo.app/) でお試しください。

## 対応 RFC ドラフト

- [draft\-ietf\-moq\-transport\-21](https://datatracker.ietf.org/doc/html/draft-ietf-moq-transport-21)
- [draft\-ietf\-moq\-loc\-04](https://datatracker.ietf.org/doc/html/draft-ietf-moq-loc-04)
- [draft\-ietf\-moq\-msf\-01](https://datatracker.ietf.org/doc/html/draft-ietf-moq-msf-01)
- [draft\-ietf\-moq\-c4m\-01](https://datatracker.ietf.org/doc/html/draft-ietf-moq-c4m-01)

## 認証方式

C4M (CAT 4 MOQT) を採用していますが、利用できるクレーム内容は 2026 年 10 月現時点では時点では固定しています。

## 時雨堂の MOQT ライブラリ

### [shiguredo/moqt-js](https://github.com/shiguredo/moqt-js)

WebTransport API や WebCodecs API を利用する高レベル API と MOQT を直接利用する低レベル (Sans I/O) API を提供しているライブラリです。

### [shiguredo/moqt-rs](https://github.com/shiguredo/moqt-rs)

### [shiguredo/moqt-py](https://github.com/shiguredo/moqt-py)
