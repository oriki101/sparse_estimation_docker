# sparse_estimation_docker
![windows](https://img.shields.io/badge/buid_windows-pass-green.svg?style=flat)
![Ubuntu](https://img.shields.io/badge/buid_ubuntu-pass-green.svg?style=flat)

Joe先生のスパース推定100問のプログラムを実行するためのdockerイメージです。

# Dependency
- [Docker for windows](https://docs.docker.com/docker-for-windows/install/) (Windowx環境で実行する場合)
- [Docker](https://docs.docker.com/engine/install/) (Linuxで実行する場合)

# Quick Start
## Windows
### 初回実行時
```
$git clone https://github.com/oriki101/sparse_estimation_docker.git
$cd sparse_estimation_docker/docker
$docker_build.bat
```

### コンテナ起動
```
$cd sparse_estimation_docker/docker
$compose_up.bat (またはフォルダ内でcompose_up.batをダブルクリック)
```

### コンテナ停止
```
$compose_down.bat (またはフォルダ内でcompose_down.batをダブルクリック)
```

## Linux
### 初回実行時
sparse_estimation_docker/docker/ディレクトリ内の*.batのファイルを*.shというファイルにリネーム
```
$git clone https://github.com/oriki101/sparse_estimation_docker.git
$cd sparse_estimation_docker/docker
$sh compose_up.sh
```
### コンテナ停止
```
$sh compose_down.sh
```

## JupyterLabにアクセス
ウェブブラウザ内で以下のurlにアクセス

[localhost:8888](localhost:8888)

# イメージの説明
JupyterLab上の/work/ディレクトリにsparse_estimation_docker/src/ディレクトリをマウントしている。つまり、work内で作成したプログラムはsrcディレクトリに保存される。
