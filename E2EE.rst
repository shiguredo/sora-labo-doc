#####################################
E2EE マルチストリーム送受信
#####################################

**この機能はまだ実験段階です**

サンプル
========

Sora Labo ダッシュボードのサンプルからお試しください

.. iamge:: https://i.gyazo.com/73a33a59eb9f9db524fa780c075414fd.png

::

    https://sora-labo.shiguredo.jp/e2ee_multi_sendrecv?channelId=shiguredo@sora-labo&signalingKey=-txMSRv1mSawsCE0xmLx6f7-fjkUjrrA4MdpHrG6Tp6SSZzy#secret

URL ハッシュの後ろの文字列が E2EE 用のパスワードで、デフォルトは secret です。

secret の部分を変更することで、共通鍵を変更できます。今の所、動的な変更には対応していません。

Sora JavaScript SDK での利用
============================

現時点ではまだ Sora JS SDK が非対応なので、お待ち下さい。
