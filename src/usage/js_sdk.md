# Sora JavaScript SDK を利用する

[WebRTC SFU Sora JavaScript SDK](https://github.com/shiguredo/sora-js-sdk) の examples を利用して Sora Labo に接続できます。

`git clone` 後 `pnpm install` した後、
`.env.template` を `.env.local` に変更して以下の値を設定してください。

```
VITE_DEFAULT_SIGNALING_URL=wss://0001.canary.sora-labo.shiguredo.app/signaling
VITE_DEFAULT_CHANNEL_ID=<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>
VITE_DEFAULT_ACCESS_TOKEN=<アクセストークン>
```

その後は `pnpm run dev` で実行可能です。
