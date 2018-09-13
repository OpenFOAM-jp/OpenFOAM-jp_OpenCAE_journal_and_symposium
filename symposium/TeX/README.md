# OpenCAEシンポジウムTeXテンプレートファイル

## 必要なソフトウェア
OpenCAEシンポジウムTeXテンプレートファイル
template_OpenCAE_symposium.tex
をコンパイルするには，
[LuaTeX](http://www.luatex.org/)と
[LuaTeX-ja](https://ja.osdn.net/projects/luatex-ja/wiki/FrontPage)
パッケージが必要です．

インストール方法については，
[LuaTeX-ja - TeX Wiki](https://texwiki.texjp.org/?LuaTeX-ja)
を参照してください．
なお，TeX Liveの場合，
TeX Live 2016以前ではコンパイルできないので，
TeX Live 2017以降を用いてください．

LuaTEX-ja パッケージの詳細については，
[LuaTEX-jaパッケージ(pdfファイル)](http://mirrors.ibiblio.org/CTAN/macros/luatex/generic/luatexja/doc/luatexja-ja.pdf)
を参照ください．

## コンパイル方法

コンパイルするにはmakeを実行します．

```
make
```

makeが使用できない場合には，以下のように手動でコンパイルします．

```
lualatex template_OpenCAE_symposium
bibtex template_OpenCAE_symposium
lualatex template_OpenCAE_symposium
lualatex template_OpenCAE_symposium #必要なだけ繰り返す
```

BiBTexを用いない場合には，以下でコンパイルします．

```
lualatex template_OpenCAE_symposium
lualatex template_OpenCAE_symposium #必要なだけ繰り返す
```
