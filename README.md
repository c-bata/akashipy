# akashi.py

## 講義ノート

ipython notebookで`notebooks/`以下に講義ノートを作成しています。
あんまり考えずに作ってるのでこうした方がいいとかあれば言って下さい。
Pull Request送ってくれても大丈夫です。


## ipython notebook

#### 実行

```
$ ipython notebook
```

コマンドモードで`h`を入力するとヘルプが見れます。

#### スライドとして表示

```
$ ipython nbconvert python_grammer.ipynb --to slides --post serve
```


## 方針・内容

1. PyCharmで統一
    * 環境のsetup
    * Pythonエンジニア養成読本を見ながら基礎
    * 無理にオブジェクト指向をつめ込まない
    * javaと違って…
2. Webアプリの開発
    * virtualenvの使い方(pycharm)
        * 画像もgrubboxで撮ってgithubにあげる
    * flask
3. ペアプロ

自分がメモとしてまとめたい内容を中心に教えていってもいいかも

* Flask、SQLAlchemy
* pdb
* ipython
* unittest, tdd
* flake8, tox
* doctest, sphinx
* パッケージング
* PyData


## 方針・今後やってみたいこと

ペアプロベース。最初に教えた人たちにTA手伝ってもらう。

* githubで資料を共有して復習できるようにする
  * ipython notebookで講義しながら資料を作成 -> notebooks
  * src に講義で作成したプログラムをcommitしていく
* こういうの作りましたとかこういうこと勉強しましたっていうのを5分ぐらいLTしてもらうといいかも

