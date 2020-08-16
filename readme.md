## 最初にやること
1.コンテナの中に入る  
```
docker exec -it market-ops_rails_1 bash
```
2.bundle install  
```
bundle install --path vendor/bundle
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
docker-compose up -d --build

# 停止
$ cd ~/path/to/serected-ops
$ docker-compose stop

# 削除
$ cd ~/path/to/serected-ops
$ docker-compose down
```
