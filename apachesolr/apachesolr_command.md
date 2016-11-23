# コマンド

すべてroot権限で実行

### 起動
```

$ bin/solr start
```

サービスとして登録した場合は下記でもOK

```
$ sudo service solr start
```

### 停止

```
$ bin/solr stop
```

サービスとして登録した場合は下記でもOK

```
$ sudo service solr stop
```

### 再起動

```
$ bin/solr restart
```

### サービスとして登録

```
$ solr-5.5.3/bin/install_solr_service.sh solr-5.5.3.tgz 
```

solrのアーカイブは`/opt/`配下にできていて、
ログなどは`/var`配下にできる

### コアの作成

```
$ cd /opt/solr/
$ bin/solr create -c [コア名]
```

### コアの削除

```
$ cd /opt/solr/
$ bin/solr delete -c [コア名]
```

### コアのリロード
```
$  curl 'http://localhost:8983/solr/admin/cores?action=RELOAD&core=[コア名]'
```

### データの登録

```
$ bin/post -c [コア名] [登録するファイル]
```



