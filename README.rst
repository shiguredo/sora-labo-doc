######################
Sora Labo ドキュメント
######################

これは時雨堂が提供している `Sora Labo <https://sora-labo.shiguredo.jp/>`_ のドキュメントです。
ご利用前にかならずご確認いただきます様、お願いいたします。

お知らせ
========

サンプル廃止と Sora DevTools 採用
---------------------------------

サンプルを廃止して https://sora-devtools.shiguredo.jp/ を利用するようにしました。

DataChannel メッセージング利用
-------------------------------

2021 年 9 月 20 日より適用

Sora Labo では DataChannel を利用したリアルタイムメッセージング機能を一足先に利用可能です。

DataChannel メッセージングには Sora Unity SDK 安定版と Sora JavaScript SDK 開発版が対応しています。

利用に申請などは不要です。

ただがっつり検証したい方に向けて、
検証向けに制限を外す事が可能ですので、
Discord の #sora-datachannel でご相談ください。

利用ルールの変更
---------------------------------------------------------------

2021 年 7 月 7 日より適用

個人での利用範囲になりますが、
時雨堂が管理している Sora Labo / Sora 関連の OSS の Discord にて、
貢献者ロールを保持していて、かつサーバーブーストを行ってくれている方に、制限解除を行います。

申請は Discord の #sora-labo にてお願いします。 GitHub アカウントも合わせてお知らせください。

利用ルールの変更
---------------------------------------------------------------

2021 年 4 月 5 日より適用

- 法人、個人事業主、アカデミックでの利用が申請が不要になりました
- 法人が利用制限を解除するために申請が必要になりました
- 個人事業主やアカデミックでの制限解除依頼を廃止し、法人のみとしました

Sora Labo で利用している Sora
-----------------------------

- 2021 年 12 月リリース予定の最新の開発版を利用しているため、製品版とは異なります

Sora 評価版について
-------------------

製品版と同等の機能が 1 ヶ月間無料で利用可能な評価版については以下をご確認ください。

https://sora.shiguredo.jp/support#sora-before

QA
==

- Sora Labo は無料で利用できますか？

  - 無料で利用できます
- Sora Labo は商用目的で利用できますか？

  - 商用目的では利用できません。Sora Labo は Sora の検証以外の目的や用途では利用できません
- Sora Labo をサービスに利用できますか？

  - 実際のサービスには利用できません。Sora Labo は Sora の検証以外の目的や用途では利用できません
- Sora Labo は法人で利用できますか？

  - 利用可能ですが、Sora の検証目的でのみご利用いただけます
- Sora Labo は個人事業主やアカデミックで利用できますか？

  - 利用可能ですが、Sora の検証目的でのみご利用いただけます、ただし制限解除依頼はできませんので評価版をご検討ください
- Sora Labo サービス全体での転送量制限がありますか？

  - サービス全体で 10TB の転送制限があります
  - 極端に伝送量の多い配信をされると他の利用者に影響しますので、ご配慮をお願いします
- Sora Labo サービス全体での帯域制限はありますか？

  - 制限はありません
- Sora Labo は同時接続数の制限がありますか？

  - 1 チャネルあたりの最大同時接続数は 10 です
- Sora Labo は映像ビットレートの制限はありますか？

  - 最大 15Mbps です
- Sora Labo の合計接続時間制限はありますか？

  - 制限解除申請前は 100 分です
  - 制限解除申請後は無制限です
- Sora Labo の連続接続時間制限はありますか？

  - 制限申請前は 10 分です。10 分経過すると接続は切断されます
  - 制限申請後は 60 分です。60 分経過すると接続は切断されます
- Sora Labo は TURN-TCP や TURN-TLS を提供していますか？

  - 提供しています
  - TURN-TCP は 443 ポートです
  - TURN-TLS は 443 ポートです
- Sora Labo の SLA はいくつですか？

  - 保証はありません。
- Sora Labo はウェブフック機能を提供しますか？

  - 提供しません。
- Sora Labo は Sora の HTTP API を提供しますか？

  - 提供しません。
- Sora Labo はサポートを提供しますか？

  - 提供しません。
- Sora SDK のサポートは提供しますか？

  - 提供しません。
- 変更などの告知は行いますか？

  - Discord にて通知します
- メンテナンス告知は行いますか？

  - 時雨堂の営業時間である平日の 10:00-17:00 の間にメンテナンスを行う場合のみ Discord にて通知します
  - それ以外は事前の告知なく行うことがあります
