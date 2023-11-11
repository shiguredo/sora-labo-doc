######################
Sora Labo ドキュメント
######################

これは時雨堂が提供している `Sora Labo <https://sora-labo.shiguredo.app/>`_ のドキュメントです。
ご利用前にかならずご確認いただきます様、お願いいたします。

ステータスページ
=====================

https://shiguredo.onlineornot.com

お知らせ
========

ロードバランサーで WebSocket が突然切断される問題への対応
------------------------------------------------------------------

:日時: 2023-07-20

シグナリング URL の一本化に利用しているロードバランサー (以下 LB) を経由した場合、 WebSocket が突然切断される問題があることがわかりました。
この問題をすぐに解決することは難しいため、 Sora Labo の Canary 版 Sora のシグナリング URL は LB を利用することを停止しました。そのため Canary 版 Sora のシグナリング URL が変更になります。

::

  (変更前) wss://canary.sora-labo.shiguredo.app/signaling
    ↓
  (変更後) wss://<node-id>.canary.sora-labo.shiguredo.app/signaling
  * <node-id> の箇所は "0001" などの文字列になります

OBS (WebRTC) は WebSocket を利用しないため、以前通り LB を指定する方式にしています。


OBS (WebRTC) 対応
------------------------------------------------------

:日時: 2023-04-17

OBS (WebRTC) での配信に対応しました。以下の URL で利用できます。
OBS の ``Bearer Token`` にはアクセストークンを指定してください。

::

    https://canary.sora-labo.shiguredo.app/whip/{channel-id}


チャネル ID の方式変更
------------------------------------------------------

:日時: 2023-04-17

チャネル ID の方式を変更しました。

いままでは ``<好きな文字列>@<github-username>#<github-id>`` でしたが、これを ``<github-username>_<github-id>_<好きな文字列>`` に変更します。

- OBS (WHIP) 機能に伴い URL にチャネル ID を指定する必要が出てきたため ``#`` と ``@`` を ``_`` に変更します
- 固有値を先頭に持ってくるため GitHub ユーザ名と ID を先頭に持ってきます
- _ は GitHub ユーザ名には利用できないため、採用しました
- GitHub ID とは GitHub アカウントに紐付けられている変更できないユニークな数値です
- GitHub Username とは GitHub アカウント名で、自由に変更が可能です

例えば GitHub ユーザ名が shiguredo で GitHub ID が 0 でチャネル名が sora の場合は ``shiguredo_0_sora`` となります。

シグナリング URL 一本化
------------------------------------------------------

:日時: 2023-04-10

Sora Labo の Canary 版 Sora のシグナリング URL を一本化しました。

::

    wss://canary.sora-labo.shiguredo.app/signaling


古いお知らせ
------------------

https://github.com/shiguredo/sora-labo-doc/blob/master/OLD_NEWS.rst

FAQ
===

**Sora Labo は検証目的以外での利用を禁止しています**

- Sora Labo は無料で利用できますか？

  - 無料で利用できます
- Sora Labo は商用目的で利用できますか？

  - 商用目的では利用できません
  - Sora Labo は Sora の検証以外の目的や用途では利用できません
  - Sora の本番環境用ライセンス、または Sora Cloud を契約してください
- Sora Labo を商用製品の開発に利用して良いですか？

  - 商用製品の開発では利用できません
  - Sora の開発環境用ライセンス、または Sora Cloud を契約してください
- Sora Labo を不特定多数向けに利用できますか？

  - 不特定多数向けのサービスには利用できません
  - Sora Labo は Sora の検証以外の目的や用途では利用できません
- Sora Labo は法人で利用できますか？

  - 利用可能ですが、Sora の検証目的でのみご利用いただけます
- Sora Labo は個人事業主で利用できますか？

  - 利用可能ですが、Sora の検証目的でのみご利用いただけます
- Sora Labo はアカデミックで利用できますか？

  - **利用できません**
  - Sora または Sora Cloud の利用を検討してください
- Sora Labo は日本以外からも利用できますか？

  - 利用できません
  - 頻繁に日本国外からのアクセスがある場合は BAN 対象とします
  - 何か問題が起きたときに海外の場合は対応ができないため、日本のみの利用に限定しています
