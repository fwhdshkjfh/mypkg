# mypkg
![test](https://github.com/fwhdshkjfh/mypkg/actions/workflows/test.yml/badge.svg)

- このリポジドリはROS2のパッケージです。
- ROS2をインストールしてない方は先にインストールをお願いします。
- ワークスペースにクローンを行ってください。

```
$ git clone https://github.com/fwhdshkjfh/mypkg.git
```


# talkerとlistener
- talkerはcountupというトピックを通じて、Int16型のメッセージを送信します。
- listenerはtalkerから送信されたInt16型のメッセージを受信して出力します。

## 入力と実行結果

- 端末を２つ用意して以下のように入力してください。

- 端末１
```
$ ros2 run mypkg talker
```
- 端末２
```
$ ros2 run mypkg listener
```
実行結果は以下のようになります。
- 端末２

```
[INFO] [1672476436.193100443] [listener]: Listen: 0
[INFO] [1672476436.681608776] [listener]: Listen: 1
[INFO] [1672476437.180927024] [listener]: Listen: 2
[INFO] [1672476437.681568509] [listener]: Listen: 3
[INFO] [1672476438.182847778] [listener]: Listen: 4
[INFO] [1672476438.682286210] [listener]: Listen: 5
(以下略)
```

# launchファイル
- launchファイルを使うことで, 複数のノードを同時に立ち上げることができます.
## 入力と実行結果
```
$ ros2 launch mypkg talk_listen.launch.py
[listener-2] [INFO] [1672477023.148972899] [listener]: Listen: 0
[listener-2] [INFO] [1672477023.639290728] [listener]: Listen: 1
[listener-2] [INFO] [1672477024.139078930] [listener]: Listen: 2
[listener-2] [INFO] [1672477024.635796765] [listener]: Listen: 3
[listener-2] [INFO] [1672477025.139608277] [listener]: Listen: 4
[listener-2] [INFO] [1672477025.639072606] [listener]: Listen: 5
(以下略)
```

# 必要なソフトウェア
- ROS2 foxy

# テスト環境
- ubuntu20.04LTS

# ライセンス
- このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
-  このパッケージのコードは、下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを、本人の許可を得て自身の著作としたものです。
- [ryuichiueda/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)

© 2022 shou uchida




