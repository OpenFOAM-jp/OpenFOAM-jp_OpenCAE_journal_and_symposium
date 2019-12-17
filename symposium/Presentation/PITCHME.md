### OpenFOAMコントリビュート活動

- 稲葉竜一
- @tkoyama010
- 松原大輔

---

### 目次

- gitを使ったossの開発
- OpenFOAM Foundation版とESI版の違い
- ESI版のコントリビュート方法
- Foundation版のコントリビュート方法
- OpeFOAM-jp
- Travis による継続的インテグレーション

---

## (予備知識)gitを使ったOSSの開発
  
![git all](symposium/Presentation/fig/git.png)

+++

## gitとは？
  
- 分散型プロジェクト管理システム
- 

+++

### issue

- バグ報告, 機能の要望, 導入予定の機能の審議と開発など
  
![GitHub issue](symposium/Presentation/fig/gitissue.png)

+++

### branchの考え方

- 目的別、作業者別に同時並行で編集可能
- 本体への影響を与えない
- 不具合発生時に問題の切り分けなどが容易になる

![GitHub branch](symposium/Presentation/fig/PR2.png)

+++

### 手元のPCでの操作

- @size[80%](リモートとのやりとり : )
  - @size[80%](clone（ダウンロード）)
  - @size[80%](pull（更新）)
  - @size[80%](push（アップロード）)
- @size[80%](ローカル : )
  - @size[80%](checkout（branch切り替えor作成）)
  - @size[80%](add（選択）)
  - @size[80%](commit（登録）)

![git operation](symposium/Presentation/fig/gitlocal.png)

+++

### 操作例
 
ローカルで自分のbranchを作成してpush

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

@[1-2](GutHubなどにあるリモートレポジトリからダウンロード)
@[3](developブランチに切り替える)
@[4](developブランチから派生したブランチを作成)
@[5-8](変更が終わったら、変更ファイルを指定(add)→コメントをつけて登録(commit)→リモートへアップロード(push))

+++

### プルリクエストを送る

GitHubなどのweb上で行う

![git operation](symposium/TeX/fig/fig-f4.png)

---

## OpenFOAM Foundation版とESI版の違い

+++

### OpenFOAM

- Imperial Collageで開発された商用ソルバー"FOAM"がベース
- 2004年にオープンソース化
- その後いくつかのForkができる
  - Foundation版：OpenFOAM Foundation Inc.によるFork
  - ESI版：ESI社とOpenCFD社によるFork
  
---

## ESI版のコントリビュート方法

+++

### ESI版

