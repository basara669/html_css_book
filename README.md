## 現場のプロが本気で教える HTML/CSSデザイン講義 サンプルデータ

![http://basara669.com/wp-content/uploads/2016/08/html_css_pro_3.jpg](http://basara669.com/wp-content/uploads/2016/08/html_css_pro_3.jpg)

こちらのページから、『現場のプロが本気で教える HTML/CSSデザイン講義』のサンプルデータがダウンロードすることが出来ます。  

購入は[こちら](http://www.amazon.co.jp/dp/4797386533)から

### 誤植や紛らわしい表記について
誤植や紛らわしい表記のため、読みづらくなっており、申し訳ございません。  
誤植についてはこちらのページにて情報を更新していきます。  
コードの太字については、追加した場所だけでなく、ポイントとなっているところも太字になっている部分も太字になっております。  
コード部分は太字だけでなく、他の部分も読みながら読み進めて頂けるようお願い申し上げます。  

### ダウンロード方法
- 右上の「Clone or download」をクリックし、ダイアログを表示させます。
- 表示されたダイアログ内の「DOWNLOAD ZIP」を押せばダウンロードが開始されます。

### ダウンロードファイルの更新について
- [リリースノート](https://github.com/basara669/html_css_book/releases) に更新内容を記載しておりますので、参考にしていただけますと幸いです。
- GitHubのアカウントをお持ちの方はwatchしていだけると、更新された際には通知が届くようになります。

### sanitize.cssについて
 本書のP82にリセットCSSとして「sanitize.css」の使い方を紹介しています。この3段落目に「ダウンロードしましょう」とありますが、執筆時点からバージョンが上がってしまったこともあり、最新版（v4.1.0 2016年10月現在）のものを適用するとその後の部分でキャプチャ通りにならなくなります。
 本ダウンロードファイルのsanitizeというフォルダの中に、執筆時点のバージョン（v3.2.0）を入れました。
 最新版は使用せず、このファイルをご使用ください。

### 「疑似要素」という文言について
当方の確認不足によって、「疑似要素」という文言が「擬似要素」となっている箇所が数か所ございます。正確には「疑似要素」ですので、「擬似要素」としてお読みください。


### FAQ
#### scssファイルの更新がcssに反映されない場合
それまでgulpが正常に動いてる場合、gulp側のエラーではなくscssファイル側に記述ミスが発生している可能性があります。  
ターミナルやコマンドプロンプト上にもエラーが起きていそうな行数が表示されているので、その周辺の修正をお願いいたします。

#### P118で突然コードが変わる
見づらいレイアウトとなっていますが、こちらはTipsというもので、本編とは違う発展的な内容になっています。  
本編だけを読みたいという方はこのTipsは読み飛ばしていただいても問題ございません。

#### P190 Font Awesomeの実装方法について
本書はあくまでCSS設計の本なので、細かいFontAwesomeの解説は省いております。しかし、もう少し詳しいことを知りたいという声があったので追記いたします。  
FontAwesomeでアイコンを使うには、cssファイルとフォントデータが必要になります。P190では、最初にmain.scssにfont-awesomeの読み込みを記述し、cssファイルを読み込んでいます。  
次にダウンロードしたファイルの「fonts」データをdistに移しているのですが、これがFontAwesomeのフォントデータを本書のサイトに移している作業になります。　
こうしてFontAwesomeを使用できる環境である、cssファイルとフォントデータが揃いました。

##### なぜファイルのパスを記述しなくてよいか？（発展内容）
FontAwesomeの公式サイトでは、フォントデータ用のpathを設定しようとあります。しかし、本書ではその手順が書かれていません。なぜそれでも動くかというと、FontAwesomeに最初から記述されている場所にフォントデータを置いているからです。  
FontAwesomeのscssのフォルダにある、`_variables.scss`に`$fa-font-path:"../fonts" !default;`という記述があります。。これはFontAwesomeのcssファイルからフォントデータを読み込む場所を記述する場所が書くところです。  
コンパイルされたscssはdist/css内に吐き出されます。このcssから1つ上の階層に上がり、fontsディレクトリを設定しているために、本書では記述を変更せずに動くことができています。
もしも、フォントデータを置く場所を変えたいということであれば、ここに記述するパスを変更すれば、使用することができます。

### 正誤表
#### P10 上から8行目
##### 誤
開設時に使用します。
##### 正
解説時に使用します。

#### P18 上部画像
##### 誤
![http://basara669.com/wp-content/uploads/2016/09/694d904d39b7b041f11d147c36f55994.png](http://basara669.com/wp-content/uploads/2016/09/694d904d39b7b041f11d147c36f55994.png)

##### 正
画像にnode_modulesというフォルダが含まれていますが、この時点では含まれず以下のようになります。

```
├── article.html
├── campaign.html
├── dist
├── gulpfile.js
├── index.html
├── package.json
├── src
└── test.html

```
#### p021 下から6行目
##### 誤
必要なものが正しくイントール
##### 正
必要なものが正しくインストール

#### p022 下から7行目
##### 誤
これらインスールしたものを使って
##### 正
これらインストールしたものを使って

#### P23 test.html
ダウンロードに入っているHTMLの参照先とpタグが抜けているので追加をしてください。  
なお、現時点のダウンロードのコードには、正の状態になっています。

##### 誤

```html
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="./dist/css/sample.min.css">
    <title>Sample</title>
</head>
<body>

</body>
</html>
```

##### 正
```html
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="./dist/css/main.min.css">
    <title>Sample</title>
</head>
<body>
  <p>テキスト</p>
</body>
</html>

```


#### P30 2行目
##### 誤
ブラウザでindex.htmlを開いてください。

##### 正
ブラウザでtest.htmlを開いてください。


#### P049 下から2行目
##### 誤
詳細度をコントールしています。

##### 正
詳細度をコントロールしています。

#### P050 下から4行目
##### 誤
対して、!imporatantはCSS内に作っているので、

##### 正
対して、!importantはCSS内に作っているので、

#### P071 下から10行目
##### 誤
Class名は、「topicBox__topickDetail__text」のよう

##### 正
Class名は、「topicBox__topicDetail__text」のよう


#### P095 5行目
##### 誤

```html
<img class="EntryPanel__thumb" src="./dist/images/top/entry1.jpg" alt="">

```

##### 正

```html
<img class="EntryPanel__thumb" src="./dist/images/top/entry1.jpg" alt="" width="275" height="250">
```

#### P095 18行目
##### 誤
```html
<img class="EntryPanel__thumb" src="./dist/images/top/entry2.jpg" alt="">
```

##### 正

```html
<img class="EntryPanel__thumb" src="./dist/images/top/entry2.jpg" alt="" width="275" height="250">
```

#### P107 最初のコード
min-heightとしているが、heightが正しい。これに伴い次のコードブロックのコンパイル後の結果のCSSも、  
min-heightではなく、heightとなる

##### 誤

```css
.Header {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  min-height: 98px; //このコードが誤り
  &__head {
    //ここにHeader__headのスタイルを記述する
  }
}
```

##### 正
```css
.Header {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  height: 98px; //このコードが誤り
  &__head {
    //ここにHeader__headのスタイルを記述する
  }
}
```

#### P108 中部コード部分
##### 誤
main.scssの1行目

```scss

@import "./modules/common/header";

```


##### 正
modulesではなく、componentsが正しいです。

```scss

@import "./components/common/header";

```

#### P111 最初のコードブロック
##### 誤

```css
&__main {
    display: flex;
    flex: 1 1 50%;
    flex-direction: column;
    justify-content: space-between;
    align-self: stretch;
}

```

##### 正
```css
&__main {
    display: flex;
    justify-content: space-between;
    align-self: stretch;
    flex: 1 1 55%;
    flex-direction: column;
    padding: 20px 0;
}
```




#### P124 中段の文章
カンマが抜けているため、1,0,0pxが100pxになってしまっている

##### 誤

```
自動的に幅が合わさるように、flexを100pxに指定します。
```

##### 正

```
自動的に幅が合わさるように、flexを1,0,0pxに指定します。
```

#### P136 1行目
「デザインカンプ通りのレイアウトになりました。」とありますが、この時点では、アスペクト比を修正しただけですので、「デザインカンプ通りのサイズになりました」が正しいです。
その後のP143でデザインカンプ通りになります。


#### P146 index.htmlのコードブロック内
不要なclassがついている

##### 誤

```html
<div class="Section__body l-row"> // Section__bodyが不要
  <div class="EntryPanel l-halfColumn">
    (省略)
  </div>
</div>
```

##### 正

```html
<div class="l-row">
  <div class="EntryPanel l-halfColumn">
    (省略)
  </div>
</div>
```


#### P148 中段の文章
カンマが抜けているため、1,0,0pxが100pxになってしまっている

##### 誤

```
自動的に幅が合わさるように、flexを100pxに指定します。
```

##### 正

```
自動的に幅が合わさるように、flexを1,0,0pxに指定します。
```


#### P151 コード部分
記述が間違っていました。

##### 誤

```css
.sectionLabel {
  (省略)
  flex: 1 1 auto;
  padding: 14px inherit;
  padding-bottom: 14px;
  (省略)
}
```

##### 正
```css
.sectionLabel {
  (省略)
  flex: 1 1 auto;
  padding: $space-unit;
  padding-bottom: $space-unit*2;
  (省略)
}
```

#### P156 下部scss
##### 誤
![http://basara669.com/wp-content/uploads/2016/09/9a82cb177e68a01b3d82b6779fb860ab.png](http://basara669.com/wp-content/uploads/2016/09/9a82cb177e68a01b3d82b6779fb860ab.png)


##### 正

```scss
.OverlayPanel {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 100%; //widthが必要です。
    padding: 10% 20%;
    background-color: rgba(0,0,0,.2);
    color: $color-white;
    &:hover {
        color: $color-white;
        background-color: rgba(0,0,0,.4);
    }
}


```




#### P157 `_overlayPanel.scss`内9行目について

`letter-spacing: .1em`となっていますが、こちらは誤りではございません。0を省略する書き方で、この書き方で0.1emとなります。


#### P172 index.html内
ここで出ているhtmlのtime要素にある、datetimeがdatatimeになっている

##### 誤

```html
<time class="NewsList__head" datatime="2016-10-12">2016.10.12</time>

```

##### 正

```html
<time class="NewsList__head" datetime="2016-10-12">2016.10.12</time>

```

#### P179 `_footer.scss`のコード
まだこの時点では書かなくて良いコードが含まれてしまっている
##### 誤
```scss
.Footer {
  (省略)
  &__head { //不要
    flex: 2 1 50%;//不要
  }　//不要
  &__head,　//不要
  &__body {　//不要
    padding-right: $space-unit;　//不要
  }　//不要
  &__body,　//不要
  &__foot {　//不要
    align-self: flex-start;　//不要
    flex: 1 1 25%　//不要
  }　//不要
  a {
  (省略)
  }
}

```
##### 正

```scss

.Footer {
  (省略)
  color: &color-link;
  a {
    color: $color-link;
    &::hover {
      color: $color-white
    }
  }
}

```

#### P184 main.scss内
コードとしては問題ありませんが、整理として`_footer.scss`の記述場所がズレている。
##### 誤

```scss
（省略）
//フッター
@import "./components/common/footer";

//Common
//----------------------------
//ヘッダー
@import "./components/common/header";
(省略)
```

##### 正
```scss
（省略）
//Common
//----------------------------
//ヘッダー
@import "./components/common/header";

//フッター
@import "./components/common/footer";
(省略)
```


#### P192 上部HTML
##### 誤

![http://basara669.com/wp-content/uploads/2016/09/e7e6e6a525fc9d645982f867cc88b99c.png](http://basara669.com/wp-content/uploads/2016/09/e7e6e6a525fc9d645982f867cc88b99c.png)

##### 正

```html
（省略）
<a class="IconPanel  l-quaterColumn">
    <span class="IconPanel__icon  fa fa-tree"></span> <!-- 追加 -->
    <h3 class="IconPanel__head">こだわりの空間</h3>
    <p class="IconPanel__body">
        ランチからディナーまでいつでもリラックスして使えるくつろぎ空間。椅子や壁、細部にまでこだわっています。
    </p>
</a>
（省略）
```

#### P196~P197 本文1行目
表現がわかりづらいというコメントをいただきましたので、正確には以下のような内容です。
##### 誤
```
今作った「SNS」というclassと「SNS__text」というclassを、HTMLに付与します。
```

##### 正
```
今作った「SNS」というclassと、後述する「SNS__text」というclassも併せて、HTMLに付与します。
```

#### P221 中部scss
sassでコンパイルすると10pxとなりどちらも同じ値になりますが、P117ページとの整合上、以下は10pxと直接が適切です。  

##### 誤
![http://basara669.com/wp-content/uploads/2016/09/61e42931750b0d71deb1ccfca3280206.png](http://basara669.com/wp-content/uploads/2016/09/61e42931750b0d71deb1ccfca3280206.png)

##### 正
```scss
(省略)  
.EntryPanel {
  (省略)  
    &__body {
        margin-top: 10px; //10pxが正しいです。
        font-size: 14px;
        @include mq-sp {
            font-size: 12px;
        }
    }
}
(省略)  
```

#### P237 サンプルコードについて
本文にあるコードブロックでは、0.3という表記になっていますが、サンプルコードでは、省略表記である.3となっています。  
これは0を省略している書き方で、0.3も.3もどちらも同じ値を示しています。
サンプルコードでは、`transition: opacity 0s .3s ease`や、`box-shadow: 0 1px 10px rgba(black, .3)`となっていますが、  
それぞれ`transition: opacity 0s 0.3s ease`と`box-shadow: 0 1px 10px rgba(black, 0.3)`のことです。


#### P237 コードブロックについて
##### 誤

```css

.isOpend & {
  opacity: 1;
  transition: opacity 0s 0s ease;
}

```

##### 正
```css

.isOpend & {
  opacity: 1;
  z-index: 1;
  transition: opacity 0s 0s ease;
}

```

#### P246 campaign.htmlのサンプルコード

`Section__head`というclassのついているdivが不要です。

##### 誤

```html
（省略）
<section class="Section l-column">
  <div class="Section__head"> //不要
    <h2 class="sectionLabel">Title1</h2>
  </div>  //不要
</section>
（省略）
```

##### 正
```html
（省略）
<section class="Section l-column">
    <h2 class="sectionLabel">Title1</h2>
</section>
（省略）
```
#### P250 上部scss
sassでコンパイルすると20pxとなりどちらも同じ値になりますが、P117ページとの整合上、以下は20pxと直接が適切です。

##### 誤
![http://basara669.com/wp-content/uploads/2016/09/61e42931750b0d71deb1ccfca3280206.png](http://basara669.com/wp-content/uploads/2016/09/61e42931750b0d71deb1ccfca3280206.png)


##### 正

```css
(省略)
.EntryPanel {
  (省略)
    &__sub {
      flex: 1 1 45%;
      margin-right: 20px;
      .EntryPanel--vertical & {
          margin-right: 0;
      }
    }
(省略)

}
(省略)

```

#### P251 campaign.html内
不要なdivタグがある。

##### 誤

```html
<section class="Section l-column">
  <div class="Section__head"> //不要
    <h2 class="sectionLabel">CAMPAIGN</h2>    
  </div>  //不要
    <div class="l-row">
        <section class="EntryPanel EntryPanel--portrait l-tripartitionColumn"> // EntryPanel--vertical
            <div class="EntryPanel__sub">
                <img class="EntryPanel__thumb" src="./dist/images/campaign/cp_entry1.jpg" alt="フルーツとグラノーラ">
            </div>
            <div class="EntryPanel__main">
                <h3 class="EntryPanel__head">1日のはじまりに</h3>
                <div class="EntryPanel__body">
                    大切なあの方にありがとうを届けたい。<br>心も体も温まる素敵なギフト。<br>プレゼントキャンペーン実施中
                </div>
                <div class="EntryPanel__foot"><a href="#" class="button">READ MORE</a></div>
            </div>
        </section>

```


##### 正

```html
<section class="Section l-column">
    <h2 class="sectionLabel">CAMPAIGN</h2>    
    <div class="l-row">
        <section class="EntryPanel EntryPanel--vertical l-tripartitionColumn">
            <div class="EntryPanel__sub">
                <img class="EntryPanel__thumb" src="./dist/images/campaign/cp_entry1.jpg" alt="フルーツとグラノーラ">
            </div>
            <div class="EntryPanel__main">
                <h3 class="EntryPanel__head">1日のはじまりに</h3>
                <div class="EntryPanel__body">
                    大切なあの方にありがとうを届けたい。<br>心も体も温まる素敵なギフト。<br>プレゼントキャンペーン実施中
                </div>
                <div class="EntryPanel__foot"><a href="#" class="button">READ MORE</a></div>
            </div>
        </section>

```

#### P255 下部の_campaign.scssの解説文とコード

`display:block`とするところが、`flex`となっている

##### 誤

これまで通り、「display」を「flex」にし、

```scss

.Campaign {
  &__sweets {
    display:flex;
  }
}

```

##### 正
「display」に「block」を設定し、
```scss

.Campaign {
  &__sweets {
    display: block;
  }
}

```

#### P260 上部の `_campaign.scss`内のコード
`&__main`としなくてはいけないのに、`&__items`となっている。
##### 誤

```scss
.Campaign {
  (省略)
  &__items {
  (省略)
  }
  (省略)
}

```


##### 正

```scss
.Campaign {
  (省略)
  &__main {
  (省略)
  }
  (省略)
}

```
