# docker-laravel-handson
DockerでLaravel8の開発環境を構築

## 環境構築手順
※ 前提条件：Docker, Docker Composeが導入済であること

### ① Dockerイメージをビルドしてコンテナーを起動
```
$ docker-compose up -d --build
```
### ② コンテナーに接続
```
$ docker-compose exec app bash
```

### ③ PHPライブラリをインストール
```
$ composer install
```

### ④ .envファイルを作成
```
$ cp .env.example .env
```

### ⑤ アプリケーションキーを作成
```
$ php artisan key:generate
```

### ⑥ マイグレーションを実行
```
$ php artisan migrate
```

### ⑦ コンテナーから切断
```
$ exit
```

### ⑧ ブラウザから接続確認
```
http://127.0.0.1:10080/
```

## 参考にした記事
[【初心者向け】20分でLaravel開発環境を爆速構築するDockerハンズオン](https://qiita.com/ucan-lab/items/56c9dc3cf2e6762672f4)
