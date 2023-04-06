# gendosu/docker-ruby

## Documentation

RubyのDockerイメージを作るDockerfileを管理します。

### ビルドする環境

Macの場合
Docker Desktop(v4.7.0以上)
もしくは
Linuxの場合
Docker CE(v20.10.13以上)

### ビルドの準備

##### 環境変数

最終的に登録するリポジトリのURL:TAGを環境変数に設定する

```
export REPOSITORY_URL=[[Docker hubのリポジトリURL]]
export REPOSITORY_TAG=[[Docker hubのリポジトリTAG]]
```

※REPOSITORY_URLの例
[user_name]/[repository_name]

※REPOSITORY_TAGの例
2.7.7
とか

##### Docker hubへのログイン

docker login

##### builderの設定

docker buildx create --name ruby_builder
docker buildx use ruby_builder

### ビルド方法（自動）

[GithubのActions](https://github.com/gendosu/docker-ruby/actions/workflows/build.yml)を開いて
`Run Workflow` をクリックする
ビルドしたいバージョンを指定してビルド実行する

### ビルド方法（手動）

2.7.7-bullseye
```
export REPOSITORY_URL=gendosu/ruby
export REPOSITORY_TAG=2.7.7-bullseye
docker buildx build --platform linux/amd64,linux/arm64 -t $REPOSITORY_URL:$REPOSITORY_TAG --push 2.7/bullseye
```
2.7.7-slim-bullseye
```
export REPOSITORY_URL=gendosu/ruby
export REPOSITORY_TAG=2.7.7-slim-bullseye
docker buildx build --platform linux/amd64,linux/arm64 -t $REPOSITORY_URL:$REPOSITORY_TAG --push 2.7/slim-bullseye
```

3.0.5-bullseye
```
export REPOSITORY_URL=gendosu/ruby
export REPOSITORY_TAG=3.0.5-bullseye-2023-03-24
docker buildx build --platform linux/amd64,linux/arm64 -t $REPOSITORY_URL:$REPOSITORY_TAG --push 3.0/bullseye
```
3.0.5-slim-bullseye
```
export REPOSITORY_URL=gendosu/ruby
export REPOSITORY_TAG=3.0.5-slim-bullseye-2023-03-24
docker buildx build --platform linux/amd64,linux/arm64 -t $REPOSITORY_URL:$REPOSITORY_TAG --push 3.0/slim-bullseye
```

3.1.3-bullseye
```
export REPOSITORY_URL=gendosu/ruby
export REPOSITORY_TAG=3.1.3-bullseye-2023-03-24
docker buildx build --platform linux/amd64,linux/arm64 -t $REPOSITORY_URL:$REPOSITORY_TAG --push 3.1/bullseye
```
3.1.3-slim-bullseye
```
export REPOSITORY_URL=gendosu/ruby
export REPOSITORY_TAG=3.1.3-slim-bullseye-2023-03-24
docker buildx build --platform linux/amd64,linux/arm64 -t $REPOSITORY_URL:$REPOSITORY_TAG --push 3.1/slim-bullseye
```

3.2.1-bullseye
```
export REPOSITORY_URL=gendosu/ruby
export REPOSITORY_TAG=3.2.1-bullseye-2023-03-24
docker buildx build --platform linux/amd64,linux/arm64 -t $REPOSITORY_URL:$REPOSITORY_TAG --push 3.2/bullseye
```
3.2.1-slim-bullseye
```
export REPOSITORY_URL=gendosu/ruby
export REPOSITORY_TAG=3.2.1-slim-bullseye-2023-03-24
docker buildx build --platform linux/amd64,linux/arm64 -t $REPOSITORY_URL:$REPOSITORY_TAG --push 3.2/slim-bullseye
```