- Sora Labo サービス全体での転送量制限がありますか？

  - あります。 Canary は 10 TB 程度、 Stable も同様です
  - 極端に転送量の多い配信をされると他の利用者に影響しますので、ご配慮をお願いします
- Sora Labo サービス全体での帯域制限はありますか？

  - 制限はありません
- Sora Labo は同時接続数の制限がありますか？

  - 1 チャネルあたりの最大同時接続数は 10 です
- Sora Labo は映像ビットレートの制限はありますか？

  - 最大 15 Mbps です
- Sora Labo の合計接続時間制限はありますか？

  - あります月 2000 分までです
  - 30 日経過すると復活します
  - 1/1 に 300 分利用すると、 1/31 に 300 分追加されます
- Sora Labo の連続接続時間制限はありますか？

  - 60 分です。60 分経過すると接続は切断されます
- Sora Labo の DataChannel メッセージング機能に制限はありますか？

  - 制限はありません
  - 極端に転送量の多い配信をされると他の利用者に影響しますので、ご配慮をお願いします
- Sora Labo は TURN-TCP や TURN-TLS を提供していますか？

  - 提供しています
  - TURN-TCP は 443 ポートです
  - TURN-TLS は 443 ポートです
- Sora Labo は IPv6 に対応していますか？

  - 対応しています
- Sora Labo の SLA はいくつですか？

  - SLA はありません
- Sora Labo はウェブフック機能を提供しますか？

  - 提供はしていません。Sora の評価版または Sora Cloud をご検討ください
- Sora Labo は Sora の HTTP API を提供しますか？

  - 提供はしていません。Sora の評価版または Sora Cloud をご検討ください
- Sora Labo はサポートを提供していますか？

  - 提供していません
- Sora SDK のサポートは提供していますか？

  - 提供していません
- 変更などの告知は行いますか？

  - すべて時雨堂 Discord の #sora-labo にて通知します
- メンテナンス告知は行いますか？

  - 時雨堂の営業時間である平日の 10:00-17:00 の間にメンテナンスを行う場合のみ Discord にて通知します
  - それ以外は事前の告知なく行います
- Sora Labo の Sora のバージョンはいくつですか？

  - Canary は今後リリースを予定している最新の Sora の開発版で、製品版とは異なります
  - Stable は現在リリースしている最新の Sora の正式版で、製品版と同じものです
- 認証エラー理由に ``PLEASE-CONTACT-US`` が出ました

  - いずれかの制限または禁止項目に当てはまっている可能性があります。Discord にてご連絡ください
- 認証エラー理由に ``CONNECTION-LIMIT`` が出ました

  - 直近 30 日間の利用が 2000 分を超えると利用できなくなります

Discord
=======

アナウンスなどの情報共有は全て Discord を利用しています。

:サポート: しません
:アドバイス: します
:フィードバック: 歓迎します

https://discord.gg/shiguredo

#sora-labo へどうぞ。

制限
====

- 最大合計接続時間は 2000 分です
- 1 接続の連続接続時間は 60 分です
- Sora の **HTTP API は提供していません**
- Sora の **ウェブフック機能は提供していません**
- Sora の HTTP API 機能を提供していないため **録画機能は提供していません**
- Sora Labo は Sora SDK と Momo 以外での利用を想定していません
- サービス全体での最大同時接続数は 1000 です
- 1 チャネルに接続できる最大の数は 10 です
- 1 接続のビットレートの最大値は 15 Mbps です

禁止
====

- アカデミックでの利用
- 商用目的での利用
- 商用製品開発目的での利用
- 同業他社の利用
- 負荷試験ツールの利用
- すでに登録済みのアカウントとは別にアカウントを作成しての利用
- Sora Labo のベンチマーク結果を第三者へ公開すること

商用利用やアカデミック利用について
=========================================

Sora Labo は商用利用は許可しておりませんので、以下をご検討ください。

- 時雨堂と `Sora Cloud <https://sora-cloud.shiguredo.jp/>`_ を契約をする

  - 運用全部任せたい
