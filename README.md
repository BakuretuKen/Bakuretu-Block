# 脱衣ブロック崩し「爆裂ブロック（Bakuretu Block）」

1999年に作成した Java Applet版「脱衣ブロック崩し」を JavaScript でリメイクした、シンプルな脱衣ブロック崩しゲームです。

↓画像クリックでゲーム開始

[![タイトル画像](img/game01.png)](https://bakuretuken.github.io/bakuretu-block/)

## 概要
- PC・スマートフォン両対応
- 反射パネルの中心でボールを当てると「爆裂貫通弾」になる特別仕様
- 画像を差し替えるだけで簡単にカスタマイズ可能
- MITライセンスで自由に利用・改造OK

## サンプル
- [公式サンプル・解説ページ](http://bakuretuken.com/block/)

[![ゲーム画像](img/game02.png)](https://bakuretuken.github.io/bakuretu-block/)

## ファイル構成
| ファイル名                | 説明                       |
|---------------------------|----------------------------|
| bakuretublock.js          | ゲーム本体                 |
| enchant.min.js            | enchant.jsゲームエンジン   |
| index.html                | ゲーム起動用HTML           |
| block_icon_boll.png       | ボール画像（44x22）        |
| block_icon_menu.png       | タイトル画像（512x256）    |
| block_icon_panel.png      | 反射パネル画像（120x32）   |
| block_image_back.jpg      | 背景画像（480x640）        |
| block_image_front.png     | ブロック画像（480x640, 透明PNG）|
| block_image_win.jpg       | 勝利画像（480x640）        |

## セットアップ・使い方
1. ファイル一式をWebサーバーにアップロード
2. `index.html`をブラウザで開く
   ※ローカルPCでは画像読み込み制限で動作しないので、サーバー上で動作確認してください
3. 画像を差し替える場合は、同じファイル名・サイズで用意

## ゲーム設定（カスタマイズ）
`index.html`で以下の変数を上書き可能
```js
<script>
var BLOCK_GAME_WIDTH = 480;         // ゲーム画面幅
var BLOCK_GAME_HEIGHT = 640;        // ゲーム画面高さ
var BLOCK_GAME_FPS = 24;            // FPS
var BLOCK_GAME_BALL_SPEED = 10;     // ボール速度
var BLOCK_BAR_MARGIN_BOTTOM = 80;   // パネルの下マージン
var BLOCK_GAME_BLOCK_SIZE = 32;     // ブロックサイズ（16 or 32）
var BLOCK_GAME_MIN_BLOCK_PIXEL = 24;// ブロック化判定ピクセル数
</script>
```

## 注意事項
- 画像を更新したのに反映されない場合は、ブラウザのキャッシュをクリアしてください
- ブロック画像は「透明PNG」で、透明部分以外が「ブロック」になります

## ライセンス
- 本ゲームプログラム・画像はMITライセンスです。自由にご利用ください
- 使用しているゲームエンジン [enchant.js](https://github.com/wise9/enchant.js/) もMITライセンスです

## クレジット
bakuretuKen 2014

---
@see http://bakuretuken.com/block/
