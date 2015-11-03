# Python/Bottleで学ぶWebアプリケーション開発基礎

HTTPについてざっと確認

## リクエストってどんなもの？

```
http://www.example.com:8000/foo?keyword=python&p=1#fragment
```

こういうURLを詳しく見て行きましょう

* `http`: プロトコル。HTTP(Hyper Text Transfer Protocol)
* `www.example.com`: ホスト名
* `:8000`: ポート番号(省略可)
* `/foo`: パス
* `?keyword=python&p=1`: クエリパラメータ。`name=value`形式。
* `#fragment`: ページのある部分を特定するために使用。サーバにはこのデータは送られない。

リクエストは **リクエストライン** から始まる。
HTTPはとってもシンプルなので、下のテキストがそのまま送信される。

```
GET /foo?keyword=python&p=1 HTTP/1.1
```

これも同じように詳しく見ていく

* `GET`: HTTPメソッド
    HTTPメソッドはいくつかあるが、最も使うのは`GET`と`POST`。GETはデータベースなどからデータを取り出す時だけに、POSTはデータを追加したり削除したりサーバ側に変更を加えたいときに使用する。

* `/foo?keyword=python&p=1`: URI
* `HTTP/1.1`: プロトコルバージョン。1.0か1.1の2通り

リクエストラインの下にはいくつかの **リクエストヘッダ** が続く。

```
HOST: www.example.com
User-Agent: Chrome v1.7 ...
:
:
```

リクエストヘッダは`Name: Value`の形式。ヘッダは自由に追加することができ、これによりリクエストにメタデータが追加される。

その下に空行が入り、メッセージボディが記述されている。
但し、HTMLや画像を取得するだけなら特にサーバに送信するデータはないため、空となっている。


## レスポンスってどんなもの？

レスポンスはリクエストラインのように **ステータスライン** から始まる

```
HTTP/1.1 200 OK
```

* `HTTP/1.1`: ここはリクエストラインと一緒。HTTPのバージョンも必ず対応
* `200`: ステータスコード
* `OK`: リーズンフレーズ

その後に **レスポンスヘッダ** が続く


## Chromeで確認

Dev tools > Network > Nameで調べたいやつを選択 > Headers

![Screenshot 2015-07-05 11.59.09.png](https://qiita-image-store.s3.amazonaws.com/0/29989/4e356562-08d5-adeb-5829-6e6989f0a708.png "Screenshot 2015-07-05 11.59.09.png")

View Sourceをクリックするとリクエストラインやステータスラインも確認出来る。



## 参考資料

* Pythonエンジニア養成読本
* [Full Stack Foundations - Udacity](https://www.udacity.com/course/full-stack-foundations--ud088)
* Bottle 公式サイト

