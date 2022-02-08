############################################
Sora Labo における Sora API ドキュメント
############################################

概要
====

Sora Labo では一部のユーザに対して Sora API の利用を解放しています。

このドキュメントでは Sora Labo での Sora API について解説します。

Sora Labo で利用可能な Sora API
================================

それぞれの API については Sora のドキュメントをご確認ください。

- https://sora-doc.shiguredo.jp/
- https://sora-doc-canary.shiguredo.jp/

シグナリング
-----------------

- Sora_20151104.DisconnectChannel
- Sora_20151104.DisconnectClient
- Sora_20151104.DisconnectConnection
- Sora_20201120.DisconnectChannelByRole
 
- Sora_20201013.ListChannelConnections

プッシュ
-----------
 
- Sora_20160711.PushChannel
- Sora_20160711.PushClient
- Sora_20160711.PushConnection
- Sora_20201120.PushChannelByRole

スポットライト
-----------------
 
- Sora_20200807.FocusSpotlightFixed
- Sora_20200807.FocusSpotlight
- Sora_20200807.UnfocusSpotlight
- Sora_20200807.ChangeSpotlightNumber
- Sora_20211215.RequestSpotlightRid
- Sora_20211215.ResetSpotlightRid
- Sora_20211215.BatchRequestSpotlightRid

サイマルキャスト
-------------------

- Sora_20201005.RequestRtpStream
- Sora_20201005.ResetRtpStream


シグナリング通知拡張
--------------------------

- Sora_20201124.ListSignalingNotifyMetadata
- Sora_20201124.GetSignalingNotifyMetadata
- Sora_20201124.PutSignalingNotifyMetadata
- Sora_20201124.DeleteSignalingNotifyMetadata
- Sora_20201124.PutSignalingNotifyMetadataItem
- Sora_20201124.DeleteSignalingNotifyMetadataItem

統計
--------------------------
 
- Sora_20170529.GetStatsConnection
- Sora_20170529.GetStatsClient
 
- Sora_20211215.ListChannelUserAgentStats
- Sora_20211215.GetUserAgentStats

その他
--------------------------

- Sora_20200401.PauseRtpStream
- Sora_20200401.ResumeRtpStream

利用方法
===================

Sora API が解放されているアカウントではダッシュボードに Sora API 用の API キーが表示されています。

- API URL は ``https://sora-api.sora-labo.shiguredo.app/`` です
- API キーを Bearer 認証のトークンとして利用します

  - ``Authorization:Bearer qPBaW3XI32S6lR_Bw_D8NTDLfaO8YlCaTfzm2_khpBuVowKcWYEM2X8SvgJnMWur`` のように指定します
- ``x-sora-release-channel`` で stable / canary どちらのクラスターへの API を実行するか指定します

  - 現時点では canary のみ対応しています

ListChannelConnections の例::

    $ http POST https://sora-api.sora-labo.shiguredo.app/ \
        x-sora-target:Sora_20201013.ListChannelConnections \
        Authorization:Bearer qPBaW3XI32S6lR_Bw_D8NTDLfaO8YlCaTfzm2_khpBuVowKcWYEM2X8SvgJnMWur \
        x-sora-release-channel:canary \
        channel_id=voluntas@sora-devtools \
        -vvv

    POST / HTTP/1.1
    Accept: application/json, */*;q=0.5
    Accept-Encoding: gzip, deflate
    Authorization: Bearer qPBaW3XI32S6lR_Bw_D8NTDLfaO8YlCaTfzm2_khpBuVowKcWYEM2X8SvgJnMWur
    Connection: keep-alive
    Content-Length: 40
    Content-Type: application/json
    Host: sora-api.sora-labo.shiguredo.app
    User-Agent: HTTPie/3.0.2
    x-sora-release-channel: canary
    x-sora-target: Sora_20201013.ListChannelConnections

    {
        "channel_id": "voluntas@sora-devtools"
    }


    HTTP/1.1 200 OK
    Connection: keep-alive
    Content-Encoding: gzip
    Content-Type: application/json
    Date: Tue, 08 Feb 2022 10:30:18 GMT
    Server: cloudflare
    Transfer-Encoding: chunked
    Vary: Accept-Encoding

    [
        {
            "audio": {
                "codec_type": "OPUS"
            },
            "channel_id": "voluntas@sora-devtools",
            "client_id": "E35JE7KG694H3F5NZ304AG3R74",
            "connection_id": "E35JE7KG694H3F5NZ304AG3R74",
            "created_time": 1644316214314590,
            "event_metadata": {
                "github_id": 15551,
                "github_username": "voluntas"
            },
            "multistream": true,
            "role": "sendrecv",
            "session_id": "SCVC9JRZZ900F0KC32T3GY6FBR",
            "simulcast": false,
            "spotlight": false,
            "video": {
                "bit_rate": 1000,
                "codec_type": "VP9"
            }
        }
    ]
