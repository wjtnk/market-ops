## 準備
1.このディレクトリをclone  
```
cd path/to/workdir
git clone git@github.com:wjtnk/market-ops.git
```

2.アプリのディレクトリを「market-ops/market」以下にclone  
```
cd path/to/workdir/market-ops/market
git clone git@github.com:wjtnk/market.git .
```

3.docker起動  
```
cd path/to/workdir/market-ops
docker-compose up -d
```

## 最初にやること
1.コンテナの中に入る  
```
docker exec -it market-ops_rails_1 bash
```
2.bundle install  
```
bundle install --path vendor/bundle
```
3.キャッシュを有効にする
```
rails dev:cache
```

## サーバー起動  
1.コンテナの中に入る  
```
docker exec -it market-ops_rails_1 bash
```
2.サーバー起動  
```
bundle exec rails s -p 3000 -b '0.0.0.0'
```

## dockerよく使うコマンド

```
# 修正した設定を反映し起動 
$ cd ~/path/to/market-ops
$ docker-compose up -d --build

# 停止
$ cd ~/path/to/market-ops
$ docker-compose stop

# 削除
$ cd ~/path/to/market-ops
$ docker-compose down
```
