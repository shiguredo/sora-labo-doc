#####################################
E2EE マルチストリーム送受信
#####################################

**この機能はまだ実験段階です**

サンプル
========

Sora Labo ダッシュボードのサンプルからお試しください

.. image:: https://i.gyazo.com/73a33a59eb9f9db524fa780c075414fd.png

参考例::

    https://sora-labo.shiguredo.jp/e2ee_multi_sendrecv?channelId=shiguredo@sora-labo&signalingKey=v#secret

URL ハッシュの後ろの文字列が E2EE 用のパスワードで、デフォルトは secret です。

secret の部分を変更することで、共通鍵を変更できます。今の所、動的な変更には対応していません。

Sora JavaScript SDK での利用
============================

develop ブランチではすでに利用可能です。

`shiguredo/sora-js-sdk: WebRTC SFU Sora JavaScript SDK <https://github.com/shiguredo/sora-js-sdk>`_
