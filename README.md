# docker-laravel-handson

## LEMP環境構築用
このディレクトリはLEMP(Laravel/Nginx/mysql/php)環境構築のために作成した。</br>
下記Qiita記事を参考にした。</br>
</br>
**【超入門】20分でLaravel開発環境を爆速構築するDockerハンズオン**</br>
URL : https://qiita.com/ucan-lab/items/56c9dc3cf2e6762672f4</br>

実際に使用する際は下記のとおり</br>
# GithubからリポジトリをClone</br>
[mac] % git clone "Github上のリポジトリURL"</br>
[mac] % cd docker-laravel-handson</br>
[mac] $ docker-compose up -d --build</br>
</br>
http://127.0.0.1:10080 にアクセス</br>

# 新しいApp構築後保存する場合はディレクトリ名を変更してpush

# 再度Docker環境を破棄する場合は
[mac] $ docker-compose down --rmi all --volumes --remove-orphans</br>
## プロジェクトを削除するのでGUIエディタを閉じておく
[mac] $ cd ..</br>
[mac] $ rm -rf docker-laravel-handson</br>