- ~~[OpenFOAM-plus](https://develop.openfoam.com/Development/OpenFOAM-plus)としてGitLabで開発~~
- **[openfoam](https://develop.openfoam.com/Development/openfoam/)としてGitLabで開発**

![GitLab Register](symposium/Presentation/fig/gitlab_top.png)

+++

### issue

議論対象：バグ報告, 機能の要望, 導入予定の機能の審議と開発など
  
![issue sample](symposium/Presentation/fig/gitlabIssues.png)

+++

### issueの立て方

- issuesのページの右上のNew Issueボタンから作成する

![GitLab issue](symposium/Presentation/fig/gitlab_issue.png)

+++

### issueを立ててみた

- 簡単なtypoのissue

![plus issue](symposium/TeX/fig/plus_issue.png)

+++

### ESI版まとめ

| :---: | :---: |
| リモートレポジトリ | GitLab |
| レポジトリ名 | ~~OpenFOAM-plus~~ [openfoam](https://develop.openfoam.com/Development/openfoam/) | 
| clone, fork | 誰でもOK |
| issue | 誰でもOK |
| Pull Request | 権限が必要 |

---

## Foundation版のコントリビュート方法

+++

### GitHub

- [OpenFOAM-dev](https://github.com/OpenFOAM/OpenFOAM-dev)としてGitHub上で開発
- 最新リリース版は**OpenFOAM-V7**

![GitHub Register](symposium/Presentation/fig/openfoam-dev-toppage.png)

+++

### Foundation版のissue

- [専用サイト](https://bugs.openfoam.org/)で行われる(GitHub上ではない)
- 申請すれば誰でもViewer→Reporterに権限が変わる

![issueTracking](symposium/Presentation/fig/issueTracking.png)

+++

### Foundation版まとめ

| リモートレポジトリ | GitHub |
| レポジトリ名 | OpenFOAM-dev |
| clone, fork | 誰でもOK |
| issue | 誰でもOK([専用サイト](https://bugs.openfoam.org/)) |
| Pull Request | 権限が必要 |

---

## ESI版とFoundation版 まとめ

|   | ESI版 | Foundation版 |
| :---: | :---: | :---: |
| 運営 | [ESI-OpenCFD](https://openfoam.com/) | @size[80%]([OpenFOAM Foundation Ltd](https://openfoam.org/)) |
| リモートレポジトリ | GitLab | GitHub |
| レポジトリ名 | ~~[OpenFOAM-plus](https://develop.openfoam.com/Development/OpenFOAM-plus)~~ [openfoam](https://develop.openfoam.com/Development/openfoam/) | [OpenFOAM-dev](https://github.com/OpenFOAM/OpenFOAM-dev) |
| clone, fork | 誰でもOK | 誰でもOK |
| issue | 誰でもOK([GitLab](https://bugs.openfoam.org/)) | 誰でもOK@size[80%](([専用サイト](https://bugs.openfoam.org/))) |
| Pull Request | 権限が必要 | 権限が必要 |

---

## OpeFOAM-jp

+++

### 目的

- コントリビュートの最初の一歩として
- OpenFOAMの開発をやってみたい
- 日本のコントリビュート活動の活性化
- Gitとかの練習をしたい

+++

### issues

- [issuesレポジトリ](https://github.com/OpenFOAM-jp/issues)を単独で作成（[vim-jp/issues](https://github.com/vim-jp/issues)のfork）
- 日本コミュニティ内でのOpenFOAMに関する議論の場
- 機能追加やチュートリアルの作成などの発案、開発に使用
- 質問は[Google Group](https://groups.google.com/forum/#!forum/openfoam)へ
- もちろん誰でも参加可能

![issueTracking](symposium/Presentation/fig/issueTracking.png)

+++

### OpenFOAM-jp

- OpenFOAM-devのfork
- 誰でもfork, Pull Requestが可能
- 事前にissuesを作成することを推奨
- インストール方法は[こちら](https://github.com/OpenFOAM-jp/issues/wiki/インストール手順)

+++

### OpenFOAM-jpまとめ

| レポジトリ名 | OpenFOAM-jp |
| :---: | :---: |
| リモートレポジトリ | GitHub |
| clone, fork | 誰でもOK |
| issue | 誰でもOK([GitHub](https://github.com/OpenFOAM-jp/issues)) |
| Pull Request | 誰でもOK |

---

## ここまでのまとめ

|   | ESI版 | Foundation版 | OpenFOAM-jp |
| :---: | :---: | :---: | :---: |
| 運営 | [ESI-OpenCFD](https://openfoam.com/) | @size[80%]([OpenFOAM Foundation Ltd](https://openfoam.org/)) | OpenFOAM-jp |
| リモートレポジトリ | GitLab | GitHub | GiHub |
| レポジトリ名 | ~~[OpenFOAM-plus](https://develop.openfoam.com/Development/OpenFOAM-plus)~~ [openfoam](https://develop.openfoam.com/Development/openfoam/) | [OpenFOAM-dev](https://github.com/OpenFOAM/OpenFOAM-dev) | [OpenFOAM-jp](https://github.com/OpenFOAM-jp/OpenFOAM-jp)
| clone, fork | 誰でもOK | 誰でもOK | 誰でもOK |
| issue | 誰でもOK([GitLab](https://bugs.openfoam.org/)) | 誰でもOK@size[80%](([専用サイト](https://bugs.openfoam.org/))) | 誰でもOK([GitHub](https://github.com/OpenFOAM-jp/issues)) | 
| Pull Request | 権限が必要 | 権限が必要 | @color[#ffa500](誰でもOK) |

---

### OpenFOAM-jp/OpenFOAM-utilities-tutorials-jp

OpenFOAMのユーティリティに関するまとめ

![util](symposium/Presentation/fig/util-tut.png)

---

## GitHub および Travis による継続的インテグレーション

+++

### 動作例

+++

### .travis.ymlの例
+++

---

### バク報告

TODO: DockerFileを使ったバク報告の方法

---

### ローカライズ

TODO: Omegatを使用したドキュメント翻訳
TODO: エラーメッセージの翻訳について
