# 《go-cookbook》

Go 安装完成后，打开 `Windows PowerShell` ，输入 `go env -w GO111MODULE=on` 打开 go modules （go modules 是 GO 的包管理工具，设置为 on，以后不论在哪儿创建项目，都会使用项目目录中的 go.mod 来管理依赖，开就对了。）

然后关闭 `Windows PowerShell` 再打开，输入 `go env GO111MODULE`，返回 on ，证明设置正确。

找到 `GOPATH` 这个配置，复制等号后面的内容，粘贴到任意文件夹的导航栏中，回车，即进入了 Go 的工作空间（workspace）。

一般来说，GOPATH 指向的工作空间包含以下几个目录：

    src：存放 Go 源代码文件，代码按照包名组织成目录结构。

    bin：存放编译后的可执行文件（可运行的二进制文件，在 windows 中是 .exe 文件）。

    pkg：存放包归档文件（理解成全局的 node_modules 就行）。
