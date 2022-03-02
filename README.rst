######################
Sora Labo ドキュメント
######################

これは時雨堂が提供している `Sora Labo <https://sora-labo.shiguredo.app/>`_ のドキュメントです。
ご利用前にかならずご確認いただきます様、お願いいたします。

ステータスページ
=====================

https://shiguredo.statusflare.app/

お知らせ
========

利用時間拡大のお知らせ
------------------------------------------------------------------------------------

:日時: 2022-02-28

利用時間を直近 30 日 1000 分から直近 30 日 2000 分に拡大いたしました。

アカデミック向けのご提供終了のお知らせ
------------------------------------------------------------------------------------

:日時: 2022-02-24

2022 年 2 月 28 日をもってアカデミックむけの提供を終了とさせていただきます。
アカデミックでのご利用をご検討されている方はライセンスの購入をご検討ください。


制限解除終了のお知らせ
------------------------------------------------------------------------------------

:日時: 2022-02-22

利用時間を直近 7 日 100 分から直近 30 日 1000 分に緩和したこともあり、制限解除申請を終了させていただきました。

現在ご利用いただいているお客様は制限期間までご利用可能です。

Sora Labo ドメインの変更およびサービス全体での最大同時接続数の変更
------------------------------------------------------------------------------------

:日時: 2022-02-01

- Sora Labo のドメイン変更を行いました

  - Sora Labo に関するすべてのドメインが ``sora-labo.shiguredo.jp`` から ``sora-labo.shiguredo.app`` へ変更されました
  - シグナリング URL も変更となります。Sora Labo サイトをご確認のうえ変更をお願いします

- Canary 版 Sora クラスターの提供を開始しました

  - 開発中のスナップショット版の Sora です
  - 3 台でクラスターを構成しているため、クラスターの最大同時接続数は 300 となります
- Stable 版 Sora クラスターの提供を開始しました

  - 正式リリース版の Sora です
  - 2 台でクラスターを構成しているため、クラスターの最大同時接続数は 200 となります
- 利用可能時間を直近 7 日間 100 分から直近 30 日間 1000 分に変更しました
- 制限時の最大接続時間を 10 分から 60 分へ変更しました
- 制限解除時の最大接続時間を無制限へ変更しました

FAQ
===

- Sora Labo は無料で利用できますか？

  - 無料で利用できます
- Sora Labo は商用目的で利用できますか？

  - 商用目的では利用できません
  - Sora Labo は Sora の検証以外の目的や用途では利用できません
- Sora Labo をサービスに利用できますか？

  - サービスには利用できません
  - Sora Labo は Sora の検証以外の目的や用途では利用できません
- Sora Labo は法人で利用できますか？

  - 利用可能ですが、Sora の検証目的でのみご利用いただけます
- Sora Labo は個人事業主で利用できますか？

  - 利用可能ですが、Sora の検証目的でのみご利用いただけます
- Sora Labo はアカデミックで利用できますか？

  - 利用できません
- Sora Labo サービス全体での転送量制限がありますか？

  - 1 Sora サーバで 1 TB の転送制限があります
  - 極端に転送量の多い配信をされると他の利用者に影響しますので、ご配慮をお願いします
- Sora Labo サービス全体での帯域制限はありますか？

  - 制限はありません
- Sora Labo は同時接続数の制限がありますか？

  - 1 チャネルあたりの最大同時接続数は 10 です
- Sora Labo は映像ビットレートの制限はありますか？

  - 最大 15 Mbps です
- Sora Labo の合計接続時間制限はありますか？

  - 1000 分です
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

  - 保証はありません。
- Sora Labo はウェブフック機能を提供しますか？

  - 提供しません。評価版をご利用ください。
- Sora Labo は Sora の HTTP API を提供しますか？

  - 提供しません。評価版をご利用ください。
- Sora Labo はサポートを提供しますか？

  - 提供しません。
- Sora SDK のサポートは提供しますか？

  - 提供しません。
