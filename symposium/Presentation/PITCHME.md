@snap[text-10]

## OpenFOAMコントリビュート活動

@snapend

@snap[south]

- 稲葉竜一
- 松原大輔
- @tkoyama010

@snapend

---

@snap[north span-100]

### 目次

@snapend

- gitを使ったossの開発
- OpenFOAMのfork
- ESI版
- Foundation版
- OpeFOAM-jp
- プロジェクトの例

---

@snap[west text-gray text-60]

@fab[git-alt fa-huge]

@snapend

## gitを使ったOSSの開発

+++

@snap[north span-100]

### gitとは？
  
- 分散型プロジェクト管理システム
- 複数人の同時作業に適している
- OSSの開発や管理に使用されていることが多い
- web上のplatformとしてGitHub @fab[github] やGitLab @fab[gitlab] などがある

@snapend

@ol
1. issueで議論 
1. branchで共同編集 
1. Pull Requestでチェック 
1. CIで自動テスト 
@olend

+++

@snap[north span-100]

### issue

- バグ報告, 機能の要望, 予定, 開発など
- 基本的にGitHubなどのplatform上で管理される

@snapend  

@snap[east]

@img[span-80](symposium/Presentation/fig/gitissue.png)

@snapend

@snap[west]

@img[span-40](symposium/Presentation/fig/issue_example.png)

@snapend

+++

@snap[north text-08 span-100]

### branchの考え方

- 各編集作業を枝分かれ(branch)して管理する
- 編集がおわったらPull Requestで議論した後にmergeする
- 目的別、作業者別に同時並行で編集可能

@snapend

@img[span-70](symposium/Presentation/fig/PR2.png)


+++

@snap[north text-08 span-100]

### 手元のPCでの操作

- ブランチを切り替え(checkout)てから作業開始
- 作業した後にそのファイルを指定(add)して登録(commit)をする
- 他の人の変更があった場合にはpull(更新)を行う

@snapend

@img[span-50](symposium/Presentation/fig/gitlocal.png)

+++

@snap[north span-100]

### ローカルの操作
 
- 例：自分のbranchを作成してpush

@snapend

@snap[east span-60 text-08]

```sh
$ git clone https://github.com/myName/myProject.git
$ cd myProject
$ git checkout develop
$ git checkout -b my-branch-1
# 作業をする
$ git add *
$ git commit -m "#16 test"
$ git push
```

@[1-2](ローカルにダウンロード)
@[3](ブランチ切替 @fab[arrow-right] develop )
@[4](ブランチ作成 develop @fab[arrow-right] my-branch-1)
@[5-8](リモートへアップロード)

@snapend

@snap[west]

@img[span-60](symposium/Presentation/fig/gitlocal.png)

@snapend

+++

@snap[north span-100]

### プルリクエストを送る

- GitHubなどのweb上で行う
- issueの様に議論をして問題がなければ権限者によりmergeされる

@snapend

@img[span-100](symposium/Presentation/fig/PR2.png)

+++

@snap[north text-08 span-100]

## 継続的インテグレーション（CI）

- push時の自動でテストシステム
- Pull Requestの承認の際の指標になる
- テスト内容は自分で作成する

@img[span-50](symposium/Presentation/fig/ci.png)

@snapend

+++

@snap[north span-100]

### CI動作例

- 本発表の梗概を共同制作
- Travis CIを活用
- 各branchをTeXで作成→push→Pull Request
- CIが通っていればmerge

@img[span-50](symposium/Presentation/fig/ci-sample.png)

@snapend

+++

@snap[north span-100]
## まとめ

- git開発は共同作業に便利
- 一度cloneすればローカルで作業可能
- CIにより自動テストなども可能

@snapend

@img[span-70](symposium/Presentation/fig/git.png)

---

## OpenFOAM

+++

@snap[north span-100]
### OpenFOAM
@snapend

