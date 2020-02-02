# 使い方

## Dockerイメージの作成
docker-compose build

## Dockerコンテナの作成
docker-compose up -d

## コンテナをコミットする必要があるので以下コマンドを実行する
### エラーのでているコンテナIDを取得
docker ps -q --filter status=exited

### コンテナをコミット
docker commit -m "exited" コンテナID

## コンテナへ接続
docker exec -it コンテナID bash