- 時雨堂と `WebRTC SFU Sora <https://sora.shiguredo.jp/>`_ を契約をする

  - 自前で頑張りたい
- さくらインターネットさんの ImageFlux Live Stremaing を契約する

  - HLS 変換したい

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
- `WebRTC SUF Sora C++ SDK <https://github.com/shiguredo/sora-cpp-sdk>`_

  - `WebRTC SFU Sora C++ SDK サンプル集 <https://github.com/shiguredo/sora-cpp-sdk-samples>`_
- `WebRTC SUF Sora Flutter SDK <https://github.com/shiguredo/sora-flutter-sdk>`_
- `WebRTC SUF Sora Python SDK <https://github.com/shiguredo/sora-python-sdk>`_
- `WebRTC Native Client Momo <https://github.com/shiguredo/momo>`_


比較表
=========================

Sora Labo は検証目的以外での利用はできません。それ以外は `Sora Cloud <https://sora-cloud.shiguredo.jp>`_ または `Sora <https://sora.shiguredo.jp>`_ をご検討ください。

.. list-table::
    :header-rows: 1

    * - 機能
      - Sora Labo
      - Sora Cloud
      - Sora
    * - タイプ
      - SaaS
      - SaaS
      - パッケージ
    * - 商用利用
      - 不可、検証目的のみ
      - 可
      - 可
    * - アカデミック利用
      - 不可
      - 可
      - 可
    * - 同時接続
      - 1 チャネル 10 程度
      - 5000 程度
      - ライセンスに依存
    * - 帯域
      - 制限あり
      - 最大 20 Gbps
      - 自由
    * - 認証
      - アクセストークン
      - アクセストークン
      - 自由
    * - ウェブフック
      - 不可
      - 可
      - 可
    * - API
      - 不可
      - 一部を除いて可
      - 可
    * - 録画
      - 不可
      - 可
      - 可
    * - 運用
      - 不要
      - 不要
      - 必要
    * - 構築
      - 不要
      - 不要
      - 必要
    * - サポート
      - 無し
      - 有り(チケット)
      - 有り(メール)


利用方法
========

アクセストークンを生成する
----------------------------------------------

- シークレットキーを利用して JWT (HS256) で生成してください
- exp はオプションです
- nbf はオプションです 
- channel_id はオプションです

  - channel_id クレームを指定するとチャネル ID が一致していないと認証に失敗します

アクセストークンは Sora Labo のダッシュボードで作成可能です。

.. image:: https://i.gyazo.com/2da238f201c08ffef50d01c791d80e34.png

シークレットキーをアクセストークンとして利用する
------------------------------------------------

アクセストークンを生成せずに、シークレットキーをそのままアクセストークンとしても利用可能です。

Sora DevTools を利用する
------------------------

`Sora DevTools <https://github.com/shiguredo/sora-devtools>`_ という開発者ツールを https://sora-devtools.shiguredo.jp/ にデプロイして公開しています。

ダッシュボードページに Sora DevTools をSora Labo 経由で利用できるように、
チャネル ID とアクセストークンとシグナリング URL 埋め込んである URL を用意してあります。

.. image:: https://i.gyazo.com/a6ed59073da7d7773303ab17ecc68250.png

Sora JavaScript SDK を利用する
--------------------------------------------

Sora JavaScript SDK のサンプル集を利用して Sora Labo に接続できます。

`WebRTC SFU Sora JavaScript SDK サンプル集 <https://github.com/shiguredo/sora-js-sdk-samples>`_

``git clone`` 後 ``pnpm install`` した後、
``sendrecv`` ディレクトリの ``.env.local.sample`` を ``.env.local`` に変更して以下の値を設定してください。

.. code-block::

  VITE_DEFAULT_SIGNALING_URL=wss://0001.canary.sora-labo.shiguredo.app/signaling
  VITE_DEFAULT_CHANNEL_ID=<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>
  VITE_DEFAULT_ACCESS_TOKEN=<アクセストークン>

その後は ``pnpm run sendrecv`` で実行可能です。

Sora Android SDK を利用する
-------------------------------

`shiguredo/sora-android-sdk: WebRTC SFU Sora Android SDK <https://github.com/shiguredo/sora-android-sdk>`_

