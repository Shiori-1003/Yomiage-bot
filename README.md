# Nursery


## 概要

Discordのテキストチャンネルに投稿された文章を[棒読みちゃん](http://chi.usamimi.info/Program/Application/BouyomiChan/)で読み上げ、その音声をボイスチャンネルに流すbotプログラムです。


## インストール方法

[インストール方法](install.md)を参照してください。


## 特徴

### 参加者全員に聞こえる読み上げbot

一般的な読み上げソフトは、音声をPCのスピーカーに流します。そのため、読み上げ音声はソフトを起動した人にだけ聞こえます。読み上げ音声を他の人に共有するには、ボイスチャンネルとは別の配信などを利用する必要があります。

Nurseryは、読み上げた音声をDiscordのボイスチャンネルに流します。そのため、 **ボイスチャンネルに参加している全員に同じ音声が聞こえます。** 

Discordのボイスチャンネル以外の機能が必要ないので、 **スマートフォン版のDiscordを使っている参加者も読み上げ音声を聞くことができます。** 

また、Nurseryはbotアカウントを介して読み上げ音声を流すため、読み上げが不要だと思ったら、botをミュートすれば対応できます。

### どんな用途に向いているか

Nurseryは以下のような状況に適しています：

* 読み上げ音声を参加者全員で聞きたいとき
* スマートフォンなど、読み上げソフトが実行できない環境の人にも読み上げ音声を共有したいとき

以下のような状況ならば、他の読み上げソフトの方が適しているかもしれません：

* 読み上げ音声が自分にだけ聞こえればいい場合
* 読み上げ音声を別の方法で配信する場合（動画配信など）

### 棒読みちゃんのコマンドを活用可能

棒読みちゃんを「配信者向け」に設定することで、棒読みちゃんの機能の一部をそのまま使用することができます。以下はその一例です。

* `教育(言葉=読み方)`コマンドを使用することで、読み方を登録することができます。
* `エコー)`コマンドを使用することで、読み上げ音声にエコーをかけることができます。

制限は以下の通りです：

* `Sound`：`Sound`コマンドの音声は使用者のPCでしか聞こえません。
（代わりに、NurseryのSEプラグインを使用することで、ボイスチャンネル上で音声を再生することができます。）

### 仮想サウンドデバイスを使用

仮想サウンドデバイスとは、大雑把に言えば「マイクとスピーカーのフリをするソフトウェア」です。

Nurseryではまず、棒読みちゃんの音声を「スピーカーのフリ」をした仮想サウンドデバイスに流すよう設定します。そして、同じ仮想サウンドデバイスに「マイクのフリ」をさせることで、読み上げ音声をDiscordのボイスチャンネルに流します。