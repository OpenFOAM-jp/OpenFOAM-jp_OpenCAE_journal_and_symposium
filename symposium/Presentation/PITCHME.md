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

## ESI版のコントリビュート方法

+++

### GitLab

- ESI版は[OpenFOAM-plus](https://develop.openfoam.com/Development/OpenFOAM-plus)としてGitLabで開発されている
- この中の最新リリース版がOpenFOAM-v1906
- GitLabは各開発レポジトリ毎にユーザー登録を行う必要がある
- 登録はページの右上のRegisterボタンから行うことができる
- `git clone`によりダウンロード可能

![GitLab Register](symposium/TeX/fig/plus_register.png)

+++

### issue

<!-- ---?image=symposium/Presentation/fig/gitlabIssues.png&size=auto 60% -->

- 登録を行うとissueを立てることができるようになる
- issueでは以下のような議論が行われている
  - バグ報告
  - 機能の要望
  - 導入予定の機能の審議と開発
  
<img src="symposium/Presentation/fig/gitlabIssues.png" title="git issue sample" width="500">

+++

### issueの立て方

- ~~issuesのページの右上のNew Issueボタンから作成する~~
- 12月頭からissue機能が使用できない状況
- (v1912リリースの影響？)

+++

### issueを立ててみた

- 簡単なtypoのissue
- 立ててから数日後に@mark氏により修正された
- こういう細かな報告も重要

<img src="symposium/TeX/fig/plus_issue.png" title="git issue sample" width="500">

+++

### まとめ

- ESI版はGitLabで開発されている
- issueの作成は-誰でもできる-現在は権限が必要
- 権限を得るためにはESI社との交渉が必要 

---

## Foundation版のコントリビュート方法

+++

### GitHub

- Foundation版は[OpenFOAM-dev](https://github.com/OpenFOAM/OpenFOAM-dev)としてGitHub上で開発されている
- この中の最新リリース版がOpenFOAM-V7
- `git clone`のみであればGitHubアカウントの登録も必要ない

![GitHub Register](symposium/Presentation/fig/openfoam-dev-toppage.png)

+++

### Foundation版のissue

- Foundation版のissueはGitHub上ではなくissueTrackingで行われる

<img src="symposium/Presentation/fig/issueTracking.png" title="git issue sample" width="600">

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

---

## Gitの使い方

TODO: イシューの立て方
TODO: ブランチの考え方
TODO: プルリクエストの立て方

+++

### 基本操作（ターミナル）

```sh
git checkout develop
# 作業をする
git add *
git commit -m "#16 test"
git push develop origin
```

@[1]("develop"ブランチに切り替え)
@[2-3](作業したらaddで変更点を読み込む)
@[4](コメントをつけてコミット)
@[5](リモートブランチにプッシュ)

+++

### git clone：OpenFOAM-jpの導入

+++

### ブランチを切る

+++

### プルリクエストを送る

---

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

+++

### OpenFOAM-jp

+++

### OpenFOAM-jp/OpenFOAM-utilities-tutorials-jp

<iframe class="stretch" data-src="https://github.com/OpenFOAM-jp/OpenFOAM-utilities-tutorials-jp/blob/master/v1906/mesh/manipulation/moveDynamicMesh/moveDynamicMesh.md"></iframe>

---

+++

---

### バク報告

TODO: DockerFileを使ったバク報告の方法

---

### ローカライズ

TODO: Omegatを使用したドキュメント翻訳
TODO: エラーメッセージの翻訳について
