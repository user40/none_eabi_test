# none_eabi_test
Dockerを使ってarm-none-eabi-gccのビルド環境を構築するテストです。
## How to use
VSCodeのGUIからイメージをビルドしたあとに、ターミナルに
```
docker run -i -t -v "$PWD"/sample_program:/home [containerID]
```
と入力してコンテナを実行します。
