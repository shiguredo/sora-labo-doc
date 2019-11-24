# WebRTC SFU Testing Service Sora Labo ドキュメント

これは時雨堂が提供している [WebRTC SFU Testing Service Sora Labo](https://sora-labo.shiguredo.jp/) のドキュメントです。

## Discord

なにか不明点などある場合はこちらでどうぞ。

https://discord.gg/k68nkRR

## Sora Labo で利用可能な SDK やクライアント、ライブラリ

- [WebRTC SFU Sora JavaScript SDK](https://github.com/shiguredo/sora-js-sdk)
    - [Sora JavaScript SDK ドキュメント](https://sora.shiguredo.jp/js-sdk-doc/)
- [WebRTC SFU Sora iOS SDK](https://github.com/shiguredo/sora-ios-sdk)
    - [Sora iOS SDK ドキュメント](https://sora.shiguredo.jp/ios-sdk-doc/)
    - [WebRTC SFU Sora iOS SDK クイックスタート](https://github.com/shiguredo/sora-ios-sdk-quickstart)
    - [WebRTC SFU Sora iOS SDK サンプル集](https://github.com/shiguredo/sora-ios-sdk-samples)
- [WebRTC SFU Sora Android SDK](https://github.com/shiguredo/sora-android-sdk)
    - [Sora Android SDK ドキュメント](https://sora.shiguredo.jp/android-sdk-doc/)
    - [WebRTC SFU Sora Android SDK クイックスタート](https://github.com/shiguredo/sora-android-sdk-quickstart)
    - [WebRTC SFU Sora Android SDK サンプル集](https://github.com/shiguredo/sora-android-sdk-samples)
- [WebRTC SFU Sora Unity SDK](https://github.com/shiguredo/sora-unity-sdk)
    - [WebRTC SFU Sora Unity SDK サンプル集](https://github.com/shiguredo/sora-unity-sdk-samples)
- [WebRTC Native Client Momo](https://github.com/shiguredo/momo)
- [React Native 用 WebRTC ライブラリ](https://github.com/shiguredo/react-native-webrtc-kit)
    - https://sora.shiguredo.jp/react-native-webrtc-kit-doc/
- [pixiv/webrtc](https://github.com/pixiv/webrtc/blob/branch-heads/pixiv-m77/README.pixiv.md)
    - [WebRTC ♥ \.NET ー WebRTCの\.NETバインディング \- pixiv inside](https://inside.pixiv.blog/nekomanma/7920)

## QA

- Sora Labo は無料ですか？
    - 無料で利用可能です
- Sora Labo は商用目的で利用可能ですか？
    - 商用目的では利用できません
- Sora Labo は法人で利用できますか？
    - [法人での利用は申請をお願いします](https://gist.github.com/voluntas/99bfcefc3b63f481941ae91584916a79#id23)
- Sora Labo はアカデミックで利用可能ですか？
    - [アカデミックでの利用は申請をお願いします](https://gist.github.com/voluntas/99bfcefc3b63f481941ae91584916a79#id23)
- Sora Labo は転送量制限がありますか？
    - 制限はありません
- Sora Labo は同時接続制限がありますか？
    - あります
    - 片方向の最大同時接続数は 10 までです
    - 双方向の最大同時接続数は 5 までです
- Sora Labo は映像ビットレートの制限はありますか？
    - 当面は制限を設けないつもりです
- Sora Labo の接続時間制限はありますか？
    - 当面は制限を設けないつもりです
- Sora Labo は TURN-TCP や TURN-TLS を提供していますか？
    - 提供しています
    - TURN-TCP は 3478 ポート
    - TURN-TLS は 443 ポート
- Sora Labo の SLA はいくつですか？
    - 保証はありません
- Sora Labo はウェブフック機能を提供しますか？
    - 提供しません
- Sora Labo は Sora の HTTP API を提供しますか？
    - 提供しません
- Sora Labo はサポートを提供しますか？
    - 提供しません
- メンテナンス告知は行いますか？
    - Discord にて行います

不明点は Discord にてお問い合わせ下さい。

## 今後

「うまくいかない環境」を気軽に利用できるような仕組みを追加していく予定です。
うまくいかない環境というのは、
帯域が細かったり、パケロスが多かったり、TLS しか通らなかったりと理不尽なネットワーク環境です。

### TURN-TCP 利用強制機能

指定した接続が TURN-TCP を利用するように強制可能にする機能です。

### TURN-TLS 利用強制機能

指定した接続が TURN-TLS を利用するように強制可能にする機能です。

### 帯域制限機能

指定した接続の帯域を制限する機能です。

### パケロス機能

指定した接続のパケロスの割合を指定する機能です。

## 古いドキュメント

ドキュメントに移行予定です。

[WebRTC SFU Testing Service Sora Labo の使い方](https://gist.github.com/voluntas/fb4cdc1626c941443e41a5a39050eb33)
