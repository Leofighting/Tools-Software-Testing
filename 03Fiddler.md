### `Fillder` 简介

> 是位于客户端和服务器端的 HTTP 代理；目前最常用的抓包工具之一
>
> - 管控浏览器所有的`THHP/HTTPS`流量
> - 查看、分析请求内容细节
> - 测试网站的性能
> - 解密`HTTPS` 的 web 会话
> - 全局、局部断点功能
> - 第三方插件

> 使用场景：
>
> - 接口调试、接口测试、线上环境调试、web性能分析
>
> - 判断前后端bug、开发环境 hosts 配置、mock、弱网断网测试



### `B/S`架构

> 编写程序部署到 web 服务器
>
> web 服务器运行在服务器上，绑定 `IP` 地址并监听某端口，接受和处理 HTTP 请求
>
> 客户端通过 HTTP 协议获取服务器上的网页、文档等资源
>
> ![image-20200330200734749](E:\测试\测试工具\images\Fillder\01.png)



### `HTTP`

> 超文本传输协议
>
> 用于从万维网服务器传输超文本到本地浏览器的传输协议
>
> 是基于TCP 的应用层的协议，它不关心数据传输的细节，主要是用来规定客户端和服务端的数据传输格式，最初是用来向客户端传输`HTML` 页面的内容，默认端口是 80
>
> 是基于请求与响应模式的、无状态的、应用层的协议



### 请求报文

> 主要由请求行、请求头部、空一行、请求正文（请求体，可能会没有）组成
>
> ![image-20200330204433930](E:\测试\测试工具\images\Fillder\02.png)

### `URL`

> 统一资源定位符；用于描述网上的资源
>
> 格式：schema://host[:post#]/path/.../[?query-string]
>
> - scheme：协议，如  `http/ftp` 等
> - host：域名或`IP`地址
> - port：端口
> - path：资源路径
> - query-string：发送的参数

### 请求头

> 可自行定义
>
> ![image-20200330210155188](E:\测试\测试工具\images\Fillder\03.png)



### 响应报文

> 主要由状态行、消息报头、空一行、响应正文
>
> ![image-20200330211221098](E:\测试\测试工具\images\Fillder\04.png)

### 响应头

> ![image-20200330211823163](E:\测试\测试工具\images\Fillder\05.png)



### `Fiddler`使用

>配置端口
>
>![image-20200330215938486](E:\测试\测试工具\images\Fillder\06.png)

> 主页面介绍
>
> ![image-20200330215902165](E:\测试\测试工具\images\Fillder\07.png)

> 基础操作
>
> - 抓取请求
> - 删除请求
> - 过滤请求

> 在会话列表添加一列 `IP`列
>
> [参考链接](https://www.jianshu.com/p/b1136e90de6c)

> 辅助标签+工具
>
> 1. Statistics：统计信息，对请求的性能分析
>
> 2. Inspectors：检查器；可以多种方式查看请求的请求报文和响应报文的相关信息
>
> 3. `AutoResponder`：自动响应器；可以拦截某一请求，进行重定向到本地的资源，使用Fiddler的内置响应，自定义响应
>
>    ![image-20200331090528672](E:\测试\测试工具\images\Fillder\08.png)
>
> 4. Composer：设计请求；可以发现黑盒测试中无法识别的bug
>
> 5. Filters：过滤器；
>
> 6. 命令行设置断点：
>
>    1. 请求前：`bpu 断点所包含的内容`；例如：`bpu login`，在请求前，拦截包含`login` 字符串的数据包；取消断点，再次输入 `bpu`
>    2. 请求后：`bpafter 断点所包含的内容`；例如`bpafter login`，在响应后，拦截包含`login` 字符串的数据包；取消断点，再次输入 `bpu`
>
> 7. 弱网测试：
>
>    1. 设置：Rules -- Performance--Simulate Modem Speeds 要勾选
>
>    2. 时间控制：Rules -- Customize Rules -- 修改时间参数
>
>       ![image-20200331100046840](E:\测试\测试工具\images\Fillder\09.png)

> 设置 Fiddler 捕获 `HTTPS` 流量
>
> ![image-20200331103009342](E:\测试\测试工具\images\Fillder\10.png)

> `iOS` 设备配置方法
>
> ![image-20200331110333866](E:\测试\测试工具\images\Fillder\11.png)
>
> ![image-20200331114728873](E:\测试\测试工具\images\Fillder\12.png)

> `Android`设备抓包
>
> ![image-20200331113614097](E:\测试\测试工具\images\Fillder\13.png)

