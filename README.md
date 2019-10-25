# github_memo
memo

・コマンド
git diff　：コミットしてるローカルのと作業ファイルとの差分を表示
git chekout -b ブランチ名 :ブランチ名。
git commit -m "コメント" ファイル名（もしくは -a）　:手元（../.gitとかにある）に保存　ファイル名を指定。
git push ユーザ名　ブランチ名：ネット上に挙げる。

gitk　：図示させる。

git status ：情報を見る

git add ファイル名：ファイルをコミットとかの追跡対象に入れる。

●やった事メモ。
・持ってくる。
$ pwd
/home/mech-user/semi_ws/src
クローンしてくる
$ git clone http://github.com/k-okada/jsk_demos
$ cd jsk_demos/
リモートを作る
$ git remote add Kanazawanaoaki http://github.com/Kanazawanaoaki/jsk_demos
$ git remote -v
Kanazawanaoaki	http://github.com/Kanazawanaoaki/jsk_demos (fetch)
Kanazawanaoaki	http://github.com/Kanazawanaoaki/jsk_demos (push)
origin	http://github.com/k-okada/jsk_demos (fetch)
origin	http://github.com/k-okada/jsk_demos (push)
ブランチを作る
$ git checkout add_jsk_2019_10_semi

・変更フェーズ
$ emacs -nw jsk_2019_10_semi/package.xml
変更を確認
$ git diff
ブランチを作る
$ git checkout -b kanazawa_naoaki

（コンフィグを設定）
$ git config --local user.email "naoaki65k@gmail.com"; git config --local user.name "Kanazawanaoaki"

コミットして保存
$ git commit -m "add my name and my email" jsk_2019_10_semi/package.xml 
自分のgitにプッシュする。
$ git push Kanazawanaoaki kanazawa_naoaki 

・プッシュしたのをプルリクエストする
githubのページをする。

(githubのマージをされて消してもいいから、git branch -d [ブランチ名])


・プルをする
ブランチを移動する。
$ git checkout add_jsk_2019_10_semi
プルをする。
$ git pull origin add_jsk_2019_10_semi


