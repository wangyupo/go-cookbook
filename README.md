# go-cookbook

一、[安装最新版 Go](https://github.com/wangyupo/go-cookbook/tree/main/一、安装最新版Go)

二、配置环境

打开 `Windows PowerShell` ，输入 `go env -w GO111MODULE=on`，开启 Go包管理。

开启包管理后，可以在任何目录下创建项目，最终会根据 go.mod 的依赖从 `GOPATH/pkg` 里找到依赖包并使用。

三、创建项目

创建文件夹后，用 GoLand 打开，使用 GoLand 自带终端输入 `go mod init github.com/wangyupo/xxx`。

注：`github.com/wangyupo/xxx` 是完整的文件路径，就这么写，替换成你的文件仓库地址路径就行

下载 gbg ，输入 air，开始开发业务即可。

