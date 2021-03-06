+++
author = "@yu-kgr"
categories = ["TIL"]
date = "2018-07-13"
description = "2018/07 - Second week I Learned | 一週間で知った事・学んだ事の個人的な備忘録"
featured = "/img/til/til.jpg"
featuredalt = "til"
featuredpath = "https://kglabo.com"
title = "2018/07 - Second week I Learned"
type = "post"
draft = "false"
+++

# 今週、知った/学んだこと

<!-- tags = ["VSCode", "Command Line"] -->

## 2018/07/09 - Learned

7月9日（月）のToday I Leaned.

### VSCodeで独自のSyntaxHighlightを作る方法

- 結論 : テンプレートエンジン`ect`のSyntaxHighlightがSublimeText / Atomにはあるにも関わらず、VSCodeにはなかったので自作した。
  - [ect-highlight](https://github.com/yu-kgr/vscode-ect-syntax-highlight)
  - [参考:Visual Studio CodeでPlane Text(.txt)で自分独自記法のハイライト表示](https://prius.hateblo.jp/entry/2016/10/15/121707)
  - [参考:VS Code の ChangeLog 用 Extension を作成する](https://blog.kondoumh.com/entry/2018/01/12/084409)

1. ect.tmLanguageファイルを作成
  - [atom用の設定ファイルを参考](https://github.com/peppage/language-ect)に用意。
2. `The Yo Code Visual Studio Code Extension Generator`を使って、VS Code用にコンバートしつつ、生成されたファイルを微修正。
3. VS Codeの指定箇所に配置する

#### 所感

- HTMLで表示していたのでHTMLLinterがエラー検知してやっかいだったのがでなくなって満足！
- 尚、VS CodeのMarketへの公開方法はいまいちわからなかった。

## 2018/07/10 - Learned

7月10日（火）のToday I Leaned.

### Command Line

- [参考:progate コマンドライン学習コース](https://prog-8.com/lessons/commandline/study/1)
- （よくわかってなかったCommandだけ抜粋。）

#### pwd Command

- `Print Working Directory` の略。現在いるディレクトリがどこかを返してくれる

#### ls Command

- `list`の略。カレントディレクトリ内のディレクトリやファイルが一覧で表示される

#### mv Command

- `move` の略。ファイルの移動及び、同じディレクトリに違う名前で移動する事が可能。
- `mv  {移動させたいファイル名} {移動先のディレクトリ名}` または、 `mv  {移動させたいディレクトリ名} {移動先のディレクトリ名}` でデータを移動する事が出来る。
- `mv {リネームしたいファイル名}` `リネーム後のファイル名` で、データの名称を変更する事も可能。
- moveなのになんで名前変更できるねん。ってツッコミに対してはコチラの記事が参考になった。
  - [参考:mvでリネームができるわけをどこまで深く話せますか](https://qiita.com/junjis0203/items/9e8f642b04d9754f1139)

#### cp Command

- `copy` の略。ファイルのコピーを行う。
- `cp {コピーするファイル名} {コピーされる新しいファイル名}` でファイルをコピーする事ができる。
- 同様に`cp -r {コピーするディレクトリ名} {コピーされる新しいディレクトリ名}` でディレクトリ単位でコピーする事ができる。
  - ディレクトリは`-r`をつけないとコピーが実行されないので注意。
  - 尚、 `-r`は`--recursive`の略でコピー元にディレクトリを指定した場合、再帰的に（サブディレクトリも含めて）コピーするという意味らしい。

#### rm Command

- `remove` の略。ファイルの削除を行う。
- `rm {削除するファイル名}`でファイルを削除する事ができる。
- `rm -r {削除するディレクトリ名}` でディレクトリを削除する事ができる。
  - こちらもディレクトリは`-r`をつけないと削除が実行されないので注意。

## 2018/07/11 - Learned

7月11日（水）のToday I Leaned.

### Confluenceでstylusを有効活用

- 捜し物したい時にConfluence開いたら「人気の投稿」が気になってしまう対策
- stylus使ってConfluence用のカスタムスタイル作成して、「全ての更新」と「人気のコンテンツ」を非表示にするというパワープレイ。
  - 必要に応じてスタイルをOFFにしたら見れるから無問題

```css
#sidebar-discover  {
    display: none;
}
```

### Macのtmpディレクトリとは一体

- 「tmpにファイルを作成して試してみましょう」系で、そもそもtmpにファイル作って後々ゴミとかにならないの？大丈夫のの？って思ったので調べてみた。
  - [参考:/tmpと/var/tmpの仁義無き戦い](https://qiita.com/kuni-nakaji/items/f29be14be578b5a19d4b)

#### /tmp
- このディレクトリはもともメモリの代わりに使用しようとしていたらしく、再起動時に内包するデータをクリアする仕様（思想？）
- 性質的には
  - 一時的ファイルを必要とするプログラムで使用
  - 再起動するとファイルは消える
  - 定期的に削除される

#### /var/tmp

- 同じtmpでも `var/tmp`というtmpディレクトリも存在する模様。
- こちらの性質としては、
  - 再起動してもファイルは消えない
  - /tmpより長い期間保持されるが定期的に削除される

という違いの模様。
`tmpにファイルを作成して試してみましょう` の意図としては、  
`放っといたら消える所だから安心してtmpに作成していろいろ試して見ましょう。` という意味だと捉えた。スッキリ。


### ssh Command

- 正式名称はSecure Shellでの接続。
- 暗号や認証の技術を利用して、安全にリモートコンピュータと通信するためのプロトコル。パスワードなどの認証部分を含むすべてのネットワーク上の通信が暗号化される。
- ひと言で言うと、「PCに対して安全に接続する為の手法」のひとつ。接続先のポートは22番がウェルノウンポートとの事。
- `ssh ユーザ名@ホスト名` で接続可能。
  - 名前解決ができれば、ホスト名の所はIP直打ちではなく`ssh ユーザー名@hoge.com`のような形も可能。
  - 更に公開鍵/秘密鍵の登録を適切に行えばID/PASSでの接続ではなく、 `ssh ユーザ名@{接続先ホスト名} -i {秘密鍵名称}`でパスワードの入力も不要になる。
 
#### ウェルノウンポート

- ウェルノウンポートとは、TCP/IPによる通信で利用されるTCPやUDPのポート番号のうち、著名なサービスやプロトコルが利用するために予約されている0番から1023番のこと。
- [参考:ウェルノウンポートとは - IT用語辞典](http://e-words.jp/w/%E3%82%A6%E3%82%A7%E3%83%AB%E3%83%8E%E3%82%A6%E3%83%B3%E3%83%9D%E3%83%BC%E3%83%88.html)
  - HTTPの80番やFTPの20・21番、SMTPの25番、POP3の110番、DNSの53番などである。また、新しいプロトコルやサービスは1024番以降を利用することが慣例となっている。
  - サーバ上でどのサービスをどのポートで動作させるかはソフトウェアによって設定できるようになっていることが多く、必ずしもウェルノウンポートでなければそのサービスを起動・利用できないわけではない。
- テレビのチャンネル（デフォ設定）みたいなもんだと認識。

#### sshrc

- sshrc をインストールすれば、~/.sshrc に書いたコマンドをssh接続先の各サーバで実行してくれるらしい。
- [参考:sshした先に.bashrcや.vimrcを持って行きたい人のためのsshrc](https://qiita.com/ikuwow/items/ba4ca57fd67c06fd1b19)

同じようなものDockerであったら便利じゃね？って思ったらあった。

#### sshrc的なdocker exec -it 用ラッパー

- ローカルに用意しておいた設定をコンテナ内に自動的に持っていく docker exec -it 用のラッパーらしい。
  - zsh / vim やらの自前環境をDocekr環境に持っていく事ができそう。
- [参考:](https://amaya382.hatenablog.jp/entry/2017/12/22/225555)

### scp Command

- Secure Copyの略。sshを利用してセキュリティを担保しつつ、ファイルの転送・コピーを行うコマンド。

- ローカルからサーバにコピーする場合は、`scp {送りたいものの場所} {ユーザ名@ホスト名:配置先}`の形で記載
  - `scp -i {ssh認証鍵の場所を指定} {送りたいものの場所} {ユーザ名@ホスト名:配置先}`でパスワードの入力を省略できる
- サーバからローカルにコピーする場合は、 `scp {ユーザ名@ホスト名:送りたいものの場所} {配置先}` でイケる
  - 同じく　 `−i ｛ssh認証鍵の場所を指定｝` でパスワード省略でイケる。

## 2018/07/12 - Learned

7月12日（木）のToday I Leaned.

### ls Command

- ls Commandって`ls {ファイル名}` で指定先の情報も取得できるのか・・・しらなんだ。
  - `ls -l {ファイル名}`も可。

### tar Command

- Tape Archievesの略。その名の通り、元々は磁気テープ向けにファイルをアーカイブするためのコマンドだったらしい。
  - [参考:tarコマンドについての素朴な疑問を調べた](https://qiita.com/tatesuke/items/c5370823adc7772d55d8)
- `tar -{オプション} {アーカイヴのファイル名} {アーカイヴするもの}` で指定したファイルのアーカイヴ化が出来る。
  - `-c`でアーカイブ化 / `-x`で展開 / `-v`で詳細表示 / `-f`でアーカイブor展開するファイル名の指定
