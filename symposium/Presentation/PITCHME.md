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
  
+++

## ESI版のコントリビュート方法

+++

### GitLab

- ESI版は[OpenFOAM-plus](https://develop.openfoam.com/Development/OpenFOAM-plus)としてGitLabで開発されている
- GitLabは各開発レポジトリ毎にユーザー登録を行う必要がある
- 登録はページの右上のRegisterボタンから行うことができる
- `git clone`によりダウンロード可能

![GitLab Register](symposium/TeX/fig/plus_register.png)

+++

### issue

- 登録を行うとissueを立てることができるようになる
- issueでは以下のような議論が行われている
  - バグ報告
  - 機能の要望
  - 導入予定の機能の審議と開発

![gitlabIssues](symposium/Presentation/fig/gitlabIssues.png&size=50%)

+++

### issueの立て方

- -issuesのページの右上のNew Issueボタンから作成する-
- 12月頭からissue機能が使用できない状況
- (v1912リリースの影響？)

+++

### issueを立ててみた

- 簡単なtypoのissue
- 立ててから数日後に@mark氏により修正された
- こういう細かな報告も重要

![gitlab issue example](symposium/TeX/fig/plus_issue.png)

+++

### まとめ

- ESI版はGitLabで開発されている
- issueの作成は-誰でもできる-現在は権限が必要
- 権限を得るためにはESI社との交渉が必要 

---

## Foundation版のコントリビュート方法

+++

### GitHub

+++

### Reporter登録

+++

### Pull Requestを送ってみた

---

## Gitの使い方

TODO: イシューの立て方
TODO: ブランチの考え方
TODO: プルリクエストの立て方

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

---

+++

---

### バク報告

TODO: DockerFileを使ったバク報告の方法

---

### ローカライズ

TODO: Omegatを使用したドキュメント翻訳
TODO: エラーメッセージの翻訳について
