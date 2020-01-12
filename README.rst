######################
Sora Labo ドキュメント
######################

これは時雨堂が提供している `Sora Labo <https://sora-labo.shiguredo.jp/>`_ のドキュメントです。

QA
==

- Sora Labo は無料ですか？

  - 無料で利用可能です
- Sora Labo は商用目的で利用可能ですか？

  - 商用目的では利用できません
- Sora Labo をサービスに利用可能ですか？

  - Sora Labo は検証目的以外では利用できません
- Sora Labo は法人や個人事業主で利用できますか？

  - 法人や個人事業主での利用は申請が必須です
- Sora Labo はアカデミックで利用可能ですか？

  - アカデミックでの利用は申請が必須です
- Sora Labo は長時間接続しても問題ありませんか？

  - 長時間接続の利用は申請をお願いします
- Sora Labo は転送量制限がありますか？

  - 制限はありません
- Sora Labo は同時接続制限がありますか？

  - あります
  - 片方向の最大同時接続数は 10 までです
  - 双方向の最大同時接続数は 5 までです
- Sora Labo は映像ビットレートの制限はありますか？

  - 制限はありません
- Sora Labo の接続時間制限はありますか？

  - 60 分間で切断されます
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
- SDK のサポートは提供しますか？

  - 提供しません
- メンテナンス告知は行いますか？

  - Discord にて行います

Discord
=======

なにか不明点などある場合は Discord でどうぞ。

https://discord.gg/k68nkRR

制限
====

- Sora Labo は Sora SDK 以外での利用を想定していません
- サービス全体での最大同時接続数は 600 です
- 1 チャネルに接続できる最大の数は 10 です
- 1 チャネルの連続接続時間は 60 分です
- ビットレートの制限現時点ではありません
- Sora の HTTP API は利用できません
- Sora のウェブフック機能は利用できません

禁止
====

- 商用目的での利用
- 申請無しでの法人やアカデミックでの利用
- 申請無しでの長時間接続

申請
====

個人以外の法人や個人事業主やアカデミックで利用する場合は申請をお願いします。
また、長時間接続を行いたい場合も申請をお願いします。

下記の必要事項を記入の上 sora-labo at shiguredo.jp までお送りください。

法人/個人事業主
---------------

- 社名
- 住所
- 電話番号
- 部署名 (あれば)
- 担当者（フルネーム)
- 担当者のメールアドレス
- 利用する GitHub アカウント
- 利用期間 (YYYY/MM/DD ~ YYYY/MM/DD)
- 何に利用するか (140 文字以内で)

アカデミック
------------------

- 学校名
- 研究室名 (あれば)
- 担当者（フルネーム)
- 担当者のメールアドレス
- 利用する GitHub アカウント
- 期間
- 何に利用するか (140 文字以内で)

長時間接続
---------------------

- お名前（フルネーム)
- メールアドレス
- 利用する GitHub アカウント
- 期間
- 何に利用するか (140 文字以内で)


利用可能な SDK やクライアント、ライブラリ
=========================================

**WebRTC SFU Sora SDK のみ動作確認しています**

- `WebRTC SFU Sora JavaScript SDK <https://github.com/shiguredo/sora-js-sdk>`_

  - `Sora JavaScript SDK ドキュメント <https://sora.shiguredo.jp/js-sdk-doc/>`_
- `WebRTC SFU Sora iOS SDK <https://github.com/shiguredo/sora-ios-sdk>`_

  - `Sora iOS SDK ドキュメント <https://sora.shiguredo.jp/ios-sdk-doc/>`_
  - `WebRTC SFU Sora iOS SDK クイックスタート <https://github.com/shiguredo/sora-ios-sdk-quickstart>`_
  - `WebRTC SFU Sora iOS SDK サンプル集 <https://github.com/shiguredo/sora-ios-sdk-samples>`_
- `WebRTC SFU Sora Android SDK <https://github.com/shiguredo/sora-android-sdk>`_

  - `Sora Android SDK ドキュメント <https://sora.shiguredo.jp/android-sdk-doc/>`_
  - `WebRTC SFU Sora Android SDK クイックスタート <https://github.com/shiguredo/sora-android-sdk-quickstart>`_
  - `WebRTC SFU Sora Android SDK サンプル集 <https://github.com/shiguredo/sora-android-sdk-samples>`_
- `WebRTC SFU Sora Unity SDK <https://github.com/shiguredo/sora-unity-sdk>`_

  - `WebRTC SFU Sora Unity SDK サンプル集 <https://github.com/shiguredo/sora-unity-sdk-samples>`_
- `WebRTC Native Client Momo <https://github.com/shiguredo/momo>`_
- `React Native 用 WebRTC ライブラリ <https://github.com/shiguredo/react-native-webrtc-kit>`_

  - `React Native WebRTC Kit ドキュメント <https://sora.shiguredo.jp/react-native-webrtc-kit-doc/>`_
- `pixiv/webrtc <https://github.com/pixiv/webrtc/blob/branch-heads/pixiv-m77/README.pixiv.md>`_

  - `WebRTC ♥ \.NET ー WebRTCの\.NETバインディング \- pixiv inside <https://inside.pixiv.blog/nekomanma/7920>`_

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
        sora --auto wss://sora-labo.shiguredo.jp/signaling shiguredo@sora-labo-test \
        --role sendrecv --multistream --video-codec VP8 --video-bitrate 2500 \
        --metadata '{"signaling_key": "jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa"}'

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

シグナリングキーが ``jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa`` の場合

.. code-block:: javascript

    {"signaling_key": "jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa"}


Sora Labo のアカウントを削除する
--------------------------------

もし今後、 Sora Labo を利用しないのであればアカウントを削除できます。

サインインした一番したにアカウントの削除があります。


検証向け機能
============

録画機能
--------

接続したチャネルで録画が有効になる機能です。

metadata 指定時に ``{"recording": true}`` を指定して下さい。

- 録画は 10 分だけ有効になります
- そのチャネルにつないでいる role: upstream の配信全てが録画されます
- 10 分経過したことには気づけません
- そのチャネルの接続が 0 になると録画が終了します
- 録画したファイルはダッシュボードで視聴またはダウンロードできます
- 録画したファイルは録画完了時から 30 分経過するとアクセスできなくなります
- 録画したファイルは 30 分単位でのバッチで録画完了時から 30 分経過していると自動で削除されます

  - 自動削除はまだ実装していません、そのうちやります
- シングルストリーム送信とマルチストリーム送受信で試せます

  - スポットライトには非対応です

.. image:: https://i.gyazo.com/f23f2c45fda9a727eddd74ece2946509.png

.. image:: https://i.gyazo.com/42fb6ea6a76dd0d958332f0a1186aa5c.png

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

トークン機能
---------------

24 時間だけ利用可能なトークンを発行する機能です。シグナリングキーの代わりに利用できます。

帯域制限機能
----------------

指定した接続の帯域を制限する機能です。

パケロス機能
----------------

指定した接続のパケロスの割合を指定する機能です。

