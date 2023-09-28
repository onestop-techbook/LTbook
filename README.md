# ワンストップLT

## 概要説明
本のタイトル：ワンストップLT

## この本の目的
LT会って、参加すると楽しいですよね。学びもあり、単純に聞いてるだけでも楽しいし、あとの懇親会も・・・

LTとは
LT会に参加してみよう
LTを聞くコツ
LTをやってみよう
LT(発表・登壇)のコツ
LT会を主催してみよう
などなど。

## 執筆・配布スケジュール
募集開始・環境構築：2023月9月28日
本文初稿：2023年10月20日
原稿締め切り：2023年10月30日
発行:2023年11月25日　技書博(蒲田:大田区産業プラザPiO)

## 著者紹介兼あとがき
Contributers.re内に、テンプレートに従って記入ください。

## 執筆にあたってのお願い
GitHubで原稿ファイルを管理しています。

まずは、https://github.com/onestop-techbook/LTbook からCloneしてください。
原稿が書けたら、当該リポジトリにプルリクを出してください。
適宜マージします。

見本の章を参考に、Markdownで本文を書くとスムーズです。

### 命名規則
chap-名前-title.md

画像は、
/images/chap-名前-title/xx.png
として格納してください。

ltbook.jsonの下の方に、執筆原稿を参照しているところがあります。ここにファイル名を追記してください。

### その他の注意

Confrictが発生した場合は、解決お願いします。または、ご相談ください。

push -f等はやめましょう。（歴史を書き換えてはいけません。

相談事：
Issue立ててください。

雑談、ざっくばらんな相談については、エンジニアの登壇を応援する会のSlackがあります。
#howto-lt-book-202311にご参加ください。

その他不明点、相談事は親方まで。https://twitter.com/oyakata2438

## 執筆方法

本書は、easybooks を使って発行されています。easybooks では Markdown か Re:VIEW で記述します。

* [Markdownでの書き方](https://raw.githubusercontent.com/erukiti/easybooks/master/example/about-easybooks.md)
* [Re:VIEWチートシート](https://gist.github.com/erukiti/c4e3189dda179a0f0b73299fb5787838) を作ってみたので、参考にしてみてください。

また、プレーンテキストやWordとかでの提出も可能です。編集部にてコンバートします。
Slackのhowto-lt-book-202311にてご相談ください。

## インストール

### Dockerを使う方法

Dockerを使うのが一番手軽です。とても面倒なTeXのインストールなどを全てDockerでやってくれるため、何も悩むことはありません。

Dockerがある環境ならば、batファイルまたはshファイル叩くとPDFが生成されます。

```sh
$ docker run -t --rm -v $(pwd):/book vvakame/review:3.2 /bin/bash -ci "cd /book && yarn && yarn build"
```

このコマンドの実行が成功すれば、コンパイルされたPDFが、`.review/OnestopLT.pdf` として出力されます。

Mac なら `open .review/OnestopLT.pdf` で PDF を開くことができます。

### WindowsでReviewを使う方法

https://qiita.com/implicit_none/items/398c6e0bbedc8b160621
暗黙の型宣言さんが詳しく書いてくれてます。あるいは、技術同人誌を書こう‐アウトプットのススメ‐をご覧ください。

Windows10(Home/Pro問わず)であれば、WSL＋docker越しにRe:VIWEを扱う方法もあります。https://qiita.com/hoshimado/items/7592cee28c1bde545b78

※2019/11/04時点で、次の環境にて後述のdockerコマンドからコンパイル出来ることを確認済み。

<!-- (3.1指定は、2.x環境と共存のため) -->

* Microsoft Windows 10 Home Version 1903 
* Ubuntu 16.01
* Docker version 17.03.2-ce, build f5ec1e2
* Docker image : vvakame/review (tag:3.1)
* Docker image : vvakame/review (tag:3.2)

### Dockerを使わずにビルドする

* TeX をインストールする
* Ruby をインストールする
  * review gem をインストールする
* Node.js をインストールする

```sh
yarn && yarn build
```

### 権利

ベースには、[TechBooster/ReVIEW\-Template: TechBoosterで利用しているRe:VIEWのテンプレート（B5/A5/電子書籍）](https://github.com/TechBooster/ReVIEW-Template) を使っています。

  * 設定ファイル、テンプレートなど制作環境（techbooster-doujin.styなど）はMITライセンスです
    * 再配布などMITライセンスで定める範囲で権利者表記をおねがいします
