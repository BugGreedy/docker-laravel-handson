# docker-laravel-handson

## LEMP環境構築用
このディレクトリはLEMP(Laravel/Nginx/mysql/php)環境構築のために作成した。</br>
下記Qiita記事を参考にした。</br>
</br>
**【超入門】20分でLaravel開発環境を爆速構築するDockerハンズオン**</br>
URL : https://qiita.com/ucan-lab/items/56c9dc3cf2e6762672f4</br>

実際に使用する際は下記のとおり</br>

**再度git Docker環境を破棄する場合は**</br>
```
[mac] % docker-compose down --rmi all --volumes --remove-orphans
```
***プロジェクトを削除するのでGUIエディタを閉じておく***</br>
```
[mac] % cd ..
[mac] % rm -rf docker-laravel-handson
```
ここまでしたら再度github上のリポジトリからCloneを行う。</br>
**GithubからリポジトリをClone**</br>
```
[mac] % git clone "Github上のリポジトリURL"
[mac] % cd docker-laravel-handson
[mac] % docker-compose up -d --build
```
http://127.0.0.1:10080 にアクセス</br>
/work/public/../vendor/autoload.php を開くのに失敗してエラーになっていることを確認</br>
appコンテナに入る</br>
```
[mac] % docker-compose exec app bash
```
vendorディレクトリにライブラリ群をインストール</br>
composer.lock ファイルを参照</br>
```
[app] $ composer install
```
再びhttp://127.0.0.1:10080 にアクセスして、"500｜Server Error"と表示される事を確認</br>
composer install 時は .env 環境変数ファイルは作成されないので、 .env.example を元にコピーして作成</br>
```
[app] $ cp .env.example .env
```

<!-- **新しいApp構築後保存する場合はディレクトリ名を変更してpush**</br> -->


