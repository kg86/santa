# サンタジェクション
サンタが壁を登ります！

## コンセプト
今日はクリスマス．

子どもたちとってはとってもとっても大事な日．

みんなサンタさんからプレゼントを貰うのを楽しみに待っている．

それなのにうっかり者のサンタさん達はお寝坊しちゃったみたい．

みんな，お寝坊なサンタを応援してサンタさんを壁の上のソリまで連れって行ってあげよう！！

## デモ
### 仕様
- ブラウザ: Chrome（それ以外のブラウザでは動作未検証）．重要！
- 対象人数: ２〜４

### デモページ
- [ゲーム画面](http://santawall.herokuapp.com/)
- [管理画面](http://santawall.herokuapp.com/unnei.html)
- [コントローラー（携帯）画面](http://santawall.herokuapp.com/shake.html)

コントローラー画面は複数開いても大丈夫です．（想定は４人）

### 遊び方

- 上記３つのページを開きます（コントローラー画面はスマホで開いて下さい）．
- コントローラー画面で操作したいサンタを選びます．
- 管理画面でゲームの進行の項目に書かれている順番にボタンを押していきます．（タイトル画面やルールなどの画面を表示する）
- サンタの名前を入力した後横のボタンを押してサンタを登場させる．
- 初期状態画面にする．（サンタが壁を登ろうとしている画面）
- ゲームスタートボタンを押す．
- コントローラー（携帯）を振って，トナカイに気をつけながら頂上を目指そう．制限時間は３０秒！

### 補足
運営画面でQWERのキーを連打するとそれぞれ赤青黄緑のサンタが登ります．
スマホが足りなかったら運営画面からゲームに参加して下さい．

## ローカルサーバーの立ち上げ方
### サーバを起動
node app.js

### js/config.js
ゲーム画面PCのIPアドレスを設定

var SERVER = "http://xxx.xxx.xxx.xxx:3000";

### ネットワーク
ローカルサーバーで遊ぶ場合は，ゲーム画面，管理画面，コントローラ画面の各端末が同じネットワークに属するようにする．
同じwifiに接続すればとりあえずOK．

以下のページを開く

- ゲーム画面 http://xxx.xxx.xxx.xxx:3000/index.html
- 管理画面 http://xxx.xxx.xxx.xxx:3000/unnei.html
- コントローラー画面 http://xxx.xxx.xxx.xxx:3000/shake.html

### 遊び方
デモの説明と同じ

## 注意事項
- ゲーム画面のロードには画像10MBほどダウンロードします．環境によっては時間がかかるかも．
- 画像を全て読み込んだのを確認してからゲーム画面に移るので，何かが原因で画像が読み込めなかったら永遠にゲーム画面に到達しないかも．
- 画面遷移や登場，ゲームスタートなどのボタンを連打すると変な動作をするかも．
- 複数人が同じサンタを選んだ場合，合計で振った数がそのままサンタの上り動作に反映される．
- 1frame毎の移動ピクセル数を少なくして，大人数で競うのもいいかも．
- 難易度は甘めに設定しているつもり，気になる人は管理画面，サンタの動き調整，1frame毎の移動ピクセル数を調整して下さい．
- 調整の仕方は数字を入力して，反映ボタンを押す．
- 画面が大きい場合は拡大縮小などして調整して下さい．