- OSSのCFDライブラリ
- Imperial Collageで開発された商用ソルバー"FOAM"がベース
- 2004年にオープンソース化
- その後いくつかのforkができる
  - Foundation版
    - 最新版は**OpenFOAM-V7**
    - FOAMの生みの親であるHenry Weller氏が管理
    - Ubuntuではaptでインストールできる
    - OpenFOAM Foundation Inc.による運営
  - ESI版
    - 最新版は**OpenFOAM-v1906**
    - OpenFAOM-3.0+として生まれたfork
    - 開発頻度が高い
    - ESI社とOpenCFD社によるFork
  - 他にもたくさんある

---

## ESI版

+++


@snap[north span-100]
### ESI版の開発

- ~~[OpenFOAM-plus](https://develop.openfoam.com/Development/OpenFOAM-plus)としてGitLab@fab[gitlab]で開発~~
- **@color[#ff0000](<NEW!!>)[openfoam](https://develop.openfoam.com/Development/openfoam/)としてGitLab@fab[gitlab]で開発**

@snapend

@img[span-70](symposium/Presentation/fig/gitlab_top.png)

+++

@snap[north span-100]

### ESI版のissue

バグ報告, 機能の要望, 導入予定の機能の審議と開発など
  
@snapend

@img[span-70](symposium/Presentation/fig/gitlabIssues.png)

+++

@snap[north span-100]
### ESI版のissueの立て方

- issuesのページの右上のNew Issueボタンから作成する

@snapend

@img[span-70](symposium/Presentation/fig/gitlab_issue.png)

+++

@snap[north span-100]
### issueを立ててみた

- 簡単なtypoのissue

@img[span-70](symposium/TeX/fig/plus_issue.png)

@snapend
+++

@snap[north span-100 text-08]
### Pull Requestなど

- プロジェクトメンバーのみがPull Requestなどを行うことができる
- メンバーに加入するには専用ページから申し込む
- ただし現在14人しかいないほど狭き門

@snapend

@img[span-70](symposium/Presentation/fig/com_contactus.png)


+++

@snap[north span-100]
### ESI版まとめ
@snapend

| repository | ~~OpenFOAM-plus~~ [openfoam](https://develop.openfoam.com/Development/openfoam/) | 
| :---: | :---: |
| platform | GitLab@fab[gitlab] |
| clone, fork | 誰でもOK |
| issue | 誰でもOK |
| Pull Request | 権限が必要 |

---

## Foundation版

+++

@snap[north span-100]
### Foundation版の開発
@snapend

- [OpenFOAM-dev](https://github.com/OpenFOAM/OpenFOAM-dev)としてGitHub@fab[github]上で開発
- 最新リリース版は**OpenFOAM-V7**

@img[span-70](symposium/Presentation/fig/openfoam-dev-toppage.png)

+++

@snap[north span-100]
### Foundation版のissue

- [専用サイト](https://bugs.openfoam.org/)で行われる(GitHub上ではない)
- 申請すれば誰でもViewer→Reporterに権限が変わる

@snapend

@img[span-70](symposium/Presentation/fig/issueTracking.png)

+++

@snap[north span-100]
### Pull Request
@snapend

- GitHubでPull Requestを送ることはできる
- ただ過去の20件のうち承認されたものはない
- issueを立てる→管理者が編集、という方式が取られている
- 管理者はおそらく二人

+++

@snap[north span-100]
### Foundation版まとめ
@snapend

| repository | OpenFOAM-dev |
| :---: | :---: |
| platform | GitHub@fab[github] |
| clone, fork | 誰でもOK |
| issue | 誰でもOK([専用サイト](https://bugs.openfoam.org/)) |
| Pull Request | 権限が必要 |

---

## OpeFOAM-jp

+++

@snap[north span-100]
### OpenFOAM-jpの目的と経緯
@snapend

- コントリビュートの最初の一歩として
- OpenFOAMの開発をやってみたい
- 日本のコントリビュート活動の活性化
- Gitとかの練習をしたい

## @fab[arrow-down]

- 有志でコミュニティを作成（現在3人）
- OpenFAOM-devをforkしたGitHub@fab[github] repositoryを作成
- 色々やってみよう！

+++

@snap[north span-100 text-08]
### OpenFOAM-jpのissue

- [issuesレポジトリ](https://github.com/OpenFOAM-jp/issues)として作成（[vim-jp/issues](https://github.com/vim-jp/issues)のfork）
- 日本コミュニティ内でのOpenFOAMに関する議論の場
- 機能追加やチュートリアルの作成などの発案、開発に使用
- OpenFOAMの質問は既存の[Google Group](https://groups.google.com/forum/#!forum/openfoam)へ
- もちろん誰でも参加可能

@snapend

@img[span-70](symposium/Presentation/fig/jp-issue.png)

+++

@snap[north span-100]
### OpenFOAM-jpの開発
@snapend

- OpenFOAM-devのfork
- 誰でもfork, Pull Requestが可能
- 事前にissuesを作成することを推奨
- インストール方法は[こちら](https://github.com/OpenFOAM-jp/issues/wiki/インストール手順)

@img[span-70](symposium/Presentation/fig/jp-OpenFOAM-jp.png)

+++

@snap[north span-100]
### OpenFOAM-jpまとめ
@snapend

| repository | [OpenFOAM-jp](https://github.com/OpenFOAM-jp/) |
| :---: | :---: |
| platform | GitHub |
| clone, fork | 誰でもOK |
| issue | 誰でもOK([GitHub](https://github.com/OpenFOAM-jp/issues)) |
| Pull Request | @color[#ff0000](誰でもOK) |

---

@snap[north span-100]
### repositoryの比較
@snapend

|   | ESI版 | Foundation版 | OpenFOAM-jp |
| :---: | :---: | :---: | :---: |
| 運営 | [ESI-OpenCFD](https://openfoam.com/) | @size[80%]([OpenFOAM Foundation Ltd](https://openfoam.org/)) | OpenFOAM-jp |
| リモートレポジトリ | GitLab | GitHub | GiHub |
| レポジトリ名 | [openfoam](https://develop.openfoam.com/Development/openfoam/) | [OpenFOAM-dev](https://github.com/OpenFOAM/OpenFOAM-dev) | [OpenFOAM-jp](https://github.com/OpenFOAM-jp/OpenFOAM-jp)
| clone, fork | 誰でもOK | 誰でもOK | 誰でもOK |
| issue | 誰でもOK  ([GitLab](https://bugs.openfoam.org/)) | 誰でもOK  @size[80%](([専用サイト](https://bugs.openfoam.org/))) | 誰でもOK  ([GitHub](https://github.com/OpenFOAM-jp/issues)) | 
| Pull Request | 権限が必要 | 権限が必要 | @color[#ff0000](誰でもOK) |

---

## OpenFOAM-jp プロジェクト紹介

+++

@snap[north span-100 text-08]

## ユーティリティのチュートリアル

OpenFOAMのユーティリティの使い方に関するまとめ

@snapend

@img[span-60](symposium/Presentation/fig/util-tut.png)

+++

## 機能追加 

- mergeMeshesのオプションの改造
- snappyHexMeshのスムージング機能独立
- transformPointsのコピーオプション追加
- fvOptionsでCHT(固体)の計算
- @size[200%](@color[#0000ff](随時募集中！（issueへ）)) |

+++

## 他にも

- ドキュメントの翻訳
- エラーメッセージの日本語化
- OpenFOAMのCIテスト
- Dockerfileを用いたバグ管理

---

## まとめ

- ESI版とFoundation版はissueを送ることでコントリビュートできる
- ただし実際に書いたコードを反映させることは権限がないとできない
- 開発をやってみたい人のためにOpenFOAM-jpを作ってみた
- @size[200%](@color[#0000ff](参加者募集中！)
- @size[200%](@color[#0000ff](やってみたいことがあったらissueへ！)