- 変更などの告知は行いますか？

  - すべて時雨堂 Discord の #sora-labo にて通知します
- メンテナンス告知は行いますか？

  - 時雨堂の営業時間である平日の 10:00-17:00 の間にメンテナンスを行う場合のみ Discord にて通知します
  - それ以外は事前の告知なく行うことがあります
- Sora Labo の Sora のバージョンはいくつですか？

  - 今後リリースを予定している最新の Sora の開発版です。製品版とは異なります
- 認証エラー理由に ``PLEASE-CONTACT-US`` が出ました

  - いずれかの制限または禁止項目に当てはまっている可能性があります。Discord にてご連絡ください
- 認証エラー理由に ``CONNECTION-LIMIT`` が出ました

  - 直近 30 日間の利用が 1000 分を超えると利用できなくなります

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

- 1 接続の連続接続時間は 60 分です
- 最大合計接続時間は 1000 分です
- Sora の **HTTP API は利用できません**
- Sora の **ウェブフック機能は利用できません**
- Sora Labo は Sora SDK 以外での利用を想定していません
- サービス全体での最大同時接続数は 500 です
- 1 チャネルに接続できる最大の数は 10 です
- ビットレートの最大値は 15 Mbps です

禁止
====

- 商用目的での利用
- 同業他社の利用
- 負荷試験ツールの利用
- すでに登録済みのアカウントとは別にアカウントを作成しての利用
- Sora Labo のベンチマーク結果を第三者へ公開すること

商用利用やアカデミック利用について
=========================================

Sora Labo は商用利用は許可しておりませんので、以下をご検討ください。

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

利用方法
========

Sora DevTools を利用する
------------------------

Sora DevTools という開発者ツールを https://sora-devtools.shiguredo.jp/ で公開しています。

ダッシュボードページに Sora DevTools をSora Labo 経由で利用できるように、
チャネル ID とシグナリングキーとシグナリング URL 埋め込んである URL を用意してあります。

.. image:: https://i.gyazo.com/6f347b31777778d9ec90a142fcba7d1b.png

Sora JS SDK を利用する
------------------------

`shiguredo/sora-js-sdk: WebRTC SFU Sora JavaScript SDK <https://github.com/shiguredo/sora-js-sdk>`_

- チャネル ID を ``<自分の GitHub Username>@<好きなチャネル名>`` のように指定してください
- 自分のシグナリングキーを metadata で指定してください

https://github.com/shiguredo/sora-js-sdk/blob/develop/example/multistream.html

双方向のサンプルの一部です。

.. code-block:: javascript

    const channelId = "shiguredo@sora-devtools";
    const debug = false;
    const sora = connection("wss://<IPv4Address>.<ClusterName>.sora.sora-labo.shiguredo.app/signaling", debug);
    const metadata = {
      signaling_key: "jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa"
    };
    const options = {
      multistream: true
    };
    const publisher = sora.publisher(channelId, metadata, options);

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

- ``signaling_endpoint`` に Sora Labo の Sora シグナリング URLs を設定してください
- ``channel_id`` に ``<自分の GitHub Username>@<好きなチャネル名>`` を指定してください

  - ここでは GitHub Username を ``shiguredo`` としています
- ``signaling_metadata`` に自分のシグナリングキーを指定してください

  - ここではシグナリングキーを ``jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa`` としています

gradle.properties への設定例::

    # Setting Sora's signaling endpoint and channel_id
    signaling_endpoint = wss://<IPv4Address>.<ClusterName>.sora.sora-labo.shiguredo.app/signaling
    channel_id         = shiguredo@sora-devtools

    # Setting Signaling Metadata.
    # Quotes must be double escaped.
    # e.g.) signaling_metadata = {\\"spam\\":\\"egg\\"}
    # This setting is required. If you do not want to use it, set it to blank.
    signaling_metadata = {\\"signaling_key\\":\\"jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa\\"}

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

