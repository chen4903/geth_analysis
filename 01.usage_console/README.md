# 快速入门

## 环境配置

推荐使用Linux系统，容易代码运行调试，本仓库基于下面的配置

- Ubuntu20.04
- nodejs：v10.19.0
- npm：6.14.4
- go：go version go1.21.0 linux/amd64
- git：git version 2.25.1
- vscode（不要在ubuntu软件商店下载，因为是阉割版）

## 安装geth

推荐使用源码安装

1.从仓库拉取：

```
# PoW版本，1.12之后是PoS版本
git clone -b v1.10.0 https://github.com/ethereum/go-ethereum.git
```

2.从源码编译：进入到go-ethereum目录，输入`make geth`。

```
github.com/ethereum/go-ethereum/cmd/geth
Done building.
Run "./build/bin/geth" to launch geth
```

3.添加到环境变量`/etc/profile`，可以快速启动：任何地方输入geth即可启动

```
export PATH=$PATH:/opt/go-ethereum/build/bin
```

4.查看版本：`geth version`

```shell
root@LEVI:/opt/go-ethereum# geth version
Geth
Version: 1.10.0-stable
Git Commit: 56dec25ae26bf749b93c3ea69538fabea60c5768
Architecture: amd64
Go Version: go1.21.0
Operating System: linux
GOPATH=
GOROOT=
```