- Sora Labo の Sora のバージョンはいくつですか？

  - 今後リリースを予定している最新の Sora の開発版です。製品版とは異なります
- 認証エラー理由に ``PLEASE-CONTACT-US`` が出ました

  - いずれかの制限または禁止項目に当てはまっている可能性があります。Discord にてご連絡ください
- 認証エラー理由に ``CONNECTION-LIMIT`` が出ました

  - 直近一週間以上の利用が 100 分を超えると利用できなくなります
  - 少し時間をおいてからご利用ください

Discord
=======

アナウンスなどは全て Discord を利用します。

:サポート: しません
:アドバイス: します
:フィードバック: 歓迎します

https://discord.gg/shiguredo

#sora-labo へどうぞ。

制限
====

- 制限解除申請なしでの 1 接続の連続接続時間は 10 分です

  - 制限解除した場合の 1 接続の連続接続時間は 60 分になります
- 制限解除申請なしでの最大合計接続時間は 100 分です

  - 制限解除した場合は合計接続時間は無制限になります
- Sora の **HTTP API は利用できません**
- Sora の **ウェブフック機能は利用できません**
- Sora Labo は Sora SDK 以外での利用を想定していません
- サービス全体での最大同時接続数は 600 です
- 1 チャネルに接続できる最大の数は 10 です
- ビットレートの最大値は 15 Mbps です

禁止
====

- 商用目的での利用
- 同業他社の利用
- 負荷試験ツールの利用
- すでに登録済みのアカウントとは別にアカウントを作成しての利用
- Sora Labo のベンチマーク結果を第三者へ公開すること

制限解除申請フロー
===================

**申請は日本国内利用のみです**

法人の方で利用制限を解除する場合は下記の必要事項を記入の上 sora-labo at shiguredo.jp までお送りください。
(このメールアドレスへの特定電子メールの送信を拒否いたします)

頂いた申請に問題がなければ **制限解除メール** をお送りします。

申請した場合の利用期間は **最長 2 週間** です。

法人
---------------

- 社名
- 住所
- 電話番号
- 部署名 (あれば)
- 担当者（フルネーム)
- 担当者のメールアドレス
- 利用する GitHub アカウント
- 利用開始日時 (YYYY/MM/DD)
- 何に利用するかを具体的に

Sora のライセンスをご契約頂いている法人
-------------------------------

開発環境用ライセンスのご利用をお願いいたします。

もしリリース前の新機能を検証したい場合は、サポートまでご連絡ください。

商用利用やアカデミック利用について
=========================================

Sora Labo は商用利用は許可しておりません、また個人事業主やアカデミックでの利用は制限解除に対応しておりませんので、以下をご検討ください。

- 時雨堂とライセンス契約をする

  - 自前で頑張りたい
- さくらインターネットさんの ImageFlux Live Stremaing を契約する

  - 運用全部任せたい

ImageFlux Live Streaming はマネージド Sora + HLS 変換サービスで、 Sora だけでも利用可能です。

利用可能な SDK やクライアント、ライブラリ
=========================================

- `WebRTC SFU Sora JavaScript SDK <https://github.com/shiguredo/sora-js-sdk>`_

  - `Sora JavaScript SDK ドキュメント <https://sora-js-sdk.shiguredo.jp//>`_
- `WebRTC SFU Sora iOS SDK <https://github.com/shiguredo/sora-ios-sdk>`_

  - `Sora iOS SDK ドキュメント <https://sora-ios-sdk.shiguredo.jp/>`_
  - `WebRTC SFU Sora iOS SDK クイックスタート <https://github.com/shiguredo/sora-ios-sdk-quickstart>`_
  - `WebRTC SFU Sora iOS SDK サンプル集 <https://github.com/shiguredo/sora-ios-sdk-samples>`_
- `WebRTC SFU Sora Android SDK <https://github.com/shiguredo/sora-android-sdk>`_

  - `Sora Android SDK ドキュメント <https://sora-android-sdk.shiguredo.jp/>`_
  - `WebRTC SFU Sora Android SDK クイックスタート <https://github.com/shiguredo/sora-android-sdk-quickstart>`_
  - `WebRTC SFU Sora Android SDK サンプル集 <https://github.com/shiguredo/sora-android-sdk-samples>`_
