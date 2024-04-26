---
title: Hexoを使ってブログを構築
date: 2023-12-08 02:00
categories:
  - Hexo
tags: 
  - blog
---

HexoっていうSSGが気になったので試してみた。

えっ？なんで学生が深夜にこんなことしてるかって？ ~~おっと、それ以上はいけない~~

## Hexoってなんだよ
Node.js製の強力なブログフレームワークらしいです。

プラグインで拡張できたり、もちろんテーマも使えます。

### テーマ
[公式サイト](https://hexo.io/themes/)だったり[GitHubのトピック](https://github.com/topics/hexo-theme)だったりで探すのがおすすめ。

おすすめなのは、[Icarus](https://github.com/ppoffice/hexo-theme-icarus)です。日本でも使っている方がたまにいるのでトラブルが起きてもどうにかなりそうなので...

### プラグイン
~~`sitemap.xml`を自動生成してくれるhexo-generator-sitemapとかは入れたほうがいいと思います。~~ hexo-generator-sitemapだとGoogleに登録できませんでした...ちゃんと動く[`hexo-generator-seo-friendly-sitemap`](https://github.com/ludoviclefevre/hexo-generator-seo-friendly-sitemap)がいいと思います。

### 構築
※Node.jsがインストールされている前提で進みます。

まず、`npm install hexo-cli -g`でHexoのCLIをインストールします。

インストールしたら、ブログ用のファイルを生成したいディレクトリに移動して、`hexo init .`を実行します。

以下のようなファイル構成になると思います。
```
├─.github
├─node_modules
│  └─...
├─scaffolds
├─source
│  └─_posts
├─package.json
└─themes
```
一応この状態でも_posts直下に.mdを作成してyarn serverすれば起動できます。

でもせっかくなので、テーマを変えてみます。
### テーマを変える
今回は、Icarusを利用します。
`npm install hexo-theme-icarus`して`hexo config theme icarus`します。
でも、テーマによっては中華フォント(Microsoft YaHeiなど)になっている場合があります。

icarusなら`node_modules\hexo-theme-icarus\include\style\base.styl`に行き、Microsoft Yaheiと書いてある部分をすべてsans-serifなどに変更します。そうすれば治ります。

### 記事を書くときに覚えておくといいこと
タグやカテゴリーは以下のように書く。
```yaml
title: Hexo
date: 0000-00-00 00:00
categories:
  - tech
tags: 
  - hexo
```

### カスタマイズ
テーマは`_config.{テーマ名}.yml`である程度カスタマイズできるようです。

方法は自分で調べてください(丸投げ)

### 生成
htmlを出力するには`hexo generate`を入力してください。入力すると、publicフォルダにhtmlが生成されます。


<p><small>めっちゃ書くのつかれた...</small></p>