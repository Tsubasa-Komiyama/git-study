# Gitの勉強

- git add コマンドで、リポジトリに変更情報を追加する
  - このことをステージングと言う
- git commit コマンドで、ステージングされた情報にコメントを付けてコミットできる
- git push コマンドで、ローカルのコミットをリモートのリポジトリに反映できる
- git tag コマンドでコミットにタグ付けできる
  - タグを追加すると、GitHub ではダウンロード用の zip ファイルが自動で作られる

# daily-meeting-team6
team6の議事録管理リポジトリ

## 手順

1. 'git fetch' でリモートとローカルの状況を確認
2. リモートに変更があれば 'git pull' でローカルを更新
3. 'git checkout -b ブランチ名' で作業ブランチに移動
4. notionで該当ページをmarkdownとcsvでエクスポート
5. ダウンロードされたzipを解凍
6. 解凍されたmarkdownの名前を変更してdaily-meeting-team6をcloneしたフォルダに保存
7. 'git add 対象ファイル名（.）' で対象ファイルを追加
8. 'git commit -m "コメント"' でコミット
9. 'git push' でリモートにプッシュ (~/.gitconfigを編集すると自動でブランチをリモートに追加 [here](## 備考))
10. GitHubのページでプルリクエストを送る
11. 誰かがApproveしたらMergeしてmainに反映

## 備考

- gitconfigに追加する内容 (場所: ~/.gitconfig)
  ```
  [push]
    autoSetupRemote = true
  ```
