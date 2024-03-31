# 認証方法

## チャネル ID を決める

アクセストークンを利用してチャネルに認証をかけます。

チャネル ID は GitHub アカウントのユーザ名を先頭に指定する必要があります。

`<自分の GitHub Username>_<自分の GitHub ID>_<好きなチャネル名>` と指定する必要があります。

以下はチャネル名 sora-devtools 、Github ユーザ名 shiguredo 、GitHub ID 0 を指定した例です。

### チャネル ID 例

```
shiguredo_0_sora-devtools
```

## metadata に access_token を指定する

Sora の SDK は metadata をシグナリング時に指定できます。metadata に `access_token` を指定して下さい。
これで利用可能になります。

アクセストークンが `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is` の場合

```javascript
{"access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjaGFubmVsX2lkIjoic29yYUBzaGlndXJlZG8jMCJ9.TYP-iQaMNcGF7xSxoa8QyqBveUyUQ6EobBc1djg1_is"}
```
