# GitHub Restaurant

レストランを題材にGit、GitHubの練習をするためのリポジトリです。

## 役割
- 客
  - 料理をオーダーする
  - 料理を受け取る

- コック(複数名を想定)
  - オーダーを受ける
  - 調理をする
  - 料理を出す

## 作業フロー
[GitHub フロー](https://docs.github.com/ja/get-started/quickstart/github-flow)を使用します。


## 0.オーダーを作成する
客役が行う作業

1. GitHubでIssue（イシュー）を立てる(作成する)
2. Issueに注文したい料理名を書く
3. コックにIssueを割り当てる
4. 上記をコック分行う

## 1.オーダーを受ける
コック役が行う作業

### 1−1.割り当てられたIsueeを確認する

割り当てられたIssueにコメントを書く

### 1−2.作業ブランチを作成する

ローカルでmainブランチから作業ブランチを作成する

ブランチ名のルール：
>**order-[number]-[menu-name]**

例：

1回目のオーダー、カレーライスの場合
>order-1-curry_rice

1回目のオーダー、牛丼の場合
>order-1-beef_bowl

1回目のオーダー、ポテトサラダの場合
>order-1-potato_salad

リモートリポジトリに作業ブランチをpushする

## 2.調理する
コック役が行う作業

### 2−1.foodstuff.mdの表を編集する
メニューを調理するのに必要な食材の在庫数を変更する

例：

カレーライスの場合
>肉、玉ねぎ、じゃがいも、にんじんの在庫数からそれぞれ１減らす

牛丼の場合
>肉、玉ねぎの在庫数からそれぞれ１減らす

ポテトサラダの場合
>玉ねぎ、じゃがいも、にんじんの在庫数からそれぞれ１減らす

### 2-2.作業ブランチにコミットする

作業ブランチに1つ目のコミットを作成する

### 2-3.dish.mdの表を編集する

調理したメニューの調理数を増やす

### 2-4.作業ブランチにコミットする

作業ブランチに2つ目のコミットを作成する

### 2-5.作業ブランチをリモートリポジトリにpushする

作業ブランチをリモートリポジトリにpushする

## 3.料理を出す
コック役が行う作業

1. GitHub上でPull Request(プルリクエスト)を作成する
2. Pull RequestとIssueを紐付ける
3. Assigneeに客を設定する

## 4.料理を受け取る
客役が行う作業

1. GitHub上でPull Request(プルリクエスト)を確認する
2. Pull Requestを閉じる

## Pull Requestに失敗した場合
コック役が行う作業

1. リモートリポジトリの変更をfetchする
2. ローカルのmainブランチにmergeする
3. ローカルのmainブランチからローカルの作業ブランチにmergeする
4. コンフリクトを解決する
5. ローカルの作業ブランチでコミットを作成する
6. ローカルの作業ブランチをリモートの作業ブランチにpushする
7. Pull Requestを修正する

## 4.参考

### ブランチ戦略
- [GitHub Flow](https://docs.github.com/ja/get-started/quickstart/github-flow)
- [git flowとgithub flow　開発運用方法の違い](https://qiita.com/Yu-kiFujiwara/items/40b503683d6525c8d274)

### リポジトリ戦略
- [モノレポ入門](https://zenn.dev/anneau/articles/4c9beff9645af7)
- [モノレポについて.md](https://gist.github.com/pipopotamasu/efe7097454d9668f80cd8b43068afafc)

### GitHub Issue/Pull Request
- [GitHubで課題を管理する便利機能Issueとその作成方法](https://tonari-it.com/github-issue/)
- [GitHubでIssueについて解決してクローズするまでの手順](https://tonari-it.com/github-issue-close/)
- [Pull RequestをIssueにリンクする](https://docs.github.com/ja/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue)

### Git操作
- [The Official GitHub Training Manual](https://githubtraining.github.io/training-manual/#/ja/)
- [GitHub GITチートシート](https://training.github.com/downloads/ja/github-git-cheat-sheet.pdf)
