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

### FAQ
#### scssファイルの更新がcssに反映されない場合
それまでgulpが正常に動いてる場合、gulp側のエラーではなくscssファイル側に記述ミスが発生している可能性があります。  
ターミナルやコマンドプロンプト上にもエラーが起きていそうな行数が表示されているので、その周辺の修正をお願いいたします。

#### P118で突然コードが変わる
見づらいレイアウトとなっていますが、こちらはTipsというもので、本編とは違う発展的な内容になっています。  
本編だけを読みたいという方はこのTipsは読み飛ばしていただいても問題ございません。


### 正誤表
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

#### P136 1行目
「デザインカンプ通りのレイアウトになりました。」とありますが、この時点では、アスペクト比を修正しただけですので、「デザインカンプ通りのサイズになりました」が正しいです。
その後のP143でデザインカンプ通りになります。

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

#### P250 上部scss
sassでコンパイルすると20pxとなりどちらも同じ値になりますが、P117ページとの整合上、以下は20pxと直接が適切です。

##### 誤
![http://basara669.com/wp-content/uploads/2016/09/61e42931750b0d71deb1ccfca3280206.png](http://basara669.com/wp-content/uploads/2016/09/61e42931750b0d71deb1ccfca3280206.png)


##### 正
```scss
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
（省略）
}
（省略）

```
