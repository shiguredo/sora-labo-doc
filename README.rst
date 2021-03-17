######################
Sora Labo ドキュメント
######################

これは時雨堂が提供している `Sora Labo <https://sora-labo.shiguredo.jp/>`_ のドキュメントです。
ご利用前にかならずご確認いただきます様、お願いいたします。

お知らせ
========

申請なしでの法人や個人事業主、アカデミックでの利用について
---------------------------------------------------------------

申請なしで法人や個人事業主、アカデミックでの利用が判明した場合、ご利用を停止させていただきます。

また、よほどの理由がない限り WebRTC SFU Sora のご提供もお断りさせて頂きます。ご了承ください。

Sora Labo で利用している Sora
-----------------------------

- 2021 年 6 月リリース予定の最新の開発版を利用しているため、製品版とは異なります
- 2021 年 5 月リリース予定の JIT を有効にした Erlang VM を利用しているため、製品版とは異なります

Sora 評価版について
-------------------

製品版と同等の機能が 1 ヶ月間無料で利用可能な評価版については以下をご確認ください。

https://sora.shiguredo.jp/support#sora-before

QA
==

- Sora Labo は無料で利用できますか？

  - 無料で利用できます。
- Sora Labo は商用目的で利用できますか？

  - 商用目的では利用できません。Sora Labo は Sora の検証以外の目的や用途では利用できません。
- Sora Labo をサービスに利用できますか？

  - 実際のサービスには利用できません。Sora Labo は Sora の検証以外の目的や用途では利用できません。
- Sora Labo は法人や個人事業主で利用できますか？

  - Sora の検証目的ではご利用いただけますが、法人や個人事業主での利用には **事前の申請が必要** です。必ず申請してください。
- Sora Labo はアカデミックで利用できますか？

  - Sora の検証目的ではご利用いただけますが、アカデミックでの利用には **事前の申請が必要** です。必ず申請してください。
- Sora Labo サービス全体での転送量制限がありますか？

  - サービス全体で 10TB の転送制限があります。極端に伝送量の多い配信をされると他の利用者に影響しますので、ご配慮をお願いします。

- Sora Labo サービス全体での帯域制限はありますか？

  - 制限はありません。
- Sora Labo は同時接続数の制限がありますか？

  - 1 チャネルあたりの片方向の最大同時接続数は 10 です。
  - 1 チャネルあたりの双方向の最大同時接続数は 5 です。
- Sora Labo は映像ビットレートの制限はありますか？

  - 最大 5Mbps です。
- Sora Labo の接続時間制限はありますか？

  - 10 分です。10 分経過すると接続は切断されます。
  - 個人の方でも利用申請をいただければ、最大 60 分まで接続できるようになります。
- Sora Labo は TURN-TCP や TURN-TLS を提供していますか？

  - 提供しています。
  - TURN-TCP は 443 ポートです。
  - TURN-TLS は 443 ポートです。
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
- メンテナンス告知は行いますか？

  - 時雨堂の営業時間である平日の 10:00-17:00 の間にメンテナンスを行う場合のみ Discord にて通知します。
  - それ以外は事前の告知なく行うことがあります。
- Sora Labo の Sora のバージョンはいくつですか？

  - 今後リリースを予定している最新の Sora の開発版です。製品版とは異なります。
- 認証エラー理由に ``PLEASE-CONTACT-US`` が出ました

  - いずれかの制限または禁止項目に当てはまっている可能性があります。Discord にてご連絡ください。
- 認証エラー理由に ``CONNECTION-LIMIT`` が出ました

  - いずれかの制限または禁止項目に当てはまっている可能性があります。Discord にてご連絡ください。

Discord
=======

サポート
  しません
アドバイス
  します
フィードバック
  歓迎します

https://discord.gg/k68nkRR

制限
====

- 申請なしでの 1 接続の連続接続時間は 10 分です

  - **個人の方で 1 接続の連続接続時間として 10 分以上利用したい場合は申請をお願いします**
  - 申請頂いた場合の 1 接続の連続接続時間は 60 分になります
- 申請なしでの最大合計接続時間は 100 分です

  - **個人の方で合計接続時間として 100 分以上利用したい場合は申請をお願いします**
  - 申請頂いた場合は期限は特になく、合計接続時間は無制限になります
- Sora の **HTTP API は利用できません**
- Sora の **ウェブフック機能は利用できません**
- Sora Labo は Sora SDK 以外での利用を想定していません
- サービス全体での最大同時接続数は 600 です
- 申請なしでの 1 チャネルに接続できる最大の数は 10 です
- ビットレートの最大値は 15 Mbps です

禁止
====

- 商用目的での利用
- 同業他社の利用
- 負荷試験ツールの利用
- 申請無しでの個人の範囲以外での利用
- 申請無しでの法人/個人事業主やアカデミックでの利用
- すでに登録済みのアカウントとは別に別アカウントを作成しての利用
- Sora Labo のベンチマーク結果を第三者へ公開すること

申請フロー
===================

**申請は日本国内利用のみです**

個人以外の法人や個人事業主やアカデミックで利用する場合は申請をお願いします。
また、長時間接続/長期間利用の場合も申請をお願いします。

下記の必要事項を記入の上 sora-labo at shiguredo.jp までお送りください。
(このメールアドレスへの特定電子メールの送信を拒否いたします)

頂いた申請に問題がなければ **利用許可メール** をお送りします。
利用許可メールを確認後、利用開始をお願いいたします。

個人以外の方で申請した場合の利用期間は **最長 1 ヶ月** で、延長は行いません。
ただし、個人での利用の場合は利用期間に期限は設けておりません。

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
- 利用期間 (YYYY/MM/DD ~ YYYY/MM/DD)
- 何に利用するか (140 文字以内で)

個人
----

**個人の方は利用期間は不要です**

- お名前（フルネーム)
- 住所
- 電話番号
- メールアドレス
- 利用する GitHub アカウント
- 何に利用するかを、かなり具体的にお願いします、特に Sora Labo でなければならない理由を明確にお願いします。


Sora のライセンスをご契約頂いているお客様
--------------------------------------------

開発環境用ライセンスのご利用をお願いいたします。

もしリリース前の新機能を検証したい場合は、サポートまでご連絡ください。

商用利用について
=========================================

Sora Labo は商用利用は許可していませんので、商用利用したい場合は 2 つ手段があります。

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

サンプルを利用する
-------------------

ダッシュボードページにシグナリングキーを埋め込んであるサンプルを用意してありますので、気軽に確認できます。

.. image:: https://i.gyazo.com/28ab069fed1aa2fb638fad58b1b6754a.png

.. image:: https://i.gyazo.com/02876da53264379d8592e8b2383c657f.png

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

  - ここでは GitHub Username を ``shiguredo`` としています
- 自分のシグナリングキーを --metadata で指定してください

  - ここではシグナリグキーを ``jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa`` としています

GitHub Username が shiguredo で、 チャネル ID が sora-labo-test の場合::

    ./momo --resolution VGA --no-audio --port 0 \
        sora --auto wss://sora-labo.shiguredo.jp/signaling shiguredo@sora-labo \
        --role sendonly --multistream true --video-codec-type VP8 --video-bit-rate 2500 \
        --metadata '{"signaling_key": "jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa"}'

Sora Labo のシングルストリーム受信を開いて接続してみてください。その際にコーデックを合わせるのを忘れないでください。

.. image:: https://i.gyazo.com/6665d90f7e241ae21c5c525a965ce178.png

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

帯域制限機能
----------------

指定した接続の帯域を制限する機能です。

パケロス機能
----------------

指定した接続のパケロスの割合を指定する機能です。
