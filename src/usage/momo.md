# WebRTC Native Client Momo で Sora を利用する

[shiguredo/momo: WebRTC Native Client Momo](https://github.com/shiguredo/momo)

Momo で Sora が利用できます。

- `channel_id` に `<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>` を指定してください
  - ここでは GitHub Username を `shiguredo` としています
  - ここでは GitHub ID を `0` としています
- 自分のアクセストークンを --metadata で指定してください
  - ここではアクセストークンを `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is` としています
- Sora Labo は Sora クラスターを採用しているため提供されているシグナリング URL をすべて指定してください

## GitHub Username が shiguredo で、 チャネル ID が sora-devtools の場合

```bash
$ ./momo --resolution VGA --no-audio-device sora --auto \
    --signaling-url \
        wss://0001.canary.sora-labo.shiguredo.app/signaling \
        wss://0002.canary.sora-labo.shiguredo.app/signaling \
        wss://0003.canary.sora-labo.shiguredo.app/signaling \
    --channel-id shiguredo_0_sora \
    --role sendonly --multistream true --video-codec-type VP8 --video-bit-rate 2500 \
    --metadata '{"access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is"}'
```

Sora DevTools のマルチストリーム受信を開いて接続してみてください。

[![Image from Gyazo](https://i.gyazo.com/ade1532c1536d36cf890e533b9185289.png)](https://gyazo.com/ade1532c1536d36cf890e533b9185289)