- ``signaling_endpoint`` に Sora Labo の Sora シグナリング URLs を設定してください
- ``channel_id`` に ``<自分の GitHub Username>@<好きなチャネル名>`` を指定してください

  - ここでは GitHub Username を ``shiguredo`` としています
- ``signalingConnectMetadata`` に自分のシグナリングキーを**追加の上**指定してください

  - ここではシグナリングキーを ``jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa`` としています

Environment.swift への設定例::

    // 接続するサーバーのシグナリング URL
    static let urls = [URL(string: "wss://<IPv4Address>.<ClusterName>.sora.sora-labo.shiguredo.app/signaling")!]

    // チャネル ID
    static let channelId = "shiguredo@sora-devtools"

    // metadata
    static let signalingConnectMetadata = ["signaling_key" : "7jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa"]

3. 接続設定の追加
^^^^^^^^^^^^^^^^^^

接続設定に ``Environment.swift`` で指定した ``signalingConnectMetadata`` を追加します

クイックスタートの Environment.swift への設定例::

    func connect() {
        // 接続の設定を行います。
        let config = Configuration(url: Environment.url,
                                   channelId: Environment.channelId,
                                   role: .sendrecv,
                                   multistreamEnabled: true)

        // signalingConnectMetadata の設定を行います。
        config.signalingConnectMetadata = Environment.signalingConnectMetadata

サンプル集の SoraSDKManager.swift.swift への設定例::

        // Configurationを生成して、接続設定を行います。
        // 必須となる設定はurl, channelId, roleのみです。
        // その他の設定にはデフォルト値が指定されていますが、ここで必要に応じて自由に調整することが可能です。
        var configuration = Configuration(urlCandidates: Environment.urls, channelId: channelId, role: role,
                                          multistreamEnabled: multistreamEnabled)

        // signalingConnectMetadata の設定を行います。
        configuration.signalingConnectMetadata = Environment.signalingConnectMetadata

WebRTC Native Client Momo で Sora を利用する
--------------------------------------------

`shiguredo/momo: WebRTC Native Client Momo <https://github.com/shiguredo/momo>`_

Momo で Sora が利用できます。

- チャネル ID を ``<自分の GitHub Username>@<好きな Room ID>`` のように指定してください

  - ここでは GitHub Username を ``shiguredo`` としています
- 自分のシグナリングキーを --metadata で指定してください

  - ここではシグナリングキーを ``jGTYhHBYhIF0IvzTTvPub0aO8qsmshksqACOCou2GrcOSNTa`` としています

GitHub Username が shiguredo で、 チャネル ID が sora-devtools の場合::

    ./momo --resolution VGA --no-audio-device sora --auto \
        --signaling-url \
            wss://<IPv4Address>.<ClusterName>.sora.sora-labo.shiguredo.app/signaling \
            wss://<IPv4Address>.<ClusterName>.sora.sora-labo.shiguredo.app/signaling \
            wss://<IPv4Address>.<ClusterName>.sora.sora-labo.shiguredo.app/signaling \
        --channel-id shiguredo@sora-devtools \
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

今後
====

**予定は未定**

- Discord 連携
- 同時接続数制限の緩和
- ダッシュボードでの Sora 監視情報の閲覧
- ダッシュボードでの Sora HTTP API 回数閲覧
- ダッシュボードでの Sora HTTP API ログ閲覧
- ダッシュボードでの Sora 統計情報閲覧
- ダッシュボードでの Kohaku 統計情報閲覧
- ダッシュボードでのクライアント問題解析機能
- ダッシュボードでの Sora ログ閲覧
- 録画合成機能
- Sora Prebuilt UI 組み込み機能
- チャネル ID 事前設定機能
- チケット機能

対応済み
----------

- 利用枠直近 7 日間 100 分から直近 30 日間 1000 分 へ拡大
- 利用枠直近 30 日間 2000 分 へ拡大
- アカデミックでの利用禁止
- access_token 認証

  - API キーを利用して署名したトークを利用
- Sora HTTP API 利用
- Sora ウェブフック利用