- `WebRTC SFU Sora Unity SDK <https://github.com/shiguredo/sora-unity-sdk>`_

  - `WebRTC SFU Sora Unity SDK サンプル集 <https://github.com/shiguredo/sora-unity-sdk-samples>`_
- `WebRTC Native Client Momo <https://github.com/shiguredo/momo>`_
- `React Native 用 WebRTC ライブラリ <https://github.com/react-native-webrtc-kit/react-native-webrtc-kit>`_

  - `React Native WebRTC Kit ドキュメント <https://react-native-webrtc-kit.shiguredo.jp/>`_
  - `React Native WebRTC Kit のサンプルアプリケーション <https://github.com/react-native-webrtc-kit/react-native-webrtc-kit-samples>`_

利用方法
========

Sora DevTools を利用する
------------------------

Sora DevTools という開発者ツールを https://sora-devtools.shiguredo.jp/ で公開しています。

ダッシュボードページに Sora DevTools をSora Labo 経由で利用できるように、
チャネル ID とシグナリングキーとシグナリング URL 埋め込んである URL を用意してあります。

.. image:: https://i.gyazo.com/94f6bdad62e94a9e7782c6f800dfa52f.png

.. image:: https://i.gyazo.com/a2b431ab75476e1011391aad6ca098ce.png

Sora JS SDK を利用する
------------------------

`shiguredo/sora-js-sdk: WebRTC SFU Sora JavaScript SDK <https://github.com/shiguredo/sora-js-sdk>`_

- チャネル ID を ``<自分の GitHub Username>@<好きな Room ID>`` のように指定してください
- 自分のシグナリングキーを metadata で指定してください

https://github.com/shiguredo/sora-js-sdk/blob/develop/example/multistream.html

双方向のサンプルの一部です。

.. code-block:: javascript

    const channelId = "shiguredo@sora-devtools";
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

  - ここでは GitHub Username を ``shiguredo`` としています
- 自分のシグナリングキーを --metadata で指定してください

  - ここではシグナリグキーを ``jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa`` としています

GitHub Username が shiguredo で、 チャネル ID が sora-devtools の場合::

    ./momo --resolution VGA --no-audio --port 0 \
        sora --auto wss://sora-labo.shiguredo.jp/signaling shiguredo@sora-devtools \
        --role sendonly --multistream true --video-codec-type VP8 --video-bit-rate 2500 \
        --metadata '{"signaling_key": "jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa"}'

Sora DevTools のマルチストリーム受信を開いて接続してみてください。

.. image:: https://i.gyazo.com/c0a807f72f7dad00084c3cd90970ca7b.png

AV1 を利用する
-------------------------------

Momo の最新版を利用することで AV1 を試すことが可能です。

`Sora と Momo で WebRTC の AV1 を試す <https://gist.github.com/voluntas/db82783b6a3f012977e6de641a16181e>`_

H.265 を利用する
-------------------------------

Safari Technology Preview 105 以降で設定で ``WebRTC H265 codec`` を有効にすることで H.265 を試すことが可能です。

`Sora で WebRTC の H.265 を試す <https://gist.github.com/voluntas/c271462d273285377593521dcb6dd6a5>`_

認証方法
========

チャネル ID を決める
--------------------

シグナリングキーを利用してチャネルに認証をかけてみます。

チャネル ID は GitHub アカウントのユーザ名を先頭に指定する必要があります。

shiguredo という GitHub ユーザ名であれば。 その後 @ を間に挟んでチャネル名を指定してください。

``チャンネル ID = {GitHubユーザ名}@{チャネル名}``

以下は shiguredo という Github ユーザ名に sora-devtools というチャネル名 を指定した例です

チャネル ID 例::

    shiguredo@sora-devtools

metadata に signaling_key を指定する
------------------------------------

Sora の SDK は metadata をシグナリング時に指定できます。metadata に ``signaling_key`` を指定して下さい。
これで利用可能になります。

シグナリングキーが ``jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa`` の場合

.. code-block:: javascript

    {"signaling_key": "jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa"}


Sora Labo のアカウントを削除する
--------------------------------

**アカウントは削除しますが、ログは削除しないためアカウントを削除したとしても利用時間はリセットされません**

もし今後、 Sora Labo を利用しないのであればアカウントを削除できます。

ダッシュボードの一番下にアカウントの削除があります。

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

以下は Sora DevTools 利用時の ``{"recording": true}`` 指定例です。

.. image:: https://i.gyazo.com/3c563b6a50d4085078a6fc753cdcb19d.png

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

