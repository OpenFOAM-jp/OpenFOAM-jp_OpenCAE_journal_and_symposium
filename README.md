# オープンCAE学会論文集・OpenCAEシンポジウムのテンプレートファイル

## 配布物
- オープンCAE学会論文集テンプレートファイル
  - [TeX版](https://gitlab.com/OpenCAE/template_OpenCAE_journal_and_symposium/tree/master/journal/TeX) 
  - Word版(準備中)
- OpenCAEシンポジウムテンプレートファイル
  - [TeX版](https://gitlab.com/OpenCAE/template_OpenCAE_journal_and_symposium/tree/master/symposium/TeX) 
  - Word版(準備中)
- オープンCAE学会論文集・OpenCAEシンポジウム共通TeXクラスファイル
  - [ltjoc.cls](https://gitlab.com/OpenCAE/template_OpenCAE_journal_and_symposium/tree/master/style/ltjoc.cls) 

## ダウンロード

本ページ上部にあるダウンロードボタンから，
お好きな形式でダウンロードして，
解凍してください．

または，以下のようにgitコマンドで取得してください．

```
git clone git@gitlab.com:OpenCAE/template_OpenCAE_journal_and_symposium.git
# または以下
git clone https://gitlab.com/OpenCAE/template_OpenCAE_journal_and_symposium.git
```

## TeXテンプレートファイル
### コンパイルに必要なソフトウェア
[LuaTeX](http://www.luatex.org/)と
[LuaTeX-ja](https://ja.osdn.net/projects/luatex-ja/wiki/FrontPage)
パッケージが必要です．

インストール方法については，
TeX Wikiの[LuaTeX-ja](https://texwiki.texjp.org/?LuaTeX-ja)
を参照してください．
なお，TeX Liveの場合，
TeX Live 2016以前ではコンパイルできないので，
TeX Live 2017以降を用いてください．

LuaTEX-ja パッケージの詳細については，
[LuaTEX-jaパッケージ(pdfファイル)](http://mirrors.ibiblio.org/CTAN/macros/luatex/generic/luatexja/doc/luatexja-ja.pdf)
を参照ください．

### コンパイル方法

コンパイルするにはmakeを実行します．

```
make
```

makeが使用できない場合には，以下のように手動でコンパイルします．

```
lualatex TeXファイル名
lualatex TeXファイル名 #必要なだけ繰り返す
```

BiBTexを用いる場合には，以下でコンパイルします．

```
lualatex TeXファイル名
bibtex TeXファイル名から拡張子.texを除いたもの
lualatex TeXファイル名
lualatex TeXファイル名 #必要なだけ繰り返す
```

### PDFファイルのフォント埋め込み確認

作成したPDFファイルのフォント埋め込み確認には，例えば以下のような方法があります．

- Adobe 社の Acrobat もしくは Acrobat readerで確認する．
  - PDFファイル名を開く．
  - 「ファイル」→「プロパティ」を選択し，「フォント」タブでフォント一覧を表示させる．
  - すべてのフォントが(埋め込み) ないしは (埋め込みサブセット) となっている事を確認する．
- evince(ドキュメントビューアー)で確認する．
  - PDFファイル名を開く．
  - 「ファイル」→「プロパティ」を選択し，「フォント」タブでフォント一覧を表示させる．
  - 「すべてのフォントが標準または埋め込みです」と表示されることを確認する．
- atril(Atril Document Viewer)で確認する．
  - PDFファイル名を開く．
  - 「ファイル」→「プロパティ」を選択し，「フォント」タブでフォント一覧を表示させる．
  - すべてのフォントが(埋め込み) ないしは (埋め込みのサブセット) となっている事を確認する．
- pdffontsで確認する．
  - ```pdffonts PDFファイル名```でフォント一覧を表示させる．
  - すべてのフォントのemb欄がyesとなっている事を確認する．

以下のWEBページも参考にしてください．
- 日本応用数理学会 [pdf ファイルのフォント埋め込みについて](http://www.jsiam.org/modules/xfsection/article.php?articleid=57)
- TeX Wiki [フォントの埋め込みとライセンス](https://texwiki.texjp.org/?%E3%83%95%E3%82%A9%E3%83%B3%E3%83%88%E3%81%AE%E5%9F%8B%E3%82%81%E8%BE%BC%E3%81%BF%E3%81%A8%E3%83%A9%E3%82%A4%E3%82%BB%E3%83%B3%E3%82%B9)

