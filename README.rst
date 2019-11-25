##################################################
WebRTC SFU Testing Service Sora Labo ドキュメント
##################################################

これは時雨堂が提供している `WebRTC SFU Testing Service Sora Labo <https://sora-labo.shiguredo.jp/>`_ のドキュメントです。

Discord
=======

なにか不明点などある場合はこちらでどうぞ。

https://discord.gg/k68nkRR

QA
==

- Sora Labo は無料ですか？

  - 無料で利用可能です
- Sora Labo は商用目的で利用可能ですか？

  - 商用目的では利用できません
- Sora Labo は法人で利用できますか？

  - `法人での利用は申請をお願いします <https://gist.github.com/voluntas/99bfcefc3b63f481941ae91584916a79#id23>`_
- Sora Labo はアカデミックで利用可能ですか？

  - `アカデミックでの利用は申請をお願いします <https://gist.github.com/voluntas/99bfcefc3b63f481941ae91584916a79#id23>`_
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

## Sora Labo で利用可能な SDK やクライアント、ライブラリ

- `WebRTC SFU Sora JavaScript SDK <https://github.com/shiguredo/sora-js-sdk`_

  - `Sora JavaScript SDK ドキュメント <https://sora.shiguredo.jp/js-sdk-doc/>`_
- `WebRTC SFU Sora iOS SDK <https://github.com/shiguredo/sora-ios-sdk>`_
    - `Sora iOS SDK ドキュメント <https://sora.shiguredo.jp/ios-sdk-doc/>`_
    - `WebRTC SFU Sora iOS SDK クイックスタート <https://github.com/shiguredo/sora-ios-sdk-quickstart>`_
    - `WebRTC SFU Sora iOS SDK サンプル集 <https://github.com/shiguredo/sora-ios-sdk-samples>`_
- `WebRTC SFU Sora Android SDK <https://github.com/shiguredo/sora-android-sdk>`_
    - `Sora Android SDK ドキュメント <https://sora.shiguredo.jp/android-sdk-doc/>`_
    - `WebRTC SFU Sora Android SDK クイックスタート](https://github.com/shiguredo/sora-android-sdk-quickstart>`_
    - `WebRTC SFU Sora Android SDK サンプル集](https://github.com/shiguredo/sora-android-sdk-samples>`_
- `WebRTC SFU Sora Unity SDK <https://github.com/shiguredo/sora-unity-sdk>`_
    - `WebRTC SFU Sora Unity SDK サンプル集 <https://github.com/shiguredo/sora-unity-sdk-samples>`_
- `WebRTC Native Client Momo <https://github.com/shiguredo/momo>`_
- `React Native 用 WebRTC ライブラリ <https://github.com/shiguredo/react-native-webrtc-kit>`_
    - https://sora.shiguredo.jp/react-native-webrtc-kit-doc/
- `pixiv/webrtc <https://github.com/pixiv/webrtc/blob/branch-heads/pixiv-m77/README.pixiv.md>`_
    - `WebRTC ♥ \.NET ー WebRTCの\.NETバインディング \- pixiv inside <https://inside.pixiv.blog/nekomanma/7920>`_

認証方法
========

チャネル ID を決める
--------------------

シグナリングキーを利用してチャネルに認証をかけてみます。

まずチャネル ID は GitHub アカウントの Username を先頭に指定する必要があります。

shiguredo という GitHub Username であれば。 その後 @ を間に挟んでチャネル ID を指定してください。

以下は sora-labo-test というチャネル ID に shiguredo という Github Username を指定した例です

チャネル ID 例::

    shiguredo@sora-labo-test

metadata に signaling_key を指定する
------------------------------------

Sora の SDK は metadata をシグナリング時に指定できます。metadata に ``signaling_key`` を指定して下さい。
これで利用可能になります。

::

    {"signaling_key": "<ここにシグナリングキーを指定する>"}


Sora Labo のアカウントを削除する
--------------------------------

もし今後、 Sora Labo を利用しないのであればアカウントを削除できます。

サインインした一番したにアカウントの削除があります。

利用方法
========

サンプルを利用する
-------------------

ダッシュボードページにシグナリングキーを埋め込んであるサンプルを用意してありますので、気軽に確認できます。

.. image:: https://i.gyazo.com/91bd05efd051a4a5a659df65a0472fb6.png

.. image:: https://i.gyazo.com/40ae6057883d6de85b453ccdb2b099f7.png

Sora JS SDK を利用する
------------------------

`shiguredo/sora-js-sdk: WebRTC SFU Sora JavaScript SDK <https://github.com/shiguredo/sora-js-sdk>`_

- チャネル ID を ``<自分の GitHub Username>@<好きな Room ID>`` のように指定してください
- 自分のシグナリングキーを metadata で指定してください

https://github.com/shiguredo/sora-js-sdk/blob/develop/example/multistream.html

双方向のサンプルの一部です。

.. code-block:: javascript

    const channelId = "shiguredo@sora-labo-js";
    const debug = false;
    const sora = connection("wss://sora-labo.shiguredo.jp/signaling", debug);
    const metadata = {
      signaling_key: "jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa"
    };
    const options = {
      multistream: true
    };
    const publisher = sora.publisher(channelId, metadata, options);

WebRTC Native Client Momo で Sora を利用する
--------------------------------------------

`shiguredo/momo: WebRTC Native Client Momo <https://github.com/shiguredo/momo>`_

Momo で Sora が利用できます。

- チャネル ID を ``<自分の GitHub Username>@<好きな Room ID>`` のように指定してください
- 自分のシグナリングキーを --metadata で指定してください

GitHub Username が shiguredo で、 チャネル ID が sora-labo-test の場合::

    ./momo --resolution VGA --no-audio --port 0 --use-sdl --show-me \
        sora --auto --video-codec VP8 --video-bitrate 2500 \
        wss://sora-labo.shiguredo.jp/signaling shiguredo@sora-labo-test --multistream \
        --metadata '{"signaling_key": "jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa"}'

機能
====

TURN-TCP 利用強制機能
---------------------

指定した接続が TURN-TCP を利用するように強制可能にする機能です。

metadata 指定時に ``{"turn_tcp_only": true}`` を指定して下さい。

TURN-TLS 利用強制機能
---------------------

指定した接続が TURN-TLS を利用するように強制可能にする機能です。

metadata 指定時に ``{"turn_tls_only": true}`` を指定して下さい。

今後
====

「うまくいかない環境」を気軽に利用できるような仕組みを追加していく予定です。
うまくいかない環境というのは、
帯域が細かったり、パケロスが多かったり、TLS しか通らなかったりと理不尽なネットワーク環境です。

帯域制限機能
----------------

指定した接続の帯域を制限する機能です。

パケロス機能
----------------

指定した接続のパケロスの割合を指定する機能です。
