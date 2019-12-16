### OpenFOAMコントリビュート活動

- 稲葉竜一
- @tkoyama010
- 松原大輔

---

### 目次

- OpenFOAM Foundation版とESI版の違い
- ESI版のコントリビュート方法
- Foundation版のコントリビュート方法
- Gitの使い方
- GitHub および Travis による継続的インテグレーション
- OpeFOAM-jp

---

## OpenFOAM Foundation版とESI版の違い

+++

### OpenFOAM

- Imperial Collageで開発された商用ソルバー"FOAM"がベース
- 2004年にオープンソース化
- その後いくつかのForkができる
  - Foundation版：OpenFOAM Foundation Inc.によるFork
  - ESI版：ESI社とOpenCFD社によるFork
  - foam-extend:
  - RapidCFD:
  
---

## gitを使ったOSSの開発
  
![git all](symposium/Presentation/fig/git.png)

+++

### issue

- バグ報告, 機能の要望, 導入予定の機能の審議と開発など
- 気づいたことはこまめにコメントを残す
  
![GitHub issue](symposium/Presentation/fig/gitissue.png)

+++

### branchの考え方

- 目的別、作業者別に同時並行で編集可能
- 本体への影響を与えない
- 不具合発生時に問題の切り分けなどが容易になる

![GitHub branch](symposium/Presentation/fig/PR2.png)

+++

### 手元のPCでの操作

- リモートとのやりとり : 
  - clone（ダウンロード）
  - pull（更新）
  - push（アップロード）
- ローカル : 
  - checkout（branch切り替えor作成）
  - add（選択）
  - commit（登録）

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

## ESI版のコントリビュート方法

+++

### GitLab

- [OpenFOAM-plus](https://develop.openfoam.com/Development/OpenFOAM-plus)としてGitLabで開発
- この中の最新リリース版がOpenFOAM-v1906

![GitLab Register](symposium/TeX/fig/plus_register.png)

+++

### issue

<!-- ---?image=symposium/Presentation/fig/gitlabIssues.png&size=auto 60% -->

議論対象：バグ報告, 機能の要望, 導入予定の機能の審議と開発など
  
![issue sample](symposium/Presentation/fig/gitlabIssues.png)

+++

### issueの立て方

- ~~issuesのページの右上のNew Issueボタンから作成する~~
- 12月頭からissue機能が使用できない状況
- (v1912リリースの影響？)

+++

### issueを立ててみた

- 簡単なtypoのissue

![plus issue](symposium/TeX/fig/plus_issue.png)

+++

### まとめ

- ESI版はGitLabで開発されている
- issueの作成は-誰でもできる-現在は権限が必要
- 権限を得るためにはESI社との交渉が必要 

---

## Foundation版のコントリビュート方法

+++

### GitHub

- [OpenFOAM-dev](https://github.com/OpenFOAM/OpenFOAM-dev)としてGitHub上で開発
- この中の最新リリース版がOpenFOAM-V7

![GitHub Register](symposium/Presentation/fig/openfoam-dev-toppage.png)

+++

### Foundation版のissue

- issueTrackingで行われる(GitHub上ではない)

![issueTracking](symposium/Presentation/fig/issueTracking.png)

+++

## Pull Requestを送ってみた

1. まずは自分のGitHubアカウントを作る
2. issueTrackingに登録
3. issueを立てる
4. OpenFOAM-devを自分のレポジトリにForkする
5. ブランチを作成する
6. `git clone`で自分のローカルマシンへダウンロード
7. 内容を変更する
8. 自分のブランチへプッシュする
9. OpenFOAM-devのdevelopブランチへPull Requestを送る

+++

### 自分のForkの作成

![Create Fork](symposium/TeX/fig/fig-f1.png)

+++

### ブランチの作成

![myFork](symposium/TeX/fig/fig-f2.png)

+++

### `git clone`で自分のローカルマシンへダウンロード

![myFork](symposium/TeX/fig/fig-f3.png)

+++

### Pull Requestを送る

![myFork](symposium/TeX/fig/fig-f4.png)

## GitHub および Travis による継続的インテグレーション

+++

### 動作例

+++

### .travis.ymlの例

---

## OpeFOAM-jp

+++

### 目的

+++

### issues

- 日本コミュニティ内でのOpenFOAMに関する議論の場
- 質問掲示板ではない

+++

### OpenFOAM-jp

- OpenFOAM-devのFork
- Gitの練習などで使用してもらえたら

+++

### OpenFOAM-jp/OpenFOAM-utilities-tutorials-jp

OpenFOAMのユーティリティに関するまとめ

![util](symposium/Presentation/fig/util-tut.png)

---

+++

---

### バク報告

TODO: DockerFileを使ったバク報告の方法

---

### ローカライズ

TODO: Omegatを使用したドキュメント翻訳
TODO: エラーメッセージの翻訳について
