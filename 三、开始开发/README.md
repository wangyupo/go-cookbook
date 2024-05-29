1、创建如下目录结构

```
GOPATH/
    src/
        github.com/
              wangyupo/
                  ginStart
```

2、用 GoLand 打开 `ginStart` 文件夹（ginStart 代表项目名，具体起什么随便，比如最入门的 curd）.

打开 GoLand 自带的 “终端” ，输入命令 `go mod init github.com/wangyupo/ginStart`，初始化项目，看到 startGin 目录下出现 go.mod 代表项目初始化成功！

```
注：
go.mod 理解成 package.json 就行，功能就是记录这个项目依赖包。

前端使用 `npm install xxx` 来安装、更新依赖，
这里使用 `go get -u <package>` 来安装依赖，
使用 `go mod tidy` 来更新依赖（如果未安装依赖，则安装依赖；如果已安装依赖，则整理 go.mod 文件，移除未使用的依赖和不再需要的指令）。
```

3、打开 [Gin 文档](https://gin-gonic.com/zh-cn/docs/quickstart/)，还是在 GoLand 自带的 “终端”，输入命令 `go get -u github.com/gin-gonic/gin` 来为本项目安装 gin。

go get 和 go install 的作用如下：

    go get -u package：用于获取和更新项目的依赖包，并相应地更新 go.mod 和 go.sum 文件。附带 -u 标志的 go get 命令则用于更新现有的依赖包到最新版本。

    go install package@version：用于安装 Go 工具或特定版本的包，通常用于命令行工具的安装，而不会修改项目的 go.mod 文件。

4、还是在 GoLand 自带的 “终端”，输入命令 `go install github.com/cosmtrek/air@latest` 安装 “热更新” 工具 [air](https://github.com/cosmtrek/air) （它可以帮助你每次做出改动后无需打包重启，加快你的开发速度）。

还是在 GoLand 自带的 “终端”，输入命令 `air init`，初始化 air 的配置文件。

5、在 ginStart 目录下新建 main.go 文件，把第一行的 `package startGin` 改为 `package main`，然后把下面的代码粘贴到下一行（代码来自 [gin 文档示例](https://gin-gonic.com/zh-cn/docs/quickstart/)）。

```
func main() {
	r := gin.Default()
	r.GET("/ping", func(c *gin.Context) {
		c.JSON(200, gin.H{
			"message": "pong",
		})
	})
	r.Run() // 监听并在 0.0.0.0:8080 上启动服务
}
```

6、还是在 GoLand 自带的 “终端”，输入命令 `air`，用浏览器打开 `localhost:8080/ping`，可以看到返回 json。修改 main.go 中的返回，Ctrl+S 保存后，air 会自动刷新，再次刷新浏览器会发现返回内容也变成你改的了。