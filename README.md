# Git Lesson

## リモートリポジトリとローカルリポジトリとはそれぞれ何でしょうか？
 - リモートリポジトリ：ファイルやディレクトリの状態をネット上で複数人で共有できるように記録する場所
 - ローカルリポジトリ：開発者一人ひとりが使用するために自分のPC上にファイルやディレクトリを記録するための場所

## プッシュとマージの違いは何でしょうか？
 - プッシュはローカルの内容をリモートにアップすること
 - マージは別のブランチの作業内容を取り込むこと

## コミットとプッシュの違い
 - コミットはファイルの編集内容をローカルで登録すること
 - プッシュは編集内容をリモートに反映すること

## コミットのメッセージはどのように書いてあげるのが最適でしょうか？
 - 一目で変更内容がわかるように書く
  prefixを先頭につけて何に対する変更なのか見やすくしたり検索しやすくする。prefixの例として、feat（新しい機能）、fix（バグの修正）などが挙げられる。

## ローカルでマージするフローと、プルリクエストでマージするフローの違いは何でしょうか？
 - ローカルでマージするフローは別のブランチでの作業内容を取り込むこと。コマンドは git merge 'マージしたい作業内容があるブランチ名'  
  リモートリポジトリには取り込んだ作業内容は反映されない。
   反映させるにはリモートリポジトリにpushする必要があります。（git push origin 'リポジトリ名'）
 - プルリクエストでマージするフローは、作業したブランチの作業内容をリモートリポジトリにプッシュした後、リモートリポジトリで差分を取り込むターゲットブランチに作業内容（差分）を取り込む。リモートリポジトリにも取り込んだ内容が反映される

## コンフリクトを起こしてしまった場合、どう対処すべきですか？
 - 変更内容の差分を確認し、先にマージされた変更内容を取り込むか、後にマージしようとしている変更内容を取り込むか、エディタを使って両方の変更内容を取り込んだ処理で上書きすることで両方を取り込む