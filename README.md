# PONG_Online
あの"ポン"がオンラインで遊べるようになりました！

と言いたいところだけどシンプルすぎなので、
アニメーションをつけるなどでグラフィックを強化するとか
* バーの長さを変えられるようにして、打つ強さが変わるとか、
* チャット機能を追加して、チャットの文字自体がラケットになる(長く打てば打ち返しやすい、や打つ強さが変わる、など)

といった工夫が必要になってくると思います。

## 概要
<http://threepipes.hateblo.jp/entry/2015/02/23/215343#fn-917a7738>のthreepipesさんの作ったブロック崩しをベースに作成してます...
クライアントとサーバモードがあり、サーバ側がほとんどゲームの処理をして、クライアントは送られきたデータで画面を描きます。

## 使用方法
Eclipseでリポジトリをクローンしてくれれば使えます。

ターミナルなどで使う場合は以下の通り...
srcディレクトリに移ります
`$cd PONG_ONLINE/src`
コンパイルします。
`$javac breakout/*.java`
実行します。
`$java breakout.Main`
あとはウィンドウが出てくるので、ポート番号やら接続先ホスト名やらを入れて好きなモードのボタンを押してください。

なお、クライアントモードは、接続先のホストが存在しない場合、すぐ終了してしまいます。

## 注意点
クライアントモードは、接続先のホストが存在しない場合、すぐ終了してしまいます。

また、接続先は現在ホスト名から探すようにしてありますが、家庭間で繋ぐ場合に問題があります。
* ドメインを取得し、特別に契約して固定IPにして家のIPアドレスを登録
* ドメインを取得し、DDNSに定期的に家のIPアドレスを登録
のどちらかなどをしてない限りホスト名から名前解決できません。
家庭間ではなく家庭内で接続するとしても、家でネームサーバーは立ててないと思うし...

なので、ホスト名から引くのではなく、IPアドレスを直打ちして繋ぐというふうに変更した方がいいかもしれません(家庭間で繋ぐ時はルータの設定とかがやっぱり必要だと思うけど...)

## 遊び方
左右矢印キーで移動。落としたらゲームオーバー。今の所は以上です。