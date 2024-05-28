# 《go-cookbook》windows 版

## 一、安装最新版 golang

### 1、卸载本机目前安装的 golang

打开 “控制面板” ，点击 “卸载程序” ，找到 `Go Programming Language xxxx`（定位 `Go Programming Language` 就行，xxx 因为版本不一致可能不一样），点击，卸载。

_注：推荐卸载完成后重启计算机，保证安装时系统的旧版本 golang 被彻底清洁。_

### 2、下载 golang 最新版本安装包

#### 2-1 确定操作系统位数（或系统类型）

在电脑桌面上，找到“此电脑”（或“计算机”、“我的电脑”等等），右键 -> 属性，查看电脑系统的位数。

在 win10 系统中，系统位数通常在 “设备规格” -> “系统类型” 后面，`64 位操作系统, 基于 x64 的处理器` 就代表操作系统是 64 位的。

#### 2-2 下载对应系统位数的 golang 安装包

在 go 的 [官方网站](https://go.dev/) 上，点击 Download 按钮，在 [下载页面](https://go.dev/dl/) 中选择下载包。

_如果你是 32 位系统，就下载 `gox.x.x.windows-386.msi` (x.x.x 代表 golang 版本号)，如果你是 64 位系统，就下载 `gox.x.x.windows-amd64.msi` (x.x.x 代表 golang 版本号)。_

### 3、安装 golang 至系统

点击运行下载的 _go 安装包_，选择你想要的安装目录（默认在 C:\Go\，作者选择安装在 D:\Go\）,一路点击 Next ，等待安装进度完成后，点击 _Finish_ 关闭安装窗口，即可完成安装。

打开 `Windows PowerShell`，输入 `go version`。如果出现和你下载的版本、系统位数一致的信息，则表明最新版 go 安装成功。

_注：在我的系统下，输入 `go version` 后，出现 `go version go1.22.3 windows/amd64`，与我下载的 `go1.22.3.windows-amd64.msi` 的 版本号、系统位数 都一致，表明我的 go 已经更新到最新版本了。_

---

**特别注意：文档编写日期为：2024-05-28，go 的最新版本为 1.22.3。读者需自行到 [go 官方网站](https://go.dev/) 找到 go 的最新版本下载，不要被文档中写的版本误导！！！**
