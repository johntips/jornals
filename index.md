# Design Pattern Specification Language: Definition and Application

- [ダウンロードリンク](https://drive.google.com/open?id=0B6fEh_E17p_rMzNrRUFjQlRuQmM)


## なんの論文か (summary)

- 2003年の論文(結構古い)
- デザインパターンに基づいた、仕様の新しい記述言語を提案する
- その名もDPSL (Desing pattern specification language)

## 何がすごいのか(merits)

- ソフトウェアの仕様を設計するときに、パワーポイントとかで図を作らずとも、DPSLのルールに則って命名したクラスやインターフェースを読み取って、UML図を生成する、その理論、ロジックと記述ロジックのDPSLという言語化
- 現代ソフトウェア開発には、マークダウンでフローチャートを出してくれるjsライブラリがあるが、13年前のそれだと思うと、すごいのかも。

## 何故選んだのか

- 僕の関心は、ソフトウェアを作るときに、コーディングですべて完結すること
- あらゆる仕様の共有を、記述言語に頼りたい。(guiツールとか勘弁)
- 今論文は、一つ、デザインパターンを特定するために必要な仕様がわりとまとまってるとみた。（完全ではないし、2003年にしてはよくまとまってる)

## どうやってデザインパターンの仕様を決めているのか？


- ソースコードと大体の構成
![Proxyパターンの場合](../images/01.png)
![組み合わせた場合](../images/02.png)

## イケてないところ

- 結局図示するためのツールとして、windowdアプリケーションを提供してるけど、いやー、例えば、rubyでも、javaでも使えるように、利用しやすい、ラッパーとしてCとかで書くべき。
- OSSとして育てるべきツールなのに、具体事例としてgithubに公開されてない(そもそも2003年からこの界隈で著者が育ててない。github存在しないか笑)
- DPSLという言語仕様を作るより、ruby,golang,haskell等、パラダイムが違う言語で実際にコーディングしたらこうなる、とかのほうが、再利用しやすいし、発展させてgemなり、gomなりで使えるほうが、みんなハッピーなきがする。
- 結局仕様のための仕様言語を覚えるモチベーションってない気がする。いつも使う自分の好きな言語で書けるようにするべきで、それはその言語のローカライズが必須なので、この論文を超える提案をするなら、全言語対応、デザパ特定ライブラリか、ライブラリのラッパーを提供することかなと思った。

## 学んだこと

- ソフトウェアをクラスやインタフェースとして分割して、全体像を把握するためにデザインパターンで可視化、理解できると、ソースコードがすんごい読みやすいので、なんとかならんかなーという問題に対して、独自記述言語を提案したのは、2003年にしてはおもろい。
- でも全然はやってないのは、やっぱ独自記述言語にしたからだと思う。
- ソースコードの可視化とある程度のフォーマット定義は大賛成なので、この手の模索している論文は見てて楽しい
- BUT,実際の中身のロジックを紐解く論理演算式がくっそほど読み慣れてないので、ぶっちゃけロジックは１０％もわかってないのにこんな文章書いてて自分ダサい
- OOP,DDDとか、そっちのほうをきちんと固めるのがぶっちゃけ近道だと思うので、ちょっと論文の選び方ミスったかも。
- 論文を選ぶ方向性、ツールの最適化を萩野先生、服部先生から突っ込んで欲しいかも。論文の選び方的サムシング
- 





### Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/johntips/jornals/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/johntips/jornals/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