Sora Android SDK のクイックスタートまたはサンプル集を利用して Sora Labo に接続できます。

- `WebRTC SFU Sora Android SDK クイックスタート <https://github.com/shiguredo/sora-android-sdk-quickstart>`_
- `WebRTC SFU Sora Android SDK サンプル集 <https://github.com/shiguredo/sora-android-sdk-samples>`_

1. gradle.properties の作成
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

クイックスタートまたはサンプル集のディレクトリトップの ``gradle.properties.example`` を元に ``gradle.properties`` を作成します。

gradle.properties の作成::

  $ cp gradle.properties.example gradle.properties

2. 接続情報の設定
^^^^^^^^^^^^^^^^^^^^^

``gradle.properties`` に Sora Labo への接続情報を設定します。

- ``signaling_endpoint`` に Sora Labo の Sora シグナリング URLs を設定してください。カンマ区切りですべてのシグナリング URL を指定をしてください。
- ``channel_id`` に ``<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>`` を指定してください

  - ここでは GitHub Username を ``shiguredo`` としています
  - ここでは GitHub ID を ``0`` としています
- ``signaling_metadata`` に自分のアクセストークンを指定してください

  - ここではアクセストークンを ``eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is`` としています

gradle.properties への設定例::

    # Setting Sora's signaling endpoint and channel_id
    signaling_endpoint = wss://0001.canary.sora-labo.shiguredo.app/signaling, wss://0002.canary.sora-labo.shiguredo.app/signaling, wss://0003.canary.sora-labo.shiguredo.app/signaling
    channel_id         = shiguredo_0_sora

    # Setting Signaling Metadata.
    # Quotes must be double escaped.
    # e.g.) signaling_metadata = {\\"spam\\":\\"egg\\"}
    # This setting is required. If you do not want to use it, set it to blank.
    signaling_metadata = {\\"access_token\\":\\"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is\\"}

Sora iOS SDK を利用する
-------------------------------

`shiguredo/sora-ios-sdk: WebRTC SFU Sora iOS SDK <https://github.com/shiguredo/sora-ios-sdk>`_

Sora iOS SDK のクイックスタートまたはサンプル集を利用して Sora Labo に接続できます。

- `WebRTC SFU Sora iOS SDK クイックスタート <https://github.com/shiguredo/sora-ios-sdk-quickstart>`_
- `WebRTC SFU Sora iOS SDK サンプル集 <https://github.com/shiguredo/sora-ios-sdk-samples>`_

1. Environment.swift の作成
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

クイックスタートまたはサンプル集の ``Environment.example.swift`` を元に ``Environment.swift`` を作成します。

Environment.swift の作成::

  $ cp Environment.example.swift Environment.swift

2. 接続情報の設定
^^^^^^^^^^^^^^^^^^^

``Environment.swift`` に Sora Labo への接続情報を設定します。

- ``signaling_endpoint`` に Sora Labo の Sora シグナリング URLs を全て指定してください
- ``channel_id`` に ``<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>`` を指定してください

  - ここでは GitHub Username を ``shiguredo`` としています
  - ここでは GitHub ID を ``0`` としています
- ``signalingConnectMetadata`` に自分のアクセストークンを指定してください

  - ここではアクセストークンを ``eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is`` としています

Environment.swift への設定例::

    // 接続するサーバーのシグナリング URL
    static let urls = [URL(string: "wss://0001.canary.sora-labo.shiguredo.app/signaling")!,
                       URL(string: "wss://0002.canary.sora-labo.shiguredo.app/signaling")!,
                       URL(string: "wss://0003.canary.sora-labo.shiguredo.app/signaling")!]

    // チャネル ID
    static let channelId = "shiguredo_0_sora"

    // metadata
    static let signalingConnectMetadata = ["access_token" : "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is"]

WebRTC Native Client Momo で Sora を利用する
--------------------------------------------

`shiguredo/momo: WebRTC Native Client Momo <https://github.com/shiguredo/momo>`_

Momo で Sora が利用できます。

- ``channel_id`` に ``<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>`` を指定してください

  - ここでは GitHub Username を ``shiguredo`` としています
  - ここでは GitHub ID を ``0`` としています
