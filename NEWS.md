# お知らせ

[README.md](./README.md) はこちら

## Sora の構成を一新しました

**日時**: 2024-05-29

Sora Labo で提供する Sora の構成を一新しました。

### Sora クラスター

- Akamai Connected Cloud に変更しました
- リージョンは大阪です
- シグナリング URL を一本化しました
  - `wss://sora.sora-labo.shiguredo.app/signaling`
- レギュラーノード: 5 / テンポラリーノード: 2 の 7 台構成に変更しました
- リレーあり / アフィニティなし

### Sora マルチリージョンクラスター

- 大阪 / チェンナイ / ストックホルム / マイアミ / シアトルの 5 リージョンでクラスターを組んでいます
- レギュラーノード: 5 の 5 台構成です
- リレーあり / アフィニティなし

### Sora IPv6 オンリー

- Akamai Connected Cloud に変更しました
- リージョンは大阪です
- シグナリング URL を変更しました
  - `wss://sora-ipv6.sora-labo.shiguredo.app/signaling`
- シングルノードです
