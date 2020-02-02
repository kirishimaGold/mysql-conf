# 使い方

## Dockerイメージの作成
docker-compose build

## Dockerコンテナの作成
docker-compose up -d

-----

# うまくいかない時はコミットしてイメージ作成、イメージそのものを起動して確認

## コンテナをコミットする必要があるので以下コマンドを実行する
### エラーのでているコンテナIDを取得
docker ps -q --filter status=exited

### コンテナをコミット
docker commit -m "exited" コンテナID
3f3898912205d15bb8e2ac605036da1b76d2ecaf67eb77031364b4f94b704dca　←実行するとでてくる

## コンテナへ接続
docker run --rm -it 3f3898912205d15bb8e2ac605036da1b76d2ecaf67eb77031364b4f94b704dca bash
