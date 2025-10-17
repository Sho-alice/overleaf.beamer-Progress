# 大山研スライドテンプレート

Overleafを使う場合、事前にOverleafのアカウント設定でGitHubアカウントとの連携を有効にすること。

## 新しいスライドを作る方法

1. ページ右上の**Use this template**ボタンを押す
2. **Owner**を自分のアカウントに切り替える
3. **Repository name**を設定する（例：`progress-20250101`）
   - 毎回新しいリポジトリを作るようにして、使い回さないことを推奨
4. **Choose visibility**はPrivateのままにする
5. **Create repository**ボタンを押してリポジトリを作成する
6. Overleafを開き、[**New project**ボタンを押して**Import from GitHub**を選ぶ](https://docs.overleaf.com/integrations-and-add-ons/git-integration-and-github-synchronization/github#creating-a-new-overleaf-project-from-a-github-repository)
7. 先ほど作ったリポジトリをインポートする
8. プロジェクトの設定（アカウントの設定ではない）を開き、コンパイラを**pdfLaTeX**から**LaTeX**に変更する
   - 付属している`latexmkrc`の設定により、**LaTeX**を選択するとupLaTeXが使われる
   - これを行わないと、`\renewcommand{\kanjifamilydefault}{\gtdefault}`でエラーが出る
9. 必ず変更する箇所を忘れずに変更する
   - `\title{...}`
   - `\author{...}`
   - `\date{...}`
10. [変更した原稿をGitHubと同期する](https://docs.overleaf.com/integrations-and-add-ons/git-integration-and-github-synchronization/github#synchronizing-with-github)
11. スライドを書く
12. こまめに原稿をGitHubと同期する
13. 完成したスライドをIndicoやMattermostなどにアップロードする前に、忘れずにサンプルページを削除する

## テンプレートに変更を加える方法

毎回この`\usepackage{...}`を書いてる、この画像は皆がよく使うと思う、デザインをもっと良くする方法を見つけた、など、毎回自分のリポジトリでやるよりもテンプレート自体を更新した方がいい場合があります。

その場合は、このリポジトリを`git clone`して、自分の名前を含むわかりやすい名前のブランチを作り（例：`git switch -c ogino-add-more-packages`）、変更を加えて`git commit`と`git push`をして、プルリクエストを作ってください。

他のメンバーは変更内容を確認し、今後作られる全員のスライドにその変更が加えられても問題なさそうならマージしてください。

全員にこのリポジトリの管理者権限を与えるので、まだもらっていないのであれば他のメンバーに依頼してください。
