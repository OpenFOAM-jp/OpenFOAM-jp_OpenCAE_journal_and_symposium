### OpenFOAMコントリビュート活動

- 稲葉竜一
- @tkoyama010
- 松原大輔

---

### 目次

- gitを使ったossの開発
- OpenFOAM Foundation版とESI版の違い
- ESI版
- Foundation版
- OpeFOAM-jp
- プロジェクトの例

---

@snap[north span-100]

## gitを使ったOSSの開発

@snapend

![git all](symposium/Presentation/fig/git.png)

+++

@snap[north span-100]
## gitとは？
@snapend
  
- 分散型プロジェクト管理システム
- 複数人の同時作業に適している
- OSSの開発や管理に使用されていることが多い
- web上のplatformとしてGitHubやGitLabなどがある

+++

@snap[north span-100]
### issue

- バグ報告, 機能の要望, 予定, 開発など
@snapend  
![GitHub issue](symposium/Presentation/fig/gitissue.png)

+++

@snap[north span-100]
### branchの考え方

- 目的別、作業者別に同時並行で編集可能
- 本体への影響を与えない
- 不具合発生時に問題の切り分けなどが容易になる

@snapend  
![GitHub branch](symposium/Presentation/fig/PR2.png)

+++

@snap[north span-100]
### 手元のPCでの操作
@snapend

![git operation](symposium/Presentation/fig/gitlocal.png)

+++

@snap[north span-100]
### 操作例
@snapend
 
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

@snap[north span-100]
### プルリクエストを送る
@snapend

GitHubなどのweb上で行う

![git operation](symposium/TeX/fig/fig-f4.png)

+++


@snap[north span-100]
## まとめ
@snapend

![git all](symposium/Presentation/fig/git.png)

---

## OpenFOAM Foundation版とESI版の違い

+++

@snap[north span-100]
### OpenFOAM
@snapend

- Imperial Collageで開発された商用ソルバー"FOAM"がベース
- 2004年にオープンソース化
- その後いくつかのForkができる
  - Foundation版：OpenFOAM Foundation Inc.によるFork
  - ESI版：ESI社とOpenCFD社によるFork
  
---

## ESI版のコントリビュート方法

+++


@snap[north span-100]
### ESI版
@snapend

- ~~[OpenFOAM-plus](https://develop.openfoam.com/Development/OpenFOAM-plus)としてGitLabで開発~~
- **@color[#ff0000](<NEW!!>)[openfoam](https://develop.openfoam.com/Development/openfoam/)としてGitLabで開発**

![GitLab Register](symposium/Presentation/fig/gitlab_top.png)

+++

@snap[north span-100]
### issue
@snapend

バグ報告, 機能の要望, 導入予定の機能の審議と開発など
  
![issue sample](symposium/Presentation/fig/gitlabIssues.png)

+++

@snap[north span-100]
### issueの立て方
@snapend

- issuesのページの右上のNew Issueボタンから作成する

![GitLab issue](symposium/Presentation/fig/gitlab_issue.png)

+++

@snap[north span-100]
### issueを立ててみた
@snapend

- 簡単なtypoのissue

![plus issue](symposium/TeX/fig/plus_issue.png)

+++

@snap[north span-100]
### Pull Requestなど
@snapend

- プロジェクトメンバーのみがPull Requestなどを行うことができる
- メンバーに加入するには専用ページから申し込む
- ただし現在14人しかいないほど狭き門

![plus issue](symposium/Presentation/fig/com_contactus.png)

+++

@snap[north span-100]
### ESI版まとめ
@snapend

| repository | ~~OpenFOAM-plus~~ [openfoam](https://develop.openfoam.com/Development/openfoam/) | 
| :---: | :---: |
| platform | GitLab |
| clone, fork | 誰でもOK |
| issue | 誰でもOK |
| Pull Request | 権限が必要 |

---

## Foundation版のコントリビュート方法

+++

@snap[north span-100]
### Foundation版
@snapend

- [OpenFOAM-dev](https://github.com/OpenFOAM/OpenFOAM-dev)としてGitHub上で開発
- 最新リリース版は**OpenFOAM-V7**

![GitHub Register](symposium/Presentation/fig/openfoam-dev-toppage.png)

+++

@snap[north span-100]
### Foundation版のissue
@snapend

- [専用サイト](https://bugs.openfoam.org/)で行われる(GitHub上ではない)
- 申請すれば誰でもViewer→Reporterに権限が変わる

![issueTracking](symposium/Presentation/fig/issueTracking.png)

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
| platform | GitHub |
| clone, fork | 誰でもOK |
| issue | 誰でもOK([専用サイト](https://bugs.openfoam.org/)) |
| Pull Request | 権限が必要 |

---

## OpeFOAM-jp

+++

@snap[north span-100]
### 目的
@snapend

- コントリビュートの最初の一歩として
- OpenFOAMの開発をやってみたい
- 日本のコントリビュート活動の活性化
- Gitとかの練習をしたい

+++

@snap[north span-100]
### issues
@snapend

- [issuesレポジトリ](https://github.com/OpenFOAM-jp/issues)を単独で作成（[vim-jp/issues](https://github.com/vim-jp/issues)のfork）
- 日本コミュニティ内でのOpenFOAMに関する議論の場
- 機能追加やチュートリアルの作成などの発案、開発に使用
- 質問は[Google Group](https://groups.google.com/forum/#!forum/openfoam)へ
- もちろん誰でも参加可能

![issueTracking](symposium/Presentation/fig/issueTracking.png)

+++

@snap[north span-100]
### OpenFOAM-jp
@snapend

- OpenFOAM-devのfork
- 誰でもfork, Pull Requestが可能
- 事前にissuesを作成することを推奨
- インストール方法は[こちら](https://github.com/OpenFOAM-jp/issues/wiki/インストール手順)

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
## 各forkのまとめ
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

@snap[north span-100]
## ユーティリティのチュートリアル
@snapend

@snap
情報の少ないOpenFOAMのユーティリティについてまとめを作成

![util](symposium/Presentation/fig/util-tut.png)
@snapend

+++

@snap[north span-100]
## 継続的インテグレーション（CI）
@snapend

@snap
- push時の自動でテストシステム
- Pull Requestの承認の際の指標になる
- テスト内容は自分で作成する

![ci](symposium/Presentation/fig/ci.png)

@snapend

+++

@snap[north span-100]
### CI動作例
@snapend

@snap
- 本発表の梗概を共同制作
- Travis CIを活用
- 各branchをTeXで作成→push→Pull Request
- CIが通っていればmerge

![ci](symposium/Presentation/fig/ci-sample.png)
@snapend

+++

## 機能追加 

- mergeMeshesのオプションの改造
- snappyHexMeshのスムージング機能独立
- transformPointsのコピーオプション追加

@size[300%](@color[#0000ff](随時募集中！（issueへ）))

+++

## ドキュメントの翻訳

---

## まとめ

- ESI版とFoundation版はissueを送ることでコントリビュートできる
- ただし実際に書いたコードを反映させることは権限がないとできない
- 開発をやってみたい人のためにOpenFOAM-jpを作ってみた
- 参加者募集中！
- やってみたいことがあったらissueへ！

---

### バグ報告

TODO: DockerFileを使ったバク報告の方法

---

### ローカライズ

TODO: Omegatを使用したドキュメント翻訳
TODO: エラーメッセージの翻訳について
