# vue-docker

[参考記事](https://qiita.com/leafeon00000/items/09384726105eee53bbb6)

<hr>

- [ここ](https://www.docker.com/)にアクセスし、dockerをインストールする。

## Dockerfileの書き方

- ``FROM``:Dockerfileの一番はじめに記載。イメージのベースを記載する。
- 書き方:``FROM プログラム:バージョン``

例）``FROM node:15.11.0``

- ``WORKDIR``:Dockerの作業をどのパスで行うか記載する。*※ディレクトリが無ければ勝手に作成される。*
- 書き方:``WORKDIR パス``

例）``WORKDIR /vue_app``

- ``COPY``:Dockerが動いているディレクトリにコピーする。
- 書き方:``COPY コピー前パス コピー後パス``

例）``COPY ./vue_app/ .``

- ``RUN``:コマンド実行
- 書き方:``RUN コマンド``

例）``RUN npm install``

- ``CMD``:docker run時に実行されるコマンドを指定します。
- 書き方:``CMD ["実行バイナリ", "パラメータ１", "パラメータ２"]``

例）``CMD ["npm", "run", "serve"]``

その他詳しくは[こちら](https://www.wakuwakubank.com/posts/270-docker-build-image/#dockerfileで利用できる命令)