- 自分のアクセストークンを --metadata で指定してください

  - ここではアクセストークンを ``eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is`` としています
- Sora Labo は Sora クラスターを採用しているため提供されているシグナリング URL をすべて指定してください

GitHub Username が shiguredo で、 チャネル ID が sora-devtools の場合::

    ./momo --resolution VGA --no-audio-device sora --auto \
        --signaling-url \
            wss://0001.canary.sora-labo.shiguredo.app/signaling \
            wss://0002.canary.sora-labo.shiguredo.app/signaling \
            wss://0003.canary.sora-labo.shiguredo.app/signaling \
        --channel-id shiguredo_0_sora \
        --role sendonly --multistream true --video-codec-type VP8 --video-bit-rate 2500 \
        --metadata '{"access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is"}'

Sora DevTools のマルチストリーム受信を開いて接続してみてください。

.. image:: https://i.gyazo.com/ade1532c1536d36cf890e533b9185289.png

AV1 を利用する
-------------------------------

Chrome や Momo を利用する事で、 AV1 が利用可能です。

H.265 を利用する
-------------------------------

Safari Technology Preview 105 以降で設定で ``WebRTC H265 codec`` を有効にすることで H.265 を試すことが可能です。

`Sora で WebRTC の H.265 を試す <https://gist.github.com/voluntas/c271462d273285377593521dcb6dd6a5>`_

OBS (WebRTC) で配信する
=======================================

手順
-------------------

#. OBS をダウンロードする
#. OBS に WHIP エンドポイント URL を指定する
#. OBS の ``Bearer Token`` にアクセストークンを指定する

OBS のダウンロード
----------------------------------------

OBS の WebRTC/WHIP は 30.0.0 から対応しています。

30.0.0 は以下からダウンロード可能です。
https://github.com/obsproject/obs-studio/releases/tag/30.0.0

OBS (WebRTC) の設定
-------------------------

#. サービスで WHIP を選ぶ
#. サーバーに WHIP エンドポイントを指定する

   - ``https://canary.sora-labo.shiguredo.app/whip/{channel_id}``
   - ``channel_id`` は ``{github-username}_{github-id}_{channel_name}`` です
#. ``Bearer Token`` を指定する

.. image:: https://i.gyazo.com/40b0143574fcdc8f27e28102d3040608.png

OBS の設定例
---------------------------

以下は macOS の H.264 HWA を利用して 1080p 60fps で配信する際の設定例です。

.. image:: https://i.gyazo.com/2343be3113f6ee62bbd5854832095d7b.png

.. image:: https://i.gyazo.com/bde10b937928dd43b588c205ee8e0435.png


認証方法
========

チャネル ID を決める
--------------------

アクセストークンを利用してチャネルに認証をかけてみます。

チャネル ID は GitHub アカウントのユーザ名を先頭に指定する必要があります。

``<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>`` と指定する必要があります。

以下はチャネル名 sora-devtools 、Github ユーザ名 shiguredo 、GitHub ID 0 を指定した例です。

チャネル ID 例::

    shiguredo_0_sora-devtools


metadata に access_token を指定する
------------------------------------

Sora の SDK は metadata をシグナリング時に指定できます。metadata に ``access_token`` を指定して下さい。
これで利用可能になります。

アクセストークンが ``eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is`` の場合

.. code-block:: javascript

    {"access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is"}

検証向け機能
============

TURN-TCP 利用強制機能
---------------------

指定した接続が TURN-TCP を利用するように強制可能にする機能です。

metadata 指定時に ``{"turn_tcp_only": true}`` を指定して下さい。

TURN-TLS 利用強制機能
---------------------

指定した接続が TURN-TLS を利用するように強制可能にする機能です。

metadata 指定時に ``{"turn_tls_only": true}`` を指定して下さい。

Sora Labo のアカウントを削除する
=================================

**アカウントは削除しますが、ログは削除しないためアカウントを削除したとしても利用時間はリセットされません**

もし今後、 Sora Labo を利用しないのであればアカウントを削除できます。

ダッシュボードの一番下にアカウントの削除があります。



